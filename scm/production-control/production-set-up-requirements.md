---
title: "Tootmise seadistusnõuded"
description: "Selles artiklis on teave seadistusnõuete kohta, mida peate teadma enne tootmise juhtimisega töötamist."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b5df3c6c776a8dafdcfb3be7e2f273e01d70bcae
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---

# <a name="production-setup-requirements"></a><span data-ttu-id="fcf1f-103">Tootmise seadistusnõuded</span><span class="sxs-lookup"><span data-stu-id="fcf1f-103">Production setup requirements</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fcf1f-104">Selles artiklis on teave seadistusnõuete kohta, mida peate teadma enne tootmise juhtimisega töötamist.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-104">This article provides information about setup requirements before you can work with Production control.</span></span> 

<span data-ttu-id="fcf1f-105">Tootmise juhtimine on integreeritud teiste moodulite funktsioonidega.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-105">Production control is integrated with features in other modules.</span></span> <span data-ttu-id="fcf1f-106">See vastastikune ühenduvus võimaldab teil muuta tootmistellimusi ja tagada, et need uueneksid automaatselt kõikides muudes süsteemi seotud protsessides ja arvutustes.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-106">This interconnectivity lets you change production orders and make sure that they are automatically updated in all other related processes and calculations in the system.</span></span> <span data-ttu-id="fcf1f-107">Järgmised seadistusprotsessid on loetletud nende tegemise järjekorras.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-107">The following setup processes are listed in the order that you should complete them in.</span></span>

## <a name="required-baseline-setup-in-other-modules"></a><span data-ttu-id="fcf1f-108">Nõutav alusjoone seadistus muudes moodulites</span><span class="sxs-lookup"><span data-stu-id="fcf1f-108">Required baseline setup in other modules</span></span>
<span data-ttu-id="fcf1f-109">Muudes moodulites olev teave tuleb seadistada enne, kui saate tootmise juhtimisega töötada.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-109">Information in other modules must be set up before you can work with Production control.</span></span> <span data-ttu-id="fcf1f-110">Seadistus hõlmab järgmisi ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-110">This setup includes the following tasks:</span></span>

-   <span data-ttu-id="fcf1f-111">ettevõtte üldteabe seadistamist;</span><span class="sxs-lookup"><span data-stu-id="fcf1f-111">Set up general company information.</span></span>
-   <span data-ttu-id="fcf1f-112">Pearaamatu seadistamist;</span><span class="sxs-lookup"><span data-stu-id="fcf1f-112">Set up the general ledger.</span></span>
-   <span data-ttu-id="fcf1f-113">kaubagruppide määramist;</span><span class="sxs-lookup"><span data-stu-id="fcf1f-113">Define item groups.</span></span>
-   <span data-ttu-id="fcf1f-114">pearaamatukontode seadistamist kaubagruppidele;</span><span class="sxs-lookup"><span data-stu-id="fcf1f-114">Set up ledger accounts for item groups.</span></span>
-   <span data-ttu-id="fcf1f-115">laokauba tabeli seadistamist laohalduses;</span><span class="sxs-lookup"><span data-stu-id="fcf1f-115">Set up the inventory item table in Inventory management.</span></span>
-   <span data-ttu-id="fcf1f-116">materjalikoosluste ja koosluseversioonide loomist laohalduses.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-116">Create bills of materials (BOMs) and BOM versions in Inventory management.</span></span>

## <a name="required-calendar-and-resource-setup"></a><span data-ttu-id="fcf1f-117">Vajalik kalendri ja ressursi seadistus</span><span class="sxs-lookup"><span data-stu-id="fcf1f-117">Required calendar and resource setup</span></span>
<span data-ttu-id="fcf1f-118">Enne tootmise juhtimise kasutamist avage organisatsiooni haldus ning looge ja määratlege kalender ja operatsiooniressursid järgmises järjekorras.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-118">Before you use Production control, open Organization administration, and create and define the calendar and operations resources in the following order:</span></span>

