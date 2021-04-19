---
title: Veose automaatse vastavusseviimise seadistamine
description: See protseduur näitab, kuidas seadistada andmeid veose automaatseks vastavusseviimiseks.
author: ShylaThompson
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4bc3998dea2e953191151f8e54345ec648ff33e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837605"
---
# <a name="set-up-automatic-freight-reconciliation"></a><span data-ttu-id="6ca98-103">Veose automaatse vastavusseviimise seadistamine</span><span class="sxs-lookup"><span data-stu-id="6ca98-103">Set up automatic freight reconciliation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6ca98-104">See protseduur näitab, kuidas seadistada andmeid veose automaatseks vastavusseviimiseks.</span><span class="sxs-lookup"><span data-stu-id="6ca98-104">This procedure shows how to set up data for automatic freight reconciliation.</span></span> <span data-ttu-id="6ca98-105">Sellega tegeleb tavaliselt laohaldur.</span><span class="sxs-lookup"><span data-stu-id="6ca98-105">This is typically done by a warehouse manager.</span></span> <span data-ttu-id="6ca98-106">Saate seda protseduuri kasutada demoandmete ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="6ca98-106">You can use this procedure in demo data company USMF.</span></span>


## <a name="set-up-the-freight-bill-type"></a><span data-ttu-id="6ca98-107">Veoarve tüübi seadistamine</span><span class="sxs-lookup"><span data-stu-id="6ca98-107">Set up the freight bill type</span></span>
1. <span data-ttu-id="6ca98-108">Avage Transpordihaldus > Seadistus > Veose vastavusseviimine > Veoarve tüüp.</span><span class="sxs-lookup"><span data-stu-id="6ca98-108">Go to Transportation management > Setup > Freight reconciliation > Freight bill type.</span></span>
    * <span data-ttu-id="6ca98-109">Veoarve tüüp määratleb, kuidas veoarveid ja vedaja arveid tuleks vastendada.</span><span class="sxs-lookup"><span data-stu-id="6ca98-109">The freight bill type defines how freight bills and carrier invoices  should be matched.</span></span>  
2. <span data-ttu-id="6ca98-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6ca98-110">Click New.</span></span>
3. <span data-ttu-id="6ca98-111">Tippige väärtus väljale Veoarve tüüp.</span><span class="sxs-lookup"><span data-stu-id="6ca98-111">In the Freight bill type field, type a value.</span></span>
4. <span data-ttu-id="6ca98-112">Tippige väljale Mootori koost Microsoft.Dynamics.Ax.Tms.dll.</span><span class="sxs-lookup"><span data-stu-id="6ca98-112">In the Engine assembly field, type 'Microsoft.Dynamics.Ax.Tms.dll'.</span></span>
    * <span data-ttu-id="6ca98-113">See on standardne transpordihalduse vastendusmootori koodi teek.</span><span class="sxs-lookup"><span data-stu-id="6ca98-113">This is the standard Transportation management matching engine code library.</span></span>  
5. <span data-ttu-id="6ca98-114">Tippige väljale Mootori klass Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer.</span><span class="sxs-lookup"><span data-stu-id="6ca98-114">In the Engine class field, type 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.</span></span>
    * <span data-ttu-id="6ca98-115">See on standardne transpordihalduse vastendusmootori klass.</span><span class="sxs-lookup"><span data-stu-id="6ca98-115">This is the standard Transportation management matching engine class.</span></span>  
6. <span data-ttu-id="6ca98-116">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6ca98-116">Click New.</span></span>
7. <span data-ttu-id="6ca98-117">Valige väljalt Kirjeldus väärtus, mis peaks veoarvel ja vedaja arvel ühtima.</span><span class="sxs-lookup"><span data-stu-id="6ca98-117">In the Description field, choose the value that should match on the freight bill and the carrier invoice.</span></span>  
8. <span data-ttu-id="6ca98-118">Valige Jah väljalt Sobitus on nõutav.</span><span class="sxs-lookup"><span data-stu-id="6ca98-118">In the Match required field, select 'Yes'.</span></span>
    * <span data-ttu-id="6ca98-119">Kui määrate selle välja väärtuseks Jah, siis tähendab see, et väljal Kirjeldus valitud väärtus peab olema vastav nii veoarvel kui ka vedaja arvel.</span><span class="sxs-lookup"><span data-stu-id="6ca98-119">If you set this field to Yes this means that the value selected in the Description field needs to match on both the freight bill and the carrier invoice.</span></span> <span data-ttu-id="6ca98-120">Kui määrate väärtuseks Ei, võib ühel neist see väli tühi olla.</span><span class="sxs-lookup"><span data-stu-id="6ca98-120">If you set it to No, the field can be blank on one of these.</span></span>  
9. <span data-ttu-id="6ca98-121">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6ca98-121">Click Save.</span></span>

## <a name="set-up-the-freight-bill-type-assignment"></a><span data-ttu-id="6ca98-122">Veoarve tüübi määramise seadistamine</span><span class="sxs-lookup"><span data-stu-id="6ca98-122">Set up the freight bill type assignment</span></span>
1. <span data-ttu-id="6ca98-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6ca98-123">Close the page.</span></span>
2. <span data-ttu-id="6ca98-124">Avage Transpordihaldus > Seadistus > Veose vastavusseviimine > Veoarve tüübi määramised.</span><span class="sxs-lookup"><span data-stu-id="6ca98-124">Go to Transportation management > Setup > Freight reconciliation > Freight bill type assignments.</span></span>
    * <span data-ttu-id="6ca98-125">Veoarve tüübi määrangut kasutatakse määramiseks, millist veoarve tüüpi konkreetse vedaja puhul kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="6ca98-125">The freight bill type assignment is used to specify which freight bill type is used for a particular carrier.</span></span>   
