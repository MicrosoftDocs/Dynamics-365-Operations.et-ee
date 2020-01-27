---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (6. mai 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 05/06/2019
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
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f06d989ea4e927111729dfbd4bb7700745a16a54
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897507"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-6-2019"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (6. mai 2019)

Selles teemas kirjeldatakse Dynamics 365 Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis

### <a name="select-optional-documents-upon-offer-creation"></a>Lisakokumentide valimine pakkumise loomisel

Kui valite pakkumise paketimalli, viipab Attract teid nüüd valima sobivaid, lisadokumente sellest paketimallist. Pakkumise ettevalmistamise ajal saate lisada muid lisadokumente.

## <a name="changes-in-onboard"></a>Muutused Onboardis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused

Jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2282. Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-26-for-finance-and-operations"></a>Finance and Operationsi 26. platvormi värskendus

Finance and Operationsi platvormivärskenduse 26 kohta lisainfo saamiseks vt [Dynamics 365 Finance and Operations platvormivärskenduse 26 (mai 2019) funktsioonide eelvaade](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26). 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service'i üksuse tugi kohandatud väljadele

Selle nädala väljaandes toetavad nüüd järgmised üksused kohandatud välju: soodustuse arvutamise sagedus, soodustuse arvutamise määr, soodustuse tüüp, töökalender, pühad töökalendris, palgatsükkel ja töötaja ID-tüübid.

### <a name="leave-mass-enrollment-changing-the-tier-basis-to-seniority-date-doesnt-refresh-the-initial-accrual-rate-318526"></a>Väljumisel hulgiregistreerimisest, tasemealuse "Staaži kuupäev" muutmine ei värskenda algset tekkepõhisuse määra (318526)

Kui hulgiregistreerite töötajad ja muudate taseme alust, kajastub esialgne tekkepõhisus nüüd teie valitud tasemes.

### <a name="workflow-showing-duplicate-place-holders-313636"></a>Töövoog näitab dubleerivaid-järjehoidjaid (313636)

Selles väljaandes tehtud muudatused kõrvaldavad järjehoidjate dubleerimise, kui töövooteatised on saadetud.

### <a name="dimension-fields-arent-updated-when-using-open-in-excel-176261"></a>Dimensioonivälju ei värskendata, kui kasutatakse funktsiooni Ava Excelis (176261)

Selle väljalaskega saate nüüd värskendada finantsdimensiooni, kasutades funktsiooni **Ava Excelis** lehel **Töötaja**. 

### <a name="worker-address-created-in-common-data-service-isnt-synced-to-talent-317555"></a>Common Data Service'is loodud töötaja aadress pole Talentiga sünkroonitud (317555)

Selle muudatusega värskendatakse aadressi, mis on loodud Common Data Service’is rakendusega Talent: Core HR.


## <a name="in-preview"></a>Eelvaates

### <a name="new-page-to-validate-position-hierarchy-data"></a>Uus leht ametikoha hierarhia andmete kinnitamiseks

Personaliosakond (HR) ja administraatorid saavad nüüd kinnitatada juhtimishierarhiat mis tahes ringviidetega, mis võivad olla kogemata imporditud. Sellele uuele leheküljele pääsete, kui lähete **Organisatsiooni haldus > Lingid > Ametikohad > Ametikoha hierarhia kinnitamine**.

### <a name="specify-reason-codes-on-leave-types"></a>Määrake puhkuse tüüpide põhjusekoodid

Organisatsioonid võivad vajada puhkuseavaldustega seotud lisanduvat infot. Nüüd saate määrata puhkuse tüüpidega seotud põhjusekoodid ja lasta töötajatel valida põhjusekood oma puhkuseavaldusele.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Kindlat tüüpi puhkusetüüpidele ja puhkuseavaldustele põhjusekoodide nõudmine

Organisatsioonid võivad nõuda teatud puhkusetüüpide korral töötajate esitatud puhkusetaotluste põhjusekoodide määramist. See nõue võib eksisteerida ettevõtte poliitika või regulatiivsete nõuete tõttu. Nüüd saate määrata, milline puhkusetüüp vajab põhjusekoodi ja saate nõuda, et töötajad esitavad oma puhkuseavaldusel oma puhkusetüübile põhjusekoodi.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Personaliosakonnale puhkuse ja puudumise kannete nimekirja esitamine

Võimalus jägida töötaja puhkuseaega ja mõista, kuidas puhkus on arvestatud, mitte ainult ei aita personaliosakonnal vastata töötajate küsimustele, vaid võimaldab ka töötajatele tagada täpse puhkusehüvitise. Personaliosakonnal on nüüd uus tehingute vaade (hüvitused, viitvõlad, korrigeerimised ja taotlused), et personaliosakond näeks saldode taga olevaid põhjuseid.

## <a name="coming-soon"></a>Peagi tulekul

### <a name="indicate-instance-type-when-provisioning-talent"></a>Näidake eksemplari tüüpi Talenti ettevalmistamisel

Uue Talenti eksemplari ettevalmistamisel saate näidata, kas eksemplari tüüp on **Tootmine** või **Liivakast**, mis võimaldab uute funktsioonide varajast testimist. Kõik olemasolevad Talenti eksemplarid uuendatakse tootmise eksemplari tüübiks. Kui soovite mõne olemasoleva eksemplari värskendada Liivakasti eksemplari tüübiks, võtke muudatuse taotlemiseks ühendust toega.
