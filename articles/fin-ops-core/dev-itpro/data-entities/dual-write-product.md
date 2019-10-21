---
title: Ühtne tootekogemus
description: Selles teemas kirjeldatakse tooteandmete integreerimist Finance and Operationsi ja teenuse Common Data Service vahel.
author: t-benebo
manager: AnnBe
ms.date: 09/3/2019
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
ms.openlocfilehash: 9dc26e0e50c0b77555d09e4a50b846c80b1d5760
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249324"
---
# <a name="unified-product-experience"></a>Ühtne tootekogemus

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Kui ettevõtte ökosüsteem koosneb Dynamics 365 rakendustest (nt Rahandus, Supply Chain Managemen ja Sales), on loomulik, et kliendid kasutavad neid rakendusi tooteandmete hankimiseks. Selle põhjuseks on asjaolu, et need rakendused pakuvad vastupidavat tooteinfrastruktuuri, mida täiendavad keerukad hinnakujunduskontseptsioonid ja täpsed käepärased laoandmed. Kliendid, kes kasutavad tooteandmete hankimiseks välist toote elutsükli halduse (PLM) süsteemi, saavad tooteid kanalitest Finance and Operations edastada teistele Dynamics 365 rakendustele. Ühtne tootekogemus viib integreeritud tooteandmete mudeli ühisesse andmeteenusesse Common Data Service, nii et kõik rakenduste kasutajad, sealhulgas teenuse Power Platform kasutajad, saavad kasutada rikkalikke tooteandmeid, mis pärinevad rakendustest Finance and Operations.

Siin on toote andmemudel müügist.

![Toodete müügi andmemudel](media/dual-write-product-4.jpg)

Siin on rakenduse Finance and Operations tooteandmete mudel

![Rakenduse Finance and Operations toodete andmemudel](media/dual-write-products-5.jpg)

Need kaks tooteandmemudelit on integreeritud ühisesse andmeteenusesse Common Data Service, nagu allpool näidatud.

![Dynamics 365 rakenduste toodete andmemudel](media/dual-write-products-6.jpg)

Toodete kahekordse kirjutamise olemikaardid on loodud andmete voogesitamiseks ainult ühesuunaliselt ning see on reaalajas ligipääsetav kogemus rakenduse Finance and Operations rakendusest Common Data Service. Kuid toote infrastruktuur on tehtud avatuks, et muuta see vajadusel kahesuunaliseks. Kliendid saavad seda oma riisikol kohandada, kuna Microsoft ei soovita seda lähenemist.

## <a name="templates"></a>Mallid

Toote teave sisaldab kogu teavet, mis on seotud tootega ja selle määratlusega, nagu tootedimensioonid või jälgimise ja laoala dimensioonid. Nagu järgmine tabel näitab, luuakse olemikaartide kogum, et sünkroonida tooteid ja seotud teavet.

Finance and Operations | Muud Dynamics 365 rakendused
-----------------------|--------------------------------
Väljastatud tooted V2 | msdyn\_sharedproductdetails
CDS väljastatud eristatavad tooted | Toode
Tootenumbriga tuvastatud vöötkood | msdyn\_productbarcodes
Tellimuse vaikesätted | msdyn\_productdefaultordersettings
Tootepõhised vaiketellimissätted | msdyn_productspecificdefaultordersettings
Tootedimensiooni grupid | msdyn\_productdimensiongroups
Laoala dimensioonigrupid | msdyn\_productstoragedimensiongroups
Jälgimisdimensioonigrupid | msdyn\_producttrackingdimensiongroups
Värvid | msdyn\_productcolors
Suurused | msdyn\_productsizes
Laadid | msdyn\_productsytles
Konfiguratsioonid | msdyn\_productconfigurations
Tooteetaloni värvid | msdyn_sharedproductcolors
Tooteetaloni suurused | msdyn_sharedproductsizes
Tooteetaloni laadid | msdyn_sharedproductstyles
Tooteetaloni konfiguratsioonid | msdyn_sharedproductconfigurations
Kõik tooted | msdyn_globalproducts
Ühik | uoms
Ühiku teisendused | msdyn_ unitofmeasureconversions
Tootepõhise mõõtühiku teisendamine | msdyn_productspecificunitofmeasureconversion
Saidid | msdyn\_operationalsites
Laod | msdyn\_inventwarehouses

[!include [symbols](../includes/dual-write-symbols.md)]

## <a name="integration-of-products"></a>Toodete integreerimine

Selles mudelis esindab teenuse Common Data Service toodet kahe üksuse kombinatsioon: **Toode** ja **msdyn\_sharedproductdetails.** Esimene üksus sisaldab toote määratlust (toote ainuidentifikaator, toote nimetus ja kirjeldus), teine üksus sisaldab välju, mis on talletatud toote tasemel. Nende kahe üksuse kombinatsiooni kasutatakse toote määratlemiseks vastavalt varude arvestusühiku mõistele (SKU). Igal väljastatud tootel on oma teave nimetatud üksustes (toote ja ühiskasutatava toote üksikasjad). Kõigi toodete (vabastatud ja mittevabastatud) jälgimiseks kasutatakse **Globaalsete toodete** üksust. 

Kuna toode on esindatud SKUna, saab eristatavate toodete, tooteetalonide ja toote variantide mõisteid jäädvustada teenuses Common Data Service järgmisel viisil:

