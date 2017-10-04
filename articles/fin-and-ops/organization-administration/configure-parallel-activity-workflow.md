---
title: "Töövoos paralleeltegevuse konfigureerimine"
description: "Paralleeltegevuse konfigureerimiseks tehke töövooredaktoris järgmist."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4c2f98803164d5c761d2089152c077cfb9e83c43
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017

---

# <a name="configure-a-parallel-activity-in-a-workflow"></a>Töövoos paralleeltegevuse konfigureerimine

[!include[banner](../includes/banner.md)]


Paralleeltegevuse konfigureerimiseks tehke töövooredaktoris järgmist.

Paralleeltegevus koosneb töövoo harudes, mis töötavad samal ajal.

## <a name="name-a-parallel-activity"></a>Paralleeltegevusele nime andmine
Paralleeltegevusele nime andmiseks tehke järgmist.
1.  Paremklõpsake paralleeltegevust ja klõpsake valikut **Atribuudid** , et avada vorm **Atribuudid**.
2.  Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
3.  Väljale **Nimi** sisestage paralleeltegevuse kordumatu nimi.
4.  Klõpsake valikut **Sule**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Paralleeltegevuse harude konfigureerimine
Selle paralleeltegevuse harude lisamiseks ja konfigureerimiseks tehke järgmist.
1.  Topeltklõpsake paralleeltegevust, et kuvada paralleeltegevuse harud.
2.  Haru lisamiseks lohistage element **Haru** alalt **Töövoo elemendid** lõuendil olevasse sisestuspunkti. Järgmisel joonisel on kujutatud sisestuspunkt.![Sisestuspunkt](./media/workflow_insertionpoint.gif)
    | **Märkus.**                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | Harude järjestus pole oluline, kuna kõik paralleeltegevuse harud töötavad samal ajal. |

3.  Iga haru konfigureerimiseks vt jaotist [Paralleelharu konfigureerimine](configure-parallel-branch-workflow.md).





