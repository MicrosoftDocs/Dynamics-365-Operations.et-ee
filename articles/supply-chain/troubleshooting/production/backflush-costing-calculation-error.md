---
title: Omahinna tagasiarvestuse arvutamise tõrge lao sulgemisel
description: Varasemates väljalasetes võib lao sulgemisel olla saadud omahinna tagasiarvestuse arvutamise tõrge. See probleem on lahendatud.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ae92b7121998d6b1ba2f08ea5736c55637867fbf
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476105"
---
# <a name="backflush-costing-calculation-error-during-inventory-closing"></a>Omahinna tagasiarvestuse arvutamise tõrge lao sulgemisel

## <a name="symptoms"></a>Sümptomid

Kui kasutate varasemat versiooni kui 10.0.13, siis kui te ei kasuta minimaalsete tootmiskulude voogu, kuvatakse lao sulgemisel järgmine ekslik hoiatusteade.

> Olete käivitamas lao sulgemist kuupäevaga %1. Perioodi lõpukuupäevaga %1 sobivat omahinna tagasiarvestust ei ole registreeritud. Palun teostage perioodi lõpukuupäevaga %1 sobiv omahinna tagasiarvestus. Varude hindamine, müüdud kaupade kulu ja erinevused ei pruugi olla abiraamatu või pearaamatu puhul õiged, kuni see on teostatud.

## <a name="resolution"></a>Lahendus

See probleem on parandatud versioonis 10.0.13 ja hilisemates versioonides. Lisateavet leiad teemast [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).
