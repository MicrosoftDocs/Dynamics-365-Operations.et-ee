---
title: Varude blokeerimise loomine ja haldamine
description: See protseduur näitab, kuidas vältida füüsilise vaba kaubavaru reserveerimist teiste väljaminevate lähtedokumentidega, kasutades varude blokeerimist.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 845d517ad10245df3b208874df61e235c199c7fe
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836393"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="50444-103">Varude blokeerimise loomine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="50444-103">Create and maintain an inventory blocking</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="50444-104">See protseduur näitab, kuidas vältida füüsilise vaba kaubavaru reserveerimist teiste väljaminevate lähtedokumentidega, kasutades varude blokeerimist.</span><span class="sxs-lookup"><span data-stu-id="50444-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="50444-105">Saate käitada protseduuri demoandmete ettevõttes USMF näidatud näidisväärtusi kasutades.</span><span class="sxs-lookup"><span data-stu-id="50444-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="50444-106">Enne selle protseduuri alustamist peab teil olema füüsilise vaba kaubavaruga kaup saadaval.</span><span class="sxs-lookup"><span data-stu-id="50444-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="50444-107">Varude blokeerimise loomine</span><span class="sxs-lookup"><span data-stu-id="50444-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="50444-108">Avage Varude haldus > Perioodilised ülesanded > Varude blokeerimine.</span><span class="sxs-lookup"><span data-stu-id="50444-108">Go to Inventory management > Periodic tasks > Inventory blocking.</span></span>
2. <span data-ttu-id="50444-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="50444-109">Click New.</span></span>
3. <span data-ttu-id="50444-110">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="50444-110">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="50444-111">Valige loendist kaup, mille soovite valida.</span><span class="sxs-lookup"><span data-stu-id="50444-111">In the list, select the item you want to choose.</span></span> 
    * <span data-ttu-id="50444-112">Valige kauba number koos füüsilise vaba kaubavaruga, mida soovite blokeerida.</span><span class="sxs-lookup"><span data-stu-id="50444-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="50444-113">USMF-i kasutamisel saate valida kauba M9201.</span><span class="sxs-lookup"><span data-stu-id="50444-113">If you’re using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="50444-114">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="50444-114">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="50444-115">Kauba M9201 kasutamisel peate valima alla 200.</span><span class="sxs-lookup"><span data-stu-id="50444-115">If you’re using item M9201, you need to select less than 200.</span></span>  
6. <span data-ttu-id="50444-116">Laiendage jaotist Varude dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="50444-116">Toggle the expansion of the Inventory dimensions section.</span></span>
7. <span data-ttu-id="50444-117">Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="50444-117">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="50444-118">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="50444-118">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="50444-119">Kauba M9201 kasutamisel saate valida lao 51.</span><span class="sxs-lookup"><span data-stu-id="50444-119">If you’re using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="50444-120">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="50444-120">Click Save.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="50444-121">Varude blokeerimise tingimuste värskendamine</span><span class="sxs-lookup"><span data-stu-id="50444-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="50444-122">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="50444-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="50444-123">Blokeeritava koguse kajastamiseks värskendage varude koguse välja.</span><span class="sxs-lookup"><span data-stu-id="50444-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="50444-124">Sisestage kuupäev väljale Eeldatav kuupäev.</span><span class="sxs-lookup"><span data-stu-id="50444-124">In the Expected date field, enter a date.</span></span>
    * <span data-ttu-id="50444-125">Võite soovida näidata, millal blokeeritud varud peaks reserveerimiseks saadaolevaks muutuma, määrates eeldatava kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="50444-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="50444-126">Kui suvand Prognoositud sissetulekud on varude blokeerimise puhul valitud, nagu blokeerimise käsitsi loomisel vaikimisi, kuvatakse see kuupäev prognoositud kandel.</span><span class="sxs-lookup"><span data-stu-id="50444-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="50444-127">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="50444-127">Click Save.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="50444-128">Varude blokeerimise eemaldamine</span><span class="sxs-lookup"><span data-stu-id="50444-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="50444-129">Klõpsake  Kustuta.</span><span class="sxs-lookup"><span data-stu-id="50444-129">Click Delete.</span></span>
2. <span data-ttu-id="50444-130">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="50444-130">Click Yes.</span></span>
3. <span data-ttu-id="50444-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="50444-131">Close the page.</span></span>

