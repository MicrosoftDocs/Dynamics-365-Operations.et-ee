---
title: Eraldatud topeltkirjutusega rakenduse orkestratsioonipakett
description: Topeltkirjutusega rakenduse orkestratsioonipakett ei ole enam üks pakett, vaid on eraldatud väiksemateks pakettideks. See teema selgitab lahendusi ja vastemeid, mida iga pakett sisaldab ja selle sõltuvust teistest pakenditest.
author: RamaKrishnamoorthy
ms.date: 04/25/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: separate-solution
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: f6950ec3e6ded49a71f119c21be67f538c8e1c69
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716548"
---
# <a name="separated-dual-write-application-orchestration-package"></a>Eraldatud topeltkirjutusega rakenduse orkestratsioonipakett

[!include [banner](../../includes/banner.md)]



Varem oli topeltkirjutusega rakenduse orkestrutuspakett üksikpakett, mis sisaldas järgmisi lahendusi:

- Dynamics 365 märkused
- Dynamics 365 finantside ja toimingute tavaankur
- Dynamics 365 finantside ja toimingute topeltkirjutuse üksuse vastekaardid
- Dynamics 365 varahalduse rakendus
- Dynamics 365 varahaldus
- HCM-i ühine
- Dynamics 365 tarneahelat on laiendatud.
- Dynamics 365 Finance Extended
- Dynamics 365 ühised finantsid ja toimingud
- Dynamics 365 ettevõte
- Valuuta vahetuskursid
- Väljateenuse üldine

Kuna see oli üks pakett, lõi see pakett klientide jaoks olukorra "kõik või mitte midagi". Microsoft on nüüd selle eraldanud väiksemateks pakettideks. Seetõttu saavad kliendid valida vaid paketid lahendustele, mida nad vajavad. Näiteks kui Dynamics 365 Supply Chain Management Dynamics 365 Human Resources olete Microsofti klient ja te ei vaja integreerimist rakendustega, märkustega ja varahaldusega, võite need lahendused installitud lahendustest välja jätta. Kuna aluseks olevad lahendusenimed, avaldaja ja vastendatud versioonid jäävad samaks, ei katke see muudatus. Olemasolevaid installe uuendatakse.

![Eraldatud pakend.](media/separated-package-1.png)

See teema selgitab lahendusi ja vastemeid, mida iga pakett sisaldab ja selle sõltuvust teistest pakenditest.

## <a name="dual-write-application-core"></a>Topeltkirjutuse rakenduse tuum

Topeltkirjutusega rakenduse tuumpakett võimaldab kasutajatel installida ja konfigureerida topeltkirjutust ilma kliendikogemuse rakenduseta. See sisaldab järgmist viit lahendust.

| Kordumatu nimi                           | Kuvatav nimi                               |
|---------------------------------------|--------------------------------------------|
| Dynamics365Company                    | Dynamics 365 ettevõte                       |
| Dynamics365FinanceAndOperationsCommon | Dynamics 365 ühised finantsid ja toimingud |
| Valuuta vahetuskursi määrad                 | Valuuta vahetuskursid                    |
| msdyn_DualWriteAppCoreMaps            | Topeltkirjutuse rakenduste põhiüksuse vastekaardid   |
| msdyn_DualWriteAppCoreAnchor          | Topeltkirjutuse rakenduste tuumankur        |

Selles paketis on saadaval järgmised vastekaardid.

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

Topeltkirjutuse rakenduse tuumpakett ei sõltu teistest pakenditest.

## <a name="dual-write-human-resources"></a>Topeltkirjutuse inimressursid

Topeltkirjutuse inimressursside pakett sisaldab inimressursside andmete sünkroonimiseks vajalikke lahendusi ja vastekaarte. See sisaldab järgmist kolme lahendust.

| Kordumatu nimi                | Kuvatav nimi                             |
|----------------------------|------------------------------------------|
| HCMCommon                  | HCM-i ühine                               |
| msdyn_Dynamics365HCMMaps   | Dynamics 365 Human Resources üksuse vastekaardid |
| msdyn_Dynamics365HCMAnchor | Dynamics 365 Human Resources Ankur      |

Selles paketis on saadaval järgmised vastekaardid.

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

Topeltkirjutuse inimressursside pakett sõltub topeltkirjutuse rakenduse põhipaketist. Seetõttu peaksite installima topeltkirjutuse rakenduse põhipaketi enne topeltkirjutuse inimressursside paketi installimist.

## <a name="dual-write-supply-chain"></a>Topeltkirjutuse hankeahel

Topeltkirjutuse tarneahela pakett sisaldab lahendusi ja vastekaarte, mida on vaja tarneahela halduse andmete sünkroonimiseks. See sisaldab järgmist kolme lahendust.

