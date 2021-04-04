---
title: Algse eelarve loomine ja seejärel esialgse eelarve kirjete tagasivõtmine avalikus sektoris
description: See teema kirjeldab, kuidas luua ja tühistada algset eelarvekirjet, kasutades eelarvemudelit ja dimensiooniväärtusi, mis hõlmavad esialgseid eelarvesummasid.
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
ms.openlocfilehash: 0b11aeb377caf50808f661de25fcbbf90429d475
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235061"
---
# <a name="create-an-original-budget-and-then-reverse-preliminary-budget-entries-in-the-public-sector"></a><span data-ttu-id="aa4d1-103">Algse eelarve loomine ja seejärel esialgse eelarve kirjete tagasivõtmine avalikus sektoris</span><span class="sxs-lookup"><span data-stu-id="aa4d1-103">Create an original budget and then reverse preliminary budget entries in the public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aa4d1-104">Kui luuakse algse eelarve kande ja mida kasutatakse eelarve mudel ja dimensiooni väärtused, mis sisaldavad esialgses eelarvesummad, esialgsete eelarvesummade saab tühistada.</span><span class="sxs-lookup"><span data-stu-id="aa4d1-104">When you create an original budget entry and use the budget model and dimension values that contain preliminary budget amounts, the preliminary budget amounts can be reversed.</span></span> <span data-ttu-id="aa4d1-105">See protseduur loodi PSUS-ettevõtte demoandmetega avaliku sektori sektsioonis.</span><span class="sxs-lookup"><span data-stu-id="aa4d1-105">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="aa4d1-106">Tehke valik Eelarvestamine > Eelarveregistri kirjed.</span><span class="sxs-lookup"><span data-stu-id="aa4d1-106">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="aa4d1-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="aa4d1-107">Click New.</span></span>
3. <span data-ttu-id="aa4d1-108">Klõpsake väljal Budget model (Eelarve mudel) otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="aa4d1-108">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="aa4d1-109">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="aa4d1-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="aa4d1-110">Klõpsake väljal Budget code (Eelarve kood) otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="aa4d1-110">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="aa4d1-111">Klõpsake loendis valikut Original budget (Algne eelarve).</span><span class="sxs-lookup"><span data-stu-id="aa4d1-111">In the list, click Original budget.</span></span>
7. <span data-ttu-id="aa4d1-112">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="aa4d1-112">Click Save.</span></span>
8. <span data-ttu-id="aa4d1-113">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="aa4d1-113">Click Add line.</span></span>
9. <span data-ttu-id="aa4d1-114">Valikuline: kui soovite päises kuupäeva muuta, sisestage uus kuupäev.</span><span class="sxs-lookup"><span data-stu-id="aa4d1-114">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="aa4d1-115">See kuupäev määrab rahdnusperioodi, millesse eelarve salvestatakse.</span><span class="sxs-lookup"><span data-stu-id="aa4d1-115">This date determines the fiscal period that the budget will be recorded to.</span></span>
10. <span data-ttu-id="aa4d1-116">Klõpsake väljal Konto struktuur otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="aa4d1-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="aa4d1-117">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="aa4d1-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="aa4d1-118">Täpsustage väljal Dimension values (Dimensiooni väärtused) soovitud väärtused.</span><span class="sxs-lookup"><span data-stu-id="aa4d1-118">In the Dimension values field, specify the desired values.</span></span>
13. <span data-ttu-id="aa4d1-119">Sisestage number väljale Summa.</span><span class="sxs-lookup"><span data-stu-id="aa4d1-119">In the Amount field, enter a number.</span></span>
14. <span data-ttu-id="aa4d1-120">Klõpsake väljal Valuuta otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="aa4d1-120">In the Currency field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="aa4d1-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="aa4d1-121">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="aa4d1-122">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="aa4d1-122">Click Save.</span></span>
17. <span data-ttu-id="aa4d1-123">Klõpsake Update budget balances (Värskenda eelarve tasakaalud).</span><span class="sxs-lookup"><span data-stu-id="aa4d1-123">Click Update budget balances.</span></span>
    * <span data-ttu-id="aa4d1-124">Valikuline: Saate valida suvandi Reverse preliminary budget (Tühista esialgne eelarve).</span><span class="sxs-lookup"><span data-stu-id="aa4d1-124">Optional: You can select the Reverse preliminary budget option.</span></span> <span data-ttu-id="aa4d1-125">Pange tähele, et saate tühistada kõik esialgsed eelarvekanded või ainult teie poolt täpsustatud eelarvekoodiga esialgsed eelarvekanded.</span><span class="sxs-lookup"><span data-stu-id="aa4d1-125">Note that you can reverse all preliminary budget entries, or only the preliminary budget entries that have the budget code that you specify.</span></span>  
    * <span data-ttu-id="aa4d1-126">Lisavalikute tegemiseks klõpsake lehe ülaosas ikooni Unlock (Vabasta lukust).</span><span class="sxs-lookup"><span data-stu-id="aa4d1-126">To make optional selections, click the Unlock icon at the top of the page.</span></span>  
18. <span data-ttu-id="aa4d1-127">Klõpsake käsku Uuenda.</span><span class="sxs-lookup"><span data-stu-id="aa4d1-127">Click Update.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]