---
title: Ostulepingu maksimaalne limiit ei kehti ostutaotluse suhtes
description: Ostulepingu maksimaalne limiit ei kehti ostutaotluse suhtes
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
ms.openlocfilehash: c19d40dce65acbe80d4572bfc4e925aa87ea4f02
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476098"
---
# <a name="the-purchase-agreement-maximum-limit-isnt-effective-on-a-purchase-requisition"></a>Ostulepingu maksimaalne limiit ei kehti ostutaotluse suhtes

## <a name="symptoms"></a>Sümptomid

Kui ostutaotlus seotakse ostulepinguga, ei kehti ostutaotluse puhul ostulepingust pärit ülempiir. Vaikehinnateave on õigesti sisestatud, kuid ostutaotluse kaudu saab tellida koguse, mis ületab ostulepingu ülempiiri.

## <a name="resolution"></a>Lahendus

Selline käitumine on oodatud. Kuna taotlusi ei kinnitata alati, ei tohi ostulepingus kogust või summat reserveerida. Seetõttu ei saa te kasutada ostulepingu ülempiiri.
