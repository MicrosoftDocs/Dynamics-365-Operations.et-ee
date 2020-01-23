---
title: Ühtne tootekogemus
description: Selles teemas kirjeldatakse tooteandmete integreerimist Finance and Operationsi ja teenuse Common Data Service vahel.
author: t-benebo
manager: AnnBe
ms.date: 12/12/2019
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
ms.openlocfilehash: 7df9097feeb9566705f50f8a62809aa79dc10cd7
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914767"
---
# <a name="unified-product-experience"></a>Ühtne tootekogemus

[!include [banner](../includes/banner.md)]

Kui ettevõtte ökosüsteem koosneb Dynamics 365 rakendustest (nt Finance, Supply Chain Management ja Sales), kasutavad ettevõtted sageli neid rakendusi tooteandmete hankimiseks. Selle põhjuseks on asjaolu, et need rakendused pakuvad vastupidavat tooteinfrastruktuuri, mida täiendavad keerukad hinnakujunduskontseptsioonid ja täpsed käepärased laoandmed. Ettevõtted, mis kasutavad tooteandmete hankimiseks välist toote elutsükli halduse (PLM) süsteemi, saavad tooteid kanalitest Finance and Operations edastada teistele Dynamics 365 rakendustele. Ühtne tootekogemus viib integreeritud tooteandmete mudeli ühisesse andmeteenusesse Common Data Service, nii et kõik rakenduste kasutajad, sealhulgas teenuse Power Platform kasutajad, saavad kasutada rikkalikke tooteandmeid, mis pärinevad rakendustest Finance and Operations.

Siin on toote andmemudel müügist.

![Toodete andmemudel CE-s](media/dual-write-product-4.jpg)

Siin on rakenduse Finance and Operations tooteandmete mudel

![Rakenduse Finance and Operations toodete andmemudel](media/dual-write-products-5.jpg)

Need kaks tooteandmemudelit on integreeritud ühisesse andmeteenusesse Common Data Service, nagu allpool näidatud.

![Dynamics 365 rakenduste toodete andmemudel](media/dual-write-products-6.jpg)

Toodete kahekordse kirjutamise olemikaardid on loodud andmete voogesitamiseks ainult ühesuunaliselt, reaalajas ligipääsetavana rakenduse Finance and Operations teenuses Common Data Service. Kuid toote infrastruktuur on tehtud avatuks, et muuta see vajadusel kahesuunaliseks. Kuid võite seda oma vastutusel kohandada, kuna Microsoft ei soovita seda lähenemist.

## <a name="templates"></a>Mallid

Toote teave sisaldab kogu teavet, mis on seotud tootega ja selle määratlusega, nagu tootedimensioonid või jälgimis- ja laoala dimensioonid. Nagu järgmine tabel näitab, luuakse olemikaartide kogum, et sünkroonida tooteid ja seotud teavet.

