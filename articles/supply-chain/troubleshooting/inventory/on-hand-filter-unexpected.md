---
title: Laoseisu loendilehe filtripaan ei toimi ootuspäraselt
description: Filtrid filter paanlil "Loendi" leheküljel ei filtreeri tulemusi, nagu sa ootad.
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
ms.openlocfilehash: df11b1c1e7de36fa0458cd931d4be7f84a15d143
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476149"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Laoseisu loendilehe filtripaan ei toimi ootuspäraselt

## <a name="symptoms"></a>Sümptomid

**Vaba kaubavaru** loendilehe filtripaani filtrid ei filtreeri tulemusi nii, nagu te eeldate.

## <a name="resolution"></a>Lahendus

Leht  **Vaba kaubavaru** loend koostatakse üksikasjalikust vaba kaubavaru tabelist, mis sisaldab kõiki saadaolevaid dimensioone. Sellel lehel olev loend on aga vaid kokkuvõte. Seetõttu võidakse selles kombineerida lähtetabeli ridu, koondades väärtuseid kuvatud dimensioonide järgi.

Filtripaanil häälestatud filtrid rakenduvad lähtetabelile, mitte koondatud loendile. Selline käitumine võib mõnikord anda ootamatuid tulemusi, nagu näha [nendes näidetes](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#examples).

Ruudustikus  [ruudustikus esitatud filtrid](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#grid-filters) *siiski* rakenduvad koondatud loendile. Need filtrid hõlmavad nii kiirfiltrit ruudustiku ülaosas kui ka iga veerupäise filtrit.