- **Tooted, mille alamtüübi tooteks** on nende endi määratletud tooted. Nende jaoks ei ole dimensioone määratud. Näitena võib tuua konkreetse raamatu. Nende toodete puhul luuakse **Toote** üksuses üks kirje ja **msdyn\_sharedproductdetails** üksuses teine kirje. Tooteperekonna kirjet pole loodud.
- **Tooteetalone** kasutatakse geneeriliste toodetena, mis hoiavad definitsiooni ja reegleid, mis määravad äriprotsesside käitumise. Nende mõistete põhjal saab luua erinevaid tooteid, mida nimetatakse tootevariantideks. Näiteks T-särk on tooteetalon ja selle dimensioonideks võivad olla värv ja suurus. VaVälja saab anda variante, millel on nendest mõõtmetest erinevad kombinatsioonid, näiteks väike sinine T-särk või keskmine roheline T-särk. Integreerimisel luuakse tootetabelis üks kirje ühe variandi kohta. See kirje sisaldab variandikohast teavet (nt erinevaid dimensioone). Toote üldine teave talletatakse **msdyn\_sharedproductdetails** üksuses. (seda üldteavet hoitakse tooteetalonis.) Lisaks luuakse tooteperekonna kohta üks kirje. Tooteetalon sünkroonitakse teenusea Common Data Service niipea, kui väljaantud tooteetalon on loodud (kuid enne variantide väljaandmist).
- **Eristatavad tooted** viitavad kõigile toodete alamtüübi tootele ja kõigile tootevariantidele. 

![Toodete andmemudel](media/dual-write-product.png)

Kui kahekordse kirjutamise funktsioon on lubatud, sünkroonitakse rakendused Finance and Operations muudes Dynamics 365 rakendustes olekus **Mustand**. Need lisatakse esimesele hinnakirjale, millel on sama valuuta. Teisisõnu lisatakse need esimesele hinnakirjale Dynamics 365 rakenduses, mis vastab teie juriidilise isiku valuutale, kus toode on väljaantud rakenduses Finance and Operations. 

Toote sünkroonimiseks **Aktiivse** olekuga saate seda otse müügitellimuse pakkumistes kasutada, näiteks tuleb valida järgmine säte: **Süsteem > Haldus > Süsteemihaldus > Süsteemi sätted > Müük**, valige **Loo tooteid aktiivses olekus = jah**. 

### <a name="cds-released-distinct-products-to-product"></a>CDS andis tootele välja eristatavad tooted

**Toote** üksus sisaldab välju, mis määratlevad toote. See hõlmab üksikuid tooteid (alamtüübiga tooted) ja tootevariante. Järgmises tabelis on vastendused.

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
PRODUCTNUMBER | >> | productnumber
PRODUCTNAME | >> | nimi
PRODUCTDESCRIPTION | >> | kirjeldus
ITEMNUMBER | >> | msdyn_itemnumber
CURRENCYCODE | >> | transactioncurrencyid.isocurrencycode
SALESUNITSYMBOL | >> | defaultuomid.msdyn_symbol
SALESPRICE | >> | hind
UNITCOST | >> | currentcost
PRODUCTTYPE | >> | producttypecode
SALESUNITDECIMALPRECISION | >> | quantitydecimal
ISCATCHWEIGHTPRODUCT | >> | msdyn_iscatchweight
PRODUCTCOLORID | >> | msdyn_productcolor.msdyn_productcolorname
PRODUCTCONFIGURATIONID | >> | msdyn_productconfiguration.msdyn_productconfiguration
PRODUCTSIZEID | >> | msdyn_productsize.msdyn_productsize
PRODUCTSTYLEID | >> | msdyn_productstyle.msdyn_productstyle

### <a name="released-products-v2-to-msdyn_sharedproductdetails"></a>Released products V2 to msdyn\_sharedproductdetails

