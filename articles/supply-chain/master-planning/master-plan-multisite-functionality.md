---
title: Koondplaani ja mitme saidi funktsionaalsuse ülevaade
description: Koondplaneerimine võtab arvesse laoala ja varude dimensioonide sätteid.
author: roxanadiaconu
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f05e3efd1716a27a659ae40145f37bb0b3d977f
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865397"
---
# <a name="master-planning-and-multisite-functionality-overview"></a><span data-ttu-id="c18cc-103">Koondplaani ja mitme saidi funktsionaalsuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="c18cc-103">Master planning and multisite functionality overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c18cc-104">Koondplaneerimine võtab arvesse laoala ja varude dimensioonide sätteid.</span><span class="sxs-lookup"><span data-stu-id="c18cc-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="c18cc-105">Laoala dimensioon on kohustuslik ja saate määrata kohustuslikuks ka lao dimensiooni.</span><span class="sxs-lookup"><span data-stu-id="c18cc-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="c18cc-106">Kui dimensioon on kohustuslik, tuleb dimensiooniväärtus sisestada kõigile laokannetele.</span><span class="sxs-lookup"><span data-stu-id="c18cc-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="c18cc-107">Seepärast on algse nõude laoala ja ladu koondplaneerimise ajal teada.</span><span class="sxs-lookup"><span data-stu-id="c18cc-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="c18cc-108">Laoala dimensioon on samuti kooskõlaline nii, et madalama taseme nõude koosnevuse jooksul laoala väärtus ei muutu.</span><span class="sxs-lookup"><span data-stu-id="c18cc-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="c18cc-109">Kui ladu ei ole seatud kohustuslikuks, ei pruugi see pärineda nõudest.</span><span class="sxs-lookup"><span data-stu-id="c18cc-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="c18cc-110">Planeerimismootor peab määratlema, millist ladu kauba, üksikute ladude ja tellimusrea üksikasjade jaoks määratud sätetel põhinedes kasutada.</span><span class="sxs-lookup"><span data-stu-id="c18cc-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="c18cc-111">Järgmised teemad kirjeldavad, kuidas toimib planeerimismootor kasutatava lao määratlemisel, kui on määratud erinevad sätted.</span><span class="sxs-lookup"><span data-stu-id="c18cc-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="c18cc-112">Koondplaneerimine – laoala ja laovarud, ladu on kohustuslik</span><span class="sxs-lookup"><span data-stu-id="c18cc-112">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="c18cc-113">Koondplaneerimine – laovarud, ladu on kohustuslik</span><span class="sxs-lookup"><span data-stu-id="c18cc-113">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="c18cc-114">Koondplaneerimine – laoala ja laovarud, ladu ei ole kohustuslik</span><span class="sxs-lookup"><span data-stu-id="c18cc-114">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="c18cc-115">Koondplaneerimine – laovarud, ladu ei ole kohustuslik</span><span class="sxs-lookup"><span data-stu-id="c18cc-115">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="c18cc-116">Koondplaneerimine – koosluse versiooni määratlemine</span><span class="sxs-lookup"><span data-stu-id="c18cc-116">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



