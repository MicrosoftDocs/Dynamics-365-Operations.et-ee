--- 
title: Hankijamaksete loomine ja eksportimine ISO20022 maksevormingu abil
description: "See protseduur näitab, kuidas luua makseridu hankija makse töölehel ja kuidas luua hankija maksefaili, kasutades ISO2022 kreeditülekande näidet."
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 032f1f09fd017a2ae8cf5973d9f5c6ee99ca797f
ms.contentlocale: et-ee
ms.lasthandoff: 09/14/2018

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="5dbef-103">Hankijamaksete loomine ja eksportimine ISO20022 maksevormingu abil</span><span class="sxs-lookup"><span data-stu-id="5dbef-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5dbef-104">See protseduur näitab, kuidas luua makseridu hankija makse töölehel ja kuidas luua hankija maksefaili, kasutades ISO2022 kreeditülekande näidet.</span><span class="sxs-lookup"><span data-stu-id="5dbef-104">This procedure shows how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span> 

<span data-ttu-id="5dbef-105">Selle protseduuri loomiseks kasutatav demoandmete ettevõte on DEMF.</span><span class="sxs-lookup"><span data-stu-id="5dbef-105">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="5dbef-106">See on viies viiest protseduurist, mis illustreerib hankija makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="5dbef-106">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="5dbef-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="5dbef-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-payment-lines"></a><span data-ttu-id="5dbef-108">Makseridade loomine</span><span class="sxs-lookup"><span data-stu-id="5dbef-108">Create payment lines</span></span>
1. <span data-ttu-id="5dbef-109">Avage Ostureskontro > Maksed > Makse tööleht.</span><span class="sxs-lookup"><span data-stu-id="5dbef-109">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="5dbef-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="5dbef-110">Click New.</span></span>
3. <span data-ttu-id="5dbef-111">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="5dbef-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="5dbef-112">Sisestage või valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="5dbef-112">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="5dbef-113">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="5dbef-113">Click Lines.</span></span>
6. <span data-ttu-id="5dbef-114">Klõpsake suvandit Maksesoovitus.</span><span class="sxs-lookup"><span data-stu-id="5dbef-114">Click Payment proposal.</span></span>
7. <span data-ttu-id="5dbef-115">Klõpsake suvandit Loo maksesoovitus.</span><span class="sxs-lookup"><span data-stu-id="5dbef-115">Click Create payment proposal.</span></span>
8. <span data-ttu-id="5dbef-116">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="5dbef-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="5dbef-117">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="5dbef-117">Click Filter.</span></span>
10. <span data-ttu-id="5dbef-118">Valige loendist rida tabelile Hankijad ja väljale Hankija konto.</span><span class="sxs-lookup"><span data-stu-id="5dbef-118">In the list, select the row for Vendors table and Vendor account field.</span></span>
11. <span data-ttu-id="5dbef-119">Sisestage või valige väärtus väljal Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="5dbef-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="5dbef-120">Saate rakendada mis tahes kriteeriume makstavate hankija kannete valimiseks, selles näites kasutage hankija kontot DE-001.</span><span class="sxs-lookup"><span data-stu-id="5dbef-120">You can apply any criteria for selecting vendor transactions to pay, for this example use DE-001 as a vendor account.</span></span>  
12. <span data-ttu-id="5dbef-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5dbef-121">Click OK.</span></span>
13. <span data-ttu-id="5dbef-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5dbef-122">Click OK.</span></span>
14. <span data-ttu-id="5dbef-123">Klõpsake suvandit Maksete loomine.</span><span class="sxs-lookup"><span data-stu-id="5dbef-123">Click Create payments.</span></span>

## <a name="generate-an-iso20022-payment-file"></a><span data-ttu-id="5dbef-124">ISO20022 maksefaili loomine</span><span class="sxs-lookup"><span data-stu-id="5dbef-124">Generate an ISO20022 payment file</span></span>


