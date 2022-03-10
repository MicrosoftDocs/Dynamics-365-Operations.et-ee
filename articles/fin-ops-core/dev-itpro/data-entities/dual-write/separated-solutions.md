---
title: Eraldatud kahe kirjutamisrakenduse orkestratsioonipakett
description: Kahe kirjaga rakenduste orkestreerimispakett ei ole enam üks pakett, vaid on jagatud väiksemateks pakenditeks. Selles teemas selgitatakse lahendusi ja kaarte, mida iga pakett sisaldab, ning selle sõltuvust teistest pakettidest.
author: RamaKrishnamoorthy
ms.date: 11/29/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.custom: separate-solution
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: e2f870368dc662032a3e7ca7ddca902feb23a713
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063258"
---
# <a name="separated-dual-write-application-orchestration-package"></a>Eraldatud kahe kirjutamisrakenduse orkestratsioonipakett

[!include [banner](../../includes/banner.md)]



Varem oli kahe kirjutamisrakenduse orkestratsioonipakett üks pakett, mis sisaldas järgmisi lahendusi:

- Dynamics 365 Notes
- Dynamics 365 Finance ja operatsioonid ühine ankur
- Dynamics 365 Finance ja toimingud Topeltkirjutus olemi kaardid
- Dynamics 365 Asset Managementi rakendus
- Dynamics 365 Asset Management
- HCM-i ühine
- Dynamics 365 Supply Chain Extended
- Dynamics 365 Finance Extended
- Dynamics 365 Finance ja operatsioonid ühised
- Dynamics 365 Company
- Valuutakursid
- Field Service Common

Kuna see oli üks pakett, lõi see pakett klientidele "kõik või mitte midagi" olukorra. Microsoft on selle nüüd väiksemateks pakettreisideks eraldanud. Seetõttu saab klient valida ainult nende jaoks mõeldud lahenduste paketid. Näiteks kui olete Microsofti Dynamics 365 Supply Chain Management klient ja ei vaja integreerimist, märkmete ja varahaldusega Dynamics 365 Human Resources, saate need lahendused installitud lahendustest välja jätta. Kuna aluseks olevad lahendusenimed, avaldaja ja kaardiversioonid jäävad samaks, ei riku see muudatus. Olemasolevaid seadmeid uuendatakse.

![Eraldatud pakend.](media/separated-package-1.png)

Selles teemas selgitatakse lahendusi ja kaarte, mida iga pakett sisaldab, ning selle sõltuvust teistest pakettidest.

## <a name="dual-write-application-core"></a>Kahe kirjaga rakenduse tuum

Kahe kirjutamisrakenduse põhipakett võimaldab kasutajatel installida ja konfigureerida topeltkirjutust ilma kliendi kaasamise rakenduseta. See sisaldab viit järgmist lahendust.

| Kordumatu nimi                           | Kuvatav nimi                               |
|---------------------------------------|--------------------------------------------|
| Dynamics365Company                    | Dynamics 365 Company                       |
| Dynamics365FinanceAndOperationsCommon | Dynamics 365 Finance ja operatsioonid ühised |
| Valuuta vahetuskursi määrad                 | Valuutakursid                    |
| msdyn_DualWriteAppCoreMaps            | Kahe kirjutamisrakenduste põhiolemi kaardid   |
| msdyn_DualWriteAppCoreAnchor          | Kahe kirjaga rakenduste tuumankur        |

Selles paketis on saadaval järgmised kaardid.

