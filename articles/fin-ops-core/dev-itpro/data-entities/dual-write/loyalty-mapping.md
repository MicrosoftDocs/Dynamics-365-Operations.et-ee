---
title: Kliendikaardid ja preemiapunktid
description: Selles teemas kirjeldatakse kliendikaartide ja preemiapunktide andmete integreerimist Finance and Operationsi rakenduste ja Common Data Service'i vahel.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
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
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: e7e67946930404ab7ba0c7fccf468722f723d675
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172965"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Kliendikaardid ja preemiapunktid

[!include [banner](../../includes/banner.md)]



Ettevõtted liigitavad kliente ja pakuvad keerukaid teenuseid klientide ostu- ja kulutamisharjumuste põhjal. Microsoft Dynamics 365 rakenduste komplektis on Dynamics 365 Commerce'il kliendikaartide, preemiapunktide, püsikliendipõhine hinnakujunduse ja preemiapõhise ostukogemusi hõlbustamiseks ja käsitlemiseks vajalik infrastruktuur ja funktsioonid. Kui Commerce'i kliendikaartide ja preemiapunktide andmed sünkroonitakse Common Data Service'isse, saavad Dynamics 365 mudeljuhitud rakendused neid kasutada. Näiteks Dynamics 365 Customer Service'i kasutajad saavad kasutada neid andmeid samade keerukate teenuste saamiseks tehnoabi kaudu.

## <a name="templates"></a>Mallid

| Finance and Operations rakendused | Mudeljuhitud Dynamics 365 rakendused | Kirjeldus |
|-----------------------------|-----------------------------------|-------------|
| Kliendikaart                | msdyn\_loyaltycards               | See mall sünkroonib kliendikaartide kohta käivat teavet. |
| Püsikliendi preemiapunktid       | msdyn\_loyaltyrewardpoints        | See mall sünkroonib kliendi preemiapunktide kohta käivat teavet. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
