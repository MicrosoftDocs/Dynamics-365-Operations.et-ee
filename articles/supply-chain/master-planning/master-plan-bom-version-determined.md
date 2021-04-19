---
title: Koosluse versiooni määramine
description: Nõudluse koostamise ajal, kui kaubal on vaiketellimuse tüüp Tootmine, leiab plaanimismootor laoalal põhineva kehtiva koosluse versiooni.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d4fd5f28d0ee85c267ea6a86a1452fbacc824620
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833613"
---
# <a name="determine-the-bom-version"></a><span data-ttu-id="82bad-103">Koosluse versiooni määramine</span><span class="sxs-lookup"><span data-stu-id="82bad-103">Determine the BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82bad-104">Nõudluse koostamise ajal, kui kaubal on vaiketellimuse tüüp Tootmine, leiab plaanimismootor laoalal põhineva kehtiva koosluse versiooni.</span><span class="sxs-lookup"><span data-stu-id="82bad-104">During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site.</span></span> 

<span data-ttu-id="82bad-105">Laoala dimensioon on alati teada ja nimetatud nõudluskandes.</span><span class="sxs-lookup"><span data-stu-id="82bad-105">The site dimension is always known and is stated on the demand transaction.</span></span> <span data-ttu-id="82bad-106">Kasutatava koosluse versiooni määramiseks kasutatakse järgmist protsessi.</span><span class="sxs-lookup"><span data-stu-id="82bad-106">The following process is used to determine the BOM version to use:</span></span>

-   <span data-ttu-id="82bad-107">Kui nõudelaoalal on kauba jaoks määratud koosluse versioon, kasutatakse seda laoalapõhist kooslust.</span><span class="sxs-lookup"><span data-stu-id="82bad-107">If there is a BOM version defined for the item at the demand site, the site-specific BOM is used.</span></span>
-   <span data-ttu-id="82bad-108">Kui nõudelaoalal pole kauba jaoks määratud koosluse versiooni, kasutatakse üldkooslust.</span><span class="sxs-lookup"><span data-stu-id="82bad-108">If there is no site-specific BOM version defined for an item at the demand site, a general BOM is used.</span></span> <span data-ttu-id="82bad-109">Üldkooslus ei nimeta laoala ja see kehtib mitme laoala korral.</span><span class="sxs-lookup"><span data-stu-id="82bad-109">A general BOM does not state a site, and it is valid for multiple sites.</span></span> <span data-ttu-id="82bad-110">Kui üldkooslus on olemas, siis kasutatakse seda.</span><span class="sxs-lookup"><span data-stu-id="82bad-110">If there is a general BOM, it is used.</span></span>
-   <span data-ttu-id="82bad-111">Kui ei ole ühtegi kasutuselolevat koosluse versiooni, lõpeb siinkohal nõudluse kooslusearvutus.</span><span class="sxs-lookup"><span data-stu-id="82bad-111">If there is no general BOM version to use, the demand explosion stops at this point.</span></span>

<span data-ttu-id="82bad-112">Kehtiv koosluse versioon, laoalapõhine või üldine, peab vastama nõutavatele kuupäeva ja koguse kriteeriumidele.</span><span class="sxs-lookup"><span data-stu-id="82bad-112">A valid BOM version, whether site-specific or general, must meet the required criteria for date and quantity.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]