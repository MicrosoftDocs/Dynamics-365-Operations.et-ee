---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (23. aprill, 2019)?
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 04/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-04-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1a70be88e3ab65bb0bdd844347e8ba69e4ba61a5
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024110"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-23-2019"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (23. aprill, 2019)?

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse Dynamics 365 Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis
See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Muutused Onboardis
See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused
Jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2253. Sulgudes olevad numbrid viitavad toenumbritele teenuses Lifecycle Services (LCS).

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service'i üksuse tugi kohandatud väljadele
Selle nädala väljaandes toetavad järgmised üksused kohandatud välju: hüvituse tase, soodustuse suvand, oskuse tüüp ja hüvituspiirkond.

### <a name="additional-odata-entities-302992"></a>Täiendavad OData üksused (302992)
Järgmised üksused on nüüd toetatud ODataga: töötaja töökogemus ja töötaja haridus.
   
### <a name="performance-journal-attachments-for-managers-and-employees-308248"></a>Juhtide ja töötajate jõudluse töölehe manused (308248)
Koos selle väljaandega on nüüd saadaval manused nii juhtidele kui ka töötajatele jõudluse töölehe kirjete loomisel ja uuendamisel.

### <a name="employee-rehire-flag-always-available-310047"></a>Töötaja uuesti palkamise lipp on alati saadaval (310047)
Töötaja uuesti palkamise suvand on nüüd saadaval uuendamiseks väljapool lõpetamise protsessi. 

### <a name="cannot-change-the-name-of-my-payment-method-308815"></a>Ei saa muuta **Minu makseviisi** (308815) nime
Isikupärastamine on lubatud, et lubada sildi **Minu makseviisi meetod** muutmist töötaja iseteeninduses.

### <a name="financial-dimensions-against-a-position-cant-be-deleted-293908"></a>Ametikoha finantsdimensioone ei saa kustutada (293908)
Finantsdimensioonid saab nüüd eemaldada olemasoleva ametikoha muudatuse taotlemisel ja finantsdimensioonide ettevõtteüleste piiride puhul. 

### <a name="customer-is-unable-to-publish-back-data-into-talent-when-opening-the-data-from-excel-302955"></a>Klient ei saa avaldada andmeid tagasi Talenti, kui avada andmed Excelis (302955)
See muudatus parandab avaldamise probleemi, kui kasutakse seotud tabeleid.

## <a name="in-preview"></a>Eelvaates

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Puhkuse tüüpidele põhjusekoodide määramise lubamine
Organisatsioonid võivad vajada puhkuseavaldustega seotud lisanduvat infot. Nüüd saate määrata puhkuse tüüpidega seotud põhjusekoodid ja lubada töötajatel valida põhjusekood oma puhkuseavaldusele.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Teatud tüüpi puhkusetüüpidele ja puhkuseavaldustele põhjusekoodide nõudmine
Organisatsioonid võivad nõuda teatud puhkusetüüpide korral töötajate esitatud puhkuseavaldustele põhjusekoodide määramist. See võib toimuda vastavalt ettevõtte poliitikale või regulatiivsetele nõuetele. Nüüd saate määrata, milline puhkusetüüp vajab põhjusekoodi ja saate nõuda, et töötaja esitab oma puhkuseavaldusel oma puhkusetüübile põhjusekoodi.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>Personaliosakonnale puhkuse ja puudumise kannete nimekirja esitamine
Töötajate puhkuseaja jälgimine ja mõistmine, kuidas puhkus on arvestatud, mitte ainult ei aita personaliosakonnal vastata töötajate küsimustele, vaid võimaldab ka töötajatele täpse puhkusehüvitise. Personaliosakonnal on nüüd uus tehingute vaade (hüvitused, viitvõlad, korrigeerimised ja taotlused), et näha saldode taga olevaid põhjuseid.

## <a name="coming-soon"></a>Peagi tulekul

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Kasutajaliidesele täiustused töötajate duplikaatide kontrollimiseks
Selle muudatusega tuvastatakse nimeväljade sisestamisel duplikaadid ja olek näitab leitud duplikaatide arvu. Võite uue lehe avamiseks valida antud lingi, et hinnata, kas kasutada tuvastatud vastet. Andmesisestuse katkestamise vältimiseks ei avane duplikaatide vorm automaatselt.
## <a name="known-issues"></a>Teadaolevad probleemid

### <a name="email-support-for-alerts"></a>E-posti tugi teatistele
Finance and Operationsi platvormi 26. uuendusega saavad kasutajad luua alarmide reegleid, mis saadavad sündmuse poolt käivitades automaatselt kontaktidele meiliteavitusi.
