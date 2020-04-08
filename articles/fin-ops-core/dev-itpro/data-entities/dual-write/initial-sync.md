---
title: Üksuse sõltuvusahel (sünkroonimisjärjestus)
description: Selles peatükis kirjeldatakse sünkroonimise järjekorda, mida peate järgima esialgsete andmete loomisel.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 4adb2c8d57ad8f67346b8d34212b7a4b0bd052ab
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173127"
---
# <a name="entity-dependency-chain-synchronization-order"></a>Üksuse sõltuvusahel (sünkroonimisjärjestus)

[!include [banner](../../includes/banner.md)]



Järgmistes tabelites on üksuses loetletud nende lubamise järjekorras. Kui lubate vastenduse esmaseks sünkroonimiseks, tuvastab topeltkirjutus automaatselt muud vastendused, mis peavad olema lubatud. Saate kasutada Finance and Operationsi rakenduste lehte **Topeltkirjutus**, et valida või tühistada üksuste valik esmase sünkroonimise ajal.

Topeltkirjutuse uusimas versioonis saate lubada ainult mõned üksused ja sõltuvused lahendatakse teie eest.

## <a name="dynamics-365-supply-chain-management-entities"></a>Dynamics 365 Supply Chain Management üksused

Järgmised Supply Chain Managementi üksused on loetletud nende lubamise järjekorras.

