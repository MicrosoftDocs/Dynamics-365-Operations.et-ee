---
title: Varude omanik pole liikumiste töötlemisel lubatud
description: Võite saada veateate, "Varude omanik %1 pole lubatud." Praegu toetavad Warehouse management protsessid ainult selle juriidilise isiku omanduses olevat laovaru.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4ee29cfc7bad990cd1ee5deaa98fca217af772ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476096"
---
# <a name="inventory-owner-not-allowed-when-processing-movements-in-the-warehouse-app"></a>Varude omanik pole laorakenduses liikumiste töötlemisel lubatud

## <a name="symptoms"></a>Sümptomid

Liikumiste töötlemisel mobiilirakenduses Warehouse Management võidakse kuvada see tõrketeade:

> Varude omanik %1 pole selles protsessis lubatud.

## <a name="cause"></a>Põhjus

See ilmneb, kui **Omaniku** jälgimise dimensioon puudub, kui liikumiste tegemiseks kasutatakse mobiilirakendust Warehouse Management. Regulaarne lao ülekandmise tööleht Supply Chain Management rakendusest näib töötavad plaanipäraselt ja seda saab sisestada ainult siis, kui **Omaniku** dimensioon on täidetud.

## <a name="resolution"></a>Lahendus

Microsoft on seda probleemi hinnanud ja on määranud, et see on funktsiooni piirang. Praegu toetavad laohalduse protsessid ainult selle juriidilise isiku omanduses olevat laovaru.