**msdyn\_sharedproductdetails** üksus sisaldab välju Finance and Operations rakendustest, mis määratlevad toote ja mis sisaldavad toote finants-ja halduse teavet. Järgmises tabelis on vastendused.

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
PRODUCTNUMBER | > | msdyn_globalproduct.msdyn_productnumber
INTRASTATCHARGEPERCENTAGE | > | msdyn_intrastatchargepercentage
ITEMNUMBER | >> | msdyn_itemnumber
APPROXIMATESALESTAXPERCENTAGE | > | msdyn_approximatesalestaxpercentage
BESTBEFOREPERIODDAYS | > | msdyn_bestbeforeperioddays
CARRYINGCOSTABCCODE | >> | msdyn_carryingcostabccode
CONSTANTSCRAPQUANTITY | > | msdyn_constantscrapquantity
COSTCHARGESQUANTITY | > | msdyn_costchargesquantity
DEFAULTRECEIVINGQUANTITY | > | msdyn_defaultreceivingquantity
FIXEDPURCHASEPRICECHARGES | > | msdyn_fixedpurchasepricecharges
FIXEDSALESPRICECHARGES | > | msdyn_fixedsalespricecharges
GROSSDEPTH | > | msdyn_grossdepth
GROSSPRODUCTHEIGHT | > | msdyn_grossproductheight
GROSSPRODUCTWIDTH | > | msdyn_grossproductwidth
INVENTORYUNITSYMBOL | > | msdyn_inventoryunitsymbol.msdyn_symbol
ISDISCOUNTPOSREGISTRATIONPROHIBITED | >> | msdyn_isdiscountposregistrationprohibited
ISEXEMPTFROMAUTOMATICNOTIFICATIONANDCANCELLATION | >> | msdyn_exemptautomaticnotificationcancel
ISINSTALLMENTELIGIBLE | >> | msdyn_isinstallmenteligible
ISINTERCOMPANYPURCHASEUSAGEBLOCKED | >> | msdyn_isintercompanypurchaseusageblocked
ISINTERCOMPANYSALESUSAGEBLOCKED | >> | msdyn_isintercompanysalesusageblocked
ISMANUALDISCOUNTPOSREGISTRATIONPROHIBITED | >> | msdyn_ismanualdiscposregistrationprohibited
ISPHANTOM | >> | msdyn_isphantom
ISPOSREGISTRATIONBLOCKED | >> | msdyn_isposregistrationblocked
ISPOSREGISTRATIONQUANTITYNEGATIVE | >> | msdyn_isposregistrationquantitynegative
ISPURCHASEPRICEAUTOMATICALLYUPDATED | >> | msdyn_ispurchasepriceautomaticallyupdated
ISPURCHASEPRICEINCLUDINGCHARGES | >> | msdyn_ispurchasepriceincludingcharges
ISSALESWITHHOLDINGTAXCALCULATED | >> | msdyn_issaleswithholdingtaxcalculated
ISRESTRICTEDFORCOUPONS | >> | msdyn_isrestrictedforcoupons
ISSALESPRICEADJUSTMENTALLOWED | >> | msdyn_issalespriceadjustmentallowed
ISSALESPRICEINCLUDINGCHARGES | >> | msdyn_issalespriceincludingcharges
ISSCALEPRODUCT | >> | msdyn_isscaleproduct
ISSHIPALONEENABLED | >> | msdyn_isshipaloneenabled
ISUNITCOSTPRODUCTVARIANTSPECIFIC | >> | msdyn_isunitcostproductvariantspecific
ISVARIANTSHELFLABELSPRINTINGENABLED | >> | msdyn_isvariantshelflabelsprintingenabled
ISZEROPRICEPOSREGISTRATIONALLOWED | >> | msdyn_iszeropriceposregistrationallowed
KEYINPRICEREQUIREMENTSATPOSREGISTER | >> | msdyn_keyinpricerequirementsatposregister
KEYINQUANTITYREQUIREMENTSATPOSREGISTER | >> | msdyn_keyinquantityrequirementsatposregister
MARGINABCCODE | >> | msdyn_marginabccode
MAXIMUMPICKQUANTITY | > | msdyn_maximumpickquantity
MUSTKEYINCOMMENTATPOSREGISTER | >> | msdyn_mustkeyincommentatposregister
NECESSARYPRODUCTIONWORKINGTIMESCHEDULINGPROPERTYID | > | msdyn_necessaryproductionworkingtimeschedulingp
NETPRODUCTWEIGHT | > | msdyn_netproductweight
PACKINGDUTYQUANTITY | > | msdyn_packingdutyquantity
POSREGISTRATIONACTIVATIONDATE | > | msdyn_posregistrationactivationdate
POSREGISTRATIONBLOCKEDDATE | > | msdyn_posregistrationblockeddate
POSREGISTRATIONPLANNEDBLOCKEDDATE | > | msdyn_posregistrationplannedblockeddate
POTENCYBASEATTIBUTETARGETVALUE | > | msdyn_potencybaseattibutetargetvalue
POTENCYBASEATTRIBUTEVALUEENTRYEVENT | >> | msdyn_potencybaseattributevalueentryevent
PRODUCTTYPE | >> | msdyn_producttype
PRODUCTIONCONSUMPTIONDENSITYCONVERSIONFACTOR | > | msdyn_productionconsumptiondensityconversion
PRODUCTIONCONSUMPTIONDEPTHCONVERSIONFACTOR | > | msdyn_productionconsumptiondepthconversion
PRODUCTIONCONSUMPTIONHEIGHTCONVERSIONFACTOR | > | msdyn_productionconsumptionheightconversion
PRODUCTIONCONSUMPTIONWIDTHCONVERSIONFACTOR | > | msdyn_productionconsumptionwidthconversion
PRODUCTVOLUME | > | msdyn_productvolume
PURCHASECHARGESQUANTITY | > | msdyn_purchasechargesquantity
PURCHASEOVERDELIVERYPERCENTAGE | > | msdyn_purchaseoverdeliverypercentage
PURCHASEPRICE | > | msdyn_purchaseprice
PURCHASEPRICEDATE | > | msdyn_purchasepricedate
PURCHASEPRICINGPRECISION | > | msdyn_purchasepricingprecision
PURCHASEUNDERDELIVERYPERCENTAGE | > | msdyn_purchaseunderdeliverypercentage
RAWMATERIALPICKINGPRINCIPLE | >> | msdyn_rawmaterialpickingprinciple
SALESCHARGESQUANTITY | > | msdyn_saleschargesquantity
SALESOVERDELIVERYPERCENTAGE | > | msdyn_salesoverdeliverypercentage
SALESPRICE | > | msdyn_salesprice
SALESPRICECALCULATIONCHARGESPERCENTAGE | > | msdyn_salespricecalculationchargespercentage
SALESPRICECALCULATIONCONTRIBUTIONRATIO | > | msdyn_salespricecalculationcontributionratio
SALESPRICECALCULATIONMODEL | >> | msdyn_salespricecalculationmodel
SALESPRICEDATE | > | msdyn_salespricedate
SALESPRICINGPRECISION | > | msdyn_salespricingprecision
SALESUNDERDELIVERYPERCENTAGE | > | msdyn_salesunderdeliverypercentage
SALESUNITSYMBOL | > | msdyn_salesunitsymbol.msdyn_symbol
SCALEINDICATOR | >> | msdyn_scaleindicator
SELLSTARTDATE | > | msdyn_sellstartdate
SHELFADVICEPERIODDAYS | > | msdyn_shelfadviceperioddays
SHELFLIFEPERIODDAYS | > | msdyn_shelflifeperioddays
SHIPSTARTDATE | > | msdyn_shipstartdate
TAREPRODUCTWEIGHT | > | msdyn_tareproductweight
TRANSFERORDEROVERDELIVERYPERCENTAGE | > | msdyn_transferorderoverdeliverypercentage
TRANSFERORDERUNDERDELIVERYPERCENTAGE | > | msdyn_transferorderunderdeliverypercentage
UNITCOST | > | msdyn_unitcost
UNITCOSTDATE | > | msdyn_unitcostdate
UNITCOSTQUANTITY | > | msdyn_unitcostquantity
VARIABLESCRAPPERCENTAGE | > | msdyn_variablescrappercentage
WAREHOUSEMOBILEDEVICEDESCRIPTIONLINE1 | > | msdyn_warehousemobiledevicedescriptionline1
WAREHOUSEMOBILEDEVICEDESCRIPTIONLINE2 | > | msdyn_warehousemobiledevicedescriptionline2
WILLINVENTORYISSUEAUTOMATICALLYREPORTASFINISHED | >> | msdyn_willinventoryissueautoreportasfinished
WILLINVENTORYRECEIPTIGNOREFLUSHINGPRINCIPLE | >> | msdyn_willinventoryreceiptignoreflushing
WILLPICKINGWORKBENCHAPPLYBOXINGLOGIC | >> | msdyn_willpickingworkbenchapplyboxinglogic
WILLTOTALPURCHASEDISCOUNTCALCULATIONINCLUDEPRODUCT | >> | msdyn_willtotalpurchdiscountcalcincludeproduct
WILLTOTALSALESDISCOUNTCALCULATIONINCLUDEPRODUCT | >> | msdyn_willtotalsalesdiscountcalcincludeproduct
WILLWORKCENTERPICKINGALLOWNEGATIVEINVENTORY | >> | msdyn_willworkcenterpickingallownegativeinvent
YIELDPERCENTAGE | > | msdyn_yieldpercentage
ISUNITCOSTAUTOMATICALLYUPDATED | >> | msdyn_isunitcostautomaticallyupdated
PURCHASEUNITSYMBOL | > | msdyn_purchaseunitsymbol.msdyn_symbol
PURCHASEPRICEQUANTITY | > | msdyn_purchasepricequantity
ISUNITCOSTINCLUDINGCHARGES | >> | msdyn_isunitcostincludingcharges
FIXEDCOSTCHARGES | >> | msdyn_fixedcostcharges
MINIMUMCATCHWEIGHTQUANTITY | >> | msdyn_minimumcatchweightquantity
MAXIMUMCATCHWEIGHTQUANTITY | >> | msdyn_maximumcatchweightquantity
ALTERNATIVEITEMNUMBER | >> | msdyn_alternativeitemnumber.msdyn_itemnumber
BOMUNITSYMBOL | >> | msdyn_bomunitsymbol.msdyn_symbol
CATCHWEIGHTUNITSYMBOL | >> | msdyn_catchweightunitsymbol.msdyn_symbol
COMPARISONPRICEBASEUNITSYMBOL | >> | msdyn_comparisonpricebaseunitsymbol.msdyn_symbol
PRIMARYVENDORACCOUNTNUMBER | >> | msdyn_vendorid.msdyn_vendoraccountnumber
ISCATCHWEIGHTPRODUCT | >> | msdyn_iscatchweight
PRODUCTDIMENSIONGROUPNAME | >> | msdyn_productdimensiongroupid.msdyn_groupname

