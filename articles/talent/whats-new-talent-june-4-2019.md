---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 for Talent (4. juuni 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 for Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0a93ad140fb9116ffb0c486b7f3175f90859f125
ms.sourcegitcommit: 7b5ff31c0a82809641beb681510201b942932c74
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/06/2019
ms.locfileid: "1621858"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-june-4-2019"></a>Mis on uut ja mida on muudetud rakenduses Dynamics 365 for Talent (4. juuni 2019)

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse Microsoft Dynamics 365 for Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis

Selles versioonis on väikesed rakenduse Dynamics 365 for Talent: Attract veaparandused.

## <a name="coming-soon-in-attract"></a>Peagi tulekul rakenduses Attract

### <a name="job-approvals-on-the-home-page"></a>Töökinnitused avalehel

Kinnitused kuvatakse armatuurlaua jaotises **Kinnitused**. Kinnitajad saavad oma kinnitusi üle vaadata osas **Teile määratud**. Selles jaotises kuvatakse töö ID, pealkiri, teised kinnitajad ja kuupäev, mil töö määrati. Kasutajad, kes edastavad töö kinnitamiseks, saavad oma töid üle vaadata osas **Teie taotletud**. Selles jaotises kuvatakse kinnitajad, kes peavad edastatud töö veel kinnitama.

## <a name="changes-in-onboard"></a>Muutused Onboardis

Selles versioonis on väikesed rakenduse Dynamics 365 for Talent: Onboard veaparandused.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused

Selles jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2330.

### <a name="new-page-to-validate-position-hierarchy-data"></a>Uus leht ametikoha hierarhia andmete kinnitamiseks

Personaliosakond (HR), personal ja administraatorid saavad kinnitada juhtimishierarhiat mis tahes ringviidetega, mis on kogemata imporditud. Sellele uuele leheküljele pääsete, kui avate **Organisatsiooni haldus \> Lingid \> Ametikohad \> Ametikoha hierarhia kinnitamine**.

### <a name="specify-reason-codes-on-leave-types"></a>Määrake puhkuse tüüpide põhjusekoodid

Organisatsioonid võivad vajada puhkuseavaldustega seotud lisanduvat infot. Nüüd saate määrata puhkuse tüüpidega seotud põhjusekoodid ja lasta töötajatel valida põhjusekood oma puhkuseavaldusele.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Kindlat tüüpi puhkusetüüpidele ja puhkuseavaldustele põhjusekoodide nõudmine

Organisatsioonid võivad nõuda teatud puhkusetüüpide korral töötajate esitatud puhkusetaotluste põhjusekoodide määramist. See nõue võib eksisteerida ettevõtte poliitika või regulatiivsete nõuete tõttu. Saate määrata, milline puhkusetüüp vajab põhjusekoodi, ja saate nõuda, et töötajad esitaksid puhkuseavaldusel oma puhkusetüübile põhjusekoodi.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Personaliosakonnale puhkuse ja puudumise kannete nimekirja esitamine

Võimalus jägida töötaja puhkuseaega ja mõista, kuidas puhkus on arvestatud, aitab personaliosakonnal vastata töötajate küsimustele ja võimaldab ka tagada töötajatele täpse puhkusehüvitise. Personaliosakonnal on nüüd uus tehingute vaade (hüvitused, viitvõlad, korrigeerimised ja taotlused), et personaliosakond näeks puhkuse saldode taga olevaid põhjuseid.

### <a name="deleting-a-record-from-talent-doesnt-remove-the-record-from-common-data-service"></a>Kirje kustutamine Talentist ei eemalda kirjet teenusest Common Data Service

Kirjed, mis eemaldatakse Talent Core HR-ist eemaldatakse nüüd ka Common Data Service'ist.

### <a name="variable-compensation-plan-valid-fromto-dates-arent-being-honored"></a>Ergutussüsteemi plaan kehtib alates/kuni kuupäevi ei austata

Selles väljalaskes ei saa te registreerida töövõtjat ergutussüsteemi plaani, kui alguskuupäev on enne plaani alguskuupäeva või lõppkuupäev on pärast plaani lõppkuupäeva. 

### <a name="performance-review-comments-are-removed-when-users-select-cancel"></a>Tulemuslikkuse hindamise kommentaarid kustutatakse, kui kasutajad valivad Tühista

See väljalase parandab probleemi, kus hindamise kommentaarid eemaldatakse, kui kasutaja hakkab kommentaari muutma, kuid valib seejärel **Tühista**. 

## <a name="in-preview"></a>Eelvaates

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Eelvaate funktsioonid on lubatud ainult liivakasti eksemplarides

Kui valmistate ette uue Talenti eksemplari, saate eksemplari tüübiks määrata **Tootmine** või **Liivakast**. **Liivakasti** tüübi eksemplarid võimaldavad uute funktsioonide varajast katsetamist. Kõik olemasolevad Talenti eksemplarid uuendatakse eksemplari tüübiks **Tootmine**. Kui soovite mõne olemasoleva eksemplari **Liivakasti** tüübile värskendada, võtke muudatuse taotlemiseks ühendust [Toega](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support).

Lisateavet muudatuste avaldamise kohta vt teemast [Talenti ettevalmistamine](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Puhkuse tüüpide piiramine puhkusetaotluste korral

Organisatsioonid võivad töötajatele pakkuda mitut erinevat tüüpi puhkust. Siiski ei pruugi töötajatel olla asjakohane teatud puhkuse tüüpide puhkusetaotluste esitamine. Neid puhkuse tüüpe võib hallata hoopis HR. Selle väljalaskega saate konfigureerida, milliste puhkusetüüpide puhkusetaotluseid töötajad saavad esitada. 

## <a name="coming-soon-in-core-hr"></a>Tulemas Core HR-i

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Halduri iseteeninduses jõudluse lisateabe kuvamine

Uus suvand võimaldab juhtidel vaadata nii oma otseste kui ka kaudsete alluvate jõudlust. Praegu saavad rea haldurid määrata ja uuendada jõudluse eesmärke ja väljastada uusi arvustusi, mida nende töötajad samuti haldavad. Lisaks saavad otsesed juhid ja nende töötajad hallata ja värskendada jõudluse töölehti, mis aitavad tagada sujuva jõudluse ülevaate protsessi. Selle muudatuse rakendamisel saavad juhid vaadata ja hallata lisaks otseste alluvate jõudlusega seotud teabele ka oma kaudsete alluvate jõudlusega seotud teavet. 

### <a name="print-performance-reviews"></a>Jõudluse ülevaadete printimine

Töötajad, juhid ja HR saavad töötaja jõudluse ülevaat välja printida.
