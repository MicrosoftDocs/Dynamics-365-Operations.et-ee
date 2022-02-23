---
title: Kliendikaardid ja preemiapunktid
description: Selles teemas kirjeldatakse topeltkirjutuses kliendikaartide ja preemiapunktide andmete integreerimist.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 28872e9510394cf3d5cee151798d4130b8b6fe27
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683494"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Kliendikaardid ja preemiapunkte

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Ettevõtted liigitavad kliente ja pakuvad keerukaid teenuseid klientide ostu- ja kulutamisharjumuste põhjal. Näiteks Dynamics 365 Commerce'il on kliendikaartide, preemiapunktide, püsikliendipõhine hinnakujunduse ja preemiapõhise ostukogemusi hõlbustamiseks ja käsitlemiseks vajalik infrastruktuur ja funktsioonid. Kui Commerce'i kliendikaartide ja preemiapunktide andmed sünkroonitakse Dataverse'i, saavad klientide kaasamise rakendused neid kasutada. Näiteks Dynamics 365 Customer Service'i kasutajad saavad kasutada neid andmeid samade keerukate teenuste saamiseks tehnoabi kaudu.

## <a name="templates"></a>Mallid

| Finance and Operations rakendused | Mudeljuhitud Dynamics 365 rakendused | Kirjeldus |
|-----------------------------|-----------------------------------|-------------|
| Kliendikaart                | msdyn\_loyaltycards               | See mall sünkroonib kliendikaartide kohta käivat teavet. |
| Püsikliendi preemiapunktid       | msdyn\_loyaltyrewardpoints        | See mall sünkroonib kliendi preemiapunktide kohta käivat teavet. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
