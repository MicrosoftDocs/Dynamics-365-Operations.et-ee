---
title: Varaloendurite automaatne värskendus
description: Selles teemas kirjeldatakse varaloendurite automaatset värskendust varahalduses.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9911d5b96bb58b5def3e7dfee0f36826d99f6ba1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263682"
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

    ![Joonis 1](media/12-work-orders.png)

5. Valige nupp **OK**. 

Pärast seda, kui varaloenduri automaatne värskendamine on tehtud, saate vaadata varaga seotud loenduri registreerimisi lehel **Varaloendurid**. Valige **Varahaldus** > **Üldine** > **Varad** > **Kõik varad**, valige vara ja seejärel valige toimingupaani vahekaardil **Vara** grupist **Ennetav** üksus **Loendurid**.

Lehel **Vara koondväärtus** saate ülevaate viimasest registreeringust, mis on tehtud kõigi varade kõigi loenduritüüpide kohta. Valige **Varahaldus** > **Päringud** > **Varad** > **Vara koondväärtus**. See lehekülg meenutab lehte **Varaloendurid**, kuid registreerimisi ei saa lisada ega redigeerida. See on ainult ülevaate jaoks.

Alloleval joonisel on esitatud lehe **Vara koondväärtus** näide.

![Joonis 2](media/13-work-orders.png)

Pidage meeles järgmiseid punkte.

- Automaatselt värskendatud loenduritüüpide jaoks saab siiski luua käsitsi loenduri väärtuse registreeringuid. Lisateabe saamiseks vaadake jaotist [Varaloendurite käsitsi värskendamine](../work-orders/manual-update-of-asset-counters.md).

- Saate häälestada loendurid, mis on seotud mõne muu loenduriga. Sel juhul värskendatakse ühe loenduri värskendamisel samaaegselt ka seotud loendureid. Teavet seotud loendurite häälestamise kohta leiate jaotisest [Loendurid](../setup-for-objects/counters.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]