## <a name="all-product-to-msdyn_global-products"></a>Kõik tooted msdyn_global toodetele

Kõikide toodete eüksus sisaldab kõiki Finance and Operations rakendustes saadaolevaid tooteid, nii väljastatud kui ka väljastamata tooteid. Tooted on saadaval rakenduses Common Data Service järgmiste vastenduste abil.

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
PRODUCTNAME | >> | msdyn_productname
PRODUCTNUMBER | >> | msdyn_productnumber

## <a name="product-dimensions"></a>Tootedimensioonid 

Tootedimensioonid on tootevarianti identifitseerivad omadused. Tootevariantide määratlemiseks vastendatakse Common Data Service ka nelja tootedimensiooniga (värv, suurus, stiil ja konfiguratsioon). Järgmisel joonisel on näidatud tootedimensiooni värvi andmetabelit. Sama mudelit rakendatakse suurustele, stiilidele ja konfiguratsioonidele. 

![Toodete andmemudel](media/dual-write-product-2.PNG)

### <a name="colors"></a>Värvid

Võimalikud värvid on saadaval teenuse Common Data Service järgmistes vastendustes.

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
COLORID | \>\> | msdyn\_productcolorname

### <a name="sizes"></a>Suurused

Võimalikud suurused on saadaval teenuse Common Data Service järgmistes vastendustes.

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
SIZEID | \>\> | msdyn\_productsize

### <a name="styles"></a>Laadid

Võimalikud stiilid on saadaval teenuse Common Data Service järgmistes vastendustes.

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
STYLEID | \>\> | msdyn\_productstyle

### <a name="configurations"></a>Konfiguratsioonid

Võimalikud konfiguratsioonid on saadaval teenuse Common Data Service järgmistes vastendustes.

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
CONFIGURATIONID | \>\> | msdyn\_nimi

Kui tootel on erinevad tootedimensioonid (nt tooteetalonil on suurus ja värv tootedimensioonidena), määratletakse iga eristatav toode (st iga tootevariant) nende dimensioonide kombinatsioonina. Näiteks toode number B0001 on eriti väike must T-särk ja toode number B0002 on väike must T-särk. Sel juhul määratletakse tootedimensioonide olemasolevad kombinatsioonid. Näiteks eelmise näite T-särk võib olla eriti väike ja must, väike ja must, keskmine ja must või suur ja must, kuid see ei saa olla eriti suur ja must. Teisisõnu on määratud tootedimensioonid, mida tooteetalon saab kasutada, ja nende väärtuste alusel saab variante väljastada.

Tootedimensioonide jälgimiseks, mida tooteetalon saab võtta, luuakse ja vastendatakse iga tootedimensiooni jaoks järgmised olemid jaotises Common Data Service. Lisateavet vt teemast [Tooteteabe ülevaade](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/pim/product-information).

### <a name="shared-product-color"></a>Ühiskasutatav tootevärv

**Ühiskasutatava tootevärvi** olem näitab värve, mida konkreetne tooteetalon võib sisaldada. Andmete järjepidevuse tagamiseks on see kontseptsioon üle viidud ühisesse andmeteenusesse Common Data Service. Järgmises tabelis on vastendused.

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
PRODUCTCOLORID | \>\> | msdyn\_productcolorid.msdyn\_productcolorname
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid.msdyn\_itemnumber
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_retaildisplayorder

### <a name="shared-product-size"></a>Ühiskasutatava toote suurus

**Ühiskasutatava toote suuruse** olem näitab suurust, mida konkreetne tooteetalon võib sisaldada. Andmete järjepidevuse tagamiseks on see kontseptsioon üle viidud ühisesse andmeteenusesse Common Data Service. Järgmises tabelis on vastendused.

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid.msdyn\_itemnumber
PRODUCTSIZEID | \>\> | msdyn\_productsizeid.msdyn\_productsize
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

### <a name="shared-product-style"></a>Ühiskasutuses toote stiil