1.  <span data-ttu-id="fcf1f-119">**Tööajamallid** – seadistage tööajamallid, et määrata kellaajad, mis on saadaval tootmise planeerimisel.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-119">**Working time templates** – Set up working time templates to define the times that are available for production scheduling.</span></span>
2.  <span data-ttu-id="fcf1f-120">**Kalendrid** – seadistage tööajakalendrid, et määratleda aastas tootmise plaanimiseks saadaval olevad päevad.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-120">**Calendars** – Set up working time calendars to define the days of the year that are available for production scheduling.</span></span>
3.  <span data-ttu-id="fcf1f-121">**Ressursigrupid** – seadistage ressursigrupid operatsiooniressursside grupeerimiseks, nii et saaksite ajastamise käivitamisel vabast mahust ülevaate.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-121">**Resource groups** – Set up resource groups to group the operations resources, so that you can get an overview of any free capacity when you run scheduling.</span></span> <span data-ttu-id="fcf1f-122">Enne operatsiooniressursside seadistamist pole vaja ressursigruppe seadistada.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-122">You don't have to set up resource groups before you set up operations resources.</span></span> <span data-ttu-id="fcf1f-123">Kuid soovitame tootmise juhtimise seadistamisel ressursside grupeerimisest aru saada.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-123">However, we recommend that you understand how to group resources when you set up Production control.</span></span>
4.  <span data-ttu-id="fcf1f-124">**Ressursid** – seadistage operatsiooniressursid, et määrata mitmesugused ressursid, mida kasutatakse tootmisprotsessi lõpetamiseks ja võimsuse planeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-124">**Resources** – Set up operations resources to define the resources that are used to complete the production process and plan for capacity.</span></span>

## <a name="required-production-parameters-setup"></a><span data-ttu-id="fcf1f-125">Nõutav tootmise parameetrite seadistus</span><span class="sxs-lookup"><span data-stu-id="fcf1f-125">Required production parameters setup</span></span>
<span data-ttu-id="fcf1f-126">**Tootmise juhtimise parameetrid** – seadistage põhilised tootmise parameetrid määratlemiseks, kuidas süsteem tootmistellimusi käsitleb ja töötleb.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-126">**Production control parameters** – Set up basic production parameters to define how the system handles and processes production orders.</span></span> <span data-ttu-id="fcf1f-127">Määratlege, kuidas tootmistellimusi luuakse, hinnatakse, plaanitakse ja tarbitakse.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-127">Define how production orders are created, estimated, scheduled, and consumed.</span></span> <span data-ttu-id="fcf1f-128">Samuti saate valida, millist tagasisidet soovite ja kuidas kuluarvestust tehakse.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-128">You can also select what kind of feedback you want and how cost accounting is done.</span></span>

## <a name="required-journal-name-identification"></a><span data-ttu-id="fcf1f-129">Töölehe nime nõutav identifitseerimine</span><span class="sxs-lookup"><span data-stu-id="fcf1f-129">Required journal name identification</span></span>
<span data-ttu-id="fcf1f-130">**Tootmistöölehtede nimed** – määrake tootmistöölehtede nimed, mida kasutatakse kannete kirjendamiseks ja sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-130">**Production journal names** – Specify the production journal names that are used to record and post transactions.</span></span>

## <a name="setup-if-you-use-operations"></a><span data-ttu-id="fcf1f-131">Seadistus toimingute kasutamisel</span><span class="sxs-lookup"><span data-stu-id="fcf1f-131">Setup if you use operations</span></span>
<span data-ttu-id="fcf1f-132">Toimingud kajastavad konkreetseid tegevusi, mida valmis toote tootmiseks tehakse.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-132">Operations represent the specific activities that are completed to produce the finished product.</span></span> <span data-ttu-id="fcf1f-133">**Märkus.** Peate teadma kauba tootmiseks vajalikke tegevuste tüüpe ning nende tegevuste järjekorda ja prioriteete.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-133">**Note:** You must know the types of activities that are required in order to produce your item, and the order and priorities of those activities.</span></span> <span data-ttu-id="fcf1f-134">Samuti peate teadma, millised ressursid ja kui palju ressursse on asjaga seotud.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-134">You must also know which resources are involved, and how many.</span></span>

1.  <span data-ttu-id="fcf1f-135">**Toimingud** – seadistage toimingud, mis kajastavad valmis kauba tootmiseks täidetavaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-135">**Operations** – Set up operations to represent the tasks that must be completed to produce the finished item.</span></span>
2.  <span data-ttu-id="fcf1f-136">**Seosed** – seadistage toimingute seosed üksikasjalike atribuutide kehtestamiseks.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-136">**Relations** – Set up operation relations to establish detailed properties.</span></span> <span data-ttu-id="fcf1f-137">Toimingute seoste määratlemiseks klõpsake valikut **Seosed** lehel **Toimingud**.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-137">To define operation relations, click **Relations** on the **Operations** page.</span></span>

