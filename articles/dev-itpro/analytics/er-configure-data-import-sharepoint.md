---
title: Andmete SharePointist importimise konfigureerimine
description: Selles teemas selgitatakse, kuidas importida andmeid Microsoft SharePointist.
author: NickSelin
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 4285db9c71208bce45d64933e692a25ef3f46b26
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2018

---
# <a name="configure-data-import-from-sharepoint"></a>Andmete SharePointist importimise konfigureerimine

[!include[banner](../includes/banner.md)]

Andmete importimiseks sissetulevast failist, kasutades elektroonilise aruandluse (ER) raamistikku, peate konfigureerima elektroonilise aruandluse vorming, mis toetab importimist, ja seejärel käivitama tüübi **Sihtkohta**, mis kasutab seda vormingut andmeallikana, mudelivastenduse. Andmete importimiseks peate navigeerima failini, mille soovite importida. Kasutaja saab sissetuleva faili käsitsi valida. Elektroonilise aruandluse uue funktsiooniga, mis toetab andmete importimist Microsoft SharePointist, saab selle protsessi konfigureerida järelevalveta protsessina. Elektroonilise aruandluse konfiguratsioonide abil saate importida andmeid Microsoft SharePointi kaustadesse salvestatud failidest. Selles teemas selgitatakse, kuidas importida andmeid SharePointist rakendusse Microsoft Dynamics 365 for Finance and Operations. Näidetes on kasutatud äriandmetena hankija kandeid.

## <a name="prerequisites"></a>Eeltingimused
Selles teemas näidete lõpuleviimiseks peavad teil olema järgmised juurdepääsuõigused.

- Juurdepääs Finance and Operationsile ühe järgmise rolli jaoks:

    - Elektroonilise aruandluse arendaja
    - Elektroonilise aruandluse funktsionaalne konsultant
    - Süsteemiadministraator

- Juurdepääs Microsoft SharePoint Serveri eksemplarile, mis on konfigureeritud kasutamiseks Finance and Operationsiga
- 1099 maksete elektroonilise aruandluse vormingu ja mudeli konfiguratsioonid

### <a name="create-required-er-configurations"></a>Vajalike elektroonilise aruandluse konfiguratsioonide loomine
Vaadake tegevusejuhiseid **Elektrooniline aruandlus: andmete importimine Microsoft Exceli failist**, mis on osa äriprotsessist **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)**. Need tegevusejuhised tutvustavad teile elektroonilise aruandluse konfiguratsioonide kujundamise ja kasutamise protsessi hankija kannete interaktiivseks importimiseks välistest Microsoft Exceli failidest. Lisateabe saamiseks vt teemat [Sissetulevate dokumentide sõelumine Microsoft Excelis](parse-incoming-documents-excel.md). Lõpuks on teil olemas järgmised.

- Elektroonilise aruandluse konfiguratsioonid:

    - elektroonilise aruandluse mudeli konfiguratsioon **1099 maksete mudel**
    - elektroonilise aruandluse vormingu konfiguratsioon **Hankija kannete Excelist importimise vorming**

[![Elektroonilise aruandluse konfiguratsioonid andmete importimiseks SharePointist](./media/GERImportFromSharePoint-01-Configurations.PNG)](./media/GERImportFromSharePoint-01-Configurations.PNG)

- Andmete importimise sissetuleva faili näide:

    - Exceli fail **1099import-data.xlsx** koos hankija kannetega, mis tuleb Finance and Operationsisse importida

[![Microsoft Exceli näidisfail SharePointist importimiseks](./media/GERImportFromSharePoint-02-Excel.PNG)](./media/GERImportFromSharePoint-02-Excel.PNG)

> [!NOTE]
> Hankija kannete importimise vorming on valitud vaike-mudelivastendusena. Seega kui käivitate **1099 maksete mudeli** mudelivastenduse ja mudelivastenduse tüüp on **Sihtkohta**, käitab mudelivastendus seda vormingut andmete importimiseks välistest failidest. Seejärel kasutab see neid andmeid rakenduse tabelite värskendamiseks.

