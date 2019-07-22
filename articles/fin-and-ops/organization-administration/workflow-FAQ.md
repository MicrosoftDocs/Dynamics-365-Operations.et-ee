---
title: Töövoo KKK
description: Teemas on toodud vastused korduma kippuvatele küsimustele rakenduse Microsoft Dynamics 365 for Finance and Operations töövoo süsteemi kohta.
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adcc9bbc422a3fddfd51d248daf95c0da6d4c9bb
ms.sourcegitcommit: 8cf77e9171d6cad8ae6c8bfad9e4f9a46fef6d23
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/19/2019
ms.locfileid: "1688996"
---
# <a name="workflow-faq"></a>Töövoo KKK

[!include [banner](../includes/banner.md)]

Teemas on toodud vastused korduma kippuvatele küsimustele rakenduse Microsoft Dynamics 365 for Finance and Operations töövoo süsteemi kohta.

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Miks võetakse tööüksuse tagasilükkamisel vastu mitu teatist?
Tööüksuse tagasilükkamisel viiakse see tööüksus tagasilükatuna lõpuni. Algatajale luuakse ja määratakse teine tööüksus. See tähendab, et algataja saab teatise tagasilükatud tööüksuse kohta ja kasutaja, kellele määrati uus „taotletakse muudatust” tööüksus, saab eraldi teatise. 

Iga teatis on erineva tööüksuse jaoks, kuid nende sarnasus võib põhjustada segadust. Otsime võimalusi selle tulevases väljaandes parandamiseks.

## <a name="why-are-my-workflow-exports-failing"></a>Miks minu töövoo eksport nurjub?
Praegu on töövoo ekspordi funktsioonil piirang, milles töövoo nimede pikkus ei tohi ületada 48 märki. Kasutades nime, mis on pikem kui 48 märki võib põhjustada tõrke "Server ei saanud taotlust autentida" ja/või takistada faili eksportimist failitüübita. Järgmine ajaveebipostitus sisaldab üksikasju [Töövoo ekspordi tõrkeotsingu](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting) kohta.

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>Kas töövoo edastaja saab töövoo ka kinnitada?
Jah, töövoo eedastaja saab töövoo ka kinnitada, kui see on nii konfigureeritud. Selle käitumise vältimiseks seadistage **Töövoo parameetrid > Üldine > Kinnitaja > Keela edastaja tehtud kinnitamine** olekule **Jah**.

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>Kas ma saan töövoogudele märguandeid lisada, et kasutajatele teatiseid edastada?
Siin on mõned asjad, millele teatsite edastamiseks töövoogudele märguandeid lisades tähelepanu pöörata.
- Märguanded versus töövoo teatiste mehhanismid
    - Märguandeid saab seadistada kirje muudatustele. Töövood muudavad kirjeid, nii et võimalik on seadistada töövoo põhjustatud kirje muudatuse märguanne. Kuid kuna töövoogudel on erinevad sisse-ehitatud teatiste võimalused, ei ole märguannete kasutamine parim variant.
- Standardsed teatised töövoogudelt 
    - Töövoogudel on sisse-ehitatud e-posti teatised. Klient saab konfigureerida teatiseid nii, et kasutajatele saadetakse e-kirjad. Need teatised ei edasta kasutajatele tegevuskeskuse teateid.
    - Tulevases uuenduses lisame tegevuskeskuse teate, nii et kasutajale määratakse töövoo tööüksus. 
- Teatiste töövoogudesse lisamine
    - Tegevuskeskuse teateid saab luua kindlatele kasutajatele, nt töövoost X++ loodud sõnum.
    - [Töövoogudel on ärisündmused](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow), mida klient saab kasutada Flowsi käivitamiseks, et saada nende otsitavad teatised.   

Kokkuvõttes, kui kasutaja ei saa töövoo tööüksuse määramisel tegevuskeskusest nõuetekohast teatist, kasutage ära [Töövoo ärisündmuseid](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) koos Microsoft Flow'ga, et pakkuda täiendavad või muid teatiseid.
