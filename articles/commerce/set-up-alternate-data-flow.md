---
title: Soovituste jaoks alternatiivse andmevoo seadistamine
description: See artikkel kirjeldab, kuidas konfigureerida keskkonda, kasutades alternatiivset andmevoogu soovituste teenusele andmete andmiseks.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: b507b9bb57c68aca9424b53f8ccc009efea733bc
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460102"
---
# <a name="set-up-an-alternate-dataflow-for-recommendations"></a>Soovituste jaoks alternatiivse andmevoo seadistamine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas konfigureerida keskkonda, kasutades alternatiivset andmevoogu soovituste teenusele andmete andmiseks.

## <a name="comparison-of-out-of-the-box-dataflow-with-alternate-dataflow"></a>Boksist väljamineku andmete voo võrdlemine alternatiivse andmevooga

Järgmine näide kirjeldab boksist väljas asuvat andmevoogu keskkonnas.

![Karbist väljas andmete voog keskkonnas](media/reco-out-of-the-box-dataflow-2.png)

Järgmine näide kirjeldab alternatiivset andmevoogu, kus üksuse poe sünkroonimise pakett-töö asendatakse alternatiivsete andmevoo etappidega.

![Alternatiivne andmevoog keskkonnas](media/reco-alternate-dataflow-2.png)

## <a name="assumptions"></a>Eeldused

- See artikkel eeldab, et olete juba lubanud oma keskkonnas soovituste teenuse. Lisateavet vt Luba [tootesoovitused](enable-product-recommendations.md).
- Failide ja kaustadega töötamisel Microsoft Azure data storage account:

    - Saate kasutada kas Azure’i veebiportaali liidest või Azure Storage Exploreri rakendust.
    - Failide ja kaustadega töötamise alguspunktid **on dynamics365-financeandoperations ümbrises, mis asub kaustas**, mille nimi vastab teie keskkonna URL-le.
    - Kui teie kausta keskkonna nimi on **MyUAT**, on keskkonna baas-URL `myuat.sandbox.operations.dynamics.com`.
    - Kui sama mälukontoga on ühendatud mitu keskkonda, on igal keskkonnal oma juurkaust.

## <a name="prerequisites"></a>Eeltingimused

Enne alternatiivse andmevoo lähenemist peavad olema täidetud järgmised eeltingimused.

### <a name="set-up-microsoft-power-platform"></a>Microsoft Power Platform-i häälestamine

Selle seadistamiseks Microsoft Power Platform järgige juhiseid funktsiooni Luba [Microsoft Power Platform integreerimine.](../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md)

### <a name="install-the-export-to-data-lake-add-in"></a>Installige lisandmoodul Export to Data Lisamised

