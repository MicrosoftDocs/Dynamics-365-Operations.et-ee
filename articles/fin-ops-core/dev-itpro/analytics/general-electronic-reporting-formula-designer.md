---
title: Valemikoostaja elektroonilises aruandluses (ER)
description: See artikkel annab teavet, kuidas kasutada valemikoosturit elektroonilises aruandluses (ER).
author: kfend
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 283c882300ece460c18ffebe572238e7629f8dee
ms.sourcegitcommit: a1d14836b40cfc556f045c6a0d2b4cc71064a6af
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/14/2022
ms.locfileid: "9476797"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>Valemikoostaja elektroonilises aruandluses (ER)

[!include [banner](../includes/banner.md)]

Selles artiklis selgitatakse, kuidas kasutada elektroonilises aruandluses (ER) valemikoostajat. ER-is kindla elektroonilise dokumendi vormingu koostamisel saate kasutada valemeid andmete teisendamiseks, et vastata selle dokumendi täitmise ja vormindamise nõuetele. Need valemid sarnanevad Microsoft Exceli valemitega. Valemites toetatakse erinevat tüüpi funktsioone: tekst, kuupäev ja kellaaeg, matemaatiline, loogika, teave ja andmetüübi teisendamise funktsioonid ning samuti teised ettevõtte domeenipõhised funktsioonid.

## <a name="formula-designer-overview"></a>Valemikoostaja ülevaade

ER toetab valemikoostajat. Seega saate koostamise ajal konfigureerida avaldisi, misa saab kasutada käitamisel järgmisteks ülesanneteks.

- Muutke rakenduse andmebaasist saadud andmeid. Need peavad olema sisestud ER-i andmemudelisse, mis on kavandatud ER-vormingute andmeallikaks. (Näiteks võivad need teisendused hõlmata filtreerimist, grupeerimist ja andmetüübi konversiooni.)
- Andmete vormindamine, mis tuleb saata loodavale elektroonilisele dokumendile kindla ER-vormingu paigutuse ja tingimuste järgi. (Näiteks võidakse vormindada kooskõlas nõutava keele, kultuuri või kodeeringuga).
- Elektrooniliste dokumentide loomise protsessi juhtimine. (Näiteks saavad avaldised olenevalt andmete töötlemisest vormingu teatud elementide arvestamist lubada või keelata. Nad saavad ka katkestada dokumentide loomisprotsessi või saata lõppkasutajatele sõnumeid.)

**Valemikoostaja** lehe saate avada järgmiste tegevuste käigus.

- Andmeallika kaupade sidumine andmemudeli komponentidega.
- Andmeallika kaupade sidumine vormingu komponentidega.
- Andmeallikate osana esinevate arvutatud väljade täielik haldamine.
- Määrake kasutaja sisestusparameetritele nähtavuse ja redigeeritavuse tingimused.
- Saate määratleda kasutaja sisestusparameetrite vaikeväärtused.
- Vormingu teisenduste kujundamine.
- Vormingu komponentide lubamistingimuste määratlemine.
- Vormingu failikomponentide failinimede määratlemine.
- Protsessi juhtimise kinnituste tingimuste määratlemine.
- Protsessi juhtimise kinnituste teate tekstide määratlemine.

## <a name="data-binding"></a><a name="Binding"></a>Andmete sidumine

ER-i valemikoostajat saab kasutada määratlemaks avaldist, mis teisendab andmeid, mis saadakse andmeallikatest, nii et käitamisel saab sisestada andmeid andmete tarbijas järgmiselt.

- Rakenduse andmeallikatest ja käitamisaja parameetritest ER-i andmemudelisse
- ER-i andmemudelist ER-i vormingusse;
- Rakenduse andmeallikatest ja käitamisaja parameetritest ER-i vormingusse

Järgmisel joonisel on seda tüüpi avaldise kujundus. Selles näites ümardab avaldis tabelis Intrastat välja **Intrastat.AmountMST** väärtuse kahe kümnendkohani ja annab siis ümardatud väärtuse.

