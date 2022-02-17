---
title: Töövoo KKK
description: Teemas on toodud vastused korduma kippuvatele küsimustele töövoo süsteemi kohta.
author: ChrisGarty
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fe11942ca41dd8c0ca23d94006569c50a4501a52
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065576"
---
# <a name="workflow-faq"></a>Töövoo KKK

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Teemas on toodud vastused korduma kippuvatele küsimustele töövoo süsteemi kohta.

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Miks võetakse tööüksuse tagasilükkamisel vastu mitu teatist?
Tööüksuse tagasilükkamisel viiakse see tööüksus tagasilükatuna lõpuni. Algatajale luuakse ja määratakse teine tööüksus. See tähendab, et algataja saab teatise tagasilükatud tööüksuse kohta ja kasutaja, kellele määrati uus „taotletakse muudatust” tööüksus, saab eraldi teatise. 

Iga teatis on erineva tööüksuse jaoks, kuid nende sarnasus võib põhjustada segadust. Otsime võimalusi selle tulevases väljaandes parandamiseks.

## <a name="why-are-my-workflow-exports-failing"></a>Miks minu töövoo eksport nurjub?
Praegu on töövoo ekspordi funktsioonil piirang, milles töövoo nimede pikkus ei tohi ületada 48 märki. Kasutades nime, mis on pikem kui 48 märki võib põhjustada tõrke "Server ei saanud taotlust autentida" ja/või takistada faili eksportimist failitüübita. Järgmine ajaveebipostitus sisaldab üksikasju [Töövoo ekspordi tõrkeotsingu](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting) kohta.

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>Kas töövoo edastaja saab töövoo ka kinnitada?
Jah, töövoo eedastaja saab töövoo ka kinnitada, kui see on nii konfigureeritud. Selle käitumise vältimiseks seadistage **Süsteemihaldus > Töövoog > Töövoo parameetrid > Üldine > Kinnitaja > Keela edastaja tehtud kinnitamine** olekule **Jah**.

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>Kas ma saan töövoogudele märguandeid lisada, et kasutajatele teatiseid edastada?
Siin on mõned asjad, millele teatsite edastamiseks töövoogudele märguandeid lisades tähelepanu pöörata.
- Märguanded versus töövoo teatiste mehhanismid
    - Märguandeid saab seadistada kirje muudatustele. Töövood muudavad kirjeid, nii et võimalik on seadistada töövoo põhjustatud kirje muudatuse märguanne. Kuid kuna töövoogudel on erinevad sisse-ehitatud teatiste võimalused, ei ole märguannete kasutamine parim variant.
- Standardsed teatised töövoogudelt 
    - Töövoogudel on sisse-ehitatud e-posti teatised. Klient saab konfigureerida teatiseid nii, et kasutajatele saadetakse e-kirjad. Need teatised ei edasta kasutajatele tegevuskeskuse teateid.
    - Tulevases uuenduses lisame tegevuskeskuse teate, nii et kasutajale määratakse töövoo tööüksus. 
- Teatiste töövoogudesse lisamine
    - Tegevuskeskuse teateid saab luua kindlatele kasutajatele, nt töövoost X++ loodud sõnum.
    - [Töövoogudel on ärisündmused](../../dev-itpro/business-events/business-events-workflow.md), mida klient saab kasutada Flowsi käivitamiseks, et saada nende otsitavad teatised.   

Kokkuvõttes, kui kasutaja ei saa töövoo tööüksuse määramisel tegevuskeskusest nõuetekohast teatist, kasutage ära [Töövoo ärisündmuseid](../../dev-itpro/business-events/business-events-workflow.md) koos Microsoft Power Automate'ga, et pakkuda täiendavad või muid teatiseid.

## <a name="why-is-workflow-editor-not-able-to-start-under-ad-fs"></a>Miks ei saa töövoo redaktor AD FS-i all käivituda?
Täiendatud keskkonnas teenuse Active Directory Federation Services (AD FS) all töötamisel võib töövoo redaktoril olla probleeme alustamisega. Kui jah, veenduge, et URL https://dynamicsaxworkfloweditor/ oleks ADFS-i sätetes lisatud atribuudile **Microsoft Dynamics 365 for Operations kohapeal – Töövoog – Omarakendus**.

## <a name="why-am-i-getting-sql-deadlocks-on-workflow-processing"></a>Miks ma saan töövoo töötlemisel SQL-i tupikuid? 
Vaikimisi välja väärtus suvandile **Töövoo üksuste arv partii kohta** lehel **Töövoo parameetrid** on 0. Väärtus 0 põhjustab vaikeväärtusel muuta 20 üksuseks partii kohta. Olge selle väärtuse kohandamisel ettevaatlik, kuna kaupade suur arv partii kohta (> 40) võib põhjustada SQL-i tupikuid.

## <a name="what-is-the-workflow-enhanced-error-feature"></a>Mis on töövoo täiustatud tõrgete funktsioon?
Töövoo täiustatud tõrgete funktsiooni versioonis 10.0.13 lisati tõrkekoodid, et eristada töövootõrgete eri klasse. Kuvatavad tõrketeated on enamasti tuttavad, välja arvatud väikeste erinevuste poolest, et neid selgemaks teha.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
