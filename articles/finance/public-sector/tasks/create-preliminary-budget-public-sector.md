---
title: Esialgse eelarve loomine avaliku sektori puhul
description: Saate luua esialgsed eelarve registreerimiskanded kindla eelarvemudeli jaoks ja dimensiooniväärtused.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22538d58cc3499bd030848699d6c5831dfd8888a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975156"
---
# <a name="create-a-preliminary-budget-for-public-sector"></a><span data-ttu-id="47c8e-103">Esialgse eelarve loomine avaliku sektori puhul</span><span class="sxs-lookup"><span data-stu-id="47c8e-103">Create a preliminary budget for Public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="47c8e-104">Saate luua esialgsed eelarve registreerimiskanded kindla eelarvemudeli jaoks ja dimensiooniväärtused.</span><span class="sxs-lookup"><span data-stu-id="47c8e-104">You can create preliminary budget register entries for a specific budget model and dimension values.</span></span> <span data-ttu-id="47c8e-105">Pärast tegeliku eelarve kinnitamist saate luua eelarve algsed registrikirjed.</span><span class="sxs-lookup"><span data-stu-id="47c8e-105">After the actual budget is approved, you can create original budget register entries.</span></span> <span data-ttu-id="47c8e-106">See protseduur loodi PSUS-ettevõtte demoandmetega avaliku sektori sektsioonis.</span><span class="sxs-lookup"><span data-stu-id="47c8e-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="47c8e-107">Tehke valik Eelarvestamine > Eelarveregistri kirjed.</span><span class="sxs-lookup"><span data-stu-id="47c8e-107">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="47c8e-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="47c8e-108">Click New.</span></span>
3. <span data-ttu-id="47c8e-109">Klõpsake väljal Budget model (Eelarve mudel) otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="47c8e-109">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="47c8e-110">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="47c8e-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="47c8e-111">Klõpsake väljal Budget code (Eelarve kood) otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="47c8e-111">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="47c8e-112">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="47c8e-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="47c8e-113">Klõpsake väljal Reason code (Põhjuse kood) otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="47c8e-113">In the Reason code field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="47c8e-114">Klõpsake loendis soovitud kirjel.</span><span class="sxs-lookup"><span data-stu-id="47c8e-114">In the list, click the desired record.</span></span>
9. <span data-ttu-id="47c8e-115">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="47c8e-115">Click Save.</span></span>
10. <span data-ttu-id="47c8e-116">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="47c8e-116">Click Add line.</span></span>
    * <span data-ttu-id="47c8e-117">Valikuline: kui soovite päises kuupäeva muuta, sisestage uus kuupäev.</span><span class="sxs-lookup"><span data-stu-id="47c8e-117">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="47c8e-118">See kuupäev määrab rahdnusperioodi, millesse eelarve salvestatakse.</span><span class="sxs-lookup"><span data-stu-id="47c8e-118">This date determines the fiscal period that the budget will be recorded to.</span></span> <span data-ttu-id="47c8e-119">Ülesannete juhendi kuvamisel teiste väljade täitmiseks klõpsake lehe ülaosas valikut Unlock (Vabasta lukust).</span><span class="sxs-lookup"><span data-stu-id="47c8e-119">When viewing the task guide, to fill out other fields, click Unlock at the top of the page.</span></span>  
11. <span data-ttu-id="47c8e-120">Klõpsake väljal Konto struktuur otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="47c8e-120">In the Account structure field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="47c8e-121">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="47c8e-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="47c8e-122">Täpsustage väljal Dimension values (Dimensiooni väärtused) soovitud väärtused.</span><span class="sxs-lookup"><span data-stu-id="47c8e-122">In the Dimension values field, specify the desired values.</span></span>
14. <span data-ttu-id="47c8e-123">Sisestage number väljale Summa.</span><span class="sxs-lookup"><span data-stu-id="47c8e-123">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="47c8e-124">Saate sisestada ka summa tüübi.</span><span class="sxs-lookup"><span data-stu-id="47c8e-124">You can also enter an amount type.</span></span>  
15. <span data-ttu-id="47c8e-125">Klõpsake väljal Valuuta otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="47c8e-125">In the Currency field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="47c8e-126">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="47c8e-126">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="47c8e-127">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="47c8e-127">Click Save.</span></span>
18. <span data-ttu-id="47c8e-128">Klõpsake Update budget balances (Värskenda eelarve tasakaalud).</span><span class="sxs-lookup"><span data-stu-id="47c8e-128">Click Update budget balances.</span></span>
19. <span data-ttu-id="47c8e-129">Klõpsake käsku Uuenda.</span><span class="sxs-lookup"><span data-stu-id="47c8e-129">Click Update.</span></span>
    * <span data-ttu-id="47c8e-130">Uuendamise tulemuste vaatamiseks klõpsake sinisel ribal valikut Message details (Teate üksikasjad).</span><span class="sxs-lookup"><span data-stu-id="47c8e-130">To see the results of the update, click Message details on the blue bar.</span></span>  

