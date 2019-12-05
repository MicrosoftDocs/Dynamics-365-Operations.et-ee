---
title: Paralleeltegevuste konfigureerimine töövoos
description: Paralleeltegevuse konfigureerimiseks tehke töövooredaktoris järgmist.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14b4410a0bd177159817cd5116a5a0d959992ad5
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812405"
---
# <a name="configure-parallel-activities-in-a-workflow"></a>Paralleeltegevuste konfigureerimine töövoos

[!include [banner](../includes/banner.md)]

Paralleeltegevuse konfigureerimiseks tehke töövooredaktoris järgmist.

Paralleeltegevus koosneb töövoo harudes, mis töötavad samal ajal.

## <a name="name-a-parallel-activity"></a>Paralleeltegevusele nime andmine

Paralleeltegevusele nime andmiseks tehke järgmist.

1. Paremklõpsake paralleeltegevust ja klõpsake valikut **Atribuudid** , et avada vorm **Atribuudid**.
2. Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
3. Väljale **Nimi** sisestage paralleeltegevuse kordumatu nimi.
4. Klõpsake valikut **Sule**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Paralleeltegevuse harude konfigureerimine

Selle paralleeltegevuse harude lisamiseks ja konfigureerimiseks tehke järgmist.

1. Topeltklõpsake paralleeltegevust, et kuvada paralleeltegevuse harud.
2. Haru lisamiseks lohistage element **Haru** alalt **Töövoo elemendid** lõuendil olevasse sisestuspunkti. Järgmisel joonisel on kujutatud sisestuspunkt.

    ![Sisestuspunkt](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > Harude järjestus pole oluline, kuna kõik paralleeltegevuse harud töötavad samal ajal.

3. Iga haru konfigureerimiseks vaadake jaotist [Töövoo paralleelsete harude konfigureerimine](configure-parallel-branch-workflow.md).