3. <span data-ttu-id="6ca98-126">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6ca98-126">Click New.</span></span>
4. <span data-ttu-id="6ca98-127">Valige või sisestage väärtus väljal Režiim.</span><span class="sxs-lookup"><span data-stu-id="6ca98-127">In the Mode field, enter or select a value.</span></span>
5. <span data-ttu-id="6ca98-128">Valige või sisestage väärtus väljal Kättetoimetaja.</span><span class="sxs-lookup"><span data-stu-id="6ca98-128">In the Shipping carrier field, enter or select a value.</span></span>
6. <span data-ttu-id="6ca98-129">Valige väljalt Veoarve tüüp varem loodud veoarve tüüp.</span><span class="sxs-lookup"><span data-stu-id="6ca98-129">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
7. <span data-ttu-id="6ca98-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6ca98-130">Close the page.</span></span>

## <a name="set-up-the-audit-master"></a><span data-ttu-id="6ca98-131">Auditi koondi seadistamine</span><span class="sxs-lookup"><span data-stu-id="6ca98-131">Set up the audit master</span></span>
1. <span data-ttu-id="6ca98-132">Avage Transpordihaldus > Seadistus > Veose vastavusseviimine > Auditi koond.</span><span class="sxs-lookup"><span data-stu-id="6ca98-132">Go to Transportation management > Setup > Freight reconciliation > Audit master.</span></span>
    * <span data-ttu-id="6ca98-133">Auditi koond määratleb automaatne veose vastavusseviimise lubatud hälbe.</span><span class="sxs-lookup"><span data-stu-id="6ca98-133">The audit master defines the tolerance limits for automatic freight reconciliation.</span></span> <span data-ttu-id="6ca98-134">See määrab kui palju veoarve ja vedaja arve rahasummad võivad erineda, et vastavusseviimine siiski toimuda saaks.</span><span class="sxs-lookup"><span data-stu-id="6ca98-134">It specifies by how much the monetary amounts on the freight bill and the carrier invoice can differ and still allow reconciliation to occur.</span></span> <span data-ttu-id="6ca98-135">See määratleb ka lahknevuste käsitlemise viisi.</span><span class="sxs-lookup"><span data-stu-id="6ca98-135">It also defines how to handle discrepancies.</span></span>  
2. <span data-ttu-id="6ca98-136">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6ca98-136">Click New.</span></span>
3. <span data-ttu-id="6ca98-137">Tippige väärtus väljale Auditi koondi ID.</span><span class="sxs-lookup"><span data-stu-id="6ca98-137">In the Audit master ID field, type a value.</span></span>
4. <span data-ttu-id="6ca98-138">Valige väljalt Kättetoimetaja sama kättetoimetaja, kelle varem valisite.</span><span class="sxs-lookup"><span data-stu-id="6ca98-138">In the Shipping carrier  field, select the same shipping carrier as you did earlier.</span></span>
5. <span data-ttu-id="6ca98-139">Valige väljalt Veoarve tüüp varem loodud veoarve tüüp.</span><span class="sxs-lookup"><span data-stu-id="6ca98-139">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
6. <span data-ttu-id="6ca98-140">Laiendage jaotist Hälve.</span><span class="sxs-lookup"><span data-stu-id="6ca98-140">Expand the Tolerance section.</span></span>
7. <span data-ttu-id="6ca98-141">Sisestage number väljale Minimaalne lubatud hälbe tase.</span><span class="sxs-lookup"><span data-stu-id="6ca98-141">In the Minimum tolerance level field, enter a number.</span></span>
8. <span data-ttu-id="6ca98-142">Sisestage number väljale Maksimaalne lubatud hälbe tase.</span><span class="sxs-lookup"><span data-stu-id="6ca98-142">In the Maximum tolerance level field, enter a number.</span></span>
9. <span data-ttu-id="6ca98-143">Laiendage jaotist Tulemus.</span><span class="sxs-lookup"><span data-stu-id="6ca98-143">Expand the Result section.</span></span>
10. <span data-ttu-id="6ca98-144">Valige või sisestage väärtus väljal Ülemakse põhjuse kood.</span><span class="sxs-lookup"><span data-stu-id="6ca98-144">In the Overpayment reason code field, enter or select a value.</span></span>
    * <span data-ttu-id="6ca98-145">Kui summad on veoarvel ja vedaja arvel erinevad, määratlevad üle- ja alamakse põhjuse koodid kontod, millel vahe tuleks registreerida, kuni vahe on lubatud hälbe piirides.</span><span class="sxs-lookup"><span data-stu-id="6ca98-145">If the monetary amounts differ on the freight bill and the carrier invoice, the overpayment and underpayment reason codes specify the accounts that the difference should be registered on, as long as the difference is within the tolerance levels.</span></span>  
11. <span data-ttu-id="6ca98-146">Valige või sisestage väärtus väljal Alamakse põhjuse kood.</span><span class="sxs-lookup"><span data-stu-id="6ca98-146">In the Underpayment reason code field, enter or select a value.</span></span>
12. <span data-ttu-id="6ca98-147">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6ca98-147">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]