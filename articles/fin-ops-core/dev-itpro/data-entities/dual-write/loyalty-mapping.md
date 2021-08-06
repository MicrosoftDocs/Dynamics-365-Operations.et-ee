---
title: Kliendikaardid ja preemiapunktid
description: Selles teemas kirjeldatakse topeltkirjutuses kliendikaartide ja preemiapunktide andmete integreerimist.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: d70fc6fea0e4e4e8f4ad73de5699b6b3fd481613
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542609"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Kliendikaardid ja preemiapunkte

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Ettevõtted liigitavad kliente ja pakuvad keerukaid teenuseid klientide ostu- ja kulutamisharjumuste põhjal. Näiteks Dynamics 365 Commerce'il on kliendikaartide, preemiapunktide, püsikliendipõhine hinnakujunduse ja preemiapõhise ostukogemusi hõlbustamiseks ja käsitlemiseks vajalik infrastruktuur ja funktsioonid. Kui Commerce'i kliendikaartide ja preemiapunktide andmed sünkroonitakse Dataverse'i, saavad klientide kaasamise rakendused neid kasutada. Näiteks Dynamics 365 Customer Service'i kasutajad saavad kasutada neid andmeid samade keerukate teenuste saamiseks tehnoabi kaudu.

## <a name="templates"></a>Mallid

Finance and Operations rakendused | Klientide kaasamise rakendused     | Kirjeldus
|-----------------------------|-----------------------------------|-------------|
[Kliendikaart](mapping-reference.md#149) | msdyn_loyaltycards | See mall sünkroonib kliendikaartide kohta käivat teavet. |
[Püsikliendi tasemed](mapping-reference.md#226) | msdyn_loyaltylevels | See mall sünkroonib kliendi preemiapunktide kohta käivat teavet. |
[Püsikliendi preemiapunktid](mapping-reference.md#150) | msdyn_loyaltyrewardpoints | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
