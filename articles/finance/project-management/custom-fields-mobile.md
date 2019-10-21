---
title: Kohandatud väljade juurutamine mobiilirakenduses Microsoft Dynamics 365 Project Timesheet iOS-is ja Androidis
description: Selles teemas on toodud üldised mustrid laienduste kasutamiseks kohandatud väljade juurutamiseks.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 4343c875da05641c57b7784bf52f1c814dd26d20
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174827"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Kohandatud väljade juurutamine mobiilirakenduses Microsoft Dynamics 365 Project Timesheet iOS-is ja Androidis

[!include [banner](../includes/banner.md)]

Selles teemas on toodud üldised mustrid laienduste kasutamiseks kohandatud väljade juurutamiseks. Hõlmab järgmisi teemasid.

- Mitmesugused andmetüübid, mida kohandatud välja raamistik toetab
- Kirjutuskaitstud või redigeeritavate väljade kuvamine ajatabeli kannetel ja kasutaja esitatud väärtuste salvestamine andmebaasi
- Kirjutuskaitstud väljade kuvamine ajatabeli päises
- Kohandatud äriloogika integreerimine vaikeväärtuste sisestamiseks väljadesse ja lisakinnituse tegemiseks

## <a name="audience"></a>Sihtrühm

See teema on mõeldud arendajatele, kes integreerivad kohandatud välju mobiilirakendusse Microsoft Dynamics 365 Project Timesheet, mis on saadaval Apple iOS-is ja Google Androidis. Eelduseks on, et lugejad on tuttavad X++ arendusega ja projekti ajatabeli funktsiooniga.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Andmeleping – klass TSTimesheetCustomField X++

Klass **TSTimesheetCustomField** X++ andmelepingu klass, mis esitavad teavet ajatabeli funktsiooni kohandatud välja kohta. Kohandatud välja objektide loendid edastatakse nii andmelepingusse TSTimesheetDetails kui ka andmelepingusse TSTimesheetEntry, et kuvada kohandatud väljad mobiilirakenduses.

- **TSTimesheetDetails** – ajatabeli päise leping.
- **TSTimesheetEntry** – ajatabeli kande leping. Nende objektide grupid, millel sama projekti teave ja väärtus **timesheetLineRecId** moodustab rea.

### <a name="fieldbasetype-types"></a>fieldBaseType (tüübid)

Atribuut **FieldBaseType** objektis **TsTimesheetCustom** määrab rakenduses kuvatava välja tüübi. Järgmisi suvandi **Tüübid** väärtusi toetatakse.

| Tüübi väärtus | Tüüp              | Märkmed |
|-------------|-------------------|-------|
| 0           | String (ja loetelu) | Väli kuvatakse tekstiväljana. |
| 1           | Täisarv           | Väärtus kuvatakse numbrina ilma komakohtadeta. |
| 2           | Tegelik              | Väärtus kuvatakse numbrina koos komakohtadega.<p>Tegeliku väärtuse kuvamiseks rakenduses valuutana kasutage atribuuti **fieldExtenededType**. Saate kasutada atribuuti **numberOfDecimals** kuvatavate komakohtade arvu määramiseks.</p> |
| 3           | Kuupäev              | Kuupäevavormingud määrab kasutaja säte **Kuupäeva, kellaaja ja numbri vorming**, mis on määratud valikuga **Keele ja riigi/regiooni eelistused** jaotises **Kasutaja suvandid**. |
| 4           | Kahendmuutuja           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Kui atribuuti **stringOptions** pole objektis **TSTimesheetCustomField**, esitatakse kasutajale vabas vormis teksti väli.

    Atribuuti **stringLength** saab kasutada kasutaja sisestatava stringi maksimaalse pikkuse määramiseks.

