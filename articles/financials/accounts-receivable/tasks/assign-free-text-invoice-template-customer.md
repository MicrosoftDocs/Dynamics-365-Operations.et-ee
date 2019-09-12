---
title: Vabas vormis arve malli määramine kliendile
description: See ülesanne näitab, kuidas määrata kliendile vabas vormis arve mall.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d9535a4678ea0c68227a54cf3c5d1b06b116a288
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916342"
---
# <a name="assign-free-text-invoice-template-to-a-customer"></a><span data-ttu-id="df80f-103">Vabas vormis arve malli määramine kliendile</span><span class="sxs-lookup"><span data-stu-id="df80f-103">Assign free text invoice template to a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="df80f-104">See ülesanne näitab, kuidas määrata kliendile vabas vormis arve mall.</span><span class="sxs-lookup"><span data-stu-id="df80f-104">This task demonstrates how to assign a free text invoice template to a customer.</span></span> <span data-ttu-id="df80f-105">See ülesanne kasutab demoettevõtet USMF ja on mõeldud müügireskontro arvete haldamise ja töötlemise eest vastutavale kasutajale.</span><span class="sxs-lookup"><span data-stu-id="df80f-105">This task uses the USMF demo company and is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="df80f-106">**Navigeerimispaan**il avage **Moodulid > Müügireskontro > Kliendid > Kõik kliendid**.</span><span class="sxs-lookup"><span data-stu-id="df80f-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="df80f-107">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="df80f-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="df80f-108">Paanil **Toimingupaan** klõpsake **Arve**.</span><span class="sxs-lookup"><span data-stu-id="df80f-108">On the **Action Pane**, click **Invoice**.</span></span>
4. <span data-ttu-id="df80f-109">Klõpsake **Korduvad arved**.</span><span class="sxs-lookup"><span data-stu-id="df80f-109">Click **Recurring invoices**.</span></span> <span data-ttu-id="df80f-110">Kasutage seda lehte klientidele vabas vormis arve määramiseks ja määratlemaks, kui sageli arveid kliendile saadetakse.</span><span class="sxs-lookup"><span data-stu-id="df80f-110">Use this page to assign free text invoice templates to customers and specify how frequently invoices will be sent to the customer.</span></span>  
5. <span data-ttu-id="df80f-111">Klõpsake **Uus**, et määrata kliendile uus mall.</span><span class="sxs-lookup"><span data-stu-id="df80f-111">Click **New** to assign a new template to the customer.</span></span>
6. <span data-ttu-id="df80f-112">Väljal **Mall** valige vabas vormis arve mall, mille soovite kliendile määrata.</span><span class="sxs-lookup"><span data-stu-id="df80f-112">In the **Template** field, select the free text invoice template you want to assign to the customer.</span></span>
7. <span data-ttu-id="df80f-113">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="df80f-113">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="df80f-114">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="df80f-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="df80f-115">Väljale **Arvelduse alguskuupäev** sisestage kuupäev, millal koostatakse esimene arve.</span><span class="sxs-lookup"><span data-stu-id="df80f-115">In the **Billing start date** field, enter the date when the first invoice will be generated.</span></span>
10. <span data-ttu-id="df80f-116">Jaotisesse **Kordumise lõpp** sisestage kordumise lõppkuupäev.</span><span class="sxs-lookup"><span data-stu-id="df80f-116">In the **Recurrence end** section, enter a recurring end date.</span></span>  
    * <span data-ttu-id="df80f-117">Valige üks järgmistest: Lõppkuupäev puudub – arveid luuakse lõputult, kuni mall kliendi kontolt eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="df80f-117">Select one of the following: No end date – Invoices will be generated indefinitely until the template is removed from the customer account.</span></span>
    * <span data-ttu-id="df80f-118">Arvelduse lõppkuupäev – valige see suvand ja sisestage viimane kuupäev, millal arvet saab koostada.</span><span class="sxs-lookup"><span data-stu-id="df80f-118">Billing end date – Select this option and enter the last date that the invoice can be generated.</span></span>  
