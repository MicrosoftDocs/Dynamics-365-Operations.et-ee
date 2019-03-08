---
title: Puhkuse haldamine
description: Selles protseduuris näitlikustatakse, kuidas luua töötaja puhkusekirjeid.
author: ShielaSogge
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmEmploymentLeave
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7687d31fbf73a02b1b924d092e77ac28b573e694
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "337965"
---
# <a name="manage-leave-of-absence"></a><span data-ttu-id="9e84d-103">Puhkuse haldamine</span><span class="sxs-lookup"><span data-stu-id="9e84d-103">Manage leave of absence</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9e84d-104">Selles protseduuris näitlikustatakse, kuidas luua töötaja puhkusekirjeid.</span><span class="sxs-lookup"><span data-stu-id="9e84d-104">This procedure walks through the creation of employee leave records.</span></span> <span data-ttu-id="9e84d-105">Saate jälgida erinevatel põhjustel, nagu meditsiiniline, hariduslik või vanemlikud kohustused, puhkusel oldud aega.</span><span class="sxs-lookup"><span data-stu-id="9e84d-105">You can track leave time for reasons that include medical, educational, or parental activities.</span></span> <span data-ttu-id="9e84d-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="9e84d-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="9e84d-107">Avage Personaliarvestus > Töötajad > Töötajad.</span><span class="sxs-lookup"><span data-stu-id="9e84d-107">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="9e84d-108">Valige loendist töötaja.</span><span class="sxs-lookup"><span data-stu-id="9e84d-108">In the list, select an employee.</span></span>
3. <span data-ttu-id="9e84d-109">Töötaja nime valides saate kuvada üksikasjaliku teabe valitud töötaja kohta.</span><span class="sxs-lookup"><span data-stu-id="9e84d-109">Display detailed information for the selected employee by selecting the employee's name.</span></span>
4. <span data-ttu-id="9e84d-110">Klõpsake vahekaarti Tööhõive.</span><span class="sxs-lookup"><span data-stu-id="9e84d-110">Click the Employment tab.</span></span>
5. <span data-ttu-id="9e84d-111">Klõpsake valikut Puhkus.</span><span class="sxs-lookup"><span data-stu-id="9e84d-111">Click Leave.</span></span>
6. <span data-ttu-id="9e84d-112">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="9e84d-112">Click New.</span></span>
7. <span data-ttu-id="9e84d-113">Klõpsake väljal Puhkuse tüüp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="9e84d-113">In the Leave type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9e84d-114">Puhkuse tüübi saate tulukoodiga seostada vormil Puhkuse tüübid.</span><span class="sxs-lookup"><span data-stu-id="9e84d-114">You can associate a leave type to an earning code in the Leave types form.</span></span> <span data-ttu-id="9e84d-115">Kui tulukoodiga on seostatud puhkuse tüüp, luuakse sisestatud puudumisperioodiks tulukoodiga seostatud tulurida.</span><span class="sxs-lookup"><span data-stu-id="9e84d-115">If a leave type is associated with an earning code, an earning line will be generated with the associated earning code during the leave period that you enter.</span></span>  
8. <span data-ttu-id="9e84d-116">Valige loendist puhkuse tüüp.</span><span class="sxs-lookup"><span data-stu-id="9e84d-116">In the list, select a leave type.</span></span> 
    * <span data-ttu-id="9e84d-117">Näide: adopteerimine</span><span class="sxs-lookup"><span data-stu-id="9e84d-117">For example: Adoption</span></span>  
9. <span data-ttu-id="9e84d-118">Sisestage puhkuse alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="9e84d-118">Enter the date that the leave will start.</span></span> <span data-ttu-id="9e84d-119">Näide: 26.10.2015</span><span class="sxs-lookup"><span data-stu-id="9e84d-119">Example: '2015-10-26'</span></span>
    * <span data-ttu-id="9e84d-120">Näide: 26.10.2015</span><span class="sxs-lookup"><span data-stu-id="9e84d-120">For example:  2015-10-26</span></span>  
10. <span data-ttu-id="9e84d-121">Sisestage puhkuse alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="9e84d-121">Enter the date that the leave will start.</span></span> 
    * <span data-ttu-id="9e84d-122">Näide: 20.11.2015</span><span class="sxs-lookup"><span data-stu-id="9e84d-122">For example:  2015-11-20</span></span>  
11. <span data-ttu-id="9e84d-123">Sisestage märkuse väljale kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="9e84d-123">In the note field, enter a description.</span></span>
    * <span data-ttu-id="9e84d-124">Näide: adopteerimispuhkus</span><span class="sxs-lookup"><span data-stu-id="9e84d-124">For example: Leave for adoption</span></span>  
12. <span data-ttu-id="9e84d-125">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9e84d-125">Click Save.</span></span>

