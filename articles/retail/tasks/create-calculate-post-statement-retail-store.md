--- 
title: " Jaekaupluse jaoks väljavõtte loomine, arvutamine ja sisestamine"
description: "See protseduur kirjeldab kaupluse kohta väljavõtte loomise, arvutamise ja sisestamise etappe."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: d29f89b1ee65523e59aafd7d43465b1e4c3b8a36
ms.contentlocale: et-ee
ms.lasthandoff: 01/17/2018

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a><span data-ttu-id="62f09-103"> Jaekaupluse jaoks väljavõtte loomine, arvutamine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="62f09-103">Create, calculate, and post a statement for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="62f09-104">See protseduur kirjeldab kaupluse kohta väljavõtte loomise, arvutamise ja sisestamise etappe.</span><span class="sxs-lookup"><span data-stu-id="62f09-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="62f09-105">Samade ülesannete jaoks saab konfigureerida ka pakett-töid.</span><span class="sxs-lookup"><span data-stu-id="62f09-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="62f09-106">Pakett-tööde konfigureerimise ja käitamise etapid leiate teistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="62f09-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="62f09-107">Selle protseduuri tegemiseks peavad teil olema kassas lõpule viidud ja seejärel Dynamics AX-i tõmmatud kanded.</span><span class="sxs-lookup"><span data-stu-id="62f09-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="62f09-108">See salvestis kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="62f09-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="62f09-109">See protseduur võib viidata Microsoft Dynamics AX-ile.</span><span class="sxs-lookup"><span data-stu-id="62f09-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="62f09-110">Arvestage, et Dynamics AX-i nimi on nüüd Microsoft Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="62f09-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="62f09-111">Avage Kõik tööruumid >...</span><span class="sxs-lookup"><span data-stu-id="62f09-111">Go to All workspaces > ..</span></span> <span data-ttu-id="62f09-112">> Jaekaupluse rahandus.</span><span class="sxs-lookup"><span data-stu-id="62f09-112">> Retail store financials.</span></span>
2. <span data-ttu-id="62f09-113">Klõpsake suvandit Uus väljavõte.</span><span class="sxs-lookup"><span data-stu-id="62f09-113">Click New statement.</span></span>
3. <span data-ttu-id="62f09-114">Klõpsake väljal Kaupluse number otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="62f09-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="62f09-115">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="62f09-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="62f09-116">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="62f09-116">Click OK.</span></span>
    * <span data-ttu-id="62f09-117">Seadistusgrupp sisaldab sätteid, mis määravad, millised kanded kaasatakse väljavõttesse ja kuidas need väljavõtteridadele grupeeritakse.</span><span class="sxs-lookup"><span data-stu-id="62f09-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="62f09-118">Saate seadistusgrupi avada ja neid sätteid muuta, kuid võite kasutada ka vaikesätteid.</span><span class="sxs-lookup"><span data-stu-id="62f09-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="62f09-119">Väli Väljavõtteviis määratleb väljavõtteridade grupeerimise viisi.</span><span class="sxs-lookup"><span data-stu-id="62f09-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="62f09-120">Valige töötaja või register, kui soovite arvutada väljavõtte ainult kindla töötaja või registri kohta.</span><span class="sxs-lookup"><span data-stu-id="62f09-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="62f09-121">Valige suvand väljal Sulgemismeetod.</span><span class="sxs-lookup"><span data-stu-id="62f09-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="62f09-122">Klõpsake suvandit Väljavõtte arvutamine.</span><span class="sxs-lookup"><span data-stu-id="62f09-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="62f09-123">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="62f09-123">Click Yes.</span></span>
    * <span data-ttu-id="62f09-124">Pärast väljavõtte arvutamist peaksid olema loodud read koos kogusummadega iga kasutatud makseviisi ja väljavõtteviisi kohta.</span><span class="sxs-lookup"><span data-stu-id="62f09-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="62f09-125">Sisestage igale reale inventeeritud summa, kui see tuleb sisestada või seda värskendada.</span><span class="sxs-lookup"><span data-stu-id="62f09-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="62f09-126">Inventeeritud summa väli täidetakse summadega kassas tehtud päevakassadest.</span><span class="sxs-lookup"><span data-stu-id="62f09-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="62f09-127">Klõpsake suvandit Väljavõtte sisestamine.</span><span class="sxs-lookup"><span data-stu-id="62f09-127">Click Post statement.</span></span>
10. <span data-ttu-id="62f09-128">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="62f09-128">Click Close.</span></span>
11. <span data-ttu-id="62f09-129">Minge jaotisse Jaemüük ja kaubandus > Kanalid > Jaekaupluse rahandus.</span><span class="sxs-lookup"><span data-stu-id="62f09-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="62f09-130">Klõpsake vahekaarti Sisestatud väljavõtted.</span><span class="sxs-lookup"><span data-stu-id="62f09-130">Click the Posted statements tab.</span></span>


