---
title: "Kõnekeskuse järjepidevusprogrammi seadistamine"
description: "Selles artiklis kirjeldatakse, kuidas seadistada kõnekeskuse järjepidevusprogrammi."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 00504b62237ac4f121d603d5144ffa4e71956cc3
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---

# <a name="set-up-a-continuity-program-for-a-call-center"></a><span data-ttu-id="23a82-103">Kõnekeskuse järjepidevusprogrammi seadistamine</span><span class="sxs-lookup"><span data-stu-id="23a82-103">Set up a continuity program for a call center</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="23a82-104">Selles artiklis kirjeldatakse, kuidas seadistada kõnekeskuse järjepidevusprogrammi.</span><span class="sxs-lookup"><span data-stu-id="23a82-104">This article describes how to set up a continuity program for a call center.</span></span>

<span data-ttu-id="23a82-105">Järjepidevusprogrammis, mida nimetatakse ka korduva tellimuse programmiks, saavad kliendid korrapäraselt tootesaadetisi eelmääratletud graafiku alusel.</span><span class="sxs-lookup"><span data-stu-id="23a82-105">In a continuity program, which is also known as a recurring order program, customers receive regular product shipments according to a predefined schedule.</span></span> <span data-ttu-id="23a82-106">Iga saadetis võib sisaldada erinevaid tooteid, nagu raamatuklubi kuu parima raamatu saatmisel, või saadetakse sama toodet korduvalt.</span><span class="sxs-lookup"><span data-stu-id="23a82-106">Each shipment can contain a different product, as in the case of a book-of-the-month club, or the same product can be sent repeatedly.</span></span> <span data-ttu-id="23a82-107">Järjepidevusprogrammi seadistamiseks täitke järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="23a82-107">To set up a continuity program, you must complete the following tasks.</span></span>

1.  <span data-ttu-id="23a82-108">Seadistage järjepidevuse parameetrid lehel **Kõnekeskuse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="23a82-108">Set the continuity parameters on the **Call center parameters** page.</span></span>
2.  <span data-ttu-id="23a82-109">Looge järjepidevusprogramm, mis määrab sellised andmed, nagu maksegraafik, saadetiste ajastus ja käsirahaga arveldus.</span><span class="sxs-lookup"><span data-stu-id="23a82-109">Create a continuity program that specifies details such as the payment schedule, the timing of the shipments, and whether billing is up front.</span></span> <span data-ttu-id="23a82-110">Samuti peate lisama järjepidevusprogrammi kaasatud toodete loendi.</span><span class="sxs-lookup"><span data-stu-id="23a82-110">You must also add a list of products that are included in the continuity program.</span></span> <span data-ttu-id="23a82-111">Iga toode saab sündmuse ID-koodi, mis määratakse järjestikuselt, alustades arvuga 1.</span><span class="sxs-lookup"><span data-stu-id="23a82-111">Each product receives an event ID number that is assigned sequentially, beginning with 1.</span></span> <span data-ttu-id="23a82-112">Sündmuse ID-d määravad järjestuse, milles tooteid saadetakse.</span><span class="sxs-lookup"><span data-stu-id="23a82-112">The event IDs determine the order that products are sent in.</span></span>
    -   <span data-ttu-id="23a82-113">Kui kliendid saavad iga saadetisega erineva toote, saadetakse tooted järjest nende sündmuse ID alusel, alustades praegusest sündmusest.</span><span class="sxs-lookup"><span data-stu-id="23a82-113">If customers receive a different product in each shipment, the products are sent in sequential order, based on their event IDs and beginning with the current event.</span></span>
    -   <span data-ttu-id="23a82-114">Kui kliendid saavad iga saadetisega sama toote, sisaldab loend ainult üht toodet ühe sündmuse ID-ga.</span><span class="sxs-lookup"><span data-stu-id="23a82-114">If customers receive the same product in each shipment, the list contains only one product that has one event ID.</span></span> <span data-ttu-id="23a82-115">Sama sündmus ilmneb korduvalt.</span><span class="sxs-lookup"><span data-stu-id="23a82-115">The same event occurs repeatedly.</span></span> <span data-ttu-id="23a82-116">Saate määrata, mitu korda iga sündmust korratakse.</span><span class="sxs-lookup"><span data-stu-id="23a82-116">You can specify how many times each event is repeated.</span></span>

