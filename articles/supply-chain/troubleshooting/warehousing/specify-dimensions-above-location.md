---
title: Osalise koguse koormust ei saa väljastada partiiülese reserveerimishierarhiaga
description: Kui kasutate kaupa reserveerimishierarhiaga partii kohal, peavad koormaread määrama dimensioonid asukohast ülalpool, et varusid eraldada.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eb7e71cc271903cb689c33777b72862246f2dd42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476095"
---
# <a name="cant-release-a-load-for-partial-quantity-with-batch-above-reservation-hierarchy"></a>Osalise koguse koormust ei saa väljastada partiiülese reserveerimishierarhiaga

## <a name="symptoms"></a>Sümptomid

Kui kasutate kaupa, millel on *partii eespool* broneerimise hierarhia, ei tööta lehekülje **Koormuse planeerimise töökoht** käsk **Väljasta laole**, kui üritada väljastada koormat osalise kogusega. Sellisel juhul kuvatakse järgnev veateade:

> Kuvatakse järgmine tõrketeade: "Kui soovite määrata voo, peavad koorma read määrama dimensioonid asukoha kohal. Nende dimensioonide määramiseks broneerige ja looge uuesti koorma rida.

Kui aga kasutate kaupa, millel on *partii allpool* broneerimise hierarhia, saate väljastada osalise kogusega koormat lehelt **Koormuse planeerimise töökoht**.

## <a name="cause"></a>Põhjus

Kui broneerimise hierarhias on dimensioon **Asukoha** dimensioonist ettepool, peab see olema määratud enne lattu väljastamist. Laovarusid saab edukalt eraldada ainult juhul, kui asukohaülestes dimensioonides ei ole erinevusi.

## <a name="resolution"></a>Lahendus

Veenduge, et ülal kõik **asukoha** dimensioonid on määratud koormarea reserveerimise ja uuestiloomise abil.
