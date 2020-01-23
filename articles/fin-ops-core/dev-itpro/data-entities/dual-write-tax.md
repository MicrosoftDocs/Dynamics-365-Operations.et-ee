---
title: Integreeritud maks
description: Selles teemas kirjeldatakse maksuandmete integreerimist rakenduse Finance and Operationsi ja teenuse Common Data Service vahel.
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
ms.openlocfilehash: 86e74086a5a74c7af5f2572d1a653a1658d729c0
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853855"
---
# <a name="integrated-tax"></a><span data-ttu-id="882d4-103">Integreeritud maks</span><span class="sxs-lookup"><span data-stu-id="882d4-103">Integrated tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="882d4-104">Maksu seadistusandmed määravad nii kaudsete maksude (KM, GST, käibemaks) kui ka kinnipeetava maksu seadistuse.</span><span class="sxs-lookup"><span data-stu-id="882d4-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="882d4-105">Need kirjeldavad maksu arvutamise reeglit, maksumäära, maksuarvestust, tasakaalustust ja muid mõisteid.</span><span class="sxs-lookup"><span data-stu-id="882d4-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="882d4-106">Mallid</span><span class="sxs-lookup"><span data-stu-id="882d4-106">Templates</span></span>

<span data-ttu-id="882d4-107">Maksuandmed sisaldavad olemikaartide kogumit, mis töötavad andmete suhtluse ajal koos, nagu on näha järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="882d4-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="882d4-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="882d4-108">Finance and Operations</span></span>   | <span data-ttu-id="882d4-109">Muud Dynamics 365 rakendused</span><span class="sxs-lookup"><span data-stu-id="882d4-109">Other Dynamics 365 apps</span></span>
-------------------------|---------------------------------
<span data-ttu-id="882d4-110">Maksukoodid</span><span class="sxs-lookup"><span data-stu-id="882d4-110">Tax codes</span></span>                  | <span data-ttu-id="882d4-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="882d4-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="882d4-112">Maksugrupid</span><span class="sxs-lookup"><span data-stu-id="882d4-112">Tax groups</span></span>               | <span data-ttu-id="882d4-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="882d4-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="882d4-114">Maksu kaubagrupid</span><span class="sxs-lookup"><span data-stu-id="882d4-114">Tax item groups</span></span>          | <span data-ttu-id="882d4-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="882d4-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="882d4-116">Maksuvabastused</span><span class="sxs-lookup"><span data-stu-id="882d4-116">Tax Exemptions</span></span>           | <span data-ttu-id="882d4-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="882d4-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="882d4-118">Maksuhaldurid</span><span class="sxs-lookup"><span data-stu-id="882d4-118">Tax Authorities</span></span>          | <span data-ttu-id="882d4-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="882d4-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="882d4-120">Kinnipeetava maksu koodid</span><span class="sxs-lookup"><span data-stu-id="882d4-120">Withholding tax codes</span></span>      | <span data-ttu-id="882d4-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="882d4-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="882d4-122">Kinnipeetava maksugrupid</span><span class="sxs-lookup"><span data-stu-id="882d4-122">Withholding tax groups</span></span>   | <span data-ttu-id="882d4-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="882d4-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="882d4-124">Maksu pearaamatukonto grupp</span><span class="sxs-lookup"><span data-stu-id="882d4-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="882d4-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="882d4-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

