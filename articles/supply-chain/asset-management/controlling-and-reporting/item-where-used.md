---
title: Üksus, kus on kasutatud
description: Selles teemas kirjeldatakse, kuidas saada ülevaadet, kuidas üksust kasutatakse varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 84ab803aedf5b803b6c5f39ff1907726335cb45d
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918322"
---
# <a name="item-where-used"></a>Üksus, kus on kasutatud

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Saate arvutada kindlat üksust, et saada ülevaade, kus vara halduses seda üksust on kasutatud. Tulemused näitavad konteksti, milles üksust on kasutatud selle kasutusea jooksul. Lehte **Üksus, kus kasutatud** saab avada vara halduse põhimenüüst ja sellele pääseb juurde ka järgmistelt lehtedelt:

[Vara kooslus](../objects/object-BOM.md)

[Vara tavatüübi varuosad](../setup-for-objects/object-types.md)

[Üksuse ennustamine hooldustöö tüübi tavaennustamisel](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

[Töökäsu hooldusprognoos](../work-orders/maintenance-forecasts.md)

[Töökäsu ostutaotlus](../work-orders/procurement.md)

[Töökäsu ost](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a>Looge „Üksus, kus kasutatud“ arvutus

1. Klõpsake **Vara haldus** > **Päringud** > **Üksus, kus kasutatud** või valige ühes ülal mainitud lehel nupp **Üksus, kus kasutatud**.

2. Dialoogis **Üksus, kus kasutatud** valige üksus, mida tahate arvutada väljas **Üksuse number**.

3. Väljaga **Tase** saate määrata, kui täpsed töö asukohtade üksuse read on. Näiteks, kui sisestate välja numbri „1“ ja teil on mitmetasemeline töö asukoha ülesehitus, näidatakse ülemisel tasemel töö asukoha kõiki üksuse ridu. Seega suhe/kogus rea kohta võidakse lisada madalama taseme töö asukohtadest. Kui sisestate välja **Tase** numbri „0“, näete põhjalikku tulemust, kus on näidatud asjakohaste kõikide töö asukoha tasemete kõik üksuse read.

4. Jaotises **Kaasamine** valige arvutusse lisatavate vahetamisnuppude seast „Jah“.

5. Arvutuse alustamiseks klõpsake **OK**.

6. Valige vahekaardi **Üksus, kus kasutatud** > toimingupaani rühmas **Rühmita alusel...** asjakohaseid nuppe, et näidata arvutuse nõutavate andmete taset. Valitud toimingupaani nupud on esile tõstetud. Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.

7. Kui tahate näidata üksusega seotud dimensioone, klõpsake **Näita dimensioone** ja valige näidatavad dimensioonid.

Alloleval joonisel on näide üksuse numbri „1000“ „Üksus, kus kasutatud“ arvutusest.

![Joonis 1](media/12-controlling-and-reporting.png)

