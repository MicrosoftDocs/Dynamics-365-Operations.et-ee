---
title: Mooduliteegi ülevaade
description: See artikkel sisaldab mooduliteegi Microsoft Dynamics 365 Commerce ülevaadet.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d9dc07b3f6417c7e284c6555c2818c2a782d7683
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268942"
---
# <a name="module-library-overview"></a>Mooduliteegi ülevaade

[!include [banner](includes/banner.md)]

See artikkel sisaldab mooduliteegi Microsoft Dynamics 365 Commerce ülevaadet.

Rakenduse Dynamics 365 Commerce mooduliteek on moodulikogum, mida saab kasutada e-kaubanduse veebisaidi loomiseks. Moodulitel on nii kasutajaliidese (UI) kui ka funktsionaalse käitumise aspektid.

Mooduliteegis olevatele moodulitele saab rakendada kujundusi, et muuta nende välimust ja olemust. Kujundused kasutavad kaskaadlaadistikke (CSS). Mooduliteegis on fiktiivse e-kaubanduse saidi Fabrikam kujundus, mida võib kasutada mallina.

## <a name="module-library-modules"></a>Mooduliteegi moodulid

Mooduliteegis on järgmist tüüpi moodulid.

- **Konteineri moodul** – konteineri moodul on lihtne moodul, mis toimib teiste moodulite hostina. See kontrollib selle sees olevate moodulite paigutust.
- **Turundusmoodulid** – turundusmoodulid sisaldavad sisubloki, tekstibloki, videopleieri ja karusselli mooduleid. Kõiki neid mooduleid võib kasutada sisu tutvustamiseks. Neid saab panna igale lehele ja need põhinevad sisuhaldussüsteemi (CMS) andmetel.
- **Päise ja jaluse moodulid** – päise ja jaluse moodulid ilmuvad kõikide saidi lehtede päistes ja jalustes. Neid mooduleid saab atribuutide kaudu vajaduse järgi konfigureerida.
- **Otsingumoodulid** – tooteid saab leida, kasutades päises otsingumoodulit. Otsingutulemused kuvatakse otsingutulemuste lehel. Tooteid saab leida ka kategoorialehtedelt, mis on kanali navigeerimishierarhias toetatud iga kategooria erilehed. Peale selle saab kasutada piiritlusmooduleid, et veelgi filtreerida otsingutulemusi otsingutulemuste ja kategoorialehel.
- **Toote üksikasjade lehe moodulid** – toote üksikasjade lehel kasutatakse mitut moodulit tooteteabe kuvamiseks. Ostukastimoodulis saavad kasutajad vaadata tooteid ja lisada neid ostukorvi. Muud moodulid, nt tehniliste andmete moodul, kuvavad toote üksikasjad. Hinnangute ja arvustuste moodulit saab kasutada arvustuste vaatamiseks ja esitamiseks.
- **Veebist ostmise ja kauplusest kättesaamise moodul** – veebist ostmise ja kauplusest kättesaamise moodul on integreeritud Bingi kaartidesse. Seda saab kasutada lähedalasuvate poodide leidmiseks, kuhu kliendid saavad ostetud toodetele järele minna.
- **Ostumoodulid** – ostumoodulid sisaldavad ostukorvimoodulit, mida saab kasutada kaupade lisamiseks ostukorvi. Väljaregistreerimismoodul jäädvustab tarneaadressi, tarnevalikud ja kinkekaardi, püsikliendi programmi ning krediitkaardi teabe, et tellimust saaks töödelda. Pärast tellimuse esitamist saab kasutada tellimuse kinnituse moodulit, et kuvada kinnituse üksikasjad.
- **Kontohaldusmoodulid** – sisselogimismoodul laseb klientidel sisse logida olemasolevale kontole ja registreerimismoodul laseb luua uue konto. Pärast konto loomist saab hiljutiste tellimuste vaatamiseks kasutada tellimuse ajaloo moodulit ja tellimuse üksikasjade moodulit saab kasutada tellimuse üksikasjade vaatamiseks.
- **Soovituste moodul** – soovitused kuvatakse, kasutades toote paigutamise moodulit. See moodul toetab algoritmilisi ja toimetusloendeid, mida saab tutvustada mis tahes lehel.

## <a name="additional-resources"></a>Lisaressursid

[Konteineri moodul](add-container-module.md)

[Ostukastimoodul](add-buy-box.md)

[Ostukorvimoodul](add-cart-module.md)

[Väljaregistreerimismoodul](add-checkout-module.md)

[Tellimuse kinnituse moodul](order-confirmation-module.md)

[Päise moodul](author-header-module.md)

[Jaluse moodul](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
