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
ms.openlocfilehash: fd11068a31b5324d87416e7c00f75a59743f695a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813503"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="45905-103">Käibemaksu tasakaalustusperioodide seadistamine</span><span class="sxs-lookup"><span data-stu-id="45905-103">Set up sales tax settlement periods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="45905-104">Selles teemas selgitatakse, kuidas seadistada käibemaksu tasumise perioode.</span><span class="sxs-lookup"><span data-stu-id="45905-104">This topic explains how to set up sales tax settlement periods.</span></span> <span data-ttu-id="45905-105">Käibemaksu tasakaalustusperioodid sisaldavad teavet perioodivahemike kohta, mille puhul tuleb esitada ja maksta käibemaksu.</span><span class="sxs-lookup"><span data-stu-id="45905-105">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="45905-106">Tasakaalustusprotsessi saab käitada konkreetse kuupäevavahemiku tasakaalustusperioodi puhul.</span><span class="sxs-lookup"><span data-stu-id="45905-106">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="45905-107">Kõik tasakaalustusperioodiga seotud maksukoodid tasakaalustatakse.</span><span class="sxs-lookup"><span data-stu-id="45905-107">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="45905-108">Seotud käibemaksuhalduri seadistamisest olenevalt sisestatakse maksukohustus kas hankija või pearaamatu kontole.</span><span class="sxs-lookup"><span data-stu-id="45905-108">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>

<span data-ttu-id="45905-109">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="45905-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="45905-110">Minge navigeerimispaneelis **Moodulid > Maks > Kaudsed maksud > Käibemaks > Käibemaksu tasakaalustusperioodid**.</span><span class="sxs-lookup"><span data-stu-id="45905-110">In the navigation pane, go to **Modules > Tax > Indirect taxes > Sales tax > Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="45905-111">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="45905-111">Select **New**.</span></span>
3. <span data-ttu-id="45905-112">Sisestage välja **Tasakaalustusperiood** väärtus.</span><span class="sxs-lookup"><span data-stu-id="45905-112">In the **Settlement period** field, type a value.</span></span>
4. <span data-ttu-id="45905-113">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="45905-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="45905-114">Valige väljal **Maksuhaldur** käibemaksu haldur, kellele tasakaalustusperioodi puhul loodud aruanded ja maksed saadetakse.</span><span class="sxs-lookup"><span data-stu-id="45905-114">In the **Authority** field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="45905-115">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="45905-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="45905-116">Valige väljas **Maksetingimused** soovitud kirje rippmenüüst.</span><span class="sxs-lookup"><span data-stu-id="45905-116">In the **Terms of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="45905-117">Seotud käibemaksuhalduri saab seadistada kui hankija ja käibemaksu tasakaalustus loob avatud hankija arve.</span><span class="sxs-lookup"><span data-stu-id="45905-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="45905-118">Maksetingimused määratlevad avatud hankija arve maksetähtaja.</span><span class="sxs-lookup"><span data-stu-id="45905-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
8. <span data-ttu-id="45905-119">Valige tasakaalustusperioodi vahemike tüüp.</span><span class="sxs-lookup"><span data-stu-id="45905-119">Select a type for the settlement period intervals.</span></span>
9. <span data-ttu-id="45905-120">Sisestage perioodivahemiku ühikute arv perioodi kohta.</span><span class="sxs-lookup"><span data-stu-id="45905-120">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="45905-121">Näiteks kvartalis on 3 kuud.</span><span class="sxs-lookup"><span data-stu-id="45905-121">For example, a quarter has 3 months.</span></span>
10. <span data-ttu-id="45905-122">Märkige või tühjendage ruut **Kasuta käibemaksu tasakaalustamiseks pakktöötlust**.</span><span class="sxs-lookup"><span data-stu-id="45905-122">Select or clear the **Use batch processing for sales tax settlement** check box.</span></span> <span data-ttu-id="45905-123">Tasakaalustusperioodi tasakaalustusprotsessi saab töödelda taustal pakett-tööna.</span><span class="sxs-lookup"><span data-stu-id="45905-123">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="45905-124">See on soovitatav suure hulga maksukannete puhul kuupäevavahemiku jooksul.</span><span class="sxs-lookup"><span data-stu-id="45905-124">This is recommended for a large number of tax transactions within a period interval.</span></span>  
    > [!NOTE]
    > <span data-ttu-id="45905-125">Praegu puudub selle tugi Hispaanias, Jaapanis ja Hollandis.</span><span class="sxs-lookup"><span data-stu-id="45905-125">Currently this is not supported in Spain, Japan, and the Netherlands.</span></span>
11. <span data-ttu-id="45905-126">Märkige või tühjendage märkeruut **Vastasmaksukannete loomise ennetamine**.</span><span class="sxs-lookup"><span data-stu-id="45905-126">Select or clear the **Prevent generating offset tax transactions** check box.</span></span> <span data-ttu-id="45905-127">Süsteem loob tasakaalustusprotsessi ajal vaikimisi vastasmaksukandeid, mis põhjustavad jõudlusprobleeme, kui perioodivahemikul on suur hulk maksukandeid.</span><span class="sxs-lookup"><span data-stu-id="45905-127">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="45905-128">Märkige see märkeruut, et vältida vastasmaksukannete loomist.</span><span class="sxs-lookup"><span data-stu-id="45905-128">Select this check box to prevent generating offset tax transactions.</span></span>
12. <span data-ttu-id="45905-129">Laiendage vahekaarti **Perioodivahemikud**.</span><span class="sxs-lookup"><span data-stu-id="45905-129">Expand the **Period intervals** tab.</span></span>
13. <span data-ttu-id="45905-130">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="45905-130">Select **Add**.</span></span>
14. <span data-ttu-id="45905-131">Sisestage kuupäev välja **Alguskuupäev** uuele reale.</span><span class="sxs-lookup"><span data-stu-id="45905-131">In the **From date** field in the new row, enter a date.</span></span>
15. <span data-ttu-id="45905-132">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="45905-132">In the **To date** field, enter a date.</span></span>
16. <span data-ttu-id="45905-133">Valige **Uus perioodivahemik**.</span><span class="sxs-lookup"><span data-stu-id="45905-133">Select **New period interval**.</span></span> <span data-ttu-id="45905-134">Kui esimene perioodivahemik on sisestatud, saab uusi perioode luua automaatselt.</span><span class="sxs-lookup"><span data-stu-id="45905-134">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="45905-135">Vajaduse korral saate naasta ja uusi perioodivahemikke lisada.</span><span class="sxs-lookup"><span data-stu-id="45905-135">You can come back and add new period intervals as required.</span></span>  
17. <span data-ttu-id="45905-136">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="45905-136">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]