---
title: Hankija koondandmete haldamine
description: Selles teemas kirjeldatakse hankija andmete integreerimist rakenduse Finance and Operationsi ja teenuse Common Data Service vahel.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.openlocfilehash: 45808bc35aba04df6fcaf6b1cbfcc2461b0b65cb
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789175"
---
## <a name="integrated-vendor-master"></a>Hankija koondandmete haldamine

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Termin *hankija* viitab tarnijariigi organisatsioonile või ainuomanikule, kes on tarneahela protsessi osa ja tarnib ettevõttele kaupu. Kuigi *hankija* on loodud mõiste rakenduses Microsoft Dynamics 365 for Finance and Operations, pole rakenduses Dynamics 365 for Customer Engagement hankija mõistet olemas. Selle asemel on mõned ettevõtted olemi Konto üle koormanud nii kliendi- kui ka hankijateabega. Teised ettevõtted kasutavad kohandatud hankija mõistet. Common Data Service'i integratsioon toetab mõlemat lahendust. Seetõttu saate olenevalt oma äristsenaariumist lubada ühe neist lahendustest.

Hankija andmete integreerimine rakenduste Finance and Operationsi ja Customer Engagement vahel võimaldab teil mitmeid koondandmeid hankida. Olenemata sellest, kust hankijaandmed pärinevad, on need integreeritud kulisside taga üle rakenduste piiride ja taristute erinevuste. 

### <a name="vendor-data-flow"></a>Hankijaandmete voog

Kui soovite kasutada hankija koondandmete jaoks rakendust Customer Engagement ja soovite isoleerida hankijateabe klienditeabest, saate kasutada uut hankijalahendust.

![Hankijaandmete voog](media/dual-write-vendor-data-flow.png)

Kui soovite kasutada hankija koondandmete jaoks rakendust Customer Engagement ja soovite hankijaandmete salvestamiseks jätkata olemi Konto kasutamist, saate kasutada uut, laiendatud hankijalahendust. Selles lahenduses on hankija üksikasjadesse talletatud laiendatud hankijateave (nt hankijagrupp ja hankija sisestuse profiil).

![Hankijaandmete laiendatud voog](media/dual-write-vendor-detail.jpg)

Hankija kontaktteave meenutab kliendi kontaktteavet. Kulisside taga talletatakse kontaktisiku teave ja tuuakse need samadest olemitest.

## <a name="templates"></a>Mallid

Hankijaandmed sisaldavad kogu teavet hankija kohta (nt hankijagrupp, aadressid, kontaktandmed, makseprofiil, arveprofiil). Olemikaartide kogum toimib koos hankijaandmete suhtluse ajal, nagu on näidatud järgmises tabelis.

Finance and Operations  | Rakendus Customer Engagement
------------------------|---------------------------------
Hankija V2               | Konto
Hankija V2               | Msdyn\_vendors
CDS-i kontaktid V2         | Kontakt
Hankijagrupid           | Msdyn\_vendorgroups
Hankija makseviis   | Msdyn\_vendorpaymentmethods
Maksegraafik        | Msdyn\_paymentschedules
Maksegraafik        | Msdyn\_paymentschedulelines
CDS-i maksepäev         | Msdyn\_paymentdays
CDS-i maksepäeva read   | Msdyn\_paymentdaylines
Maksetingimused        | Msdyn\_paymentterms
Nimeliited            | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="vendor-v2-and-account"></a>Hankija V2 ja konto 

Ettevõtted, mis kasutavad hankija teabe talletamiseks olemit Konto, saavad jätkata selle kasutamist samal viisil. Nad saavad kasutada ka konkreetseid hankijafunktsioone rakendusest Finance and Operations integratsiooni tõttu.

## <a name="vendor-v2-and-msdyn_vendors"></a>Hankija V2 and Msdyn\_vendors

Ettevõtted, mis kasutavad hankijatele, saavad ära kasutada valmislahendusena hankija eeliseid, mis on Finance and Operations integratsiooni kaudu juurutatud teenuses Common Data Service. 

<!-- ![vendor mappings](media/dual-write-vendors-1.png) -->

<!-- ![vendor mappings](media/dual-write-vendors-2.png) -->

