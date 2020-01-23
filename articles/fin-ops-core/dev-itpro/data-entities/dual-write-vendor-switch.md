---
title: Hankija kujunduste vaheldumisi aktiveerimine
description: Selles teemas kirjeldatakse, kuidas lülitada hankija andmete integreerimise vahel Finance and Operationsi rakenduste ja teenuse Common Data Service vahel.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 204d788e72e79e7acf744d24cbeacb0f9b47da7d
ms.sourcegitcommit: 3306e451f04df01c51d8d332306b135d8ae1e254
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/09/2019
ms.locfileid: "2902721"
---
# <a name="switch-between-vendor-designs"></a>Hankija kujunduste vaheldumisi aktiveerimine

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a>Hankijaandmete voog 

Kui kasutate hankija koondandmete jaoks teisi Dynamics 365 rakendusi ja soovite isoleerida hankijateabe klientidest, kasutage seda üldist hankijalahendust.  

![Hankija üldine voog](media/dual-write-vendor-data-flow.png)
 
Kui kasutate hankija koondandmete jaoks teisi Dynamics 365 rakendusi ja soovite hankijaandmete salvestamiseks jätkata olemi **Konto** kasutamist, kasutage seda laiendatud hankijalahendust. Selles lahenduses salvestatakse laiendatud hankijateave, nagu hankija ootelolek ja hankijaprofiil, üksusesse **hankijad** Common Data Service’is. 

![Hankija laiendatud voog](media/dual-write-vendor-detail.jpg)
 
Hankija laiendatud voo kasutamiseks tehke järgmist. 
 
1. Lahendusepakett **SupplyChainCommon** sisaldab töövooprotsessi malle, nagu on näha alloleval pildil.
    > [!div class="mx-imgBorder"]
    > ![Töövooprotsessi mallid](media/dual-write-switch-3.png)
2. Looge uued töövooprotsessid, kasutades töövooprotsessi malle. 
    1. Looge uus töövooprotsess üksusele **Hankija**, kasutades töövooprotsessi malli **Hankijate loomine konto üksuses**, ja klõpsake nuppu **OK**. See töövoog käsitseb üksuse **Konto** hankija loomise stsenaariumi.
        > [!div class="mx-imgBorder"]
        > ![Hankijate loomine konto üksuses](media/dual-write-switch-4.png)
    2. Looge uus töövooprotsess üksusele **Hankija**, kasutades töövooprotsessi malli **Kontode üksuse värskendamine**, ja klõpsake nuppu **OK**. See töövoog käsitseb üksuse **Konto** hankija värskendamise stsenaariumi. 
        > [!div class="mx-imgBorder"]
        > ![Kontode üksuse värskendamine](media/dual-write-switch-5.png)
    3. Looge uued töövooprotsessid mallidest, mis on loodud üksuses **Kontod**. 
        > [!div class="mx-imgBorder"]
        > ![Hankijate loomine hankijate üksuses](media/dual-write-switch-6.png)
        > [!div class="mx-imgBorder"]
        > ![Hankijate üksuse värskendamine](media/dual-write-switch-7.png)
    4. Saate konfigureerida töövoogusid reaalajas või taustatöövoogudena, olenevalt teie nõuetest. 
        > [!div class="mx-imgBorder"]
        > ![Teisendamine taustatöövooks](media/dual-write-switch-8.png)
    5. Aktiveerige töövood, mille lõite üksustes **Konto** ja **Hankija**, et hakata kasutama hankijateabe salvestamiseks üksust **Konto**. 
 
