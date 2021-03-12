---
title: Järeletulemisteabe moodul
description: See teema hõlmab järeletulemisteabe moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce maksmise lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d04e2650f9c601d008ebf19080059b70416d7917
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000605"
---
# <a name="pickup-information-module"></a>Järeletulemise teabe moodul

[!include [banner](includes/banner.md)]

See teema hõlmab järeletulemisteabe moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce maksmise lehtedele lisada.

Järeletulemisteabe moodulit saab kasutada maksmise moodulis tellimusele järele tulemise teabe näitamiseks. Kliendid saavad vaadata saadaolevaid järeletulemiskuupäevi ja -aegu ning seejärel valida tellimusele järeletulemiseks sobiva aja. Näiteks saab klient valida, et tuleb San Francisco poodi tellimusele järele 21. märtsil kell 15.00.

Sobivate poodide järeletulemise ajavahemik peab olema konfigureeritud Commerce'i peakontoris. Lisateavet vt teemast [Kliendi järeletulemise ajavahemike loomine ja värskendamine](dev-itpro/pickup-timeslots.md).

Kui järeletulemisteabe moodul luuakse maksmise lehel, kuid pealevõtmiseks valitud poele ei ole määratud ajavahemikke, näitab moodul teavet, kuid kasutaja ei saa valida ühtegi ajavahemikku. Ajavahemikud on valikulised ja neid ei nõuta tellimuse tegemiseks.

Kui mitmele kaubale tullakse järele mitmesse poodi, võimaldab järeletulemisteabe moodul kasutajal valida iga kaupluse jaoks ajavahemiku tingimusel, et selle jaoks on saadaval ajavahemikud.

> [!NOTE]
> Ajavahemikue ja maksmisel järeletulemisteabe mooduli tugi on saadaval Dynamics 365 Commerce'i versioonis 10.0.15 ja uuemates versioonides.

Järgmisel joonisel on kujutatud ajavahemiku valiku näide maksmise lehel järeletulemisteabe mooduli kaudu.

![Järeletulemisteabe mooduli näide maksmise lehel](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a>Mooduli atribuudid

- **Pealkiri** – sisestage mooduli pealkiri.

## <a name="show-time-slot-information-after-an-order-is-placed"></a>Ajavahemikuteabe kuvamine tellimuse esitamise järel

Pärast tellimuse esitamist saab valitud ajavahemiku teavet vaadata [tellimuse kinnitamise moodulis](order-confirmation-module.md) ja [tellimuse üksikasjade moodulis](account-management.md#order-details-page). Mõlemal moodulil on atribuut **Ajavahemiku teabe kuvamine**. Enne valitud ajavahemiku kuvamist tellimise ajal peab selle atribuudi väärtuseks olema seatud **Tõene**.

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a>Maksmise lehele järeletulemisteabe mooduli lisamine

Juhiste saamiseks järeletulemisteabe mooduli lisamiseks maksmise lehele ja nõutavate atribuutide määramiseks vt teemat [Maksmismoodul](add-checkout-module.md).

Järgmisel joonisel on kujutatud näide e-kaubanduse maksmise lehest, mis sisaldab reaüksuste jaoks järeletulemise ajavahemikke.

![Näide e-kaubanduse maksmise lehest, mis sisaldab reaüksuste jaoks järeletulemise ajavahemikke](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a>Lisaressursid

[Kliendi järeletulemise ajavahemike loomine ja värskendamine](dev-itpro/pickup-timeslots.md)

[Maksmismoodul](add-checkout-module.md)

[Tellimuse kinnituse moodul](order-confirmation-module.md)

[Tellimuse üksikasjade moodul](account-management.md)
