---
title: Koondplaani ja mitme saidi funktsionaalsuse ülevaade
description: Koondplaneerimine võtab arvesse laoala ja varude dimensioonide sätteid.
author: roxanadiaconu
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da8db87f44c974b3fee8e249e318669ca8e9f2b8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220820"
---
# <a name="master-planning-and-multisite-functionality-overview"></a><span data-ttu-id="ba9dc-103">Koondplaani ja mitme saidi funktsionaalsuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="ba9dc-103">Master planning and multisite functionality overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba9dc-104">Koondplaneerimine võtab arvesse laoala ja varude dimensioonide sätteid.</span><span class="sxs-lookup"><span data-stu-id="ba9dc-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="ba9dc-105">Laoala dimensioon on kohustuslik ja saate määrata kohustuslikuks ka lao dimensiooni.</span><span class="sxs-lookup"><span data-stu-id="ba9dc-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="ba9dc-106">Kui dimensioon on kohustuslik, tuleb dimensiooniväärtus sisestada kõigile laokannetele.</span><span class="sxs-lookup"><span data-stu-id="ba9dc-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="ba9dc-107">Seepärast on algse nõude laoala ja ladu koondplaneerimise ajal teada.</span><span class="sxs-lookup"><span data-stu-id="ba9dc-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="ba9dc-108">Laoala dimensioon on samuti kooskõlaline nii, et madalama taseme nõude koosnevuse jooksul laoala väärtus ei muutu.</span><span class="sxs-lookup"><span data-stu-id="ba9dc-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="ba9dc-109">Kui ladu ei ole seatud kohustuslikuks, ei pruugi see pärineda nõudest.</span><span class="sxs-lookup"><span data-stu-id="ba9dc-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="ba9dc-110">Planeerimismootor peab määratlema, millist ladu kauba, üksikute ladude ja tellimusrea üksikasjade jaoks määratud sätetel põhinedes kasutada.</span><span class="sxs-lookup"><span data-stu-id="ba9dc-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="ba9dc-111">Järgmised teemad kirjeldavad, kuidas toimib planeerimismootor kasutatava lao määratlemisel, kui on määratud erinevad sätted.</span><span class="sxs-lookup"><span data-stu-id="ba9dc-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="ba9dc-112">Laoala ja lao katmise koondplaanimine, ladu on kohustuslik</span><span class="sxs-lookup"><span data-stu-id="ba9dc-112">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="ba9dc-113">Koondplaanimine laovarude puhul, kohustuslik ladu</span><span class="sxs-lookup"><span data-stu-id="ba9dc-113">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="ba9dc-114">Laoala ja lao katmise koondplaanimine, ladu ei ole kohustuslik</span><span class="sxs-lookup"><span data-stu-id="ba9dc-114">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="ba9dc-115">Koondplaanimine laovarude puhul, ladu ei ole kohustuslik</span><span class="sxs-lookup"><span data-stu-id="ba9dc-115">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="ba9dc-116">Koosluse versiooni määratlemine</span><span class="sxs-lookup"><span data-stu-id="ba9dc-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]