- Kui atribuuti **stringOptions** pole objektis **TSTimesheetCustomField**, on need loendi elemendid ainsad väärtused, mida kasutajad saavad suvandi nuppudega (raadionuppudega) valida.

    Sellisel juhul võib stringiväli toimida loetelu väärtusena kasutaja kirje jaoks. Väärtuse salvestamiseks andmebaasi loeteluna vastendage enne andmebaasi salvestamist stringiväärtus käsitsi loetelu väärtusega, kasutades käsuliini (vt näidet allpool selle teema jaotises „Käsuliini kasutamine klassil TSTimesheetEntryService ajatabeli kande salvestamiseks rakendusest tagasi andmebaasi”).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Seda atribuuti saate kasutada tegelike väärtuste vormindamiseks valuutana. See lähenemine on rakendatav ainult siis, kui väärtus **fieldBaseType** on **Tegelik**.

- **TSCustomFieldExtendedType:None** – vormindamist ei rakendata.
- **TSCustomFieldExtendedType::Valuuta** – väärtus vormindatakse valuutana.

    Kui valuuta vormindamine on aktiivne, saab välja **stringValue** kasutada valuutakoodi edastamiseks, mis tuleb rakenduses kuvada. Väärtus on kirjutuskaitstud väärtus.

    Väli **realValue** sisaldab rahasummat, mis tuleb andmebaasi salvestada.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Saate kasutada seda atribuuti, et määrata, kus peaks kohandatud väli rakenduses ilmuma.

- **TSCustomFieldSection::Päis** – väli kuvatakse rakenduses jaotises **Kuva rohkem üksikasju**. Need väljad on alati kirjutuskaitstud.
- **TSCustomFieldSection::Rida** – väli kuvatakse kõikide valmis reaväljade järel ajatabeli kannetes. Need väljad võivad olla redigeeritavad või kirjutuskaitstud.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

See atribuut tuvastab välja, kui rakenduse esitatud väärtused salvestatakse tagasi andmebaasi.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

See atribuut tuvastab välja, kui rakenduse esitatud väärtused salvestatakse tagasi andmebaasi.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Määrake see atribuut väärtusele **Jah**, et määrata, kas välja ajatabeli kande jaotises saavad kasutajad redigeerida. Määrake atribuudi väärtuseks **Ei**, et muuta väli kirjutuskaitstuks.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Määrake see atribuut väärtusele **Jah**, et määrata, kas väli ajatabeli kande jaotises peaks olema kohustuslik.

### <a name="label-str"></a>label (str)

See atribuut määrab sildi, mis kuvatakse rakenduses välja kõrval.

### <a name="stringoptions-list-of-strings"></a>stringOptions (List of Strings)

See atribuut on rakendatav ainult siis, kui **fieldBaseType** on seatud väärtusele **String**. Kui määratud on **stringOptions**, määratakse loendis olevate stringidega määratud suvandi nuppudega (raadionuppudega) valitavad stringiväärtused. Kui ühtegi stringi pole olemas, lubatakse stringiväljas vabas vormis teksti kanne (vt näidet allpool selle teema jaotises „„Käsuliini kasutamine klassil TSTimesheetEntryService ajatabeli kande salvestamiseks rakendusest tagasi andmebaasi”).

### <a name="stringlength-int"></a>stringLength (int)

See atribuut määrab stringivälja maksimaalse pikkuse. See on rakendatav ainult siis, kui **fieldBaseType** on seatud väärtusele **String**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

See atribuut määrab komakohtade arvu, mida tegeliku välja kohta näidatakse. See on rakendatav ainult siis, kui **fieldBaseType** on seatud väärtusele **Tegelik**.

### <a name="ordersequence-int"></a>orderSequence (int)

See atribuut reguleerib järjekorda, milles kohandatud välju rakenduses kuvatakse, kui määratud on rohkem kui üks kohandatud väli. Pikemate arvudega väljad kuvatakse enne.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Tüübi **Boolean** väljade jaoks saadab see atribuut välja Booleani väärtust serveri ja rakenduse vahel.

### <a name="guidvalue-guid"></a>guidValue (guid)

Tüübi **GUID** väljade jaoks saadab see atribuut välja globaalse ainuidentifikaatori (GUID) väärtust serveri ja rakenduse vahel.

