---
title: Hankija koostöö kasutajate haldamine
description: See teema kirjeldab, kuidas saate taotleda uue hankija koostöö kasutajate ettevalmistamist ja kuidas lisada uue hankija koostöö kontakte.
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 29930fdb65f96e281e0f0f01db41ec1475ad81c2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426542"
---
# <a name="manage-vendor-collaboration-users"></a>Hankija koostöö kasutajate haldamine

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas saate taotleda uue hankija koostöö kasutajate ettevalmistamist ja kuidas lisada uue hankija koostöö kontakte. 

Hankija koostöö liides rakenduses Dynamics 365 Supply Chain Management avaldab teavet ostutellimuste, arvete ja veosevarude kohta välistele hankijatele. Saate luua uued hankija koostöö kontaktid ja nõuda, et uued kasutajad valmistatakse ette, kui töötate välise hankijana turberolliga **Hankija administraator (väline)** või sarnaste lubadega. Samuti saate teha need ülesanded, kui töötate hankeprofessionaalina. Selles teemas viitab see roll hankeprofessionaalile, kes töötab selle ettevõtte siseselt, millele kuulub Supply Chain Managementi eksemplar. Lisateavet selle kohta, kuidas kasutada hankija koostööd, kui olete väline hankija, vaadake jaotisest [Hankija koostöö klientidega](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Lisateavet selle kohta, kuidas kasutada hankija koostööd, kui olete väline hankija, vaadake teemast [Hankija koostöö väliste hankijatega](vendor-collaboration-work-external-vendors.md).

## <a name="add-new-vendor-collaboration-contacts"></a>Uue hankija koostöö kontaktide lisamine
Kui soovite, et kellelgi oleks juurdepääs hankija koostööle, tuleb nad esmalt lisada hankija koostöö kontaktina. Võite soovi korral lisada kontakte oma ettevõtte töötajatele, kes ei kasuta hankija koostööd. Näiteks võivad nad olla kontaktpunktiks teist tüüpi hanketeabele. Uued kontaktid lisatakse lehel **Kõik kontaktid** millele on juurdepääs menüüst **Hankija koostöö** &gt; **Kontaktid**. Uue kontakti lisamiseks:

1.  Klõpsake valikut **Uus**.
2.  Sisestage kontaktisiku üksikasjad.
3.  Valige, millist juriidilist isikut nad teie ettevõttes tähistavad ja millise juriidilise isikuga nad töötavad ettevõttes, millega nad koostööd teevad. Selleks valite paari **Juriidiline isik minu ettevõttes**/**Juriidiline isik kliendi ettevõttes**.
4.  Klõpsake valikut **Loo**.

Kui soovite kontakti kustutada, siis on võimalik kustutada ainult need, mille olete loonud.

## <a name="vendor-collaboration-user-requests"></a>Hankija koostöö kasutajataotlused
Hankija koostöö kasutajataotlused saab tõstada hankeprofessionaal või väline hankija administraator.

-   Kui olete väline hankija, edastate taotlusi lehelt **Kõik kontaktid** mooduli **Hankija koostöö** siseselt.
-   Kui olete hankeprofessionaal, edastate taotlusi lehelt **Kuva kontaktid**. Selleks tehke hankija kirjel Toimingupaani jaotises **Seadistus** valikud **Kontaktid** &gt; **Kuva kontaktid**.

Saate teha taotluse kasutaja ettevalmistamiseks, kasutaja inaktiveerimiseks või turberollide modifitseerimiseks. Kui olete välise hankija administraator, peate olema registreeritud selliste hankijakontode kontaktisikuna, mille jaoks soovite kasutajataotlusi teha, ja teil peab olema juurdepääs hankija koostöö liidesele nende hankijakontode puhul.  

Taotluse edastamisel lisatakse see mooduli **Hankija koostöö** loendisse **Hankija koostöö kasutajataotlused** ja mooduli **Hanked** loendisse **Hankija koostöö kasutajataotlus** (hangete moodul ei ole välistele kasutajatele juurdepääsetav).

### <a name="provision-a-user"></a>Kasutaja ettevalmistamine

Enne kui saate taotleda uue kasutaja ettevalmistamist, tuleb see isik seadistada kontaktina ühe või mitme hankijakonto jaoks. Uue hankija koostöö kasutaja jaoks taotluse loomiseks:

1. Lehel **Kõik kontaktid** klõpsake valikut **Valmista ette hankija-kasutaja**.
2. Sisestage kasutaja meiliaadress. Kasutaja kasutab seda aadressi Supply Chain Managementi sisselogimiseks. Kui meiliaadress kuulub domeenile, mis on registreeritud Microsoft Azure’is üürnikuna, siis peab meiliaadress olema olemasolev Azure Active Directory (AAD) konto, et ettevalmistamise protsessi saaks edukalt lõpule viia. Kui meiliaadress ei kuulu Microsoft Azure’is registreeritud domeenile, luuakse AAD konto osana ettevalmistamise protsessist ja uus kasutaja saab kutsemeili. Laiatarbemeiliaadresse, mis on selliste domeenidega nagu @hotmail.com, @gmail.com või @comcast.net, ei saa kasutada kasutaja registreerimiseks.
3. Seadke suvand **Hankija koostöö juurdepääs on lubatud** valikule **Jah** kõikide juriidiliste isikute puhul, millele kasutaja vajab juurdepääsu.
4. Jaotises **Kasutaja rollide määramine** valige märkeruut **Määra** turberollidele, mis uuel kasutajal peaks olema.
5. Klõpsake **Edasta**.

Hankija-kasutaja taotluse edastamisel seatakse valitud hankija konto väli **Hankija koostöö juurdepääs on lubatud** olekusse **Jah** ja käivitatakse kasutajataotluse töövoog. Osana töövoost luuakse uus kasutaja ja määratakse turberollid. Lisaks aktiveeritakse Azure B2B teenus, mis käivitab suhtluse Azure'i portaaliga ja seostab uut või olemasolevat AAD kontot Supply Chain Managementi kasutajakontoga. Lisateavet vt teemast [Mis on Azure AD B2B koostöö?](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b).

### <a name="inactivate-a-user"></a>Kasutaja inaktiveerimine

On kaks viisi, kuidas eemaldada kasutaja juurdepääs hankija koostööle:

-   Hankija lehel **Kontaktid** määrake suvandi **Hankija koostöö juurdepääs on lubatud** sätteks kontakti puhul **Ei**. Seda saab teha individuaalselt juriidilise isiku järgi, millele isik kontakt on. Seda suvandit saavad kasutada ainult hankeprofessionaalid.
-   Inaktiveerige kogu kasutajakonto, edastades taotluse **Hankija-kasutaja inaktiveerimine**.

Kasutaja inaktiveerimise taotlemiseks tehke järgmist.

1.  Klõpsake lehel **Kõik kontaktid** valikut **Inaktiveeri** **hankija-kasutaja**.
2.  Kirjutage kommentaar väljale **Äripõhjendus**.
3.  Klõpsake **Edasta**.

### <a name="modify-security-roles"></a>Turberollide modifitseerimine

Leht **Säilita hankija-kasutaja rollid** on sama mis leht **Valmista ette hankija-kasutaja**, välja arvatud see, et turberollide loendit saab redigeerida.  

Kasutaja turberollide muutmise taotlemiseks tehke järgmist.

1.  Klõpsake lehel **Kõik kontaktid** valikut **Halda** **hankija-kasutaja rolle**.
2.  Kirjutage kommentaar väljale **Äripõhjendus**.
3.  Jaotises **Säilita kasutajarollid** valige turberollid, mida soovite määrata, või tühjendage need, mida soovite eemaldada.
4.  Klõpsake **Edasta**.




