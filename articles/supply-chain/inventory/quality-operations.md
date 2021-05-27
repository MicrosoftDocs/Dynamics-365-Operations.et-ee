---
title: MIttevastavuste toimingud
description: See teema kirjeldab, kuidas luua ja kasutada mittevastavuste toiminguid.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9a6cc88b80f82d77edac0341cb6a3c0db4b42ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022200"
---
# <a name="operations-for-nonconformances"></a><span data-ttu-id="c18a8-103">MIttevastavuste toimingud</span><span class="sxs-lookup"><span data-stu-id="c18a8-103">Operations for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c18a8-104">See teema kirjeldab, kuidas luua ja kasutada mittevastavuste toiminguid.</span><span class="sxs-lookup"><span data-stu-id="c18a8-104">This topic describes how to create and use operations for nonconformances.</span></span>

<span data-ttu-id="c18a8-105">Kasutage lehte **Toimingud** klassifikatsiooni määratlemiseks tööle, mida saab teha kinnitatud mittevastavuse puhul.</span><span class="sxs-lookup"><span data-stu-id="c18a8-105">You can use the **Operations** page to define classifications of the work that can be performed for an approved nonconformance.</span></span> <span data-ttu-id="c18a8-106">Kui määrate mittevastavusele seotud toimingu, saate pakkuda üksikasjalikku teavet, nagu teavet toimingu tegemiseks nõutava seotud materjali, töötundide ja toimingute lisakulude kohta.</span><span class="sxs-lookup"><span data-stu-id="c18a8-106">When you assign a related operation to a nonconformance, you can provide details such as the associated material, labor hours, and charges that are required to do the operation.</span></span> <span data-ttu-id="c18a8-107">Seda teavet kasutatakse toimingu eeldatava maksumuse arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="c18a8-107">The system uses this information to calculate an estimated cost for the operation.</span></span> <span data-ttu-id="c18a8-108">Üksikasjalikku teavet ja eeldatavat omahinda kasutatakse viitena.</span><span class="sxs-lookup"><span data-stu-id="c18a8-108">The detailed information and estimated costs are for reference.</span></span> <span data-ttu-id="c18a8-109">Kvaliteediga seotud toimingud erinevad toimingutest, mida saab määrata tootmisprotsessile.</span><span class="sxs-lookup"><span data-stu-id="c18a8-109">The related operations for quality differ from the operations that can be defined for a production route.</span></span>

> [!NOTE]
> <span data-ttu-id="c18a8-110">Ehkki saate jälgida mittevastavusega seotud operatsioonides kasutatavaid kulusid, aega ja kaupu, on teie sisestatavad andmed ainult formaalsed.</span><span class="sxs-lookup"><span data-stu-id="c18a8-110">Although you can track costs, time, and the items that are used in an operation that is related to a nonconformance, the data that you enter is only informational.</span></span> <span data-ttu-id="c18a8-111">See ei ole automaatselt integreeritud pearaamatu, varude alammooduli ega **Kellaaeg ja kohalviibimine** mooduliga.</span><span class="sxs-lookup"><span data-stu-id="c18a8-111">It isn't automatically integrated with the general ledger, inventory subledger, or the **Time and attendance** module.</span></span>

## <a name="examples-of-operations"></a><span data-ttu-id="c18a8-112">Toimingute näited</span><span class="sxs-lookup"><span data-stu-id="c18a8-112">Examples of operations</span></span>

<span data-ttu-id="c18a8-113">Te töötate tootmisettevõttes.</span><span class="sxs-lookup"><span data-stu-id="c18a8-113">You work for a manufacturing company.</span></span> <span data-ttu-id="c18a8-114">Mittevastavus loodi ja kiideti heaks kaupadele, mille kvaliteeditest ebaõnnestus.</span><span class="sxs-lookup"><span data-stu-id="c18a8-114">A nonconformance was created and approved for items that failed a quality test.</span></span> <span data-ttu-id="c18a8-115">Loodi parandus, mis näitas, et probleem oli seotud masina laagri veaga.</span><span class="sxs-lookup"><span data-stu-id="c18a8-115">A correction was created to indicate that the problem was related to a bad bearing on a machine.</span></span> <span data-ttu-id="c18a8-116">Selle laagri asendamiseks on vaja mitut etappi ja vastutust iga toimingu eest jälgitakse.</span><span class="sxs-lookup"><span data-stu-id="c18a8-116">Several steps are required to replace the bearing, and the responsibility for each operation is tracked.</span></span> <span data-ttu-id="c18a8-117">Näiteks võivad olla nõutavad järgmised sammud:</span><span class="sxs-lookup"><span data-stu-id="c18a8-117">For example, the following steps might be required:</span></span>