### <a name="int64value-int64"></a>int64Value (int64)

Tüübi **Int64** väljade jaoks saadab see atribuut välja int64 väärtust serveri ja rakenduse vahel.

### <a name="intvalue-int"></a>intValue (int)

Tüübi **Int** väljade jaoks saadab see atribuut välja int väärtust serveri ja rakenduse vahel.

### <a name="realvalue-real"></a>realValue (real)

Tüübi **Tegelik** väljade jaoks saadab see atribuut välja tegelikku väärtust serveri ja rakenduse vahel.

### <a name="stringvalue-str"></a>stringValue (str)

Tüübi **String** väljade jaoks saadab see atribuut välja stringi väärtust serveri ja rakenduse vahel. Seda kasutatakse ka tüübi **Tegelik** väljade jaoks, mis on vormindatud valuutana. Nende väljade jaoks kasutatakse atribuuti valuutakoodi saatmiseks rakendusse.

### <a name="datevalue-date"></a>dateValue (date)

Tüübi **Kuupäev** väljade jaoks saadab see atribuut välja kuupäeva väärtust serveri ja rakenduse vahel.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Kohandatud välja kuvamine ja salvestamine ajatabeli kande jaotises

All on mobiilirakenduse kuvatõmmis ajatabeli kande loomisest. See näitab valmis välju ja kohandatud välja suvandi Ajakirje jaotises Kontrollstring, mille loetelu väärtus Teine suvand on juba määratud.

![Kontrollstringi kohandatud väli rakenduses](media/timesheet-entry.jpg)



All on mobiilirakenduse kuvatõmmis, kus kasutaja valib ühe loetelu suvandi, mis on saadaval kohandatud välja Kontrollstring jaoks.  Need kaks suvandit, Esimene suvand ja Teine suvand, kuvatakse raadionuppudena. Praegu on valitud teine suvand.

