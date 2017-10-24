---
title: Veose seadistamine
description: Selles teemas selgitatakse, kuidas konfigureerida sissetuleva veose laotoiminguid.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 41c1b8de0aae24efb30a670d3109b6d65e6abd9c
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-consignment"></a><span data-ttu-id="29bf3-103">Veose seadistamine</span><span class="sxs-lookup"><span data-stu-id="29bf3-103">Set up consignment</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="29bf3-104">Selles teemas selgitatakse, kuidas konfigureerida sissetuleva veose laotoiminguid.</span><span class="sxs-lookup"><span data-stu-id="29bf3-104">This topic explains how to configure inbound consignment inventory operations.</span></span>

<span data-ttu-id="29bf3-105">Veose varud on varud, mis kuuluvad hankijale, kuid mida hoitakse teie tegevuskohas.</span><span class="sxs-lookup"><span data-stu-id="29bf3-105">Consignment inventory is inventory that’s owned by a vendor, but stored at your site.</span></span> <span data-ttu-id="29bf3-106">Kui olete valmis tarbima või kasutama varusid, võtate varude omandiõiguse üle.</span><span class="sxs-lookup"><span data-stu-id="29bf3-106">When you’re ready to consume or use the inventory, you take over the ownership of the inventory.</span></span> <span data-ttu-id="29bf3-107">See teema kirjeldab veose protsesside lubamiseks vajalikku seadistust.</span><span class="sxs-lookup"><span data-stu-id="29bf3-107">This topic describes the setup needed to enable consignment processes.</span></span> <span data-ttu-id="29bf3-108">Veoseprotsesside kohta lisateabe saamiseks vaadake [Saadetis](consignment.md).</span><span class="sxs-lookup"><span data-stu-id="29bf3-108">For more information about consignment processes, see [Consignment](consignment.md).</span></span>

## <a name="inventory-owners"></a><span data-ttu-id="29bf3-109">Varude omanikud</span><span class="sxs-lookup"><span data-stu-id="29bf3-109">Inventory owners</span></span>
<span data-ttu-id="29bf3-110">Füüsiliste sissetulevate veose varude kirjendamiseks peate määratlema hankijast omaniku.</span><span class="sxs-lookup"><span data-stu-id="29bf3-110">In order to record physical inbound consignment inventory, you need to define a vendor owner.</span></span> <span data-ttu-id="29bf3-111">Seda tehakse lehel **Varude omanik**.</span><span class="sxs-lookup"><span data-stu-id="29bf3-111">This is done on the **Inventory owner** page.</span></span> <span data-ttu-id="29bf3-112">Kui teete valiku **Hankija konto**, loob see väljade **Nimi** ja **Omanik** jaoks vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="29bf3-112">When you select a **Vendor account** this generates default values for the **Name** and **Owner** fields.</span></span> <span data-ttu-id="29bf3-113">Väärtus väljal **Omanik** on hankijale nähtav, seega võite soovi korral seda muuta, kui hankijakonto nimesid pole välistel inimestel lihtne tuvastada.</span><span class="sxs-lookup"><span data-stu-id="29bf3-113">The value in the **Owner** field will be visible to the vendor, so you might want to change it if your vendor account names aren’t easy for external people to recognize.</span></span> <span data-ttu-id="29bf3-114">On võimalik redigeerida välja **Omanik**, kuid ainult kirje **Varude omanik** salvestamiseni.</span><span class="sxs-lookup"><span data-stu-id="29bf3-114">It’s possible to edit the **Owner** field, but only up to the point when you save the **Inventory owner** record.</span></span> <span data-ttu-id="29bf3-115">Väli **Nimi** täidetakse selle osapoole nimega, millega hankija konto on seostatud ja seda ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="29bf3-115">The **Name** field is populated with the name of the party that the vendor account is associated with, and this cannot be changed.</span></span>

<span data-ttu-id="29bf3-116">[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)</span><span class="sxs-lookup"><span data-stu-id="29bf3-116">[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)</span></span>

