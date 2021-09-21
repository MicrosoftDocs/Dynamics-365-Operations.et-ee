---
title: Tootmise planeerimisel ei arvestata ohutusvarusid
description: Tootmise planeerimisel ei arvestata ohutusvaru, mis on seatud kauba laovarule fikseeritud tarne puhul
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 738296b7570ded0a4ee806e4445204a68e6a08c8
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476099"
---
# <a name="production-scheduling-doesnt-consider-the-safety-margins"></a>Tootmise planeerimisel ei arvestata ohutusvarusid

## <a name="symptoms"></a>Sümptomid

Koondplaneerimine vaatleb ohutusvaru. Siiski eiratakse ohutusvaru plaanitud tootmistellimuste planeerimisel.

## <a name="resolution"></a>Lahendus

Marginaale arvestatakse ainult koondplaneerimise käigus, mitte käsitsi planeerimisel. Veerised on kavandatud toimima puhvrina planeerimise faasis, et anda osa "marginaali" tegeliku protsessi jaoks.

Soovitud tulemuse saamiseks saate marginaali eemaldada. Seejärel tuleb protsessi uuendada nii, et see sisaldaks soovitud kellaaega (nt ooteaeg). Nii koondplaneerimine kui ka käsitsi planeerimine peaksid seejärel esitama sama tulemuse.