Finance and Operations | Muud Dynamics 365 rakendused | Kirjeldus
-----------------------|--------------------------------|---
Väljastatud tooted V2 | msdyn\_sharedproductdetails | **msdyn\_sharedproductdetails** üksus sisaldab välju Finance and Operations rakendustest, mis määratlevad toote ja mis sisaldavad toote finants-ja halduse teavet. 
Common Data Service’is väljastatud eristatavad tooted | Toode | **Toote** üksus sisaldab välju, mis määratlevad toote. See hõlmab üksikuid tooteid (alamtüübiga tooted) ja tootevariante. Järgmises tabelis on vastendused.
Tootenumbriga tuvastatud vöötkood | msdyn\_productbarcodes | Toote vöötkoode kasutatakse toodete unikaalseks identifitseerimiseks.
Tellimuse vaikesätted | msdyn\_productdefaultordersettings
Tootepõhised vaiketellimissätted | msdyn_productdefaultordersettings
Tootedimensiooni grupid | msdyn\_productdimensiongroups | Tootedimensioon määratleb, millised tootedimensioonid määratlevad toote. 
Laoala dimensioonigrupid | msdyn\_productstoragedimensiongroups | Toote laoala dimensiooni grupp tähistab meetodit, mida kasutatakse toote paigutuse määratlemiseks laos.
Jälgimisdimensioonigrupid | msdyn\_producttrackingdimensiongroups | Toote jälgimisdimensiooni grupp tähistab meetodit, mida kasutatakse toote jälgimiseks laos.
Värvid | msdyn\_productcolors
Suurused | msdyn\_productsizes
Laadid | msdyn\_productsytles
Konfiguratsioonid | msdyn\_productconfigurations
Tooteetaloni värvid | msdyn_sharedproductcolors | **Ühiskasutatava tootevärvi** olem näitab värve, mida konkreetne tooteetalon võib sisaldada. Andmete järjepidevuse tagamiseks on see kontseptsioon üle viidud ühisesse andmeteenusesse Common Data Service.
Tooteetaloni suurused | msdyn_sharedproductsizes | Üksus **Ühiskasutatava toote suurus** näitab suurust, mida konkreetne tooteetalon võib sisaldada. Andmete järjepidevuse tagamiseks on see kontseptsioon üle viidud ühisesse andmeteenusesse Common Data Service.
Tooteetaloni laadid | msdyn_sharedproductstyles | **Ühiskasutatava toote stiili** olem näitab stiili, mida konkreetne tooteetalon võib sisaldada. Andmete järjepidevuse tagamiseks on see kontseptsioon üle viidud ühisesse andmeteenusesse Common Data Service.
Tooteetaloni konfiguratsioonid | msdyn_sharedproductconfigurations | **Ühiskasutatava toote konfiguratsiooni** olem näitab konfiguratsioone, mida konkreetne tooteetalon võib sisaldada. Andmete järjepidevuse tagamiseks on see kontseptsioon üle viidud ühisesse andmeteenusesse Common Data Service.
Kõik tooted | msdyn_globalproducts | Kõikide toodete eüksus sisaldab kõiki Finance and Operations rakendustes saadaolevaid tooteid, nii väljastatud kui ka väljastamata tooteid.
Ühik | uoms
Ühiku teisendused | msdyn_ unitofmeasureconversions
Tootepõhise mõõtühiku teisendamine | msdyn_productspecificunitofmeasureconversion
Tootekategooriad | msdyn_productcategories | Iga tootekategooria ning teave selle struktuuri ja omaduste kohta sisaldub tootekategooria üksuses. 
Tootekategooria hierarhiad | msdyn_productcategoryhierarhies | Kasutage kategooriahierarhiaid toodete liigitamiseks või rühmitamiseks. Kategooriahierarhiad on saadaval Common Data Service’is, kasutades tootekategooria hierarhia üksust. 
Tootekategooria hierarhia rollid | msdyn_productcategoryhierarchies | Tootehierarhiaid saab kasutada mitmesuguste rollide jaoks rakenduses D365 Finance and Operations. Selleks et määrata, millist kategooriat igas rollis kasutatakse, kasutatakse tootekategooria rolli üksust. 
Tootekategooria määramised | msdyn_productcategoryassignments | Toote määramiseks kategooriasse võib kasutada tootekategooria määramiste üksust.

## <a name="integration-of-products"></a>Toodete integreerimine

Selles mudelis esindab teenuse Common Data Service toodet kahe üksuse kombinatsioon: **Toode** ja **msdyn\_sharedproductdetails.** Esimene üksus sisaldab toote määratlust (toote ainuidentifikaator, toote nimetus ja kirjeldus), teine üksus sisaldab välju, mis on talletatud toote tasemel. Nende kahe üksuse kombinatsiooni kasutatakse toote määratlemiseks vastavalt varude arvestusühiku mõistele (SKU). Igal väljastatud tootel on oma teave nimetatud üksustes (toote ja ühiskasutatava toote üksikasjad). Kõigi toodete (vabastatud ja mittevabastatud) jälgimiseks kasutatakse üksust **Globaalsed tooted**. 

Kuna toode on esindatud SKUna, saab eristatavate toodete, tooteetalonide ja toote variantide mõisteid jäädvustada teenuses Common Data Service järgmisel viisil:

