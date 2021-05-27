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
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026438"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a>Ühele kviitungile prinditakse mitme tööpäise jaoks ainult üks silt

KB number: 4614667

## <a name="symptoms"></a>Sümptomid

Mitu tööpäist luuakse samale sihtlitsentsiplaadile osana ühest laorakenduse vastuvõtusündmusest. Toote saabumisel prinditakse siiski ainult üks litsentsiplaadi silt.

## <a name="resolution"></a>Eraldusvõime

Süsteem käitub kavandatud viisil.

Praeguses kujunduses luuakse alati üks litsentsiplaadi silt, sõltumata töö päise ja töörea kombinatsioonide arvust. Loodud silt sisaldab teavet ainult ühe kombinatsiooni kohta.

Selle probleemi lahendamiseks veenduge, et töö päise loomine on alati vastendatud ainult ühe sihtlitsentsiplaadiga.