| Finance and Operationsi rakendused     | Klientide kaasamise rakendused                    |
|---------------------------------|---------------------------------------------|
| Tootmisüksus                  | msdyn_internalorganizations                 |
| Organisatsiooni hierarhia          | msdyn_internalorganizationhierarchies       |
| Juriidilised isikud                  | msdyn_internalorganizations                 |
| Juriidilised isikud                  | cdm_companies                               |
| Organisatsiooni hierarhia eesmärgid | msdyn_internalorganizationhierarchypurposes |
| Vahetuskursi valuutapaar     | msdyn_currencyexchangeratepairs             |
| Nime liited                    | msdyn_nameaffixes                           |
| Vahetuskursi tüüp              | msdyn_exchangeratetypes                     |
| CDS-i valuutakursid              | msdyn_currencyexchangerates                 |
| Organisatsiooni hierarhia tüüp     | msdyn_internalorganizationhierarchytypes    |
| Valuutad                      | transactioncurrencies                       |
| Hübriidreaalsusjuhiste üksus     | msmrw_guides                                |

**Sõltuvuse teave**

Kahe kirjutamisrakenduse põhipakett ei sõltu teistest pakettidest.

## <a name="dual-write-human-resources"></a>Kahepalgeline inimressursid

Kahe kirjutamisega inimressursside pakett sisaldab lahendusi ja kaarte, mis on vajalikud inimressursside andmete sünkroonimiseks. See sisaldab kolme järgmist lahendust.

| Kordumatu nimi                | Kuvatav nimi                             |
|----------------------------|------------------------------------------|
| HCMCommon                  | HCM-i ühine                               |
| msdyn_Dynamics365HCMMaps   | Dynamics 365 Human Resources olemi kaardid |
| msdyn_Dynamics365HCMAnchor | Dynamics 365 Human Resources ankur      |

Selles paketis on saadaval järgmised kaardid.

| Finance and Operationsi rakendused | Klientide kaasamise rakendused         |
|-----------------------------|----------------------------------|
| Etniline päritolu              | cdm_ethnicorigins                |
| Tasu tööfunktsioon   | cdm_jobfunctions                 |
| Ametikohad V2                | cdm_jobpositions                 |
| Tööd                        | cdm_jobs                         |
| Tasu töötüüp       | cdm_jobtypes                     |
| Keelekoodid              | cdm_languages                    |
| Positsiooni tüüp               | cdm_positiontypes                |
| Positsiooni töötaja ülesanded | cdm_positionworkerassignmentmaps |
| Veterani staatus              | cdm_veteranstatuses              |
| Töötaja                      | cdm_workers                      |
| Töölevõtt ettevõtete kaupa      | cdm_employments                  |

**Sõltuvuse teave**

Kahe kirjutaga inimressursside pakett sõltub kahe kirjaga rakenduspõhi paketist. Seetõttu peaksite enne kahe kirjutava inimressursside paketi installimist installima topeltkirjutamisrakenduse põhipaketi.

## <a name="dual-write-supply-chain"></a>Kahe kirjaga tarneahel

Kahe kirjutakuga tarneahela pakett sisaldab lahendusi ja kaarte, mis on vajalikud tarneahela halduse andmete sünkroonimiseks. See sisaldab kolme järgmist lahendust.

| Kordumatu nimi                                | Kuvatav nimi                                              |
|--------------------------------------------|-----------------------------------------------------------|
| Dynamics365SupplyChainExtended             | Dynamics 365 Supply Chain Extended                        |
| msdyn_Dynamics365SupplyChainExtendedMaps   | Dynamics 365 Supply Chain Management laiendatud olemikaardid |
| msdyn_Dynamics365SupplyChainExtendedAnchor | Dynamics 365 Supply Chain Management laiendatud ankur      |

Selles paketis on saadaval järgmised kaardid.

