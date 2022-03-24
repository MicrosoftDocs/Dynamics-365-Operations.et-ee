---
title: ER-i andmemudelite parameetritega seotud kutsete tugi
description: See teema kirjeldab, kuidas rakendada elektroonilise aruandluse (ER) andmemudelite parameetriga esitatud kutseid.
author: NickSelin
ms.date: 03/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula, ERDataModelDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 968b0769607e9fdbed57c25b727ed44988a92913
ms.sourcegitcommit: 399d0d3f8e2ebb81b6b9d640365ebe182690bab2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/15/2022
ms.locfileid: "8419512"
---
# <a name="support-parameterized-calls-of-er-data-models"></a>ER-i andmemudelite parameetritega seotud kutsete tugi

[!include [banner](../includes/banner.md)]

Äridokumentide loomiseks konfigureerige elektroonilise aruandluse [(ER) lahendus](general-electronic-reporting.md), mis sisaldab järgmisi ER-komponente:

- **[Vorming](er-overview-components.md#format-component)** : see komponent määrab äridokumendi struktuuri.
- **Vormingu vastendamine** – see komponent kontrollib, kuidas äridokument käitusajal täidetakse.
- **[Mudeli vastendamine](er-overview-components.md#model-mapping-component)** – see komponent määrab, mida andmed rakendusest vormingu vastenduseks tõmbavad.
- **[Andmemudel](er-overview-components.md#data-model-component)** – see komponent läbib üksikute komponentide vahelise teabe.

ER-vormingu käivitamisel käivitatakse kõik vorminguelemendid, alustades juurvormingu elemendist. Iga kord, kui käitatud [vorminguelement](general-electronic-reporting.md#configuring-data-model-mappings-for-outgoing-documents) sisaldab andmeallika sidumist, käivitatakse andmeallikas eeldatavate andmete üle andmiseks ja selle kasutamiseks vorminguelemendi täitmiseks. Mudelitüübi andmeallika kutsumisel *kutsutakse* mudeli vastendus mudeli vastenduste sätete põhjal rakendusest välja tõmbamiseks.

Eelnevalt ei saanud neid mudeli vastendamise kutseid parameetereerida, et teha neid sõltuvaks käitatud vormingu loogikast. Toetati ainult järgmist andmevoogu.

<table>
<tbody>
<tr align="center">
<td>
<b>Vorming</b><br>
Vormindaelement&nbsp;<br>
&nbsp;
</td>
<td>
<i>Sidumine</i><br>
&gt;&nbsp; Taotluse&nbsp;&gt;<br>
&lt;&nbsp;väärtus&nbsp;&lt;
</td>
<td><b>Vormindamine&nbsp;</b><br>
Andmeallikas<br>
&nbsp;
</td>
<td>
<i>andmemudel&nbsp;</i><br>
&gt;&nbsp; Taotluse&nbsp;&gt;<br>
&lt;&nbsp;väärtus&nbsp;&lt;
</td>
<td>
<b>Modelmapping&nbsp;</b><br>
Andmeallikas&nbsp;<br>
&nbsp;
</td>
<td>
<i>Sidumine</i><br>
&gt;&nbsp; Taotluse&nbsp;&gt;<br>
&lt;&nbsp;väärtus&nbsp;&lt;
</td>
<td>
<b>Tabel</b><br>
Kirje<br>
Väli
</td>
</tr>
</tbody>
</table>

Versioonis 10.0.15 ja uuemates versioonides saate konfigureerida andmemudeli välju, mida saab kutsuda ainult konfigureeritud parameetrite väärtuste andmisel. Kui see väli on konfigureeritud ja kutsuda vormingu komponendist, peavad nõutavad parameetrid olema antud vormingu sidumises kutse argumentidena. Sellisel juhul saab argumentide väärtusi määrata vormingupõhiste väärtuste alusel. Seetõttu saate kasutada dünaamilist **käitusaja parametreerimist** andmemudeli kutsete jaoks, et toetada järgmist andmevoogu.

<table>
<tbody>
<tr align="center">
<td>
<b>Vorming</b><br>
Vormingelement1&nbsp;&nbsp;<br>
<br>
Vormingelement2&nbsp;&nbsp;<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Sidumine</i><br>
&gt;&nbsp; taotlus&nbsp; 1&nbsp;&gt;<br>
&lt;&nbsp; väärtus&nbsp; 1&nbsp;&lt;<br>
&gt;&nbsp; taotlus&nbsp; 2&nbsp;&gt;<br>
&lt;&nbsp; väärtus3&nbsp;&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Formatmapping&nbsp;</b><br>
Andmeallikas&nbsp;&nbsp; 1<br>
&nbsp;<br>
<b>value2=Func(väärtus1)</b><br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>andmemudel&nbsp;</i><br>
&gt;&nbsp; Väli 1&nbsp;&gt;<br>
&lt;&nbsp; väärtus&nbsp; 1&nbsp;&lt;<br>
<b>&gt;&nbsp; field2(väärtus2)&nbsp;&gt;</b><br>
&lt;&nbsp; väärtus3&nbsp;&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Modelmapping&nbsp;</b><br>
Andmeallikas&nbsp;&nbsp; 1<br>
<br>
Andmeallikas&nbsp;&nbsp; 2<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Sidumine</i><br>
&gt;&nbsp; taotlus&nbsp; 1&nbsp;&gt;<br>
&lt;&nbsp; väärtus&nbsp; 1&nbsp;&lt;<br>
&gt;&nbsp; taotlus&nbsp; 2&nbsp;&gt;<br>
&lt;&nbsp; väärtus3&nbsp;&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>tabel&nbsp; 1</b><br>
Kirje&nbsp; 1<br>
Väli&nbsp; 1<br>
<b>tabel2&nbsp;</b><br>
Kirje&nbsp; 2<br>
Väli&nbsp; 2
</td>
</tr>
</tbody>
</table>

Uue funktsiooniga saate parametriksi kutsuda mis tahes andmemudeli väljale, mille tüüp on [*·*](er-formula-supported-data-types-composite.md#record) Kirje [*või Kirje*](er-formula-supported-data-types-composite.md#record-list). Andmemudeli välja parameetrite jaoks toetatakse järgmisi andmetüüpe:

- [Loogiline](er-formula-supported-data-types-primitive.md#boolean)
- [Konteiner](er-formula-supported-data-types-composite.md#container)
- [Kuupäev](er-formula-supported-data-types-primitive.md#date)
- [DateTime](er-formula-supported-data-types-primitive.md#datetime)
- [GUID](er-formula-supported-data-types-primitive.md#guid)
- [Int64](er-formula-supported-data-types-primitive.md#int64)
- [Täisarv](er-formula-supported-data-types-primitive.md#integer)
- [Tegelik](er-formula-supported-data-types-primitive.md#real)
- [String](er-formula-supported-data-types-primitive.md#string)

Saate määrata andmemudeli välja iga parameetri, mille kohta saab argumenti esitada määratletud andmetüübi üksiku väärtusena, [*ja selliste*](er-formula-supported-data-types-composite.md#record-list) väärtuste loendi.

> [!NOTE]
> Andmemudeli välja parameetri vaikeväärtust ei toetata. Kui lisate andmemudeli väljale parameetri ja selle andmemudeli versioon on juba väljastatud ja avaldatud, [peate](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) kõik vastavad mudelivastendused ja vormingud selle mudeli uuele versioonile tagasi põhinema, sest see andmemudeli muudatus ei ühildu tagasi.

Saate konfigureerida parametriseeritud andmemudeli väljad, et teha mudeli vastendamise kutsed vormingupõhiseks. See lähenemine aitab teil vähendada mudeli vastenduste arvu, mida tuleb konfigureerida ühe andmemudeli mitme vormingu jaoks. Saate kasutada seda lähenemist ka oma vormingute täitmisjõudluse parandamiseks ja äridokumentide loomiseks kuluv aja vähendamiseks. Lisateabe saamiseks selle funktsiooni kohta läbige siinse teema näide.

## <a name="example-use-parameterized-calls-of-er-data-models"></a>Näide: kasutage ER-i andmemudelite parameeteriseeritud kutseid

Järgmistes sammudes selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolliga kasutaja saab kujundada ER-i lahendust, mis sisaldab andmemudelit, mudeli vastendust ja vormingu ER-komponenti, mis on konfigureeritud kutsuma mudeli vastendust vormingust, pakkudes kutse argumenti, mille väärtus arvutati käitusajal jooksva vormingu valemi abil. 

Neid toiminguid saab teha ettevõttes **DEMF**. Koodi ei ole vaja muuta. 

Selles näites loote nõutavad ER konfiguratsioonid [näidisettevõttele](general-electronic-reporting.md#Configuration) **Litware, Inc**. Veenduge, et konfiguratsioonipakkuja **Litware, Inc.** (`http://www.litware.com`) näidisettevõttele on esitatud ER raamistikus ja et see on märgitud **aktiivseks**. Kui seda konfiguratsioonipakkujat pole loendis või **kui** see pole märgitud aktiivseks, [järgige konfiguratsioonipakkuja loomise juhiseid ja märkige see aktiivseks](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="business-scenario"></a>Äristsenaarium

Teil on ER-lahendus, mis sisaldab vormingut, mida saate käitada, et luua auditi eesmärgil elektrooniline dokument. Vorming sisaldab käibemaksukandeid, mis on seotud müügitellimuste ja ostutellimustega ning mil on nõutavad üksikasjad, nt kande kuupäev ja maksuväärtus. Uue rahandusaasta jooksul on selle dokumendi struktuur muutunud. Nüüd peate esitama laiendatud dokumendi, mis sisaldab kõigi nende osapoolte (klientide ja hankijate) täiendavaid üksikasju (nimesid), kelle kanded on loodud aruannetes esitatud. Seetõttu peate muutma ER-i lahendust nii, et see loob sellele uuele nõudele vastavad dokumendid.

### <a name="configure-the-er-framework"></a>ER-raamistiku konfigureerimine

Minimaalsete [ER-i parameetrite konfigureerimine](er-quick-start2-customize-report.md#ConfigureFramework), mis on vajalikud ER-i raamistiku kasutamiseks. Enne ER-raamistiku kasutamist uue ER-lahenduse loomiseks peate selle häälestuse lõpule viima.

### <a name="design-a-domain-specific-data-model"></a>Domeenipõhise andmemudeli kujundamine

Peate looma uue ER-i konfiguratsiooni, mis sisaldab nõutavat andmemudeli komponenti. Seda andmemudelit kasutatakse andmeallikana hiljem, kui kujundate auditi aruande loomiseks ER-vormingu.

Järgige neid samme, et importida nõutud andmemudel Microsofti antud XML-failist.

1. Laadige alla [fail Näidisaudit model.version.1.xml](https://download.microsoft.com/download/7/1/9/719b0132-fed7-4c73-8afa-90cac29c2fee/Sample-audit-model.version.1.xml) ja salvestage see kohalikku arvutisse.
2. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
3. Valige tööruumis **Elektrooniline aruandlus** suvand **Aruandluse konfiguratsioonid**.
4. Valige tegevuspaanil **Konfiguratsioonide** leht suvand **Vahetuslaadimine** \> **XML-failist.**
5. Valige **sirvimine** ning seejärel otsige ja valige fail **Näidisauditi mudel.version.1.xml**.
6. Konfiguratsiooni importimiseks valige **OK**.

    ![Imporditud ER-i andmemudeli konfiguratsioon lehel Konfiguratsioonid](./media/er-data-model-parameterized-calls-imported-model.png)

Järgmine näide näitab konfigureeritud andmemudeli redigeeritavat versiooni andmemudeli **kujundaja lehel**.

![ER-andmemudeli struktuur andmemudeli kujundaja lehel.](./media/er-data-model-parameterized-calls-model1.png)

Praegu on mudel loodud kuvama ainult nõutavate üksikasjadega maksukandeid.

### <a name="design-a-model-mapping-for-the-configured-data-model"></a>Mudelivastenduse kujundamine konfigureeritud andmemudelile

Kasutajana elektroonilise aruandlusarendaja rollis peate looma uue ER-i konfiguratsiooni, mis sisaldab mudeli vastendamise komponenti näidisauditi andmemudeli jaoks. See komponent juurutab Microsofti konfigureeritud andmemudeli ja Dynamics 365 Finance on sellele rakendusele omane. Peate konfigureerima mudelivastenduse komponendi, et määrata rakenduse objektid, mida tuleb käitusajal kasutada rakenduse andmete lisamiseks konfigureeritud andmemudelisse. Selle ülesande lõpetamiseks peate aru saama, kuidas maksuäridomeeni andmestruktuuri finantsis rakendatakse.

Järgige neid samme, et importida nõutud mudelivastendus Microsofti antud XML-failist.

1. Laadige alla [näidisauditi mudeli vastendus.version.1.1.xml](https://download.microsoft.com/download/c/0/3/c03a4673-b1b1-4ef8-96d0-bf96518be6e0/Sample-audit-model-mapping.version.1.1.xml) fail ja salvestage see kohalikku arvutisse.
2. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
3. Valige tööruumis **Elektrooniline aruandlus** suvand **Aruandluse konfiguratsioonid**.
4. Valige tegevuspaanil **Konfiguratsioonide** leht suvand **Vahetuslaadimine** \> **XML-failist.**
5. Valige **sirvimine** ning seejärel otsige ja valige näidisauditi **mudeli vastendus.version.1.1.xml** fail.
6. Konfiguratsiooni importimiseks valige **OK**.

    ![Imporditud ER-mudeli vastendamise konfiguratsioon lehel Konfiguratsioonid](./media/er-data-model-parameterized-calls-imported-mapping.png)

Järgmine näide näitab konfigureeritud mudeli vastendamise redigeeritavat versiooni mudeli vastendamise **kujundaja lehel**.

![ER-mudeli vastendamise struktuur mudeli vastendamise kujundaja lehel](./media/er-data-model-parameterized-calls-mapping1.png)

Praegu on mudeli vastendamine mõeldud esitama nõutavate üksikasjadega maksukandeid. See toob selle teabe rakenduse tabelist `TaxTrans`, kasutades konfigureeritud ja `TaxTrans``TaxTransFiltered` ER-i andmeallikaid.

### <a name="design-a-new-format"></a>Uue vormingu kujundamine

Elektroonilise aruandluse funktsionaalse konsultandi rollis kasutajana peate looma uue ER-i konfiguratsiooni, mis sisaldab vormingu komponenti. Peate konfigureerima vormingu komponendi, et täita loodud aruanded maksukannetega, mis on kõigi nõutud üksikasjadega.

Järgige neid samme, et importida nõutav vorming Microsofti antud XML-failist.

1. Laadige alla [fail Auditi näidisvorming.version.1.1.xml](https://download.microsoft.com/download/e/b/7/eb7e126e-2bb3-4bbb-a735-ffd4c48920b1/Sample-audit-format.version.1.1.xml) ja salvestage see kohalikku arvutisse.
2. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
3. Valige tööruumis **Elektrooniline aruandlus** suvand **Aruandluse konfiguratsioonid**.
4. Valige tegevuspaanil **Konfiguratsioonide** leht suvand **Vahetuslaadimine** \> **XML-failist.**
5. Valige **sirvimine** ning leidke ja valige fail **Näidisauditi vorming.version.1.1.xml**.
6. Konfiguratsiooni importimiseks valige **OK**.

    ![Imporditud ER-vormingu konfiguratsioon lehel Konfiguratsioonid.](./media/er-data-model-parameterized-calls-imported-format.png)

Järgmine näide näitab vormingukujundaja lehel konfigureeritud vormingu redigeeritavat **versiooni**.

![ER-vormingu struktuur vormingukujundaja lehel.](./media/er-data-model-parameterized-calls-format1.png)

ER-vorming on konfigureeritud aruande loomiseks tekstifailina komaga eraldatud väärtuste (CSV) vormingus.

### <a name="run-the-imported-format"></a>Imporditud vormingu käivitamine

1. Valige konfiguratsioonide **lehel** auditi näidiskonfiguratsiooni **konfiguratsioon** ja seejärel valige tegevuspaanil käsk **Käivita**.
2. **Valige dialoogiboksi Elektroonilise aruande** parameetrid vahekaardil Kirjed **, mida kaasata**, suvand **Filter**.
3. Saate määrata tingimused kannete **PIV-110000004** ja **INV-10000001** kannete valimiseks.
4. Valige nupp **OK**.
5. Valige nupp **OK**.
6. Vaadake üle loodud dokument, mis sisaldab valitud kannete maksukandeid.

    ![Loodud dokumendi eelvaade koos maksukannetega.](./media/er-data-model-parameterized-calls-output1.png)

### <a name="adjust-the-imported-er-solution"></a>Imporditud ER-lahenduse kohandamine

Vastavalt uuele nõudele peab esitav dokument sisaldama nende klientide ja hankijate nimesid, kelle kanded on kaasatud. Seetõttu peate muutma imporditud ER-lahendust nii, et see loob dokumendi, mis vastab sellele uuele nõudele.

Otsustage, kuidas soovite imporditud ER-i komponentide nõutavaid muudatusi rakendada.

Lähenemisviisiks on järgmiste muudatuste juurutamine:

- Lisage andmemudelile stringi `Transaction.Party.Name` tüübi uus andmemudeli *väli*.
- Mudeli vastendamisel konfigureerige sidumine uue andmemudeli väljaga, kasutades saadaolevaid tabeliseost, `DirPartyTable``Name` et pääseda juurde rakendustabeli vastavale kirjele ja tuua välja väärtus sealt.

Kuigi see lähenemine töötab, võib see põhjustada jõudlusprobleeme SQL-andmebaasis, `TaxTrans` sest see on kandetabel ja võib seetõttu sisaldada suurt hulka kirjeid. Sellisel juhul peab kutsete arv olema `DirPartyTable` võrdne kirjete arvuga `TaxTrans` tabelis, mis võivad jõudlusprobleeme põhjustada.

Võite rakendada ka järgmisi muudatusi.

- Lisage oma andmemudelile uus `Party` juur ja uus `Party.Name` väli.
- Mudeli vastendamises lisage uus `DirPartyTable` andmeallikas, mis liitub kõigi tabeliseostes kasutatavate tabelite kirjetega, et pääseda juurde rakendustabeli vastavale kirjele alates tabelist`TaxTrans`.

Kuigi see lähenemine töötab, võib see põhjustada mälutarbimise probleeme. Isegi kui uus [JOIN-andmeallikas](er-join-data-sources.md) käivitatakse üksiku SQL-i taotlusena rakenduse andmebaasi andmebaasi jõudluse probleemide vältimiseks, tuleb tulemus tuua rakendusserveri mälusse. Kuna kirjete arv ja väljade arv nendes kirjetes on üsna suur, võib see lähenemine põhjustada väga rasket mälu tarbimist. Võib ilmneda ka mälust väljas käitusaja erand.

Saate juurutada muudatused, kui jooksev vorming kogub mälus kliendi ja hankija kordumatuid ID-koode kõigile maksukannetele, mis esitatakse loodud aruandes. Kuna ainult kordumatud koodid tuleb säilitada, ei ole lõplik koodide kogum piisavalt suur, et mõjutada mälu tarbimist. Koodide kogum edastatakse seejärel mudeli vastendusele mudelitüübi teise andmeallika *argumendina*. Selle kutse alusel käivitab mudeli vastendamine uue ER-i andmeallika, `DirPartyTable` mis teeb rakenduse andmebaasi jaoks ühe SQL-i taotluse tuua tabelist ainult nende osapoolte kirjed, kelle koodid on esitatud esitatud koodide komplektis.

### <a name="adjust-the-imported-data-model"></a>Imporditud andmemudeli korrigeerimine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. **Valige vasakul paanil** konfiguratsioonipuu lehel Konfiguratsioonid auditi **näidismudel**.
3. Valige kiirkaardil Versioonid versioon **2**, mille olek on **Mustand**.**[...](general-electronic-reporting.md#component-versioning)**
4. Valige kiirkaart **Konfiguratsiooni komponendid**.
5. **Valige** kujundaja, et avada andmemudel redigeerimiseks.
6. **Veenduge, et** andmemudeli lehel on väli `Root` valitud ja valige väärtus **Uus**.
7. Dialoogiakna ripploendis järgige allolevaid etappe.

    1. **Valige jaotises Uus sõlm** väljagrupina **suvand Aktiivse sõlme tütarsõlm**.
    2. Sisestage **väljale** Nimi **osapool**.
    3. Valige väljalt **Üksuse tüüp** suvand **Kirjete loend**.
    4. Uue **välja** lisamise lõpetamiseks klõpsake nuppu Lisa.

8. Kontrollige, `Root.Party` kas väli on valitud, ja seejärel valige **vahekaardil** Sõlm suvand **Parameetrid**.
9. **Dialoogiboksis Parameetrid** järgige neid samme.

    1. **Valige vahekaardil Parameetrid** suvand **Uus**.
    2. Väljale Nimi **sisestage** **PartyRefRecId**.
    3. **Väljal Tüüp** valige **Int64**.
    4. Märkige ruut **Loend**.
    5. Parameetrite **sisestamise lõpetamiseks valige OK**.

    > [!NOTE]
    > Konfigureerisite andmemudeli `Root.Party` välja just väljana, mida kutsutakse, kui Parameetris **PartyRefRecId on esitatud** väärtus. See väärtus peab olema kirjeloendis, mis sisaldab andmetüübi `Value`*Int64* välja.

    ![Parameetrite dialoogiboks.](./media/er-data-model-parameterized-calls-model2a.png)

10. Kontrollige, kas väli `Root.Party` on endiselt valitud, ja valige väärtus **Uus**.
11. Dialoogiakna ripploendis järgige allolevaid etappe.

    1. **Valige jaotises Uus sõlm** väljagrupina **suvand Aktiivse sõlme tütarsõlm**.
    2. Väljale Nimi **sisestage** **nimi**.
    3. Valige väljalt **Üksuse tüüp** suvand **String**.
    4. Uue **välja** lisamise lõpetamiseks klõpsake nuppu Lisa.

12. Valige **Salvesta** ja sulgege andmemudeli **leht**.

    ![Korrigeeritud ER-andmemudeli struktuur andmemudeli kujundaja lehel.](./media/er-data-model-parameterized-calls-model2b.png)

13. Valige versiooni **2 kiirkaardil** Versioonide olekuks **Lõpetatud** **·**\>.**·** Seejärel valige **OK**.

    > [!NOTE]
    > Teie andmemudeli muudatused **salvestatakse** **näidisauditi** mudeli andmemudeli komponendi teise revisjoni, mis asub auditi näidismudeli ER-i konfiguratsiooni teises versioonis.

![ER-i andmemudeli uuendatud konfiguratsioon lehel Konfiguratsioonid](./media/er-data-model-parameterized-calls-updated-model.png)

### <a name="adjust-the-imported-model-mapping"></a>Imporditud mudeli vastendamise kohandamine

1. Laiendage **konfiguratsioonilehe** vasakpoolse paani konfiguratsioonipuus valikut Näidisauditi **mudel**.
2. Valige **auditi** **näidismudeli** vastendamine ja seejärel valige kiirkaardil Versioonid teine vastendamisversioon, mis põhineb esimesel andmemudeli versioonil (**versioon 1.2**) **ja mille olekuks on Mustand.**
3. Valige **Aluse muutmine**.
4. Jätke sihtversiooni **väljale** näidisauditi **põhimudeli** versioon **2**.
5. Valige **OK,** et tagasi põhineda ja viia oma mudeli vastendamine viimaste andmemudeli muudatustega vastavusse.

    Pange tähele, et **teie redigeeritava mudeli vastenduse versiooninumber on muutunud versioonilt 1.2** **versiooniks 2.2**, mis näitab, et teist mudelit kasutatakse praegu alusena.

6. Valige **Kujundaja**.
7. Valige mudeli **ja andmeallika vastendamise lehel** praeguse mudeli **vastendamise** jaoks suvand Kujundaja.
8. Järgige neid samme uue andmeallika lisamiseks rakenduse tabelile `DirPartyTable` juurdepääsemiseks:

    1. Valige andmeallika **tüübi paanil** tabelikirjed **Dynamics 365 for Operations\>**.
    2. Valige paanil **Andmeallikad** suvand **Lisa juur**.
    3. Sisestage **väljale Nimi** väärtus **PartyTable**.
    4. Sisestage **tabeli** väljale **DirPartyTable**.
    5. Valige **OK**, et lõpetada uue andmeallika lisamine.

9. Järgige neid samme uue andmeallika lisamiseks kirjete taotlusele `DirPartyTable`, mis põhineb kirje ID-koodide esitatud loendis.

    1. Valige andmeallika **tüübi paanil** suvand Üldine **tühi \> konteiner**.
    2. Valige paanil **Andmeallikad** suvand **Lisa juur**.
    3. Sisestage **väljale** Nimi **andmed**.
    4. Valige **OK**, et lõpetada uue andmeallika lisamine.
    5. Valige andmeallikate **paanil** **andmeallikas**.
    6. Valige andmeallika **tüübi paanil** funktsioonid **\> arvutatud väli**.
    7. Valige andmeallikate **paanil** käsk **Lisa**.
    8. Väljale Nimi **sisestage** **DirParty**.
    9. Valige **Valemi redigeerimine**.
    10. Valige valemikoosturi **lehel** parameetrid **·**.
    11. **Dialoogiboksis Parameetrid** järgige neid samme.

        1. **Valige vahekaardil Parameetrid** suvand **Uus**.
        2. Väljale Nimi **sisestage** **DirPartyId**.
        3. **Väljal Tüüp** valige **Int64**.
        4. Märkige ruut **Loend**.
        5. Valige nupp **OK**.

        > [!NOTE]
        > Konfigureerinud selle arvutatud välja nii, et see aktsepteeriks käitusajal üksiku parameetri argumenti, mis on konfigureeritud `Value`*kirjeloendina, mille ühel väljal on Int64* tüüp.

    12. Sisestage väljale **Valem** järgmine avaldis.

        `FILTER(PartyTable, VALUEINLARGE(PartyTable.RecId, DirPartyId, DirPartyId.Value))`

        > [!NOTE]
        > Konfigureerisite äsja arvutatud välja `DirParty``DirPartyTable``DirPartyId``DirParty`, et tuua ainult kirjed, kus kirje ID-koodid on lisatud loendisse, mis on antud argumendina välja kutsumisel.

        ![Valem osapoolte nimede toomiseks rakenduse tabelist valemikoosturi lehel.](./media/er-data-model-parameterized-calls-formula1.png)

    13. Valige **Salvesta** ja sulgege leht **Valemikoostaja**.
    14. Valige **salvestamine** ja seejärel valige **OK**, et lõpetada uue andmeallika lisamine.

10. Järgige neid samme uue andmeallika sidumiseks uue andmemudeli väljaga nii, et andmemudelit kasutatakse osapoolenimede astetmiseks.

    1. Valige andmemudeli **paanil** andmemudeli `Root.Party` väli.
    2. Valige paanil **Andmemudel** suvand **Redigeeri**.
    3. Sisestage **avaldis** väljale **Valem** kujundaja lehe väärtus Valem `Data.DirParty(PartyRefRecId)`.
    4. Valige **Salvesta** ja sulgege leht **Valemikoostaja**.

        > [!NOTE]
        > Konfigureerisite just sidumise, et kutsuda konfigureeritud `Data.DirParty``Root.Party` andmeallikas ja esitada kirje ID-koodide loend, mis määratakse vormingus andmemudeli välja kutsumisel.

    5. Valige andmemudeli **paanil** andmemudeli `Root.Party.Name` väli.
    6. Valige paanil **Andmemudel** suvand **Redigeeri**.
    7. Laiendage **andmeallika paanil** valemikoosturi **lehel** valikut **Data \> DirParty ja** valige suvand **Name (Nimi**).
    8. Valige **Andmeallika lisamine**.
    9. Valige **Salvesta** ja sulgege leht **Valemikoostaja**.

    ![Korrigeeritud ER-mudeli vastendamise struktuur mudeli vastendamise kujundaja lehel.](./media/er-data-model-parameterized-calls-mapping2.png)

11. Valige **salvestamine** ja sulgege mudeli vastendamise **kujundaja** leht.
12. Sulgege leht **Mudelist andmeallikasse vastendamine**.
13. **Versiooni** 2.2 puhul valige versioonide **kiirkaardil** suvand **Muuda olekut \> Lõpetatud**. Seejärel valige **OK**.

### <a name="adjust-the-imported-format"></a>Kohandage imporditud vormingut.

1. **Lehel Konfiguratsioonid** valige auditi **näidisvorming**.
2. Valige versioonide kiirkaardil versioon 1.2 **, mille olek on Mustand** **.** **·**
3. Valige **Aluse muutmine**.
4. Jätke sihtversiooni **väljale** näidisauditi **põhimudeli** versioon **2**.
5. Valige **OK,** et alustada ja joondada oma vorming viimaste andmemudeli muudatustega.
6. Valige **Kujundaja**.
7. Valige vasakul **paanil** vormingukujundaja leheküljel vormingustruktuuri puus suvand Laienda **/Ahenda**.
8. Järgige neid samme uue vorminguelemendi lisamiseks, et koguda nende osapoolte kirje ID-koode, kelle kanded on loodud aruannetes esitatud.

    1. Valige vormingustruktuuri puus element **Report.Row.Trans** sequence.
    2. Valige **Lisa**.
    3. Valige dialoogiboksis **Lisa andmeallika** üksus **\>.**
    4. Sisestage **dialoogiboksi** Komponendi atribuudid väljale **Nimi** **ID**.
    5. **Väljal Andmetüüp** valige **Int64**.
    6. Valige nupp **OK**.

    > [!NOTE]
    > Andmeallika **kauba elementi \>** saab kasutada sisemiste arvutuste ja andmete teisendamise tegemiseks ainult käitatud vormingu ulatuse puhul. Seetõttu ei muuda te selle vorminguelemendi lisamisega loodud dokumendi sisu.

9. Järgige neid samme uute vorminguelementide lisamiseks, et sisestada osapoolte nimed loodud aruannetesse.

    1. Valige element **Aruanne.Reaseeria**.
    2. Valige **Lisa**.
    3. Dialoogiaknas **Lisa** valige tekstiseeria **\>**.
    4. Sisestage **dialoogiboksi** Komponendi atribuudid väljale **Nimi** väärtus **Osapool**.
    5. Valige nupp **OK**.
    6. Valige report.Row.Party **järjestuse** element.
    7. Valige **Lisa**.
    8. Dialoogiaknas **Lisa** valige tekstistring **\>**.
    9. **Dialoogiboksi Komponendi** atribuudid väljale **Nimi sisestage** **nimi**.
    10. Valige nupp **OK**.

10. Järgige neid samme uue andmeallika lisamiseks, et koguda nende osapoolte kirje ID-koode, kelle kanded on loodud aruannetes esitatud.

    1. Valige vahekaardil **Vastendamine** suvand **Lisa juur**.
    2. Valige dialoogiboksis **Andmeallika lisamine** suvand Funktsioonid **andmete \> kogum**.
    3. Sisestage **dialoogiboksi "Andmete kogum" andmeallika** atribuudid väljale **Nimi** väärtus **PartyIds**.
    4. **Väljal Kauba tüüp** valige **Int64**.
    5. Valige nupp **OK**.

11. Järgige neid samme, et lisada uus sidumine, et koguda nende osapoolte kirje ID-koode, kelle kanded on loodud aruannetes esitatud.

    1. Valige vormingustruktuuri puus Report.Row.Trans.Id **element**.
    2. Valige **Valemi redigeerimine**.
    3. Sisestage **avaldis valemikoosturi** lehele `PartyIds.Collect(model.Transaction.Party.RecId)`.
    4. Valige **Salvesta** ja sulgege leht **Valemikoostaja**.

12. Järgige neid samme uute sidumiste lisamiseks, et sisestada loodud aruannetele osapoolte nimed.

    1. Valige vormingustruktuuri puus aruanne.Osapoole **järjestuse** element.
    2. Valige **Valemi redigeerimine**.
    3. Sisestage **avaldis valemikoosturi** lehele `model.Party(PartyIds.Result)`.
    4. Valige **Salvesta** ja sulgege leht **Valemikoostaja**.
    5. Valige vormingustruktuuri puus valitud **Report.Party.Name** element.
    6. Valige vahekaardil **Vastendamine** andmemudeli `model.Party.Name` väli.
    7. Valige **Seo**.

    ![Korrigeeritud ER-vormingu struktuur vormingukujundaja lehel.](./media/er-data-model-parameterized-calls-format2.png)

13. Valige **salvestamine** ja sulgege vormingukujundaja **leht**.
14. Sulgege leht **Mudelist andmeallikasse vastendamine**.
15. **Versiooni** 2.2 puhul valige versioonide **kiirkaardil** suvand **Muuda olekut** \> **Lõpetatud**. Seejärel valige **OK**.

### <a name="run-the-adjusted-format"></a>Käivita korrigeeritud vorming

1. Valige konfiguratsioonide **lehel** auditi **näidisvorming** ja seejärel valige tegevuspaanil käsk **Käivita**.
2. **Valige dialoogiboksi Elektroonilise aruande** parameetrid vahekaardil Kirjed **, mida kaasata**, suvand **Filter**.
3. Saate määrata tingimused kannete **PIV-110000004** **ja INV-10000001** kannete valimiseks.
4. Valige nupp **OK**.
5. Valige nupp **OK**.
6. Vaadake üle loodud dokument, mis sisaldab valitud kannete maksukandeid ning vastava kliendi ja hankija nimesid.

    ![Loodud dokumendi eelvaade koos maksukannete ja osapoolte nimedega](./media/er-data-model-parameterized-calls-output2.png)

7. Minge **ostureskontrosse** \> **·** \> **Hankijad** Kõik hankijad ja vaadake **üle valitud kande PIV-110000004** üksikasjad, k.a hankija nimi.

    ![Ostukande üksikasjade ülevaatamine kõigi hankijate ja arve töölehelehtedel](./media/er-data-model-parameterized-calls-review1.gif)

8. Minge **müügireskontro** \> **·** \> **klientidesse** ja vaadake üle valitud **INV-10000001 üksikasjad, k.a** kliendi nimi.

    ![Müügikande üksikasjade ülevaatamine kõigil klientidel ja sisestatud käibemaksulehtedel.](./media/er-data-model-parameterized-calls-review2.gif)

ER-i lahenduse käivitamise kohta lisateabe saamiseks kasutage ER-i integreeritud jõudluse jälituse [parserit](trace-execution-er-troubleshoot-perf.md).

## <a name="additional-resources"></a>Lisaressursid

- [Arvutatud väljatüübi ER-andmeallikate parameetritega kõned](er-calculated-field-type.md)
- [Elektroonilise aruandluse vormingute täitmise jälitamine jõudlusprobleemide tõrkeotsinguks](trace-execution-er-troubleshoot-perf.md)
- [Kasuta elektroonilise aruandluse vormingutes ANDMEKOGUMI andmeallikaid](er-data-collection-data-sources.md)
- [Funktsioon ValueInLarge ER](er-functions-logical-valueinlarge.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
