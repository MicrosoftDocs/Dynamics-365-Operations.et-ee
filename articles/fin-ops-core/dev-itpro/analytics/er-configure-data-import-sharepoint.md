---
title: SharePointist andmete importimise konfigureerimine
description: See artikkel selgitab, kuidas Microsoftist andmeid importida SharePoint.
author: kfend
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: 11208267de0cc35db55c64ccf2de224df854404d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277782"
---
# <a name="configure-data-import-from-sharepoint"></a>SharePointist andmete importimise konfigureerimine

[!include[banner](../includes/banner.md)]

Andmete importimiseks sissetulevast failist, kasutades elektroonilise aruandluse (ER) raamistikku, peate konfigureerima elektroonilise aruandluse vorming, mis toetab importimist, ja seejärel käivitama tüübi **Sihtkohta**, mis kasutab seda vormingut andmeallikana, mudelivastenduse. Andmete importimiseks peate navigeerima failini, mille soovite importida. Kasutaja saab sissetuleva faili käsitsi valida. Elektroonilise aruandluse uue funktsiooniga, mis toetab andmete importimist Microsoft SharePointist, saab selle protsessi konfigureerida järelevalveta protsessina. Elektroonilise aruandluse konfiguratsioonide abil saate importida andmeid Microsoft SharePointi kaustadesse salvestatud failidest. See artikkel selgitab, kuidas importimist lõpetada SharePoint. Näidetes on kasutatud äriandmetena hankija kandeid.

## <a name="prerequisites"></a>Eeltingimused
Selle artikli näidete lõpetamiseks peab teil olema järgmine juurdepääs:

- Juurdepääs üheöe järgmistest rollidest:

    - Elektroonilise aruandluse arendaja
    - Elektroonilise aruandluse funktsionaalne konsultant
    - Süsteemiadministraator

- Juurdepääs Microsoft SharePoint Serveri eksemplarile, mis on konfigureeritud kasutamiseks rakendusega.
- 1099 makse elektroonilise aruandluse vormingu ja mudeli konfiguratsioonid.

### <a name="create-required-er-configurations"></a>Vajalike elektroonilise aruandluse konfiguratsioonide loomine
Vaadake tegevusjuhiseid **Elektrooniline aruandlus: andmete importimine Microsoft Exceli failist**, mis on osa äriprotsessist **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)**. Need tegevusjuhised tutvustavad elektroonilise aruandluse konfiguratsioonide kujundamise ja kasutamise protsessi hankija kannete interaktiivseks importimiseks Microsoft Exceli failidest. Lisateavet vt [Sissetulevate dokumentide sõelumine Exceli vormingus](parse-incoming-documents-excel.md). Pärast tegevusjuhiste täitmist on teil järgmised seadistused.

#### <a name="er-configurations"></a>Elektroonilise aruandluse konfiguratsioonid

- elektroonilise aruandluse mudeli konfiguratsioon **1099 maksete mudel**
- elektroonilise aruandluse vormingu konfiguratsioon **Hankija kannete Excelist importimise vorming**

![Elektroonilise aruandluse konfiguratsioonid andmete importimiseks rakendusest SharePoint.](./media/GERImportFromSharePoint-01-Configurations.PNG)

#### <a name="sample-of-the-incoming-file-for-data-import"></a>Andmete importimise sissetuleva faili näide

- Exceli fail **1099import-data.xlsx** koos hankija kannetega, mis tuleb importida.

![Exceli näidisfail rakendusest SharePoint importimiseks.](./media/GERImportFromSharePoint-02-Excel.PNG)
    
> [!NOTE]
> Hankija kannete importimise vorming on valitud vaike-mudelivastendusena. Seega kui käivitate **1099 maksete mudeli** mudelivastenduse ja mudelivastenduse tüüp on **Sihtkohta**, käitab mudelivastendus seda vormingut andmete importimiseks välistest failidest. Seejärel kasutab see neid andmeid rakenduse tabelite värskendamiseks.