## <a name="configure-document-management-parameters"></a>Dokumendihalduse parameetrite konfigureerimine
1. Lehel **Dokumendihalduse parameetrid** saate konfigureerida juurdepääsu SharePoint Serveri eksemplarile, mida kasutab ettevõte, kuhu olete parajasti sisse logitud. Selles näites on ettevõte USMF.
2. Testige ühendust SharePoint Serveri eksemplariga veendumaks, et teile on antud juurdepääs.

[![Dokumendihalduse säte – SharePointi server](./media/GERImportFromSharePoint-03-SharePointSetup.png)](./media/GERImportFromSharePoint-03-SharePointSetup.png)

3. Avage konfigureeritud SharePointi sait ja looge järgmised kaustad, kuhu saab sissetulevad failid salvestada.

    - Failide impordiallikas (peamine)
    - Failide impordiallikas (alternatiivne)

[![Dokumendihalduse säte – SharePointi server](./media/GERImportFromSharePoint-04-SharePointFolder1.png)](./media/GERImportFromSharePoint-04-SharePointFolder1.png)

[![Dokumendihalduse säte – SharePointi server](./media/GERImportFromSharePoint-05-SharePointFolder2.png)](./media/GERImportFromSharePoint-05-SharePointFolder2.png)

4. Looge Finance and Operationsi lehel **Dokumenditüübid** järgmised dokumenditüübid, mida kasutatakse äsjaloodud SharePointi kaustadele juurdepääsuks.

    - SP peamine
    - SP alternatiivne

5. Sisestage loodud dokumenditüüpide puhul väljale **Rühm** sõna **Fail** ja väljale **Asukoht** sõna **SharePoint**. Seejärel sisestage SharePointi kausta aadress.

    - Dokumenditüübi **SP peamine** puhul: failide impordiallikas (peamine)
    - Dokumenditüübi **SP alternatiivne** puhul: failide impordiallikas (alternatiivne)

