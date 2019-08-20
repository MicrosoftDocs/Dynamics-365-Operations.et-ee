---
title: Käibemaksugruppide ja kauba käibemaksugruppide seadistamine
description: See ülesande salvestis annab teile ülevaate käibemaksu ja kauba käibemaksugruppide seadistamise kohta.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c58755be2c927de1d308576a2bff2ed3340db34
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846267"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="b666e-103">Käibemaksugruppide ja kauba käibemaksugruppide seadistamine</span><span class="sxs-lookup"><span data-stu-id="b666e-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b666e-104">See ülesande salvestis annab teile ülevaate käibemaksu ja kauba käibemaksugruppide seadistamise kohta.</span><span class="sxs-lookup"><span data-stu-id="b666e-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="b666e-105">Käibemaksugrupid on käibemaksukoodide grupid, mis on seotud klientide ja hankijatega.</span><span class="sxs-lookup"><span data-stu-id="b666e-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="b666e-106">Need on seotud ka pearaamatukontodega kannete puhul, mis pole konkreetse hankija või kliendi puhul sisestatud.</span><span class="sxs-lookup"><span data-stu-id="b666e-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="b666e-107">Kauba käibemaksugrupid on käibemaksukoodide grupid, mis on seotud ressurssidega, nagu tooted.</span><span class="sxs-lookup"><span data-stu-id="b666e-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="b666e-108">Konkreetse kande korral kehtivad käibemaksud määratletakse käibemaksukoodidega, mida sisaldavad nii kande käibemaksugrupp kui ka kauba käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="b666e-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="b666e-109">Käibemaksu saab arvutada vaid juhul, kui käibemaksugrupp ja kauba käibemaksugrupp valitakse iga kande puhul, mille puhul tuleb käibemaks arvutada või salvestada.</span><span class="sxs-lookup"><span data-stu-id="b666e-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="b666e-110">Avage Maks > Kaudsed maksud > Käibemaks > Käibemaksu grupid.</span><span class="sxs-lookup"><span data-stu-id="b666e-110">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="b666e-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b666e-111">Click New.</span></span>
3. <span data-ttu-id="b666e-112">Sisestage väärtus väljale Käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="b666e-112">In the Sales tax group field, type a value.</span></span>
4. <span data-ttu-id="b666e-113">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="b666e-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b666e-114">Lülitage jaotise Seadistus laiendamist.</span><span class="sxs-lookup"><span data-stu-id="b666e-114">Toggle the expansion of the Setup section.</span></span>
6. <span data-ttu-id="b666e-115">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="b666e-115">Click Add.</span></span>
7. <span data-ttu-id="b666e-116">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b666e-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="b666e-117">Klõpsake väljal Käibemaksukood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b666e-117">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="b666e-118">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b666e-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="b666e-119">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b666e-119">Click Save.</span></span>
11. <span data-ttu-id="b666e-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b666e-120">Close the page.</span></span>
12. <span data-ttu-id="b666e-121">Avage Maks > Kaudsed maksud > Käibemaks > Käibemaksukoodid.</span><span class="sxs-lookup"><span data-stu-id="b666e-121">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
13. <span data-ttu-id="b666e-122">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b666e-122">Click New.</span></span>
14. <span data-ttu-id="b666e-123">Sisestage väärtus väljale Kauba käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="b666e-123">In the Item sales tax group field, type a value.</span></span>
15. <span data-ttu-id="b666e-124">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="b666e-124">In the Description field, type a value.</span></span>
16. <span data-ttu-id="b666e-125">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="b666e-125">Click Add.</span></span>
17. <span data-ttu-id="b666e-126">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b666e-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="b666e-127">Klõpsake väljal Käibemaksukood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b666e-127">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="b666e-128">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b666e-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="b666e-129">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b666e-129">Click Save.</span></span>