1. <span data-ttu-id="c18a8-118">Tootmisliin on peatatud ja teostatakse puhastamist.</span><span class="sxs-lookup"><span data-stu-id="c18a8-118">The production line is stopped, and the clean-out routine is performed.</span></span>
1. <span data-ttu-id="c18a8-119">Hoolduspersonal asendab laagri.</span><span class="sxs-lookup"><span data-stu-id="c18a8-119">Maintenance personnel replace the bearing.</span></span>
1. <span data-ttu-id="c18a8-120">Kvaliteedi tagamise personal kontrollib masinat enne selle tagasi sisselülitamist.</span><span class="sxs-lookup"><span data-stu-id="c18a8-120">Quality assurance personnel inspect the machine before it's turned back on.</span></span>

<span data-ttu-id="c18a8-121">Selle näite korral saab luua järgmisi toiminguid, mis tähistavad tööd, mida tuleb teha:</span><span class="sxs-lookup"><span data-stu-id="c18a8-121">For this example, the following operations can be created to represent the work that must be done:</span></span>

- <span data-ttu-id="c18a8-122">Peatage tootmisliin.</span><span class="sxs-lookup"><span data-stu-id="c18a8-122">Stop the production line.</span></span>
- <span data-ttu-id="c18a8-123">Tootmisliini puhastamine.</span><span class="sxs-lookup"><span data-stu-id="c18a8-123">Clean out the production line.</span></span>
- <span data-ttu-id="c18a8-124">Masina hoolduse tegemine.</span><span class="sxs-lookup"><span data-stu-id="c18a8-124">Perform machine maintenance.</span></span>
- <span data-ttu-id="c18a8-125">Kontrollige masinat.</span><span class="sxs-lookup"><span data-stu-id="c18a8-125">Inspect the machine.</span></span>

## <a name="create-an-operation"></a><span data-ttu-id="c18a8-126">Toimingu loomine</span><span class="sxs-lookup"><span data-stu-id="c18a8-126">Create an operation</span></span>

1. <span data-ttu-id="c18a8-127">Avage **Varude haldus \> Seadistus \> Kvaliteedijuhtimine \> Toimingud**.</span><span class="sxs-lookup"><span data-stu-id="c18a8-127">Go to **Inventory management \> Setup \> Quality management \> Operations**.</span></span>
1. <span data-ttu-id="c18a8-128">Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="c18a8-128">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="c18a8-129">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="c18a8-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="c18a8-130">**Toiming** – sisestage toimingu kordumatu kood või nimi.</span><span class="sxs-lookup"><span data-stu-id="c18a8-130">**Operation** – Enter a unique ID or name for the operation.</span></span>
    - <span data-ttu-id="c18a8-131">**Kirjeldus** – Sisestage toimingu detailne kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="c18a8-131">**Description** – Enter a detailed description of the operation.</span></span>
    - <span data-ttu-id="c18a8-132">**Tüüp** – Kui toimingut saab kasutada ainult mittevastavustega, mis on seotud kindlat tüüpi tellimusega, valige tellimuse tüüp (*Ostutellimus* või *Müügitellimus*).</span><span class="sxs-lookup"><span data-stu-id="c18a8-132">**Type** – If the operation can be used only with nonconformances that are related to a specific type of order, select the order type (*Purchase order* or *Sales order*).</span></span>

1. <span data-ttu-id="c18a8-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c18a8-133">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c18a8-134">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c18a8-134">Additional resources</span></span>

- [<span data-ttu-id="c18a8-135">Kvaliteedijuhtimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="c18a8-135">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="c18a8-136">Kvaliteedi ja mittevastavuse haldamise lubamine</span><span class="sxs-lookup"><span data-stu-id="c18a8-136">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="c18a8-137">Mittevastavuste loomine ja töötlemine</span><span class="sxs-lookup"><span data-stu-id="c18a8-137">Create and process nonconformances</span></span>](tasks/create-process-non-conformance.md)
- [<span data-ttu-id="c18a8-138">Mittevastavuste kinnitamise eest vastutavad töötajad</span><span class="sxs-lookup"><span data-stu-id="c18a8-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="c18a8-139">Mittevastavuste garantiitsoonid</span><span class="sxs-lookup"><span data-stu-id="c18a8-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="c18a8-140">Mittevastavuste diagnostika tüübid</span><span class="sxs-lookup"><span data-stu-id="c18a8-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="c18a8-141">Kvaliteeditasud mittevastavustele</span><span class="sxs-lookup"><span data-stu-id="c18a8-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="c18a8-142">Mittevastavuste probleemitüübid</span><span class="sxs-lookup"><span data-stu-id="c18a8-142">Problem types for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="c18a8-143">Laoprotsesside kvaliteedijuhtimine</span><span class="sxs-lookup"><span data-stu-id="c18a8-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
