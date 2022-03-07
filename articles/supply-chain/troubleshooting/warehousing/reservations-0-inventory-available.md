---
title: Süsteem ei saa varude reserveeringuid teha, sest laos on saadaval 0,00
description: Saate tõrketeate, mis ütleb, et süsteem ei saa reserveeringuid teha, sest laos on saadaval 0,00. See probleem on tõenäoliselt põhjustatud avatud tööst.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 75d72f7ee1bdecca5a087b75b1de9907b9d244ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476151"
---
# <a name="system-cant-make-reservations-because-000-are-available-in-the-inventory"></a>Süsteem ei saa reserveeringuid teha, sest laos on saadavus 0,00

## <a name="symptoms"></a>Sümptomid

See probleem võib ilmneda juhul, kui süsteem ei saa varude kogust värskendada, kuna pole piisavalt laokandeid, millel on määratud dimensioone. Sellisel juhul kuvatakse järgnev veateade:

> Füüsiline vaba kaubavaru sait=%1, ladu=%2, varude olek=saadaval, partii number=%3, omanik=%4: %5 ei saa broneerida, kuna laos on saadaval ainult 0,00.

## <a name="resolution"></a>Lahendus

See probleem on tõenäoliselt põhjustatud avatud tööst. Lõpetage töö või võtke vastu ilma töö loomiseta. Veenduge, et varude kanded ei broneeriks kauba kogust füüsiliselt. Näiteks võivad need kanded olla avatud kvaliteetsed tellimused, lao blokeerimise kirjed või väljamineku tellimused.
