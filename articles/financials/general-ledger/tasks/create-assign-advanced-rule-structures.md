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
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834884"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="cf9f1-103">Täpsemate reeglistruktuuride loomine ja määramine</span><span class="sxs-lookup"><span data-stu-id="cf9f1-103">Create and assign advanced rule structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cf9f1-104">Selles teemas selgitatakse, kuidas luua ja määrata täpsustatud reegli struktuuri konto struktuurile.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="cf9f1-105">Juhendis kasutatakse demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="cf9f1-106">Täpsema reegli struktuuri loomine</span><span class="sxs-lookup"><span data-stu-id="cf9f1-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="cf9f1-107">Avage **Navigeerimispaan > Pearaamat > Kontoplaan > Struktuurid > Täpsema reegli struktuurid**.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="cf9f1-108">Rippdialoogi avamiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="cf9f1-109">Sisestage väljale **Täpsema reegli struktuur** reegli struktuuri kirjeldav nimi.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="cf9f1-110">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-110">Select **OK**.</span></span>
5. <span data-ttu-id="cf9f1-111">Valige nupp **Lisa segment**.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="cf9f1-112">Valige segmentide loendist finantsdimensioon.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="cf9f1-113">Näiteks **Pood**.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="cf9f1-114">Valige nupp **Lisa segment**.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="cf9f1-115">Valige **Aktiveeri**.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="cf9f1-116">Täpsema reegli rakendamine konto struktuurile.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="cf9f1-117">Avage **Navigeerimispaan > Moodulid > Pearaamat > Kontoplaan > Struktuurid >Konfigureeri konto struktuurid**.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="cf9f1-118">Leidke ja valige loendist konto struktuur, millele soovite täpsema reegli rakendada.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="cf9f1-119">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-119">Select **Edit**.</span></span> <span data-ttu-id="cf9f1-120">Võite klõpsata ka suvandit **Täpsemad reeglid**, seejärel palutakse teil panna konto struktuur **mustandrežiimi**.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="cf9f1-121">Valige **Täpsemad reeglid**.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="cf9f1-122">Rippdialoogi avamiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="cf9f1-123">Sisestage väärtus väljale **Täpsem reegel**.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="cf9f1-124">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="cf9f1-125">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-125">Select **Create**.</span></span>
9. <span data-ttu-id="cf9f1-126">Valige **Lisa uus kriteerium**.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="cf9f1-127">Väljal **Kus** valige põhikonto või finantsdimensioon.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="cf9f1-128">Valige suvand väljal **Operaator**, näiteks **vahemikus** ja **hõlmab**.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="cf9f1-129">Sisestage väärtus väljale **Väärtus**.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="cf9f1-130">Sisestage väärtus väljale **Kuni**.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="cf9f1-131">Klõpsake valikut **Lisa** rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="cf9f1-132">Leidke loendis täpsema reegli struktuur, mida soovite kasutada, kui teie sisestatud kriteeriumid on täidetud.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="cf9f1-133">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-133">Select **Add**.</span></span>
17. <span data-ttu-id="cf9f1-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-134">Close the page.</span></span>
18. <span data-ttu-id="cf9f1-135">Valige **Aktiveeri**.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-135">Select **Activate**.</span></span>

