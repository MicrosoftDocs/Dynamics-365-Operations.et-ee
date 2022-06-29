---
title: Varaloendurite automaatne värskendamine
description: Selles artiklis kirjeldatakse varahalduses varaloendurite automaatset uuendamist.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8ea84259eb8f12becdcf008ed9222a44b2626a0d
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016213"
---
# <a name="automatic-update-of-asset-counters"></a>Varaloendurite automaatne värskendamine

[!include [banner](../../includes/banner.md)]

Teavet varaloendurite käsitsi registreerimise kohta leiate jaotisest [Varaloendurite käsitsi värskendamine](../work-orders/manual-update-of-asset-counters.md). Teavet varaloendurite häälestamise kohta leiate jaotisest [Loendurid](../setup-for-objects/counters.md).

Loenduri väärtusi saab automaatselt värskendada ka tootmise registreeringutest tootmistundide ja tootmiskoguse (s.t toodetava koguse) alusel. See värskendus tehakse lehel **Varaloendurite värskendamine**. Saate värskendada ühe või mitu vara, määrates ühe parameetri väljal **Kuupäevast**. See parameeter määrab toodangu registreerimiste alguskuupäeva (tootmistunnid või tootmiskogused). Teisisõnu määrab see kuupäeva, millest alates tuleb loenduri väärtusi värskendada.

Kõik varad, mis on seotud ressursiga *ja* millel on varaloendurid, mis on seadistatud värskendamisele tootmistundide või toodangu koguse põhjal, kaasatakse automaatsesse värskendusse. Luuakse uued loenduri väärtused.

Nende loendurite puhul, mis põhinevad toodangu kogusel, hõlmab arv nii õiget kogust kui ka registreeritud veakogust. Kui toodangu koguse registreerimise ühik erineb loenduri kasutatavast ühikust, teisendatakse kogus nii, et see vastaks loenduri ühikule.

Nagu ülal mainitud, saab loenduri väärtuseid automaatselt värskendada tootmise registreeringutest. Seetõttu peab vara, mille kohta soovite automaatse värskenduse loendureid, olema seotud ressursiga (masin). Kui toodetud kogused ja tootmise tunnid on ressursile registreeritud, saate värskendada seotud varaloendureid.

1. Valige **Varahaldus** > **Perioodiline** > **Varad** > **Värskenda varaloendurid**.

2. Valige väljalt **Alguskuupäev** automaatse värskenduse alguskuupäev.

    >[!NOTE]
    >Kuupäev sellel väljal on "poolelioleva töö" kuupäev suvandi **Protsessikanded** (**Tootmise juhtimine** > **Päringud ja aruanded** > **Tootmine** > **Protsessikanded** > väljal **Füüsiline kuupäev**).

3. Kiirkaardil **Kaasatavad kirjed** saate valida kindlad varad, varatüübid või ressursid automaatseks värskendamiseks. Valige **Filter** ja tehke vajalikud valikud.

4. Vahekaardil **Taustal käitamine** saate vastavalt vajadusele seadistada automaatse värskenduse pakett-tööna.

    Alloleval joonisel on esitatud dialoogi **Varaloendurite värskendamine** näide.

    ![Joonis 1.](media/12-work-orders.png)

5. Valige nupp **OK**. 

Pärast seda, kui varaloenduri automaatne värskendamine on tehtud, saate vaadata varaga seotud loenduri registreerimisi lehel **Varaloendurid**. Valige **varahalduse** > **·** > **varad Kõik**, **valige vara ja seejärel valige tegevuspaani vahekaardil Vara** **grupis Ennetusloendurid** **·**.

Lehel **Vara koondväärtus** saate ülevaate viimasest registreeringust, mis on tehtud kõigi varade kõigi loenduritüüpide kohta. Valige **Varahaldus** > **Päringud** > **Varad** > **Vara koondväärtus**. See lehekülg meenutab lehte **Varaloendurid**, kuid registreerimisi ei saa lisada ega redigeerida. See on ainult ülevaate jaoks.

Alloleval joonisel on esitatud lehe **Vara koondväärtus** näide.

![Joonis 2.](media/13-work-orders.png)

Pidage meeles järgmiseid punkte.

- Automaatselt värskendatud loenduritüüpide jaoks saab siiski luua käsitsi loenduri väärtuse registreeringuid. Lisateabe saamiseks vaadake jaotist [Varaloendurite käsitsi värskendamine](../work-orders/manual-update-of-asset-counters.md).

- Saate häälestada loendurid, mis on seotud mõne muu loenduriga. Sel juhul värskendatakse ühe loenduri värskendamisel samaaegselt ka seotud loendureid. Teavet seotud loendurite häälestamise kohta leiate jaotisest [Loendurid](../setup-for-objects/counters.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]