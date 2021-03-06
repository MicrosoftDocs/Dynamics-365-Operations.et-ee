---
title: Üksus, kus on kasutatud
description: Selles teemas kirjeldatakse, kuidas saada ülevaadet, kuidas üksust kasutatakse varahalduses.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetItemWhereUsed, EntAssetItemWhereUsedCalculate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 262a5a9d83767599f6e15183d6afcacf4b5901fe
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808636"
---
# <a name="item-where-used"></a>Üksus, kus on kasutatud

[!include [banner](../../includes/banner.md)]

 

Saate arvutada kindlat üksust, et saada ülevaade, kus vara halduses seda üksust on kasutatud. Tulemused näitavad konteksti, milles üksust on kasutatud selle kasutusea jooksul. Lehte **Üksus, kus kasutatud** saab avada varahalduse põhimenüüst ja sellele pääseb juurde ka järgmistelt lehtedelt:

- [Vara kooslused](../objects/object-BOM.md)

- [Vara tavatüübi varuosad](../setup-for-objects/object-types.md#spare-parts-on-the-asset-type-setup)

- [Hooldustööde tüüpide kategooriad ja hooldustööde tüübid, hooldustööde tüüpide variandid, hooldustööde kaubandus ja hoolduse kontrollnimekirjad](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [Hooldusprognoos](../work-orders/maintenance-forecasts.md)

- [Hange](../work-orders/procurement.md)

- [Töökäsu ost](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a>Looge „Üksus, kus kasutatud“ arvutus

1. Klõpsake **Vara haldus** > **Päringud** > **Üksus, kus kasutatud** või valige ühes ülal mainitud lehel nupp **Üksus, kus kasutatud**.

2. Dialoogis **Üksus, kus kasutatud** valige üksus, mida tahate arvutada väljas **Üksuse number**.

3. Väljaga **Tase** saate määrata, kui täpsed töö asukohtade üksuse read on. 

    Näiteks, kui sisestate välja numbri „1“ ja teil on mitmetasemeline töö asukoha ülesehitus, näidatakse ülemisel tasemel töö asukoha kõiki üksuse ridu. Seega suhe/kogus rea kohta võidakse lisada madalama taseme töö asukohtadest. 
    
    Kui sisestate välja **Tase** numbri „0“, näete põhjalikku tulemust, kus on näidatud asjakohaste kõikide töö asukoha tasemete kõik üksuse read.

4. Jaotises **Kaasamine** valige arvutusse lisatavate vahetamisnuppude seast „Jah“.

5. Arvutuse alustamiseks klõpsake **OK**.

6. Valige vahekaardi **Üksus, kus kasutatud** nupud  **Rühmitusalus**, et näidata arvutuse nõutavate andmete taset. Valitud nupud **Rühmitusalus** on esile tõstetud. Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.

7. Kui tahate näidata üksusega seotud dimensioone, klõpsake **Näita dimensioone** ja valige näidatavad dimensioonid.

## <a name="example"></a>Näide

Alloleval kuvatõmmisel on näide üksuse numbri „1000“ „Üksus, kus kasutatud“ arvutusest.

![„Üksus, kus kasutatud“ arvutuse näide](media/12-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]