---
title: Aja- ja materjalikulu projektide müügitellimused
description: Selles teemas kirjeldatakse, kuidas aja- ja materjalikulu projektides projektipõhiseid müügitellimusi luua.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 2f27e3e0a2d6aadc4c5224b55f8a416cbe4e83aa
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551198"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Aja- ja materjalikulu projektide müügitellimused

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

See teema kirjeldab, kuidas luua projekti müügitellimust. Müügitellimusi saab luua ainult projektide puhul, mille tüüp on **aja- ja materjalikulu**.

Kui aja- ja materjalikulu projekti lepingus on mitu rahastamisallikat, peate lehel **Projektihalduse ja -arvestuse parameetrid** lubama parameetri **Luba müügitellimused mitme rahastamisallikaga projektide puhul**. 

> [!NOTE]
> - Mitme rahastamisallikaga projektide müügitellimuste tugi on saadaval rakenduse väljalaskes 10.0.2 ja uuemates väljalasetes.
> - Parameeter, millega lubada mitme rahastamisallikaga projektide müügitellimuste tugi, eemaldatakse 2020. aasta aprilli väljalaskevooga, pärast mida on funktsioon alati lubatud.

Projektipõhiseid müügitellimusi saate luua kahel viisil.

- Otse projektis. Valige Tegumiribal **Halda > Kaubatoimingud > Müügitellimus**. Projektiteave kasutab vaikimisi projekti müügitellimust. Kui projektilepingus on rohkem kui üks rahastamisallikas, peate müügitellimuse kliendi määramiseks valima rahastamisallika. Kui projektil on ainult üks rahastamisallikas, siis määratakse klient automaatselt.
- Liikuge loendilehele **Kõik müügitellimused** ja looge uus müügitellimus. Peate valima müügitellimuse projekti. Kui projekt on valitud, määratakse klient rahastamisallikast või kui projektil on mitu rahastamisallikat, peate valima rahastamisallika.

