---
title: "Kõnekeskuse funktsioonid"
description: "Selles artiklis antakse ülevaade kõnekeskuse müügifunktsioonidest Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2c58f71230a0781ee957632b453ced86ca03b15a
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="call-center-functionality"></a><span data-ttu-id="bf5f3-103">Kõnekeskuse funktsioonid</span><span class="sxs-lookup"><span data-stu-id="bf5f3-103">Call center functionality</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="bf5f3-104">Selles artiklis antakse ülevaade kõnekeskuse müügifunktsioonidest Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-104">This article provides an overview of the call center sales functionality in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="bf5f3-105">Dynamics 365 for Retail toetab jaemüügikanali tüübina ka kõnekeskusi.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-105">Dynamics 365 for Retail supports call centers as a type of retail channel.</span></span> <span data-ttu-id="bf5f3-106">Kõnekeskuses võtavad töötajad telefonitsi klientide tellimusi vastu ja loovad müügitellimusi.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-106">In a call center, workers take orders from customers over the phone and create sales orders.</span></span> <span data-ttu-id="bf5f3-107">Kõnekeskuse funktsioonid hõlbustavad telefonitsi tellimuste vastuvõtmist ja kliendi teenuse käsitlemist tellimuse täitmise protsessi jooksul.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-107">Call center functionality includes features that are designed to make it easier to take phone orders and handle customer service throughout the order fulfillment process.</span></span> <span data-ttu-id="bf5f3-108">Näiteks saavad kõnekeskuse töötajad sisestada makseteavet otse müügitellimusse ning vaadata tasude ja maksete üksikasjalikku kokkuvõtet enne tellimuse esitamist.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-108">For example, call center workers can enter payment information directly into the sales order, and can view a detailed summary of charges and payments before they submit the order.</span></span> <span data-ttu-id="bf5f3-109">Töötajatel on ka hinnakujundamise juhtimise võimalused ning nad pääsevad lehelt **Müügitellimus** klientide, toodete ja hindadega seotud mitmesuguste andmete juurde.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-109">Workers also have options for controlling pricing, and can access various data about customers, products, and prices from the **Sales order** page.</span></span> <span data-ttu-id="bf5f3-110">Kõnekeskustel on lisaks täiustatud funktsioonid klientide ajaloo ja tellimuse oleku jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-110">Additionally, call centers have enhanced functionality for tracking customer history and order status.</span></span> <span data-ttu-id="bf5f3-111">Igal kõnekeskusel võivad olla oma kasutajad, makseviisid, hinnagrupid, finantsdimensioonid ja tarneviisid.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-111">Each call center can have its own users, payment methods, price groups, financial dimensions, and modes of delivery.</span></span> <span data-ttu-id="bf5f3-112">Saate neid suvandeid konfigureerida kõnekeskuse loomisel.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-112">You can configure these options when you create the call center.</span></span> <span data-ttu-id="bf5f3-113">Lisaks saate kasutada lehte **Kõnekeskus**, et lubada või keelata järgmised funktsioonide grupid, mis on kõneskuste puhul kordumatud.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-113">Additionally, you can use the **Call center** page to enable or disable the following groups of features that are unique to call centers:</span></span>

-   <span data-ttu-id="bf5f3-114">**Tellimuse lõpuleviimine** – see grupp hõlmab funktsioone, mis on seotud maksete ja tellimuse lõpulevimisega lehel **Müügitellimus**.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-114">**Order completion** – This group includes features that are related to payments and order completion on the **Sales order** page.</span></span>
-   <span data-ttu-id="bf5f3-115">**Suunatud müük** – see grupp hõlmab funktsioone, mis on seotud lähtekoodide, skriptide ja kataloogitaotlustega.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-115">**Directed selling** – This group includes features that are related to source codes, scripts, and catalog requests.</span></span>

<span data-ttu-id="bf5f3-116">Pärast kõnekeskuse sätetes nende funktsioonide lubamist on need kõnekeskusega seostatud kasutajatele saadaval lehel **Müügitellimus**.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-116">After you enable these features in the call center settings, they are available on the **Sales order** page to users who are associated with the call center.</span></span> <span data-ttu-id="bf5f3-117">Enamik neist funktsioonidest nõuab enne kasutamist lisaseadistamist.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-117">Most of these features require additional setup before they can be used.</span></span> <span data-ttu-id="bf5f3-118">Enne kui kasutajad saavad luua kõnekeskuse tellimusi, peate lisama need kasutajad kõnekeskusse kõnekeskuse kasutajatena.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-118">Before users can create call center orders, you must add those users to the call center as call center users.</span></span> <span data-ttu-id="bf5f3-119">See etapp võimaldab kõnekeskuse kanalipõhist konfiguratsiooni ja funktsionaalsust.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-119">This step enables the call center channel-specific configuration and functionality.</span></span> <span data-ttu-id="bf5f3-120">Siin on mõned näited funktsioonidest, mis muutuvad kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-120">Here are some examples of the functionality that becomes available:</span></span>

-   <span data-ttu-id="bf5f3-121">Juhendatud müük pakub konfiguratsioonisuvandeid telemüügi skriptidele ja toote piltidele, et aidata ja juhendada müüjaid tellimuste vastuvõtmisel.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-121">Guided selling provides configuration options for telesales scripts and product images to help and guide sales clerks while they take orders.</span></span>
-   <span data-ttu-id="bf5f3-122">Tellimusi ei saa lõpule viia, kui müüjad ei ole hõivanud vähemalt ühte makseviisi.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-122">Orders can't be completed until sales clerks have captured at least one payment method.</span></span>
-   <span data-ttu-id="bf5f3-123">Lisa- ja kaasmüügi reeglites saab konfigureerida viibad müüjatele, et nad reklaamiksid kliendile kindlaid tooteid.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-123">Upsell and cross-sell rules can be configured to prompt sales clerks to promote specific products to the customer.</span></span>
-   <span data-ttu-id="bf5f3-124">Müüjad saavd hõivata allikakoodi kataloogilt, millest klient tellib.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-124">Sales clerks can capture the source code for the catalog that a customer is ordering from.</span></span>
-   <span data-ttu-id="bf5f3-125">Müüjad saavad lisada tellimusele jaemüüja kupongid.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-125">Sales clerks can add a retailer's coupons to the order.</span></span>
-   <span data-ttu-id="bf5f3-126">Müüjad saavad müüa järjepidevusprogramme.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-126">Sales clerks can sell continuity programs.</span></span>
-   <span data-ttu-id="bf5f3-127">Tellimusi saab käsitsi või automaatselt ootele panna näitamaks, et enne tellimuse töötlemist on nõutav täeindav uurimine.</span><span class="sxs-lookup"><span data-stu-id="bf5f3-127">Orders can be put on hold manually or automatically, to indicate that additional investigation is required before the order can be processed.</span></span>





