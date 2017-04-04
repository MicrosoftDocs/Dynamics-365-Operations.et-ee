---
title: E juhtumist Power BI andmetega Dynamics 365 operatsioonide seadistamine
description: "See teema selgitab, kuidas saate kasutada oma elektroonilise aruandluse (ER) konfiguratsiooni, et korraldada andmete üleviimine teie rakenduse Dynamics 365 for Operations eksemplarist Power BI teenustesse. Näitena kasutab see teema Intrastati kandeid äriandmetena, mis tuleb üle viia. Power BI kaardi visualisatsioon kasutab selle Intrastati kande andmeid, et esitleda Power BI aruandes ettevõtte impordi-/eksporditegevuse analüüsi vaadet."
author: kfend
manager: AnnBe
ms.date: 2016-10-31 13 - 22 - 29
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: ed0192c44b6d7e88120c64e539ebb0ac3b379831
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-electronic-reporting-to-provide-power-bi-with-data-from-dynamics-365-for-operations"></a>E juhtumist Power BI andmetega Dynamics 365 operatsioonide seadistamine

See teema selgitab, kuidas saate kasutada oma elektroonilise aruandluse (ER) konfiguratsiooni, et korraldada andmete üleviimine teie rakenduse Dynamics 365 for Operations eksemplarist Power BI teenustesse. Näitena kasutab see teema Intrastati kandeid äriandmetena, mis tuleb üle viia. Power BI kaardi visualisatsioon kasutab selle Intrastati kande andmeid, et esitleda Power BI aruandes ettevõtte impordi-/eksporditegevuse analüüsi vaadet.

<a name="overview"></a>Ülevaade
--------

Microsoft Power BI on kogumik tarkvara teenustest, rakendustest ja konnektoritest, mis töötavad koos, et muuta andmete välised allikad sidusateks, visuaalselt kaasahaaravateks ja interaktiivseteks ülevaadeteks. Elektrooniline aruandlus (ER) võimaldab rakenduse Microsoft Dynamics 365 for Operations kasutajatel andmeallikaid hõlpsasti konfigureerida ja korraldada andmete üleviimist rakendusest Dynamics 365 for Operations rakendusse Power BI-le. Andmed edastatakse failidena OpenXML-i töölehe (Microsoft Exceli töövihiku fail) vormingus. Edastatud failid talletatakse Microsoft SharePoint Serverisse, mis on selleks otstarbeks konfigureeritud. Talletatud faile kasutatakse Power BI-s, et teha aruandeid, mis hõlmavad visualisatsioone (tabelid, diagrammid, kaardid jne). Power BI aruandeid jagatakse Power BI kasutajatega ja neile on juurdepääs Power BI armatuurlaudade ja Dynamics 365 for Operationsi lehekülgede kaudu. See teema selgitab järgmisi ülesandeid:

-   Konfigureerige Dynamics 365 for Operationsi.
-   Valmistage ette elektroonilise aruandluse vormingus konfiguratsioon, et saada andmeid rakendusest Dynamics 365 for Operations.
-   Konfigureerige elektroonilise aruandluse keskkonda, et kanda andmeid üle Power BI-sse.
-   Kasutage edastatud andmeid, et luua Power BI aruanne.
-   Muutke Power BI aruanne rakenduses Dynamics 365 for Operations juurdepääsetavaks.

## <a name="prerequisites"></a>Eeltingimused
Selles teemas näite lõpuleviimiseks peab teil olema järgmine juurdepääs:

-   Juurdepääs Dynamics 365 for Operationsile ühe järgmise rolli jaoks:
    -   Elektroonilise aruandluse arendaja
    -   Elektroonilise aruandluse funktsionaalne konsultant
    -   Süsteemiadministraator
-   Juurdepääs SharePoint Serverile, mis on konfigureeritud kasutamiseks Dynamics 365 for Operationsiga
-   Juurdepääs Power BI raamistikule

