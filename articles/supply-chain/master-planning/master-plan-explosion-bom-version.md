---
title: Koosluse versiooni koosnevusarvutus
description: Selles artiklis selgitatakse koondplaanimise stsenaariumi, mis hõlmab koosluse versiooni koosnevusarvutust.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 617d9c3f05f2db30ec075a07b54c4827e668c20e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220844"
---
# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="2f035-103">Koosluse versiooni koosnevusarvutus</span><span class="sxs-lookup"><span data-stu-id="2f035-103">Explosion of a BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f035-104">Selles artiklis selgitatakse koondplaanimise stsenaariumi, mis hõlmab koosluse versiooni koosnevusarvutust.</span><span class="sxs-lookup"><span data-stu-id="2f035-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="2f035-105">Koosluse versiooni nõudluskoosnevusarvutus loob iga koosluserea kauba nõudluse konkreetses tegevuskohas ning võimalik, et ka konkreetses laos.</span><span class="sxs-lookup"><span data-stu-id="2f035-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="2f035-106">Tegevuskohapõhises koosluses saab igale koosluse reale määrata konkreetse lao.</span><span class="sxs-lookup"><span data-stu-id="2f035-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="2f035-107">Iga koosluserea puhul määratlevad kauba dimensioonisätted ka lao vajaduse.</span><span class="sxs-lookup"><span data-stu-id="2f035-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="2f035-108">Iga koosluserea kaubast tulenevast nõudlusest saab seejärel täiendava nõudluskoosnevusarvutuse alguspunkt.</span><span class="sxs-lookup"><span data-stu-id="2f035-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="2f035-109">See koondplaneerimise stsenaarium sisaldab järgmisi tingimusi.</span><span class="sxs-lookup"><span data-stu-id="2f035-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="2f035-110">Laoala dimensioon on kohustuslik ja see tuleb sisestada nõudluskandel.</span><span class="sxs-lookup"><span data-stu-id="2f035-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="2f035-111">Laoala dimensioon on kooskõlaline.</span><span class="sxs-lookup"><span data-stu-id="2f035-111">The site dimension is consistent.</span></span> <span data-ttu-id="2f035-112">Seepärast on madalatasemeline nõudlus sama, mis laoala algsel nõudluskandel.</span><span class="sxs-lookup"><span data-stu-id="2f035-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="2f035-113">Järgmisel joonisel on toodud koondplaneerimise nõudluskoosnevusarvutuse protsess.</span><span class="sxs-lookup"><span data-stu-id="2f035-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![Nõude koostamine, kasutades koosluse versiooni](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a><span data-ttu-id="2f035-115">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="2f035-115">Additional resources</span></span>
--------

[<span data-ttu-id="2f035-116">Koosluse versiooni määratlemine</span><span class="sxs-lookup"><span data-stu-id="2f035-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="2f035-117">Koondplaneerimine ja mitme tegevuskoha funktsiooni ülevaade</span><span class="sxs-lookup"><span data-stu-id="2f035-117">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]