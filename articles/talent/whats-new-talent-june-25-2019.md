---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 Talent (25. juuni 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 06/25/2019
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
ms.search.validFrom: 2019-06-25
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 98ac7df9fa33635814b390427fd3292bdc1175ed
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528641"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-25-2019"></a>Mis on uut ja mida on muudetud rakenduses Dynamics 365 Talent (25. juuni 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Attract.

## <a name="coming-soon-in-attract"></a>Peagi tulekul rakenduses Attract

### <a name="job-approvals-appear-on-the-home-page"></a>Töökinnitused kuvatakse avalehel

Kinnitused kuvatakse armatuurlaua jaotises **Kinnitused**. Kinnitajad saavad kinnitusi üle vaadata jaotises **Teile määratud**, kus kuvatakse töö ID, töö pealkiri, teised kinnitajad ja töö määramise kuupäev. Kasutajad, kes töö kinnitamiseks esitavad, saavad oma töid üle vaadata jaotises **Teie taotletud**, mis kuvab kinnitajaid, kes peavad edastatud tööd veel kinnitama.

## <a name="changes-in-onboard"></a>Muutused Onboardis
See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused

Jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2357.

### <a name="incorrect-value-displayed-for-primary-position-314266"></a>Peamise positsiooni puhul kuvatakse vale väärtus (314266)

Need muudatused kuvavad järjepidevalt kõigil lehtedel **Peamise positsiooni** sätteid.

### <a name="cant-edit-after-recalling-the-workflow-in-review-318180"></a>Ei saa redigeerida pärast ülevaates töövoo tagasikutsumist (318180)

Töövoo kaudu tagasikutsutud ülevaateid saab nüüd redigeerida.

### <a name="final-comments-field-in-reviews-isnt-translated-325921"></a>Ülevaatamiste lõppkommentaaride välja ei tõlgita (325921)

Talentis tõlgitakse **Lõppkommentaaride** silt.

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>Eelvaatefunktsioonid on lubatud ainult liivakastikeskkondades

Kui valmistate ette uue Talenti eksemplari, saate eksemplari tüübiks määrata **Tootmine** või **Liivakast**. **Liivakasti** eksemplari tüüp lubab uute funktsioonide varajast katsetamist. Kõik olemasolevad Talenti eksemplarid uuendatakse eksemplari tüübiks **Tootmine**. Kui soovite mõne olemasoleva eksemplari **Liivakasti** tüübile värskendada, võtke muudatuse taotlemiseks ühendust [Toega](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support).

Lisateavet muudatuste avaldamise kohta vt teemast [Talenti ettevalmistamine](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

## <a name="in-preview"></a>Eelvaates

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Puhkuse tüüpide piiramine puhkusetaotluste korral

Organisatsioonid saavad töötajatele pakkuda mitut tüüpi puhkust. Siiski ei pruugi töötajatel olla asjakohane teatud puhkuse tüüpide puhkusetaotluste esitamine. Neid puhkuse tüüpe võib hallata hoopis pesonaliosakond (HR). Selle väljalaskega saate konfigureerida, milliste puhkusetüüpide puhkusetaotluseid töötajad saavad esitada. 

## <a name="coming-soon-in-core-hr"></a>Tulemas Core HR-i

### <a name="feature-management-area-in-talent"></a>Funktsioonihalduse ala Talentis

**Funktsioonihaldus** eemaldatakse **Süsteemihaldusest** selle funktsiooni probleemide tõttu. Tutvustame **Funktsioonihaldust** uuesti tulevases väljalaskes. 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service'i üksuse tugi kohandatud väljadele

Järgmised üksused toetavad kohandatud välju: **Palga tulukood**, **Fikseeritud kompensatsiooni sündmus**, **Kompensatsiooni ruudustik**, **Makseperiood** ja **Kompensatsiooni viitepunkt**. 

### <a name="new-common-data-service-entities"></a>Uued Common Data Service'i üksused

Common Data Service'ile lisatakse **Põhjuskoodide** üksus.

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Halduri iseteeninduses otseste ja kaudsete alluvate jõudluse teabe kuvamine

Uus suvand võimaldab juhtidel vaadata nii oma otseste kui ka kaudsete alluvate jõudlust. Praegu saavad rea haldurid määrata ja uuendada jõudluse eesmärke ja väljastada uusi arvustusi. Lisaks saavad otsesed juhid ja nende töötajad hallata ja värskendada jõudluse töölehti, mis aitavad tagada sujuva jõudluse ülevaate protsessi. Selle muudatuse rakendamisel saavad juhid vaadata ja hallata lisaks otseste alluvate jõudlusega seotud teabele ka oma kaudsete alluvate jõudlusega seotud teavet.

### <a name="print-performance-reviews"></a>Jõudluse ülevaadete printimine

Töötajad, juhid ja HR saavad töötaja jõudluse ülevaat välja printida.
