---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 for Talent (11. juuni 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 for Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 06/11/2019
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
ms.search.validFrom: 2019-06-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 42b9541b152d2a6daa1dbf95ecf30a2f51eb36f3
ms.sourcegitcommit: 31a918d357a7182f3870713a9c4455bd5c44cd58
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/18/2019
ms.locfileid: "1634476"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-june-11-2019"></a>Mis on uut ja mida on muudetud rakenduses Dynamics 365 for Talent (11. juuni 2019)

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse Microsoft Dynamics 365 for Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis

### <a name="search-engine-optimization-for-job-posts"></a>Otsingumootori optimeerimine töökuulutuste jaoks

Kui lülitate Dynamics 365 for Talent: Attracti halduskeskuses sisse **Otsingumootori optimeerimise**, teavitab Attract Google'i indekseerimise rakendusliidest (API), et see sirviks veebilehte iga kord kui aktiveerite ja postitate uue töö või värskendate olemasolevat. Sel viisil kuvatakse töökuulutus Google'i ja teiste otsingumootorite otsingutulemustes.

Samuti, kui võitate töökuulutuse maha, teavitab Attract indekseerimise API-t, et mahavõetud töökuulutust ei kuvataks otsingutulemustes.

> [!NOTE]
> Veebiämblik ei ole määratud ajavahemikku veebilehtede sirvimiseks ega otsingutulemuste värskendamiseks.

## <a name="coming-soon-in-attract"></a>Peagi tulekul rakenduses Attract

### <a name="job-approvals-appear-on-the-home-page"></a>Töökinnitused kuvatakse avalehel

Kinnitused kuvatakse armatuurlaua jaotises **Kinnitused**. Kinnitajad saavad kinnitusi üle vaadata jaotises **Teile määratud**, kus kuvatakse töö ID, töö pealkiri, teised kinnitajad ja töö määramise kuupäev. Kasutajad, kes töö kinnitamiseks esitavad, saavad oma töid üle vaadata jaotises **Teie taotletud**, mis kuvab kinnitajaid, kes peavad edastatud tööd veel kinnitama.

## <a name="changes-in-onboard"></a>Muutused Onboardis

Selles versioonis on väikesed rakenduse Dynamics 365 for Talent: Onboard veaparandused.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused

Selles jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2337.

### <a name="platform-update-27"></a>Platvormivärskendus update 27

Platvormivärskenduse 27 kohta lisainfo saamiseks vt [Dynamics 365 for Finance and Operations platvormivärskenduse 27 (juuni 2019) funktsioonide eelvaade](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27).

### <a name="feature-management-workspace-in-talent"></a>Funktsioonihalduse tööruum Talentis

**Funktsioonihalduse** tööruum **Süsteemihalduses** võimaldab teil vaadata, lubada, keelata ja planeerida igas väljalaskes toodud funktsioone. Vaikimisi on uued funktsioonid välja lülitatud. Saate kasutada **Funktsioonihalduse** tööruumi funktsioonide sisselülitamiseks ja nende dokumentatsiooni vaatamiseks.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service'i üksuse tugi kohandatud väljadele

Väljastava asutuse üksus toetab nüüd kohandatud välju.

### <a name="new-common-data-service-entities"></a>Uued Common Data Service'i üksused

Lisatud on ülesandegrupi üksus.

## <a name="in-preview"></a>Eelvaates

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>Eelvaatefunktsioonid on lubatud ainult liivakastikeskkondades

Lisateavet muudatuste avaldamise kohta vt teemast [Talenti ettevalmistamine](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).

Kui valmistate ette uue Talenti eksemplari, saate eksemplari tüübiks määrata Tootmine või Liivakast. Liivakasti eksemplari tüüp lubab uute funktsioonide varajast katsetamist. Kõik olemasolevad Talenti eksemplarid uuendatakse eksemplari tüübiks **Tootmine**. Kui soovite mõne olemasoleva eksemplari **Liivakasti** tüübile värskendada, võtke muudatuse taotlemiseks ühendust [Toega](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/talent-support).

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Puhkuse tüüpide piiramine puhkusetaotluste korral

Organisatsioonid saavad töötajatele pakkuda mitut tüüpi puhkust. Siiski ei pruugi töötajatel olla asjakohane teatud puhkuse tüüpide puhkusetaotluste esitamine. Neid puhkuse tüüpe võib hallata hoopis pesonaliosakond (HR). Selle väljalaskega saate konfigureerida, milliste puhkusetüüpide puhkusetaotluseid töötajad saavad esitada. 

## <a name="coming-soon-in-core-hr"></a>Tulemas Core HR-i

### <a name="view-extended-information-about-report-performance-in-manager-self-service"></a>Halduri iseteeninduses alluvate jõudluse lisateabe kuvamine

Uus suvand võimaldab juhtidel vaadata nii oma otseste kui ka kaudsete alluvate jõudlust. Praegu saavad rea haldurid määrata ja uuendada jõudluse eesmärke ja väljastada uusi arvustusi. Lisaks saavad otsesed juhid ja nende töötajad hallata ja värskendada jõudluse töölehti, mis aitavad tagada sujuva jõudluse ülevaate protsessi. Selle muudatuse rakendamisel saavad juhid vaadata ja hallata lisaks otseste alluvate jõudlusega seotud teabele ka oma kaudsete alluvate jõudlusega seotud teavet.

### <a name="print-performance-reviews"></a>Jõudluse ülevaadete printimine

Töötajad, juhid ja HR saavad töötaja jõudluse ülevaat välja printida.
