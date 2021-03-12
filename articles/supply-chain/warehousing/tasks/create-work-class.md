---
title: Tööklassi loomine
description: See protseduur näitab, kuidas seadistada tööklassi.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0e06cd5fc6dc27f79eb39bbd78932a166e9d442
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977209"
---
# <a name="create-a-work-class"></a><span data-ttu-id="2b28d-103">Tööklassi loomine</span><span class="sxs-lookup"><span data-stu-id="2b28d-103">Create a work class</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2b28d-104">See protseduur näitab, kuidas seadistada tööklassi.</span><span class="sxs-lookup"><span data-stu-id="2b28d-104">This procedure shows you how to set up a work class.</span></span> <span data-ttu-id="2b28d-105">Tööklassidega suunatakse ja/või piiratakse töötellimuse ridade tüüpi, mida laotöötaja saab mobiilses seadmes töödelda.</span><span class="sxs-lookup"><span data-stu-id="2b28d-105">Work classes are used to direct and/or limit the type of work order lines that a warehouse worker can process on a mobile device.</span></span> <span data-ttu-id="2b28d-106">Read, mida töötaja saab töödelda, määratakse mobiilse seadme menüü-üksustes, millele laotöötajal on juurdepääs, tööklassidest ja tööridadel määratud tööklassist.</span><span class="sxs-lookup"><span data-stu-id="2b28d-106">The lines that a worker can process are determined from the work classes on the mobile device menu items that the warehouse worker has access to and the work class that's specified on the work lines.</span></span> <span data-ttu-id="2b28d-107">Tööklasse saab kasutada ka mahapaneku asukoha kinnitamiseks töötellimuse rea puhul.</span><span class="sxs-lookup"><span data-stu-id="2b28d-107">Work classes can also be used to validate the put location for a work order line.</span></span> <span data-ttu-id="2b28d-108">Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega.</span><span class="sxs-lookup"><span data-stu-id="2b28d-108">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="2b28d-109">See protseduur on mõeldud laohaldurile.</span><span class="sxs-lookup"><span data-stu-id="2b28d-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="2b28d-110">Avage Laohaldus > Seadistus > Töö > Tööklassid.</span><span class="sxs-lookup"><span data-stu-id="2b28d-110">Go to Warehouse management > Setup > Work > Work classes.</span></span>
2. <span data-ttu-id="2b28d-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="2b28d-111">Click New.</span></span>
3. <span data-ttu-id="2b28d-112">Sisestage väärtus väljale Tööklassi ID.</span><span class="sxs-lookup"><span data-stu-id="2b28d-112">In the Work class ID field, type a value.</span></span>
4. <span data-ttu-id="2b28d-113">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="2b28d-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2b28d-114">Valige suvand väljal Töökäsu tüüp.</span><span class="sxs-lookup"><span data-stu-id="2b28d-114">In the Work order type field, select an option.</span></span>
6. <span data-ttu-id="2b28d-115">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="2b28d-115">Click New.</span></span>
7. <span data-ttu-id="2b28d-116">Sisestage väärtus väljale Asukoha tüüp.</span><span class="sxs-lookup"><span data-stu-id="2b28d-116">In the Location type field, type a value.</span></span>
    * <span data-ttu-id="2b28d-117">Asukoha tüübi valimisel piirab see asukohta, kuhu kaubad saab pärast komplekteerimist panna.</span><span class="sxs-lookup"><span data-stu-id="2b28d-117">If you select a location type, this sets a restriction on where items can be put after they've been picked.</span></span> <span data-ttu-id="2b28d-118">Seda sätet kasutatakse, kui asukohakorraldus püüab asukohta lahendada või kui laotöötaja esitab mobiilse seadme menüü-üksuse jaoks asukoha käsitsi.</span><span class="sxs-lookup"><span data-stu-id="2b28d-118">This setting is used when a location directive tries to resolve the location, or if a warehouse worker manually provides the location for the mobile device menu item.</span></span>  
8. <span data-ttu-id="2b28d-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2b28d-119">Close the page.</span></span>

