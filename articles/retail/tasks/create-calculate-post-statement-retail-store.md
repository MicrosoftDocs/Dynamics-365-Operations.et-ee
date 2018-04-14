--- 
title: " Jaekaupluse jaoks väljavõtte loomine, arvutamine ja sisestamine"
description: "See protseduur kirjeldab kaupluse kohta väljavõtte loomise, arvutamise ja sisestamise etappe."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d9f9888d04f4e2419de9d4a6857a81ae40f6f21a
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a><span data-ttu-id="7ae90-103"> Jaekaupluse jaoks väljavõtte loomine, arvutamine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="7ae90-103">Create, calculate, and post a statement for a retail store</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="7ae90-104">See protseduur kirjeldab kaupluse kohta väljavõtte loomise, arvutamise ja sisestamise etappe.</span><span class="sxs-lookup"><span data-stu-id="7ae90-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="7ae90-105">Samade ülesannete jaoks saab konfigureerida ka pakett-töid.</span><span class="sxs-lookup"><span data-stu-id="7ae90-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="7ae90-106">Pakett-tööde konfigureerimise ja käitamise etapid leiate teistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="7ae90-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="7ae90-107">Selle protseduuri tegemiseks peavad teil olema kassas lõpule viidud ja seejärel Dynamics AX-i tõmmatud kanded.</span><span class="sxs-lookup"><span data-stu-id="7ae90-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="7ae90-108">See salvestis kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="7ae90-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="7ae90-109">See protseduur võib viidata Microsoft Dynamics AX-ile.</span><span class="sxs-lookup"><span data-stu-id="7ae90-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="7ae90-110">Arvestage, et Dynamics AX-i nimi on nüüd Microsoft Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="7ae90-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="7ae90-111">Avage Kõik tööruumid >...</span><span class="sxs-lookup"><span data-stu-id="7ae90-111">Go to All workspaces > ..</span></span> <span data-ttu-id="7ae90-112">> Jaekaupluse rahandus.</span><span class="sxs-lookup"><span data-stu-id="7ae90-112">> Retail store financials.</span></span>
2. <span data-ttu-id="7ae90-113">Klõpsake suvandit Uus väljavõte.</span><span class="sxs-lookup"><span data-stu-id="7ae90-113">Click New statement.</span></span>
3. <span data-ttu-id="7ae90-114">Klõpsake väljal Kaupluse number otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="7ae90-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="7ae90-115">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="7ae90-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="7ae90-116">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7ae90-116">Click OK.</span></span>
    * <span data-ttu-id="7ae90-117">Seadistusgrupp sisaldab sätteid, mis määravad, millised kanded kaasatakse väljavõttesse ja kuidas need väljavõtteridadele grupeeritakse.</span><span class="sxs-lookup"><span data-stu-id="7ae90-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="7ae90-118">Saate seadistusgrupi avada ja neid sätteid muuta, kuid võite kasutada ka vaikesätteid.</span><span class="sxs-lookup"><span data-stu-id="7ae90-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="7ae90-119">Väli Väljavõtteviis määratleb väljavõtteridade grupeerimise viisi.</span><span class="sxs-lookup"><span data-stu-id="7ae90-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="7ae90-120">Valige töötaja või register, kui soovite arvutada väljavõtte ainult kindla töötaja või registri kohta.</span><span class="sxs-lookup"><span data-stu-id="7ae90-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="7ae90-121">Valige suvand väljal Sulgemismeetod.</span><span class="sxs-lookup"><span data-stu-id="7ae90-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="7ae90-122">Klõpsake suvandit Väljavõtte arvutamine.</span><span class="sxs-lookup"><span data-stu-id="7ae90-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="7ae90-123">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="7ae90-123">Click Yes.</span></span>
    * <span data-ttu-id="7ae90-124">Pärast väljavõtte arvutamist peaksid olema loodud read koos kogusummadega iga kasutatud makseviisi ja väljavõtteviisi kohta.</span><span class="sxs-lookup"><span data-stu-id="7ae90-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="7ae90-125">Sisestage igale reale inventeeritud summa, kui see tuleb sisestada või seda värskendada.</span><span class="sxs-lookup"><span data-stu-id="7ae90-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="7ae90-126">Inventeeritud summa väli täidetakse summadega kassas tehtud päevakassadest.</span><span class="sxs-lookup"><span data-stu-id="7ae90-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="7ae90-127">Klõpsake suvandit Väljavõtte sisestamine.</span><span class="sxs-lookup"><span data-stu-id="7ae90-127">Click Post statement.</span></span>
10. <span data-ttu-id="7ae90-128">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="7ae90-128">Click Close.</span></span>
11. <span data-ttu-id="7ae90-129">Minge jaotisse Jaemüük ja kaubandus > Kanalid > Jaekaupluse rahandus.</span><span class="sxs-lookup"><span data-stu-id="7ae90-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="7ae90-130">Klõpsake vahekaarti Sisestatud väljavõtted.</span><span class="sxs-lookup"><span data-stu-id="7ae90-130">Click the Posted statements tab.</span></span>