<!-- ![vendor mappings](media/dual-write-vendors-3.png) -->

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
VENDORACCOUNTNUMBER | = | msdyn\_vendoraccountnumber
VENDORGROUPID | = | msdyn\_vendorgroupid.msdyn\_vendorgroup
VENDORORGANIZATIONNAME | = | msdyn\_name
VENDORPARTYTYPE | \>\< | msdyn\_isperson
PERSONFIRSTNAME | = | msdyn\_firstname
PERSONLASTNAME | = | msdyn\_lastname
CREDITLIMIT | = | msdyn\_vendorcreditlimit
ISFOREIGNENTITY | \>\< | msdyn\_isforeignentity
ISONETIMEVENDOR | \>\< | msdyn\_isonetimevendor
ADDRESSBUILDINGCOMPLIMENT | = | msdyn\_addressbuildingcompliment
PERSONCHILDRENNAMES | = | msdyn\_childrennames
ADDRESSCITY | = | msdyn\_addresscity
ADDRESSCOUNTRYREGIONID | = | msdyn\_addresscountryregionid
ADDRESSCOUNTRYREGIONISOCODE | = | msdyn\_addresscountryregionisocode
ADDRESSCOUNTYID | = | msdyn\_addresscountyid
CREDITRATING | = | msdyn\_creditrating
ADDRESSDESCRIPTION | = | msdyn\_addressdescription
ADDRESSDISTRICTNAME | = | msdyn\_addressdistrictname
DUNSNUMBER | = | msdyn\_dunsnumber
ETHNICORIGINID | = | msdyn\_ethnicorigin
FORMATTEDPRIMARYADDRESS | = | msdyn\_formattedprimaryaddress
PERSONHOBBIES | = | msdyn\_hobbies
PERSONINITIALS | = | msdyn\_initials
LANGUAGEID | = | msdyn\_languageid
PERSONLASTNAMEPREFIX | = | msdyn\_lastnameprefix
PERSONMIDDLENAME | = | msdyn\_middlename
ORGANIZATIONNUMBER | = | msdyn\_organizationnumber
OURACCOUNTNUMBER | = | msdyn\_ourvendoraccountnumber
PAYMENTID | = | msdyn\_paymentid
PERSONPHONETICFIRSTNAME | = | msdyn\_phoneticfirstname
PERSONPHONETICMIDDLENAME | = | msdyn\_phoneticmiddlename
PERSONPHONETICLASTNAME | = | msdyn\_phoneticlastname
ORGANIZATIONPHONETICNAME | = | msdyn\_organizationphoneticname
ADDRESSPOSTBOX | = | msdyn\_addresspostbox
PRIMARYURL | = | msdyn\_primarycontacturl
PRIMARYEMAILADDRESS | = | msdyn\_primaryemailaddress
PRIMARYEMAILADDRESSDESCRIPTION | = | msdyn\_primaryemailaddressdescription
PRIMARYFACEBOOK | = | msdyn\_primaryfacebook
PRIMARYFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYFAXNUMBER | = | msdyn\_primaryfaxnumber
PRIMARYFAXNUMBERDESCRIPTION | = | msdyn\_primaryfaxnumberdescription
PRIMARYFAXNUMBEREXTENSION | = | msdyn\_primaryfaxnumberextension
PRIMARYLINKEDIN | = | msdyn\_primarylinkedin
PRIMARYLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescription
PRIMARYPHONENUMBER | = | msdyn\_pimaryphonenumber
PRIMARYPHONENUMBERDESCRIPTION | = | msdyn\_primaryphonenumberdescription
PRIMARYPHONENUMBEREXTENSION | = | msdyn\_primaryphonenumberextension
PRIMARYTELEX | = | msdyn\_primarytelex
PRIMARYTELEXDESCRIPTION | = | msdyn\_primarytelexdescription
PRIMARYTWITTER | = | msdyn\_primarytwitter
PRIMARYTWITTERDESCRIPTION | = | msdyn\_primarytwitterdescription
PRIMARYURLDESCRIPTION | = | msdyn\_primaryurldescription
PERSONPROFESSIONALSUFFIX | = | msdyn\_professionalsuffix
PERSONPROFESSIONALTITLE | = | msdyn\_professionatitle
ADDRESSSTATEID | = | msdyn\_addressstateid
ADDRESSSTREET | = | msdyn\_addressstreet
AADRESSSTREETINUMBER | = | msdyn\_addressstreetnumber
VENDORKNOWNASNAME | = | msdyn\_vendorknownasname
ADDRESSZIPCODE | = | msdyn\_addresszipcode
DEFAULTPAYMENTDAYNAME | = | msdyn\_defaultpaymentdayname.msdyn\_name
DEFAULTPAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
DEFAULTPAYMENTTERMSNAME | = | msdyn\_paymentterms.msdyn\_name
HASONLYTAKENBIDS | \>\< | msdyn\_hasonlytakenbids
ISMINORITYOWNED | \>\< | msdyn\_isminorityowned
ISVENDORLOCALLYOWNED | \>\< | msdyn\_isvendorlocallyowned
ISSERVICEVETERANOWNED | \>\< | msdyn\_isserviceveteranowned
ISOWNERDISABLED | \>\< | msdyn\_ownerisdisabled
ISWOMANOWNER | \>\< | msdyn\_womanowner
PERSONANNIVERSARYDAY | = | msdyn\_personanniversaryday
PERSONANNIVERSARYYEAR | = | msdyn\_anniversaryyear
PERSONBIRTHDAY | = | msdyn\_birthday
PERSONBIRTHYEAR | = | msdyn\_birthyear
ORGANIZATIONEMPLOYEEAMOUNT | = | msdyn\_numberofemployees
VENDORHOLDRELEASEDATE | = | msdyn\_vendoronholdreleasedate
VENDORPARTYNUMBER | = | msdyn\_vendorpartynumber
ADDRESSLOCATIONID | = | msdyn\_addresslocationid
PERSONANNIVERSARYMONTH | = | msdyn\_vendorpersonanniversarymonth
PERSONBIRTHMONTH | = | msdyn\_vendorpersonbirthmonth
PERSONMARITALSTATUS | \>\< | msdyn\_maritalstatus
ADDRESSLATITUDE | \>\> | msdyn\_addresslatitude
ADDRESSLONGITUDE | \>\> | msdyn\_addresslongitude
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
CURRENCYCODE | = | msdyn\_currencycode.isocurrencycode
ISVENDORLOCATEDINHUBZONE | \>\< | msdyn\_isvendorlocatedinhubzone
DEFAULTVENDORPAYMENTMETHODNAME | = | msdyn\_vendorpaymentmethod.msdyn\_name
INVOICEVENDORACCOUNTNUMBER | = | msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber
PERSONGENDER | \>\< | msdyn\_gender
AREPRICESINCLUDINGSALESTAX | \>\< | msdyn\_priceincludessalestax
SALESTAXGROUPCODE | = | msdyn\_taxgroup.msdyn\_name
VENDORPRICETOLERANCEGROUPID | = | msdyn\_pricetolerancegroup.msdyn\_groupid

