---
title: Kehtetu litsentsiplaat või asukoha tõrge mobiilirakenduses
description: See tõrketeade kuvatakse, kui skaneerite identifitseerimisnumbri või asukoha. Veenduge, et identifitseerimisnumber ei ole reserveeritud muuks.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f9f10dbade0d13b8fc4b0fc92981d84e6e28e83e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476171"
---
# <a name="invalid-license-plate-or-location-error-when-scanning-in-the-mobile-app"></a>Kehtetu litsentsiplaadi tõrge ID skannimisel mobiilirakenduses

## <a name="symptoms"></a>Sümptomid

Kui skaneerite identifitseerimisnumbri või asukoha, võidakse kuvada see tõrketeade:

> Litsentsiplaat või asukoht on kehtetu.

## <a name="resolution"></a>Lahendus

Veenduge, et identifitseerimisnumber ei ole reserveeritud muuks. See probleem tekkis, kui väärtus, mida kasutaja mobiilirakenduses Warehouse Management skaneeris, oli nii kehtiv asukoht kui ka kehtiv identifitseerimisnumber. See probleem lahendati versioonis 10.0.11.
