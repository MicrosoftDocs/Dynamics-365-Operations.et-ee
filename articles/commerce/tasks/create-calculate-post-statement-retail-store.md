---
title: Jaekaupluse jaoks väljavõtete loomine, arvutamine ja sisestamine
description: See protseduur kirjeldab kaupluse kohta väljavõtte loomise, arvutamise ja sisestamise etappe.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ef31bc02fe1761a587ff6bcbecf4a0f34daea9b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964866"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="7edf3-103">Jaekaupluse jaoks väljavõtete loomine, arvutamine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="7edf3-103">Create, calculate, and post statements for a retail store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7edf3-104">See protseduur kirjeldab kaupluse kohta väljavõtte loomise, arvutamise ja sisestamise etappe.</span><span class="sxs-lookup"><span data-stu-id="7edf3-104">This topic describes the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="7edf3-105">Samade ülesannete jaoks saab konfigureerida ka pakett-töid.</span><span class="sxs-lookup"><span data-stu-id="7edf3-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="7edf3-106">Pakett-tööde konfigureerimise ja käitamise etapid leiate teistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="7edf3-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="7edf3-107">Selle protseduuri tegemiseks peavad teil olema kassas lõpule viidud ja seejärel Dynamics Dynamics 365 Commerce-i tõmmatud kanded.</span><span class="sxs-lookup"><span data-stu-id="7edf3-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics 365 Commerce.</span></span> <span data-ttu-id="7edf3-108">See salvestis kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="7edf3-108">This recording uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="7edf3-109">Valige avalehel **Kaupluse rahandus**.</span><span class="sxs-lookup"><span data-stu-id="7edf3-109">Select **Store financials** from the home page.</span></span>
2. <span data-ttu-id="7edf3-110">**Väljavõtte** valimine</span><span class="sxs-lookup"><span data-stu-id="7edf3-110">Select **New statement**.</span></span>
3. <span data-ttu-id="7edf3-111">Valige rippmenüüst suvand **Kaupluse number**.</span><span class="sxs-lookup"><span data-stu-id="7edf3-111">In the **Store number** field, select a option from the drop-down.</span></span>
4. <span data-ttu-id="7edf3-112">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="7edf3-112">Select **OK**.</span></span>
5. <span data-ttu-id="7edf3-113">Rühm **Häälestus** sisaldab sätteid, mis määravad, millised kanded kaasatakse väljavõttesse ja kuidas need väljavõtteridadele grupeeritakse.</span><span class="sxs-lookup"><span data-stu-id="7edf3-113">The **Setup** group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="7edf3-114">Saate rühma **Häälestus** avada ja neid sätteid muuta, kuid võite kasutada ka vaikesätteid.</span><span class="sxs-lookup"><span data-stu-id="7edf3-114">You can open the **Setup** group and change these settings, or you can use the defaults.</span></span>  
    - <span data-ttu-id="7edf3-115">Väli **Väljavõtteviis** määratleb väljavõtteridade grupeerimise viisi.</span><span class="sxs-lookup"><span data-stu-id="7edf3-115">The **Statement method** field defines how the statement lines will be grouped.</span></span>  
    - <span data-ttu-id="7edf3-116">Valige väli **töötaja või register**, kui soovite arvutada väljavõtte ainult kindla töötaja või registri kohta.</span><span class="sxs-lookup"><span data-stu-id="7edf3-116">Select a staff member or a register in the **staff/register** field if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="7edf3-117">Valige suvand väljal **Sulgemismeetod**.</span><span class="sxs-lookup"><span data-stu-id="7edf3-117">In the **Closing method** field, select an option.</span></span>
7. <span data-ttu-id="7edf3-118">Valige toimingupaanilt **Lause arvutamine**.</span><span class="sxs-lookup"><span data-stu-id="7edf3-118">Select **Calculate statement** from the Action Pane.</span></span>
8. <span data-ttu-id="7edf3-119">Valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="7edf3-119">Select **Yes**.</span></span>
    - <span data-ttu-id="7edf3-120">Pärast väljavõtte arvutamist peaksid olema loodud read koos kogusummadega iga kasutatud makseviisi ja väljavõtteviisi kohta.</span><span class="sxs-lookup"><span data-stu-id="7edf3-120">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    - <span data-ttu-id="7edf3-121">Sisestage igale reale inventeeritud summa, kui see tuleb sisestada või seda värskendada.</span><span class="sxs-lookup"><span data-stu-id="7edf3-121">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="7edf3-122">Inventeeritud summa väli täidetakse summadega kassas tehtud päevakassadest.</span><span class="sxs-lookup"><span data-stu-id="7edf3-122">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="7edf3-123">Valige toimingupaanilt **Sisesta väljavõte**.</span><span class="sxs-lookup"><span data-stu-id="7edf3-123">Select **Post statement** from the Action Pane.</span></span>
10. <span data-ttu-id="7edf3-124">Valige suvand **Sule**.</span><span class="sxs-lookup"><span data-stu-id="7edf3-124">Select **Close**.</span></span>
11. <span data-ttu-id="7edf3-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="7edf3-125">Close the pane.</span></span>
12. <span data-ttu-id="7edf3-126">Valige avalehel **Kaupluse rahandus**.</span><span class="sxs-lookup"><span data-stu-id="7edf3-126">At the home page, select **Store financials**.</span></span>
13. <span data-ttu-id="7edf3-127">Klõpsake vahekaarti **Sisestatud väljavõtted**.</span><span class="sxs-lookup"><span data-stu-id="7edf3-127">Select the **Posted statements** tab.</span></span>