3.  <span data-ttu-id="23a82-117">Looge ematoode, mis tähistab ülesandes 2 loodud järjepidevusprogrammi.</span><span class="sxs-lookup"><span data-stu-id="23a82-117">Create a parent product that represents the continuity program that you created in task 2.</span></span> <span data-ttu-id="23a82-118">Kui lisate selle toote müügitellimusele, avaneb leht **Järjepidevus**.</span><span class="sxs-lookup"><span data-stu-id="23a82-118">If you add this product to a sales order, the **Continuity** page opens.</span></span> <span data-ttu-id="23a82-119">Seejärel saate kasutada seda lehte tegeliku järjepideva tellimuse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="23a82-119">You can then use that page to create the actual continuity order.</span></span> <span data-ttu-id="23a82-120">Ematoode ei määra üksikuid tooteid, mida klient iga saadetisega saab.</span><span class="sxs-lookup"><span data-stu-id="23a82-120">The parent product doesn't specify the individual products that the customer receives in each shipment.</span></span>

<span data-ttu-id="23a82-121">Kui olete järjepidevusprogrammi seadistanud, nagu eespool kirjeldatud, saate kliendile luua järjepideva tellimuse.</span><span class="sxs-lookup"><span data-stu-id="23a82-121">After you've set up a continuity program as described above, you can create a continuity order for a customer.</span></span> <span data-ttu-id="23a82-122">Teil võib olla vaja teha ka järgmisi lisahaldustoiminguid.</span><span class="sxs-lookup"><span data-stu-id="23a82-122">You might also have to perform the following additional maintenance tasks.</span></span>

-   <span data-ttu-id="23a82-123">**Järjepidevuse praeguse sündmuse perioodi värskendus** – seadistage pakett-töö, mis ütleb süsteemile, milline on praegune sündmuse periood.</span><span class="sxs-lookup"><span data-stu-id="23a82-123">**Update the current continuity event period** – Set up a batch job that tells the system what the current event period is.</span></span>
-   <span data-ttu-id="23a82-124">**Järjepidevuse tütartellimuste loomine** – looge järjepidevuse ematellimusest tütartellimused.</span><span class="sxs-lookup"><span data-stu-id="23a82-124">**Create continuity child orders** – Create child orders from the parent continuity order.</span></span>
-   <span data-ttu-id="23a82-125">**Järjepidevuse maksete töötlemine** – töödelge arveldust ja teatisi järjepidevuse müügitellimustega seostatud maksete kohta.</span><span class="sxs-lookup"><span data-stu-id="23a82-125">**Process continuity payments** – Process billing and notifications for payments that are associated with continuity sales orders.</span></span>
-   <span data-ttu-id="23a82-126">**Järjepidevuse ridade pikendamine** (vajaduse korral) – pikendage nii mitu korda, kui järjepidevat sündmust saab korrata.</span><span class="sxs-lookup"><span data-stu-id="23a82-126">**Extend continuity lines** (if required) – Extend the number of times that a continuity event can be repeated.</span></span> <span data-ttu-id="23a82-127">Saadetiste kordamine võib siis ületada kõnekeskuse parameetrite väljal **Järjepidevuse kordumise lävi** seadistatud limiidi.</span><span class="sxs-lookup"><span data-stu-id="23a82-127">The repetition of shipments can then extend beyond the limit that was set in the **Continuity repeat threshold** field in the call center parameters.</span></span>
-   <span data-ttu-id="23a82-128">**Järjepidevuse värskendamine** (vajaduse korral) – sünkroonige muudatusi järjepidevusprogrammi ja järjepidevuse emamüügitellimuste vahel.</span><span class="sxs-lookup"><span data-stu-id="23a82-128">**Perform a continuity update** (if required) – Synchronize changes between the continuity program and the continuity parent sales orders.</span></span>
-   <span data-ttu-id="23a82-129">**Järjepidevuse põhiridade ja tellimuste sulgemine** – sulgege järjepidevad tellimused.</span><span class="sxs-lookup"><span data-stu-id="23a82-129">**Close continuity parent lines and orders** – Close continuity orders.</span></span>





