---
title: Uue elektroonilise aruandluse lahenduse kujundamine ZPL-siltide printimiseks
description: See teema kirjeldab, kuidas kujundada uut elektroonilise aruandluse (ER) lahendust Spikribra Programming Language (ZPL) siltide printimiseks.
author: NickSelin
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-02-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: c1bedf1184b45741102000fa68c8d662c7383301
ms.sourcegitcommit: 2977e92a76211875421e608555311c363cfbdc25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/16/2022
ms.locfileid: "8612349"
---
# <a name="design-a-new-er-solution-to-print-zpl-labels"></a>Uue elektroonilise aruandluse lahenduse kujundamine ZPL-siltide printimiseks

[!include [banner](../includes/banner.md)]


See teema selgitab, kuidas kasutaja süsteemiadministraatoris, elektroonilise aruandluse arendajas või elektroonilise aruandluse funktsionaalne nõustaja rollis saab konfigureerida elektroonilise aruandluse (ER) [raamistiku parameetreid, kujundada uue ER-lahenduse nõutud ER](general-electronic-reporting.md) konfiguratsioone, et pääseda juurde laohalduse süsteemi andmetele, ja luua kohandatud lao asukoha silte Rakenduste [programmeerimiskeele](general-electronic-reporting.md#Configuration) (ZPL) II vormingus. Neid toiminguid saab teha ettevõttes **USRT**.

## <a name="business-scenario"></a>Äristsenaarium

Te esindate ettevõtet, mis rakendas laohaldust Microsoft Dynamics 365 Finantsis. Igale lao asukohale peab olema sildistatud eneselevitatav silt, mis sisaldab vöötkoodi. Laotöötajad kasutavad vöötkoodi skannimiseks pihuseadmega vöötkoodi lugejaid.

Kõik lao asukohad on eelinstallimistegevuste ulatusele märgistatud. Kuid kui olemasolevad sildid muutuvad vigasteks või lao riiulid on ümber seadistatud, peab teil olema ka võimalik printida lao asukoha silte. Hiljuti väljastatud ER-i funktsiooni kasutades saate konfigureerida uue ER-lahenduse, mis võimaldab lao ülevaatajal printida sildid otse sildiprinterile.

## <a name="configure-the-er-framework"></a>ER-raamistiku konfigureerimine

Minimaalsete [ER-i parameetrite konfigureerimine](er-quick-start2-customize-report.md#ConfigureFramework), mis on vajalikud ER-i raamistiku kasutamiseks. Enne ER-raamistiku kasutamist uue ER-lahenduse loomiseks peate selle häälestuse lõpule viima.

## <a name="design-a-domain-specific-data-model"></a>Domeenipõhise andmemudeli kujundamine

Looge uus ER-i konfiguratsioon, mis sisaldab [laohalduse](er-overview-components.md#data-model-component) domeeni andmemudelikomponenti. Seda andmemudelit kasutatakse andmeallikana hiljem, kui kujundate lao asukoha siltide loomiseks ER-vormingu.

### <a name="import-a-data-model-configuration"></a>Andmemudeli konfiguratsiooni importimine

Järgige neid samme, et importida nõutud andmemudel Microsofti antud XML-failist. Teise võimalusena saate luua oma andmemudeli, nagu kirjeldatud järgmises jaotises.

1. Laadige alla [fail Warehouse model.version.1.xml](https://download.microsoft.com/download/9/f/1/9f136e9b-bf5f-403a-b089-a2b2ed1da2ba/Warehouse-model.version.1.xml) ja salvestage see kohalikku arvutisse.
2. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
3. Valige tööruumis **Elektrooniline aruandlus** suvand **Aruandluse konfiguratsioonid**.
4. Valige tegevuspaanil **Konfiguratsioonide** leht suvand **Vahetuslaadimine** \> **XML-failist.**
5. Valige **sirvimine** ning seejärel otsige ja valige lao **mudel.version.1.xml** fail.
6. Konfiguratsiooni importimiseks valige **OK**.

![Imporditud ER-i andmemudeli konfiguratsioon lehel Konfiguratsioonid](./media/er-design-zpl-labels-imported-model.png)

### <a name="create-a-data-model-configuration"></a>Andmemudeli konfiguratsiooni loomine

Microsofti esitatud andmemudelifaili importimise asemel saate nullist luua andmemudeli. Näiteid selle ülesande lõpule viimise kohta vt uue [andmemudeli konfiguratsiooni loomine](er-quick-start1-new-solution.md#DesignDataModel).

### <a name="review-the-data-model"></a>Andmemudeli ülevaatamine

Konfigureeritud andmemudeli redigeeritavat versiooni saate vaadata andmemudeli **kujundaja** lehel.

![ER-andmemudeli struktuur andmemudeli kujundaja lehel.](./media/er-design-zpl-labels-model.png)

## <a name="design-a-model-mapping-for-the-configured-data-model"></a>Mudelivastenduse kujundamine konfigureeritud andmemudelile

Kasutajana elektroonilise aruandluse arendaja rollis peate looma uue ER-i konfiguratsiooni, mis sisaldab lao [andmemudeli](er-overview-components.md#model-mapping-component) mudelivastenduse komponenti. Komponent juurutab Dynamics 365 Finance'i konfigureeritud andmemudeli ja on selle rakenduse spetsiifiline. Peate selle konfigureerima, et määrata rakendusobjektid, mida kasutatakse konfigureeritud andmemudeli täitmiseks käitusajal rakenduse andmetega. Selle ülesande lõpuleviimiseks peate aru saama, kuidas laohalduse äridomeeni andmestruktuuri finantsidesse rakendatakse.

### <a name="import-a-model-mapping-configuration"></a>Mudeli vastendamise konfiguratsiooni importimine

Järgige neid samme, et importida nõutud mudelivastendus Microsofti antud XML-failist. Teise võimalusena saate luua oma mudelivastenduse, nagu kirjeldatud järgmises jaotises.

1. Laadige alla [laomudeli vastendus.version.1.1.xml](https://download.microsoft.com/download/1/c/c/1cc94d28-3d90-4ffd-a118-77d6c322904f/Warehouse-model-mapping.version.1.1.xml) fail ja salvestage see kohalikku arvutisse.
2. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
3. Valige tööruumis **Elektrooniline aruandlus** suvand **Aruandluse konfiguratsioonid**.
4. Valige tegevuspaanil **Konfiguratsioonide** leht suvand **Vahetuslaadimine** \> **XML-failist.**
5. Valige **sirvimine** ning seejärel otsige ja valige laomudeli **vastendus.version.1.1.xml** fail.
6. Konfiguratsiooni importimiseks valige **OK**.

![Imporditud ER-mudeli vastendamise konfiguratsioon lehel Konfiguratsioonid](./media/er-design-zpl-labels-imported-mapping.png)

### <a name="create-a-model-mapping-configuration"></a>Mudeli vastendamise konfiguratsiooni loomine

Microsofti esitatud mudeli vastendamisfaili importimise asemel saate mudeli vastendamise nullist luua. Näiteid selle ülesande lõpule viimise kohta vt uue [mudelivastenduse konfiguratsiooni loomine](er-quick-start1-new-solution.md#CreateModelMapping).

### <a name="review-the-model-mapping"></a>Mudeli vastendamise läbivaatamine

Konfigureeritud mudeli vastendamise redigeeritavat versiooni saate vaadata mudeli vastendamise **kujundaja** lehel.

![ER-mudeli vastendamise struktuur mudeli vastendamise kujundaja lehel](./media/er-design-zpl-labels-mapping.png)

## <a name="design-a-format"></a>Vormingu kujundamine

Elektroonilise aruandluse funktsionaalse konsultandi rollis kasutajana peate looma uue ER-i konfiguratsiooni, mis sisaldab [vormingu](er-overview-components.md#format-component) komponenti. Komponendi konfigureerimiseks kasutate oma lao asukoha sildi paigutuse määramiseks ZPL II koodi.

### <a name="import-a-format-configuration"></a>Vormingukonfiguratsiooni importimine

Järgige neid samme, et importida nõutav vorming Microsofti antud XML-failist. Teise võimalusena saate luua oma vormingu, nagu kirjeldatud järgmises jaotises.

1. Laadige alla [lao asukoha sildid.version.1.1.xml](https://download.microsoft.com/download/5/7/5/5758b551-69a5-45bd-a2b2-21c3db73a6fc/Warehouse-location-labels.version.1.1.xml) fail ja salvestage see oma kohalikku arvutisse.
2. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
3. Valige tööruumis **Elektrooniline aruandlus** suvand **Aruandluse konfiguratsioonid**.
4. Valige tegevuspaanil **Konfiguratsioonide** leht suvand **Vahetuslaadimine** \> **XML-failist.**
5. Valige **sirvimine** ning seejärel otsige ja valige lao **asukoha sildid.version.1.1.xml fail**.
6. Konfiguratsiooni importimiseks valige **OK**.

![Imporditud ER-vormingu konfiguratsioon lehel Konfiguratsioonid.](./media/er-design-zpl-labels-imported-format.png)

### <a name="create-a-format-configuration"></a>Vormingukonfiguratsiooni loomine

Microsofti esitatud vormingufaili importimise asemel võite nullist luua vormingu. Näiteid, mis näitavad, kuidas seda ülesannet lõpule viia, vaadake teemast [Uue vormingu konfiguratsiooni loomine](er-quick-start1-new-solution.md#FormatCreate).

### <a name="review-the-format"></a>Vormingu läbivaatamine

Konfigureeritud vormingu redigeeritavat versiooni saate vaadata vormingukujundaja **lehel**.

![ER-vormingu struktuur vormingukujundaja lehel.](./media/er-design-zpl-labels-format.png)

Selle `model.Location.Label` vormingu andmeallikas on konfigureeritud looma silte, mis sisaldavad järgmist teavet:

- Lao pealkiri tekstina
- Lao pealkiri vöötkoodina
- Asukoha pealkiri
- Kontrollnumbrid

**Andmeallika valemikoostaja** lehel sisaldab siltide loomiseks kasutatav ER-valem `CONCATENATE` funktsiooni, mis ühendab teabe soovitud kavandis.

![Andmeallika valem valemikujundaja lehel.](./media/er-design-zpl-labels-review-formula.png)

> [!TIP]
> Sildi paigutus on kujundatud nii, et asukoha pealkiri ja kontrollnumbrid on sildi keskel joondatud. ZPL II ei toeta siiski vöötkoodide joondusekeskust. Seetõttu kasutatakse andmeallika valemit `model.Location.Warehouse.Alignment` vöötkoodi joondamiseks sildi keskel. See valem arvutab vöötkoodi vasakpoolse nihke, mis põhineb lao pealkirjas märkide arvul.

## <a name="prepare-your-environment-for-previewing-generated-labels"></a>Loodud siltide eelvaateks keskkonna ettevalmistamine

Järgmises näites kasutatakse ZPL-siltide printeri emulaatori rakendust loodud siltide eelvaate kuvamiseks ekraanil. Järgige neid samme selle suvandi lubamiseks.

1. Lisage lao [asukoha sildi](er-destination-type-print.md) ER-vormingule printeri **ER**[sihtkoht ja konfigureerige see finantside loodud siltide saatmiseks dokumendi protsessiagendisse (DRA)](install-document-routing-agent.md).
2. Installige ja konfigureerige DRA finantside loodud siltide protsessi jaoks kohalikuks printeriks, millele on juurdepääs praegusest tööjaamast.
3. Lisage praegusele tööjaamale kohalik printer ja konfigureerige see mööduma DRA-st loodud sildid printeri emulaatori rakendusele.
4. Installige printeri emulaatori rakendus Kroomitud veebibrauseri laiendina ja konfigureerige see mööduma kohalikust printerist genereeritud sildid veebiteenusele, mis renderdab loodud sildid ja tagastab need eelvaateks printeri emulaatorile.

<table>
<tbody>
<tr align="center">
<td>
<p>Finance</p>
<p>ER-aruanne</p>
<p>Printeri sihtkoht</p>
</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from Finance to the DRA."></td>
<td>Dokumendi protsessiagent</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from the DRA to a local printer."></td>
<td>Kohalik printer</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from a local printer to a printer emulator."></td>
<td>Printeri emulaator</td>
<td><img src="./media/er-design-zpl-labels-flow2.png" alt="Data flow direction: from a printer emulator to a rendering web service and then back to the printer emulator."></td>
<td>Veebiteenuse renderdamine</td>
</td>
</tr>
</tbody>
</table>

### <a name="install-and-configure-a-printer-emulator-application"></a>Printeri emulaatori rakenduse installimine ja konfigureerimine

Lisage printeri emulaatori rakendus ZPL-i renderdamismootorile oma Kroomitud veebibrauserile. Selles näites kasutatakse [sildipõhisel](https://chrome.google.com/webstore/detail/zpl-printer/phoidlklenidapnijkabnfdgmadlcmjo)[ZPL-i veebiteenusel põhinevat Zpl-printeri emulaatorit](http://labelary.com/service.html). Printeri emulaatori rakendus annab genereeritud sildid ZPL-vormingus kohalikust printerist veebiteenusele ja tagastab seejärel eelvaateks sildid PDF- või PNG-failidena.

1. Leidke ja valige Kroomitud veebipoes printeri emulaatori rakendus, mida soovite kasutada. Seejärel valige lisa **Kroomitud** tabelisse, et lisada see oma Kroomitud veebibrauserisse.

    ![Printeri emulaatori rakenduse lisamine Kroomitud veebipoes Kroomitud veebibrauserile.](./media/er-design-zpl-labels-add-app.png)

2. Valige **Käivitusrakendus** printeri emulaatori rakenduse käivitamiseks Kroomitud veebibrauserist.

    ![Printeri emulaatori rakenduse käivitamine Kroomitud veebibrauserist.](./media/er-design-zpl-labels-run-app.png)

3. Konfigureerige käitav rakendus:

    1. Lülitab rakenduse välja.
    2. Printeri sätetes määrake hosti väärtuseks **127.0.0.1**.
    3. Määrake pordi väärtuseks **9100**.

        ![Printeri emulaatori rakenduse konfigureerimine.](./media/er-design-zpl-labels-configure-app.png)

    4. Lülitage rakendus uuesti sisse. Peaksite saama teate, mis täpsustab, et printer käivitati määratud hostil ja pordil.

        ![Printeri emulaatori rakendus lülitati tagasi sisse.](./media/er-design-zpl-labels-turn-on-app.png)

> [!NOTE]
> Kuna selles näites kasutatud printeri emulaatori rakendus põhineb siltide renderdamisel veebiteenusel, kontrollige, et teie turvaseaded võimaldavad teil teenusega suhelda. Vastasel juhul ei saa rakendus renderdatud silte ja nende siltide eelvaated pole saadaval.

### <a name="add-and-configure-a-local-printer"></a>Kohaliku printeri lisamine ja konfigureerimine

[Lisage uus kohalik printer,](https://support.microsoft.com/windows/install-a-printer-in-windows-10-cc0724cf-793e-3542-d1ff-727e4978638b) mida praegune seade saab kasutada DRA-st loodud siltide läbimiseks printeri emulaatori rakendusele.

1. Windowsis valige Start-sätete **·** \> **seadmete** \> **printeriskanner.** \> **\&**
2. Valige **printeriskanneri \& sätted**.
3. Printeri **või skanneri lisamiseks valige** suvand **Lisa seade**.
4. **Soovitud printeri loendis pole,** valige lisa **käsitsi**.
5. Väljal Leidke **printer muude suvandite abil** valige suvand Lisa **käsitsi sätetega kohalik printer või võrguprinter**.
6. Valige väljal **Vali printeri port** suvand **Loo uus port ja** seejärel järgige neid samme.

    1. Pordi tüübi **väljal valige** standardne **TCP/IP-port**.
    2. Väljale Hostinimi **või IP-aadress** sisestage **127.0.0.1**.
    3. Sisestage **väljale Pordi** nimi **ZPL**.
    4. Oodake, kuni **tuvastav TCP/IP-pordi** toiming on lõpule viidud.
    5. Valige väljal **Seadme tüüp väärtus** Kohandatud ja **seejärel sätted** **.**
    6. Veenduge, et määratud on järgmised pordisätted:

        - **Pordi nimi:** ZPL
        - **Printeri nimi või IP-aadress:** 127.0.0.1
        - **Protokoll: toor**
        - **Pordi number:** 9100

7. Väljal Printeri **draiveri installimine valige** ainult **Üldine/tekst**.
8. Sisestage **väljale Printeri** nimi **VäärtusbraPrinter**.

![Praegusele seadmele kohaliku printeri lisamine.](./media/er-design-zpl-labels-configure-printer.png)

### <a name="install-and-configure-the-dra"></a>DRA installimine ja konfigureerimine

Valmistage DRA ette loodud siltide läbimiseks finantsidelt konfigureeritud kohalikule printerile.

1. [Installige DRA](install-document-routing-agent.md#install-the-document-routing-agent).
2. [Konfigureerige DRA](install-document-routing-agent.md#configure-the-document-routing-agent).
3. [Registreerige kohalik printer](install-document-routing-agent.md#register-network-printers) DRA-s.
4. [Saate aktiveerida kohaliku printeri](install-document-routing-agent.md#administer-network-printers) finantskeskkonnas.

![DRA ettevalmistamine loodud siltide printimiseks.](./media/er-design-zpl-labels-configure-dra.png)

### <a name="configure-the-er-destination"></a>Elektroonilise aruandluse sihtkoha konfigureerimine

Valmistage ER-i sihtkoht ette, et edastada loodud sildid finantsidelt DRA-le.

1. Avage **Organisatsiooni haldus** \> **Elektrooniline aruandlus** \> **Elektroonilise aruandluse sihtkoht**.
2. Valige elektroonilise **aruandluse sihtlehe** tegevuspaanil suvand **Uus**.
3. **Väljal Viide** valige lao asukoha **sildid**.
4. Valige **Faili sihtkoht** kiirkaardil **Uus**.
5. Sisestage **sildid** väljale **Nimi**.
6. Valige väljal **Faili** komponendi nimi väärtus **Aruanne**.
7. Valige **Sätted**.
8. **Seadke dialoogiboksi Sihtsätted** vahekaardil **Printer** suvandi **Lubatud väärtuseks** **Jah**.
9. Valige printeri **nime väljal** soovitud **PrinterPrinter.%1**.
10. Valige dokumendi **protsessi tüübi väljal** ZPL **·**.
11. Valige nupp **OK**.

![ER-i sihtkoha konfigureerimine lao asukoha siltide vormingu jaoks elektroonilise aruandluse sihtlehel](./media/er-design-zpl-labels-configure-destination.png)

## <a name="review-warehouse-locations"></a>Ladude asukohtade ülevaatamine

1. Minge laohalduse **seadistuse** \> **lao** \> **asukohta.** \> **·**
2. Filtreerige **asukohad** lehel, et vaadata ainult asukohti, mille väärtus on väljal **Kontrollnumbrid**.

![Lao asukohtade ülevaatamine asukohtade lehel.](./media/er-design-zpl-labels-review-locations.png)

## <a name="print-warehouse-location-labels"></a>Lao asukoha siltide printimine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage **konfiguratsioonipuu** lehel Konfiguratsioonid valikut **Laomudel ja** valige lao **asukoha sildid**.
3. Valige toimingupaanil käsk **Käivita**.
4. **Valige dialoogiboksi Elektroonilise aruande** parameetrid vahekaardil Kirjed **, mida kaasata**, suvand **Filter**.
5. Leidke vahekaardil **Vahemik** rida, kus **välja Tabel väärtuseks** on **seatud Asukohad** **ja välja väärtuseks** on seatud **Asukoht**. Sisestage **kriteeriumiväljale** **LPEnabled**.
6. Valige nupp **OK**.
7. Valige nupp **OK**. Silt luuakse ja kuvatakse printeri emulaatori rakenduse eelvaatelehel.

![Loodud sildi ülevaatamine Zpl-printeri emulaatori rakenduse eelvaate lehel.](./media/er-design-zpl-labels-preview-label.png)

## <a name="modify-the-layout-of-a-label"></a>Sildi kavandi muutmine

Saate muuta oma lao asukoha siltide praegust kavandit. Järgmine näide näitab, kuidas muuta kavandit nii, et loodud sildid sisaldaks asukoha profiili ID-d.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Seadke mustandi **oleku ER kasutajaparameetri**[jaoks sihtkohtade kasutamine väärtusele](electronic-reporting-destinations.md#applicability)**Jah**.
3. Laiendage **konfiguratsioonipuu** lehel Konfiguratsioonid valikut **Laomudel ja** valige lao **asukoha sildid**.
4. Valige **Kujundaja**.
5. **Valige vahekaardil Vastendus** kujundaja **lehel** Vormingu kujundaja `model.Location.Label` andmeallikas.
6. Valige dialoogiboksis **Andmeallika atribuudid** suvand **Redigeeri** \> **valemit.**
7. Vaadake valemikoostaja **lehe** valemiväljal **üle** ER valem, mida kasutatakse siltide loomiseks.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^XZ")
    ```

8. Värskendage valemit, et lisada loodud siltidele asukohaprofiili ID.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^CF0,40,40^FO0,240^FB800,1,0,C,0^FD",@.ProfileID,"\&^FS",CrLf,
    "^XZ")
    ```

9. Valige käsk **Salvesta**.
10. Valige nupp **OK**.
11. Valige toimingupaanil käsk **Käivita**.
12. **Valige dialoogiboksi Elektroonilise aruande** parameetrid vahekaardil Kirjed **, mida kaasata**, suvand **Filter**.
13. Leidke vahekaardil **Vahemik** rida, kus **välja Tabel väärtuseks** on **seatud Asukohad** **ja välja väärtuseks** on seatud **Asukoht**. Sisestage **kriteeriumiväljaleKriteerium** **·**.
14. Valige nupp **OK**.
15. Valige nupp **OK**. Silt luuakse ja kuvatakse printeri emulaatori rakenduse eelvaatelehel.

![Vaadake üle loodud silt, mis sisaldab asukohaprofiili ID-d Zpl printeri emulaatori rakenduse eelvaatelehel.](./media/er-design-zpl-labels-preview-label2.png)

## <a name="encoding"></a>Kodeerimine

> [!NOTE]
> Redigeeritava ER-vormingu **Common\\File** komponendi kodeerimissätt ja kujundatava sildi sobiv säte tuleb sünkroonida. **[...](er-suppress-bom-characters.md)** CommonFile'i **\\ komponendi** kodeerimisvälja väärtus ei tohi vastuolus olla ZPL-käsuga, mida kasutatakse sildi kodeerimise juhtimiseks (nt `^CI` käsk). ER ei kontrolli nende sätete sünkroonimist.

## <a name="additional-resources"></a>Lisaressursid

[Printeri sihtkoht](er-destination-type-print.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