- **Tooted, mille alamtüübi tooteks** on nende endi määratletud tooted. Dimensioone ei ole vaja määrata. Näitena võib tuua konkreetse raamatu. Nende toodete puhul luuakse **Toote** üksuses üks kirje ja **msdyn\_sharedproductdetails** üksuses teine kirje. Tooteperekonna kirjet pole loodud.
- **Tooteetalone** kasutatakse geneeriliste toodetena, mis hoiavad definitsiooni ja reegleid, mis määravad äriprotsesside käitumise. Nende mõistete põhjal saab luua erinevaid tooteid, mida nimetatakse tootevariantideks. Näiteks T-särk on tooteetalon ja selle dimensioonideks võivad olla värv ja suurus. VaVälja saab anda variante, millel on nendest mõõtmetest erinevad kombinatsioonid, näiteks väike sinine T-särk või keskmine roheline T-särk. Integreerimisel luuakse tootetabelis üks kirje ühe variandi kohta. See kirje sisaldab variandikohast teavet (nt erinevaid dimensioone). Toote üldine teave talletatakse **msdyn\_sharedproductdetails** üksuses. (seda üldteavet hoitakse tooteetalonis.) Lisaks luuakse tooteperekonna kohta üks kirje. Tooteetalon sünkroonitakse teenusea Common Data Service niipea, kui väljaantud tooteetalon on loodud (kuid enne variantide väljaandmist).
- **Eristatavad tooted** viitavad kõigile toodete alamtüübi tootele ja kõigile tootevariantidele. 

![Toodete andmemudel](media/dual-write-product.png)

Kui kahekordse kirjutamise funktsioon on lubatud, sünkroonitakse rakendused Finance and Operations muudes Dynamics 365 rakendustes olekus **Mustand**. Need lisatakse esimesele hinnakirjale, millel on sama valuuta. Teisisõnu lisatakse need esimesele hinnakirjale Dynamics 365 rakenduses, mis vastab teie juriidilise isiku valuutale, kus toode on väljaantud rakenduses Finance and Operations. 

Vaikimisi sünkroonitakse Finance and Operationsi rakenduste tooteid teiste Dynamics 365 rakendustega olekus **Mustand**. Toote sünkroonimiseks olekuga **Aktiivne**, et saaksite seda kasutada näiteks otse müügitellimuse pakkumistes, tuleb valida järgmine säte: **Süsteem > Haldus > Süsteemihaldus > Süsteemi sätted > Müük** ja seejärel suvand **Loo tooteid aktiivses olekus = jah**. 

Pange tähele, et toodete sünkroonimine toimub Finance and Operationsi rakendustest Common Data Service’isse. See tähendab, et toote üksuse väljade väärtusi saab muuta Common Data Service’is, aga kui käivitatakse sünkroonimine (kui tootevälja muudetakse Finance and Operationsi rakenduses), alistab see väärtused Common Data Service’is. 

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [products](dual-write/EcoResReleasedDistinctProductCDSEntity-products.md)]

[!include [product details](dual-write/EcoResReleasedProductV2-msdyn-sharedproductdetails.md)]

[!include [global products](dual-write/EcoResEveryProductEntity-msdyn-globalproducts.md)]

## <a name="product-dimensions"></a>Tootedimensioonid 

Tootedimensioonid on tootevarianti identifitseerivad omadused. Tootevariantide määratlemiseks vastendatakse Common Data Service ka nelja tootedimensiooniga (värv, suurus, stiil ja konfiguratsioon). Järgmisel joonisel on näidatud tootedimensiooni värvi andmetabelit. Sama mudelit rakendatakse suurustele, stiilidele ja konfiguratsioonidele. 

![Toodete andmemudel](media/dual-write-product-2.PNG)

[!include [product colors](dual-write/EcoResProductColorEntity-msdyn-productcolor.md)]

[!include [product sizes](dual-write/EcoResProductSizeEntity-msdyn-productsizes.md)]

[!include [product sizes](dual-write/EcoResProductStyleEntity-msdyn-productstyles.md)]

[!include [product sizes](dual-write/EcoResProductConfigurationsEntity-msdyn-productconfigurations.md)]