| Finance and Operationsi rakendused                 | Klientide kaasamise rakendused                      |
|---------------------------------------------|-----------------------------------------------|
| Ühikud                                       | uoms                                          |
| CDS-i müügitellimuse päised                     | müügitellimused                                   |
| CDS-i müügitellimuse read                       | müügitellimuse üksikasjad                             |
| CDS-i müügipakkumise päis                  | pakkumised                                        |
| CDS-i müügipakkumise read                   | Pakkumise üksikasjad                                  |
| CDS väljastatud eristatavad tooted              | toodet                                      |
| Laotsoonid                             | msdyn_warehousezones                          |
| Laotsooni grupid                       | msdyn_warehousezonegroups                     |
| Lao tööread                        | msdyn_warehouseworklines                      |
| Lao tööpäised                      | msdyn_warehouseworkheaders                    |
| Laod                                  | msdyn_warehouses                              |
| Lao riiulirida                             | msdyn_warehouseaisles                         |
| Ühiku teisendused                            | msdyn_unitofmeasureconversions                |
| Tarnetingimused                           | msdyn_termsofdeliveries                       |
| Tarneviisid                           | msdyn_shipvias                                |
| Tooteetaloni laadid                       | msdyn_sharedproductstyles                     |
| Müügiarve read V2                      | invoicedetails                                |
| Müügiarve päised V2                    | arved                                      |
| Tooteetaloni suurused                        | msdyn_sharedproductsizes                      |
| Väljastatud tooted V2                        | msdyn_sharedproductdetails                    |
| Tooteetaloni konfiguratsioonid               | msdyn_sharedproductconfigurations             |
| Tooteetaloni värvid                       | msdyn_sharedproductcolors                     |
| Müügitellimuse päritolukoodid                    | msdyn_salesorderorigins                       |
| Toote sissetuleku päis                      | msdyn_purchaseorderreceipts                   |
| Toote sissetuleku rida                        | msdyn_purchaseorderreceiptproducts            |
| Ostutellimuse päised V2                   | msdyn_purchaseorders                          |
| CDS-i ostutellimuse rea ajutiselt kustutatud üksus | msdyn_purchaseorderproducts                   |
| CDS-i ostutellimuse rea üksus              | msdyn_purchaseorderproducts                   |
| Jälgimisdimensioonigrupid                   | msdyn_producttrackingdimensiongroups          |
| Laadid                                      | msdyn_productstyles                           |
| Laoala dimensioonigrupid                    | msdyn_productstoragedimensiongroups           |
| Tootepõhised ühikute teisendused           | msdyn_productspecificunitofmeasureconversions |
| Toote vaiketellimissätted V2           | msdyn_productspecificdefaultordersettings     |
| Suurused                                       | msdyn_productsizes                            |
| Tootedimensiooni grupid                    | msdyn_productdimensiongroups                  |
| Tellimuse vaikesätted                      | msdyn_productdefaultordersettings             |
| Konfiguratsioonid                              | msdyn_productconfigurations                   |
| Kõik tooted                                | msdyn_globalproducts                          |
| Värvid                                      | msdyn_productcolors                           |
| Tootekategooria hierarhia rollid            | msdyn_productcategoryhierarchyroles           |
| Tootekategooria hierarhiad                | msdyn_productcategoryhierarchies              |
| Tootekategooria määramised                | msdyn_productcategoryassignments              |
| Tootekategooriad                          | msdyn_productcategories                       |
| Lao asukohad                         | msdyn_inventorylocations                      |
| CDS-i varud on peal                            | msdyn_inventoryonhandentries                  |
| Tootekategooriad                          | msdyn_productcategories                       |
| CDS-i varud on peal                            | msdyn_inventoryonhandrequests                 |
| Tootenumbriga tuvastatud vöötkood           | msdyn_productbarcodes                         |
| Kliendikaart                                | msdyn_loyaltycards                            |
| Püsikliendi preemiapunktid                       | msdyn_loyaltyrewardpoints                     |
| Hinna kliendigrupid                       | msdyn_pricecustomergroups                     |
| Saidid                                       | msdyn_operationalsites                        |
| CDS-i müügipakkumise read                   | Pakkumise üksikasjad                                  |
| CDS-i müügitellimuse read                       | müügitellimuse üksikasjad                             |

**Sõltuvuse teave**

Kahe kirjaga tarneahela pakett sõltub järgmisest kolmest paketist. Seetõttu peaksite need paketid enne topeltkirjutamispaketi installimist installima.