Add-ina DataArvutisse eksportimise installimiseks [järgige juhendit "Install Export to Azure Data Azure Data Azure" lisandmoodulis](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

> [!NOTE]
> Märkige konfiguratsiooniväärtused üles, sest teil on vaja neid mõnede järgnevate sammude jaoks.

### <a name="configure-tables-to-export-in-dynamics-365"></a>Dynamics 365-is eksporditabelite konfigureerimine

Tabeli sünkroonimist Dynamics 365-st Azure Data Lake Storage hallatakse lehel **Andmete eksportimine**. Kuna sellel lehel pole praegu menüükäsku, saavad seda avada ainult süsteemiadministraatori **turberollis** kasutajad.

Dynamics 365-s eksporditabelite konfigureerimiseks järgige neid samme.

1. Lehe Ekspordi **andmetesse avamiseks** lisage string `?mi=DataFeedsDefinitionWorkspace` keskkonna baas-URL-i, nagu näha järgmises näites.

    `https://<environment-URL>/?mi=DataFeedsDefinitionWorkspace`

1. **Leheküljel Ekspordi andmetesse Ja** kopeerige [tabelid, mis on loetletud selle artikli jaotises RetailSales kuubitabelite](#list-of-retailsales-cube-tables) loend.
1. Laiendage **veerus Süsteemi** nimi filtrisuvandite loendit.
1. Valige filtritüübi jaoks **üks neist**. Seejärel asetage kursor tekstiboksi ja kleepige tabelite loend, mille **kopeerisite leheküljelt Ekspordi andmete loendisse**.
1. Valige filtrisuvandite loendi allosas suvand **Rakenda**.
1. Valige ruudustikus kõik read ja seejärel **aktiveeri**.

> [!NOTE]
> Enne järgmisele sammule liikumisel tuleb kõik read uuendada olekusse **Käita**. Tehke tõrkeotsing ja lahendage mis tahes tõrked vastavalt vajadusele.

### <a name="create-a-synapse-workspace"></a>Sünapse tööruumi loomine

Kui teil veel üht tööruumi pole, [järgige Sünapse tööruumi loomiseks Kiirkäivitus juhiseid: looge Sünonapse tööruum](/azure/synapse-analytics/quickstart-create-workspace).

Oma Azure’i ressursside organiseerimiseks soovitame teil panna Seliinuse ressursigrupis Koos The Workspace’i ladustamise konto ja Synapse’iga tööruum kokku. Saate taaskasutada ladustuskontot, mille lõite add-ina Andmete eksportimine installimisel.

## <a name="create-a-database-in-synapse-for-recommendation-data-processing"></a>Andmebaasi loomine Synapse’i soovitusandmete töötlemiseks

Utiliidi Common Data Model konsoolrakenduse (CDMUtil_ConsoleApp) abil saate luua andmebaasi oma Sünapse tööruumis ja asustada selle DataExi laoala üldandmete mudeli tabelitest. Soovitame laiendite puhul kasutada koos andmebaasiga ühise andmemudeli utiliiti arenduskeskkonnas.

> [!NOTE]
> Järgmised sammud eeldavad, et rakenduse RetailSales kuubile ei lisata laiendusandmeid.

Andmebaasi loomiseks Sünapse’s järgige neid samme.

1. Minge Dynamics-365-FastTrack-Implementation-Assets [GitHub’i](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Analytics/CDMUtilSolution#2-cdmutil-console-app) ja **järgige faili CDMUtilConsoleApp.zip allalaadimise** samme.
1. Ekstraktige sihtfail kohalikku kausta.
1. Avage tekstiredaktoris **fail CDMUtil_ConsoleApp.dll.config** ja uuendage järgmised väärtused:

    1. Määrake rentniku **ID väärtus** (Azure’i rentniku ID).
    1. Seadistage **pääsuvõtme** väärtus (Laokonto Data Storage account pääsuvõti).

        1. Avage Azure’i portaalis ladustamiskonto.
        1. Valige menüüst lehe vasakul poolel **pääsuvõtmed**.
        1. Lehe ülaosas valige näita **võtmeid**.
        1. Valige kopeerimisnupp ühele kahest võtmeväljast ja seejärel kleepige väärtus konfiguratsioonifailis topeltjutumärkide vahele.

    1. Seadke manifestURL-väärtus **oma** faili Tables.manifest.cdm.json **URL-ile**.Azure Data Lake Storage URL-i hankimiseks sirvige failiNi Azure’i portaalis, valige ellips (**...**) vaate paremal küljel ja seejärel valige **Atribuudid**. URL on esimene atribuut, mis kuvatakse vahekaardil **Ülevaade**.
    1. Seadke TargetDbConnectionString **väärtuseks** ühendusstring teie Synapse tööruumi integreeritud SQL-i serverita SQL-i väljale.

        1. Valige Sünapse’i tööruumis vahekaart **Haldamine**.
        1. Valige alammenüüst SQL-i **poolsed**.
        1. Valige kausta **atribuutide** vaatamiseks integreeritud nimi.
        1. Valige atribuutide dialoogiboksis ADO.NET ühenduse tüüp, mida soovite kasutada. Seejärel kopeerige ühenduse stringi väärtus ja kleepige see konfiguratsioonifailis kahekordsete jutumärkide vahele.

        > [!NOTE]
        > Teil peab olema luba andmebaaside loomiseks. Kasutamise lihtsustamiseks võite soovida kasutada integreeritud administraatorikontot **sqladminuser**.

    1. Eemaldage üksuse ProcessEntities **sõlm ja seadke selle väärtus tõeseks** **(nt**).`<add key="ProcessEntities" value ="true"/>`

1. Salvestage ja sulgege **fail CDMUtil_ConsoleApp.dll.config**.
1. Kopeerige **fail EntityList.json** kausta **/Manifest**.
1. Käsuviibaaknas käivitage fail **cdmutil_consoleapp.exe**.

> [!NOTE]
> Väljundi läbivaatamisel peaks olema 35 olemit/vaadet, vähemalt 75 tabelit ja tõrkeid mitte.

## <a name="prepare-the-data-lake-retailsales-aggregate-measurements-directory"></a>Jaemüügi retailSales liitmõõtude kausta ettevalmistamine

### <a name="back-up-your-current-retailsales-cube-data-from-data-lake-storage"></a>Varundage praeguse rakenduse RetailSales kuubi andmed andmete salvestist

Hõlpsaim viis praeguse rakenduse RetailSales **kuubi andmete varundamiseks on kataloogi RetailSales** ümbernimetamine rakenduse Data Storage **RetailSales-backup** abil või midagi sarnast. See meetod säilitab olemasolevad andmed juhul, kui hiljem on vaja tõrkeotsingut.

Kuubi **RetailSales** kausta leiate järgmisest asukohast:

`<storage-account>/dynamics365-financeandoperations/<environment-url (for example, myuat.sandbox.operations.dynamics.com)>/AggregateMeasurements/RetailSales`

### <a name="create-a-new-retailsales-folder-and-upload-the-model-file"></a>Looge uus kaust RetailSales ja laadige üles mudelifail.

Uue kataloogi **RetailSales loomiseks** ja **faili model.json** üles laadimiseks andmete ladustamiseks järgige neid samme.

1. Looge uus tühi kaust eelmise kaustaga samal tasemel ja nimetage see **RetailSalesiks**.
1. Laadige fail **model.json** üles uude kausta.

## <a name="create-a-pipeline-to-copy-the-retailsales-cube-data"></a>Müügivõimaluste loomine rakenduse RetailSales kuubi andmete kopeerimiseks

Müügivõimaluste abil loetakse rakenduse RetailSales kuubivaateid ja eksporditakse andmed Data Storagei csv-failidesse.

Müügivõimaluste loomiseks rakenduse RetailSales kuubi andmete kopeerimiseks järgige neid samme.

1. Valige Sünapse’i tööruumis vahekaart **Integreeri**.
1. Valige plussmärk (**+**) ja seejärel valige suvand **Impordi müügivõimaluste mallist**.
1. Laadige alla ja valige fail [ExportRetailSalesCubeViews.zip](https://aka.ms/reco-alternate-dataflow-files).
1. Valige oma SQL-andmebaasiga seotud teenus.
1. Valige oma lingitud ladustamiskonto teenus.
1. Avage andmete **kopeerimise tööriist** ja muutke kausta tee **atribuudi** väärtuseks **\<environment_name\>/...**.

### <a name="test-execution-of-the-pipeline"></a>Müügivõimaluste käivitamise test

Soovitame konveierit katsetada ainult ühe vaatega. Vaade **RetailSales_RetailMediaTemplateView** toimib hästi, kuna see sisaldab tavaliselt alla 10 rea.

## <a name="schedule-the-pipeline-to-run-on-a-recurring-schedule"></a>Plaanige müügivõimaluste käitamine korduva graafiku alusel

Iga kord, kui konveier töötab, leiab aset Azure’i tarbimine. Soovitame teil planeerida käivitamist 48-tunnise või pikema intervalliga. Kui peate andmeid kohe sünkroonima, saate konveieri alati käsitsi käivitada. 
 
## <a name="table-list-for-synchronization-from-dynamics-365-to-data-lake-storage"></a>Tabeliloend sünkroonimiseks Dynamics 365-st Data Storagei

Järgmine tabelite loend on kõigi kogu RetailSales kuubi jaoks vajalike tabelite alamkogum. Soovituste teenus kasutab ainult 15 vaadet kuubis RetailSales ja vastavalt filtreeriti nõutud tabelite loend.

### <a name="list-of-retailsales-cube-tables"></a>RetailSales-kuubi tabelite loend

- Välja BICalendarOffsets
- Ärianalüüsi (BIDateDimension)
- Väärtuse BIDateDimensionValue väärtus
- Kataloog
- CatalogProduct
- CatalogProductCategory
- Üksuse CustInvoiceJour
- CustInvoiceTrans
- CustTable
- DataArea
- Atribuudi DimensionAttributeValueCombination väärtus
- Atribuudi DimensionAttributeValueSet väärtus
- Tabel DirPartyTable
- EcoResCategory
- EcoResCategoryHierarchy
- EcoResCategoryHierarchyRole
- EcoResColor
- EcoResConfiguration
- EcoResProduct
- EcoResProductCategory
- EcoResProductTranslation
- EcoResSize (väljad EcoResSize)
- EcoResStyle
- HcmWorker
- InventDim
- InventDimCombination
- InventItemGroup
- InventItemGroupItem
- InventItemSetupSupplyType
- InventTable
- InventTrans
- LogisticsAddressCountryRegion
- LogisticsAddressCountryRegionTranslation
- Logistikaasukoht
- LogisticsPostalAddress
- OMHIERARCHYPURPOSE
- RetailAssortmentLookup
- Grupp RetailAssortmentLookupChannelGroup
- Fail RetailChannelProfile
- JaemüügichannelProfileProperty
- RetailChannelTable
- RetailChannelTableExt
- Fail RetailConnDatabaseProfile
- RetailCustInvoiceJourTable
- RetailCustTable
- RetailMediaTemplate
- RetailOfflineProfile
- RetailPeriodicDiscount
- RetailRecoListConfigurationParameters
- Grupp RetailSalesTaxOverrideGroup
- RetailSharedParameters
- RetailSpecialCategoryMember
- RetailTenderTypeCardTable
- RetailTenderTypeTable
- RetailTerminalTable
- RetailTmpProductMedia
- RetailTransactionDiscountTrans
- RetailTransactionPaymentTrans
- RetailTransactionPaymentTransExt
- RetailTransactionSalesTrans
- RetailTransactionSalesTransExt
- RetailTransactionTable
- SalesLine
- SalesTable
- SystemParameters
- RETAILCATALOGINTERNALORG
- RETAILGROUPMEMBERLINE
- RETAILINTERNALORGANIZATION
- RETAILSPECIALCATEGORYPRODUCT
- RETAILPRODUCTCATEGORY
- VÄLJA ECORESCONFIGURATION VÄLJAD
- DIMENSIONATTRIBUTE
- ATRIBUUDI DIMENSIONATTRIBUTEVALUESET VÄÄRTUS
- DIMENSIOONIHIERARHIA
- DIMENSIONHIERARCHYINTEGRATION
- DIMENSIOONIHIERARHIA (DIMENSIONHIERARCHYLEVEL)
- DIMENSIONPARAMETER
- OMExplodedOrganizationSecurityGraph

### <a name="view-list-for-the-parameter-to-pass-to-the-synapse-pipeline"></a>Saate kuvada loendi parameetri kohta, mis edastada Sünapse müügivõimalustele.

Järgmine komaga eraldatud loend sisaldab RetailSales-kuubi vaateid, mille konveier teeb toimingu "select" (vali). Seejärel kopeerib see tulemused andmete salvestamisele.

RetailSales_RetailAssortmentRulesView, RetailSales_RetailChannelNavigationHierarchiesView RetailSales_RetailChannelNavigationHierarchyCatalogProductsView, RetailSales_RetailChannelNavigationHierarchyCategoryNodesView, RetailSales_RetailChannelNavigationHierarchyCategoryProductsView, RetailSales_RetailMediaBaseUrlChannelView, RetailSales_RetailMediaRelativeUrlProductView, RetailSales_RetailMediaTemplateView, RetailSales_RetailOptOutCustomersView RetailSales_RetailProductCategory, RetailSales_RetailProductTransaction RetailSales_RetailProductVariantDimensionsView, RetailSales_RetailRecoListConfigurationParametersView, RetailSales_RetailRecoListsSharedParametersView, RetailSales_RetailEcoResProductTranslation

> [!IMPORTANT]
> Konveieri parameeter peab olema ühe komaga eraldatud vaatenimede loend. Tühikuid ega reavooge ei tohi olla.

## <a name="environment-specific-fixes"></a>Keskkonnapõhised parandused

### <a name="retailchannelview-fix"></a>RETAILCHANNELVIEW parandus

Vaade **RETAILCHANNELVIEW** sisaldab tugevalt kodeeritud täisarvu, mis esindab jaemüügikanali tüübi organisatsiooni. Tüübi tegelik väärtus võib muutuda keskkonnast keskkonda või rentnikust rentnikuks.

```SQL
CREATE OR ALTER   VIEW [dbo].[RETAILCHANNELVIEW]
AS
SELECT T1.RECID AS RECID1,
       T1.STOREAREA AS STOREAREA,
       T1.OMOPERATINGUNITID AS OMOPERATINGUNITID,
       T1.DEFAULTCUSTACCOUNT AS DEFAULTCUSTOMER,
       T1.RETAILCHANNELID AS RETAILCHANNELID,
       T1.CHANNELTYPE AS CHANNELTYPE,
       T1.PARTITION AS PARTITION,
       T1.RECID AS RECID,
       T2.OMOPERATINGUNITNUMBER AS OMOPERATINGUNITNUMBER,
       T3.NAME AS NAME
FROM   dbo.RETAILCHANNELTABLE AS T1 CROSS JOIN dbo.DIRPARTYTABLE AS T2 CROSS JOIN dbo.DIRPARTYTABLE AS T3
WHERE  ((((T1.OMOPERATINGUNITID = T2.RECID)
          )
         AND ((T2.RECID = T3.RECID)
              ))
        AND T2.INSTANCERELATIONTYPE IN (8363));
```

Mitteindekseeritud täisarvu uuendamiseks järgige neid samme.

1. Dynamics 365-s vaadake oma võrgukanali **ChannelID** väärtust.
1. Sünapse andmebaasiga seotud SQL Server Management Studio (SSMS) eksemplaris käivitage järgmine päring.

    ```SQL
    select INSTANCERELATIONTYPE, NAME, NAMEALIAS, * from dbo.DIRPARTYTABLE where RECID IN (select OMOPERATINGUNITID from dbo.RETAILCHANNELTABLE where RETAILCHANNELID =     <channelID>)
    ```

1. Kopeerige väärtus esimesest veerust (**INSTANCERELATIONTYPE**) ja kleepige see vaate definitsiooni.

## <a name="troubleshooting"></a>Tõrkeotsing

### <a name="pipeline-task-fails"></a>Müügivõimaluste ülesanne nurjub.

CopyData **ülesandel peaks olema 15 konveieriülesande** käivitamist. Kui mis tahes käivitamine nurjub, peate kinnitama, et olemas on kõik sõltuvad SQL-objektid ja et päringud käivitataks. Hõlpsaim viis kõigi sõltuvuste juurde pääsemiseks on kasutada andmebaasiga ühenduse loomiseks SSMS-i. Seejärel saate vaadet valida ja ootele hoida (või seda paremklõpsada) ja valida **uue aknana loo loomine**.

Veateade võib sisaldada järgmist teksti:

- Tõrge: allika poolel <a0/& ilmnes tõrge.
- Tõrge välisfaili käsitlemisel: suurim tõrgete arv.
- /RetailSales/RetailSales_xxxxxx

#### <a name="example-scenario"></a>Näidisstsenaarium

Selles näites ebaõnnestub **RetailSales_RetailProductCategory** tõrge ja kuvatakse tõrge "Suurim tõrgete arv".

Tõrke silumiseks järgige neid samme.

1. Avage fail **EntityList.json** tekstiredaktoriga (nt Visual Studio Kood).
1. Otsige välja<a0/&RetailSales_RetailProductCategory **·**.

    ```SQL
    CREATE  VIEW [dbo].[RetailSales_RetailProductCategory] AS SELECT 0 AS ROW_UNIQUEKEY ,CATEGORY AS CATEGORYID ,PRODUCT AS PRODUCTID ,PRODUCTNAME ,CATEGORYNAME     ,PARENTCATEGORY AS PARENTCATEGORYID ,PARTITION ,RECID FROM RetailProductCategoryView
    ```

1. See vaade sõltub ainult ühest vaatest: **RetailProductCategoryView** _. Leidke _*RetailProductCategoryView**.

    ```SQL
    CREATE VIEW [DBO].[RETAILPRODUCTCATEGORYVIEW] AS SELECT T1.CATEGORY AS CATEGORY, T1.PRODUCT AS PRODUCT, T1.PARTITION AS PARTITION, T1.RECID AS RECID, T2.PRODUCTNAME AS PRODUCTNAME, T2.PARTITION AS PARTITION#2, T3.NAME AS CATEGORYNAME, T3.PARENTCATEGORY AS PARENTCATEGORY, T3.PARTITION AS PARTITION#3 FROM RETAILPRODUCTCATEGORY T1 CROSS JOIN ECORESPRODUCTTRANSLATIONS T2 CROSS JOIN RETAILCATEGORYEXPANDED T3 WHERE((( T1.PRODUCT = T2.PRODUCT) AND ( T1.PARTITION = T2.PARTITION)) AND (( T1.CATEGORY = T3.RECID) AND ( T1.PARTITION = T3.PARTITION)))
    ```

1. See vaade sõltub kolmest vaatest: RETAILPRODUCTCATEGORY **,** ECORESPRODUCTTRANSLATIONS **JA** RETAILCATEGORYEXPANDED **·**. Leidke kõigi nende vaadete definitsioon ja loetlege nende sõltuvused. Jätkake, kuni leiate kõik sõltuvad vaated.

    Siin on kogu loend sõltuvuste puu järjestuses. Kinnitada tuleb kolmteist vaadet.

    - RetailSales_RetailProductCategory

        - Vaade RetailProductCategoryView

            - RETAILPRODUCTCATEGORY

                - KATEGOORIA ECORESPRODUCTCATEGORY
                - ECORESCATEGORYHIERARCHYROLE
                - RETAILSPECIALCATEGORYPRODUCT

                    - ECORESPRODUCT
                    - RETAILGROUPMEMBERLINE
                    - RETAILSPECIALCATEGORYMEMBER

            - ECORESPRODUCTTRANSLATIONS

                - ECORESPRODUCT
                - ECORESPRODUCTTRANSLATION
                - SYSTEMPARAMETERS

            - RETAILCATEGORYEXPANDED

                - KATEGOORIA ECORESCATEGORY
                - ECORESCATEGORYHIERARCHYROLE

1. Excelis looge väljavõtetest järgmine 13 **select count(\*)\<view_name\>**. Käivitage need väljavõtted SSMS-s ja saatke tulemused teksti. Seejärel kerige läbi tulemuste, et näha, kas mõni vaadetest ebaõnnestus. Esialgne tõrge soovitab, et vähemalt üks vaadetest nurjub.

    ```SQL
    select count(*) from RetailProductCategoryView
    select count(*) from RETAILPRODUCTCATEGORY
    select count(*) from ECORESPRODUCTCATEGORY
    select count(*) from ECORESCATEGORYHIERARCHYROLE
    select count(*) from RETAILSPECIALCATEGORYPRODUCT
    select count(*) from ECORESPRODUCT
    select count(*) from RETAILGROUPMEMBERLINE
    select count(*) from RETAILSPECIALCATEGORYMEMBER
    select count(*) from ECORESPRODUCTTRANSLATIONS
    select count(*) from ECORESPRODUCTTRANSLATION
    select count(*) from SYSTEMPARAMETERS
    select count(*) from RETAILCATEGORYEXPANDED
    select count(*) from ECORESCATEGORY
    ```

1. Üks võimalus kontrollida, mida vaatate, on luua juurst sõltuv vaade vaate loomiseks SSMS-is. Seejärel kontrollige, et on olemas Azure Data Azure’i failiveerg, mille nimi on **r.filepath**. Selle veeru olemasolu näitab, et vaates, mida vaatate, on andmete salvestise data lugemise vaade.

## <a name="additional-resources"></a>Lisaressursid

[Tootesoovituste ülevaade](product-recommendations.md)

[ Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas](enable-adls-environment.md)

[Isikupärastatud soovituste lubamine](personalized-recommendations.md)

[„Sarnaste toodete vaatamise” soovituste lubamine](shop-similar-looks.md)

[Isikupärastatud tootesoovitustest loobumine](personalization-gdpr.md)

[Tootesoovituste lisamine kassas](product.md)

[Soovituste lisamine kandeekraanile](add-recommendations-control-pos-screen.md)

[AI-ML-i soovituste tulemuste kohandamine](modify-product-recommendation-results.md)

[Loo kuraatorite soovitused käsitsi](create-editorial-recommendation-lists.md)

[Soovituste loomine demoandmetega](product-recommendations-demo-data.md)

[Tootesoovituste KKK](faq-recommendations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
