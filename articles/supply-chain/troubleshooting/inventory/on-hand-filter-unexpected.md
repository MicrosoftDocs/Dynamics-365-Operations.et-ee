---
title: Laoseisu loendilehe filtripaan ei toimi ootuspäraselt
description: Filtripaani filtrid lehel "Vaba kaubavaru loend" ei filtreeri tulemusi nii, nagu te eeldate.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 3857ce3720430c6f512d5abc4c9c4d390a0c3377
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686679"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Laoseisu loendilehe filtripaan ei toimi ootuspäraselt

## <a name="symptoms"></a>Sümptomid

Filtripaani filtrid vaba loendi **lehel** ei filtreeri tulemusi nii, nagu te eeldate.

## <a name="resolution"></a>Lahendus

Leht **Vaba kaubavaru loend** koostatakse üksikasjalikust vaba kaubavaru tabelist, mis sisaldab kõiki saadaolevaid dimensioone. Sellel lehel olev loend on aga vaid kokkuvõte. Seetõttu võidakse selles kombineerida lähtetabeli ridu, koondades väärtuseid kuvatud dimensioonide järgi.

Filtripaanil seadistatud filtrid kehtivad lähtetabeli, mitte koondloendi kohta. Selline käitumine võib mõnikord anda ootamatuid tulemusi, nagu näha [nendes näidetes](/dynamics365/supply-chain/inventory/inventory-on-hand-list#examples).

[Ruudustikus esitatud filtrid](/dynamics365/supply-chain/inventory/inventory-on-hand-list#grid-filters) rakenduvad *siiski* koondatud loendile. Need filtrid hõlmavad nii kiirfiltrit ruudustiku ülaosas kui ka iga veerupäise filtrit.