Kui tootel on erinevad tootedimensioonid (nt tooteetalonil on suurus ja värv tootedimensioonidena), määratletakse iga eristatav toode (st iga tootevariant) nende dimensioonide kombinatsioonina. Näiteks toode number B0001 on eriti väike must T-särk ja toode number B0002 on väike must T-särk. Sel juhul määratletakse tootedimensioonide olemasolevad kombinatsioonid. Näiteks eelmise näite T-särk võib olla eriti väike ja must, väike ja must, keskmine ja must või suur ja must, kuid see ei saa olla eriti suur ja must. Teisisõnu on määratud tootedimensioonid, mida tooteetalon saab kasutada, ja nende väärtuste alusel saab variante väljastada.

Tootedimensioonide jälgimiseks, mida tooteetalon saab võtta, luuakse ja vastendatakse iga tootedimensiooni jaoks järgmised olemid jaotises Common Data Service. Lisateavet vt teemast [Tooteteabe ülevaade](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/pim/product-information).

[!include [product colors](dual-write/EcoResProductMasterColorEntity-msdyn-sharedproductcolors.md)]

[!include [product sizes](dual-write/EcoResProductMasterSize-msdyn-sharedproductsizes.md)]

[!include [product styles](dual-write/EcoResProductMasterStyleEntity-msdyn-sharedproductstyles.md)]

[!include [product configurations](dual-write/EcoResProductMasterConfigurationEntity-msdyn-sharedproductconfigurations.md)]

[!include [product bar codes](dual-write/EcoResProductNumberIdentifiedBarcode-msdyn-productbarcodes.md)]

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Tellimuse vaikesätted ja tootespetsiifilise vaiketellimuse sätted

Tellimuse vaikesätted määratlevad tegevuskoha ja lao, kust kaupu hangitakse või hoitakse, miinimum-, maksimum-, mitmik- ja standardkogused, mida kasutatakse kaubanduse või varude halduse jaoks, täitmisajad, peatamislipu ja tellimuse lubamise meetodi. See teave on saadaval Common Data Service’is, kasutades tellimuse vaikesätteid ja tootespetsiifilisi tellimuse vaikesätete üksust. Lugege lisateavet funktsioonide kohta teemast [Tellimuse vaikesätted](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/production-control/default-order-settings).

[!include [product sizes](dual-write/InventProductDefaultOrderSettingsEntity-msdyn-productdefaultordersetting.md)]

[!include [product sizes](dual-write/InventProductSpecificOrderSettingsV2Entity-msdyn-productspecificdefaultordersetting.md)]

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Mõõtühik ja mõõtühiku teisendused

Mõõtühikud ja selle vastavad teisendused on saadaval Common Data Service’is, mis järgib diagrammil kuvatavat andmudelit.

![Toodete andmemudel](media/dual-write-product-3.PNG)

Mõõtühiku kontseptsioon on integreeritud Finance and Operations rakenduste ja muude Dynamics 365 rakenduste vahel. Iga ühiku klassi kohta Finance and Operationsi rakenduses luuakse ühiku grupp Dynamics 365 rakenduses, mis sisaldab ühiku klassi kuuluvaid ühikuid. Iga ühikurühma jaoks luuakse ka vaikimisi baasühik. 

[!include [unit of measure](dual-write/UnitOfMeasureEntity-uom.md)]

[!include [unit of measure conversions](dual-write/UnitOfMeasureConversionEntity-msdyn-unitofmeasureconversions.md)]

[!include [product specific unit of measure conversions](dual-write/EcoResProductSpecificUnitConversionEntity-msdyn-productspecificunitofmeasureconversions.md)]

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-common-data-service"></a>Ühikute andmete vastavusse viimise esialgne sünkroonimine Finance and Operationsi ja Common Data Service’i vahel

### <a name="initial-synchronization-of-units"></a>Ühikute esialgne sünkroonimine

Kui topeltkirjutamine on lubatud, sünkroonitakse Finance and Operationsi rakenduste tooteid teiste Dynamics 365 rakendustega. Finance and Operationsi rakendustest Common Data Service’is sünkroonitud ühikute gruppidel on lippude komplekt, mis tähistab, et need on väliselt hallatavad.

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Ühikute ja ühiku klasside/gruppide andmete vastavusse viimine Finance and Operationsist ja muudest Dynamics 365 rakendusest

