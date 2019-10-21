---
title: Integreeritud klientide koond
description: Selles teemas kirjeldatakse kliendiandmete integreerimist Finance and Operationsi ja Common Data Service'i vahel.
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
ms.openlocfilehash: 6c8c94eb8ff04d489eb24b7e0f4642aef20a3b18
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182044"
---
## <a name="integrated-customer-master"></a>Integreeritud klientide koond

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Kliendikirjete loomine mitmes rakenduses on tavaline. Näiteks võib müügitegevus tuua ärikliendi kirjeid rakenduse Sales kaudu ja e-kaubandus või jaemüük võivad tuua kliendikirjeid rakenduse Finance and Operations kaudu. Olenemata sellest, kust kliendikirje pärineb, on see integreeritud kulisside taga üle rakenduste piiride ja taristute erinevuste. Integreeritud klientide loomine aitab käsitleda mitut loodud stsenaariumi ja annab põhjaliku kliendivaate Dynamics 365 rakenduse komplektile.

## <a name="customer-data-flow"></a>Kliendiandmete voog

*Klient* on rakendustes täpselt määratletud mõiste. Seetõttu hõlmab kliendiandmete integreerimine lihtsalt kliendikontseptsiooni ühtlustamist kahe rakenduse vahel. Järgmine illustratsioon näitab kliendiandmete voogu.

![Kliendiandmete voog](media/dual-write-customer-data-flow.png)

Kliente saab laias laastus liigitada kahte tüüpi: äri-/organisatsioonikliendid ning tarbijad/lõppkasutajad. Neid kahte tüüpi kliente talletatakse ja käsitletakse rakendustes Finance and Operations ja Common Data Service erinevalt.

Rakenduses Finance and Operations luuakse nii äri-/organisatsioonikliendid kui ka tarbijad/lõppkasutajad ühed tabelis nimetusega **CustTable** (CustomerCustomerV3Entity) ja neid liigitatakse atribuudi **Tüüp** järgi. (Kui atribuudiks **Tüüp** on määratud **Organisatsioon**, on klient äri-/organisatsiooniklient ja kui atribuudiks **Tüüp** on määratud **Isik**, on klient tarbija/lõppkasutaja.) Esmase kontaktisiku teavet töödeldakse olemi SMMContactPersonEntity kaudu.

Rakenduses Common Data Service luuakse äri-/organisatsioonikliendid olemis Konto ja tuvastatakse klientidena, kui atribuudiks **Seose tüüp** on määratud **Klient**. Nii tarbijaid/lõppkasutajaid kui ka kontaktisikut esindab olem Kontakt. Et tagada tarbija/lõppkasutaja ja kontaktisiku selge eristamine, on olemil**Kontakt** loogikalipp nimega **Müüdav**. Kui **Müüdav** on **Tõene**, on kontakt tarbija/lõppkasutaja ja selle kontakt jaoks saab luua pakkumisi ja tellimusi. Kui **Müüdav** on **Väär**, on kontakt vaid kliendi esmane kontaktisik.

Kui mittemüüdav kontakt osaleb pakkumise või tellimuse toimingus, on atribuudiks **Müüdav** määratud **Tõene**, et märkida kontakt lipuga müüdava kontaktina. Kontakt, kes on saanud müüdavaks kontaktiks, jääb müüdavaks kontaktiks.

## <a name="templates"></a>Mallid

Kliendiandmed sisaldavad kogu teavet kliendi kohta (nt. kliendigrupp, aadressid, kontaktandmed, makseprofiil, arveprofiil ja püsikliendi olek). Olemikaartide kogum toimib koos kliendiandmete suhtluse ajal, nagu on näidatud järgmises tabelis.

Finance and Operationsi rakendused    | Muud Dynamics 365 rakendused
--------------------------|---------------------------------
Klient V3               | Konto
Klient V3               | Kontakt
CDS-i kontaktid V2           | Kontakt
Kliendigrupid           | Msdyn\_customergroups
Kliendi makseviis   | Msdyn\_customerpaymentmethods
Kliendikaart              | Msdyn\_loyaltycards
Maksegraafik          | Msdyn\_paymentschedules
Maksegraafik          | Msdyn\_paymentschedulelines
CDS-i maksepäev           | Msdyn\_paymentdays
CDS-i maksepäeva read     | Msdyn\_paymentdaylines
Maksetingimused          | Msdyn\_paymentterms
Nimeliited              | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="customer-v3-to-account"></a>Klient V3 kontole

