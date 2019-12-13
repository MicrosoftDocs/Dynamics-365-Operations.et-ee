---
title: Päise moodul
description: See teema hõlmab pease mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce luua.
author: anupamar
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d393701dacb88ab03a4b56724d93c794da6bb5c8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697271"
---
# <a name="header-module"></a>Päise moodul

[!include [banner](includes/preview-banner.md)] [!include [banner](includes/banner.md)]

See teema hõlmab pease mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce luua.

## <a name="overview"></a>Ülevaade

Päise moodul on erikonteiner, mida kasutatakse kõigi lehe päises kuvatavate moodulite majutamiseks. Näiteks võib see sisaldada saidi logo, navigeerimishierarhia linke, linke saidi teistele lehtedele ja otsinguriba.

Päise moodul optimeeritakse automaatselt seadmele, millega saiti vaadatakse (s.o töölauga seade või mobiilne seade). Näiteks mobiilses seadmes on navigeerimisriba ahendatud nupule **Menüü** (mida nimetatakse mõnikord ka *hamburgerimenüüks*).

## <a name="properties-of-a-header"></a>Päise atribuudid

Sarnaselt üldistele konteineritele toetavad päise mooduleid **pealkirja** ja **laiuse** atribuute.

Päise moodulil on mitu pesa. Näiteks on olemas pesad teabesõnumi, navigeerimismenüü, logo, otsinguriba, ostukorvi ikooni, soovinimekirja ikooni ja kontoteabe jaoks. Iga pesa toetab kindlat moodulite kogumit.

## <a name="modules-that-are-available-in-a-header-module"></a>Päise moodulis saadaolevad moodulid

Päise moodulis saab kasutada järgmisi mooduleid.

- **Navigeerimismenüü** – navigeerimismenüü tähistab kanali navigeerimishierarhiat ja teisi staatilisi navigeerimislinke. Kanali navigeerimishierarhiat saab konfigureerida rakenduses Dynamics 365 Retail. Konfigureeritud üksused ilmuvad seejärel päise navigeerimises. Lisaks on võimalik konfigureerida staatilisi navigeerimislinke ja sisestada suhtelisi linke teistele e-kaubanduse saidi lehtedele. Päist ennast saab joondada vasakule, paremale või keskele.
- **Ostukorvi ikoon** – ostukorvi ikoon on spetsiaalne ikoon, mis tähistab ostukorvi. See kuvatakse päises ja see näitab ostukorvis olevate kaupade arvu. Ostukorvi ikooniga peab olema kaasas ostukorvi leht, et kliendid oleks võimalik ikooniga suheldes suunata ümber ostukorvi lehele.
- **Soovinimekirja ikoon** – päises kuvatakse soovinimekirja ikoon ja see näitab kliendi soovinimekirja lisatud kaupade arvu. Selle ikooniga peab olema kaasas soovinimekirja leht, et kliendid oleks võimalik ikooniga suheldes suunata ümber soovinimekirja lehele.
- **Sisselogimismoodul** – sisselogimismoodul kuvatakse päises. See võimaldab klientidel oma kontole sisse logida või registreerida konto. Kui klient on juba sisse logitud, saab mooduli konfigureerida kuvama linke konto lehele, tellimuse ajaloo lehele või muule lehele.
- **Logo moodul** – see moodul kuvab jaemüüjat ja kaubamärki esindava logo. See on lingiga pilt. Link on tavaliselt konfigureeritud nii, et sellel on ümbersuunamine kodulehele, seega saavad kliendid kiiresti naasta avalehele mis tahes lehelt.
- **Teatis** – teatis kuvatakse päises ja seda kasutatakse tekstisisese teate kuvamiseks, mis rakendub kõigile saidi lehtedele. Näiteks võib teatis kuvada sõnumi „Iga-aastane allahindlus lõpeb 2 päeva pärast”.
- **Otsinguriba** – otsinguriba võimaldab kasutajatel sisestada otsinguterminid, et otsida tooteid. Moodul peab olema konfigureeritud otsingutulemuste lehe URL-iga. Päringustringi parameetrit saab konfigureerida (vaikeväärtus on **„q”**). Otsinguribal on automaatse soovitamise pesa, kuhu tuleks lisada automaatse soovitamise moodul.
- **Automaatne soovitamine** – automaatse soovitamise moodul kuvab automaatselt soovitatud tulemused. Need tulemused võivad olla võtmesõnad, tooted või kategooriad, kus otsingusõna leitakse.

## <a name="create-a-header-module"></a>Päisemooduli loomine

Päise mooduli loomiseks tehke järgmist.

1. Looge lehekülje fragment, mis sisaldab päise moodulit.
1. Lisage moodulid päise mooduli pesadesse.
1. Uuendage iga mooduli sätteid.
1. Salvestage lehe fragment. 
1. Registreerige leht ja avaldage see.

Päise igal lehel kuvamise tagamiseks järgige neid samme iga malli jaoks, mis on saidi jaoks loodud.

1. Lisage vaikelehel päise moodulit sisaldav lehe fragment peamise pesa päisele.
1. Salvestage mall 
1. Registreerige mall ja avaldage see.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Konteinermoodul](add-container-module.md)

[Ostukasti moodul](add-buy-box.md)

[Ostukorvi moodul](add-cart-module.md)

[Maksmise moodul](add-checkout-module.md)

[Tellimuse kinnituse moodul](order-confirmation-module.md)

[Päise moodul](author-header-module.md)

[Jaluse moodul](author-footer-module.md)
