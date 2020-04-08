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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 002700ae7f6474b48fbe09cb3aaa72e9516b8224
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143538"
---
# <a name="manage-leave-of-absence"></a><span data-ttu-id="8973f-103">Puhkuse haldamine</span><span class="sxs-lookup"><span data-stu-id="8973f-103">Manage leave of absence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8973f-104">Selles protseduuris näitlikustatakse, kuidas luua töötaja puhkusekirjeid.</span><span class="sxs-lookup"><span data-stu-id="8973f-104">This procedure walks through the creation of employee leave records.</span></span> <span data-ttu-id="8973f-105">Saate jälgida erinevatel põhjustel, nagu meditsiiniline, hariduslik või vanemlikud kohustused, puhkusel oldud aega.</span><span class="sxs-lookup"><span data-stu-id="8973f-105">You can track leave time for reasons that include medical, educational, or parental activities.</span></span> <span data-ttu-id="8973f-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="8973f-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="8973f-107">Avage Personaliarvestus > Töötajad > Töötajad.</span><span class="sxs-lookup"><span data-stu-id="8973f-107">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="8973f-108">Valige loendist töötaja.</span><span class="sxs-lookup"><span data-stu-id="8973f-108">In the list, select an employee.</span></span>
3. <span data-ttu-id="8973f-109">Töötaja nime valides saate kuvada üksikasjaliku teabe valitud töötaja kohta.</span><span class="sxs-lookup"><span data-stu-id="8973f-109">Display detailed information for the selected employee by selecting the employee's name.</span></span>
4. <span data-ttu-id="8973f-110">Klõpsake vahekaarti Tööhõive.</span><span class="sxs-lookup"><span data-stu-id="8973f-110">Click the Employment tab.</span></span>
5. <span data-ttu-id="8973f-111">Klõpsake valikut Puhkus.</span><span class="sxs-lookup"><span data-stu-id="8973f-111">Click Leave.</span></span>
6. <span data-ttu-id="8973f-112">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="8973f-112">Click New.</span></span>
7. <span data-ttu-id="8973f-113">Klõpsake väljal Puhkuse tüüp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="8973f-113">In the Leave type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8973f-114">Puhkuse tüübi saate tulukoodiga seostada vormil Puhkuse tüübid.</span><span class="sxs-lookup"><span data-stu-id="8973f-114">You can associate a leave type to an earning code in the Leave types form.</span></span> <span data-ttu-id="8973f-115">Kui tulukoodiga on seostatud puhkuse tüüp, luuakse sisestatud puudumisperioodiks tulukoodiga seostatud tulurida.</span><span class="sxs-lookup"><span data-stu-id="8973f-115">If a leave type is associated with an earning code, an earning line will be generated with the associated earning code during the leave period that you enter.</span></span>  
8. <span data-ttu-id="8973f-116">Valige loendist puhkuse tüüp.</span><span class="sxs-lookup"><span data-stu-id="8973f-116">In the list, select a leave type.</span></span> 
    * <span data-ttu-id="8973f-117">Näide: adopteerimine</span><span class="sxs-lookup"><span data-stu-id="8973f-117">For example: Adoption</span></span>  
9. <span data-ttu-id="8973f-118">Sisestage puhkuse alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="8973f-118">Enter the date that the leave will start.</span></span> <span data-ttu-id="8973f-119">Näide: 26.10.2015</span><span class="sxs-lookup"><span data-stu-id="8973f-119">Example: '2015-10-26'</span></span>
    * <span data-ttu-id="8973f-120">Näide: 26.10.2015</span><span class="sxs-lookup"><span data-stu-id="8973f-120">For example:  2015-10-26</span></span>  
10. <span data-ttu-id="8973f-121">Sisestage puhkuse alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="8973f-121">Enter the date that the leave will start.</span></span> 
    * <span data-ttu-id="8973f-122">Näide: 20.11.2015</span><span class="sxs-lookup"><span data-stu-id="8973f-122">For example:  2015-11-20</span></span>  
11. <span data-ttu-id="8973f-123">Sisestage märkuse väljale kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="8973f-123">In the note field, enter a description.</span></span>
    * <span data-ttu-id="8973f-124">Näide: adopteerimispuhkus</span><span class="sxs-lookup"><span data-stu-id="8973f-124">For example: Leave for adoption</span></span>  
12. <span data-ttu-id="8973f-125">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="8973f-125">Click Save.</span></span>

