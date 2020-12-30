---
title: Vedajate grupid
description: Selles teemas kirjeldatakse, kuidas seadistada andmeid vedajagruppidele.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2570479edac9bc8cc7aa998a8b69f54ffc10cd61
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646382"
---
# <a name="carrier-groups"></a><span data-ttu-id="14f53-103">Vedajate grupid</span><span class="sxs-lookup"><span data-stu-id="14f53-103">Carrier groups</span></span>

<span data-ttu-id="14f53-104">Vedajagrupp on kättetoimetajate ja kättetoimetamisteenuste kogum.</span><span class="sxs-lookup"><span data-stu-id="14f53-104">A carrier group is a collection of shipping carriers and carrier services.</span></span> <span data-ttu-id="14f53-105">Iga vedajagrupp määrab enda kättetoimetajate ja kättetoimetamisteenuste eelisjärjekorra.</span><span class="sxs-lookup"><span data-stu-id="14f53-105">Each carrier group specifies the preferred sequence for the shipping carriers and carrier services that belong to it.</span></span>

<span data-ttu-id="14f53-106">Kui sama marsruudi segmendi jaoks on olemas mitu kättetoimetajat ja kättetoimetamisteenust, saate marsruudiplaanis või -juhendis määrata konkreetse kättetoimetaja ja kättetoimetamisteenuse asemel vedajagrupi.</span><span class="sxs-lookup"><span data-stu-id="14f53-106">When multiple shipping carriers and carrier services exist for the same route segment, you can specify a carrier group instead of a specific shipping carrier and carrier service in the route plan or route guide.</span></span>

## <a name="create-a-carrier-group"></a><span data-ttu-id="14f53-107">Vedajagrupi loomine</span><span class="sxs-lookup"><span data-stu-id="14f53-107">Create a carrier group</span></span>

1. <span data-ttu-id="14f53-108">Avage jaotis **Transpordihaldus &gt; Seadistus &gt; Vedajad &gt; Vedajagrupp**.</span><span class="sxs-lookup"><span data-stu-id="14f53-108">Go to **Transportation management &gt; Setup &gt; Carriers &gt; Carrier group**.</span></span>
1. <span data-ttu-id="14f53-109">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="14f53-109">Select **New**.</span></span>
1. <span data-ttu-id="14f53-110">Sisestage väljale **Vedajagrupp** grupi ainuidentifikaator (ID).</span><span class="sxs-lookup"><span data-stu-id="14f53-110">In the **Carrier group** field, enter a unique identifier (ID) for the group.</span></span>
1. <span data-ttu-id="14f53-111">Sisestage väljale **Nimi** gruppi kirjeldav nimi.</span><span class="sxs-lookup"><span data-stu-id="14f53-111">In the **Name** field, enter a descriptive name for the group.</span></span>
1. <span data-ttu-id="14f53-112">Lisage kiirkaardil **Üksikasjad** rida ja valige selle jaoks kättetoimetaja ja kättetoimetamisteenus.</span><span class="sxs-lookup"><span data-stu-id="14f53-112">On the **Details** FastTab, add a row, and select a shipping carrier and a carrier service for it.</span></span> <span data-ttu-id="14f53-113">Korrake seda sammu seni, kuni olete lisanud nii palju vedajaid, kui teil grupi jaoks vaja on.</span><span class="sxs-lookup"><span data-stu-id="14f53-113">Repeat this step until you've added as many carriers as you require for the group.</span></span>
1. <span data-ttu-id="14f53-114">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="14f53-114">Close the page.</span></span>