| Kordumatu nimi                                | Kuvatav nimi                                              |
|--------------------------------------------|-----------------------------------------------------------|
| Dynamics365SupplyChainextended             | Dynamics 365 tarneahelat on laiendatud.                        |
| msdyn_Dynamics365SupplyChainExtendedMaps   | Dynamics 365 Supply Chain Management laiendatud üksuse vastekaardid |
| msdyn_Dynamics365SupplyChainExtendedAnchor | Dynamics 365 Supply Chain Management laiendatud ankur      |

Selles paketis on saadaval järgmised vastekaardid.

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
| CDS-varud sisse                            | msdyn_inventoryonhandentries                  |
| Tootekategooriad                          | msdyn_productcategories                       |
| CDS-varud sisse                            | msdyn_inventoryonhandrequests                 |
| Tootenumbriga tuvastatud vöötkood           | msdyn_productbarcodes                         |
| Kliendikaart                                | msdyn_loyaltycards                            |
| Püsikliendi preemiapunktid                       | msdyn_loyaltyrewardpoints                     |
| Hinna kliendigrupid                       | msdyn_pricecustomergroups                     |
| Saidid                                       | msdyn_operationalsites                        |
| CDS-i müügipakkumise read                   | Pakkumise üksikasjad                                  |
| CDS-i müügitellimuse read                       | müügitellimuse üksikasjad                             |

**Sõltuvuse teave**

Topeltkirjutuse tarneahela pakett sõltub järgmisest kolmest paketist. Seetõttu peaksite need paketid installima enne tarneahela topeltkirjutuse paketi installimist.

- Topeltkirjutuse rakenduse tuumpakett
- Topeltkirjutuse finantspakett
- Topeltkirjutuse inimressursside pakett

## <a name="dual-write-finance"></a>Topeltkirjutuse finantsid

Topeltkirjutuse finantspakett sisaldab Dynamics 365 Financei andmete sünkroonimiseks vajalikke lahendusi ja vastekaarte. See sisaldab järgmist nelja lahendust.

| Kordumatu nimi                            | Kuvatav nimi                               |
|----------------------------------------|-------------------------------------------|
| Dynamics365FinanceExtended             | Dynamics 365 Finance Extended             |
| msdyn_Dynamics365FinanceExtendedMaps   | Dynamics 365 finantside laiendatud üksuse vastekaardid |
| FieldServiceCommon                     | Väljateenuse üldine                      |
| msdyn_Dynamics365FinanceExtendedAnchor | Dynamics 365 finantside laiendatud ankur      |

Selles paketis on saadaval järgmised vastekaardid.

| Finance and Operationsi rakendused             | Klientide kaasamise rakendused        |
|-----------------------------------------|---------------------------------|
| Kinnipeetava maksu grupid                  | msdyn_withholdingtaxgroups      |
| CDS Contacts V2 (klient)              | kontaktid                        |
| CDS-kontaktid V2 (hankija)                | kontaktid                        |
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
| Pearaamat                                  | msdyn_ledgers                   |
| Kliendid V3                            | kontod                        |

**Sõltuvuse teave**

Topeltkirjutuse finantspakett sõltub topeltkirjutuse rakenduse põhipaketist. Seetõttu peate installima topeltkirjutuse rakenduse põhipaketi enne topeltkirjutuse finantside paketi installimist.

## <a name="dual-write-notes"></a>Topeltkirjutusmärkmed

Topeltkirjutuse märkuste pakett sisaldab lahendusi ja vastendusi, mida on vaja märkuse või marginaali andmete sünkroonimiseks. See sisaldab järgmist nelja lahendust.

| Kordumatu nimi                  | Kuvatav nimi                   |
|------------------------------|--------------------------------|
| Dynamics365notes             | Dynamics 365 märkused             |
| Dynamics365NotesExtended     | Dynamics 365-märkusi on laiendatud.    |
| msdyn_Dynamics365NotesMaps   | Dynamics 365 märkuste üksuse vastemed |
| msdyn_Dynamics365NotesAnchor | Dynamics 365 märkuste ankur      |

Selles paketis on saadaval järgmised vastekaardid.

| Finance and Operations                     | Customer Engagement |
|--------------------------------------------|---------------------|
| Müügitellimuse päise dokumendi manused    | Marginaalid         |
| Kliendi manused                       | Marginaalid         |
| Hankija dokumendimanused                | Marginaalid         |
| Ostutellimuse päise dokumendi manused | Marginaalid         |

**Sõltuvuse teave**

