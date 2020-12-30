---
title: " Kõnekeskuse tellimuste loomine"
description: See protseduur juhendab kliendi otsimisel, uue tellimuse loomisel, toote otsimisel ja kliendilt makse vastuvõtmisel.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c875eaa85d9da997b75b296ad9ace99ae1e91798
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594232"
---
# <a name="create-call-center-orders"></a><span data-ttu-id="f4a57-103"> Kõnekeskuse tellimuste loomine</span><span class="sxs-lookup"><span data-stu-id="f4a57-103">Create call center orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4a57-104">See protseduur juhendab kliendi otsimisel, uue tellimuse loomisel, toote otsimisel ja kliendilt makse vastuvõtmisel.</span><span class="sxs-lookup"><span data-stu-id="f4a57-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="f4a57-105">See protseduur kasutab ettevõtte USRT demoandmeid ja on mõeldud müügitellimuste ametnikule.</span><span class="sxs-lookup"><span data-stu-id="f4a57-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="f4a57-106">Eeltingimused: kasutaja, kes viib protseduuri lõpule, häälestatakse kõnekeskuse kasutajana ja Fabrikami poolaastakataloogis avaldatakse vähemalt üks lähtekood.</span><span class="sxs-lookup"><span data-stu-id="f4a57-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="f4a57-107">Avage **Jaemüük ja kaubandus \> Kliendid \> Klienditeenindus**.</span><span class="sxs-lookup"><span data-stu-id="f4a57-107">Go to **Retail and Commerce \> Customers \> Customer service**.</span></span>
2. <span data-ttu-id="f4a57-108">Sisestage väljale **SearchText** otsingukriteeriumid kliendi leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="f4a57-108">For **SearchText**, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="f4a57-109">Selleks näidisprotseduuriks sisestage „Karen” ja valige **Vahekaart**.</span><span class="sxs-lookup"><span data-stu-id="f4a57-109">For this example procedure, enter "Karen" and select **Tab**.</span></span>  
3. <span data-ttu-id="f4a57-110">Valige Otsi.</span><span class="sxs-lookup"><span data-stu-id="f4a57-110">Select Search.</span></span>
    * <span data-ttu-id="f4a57-111">Kuna demoandmetes on ainult ühe kliendi nimi Karen, valitakse tulemus automaatselt.</span><span class="sxs-lookup"><span data-stu-id="f4a57-111">Since there is only one customer named "Karen" in demo data, the result will be automatically selected.</span></span>  
4. <span data-ttu-id="f4a57-112">Valige **Uus müügitellimus**.</span><span class="sxs-lookup"><span data-stu-id="f4a57-112">Select **New sales order**.</span></span>
5. <span data-ttu-id="f4a57-113">Laiendage või ahendage jaotise **Müügitellimus** päiseosa.</span><span class="sxs-lookup"><span data-stu-id="f4a57-113">Expand or collapse the **Sales order** header section.</span></span>
6. <span data-ttu-id="f4a57-114">Valige kataloogi jaoks lähtekood.</span><span class="sxs-lookup"><span data-stu-id="f4a57-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="f4a57-115">Kui ühtegi aktiivset lähtekoodi ei ole, saab selle etapi vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="f4a57-115">If there are no active source codes you can skip this step.</span></span>  
7. <span data-ttu-id="f4a57-116">Valige **Lisa rida**.</span><span class="sxs-lookup"><span data-stu-id="f4a57-116">Select **Add line**.</span></span>
8. <span data-ttu-id="f4a57-117">Sisestage väljale **Kaubakood** kauba otsingusõna.</span><span class="sxs-lookup"><span data-stu-id="f4a57-117">For **Item number**, enter the item search term.</span></span>
    * <span data-ttu-id="f4a57-118">Selleks näidisprotseduuriks sisestage osaline kaubakood 8111 ja vajutage vahekaarti. See tegevus avab kauba otsinguakna.</span><span class="sxs-lookup"><span data-stu-id="f4a57-118">For this sample procedure, enter a partial item number of '8111' and press tab. This action will bring up the item search window.</span></span>  
9. <span data-ttu-id="f4a57-119">Valige toode müügitellimusele lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="f4a57-119">Select the product to add to the sales order.</span></span>
10. <span data-ttu-id="f4a57-120">Sisestage müügikogus.</span><span class="sxs-lookup"><span data-stu-id="f4a57-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="f4a57-121">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="f4a57-121">Select **Create**.</span></span>
12. <span data-ttu-id="f4a57-122">Klõpsake kliendi makse vastuvõtmiseks nuppu Complete **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="f4a57-122">Select **Complete** to capture the customer payment.</span></span>
13. <span data-ttu-id="f4a57-123">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="f4a57-123">Select **Add**.</span></span>
    * <span data-ttu-id="f4a57-124">Lisamise link on vahekaardil Payments (Maksed). Laiendage maksete vahekaarti, kui see on kokku pandud.</span><span class="sxs-lookup"><span data-stu-id="f4a57-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="f4a57-125">Valige makseviis.</span><span class="sxs-lookup"><span data-stu-id="f4a57-125">Select the payment method.</span></span>
    * <span data-ttu-id="f4a57-126">Valige selle protseduuri jaoks sularaha maksemeetod.</span><span class="sxs-lookup"><span data-stu-id="f4a57-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="f4a57-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f4a57-127">Close the page.</span></span>
16. <span data-ttu-id="f4a57-128">Sisestage summa.</span><span class="sxs-lookup"><span data-stu-id="f4a57-128">Enter the amount.</span></span>
    * <span data-ttu-id="f4a57-129">Sisestage selle protseduuri jaoks summa, mis on võrdne tellimuse saldoga, mis on nähtav müügitellimuse kokkuvõtte lehel summa väljast vasakul pool.</span><span class="sxs-lookup"><span data-stu-id="f4a57-129">For this procedure, enter an amount equal to the order balance that can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="f4a57-130">See tegevus võimaldab teil tellimuse täielikult tasutuna lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="f4a57-130">This action will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="f4a57-131">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="f4a57-131">Select **OK**.</span></span>
18. <span data-ttu-id="f4a57-132">Valige käsk **Esita**.</span><span class="sxs-lookup"><span data-stu-id="f4a57-132">Select **Submit**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4a57-133">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f4a57-133">Additional resources</span></span>

[<span data-ttu-id="f4a57-134">Tehingumeilide kohandamine tarneviisi alusel</span><span class="sxs-lookup"><span data-stu-id="f4a57-134">Customize transactional emails by mode of delivery</span></span>](../customize-email-delivery-mode.md)

[<span data-ttu-id="f4a57-135">Kassas tarneviisi muutmine</span><span class="sxs-lookup"><span data-stu-id="f4a57-135">Change mode of delivery in POS</span></span>](../pos-change-delivery-mode.md)

