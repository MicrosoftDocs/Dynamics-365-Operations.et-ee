---
title: Kontsernisiseste tellimuste filtreerimine üksuste Orders ja OrderLines sünkroonimise vältimiseks
description: See teema kirjeldab, kuidas filtreerida kontsernisiseseid tellimusi üksuste Orders (Tellimused) ja OrderLines (Tellimuse read) sünkroonimise vältimiseks.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 6c5e1e2467673badd20366d3bd8e1b93b8078b26
ms.sourcegitcommit: 0eb33909a419d526eb84b4e4b64d3595d01731ef
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4701029"
---
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a><span data-ttu-id="40e3a-103">Kontsernisiseste tellimuste filtreerimine üksuste Orders ja OrderLines sünkroonimise vältimiseks</span><span class="sxs-lookup"><span data-stu-id="40e3a-103">Filter intercompany orders to avoid synchronizing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="40e3a-104">Saate filtreerida kontsernisiseseid tellimusi, et vältida üksuste **Orders** ja **OrderLines** sünkroonimist.</span><span class="sxs-lookup"><span data-stu-id="40e3a-104">You can filter intercompany orders to avoid synchronizing the **Orders** and **OrderLines** entities.</span></span> <span data-ttu-id="40e3a-105">Mõningatel juhtudel ei ole kontsernisiseste tellimuste üksikasjad klientide kaasamise rakenduses vajalikud.</span><span class="sxs-lookup"><span data-stu-id="40e3a-105">In some scenarios, the intercompany order details are not necessary in customer engagement app.</span></span>

<span data-ttu-id="40e3a-106">Kõiki standardsed teenuse Common Data Service üksused on laiendatud viidetega väljale **IntercompanyOrder** ja topeltkirjutamise kaardid on muudetud, et need viitaksid filtrites täiendavatele väljadele.</span><span class="sxs-lookup"><span data-stu-id="40e3a-106">Each of the standard Common Data Service entities is extended with references to the **IntercompanyOrder** field, and the dual-write maps are modified to refer to the additional fields in the filters.</span></span> <span data-ttu-id="40e3a-107">Selle tulemuseks on, et kontsernisiseseid tellimusi enam ei sünkroonita.</span><span class="sxs-lookup"><span data-stu-id="40e3a-107">The result is that the intercompany orders are no longer synchronized.</span></span> <span data-ttu-id="40e3a-108">See protsess väldib tarbetuid andmeid klientide kaasamise rakenduses.</span><span class="sxs-lookup"><span data-stu-id="40e3a-108">This process avoids unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="40e3a-109">Lisage üksuse **IntercompanyOrder** viide suvandile **CDS-i müügitellimuse päised**.</span><span class="sxs-lookup"><span data-stu-id="40e3a-109">Add a reference to **IntercompanyOrder** to **CDS Sales Order Headers**.</span></span> <span data-ttu-id="40e3a-110">See on täidetud ainult kontsernisiseste tellimuste puhul.</span><span class="sxs-lookup"><span data-stu-id="40e3a-110">It is populated on only intercompany orders.</span></span> <span data-ttu-id="40e3a-111">Väli **IntercompanyOrder** on saadaval üksuses **SalesTable**.</span><span class="sxs-lookup"><span data-stu-id="40e3a-111">The field **IntercompanyOrder** is available in **SalesTable**.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Sihtmärgini ajastamise kaardistamine, SalesOrderHeader":::
    
2. <span data-ttu-id="40e3a-113">Pärast suvandi **CDS-i müügitellimuse päised** laiendamist on väli **IntercompanyOrder** vastendamiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="40e3a-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** field is available in the mapping.</span></span> <span data-ttu-id="40e3a-114">Rakendage filter atribuudiga `INTERCOMPANYORDER == ""` päringu stringina.</span><span class="sxs-lookup"><span data-stu-id="40e3a-114">Apply a filter with `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Müügitellimuste päised, päringu redigeerimine":::