## <a name="contacts"></a>Kontaktid

See mall sünkroonib nii klientide kui ka hankijate maksetingimuste esmased, sekundaarsed ja tertsiaarsed kontaktandmed rakenduste Finance and Operations ja Customer Engagement vahel. Olemi kaardi üksikasjade kohta lugege teemat [Kliendi integreeritud koondandmed](dual-write-customer.md#contacts).

## <a name="vendor-groups"></a>Hankijagrupid

See mall sünkroonib hankijagrupi teabe rakenduste Finance and Operations ja Customer Engagement vahel.

<!-- ![vendor groups mappings](media/dual-write-vendor-groups.png) -->

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
DEFAULTPAYMENTTERMNAME | = | msdyn\_paymentterms.msdyn\_name
KIRJELDUS | = | msdyn\_description
VENDORGROUPID | = | msdyn\_vendorgroup
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymentpermname.msdyn\_name

### <a name="vendor-payment-method"></a>Hankija makseviis

See mall sünkroonib hankija makseviisi teabe rakenduste Finance and Operations ja Customer Engagement vahel.

<!-- ![vendor payment method mappings](media/dual-write-vendor-payment-method.png) -->

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
NIMI | = | msdyn\_name
KIRJELDUS | = | msdyn\_description
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
ALLOWPAYMENTCOPIES | \>\< | msdyn\_allowpaymentcopies
PAYMENTTYPE | \>\< | msdyn\_paymenttype
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
ACCOUNTTYPE | \>\< | msdyn\_accounttype
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingposting
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_postdatedcheckclearingposting
PROMISSORYNOTEDRAFTTYPE | \>\< | msdyn\_promissorynotedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

