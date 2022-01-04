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
ms.openlocfilehash: 2b2b233e22378c8710a63dce83d168bfd89eba7f
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920494"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Laoseisu loendilehe filtripaan ei toimi ootuspäraselt

## <a name="symptoms"></a>Sümptomid

Filtripaani filtrid vaba loendi lehel ei filtreeri tulemusi nii, **nagu** te eeldate.

## <a name="resolution"></a>Lahendus

Leht **Vaba kaubavaru loend** koostatakse üksikasjalikust vaba kaubavaru tabelist, mis sisaldab kõiki saadaolevaid dimensioone. Sellel lehel olev loend on aga vaid kokkuvõte. Seetõttu võidakse selles kombineerida lähtetabeli ridu, koondades väärtuseid kuvatud dimensioonide järgi.

Filtripaanil seadistatud filtrid kehtivad lähtetabeli, mitte koondloendi kohta. Selline käitumine võib mõnikord anda ootamatuid tulemusi, nagu näha [nendes näidetes](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#examples).

[Ruudustikus esitatud filtrid](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#grid-filters) rakenduvad *siiski* koondatud loendile. Need filtrid hõlmavad nii kiirfiltrit ruudustiku ülaosas kui ka iga veerupäise filtrit.
