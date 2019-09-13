---
title: Varaloendurite automaatne värskendus
description: Selles teemas kirjeldatakse varaloendurite automaatset värskendust varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875616"
---
# <a name="automatic-update-of-asset-counters"></a>Varaloendurite automaatne värskendus

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Eelmises jaotises kirjeldatakse varaloendurite käsitsi registreerimist. Varaloendurite seadistamist kirjeldatakse jaotises [Loendurid](../setup-for-objects/counters.md).

Loenduri väärtuseid saab automaatselt värskendada ka tootmise registreeringutest tootmise tundide ja tootmise koguse alusel. Seda saab teha suvandis **Värskenda varaloendurid**. Saate värskendada ühe või mitu vara, sisestades ühe parameetri väljal **Kuupäevast**. See parameeter määratleb tootmise registreeringute (tundide või toodetud koguse kohta) alguskuupäeva, mis tähendab alguskuupäeva, millest alates peaks loenduri väärtusi värskendama.

Kõik varad, mis on seotud ressursiga *ja* millel on varaloendurid, mis on seadistatud värskendusele toodetud koguse või tootmise tundide põhjal, kaastakse automaatsesse värskendusse ja luuakse uued loenduri väärtused.

Tootmiskogusel põhinevate loendurite puhul kaasatakse loendusse nii registreeritud õige kogus kui ka veakogus. Kui toodetud koguse registreerimise ühik erineb loenduri kasutatavast ühikust, teisendatakse kogus, et see vastaks loenduri ühikule.

Nagu ülal mainitud, saab loenduri väärtuseid automaatselt värskendada tootmise registreeringutest. Seetõttu peab vara, mille kohta soovite automaatse värskenduse loendureid, olema seotud ressursiga (masin). Järgnevad kirjeldused annavad tootmistellimuste seadistamise ja töötlemise kohta ülevaate (moodulis **Tootmise juhtimine**), mida kasutatakse vara loendurite automaatse värskendamise alusena moodulis **Varahaldus**.

Kui toodetud kogused ja tootmise tunnid on ressursile registreeritud, saate värskendada seotud varaloendureid.

1. Klõpsake **Varahaldus** > **Perioodiline** > **Varad** > **Värskenda varaloendurid**.

2. Valige väljalt **Alguskuupäev** automaatse värskenduse alguskuupäev.

>[!NOTE]
>Kuupäev sellel väljal on "poolelioleva töö" kuupäev suvandi **Protsessikanded** (**Tootmise juhtimine** > **Päringud ja aruanded** > **Tootmine** > **Protsessikanded** > väljal **Füüsiline kuupäev**).

3. Kui soovite automaatse värskenduse jaoks valida konkreetseid varasid, vara tüüpe või ressursse, klõpsake vahekaardil **Kaasatavad kirjed** nuppu **Filtreeri** ja tehke sobivad valikud.

4. Vajadusel saate seadistada automaatse värskenduse pakett-tööna kiirkaardil **Taustal käitamine**.

![Joonis 1](media/12-work-orders.png)

5. Klõpsake valikut **OK**. Kui automaatne vara loenduri värskendus on tehtud, näete varaga seotud loenduri registreeringuid lehel **Varaloendurid** (**Varahaldus** > **Ühine** > **Varad** > **Kõik varad** > vali vara > nupul **Loendurid**).

Lehel **Varaloenduri kokkuvõte** saate ülevaate viimastest registreeringutest, mis on tehtud kõigi loenduri tüüpide kohta kõigile varadele. Klõpsake **Varahaldus** > **Päringud** > **Varad** > **Vara koondväärtus**. See vaade on väga sarnane lehe **Varaloendurid** vaatega, kui lehel **Vara koondväärtus** ei saa lisada registreeringuid ega neid redigeerida. See on ainult ülevaate jaoks.

![Joonis 2](media/13-work-orders.png)


- Automaatselt värskendatud loenduri tüüpide jaoks on siiski võimalik luua käsitsi loenduri väärtuse registreeringuid. Lisateabe saamiseks vaadake jaotist "Varaloendurite käsitsi värskendamine".
- Saate luua teise loenduriga seotud loendureid, mis tähendab seda, et loenduri värskendamisel värskendatakse samal ajal automaatselt ka seotud loendurid. Seotud loendurite seadistamiseks vaadake jaotist [Loendurid](../setup-for-objects/counters.md).
