---
title: "Kõnekeskuse kataloogid"
description: "Selles artiklis kirjeldatakse kõnekeskusepõhiseid funktsioone Microsoft Dynamics 365 for Retaili kataloogidele."
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
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7be87496ceaea2d1d5f97a5cc17e50dcddbaf33d
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="call-center-catalogs"></a><span data-ttu-id="f5e72-103">Kõnekeskuse kataloogid</span><span class="sxs-lookup"><span data-stu-id="f5e72-103">Call center catalogs</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="f5e72-104">Selles artiklis kirjeldatakse kõnekeskusepõhiseid funktsioone Microsoft Dynamics 365 for Retaili kataloogidele.</span><span class="sxs-lookup"><span data-stu-id="f5e72-104">This article describes the call center–specific functionality for catalogs in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="f5e72-105">Kõnekeskuses saate kasutada tootekatalooge, et tuvastada tooteid, mida soovite klientidele pakkuda.</span><span class="sxs-lookup"><span data-stu-id="f5e72-105">In a call center, you can use product catalogs to identify the products that you want to offer to customers.</span></span> <span data-ttu-id="f5e72-106">Kõnekeskused kasutavad tavaliselt prinditud katalooge.</span><span class="sxs-lookup"><span data-stu-id="f5e72-106">Call centers typically use printed catalogs.</span></span> <span data-ttu-id="f5e72-107">Trükitud kataloogi kujundust ja tootmist hallatakse väljaspool Dynamics 365 for Retaili.</span><span class="sxs-lookup"><span data-stu-id="f5e72-107">The design and production of a printed catalog is handled outside Dynamics 365 for Retail.</span></span> <span data-ttu-id="f5e72-108">Kuid saate luua ja talletada kataloogi digitaalse vormi, kasutades samu lehti, mida kasutate võrgus jaemüügikataloogide seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="f5e72-108">However, you can create and store a digital form of a catalog by using the same pages that you use to set up online retail catalogs.</span></span> <span data-ttu-id="f5e72-109">Enne kataloogi loomist tuleb seadistada toote sortimendid ja määrata sortimendid kõnekeskusele.</span><span class="sxs-lookup"><span data-stu-id="f5e72-109">Before you can create a catalog, you must set up product assortments and assign the assortments to a call center.</span></span> <span data-ttu-id="f5e72-110">Seejärel saate lisada tooteid kataloogi, valides need sortimentidest.</span><span class="sxs-lookup"><span data-stu-id="f5e72-110">You then add products to the catalog by selecting products from these assortments.</span></span> <span data-ttu-id="f5e72-111">Pärast toodete lisamist kataloogi ja kataloogi lõpetamist tuleb kataloog andmete õigsuse kontrollimiseks kinnitada.</span><span class="sxs-lookup"><span data-stu-id="f5e72-111">After products have been added to the catalog, and the catalog is complete, you must validate the catalog to verify the data.</span></span> <span data-ttu-id="f5e72-112">Seejärel tuleb kataloog ülevaatamiseks ja heakskiitmiseks esitada.</span><span class="sxs-lookup"><span data-stu-id="f5e72-112">You must then submit the catalog for review and approval.</span></span> <span data-ttu-id="f5e72-113">Kui kataloog on kinnitatud, võib selle avaldada.</span><span class="sxs-lookup"><span data-stu-id="f5e72-113">After the catalog is approved, it can be published.</span></span> <span data-ttu-id="f5e72-114">Kui kõnekeskuse kataloog on loodud, saate kataloogi avaldamise hetkel kataloogi andmetest hetktõmmise teha.</span><span class="sxs-lookup"><span data-stu-id="f5e72-114">When a call center catalog is created, you can take a snapshot of the catalog data at the time that the catalog is published.</span></span> <span data-ttu-id="f5e72-115">See hetktõmmise funktsioon võimaldab juurdepääsu kataloogi konkreetsele versioonile isegi siis, kui kataloogi hiljem muudetakse ja uuendatakse.</span><span class="sxs-lookup"><span data-stu-id="f5e72-115">This snapshot functionality lets you access a particular version of the catalog even if the catalog is later changed and updated.</span></span> <span data-ttu-id="f5e72-116">Kõnekeskuse kataloogid saab seadistada ka nii, et neis sisalduvad järgmised valikulised funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="f5e72-116">Call center catalogs can also be set up to include the following optional features:</span></span>

-   <span data-ttu-id="f5e72-117">**Lähtekoodid** – lähtekoode kasutatakse kliendi vastuse jälgimiseks konkreetsele kataloogi postitusele.</span><span class="sxs-lookup"><span data-stu-id="f5e72-117">**Source codes** – Source codes are used to track the customer response to specific catalog mailings.</span></span>
-   <span data-ttu-id="f5e72-118">**Tasuta tooted** – tooted saab lisada kliendi tellimusele lisatasuta.</span><span class="sxs-lookup"><span data-stu-id="f5e72-118">**Free products** – Products can be included in a customer's order at no additional charge.</span></span> <span data-ttu-id="f5e72-119">Need tooted lisatakse tellimusse automaatselt kataloogi lähtekoodi sisestamisel tellimusse.</span><span class="sxs-lookup"><span data-stu-id="f5e72-119">These products are automatically added to an order when the source code for the catalog is entered into the order.</span></span>
-   <span data-ttu-id="f5e72-120">**Skriptid** – skriptid on tekstid, mida kõnekeskuse töötaja kliendile müügitellimuse loomisel ette loeb.</span><span class="sxs-lookup"><span data-stu-id="f5e72-120">**Scripts** – Scripts are texts that a call center worker reads to a customer when a sales order is being created.</span></span> <span data-ttu-id="f5e72-121">Skriptid võivad sisaldada tervitusi või ostusoovitusi.</span><span class="sxs-lookup"><span data-stu-id="f5e72-121">Scripts can include greetings or purchase suggestions.</span></span>
-   <span data-ttu-id="f5e72-122">**Lehe paigutus** – lehe paigutus jäädvustab toodete asendi lehel trükitud kataloogis.</span><span class="sxs-lookup"><span data-stu-id="f5e72-122">**Page layout** – A page layout captures the page position of products in the printed catalog.</span></span> <span data-ttu-id="f5e72-123">Seda teavet kasutatakse kataloogiala analüüsi aruandes.</span><span class="sxs-lookup"><span data-stu-id="f5e72-123">This information is used for the catalog area analysis report.</span></span>





