---
title: Toote konfiguratsioonimudeli kinnitamine
description: Selle protseduuri käitamine nõuab vähemalt ühe toote konfiguratsioonimudeli kättesaadavust.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c196731046fa01059d61f2df08f47639ba839642
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "360505"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="5b11d-103">Toote konfiguratsioonimudeli kinnitamine</span><span class="sxs-lookup"><span data-stu-id="5b11d-103">Approve a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5b11d-104">Selle protseduuri käitamine nõuab vähemalt ühe toote konfiguratsioonimudeli kättesaadavust.</span><span class="sxs-lookup"><span data-stu-id="5b11d-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="5b11d-105">See protseduur kasutab tipptasemel kõlari mudelit demoettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="5b11d-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="5b11d-106">Pange tähele, et see mudel on juba kinnitatud, kuid protseduur juhatab teid läbi kogu protsessi.</span><span class="sxs-lookup"><span data-stu-id="5b11d-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="5b11d-107">Klõpsake valikut Tootevariandi mudeli määratlus.</span><span class="sxs-lookup"><span data-stu-id="5b11d-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="5b11d-108">Klõpsake valikut Toote konfiguratsioonimudelid.</span><span class="sxs-lookup"><span data-stu-id="5b11d-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="5b11d-109">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="5b11d-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5b11d-110">Valige selle protseduuri jaoks tipptasemel kõlari mudel.</span><span class="sxs-lookup"><span data-stu-id="5b11d-110">Select the High end speaker model for this procedure.</span></span>  
4. <span data-ttu-id="5b11d-111">Klõpsake valikut Versioonid.</span><span class="sxs-lookup"><span data-stu-id="5b11d-111">Click Versions.</span></span>
5. <span data-ttu-id="5b11d-112">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="5b11d-112">Click New.</span></span>
6. <span data-ttu-id="5b11d-113">Sisestage või valige väärtus väljal Tootenumber.</span><span class="sxs-lookup"><span data-stu-id="5b11d-113">In the Product number field, enter or select a value.</span></span>
    * <span data-ttu-id="5b11d-114">Viide tootele kajastab toote konfiguratsioonimudeli versiooni.</span><span class="sxs-lookup"><span data-stu-id="5b11d-114">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="5b11d-115">Ainult need tooteetalonid, millel on piirangupõhise konfiguratsiooni tehnoloogia, kuvatakse selles loendis.</span><span class="sxs-lookup"><span data-stu-id="5b11d-115">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
7. <span data-ttu-id="5b11d-116">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="5b11d-116">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="5b11d-117">Valige, millal tootemudeli versioon kättesaadavaks muutub.</span><span class="sxs-lookup"><span data-stu-id="5b11d-117">Select when the product model version will be available.</span></span>  
8. <span data-ttu-id="5b11d-118">Sisestage kuupäev väljale Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="5b11d-118">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="5b11d-119">Valige lõppkuupäev, millal see tootemudeli versioon aegub, või valige Mitte kunagi.</span><span class="sxs-lookup"><span data-stu-id="5b11d-119">Select an end date when this product model version will expire, or select Never.</span></span>  
9. <span data-ttu-id="5b11d-120">Klõpsake dialoogi avamiseks valikut Kinnita.</span><span class="sxs-lookup"><span data-stu-id="5b11d-120">Click Approve to open the drop dialog.</span></span>
10. <span data-ttu-id="5b11d-121">Valige või sisestage väärtus väljal Kinnitaja.</span><span class="sxs-lookup"><span data-stu-id="5b11d-121">In the Approved by field, enter or select a value.</span></span>
    * <span data-ttu-id="5b11d-122">Valige isik, kes vastutab toimingutes kasutatavate tootemudelite kinnitamise eest.</span><span class="sxs-lookup"><span data-stu-id="5b11d-122">Select the person who is responsible for approving product models for use in operations.</span></span>  
11. <span data-ttu-id="5b11d-123">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5b11d-123">Click OK.</span></span>
12. <span data-ttu-id="5b11d-124">Valige suvand väljal Hinnakujundusmeetod.</span><span class="sxs-lookup"><span data-stu-id="5b11d-124">In the Pricing method field, select an option.</span></span>
    * <span data-ttu-id="5b11d-125">Aktiveerige tootemudeli versioon.</span><span class="sxs-lookup"><span data-stu-id="5b11d-125">Activate the product model version.</span></span> <span data-ttu-id="5b11d-126">Korraga saab ühel tootemudelil olla aktiivne üks toode.</span><span class="sxs-lookup"><span data-stu-id="5b11d-126">It is only possible to have one product active for one product model at a time.</span></span>  
13. <span data-ttu-id="5b11d-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5b11d-127">Close the page.</span></span>

