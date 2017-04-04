---
title: "Hankija koostöö kasutajate haldamine"
description: "See teema kirjeldab, kuidas saate taotleda uue hankija koostöö kasutajate ettevalmistamist ja kuidas lisada uue hankija koostöö kontakte."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 380f1bcdf7109dc12fd898199033eac7710d863c
ms.lasthandoff: 03/31/2017


---

# <a name="manage-vendor-collaboration-users"></a>Hankija koostöö kasutajate haldamine

See teema kirjeldab, kuidas saate taotleda uue hankija koostöö kasutajate ettevalmistamist ja kuidas lisada uue hankija koostöö kontakte. 

Hankija koostöö liides rakenduses Microsoft Dynamics 365 for Operations paljastab teavet ostutellimuste, arvete ja veosevarude kohta välistele hankijatele. Saate luua uued hankija koostöö kontaktid ja nõuda, et uued kasutajad valmistatakse ette, kui töötate välise hankijana turberolliga **Hankija administraator (väline)** või sarnaste lubadega. Samuti saate teha need ülesanded, kui töötate hankeprofessionaalina. Selles teemas viitab see roll hankeprofessionaalile, kes töötab selle ettevõtte siseselt, millele kuulub rakenduse Dynamics 365 for Operations eksemplar. Kui sa välise hankija hankija koostöö kasutamise kohta lisateabe saamiseks vt [hankija klientidega](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Kasutamise hankija koostöö, kui sa oled professionaalne hanke kohta lisateabe saamiseks vt [hankija koostöö väliste tarnijate](vendor-collaboration-work-external-vendors.md).

## <a name="add-new-vendor-collaboration-contacts"></a>Uue hankija koostöö kontaktide lisamine
Kui soovite, et kellelgi oleks juurdepääs hankija koostööle, tuleb nad esmalt lisada hankija koostöö kontaktina. Võite soovi korral lisada kontakte oma ettevõtte töötajatele, kes ei kasuta hankija koostööd. Näiteks võivad nad olla kontaktpunktiks teist tüüpi hanketeabele. Uued kontaktid on lisatud ka **kõik kontaktid** leht, mis pääseb on **hankija koostöö**&gt;**kontaktid** menüü. Uue kontakti lisamiseks:

1.  Klõpsake valikut **Uus**.
2.  Sisestage kontaktisiku üksikasjad.
3.  Valige, millist juriidilist isikut nad teie ettevõttes tähistavad ja millise juriidilise isikuga nad töötavad ettevõttes, millega nad koostööd teevad. Seda valides on **minu firma juriidilise isiku**/**kliendi ettevõtte juriidilise isiku** paari.
4.  Klõpsake valikut **Loo**.

Kui soovite kontakti kustutada, siis on võimalik kustutada ainult need, mille olete loonud.

## <a name="vendor-collaboration-user-requests"></a>Hankija koostöö kasutajataotlused
Hankija koostöö kasutajataotlused saab tõstada hankeprofessionaal või väline hankija administraator.

-   Kui sa välise hankija, esitate taotlusi ning **kõik kontaktid** jooksul lehekülg on **hankija koostöö** moodul.
-   Kui olete hankeprofessionaal, edastate taotlusi lehelt **Kuva kontaktid**. Selleks hankija kohta, mis on **Setup** lõik tegevus paanil valige **kontaktid**&gt;**kontaktisikute**.

Saate teha taotluse kasutaja ettevalmistamiseks, kasutaja inaktiveerimiseks või turberollide modifitseerimiseks. Kui olete välise hankija administraator, peate olema registreeritud selliste hankijakontode kontaktisikuna, mille jaoks soovite kasutajataotlusi teha, ja teil peab olema juurdepääs hankija koostöö liidesele nende hankijakontode puhul.  

Taotluse edastamisel lisatakse see mooduli **Hankija koostöö** loendisse **Hankija koostöö kasutajataotlused** ja mooduli **Hanked** loendisse **Hankija koostöö kasutajataotlus** (hangete moodul ei ole välistele kasutajatele juurdepääsetav).

### <a name="provision-a-user"></a>Kasutaja ettevalmistamine

Enne kui saate taotleda uue kasutaja ettevalmistamist, tuleb see isik seadistada kontaktina ühe või mitme hankijakonto jaoks. Uue hankija koostöö kasutaja jaoks taotluse loomiseks:

1.  Kohta ning **kõik kontaktid** klõpsake valikul **sätte hankija kasutaja**.
2.  Sisestage kasutaja meiliaadress. Seda aadressi kasutab kasutaja, et logida sisse rakendusse Dynamics 365 for Operations. Kui meiliaadress kuulub domeenile, mis on registreeritud Microsoft Azure'iga üürnikuna, siis peab meiliaadress olema olemasolev Azure Active Directory (ADD) konto, et ettevalmistamise protsessi saaks edukalt lõpuke viia. Kui meiliaadress ei kuulu Microsoft Azure'iga registreeritud domeenile, luuakse ADD konto osana ettevalmistamise protsessit ja uus kasutaja saab kutsemeili. Tarbija e-posti käsitletakse valdkonda nagu @hotmail.com, @gmail.com, või @comcast.netei saa kasutada Dynamics 365 toimingute kasutaja registreerimiseks.
3.  Seadke suvand **Hankija koostöö juurdepääs on lubatud** valikule **Jah** kõikide juriidiliste isikute puhul, millele kasutaja vajab juurdepääsu.
4.  Jaotises **Kasutaja rollide määramine** valige märkeruut **Määra** turberollidele, mis uuel kasutajal peaks olema.
5.  Klõpsake **Edasta**.

Hankija kasutaja taotluse esitamisel on **hankija koostöö ligipääsetavuse** on välja **Jah** valitud hankija konto ja kasutaja paluda töövoo käivitamist. Osana töövoost luuakse rakenduses Dynamics 365 for Operations uus kasutaja ja määratakse turberollid. Lisaks aktiveeritakse Azure B2B teenus, mis käivitab suhtluse Azure'i portaaliga ja seostab uut või olemasolevat AAD kontot rakenduse Dynamics 365 for Operations kasutajakontoga.

### <a name="inactivate-a-user"></a>Kasutaja inaktiveerimine

On kaks viisi, kuidas eemaldada kasutaja juurdepääs hankija koostööle:

-   Hankija lehel **Kontaktid** määrake suvandi **Hankija koostöö juurdepääs on lubatud** sätteks kontakti puhul **Ei**. Seda saab teha individuaalselt juriidilise isiku järgi, millele isik kontakt on. Seda suvandit saavad kasutada ainult hankeprofessionaalid.
-   Inaktiveerige kogu kasutajakonto, edastades taotluse **Hankija-kasutaja inaktiveerimine**.

Taotleda, et kasutaja on aktiivne:

1.  Kohta ning **kõik kontaktid** klõpsake valikul **Inactivate****hankija kasutaja**.
2.  Kirjutage kommentaar väljale **Äripõhjendus**.
3.  Klõpsake **Edasta**.

### <a name="modify-security-roles"></a>Turberollide modifitseerimine

Selle **säilitada hankija Kasutajarollid** lehekülg on sama, mis on **sätte hankija kasutaja** lehekülg välja, et turberollid loendi redigeerimiseks.  

Taotleda, et turberollid muudetakse kasutaja:

1.  Kohta ning **kõik kontaktid** klõpsake valikul **Säilita****hankija Kasutajarollid**.
2.  Kirjutage kommentaar väljale **Äripõhjendus**.
3.  Jaotises **Säilita kasutajarollid** valige turberollid, mida soovite määrata, või tühjendage need, mida soovite eemaldada.
4.  Click **Submit**.



