---
title: Koosluse versiooni koosnevusarvutus
description: "Selles artiklis selgitatakse koondplaanimise stsenaariumi, mis hõlmab koosluse versiooni koosnevusarvutust."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: bce6ffd0ee284f2a5e5b5fef0bdfa92e192b2f42
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="0b08d-103">Koosluse versiooni koosnevusarvutus</span><span class="sxs-lookup"><span data-stu-id="0b08d-103">Explosion of a BOM version</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="0b08d-104">Selles artiklis selgitatakse koondplaanimise stsenaariumi, mis hõlmab koosluse versiooni koosnevusarvutust.</span><span class="sxs-lookup"><span data-stu-id="0b08d-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="0b08d-105">Koosluse versiooni nõudluskoosnevusarvutus loob iga koosluserea kauba nõudluse konkreetses tegevuskohas ning võimalik, et ka konkreetses laos.</span><span class="sxs-lookup"><span data-stu-id="0b08d-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="0b08d-106">Tegevuskohapõhises koosluses saab igale koosluse reale määrata konkreetse lao.</span><span class="sxs-lookup"><span data-stu-id="0b08d-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="0b08d-107">Iga koosluserea puhul määratlevad kauba dimensioonisätted ka lao vajaduse.</span><span class="sxs-lookup"><span data-stu-id="0b08d-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="0b08d-108">Iga koosluserea kaubast tulenevast nõudlusest saab seejärel täiendava nõudluskoosnevusarvutuse alguspunkt.</span><span class="sxs-lookup"><span data-stu-id="0b08d-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="0b08d-109">See koondplaneerimise stsenaarium sisaldab järgmisi tingimusi.</span><span class="sxs-lookup"><span data-stu-id="0b08d-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="0b08d-110">Laoala dimensioon on kohustuslik ja see tuleb sisestada nõudluskandel.</span><span class="sxs-lookup"><span data-stu-id="0b08d-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="0b08d-111">Laoala dimensioon on kooskõlaline.</span><span class="sxs-lookup"><span data-stu-id="0b08d-111">The site dimension is consistent.</span></span> <span data-ttu-id="0b08d-112">Seepärast on madalatasemeline nõudlus sama, mis laoala algsel nõudluskandel.</span><span class="sxs-lookup"><span data-stu-id="0b08d-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="0b08d-113">Järgmisel joonisel on toodud koondplaneerimise nõudluskoosnevusarvutuse protsess.</span><span class="sxs-lookup"><span data-stu-id="0b08d-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![Nõude koostamine, kasutades koosluse versiooni](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="see-also"></a><span data-ttu-id="0b08d-115">Vt ka</span><span class="sxs-lookup"><span data-stu-id="0b08d-115">See also</span></span>
--------

[<span data-ttu-id="0b08d-116">Koondplaanimine – koosluse versiooni määratlemine</span><span class="sxs-lookup"><span data-stu-id="0b08d-116">Master planning - how the BOM version is determined</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="0b08d-117">Koondplaanimine ja mitme laoala funktsioon</span><span class="sxs-lookup"><span data-stu-id="0b08d-117">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)




