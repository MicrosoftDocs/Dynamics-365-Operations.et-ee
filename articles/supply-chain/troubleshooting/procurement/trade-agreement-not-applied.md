---
title: Kaubanduslelepingu tingimusi ei rakendata imporditud tellimuseridadele
description: Kaubandusleppe hindu ja allahindlusi ei rakendata müügi- või ostutellimuse ridadel, mis imporditakse andmehalduse kaudu
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: fef38819efaff2f2a927cf09fc7f469490149574
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476148"
---
# <a name="trade-agreement-conditions-arent-applied-to-imported-order-lines"></a>Kaubanduslelepingu tingimusi ei rakendata imporditud tellimuseridadele

## <a name="symptoms"></a>Sümptomid

Müügi- või ostutellimuse ridade puhul kohalduvaid kaubandusleppeid ei rakendata ridadel, mis imporditakse andmehalduse kaudu. Samas rakendatakse samu kaubandusleppeid käsitsi loodud müügi- või ostutellimuse ridadel.

## <a name="cause"></a>Põhjus

Kui andmehalduse kaudu imporditud ostutellimuse read sisaldavad juba hinnateavet, ei hinnata kaubanduslepet nende ridade puhul ümber. Näiteks kui rea puhul on seadistatud **Rea allahindluse protsent** või mis tahes hinna ja allahindluse väärtus, siis ei otsita selle rea puhul kaubandusleppeid.

## <a name="workaround"></a>Vastukaal

Selline käitumine on oodatud ja on sarnane nii müügi- kui ka ostutellimuste puhul.

Lahendusega importige ostutellimuse read ilma hinnateavet määramata. Seejärel rakendatakse kaubandusleppeid ja ostutellimuse read värskendatakse määratletud kaubanduslepete alusel.