[![SharePointi säte – uus dokumenditüüp](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)

## <a name="configure-er-sources-for-the-er-format"></a>Elektroonilise aruandluse allikate konfigureerimine elektroonilise aruandluse vormingu jaoks
1. Klõpsake valikuid **Organisatsiooni haldus** > **Elektrooniline aruandlus** > **Elektroonilise aruandluse allikas**.
2. Lehel **Elektroonilise aruandluse allikas** saate konfigureerida andmeimpordi lähtefailid, kasutades konfigureeritud elektroonilise aruandluse vormingut.
3. Määratlege failinime mask, et imporditaks ainult xlsx-laiendiga failid. Failinime mask on valikuline ja seda kasutatakse ainult siis, kui see on määratletud. Iga elektroonilise aruandluse vormingu jaoks saate määratleda ainult ühe maski.
4. Valige mõlemad varem loodud SharePointi kaustad.

[![Elektroonilise aruandluse failide allika säte](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)

> [!NOTE]
>Elektroonilise aruandluse *allikas* määratletakse iga rakenduse ettevõtte puhul eraldi. Elektroonilise aruandluse *konfiguratsioonid* on aga ettevõtete vahel ühiskasutatavad.

> [!NOTE]
> Kui kustutate elektroonilise aruandluse vormingu elektroonilise aruandluse allika sätte, kustutatakse ka kõik ühendatud faili olekud (vt allpool).

## <a name="review-the-files-states-for-the-er-format"></a>Elektroonilise aruandluse failide olekute ülevaatamine
1. Valige lehel **Elektroonilise aruandluse allikas** suvand **Allikate failiolekud**, et vaadata praeguse elektroonilise aruandluse vormingu puhul konfigureeritud failiallikad üle.
2. Jaotises **Failid** vaadake failide loend üle. See loend kujutab järgmist.

    - Failinime maski põhjal (kui failinime mask on määratletud) kohalduvad ja andmeimpordiks valmis lähtefailid. Nende failide puhul on jaotis **Impordivormingu allikate logi** tühi.
    - Varem imporditud failid. Iga faili puhul saate jaotises **Impordivormingu allikate logi** vaadata üle selle faili importimise ajaloo.

Saate lehe **Allikate failiolekud** avada ka, valides suvandid **Organisatsiooni haldus** \> **Elektrooniline aruandlus** \> **Allikate failiolekud**. Sellisel juhul annab leht teavet failiallikate kohta kõigi elektroonilise aruandluse vormingute puhul, mille jaoks on failiallikad ettevõttes, millesse olete parajasti sisse logitud, konfigureeritud.

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a>Andmete importimine SharePointi kaustas olevatest Exceli failidest
1. Laadige SharePointis hankija kandeid sisaldav Microsoft Exceli fail **1099import-data.xlsx** üles varem loodud SharePointi kausta **Failide impordiallikas (peamine)**.

[![SharePointi sisu – imporditav Microsoft Exceli fail](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)

2. Valige Finance and Operationsis lehel **Allikate failiolekud** suvand **Värskenda**, et lehte värskendada. Pange tähele, et SharePointi üleslaaditud Exceli fail kuvatakse sellel vormil olekuga **Valmis**. Praegu toetatakse järgmisi olekuid.

    - **Valmis** – määratakse automaatselt igale uuele failile SharePointi kaustas. See olek tähendab, et fail on importimiseks valmis.
    - **Importimine** – selle määrab automaatselt elektroonilise aruandluse aruanne, kui impordiprotsess on faili lukustanud, et takistada selle kasutamist teistes protsessides (kui neid töötab korraga mitu).
    - **Imporditud** – selle määrab automaatselt elektroonilise aruandluse aruanne, kui faili importimine on edukalt lõpule viidud. See olek tähendab, et imporditud fail on konfigureeritud failide allikast (SharePointi kaustast) kustutatud.
    - **Nurjunud** – selle määrab automaatselt elektroonilise aruandluse aruanne, kui faili importimine on lõpule viidud tõrgete või eranditega.
    - **Ootel** – selle määrab kasutaja vormil käsitsi. See olek tähendab, et faili praegu ei impordita. Seda olekut saab kasutada mõne faili importimise edasilükkamiseks.

[![Elektroonilise aruandluse failiolekute leht valitud allikate puhul](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)

## <a name="import-data-from-sharepoint-files"></a>Andmete importimine SharePointi failidest
1. Avage elektroonilise aruandluse puu, valige suvand **1099 maksete mudel** ja laiendage elektroonilise aruandluse komponentide loend.
2. Valige mudelivastenduse nimi, et avada valitud elektroonilise aruandluse mudeli konfiguratsiooni mudelivastenduste loend.

[![Elektroonilise aruandluse failiolekute leht valitud allikate puhul](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)

3. Valitud mudelivastenduse käivitamiseks valige käsk **Käivita**. Kuna konfigureerisite elektroonilise aruandluse vormingu failiallikaid, saate suvandi **Failiallikas** sätet soovitud viisil muuta. Kui säilitate selle suvandi sätte, imporditakse xlsx-failid konfigureeritud allikatest (selles näites SharePointi kaustadest).

    Selles näites impordite ainult ühe faili. Kui aga faile on mitu, valitakse need importimiseks järjekorras, milles need SharePointi kausta lisati. Iga elektroonilise aruandluse vormingu käitamine impordib ühe valitud faili.

[![Elektroonilise aruandluse mudelivastenduse käitamine](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)

4. Mudelivastendust saab käitada pakettrežiimis järelevalveta. Sellisel juhul imporditakse igal selle elektroonilise aruandluse vormingu pakettkäitusel üks fail konfigureeritud failiallikatest. Kasutage selle pakettkäituse juurutamiseks järgmist koodi.

    ```
    ERObjectsFactory::createMappingDestinationRunByImportFormatMappingId().run()
    ```

    Kui fail on SharePointi kaustast edukalt imporditud, kustutatakse see sellest kausta.

5. Sisestage kande ID, nt **V-00001**, ja seejärel valige **OK**.

[![Elektroonilise aruandluse mudelivastenduse käitamine](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)

6. Valige lehel **Allikate failiolekud** suvand **Värskenda**, et lehte värskendada.

[![Elektroonilise aruandluse failiolekute leht valitud allikate puhul](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)

7. Jaotises **Failid** vaadake failide loend üle. Jaotises **Impordivormingu allikate logi** kuvatakse Exceli faili importimise ajalugu. Kuna see fail on edukalt imporditud, on see SharePointi kaustas märkega **Kustutatud**.
8. Vaadake üle SharePointi kaust **Failide impordiallikas (peamine)**. Edukalt imporditud Exceli failid on sellest kaustast kustutatud.
9. Valige Finance and Operationsis suvandid **Ostureskontro** \> **Perioodilised ülesanded** \> **Maks 1099** \> **Hankija tasakaalustus 1099 jaoks**.
10. Sisestage väljadele **Alguskuupäev** ja **Lõppkuupäev** asjakohased väärtused. Seejärel valige suvand **Manuaalsed 1099 kanded**.

    Lehel kuvatakse kande puhul **V-00001** SharePointis olevatest Exceli failidest imporditud hankija kanded.

[![1099 hankija kannete leht](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)

## <a name="prepare-an-excel-file-for-import"></a>Exceli faili ettevalmistamine importimiseks
1. Avage Exceli fail, mida varem kasutasite. Lisage 3. rea 1. veergu hankija kood, mida rakenduses olemas ei ole. Lisage reale täiendav vale hankija teave.

[![Microsoft Exceli näidisfail SharePointist importimiseks](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)

2. Laadige hankija kandeid sisaldav värskendatud Exceli fail üles SharePointi kausta **Failide impordiallikas (peamine)**.
3. Avage Finance and Operationsis elektroonilise aruandluse puu, valige suvand **1099 maksete mudel** ja laiendage elektroonilise aruandluse komponentide loend.
4. Valige mudelivastenduse nimi, et värskendada mudelivastendust nii, et andmete impordiprotsessi käigus käsitletaks vale hankija koodi tõrkena.
5. Valige **Kujundaja**.
6. Vahekaardil **Kinnitused** peate muutma konfigureeritud kinnitamisreegli kinnitamisjärgset tegevust, et hinnata, kas imporditud hankija konto on rakenduses olemas. Värskendage välja **Kinnitusjärgne tegevus** väärtus valikule **Peata täitmine**, salvestage muudatused ja sulgege leht.

[![Elektroonilise aruandluse mudelivastenduse kujundaja leht](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)

7. Salvestage muudatused ja sulgege elektroonilise aruandluse mudelivastenduse kujundaja.
8. Muudetud elektroonilise aruandluse mudelivastenduse käivitamiseks valige käsk **Käivita**.
9. Sisestage kande ID, nt **V-00002**, ja seejärel valige **OK**.

    Pange tähele, et teabelogi sisaldab teatist selle kohta, et SharePointi kaustas asuv fail sisaldab vale hankija kontot ja seda ei saa importida.

[![Elektroonilise aruandluse mudelivastenduse käitamine](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)

10. Valige lehel **Allikate failiolekud** suvand **Värskenda** ja siis vaadake jaotises **Failid** faililoend üle.

[![Elektroonilise aruandluse failiolekute leht valitud allikate puhul](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)

Jaotises **Impordivormingu allikate logi** on näidatud, et impordiprotsess nurjus ja fail on endiselt SharePointi kaustas (ruut **On kustutatud** on märkimata). Kui parandate selle faili SharePointis, lisades õige hankija koodi, ja seejärel muudate faili oleku jaotises **Impordivormingu allikate logi** väärtuselt **Nurjunud** väärtusele **Valmis**, saate faili uuesti importida.

11. Vaadake üle SharePointi kaust **Failide impordiallikas (peamine)**. Pange tähele, et Excel fail, mida ei imporditud, on selles kaustas endiselt alles.
12. Valige Finance and Operationsis suvandid **Ostureskontro** \> **Perioodilised ülesanded** \> **Maks 1099** \> **Hankija tasakaalustus 1099 jaoks**, sisestage väljadele **Alguskuupäev** ja **Lõppkuupäev** asjakohased väärtused ning siis valige suvand **Manuaalsed 1099 kanded**.

    Saadaval on ainult kanded kandele V-00001. Kandele V-00002 ei ole kandeid saadaval, kuigi Exceli failis leiti viimati imporditud kande tõrge.

