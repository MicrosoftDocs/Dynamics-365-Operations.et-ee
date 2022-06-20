---
title: Elektroonilise aruandluse (ER) konfigureerimine andmete tõmbamiseks Power BI-sse
description: See artikkel selgitab, kuidas te saate kasutada elektroonilise aruandluse (ER) konfiguratsiooni andmete edastamise korraldamiseks eksemplarist teenustesse Power BI.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e6903513dec4da20dbc4463fbae6a406fc06e1a6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896730"
---
# <a name="configure-electronic-reporting-er-to-pull-data-into-power-bi"></a>Elektroonilise aruandluse (ER) konfigureerimine andmete tõmbamiseks Power BI-sse

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas te saate kasutada elektroonilise aruandluse (ER) konfiguratsiooni andmete edastamise korraldamiseks eksemplarist teenustesse Power BI. See artikkel kasutab näiteks Intrastat-kandeid äriandmetena, mis tuleb üle kanda. Power BI kaardi visualisatsioon kasutab neid Intrastati kande andmeid, et esitleda Power BI aruandes ettevõtte impordi-/eksporditegevuse analüüsi vaadet.

## <a name="overview"></a>Ülevaade

Microsoft Power BI on kogumik tarkvarateenustest, rakendustest ja konnektoritest, mis töötavad koos, et muuta välised andmeallikad sidusateks, visuaalselt kaasahaaravateks ja interaktiivseteks ülevaadeteks. Elektrooniline aruandlus (ER) võimaldab kasutajatel hõlpsasti konfigureerida andmeallikaid ja korraldada andmete edastamine rakendusest Power BI-sse. Andmed edastatakse failidena OpenXML-i töölehe (Microsoft Exceli töövihiku fail) vormingus. Edastatud failid talletatakse Microsoft SharePoint Serverisse, mis on selleks otstarbeks konfigureeritud. Talletatud faile kasutatakse Power BI aruannete koostamiseks, mis hõlmavad visualisatsioone (tabelid, diagrammid, kaardid jne). Power BI aruandeid jagatakse Power BI kasutajatega ning neile pääseb juurde Power BI armatuurlaudade ja rakenduse lehtede kaudu. See artikkel selgitab järgmisi ülesandeid:

- Konfigureerige Microsoft Dynamics 365 Finantsid.
- Valmistage ette elektroonilise aruandluse vormingus konfiguratsioon, et saada andmeid rakendusest Finance.
- Konfigureerige elektroonilise aruandluse keskkond andmete edastamiseks Power BI-sse.
- Looge edastatud andmeid kasutades Power BI aruanne.
- Muutke Power BI aruanne Finance'is juurdepääsetavaks.

## <a name="prerequisites"></a>Eeltingimused
Selle artikli näite lõpuleviimiseks peab teil olema järgmine juurdepääs:

- Juurdepääs ühe järgmise rolli jaoks:

    - Elektroonilise aruandluse arendaja
    - Elektroonilise aruandluse funktsionaalne konsultant
    - Süsteemiadministraator

- Juurdepääs SharePoint Serverile, mis on konfigureeritud kasutamiseks rakendusega
- Juurdepääs Power BI raamistikule