3. <span data-ttu-id="40e3a-116">Lisage viide üksusest **IntercompanyInventTransId** suvandisse **CDS-i müügitellimuste read**.</span><span class="sxs-lookup"><span data-stu-id="40e3a-116">Add a reference to **IntercompanyInventTransId** to **CDS Sales Order Lines**.</span></span>  <span data-ttu-id="40e3a-117">See on täidetud ainult kontsernisiseste tellimuste puhul.</span><span class="sxs-lookup"><span data-stu-id="40e3a-117">It is populated on only intercompany orders.</span></span> <span data-ttu-id="40e3a-118">Väli **InterCompanyInventTransID** on saadaval üksuses **SalesLine**.</span><span class="sxs-lookup"><span data-stu-id="40e3a-118">The field **InterCompanyInventTransID** is available in **SalesLine**.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Sihtmärgini ajastamise kaardistamine, SalesOrderLine":::

4. <span data-ttu-id="40e3a-120">Pärast suvandi **CDS-i müügitellimuse read** laiendamist on väli **IntercompanyInventTransId** vastendamiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="40e3a-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** field is available in the mapping.</span></span> <span data-ttu-id="40e3a-121">Rakendage filter atribuudiga `INTERCOMPANYINVENTTRANSID == ""` päringu stringina.</span><span class="sxs-lookup"><span data-stu-id="40e3a-121">Apply a filter with `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Müügitellimuse read, päringu redigeerimine":::

5. <span data-ttu-id="40e3a-123">Laiendage suvandid **müügitellimuse päis V2** ja **müügiarve read V2** samal viisil, nagu laiendasite teenuse Common Data Service olemid etappides 1 ja 2.</span><span class="sxs-lookup"><span data-stu-id="40e3a-123">Extend **Sales Invoice Header V2** and **Sales Invoice Lines V2** in the same way you extended the Common Data Service entities in steps 1 and 2.</span></span> <span data-ttu-id="40e3a-124">Seejärel lisage filtri päringud.</span><span class="sxs-lookup"><span data-stu-id="40e3a-124">Then add the filter queries.</span></span> <span data-ttu-id="40e3a-125">Filtri string suvandi **müügiarve päis V2** jaoks on `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span><span class="sxs-lookup"><span data-stu-id="40e3a-125">The filter string for **Sales Invoice Header V2** is `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span></span> <span data-ttu-id="40e3a-126">Filtri string suvandi **müügiarve read V2** jaoks on `INTERCOMPANYINVENTTRANSID == ""`.</span><span class="sxs-lookup"><span data-stu-id="40e3a-126">The filter string for **Sales Invoice Lines V2** is `INTERCOMPANYINVENTTRANSID == ""`.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Sihtmärgini ajastamise kaardistamine, müügiarve päised":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Müügiarve päised, päringu redigeerimine":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Müügiarve read, päringu redigeerimine":::

6. <span data-ttu-id="40e3a-130">Olemil **Pakkumised** puudub kontsernisisene suhe.</span><span class="sxs-lookup"><span data-stu-id="40e3a-130">The **Quotations** entity doesn't have an intercompany relationship.</span></span> <span data-ttu-id="40e3a-131">Kui keegi loob ühe teie kontsernisisese kliendi jaoks pakkumise, saate panna kõik need kliendid ühte kliendigrupi, kasutades välja **CustGroup**.</span><span class="sxs-lookup"><span data-stu-id="40e3a-131">If someone creates a quote for one of your intercompany customers, you can put all of these customers in one customer group by using the **CustGroup** field.</span></span>  <span data-ttu-id="40e3a-132">Päist ja ridu saab laiendada, et lisada väli **CustGroup** ja seejärel filtreerida, et see grupp ei oleks kaasatud.</span><span class="sxs-lookup"><span data-stu-id="40e3a-132">Header and lines can be extended to add the **CustGroup** field and then filter to not include this group.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="Sihtmärgini ajastamise kaardistamine, müügipakkumise päis":::

7. <span data-ttu-id="40e3a-134">Pärast olemi **Pakkumised** laiendamist rakendage filter koos atribuudiga `CUSTGROUP !=  "<company>"` päringu stringina.</span><span class="sxs-lookup"><span data-stu-id="40e3a-134">After you extent the **Quotations** entity, apply a filter with `CUSTGROUP !=  "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Müügipakkumise päis, päringu redigeerimine":::