## <a name="configure-access-to-sharepoint-for-file-storage"></a>SharePointile juurdepääsu konfigureerimine failitalletuseks
Elektroonilise aruande failide talletamiseks SharePointi asukohas tuleb konfigureerida juurdepääs praeguses ettevõttes kasutatavale SharePointi Serveri eksemplarile. Selles näites on ettevõte USMF. Juhiseid vt teemast [SharePointi salvestusruumi konfigureerimine](../../fin-ops/organization-administration/configure-document-management.md#configure-sharepoint-storage).

1. Järgige juhiseid jaotises teemas [SharePointi salvestusruumi konfigureerimine](../../fin-ops/organization-administration/configure-document-management.md#configure-sharepoint-storage).
2. Avage konfigureeritud SharePointi sait.
3. Looge sissetulevate elektrooniliste aruandluse failide talletamiseks järgmised kaustad:

     - Failide importimine allikas (põhi) (nt pildil)
     - Failide impordiallikas (alternatiivne)

    ![Failide impordiallikas (peamine).](./media/GERImportFromSharePoint-04-SharePointFolder1.png)

4. (Valikuline) Looge järgmised kaustad, et talletada faile pärast importimist. 

    - Failide arhiivikausta – See kaust oleks edukalt imporditud failide jaoks.
    - Failide hoiatuskaust - See kaust oleks failide jaoks, mille importimisel anti hoiatus.
    - Failide veakaust – See kaust oleks failide jaoks, mida ei saanud importida.

4. Avage **Organisatsiooni haldus > Dokumendihaldus > Dokumenditüübid**.
5. Looge dokumenditüübid, mida kasutatakse loodud SharePointi kaustadele juurdepääsuks. Lisateabe saamiseks vaadake [Dokumenditüüpide konfigureerimine](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types).

|Dokumendi tüüp        | Grupeeri              | Koht      | SharePointi kaust      |
|--------------------|--------------------|---------------|------------------------|
|SP peamine             |Fail                |SharePoint     |Failide impordiallikas (peamine)|
|SP alternatiivne             |Fail                |SharePoint     |Failide impordiallikas (alternatiivne)|
|SP arhiiv             |Fail                |SharePoint     |Failide arhiivikaust|
|SP hoiatus             |Fail                |SharePoint     |Failide hoiatuste kaust|
|SP tõrge             |Fail                |SharePoint     |Failide veakaust|

![SharePoint säte – uus dokumenditüüp.](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)

## <a name="configure-er-sources-for-the-er-format"></a>Elektroonilise aruandluse allikate konfigureerimine elektroonilise aruandluse vormingu jaoks
1. Klõpsake valikuid **Organisatsiooni haldus** \> **Elektrooniline aruandlus** \> **Elektroonilise aruandluse allikas**.
2. Lehel **Elektroonilise aruandluse allikas** saate konfigureerida andmeimpordi lähtefailid, kasutades konfigureeritud elektroonilise aruandluse vormingut.
3. Määratlege failinime mask, et imporditaks ainult xlsx-laiendiga failid. Failinime mask on valikuline ja seda kasutatakse ainult siis, kui see on määratletud. Iga elektroonilise aruandluse vormingu jaoks saate määratleda ainult ühe maski.
4. Muutke valikut **Failide sorteerimine enne importimist** – **Mitte sorteerida**, kui teil on importimiseks mitu faili ja importimise järjekord pole oluline
5. Valige kõik varem loodud SharePointi kaustad.

    [![Elektroonilise aruandluse failide allika säte.](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)

> [!NOTE]
> - Elektroonilise aruandluse *allikas* määratletakse iga rakenduse ettevõtte puhul eraldi. Elektroonilise aruandluse *konfiguratsioonid* on aga ettevõtete vahel ühiskasutatavad.
> - Kui kustutate elektroonilise aruandluse vormingu elektroonilise aruandluse allika sätte, kinnitate, et kustutatakse ka kõik ühendatud faili olekud (vt allpool).

## <a name="review-the-files-states-for-the-er-format"></a>Elektroonilise aruandluse failide olekute ülevaatamine
1. Valige lehel **Elektroonilise aruandluse allikas** suvand **Allikate failiolekud**, et vaadata praeguse elektroonilise aruandluse vormingu puhul konfigureeritud failiallikad üle.
2. Jaotises **Failid** vaadake failide loend üle. See loend kujutab järgmist.

    - Failinime maski põhjal (kui failinime mask on määratletud) kohalduvad ja andmeimpordiks valmis lähtefailid. Nende failide puhul on jaotis **Impordivormingu allikate logi** tühi.
    - Varem imporditud failid. Iga faili puhul saate jaotises **Impordivormingu allikate logi** vaadata üle selle faili importimise ajaloo.

Saate lehe **Allikate failiolekud** avada ka, valides suvandid **Organisatsiooni haldus** \> **Elektrooniline aruandlus** \> **Allikate failiolekud**. Sellisel juhul annab leht teavet failiallikate kohta kõigi elektroonilise aruandluse vormingute puhul, mille jaoks on failiallikad ettevõttes, millesse olete parajasti sisse logitud, konfigureeritud.

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a>Andmete importimine SharePointi kaustas olevatest Exceli failidest
1. Laadige SharePointis hankija kandeid sisaldav Microsoft Exceli fail **1099import-data.xlsx** üles varem loodud SharePointi kausta **Failide impordiallikas (peamine)**.

    [![SharePoint`i sisu – imporditav Microsoft Excel`i fail.](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)

2. Valige lehel **Allikate failiolekud** suvand **Värskenda**, et lehte värskendada. SharePointi üleslaaditud Exceli fail kuvatakse sellel lehel olekuga **Valmis**. Praegu toetatakse järgmisi olekuid.

    - **Valmis** – määratakse automaatselt igale uuele failile SharePointi kaustas. See olek tähendab, et fail on importimiseks valmis.
    - **Importimine** – selle määrab automaatselt elektroonilise aruandluse aruanne, kui impordiprotsess on faili lukustanud, et takistada selle kasutamist teistes protsessides (kui neid töötab korraga mitu).
    - **Imporditud** – selle määrab automaatselt elektroonilise aruandluse aruanne, kui faili importimine on edukalt lõpule viidud. See olek tähendab, et imporditud fail on konfigureeritud failiallikast (SharePointi kaustast) kustutatud.
    - **Nurjunud** – selle määrab automaatselt elektroonilise aruandluse aruanne, kui faili importimine on lõpule viidud tõrgete või eranditega.
    - **Ootel** – selle määrab kasutaja lehel käsitsi. See olek tähendab, et faili praegu ei impordita. Seda olekut saab kasutada mõne faili importimise edasilükkamiseks.

    [![Värskendatud elektroonilise aruandluse failiolekute leht valitud allikate puhul.](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)

## <a name="import-data-from-sharepoint-files"></a>Andmete importimine SharePointi failidest
1. Avage elektroonilise aruandluse puu, valige suvand **1099 maksete mudel** ja laiendage elektroonilise aruandluse komponentide loend.
2. Valige mudelivastenduse nimi, et avada valitud elektroonilise aruandluse mudeli konfiguratsiooni mudelivastenduste loend.

    [![Konfigureerimise leht.](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)

3. Valitud mudelivastenduse käivitamiseks valige käsk **Käivita**. Kuna konfigureerisite elektroonilise aruandluse vormingu failiallikaid, saate suvandit **Failiallikas** sätet vajadusel muuta. Kui säilitate selle suvandi sätte, imporditakse xlsx-failid konfigureeritud allikatest (selles näites SharePointi kaustadest).

    Selles näites impordite ainult ühe faili. Kui aga faile on mitu, valitakse need importimiseks järjekorras, milles need SharePointi kausta lisati. Iga elektroonilise aruandluse vormingu käitamine impordib ühe valitud faili.

    [![SharePoint`ist importimine ja ER-i mudeli vastendamise käitamine.](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)

4. Mudelivastendust saab käitada pakettrežiimis [järelevalveta](#limitations). Sellisel juhul imporditakse igal selle elektroonilise aruandluse vormingu pakettkäitusel üks fail konfigureeritud failiallikatest.

    Kui fail on SharePointi kaustast edukalt imporditud, kustutatakse see sellest kaustast ja teisaldatakse edukalt imporditud failide kausta või hoiatustega imporditud failide kausta. Vastasel juhul teisaldatakse see nurjunud failide kausta või jääb kausta siis, kui nurjunud failide kaust ei ole häälestatud. 

5. Sisestage kande ID, nt **V-00001**, ja seejärel valige **OK**.

    [![Elektroonilise aruandluse mudelivastenduse käitamine.](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)

6. Valige lehel **Allikate failiolekud** suvand **Värskenda**, et lehte värskendada.

    [![Allikalehe elektroonilise aruandluse failiolekud.](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)

7. Jaotises **Failid** vaadake failide loend üle. Jaotises **Impordivormingu allikate logi** kuvatakse Exceli faili importimise ajalugu. Kuna see fail on edukalt imporditud, on see SharePointi kaustas märkega **Kustutatud**.
8. Vaadake üle SharePointi kaust **Failide impordiallikas (peamine)**. Edukalt imporditud Exceli failid on sellest kaustast kustutatud.
9. Valige **Ostureskonto** \> **Perioodilised ülesanded** \> **Maksu 1099** \> **Hankija tasakaalustus 1099 jaoks**.
10. Sisestage väljadele **Alguskuupäev** ja **Lõppkuupäev** asjakohased väärtused. Seejärel valige suvand **Manuaalsed 1099 kanded**.

    Lehel kuvatakse kande **V-00001** puhul SharePointis olevatest Exceli failidest imporditud hankija kanded.

    [![1099 hankija kannete leht.](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)

## <a name="prepare-an-excel-file-for-import"></a>Exceli faili ettevalmistamine importimiseks
1. Avage Exceli fail, mida varem kasutasite. Lisage 3. rea 1. veergu hankija kood, mida rakenduses olemas ei ole. Lisage reale täiendav vale hankija teave.

    [![Näidis Microsoft Excel fail SharePoint`ist importimiseks.](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)

2. Laadige hankija kandeid sisaldav värskendatud Exceli fail üles SharePointi kausta **Failide impordiallikas (peamine)**.
3. Avage elektroonilise aruandluse puu, valige suvand **1099 maksete mudel** ja laiendage elektroonilise aruandluse komponentide loend.
4. Valige mudelivastenduse nimi, et värskendada mudelivastendust nii, et andmete impordiprotsessi käigus käsitletaks vale hankija koodi tõrkena.
5. Valige **Kujundaja**.
6. Vahekaardil **Kinnitused** peate muutma konfigureeritud kinnitamisreegli kinnitamisjärgset tegevust, et hinnata, kas imporditud hankija konto on rakenduses olemas. Värskendage välja **Kinnitusjärgne tegevus** väärtus valikule **Peata täitmine**, salvestage muudatused ja sulgege leht.

    [![ER-i mudelivastenduse koostaja leht.](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)

7. Salvestage muudatused ja sulgege elektroonilise aruandluse mudelivastenduse kujundaja.
8. Muudetud elektroonilise aruandluse mudelivastenduse käivitamiseks valige käsk **Käivita**.
9. Sisestage kande ID, nt **V-00002**, ja seejärel valige **OK**.

    Teabelogi sisaldab teatist selle kohta, et SharePointi kaustas asuv fail sisaldab vale hankija kontot ja seda ei saa importida.

    [![Lõpetatud elektroonilise aruandluse mudelivastenduse käitamine.](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)

10. Valige lehel **Allikate failiolekud** suvand **Värskenda** ja siis vaadake jaotises **Failid** faililoend üle.

    [![Elektroonilise aruandluse failiolekute leht valitud allikate puhul.](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)

   Jaotises **Impordivormingu allikate logi** on näidatud, et impordiprotsess nurjus ja fail on endiselt SharePointi failide veakaustas (ruut **On kustutatud** on märkimata). Kui parandate selle faili SharePointis, lisades õige hankija koodi, ja seejärel teisaldate selle SharePointi kausta Failide impordiallikas (peamine), saate faili uuesti importida.

11. Valige suvandid **Ostureskontro** \> **Perioodilised ülesanded** \> **Maks 1099** \> **Hankija tasakaalustus 1099 jaoks**, sisestage väljadele **Alguskuupäev** ja **Lõppkuupäev** asjakohased väärtused ning siis valige suvand **Manuaalsed 1099 kanded**.

    Saadaval on ainult kanded kandele V-00001. Kandele V-00002 ei ole kandeid saadaval, kuigi Exceli failis leiti viimati imporditud kande tõrge.

## <a name=""></a><a name="limitations">Kitsendused</a>

Dynamics 365 Finance versioonides enne versiooni 10.0.25 ei paku ER frameworki kasutajaliides uut pakett-tööd, mis käivitab andmete importimise mudelivastenduse režiimis. Selle asemel peate välja arendama uue loogika, nii et konfigureeritud ER-mudeli vastendust saab kutsuda rakenduse kasutajaliidesest andmete importimiseks sissetulevadest failidest. Selle loogika arendamiseks on vaja mõnda tehnikatööd. 

Lisateavet vastava ER API kohta vt koodist, [...](er-apis-app73.md#code-to-run-a-format-mapping-for-data-import)[et käivitada andmete impordi vormingu vastendamine ER-i raamistiku API muudatustes rakenduse värskenduse 7.3 jaoks](er-apis-app73.md). Vaadake kood läbi klassi `BankImport_RU` mudelis `Application Suite`, et näha, kuidas teie kohandatud loogikat saab rakendada. Klass `BankImport_RU` laiendab `RunBaseBatch` klassi. Täpsemalt, vaadake üle `runER()` meetod, kus `ERIModelMappingDestinationRun` objekt luuakse ER-mudeli vastenduse objektina.

Finantsversioonis 10.0.25 ja uuemas versioonis pakub ER framework UI võimalust käivitada uus pakett-töö, mille puhul käivitatakse andmete importimise mudelvastendus režiimis, mis pole kohustuslik. Lisateavet selle protsessi kohta vt partiirežiimis [andmete importimine käsitsi valitud failidest](er-configure-data-import-batch.md).

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)

[ER-i raamistiku API muudatused rakenduse värskenduse 7.3 puhul](er-apis-app73.md)

[ER-i raamistiku API muudatused rakenduse värskenduse 10.0.23 puhul](er-apis-app10-0-23.md)

[ER-i raamistiku API muudatused rakenduse värskenduse 10.0.25 puhul](er-apis-app10-0-25.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
