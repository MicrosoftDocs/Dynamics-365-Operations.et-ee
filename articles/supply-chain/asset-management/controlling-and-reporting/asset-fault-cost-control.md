---
title: Vara vea kulujuhtimine
description: Selles teemas selgitatakse vara vea kulujuhtimist Varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bade6ffa5d5a9af6d23d0d681c32e72eb62d4ecc
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205525"
---
# <a name="asset-fault-cost-control"></a>Vara vea kulujuhtimine

[!include [banner](../../includes/banner.md)]

 

Varahalduses saate arvutada vara vea registreerimiste kulusid, et saada ülevaate tegelikest kuludest võrreldes eelarvekuludega. Tegelikud kulud põhinevad sisestatud kannetel. Kuupäev on vea kuupäev, mil sümptom registreeriti.

1. Klõpsake **Varahaldus** > **Päringud** > **Vara viga** > **Vara vea kulujuhtimine**.

2. Valige dialoogiaknas **Vara vea kulujuhtimine** finantsdimensioon, mida soovite arvutusse kaasata, kui see on nõutav.

4. Kui te ei soovi nulli kuluga tulemusi näidata, valige "Jah" lülitusnupul **Jäta null vahele**.

5. Saate kasutada välja **Tase**, et näidata, kui üksikasjalikult soovite, et kulujuhtimise read oleksid seotud töö asukohtadega. 

    Näiteks kui sisestate väljale numbri "1" ja teil on mitmetasandiline töö asukoha struktuur, kuvatakse ülemisel tasemel kõik vara vea kulujuhtimise read töö asukoha kohta ja seetõttu võib rea tunnid liita töö asukohast, mis asuvad madalamal tasemel. 
    
    Kui sisestate numbri "0" väljale **Tase**, näete üksikasjalikku tulemust, mis näitab kõiki vara vea kulujuhtimise ridu kõigi töö asukoha tasemete puhul, millega need on seotud.

6. Kui soovite otsingut piirata, saate valida kindlad varad, vea kuupäevad ja vea põhjused **Lisamiskirjed** kiirkaardi valikus.

7. Arvutuse alustamiseks klõpsake **OK**.

8. Valige nupud **Rühmitusalus**, et vaadata arvutuse soovitud üksikasja taset. Valitud nupud **Rühmitusalus** on esile tõstetud. Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.

## <a name="example"></a>Näide

Selles näites kuvatakse vara vea kulujuhtimise arvutamist.

- **Algne eelarve** väli näitab eelarve kulusid töökäskude prognoosist. 
- Väljal **Tegelik kulu** kuvatakse töökäskudesse sisestatud kulud. 
- Väli **Kooskõlastatud kulu** näitab kogukulusid, millele teie ettevõte on pühendunud seoses töökäskudega.

    ![Joonis 1](media/05-controlling-and-reporting.png)

Teavet vigade häälestamise kohta vaadake teemast [Veahaldus](../setup-for-work-orders/fault-management.md).