Topeltkirjutuse märkuste pakett sõltub kahest järgmisest paketist. Seetõttu peaksite need paketid installima enne topeltkirjutuse märkuste paketi installimist.

- Topeltkirjutuse rakenduse tuumpakett
- Topeltkirjutuse finantspakett

## <a name="dual-write-asset-management"></a>Topeltkirjutuse varahaldus

Topeltkirjutuse varahalduse pakett sisaldab lahendusi ja vastekaarte, mida on vaja varade haldamisest või kaartidest sünkroonimiseks Dynamics 365 Field Service. See sisaldab järgmist nelja lahendust.

| Kordumatu nimi                          | Kuvatav nimi                              |
|--------------------------------------|-------------------------------------------|
| Dynamics365AssetManagement           | Dynamics 365 varahaldus             |
| Dynamics365AssetManagementApp        | Dynamics365 varahalduse rakendus          |
| msdyn_DualWriteAssetManagementMaps   | Dynamics 365 varahalduse üksuse vastekaardid |
| msdyn_DualWriteAssetManagementAnchor | Dynamics 365 varahalduse ankur      |

Selles paketis on saadaval järgmised vastekaardid.

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

Topeltkirjutuse varahalduse pakett sõltub topeltkirjutuse rakenduse põhipaketist. Seetõttu peate installima topeltkirjutuse rakenduse põhipaketi enne topeltkirjutuse varahalduse paketi installimist.

## <a name="packages-required-for-project-operations"></a>Projektitoiminguteks vajalikud paketid
Projektitoimingud sõltuvad järgmistest pakettdest. Seetõttu peaksite need paketid installima enne projektitoimingute installimist.

- Topeltkirjutuse rakenduse tuumpakett
- Topeltkirjutuse finantspakett
- Topeltkirjutuse tarneahela pakett
- Topeltkirjutuse varahalduse pakett
- Topeltkirjutuse inimressursside pakett

## <a name="dual-write-party-and-global-address-book-solutions"></a>Topeltkirjutuse osapoole ja globaalse aadressiraamatu lahendused

Topeltkirjutuse osapool ja globaalse aadressiraamatu pakett sisaldab järgmisi lahendusi ja vastekaarte, mida on vaja osapoole ja globaalse aadressiraamatu andmete sünkroonimiseks. 

| Kordumatu nimi                       | Kuvatav nimi                            |
|-----------------------------------|-----------------------------------------|
| Osapool                             | Osapool                                   |
| Dynamics365GAB laiendatud            | Dynamics 365 laiendatud GAB               |
| Dynamics365GABDualWriteEntityMaps | Dynamics 365 GAB topeltkirjutuse üksuse vastekaardid |
| Dynamics365GABParty_Anchor        | Dynamics 365 osaline jagav osaline              |

Selles paketis on saadaval järgmised vastekaardid.

| Finance and Operations rakendused | Klientide kaasamise rakendused | 
|-----------------------------|--------------------------|
| CDS osapooled | msdyn_parties | 
| CDS-i postiaadressi asukohad | msdyn_postaladdresscollections | 
| CDS-i postiaadressi ajalugu V2 | msdyn_postaladdresses | 
| CDS-i osapoole postiaadressi asukohad | msdyn_partypostaladdresses | 
| Osapoole kontaktid V3 | msdyn_partyelectronicaddresses | 
| Kliendid V3 | kontod | 
| Kliendid V3 | kontaktid | 
| Hankijad V2 | msdyn_vendors | 
| Kontaktisiku tiitlid | msdyn_salescontactpersontitles | 
| Viisakusväljendid | msdyn_complimentaryclosings | 
| Tervitused | msdyn_salutations | 
| Otsustamisrollid | msdyn_decisionmakingroles | 
| Tööhõive tööfunktsioonid | msdyn_employmentjobfunctions | 
| Püsikliendi tasemed | msdyn_loyaltylevels | 
| Isiklikud märgitüübid | msdyn_personalcharactertypes | 
| Kontaktid V2 | msdyn_contactforparties | 
| CDS-i müügipakkumise päis | pakkumised | 
| CDS-i müügitellimuse päised | müügitellimused | 
| Müügiarve päised V2 | arved | 
| CDS-aadressi rollid | msdyn_addressroles |

**Sõltuvuse teave**

Topeltkirjutuse osapoole ja globaalse aadressiraamatu lahendused sõltuvad järgmisest kolmest paketist. Seetõttu peaksite need paketid installima enne topeltkirjutuse osapoole ja globaalse aadressiraamatu lahenduste paketi installimist.

- Topeltkirjutuse rakenduse tuumpakett
- Topeltkirjutuse finantspakett
- Topeltkirjutuse tarneahela pakett