## <a name="configure-document-management-parameters"></a>Dokumendihalduse parameetrite konfigureerimine
1.  Lehel **Dokumendihalduse parameetrid** konfigureerige juurdepääs SharePoint Serverile, mida kasutatakse ettevõttes, kuhu olete sisse logitud (DEMF ettevõte selles näites).
2.  Testige ühendust SharePoint Serveriga tagamaks, et teile on antud juurdepääs. [![Dokumendi parameetrid lehele](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)
3.  Avage konfigureeritud SharePointi tegevuskoht. Looge uus kaust, kuhu elektrooniline aruandlus talletab Exceli failid, millel on äriandmed, mida Power BI aruanded vajavad Power BI andmekogumite allikana.
4.  Rakenduses Dynamics 365 for Operations lehel **Dokumenditüübid** looge uus dokumendi tüüp, mida kasutatakse värskelt loodud SharePointi kaustale juurdepääsemiseks. Sisestage **Fail** väljale **Grupp** ja **SharePoint** väljale **Asukoht** ja sisestage seejärel SharePointi kausta aadress. [![Dokumendi liigid lehele](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>Elektroonilise aruandluse parameetrite konfigureerimine
1.  Tööruumis **Elektrooniline aruandlus** klõpsake linki **Elektroonilise aruandluse parameetrid**.
2.  Vahekaardil **Manused** valige kõikide väljade puhul dokumendi tüübiks **Fail**.
3.  Tööruumis **Elektrooniline aruandlus** tehke soovitud teenusepakkuja aktiivseks, klõpsates valikut **Aktiivsena seadistamine**. Lisateabe jaoks esitage tegevuse juhis **Elektroonilise aruandluse teenusepakkuja valimine**.

## <a name="use-an-er-data-model-as-the-source-of-data"></a>Elektroonilise aruandluse andmemudeli kasutamine andmeallikana
Teil peab olema äriandmete allikaks elektroonilise aruandluse andmemudel, mida kasutatakse Power BI aruannetes. See andmemudel laetakse üles elektroonilise aruandluse konfiguratsioonide hoidlast. Lisateabe jaoks vaadake [Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services](download-electronic-reporting-configuration-lcs.md) või esitage tegevuse juhis **Elektroonilise aruande konfiguratsiooni importimine teenusest Lifecycle Services** . Valige andmemudeliks **Intrastat **, mis laetakse üles valitud elektroonilise aruandluse konfiguratsioonide hoidlast. (Selles näites versiooni 1 mudeli kasutatakse.) Seejärel pääsete selle **Intrastat** ER mudeli konfiguratsiooni ning **koosseisud** lehekülg. [![Konfiguratsiooni leht](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>Elektroonilise aruandluse vormingu konfiguratsiooni kujundamine
Peate looma uue elektroonilise aruandluse vormingus konfiguratsiooni, mis kasutab äriandmete allikana andmemudelit **Intrastat**. Selles vormingus konfiguratsioon peab looma väljundtulemused elektrooniliste dokumentidena OpenXML-i vormingus (Exceli fail). Lisateabe saamiseks esitage tegevuse juhis **ER-i konfiguratsiooni loomine aruannete loomiseks vormingus OPENXML**. Määrake uue konfiguratsiooni nimeks **Tegevuste importimine/eksportimine**, a Kasutage elektroonilise aruandluse vormingu kujundamisel mallina Exceli faili [Elektroonilise aruandluse andmed – impordi ja ekspordi üksikasjad](https://go.microsoft.com/fwlink/?linkid=845208). (Teavet vormingus malli importimiseks mängida ülesande juhend.) [![Import / eksport tegevuse konfiguratsiooni](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png) muuta on **impordi / ekspordi** konfiguratsiooni vormindada, toimige järgmiselt.

1.  Klõpsake valikut **Kujundaja**.
2.  Vahekaardil **Vorming** nimetage selle vormingu **Exceli väljundfail** faili element. [![Excel väljund faili element](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)
3.  Vahekaardil **Vastendamine** määrake Exceli faili nimi, mis luuakse alati, kui see vorming käivitatakse. Konfigureerige seotud avaldis, et tagastada väärtus **Impordi ja ekspordi üksikasjad** (xlsx-faili nime laiend lisatakse automaatselt). [![Format designer](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)
4.  Lisage selle vormingu jaoks uus andmeallika üksus. (See loetelu on vajalik täiendavaks andmete sidumist.)
    1.  Andmeallika nime **suunas\_loetelu**.
    2.  Valige andmeallika tüübiks **Andmemudeli loetelu**.
    3.  Viidake andmemudeli loetelule **Suund**.

    [![suund\_loetelu](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)
5.  Lõpetage andmemudeli **Intrastat** elementide ja koostatud vormingu elementide sidumine, nagu on näidatud järgmisel joonisel. [![Täites sidumise](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

Pärast selle käivitamist loob elektroonilise aruandluse vorming Exceli vormingus väljundtulemuse. See saadab Intrastati kannete üksikasjad väljundtulemusele ja eraldab need kannetena, mis kirjeldavad impordi- ja eksporditegevusi. Klõpsake **käivitada** testida uus ER vorm Intrastat-kannete loendit ning **Intrastat** lehele (**maksu**&gt;**deklaratsioonid**&gt;**väliskaubanduse**&gt;**Intrastat**). [![Intrastat-lk](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png) järgmine väljund tulemusena luuakse. Faili nimi on **Impordi ja ekspordi üksikasjad.xlsx**, nagu määrasite vormingu sätetes. [![Impordi ja ekspordi details.xlsx](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>Elektroonilise aruandluse sihtkoha konfigureerimine
Peate konfigureerima elektroonilise aruandluse raamistiku, et saata uue elektroonilise aruandluse vormingu konfiguratsiooni väljundtulemus erilisel viisil.

-   Väljundtulemus tuleb saata valitud SharePoint Serveri kausta.
-   Iga vormingu konfiguratsiooni käivitamine peab looma samast Exceli failist uue versiooni.

Kohta on **elektrooniline** lehe (**organisatsiooni haldamine**&gt;**elektrooniline**), klõpsake selle **elektroonilise aruandluse sihtkoha** punktile ning lisada uue sihtkoha. Väljal **Viide** valige varasemalt loodud vormingu konfiguratsioon **Impordi-/eksporditegevused**. Järgige neid juhiseid, et viite jaoks uus faili sihtkoha kirje lisada.

1.  Väljale **Nimi** sisestage faili sihtkoha pealkiri.
2.  Väljal **Faili nimi** valige Exceli faili vormingu komponendi jaoks nimi **Exceli väljundfail**.

Klõpsake uue sihtkoha kirje jaoks nuppu **Sätted**. Seejärel järgige dialoogiboksis **Sihtkoha sätted** neid juhiseid.

1.  Vahekaardil **Power BI** seadke suvandi **Lubatud** sätteks **Jah**.
2.  Väljal **SharePoint** valige varasemalt loodud dokumendi tüüp **Jagatud**.

## <a name="schedule-execution-of-the-configured-er-format"></a>Konfigureeritud elektroonilise aruandluse vormingu käivitamise ajastamine
Kohta ning **koosseisud** leht (**organisatsiooni haldamine**&gt;**elektrooniline**&gt;**koosseisud**), koosseisud puu, valige selle **impordi / ekspordile** konfiguratsiooni, varem loodud. Muutke versiooni 1.1 olekut variandilt **Mustand** variandile **Lõpetatud**, et muuta see vorming kasutamiseks kättesaadavaks. [![Koosseisud lehe](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png) valige selle versiooni on **impordi / ekspordi** konfiguratsiooni ja seejärel klõpsake **käivitada**. Pange tähele, et konfigureeritud sihtkoht rakendatakse väljundtulemusele, mis luuakse Exceli vormingus. Määrake suvandi **Pakktöötlus** sätteks **Jah**, et käivitada see aruanne järelevalveta režiimis. Klõpsake valikut **Kordumine**, et ajastada selle partii käivitamise vajalik kordumine. Kordumine määratleb, kui sageli värskendatud andmed edastatakse rakendusest Dynamics 365 for Operations rakendusse Power BI. [![Elektroonilise aruande parameetrid dialoogiboksi](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png) pärast seda, kui see on konfigureeritud, leiate ER aruande täitmise töö on **pakett-töid** lehele (**süsteemi halduse &gt;päringute &gt;pakett-töid**). [![Partii töökohti lehel](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png) selle töö käitamisel esimest korda sihtkoha loob uue Exceli faili, mis on konfigureeritud nimi valitud SharePointi kausta. Igal järgneval korral, kui töö käivitatakse, loob sihtkoht sellest Exceli failist uue versiooni. [![Exceli faili uus versioon](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>Power BI andmekomplekti loomine, kasutades elektroonilise aruandluse vormingu väljundtulemust.
Logige sisse rakendusse Power BI ja avage olemasolev Power BI grupp (tööruum) või looge uus grupp. Klõpsake **lisa** all **failid** ja selle **importimine või andmetega ühenduse loomine** jagu, või klõpsake (**+**) kõrval **andmekogumite** vasakul paanil. [![Andmekogumi loomise](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png) valige selle **SharePoint-meeskonnasaitide** variant ja sisestage tee SharePoint Server, mida kasutate (**https://ax7partner.spoppe.com** meie näites). Seejärel sirvige kausta **/Shared Documents/GER data/PowerBI** ja valige Exceli fail, mille lõite andmeallikaks uue Power BI andmekogumi jaoks. [![Valides Exceli faili](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png) klõpsake **Loo**, ja seejärel klõpsake **impordi**. Luuakse uus andmekogum, mis põhineb valitud Exceli failil. Andmekogumi saab automaatselt värskelt loodud armatuurlauale lisada. [![Andmekogumi armatuurlaua](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png) konfigureerida tuvastatavate perioodilise värskendus sundida Värskenda ajakava. Perioodilised värskendused võimaldavad rakendusest Dynamics 365 for Operations elektroonilise aruandluse aruande perioodilise käivitamise kaudu tulevate uute äriandmete tarbimist ja seda SharePoint Serveris loodud Exceli faili uute versioonide kaudu.

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>Power BI aruande loomine uut andmekogumit kasutades
Uue Power BI aruande loomiseks klõpsake loodud Power BI andmekogumit **Impordi ja ekspordi üksikasjad**. Seejärel konfigureerige visualiseerimine. Näiteks valige visualiseerimine **Täidetud kaart** ja konfigureerige see järgmiselt.

-   Määrake andmekogumi väli **CountryOrigin** kaardi visualiseerimise väljale **Asukoht**.
-   Määrake andmekogumi väli **Summa** kaardi visualiseerimise väljale **Värvi küllastus**.
-   Lisage andmekogumi väljad **Tegevus** ja **Aasta** kaardi visualiseerimise väljade kogumikule **Filtrid**.

Salvestage Power BI aruanne kui **Impordi ja ekspordi üksikasjade aruanne**. [![Impordi ja ekspordi üksikasjade aruanne](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png) Pange tähele, et kaardil on nimetatud Exceli faili (Austria ja Šveits selles näites) riikides/regioonides. Need riigid/regioonid on tehtud värviliseks, et näidata iga ühe arveldatud summade osakaalu. Värskendage Intrastati kannete loendit. Itaalias pärinev ekspordikanne on lisatud. [![Intrastat-kannete loendi](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png) oodata ER aruande järgmise ajastatud käivitamise ja järgmise ajastatud värskendamise Power BI andmekogumi. Seejärel vaadake Power BI aruanne üle (valige, et näidata ainult impordikandeid). Värskendatud kaart näitab nüüd Itaaliat. [![Uuendatud kaart](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-dynamics-365-for-operations"></a>Juurdepääs Power BI aruandel rakenduses Dynamics 365 for Operations
Seadistage rakenduste Dynamics 365 for Operations ja Power BI vaheline integratsioon. Lisateabe jaoks vaadake [Power BI integreerimise konfigureerimine tööruumidele](configure-power-bi-integration.md). Kohta ning **elektrooniline** tööruumi lehekülg, mis toetab Power BI integratsioon (**organisatsiooni haldamine**&gt;**tööruumide**&gt;**elektroonilise aruandluse tööruumi**), klõpsake **Valikud**&gt;**avatud aruandesse kataloogi**. Valige loodud Power BI aruanne **Impordi ja ekspordi üksikasjad**, et näidata seda aruannet valitud lehel tegevusüksusena. Klõpsake tegevusüksust, et avada leht Dynamics 365 for Operations, mis näitab Power BI-s loodud aruannet. [![Impordi ja ekspordi üksikasjade aruanne](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

<a name="see-also"></a>Vt ka
--------

[Elektroonilise aruandluse sihtkohad](electronic-reporting-destinations.md)

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)