See mall sünkroonib äri-ja organisatsiooniklientide kliendi koondteabe rakenduste Finance and Operationsi rakenduste ja Common Data Service vahel.

<!-- ![](media/dual-write-account-1.png) -->

<!-- ![](media/dual-write-account-2.png) -->

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
CUSTOMERACCOUNT | = | accountnumber
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
CREDITLIMIT | = | creditlimit
DELIVERYADDRESSCITY | = | address1\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
DELIVERYADDRESSCOUNTY | = | address1\_county
DELIVERYADDRESSLATITUDE | \> | address1\_latitude
DELIVERYADDRESSLONGITUDE | \> | address1\_longitude
DELIVERYADDRESSZIPCODE | = | address1\_postalcode
ORGANIZATIONNAME | = | nimi
ORGANIZATIONNUMBEROFEMPLOYEES | = | numberofemployees
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTFAX | = | faks
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTTWITTER | = | primarytwitterid
PRIMARYCONTACTURL | = | websiteurl
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | kirjeldus
CREDITLIMITISMANDATORY | \>\< | msdyn\_creditlimitismandatory
CREDITRATING | = | msdyn\_creditrating
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
INVOICEACCOUNT | = | msdyn\_billingaccount.accountnumber
INVOICEADDRESS | \>\< | msdyn\_invoiceaddress
ISONETIMECUSTOMER | \>\< | msdyn\_onetimecustomer
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PAYMENTDAY | = | msdyn\_paymentday.msdyn\_name
PAYMENTMETHOD | = | msdyn\_customerpaymentmethod.msdyn\_name
PAYMENTSCHEDULE | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTTERMS | = | msdyn\_paymentterm.msdyn\_name
PAYMENTTERMSBASEDAYS | = | msdyn\_paymenttermsbasedays
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
PRIMARYCONTACTLINKEDIN | = | msdyn\_primarylinkedinid
TAXEXEMPTNUMBER | = | msdyn\_taxexemptnumber
VENDORACCOUNT | = | msdyn\_vendor.msdyn\_vendoraccountnumber
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
LANGUAGEID | \<\< | Pole
DELIVERYADDRESSSTREET | = | address1\_line1
DELIVERYADDRESSSTATE | = | address1\_stateorprovince
Pole | \>\> | address1\_addresstypecode
Pole | \>\> | customertypecode
PARTYTYPE | \<\< | Pole
PARTYNUMBER | = | msdyn\_partynumber

## <a name="customer-v3-to-contact"></a>Klient V3 kontaktile

See mall sünkroonib klientide ja lõppkasutajate klientde koondandmed rakenduste Finance and Operations ja teiste Dynamics 365 rakenduste vahel.

<!-- ![](media/dual-write-contact-1.png) -->
<!-- ![](media/dual-write-contact-2.png) -->

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
Pole | \>\> | msdyn\_sellable
PARTYTYPE | \<\< | Pole
PARTYNUMBER | = | msdyn\_partynumber
CUSTOMERACCOUNT | = | msdyn\_contactpersonid
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
PERSONFIRSTNAME | = | firstname
PERSONLASTNAME | = | lastname
PERSONMIDDLENAME | = | middlename
PERSONPROFESSIONALTITLE | = | jobtitle
PERSONGENDER | \>\< | gendercode
PERSONMARITALSTATUS | \>\< | familystatuscode
LANGUAGEID | \<\< | Pole
ADDRESSCITY | = | address1\_city
ADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
ADDRESSCOUNTY | = | address1\_county
ADDRESSLATITUDE | \> | address1\_latitude
ADDRESSLONGITUDE | \> | address1\_longitude
ADDRESSLOCATIONROLES | \<\< | Pole
ADDRESSSTATE | = | address1\_stateorprovince
ADDRESSSTREET | = | address1\_line1
ADDRESSZIPCODE | = | address1\_postalcode
AADRESSPOSTBOX | = | address1\_postofficebox
Pole | \>\> | address1\_addresstypecode
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
Pole | \>\> | address2\_addresstypecode
DELIVERYADDRESSCITY | = | address3\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address3\_country
DELIVERYADDRESSCOUNTY | = | address3\_county
DELIVERYADDRESSLATITUDE | \> | address3\_latitude
DELIVERYADDRESSLONGITUDE | \>\> | address3\_longitude
DELIVERYADDRESSSTATE | = | address3\_stateorprovince
DELIVERYADDRESSSTREET | = | address3\_line1
DELIVERYADDRESSZIPCODE | = | address3\_postalcode
Pole | \>\> | address3\_addresstypecode
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFAX | = | faks
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTLINKEDIN | = | msdyn\_primaryinkedinid
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTER | = | msdyn\_primarytwitterid
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURL | = | websiteurl
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | kirjeldus

