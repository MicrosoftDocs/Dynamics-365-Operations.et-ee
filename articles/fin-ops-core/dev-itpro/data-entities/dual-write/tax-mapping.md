---
title: Integreeritud maks
description: Selles teemas kirjeldatakse maksuandmete integreerimist rakenduse Finance and Operations ja teenuse Dataverse vahel.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a7992520b57b4c19b6dc8e13bd8e9ffc87b40f5a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750638"
---
# <a name="integrated-tax"></a><span data-ttu-id="ef94f-103">Integreeritud maks</span><span class="sxs-lookup"><span data-stu-id="ef94f-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="ef94f-104">Maksu seadistusandmed määravad nii kaudsete maksude (KM, GST, käibemaks) kui ka kinnipeetava maksu seadistuse.</span><span class="sxs-lookup"><span data-stu-id="ef94f-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="ef94f-105">Need kirjeldavad maksu arvutamise reeglit, maksumäära, maksuarvestust, tasakaalustust ja muid mõisteid.</span><span class="sxs-lookup"><span data-stu-id="ef94f-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="ef94f-106">Mallid</span><span class="sxs-lookup"><span data-stu-id="ef94f-106">Templates</span></span>

<span data-ttu-id="ef94f-107">Maksuandmed sisaldavad tabeli kaartide kogumit, mis töötavad andmete suhtluse ajal koos, nagu on näha järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="ef94f-107">Tax data includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="ef94f-108">Finance and Operations rakendused</span><span class="sxs-lookup"><span data-stu-id="ef94f-108">Finance and Operations apps</span></span> | <span data-ttu-id="ef94f-109">Mudeljuhitud Dynamics 365 rakendused</span><span class="sxs-lookup"><span data-stu-id="ef94f-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="ef94f-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ef94f-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="ef94f-111">Kauba käibemaksugrupp</span><span class="sxs-lookup"><span data-stu-id="ef94f-111">Item sales tax group</span></span> | <span data-ttu-id="ef94f-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="ef94f-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="ef94f-113">Käibemaksuhaldurid</span><span class="sxs-lookup"><span data-stu-id="ef94f-113">Sales tax authorities</span></span> | <span data-ttu-id="ef94f-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="ef94f-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="ef94f-115">Käibemaksuvabastuse koodi olemi CDS</span><span class="sxs-lookup"><span data-stu-id="ef94f-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="ef94f-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="ef94f-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="ef94f-117">Käibemaksugrupid</span><span class="sxs-lookup"><span data-stu-id="ef94f-117">Sales tax groups</span></span> | <span data-ttu-id="ef94f-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="ef94f-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="ef94f-119">Käibemaksu pearaamatu sisestusgrupid V2</span><span class="sxs-lookup"><span data-stu-id="ef94f-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="ef94f-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="ef94f-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="ef94f-121">Kinnipeetava maksu koodid</span><span class="sxs-lookup"><span data-stu-id="ef94f-121">Withholding tax codes</span></span> | <span data-ttu-id="ef94f-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="ef94f-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="ef94f-123">Kinnipeetava maksugrupid</span><span class="sxs-lookup"><span data-stu-id="ef94f-123">Withholding tax groups</span></span> | <span data-ttu-id="ef94f-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="ef94f-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]