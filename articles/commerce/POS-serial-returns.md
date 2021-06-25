---
title: Tagasta seerianumbriga kontrollitud tooted kassas
description: See teema kirjeldab võimalusi järjestatud kaupade valideerimiseks osana müügikoha rakenduse Microsoft Dynamics 365 Commerce tagastusprotsessist.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7a067994828f3df577c0dc4146d26ac81990d4ac
ms.sourcegitcommit: 927574c77f4883d906e5c7bddf0af9b717e492bf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129803"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a>Tagasta seerianumbriga kontrollitud tooted kassas

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

See teema kirjeldab võimalusi järjestatud kaupade valideerimiseks osana müügikoha rakenduse Microsoft Dynamics 365 Commerce tagastusprotsessist.

> [!NOTE]
> Commerce version 10.0.20 väljalaskes ja hilisemas versioonis on saadaval uus funktsioon nimega **Ühtne tagastuse töötlemise kogemus kassas**. Seerianumbrite valideerimiseks tagastustellimuse töötlemise ajal kassas peate selle funktsiooni sisse lülitama. Teavet teiste võimaluste kohta, mida see funktsioon pakub, kui see on sisse lülitatud, vt [loo tagastused müügikohas](POS-returns.md).
>
> Kui funktsioon on sisse lülitatud, ei saa seda välja lülitada.

## <a name="options-for-validating-serialized-returns"></a>Järjestatud tagastuste kinnitamise suvandid

Kui kassa funktsioon **ühtne tagastustöötluse kogemus** on sisse lülitatud, saavad organisatsioonid kassa kaudu kontrollida seerianumbriga kaupade tagastusi. See võimalus võib hoiatada kasutajaid, kui tagastatav seerianumber erineb algsest müüdud seerianumbrist. Commerce version 10.0.20 väljalaskes ja hilisemas versioonis on teade, mille kasutajad saavad, ainult hoiatusteade. Kasutajad saavad tagastust jätkata seerianumbri suhtes, mis erineb algselt müüdud seerianumbrist.

Organisatsiooni seerianumbri kinnitamise konfigureerimiseks pärast seda, kui kassa funktsiooni **Ühtne tagastustöötluse kogemus** on sisse lülitatud, minge **Jaemüük ja Äri \> Headquarters häälestus \> Parameetrid \> Commerce parameetrid** rakenduses Commerce headquarters. Seadke vahekaardil **Varud** kiirkaardil **Kaupluse lao toimingud** suvandile **Luba müügikohas seerianumbrite valideerimine** väärtuseks **Jah**.

## <a name="process-returns-for-serialized-items-in-pos"></a>Kassas järjestatud kaupade tagastuste protsess

Kui valik **Luba müügikoha tagastuste seerianumbrite valideerimine** on seatud väärtusele **Jah**, kui seerianumbri juhitav kaup tagastatakse müügikoha kaudu, saab kasutaja sisestada tagastusrea seerianumbri lehekülje üksikasjade **tagastatavate toodete** paanile. Kui sisestatud seerianumber ei vasta algsele müügikande seerianumbrile, saab kasutaja hoiatusteate. Rakendus ei takista siiski kasutajal tagastuse sisestamist jätkata.

> [!NOTE]
> Praegu toetab müügikoht seerianumbrite kinnitamist ainult tagastusridadel, kus algne tellitud kogus ei ole suurem kui üks. Kui algne müügitellimuse rida loodi mittekassakanalis ja kui tellitud kogus antud müügireal on rohkem kui üks, ei saa kaupa kassa kaudu õigesti tagastada.

## <a name="additional-resources"></a>Lisaressursid

[Tagastuste loomine müügikohas](POS-returns.md)