## <a name="tracking-dimension-group"></a><span data-ttu-id="29bf3-117">Jälgimisdimensioonigrupp</span><span class="sxs-lookup"><span data-stu-id="29bf3-117">Tracking dimension group</span></span>
<span data-ttu-id="29bf3-118">Veose protsessides kasutatavad kaubad tuleb seostada valikuga **Jälgimisdimensioonigrupp**, kus dimensioon **Omanik** on määratud sättele **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="29bf3-118">Items that are going to be used in consignment processes must be associated with a **Tracking dimension group** where the **Owner** dimension is set to **Active**.</span></span> <span data-ttu-id="29bf3-119">Dimensioonil Omanik on suvandid **Füüsiline ladu** ja **Finantsiline laovaru** valitud.</span><span class="sxs-lookup"><span data-stu-id="29bf3-119">The Owner dimension always has the **Physical inventory** and **Financial inventory** options selected.</span></span> <span data-ttu-id="29bf3-120">Suvand **Laovarude planeerimine dimensioonide kaupa** pole kunagi valitud.</span><span class="sxs-lookup"><span data-stu-id="29bf3-120">The **Coverage plan by dimension** is never selected.</span></span>

<span data-ttu-id="29bf3-121">[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span><span class="sxs-lookup"><span data-stu-id="29bf3-121">[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span></span>

## <a name="inventory-ownership-change-journal"></a><span data-ttu-id="29bf3-122">Varude omandiõiguse muutmise tööleht</span><span class="sxs-lookup"><span data-stu-id="29bf3-122">Inventory ownership change journal</span></span>
<span data-ttu-id="29bf3-123">Töölehte **Varude omandiõiguse muutmine**kasutatakse, et kirjendada veose varude omandiõiguse ülekannet hankijalt juriidilisele isikule, kes seda tarbib.</span><span class="sxs-lookup"><span data-stu-id="29bf3-123">The **Inventory ownership change** journal is used to record the transfer of ownership of consignment inventory from the vendor to the legal entity that’s consuming it.</span></span> <span data-ttu-id="29bf3-124">Nagu iga varude töölehega, tuleb see tuvastada lao töölehe nimega.</span><span class="sxs-lookup"><span data-stu-id="29bf3-124">Like any inventory journal, it must be identified with an Inventory journal name.</span></span> <span data-ttu-id="29bf3-125">Need nimed luuakse lehel **Lao töölehe nimed** ja valik **Töölehe tüüp** tuleb määrata sättele **Omandiõiguse muutmine**.</span><span class="sxs-lookup"><span data-stu-id="29bf3-125">These names are created on the **Inventory journal names** page, and the **Journal type** must be set to **Ownership change**.</span></span>

<span data-ttu-id="29bf3-126">[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span><span class="sxs-lookup"><span data-stu-id="29bf3-126">[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span></span>

## <a name="vendor-collaboration-in-consignment-processes"></a><span data-ttu-id="29bf3-127">Hankija koostöö veoseprotsessides</span><span class="sxs-lookup"><span data-stu-id="29bf3-127">Vendor collaboration in consignment processes</span></span>
<span data-ttu-id="29bf3-128">Kui hankijad kasutavad hankija koostööliidest, saavad nad seda kasutada varude tarbimise jälgimiseks teie tegevuskohas.</span><span class="sxs-lookup"><span data-stu-id="29bf3-128">If your vendors are using the vendor collaboration interface, they can use this to monitor the consumption of inventory at your site.</span></span> <span data-ttu-id="29bf3-129">Hankija koostöö kasutamiseks hankijate seadistamise kohta lisateabe saamiseks vaadake [Hankija koostöö kasutajate turbe konfigureerimine](../procurement/configure-security-vendor-portal-users.md).</span><span class="sxs-lookup"><span data-stu-id="29bf3-129">For more information about setting up vendors to use vendor collaboration, see [Configuration of security for vendor collaboration users](../procurement/configure-security-vendor-portal-users.md).</span></span>

