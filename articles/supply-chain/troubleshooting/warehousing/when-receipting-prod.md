---
title: Ühele kviitungile prinditakse mitme tööpäise jaoks ainult üks silt
description: Ühele kviitungile prinditakse mitme tööpäise jaoks ainult üks silt.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: cf307964a07c2b69eb5e4ef2cf9dc094482736d0970e333e84f674c9be6331c7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740523"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a>Ühele kviitungile prinditakse mitme tööpäise jaoks ainult üks silt

KB number: 4614667

## <a name="symptoms"></a>Sümptomid

Mitu tööpäist luuakse samale sihtlitsentsiplaadile osana ühest laorakenduse vastuvõtusündmusest. Toote saabumisel prinditakse siiski ainult üks litsentsiplaadi silt.

## <a name="resolution"></a>Eraldusvõime

Süsteem käitub kavandatud viisil.

Praeguses kujunduses luuakse alati üks litsentsiplaadi silt, sõltumata töö päise ja töörea kombinatsioonide arvust. Loodud silt sisaldab teavet ainult ühe kombinatsiooni kohta.

Selle probleemi lahendamiseks veenduge, et töö päise loomine on alati vastendatud ainult ühe sihtlitsentsiplaadiga.
