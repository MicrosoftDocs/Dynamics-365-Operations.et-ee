---
title: Automaatse reserveerimise viip kuvatakse koos saadaoleva laoseisuga
description: Kui kasutate laos kaupa, mis pole laoprotsessides lubatud, ei kuvata automaatse reserveerimise viipa. Määrake kõik dimensioonid asukoha kohal.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a15502ce8c5bc61d37cedd746985176408a2f362
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476157"
---
# <a name="auto-reservation-prompt-for-batch-number-is-shown-even-with-available-inventory"></a>Automaatse reserveerimise viip kuvatakse koos saadaoleva laoseisuga

## <a name="symptoms"></a>Sümptomid

Kui kasutate kaupa, mille reserveerimishierarhia on laos *partiiülene*, kus pole lubatud laoprotsessid ja automaatne reserveerimine on lubatud, kuvatakse partiinumbri automaatse reserveerimise viip isegi siis, kui komplekteerimiseks on saadaval ainult üks partii.

Kuid kui kasutate sama kaupa laos, kus laoprotsessid on lubatud, ei kuvata automaatse reserveerimise viipa.

## <a name="resolution"></a>Lahendus

Kui reserveerimishierarhia on määratletud *partiiülese* või *seeriaülesena*, peab viidatud dimensioon (**partiinumber** või **seerianumber**) alati olema määratud nõudlustellimustel. Laoprotsessid võivad teabe lõpule viia, kui saadaval on üks partii- või seerianumber. Kuna ladu ei ole laoprotsesside jaoks lubatud, peab kasutaja alati määrama kõik **asukohast** ülalnimetatud dimensioonid.
