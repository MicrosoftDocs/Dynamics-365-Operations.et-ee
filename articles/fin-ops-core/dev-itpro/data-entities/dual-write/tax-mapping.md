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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 26818ceace7d2b7e7c3ed4d0bb0bd9ab2e884aba
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997596"
---
# <a name="integrated-tax"></a><span data-ttu-id="803a4-103">Integreeritud maks</span><span class="sxs-lookup"><span data-stu-id="803a4-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="803a4-104">Maksu seadistusandmed määravad nii kaudsete maksude (KM, GST, käibemaks) kui ka kinnipeetava maksu seadistuse.</span><span class="sxs-lookup"><span data-stu-id="803a4-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="803a4-105">Need kirjeldavad maksu arvutamise reeglit, maksumäära, maksuarvestust, tasakaalustust ja muid mõisteid.</span><span class="sxs-lookup"><span data-stu-id="803a4-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="803a4-106">Mallid</span><span class="sxs-lookup"><span data-stu-id="803a4-106">Templates</span></span>

<span data-ttu-id="803a4-107">Maksuandmed sisaldavad olemikaartide kogumit, mis töötavad andmete suhtluse ajal koos, nagu on näha järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="803a4-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="803a4-108">Finance and Operations rakendused</span><span class="sxs-lookup"><span data-stu-id="803a4-108">Finance and Operations apps</span></span> | <span data-ttu-id="803a4-109">Mudeljuhitud Dynamics 365 rakendused</span><span class="sxs-lookup"><span data-stu-id="803a4-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="803a4-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="803a4-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="803a4-111">Kauba käibemaksugrupp</span><span class="sxs-lookup"><span data-stu-id="803a4-111">Item sales tax group</span></span> | <span data-ttu-id="803a4-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="803a4-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="803a4-113">Käibemaksuhaldurid</span><span class="sxs-lookup"><span data-stu-id="803a4-113">Sales tax authorities</span></span> | <span data-ttu-id="803a4-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="803a4-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="803a4-115">Käibemaksuvabastuse koodi olemi CDS</span><span class="sxs-lookup"><span data-stu-id="803a4-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="803a4-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="803a4-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="803a4-117">Käibemaksugrupid</span><span class="sxs-lookup"><span data-stu-id="803a4-117">Sales tax groups</span></span> | <span data-ttu-id="803a4-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="803a4-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="803a4-119">Käibemaksu pearaamatu sisestusgrupid V2</span><span class="sxs-lookup"><span data-stu-id="803a4-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="803a4-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="803a4-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="803a4-121">Kinnipeetava maksu koodid</span><span class="sxs-lookup"><span data-stu-id="803a4-121">Withholding tax codes</span></span> | <span data-ttu-id="803a4-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="803a4-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="803a4-123">Kinnipeetava maksugrupid</span><span class="sxs-lookup"><span data-stu-id="803a4-123">Withholding tax groups</span></span> | <span data-ttu-id="803a4-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="803a4-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

