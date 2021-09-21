---
title: Te ei saa mitut toote sissetulekut üheks ostutellimuseks konsolideerida
description: Te ei saa mitut toote sissetulekut üheks ostutellimuseks konsolideerida, kui toote sissetuleku ridadel on eri aruandluskuupäevad.
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 485306279281ceb55a140526f4216af35574af42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476089"
---
# <a name="you-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>Te ei saa mitut toote sissetulekut üheks ostutellimuseks konsolideerida

## <a name="symptoms"></a>Sümptomid

Te ei saa mitut toote sissetulekut üheks ostutellimuseks konsolideerida, kui toote sissetuleku ridadel on eri aruandluskuupäevad.

## <a name="resolution"></a>Lahendus

Rakenduse Microsoft Dynamics 365 Supply Chain Management varasemates versioonides oli selles olukorras konsolideerimine lubatud. Kuid selle tava puhul tekivad tihti vead. Loodavate ostutellimuse ridade aruandluskuupäev ei tohi erineda selliste toote sissetuleku ridade aruandluskuupäevast, mille põhjal need ostutellimuse read loodi. (Ostutellimuse ridade aruandluskuupäev ühtib ostutellimuse päises oleva aruandluskuupäevaga.) Seetõttu pole mitme toote sissetuleku konsolideerimine üheks ostutellimuseks enam lubatud.

Aruandluskuupäeva kasutatakse näiteks eelarvereservi ja pandiõiguse puhul. Seetõttu tuleks see säilitada toote sissetulekust ostutellimusele ülemineku ajal.
