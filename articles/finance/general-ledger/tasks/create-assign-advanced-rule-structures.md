---
title: Täpsemate reeglistruktuuride loomine ja määramine
description: Selles teemas selgitatakse, kuidas luua ja määrata täpsustatud reegli struktuuri konto struktuurile.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cff07c13553ea140f537160da7f93820d5e3f77a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175389"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="e586c-103">Täpsemate reeglistruktuuride loomine ja määramine</span><span class="sxs-lookup"><span data-stu-id="e586c-103">Create and assign advanced rule structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e586c-104">Selles teemas selgitatakse, kuidas luua ja määrata täpsustatud reegli struktuuri konto struktuurile.</span><span class="sxs-lookup"><span data-stu-id="e586c-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="e586c-105">Juhendis kasutatakse demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="e586c-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="e586c-106">Täpsema reegli struktuuri loomine</span><span class="sxs-lookup"><span data-stu-id="e586c-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="e586c-107">Avage **Navigeerimispaan > Pearaamat > Kontoplaan > Struktuurid > Täpsema reegli struktuurid**.</span><span class="sxs-lookup"><span data-stu-id="e586c-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="e586c-108">Rippdialoogi avamiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e586c-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="e586c-109">Sisestage väljale **Täpsema reegli struktuur** reegli struktuuri kirjeldav nimi.</span><span class="sxs-lookup"><span data-stu-id="e586c-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="e586c-110">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e586c-110">Select **OK**.</span></span>
5. <span data-ttu-id="e586c-111">Valige nupp **Lisa segment**.</span><span class="sxs-lookup"><span data-stu-id="e586c-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="e586c-112">Valige segmentide loendist finantsdimensioon.</span><span class="sxs-lookup"><span data-stu-id="e586c-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="e586c-113">Näiteks **Pood**.</span><span class="sxs-lookup"><span data-stu-id="e586c-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="e586c-114">Valige nupp **Lisa segment**.</span><span class="sxs-lookup"><span data-stu-id="e586c-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="e586c-115">Valige **Aktiveeri**.</span><span class="sxs-lookup"><span data-stu-id="e586c-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="e586c-116">Täpsema reegli rakendamine konto struktuurile.</span><span class="sxs-lookup"><span data-stu-id="e586c-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="e586c-117">Avage **Navigeerimispaan > Moodulid > Pearaamat > Kontoplaan > Struktuurid >Konfigureeri konto struktuurid**.</span><span class="sxs-lookup"><span data-stu-id="e586c-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="e586c-118">Leidke ja valige loendist konto struktuur, millele soovite täpsema reegli rakendada.</span><span class="sxs-lookup"><span data-stu-id="e586c-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="e586c-119">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="e586c-119">Select **Edit**.</span></span> <span data-ttu-id="e586c-120">Võite klõpsata ka suvandit **Täpsemad reeglid**, seejärel palutakse teil panna konto struktuur **mustandrežiimi**.</span><span class="sxs-lookup"><span data-stu-id="e586c-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="e586c-121">Valige **Täpsemad reeglid**.</span><span class="sxs-lookup"><span data-stu-id="e586c-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="e586c-122">Rippdialoogi avamiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e586c-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="e586c-123">Sisestage väärtus väljale **Täpsem reegel**.</span><span class="sxs-lookup"><span data-stu-id="e586c-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="e586c-124">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="e586c-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="e586c-125">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="e586c-125">Select **Create**.</span></span>
9. <span data-ttu-id="e586c-126">Valige **Lisa uus kriteerium**.</span><span class="sxs-lookup"><span data-stu-id="e586c-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="e586c-127">Väljal **Kus** valige põhikonto või finantsdimensioon.</span><span class="sxs-lookup"><span data-stu-id="e586c-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="e586c-128">Valige suvand väljal **Operaator**, näiteks **vahemikus** ja **hõlmab**.</span><span class="sxs-lookup"><span data-stu-id="e586c-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="e586c-129">Sisestage väärtus väljale **Väärtus**.</span><span class="sxs-lookup"><span data-stu-id="e586c-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="e586c-130">Sisestage väärtus väljale **Kuni**.</span><span class="sxs-lookup"><span data-stu-id="e586c-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="e586c-131">Klõpsake valikut **Lisa** rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="e586c-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="e586c-132">Leidke loendis täpsema reegli struktuur, mida soovite kasutada, kui teie sisestatud kriteeriumid on täidetud.</span><span class="sxs-lookup"><span data-stu-id="e586c-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="e586c-133">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="e586c-133">Select **Add**.</span></span>
17. <span data-ttu-id="e586c-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e586c-134">Close the page.</span></span>
18. <span data-ttu-id="e586c-135">Valige **Aktiveeri**.</span><span class="sxs-lookup"><span data-stu-id="e586c-135">Select **Activate**.</span></span>

