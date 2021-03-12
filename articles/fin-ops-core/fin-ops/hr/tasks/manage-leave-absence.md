---
title: Puhkuse haldamine
description: Selles protseduuris näitlikustatakse, kuidas luua töötaja puhkusekirjeid.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmEmploymentLeave
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd49e4c1c5c97094061fa119ac1dda99ef69e5e4
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797978"
---
# <a name="manage-leave-of-absence"></a><span data-ttu-id="eb0e2-103">Puhkuse haldamine</span><span class="sxs-lookup"><span data-stu-id="eb0e2-103">Manage leave of absence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eb0e2-104">Selles protseduuris näitlikustatakse, kuidas luua töötaja puhkusekirjeid.</span><span class="sxs-lookup"><span data-stu-id="eb0e2-104">This procedure walks through the creation of employee leave records.</span></span> <span data-ttu-id="eb0e2-105">Saate jälgida erinevatel põhjustel, nagu meditsiiniline, hariduslik või vanemlikud kohustused, puhkusel oldud aega.</span><span class="sxs-lookup"><span data-stu-id="eb0e2-105">You can track leave time for reasons that include medical, educational, or parental activities.</span></span> <span data-ttu-id="eb0e2-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="eb0e2-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="eb0e2-107">Avage Personaliarvestus > Töötajad > Töötajad.</span><span class="sxs-lookup"><span data-stu-id="eb0e2-107">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="eb0e2-108">Valige loendist töötaja.</span><span class="sxs-lookup"><span data-stu-id="eb0e2-108">In the list, select an employee.</span></span>
3. <span data-ttu-id="eb0e2-109">Töötaja nime valides saate kuvada üksikasjaliku teabe valitud töötaja kohta.</span><span class="sxs-lookup"><span data-stu-id="eb0e2-109">Display detailed information for the selected employee by selecting the employee's name.</span></span>
4. <span data-ttu-id="eb0e2-110">Klõpsake vahekaarti Tööhõive.</span><span class="sxs-lookup"><span data-stu-id="eb0e2-110">Click the Employment tab.</span></span>
5. <span data-ttu-id="eb0e2-111">Klõpsake valikut Puhkus.</span><span class="sxs-lookup"><span data-stu-id="eb0e2-111">Click Leave.</span></span>
6. <span data-ttu-id="eb0e2-112">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="eb0e2-112">Click New.</span></span>
7. <span data-ttu-id="eb0e2-113">Klõpsake väljal Puhkuse tüüp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="eb0e2-113">In the Leave type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="eb0e2-114">Puhkuse tüübi saate tulukoodiga seostada vormil Puhkuse tüübid.</span><span class="sxs-lookup"><span data-stu-id="eb0e2-114">You can associate a leave type to an earning code in the Leave types form.</span></span> <span data-ttu-id="eb0e2-115">Kui tulukoodiga on seostatud puhkuse tüüp, luuakse sisestatud puudumisperioodiks tulukoodiga seostatud tulurida.</span><span class="sxs-lookup"><span data-stu-id="eb0e2-115">If a leave type is associated with an earning code, an earning line will be generated with the associated earning code during the leave period that you enter.</span></span>  
8. <span data-ttu-id="eb0e2-116">Valige loendist puhkuse tüüp.</span><span class="sxs-lookup"><span data-stu-id="eb0e2-116">In the list, select a leave type.</span></span> 
    * <span data-ttu-id="eb0e2-117">Näide: adopteerimine</span><span class="sxs-lookup"><span data-stu-id="eb0e2-117">For example: Adoption</span></span>  
9. <span data-ttu-id="eb0e2-118">Sisestage puhkuse alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="eb0e2-118">Enter the date that the leave will start.</span></span> <span data-ttu-id="eb0e2-119">Näide: 26.10.2015</span><span class="sxs-lookup"><span data-stu-id="eb0e2-119">Example: '2015-10-26'</span></span>
    * <span data-ttu-id="eb0e2-120">Näide: 26.10.2015</span><span class="sxs-lookup"><span data-stu-id="eb0e2-120">For example:  2015-10-26</span></span>  
10. <span data-ttu-id="eb0e2-121">Sisestage puhkuse alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="eb0e2-121">Enter the date that the leave will start.</span></span> 
    * <span data-ttu-id="eb0e2-122">Näide: 20.11.2015</span><span class="sxs-lookup"><span data-stu-id="eb0e2-122">For example:  2015-11-20</span></span>  
11. <span data-ttu-id="eb0e2-123">Sisestage märkuse väljale kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="eb0e2-123">In the note field, enter a description.</span></span>
    * <span data-ttu-id="eb0e2-124">Näide: adopteerimispuhkus</span><span class="sxs-lookup"><span data-stu-id="eb0e2-124">For example: Leave for adoption</span></span>  
12. <span data-ttu-id="eb0e2-125">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="eb0e2-125">Click Save.</span></span>