![Kontrollstringi kohandatud välja suvandi nupud (raadionupud)](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Tabeli TSTimesheetLine laiendamine, nii et sellel on kohandatud väli

Tavalises stsenaariumis on tõenäoline, et ajatabeli kande jaotise kohandatud välja andmed salvestatakse tabelisse TSTimesheetLine. Kuid muid tabeleid saab kasutada, kui andmeid saab võtta olemasoleva kirje TSTimesheetTrans põhjal või kui sellel pole konkreetset kirje konteksti (nt kui väli on projekti parameetrites määratud kirjutuskaitstuks).

Pange tähele, et kohandatud väljadel ei pea olema toetavaid andmebaasikirjeid. Neid saab dünaamiliselt luua X++ loogika põhjal. See lähenemine võib olla kasulik kirjutuskaitstud stsenaariumide korral (näidet dünaamiliselt loodud kohandatud välja väärtuste kohta vaadake jaotisest „Käsuliini kasutamine klassil TSTimesheetDetails, meetod buildCustomFieldListForHeader ajatabeli üksikasjade täitmiseks”).

All on kuvatõmmis rakendusobjektide puu rakendusest Visual Studio. See kuvab tabeli TSTimesheetLine laienduse, kuhu on kohandatud väljana lisatud väli TestLineString.

![Reastring](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Käsuliini kasutamine klassi TSTimesheetSettings meetodil buildCustomFieldList välja kuvamiseks ajatabeli kande jaotises

See kood reguleerib välja kuvasätteid rakenduses. Näiteks reguleerib see välja tüüpi, silti, seda, kas väli on kohustuslik, ja millises jaotises väli ilmub.

Järgmises näites on näha stringiväli ajakirjetel. Sellel väljal on kaks suvandit, **Esimene suvand** ja **Teine suvand**, mis on saadaval suvandi nuppude (raadionuppude) kaudu. Väli rakenduses on seotud väljaga **TestLineString**, mis lisatakse tabelile TSTimesheetLine.

Pange tähele, et kasutatud on meetodit **TSTimesheetCustomField::newFromMetatdata()** kohandatud välja atribuutide lähtestamise lihtsustamiseks: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** ja **numberOfDecimals**. Saate neid parameetreid ka eelistuste järgi käsitsi seadistada.

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Käsuliini kasutamine klassi TSTimesheetEntry meetodil buildCustomFieldListForEntry väärtuste sisestamiseks ajatabeli kandesse

Meetodit **buildCustomFieldListForEntry** kasutatakse väärtuste sisestamiseks salvestatud ajatabeli ridadele mobiilirakenduses. See kasutab kirjet TSTimesheetTrans parameetrina. Välju sellest kirjest saab kasutada kohandatud välja väärtuse täitmiseks rakenduses.

```
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Käsuliini kasutamine klassil TSTimesheetEntryService ajatabeli kande salvestamiseks rakendusest tagasi andmebaasi

Kohandatud välja salvestamiseks tagasi andmebaasi tavakasutuse korral peate laiendama mitut meetodit.

- Meetodit **timesheetLineNeedsUpdating** kasutatakse määramaks, kas kasutaja on rakenduses rea kirjet muutnud ja kas see tuleb andmebaasi salvestada. Kui jõudlus pole probleem, saab seda meetodit lihtsustada, et see annaks alati tulemuseks **tõene**.
- Meetodeid **populateTimesheetLineFromEntryDuringCreate** ja **populateTimesheetLineFromEntryDuringUpdate** saab laiendada, nii et need sisestavad väärtused andmebaasikirjesse TSTimesheetLine olemasolevast andmelepingu kirjest TSTimesheetEntry. Järgnevas näites pange tähele, kuidas on X++ koodiga tehtud vastendamine andmebaasi välja ja kandevälja vahel.
- Meetodit **populateTimesheetWeekFromEntry** saab laiendada ka siis, kui objektiga **TSTimesheetEntry** vastendatud kohandatud väli peab värskendama andmebaasi tabelit TSTimesheetLineweek.

> [!NOTE]
> Järgmises näites salvestatakse kasutaja valitud väärtus **firstOption** või **secondOption** andmebaasi toorstringi väärtusena. Kui andmebaasi väli on tüüp **Loetelu**, saan neid väärtusi käsitsi vastendada loetelu väärtusega ja seejärel salvestada need loetelu välja andmebaasi tabelis.

```
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Kohandatud välja kuvamine ajatabeli päise jaotises

All on mobiilirakenduse kuvatõmmis ajatabelit vaatavast kasutajast. Ülevalt paremast nurgast on valitud nupp Lisateave, mis kuvab suvandi Kuva rohkem üksikasju.  

![Käsk Kuva rohkem üksikasju](media/show-more.png)



All on mobiilirakenduse kuvatõmmis ajatabeli jaotisest Rohkem. Ajatabeli päise jaotisesse on lisatud kohandatud väli nimega Selle ajatabeli tulususmäär (arvutatud kohandatud väli). Kohandatud väljale on määratud kirjutuskaitstud väärtus 0,667.

![Jaotis Rohkem](media/more-section.jpg)



### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Tabeli TSTimesheetTable laiendamine, nii et sellel on kohandatud väli

Tavalises stsenaariumis on tõenäoline, et päise jaotise kohandatud välja andmed võetakse tabelist TSTimesheetLine. Kuid muid tabeleid saab kasutada, kui andmeid saab võtta olemasoleva kirje TSTimesheetTable põhjal või kui sellel pole konkreetset kirje konteksti (nt kui väli on projekti parameetrites määratud kirjutuskaitstuks).

Pange tähele, et kohandatud väljadel ei pea olema toetavaid andmebaasikirjeid. Neid saab dünaamiliselt luua X++ loogika põhjal. Järgmises näites on näha see lähenemine.

Päise jaotises olevad väljad on rakenduses alati kirjutuskaitstud.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Käsuliini kasutamine klassi TSTimesheetSettings meetodil buildCustomFieldList välja kuvamiseks päise jaotises

See kood reguleerib välja kuvasätteid rakenduses. Näiteks reguleerib see välja tüüpi, silti, seda, kas väli on kohustuslik, ja millises jaotises väli ilmub.

Järgmises näites on näha arvutatud väärtus rakenduse päise jaotises.

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Käsuliini kasutamine klassi TSTimesheetDetails meetodil buildCustomFieldListForHeader ajatabeli üksikasjade täitmiseks

Meetodit **buildCustomFieldListForHeader** kasutatakse ajatabeli päise üksikasjade sisestamiseks salvestatud ajatabeli ridadele mobiilirakenduses. See kasutab kirjet TSTimesheetTable parameetrina. Välju sellest kirjest saab kasutada kohandatud välja väärtuse täitmiseks rakenduses. Järgmises näites ei loeta andmebaasist ühtki väärtust. Selle asemel kasutab see X++ loogikat arvutatud väärtuse loomiseks, mis kuvatakse seejärel rakenduses.


```
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Muud konfigureeritavuse/laiendatavuse võimalused

### <a name="adding-additional-validation-for-the-app"></a>Lisakinnituse lisamine rakendusele

Ajatabeli funktsiooni olemasolev loogika andmebaasi tasemel töötab endiselt ootuspäraselt. Salvestamise või esitamise toimingu lõpetamise katkestamiseks ja konkreetse tõrketeate kuvamiseks saate lisada koodile käsuliini laienduse kaudu suvandi **kuvatakse tõrge (teade kasutajale)**. Siin on kolm näidet kasulikest laiendatavatest meetoditest.

- Kui **validateWrite** tabelis TSTimesheetLine annab ajatabeli rea salvestamise ajal tulemuse **väär**, kuvatakse mobiilirakenduses tõrketeade.
- Kui **validateSubmit** tabelis TSTimesheetTable annab ajatabeli esitamise ajal rakenduses tulemuse **väär**, kuvatakse kasutajale tõrketeade.
- Käitatakse siiski loogika, mis täidab väljad (näiteks **Rea atribuut**) meetodi **insert** ajal tabelis TSTimesheetLine.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Valmis väljade peitmine ja märkimine kirjutuskaitstuteks konfiguratsiooni kaudu

Projekti parameetrites saate muuta valmis väljad mobiilirakenduses kirjutuskaitstuks või neid peita. Määrake suvandid jaotises **Mobiili ajatabelid** vahekaardil **Ajatabel** lehel **Projektihalduse ja -arvestuse parameetrid**.

![Projekti parameetrid](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Laienduste kaudu valimiseks saadaolevate tegevuste muutmine

Projekti jaoks valimiseks saadaolevad tegevused täidetakse meetoditega **getActivitiesForProject()** ja **getActivityQuery()** klassis **TsTimesheetProjectService**. Selle käitumise muutmiseks saate kasutada käsuliini, et vastendada oma äristsenaarium tegevustega, mis on valimiseks saadaval konkreetse projekti jaoks.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Projekti vaikekategooria sisestamine ajatabeli kannetele

Projekti vaikekategooria sisestamine ajatabeli kannetele toimub kolmel tasemel. Käitumise laiendamiseks ühel või kõigil tasemetel võite kasutada käsuliini soovitud tulemuse saavutamiseks. Arvutamisel kasutatakse järgmist hierarhiat:

1. Rakendus üritab võtta vaikekategooria projektiressursist. See vaikekategooria määratakse meetodites **getCurrentUserResource** ja **getDelegatedResourcesForCurrentUser** klassis **TSTimesheetSettingsService**.
2. Kui projektiressursi tasemel ei pakuta vaikekategooriat, üritab rakendus võtta seda projekti tegevusest. See vaikekategooria määratakse meetodis **getActivitiesForProject** klassis **TSTimesheetProjectService**.
3. Kui projekti tegevuse tasemel ei pakuta vaikekategooriat, võetakse vaikekategooria projekti parameetritest. See vaikekategooria määratakse meetodis **getProjectDetailsbyRule** klassis **TSTimesheetProjectService**.
