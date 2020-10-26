---
title: Käibemaksugruppide ja kauba käibemaksugruppide seadistamine
description: See ülesande salvestis annab teile ülevaate käibemaksu ja kauba käibemaksugruppide seadistamise kohta.
author: twheeloc
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 24210129f7595c6544234c20915f4003bf0e1eb8
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3984693"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="930b1-103">Käibemaksugruppide ja kauba käibemaksugruppide seadistamine</span><span class="sxs-lookup"><span data-stu-id="930b1-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="930b1-104">See ülesande salvestis annab teile ülevaate käibemaksu ja kauba käibemaksugruppide seadistamise kohta.</span><span class="sxs-lookup"><span data-stu-id="930b1-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="930b1-105">Käibemaksugrupid on käibemaksukoodide grupid, mis on seotud klientide ja hankijatega.</span><span class="sxs-lookup"><span data-stu-id="930b1-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="930b1-106">Need on seotud ka pearaamatukontodega kannete puhul, mis pole konkreetse hankija või kliendi puhul sisestatud.</span><span class="sxs-lookup"><span data-stu-id="930b1-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="930b1-107">Kauba käibemaksugrupid on käibemaksukoodide grupid, mis on seotud ressurssidega, nagu tooted.</span><span class="sxs-lookup"><span data-stu-id="930b1-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="930b1-108">Konkreetse kande korral kehtivad käibemaksud määratletakse käibemaksukoodidega, mida sisaldavad nii kande käibemaksugrupp kui ka kauba käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="930b1-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="930b1-109">Käibemaksu saab arvutada vaid juhul, kui käibemaksugrupp ja kauba käibemaksugrupp valitakse iga kande puhul, mille puhul tuleb käibemaks arvutada või salvestada.</span><span class="sxs-lookup"><span data-stu-id="930b1-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="930b1-110">Avage **Navigeerimispaneel > Moodulid > Maks > Kaudsed maksud > Käibemaks > Käibemaksugrupid**.</span><span class="sxs-lookup"><span data-stu-id="930b1-110">Go to **Navigation pane > Modules > Tax > Indirect taxes > Sales tax > Sales tax groups**.</span></span>
2. <span data-ttu-id="930b1-111">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="930b1-111">Click **New**.</span></span>
3. <span data-ttu-id="930b1-112">Sisestage väärtus väljale **Käibemaksugrupp**.</span><span class="sxs-lookup"><span data-stu-id="930b1-112">In the **Sales tax group** field, type a value.</span></span>
4. <span data-ttu-id="930b1-113">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="930b1-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="930b1-114">Kasutage jaotise **Seadistus** laiendamist.</span><span class="sxs-lookup"><span data-stu-id="930b1-114">Toggle the expansion of the **Setup** section.</span></span>
6. <span data-ttu-id="930b1-115">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="930b1-115">Click **Add**.</span></span>
7. <span data-ttu-id="930b1-116">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="930b1-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="930b1-117">Klõpsake väljal **Käibemaksukood** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="930b1-117">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="930b1-118">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="930b1-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="930b1-119">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="930b1-119">Click **Save**.</span></span>
11. <span data-ttu-id="930b1-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="930b1-120">Close the page.</span></span>
12. <span data-ttu-id="930b1-121">Avage **Maks > Kaudsed maksud > Käibemaks > Kauba käibemaksugrupid**.</span><span class="sxs-lookup"><span data-stu-id="930b1-121">Go to **Tax > Indirect taxes > Sales tax > Item sales tax groups**.</span></span>
13. <span data-ttu-id="930b1-122">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="930b1-122">Click **New**.</span></span>
14. <span data-ttu-id="930b1-123">Sisestage väärtus väljale **Kauba käibemaksugrupp**.</span><span class="sxs-lookup"><span data-stu-id="930b1-123">In the **Item sales tax group** field, type a value.</span></span>
15. <span data-ttu-id="930b1-124">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="930b1-124">In the **Description** field, type a value.</span></span>
16. <span data-ttu-id="930b1-125">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="930b1-125">Click **Add**.</span></span>
17. <span data-ttu-id="930b1-126">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="930b1-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="930b1-127">Klõpsake väljal **Käibemaksukood** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="930b1-127">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="930b1-128">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="930b1-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="930b1-129">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="930b1-129">Click **Save**.</span></span>