## <a name="setup-if-you-use-routes"></a><span data-ttu-id="fcf1f-138">Seadistus protsesside kasutamisel</span><span class="sxs-lookup"><span data-stu-id="fcf1f-138">Setup if you use routes</span></span>
<span data-ttu-id="fcf1f-139">Kui töötate protsessidega, tuleb määratleda iga tootmisprotsessi jaoks seadistatud toimingud.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-139">If you're working with routes, operations must be defined for every production route that you set up.</span></span> <span data-ttu-id="fcf1f-140">Protsess kujutab endast teed, mille kaup ühest toimingust teise liikudes läbib, tootmisprotsessi algusest lõpuni.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-140">The route represents the path that the item takes from operation to operation, from the start of the production process to the end.</span></span>

1.  <span data-ttu-id="fcf1f-141">**Kulukategooriad** – seadistage kulukategooriad määratletud protsesside tunnihinna ja seadistusaegade määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-141">**Cost categories** – Set up cost categories to define the cost per hour of specified processes and setup times.</span></span>
2.  <span data-ttu-id="fcf1f-142">**Kulugrupid** – seadistage kulugrupid, et luua ja hallata kulude eri tüüpe.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-142">**Cost groups** – Set up cost groups to create and maintain different types of costing.</span></span>
3.  <span data-ttu-id="fcf1f-143">**Protsessigrupid** – seadistage protsessigrupid protsessigruppidega seotud parameetrite määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-143">**Route groups** – Set up route groups to define parameters that are related to groups of routes.</span></span> <span data-ttu-id="fcf1f-144">Enne tootmisprotsesside loomist peate seadistama protsessigrupid.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-144">You must set up route groups before you can create production routes.</span></span>
4.  <span data-ttu-id="fcf1f-145">**Protsessid** – seadistage tootmisprotsessid ja määrake vaikesätted protsessitoimingute plaanimise, kuluarvutuse ja hinnakujunduse ning edenemisaruandluse juhtimiseks.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-145">**Routes** – Set up production routes, and define default settings to control scheduling, costing, and pricing of route operations, and to control progress reporting.</span></span>
5.  <span data-ttu-id="fcf1f-146">**Protsessid** – seadistage protsessiversioonid tootmises kaubavariatsioonide lubamiseks.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-146">**Routes** – Set up route versions to enable item variations in production.</span></span>

## <a name="optional-advanced-settings"></a><span data-ttu-id="fcf1f-147">Valikulised täpsemad sätted</span><span class="sxs-lookup"><span data-stu-id="fcf1f-147">Optional advanced settings</span></span>
1.  <span data-ttu-id="fcf1f-148">**Tootmisgrupid** – seadistage tootmisgrupid seoste loomiseks tootmistellimuse ja pearaamatukonto vahel.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-148">**Production groups** – Set up production groups to establish relationships between the production order and ledger accounts.</span></span> <span data-ttu-id="fcf1f-149">Pearaamatukontosid kasutatakse tellimuste sisestamiseks või grupeerimiseks aruandluse jaoks.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-149">The ledger accounts are used to post or group orders for reporting.</span></span>
2.  <span data-ttu-id="fcf1f-150">**Tootmiskaustad** – looge tootmiskaustad tootmistellimuste grupeerimiseks, et saaksite töödelda kiireid tootmistellimusi või kustutada ja sisestada tellimuste gruppe.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-150">**Production pools** – Create production pools to group production orders so that you can process urgent production orders, or delete and post groups of orders.</span></span>
3.  <span data-ttu-id="fcf1f-151">**Atribuudid** – määratlege atribuudid eriatribuutide loomiseks, mille saate määrata oma ressurssidele tootmiste järjekorra juhtimiseks.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-151">**Properties** – Define properties to create special attributes that you can assign to your resources to control the order of productions.</span></span> <span data-ttu-id="fcf1f-152">Need atribuudid ühendatakse tööajamalliga.</span><span class="sxs-lookup"><span data-stu-id="fcf1f-152">These attributes are connected to the working time template.</span></span>





