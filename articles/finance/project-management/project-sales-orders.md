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
ms.openlocfilehash: d19ee9de70cd14c78a997b7a87c10b53ab3917b0
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249089"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Aja- ja materjalikulu projektide müügitellimused

[!include[banner](../includes/banner.md)]

See teema kirjeldab, kuidas luua projekti müügitellimust. Müügitellimusi saab luua ainult projektide puhul, mille tüüp on **aja- ja materjalikulu**.

Kui aja- ja materjalikulu projekti lepingus on mitu rahastamisallikat, peate lehel **Projektihalduse ja -arvestuse parameetrid** lubama parameetri **Luba müügitellimused mitme rahastamisallikaga projektide puhul**. 

> [!NOTE]
> - Mitme rahastamisallikaga projektide müügitellimuste tugi on saadaval rakenduse väljalaskes 10.0.2 ja uuemates väljalasetes.
> - Parameeter, millega lubada mitme rahastamisallikaga projektide müügitellimuste tugi, eemaldatakse 2020. aasta aprilli väljalaskevooga, pärast mida on funktsioon alati lubatud.

Projektipõhiseid müügitellimusi saate luua kahel viisil.

- Otse projektis. Valige Tegumiribal **Halda > Kaubatoimingud > Müügitellimus**. Projektiteave kasutab vaikimisi projekti müügitellimust. Kui projektilepingus on rohkem kui üks rahastamisallikas, peate müügitellimuse kliendi määramiseks valima rahastamisallika. Kui projektil on ainult üks rahastamisallikas, siis määratakse klient automaatselt.
- Liikuge loendilehele **Kõik müügitellimused** ja looge uus müügitellimus. Peate valima müügitellimuse projekti. Kui projekt on valitud, määratakse klient rahastamisallikast või kui projektil on mitu rahastamisallikat, peate valima rahastamisallika.

