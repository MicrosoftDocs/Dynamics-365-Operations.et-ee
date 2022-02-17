---
title: Isik
description: Selles teemas kirjeldatakse olemit Isik rakenduse Dynamics 365 Human Resources jaoks.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 728e383be44949ec7f1e51feb5157c61679b3e7b
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068655"
---
# <a name="person"></a>Isik


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse olemit Isik rakenduse Dynamics 365 Human Resources jaoks.

Füüsiline nimi: mshr_dirpersonentity

### <a name="description"></a>Kirjeldus

See olem pakab kandidaadiks oleva isiku isikuandmeid.

## <a name="json-representation"></a>JSON-i esindus

```json
{
    "mshr_partynumber": "String",
    "mshr_name": "String",
    "mshr_namealias": "String",
    "mshr_knownas": "String",
    "mshr_languageid": "String",
    "mshr_addressbooks": "String",
    "mshr_anniversaryday": Int,
    "mshr_anniversarymonth": Int,
    "mshr_anniversaryyear": Int,
    "mshr_birthday": Int,
    "mshr_birthmonth": Int,
    "mshr_birthyear": Int,
    "mshr_childrennames": "String",
    "mshr_gender": Int,
    "mshr_hobbies": "String",
    "mshr_initials": "String",
    "mshr_maritalstatus": Int,
    "mshr_phoneticfirstname": "String",
    "mshr_phoneticlastname": "String",
    "mshr_phoneticmiddlename": "String",
    "mshr_personalsuffix": "String",
    "mshr_personaltitle": "String",
    "mshr_professionalsuffix": "String",
    "mshr_professionaltitle": "String",
    "mshr_fullprimaryaddress": "String",
    "mshr_addresscity": "String",
    "mshr_addresscountryregionid": "String",
    "mshr_addresscountryregionisocode": "String",
    "mshr_addresscounty": "String",
    "mshr_addressdistrictname": "String",
    "mshr_addresslatitude": Decimal,
    "mshr_addresslocationid": "000003212",
    "mshr_addresslocationroles": "Home",
    "mshr_addresslongitude": Decimal,
    "mshr_addressstate": "String",
    "mshr_addressstreet": "String",
    "mshr_addressvalidfrom": "Date",
    "mshr_addressvalidto": "Date",
    "mshr_addresszipcode": "String",
    "mshr_addressisprivate": Int,
    "mshr_addressdescription": "String",
    "mshr_primarycontactemail": "String",
    "mshr_primarycontactemaildescription": "String",
    "mshr_primarycontactemailisim": Int,
    "mshr_primarycontactemailpurpose": "String",
    "mshr_primarycontactfax": "String",
    "mshr_primarycontactfaxdescription": "String",
    "mshr_primarycontactfaxextension": "String",
    "mshr_primarycontactfaxpurpose": "String",
    "mshr_primarycontactphone": "String",
    "mshr_primarycontactphonedescription": "String",
    "mshr_primarycontactphoneextension": "String",
    "mshr_primarycontactphoneismobile": Int,
    "mshr_primarycontactphonepurpose": "String",
    "mshr_primarycontacttelex": "String",
    "mshr_primarycontacttelexdescription": "String",
    "mshr_primarycontacttelexpurpose": "String",
    "mshr_primarycontacturl": "String",
    "mshr_primarycontacturldescription": "String",
    "mshr_primarycontacturlpurpose": "String",
    "mshr_primarycontactfacebook": "String",
    "mshr_primarycontactfacebookdescription": "String",
    "mshr_primarycontactfacebookisprivate": Int,
    "mshr_primarycontactfacebookpurpose": "String",
    "mshr_primarycontactlinkedin": "String",
    "mshr_primarycontactlinkedindescription": "String",
    "mshr_primarycontactlinkedinisprivate": Int,
    "mshr_primarycontactlinkedinpurpose": "String",
    "mshr_primarycontacttwitter": "String",
    "mshr_primarycontacttwitterdescription": "String",
    "mshr_primarycontacttwitterisprivate": Int,
    "mshr_primarycontacttwitterpurpose": "String",
    "mshr_partytype": "String",
    "mshr_namesequencedisplayas": "String",
    "mshr_firstname": "String",
    "mshr_lastnameprefix": "String",
    "mshr_lastname": "String",
    "mshr_middlename": "String",
    "mshr_electroniclocationid": "String",
    "mshr_dirpersonentityid": "Guid",
    "mshr_addresstimezone": Int
}
```

