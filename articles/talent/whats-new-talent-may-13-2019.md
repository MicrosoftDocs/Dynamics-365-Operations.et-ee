---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (13. mai 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 05/13/2019
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
ms.search.validFrom: 2019-05-13
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 11c9f03f4b3915d81b624115a1d97a0c7bc31709
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529728"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-13-2019"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (13. mai 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas kirjeldatakse Dynamics 365 Talenti uusi või muutunud funktsioone.

## <a name="coming-soon-in-attract"></a>Peagi tulekul rakenduses Attract

### <a name="job-approvals-on-home-page"></a>Töökinnitused avalehel

Kinnitused kuvatakse armatuurlaua jaotises **Kinnitused**. Kinnitajad saavad kinnitusi üle vaadata jaotises **Teile määratud**, kus kuvatakse töö ID, pealkiri, teised kinnitajad ja määramise kuupäev. Kasutajad, kes töö kinnitamiseks esitavad, saavad oma töid üle vaadata jaotises **Teie taotletud**, mis kuvab kinnitajaid, kes peavad edastatud tööd veel kinnitama.

## <a name="changes-in-onboard"></a>Muutused Onboardis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused

Jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2297. Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Microsoft Dynamics Lifecycle Services (LCS).

### <a name="indicate-instance-type-when-provisioning-talent"></a>Näidake eksemplari tüüpi Talenti ettevalmistamisel

Uue Talenti eksemplari ettevalmistamisel saate näidata, kas eksemplari tüüp on **Tootmine** või **Liivakast**, mis võimaldab uute funktsioonide varajast testimist. Kõik olemasolevad Talenti eksemplarid uuendatakse eksemplari tüübiks **Tootmine**. Kui soovite mõne olemasoleva eksemplari värskendada eksemplari tüübiks **Liivakast**, võtke muudatuse taotlemiseks ühendust [toega](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support).

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service'i üksuse tugi kohandatud väljadele

Selle nädala väljaandes toetavad nüüd järgmised teenuse Common Data Service üksused kohandatud välju: tööhõive, soodustuse arvutamise sagedus, soodustuse arvutamise määr, pühad töökalendris ja identifikatsiooni tüüp.

### <a name="common-data-service-integration-page"></a>Teenuse Common Data Service integratsiooni leht

Selles väljalaskes pakutakse uut suvandit menüüs **Süsteemihaldus > Lingid > Integratsioonid > Teenuse Common Data Service konfiguratsioon**. Suvand **Teenuse Common Data Service konfiguratsioon** pakub administraatorile või andmehalduse administraatorile paindlikkust ja ülevaateid teenusega Common Data Service. Selle suvandiga saate lubada või keelata teenuse Common Data Service integratsiooni Talenti eksemplariga ja vaadata sünkroonimise üksikasju Talenti eksemplaris ning teenuses Common Data Service.

### <a name="import-performance-data-with-final-employee-rating-316710"></a>Jõudluse andmete importimine lõpliku töötaja hinnanguga (316710)

Selles väljalaskes saate importida ajaloolisi töötajate hinnangute andmeid. Väljal **FinalEmployeeRatingId** on nüüd kirjutusõigus.

### <a name="cant-create-worker-address-in-common-data-service-and-sync-it-with-talent-317555"></a>Teenuses Common Data Service ei saa luua töötaja aadressi ja seda Talentiga sünkroonida (317555)

See muudatus lubab teenuses Common Data Service loodud aadressiandmeid Talentiga sünkroonida.

## <a name="in-preview"></a>Eelvaates

### <a name="new-page-to-validate-position-hierarchy-data"></a>Uus leht ametikoha hierarhia andmete kinnitamiseks

Personaliosakond ja administraatorid saavad kinnitada juhtimishierarhiat mis tahes ringviidetega, mis võivad olla kogemata imporditud. Sellele uuele leheküljele pääsete, kui lähete **Organisatsiooni haldus > Lingid > Ametikohad > Ametikoha hierarhia kinnitamine**.

### <a name="specify-reason-codes-on-leave-types"></a>Määrake puhkuse tüüpide põhjusekoodid

Organisatsioonid võivad vajada puhkuseavaldustega seotud lisanduvat infot. Nüüd saate määrata puhkuse tüüpidega seotud põhjusekoodid ja lasta töötajatel valida põhjusekood oma puhkuseavaldusele.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Kindlat tüüpi puhkusetüüpidele ja puhkuseavaldustele põhjusekoodide nõudmine

Organisatsioonid võivad nõuda teatud puhkusetüüpide korral töötajate esitatud puhkusetaotluste põhjusekoodide määramist. See nõue võib eksisteerida ettevõtte poliitika või regulatiivsete nõuete tõttu. Saate määrata, milline puhkusetüüp vajab põhjusekoodi, ja saate nõuda, et töötajad esitaksid puhkuseavaldusel oma puhkusetüübile põhjusekoodi.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Personaliosakonnale puhkuse ja puudumise kannete nimekirja esitamine

Võimalus jägida töötaja puhkuseaega ja mõista, kuidas puhkus on arvestatud, mitte ainult ei aita personaliosakonnal vastata töötajate küsimustele, vaid võimaldab ka töötajatele tagada täpse puhkusehüvitise. Personaliosakonnal on nüüd uus tehingute vaade (hüvitused, viitvõlad, korrigeerimised ja taotlused), et personaliosakond näeks puhkuse saldode taga olevaid põhjuseid.


[!INCLUDE[footer-include](../includes/footer-banner.md)]