Kõigepealt on oluline tähele panna, et ühiku integreerimisvõti on msdyn_symbol. Seetõttu peab see väärtus olema kordumatu Common Data Service’is või muudes Dynamics 365 rakendustes. Kuna teistes Dynamics 365 rakendustes määrab ühiku kordumatuse paar Ühiku grupi ID ja Nimi, peate kaaluma erinevaid stsenaariume ühiku andmete vastavusse viimiseks Finance and Operationsi rakenduste ja Common Data Service’i vahel.

Ühikute vastavusse viimiseks / katmiseks Finance and Operationsi rakendustes ja teistes Dynamics 365 rakendustes tehke järgmist.

+ **Ühik kuulub ühikute gruppi teistes Dynamics 365 rakendustes, mis vastavad seotud ühiku klassile Finance and Operationsi rakendustes**. Sellisel juhul tuleb väli msdyn_symbol teistes Dynamics 365 rakendustes täita ühiku sümboliga Finance and Operationsi rakendustest. Seega kui andmed viiakse vastavusse, siis seatakse ühikute grupp teistes Dynamics 365 rakendustes väliselt hallatavaks.
+ **Ühiku kuulub ühikute gruppi teistes Dynamics 365 rakendustes, mis ei vasta seotud ühiku klassile Finance and Operationsi rakendustes (puudub ühiku klass Finance and Operationsi rakendustes ühiku klassile teistes Dynamics 365 rakendustes).** Sellisel juhul tuleb väli msdyn_symbol täita suvalise stringiga. Pange tähele, et see väärtus peab olema kordumatu teistes Dynamics 365 rakendustes.

Ühikute ja ühiku klasside jaoks, mida teistes Dynamics 365 rakendustes ei ole, tehke järgmist.

Osana topeltkirjutamisest luuakse ja sünkroonitakse ühikute grupid Finance and Operationsi rakendustest ning neile vastavad ühikud teistes Dynamics 365 rakendustes ja Common Data Service’is ning ühikute grupp määratakse väliselt hallatavaks. Täiendavat alglaadimist pole vaja.

Ühikute jaoks teistes Dynamics 365 rakendustes, mida pole Finance and Operationsi rakendustes, tehke järgmist.

Väli msdyn_symbol tuleb täita kõikide ühikute kohta. Ühikuid saab alati luua Finance and Operationsi rakendustes vastavas ühiku klassis (kui see on olemas). Kui ühiku klassi pole, tuleb kõigepealt luua ühiku klass (pange tähele, et ühiku klassi ei saa luua Finance and Operationsi rakendustes muud moodi kui läbi laienduse, kui laiendate loetelu), mis vastab teiste Dynamics 365 rakenduste ühiku grupile. Seejärel saate luua ühiku. Pange tähele, et ühiku sümbol Finance and Operationsi rakendustes peab olema varem teistes Dynamics 365 rakendustes ühikuks määratud msdyn_symbol.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Tootepoliitika: dimensioon, jälgimise ja laoala grupid

Tootepoliitikad on poliitikakogumid, mida kasutatakse toodete ja selle omaduste määratlemiseks laos. Tootedimensiooni gruppi, toote jälgimisdimensiooni gruppi ja laoala dimensiooni gruppi võib leida tootepoliitikana. 

[!include [product dimension group](dual-write/EcoResProductDimensionGroup-msdyn-productdimensiongroups.md)]

[!include [product tracking dimension group](dual-write/EcoResTrackingDimensionGroup-msdyn-producttrackingdimensiongroups.md)]

[!include [product storage dimension group](dual-write/EcoResStorageDimensionGroup-msdyn-productstoragedimensiongroups.md)]

## <a name="product-hierarchies"></a>Tootehierarhiad

[!include [product category hierarchy](dual-write/EcoResProductCategoryHierarchyEntity-msdyn-productcategoryhierarchy.md)]

[!include [product category](dual-write/EcoResProductCategoryEntity-msdyn-productcategory.md)]