**Ühiskasutatava toote stiili** olem näitab stiili, mida konkreetne tooteetalon võib sisaldada. Andmete järjepidevuse tagamiseks on see kontseptsioon üle viidud ühisesse andmeteenusesse Common Data Service. Järgmises tabelis on vastendused.

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailsid.msdyn\_itemnumber
PRODUCTSTYLEID | \>\> | msdyn\_productstyleintegration
PRODUCTSTYLEID | \>\> | msdyn\_productstyleid.msdyn\_productstyle
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

### <a name="shared-product-configuration"></a>Ühiskasutatava toote konfiguratsioon

**Ühiskasutatava toote konfiguratsiooni** olem näitab konfiguratsioone, mida konkreetne tooteetalon võib sisaldada. Andmete järjepidevuse tagamiseks on see kontseptsioon üle viidud ühisesse andmeteenusesse Common Data Service. Järgmises tabelis on vastendused.

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
CONTAINERUNITSYMBOL | \>\> | msdyn\_containerunitsymbol
PRODUCTCONFIGURATIONID | \>\> | msdyn\_productconfigurationid.msdyn\_productconfiguration
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid.msdyn\_itemnumber
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

## <a name="product-number-identifier-bar-codes"></a>Tootenumbri identifikaatori vöötkoodid

Toote vöötkoode kasutatakse toodete unikaalseks identifitseerimiseks. Järgnevaid vastendusi kasutatakse nende toote vöötkoodide kättesaadavaks tegemiseks rakenduses Common Data Service.

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
PRODUCTNUMBER | \> | msdyn\_productnumberid.productnumber
BARCODE | \> | msdyn\_nimi
BARCODE | \> | msdyn\_barcode
PRODUCTQUANTITY | \> | msdyn\_productquantity
PRODUCTDESCRIPTION | \> | msdyn\_productdescription
BARCODESETUPID | \> | msdyn\_barcodesetupid
PRODUCTQUANTITYUNITSYMBOL | \> | msdyn\_unitofmeasureid.name
ISDEFAULTSCANNEDBARCODE | \>\> | msdyn\_isdefaultscannedbarcode
ISDEFAULTPRINTEDBARCODE | \>\> | msdyn\_isdefaultprintedbarcode
ISDEFAULTDISPLAYEDBARCODE | \>\> | msdyn\_isdefaultdisplayedbarcode

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Tellimuse vaikesätted ja tootespetsiifilise vaiketellimuse sätted

Tellimuse vaikesätted määratlevad tegevuskoha ja lao, kust kaupu hangitakse või hoitakse, miinimum-, maksimum-, mitmik- ja standardkogused, mida kasutatakse kaubanduse või varude halduse jaoks, täitmisajad, peatamislipu ja tellimuse lubamise meetodi. See teave on saadaval CDSis, kasutades tellimuse vaikesätteid ja tootespetsiifilisi tellimuse vaikesätete olemit. Saate lugeda Lisateavet funktsioonide kohta lehel [Tellimuse vaikesätted](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/production-control/default-order-settings).

### <a name="default-order-settings"></a>Tellimuse vaikesätted

Järgnevaid vastendusi kasutatakse tellimuse vaikesätete kättesaadavaks tegemiseks rakenduses Common Data Service.

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
INVENTWAREHOUSEID | = | msdyn_inventorywarehouse.msdyn_warehouseidentifier
INVENTORYSITEID | = | msdyn_inventorysite.msdyn_siteid
INVENTORYATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_inventoryatpdelayeddemandoffsetdays
INVENTORYATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_inventoryatpdelayedsupplyoffsetdays
ITEMNUMBER | = | msdyn_itemnumber.msdyn_itemnumber
INVENTORYATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_inventoryatpbackwarddemandtimefencedays
INVENTORYATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_inventoryatpbackwardsupplytimefencedays
INVENTORYATPTIMEFENCEDAYS | = | msdyn_inventoryatptimefencedays
MAXIMUMINVENTORYORDERQUANTITY | = | msdyn_maximuminventoryorderquantity
MAXIMUMPROCUREMENTORDERQUANTITY | = | msdyn_maximumprocurementorderquantity
MAXIMUMSALESORDERQUANTITY | = | msdyn_maximumsalesorderquantity
MINIMUMINVENTORYORDERQUANTITY | = | msdyn_minimuminventoryorderquantity
MINIMUMPROCUREMENTORDERQUANTITY | = | msdyn_minimumprocurementorderquantity
MINIMUMSALESORDERQUANTITY | = | msdyn_minimumsalesorderquantity
STANDARDINVENTORYORDERQUANTITY | = | msdyn_standardinventoryorderquantity
STANDARDPROCUREMENTORDERQUANTITY | = | msdyn_standardprocurementorderquantity
STANDARDSALESORDERQUANTITY | = | msdyn_standardsalesorderquantity
INVENTORYLEADTIMEDAYS | = | msdyn_inventoryleadtimedays
INVENTORYQUANTITYMULTIPLES | = | msdyn_inventoryquantitymultiples
PROCUREMENTQUANTITYMULTIPLES | = | msdyn_procurementquantitymultiples
SALESQUANTITYMULTIPLES | = | msdyn_salesquantitymultiples
PROCUREMENTSITEID | = | msdyn_procurementsite.msdyn_siteid
PROCUREMENTLEADTIMEDAYS | = | msdyn_procurementleadtimedays
SALESSITEID | = | msdyn_salessite.msdyn_siteid
SALESATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_salesatpdelayeddemandoffsetdays
SALESATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_salesatpdelayedsupplyoffsetdays
SALESATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_salesatpbackwarddemandtimefencedays
SALESATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_salesatpbackwardsupplytimefencedays
SALESATPTIMEFENCEDAYS | = | msdyn_salesatptimefencedays
SALESLEADTIMEDAYS | = | msdyn_salesleadtimedays
PROCUREMENTWAREHOUSEID | = | msdyn_procurementwarehouse.msdyn_warehouseidentifier
SALESWAREHOUSEID | = | msdyn_saleswarehouse.msdyn_warehouseidentifier
AREINVENTORYORDERPROMISINGDEFAULTSOVERRIDDEN | >< | msdyn_areinventoryorderdefaultsoverridden
INVENTORYORDERPROMISINGMETHOD | >< | msdyn_inventoryorderpromisingmethod
ISINVENTORYATPINCLUDINGPLANNEDORDERS | >< | msdyn_isinventoryatpincludingplannedorders
ISINVENTORYUSINGWORKINGDAYS | >< | msdyn_isinventoryusingworkingdays
ISINVENTORYSITEMANDATORY | >< | msdyn_isinventorysitemandatory
ISINVENTORYPROCESSINGSTOPPED | >< | msdyn_isinventoryprocessingstopped
ISPROCUREMENTUSINGWORKINGDAYS | >< | msdyn_isprocurementusingworkingdays
ISPROCUREMENTSITEMANDATORY | >< | msdyn_isprocurementsitemandatory
ISPROCUREMENTPROCESSINGSTOPPED | >< | msdyn_isprocurementprocessingstopped
ARESALESORDERPROMISINGDEFAULTSOVERRIDDEN | >< | msdyn_aresalesorderdefaultsoverridden
SALESORDERPROMISINGMETHOD | >< | msdyn_salesorderpromisingmethod
ISSALESATPINCLUDINGPLANNEDORDERS | >< | msdyn_issalesatpincludingplannedorders
ISSALESSITEMANDATORY | >< | msdyn_issalessitemandatory
ISSALESLEADTIMEOVERRIDDEN | >< | msdyn_issalesleadtimeoverridden
ISSALESPROCESSINGSTOPPED | >< | msdyn_issalesprocessingstopped
ISINVENTORYWAREHOUSEMANDATORY | >< | msdyn_isinventorywarehousemandatory
ISPROCUREMENTWAREHOUSEMANDATORY | >< | msdyn_isprocurementwarehousemandatory
ISSALESWAREHOUSEMANDATORY | >< | msdyn_issaleswarehousemandatory