11. <span data-ttu-id="df80f-119">Väljale **Maksimaalne kumulatiivne summa** sisestage maksimaalne kumulatiivne summa, pärast mida lõpetatakse arve koostamine.</span><span class="sxs-lookup"><span data-stu-id="df80f-119">In the **Maximum cummulative amount** field, enter the maximum cumulative amount after which invoice generation will stop.</span></span> <span data-ttu-id="df80f-120">Sisestage maksimaalne kumulatiivne summa, mille saab valitud malli abil saavutada.</span><span class="sxs-lookup"><span data-stu-id="df80f-120">Enter the maximum cumulative amount that can be reached using the selected template.</span></span> <span data-ttu-id="df80f-121">Näiteks kui sisestate 1000,00 ja loote iga kuu puhul 100,00 arvet, peatatakse arvete loomine pärast kümnenda arve loomist.</span><span class="sxs-lookup"><span data-stu-id="df80f-121">For example, if you enter 1,000.00 and generate monthly invoices for 100.00 each, invoices will stop generating after the tenth invoice is generated.</span></span>  
12. <span data-ttu-id="df80f-122">Jaotises **Loo korduvaid arved, kasutades vaikeväärtusi** valige kas vabas vormis arve mall või kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="df80f-122">In the **Generate recurring invoices by using the default values from** section, select either free text invoice template or the customer account.</span></span> <span data-ttu-id="df80f-123">Valige, kas kasutada vaba teksti arve malli või kliendi kontot, et määrata keele, sisestusreeglite, käibemaksugrupi, loendikoodi, tarneriigi/-piirkonna, valuuta, maksetingimuste, makseviisi, maksetäpsustuse, maksegraafiku, skonto, finantsdimensioonide ja maksekorralduse vaikeväärtused arvete koostamisel.</span><span class="sxs-lookup"><span data-stu-id="df80f-123">Select whether to use the free text invoice template or the customer account to determine the default values for the language, posting profile, sales tax group, item sales tax group, list code, country/region for delivery, currency, terms of payment, method of payment, payment specification, payment schedule, cash discount, financial dimensions, and giro money transfer slip when invoices are created.</span></span>  
13. <span data-ttu-id="df80f-124">Väljal **Kordumissagedus** valige kordumissagedus.</span><span class="sxs-lookup"><span data-stu-id="df80f-124">In the **Recurrence pattern** field, select the recurrence pattern.</span></span>
    + <span data-ttu-id="df80f-125">Iga päev – valige see suvand ja sisestage päevade arv väljale Kohta.</span><span class="sxs-lookup"><span data-stu-id="df80f-125">Daily – Select this option and enter the number of days in the Per field.</span></span> <span data-ttu-id="df80f-126">Näiteks kui sisestate 15, koostatakse arve sellele kliendile iga 15 päeva tagant.</span><span class="sxs-lookup"><span data-stu-id="df80f-126">For example, if you enter 15, an invoice will be generated every 15 days for this customer.</span></span>
    + <span data-ttu-id="df80f-127">Iga nädal – valige see suvand ja sisestage nädalate arv väljale Kohta.</span><span class="sxs-lookup"><span data-stu-id="df80f-127">Weekly - Select this option and enter the number of weeks in the Per field.</span></span> <span data-ttu-id="df80f-128">Näiteks kui sisestate 2, koostatakse arve sellele kliendile iga kahe nädala tagant.</span><span class="sxs-lookup"><span data-stu-id="df80f-128">For example, if you enter 2, an invoice will be generated every two weeks for this customer.</span></span>
    + <span data-ttu-id="df80f-129">Iga kuu – valige see suvand ja sisestage kuude arv väljale Kohta.</span><span class="sxs-lookup"><span data-stu-id="df80f-129">Monthly - Select this option and enter the number of months in the Per field.</span></span> <span data-ttu-id="df80f-130">Näiteks kui sisestate 6, koostatakse arve sellele kliendile iga kuue kuu tagant.</span><span class="sxs-lookup"><span data-stu-id="df80f-130">For example, if you enter 6, an invoice will be generated every six months for this customer.</span></span>
    + <span data-ttu-id="df80f-131">Iga aasta – valige see suvand ja sisestage aastate arv väljale Kohta.</span><span class="sxs-lookup"><span data-stu-id="df80f-131">Yearly – Select this option and enter the number of years in the Per field.</span></span> <span data-ttu-id="df80f-132">Näiteks kui sisestate 2, koostatakse arve sellele kliendile iga kahe aasta tagant.</span><span class="sxs-lookup"><span data-stu-id="df80f-132">For example, if you enter 2, an invoice will be generated every two years for this customer.</span></span>  
14. <span data-ttu-id="df80f-133">Väljale **Kohta** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="df80f-133">In the **Per** field, enter a number.</span></span>