- Kahe kirjaga rakenduse põhipakett
- Kahe kirjaga finantspakett
- Kahe kirjutaga inimressursside pakett

## <a name="dual-write-finance"></a>Kahe kirjutaga rahandus

Kahe kirjutamisega finantspakett sisaldab lahendusi ja kaarte, mis on vajalikud andmete sünkroonimiseks Dynamics 365 Finance. See sisaldab nelja järgmist lahendust.

| Kordumatu nimi                            | Kuvatav nimi                               |
|----------------------------------------|-------------------------------------------|
| Dynamics365FinanceExtended             | Dynamics 365 Finance Extended             |
| msdyn_Dynamics365FinanceExtendedMaps   | Dynamics 365 Finance laiendatud olemikaardid |
| FieldServiceCommon                     | Field Service Common                      |
| msdyn_Dynamics365FinanceExtendedAnchor | Dynamics 365 Finance laiendatud ankur      |

Selles paketis on saadaval järgmised kaardid.

| Finance and Operationsi rakendused             | Klientide kaasamise rakendused        |
|-----------------------------------------|---------------------------------|
| Kinnipeetava maksugrupid                  | msdyn_withholdingtaxgroups      |
| CDS kontaktid V2 (klient)              | kontaktid                        |
| CDS kontaktid V2 (hankija)                | kontaktid                        |
| Kliendid V3                            | kontaktid                        |
| Kinnipeetava maksu koodid                   | msdyn_withholdingtaxcodes       |
| Hankijad V2                              | msdyn_vendors                   |
| Tarnija makseviis                   | msdyn_vendorpaymentmethods      |
| Hankijagrupid                           | msdyn_vendorgroups              |
| Kontoplaan                       | msdyn_chartofaccountses         |
| Käibemaksu pearaamatu sisestusgrupid V2      | msdyn_taxpostinggroups          |
| Kauba käibemaksugrupp                    | msdyn_taxitemgroups             |
| Käibemaksugrupid                        | msdyn_taxgroups                 |
| Käibemaksuvabastuse koodi olemi CDS        | msdyn_taxexemptcodes            |
| Kliendigrupid                         | msdyn_customergroups            |
| Kliendi makseviis                 | msdyn_customerpaymentmethods    |
| Finantsdimensioonid                    | msdyn_dimensionattributes       |
| Käibemaksuhaldurid                   | msdyn_taxauthorities            |
| Finantsdimensiooni vorming              | msdyn_financialdimensionformats |
| Rahanduskalendri periood                  | msdyn_fiscalcalendarperiods     |
| Rahanduskalendri integratsiooniüksus      | msdyn_fiscalcalendars           |
| Rahanduskalendri aasta integratsiooniüksus | msdyn_fiscalcalendaryears       |
| Maksetingimused                        | msdyn_paymentterms              |
| Maksegraafik                        | msdyn_paymentschedules          |
| Maksegraafiku read                  | msdyn_paymentschedulelines      |
| CDS-i maksepäevad                        | msdyn_paymentdays               |
| CDS V2 maksepäeva read                | msdyn_paymentdaylines           |
| Põhikonto                            | msdyn_mainaccounts              |
| Põhikonto kategooriad                 | msdyn_mainaccountcategories     |
| Ledger                                  | msdyn_ledgers                   |
| Kliendid V3                            | kontod                        |

**Sõltuvuse teave**

Kahe kirjutakuga finantspakett sõltub kahe kirjaga rakenduse põhipaketist. Seetõttu peaksite enne topeltkirjutusrakenduse finantspaketi installimist installima topeltkirjutamisrakenduse põhipaketi.

## <a name="dual-write-notes"></a>Kahe kirjutamismärkmed

Kahe kirjutamisega märkmete pakett sisaldab lahendusi ja kaarte, mis on vajalikud märkme- või marginaaliandmete sünkroonimiseks. See sisaldab nelja järgmist lahendust.