## <a name="contacts"></a>Kontaktid

See mall sünkroonib nii klientide kui ka hankijate maksetingimuste esmased, sekundaarsed ja tertsiaarsed kontaktandmed rakenduste Finance and Operations ja teiste Dynamics 365 rakenduste vahel.

<!-- ![](media/dual-write-contacts.png) -->

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn\_partynumber
ASSOCIATEDCONTACTTYPE | \<\< | Pole
FIRSTNAME | = | firstname
MIDDLENAME | = | middlename
LASTNAME | = | lastname
ASSOCIATEDCONTACTNUMBER | = | msdyn\_vendorcontactid.msdyn\_vendoraccountnumber
PRIMARYADDRESSCITY | = | address1\_city
PRIMARYADDRESSCOUNTRYREGIONID | = | address1\_country
PRIMARYADDRESSCOUNTYID | = | address1\_county
PRIMARYFAXNUMBER | = | faks
PRIMARYADDRESSSTATEID | = | address1\_stateorprovince
PRIMARYADDRESSSTREET | = | address1\_line1
PRIMARYADDRESSZIPCODE | = | address1\_postalcode
PRIMARYPHONENUMBER | = | telephone1
PRIMARYEMAILADDRESS | = | emailaddress1
EMPLOYMENTDEPARTMENT | = | osakond
MÄRKMED | = | kirjeldus
SUGU | \>\< | gendercode
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid
PRIMARYURL | = | websiteurl
MARITALSTATUS | \>\< | familystatuscode
ISRECEIVINGDIRECTMAIL | \>\< | donotemail
EMPLOYMENTPROFESSION | = | jobtitle
SPOUSENAME | = | spousesname
Pole | \>\> | msdyn\_contactforvendor
Pole | \>\> | msdyn\_contactpersonid

## <a name="customer-groups"></a>Kliendigrupid

See mall sünkroonib kliendigrupi teabe rakenduste Finance and Operations ja teiste Dynamics 365 rakenduste vahel.

<!-- ![](media/dual-write-customer-groups.png) -->

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
CUSTOMERGROUPID | = | msdyn\_groupid
KIRJELDUS | = | msdyn\_description
ISSALESTAXINCLUDEDINPRICE | \>\< | msdyn\_issalestaxincludedinprice
PAYMENTTERMID | = | msdyn\_paymenttermid.msdyn\_name
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymenttermname.msdyn\_name

## <a name="customer-payment-methods"></a>Kliendi makseviisid

See mall sünkroonib kliendi makseviisi teabe rakenduste Finance and Operations ja teiste Dynamics 365 rakenduste vahel.

<!-- ![](media/dual-write-customer-payment-methods.png) -->

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
NIMI | = | msdyn\_nimi
ACCOUNTTYPE | \>\< | msdyn\_accounttype
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingpostingenabled
ISSEPA | \>\< | msdyn\_issepa
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
KIRJELDUS | = | msdyn\_description
PAYMENTTYPE | \>\< | msdyn\_paymenttype
CREATEANDDRAWBILLOFEXCHANGEDURINGINVOICEPOSTING | \>\< | msdyn\_invoiceupdate
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_enablepostdatescheckclearingposting
BILLOFEXCHANGEDRAFTTYPE | \>\< | msdyn\_billofexchangedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

## <a name="loyalty-cards"></a>Kliendikaardid

See mall sünkroonib kliendikaardi teabe rakenduste Finance and Operations ja teiste Dynamics 365 rakenduste vahel.

<!-- ![](media/dual-write-loyalty-cards.png) -->

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
CARDNUMBER | = | msdyn\_cardnumber
CARDTENDERTYPE | \>\< | msdyn\_cardtendertype
PARTYNUMBER | = | msdyn\_partynumber
REPLACEMENTCARDNUMBER | \> | msdyn\_replacementcardnumber
OMOPERATINGUNITNUMBER | = | msdyn\_operatingunitnumber
LOYALTYENROLLMENTDATE | = | msdyn\_enrollmentdate

## <a name="payment-schedules"></a>Maksegraafikud

