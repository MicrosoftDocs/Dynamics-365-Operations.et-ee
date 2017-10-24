---
title: "Toodetavate või hangitavate toodete seadistamine"
description: "Tooteid saab hankida mitmel viisil: neid saab toota (valmistada) või hankida (osta). See artikkel kirjeldab mõnda tüüpilist punkti, mida arvestada, kui konfigureerite tooteid mitme allhanke toetamiseks."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6a11167e2ae2597356ca0e8c0fc8ac8417f3a5bf
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-products-that-can-be-produced-or-procured"></a><span data-ttu-id="124a2-104">Toodetavate või hangitavate toodete seadistamine</span><span class="sxs-lookup"><span data-stu-id="124a2-104">Set up products that can be produced or procured</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="124a2-105">Tooteid saab hankida mitmel viisil: neid saab toota (valmistada) või hankida (osta).</span><span class="sxs-lookup"><span data-stu-id="124a2-105">Products can be sourced in various ways -  they can be produced (manufactured) or procured (purchased).</span></span> <span data-ttu-id="124a2-106">See artikkel kirjeldab mõnda tüüpilist punkti, mida arvestada, kui konfigureerite tooteid mitme allhanke toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="124a2-106">This article describes some typical points to consider when you configure products to support multi-sourcing.</span></span> 

<span data-ttu-id="124a2-107">Mitme tarnijaga hanget kasutatakse tavaliselt harva toodetava kauba ostmiseks või juhul, kui peamiselt toodetud kaupa muudetakse, nii et nüüd on see peamiselt ostetav kaup.</span><span class="sxs-lookup"><span data-stu-id="124a2-107">Multi-sourcing is typically used for a purchased item that is occasionally manufactured, or when an item that was primarily a manufactured item is changed so that it's now primarily a purchased item.</span></span> <span data-ttu-id="124a2-108">Esmalt määratakse kaup toodetavaks kaubaks, et määratleda saaks koosluse- ja protsessiteabe ning toetada kauba tootmistellimusi.</span><span class="sxs-lookup"><span data-stu-id="124a2-108">The item is first designated as a manufactured item, so that bill of materials (BOM) and route information can be defined, and to support production orders for the item.</span></span> <span data-ttu-id="124a2-109">Tootmise tüübiks peab olema määratud **Kooslus** (tootmise töötlemiseks **Valem** või **Kaastoode**).</span><span class="sxs-lookup"><span data-stu-id="124a2-109">The production type should be set to **BOM** (or, for process manufacturing, **Formula** or **Co-Product**).</span></span>

<span data-ttu-id="124a2-110">Standardkulu kasutamisel saab toodetud kauba jaoks arvutada kauba kulukirje.</span><span class="sxs-lookup"><span data-stu-id="124a2-110">When you use standard cost, the item cost record can be calculated for the manufactured item.</span></span> <span data-ttu-id="124a2-111">Kauba kulukirje ei pruugi siiski ühtida standardkuluga, mida ostu puhul soovite.</span><span class="sxs-lookup"><span data-stu-id="124a2-111">However, the item cost record might not match the standard cost that you want for purchasing purposes.</span></span> <span data-ttu-id="124a2-112">Sellisel juhul tuleb soovitud standardkulu kauba kulukirje jaoks käsitsi sisestada ja aktiveerida.</span><span class="sxs-lookup"><span data-stu-id="124a2-112">In this case, the standard cost must be manually entered and activated for the item cost record.</span></span> <span data-ttu-id="124a2-113">Kuluarvutuseks kaaluge erikoosluse ja -protsessi kasutamist, mis esindaks toote tarnekombinatsiooni rahandusperioodi jooksul, et minimeerida aja jooksul hälbeid.</span><span class="sxs-lookup"><span data-stu-id="124a2-113">For the cost calculation, consider using a special BOM and route that represent the supply mix of the product over the course of a fiscal period, to minimize the variances over time.</span></span> <span data-ttu-id="124a2-114">Peale selle saab ühes tegevuskohas toodetud kauba üle kanda teise tegevuskohta.</span><span class="sxs-lookup"><span data-stu-id="124a2-114">Additionally, a manufactured item at one site can be transferred to another site.</span></span> <span data-ttu-id="124a2-115">Seetõttu tuleb kauba kulu käsitsi sisestada ja aktiveerida selle tegevuskoha puhul, kuhu kaup üle kantakse.</span><span class="sxs-lookup"><span data-stu-id="124a2-115">Therefore, the item's cost must be manually entered and activated for the site that the item is transferred to.</span></span> <span data-ttu-id="124a2-116">Kui kasutate toodetud kaupa kõrgema taseme toodete komponendina, tuleb komponendi kulusid käsitleda ostetud kaubana.</span><span class="sxs-lookup"><span data-stu-id="124a2-116">When you use the manufactured item as a component in higher-level products, the component's costs should be treated as a purchased item.</span></span> <span data-ttu-id="124a2-117">See juhis kehtib olenemata sellest, kas komponendi kulud on arvutatud või käsitsi sisestatud.</span><span class="sxs-lookup"><span data-stu-id="124a2-117">This guideline applies, regardless of whether the component’s costs were calculated or manually entered.</span></span> <span data-ttu-id="124a2-118">Teisisõnu tuleb koosluse arvutus käsitlema kauba kulusid ostetud komponendina, mitte kasutama kulude arvutamiseks kauba koosluse- ja protsessiteavet.</span><span class="sxs-lookup"><span data-stu-id="124a2-118">In other words, a BOM calculation should treat the item's costs as a purchased component instead of using the item's BOM and route information to calculate costs.</span></span> <span data-ttu-id="124a2-119">Arvutamise vältimiseks valige lipp **Peata koosnevusarvutus**, mis on manustatud kaubale määratud koosluse arvutamise grupile.</span><span class="sxs-lookup"><span data-stu-id="124a2-119">To prevent the calculation from occurring, select the **Stop explosion** flag that is embedded in the BOM calculation group that is assigned to the item.</span></span> <span data-ttu-id="124a2-120">Selleks et vältida kauba kaudu koondplaneerimise arvutusi koosnevusnõuetest, määrake kauba laovarudes või laovarude grupis koosnevuspiiriks 0 (null) päeva.</span><span class="sxs-lookup"><span data-stu-id="124a2-120">To prevent master scheduling calculations from exploding requirements through the item, set the explosion fence to 0 (zero) days in item coverage or in the coverage group.</span></span> <span data-ttu-id="124a2-121">Koondplaneerimise arvutus käsitleb siis kaupa ostetud kaubana ega tee kauba koosluse- ja protsessiteabe jaoks rohkem arvutusi.</span><span class="sxs-lookup"><span data-stu-id="124a2-121">The master scheduling calculation will then treat the item as a purchased item and won't perform more calculations for the item's BOM and route information.</span></span>






