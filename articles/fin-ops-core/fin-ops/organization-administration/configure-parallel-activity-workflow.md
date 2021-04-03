---
title: Paralleeltegevuste konfigureerimine töövoos
description: Paralleeltegevuse konfigureerimiseks tehke töövooredaktoris järgmist.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 450420d44ad4aab233afc5a116369e993aa7a15b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570610"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]