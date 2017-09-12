--- 
title: "Vabas vormis arve malli määramine kliendile"
description: "See ülesanne näitab, kuidas määrata kliendile vabas vormis arve mall."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3bcb59c6edd04877dc2a052002be513205ae840a
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a><span data-ttu-id="f5e59-103">Vabas vormis arve malli määramine kliendile</span><span class="sxs-lookup"><span data-stu-id="f5e59-103">Assign a free text invoice template to a customer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f5e59-104">See ülesanne näitab, kuidas määrata kliendile vabas vormis arve mall.</span><span class="sxs-lookup"><span data-stu-id="f5e59-104">This task demonstrates how to assign a free text invoice template to a customer.</span></span> <span data-ttu-id="f5e59-105">See ülesanne kasutab demoettevõtet USMF ja on mõeldud müügireskontro arvete haldamise ja töötlemise eest vastutavale kasutajale.</span><span class="sxs-lookup"><span data-stu-id="f5e59-105">This task uses the USMF demo company and is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="f5e59-106">Avage Müügireskontro > Kliendid > Kõik kliendid.</span><span class="sxs-lookup"><span data-stu-id="f5e59-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="f5e59-107">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f5e59-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f5e59-108">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="f5e59-108">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="f5e59-109">Klõpsake suvandit Korduvad arved.</span><span class="sxs-lookup"><span data-stu-id="f5e59-109">Click Recurring invoices.</span></span>
    * <span data-ttu-id="f5e59-110">Kasutage seda lehte klientidele vabas vormis arve määramiseks ja määratlemaks, kui sageli arveid kliendile saadetakse.</span><span class="sxs-lookup"><span data-stu-id="f5e59-110">Use this page to assign free text invoice templates to customers and specify how frequently invoices will be sent to the customer.</span></span>  
5. <span data-ttu-id="f5e59-111">Klõpsake kliendile uue malli määramiseks suvandit Uus.</span><span class="sxs-lookup"><span data-stu-id="f5e59-111">Click New to assign a new template to the customer.</span></span>
6. <span data-ttu-id="f5e59-112">Valige vabas vormis arve mall, mille soovite kliendile määrata.</span><span class="sxs-lookup"><span data-stu-id="f5e59-112">Select the free text invoice template you want to assign to the customer.</span></span>
7. <span data-ttu-id="f5e59-113">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f5e59-113">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="f5e59-114">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f5e59-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f5e59-115">Sisestage esimese arve loomise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="f5e59-115">Enter the date when the first invoice will be generated.</span></span>
    * <span data-ttu-id="f5e59-116">Sisestage korduv lõppkuupäev.</span><span class="sxs-lookup"><span data-stu-id="f5e59-116">Enter a recurring end date.</span></span>  
    * <span data-ttu-id="f5e59-117">Valige üks järgmistest: Lõppkuupäev puudub – arveid luuakse lõputult, kuni mall kliendi kontolt eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="f5e59-117">Select one of the following: No end date – Invoices will be generated indefinitely until the template is removed from the customer account.</span></span>  <span data-ttu-id="f5e59-118">Arvelduse lõppkuupäev – valige see suvand viimase päeva sisestamiseks, millal arvet saab koostada.</span><span class="sxs-lookup"><span data-stu-id="f5e59-118">Billing end date – Select this option and enter the last date that the invoice can be generated.</span></span>  
    * <span data-ttu-id="f5e59-119">Maksimaalne kumulatiivne summa, mille järel arve loomine peatatakse.</span><span class="sxs-lookup"><span data-stu-id="f5e59-119">Maximum cumulative amount after which invoice generation will stop.</span></span>  
    * <span data-ttu-id="f5e59-120">Sisestage maksimaalne kumulatiivne summa, mille saab valitud malli abil saavutada.</span><span class="sxs-lookup"><span data-stu-id="f5e59-120">Enter the maximum cumulative amount that can be reached using the selected template.</span></span> <span data-ttu-id="f5e59-121">Näiteks kui sisestate 1000,00 ja loote iga kuu puhul 100,00 arvet, peatatakse arvete loomine pärast kümnenda arve loomist.</span><span class="sxs-lookup"><span data-stu-id="f5e59-121">For example, if you enter 1,000.00 and generate monthly invoices for 100.00 each, invoices will stop generating after the tenth invoice is generated.</span></span>  
    * <span data-ttu-id="f5e59-122">Looge korduvaid arveid, kasutades kas vabas vormis arve malli või kliendikonto vaikeväärtusi.</span><span class="sxs-lookup"><span data-stu-id="f5e59-122">Generate recurring invoices by using the default values from either free text invoice template or the customer account.</span></span>  
    * <span data-ttu-id="f5e59-123">Valige, kas kasutada vaba teksti arve malli või kliendi kontot, et määrata keele, sisestusreeglite, käibemaksugrupi, loendikoodi, tarneriigi/-piirkonna, valuuta, maksetingimuste, makseviisi, maksetäpsustuse, maksegraafiku, skonto, finantsdimensioonide ja maksekorralduse vaikeväärtused arvete koostamisel.</span><span class="sxs-lookup"><span data-stu-id="f5e59-123">Select whether to use the free text invoice template or the customer account to determine the default values for the language, posting profile, sales tax group, item sales tax group, list code, country/region for delivery, currency, terms of payment, method of payment, payment specification, payment schedule, cash discount, financial dimensions, and giro money transfer slip when invoices are created.</span></span>  
