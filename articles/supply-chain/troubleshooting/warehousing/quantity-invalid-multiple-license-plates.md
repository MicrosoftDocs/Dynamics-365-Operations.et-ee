---
title: Kogus ei kehti mitme LP-ga tööde korjamisel
description: Kui ühes kohas tehakse korjamistöid mitme numbrimärgiga, ei kehti kogus ühiku tk puhul. Kontrollige, et järgmised väljad on õiged.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5b245f71e80339fee3e42cfffa0396078a56926e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476079"
---
# <a name="quantity-not-valid-when-theres-picking-work-with-multiple-lps-in-one-location"></a>Kogus on kehtetu, kui ühes asukohas on komplekteerimistöö, kus on mitu LP-d

## <a name="symptoms"></a>Sümptomid

Kui ühes kohas tehakse korjamistöid mitme numbrimärgiga, ei kehti kogus ühiku *tk* puhul ja kuvatakse järgmine tõrketeade:

> Kogus ei kehti ühiku 1% kohta.

## <a name="resolution"></a>Lahendus

Veenduge, et väljastatud toote või tootevariandi väljad **Toote seeria ID** ja **Ühiku teisendused** on õigesti seadistatud.

Võtke arvesse, et tõrketeadet on parandatud versioonis 10.0.15 oodatud koguse näitamiseks (vt [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). Uus tõrketeade on:

> Kogus on kehtetu. Eeldatud %1 %2.