See mall sünkroonib nii klientide kui ka hankijate maksegraafiku viiteandmed rakenduste Finance and Operations ja teiste Dynamics 365 rakenduste vahel.

<!-- ![](media/dual-write-payment-schedules.png) -->

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
NIMI | = | msdyn\_nimi
KIRJELDUS | = | msdyn\_description
ALLOCATIONMETHOD | \>\< | msdyn\_allocationmethod
PAYMENTFREQUENCYUNITS | \>\< | msdyn\_paymentfrequencyunit
PAYMENTFREQUENCY | = | msdyn\_paymentfrequency
NUMBEROFPAYMENTS | = | msdyn\_numberofpayments
FIXEDPAYMENTAMOUNT | = | msdyn\_fixedpaymentamount
MINIMUMPAYMENTAMOUNT | = | msdyn\_minimumpaymentamount
SALESTAXALLOCATIONMETHOD | \>\< | msdyn\_salestaxallocationmethod
MÄRKMED | = | msdyn\_note

## <a name="payment-schedule-lines"></a>Maksegraafiku read

Sünkroonib nii klientide kui ka hankijate maksegraafiku ridade viiteandmed rakenduste Finance and Operations ja teiste Dynamics 365 rakenduste vahel.

<!-- ![](media/dual-write-payment-schedule-lines.png) -->

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTSCHEDULENAME | \> | msdyn\_name
LINENUMBER | = | msdyn\_linenumber
PERIODSAFTERDUEDATE | = | msdyn\_periodsafterduedate
PERCENTORAMOUNT | \>\< | msdyn\_percentoramount
PERCENTORAMOUNTVALUE | = | msdyn\_percentoramountvalue

## <a name="payment-days"></a>Maksepäevad

See mall sünkroonib nii klientide kui ka hankijate maksepäevade viiteandmed rakenduste Finance and Operations ja teiste Dynamics 365 rakenduste vahel.

<!-- ![](media/dual-write-payment-days.png) -->

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
NIMI | = | msdyn\_nimi
KIRJELDUS | = | msdyn\_description

## <a name="payment-day-lines"></a>Maksepäeva read

See mall sünkroonib nii klientide kui ka hankijate maksepäevade ridade viiteandmed rakenduste Finance and Operations ja teiste Dynamics 365 rakenduste vahel.

<!-- ![](media/dual-write-payment-day-lines.png) -->

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
CDSINTEGRATIONKEY | = | msdyn\_paymentdaylineid
FREQUENCY | \>\< | msdyn\_frequency
DAYOFWEEK | \>\< | msdyn\_dayofweek
DAYOFMONTH | = | msdyn\_dayofmonth
NIMI | = | msdyn\_paymentday.msdyn\_name

## <a name="payment-terms"></a>Maksetingimused

See mall sünkroonib nii klientide kui ka hankijate maksetingimuste viiteandmed rakenduste Finance and Operations ja teiste Dynamics 365 rakenduste vahel.

<!-- ![](media/dual-write-payment-terms.png) -->

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
KIRJELDUS | = | msdyn\_description
NIMI | = | msdyn\_name
NUMBEROFMONTHS | = | msdyn\_numberofmonth
CUTOFFDAYOFMONTH | = | msdyn\_cutoffdayofmonth
ISCASHPAYMENT | \>\< | msdyn\_iscashpayment
NUMBEROFDAYS | = | msdyn\_days
ISCERTIFIEDCOMPANYCHECK | \>\< | msdyn\_iscertifiedcompanycheck
ISDEFAULTPAYMENTTERM | \>\< | msdyn\_isdefaultpaymentterm
CREDITCARDPAYMENTTYPE | \>\< | msdyn\_creditcardpaymenttype
CREDITCARDCREDITCHECKTYPE | \>\< | msdyn\_creditcardcreditchecktype
PAYMENTDAYNAME | = | msdyn\_paymentdayname.msdyn\_name
PAYMENTMETHODTYPE | \>\< | msdyn\_paymentmethodtype
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedulename.msdyn\_name

## <a name="name-affixes"></a>Nimeliited

See mall sünkroonib nii klientide kui ka hankijate nimeliidete viiteandmed rakenduste Finance and Operations ja teiste Dynamics 365 rakenduste vahel.

<!-- ![](media/dual-write-name-affixes.png) -->

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
LIIDE | = | msdyn\_affix
TÜÜP | \>\< | msdyn\_affixtype
KIRJELDUS | = | msdyn\_description
