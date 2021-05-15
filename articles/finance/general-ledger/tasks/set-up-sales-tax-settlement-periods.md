---
title: Käibemaksu tasakaalustusperioodide seadistamine
description: Selles teemas selgitatakse, kuidas seadistada käibemaksu tasakaalustusperioode rakenduses Dynamics 365 Finance.
author: twheeloc
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 83587df3963d215fec020150e6b707e431c1b6eb
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944773"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="a094f-103">Käibemaksu tasakaalustusperioodide seadistamine</span><span class="sxs-lookup"><span data-stu-id="a094f-103">Set up sales tax settlement periods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a094f-104">Selles teemas selgitatakse, kuidas seadistada käibemaksu tasumise perioode.</span><span class="sxs-lookup"><span data-stu-id="a094f-104">This topic explains how to set up sales tax settlement periods.</span></span> <span data-ttu-id="a094f-105">Käibemaksu tasakaalustusperioodid sisaldavad teavet perioodivahemike kohta, mille puhul tuleb esitada ja maksta käibemaksu.</span><span class="sxs-lookup"><span data-stu-id="a094f-105">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="a094f-106">Tasakaalustusprotsessi saab käitada konkreetse kuupäevavahemiku tasakaalustusperioodi puhul.</span><span class="sxs-lookup"><span data-stu-id="a094f-106">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="a094f-107">Kõik tasakaalustusperioodiga seotud maksukoodid tasakaalustatakse.</span><span class="sxs-lookup"><span data-stu-id="a094f-107">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="a094f-108">Seotud käibemaksuhalduri seadistamisest olenevalt sisestatakse maksukohustus kas hankija või pearaamatu kontole.</span><span class="sxs-lookup"><span data-stu-id="a094f-108">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>

<span data-ttu-id="a094f-109">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="a094f-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="a094f-110">Minge navigeerimispaneelis **Moodulid > Maks > Kaudsed maksud > Käibemaks > Käibemaksu tasakaalustusperioodid**.</span><span class="sxs-lookup"><span data-stu-id="a094f-110">In the navigation pane, go to **Modules > Tax > Indirect taxes > Sales tax > Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="a094f-111">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a094f-111">Select **New**.</span></span>
3. <span data-ttu-id="a094f-112">Sisestage välja **Tasakaalustusperiood** väärtus.</span><span class="sxs-lookup"><span data-stu-id="a094f-112">In the **Settlement period** field, type a value.</span></span>
4. <span data-ttu-id="a094f-113">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="a094f-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="a094f-114">Valige väljal **Maksuhaldur** käibemaksu haldur, kellele tasakaalustusperioodi puhul loodud aruanded ja maksed saadetakse.</span><span class="sxs-lookup"><span data-stu-id="a094f-114">In the **Authority** field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="a094f-115">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="a094f-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="a094f-116">Valige väljas **Maksetingimused** soovitud kirje rippmenüüst.</span><span class="sxs-lookup"><span data-stu-id="a094f-116">In the **Terms of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="a094f-117">Seotud käibemaksuhalduri saab seadistada kui hankija ja käibemaksu tasakaalustus loob avatud hankija arve.</span><span class="sxs-lookup"><span data-stu-id="a094f-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="a094f-118">Maksetingimused määratlevad avatud hankija arve maksetähtaja.</span><span class="sxs-lookup"><span data-stu-id="a094f-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
8. <span data-ttu-id="a094f-119">Valige tasakaalustusperioodi vahemike tüüp.</span><span class="sxs-lookup"><span data-stu-id="a094f-119">Select a type for the settlement period intervals.</span></span>
9. <span data-ttu-id="a094f-120">Sisestage perioodivahemiku ühikute arv perioodi kohta.</span><span class="sxs-lookup"><span data-stu-id="a094f-120">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="a094f-121">Näiteks kvartalis on 3 kuud.</span><span class="sxs-lookup"><span data-stu-id="a094f-121">For example, a quarter has 3 months.</span></span>
10. <span data-ttu-id="a094f-122">Märkige või tühjendage ruut **Kasuta käibemaksu tasakaalustamiseks pakktöötlust**.</span><span class="sxs-lookup"><span data-stu-id="a094f-122">Select or clear the **Use batch processing for sales tax settlement** check box.</span></span> <span data-ttu-id="a094f-123">Tasakaalustusperioodi tasakaalustusprotsessi saab töödelda taustal pakett-tööna.</span><span class="sxs-lookup"><span data-stu-id="a094f-123">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="a094f-124">See on soovitatav suure hulga maksukannete puhul kuupäevavahemiku jooksul.</span><span class="sxs-lookup"><span data-stu-id="a094f-124">This is recommended for a large number of tax transactions within a period interval.</span></span>
11. <span data-ttu-id="a094f-125">Märkige või tühjendage märkeruut **Vastasmaksukannete loomise ennetamine**.</span><span class="sxs-lookup"><span data-stu-id="a094f-125">Select or clear the **Prevent generating offset tax transactions** check box.</span></span> <span data-ttu-id="a094f-126">Süsteem loob tasakaalustusprotsessi ajal vaikimisi vastasmaksukandeid, mis põhjustavad jõudlusprobleeme, kui perioodivahemikul on suur hulk maksukandeid.</span><span class="sxs-lookup"><span data-stu-id="a094f-126">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="a094f-127">Märkige see märkeruut, et vältida vastasmaksukannete loomist.</span><span class="sxs-lookup"><span data-stu-id="a094f-127">Select this check box to prevent generating offset tax transactions.</span></span>
12. <span data-ttu-id="a094f-128">Laiendage vahekaarti **Perioodivahemikud**.</span><span class="sxs-lookup"><span data-stu-id="a094f-128">Expand the **Period intervals** tab.</span></span>
13. <span data-ttu-id="a094f-129">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="a094f-129">Select **Add**.</span></span>
14. <span data-ttu-id="a094f-130">Sisestage kuupäev välja **Alguskuupäev** uuele reale.</span><span class="sxs-lookup"><span data-stu-id="a094f-130">In the **From date** field in the new row, enter a date.</span></span>
15. <span data-ttu-id="a094f-131">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="a094f-131">In the **To date** field, enter a date.</span></span>
16. <span data-ttu-id="a094f-132">Valige **Uus perioodivahemik**.</span><span class="sxs-lookup"><span data-stu-id="a094f-132">Select **New period interval**.</span></span> <span data-ttu-id="a094f-133">Kui esimene perioodivahemik on sisestatud, saab uusi perioode luua automaatselt.</span><span class="sxs-lookup"><span data-stu-id="a094f-133">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="a094f-134">Vajaduse korral saate naasta ja uusi perioodivahemikke lisada.</span><span class="sxs-lookup"><span data-stu-id="a094f-134">You can come back and add new period intervals as required.</span></span>  
17. <span data-ttu-id="a094f-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a094f-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
