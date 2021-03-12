---
title: Kontsernisiseste tellimuste filtreerimine tellimuse ja tellimuseridade sünkroonimise vältimiseks
description: See teema kirjeldab, kuidas filtreerida kontsernisiseseid tellimusi nii, et tellimuste ja tellimuseridade üksused ei oleks sünkroonitud.
author: negudava
manager: tfehr
ms.date: 11/09/2020
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
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 342db8c1b4337145bfd61f5698ff6de25434a400
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796602"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a><span data-ttu-id="f7517-103">Kontsernisiseste tellimuste filtreerimine tellimuse ja tellimuseridade sünkroonimise vältimiseks</span><span class="sxs-lookup"><span data-stu-id="f7517-103">Filter intercompany orders to avoid syncing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f7517-104">Saate filtreerida kontsernisiseseid tellimusi nii, et tabeleid **Tellimused** ja **Tellimuseread** ei sünkroonita.</span><span class="sxs-lookup"><span data-stu-id="f7517-104">You can filter intercompany orders so that the **Orders** and **OrderLines** tables aren't synced.</span></span> <span data-ttu-id="f7517-105">Mõningatel juhtudel ei ole kontsernisiseste tellimuste üksikasjad klientide kaasamise rakenduses nõutavad.</span><span class="sxs-lookup"><span data-stu-id="f7517-105">In some scenarios, the intercompany order details aren't required in a customer engagement app.</span></span>

<span data-ttu-id="f7517-106">Kõik standardsed teenuse Dataverse tabelid on laiendatud viidetega veerule **IntercompanyOrder** ja topeltkirjutamise kaardid on muudetud, et need viitaksid filtrites täiendavatele veergudele.</span><span class="sxs-lookup"><span data-stu-id="f7517-106">Each standard Dataverse table is extended through references to the **IntercompanyOrder** column, and the dual-write maps are modified so that they refer to the additional columns in the filters.</span></span> <span data-ttu-id="f7517-107">Seega kontsernisiseseid tellimusi enam ei sünkroonita.</span><span class="sxs-lookup"><span data-stu-id="f7517-107">Therefore, the intercompany orders are no longer synced.</span></span> <span data-ttu-id="f7517-108">See protsess aitab ennetada tarbetuid andmeid klientide kaasamise rakenduses.</span><span class="sxs-lookup"><span data-stu-id="f7517-108">This process helps prevent unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="f7517-109">Laiendage tabelit **CDS-i müügitellimuse päised**, lisades viite veerule **IntercompanyOrder**.</span><span class="sxs-lookup"><span data-stu-id="f7517-109">Extend the **CDS Sales Order Headers** table by adding a reference to the **IntercompanyOrder** column.</span></span> <span data-ttu-id="f7517-110">See veerg täidetakse ainult kontsernisiseste tellimuste puhul.</span><span class="sxs-lookup"><span data-stu-id="f7517-110">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="f7517-111">Veerg **IntercompanyOrder** on saadaval tabelis **SalesTable**.</span><span class="sxs-lookup"><span data-stu-id="f7517-111">The **IntercompanyOrder** column is available in the **SalesTable** table.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="CDS-i müügitellimuse päisete vastendamine kaardil sihtkohaks":::

2. <span data-ttu-id="f7517-113">Pärast suvandi **CDS-i müügitellimuse päised** laiendamist on veerg **IntercompanyOrder** vastendamiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="f7517-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** column is available in the mapping.</span></span> <span data-ttu-id="f7517-114">Rakendage filter, millel on `INTERCOMPANYORDER == ""`, päringu stringina.</span><span class="sxs-lookup"><span data-stu-id="f7517-114">Apply a filter that has `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="CDS-i müügitellimuse päisete päringu dialoogiboksi redigeerimine":::

