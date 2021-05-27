---
title: Mittevastavuste garantiitsoonid
description: See teema kirjeldab, kuidas luua ja kasutada mittevastavuste garantiitsoone.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80f4b9dfc7882af4570bf1908784b8d114396402
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021800"
---
# <a name="quarantine-zones-for-nonconformances"></a><span data-ttu-id="81266-103">Mittevastavuste garantiitsoonid</span><span class="sxs-lookup"><span data-stu-id="81266-103">Quarantine zones for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81266-104">See teema kirjeldab, kuidas luua ja kasutada mittevastavuste garantiitsoone.</span><span class="sxs-lookup"><span data-stu-id="81266-104">This topic describes how to create and use quarantine zones for nonconformances.</span></span>

<span data-ttu-id="81266-105">Kasutage lehte **Garantii tsoonid** tsoonide määratlemiseks, mida saab mittevastavusele määrata.</span><span class="sxs-lookup"><span data-stu-id="81266-105">You use the **Quarantine zones** page to define zones that can be assigned to nonconformances.</span></span> <span data-ttu-id="81266-106">Kui loote mittevastavuse, saate seadistada **Garantii tsoon** ja **Garantiitüüp** väljad vahekaardil **Üldine** lehel **Mittevastavused**.</span><span class="sxs-lookup"><span data-stu-id="81266-106">When you create a nonconformance, you can set the **Quarantine zone** and **Quarantine type** fields on the **General** tab of the **Non conformances** page.</span></span> <span data-ttu-id="81266-107">**Garantiitsoon** väli näitab tavaliselt ala või asukohta, kus kaup asub.</span><span class="sxs-lookup"><span data-stu-id="81266-107">The **Quarantine zone** field typically indicates the area or location where the item is located.</span></span> <span data-ttu-id="81266-108">**Garantii tüüp** väli määratleb kauba kas *Piiratud kasutusena* või *kasutuskõlbmatuna*.</span><span class="sxs-lookup"><span data-stu-id="81266-108">The **Quarantine type** field defines the item as either *Restricted usage* or *Unusable*.</span></span>

<span data-ttu-id="81266-109">Mittevastavuse või mittevastavuse paranduste aruande printimisel saate vaadata garantiitsooni, kus üksus asub.</span><span class="sxs-lookup"><span data-stu-id="81266-109">When you print a nonconformance or corrections report for a nonconformance, you can view the quarantine zone where the item is located.</span></span>

<span data-ttu-id="81266-110">Saate printida ka mittevastavuse sildi.</span><span class="sxs-lookup"><span data-stu-id="81266-110">You can also print a nonconformance tag for a nonconformance.</span></span> <span data-ttu-id="81266-111">See aruanne näitab määratud garantiitsooni ja teavet kasutamise kohta, et anda juhiseid defektse materjaliga ümberkäimise kohta.</span><span class="sxs-lookup"><span data-stu-id="81266-111">This report shows the assigned quarantine zone and information about usage to provide guidance about how defective material should be handled.</span></span> <span data-ttu-id="81266-112">Garantiitsoonid võivad vastata lao asukohtadele või toimingute ressurssidele.</span><span class="sxs-lookup"><span data-stu-id="81266-112">The quarantine zones might correspond to inventory locations or operations resources.</span></span>

## <a name="examples-of-quarantine-zones"></a><span data-ttu-id="81266-113">Garantiitsoonide näited</span><span class="sxs-lookup"><span data-stu-id="81266-113">Examples of quarantine zones</span></span>

### <a name="example-1"></a><span data-ttu-id="81266-114">Näide 1</span><span class="sxs-lookup"><span data-stu-id="81266-114">Example 1</span></span>

<span data-ttu-id="81266-115">Töötate elektroonikaettevõttes, mis toodab ja tarnib televiisoreid, kõlareid ja meediapleiereid.</span><span class="sxs-lookup"><span data-stu-id="81266-115">You work at an electronics manufacturing company that produces and distributes televisions, speakers, and media players.</span></span> <span data-ttu-id="81266-116">Sel juhul saate garantiitsooni konfigureerida esindama igat tüüpi toodet.</span><span class="sxs-lookup"><span data-stu-id="81266-116">In this case, you can configure a quarantine zone to represent each type of product.</span></span>

### <a name="example-2"></a><span data-ttu-id="81266-117">Näide 2</span><span class="sxs-lookup"><span data-stu-id="81266-117">Example 2</span></span>

<span data-ttu-id="81266-118">Mittevastavate esemete hoidmiseks kasutatakse kolme prügikasti ja kahte riiulit.</span><span class="sxs-lookup"><span data-stu-id="81266-118">Three bins and two racks are used to store items that are nonconforming.</span></span> <span data-ttu-id="81266-119">Sel juhul saate konfigureerida viis garantiitsooni, üks igale prügikastile ja riiulile.</span><span class="sxs-lookup"><span data-stu-id="81266-119">In this case, you can configure five quarantine zones, one for each bin and each rack.</span></span>

## <a name="create-a-quarantine-zone"></a><span data-ttu-id="81266-120">Looge uus garantiitsoon</span><span class="sxs-lookup"><span data-stu-id="81266-120">Create a quarantine zone</span></span>

1. <span data-ttu-id="81266-121">Avage **Laohaldus \> Seadistus \> Kvaliteedijuhtimine \> Garantiitsoonid**.</span><span class="sxs-lookup"><span data-stu-id="81266-121">Go to **Inventory management \> Setup \> Quality management \> Quarantine zones**.</span></span>
1. <span data-ttu-id="81266-122">Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="81266-122">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="81266-123">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="81266-123">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="81266-124">**Garantiitsoon** – Sisestage garantiitsoonile kordumatu ID või nimi.</span><span class="sxs-lookup"><span data-stu-id="81266-124">**Quarantine zone** – Enter a unique ID or name for the quarantine zone.</span></span>
    - <span data-ttu-id="81266-125">**Kirjeldus** – Sisestage garantiitsooni detailne kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="81266-125">**Description** – Enter a detailed description of the quarantine zone.</span></span>

1. <span data-ttu-id="81266-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="81266-126">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81266-127">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="81266-127">Additional resources</span></span>

- [<span data-ttu-id="81266-128">Kvaliteedijuhtimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="81266-128">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="81266-129">Kvaliteedi ja mittevastavuse haldamise lubamine</span><span class="sxs-lookup"><span data-stu-id="81266-129">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="81266-130">Mittevastavuste kinnitamise eest vastutavad töötajad</span><span class="sxs-lookup"><span data-stu-id="81266-130">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="81266-131">Mittevastavuste probleemitüübid</span><span class="sxs-lookup"><span data-stu-id="81266-131">Problem types for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="81266-132">Mittevastavuste diagnostika tüübid</span><span class="sxs-lookup"><span data-stu-id="81266-132">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="81266-133">Kvaliteeditasud mittevastavustele</span><span class="sxs-lookup"><span data-stu-id="81266-133">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="81266-134">MIttevastavuste toimingud</span><span class="sxs-lookup"><span data-stu-id="81266-134">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="81266-135">Laoprotsesside kvaliteedijuhtimine</span><span class="sxs-lookup"><span data-stu-id="81266-135">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
