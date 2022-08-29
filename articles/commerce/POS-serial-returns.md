---
title: Tagasta seerianumbriga kontrollitud tooted kassas
description: See artikkel kirjeldab võimalusi seeriaks jaotatud Microsoft Dynamics 365 Commerce kaupade kinnitamise võimalusena müügikoha rakenduse tagastusprotsessi osana.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9fa7e47b6d650370afe4b98d7eca01253bd1bc36
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268470"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a>Tagasta seerianumbriga kontrollitud tooted kassas

[!include [banner](includes/banner.md)]

See artikkel kirjeldab võimalusi seeriaks jaotatud Microsoft Dynamics 365 Commerce kaupade kinnitamise võimalusena müügikoha rakenduse tagastusprotsessi osana.

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