### <a name="product-specific-default-order-settings"></a>Tootepõhised vaiketellimissätted

Järgnevaid vastendusi kasutatakse tootespetsiifilise tellimuse vaikesätete kättesaadavaks tegemiseks rakenduses Common Data Service.

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
INVENTORYWAREHOUSEID | = | msdyn_inventorywarehouse.msdyn_warehouseidentifier
INVENTORYSITEID | = | msdyn_inventorysite.msdyn_siteid
INVENTORYATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_inventoryatpdelayeddemandoffsetdays
INVENTORYATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_inventoryatpdelayedsupplyoffsetdays
ITEMNUMBER | = | msdyn_itemnumber.msdyn_itemnumber
INVENTORYATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_inventoryatpbackwarddemandtimefencedays
INVENTORYATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_inventoryatpbackwardsupplytimefencedays
INVENTORYATPTIMEFENCEDAYS | = | msdyn_inventoryatptimefencedays
MAXIMUMINVENTORYORDERQUANTITY | = | msdyn_maximuminventoryorderquantity
MAXIMUMPROCUREMENTORDERQUANTITY | = | msdyn_maximumprocurementorderquantity
MAXIMUMSALESORDERQUANTITY | = | msdyn_maximumsalesorderquantity
MINIMUMINVENTORYORDERQUANTITY | = | msdyn_minimuminventoryorderquantity
MINIMUMPROCUREMENTORDERQUANTITY | = | msdyn_minimumprocurementorderquantity
MINIMUMSALESORDERQUANTITY | = | msdyn_minimumsalesorderquantity
STANDARDINVENTORYORDERQUANTITY | = | msdyn_standardinventoryorderquantity
STANDARDPROCUREMENTORDERQUANTITY | = | msdyn_standardprocurementorderquantity
STANDARDSALESORDERQUANTITY | = | msdyn_standardsalesorderquantity
INVENTORYLEADTIMEDAYS | = | msdyn_inventoryleadtimedays
INVENTORYQUANTITYMULTIPLES | = | msdyn_inventoryquantitymultiples
PROCUREMENTQUANTITYMULTIPLES | = | msdyn_procurementquantitymultiples
SALESQUANTITYMULTIPLES | = | msdyn_salesquantitymultiples
PROCUREMENTSITEID | = | msdyn_procurementsite.msdyn_siteid
PROCUREMENTLEADTIMEDAYS | = | msdyn_procurementleadtimedays
SALESSITEID | = | msdyn_salessite.msdyn_siteid
SALESATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_salesatpdelayeddemandoffsetdays
SALESATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_salesatpdelayedsupplyoffsetdays
SALESATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_salesatpbackwarddemandtimefencedays
SALESATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_salesatpbackwardsupplytimefencedays
SALESATPTIMEFENCEDAYS | = | msdyn_salesatptimefencedays
SALESLEADTIMEDAYS | = | msdyn_salesleadtimedays
PROCUREMENTWAREHOUSEID | = | msdyn_procurementwarehouse.msdyn_warehouseidentifier
SALESWAREHOUSEID | = | msdyn_saleswarehouse.msdyn_warehouseidentifier
AREINVENTORYDEFAULTORDERSETTINGSOVERRIDDEN | >< | msdyn_areinventoryorderdefaultsoverridden
INVENTORYORDERPROMISINGMETHOD | >< | msdyn_inventoryorderpromisingmethod
ISINVENTORYATPINCLUDINGPLANNEDORDERS | >< | msdyn_isinventoryatpincludingplannedorders
ISINVENTORYUSINGWORKINGDAYS | >< | msdyn_isinventoryusingworkingdays
ISINVENTORYSITEMANDATORY | >< | msdyn_isinventorysitemandatory
ISINVENTORYPROCESSINGSTOPPED | >< | msdyn_isinventoryprocessingstopped
ISPROCUREMENTUSINGWORKINGDAYS | >< | msdyn_isprocurementusingworkingdays
ISPROCUREMENTSITEMANDATORY | >< | msdyn_isprocurementsitemandatory
ISPROCUREMENTPROCESSINGSTOPPED | >< | msdyn_isprocurementprocessingstopped
ARESALESDEFAULTORDERSETTINGSOVERRIDDEN | >< | msdyn_aresalesorderdefaultsoverridden
SALESORDERPROMISINGMETHOD | >< | msdyn_salesorderpromisingmethod
ISSALESATPINCLUDINGPLANNEDORDERS | >< | msdyn_issalesatpincludingplannedorders
ISSALESSITEMANDATORY | >< | msdyn_issalessitemandatory
ISSALESLEADTIMEOVERRIDDEN | >< | msdyn_issalesleadtimeoverridden
ISSALESPROCESSINGSTOPPED | >< | msdyn_issalesprocessingstopped
ISINVENTORYWAREHOUSEMANDATORY | >< | msdyn_isinventorywarehousemandatory
ISPROCUREMENTWAREHOUSEMANDATORY | >< | msdyn_isprocurementwarehousemandatory
ISSALESWAREHOUSEMANDATORY | >< | msdyn_issaleswarehousemandatory
OPERATIONALSITEID | = | msdyn_operationalsite.msdyn_siteid
PRODUCTCOLORID | = | msdyn_productcolor.msdyn_productcolorname
PRODUCTCONFIGURATIONID | = | msdyn_productconfiguration.msdyn_productconfiguration
PRODUCTSIZEID | = | msdyn_productsize.msdyn_productsize
PRODUCTSTYLEID | = | msdyn_productstyle.msdyn_productstyle

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Mõõtühik ja mõõtühiku teisendused