[![Andmete sidumise avaldis.](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

Järgmine joonis näitab, kuidas seda tüüpi avaldist saab kasutada. Selles näites on koostatud avaldise tulem sisestatud andmemudeli **Maksu aruandluse mudel** komponendile **Transaction.InvoicedAmount**.

[![Kasutatav andmete sidumise avaldis.](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Käitusajal ümardab koostatud valem `ROUND (Intrastat.AmountMST, 2)` välja **AmountMST** väärtuse tabeli Intrastat iga kirje puhul kahe kümnendkohani. Seejärel sisestab see ümardatud väärtuse andmemudeli **Maksu aruandlus** komponenti **Transaction.InvoicedAmount**.

## <a name="data-formatting"></a><a name="Transformation"></a>Andmete vormindamine

ER-i valemikoostajat saab kasutada määratlemaks avaldist, mis vormindab andmeid, mis saadakse andmeallikatest, nii et andmeid saab saata elektroonilise dokumendi loomise osana. Teil võib olla vorming, mida tuleb rakendada tüüpilise reeglina, mida tuleb vormingu puhul taaskasutada. Sel juhul saate seda vormingut kasutada ühe korra vormingu konfiguratsioonis nimega teisendusena, millel on vormindamisavaldis. Selle nimelise teisenduse saab siduda paljude vormingu komponentidega, mille väljund peab olema vormindatud loodud vormindamisavaldise järgi.

Järgmisel joonisel on seda tüüpi teisenduse kujundus. Selles näites kärbib teisendus **TrimmedString** andmetüübi *String* sissetulevad andmed, eemaldades algus- ja lõputühikud. Seejärel tagastab see kärbitud stringiväärtuse.

[![Teisendus.](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

Järgmine joonis näitab, kuidas seda tüüpi teisendust saab kasutada. Selles näites saadavad mitu vormingu komponenti teksti käitusajal väljundina loodavale elektroonilisele dokumendile. Kõik need vormingukomponendid viitavad teisendusele **TrimmedString** nime järgi.

[![Kasutatav teisendamine.](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Kui vormingu komponendid (näiteks komponendi **partyName** puhul eelmises näites) viitavad teisendusele **TrimmedString**, saadab teisendus teksti väljundina loodavasse elektroonilisse dokumenti. See tekst ei sisalda algus- ega lõputühikuid.

Kui teil on vorming, mida tuleb rakendada eraldi, saab selle kasutusele võtta kindla vormingu komponendi sidumise üksiku avaldisena. Järgmisel joonisel on seda tüüpi avaldis. Selles näites on vormingu komponent **partyType** seotud andmeallikaga avaldise kaudu, mis teisendab sissetulevad andmeallika andmed väljalt **Model.Company.RegistrationType** suurtäheliseks tekstiks. Seejärel saadab avaldis selle teksti väljundina elektroonilisse dokumenti.

[![Vorminduse rakendamine üksikule komponendile.](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

## <a name="process-flow-control"></a><a name="Validation"></a>Protsessi voo juhtimine

ER-i valemikoostajat saab kasutada elektrooniliste dokumentide loomise protsessivoo juhtimiseks kasutatavate avaldiste määratlemiseks. Saate teha järgmisi toiminguid.

- Määratlege tingimused, mis määravad, millal tuleb dokumendi loomise protsess peatada.
- Määrake avaldised, mis loovad kasutajale sõnumeid peatatud protsesside kohta või heidavad käivitamislogi sõnumeid aruande loomise protsessi jätkamise kohta.
- Määrake loodavate elektrooniliste dokumentide failinimed ja juhtige nende loomise tingimusi.

Iga protsessi voo juhtimise reegel on koostatud üksiku kinnitusena. Järgmisel joonisel on seda tüüpi kinnitus. Siin on selles näites oleva konfiguratsiooni selgitus.

- Kinnitamist hinnatakse, kui XML-faili loomisel luuakse **INSTAT**-sõlm.
- Kui kannete loend on tühi, lõpetab kinnitamine käivitamisprotsessi ja tagastab väärtuse **FALSE**.
- Kinnitamine annab tõrketeate, mis sisaldab SYS70894 teksti kasutaja eelistatud keeles.

[![Kinnitamine.](./media/picture-validation.jpg)](./media/picture-validation.jpg)

ER-i valemikoostajat saab kasutada ka faili nime loomiseks loodavale elektroonilisele dokumendile ja faili loomise protsessi juhtimiseks. Järgmisel joonisel on seda tüüpi protsessi voo juhtimise kujundus. Siin on selles näites oleva konfiguratsiooni selgitus.

- Andmeallika **model.Intrastat** kirjete loend on jagatud partiideks. Iga partii sisaldab 1000 kirjet.
- Väljund loob zip-faili, mis sisaldab ühte XML-vormingus faili iga loodud partii kohta.
- Avaldis annab vastuseks failinime loodavatele elektroonilistele dokumentidele, liites faili nime ja failinime laiendi. Teise partii ja kõikide järgnevate partiide puhul sisaldab faili nimi järelliitena partii ID-d.
- Avaldis lubab (andes vatuseks väärtuse **TRUE**) faili loomise protsessi partiidele, mis sisaldavad vähemalt ühte kirjet.

[![Protsessi voo juhtimine.](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

## <a name="document-content-control"></a><a name="Enabled"></a>Dokumendi sisu juhtelement

ER-valemi koostajaga saab seadistada väljendeid, millega valitakse, mis andmeid pannakse käitusajal loodud elektroonilistesse dokumentidesse. Väljendid võivad lubada või keelata vormingu teatud elementide väljundit vastavalt töödeldavatele andmetele ja seadistatud loogikale. Neid väljendeid saab sisestada ühes vormingus elemendi jaoks lehe **Tegevuste kujundaja** vahekaardi **Vastendamine** väljal **Lubatud**. Saate sisestada avaldisi loogika tingimusena, mis tagastab väärtuse *Kahendmuutuja*.

- Kui tingimus annab tulemuse **True**, käitatakse praegust vormingu elementi.
- Kui tingimus annab tulemuse **False**, jäetakse praegune vormingu element vahele.

Järgmisel joonisel on näidatud seda tüüpi avaldised. (Näitena on kasutatud Microsofti pakutavat **ISO20022 krediidiedastuse (NO)** versiooni 11.12.11 vormingu seadistust). **XMLHeader** vormingu komponent on konfigureeritud kirjeldama krediidi edastamise sõnumi ülesehitust vastavalt ISO 20022 XML sõnumi standarditele. Vormingu komponent **XMLHeader/Document/CstmrCdtTrfInitn/PmtInf/CdtTrfTxInf/RmtInf/Ustrd** on konfigureeritud lisama XML elemendi **Ustrd** loodud sõnumile ja panema rahaülekande teabe struktureerimata vormingus järgmiste XML elementide tekstina.

- Komponenti **PaymentNotes** kasutatakse maksemärkmete teksti loomiseks.
- Komponent **DelimitedSequence** loob komaga eraldatud arve numbreid, mida kasutatakse praeguse krediidiedastuse tasakaalustamiseks.

[![Komponendid PaymentNotes ja DelimitedSequence.](./media/GER-FormulaEditor-ControlContent-1.png)](./media/GER-FormulaEditor-ControlContent-1.png)

> [!NOTE]
> Komponendid **PaymentNotes** ja **DelimitedSequence** sildistatakse küsimärki kasutades. Küsimärk näitab, et komponendi kasutamine on tingimuslik. Sellisel juhul põhineb komponentide kasutamine järgmistel kriteeriumitel.
>
> - Väljend `@.PaymentsNotes <> ""`, mis on määratletud komponendi **PaymentNotes** võimaldab (annab tulemuse **TRUE**) XML elemendi **Ustrd** täitmist maksemärkmete tekstiga, kui see tekst pole praeguse krediidiedastuse jaoks tühi.
>
>    [![Komponendi PaymentNotes avaldis.](./media/GER-FormulaEditor-ControlContent-2.png)](./media/GER-FormulaEditor-ControlContent-2.png)
>
> - Avaldis `@.PaymentsNotes = ""`, mis määratletakse komponendi **DelimitedSequence** jaoks, võimaldab (annab tulemuse **TRUE**) XML elemendi **Ustrd** täitmist komaga eraldatud arve numbrite loendiga, mida kasutatakse praeguse krediidiedastuse arveldamiseks, kui selle krediidiedastuse maksemärkmete tekst on tühi.
>
>    [![Komponendi DelimitedSequence avaldis.](./media/GER-FormulaEditor-ControlContent-3.png)](./media/GER-FormulaEditor-ControlContent-3.png)
> 
> Vastavalt sellele seadistusele sisaldab iga deeboitori makse (XML-elemendi **Ustrd**) jaoks loodud sõnum kas maksemärkmete teksti või sellise teksti puudumisel komaga eraldatud arve numbreid, mida kasutatakse makse arveldamiseks.

## <a name="assistance-in-formulas-writing"></a>Abi valemite kirjutamisel

### <a name="data-sources-navigator"></a>Andmeallikate navigeerija

Saate muuta valemit, mis esindab struktureeritud andmeallika elementi. Kui konfigureerisite ER-parameetrid [...](relative-path-data-bindings-er-models-format.md), et esitada tee struktureeritud andmeallika elemendile suhtelise teena, näidatakse valemis märki "at" (@) [kasutatava](er-formula-language.md#relative-path) hierarhilise puustruktuuri absoluutse tee ülejäänud osa asemel. See absoluutne tee ülejäänud osa on suunatud redigeeritava tee emaelemendile. Finantsversiooni 10.0.30 ja hilisemate kuupäevade kujundaja lehel Andmeallikate paanil saate valida suvandi Mine kohta @**, et asetada andmeallikate puu kursor elemendile,** mis **on** **redigeeritava** elemendi ema.**·** Kõigi ahendatud kasvavate elementide struktuur laiendatakse vajadusel automaatselt ja rekursiivselt. See laiendus aitab teil kiiresti visualiseerida redigeeritava põhielementi, jälgida andmeallikate puus redigeeritava elemendi vendi ja kasutada kõiki neid vajadusel redigeeritavas valemis.

![Kasutage suvandit Mine @, et asetada andmeallikate puu kursor elemendi juurde, mis on redigeeritava elemendi ema valemikujundaja lehel.](./media/er_formula-designer-data-sources-navigator.gif)

### <a name="data-sources-picker"></a>Andmeallikate valija

**Valige valemikoosturi** lehel **vasakul** andmeallikate paanil üks andmeallika element, mille soovite toimetatavasse valemisse tuua. Seejärel valige **suvand Lisa andmeallikas**. Pange tähele, et valitud element lisatakse redigeeritava valemi tekstile.

> [!TIP]
> Kui kasutate vaikevalemiredaktoris **valikut** Lisa andmeallikat, lisatakse valitud element alati valemiteksti lõppu. Kui teete seda sama täpsemas [valemiredaktoris](er-advanced-formula-editor.md), lisatakse valitud element valemitekstile kursori praeguses asukohas.

### <a name="built-in-functions-picker"></a>Integreeritud funktsioonide valija

Valige valemi **kujundaja** lehe parempoolsel **paanil** Funktsioonid ER-i sisseehitatud funktsioon, mille soovite lisada redigeeritavasse valemisse. Seejärel valige lisa **funktsioon**. Pange tähele, et valitud funktsioon lisatakse redigeeritava valemi tekstile.

> [!TIP]
> Kui kasutate vaikevalemiredaktoris **funktsiooni** Lisa funktsioon, lisatakse valitud funktsioon alati valemi teksti lõppu. Kui teete seda sama täpsemas [valemiredaktoris](er-advanced-formula-editor.md), lisatakse valitud funktsioon valemitekstile kursori praeguses asukohas.

### <a name="validation-of-configured-formulas"></a><a name="TestFormula"></a>Konfigureeritud valemite valideerimine

Lehel **Valemi kujundaja** valige suvand **Katse**, et valideerida konfigureeritud valemi töötamisviis.

[![Valemi valideerimiseks suvandi Katse valimine.](./media/ER-FormulaTest-Start.png)](./media/ER-FormulaTest-Start.png)

Kui nõutavad on valemi argumentide väärtused, saate avada dialoogiboksi **Testavaldis** lehelt **Valemikoostaja**. Enamikul juhtudel tuleb need argumendid käsitsi määratleda, kuna konfigureeritud sidumisi kujundamise ajal ei käitata. Vahekaart **Katsetulemus** lehel **Valemi kujundaja** näitab konfigureeritud valemi käivitamise tulemust.

Järgmine näide näitab, kuidas saate testida väliskaubanduse domeeni jaoks konfigureeritud valemit veendumaks, et Intrastati kaubakood sisaldaks ainult numbreid.

Selle valemi testimisel saate kasutada dialoogiboksi **Testavaldis**, et määrata testimiseks Intrastati kaubakoodi väärtus.

[![Testimiseks Intrastati kaubakoodi määramine.](./media/ER-FormulaTest-Start-EnterArguments.png)](./media/ER-FormulaTest-Start-EnterArguments.png)

Pärast seda, kui määrate Intrastati kaubakoodi ja valite **OK**, kuvatakse vahekaardil **Katsetulemus** lehel **Valemi koostaja** konfigureeritud valemi käivitamise tulemus. Seejärel saate hinnata, kas tulemus on vastuvõetav. Kui tulemus ei ole vastuvõetav, saate valemit värskendada ja seda uuesti katsetada.

[![Katsetulemus.](./media/ER-FormulaTest-Result.png)](./media/ER-FormulaTest-Result.png)

Osasid valemeid ei saa kujundamise ajal testida. Näiteks võib valem tagastada andmetüübi tulemuse, mida ei saa vahekaardil **Katsetulemus** kuvada. Sellisel juhul kuvatakse tõrketeade, mis teatab, et valemit ei saa katsetada.

[![Tõrketeade.](./media/ER-FormulaTest-Error.png)](./media/ER-FormulaTest-Error.png)

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)
- [Elektroonilise aruandluse valemi keel](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
