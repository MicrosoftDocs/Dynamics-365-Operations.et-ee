---
title: Ootelolevad tellimused
description: Selles teemas kirjeldatakse tellimuste ootele panemist, kasutades Dynamics 365 for Retaili.
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
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8b4c8ecbef1dc667d3b60411a53f0c63686529c2
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="order-holds"></a><span data-ttu-id="37698-103">Ootelolevad tellimused</span><span class="sxs-lookup"><span data-stu-id="37698-103">Order holds</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="37698-104">Selles teemas kirjeldatakse tellimuste ootele panemist, kasutades Dynamics 365 for Retaili.</span><span class="sxs-lookup"><span data-stu-id="37698-104">This topic describes holds on orders using Dynamics 365 for Retail.</span></span>

<span data-ttu-id="37698-105">Tellimuse saab ootele panna mitmel põhjusel.</span><span class="sxs-lookup"><span data-stu-id="37698-105">An order can be put on hold for various reasons.</span></span> <span data-ttu-id="37698-106">Näiteks võidakse tellimus ootele panna seni, kuni kliendi aadressi või makseviisi saab kinnitada või kuni haldur saab kliendi krediidilimiidi üle vaadata.</span><span class="sxs-lookup"><span data-stu-id="37698-106">For example, you might put an order on hold until the customer address or payment method can be verified, or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="37698-107">Müügiprotsessi ajal esineb olukordi, mil müügitellimused tuleb panna ootele.</span><span class="sxs-lookup"><span data-stu-id="37698-107">During the sales process, there are times when sales orders must be put on hold.</span></span> <span data-ttu-id="37698-108">Näiteks võidakse müügitellimus ootele panna kliendi makseprobleemide, kahtlustatud pettuse tõttu või selleks, et haldur tellimuse üle vaataks.</span><span class="sxs-lookup"><span data-stu-id="37698-108">For example, a sales order might be put on hold because of issues with a customer payment, because of suspected fraud, or because a manager must review the order.</span></span> <span data-ttu-id="37698-109">Kui müügitellimus on ootel, määratakse müügitellimusele ooteloleku kood, et näidata ooteloleku põhjust.</span><span class="sxs-lookup"><span data-stu-id="37698-109">When a sales order is put on hold, an order hold code is assigned to the sales order to indicate the reason for the hold.</span></span> <span data-ttu-id="37698-110">Müügitellimuse ooteloleku koodid konfigureeritakse valikus **Müük ja turundus** &gt; **Seadistus** &gt; **Müügitellimus** &gt; **Tellimuse ooteloleku koodid**.</span><span class="sxs-lookup"><span data-stu-id="37698-110">Sales order hold codes are configured at **Sales and marketing** &gt; **Setup** &gt; **Sales orders** &gt; **Order holds codes**.</span></span> <span data-ttu-id="37698-111">Müügitellimuse saab ootele panna käsitsi tellimuse loomisel või hiljem.</span><span class="sxs-lookup"><span data-stu-id="37698-111">A sales order can be put on hold manually at the time of order creation or later.</span></span> <span data-ttu-id="37698-112">Lisaks saab tellimuse automaatselt ootele panna pettuse reeglite alusel.</span><span class="sxs-lookup"><span data-stu-id="37698-112">Additionally, an order can be put on hold automatically, based on fraud rules.</span></span> <span data-ttu-id="37698-113">Kui müügitellimus on ootel, peate seda võib-olla lisateabefa värskendama.</span><span class="sxs-lookup"><span data-stu-id="37698-113">While a sales order is on hold, you might have to update it with more information.</span></span> <span data-ttu-id="37698-114">Teise võimalusena soovite võib-olla müügitellimuse välja registreerida, kui sellega tööd jätkate.</span><span class="sxs-lookup"><span data-stu-id="37698-114">Alternatively, you might want to check out the sales order as you continue to work on it.</span></span> <span data-ttu-id="37698-115">Saate müügitellimuse välja registreerida, selle uuesti sisse registreerida ja isegi alistada teise kasutaja väljaregistreerimise, kasutades tellimuse ooteloleku töölauda (**Jaemüük** &gt; **Kliendid** &gt; **Ootelolevad tellimused**).</span><span class="sxs-lookup"><span data-stu-id="37698-115">You can check out a sales order, check it back in, and even override the checkout of another user by using the order hold workbench (**Retail** &gt; **Customers** &gt; **Order holds**).</span></span> <span data-ttu-id="37698-116">Kui tellimus on lõpule viimiseks valmis, peate eemaldama ooteloleku, enne kui saate tellimuse protsessi lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="37698-116">When an order is ready to be completed, you must remove the hold before you can complete the order process.</span></span>