[!include [product category assignments](dual-write/EcoResProductCategoryAssignmentEntity-msdyn-productcategoryassignment.md)]

[!include [product category role](dual-write/EcoResProductCategoryHierarchyRoleEntity-msdyn-productcategoryhierarchyrole.md)]


## <a name="integration-key-for-products"></a>Toodete integreerimisvõti 

Toodete kordumatuks tuvastamiseks Dynamics 365 for Finance and Operationsi ja Common Data Service’i toodete vahel kasutatakse integreerimisvõtmeid. Toodete integreerimisvõti on **(productnumber)**, millega tuvastatakse toode Common Data Service’is. Selles on liidetud järgmised üksused: **(ettevõte, msdyn_productnumber)**. Üksus **ettevõte** tähistab juriidilist isikut Finance and Operationsis ja **msdyn_productnumber** tähistab määratud toote tootenumbrit Finance and Operationsis. 

Teiste Dynamics 365 rakenduste kasutaja jaoks tuvastatakse toode kasutajaliideses üksusega **msdyn_productnumber** (pange tähele, et välja silt on **Tootenumber**). Toote vormil kuvatakse nii ettevõte kui ka msydn_productnumber. Kuid välja (productnumber), toote kordumatut võtit, ei kuvata. 

Pange tähele, et kui rakendused ehitatakse Common Data Service’i peale, tuleb eraldi tähelepanu pöörata välja (productnumber) kasutamisele, mis on toote kordumatu ID, nagu integreerimisvõti, mitte msdyn_productnumber, kuna viimane ei ole kordumatu. 

## <a name="initial-synchronization-of-products-and-migration-of-data-from-common-data-service-to-finance-and-operations"></a>Toodete esialgne sünkroonimine ja andmete migreerimine Common Data Service’ist Finance and Operationsisse

### <a name="initial-synchronization-of-products"></a>Toodete esialgne sünkroonimine 

Kui topeltkirjutamine on lubatud, sünkroonitakse Dynamics 365 Finance and Operationsi tooteid Common Data Service’i ja teiste Dynamics 365 rakendustega. Pange tähele, et Common Data Service’is ja teistes Dynamics 365 rakendustes enne topeltkirjutamist loodud tooteid ei värskendata ega viida vastavusse toote andmetega Finance and Operationsist.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Toote andmete vastavusse viimine Finance and Operationsi ja teiste Dynamics 365 rakendustega

Kui samu tooteid säilitatakse (kattuvad/ühtivad) Finance and Operationsis ja Common Data Service’is ning teistes Dynamics 365 rakendustes, toimub Finance and Operationsi toodete sünkroonimise topeltkirjutamise lubamine ja duplikaatkirjed kuvatakse Common Data Service’is sama toote kohta.
Kui teistes Dynamics 365 rakendustes on tooteid, mis kattuvad / on vastavuse Finance and Operationsi toodetega, peab topeltkirjutamise lubanud administraator eelmise olukorra vältimiseks alglaadima väljad **Ettevõte** (nt USMF) ja **msdyn_productnumber** (nt 1234:Black:S), enne kui toimub toodete sünkroonimine. Teisisõnu tuleb kaks välja Common Data Service’i tootes täita vastava ettevõttega Finance and Operationsis, millele toode peab vastama, ja selle tootenumbriga. 

Kui seejärel sünkroonimine lubatakse ja see toimub, sünkroonitakse tooteid Finance and Operationsist vastavusse viidud toodetega Common Data Service’is ja teistes Dynamics 365 rakendustes. See kehtib nii eristatavate toodete kui ka tootevariantide kohta. 


### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Toote andmete migreerimine teistest Dynamics 365 rakendustest Finance and Operationsisse

Kui teistes Dynamics 365 rakendustes on tooteid, mida ei esine Finance and Operationsis, võib administraator kõigepealt kasutada üksust **EcoResReleasedProductCreationV2Entity** nende toodete importimiseks Finance and Operationsis. Järgmiseks tuleb viia vastavusse toote andmed Finance and Operationsist ja teistest Dynamics 365 rakendustest, nagu on kirjeldatud üleval. 
