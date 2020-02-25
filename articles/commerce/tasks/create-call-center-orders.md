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
ms.openlocfilehash: d1675d21f1e4176839feace76359afdbdc336c99
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022259"
---
# <a name="create-call-center-orders"></a><span data-ttu-id="aeeec-103"> Kõnekeskuse tellimuste loomine</span><span class="sxs-lookup"><span data-stu-id="aeeec-103">Create call center orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="aeeec-104">See protseduur juhendab kliendi otsimisel, uue tellimuse loomisel, toote otsimisel ja kliendilt makse vastuvõtmisel.</span><span class="sxs-lookup"><span data-stu-id="aeeec-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="aeeec-105">See protseduur kasutab ettevõtte USRT demoandmeid ja on mõeldud müügitellimuste ametnikule.</span><span class="sxs-lookup"><span data-stu-id="aeeec-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="aeeec-106">Eeltingimused: kasutaja, kes viib protseduuri lõpule, häälestatakse kõnekeskuse kasutajana ja Fabrikami poolaastakataloogis avaldatakse vähemalt üks lähtekood.</span><span class="sxs-lookup"><span data-stu-id="aeeec-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="aeeec-107">Avage Jaemüük ja kaubandus > Kliendid > Klienditeenindus.</span><span class="sxs-lookup"><span data-stu-id="aeeec-107">Go to Retail and Commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="aeeec-108">Sisestage väljale SearchText otsingukriteeriumid kliendi leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="aeeec-108">In the SearchText field, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="aeeec-109">Selleks näidisprotseduuriks trükkige "karen" ja vajutage klahvi Tab.</span><span class="sxs-lookup"><span data-stu-id="aeeec-109">For this example procedure type in 'karen' and press tab.</span></span>  
3. <span data-ttu-id="aeeec-110">Klõpsake nuppu Otsing.</span><span class="sxs-lookup"><span data-stu-id="aeeec-110">Click Search.</span></span>
    * <span data-ttu-id="aeeec-111">Kuna demoandmetes on ainult ühe kliendi nimi Karen, valitakse need automaatselt.</span><span class="sxs-lookup"><span data-stu-id="aeeec-111">Since there is only one customer named Karen in demo data they will be automatically selected.</span></span>  
4. <span data-ttu-id="aeeec-112">Klõpsake valikul New sales order (Uus müügitellimus).</span><span class="sxs-lookup"><span data-stu-id="aeeec-112">Click New sales order.</span></span>
5. <span data-ttu-id="aeeec-113">Laiendage või ahendage jaotise Sales order (Müügitellimus) päiseosa.</span><span class="sxs-lookup"><span data-stu-id="aeeec-113">Expand or collapse the Sales order header section.</span></span>
6. <span data-ttu-id="aeeec-114">Valige kataloogi jaoks lähtekood.</span><span class="sxs-lookup"><span data-stu-id="aeeec-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="aeeec-115">Kui ühtegi aktiivset lähtekoodi ei ole, saab välja Source (Allikas) sulgeda ning selle etapi vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="aeeec-115">If there are no active Source codes you can close the Source field and skip this step.</span></span>  
7. <span data-ttu-id="aeeec-116">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="aeeec-116">Click Add line.</span></span>
8. <span data-ttu-id="aeeec-117">Sisestage väljale Item number (Kauba number) kauba otsingusõna.</span><span class="sxs-lookup"><span data-stu-id="aeeec-117">In the Item number field, enter the item search term.</span></span>
    * <span data-ttu-id="aeeec-118">Selleks näidisprotseduuriks sisestage osaline kaubanumber 8111 ja vajutage klahvi Tab. See avab kauba otsingu hüpikakna.</span><span class="sxs-lookup"><span data-stu-id="aeeec-118">For this sample procedure enter a partial item number of '8111' and press tab. This will pop up the item search window.</span></span>  
9. <span data-ttu-id="aeeec-119">Valige toode müügitellimusele lisamiseks</span><span class="sxs-lookup"><span data-stu-id="aeeec-119">Select the product to add to the sales order</span></span>
10. <span data-ttu-id="aeeec-120">Sisestage müügikogus.</span><span class="sxs-lookup"><span data-stu-id="aeeec-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="aeeec-121">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="aeeec-121">Click Create.</span></span>
12. <span data-ttu-id="aeeec-122">Klõpsake kliendi makse vastuvõtmiseks nuppu Complete (Valmis).</span><span class="sxs-lookup"><span data-stu-id="aeeec-122">Click Complete to capture the customer payment.</span></span>
13. <span data-ttu-id="aeeec-123">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="aeeec-123">Click Add.</span></span>
    * <span data-ttu-id="aeeec-124">Lisamise link on vahekaardil Payments (Maksed). Laiendage maksete vahekaarti, kui see on kokku pandud.</span><span class="sxs-lookup"><span data-stu-id="aeeec-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="aeeec-125">Valige makseviis.</span><span class="sxs-lookup"><span data-stu-id="aeeec-125">Select the payment method.</span></span>
    * <span data-ttu-id="aeeec-126">Valige selle protseduuri jaoks sularaha maksemeetod.</span><span class="sxs-lookup"><span data-stu-id="aeeec-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="aeeec-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="aeeec-127">Close the page.</span></span>
16. <span data-ttu-id="aeeec-128">Sisestage summa.</span><span class="sxs-lookup"><span data-stu-id="aeeec-128">Enter the amount.</span></span>
    * <span data-ttu-id="aeeec-129">Sisestage selle protseduuri jaoks summa, mis on võrdne tellimuse saldoga, mis on nähtav müügitellimuse kokkuvõtte lehel summa väljast vasakul pool.</span><span class="sxs-lookup"><span data-stu-id="aeeec-129">For this procedure enter an amount equal to the order balance which can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="aeeec-130">See võimaldab teil tellimuse täielikult tasutuna lõpetada.</span><span class="sxs-lookup"><span data-stu-id="aeeec-130">This will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="aeeec-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="aeeec-131">Click OK.</span></span>
18. <span data-ttu-id="aeeec-132">Klõpsake Edasta.</span><span class="sxs-lookup"><span data-stu-id="aeeec-132">Click Submit.</span></span>

