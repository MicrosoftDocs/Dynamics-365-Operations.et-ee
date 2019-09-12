---
title: Vara vea kulujuhtimine
description: Selles teemas selgitatakse vara vea kulujuhtimist Varahalduses.
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
ms.openlocfilehash: 2fe75c327cdc2bdd76173430ed551895f5941c7b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918299"
---
# <a name="asset-fault-cost-control"></a>Vara vea kulujuhtimine

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Varahalduses saate arvutada vara vea registreerimiste kulusid, et saada ülevaate tegelikest kuludest võrreldes eelarvekuludega vigadele. Tegelikud kulud põhinevad sisestatud kannetel. Kuupäev on vea kuupäev, mil sümptom registreeriti.

1. Klõpsake **Varahaldus** > **Päringud** > **Vara viga** > **Vara vea kulujuhtimine**.

2. Valige dialoogiaknas **Vara vea kulujuhtimine** finantsdimensioon, mida soovite arvutusse kaasata, kui see on nõutav.

4. Kui te ei soovi nulli kuluga tulemusi näidata, valige "Jah" lülitusnupul **Jäta null vahele**.

5. Saate kasutada välja **Tase**, et näidata, kui üksikasjalikult soovite, et kulujuhtimise read oleksid seotud töö asukohtadega. Näiteks kui sisestate väljale numbri "1" ja teil on mitmetasandiline töö asukoha struktuur, kuvatakse ülemisel tasemel kõik vara vea kulujuhtimise read töö asukoha kohta ja seetõttu võib rea tunnid liita töö asukohast, mis asuvad madalamal tasemel. Kui sisestate numbri "0" väljale **Tase**, näete üksikasjalikku tulemust, mis näitab kõiki vara vea kulujuhtimise ridu kõigi töö asukoha tasemete puhul, millega need on seotud.

6. Kui soovite otsingut piirata, saate valida kindlad varad, vea kuupäevad ja vea põhjused **Lisamiskirjed** kiirkaardi valikus.

7. Arvutuse alustamiseks klõpsake **OK**.

8. Toimingupaani rühmades **Rühmitusalus** klõpsake asjakohastele nuppudele, et näidata arvutuse soovitud üksikasja taset. Valitud toimingupaani nupud on esile tõstetud. Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.

Alltoodud joonisel on näidatud vara vea kulujuhtimise arvutamise näide.

![Joonis 1](media/05-controlling-and-reporting.png)

Lisateavet vigade seadistamise kohta vaadake jaotisest [Veahaldus](../setup-for-work-orders/fault-management.md).

>[!NOTE]
>**Algne eelarve** väli näitab eelarve kulusid töökäskude prognoosist. Väljal **Tegelik kulu** kuvatakse töökäskudesse sisestatud kulud. Väli **Kooskõlastatud kulu** näitab kogukulusid, millele teie ettevõte on pühendunud seoses töökäskudega.

