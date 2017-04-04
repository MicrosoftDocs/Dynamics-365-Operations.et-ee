---
title: "Konfigureerida paralleelselt tegutseda töövoos"
description: "Paralleeltegevuse konfigureerimiseks tehke töövooredaktoris järgmist."
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
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
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 818fb054742b935d002a7341e54a37eca0bb4761
ms.lasthandoff: 03/31/2017


---

# <a name="configure-a-parallel-activity-in-a-workflow"></a>Konfigureerida paralleelselt tegutseda töövoos

Paralleeltegevuse konfigureerimiseks tehke töövooredaktoris järgmist.

Paralleeltegevus koosneb töövoo harudes, mis töötavad samal ajal.

## <a name="name-a-parallel-activity"></a>Paralleeltegevusele nime andmine
Paralleeltegevusele nime andmiseks tehke järgmist.
1.  Paralleelselt tegutseda paremklõpsake ja seejärel klõpsake **atribuudid** avamiseks ning **atribuudid** vormi.
2.  Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
3.  Väljale **Nimi** sisestage paralleeltegevuse kordumatu nimi.
4.  Klõpsake valikut **Sule**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Paralleeltegevuse harude konfigureerimine
Selle paralleeltegevuse harude lisamiseks ja konfigureerimiseks tehke järgmist.
1.  Topeltklõpsake paralleeltegevust, et kuvada paralleeltegevuse harud.
2.  Haru lisamiseks lohistage element **Haru** alalt **Töövoo elemendid** lõuendil olevasse sisestuspunkti. Järgmisel joonisel on kujutatud sisestuspunkt.![Sisestuspunkt](./media/workflow_insertionpoint.gif)
    | **Märkus. **                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | Harude järjestus pole oluline, kuna kõik paralleeltegevuse harud töötavad samal ajal. |

3.  Iga haru konfigureerimiseks vt jaotist [Paralleelharu konfigureerimine](http://axhelp.dynamics.com/en/wiki/configure-a-parallel-branch/).




