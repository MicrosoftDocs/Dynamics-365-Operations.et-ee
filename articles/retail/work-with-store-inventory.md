---
title: Kaupluse varude haldamine
description: "See artikkel kirjeldab dokumendi tüüpe, mida saate kasutada varude haldamiseks."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 031a2f9c27bb6223dc65c3ae6b3d4e3ce775ae21
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="manage-store-inventory"></a><span data-ttu-id="9407d-103">Kaupluse varude haldamine</span><span class="sxs-lookup"><span data-stu-id="9407d-103">Manage store inventory</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9407d-104">See artikkel kirjeldab dokumendi tüüpe, mida saate kasutada varude haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="9407d-104">This article describes the types of documents that you can use to manage inventory.</span></span>

<span data-ttu-id="9407d-105">Organisatsiooni varude haldamiseks saab kasutada järgmist tüüpi dokumente.</span><span class="sxs-lookup"><span data-stu-id="9407d-105">You can use the following types of documents to manage your organization's inventory.</span></span>

## <a name="purchase-orders"></a><span data-ttu-id="9407d-106">Ostutellimused</span><span class="sxs-lookup"><span data-stu-id="9407d-106">Purchase orders</span></span>
<span data-ttu-id="9407d-107">Ostutellimused koostatakse peakontoris.</span><span class="sxs-lookup"><span data-stu-id="9407d-107">Purchase orders are created at the head office.</span></span> <span data-ttu-id="9407d-108">Kui ostutellimuse päisesse on kaasatud jaemüügiladu, saab tellimust vastu võtta kaupluses, kasutades rakenduses Microsoft Dynamics 365 for Retail kaasaegset kassat (MPOS) või pilve POS-i.</span><span class="sxs-lookup"><span data-stu-id="9407d-108">If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="9407d-109">Pärast kaupluses vastuvõetud koguste sisestamist saab need kohalikult täiendavaks modifitseerimiseks salvestada.</span><span class="sxs-lookup"><span data-stu-id="9407d-109">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="9407d-110">Teise võimalusena saab kogused kooskõlastada ja saata peakontorisse.</span><span class="sxs-lookup"><span data-stu-id="9407d-110">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="9407d-111">Peakontoris kuvatakse kaupluses vastu võetud kogused rakenduses Dynamics 365 for Retail ostutellimuse real **Kohe tarnitav**.</span><span class="sxs-lookup"><span data-stu-id="9407d-111">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the purchase order.</span></span>

## <a name="transfer-orders"></a><span data-ttu-id="9407d-112">Üleviimistellimused</span><span class="sxs-lookup"><span data-stu-id="9407d-112">Transfer orders</span></span>
<span data-ttu-id="9407d-113">Üleviimistellimuses saab määrata, et konkreetne kauplus on koht, kust kaupu saab teele panna.</span><span class="sxs-lookup"><span data-stu-id="9407d-113">A transfer order can specify that a particular store is a location that items can be shipped from.</span></span> <span data-ttu-id="9407d-114">Sellisel juhul kuvatakse üleviimistellimus kaupluses MPOS-is või pilve POS-is komplekteerimistaotlusena.</span><span class="sxs-lookup"><span data-stu-id="9407d-114">In this case, the transfer order appears at the store as a picking request in MPOS or Cloud POS.</span></span> <span data-ttu-id="9407d-115">Pärast taotletud koguste komplekteerimist need kooskõlastatakse ja saadetakse peakontorisse.</span><span class="sxs-lookup"><span data-stu-id="9407d-115">After the quantities that are requested are picked, they are committed and sent to the head office.</span></span> <span data-ttu-id="9407d-116">Peakontoris kuvatakse kaupluses komplekteeritud kogused rakenduses Dynamics 365 for Retail üleviimistellimuse väljal **Läheta kohe**.</span><span class="sxs-lookup"><span data-stu-id="9407d-116">At the head office, the quantities that were picked at the store are displayed in Dynamics 365 for Retail, in the **Ship now** field on the transfer order.</span></span> <span data-ttu-id="9407d-117">Üleviimistellimuses saab määrata, et konkreetne kauplus on koht, kuhu kaupu saab saata.</span><span class="sxs-lookup"><span data-stu-id="9407d-117">A transfer order may specify that a particular store is a location that items can be shipped to.</span></span> <span data-ttu-id="9407d-118">Sellisel juhul kuvatakse üleviimistellimus kaupluses MPOS-is või pilve POS-is vastuvõtmistaotlusena.</span><span class="sxs-lookup"><span data-stu-id="9407d-118">In this case, the transfer order appears at the store as a receiving request in MPOS or Cloud POS.</span></span> <span data-ttu-id="9407d-119">Pärast kaupluses vastuvõetud koguste sisestamist saab need kohalikult täiendavaks modifitseerimiseks salvestada.</span><span class="sxs-lookup"><span data-stu-id="9407d-119">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="9407d-120">Teise võimalusena saab kogused kooskõlastada ja saata peakontorisse.</span><span class="sxs-lookup"><span data-stu-id="9407d-120">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="9407d-121">Peakontoris kuvatakse kaupluses vastu võetud kogused rakenduses Dynamics 365 for Retail üleviimistellimuse real **Kohe tarnitav**.</span><span class="sxs-lookup"><span data-stu-id="9407d-121">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the transfer order.</span></span>

