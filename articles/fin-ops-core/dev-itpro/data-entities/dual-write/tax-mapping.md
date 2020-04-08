---
title: Integreeritud maks
description: Selles teemas kirjeldatakse maksuandmete integreerimist rakenduse Finance and Operations ja teenuse Common Data Service vahel.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a4da37d45698290b40f6c72148f1500bef72127a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173081"
---
# <a name="integrated-tax"></a><span data-ttu-id="17c0e-103">Integreeritud maks</span><span class="sxs-lookup"><span data-stu-id="17c0e-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="17c0e-104">Maksu seadistusandmed määravad nii kaudsete maksude (KM, GST, käibemaks) kui ka kinnipeetava maksu seadistuse.</span><span class="sxs-lookup"><span data-stu-id="17c0e-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="17c0e-105">Need kirjeldavad maksu arvutamise reeglit, maksumäära, maksuarvestust, tasakaalustust ja muid mõisteid.</span><span class="sxs-lookup"><span data-stu-id="17c0e-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="17c0e-106">Mallid</span><span class="sxs-lookup"><span data-stu-id="17c0e-106">Templates</span></span>

<span data-ttu-id="17c0e-107">Maksuandmed sisaldavad olemikaartide kogumit, mis töötavad andmete suhtluse ajal koos, nagu on näha järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="17c0e-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="17c0e-108">Finance and Operations rakendused</span><span class="sxs-lookup"><span data-stu-id="17c0e-108">Finance and Operations apps</span></span> | <span data-ttu-id="17c0e-109">Mudeljuhitud Dynamics 365 rakendused</span><span class="sxs-lookup"><span data-stu-id="17c0e-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="17c0e-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="17c0e-110">Description</span></span> |
-------------------------|---------------------------------
<span data-ttu-id="17c0e-111">Maksukoodid</span><span class="sxs-lookup"><span data-stu-id="17c0e-111">Tax codes</span></span>                   | <span data-ttu-id="17c0e-112">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="17c0e-112">msdyn\_taxcodes.md</span></span> | 
<span data-ttu-id="17c0e-113">Maksugrupid</span><span class="sxs-lookup"><span data-stu-id="17c0e-113">Tax groups</span></span>                 | <span data-ttu-id="17c0e-114">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="17c0e-114">msdyn\_taxgroups.md</span></span> | 
<span data-ttu-id="17c0e-115">Maksu kaubagrupid</span><span class="sxs-lookup"><span data-stu-id="17c0e-115">Tax item groups</span></span>             | <span data-ttu-id="17c0e-116">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="17c0e-116">msdyn\_taxitemgroups.md</span></span> | 
<span data-ttu-id="17c0e-117">Maksuvabastused</span><span class="sxs-lookup"><span data-stu-id="17c0e-117">Tax Exemptions</span></span>             | <span data-ttu-id="17c0e-118">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="17c0e-118">msdyn\_taxexemptcodes.md</span></span> | 
<span data-ttu-id="17c0e-119">Maksuhaldurid</span><span class="sxs-lookup"><span data-stu-id="17c0e-119">Tax Authorities</span></span>             | <span data-ttu-id="17c0e-120">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="17c0e-120">msdyn\_taxauthorities.md</span></span> | 
<span data-ttu-id="17c0e-121">Kinnipeetava maksu koodid</span><span class="sxs-lookup"><span data-stu-id="17c0e-121">Withholding tax codes</span></span>       | <span data-ttu-id="17c0e-122">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="17c0e-122">msdyn\_withholdingtaxcodes.md</span></span> | 
<span data-ttu-id="17c0e-123">Kinnipeetava maksugrupid</span><span class="sxs-lookup"><span data-stu-id="17c0e-123">Withholding tax groups</span></span>     | <span data-ttu-id="17c0e-124">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="17c0e-124">msdyn\_withholdingtaxgroups.md</span></span> | 
<span data-ttu-id="17c0e-125">Maksu pearaamatukonto grupp</span><span class="sxs-lookup"><span data-stu-id="17c0e-125">Tax Ledger Account Group</span></span> | <span data-ttu-id="17c0e-126">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="17c0e-126">msdyn\_taxpostinggroups</span></span>     | 

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

