---
title: Sama partii reserveerimine müügitellimuse jaoks
description: Selles artiklis selgitatakse, kuidas seadistada toodet lubama varude reserveerimist üksiku varude partii suhtes.
author: omulvad
manager: tfehr
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0fb1f9e017de71d01fbf7a05b579d68b702aa7c9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001495"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="f1bde-103">Sama partii reserveerimine müügitellimuse jaoks</span><span class="sxs-lookup"><span data-stu-id="f1bde-103">Reserve the same batch for a sales order</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1bde-104">Selles artiklis selgitatakse, kuidas seadistada toodet lubama varude reserveerimist üksiku varude partii suhtes.</span><span class="sxs-lookup"><span data-stu-id="f1bde-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="f1bde-105">Sama partii reserveerimisel saate reserveerida müügitellimuse rea varusid ühe varupartii suhtes.</span><span class="sxs-lookup"><span data-stu-id="f1bde-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="f1bde-106">Näiteks võib tapeeti telliv klient soovida, et kogu tellimus täidetaks samast partiist, et vältida rullidevahelist erinevust.</span><span class="sxs-lookup"><span data-stu-id="f1bde-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="f1bde-107">Toote seadistamiseks nii, et kasutataks sama partii reserveerimist, peavad järgmised sätted olema tootele määratavas kauba mudeligrupis, jälgimisdimensioonide grupis ja laoala dimensioonigrupis aktiivsed.</span><span class="sxs-lookup"><span data-stu-id="f1bde-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

- <span data-ttu-id="f1bde-108">**Kauba mudeligrupid** – kauba mudeligrupil peavad olema varude poliitikate väljagrupis **Reserveerimine** valitud väljad **Sama partii valimine** ja **Konsolideeri vajadus**.</span><span class="sxs-lookup"><span data-stu-id="f1bde-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
- <span data-ttu-id="f1bde-109">**Jälgimisdimensioonide grupid** – jälgimisdimensiooni grupil peab olema partiinumbri puhul valitud väli **Laovarude planeerimine dimensioonide kaupa**.</span><span class="sxs-lookup"><span data-stu-id="f1bde-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
- <span data-ttu-id="f1bde-110">**Laodimensioonide grupid** – laodimensiooni grupil peab olema väljadele **Laoala** ja **Ladu** valitud väli **Laovarude planeerimine dimensioonide kaupa**.</span><span class="sxs-lookup"><span data-stu-id="f1bde-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="f1bde-111">Kui reserveerite sama partii valikuga müügitellimuse real olevale tootele varusid, püüab süsteem reserveerida tellitud koguse ühest varude partiist.</span><span class="sxs-lookup"><span data-stu-id="f1bde-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, the system tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="f1bde-112">Arvestatakse ka konkreetse partii atribuudi nõudeid.</span><span class="sxs-lookup"><span data-stu-id="f1bde-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="f1bde-113">Kui kogust ei saa ühest partiist täita, kuvatakse leht **Sama partii reserveerimise konflikt**.</span><span class="sxs-lookup"><span data-stu-id="f1bde-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="f1bde-114">See leht kirjeldab probleeme ja ka tegevusi, mida saate reserveerimise jätkamiseks teha.</span><span class="sxs-lookup"><span data-stu-id="f1bde-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="f1bde-115">Järgmised tingimused võivad partii reserveerimist takistada.</span><span class="sxs-lookup"><span data-stu-id="f1bde-115">The following conditions might prevent the batch from being reserved:</span></span>

- <span data-ttu-id="f1bde-116">Partii likvideerimiskoodil on müügi väljal **Blokeeri reserveering** lipp **Blokeeritud**.</span><span class="sxs-lookup"><span data-stu-id="f1bde-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
- <span data-ttu-id="f1bde-117">Partii on aegumiskuupäeva ja kehtivate kliendi müümispäevade alusel aegunud.</span><span class="sxs-lookup"><span data-stu-id="f1bde-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="f1bde-118">Kaupa saab siiski reserveerimisel arvestada, kui kauba mudeligrupp on selle kauba puhul arvestatakse „esimesena aegunud esimesena välja” (FEFO) kuupäeva ja kui komplekteerimise kriteeriumina on valitud parim-enne kuupäev.</span><span class="sxs-lookup"><span data-stu-id="f1bde-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
- <span data-ttu-id="f1bde-119">Partiil pole jäänud järele piisavalt kõlblikkusaja päevi, tuginedes aegumiskuupäevale ja parim-enne kuupäevale, millele on liidetud kliendi müümispäevad.</span><span class="sxs-lookup"><span data-stu-id="f1bde-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>

<span data-ttu-id="f1bde-120">Laoala dimensiooni grupiga seostatud kaupade puhul, millel on lubatud suvand **Kasuta laohaldusprotsesse**, saate reserveerida kindlaid partiinumbreid, kasutades reserveerimishierarhiat, kus partiinumbri varude dimensioon on määratletud asukohadimensiooni kohal.</span><span class="sxs-lookup"><span data-stu-id="f1bde-120">For items associated with a storage dimension group that has **Use warehouse management processes** enabled, you can reserve specific batch numbers by using a reservation hierarchy with the batch number inventory dimension defined above the location dimension.</span></span> <span data-ttu-id="f1bde-121">Müügi ja ülekandetellimuse ridade lehel **Partii reserveerimine** saate ka valida ja reserveerida mitu rida saadaolevate partiinumbrite põhjal.</span><span class="sxs-lookup"><span data-stu-id="f1bde-121">The **Batch reservation** page for sales and transfer order lines also lets you select and reserve multiple lines based on the available batch numbers.</span></span> <span data-ttu-id="f1bde-122">Lisateabe saamiseks selle kohta, mida teha, kui kasutate reserveerimishierarhiat, kus partiinumbri dimensioon on asukoha all, vaadake teemat [Paindlik dimensiooni reserveerimise poliitika laotaseme](../warehousing/flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="f1bde-122">For more information about what to do if you are using a reservation hierarchy that has the batch number dimension below the location, see [Flexible warehouse-level dimension reservation policy](../warehousing/flexible-warehouse-level-dimension-reservation.md).</span></span>