## <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Isiku olemi ID**<br>mshr_dirpersonentityid<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Süsteemi loodud | Olemi kirje süsteemi loodud kordumatu identifikaator. |
| **Osapoole number**<br>mshr_partynumber<br>*String* | Kirjutuskaitstud<br>Nõutav<br>Süsteemi loodud | Isiku süsteemi loodud kordumatu kasutaja poolt loetav identifikaator.  |
| **Nimi**<br>mshr_name<br>*String* | Kirjutuskaitstud<br>Nõutav | Välja väärtus ühendab eesnime, teist eesnime, perekonnanime eesliidet ja perekonnanime väljal **Nime kuvamise järjestus** määratletud järjekorras. |
| **Nime pseudonüüm**<br>mshr_namealias<br>*String* | Loe/kirjuta<br>Valikuline | Nime pseudonüüm, mis võidaks isikule anda. |
| **Tuntud kui**<br>mshr_knownas<br>*String* | Loe/kirjuta<br>Valikuline | Nimi, mida võidakse isiku kohta kasutada, kui teda tuntakse tavaliselt teise nimega. |
| **Keele ID**<br>mshr_languageid<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmase keele ID, nagu määratud ISO 639-1 vormingus. |
| **Aadressiraamatud**<br>mshr_addressbooks<br>*String* | Loe/kirjuta<br>Valikuline | Aadressiraamat, kuhu võidakse isik määrata. Organisatsiooni jaoks seadistatud aadressiraamatud on loetletud olemis mshr_diraddressbooksentity. |
| **Aastapäeva kuupäev**<br>mshr_anniversaryday<br>*Int* | Loe/kirjuta<br>Valikuline | Isiku aastapäeva kuupäev. |
| **Aastapäeva kuu**<br>mshr_anniversarymonth<br>*suvandikomplekt mshr_monthsofyear* | Loe/kirjuta<br>Valikuline | Isiku aastapäeva kuupäeva kuu. |
| **Aastapäeva aasta**<br>mshr_anniversaryyear<br>*Int* | Loe/kirjuta<br>Valikuline | Isiku aastapäeva kuupäeva aasta. |
| **Sünnikuupäev**<br>mshr_birthday<br>*Int* | Loe/kirjuta<br>Valikuline | Isiku sünnikuupäeva päev. |
| **Sünnikuu**<br>mshr_birthmonth<br>*suvandikomplekt mshr_monthsofyear* | Loe/kirjuta<br>Valikuline | Isiku sünnikuupäeva kuu. |
| **Sünniaasta**<br>mshr_birthyear<br>*Int* | Loe/kirjuta<br>Valikuline | Isiku sünnikuupäeva aasta. |
| **Laste nimed**<br>mshr_childrennames<br>*String* | Loe/kirjuta<br>Valikuline | Isiku laste nimede string. Kohustuslik piiritlemine puudub. |
| **Sugu**<br>mshr_gender<br>*suvandikomplekt mshr_hcmpersongender* | Loe/kirjuta<br>Valikuline | Isiku sugu. |
| **Hobid**<br>mshr_hobbies<br>*String* | Loe/kirjuta<br>Valikuline | Isiku hobid. |
| **Initsiaalid**<br>mshr_initials<br>*String* | Loe/kirjuta<br>Valikuline | Isiku nimetähed. |
| **Perekonnaseis**<br>mshr_maritalstatus<br>*suvandikomplekt mshr_hcmpersonmaritalstatus* | Loe/kirjuta<br>Valikuline | Isiku perekonnaseis. |
| **Foneetiline eesnimi**<br>mshr_phoneticfirstname<br>*String* | Loe/kirjuta<br>Valikuline | Isiku eesnime foneetiline hääldus. |
| **Foneetiline perekonnanimi**<br>mshr_phoneticlastname<br>*String* | Loe/kirjuta<br>Valikuline | Isiku perekonnanime foneetiline hääldus. |
| **Foneetiline teine eesnimi**<br>mshr_phoneticmiddlename<br>*String* | Loe/kirjuta<br>Valikuline | Isiku perekonnanime foneetiline hääldus. |
| **Isiku järelliide**<br>mshr_personalsuffix<br>*String* | Loe/kirjuta<br>Valikuline | Isiku isiklik järelliide. Kehtivad väärtused olemis mshr_dirnameaffixentity, kus mshr-tüüp on järelliide (200000001). |
| **Isiku tiitel**<br>mshr_personaltitle<br>*String* | Loe/kirjuta<br>Valikuline | Isiku isiklik tiitel. Kehtivad väärtused olemis mshr_dirnameaffixentity, kus mshr-tüüp on tiitel (200000000).
| **Tööalane järelliide**<br>msdyn_professionalsuffix<br>*String* | Loe/kirjuta<br>Valikuline | Tööalane järelliide. |
| **Ametinimetus**<br>mshr_professionaltitle<br>*String* | Loe/kirjuta<br>Valikuline | Ametinimetus. |
| **Täielik esmane aadress**<br>mshr_fullprimaryaddress<br>*String* | Loe/kirjuta<br>Valikuline | Isiku täielik esmane aadress, kus on ühendatud esmase aadressi väljad. |
| **Aadressi linn**<br>mshr_addresscity<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmase aadressi linn. Olemi mshr_logisticsaddresscityentity seadistamine. |
| **Aadressi riigi piirkond**<br>mshr_addresscountryregionid<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmase aadressi riik/piirkond linn. Kehtivad väärtused olemis mshr_logisticsaddresscountryregionentity. |
| **Aadressi riigi piirkonna ISO-kood**<br>mshr_addresscountryregionisocode<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmase aadressi riigi ISO-kood. |
| **Aadressi riik**<br>mshr_addresscounty<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmase aadressi riik. Olemi mshr_logisticsaddresscountyentity seadistamine. |
| **Aadressi piirkonna nimi**<br>mshr_addressdistrictname<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmase aadressi piirkond. Olemi mshr_logisticsaddressdistrictentity seadistamine. |
| **Aadressi laiuskraad**<br>mshr_addresslatitude<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmase aadressi laiuskraad. |
| **Aadressi asukoha ID**<br>mshr_addresslocationid<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmase aadressi asukoha kordumatu identifikaator. Kehtivad väärtused olemis mshr_logisticspostaladdresslocationcdsentity. |
| **Aadressi asukoha rollid**<br>mshr_addresslocationroles<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmase aadressi asukoha roll linn. Olemi mshr_logisticslocationrolecdsentity seadistamine. |
| **Aadressi Pikkuskraad**<br>mshr_addresslongitude<br>*String* |  Loe/kirjuta<br>Valikuline | Isiku esmase aadressi pikkuskraad. |
| **Aadressi osariik**<br>mshr_addressstate<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmase aadressi osariik. Olemi mshr_logisticsaddressstateentity seadistamine. |
| **Aadressi tänav**<br>mshr_addressstreet<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmase aadressi tänava aadress linn. |
| **Aadress kehtiv alates**<br>mshr_addressvalidfrom<br>*Kuupäev* | Loe/kirjuta<br>Valikuline | Kuupäev, millest alates isiku esmane aadress kehtib. |
| **Aadress kehtiv kuni**<br>mshr_addressvalidto<br>*Kuupäev* | Loe/kirjuta<br>Valikuline | Kuupäev, milleni isiku esmane aadress kehtib. |
| **Aadressi sihtnumber**<br>mshr_addresszipcode<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmase aadressi sihtnumber. Olemi mshr_logisticsaddresspostalcodeentity seadistamine. |
| **Aadress on privaatne**<br>mshr_addressisprivate<br>*suvandikomplekt mshr_noyes* | Loe/kirjuta<br>Valikuline | Määratleb, kas isiku esmast aadressi jagatakse organisatsioonis teistega. |
| **Aadressi kirjeldus**<br>mshr_addressdescription<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmase aadressi kirjeldus. |
| **Esmane kontaktmeil**<br>mshr_primarycontactemail<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmane meiliaadress. |
| **Esmase kontaktmeili kirjeldus**<br>mshr_primarycontactemaildescription<br>*String* | Loe/kirjuta<br>Valikuline | Esmasele meiliaadressile antud kirjeldus. |
| **Esmane kontaktmeil on IM**<br>mshr_primarycontactemailisim<br>*suvandikomplekt mshr_noyes* | Loe/kirjuta<br>Valikuline | Määratleb, kas esmane meiliaadress on kiirsõnumite jaoks saadaval. |
| **Esmase kontaktmeili otstarve**<br>mshr_primarycontactemailpurpose<br>*String* | Loe/kirjuta<br>Valikuline | Esmase meiliaadressi otstarve. Olemi mshr_logisticslocationroleentity seadistamine. |
| **Esmane kontaktfaks**<br>mshr_primarycontactfax<br>*String* | Loe/kirjuta<br>Valikuline | Esmane faksinumber. |
| **Esmase kontaktfaksi kirjeldus**<br>mshr_primarycontactfaxdescription<br>*String* | Loe/kirjuta<br>Valikuline | Esmasele faksinumbrile antud kirjeldus. |
| **Esmase kontaktfaksi laiend**<br>mshr_primarycontactfaxextension<br>*String* | Loe/kirjuta<br>Valikuline | Esmase faksinumbri laiend. |
| **Esmase kontaktfaksi otstarve**<br>mshr_primarycontactfaxpurpose<br>*String* | Loe/kirjuta<br>Valikuline | Esmase faksinumbri otstarve. Olemi mshr_logisticslocationroleentity seadistamine.
| **Esmane kontakttelefon**<br>mshr_primarycontactphone<br>*String* | Loe/kirjuta<br>Valikuline | Esmane telefoninumber. |
| **Esmase kontakttelefoni kirjeldus**<br>mshr_primarycontactphonedescription<br>*String* | Loe/kirjuta<br>Valikuline | Esmasele telefoninumbrile antud kirjeldus. |
| **Esmase kontakttelefoni laiend**<br>mshr_primarycontactphoneextension<br>*String* | Loe/kirjuta<br>Valikuline | Esmase telefoninumbri laiend. |
| **Esmane kontakttelefon on mobiil**<br>mshr_primarycontactphoneismobile<br>*suvandikomplekt mshr_noyes* | Loe/kirjuta<br>Valikuline | Määratleb, kas esmane telefoninumber on mobiiltelefon. |
| **Esmase kontakttelefoni otstarve**<br>mshr_primarycontactphonepurpose<br>*String* | Loe/kirjuta<br>Valikuline | Esmase telefoninumbri otstarve. Olemi mshr_logisticslocationroleentity seadistamine. |
| **Esmane kontaktteleks**<br>mshr_primarycontacttelex<br>*String* | Loe/kirjuta<br>Valikuline | Esmane teleksi number. |
| **Esmase kontaktteleksi kirjeldus**<br>mshr_primarycontacttelexdescription<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmasele teleksinumbrile antud kirjeldus. |
| **Esmase kontaktteleksi otstarve**<br>mshr_primarycontacttelexpurpose<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmase teleksinumbri otstarve. Olemi mshr_logisticslocationroleentity seadistamine. |
| **Esmase kontakti URL**<br>mshr_primarycontacturl<br>*String* | Loe/kirjuta<br>Valikuline | Esmane URL. |
| **Esmase kontakti URLi kirjeldus**<br>mshr_primarycontacturldescription<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmasele URLile antud kirjeldus. |
| **Esmase kontakti URLi otstarve**<br>mshr_primarycontacturldescription<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmase URLi otstarve. Olemi mshr_logisticslocationroleentity seadistamine. |
| **Esmane kontakti Facebook**<br>mshr_primarycontactfacebook<br>*String* | Loe/kirjuta<br>Valikuline | Esmane Facebooki konto. Tuvastanud kasuta ID. |
| **Esmase kontakti Facebooki kirjeldus**<br>mshr_primarycontactfacebookdescription<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmasele Facebooki kontole antud kirjeldus. |
| **Esmane kontakti Facebook on privaatne.**<br>mshr_primarycontactfacebookisprivate<br>*suvandikomplekt mshr_noyes* | Loe/kirjuta<br>Valikuline | Määratleb, kas esmane Facebooki konto on teistele kasutajatele nähtav. |
| **Esmase kontakti Facebooki otstarve**<br>mshr_primarycontactfacebookpurpose<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmase Facebooki konto otstarve. Olemi mshr_logisticslocationroleentity seadistamine. |
| **Esmane kontakt LinkedIn**<br>mshr_primarycontactlinkedin<br>*String* | Loe/kirjuta<br>Valikuline | Esmane LinkedIni konto. Tuvastatud kasutajanime järgi. |
| **Esmase kontakti LinkedIni kirjeldus**<br>mshr_primarycontactlinkedindescription<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmasele LinkedIni kontole antud kirjeldus. |
| **Esmase kontakti LinkedIn on privaatne**<br>mshr_primarycontactlinkedinisprivate<br>*suvandikomplekt mshr_noyes* | Loe/kirjuta<br>Valikuline | Määratleb, kas isiku esmast LinkedIni kontoteavet jagatakse teiste kasutajatega. |
| **Esmase kontakti LinkedIni otstarve**<br>mshr_primarycontactlinkedinpurpose<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmase LinkedIni konto otstarve. Olemi mshr_logisticslocationroleentity seadistamine. |
| **Esmase kontakti Twitter**<br>mshr_primarycontacttwitter<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmane Twitteri konto. Tuvastatud @username järgi. |
| **Esmase kontakti Twitteri kirjeldus**<br>mshr_primarycontacttwitterdescription<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmasele Twitteri kontole antud kirjeldus. |
| **Esmase kontakti Twitter on privaatne**<br>mshr_primarycontacttwitterisprivate<br>*suvandikomplekt mshr_noyes* | Loe/kirjuta<br>Valikuline | Määratleb, kas isiku esmast Twitteri kontoteavet jagatakse teiste kasutajatega. |
| **Esmase kontakti Twitteri otstarve**<br>mshr_primarycontacttwitterpurpose<br>*String* | Loe/kirjuta<br>Valikuline | Isiku esmase Twitteri konto otstarve. Olemi mshr_logisticslocationroleentity seadistamine. |
| **Osapoole tüüp**<br>mshr_partytype<br>*String* | Loe/kirjuta<br>Valikuline | Isiku osapoole tüüp. Kandidaatide joaks on see alati **Isik**. |
| **Nime järjekorra kuvamine**<br>mshr_namesequencedisplayas<br>*String* | Loe/kirjuta<br>Valikuline | Järjestus, milles isiku nime atribuute Nime (mshr_name) atribuuti väärtuse moodustamiseks koondatakse. |
| **Eesnimi**<br>mshr_firstname<br>*String* | Loe/kirjuta<br>Nõutav | Isiku eesnimi. |
| **Teine eesnimi**<br>mshr_middlename<br>*String* | Loe/kirjuta<br>Valikuline | Isiku teine eesnimi. |
| **Perekonnanime eesliide**<br>mshr_lastnameprefix<br>*String* | Loe/kirjuta<br>Valikuline | Isiku perekonnanime eesliide. |
| **Perekonnanimi**<br>mshr_lastname<br>*String* | Loe/kirjuta<br>Valikuline | Isiku perekonnanimi. |
| **Elektroonilise asukoha ID**<br>mshr_electroniclocationid<br>*String* | Loe/kirjuta<br>Valikuline | Isiku elektroonilise asukoha ID. |
| **Aadressi ajavöönd**<br>mshr_addresstimezone<br>*Int* | Loe/kirjuta<br>Valikuline | Isiku esmase aadressi ajavöönd. |

## <a name="see-also"></a>Vt ka

[Kandidaadi jälgimissüsteemi integreerimise API tutvustus](hr-admin-integration-ats-api-introduction.md)<br>
[Palgatava kandidaadi päringu näidis](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
