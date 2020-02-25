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
ms.openlocfilehash: 0d32a5f7859f0200da823a73d94b9a6b2a9c8e7d
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019736"
---
# <a name="integrated-tax"></a><span data-ttu-id="6f9d0-103">Integreeritud maks</span><span class="sxs-lookup"><span data-stu-id="6f9d0-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="6f9d0-104">Maksu seadistusandmed määravad nii kaudsete maksude (KM, GST, käibemaks) kui ka kinnipeetava maksu seadistuse.</span><span class="sxs-lookup"><span data-stu-id="6f9d0-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="6f9d0-105">Need kirjeldavad maksu arvutamise reeglit, maksumäära, maksuarvestust, tasakaalustust ja muid mõisteid.</span><span class="sxs-lookup"><span data-stu-id="6f9d0-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="6f9d0-106">Mallid</span><span class="sxs-lookup"><span data-stu-id="6f9d0-106">Templates</span></span>

<span data-ttu-id="6f9d0-107">Maksuandmed sisaldavad olemikaartide kogumit, mis töötavad andmete suhtluse ajal koos, nagu on näha järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="6f9d0-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="6f9d0-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6f9d0-108">Finance and Operations</span></span>   | <span data-ttu-id="6f9d0-109">Muud Dynamics 365 rakendused</span><span class="sxs-lookup"><span data-stu-id="6f9d0-109">Other Dynamics 365 apps</span></span>
-------------------------|---------------------------------
<span data-ttu-id="6f9d0-110">Maksukoodid</span><span class="sxs-lookup"><span data-stu-id="6f9d0-110">Tax codes</span></span>                  | <span data-ttu-id="6f9d0-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="6f9d0-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="6f9d0-112">Maksugrupid</span><span class="sxs-lookup"><span data-stu-id="6f9d0-112">Tax groups</span></span>               | <span data-ttu-id="6f9d0-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="6f9d0-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="6f9d0-114">Maksu kaubagrupid</span><span class="sxs-lookup"><span data-stu-id="6f9d0-114">Tax item groups</span></span>          | <span data-ttu-id="6f9d0-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="6f9d0-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="6f9d0-116">Maksuvabastused</span><span class="sxs-lookup"><span data-stu-id="6f9d0-116">Tax Exemptions</span></span>           | <span data-ttu-id="6f9d0-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="6f9d0-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="6f9d0-118">Maksuhaldurid</span><span class="sxs-lookup"><span data-stu-id="6f9d0-118">Tax Authorities</span></span>          | <span data-ttu-id="6f9d0-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="6f9d0-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="6f9d0-120">Kinnipeetava maksu koodid</span><span class="sxs-lookup"><span data-stu-id="6f9d0-120">Withholding tax codes</span></span>      | <span data-ttu-id="6f9d0-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="6f9d0-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="6f9d0-122">Kinnipeetava maksugrupid</span><span class="sxs-lookup"><span data-stu-id="6f9d0-122">Withholding tax groups</span></span>   | <span data-ttu-id="6f9d0-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="6f9d0-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="6f9d0-124">Maksu pearaamatukonto grupp</span><span class="sxs-lookup"><span data-stu-id="6f9d0-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="6f9d0-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="6f9d0-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

