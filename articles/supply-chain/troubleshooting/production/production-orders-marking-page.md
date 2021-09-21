---
title: Tootmistellimusi ei kuvata märgistuse lehel
description: Mõningaid tootmistellimusi ei kuvata Märgistamine lehel. See teema kirjeldab kolme toote konfiguratsiooni, mis pole märkimiseks saadaval.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 87507e91d3feb2557e7ba771b8e34ff7ca105749
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476066"
---
# <a name="production-orders-arent-shown-on-the-marking-page"></a>Tootmistellimusi ei kuvata märgistuse lehel

## <a name="symptoms"></a>Sümptomid

Diskreetse tootmisega töötamisel ei kuvata lehel **Märgistus** mõnda tootmistellimust.

## <a name="resolution"></a>Lahendus

Tooted, millel on järgmine konfiguratsioon, pole märkimiseks saadaval. Seetõttu ei kuvata neid **Märgistamine** lehel:

- Tooted on määratletud kui *tegeliku kaalu* tüübi tooted.
- Need on lubatud täpsemate lao protsesside jaoks.
- Need on konfigureeritud, et neid kontrollitaks *Standardkulu* põhimõttega.
