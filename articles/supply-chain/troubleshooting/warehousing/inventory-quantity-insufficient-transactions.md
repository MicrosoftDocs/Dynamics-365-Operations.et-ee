---
title: Laokogust ei uuendatud ebapiisavate kannete tõttu
description: Laokogusest -1% ei saa värskendada, kuna üksuse %2 jaoks pole piisavalt dimensioonidega varutehinguid.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 88130a969039dd741c8ea4fbaabe81acf0e6fb6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476071"
---
# <a name="system-cant-update-inventory-quantity-because-of-insufficient-transactions"></a>Süsteem ei saa varude kogust ebapiisavate kannete tõttu uuendada

## <a name="symptoms"></a>Sümptomid

See probleem võib ilmneda juhul, kui süsteem ei saa varude kogust värskendada, kuna pole piisavalt laokandeid, millel on määratud dimensioone. Sellisel juhul kuvatakse järgnev veateade:

> Varude kogust -%1 ei saanud värskendada, kuna pole piisavalt laokandeid kaubaga %2, mille dimensioonid on suurus =%3, värvus =%4, täiendused =%5, sait =%6, ladu =%7, asukoht =%8, varude olek = saadaval, identifitseerimisnumber =%9, partii number =%10 ID-kood %11 saatepartii ID %12.

## <a name="resolution"></a>Lahendus

Veenduge, et varude kanded ei broneeriks kauba kogust füüsiliselt. Näiteks võivad need kanded avada kvaliteetseid tellimusi, lao blokeerimise kirjeid või väljaminekuordereid.