Mõõtühikud ja selle vastavad teisendused on saadaval teenuse Common Data Service järgmises diagrammis kuvatavas andmudelis.

![Toodete andmemudel](media/dual-write-product-3.PNG)

Mõõtühiku kontseptsioon on integreeritud Finance and Operations rakenduste ja muude Dynamics 365 rakenduste vahel. Iga ühiku klassi kohta Finance and Operations rakenduses luuakse ühiku grupp Dynamics 365 rakenduses, mis sisaldab ühiku klassi kuuluvaid üksusi. Iga ühikurühma jaoks luuakse ka vaikimisi baasühik. 

### <a name="unit-of-measure"></a>Mõõtühik

Järgmisi vastendusi kasutatakse Finance and Operations rakenduste mõõtühikute kättesaadavaks tegemiseks ühisandmeteenustes Common Data Service.

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
UNITSYMBOL | >> | msdyn_symbol
UNITCLASS | >> | msdyn_externalunitclassname
DECIMALPRECISION | >> | msdyn_decimalprecision
ISBASEUNIT | >> | msdyn_isbaseunit
ISSYSTEMUNIT | >> | msdyn_issystemunit
SYSTEMOFUNITS | >> | msdyn_systemofunits
UNITSYMBOL | >> | nimi
UNITDESCRIPTION | >> | msdyn_description

### <a name="unit-of-measure-conversions"></a>Mõõtühikute teisendused

Järgmisi vastendusi kasutatakse Finance and Operations rakenduste mõõtühikute teisenduste kättesaadavaks tegemiseks ühisandmeteenustes Common Data Service.

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
DENOMINATOR | = | msdyn_denominator
NUMERATOR | = | msdyn_numerator
FACTOR | = | msdyn_factor
INNEROFFSET | = | msdyn_inneroffset
OUTEROFFSET | = | msdyn_outeroffset
ROUNDING | >< | msdyn_rounding
TOUNITSYMBOL | = | msdyn_tounit.msdyn_symbol
FROMUNITSYMBOL | = | msdyn_fromunit.msdyn_symboll

### <a name="product-specific-unit-of-measure-conversions"></a>Tootepõhise mõõtühiku teisendamised

Järgmisi vastendusi kasutatakse Finance and Operations tootespetsiifiliste rakenduste mõõtühikute teisendamiste kättesaadavaks tegemiseks ühisandmeteenustes Common Data Service.

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
DENOMINATOR | = | msdyn_denominator
NUMERATOR | = | msdyn_numerator
FACTOR | = | msdyn_factor
FROMUNITSYMBOL | = | msdyn_fromunit.msdyn_symboll
TOUNITSYMBOL | = | msdyn_tounit.msdyn_symbol
PRODUCTNUMBER | = | msdyn_globalproduct.msdyn_productnumber
INNEROFFSET | = | msdyn_inneroffset
OUTEROFFSET | = | msdyn_outeroffset
ROUNDING | >< | msdyn_rounding

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Tootepoliitika: dimensioon, jälgimise ja laoala grupid

Tootepoliitikad on poliitikakogumid, mida kasutatakse toodete ja selle omaduste määratlemiseks laos. Tootedimensiooni gruppi, toote jälgimisdimensiooni gruppi ja laoala dimensiooni gruppi võib leida tootepoliitikana. 

### <a name="product-dimension-group"></a>Tootedimensioonigrupp

Tootedimensioon määratleb, millised tootedimensioonid määratlevad toote. Neli võimalikku toomedimensiooni gruppi on: suurus, värv, stiil ja konfiguratsioon. Tootedimensiooni grupid on saadaval rakenduses Common Data Service järgmiste vastenduste abil. 

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
WILLSALESPRICESEARCHUSEPRODUCTSTYLE | >< | msdyn_willsalespricesearchuseproductstyle
WILLPURCHASEPRICESEARCHUSEPRODUCTSIZE | >< | msdyn_willpurchasepricesearchuseproductsize
WILLSALESPRICESEARCHUSEPRODUCTCONFIGURATION | >< | msdyn_willsalespricesearchuseprodconfig
WILLSALESPRICESEARCHUSEPRODUCTCOLOR | >< | msdyn_willsalespricesearchuseproductcolor
WILLPURCHASEPRICESEARCHUSEPRODUCTSTYLE | >< | msdyn_willpurchasepricesearchuseproductstyle
WILLPURCHASEPRICESEARCHUSEPRODUCTCONFIGURATION | >< | msdyn_willpurchpricesearchuseprodconfig
WILLPURCHASEPRICESEARCHUSEPRODUCTCOLOR | >< | msdyn_willpurchpricesearchuseproductcolor
ISPRODUCTSTYLEACTIVE | >< | msdyn_isproductstyleactive
ISPRODUCTSIZEACTIVE | >< | msdyn_isproductsizeactive
ISPRODUCTCONFIGURATIONACTIVE | >< | msdyn_isproductconfigurationactive
ISPRODUCTCOLORACTIVE | >< | msdyn_isproductcoloractive
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
PRODUCTVARIANTNOMENCLATURENAME | = | msdyn_productvariantnomenclaturename
WILLSALESPRICESEARCHUSEPRODUCTSIZE | >< | msdyn_willsalespricesearchuseproductsize

