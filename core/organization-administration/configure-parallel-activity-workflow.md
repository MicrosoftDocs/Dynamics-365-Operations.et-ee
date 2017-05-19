---
title: "Töövoos paralleeltegevuse konfigureerimine"
description: "Paralleeltegevuse konfigureerimiseks tehke töövooredaktoris järgmist."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: ce3fca9d2dbca046232365b1375bfd920d5b10fd
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


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