3. <span data-ttu-id="f7517-116">Laiendage tabelit **CDS-i müügitellimuse read**, lisades viite veerule **IntercompanyInventTransId**.</span><span class="sxs-lookup"><span data-stu-id="f7517-116">Extend the **CDS Sales Order Lines** table by adding a reference to the **IntercompanyInventTransId** column.</span></span> <span data-ttu-id="f7517-117">See veerg täidetakse ainult kontsernisiseste tellimuste puhul.</span><span class="sxs-lookup"><span data-stu-id="f7517-117">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="f7517-118">Veerg **InterCompanyInventTransId** on saadaval tabelis **SalesLine**.</span><span class="sxs-lookup"><span data-stu-id="f7517-118">The **InterCompanyInventTransId** column is available in the **SalesLine** table.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="CDS-i müügitellimuse ridade vastendamine kaardil sihtkohaks":::

4. <span data-ttu-id="f7517-120">Pärast suvandi **CDS-i müügitellimuse read** laiendamist on veerg **IntercompanyInventTransId** vastendamiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="f7517-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** column is available in the mapping.</span></span> <span data-ttu-id="f7517-121">Rakendage filter, millel on `INTERCOMPANYINVENTTRANSID == ""`, päringu stringina.</span><span class="sxs-lookup"><span data-stu-id="f7517-121">Apply a filter that has `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="CDS-i müügitellimuse ridade päringu dialoogiboksi redigeerimine":::

5. <span data-ttu-id="f7517-123">Korrake samme 1 ja 2, et laiendada tabelit **Müügiarve päis V2**, ja lisage filtripäring.</span><span class="sxs-lookup"><span data-stu-id="f7517-123">Repeat steps 1 and 2 to extend the **Sales Invoice Header V2** table and add a filter query.</span></span> <span data-ttu-id="f7517-124">Sellisel juhul kasutage filtri päringustringina atribuuti `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span><span class="sxs-lookup"><span data-stu-id="f7517-124">In this case, use `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Müügiarve päise V2 vastendamine kaardil sihtkoha lehele":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Müügiarve päise V2 päringu dialoogiboksi redigeerimine":::

6. <span data-ttu-id="f7517-127">Korrake samme 3 ja 4, et laiendada tabelit **Müügiarve read V2**, ja lisage filtripäring.</span><span class="sxs-lookup"><span data-stu-id="f7517-127">Repeat steps 3 and 4 to extend the **Sales Invoice Lines V2** table and add a filter query.</span></span> <span data-ttu-id="f7517-128">Sellisel juhul kasutage filtri päringustringina atribuuti `INTERCOMPANYINVENTTRANSID == ""`.</span><span class="sxs-lookup"><span data-stu-id="f7517-128">In this case, use `INTERCOMPANYINVENTTRANSID == ""` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Müügiarve read V2 päringu dialoogiboksi redigeerimine":::

7. <span data-ttu-id="f7517-130">Tabelil **Pakkumised** puudub kontsernisisene suhe.</span><span class="sxs-lookup"><span data-stu-id="f7517-130">The **Quotations** table doesn't have an intercompany relationship.</span></span> <span data-ttu-id="f7517-131">Kui keegi loob ühe teie kontsernisisese kliendi jaoks pakkumise, saate kasutada veergu **CustGroup**, et panna kõik need kliendid ühte kliendigruppi.</span><span class="sxs-lookup"><span data-stu-id="f7517-131">If someone creates a quotation for one of your intercompany customers, you can use the **CustGroup** column to put all those customers into one customer group.</span></span> <span data-ttu-id="f7517-132">Saate laiendada päist ja ridu, lisades veeru **CustGroup** ja seejärel filtreerida nii, et gruppi ei kaasata.</span><span class="sxs-lookup"><span data-stu-id="f7517-132">You can extend the header and lines by adding the **CustGroup** column, and then filter so that the group isn't included.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="CDS-i müügipakkumise päise vastendamine kaardil sihtkoha lehele":::

8. <span data-ttu-id="f7517-134">Pärast olemi **Pakkumised** laiendamist rakendage filter, millel on atribuut `CUSTGROUP != "<company>"`, päringu stringina.</span><span class="sxs-lookup"><span data-stu-id="f7517-134">After **Quotations** is extended, apply a filter that has `CUSTGROUP != "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="CDS-i müügipakkumise päise päringu dialoogiboksi redigeerimine":::