| Kordumatu nimi                  | Kuvatav nimi                   |
|------------------------------|--------------------------------|
| Dynamics365Notes             | Dynamics 365 Notes             |
| Dynamics365NotesExtended     | Dynamics 365 märkmeid laiendatud    |
| msdyn_Dynamics365NotesMaps   | Dynamics 365 märkmete olemikaardid |
| msdyn_Dynamics365NotesAnchor | Dynamics 365 märkmete ankur      |

Selles paketis on saadaval järgmised kaardid.

| Finance and Operations                     | Customer Engagement |
|--------------------------------------------|---------------------|
| Müügitellimuse päise dokumendi manused    | Marginaalid         |
| Kliendi manused                       | Marginaalid         |
| Hankija dokumendimanused                | Marginaalid         |
| Ostutellimuse päise dokumendi manused | Marginaalid         |

**Sõltuvuse teave**

Kahe kirjaga märkmete pakett sõltub kahest järgmisest paketist. Seetõttu peaksite need paketid enne topeltkirjutusmärkmete paketi installimist installima.

- Kahe kirjaga rakenduse põhipakett
- Kahe kirjaga finantspakett

## <a name="dual-write-asset-management"></a>Kahe kirjaga varahaldus

Kahe kirjutamisvarahalduse pakett sisaldab lahendusi ja kaarte, mis on vajalikud tarneahela halduse või Dynamics 365 Field Service. See sisaldab nelja järgmist lahendust.

| Kordumatu nimi                          | Kuvatav nimi                              |
|--------------------------------------|-------------------------------------------|
| Dynamics365AssetManagement           | Dynamics 365 Asset Management             |
| Dynamics365AssetManagementApp        | Dynamics365 Asset Managementi rakendus          |
| msdyn_DualWriteAssetManagementMaps   | Dynamics 365 Asset Managementi olemikaardid |
| msdyn_DualWriteAssetManagementAnchor | Dynamics 365 Asset Managementi ankur      |

Selles paketis on saadaval järgmised kaardid.

| Finance and Operationsi rakendused                           | Klientide kaasamise rakendused                |
|-------------------------------------------------------|-----------------------------------------|
| Varahalduse garantii                             | msdyn_warranties                        |
| Varahalduse mudelid                               | msdyn_models                            |
| Varahalduse tootjad                        | msdyn_manufacturers                     |
| Varahalduse töö asukohtade tüübid            | msdyn_functionallocationtypes           |
| Varahalduse töö asukohad                 | msdyn_functionallocations               |
| Varahalduse töö asukoha töötsükli olekud | msdyn_functionallocationlifecyclestates |
| Varahalduse töö asukoha töötsükli mudelid | msdyn_functionallocationlifecyclemodels |
| Varahalduse varad                               | msdyn_customerassets                    |
| Varahalduse varade tüübid                          | msdyn_customerassetcategories           |
| Varahalduse vara töötsükli olekud               | msdyn_assetlifecyclestates              |
| Varahalduse vara töötsükli mudelid               | msdyn_assetlifecyclemodels              |

**Sõltuvuse teave**

Kahe kirjutamisvarahalduse pakett sõltub kahe kirjaga rakenduspõhi paketist. Seetõttu peaksite enne topeltkirjutusvarahalduse paketi installimist installima topeltkirjutamisrakenduse põhipaketi.

## <a name="packages-required-for-project-operations"></a>Projektitoimingute jaoks vajalikud paketid
Projektitoimingud sõltuvad järgmistest pakettidest. Seetõttu peaksite need paketid enne Project Operationsi installimist installima.

- Kahe kirjaga rakenduse põhipakett
- Kahe kirjaga finantspakett
- Kahe kirjaga tarneahela pakett
- Kahe kirjaga varahalduse pakett
- Kahe kirjutaga inimressursside pakett