## <a name="configure-document-management-parameters"></a>Dokumendihalduse parameetrite konfigureerimine
1. Lehel **Dokumendihalduse parameetrid** konfigureerige juurdepääs SharePoint Serverile, mida kasutatakse ettevõttes, kuhu olete sisse logitud (selles näites ettevõte DEMF).
2. Kontrollige ühendust SharePoint Serveriga veendumaks, et teile on antud juurdepääs.

    [![Dokumendihalduse parameetrite leht.](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)

3. Avage konfigureeritud SharePointi sait. Looge uus kaust, kuhu elektrooniline aruandlus talletab Exceli failid, millel on äriandmed, mida Power BI aruanded vajavad Power BI andmekogumite allikana.
4. Lehel **Dokumenditüübid** looge uus dokumenditüüp, mida kasutatakse äsjaloodud SharePointi kaustale juurdepääsemiseks. Sisestage **Fail** väljale **Grupp** ja **SharePoint** väljale **Asukoht** ja seejärel sisestage SharePointi kausta aadress.

    [![Dokumenditüüpide lehed.](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>Elektroonilise aruandluse parameetrite konfigureerimine
1. Tööruumis **Elektrooniline aruandlus** klõpsake linki **Elektroonilise aruandluse parameetrid**.
2. Vahekaardil **Manused** valige kõikide väljade puhul dokumendi tüübiks **Fail**.
3. Tööruumis **Elektrooniline aruandlus** tehke soovitud teenusepakkuja aktiivseks, klõpsates valikut **Aktiivsena seadistamine**. Lisateabe jaoks esitage tegevuse juhis **Elektroonilise aruandluse teenusepakkuja valimine**.

## <a name="use-an-er-data-model-as-the-source-of-data"></a>Elektroonilise aruandluse andmemudeli kasutamine andmeallikana
Power BI aruannetes kasutatavate äriandmete allikaks peab olema elektroonilise aruandluse andmemudel. See andmemudel laetakse üles elektroonilise aruandluse konfiguratsioonide hoidlast. Lisateabe jaoks vaadake [Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services](download-electronic-reporting-configuration-lcs.md) või esitage tegevuse juhis **Elektroonilise aruande konfiguratsiooni importimine teenusest Lifecycle Services** . Valige andmemudeliks **Intrastat**, mis laetakse üles valitud elektroonilise aruandluse konfiguratsioonide hoidlast. (Selles näites kasutatakse mudeli versiooni 1.) Seejärel saate lehel **Konfiguratsioonid** pääseda juurde **Intrastat** i elektroonilise aruandluse mudeli konfiguratsioonile.

[![Intrastati ER-mudeli konfiguratsioon konfiguratsioonide lehel.](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>Elektroonilise aruandluse vormingu konfiguratsiooni kujundamine
Peate looma uue elektroonilise aruandluse vormingus konfiguratsiooni, mis kasutab äriandmete allikana andmemudelit **Intrastat**. Selles vormingus konfiguratsioon peab looma väljundtulemused elektrooniliste dokumentidena OpenXML-i vormingus (Exceli fail). Lisateabe saamiseks esitage tegevuse juhis **ER-i konfiguratsiooni loomine aruannete loomiseks vormingus OPENXML**. Määrake uue konfiguratsiooni nimeks **Tegevuste importimine/eksportimine**, a Kasutage elektroonilise aruandluse vormingu kujundamisel mallina Exceli faili [Elektroonilise aruandluse andmed – impordi ja ekspordi üksikasjad](https://download.microsoft.com/download/f/7/5/f755c0fd-025c-4aa9-920b-909abb8302ad/ER-data-import-and-export-details.xlsx). (Saamaks lisateavet, kuidas vormingumalli importida, esitage tegevuse juhis.)

[![Impordi-/eksporditegevuste konfiguratsioon.](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png)

Vormingu konfiguratsiooni **Impordi-/eksporditegevused** muutmiseks järgige neid juhiseid.

1. Klõpsake valikut **Kujundaja**.
2. Vahekaardil **Vorming** nimetage selle vormingu **Exceli väljundfail** faili element.

    [![Exceli väljundfaili element.](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)

3. Vahekaardil **Vastendamine** määrake Exceli faili nimi, mis luuakse alati, kui see vorming käivitatakse. Konfigureerige seotud avaldis, et tagastada väärtus **Impordi ja ekspordi üksikasjad** (xlsx-faili nime laiend lisatakse automaatselt).

    [![Vormingu koostaja.](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)

4. Lisage selle vormingu jaoks uus andmeallika üksus. (See loetelu on vajalik täiendavaks andmete sidumist.)

    1. Nimetage andmeallikas **direction\_enum**.
    2. Valige andmeallika tüübiks **Andmemudeli loetelu**.
    3. Viidake andmemudeli loetelule **Suund**.

    [![direction_enum.](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)

5. Lõpetage andmemudeli **Intrastat** elementide ja koostatud vormingu elementide sidumine, nagu on näidatud järgmisel joonisel.

    [![Sidumise lõpuleviimine.](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

Pärast selle käivitamist loob elektroonilise aruandluse vorming Exceli vormingus väljundtulemuse. See saadab Intrastati kannete üksikasjad väljundtulemusele ja eraldab need kannetena, mis kirjeldavad impordi- ja eksporditegevusi. Klõpsake valikut **Käivita**, et testida uut elektroonilise aruandluse vormingut Intrastati kannete loendi jaoks lehel **Intrastat** (**Maks** &gt; **Deklaratsioonid** &gt; **Väliskaubandus** &gt; **Intrastat**).

[![Intrastati leht.](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png)

Luuakse järgmine väljundtulemus. Faili nimi on **Impordi ja ekspordi üksikasjad.xlsx**, nagu määrasite vormingu sätetes.

[![Impordi ja ekspordi üksikasjad.xlsx.](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>Elektroonilise aruandluse sihtkoha konfigureerimine
Peate konfigureerima elektroonilise aruandluse raamistiku, et saata uue elektroonilise aruandluse vormingu konfiguratsiooni väljundtulemus erilisel viisil.

- Väljundtulemus tuleb saata valitud SharePoint Serveri kausta.
- Iga vormingu konfiguratsiooni käivitamine peab looma samast Exceli failist uue versiooni.

Lehel **Elektrooniline aruandlus** (**Organisatsiooni haldus** &gt; **Elektrooniline aruandlus**) klõpsake üksust **Elektroonilise aruandluse sihtkoht** ja lisage uus sihtkoht. Väljal **Viide** valige varasemalt loodud vormingu konfiguratsioon **Impordi-/eksporditegevused**. Järgige neid juhiseid, et viite jaoks uus faili sihtkoha kirje lisada.

1. Väljale **Nimi** sisestage faili sihtkoha pealkiri.
2. Väljal **Faili nimi** valige Exceli faili vormingu komponendi jaoks nimi **Exceli väljundfail**.

Klõpsake uue sihtkoha kirje jaoks nuppu **Sätted**. Seejärel järgige dialoogiboksis **Sihtkoha sätted** neid juhiseid.

1. Vahekaardil **Power BI** valige suvandi **Lubatud** sätteks **Jah**.
2. Väljal **SharePoint** valige varem loodud dokumenditüüp **Jagatud**.

## <a name="schedule-execution-of-the-configured-er-format"></a>Konfigureeritud elektroonilise aruandluse vormingu käivitamise ajastamine
1. Lehel **Konfiguratsioonid** (**Organisatsiooni haldus** &gt; **Elektrooniline haldus** &gt; **Konfiguratsioonid**) konfiguratsioonide puul valige varasemalt loodud konfiguratsioon **Impordi-/eksporditegevused**.
2. Muutke versiooni 1.1 olekut variandilt **Mustand** variandile **Lõpetatud**, et muuta see vorming kasutamiseks kättesaadavaks.

    [![Konfiguratsioonide lehel tegevuste konfiguratsiooni importimine/eksportimine.](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png)

3. Valige konfiguratsiooni **Impordi-/eksporditegevused** lõpetatud versioon ja klõpsake seejärel valikut **Käivita**. Pange tähele, et konfigureeritud sihtkoht rakendatakse väljundtulemusele, mis luuakse Exceli vormingus.
4. Määrake suvandi **Pakktöötlus** sätteks **Jah**, et käivitada see aruanne järelevalveta režiimis.
5. Klõpsake valikut **Kordumine**, et ajastada selle partii käivitamise vajalik kordumine. Kordumine määratleb, kui sageli värskendatud andmeid Power BI-sse edastatakse.

    [![Elektroonilise aruande parameetrite dialoogiaken.](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png)

6. Pärast selle konfigureerimist saate leida elektroonilise aruandluse käivitamistöö lehel **Pakett-tööd** (**Süsteemihaldus &gt; Päringud &gt; Pakett-tööd**).

    [![Pakett-tööde leht.](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png)

7. Selle töö esmaskordsel käivitamisel loob sihtkoht uue Exceli faili, millel on valitud SharePointi kaustas konfigureeritud nimi. Igal järgneval korral, kui töö käivitatakse, loob sihtkoht sellest Exceli failist uue versiooni.

    [![Exceli faili uus versioon.](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>Power BI andmekogumi loomine, kasutades elektroonilise aruandluse vormingu väljundtulemust
1. Logige sisse Power BI-sse ja avage olemasolev Power BI grupp (tööruum) või looge uus grupp. Klõpsake suvandit **Lisa** menüüs **Failid** jaotises **Andmete importimine või ühendamine** või klõpsake vasakul paanil plussmärki (**+**), mis asub valiku **Andmekogumid** kõrval.

    [![Andmekogumi loomine.](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png)

2. Valige suvand **SharePoint – meeskonna saidid** ja seejärel sisestage kasutatav SharePoint Serveri tee (meie näites `https://ax7partner.litware.com`).
3. Sirvige kausta **/Shared Documents/GER data/PowerBI** ja valige Exceli fail, mille lõite andmeallikana uue Power BI andmekogumi jaoks.

    [![Exceli faili valimine.](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png)

4. Klõpsake valikut **Ühenda** ja klõpsake seejärel valikut **Impordi**. Luuakse uus andmekogum, mis põhineb valitud Exceli failil. Andmekogumi saab automaatselt värskelt loodud armatuurlauale lisada.

    [![Andmekogum armatuurlaual.](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png)

5. Konfigureerige selle andmekogumi jaoks värskendamisgraafik, et jõustada perioodilist värskendamist. Perioodilised uuendused võimaldavad elektroonilise aruandluse aruande perioodilise käivitamise kaudu tulevate uute äriandmete tarbimist ja seda SharePoint Serveris loodud Exceli faili uute versioonide kaudu.

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>Power BI aruande loomine uut andmekogumit kasutades
1. Klõpsake loodud Power BI andmekogumit **Impordi ja ekspordi üksikasjad**.
2. Konfigureerige visualiseerimine. Näiteks valige visualiseerimine **Täidetud kaart** ja konfigureerige see järgmiselt.

    - Määrake andmekogumi väli **CountryOrigin** kaardi visualiseerimise väljale **Asukoht**.
    - Määrake andmekogumi väli **Summa** kaardi visualiseerimise väljale **Värvi küllastus**.
    - Lisage andmekogumi väljad **Tegevus** ja **Aasta** kaardi visualiseerimise väljade kogumikule **Filtrid**.

3. Salvestage Power BI aruanne kui **Impordi ja ekspordi üksikasjade aruanne**.

    [![Impordi ja ekspordi üksikasjade aruanne.](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png)

    Pange tähele, et kaart näitab riike/piirkondi, mis on mainitud Exceli failis (selles näites Austria ja Šveits). Need riigid/regioonid on tehtud värviliseks, et näidata iga ühe arveldatud summade osakaalu.

4. Värskendage Intrastati kannete loendit. Itaalias pärinev ekspordikanne on lisatud.

    [![Intrastati kannete loend.](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png)

5. Oodake elektroonilise aruande järgmist plaanilist käivitamist ja Power BI andmekogumi järgmist plaanilist värskendust. Seejärel vaadake Power BI aruanne üle (valige ainult impordikannete kuvamine). Värskendatud kaart näitab nüüd Itaaliat.

    [![Värskendatud kaart.](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-finance"></a>Juurdepääs Power BI aruandele rakenduses Finance
Seadistage integreerimine lahendusega Power BI. Lisateavet vt [Power BI integreerimise konfigureerimine tööruumidele](configure-power-bi-integration.md).

1. Tööruumi lehel **Elektrooniline aruandlus**, mis toetab Power BI integratsiooni (**Organisatsiooni haldus** &gt; **Tööruumid** &gt; **Elektroonilise aruandluse tööruum**), klõpsake valikuid **Suvandid** &gt; **Aruande kataloogi avamine**.
2. Valige loodud Power BI aruanne **Impordi ja ekspordi üksikasjad**, et kuvada see aruanne valitud lehel tegevusüksusena.
3. Klõpsake tegevusüksust, et avada leht, millel kuvatakse Power BI-s loodud aruanne.

    [![Impordi ja ekspordi üksikasjade aruanne, mis on kujundatud rakenduses Power BI.](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse (ER) sihtkohad](electronic-reporting-destinations.md)

[Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