## <a name="stock-counts"></a><span data-ttu-id="9407d-122">Laoinventuurid</span><span class="sxs-lookup"><span data-stu-id="9407d-122">Stock counts</span></span>
<span data-ttu-id="9407d-123">Laoinventuurid võivad olla plaanipärased või plaanivälised.</span><span class="sxs-lookup"><span data-stu-id="9407d-123">Stock counts can be either scheduled or unscheduled.</span></span> <span data-ttu-id="9407d-124">Plaanitud laoinventuurid algatab peakontor, mis määrab ka loendatavad kaubad.</span><span class="sxs-lookup"><span data-stu-id="9407d-124">Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</span></span> <span data-ttu-id="9407d-125">Peakontor loob inventuuridokumendi, mida saab vastu võtta kaupluses, kus vaba laovaru kogused sisestatakse MPOS-is või pilve POS-is.</span><span class="sxs-lookup"><span data-stu-id="9407d-125">The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</span></span> <span data-ttu-id="9407d-126">Plaanimata laoinventuurid käivitatakse kaupluses ja vaba laoseisu koguseid värskendatakse MPOS-is või pilve POS-is.</span><span class="sxs-lookup"><span data-stu-id="9407d-126">Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</span></span> <span data-ttu-id="9407d-127">Erinevalt ajastatud laoinventuuridest puudub plaanimata laovarudel eelmääratletud kaupade loend.</span><span class="sxs-lookup"><span data-stu-id="9407d-127">Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</span></span> <span data-ttu-id="9407d-128">Mõlemat tüüpi laoinventuuri lõpetamisel see kooskõlastatakse ja saadetakse peakontorisse.</span><span class="sxs-lookup"><span data-stu-id="9407d-128">When a stock count of either type is completed, it is committed and sent to the head office.</span></span> <span data-ttu-id="9407d-129">Peakontoris inventuur kinnitatakse ja sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="9407d-129">At the head office, the count is validated and posted.</span></span>

## <a name="inventory-lookup"></a><span data-ttu-id="9407d-130">Otsing varudest</span><span class="sxs-lookup"><span data-stu-id="9407d-130">Inventory lookup</span></span>
<span data-ttu-id="9407d-131">Jooksvat vaba tootekogust mitme kaupluse ja lao kohta saab vaadata varude otsingulehelt.</span><span class="sxs-lookup"><span data-stu-id="9407d-131">The current product quantity on hand for multiple stores and warehouses can be viewed on the Inventory lookup page.</span></span> <span data-ttu-id="9407d-132">Lisaks jooksvale vabale kaubavarule saab tulevasi lubamiseks saadaval (ATP) koguseid vaadata iga eraldi kaupluse kohta.</span><span class="sxs-lookup"><span data-stu-id="9407d-132">In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</span></span> <span data-ttu-id="9407d-133">Selleks valige kauplus, mille ATP-d soovite vaadata, ja seejärel klõpsake valikut **Kaupluse saadavuse kuvamine**.</span><span class="sxs-lookup"><span data-stu-id="9407d-133">To do so, select the store that you want to view the ATP for and then click **Show store availability**.</span></span>