| Vastenduse nimi topeltkirjutuse lehel | Üksuse metaandmete nimi Supply Chain Managementis | Üksuse metaandmete nimi Common Data Service'is | Märkmed |
|---|---|---|---|
| Ühikud ... uoms                                                                      | UnitOfMeasureEntity                                    | uom                                          | |
| Ühiku teisendused ... msdyn_unitofmeasureconversions                                 | UnitOfMeasureConversionEntity                          | msdyn_unitofmeasureconversion                | |
| Kõik tooted ... msdyn_globalproducts                                               | EcoResEveryProductEntity                               | msdyn_globalproduct                          | |
| Tootedimensiooni grupid ... msdyn_productdimensiongroups                           | EcoResProductDimensionGroupEntity                      | msdyn_productdimensiongroup                  | |
| Laoala dimensiooni grupid ... msdyn_productstoragedimensiongroups                    | EcoResStorageDimensionGroupEntity                      | msdyn_productstoragedimensiongroup           | |
| Jälgimisdimensiooni grupid ... msdyn_producttrackingdimensiongroups                  | EcoResTrackingDimensionGroupEntity                     | msdyn_producttrackingdimensiongroup          | |
| Värvid ... msdyn_productcolors                                                      | EcoResProductColorEntity                               | msdyn_productcolor                           | |
| Suurused ... msdyn_productsizes                                                        | EcoResProductSizeEntity                                | msdyn_productsize                            | |
| Laadid ... msdyn_productstyles                                                      | EcoResProductStyleEntity                               | msdyn_productstyle                           | |
| Konfiguratsioonid ... msdyn_productconfigurations                                      | EcoResProductConfigurationEntity                       | msdyn_productconfiguration                   | |
| Väljastatud tooted V2 ... msdyn_sharedproductdetails                                 | EcoResReleasedProductV2Entity                          | msdyn_sharedproductdetail                    | |
| Common Data Service'i väljastatud eristatavad tooted ... toodetele                         | EcoResReleasedDistinctProductCommon Data ServiceEntity | toode                                      | |
| Tootenumbri tuvastatud vöötkood ... msdyn_productbarcodes                         | EcoResProductNumberIdentifiedBarcodeEntity             | msdyn_productbarcode                         | |
| Vaiketellimissätted ... msdyn_productdefaultordersettings                        | InventProductDefaultOrderSettingsEntity                | msdyn_productdefaultordersetting             | |
| Toote vaiketellimissätted V2 ... msdyn_productspecificdefaultordersettings     | InventProductSpecificOrderSettingsV2Entity             | msdyn_productspecificdefaultordersetting     | |
| Tootepõhised ühikute teisendused ... msdyn_productspecificunitofmeasureconversions | EcoResProductSpecificUnitConversionEntity              | msdyn_productspecificunitofmeasureconversion | |
| Saidid ... msdyn_operationalsites                                                    | InventOperationalSiteEntity                            | msdyn_operationalsite                        | |
| Laod ... msdyn_warehouses                                                     | InventWarehouseEntity                                  | msdyn_warehouse                              | Vt [märkus 1](#scm-notes). |
| Tooteetaloni värvid ... msdyn_sharedproductcolors                                 | EcoResProductMasterColorEntity                         | msdyn_sharedproductcolor                     | |
| Tooteetaloni suurused ... msdyn_sharedproductsizes                                   | EcoResProductMasterSizeEntity                          | msdyn_sharedproductsize                      | |
| Tooteetaloni laadid ... msdyn_sharedproductstyles                                 | EcoResProductMasterStyleEntity                         | msdyn_sharedproductstyle                     | |
| Tooteetaloni konfiguratsioonid ... msdyn_sharedproductconfigurations                 | EcoResProductMasterConfigurationEntity                 | msdyn_sharedproductconfiguration             | |
| Tootekategooriad ... msdyn_productcategories                                      | EcoResProductCategoryEntity                            | msdyn_productcategory                        | Vt [märkus 2](#scm-notes). |
| Tootekategooria määramised ... msdyn_productcategoryassignments                   | EcoResProductCategoryAssignmentEntity                  | msdyn_productcategoryassignment              | |
| Toote kategooriahierarhiad ... msdyn_productcategoryhierarchies                   | EcoResProductCategoryHierarchyEntity                   | msdyn_productcategoryhierarchy               | |
| Toote kategooriahierarhia rollid ... msdyn_productcategoryhierarchyroles            | EcoResProductCategoryHierarchyRoleEntity               | msdyn_productcategoryhierarchyrole           | |
| Varude riiulirida ... msdyn_warehouseaisles                                           | WMSWarehouseAisleEntity                                | msdyn_warehouseaisle                         | |
| Lao tsoonid ... msdyn_warehousezones                                            | WHSWarehouseZoneEntity                                 | msdyn_warehousezone                          | |
| Lao tsoonigrupid ... msdyn_warehousezonegroups                                 | WHSWarehouseZoneGroupEntity                            | msdyn_warehousezonegroup                     | |
| Lao asukohad ... msdyn_inventorylocations                                    | WMSWarehouseLocationEntity                             | msdyn_inventorylocation                      | Vt [märkus 3](#scm-notes). |
| Lao töö päised ... msdyn_warehouseworkheaders                               | WHSWarehouseWorkHeaderEntity                           | msdyn_warehouseworkheader                    | |
| Lao tööread ... msdyn_warehouseworklines                                    | WHSWarehouseWorkLineEntity                             | msdyn_warehouseworklines                     | Vt [märkus 4](#scm-notes). |
| Tarneviisid ... msdyn_shipvias                                                | DlvDeliveryModeEntity                                  | msdyn_shipvias                               | |
| Tarnetingimused ... msdyn_termsofdeliveries                                       | DeliveryTermsEntity                                    | msdyn_termsofdelivery                        | |
| Müügitellimuse päritolu koodid ... msdyn_salesorderorigins                                | SalesOrderOriginEntity                                 | msdyn_salesorderorigin                       | |
| Common Data Service müügitellimuste päised ... salesorders                             | SalesOrderHeaderCommon Data ServiceEntity              | salesorder                                   | |
| Common Data Service müügitellimuse read ... salesorderdetails                         | SalesOrderLineCommon Data ServiceEntity                | müügitellimuse üksikasjad                            | |
| Common Data Service müügipakkumise päis ... pakkumised                               | SalesQuotationHeaderCommon Data ServiceEntity          | pakkumine                                        | |
| Common Data Service müügipakkumise read ... quotedetails                          | SalesQuotationLineCommon Data ServiceEntity            | QuoteDetails                                 | |
| Müügiarve päised V2 ... arved                                               | SalesInvoiceHeaderV2Entity                             | arve                                      | |
| Müügiarve read V2 ... invoicedetails                                           | SalesInvoiceLineV2Entity                               | invoicedetail                                | |

### <a name="mapping-specific-notes"></a><a id='scm-notes'></a>vastendamispõhised märkmed

1. Enesesõltuvuse tõttu võib juhtuda, et peate esmase sünkroonimise kaks korda käivitama.
2. Vaikimisi on esmane sünkroonimine välja lülitatud põhi/alamüksuse seose tõttu (platvorm ei käsitle nutikat järjestust). Seetõttu tuleb olemasolevad tootekategooriad õiges järjestuses käsitsi sünkroonida, nt ajakohastada kategooria kirjeldust (esmalt juurkategooria, seejärel alamüksused ja nende alamäksused). Minge jaotisse **Tooteteabe haldus \> Seadistus \> Kategooriad ja atribuudid \> Kategooriahierarhiad.** Lehel **Kategooriahierarhiad** saate valida iga hierarhia ja vaadata selle tootekategooriaid.
3. Esmane sünkroonimine nurjub tühja otsinguvälja **ItemNumberInLocation** ning esimese, teise ja kolmanda täiendava laotsooni vastendamise tõttu. Seetõttu eemaldatakse need vastendused praegu.
4. Esmase sünkroonimise nurjumist põhjustab tühja välja **CaptureWeight** vastendamine. Seetõttu eemaldatakse see vastendus praegu.

### <a name="setup-related-information"></a>Häälestamisega seonduv teave

+ Kirjete algsel loomisel Dynamics 365 mudeljuhitud rakenduse üksuses **Tooted**, on nende olek **Mustand**. Selle muutmiseks olekusse **Aktiivne** avage mudeljuhitud rakenduse jaotis **Sätted \> Haldus \> Süsteemisätted \> Müük** ja seadke suvandi **Loo tooted aktiivses olekus** väärtuseks **Jah**.
+ Kirjete loomisel Dynamics 365 mudeljuhitud rakenduste või Common Data Service'i üksuses **Tooted** enne, kui topeltirjutus on lubatud, värskendatakse neid kirjeid ainult siis, kui kogu võti, sealhulgas **Ettevõte**, vastab rakenduse Finance and Operations andmetele.
+ Üksuse **Tooted** sünkroonimine on ühesuunaline, Finance and Operationsi rakendustest Common Data Service'isse. Kui Dynamics 365 mudeljuhitud rakenduste üksuse **Tooted** vastendatud välja värskendatakse, kirjutatakse värskendus üle järgmise sünkroonimise ajal Finance and Operationsi rakenduses.

### <a name="known-issues"></a>Teadaolevad probleemid

- Üksuse kustutamisel Finance and Operationsi rakenduses ilmneb tõrge. Kui mõõtühikud sünkroonitakse Finance and Operationsi rakendusest Common Data Service'isse, luuakse konkreetse klassi esimene ühik esmase ühikuna ja see takistab kustutamist.

    **Leevendamine:** kustutage üksus esmalt Common Data Service'is. Seejärel saab seda kustutada Finance and Operationsi rakenduses.

- Tegevuskoha kustutamisel Common Data Service'i rakenduses ilmneb tõrge. Kuvatakse tõrketeade „Teabelogi: Hoiatus: esmast aadressi ei saa kustutada.; Hoiatus: üksuse kirjet ei saanud kustutada, kuna valideerimine nurjus järgmise andmeallika puhul: InventSiteLogisticsLocation (InventSiteLogisticsLocation).” Selle tõrke põhjustab Finance and Operationsi rakenduse andmeüksuse probleem.

    **Leevendamine:** saate kustutada saidi Finance and Operationsi rakenduses. Saiti saab seejärel kustutada Common Data Service'is, kui vastav topeltkirjutuse vastendus töötab.

## <a name="dynamics-365-finance-entities"></a>Dynamics 365 Finance üksused

Järgmised Dynamics 365 Finance'i üksused on loetletud nende lubamise järjekorras.

| Vastenduse nimi topeltkirjutuse lehel | Üksuse metaandmete nimi Finance'is | Üksuse metaandmete nimi Common Data Service'is | Märkmed |
|---|---|---|---|
| Valuutad ... transactioncurrencies                                            | CurrencyEntity                              | Currency                                   | |
| Vahetuskursi tüüp ... msdyn_exchangeratetypes                                  | ExchangeRateTypeEntity                      | msdyn_exchangeratetype                     | |
| Vahetuskursi valuutapaar ... msdyn_currencyexchangeratepairs                 | ExchangeRateCurrencyPairEntity              | msdyn_currencyexchangeratepair             | |
| Common Data Service vahetuskursid ... msdyn_currencyexchangerates              | ExchangeRateCommon Data ServiceEntity       | msdyn_currencyexchangerate                 | Vt [märkus 1](#fin-notes). |
| Rahanduskalendri integreerimise üksus ... msdyn_fiscalcalendars                    | FiscalCalendarEntity                        | msdyn_fiscalcalendar                       | |
| Rahanduskalendri aasta integreerimise üksus ... msdyn_fiscalcalendaryears           | FiscalCalendarYearEntity                    | msdyn_fiscalcalendaryear                   | |
| Rahanduskalendri periood ... msdyn_fiscalcalendarperiods                          | FiscalPeriodEntity                          | msdyn_fiscalcalendarperiod                 | |
| Organisatsiooni hierarhia tüüp ... msdyn_internalorganizationhierarchytypes        | OMOrganizationHierarchyTypeEntity           | msdyn_internalorganizationhierarchytype    | Vt [märkus 1](#fin-notes). |
| Organisatsiooni hierarhia eesmärgid ... msdyn_internalorganizationhierarchypurposes | OMOrganizationHierarchyPurposeEntity        | msdyn_internalorganizationhierarchypurpose | Vt [märkus 1](#fin-notes). |
| Juriidilised isikud ... msdyn_internalorganizations                                  | OMLegalEntity                               | msdyn_internalorganization                 | Vt [märkus 1](#fin-notes). |
| Juriidilised isikud ... cdm_companies                                                | OMLegalEntity                               | cdm_company                                | |
| Tootmisüksus ... msdyn_internalorganizations                                  | OMOperatingUnitEntity                       | msdyn_internalorganization                 | Vt [märkus 1](#fin-notes). |
| Organisatsiooni hierarhia – avaldatud ... msdyn_internalorganizationhierarchies    | OMOrganizationHierarchyPublishedEntity      | msdyn_internalorganizationhierarchy        | Vt [märkus 1](#fin-notes). |
| Nime liited ... msdyn_nameaffixes                                              | DirNameAffixEntity                          | msdyn_nameaffix                            | |
| Common Data Service'i maksepäevad ... msdyn_paymentdays                          | PaymentDayCommon Data ServiceEntity         | msdyn_paymentday                           | |
| Common Data Service'i maksepäeva read V2 ... msdyn_paymentdaylines              | PaymentDayLineCommon Data ServiceV2Entity   | msdyn_paymentdayline                       | |
| Maksegraafik ... msdyn_paymentschedules                                     | PaymentScheduleEntity                       | msdyn_paymentschedule                      | |
| Maksegraafiku read ... msdyn_paymentschedulelines                           | PaymentScheduleLineEntity                   | msdyn_paymentscheduleline                  | |
| Maksetingimused ... msdyn_paymentterms                                         | PaymentTermEntity                           | msdyn_paymentterm                          | |
| Kliendi makseviis ... msdyn_customerpaymentmethods                        | CustomerPaymentMethodEntity                 | msdyn_customerpaymentmethod                | |
| Hankija makseviis ... msdyn_vendorpaymentmethods                            | VendorPaymentMethodEntity                   | msdyn_vendorpaymentmethod                  | |
| Kliendigrupid ... msdyn_customergroups                                        | CustCustomerGroupEntity                     | msdyn_customergroup                        | |
| Hankijagrupid ... msdyn_vendorgroups                                            | VendVendorGroupEntity                       | msdyn_vendorgroup                          | |
| Käibemaksugrupid ... msdyn_taxgroups                                            | TaxGroupEntity                              | msdyn_taxgroup                             | |
| Kauba käibemaksugrupid ... msdyn_taxitemgroups                                   | TaxItemGroupEntity                          | msdyn_taxitemgroup                         | |
| Käibemaksu pearaamatu sisestamisgrupid V2 ... msdyn_taxpostinggroups                   | TaxPostingGroupEntityV2                     | msdyn_taxpostinggroup                      | |
| Common Data Service'i käibemaksu vabastuse koodi üksus ... msdyn_taxexemptcodes       | TaxExemptCodeCommon Data ServiceEntity      | msdyn_taxexemptcode                        | |
| Käibemaksuhaldurid ... msdyn_taxauthorities                                  | TaxAuthorityEntity                          | msdyn_taxauthority                         | |
| Käibemaksukood ... msdyn_taxcodes                                               | TaxCodeEntity                               | msdyn_taxcode                              | Vt [märkus 1](#fin-notes). |
| Finantsdimensiooni vorming ... msdyn_financialdimensionformats                  | DimensionIntegrationFormatEntity            | msdyn_financialdimensionformat             | |
| Finantsdimensioonid ... msdyn_dimensionattributes                              | DimensionAttributeEntity                    | msdyn_dimensionattribute                   | |
| Kinnipeetava maksu grupid ... msdyn_withholdingtaxgroups                           | TaxWithholdingGroupEntity                   | msdyn_withholdingtaxgroup                  | |
| Kinnipeetava maksu koodid ... msdyn_withholdingtaxcodes                             | TaxWithholdingTaxCodes                      | msdyn_withholdingtaxcode                   | |
| Kontoplaan ... msdyn_chartofaccountses                                   | LedgerChartOfAccountsEntity                 | msdyn_chartofaccounts                      | |
| Pearaamat ... msdyn_ledgers                                                        | LedgerEntity                                | msdyn_ledger                               | Vt [märkus 1](#fin-notes). |
| Põhikonto kategooriad ... msdyn_mainaccountcategories                         | MainAccountCategoryEntity                   | msdyn_mainaccountcategory                  | |
| Põhikonto ... msdyn_mainaccounts                                             | MainAccountEntity                           | msdyn_mainaccount                          | |
| Kliendi V3 ... kontod                                                       | CustCustomerV3Entity                        | konto                                    | Vt [märkus 2](#fin-notes). |
| Kliendi V3 ... kontaktid                                                       | CustCustomerV3Entity                        | kontakt                                    | Vt [märkus 3](#fin-notes). |
| Hankijad V2 ... msdyn_vendors                                                    | VendVendorV2Entity                          | msdyn_vendor                               | Vt [märkus 2](#fin-notes). |
| Common Data Service'i kontakti V2 ... kontaktid                                    | smmContactPersonCommon Data ServiceV2Entity | kontakt                                    | Vt [märkus 4](#fin-notes). |
| Common Data Service'i kontakti V2 ... kontaktid                                    | smmContactPersonCommon Data ServiceV2Entity | kontakt                                    | Vt [märkus 5](#fin-notes). |

### <a name="mapping-specific-notes"></a><a id='fin-notes'></a>vastendamispõhised märkmed

1. Ühesuunaline sünkroonimine ilmneb Finance and Operationsi rakendustest Common Data Service'isse.
2. Enesesõltuvuse tõttu võib juhtuda, et peate esmase sünkroonimise käivitama rohkem kui ühe korra. Veenduge, et valite seose tüübiks **Klient**, kui loote konto Common Data Service'i lehe **Kontod** abil. Kui esmasel sünkroonimisel ilmneb probleem väljaga **Põhikontakt**, eemaldage see väli vastendusestt ja käivitage seejärel esmane sünkroonimine uuesti. Kui algne sünkroonimine on edukalt lõpule viidud, peatage vastendamine ja lisage sellele väli **Põhikontakt** uuesti. Seejärel käivitage vastendamine, kuid jätke esmane sünkroonimine vahele. Välja **Põhikontakt** väärtust ei kaasata esmases sünkroonimises ja peate väärtused käsitsi migreerima.
3. Veenduge, et määrate Common Data Service'i lehel **Kontaktid** suvandi **Müüdavad** väärtuseks **Jah** klienti tüübiga **Isik**.
4. Sellel vastendamisel on kliendi kontaktide linkimiseks filter kummalgi pool. Avage vastendamise üksikasjad, valige üksuse **Sales.Contact** kõrval filtri nupp (lehtri sümbol) ja veenduge, et faili kriteerium sisaldaks üksust **msdyn_contactforvendor eq true and msdyn_sellable eq false**.
5. Sellel vastendamisel on hankija kontaktide linkimiseks filter kummalgi pool. Avage vastendamise üksikasjad, valige üksuse **Sales.Contact** kõrval filtri nupp (lehtri sümbol) ja veenduge, et filtri kriteerium sisaldaks üksust **msdyn_contactforvendor eq true and msdyn_sellable eq false**. 

## <a name="dynamics-365-human-resources-entities"></a>Dynamics 365 Human Resources üksused

Järgmised Dynamics 365 Human Resources'i üksused on loetletud nende lubamise järjekorras.

| Vastenduse nimi topeltkirjutuse lehel | Üksuse metaandmete nimi Human Resourcesis | Üksuse metaandmete nimi Common Data Service'is | Märkmed |
|---|---|---|---|
| cdm_jobfunction – töö funktsioon                                |                                   | cdm_jobfunction                  | |
| cdm_jobtypes – töö tüübid                                      |                                   | cdm_jobtypes                     | |
| cdm_jobs – tööd                                               |                                   | cdm_jobs                         | |
| cdm_jobs – töö üksikasjad                                        |                                   | cdm_jobs                         | |
| cdm_positiontype – ametikoha tüüp                               | HcmPositionTypeEntity             | cdm_positiontype                 | |
| cdm_jobpositions – põhiametikoht                              | HcmPositionBaseEntity             | cdm_jobposition                  | Vt [märkus 1](#hr-notes). |
| cdm_jobposition – ametikoha üksikasjad                            | HcmPositionDetailEntity           | cdm_jobposition                  | Vt [märkus 1](#hr-notes). |
| cdm_jobposition – ametikoha kestus                           | HcmPositionDurationEntity         | cdm_jobposition                  | Vt [märkus 1](#hr-notes). |
| cdm_jobposition – ametikoha hierarhiad                        | HcmPositionHierarchyEntity        | cdm_jobposition                  | Vt [märkus 1](#hr-notes). |
| cdm_veteranstatus – veterani staatus                            |                                   | cdm_veteranstatus                | |
| cdm_ethnicorigin – rahvuslik päritolu                              |                                   | cdm_ethnicorigin                 | |
| cdm_languagecode – keelekood                              |                                   | cdm_languagecode                 | |
| cdm_worker – töötaja                                           | HcmWorkerEntity                   | cdm_worker                       | |
| cdm_employments – töölevõtud                                 |                                   | cdm_employments                  | |
| cdm_employments – töölevõtu üksikasjad                           |                                   | cdm_employments                  | |
| cdm_positionworkerassignmentmaps – töötaja määramine ametikohale | HcmPositionWorkerAssignmentEntity | cdm_positionworkerassignmentmaps | Vt [märkus 2](#hr-notes).|

### <a name="mapping-specific-notes"></a><a id='hr-notes'></a>vastendamispõhised märkmed

1. Üks Common Data Service'i üksus on vastendatud mitme Finance and Operationsi rakenduse üksusega.
2. Sellel vastendusel on eneseviide.

## <a name="asset-management-entities"></a>Varahalduse üksused

Järgmised Dynamics 365 Supply Chain Managementi varahalduse üksused on loetletud nende lubamise järjekorras.

| Vastenduse nimi topeltkirjutuse lehel | Üksuse metaandmete nimi varahalduses | Üksuse metaandmete nimi Common Data Service'is | Märkmed |
|---|---|---|---|
| FO.AssetManagementAssetLifecycleStates--Common Data Service.msdyn_assetlifecyclestates                           | Varahalduse vara töötsükli olekud               | msdyn_assetlifecyclestates               | |
| FO.AssetManagementAssetLifecycleModels--Common Data Service.msdyn_assetlifecyclemodels                           | Varahalduse vara töötsükli mudelid               | msdyn_assetlifecyclemodels               | |
| FO.AssetManagementFunctionalLocationLifecycleModels--Common Data Service.msdyn_functionallocationlifecyclemodels | Varahalduse töö asukoha töötsükli mudelid | msdyn_functionallocationlifecyclemodels  | |
| FO.AssetManagementFunctionalLocationLifecycleStates--Common Data Service.msdyn_functionallocationlifecyclestates | Varahalduse töö asukoha töötsükli olekud | msdyn_functionallocationlifecyclestates  | |
| FO.AssetManagementAssetTypes--Common Data Service.msdyn_customerassetcategories                                  | Varahalduse varade tüübid                          | msdyn_customerassetcategories            | |
| FO.AssetManagementFunctionalLocationTypes--Common Data Service.msdyn_functionallocationtypes                     | Varahalduse töö asukohtade tüübid            | msdyn_functionallocationtypes            | |
| FO.AssetManagementFunctionalLocations--Common Data Service.msdyn_functionallocations                             | Varahalduse töö asukohad                 | msdyn_functionallocations                | Vt [märkust](#am-notes). |
| FO.AssetManagementAssets--Common Data Service.msdyn_customerassets                                               | Varahalduse varad                               | msdyn_customerassets                     | Vt [märkust](#am-notes). |
| FO.AssetManagementManufacturers--Common Data Service.msdyn_manufacturers                                         | Varahalduse tootjad                        | msdyn_manufacturers                      | |
| FO.AssetManagementModels--Common Data Service.msdyn_models                                                       | Varahalduse mudelid                               | msdyn_models                             | |
| FO.AssetManagementWarranty--Common Data Service.msdyn_warranties                                                 | Varahalduse garantii                             | msdyn_warranties                         | |

### <a name="mapping-specific-notes"></a><a id='am-notes'></a>vastendamispõhised märkmed

- Enesesõltuvuse tõttu võib juhtuda, et peate esmase sünkroonimise käivitama rohkem kui ühe korra.