10. <span data-ttu-id="f5e59-124">Valige kordumismuster.</span><span class="sxs-lookup"><span data-stu-id="f5e59-124">Select the recurrence pattern.</span></span>
    * <span data-ttu-id="f5e59-125">Iga päev – valige see suvand ja sisestage päevade arv väljale Kohta.</span><span class="sxs-lookup"><span data-stu-id="f5e59-125">Daily – Select this option and enter the number of days in the Per field.</span></span> <span data-ttu-id="f5e59-126">Näiteks kui sisestate 15, koostatakse arve sellele kliendile iga 15 päeva tagant.</span><span class="sxs-lookup"><span data-stu-id="f5e59-126">For example, if you enter 15, an invoice will be generated every 15 days for this customer.</span></span>  <span data-ttu-id="f5e59-127">Iga nädal – valige see suvand ja sisestage nädalate arv väljale Kohta.</span><span class="sxs-lookup"><span data-stu-id="f5e59-127">Weekly - Select this option and enter the number of weeks in the Per field.</span></span> <span data-ttu-id="f5e59-128">Näiteks kui sisestate 2, koostatakse arve sellele kliendile iga kahe nädala tagant.</span><span class="sxs-lookup"><span data-stu-id="f5e59-128">For example, if you enter 2, an invoice will be generated every two weeks for this customer.</span></span>  <span data-ttu-id="f5e59-129">Iga kuu – valige see suvand ja sisestage kuude arv väljale Kohta.</span><span class="sxs-lookup"><span data-stu-id="f5e59-129">Monthly - Select this option and enter the number of months in the Per field.</span></span> <span data-ttu-id="f5e59-130">Näiteks kui sisestate 6, koostatakse arve sellele kliendile iga kuue kuu tagant.</span><span class="sxs-lookup"><span data-stu-id="f5e59-130">For example, if you enter 6, an invoice will be generated every six months for this customer.</span></span>  <span data-ttu-id="f5e59-131">Iga aasta – valige see suvand ja sisestage aastate arv väljale Kohta.</span><span class="sxs-lookup"><span data-stu-id="f5e59-131">Yearly – Select this option and enter the number of years in the Per field.</span></span> <span data-ttu-id="f5e59-132">Näiteks kui sisestate 2, koostatakse arve sellele kliendile iga kahe aasta tagant.</span><span class="sxs-lookup"><span data-stu-id="f5e59-132">For example, if you enter 2, an invoice will be generated every two years for this customer.</span></span>  
11. <span data-ttu-id="f5e59-133">Sisestage number väljale Kohta.</span><span class="sxs-lookup"><span data-stu-id="f5e59-133">In the Per field, enter a number.</span></span>