### <a name="product-tracking-dimension-group"></a>Toote jälgimisdimensiooni grupp

Toote jälgimisdimensiooni grupp tähistab meetodit, mida kasutatakse toote jälgimiseks laos. Need on saadaval rakenduses Common Data Service järgmiste vastenduste abil. 

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
SERIALNUMBERCAPTURINGOPERATION | >< | msdyn_serialnumbercapturingoperation
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
ISSERIALNUMBERENABLEDFORPRODUCTIONCONSUMPTIONPROCESS | >< | msdyn_issnenabledforpcprocess
ISSERIALNUMBERCONTROLENABLED | >< | msdyn_isserialnumbercontrolenabled
ISSERIALNUMBERENABLEDFORSALESPROCESS | >< | msdyn_isserialnumberenabledforsalesprocess
ISSERIALNUMBERACTIVE | >< | msdyn_isserialnumberactive
ISSALESPRICEBYSERIALNUMBER | >< | msdyn_issalespricebyserialnumber
ISSALESPRICEBYBATCHNUMBER | >< | msdyn_issalespricebybatchnumber
ISPURCHASEPRICEBYSERIALNUMBER | >< | msdyn_ispurchasepricebyserialnumber
ISPURCHASEPRICEBYBATCHNUMBER | >< | msdyn_ispurchasepricebybatchnumber
ISPRIMARYSTOCKINGENABLEDFORSERIALNUMBER | >< | msdyn_isprimarystockingenabledforsn
ISPRIMARYSTOCKINGENABLEDFORBATCHNUMBER | >< | msdyn_isprimarystockingenabledforbn
ISPHYSICALINVENTORYENABLEDFORSERIALNUMBER | >< | msdyn_isphysicalinventoryenabledforsn
ISPHYSICALINVENTORYENABLEDFORBATCHNUMBER | >< | msdyn_isphysicalinventoryenabledforbn
ISFINANCIALINVENTORYENABLEDFORSERIALNUMBER | >< | msdyn_isfinancialinventoryenabledforsn
ISFINANCIALINVENTORYENABLEDFORBATCHNUMBER | >< | msdyn_isfinancialinventoryenabledforbn
ISCOVERAGEPLANENABLEDFORSERIALNUMBER | >< | msdyn_iscoverageplanenabledforserialnumber
ISCOVERAGEPLANENABLEDFORBATCHNUMBER | >< | msdyn_iscoverageplanenabledforbatchnumber
ISBLANKRECEIPTALLOWEDFORSERIALNUMBER | >< | msdyn_isblankreceiptallowedforserialnumber
ISBLANKRECEIPTALLOWEDFORBATCHNUMBER | >< | msdyn_isblankreceiptallowedforbatchnumber
ISBLANKISSUEALLOWEDFORSERIALNUMBER | >< | msdyn_isblankissueallowedforserialnumber
ISBLANKISSUEALLOWEDFORBATCHNUMBER | >< | msdyn_isblankissueallowedforbatchnumber
ISBATCHNUMBERACTIVE | >< | msdyn_isbatchnumberactive
ISINVENTORYOWNERACTIVE | >< | msdyn_isinventoryowneractive

### <a name="product-storage-dimension-group"></a>Toote laoala dimensiooni grupp

Toote laoala dimensiooni grupp tähistab meetodit, mida kasutatakse toote paigutuse määratlemiseks laos. Need on saadaval rakenduses Common Data Service järgmiste vastenduste abil. 

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
WILLSALESPRICESEARCHUSEWAREHOUSE | >< | msdyn_willsalespricesearchusewarehouse
WILLSALESPRICESEARCHUSESITE | >< | msdyn_willsalespricesearchusesite
WILLSALESPRICESEARCHUSEINVENTORYSTATUS | >< | msdyn_willsalespricesearchuseinventorystatus
WILLPURCHASEPRICESEARCHUSEWAREHOUSE | >< | msdyn_willpurchasepricesearchusewarehouse
WILLPURCHASEPRICESEARCHUSESITE | >< | msdyn_willpurchasepricesearchusesite
WILLPURCHASEPRICESEARCHUSEINVENTORYSTATUS | >< | msdyn_willpurchpricesearchuseinventstatus
WILLCOVERAGEPLANNINGUSEWAREHOUSE | >< | msdyn_willcoverageplanusewarehouse
WILLCOVERAGEPLANNINGUSELOCATION | >< | msdyn_iscoverageplanenabledforlocation
WILLCOVERAGEPLANNINGUSEINVENTORYSTATUS | >< | msdyn_willcoverageplanuseinventorystatus
AREADVANCEDWAREHOUSEMANAGEMENTPROCESSESENABLED | >< | msdyn_areadvancedwmprocessesenabled
ISWAREHOUSEPRIMARYSTORAGEDIMENSION | >< | msdyn_iswarehouseprimarystoragedimension
ISWAREHOUSEMANDATORY | >< | msdyn_iswarehousemandatory
ISPHYSICALINVENTORYENABLEDFORWAREHOUSE | >< | msdyn_isphysicalinventoryenabledforwarehouse
ISPHYSICALINVENTORYENABLEDFORLOCATION | >< | msdyn_isphysicalinventoryenabledforlocation
ISLOCATIONACTIVE | >< | msdyn_islocationactive
ISFINANCIALINVENTORYENABLEDFORWAREHOUSE | >< | msdyn_isfinancialinventoryenabledforwarehouse
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
ISBLANKRECEIPTALLOWEDFORLOCATION | >< | msdyn_isblankreceiptallowedforlocation
ISBLANKISSUEALLOWEDFORLOCATION | >< | msdyn_isblankissueallowedforlocation

