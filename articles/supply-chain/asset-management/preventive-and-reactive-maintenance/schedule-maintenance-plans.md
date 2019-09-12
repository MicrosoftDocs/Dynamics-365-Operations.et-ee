---
title: Hoolduskavade plaanimine
description: Selles teemas selgitatakse hoolduskavade plaanimist varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6b6e5bde83474fe8971e482af518f7cee23a2220
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875605"
---
# <a name="schedule-maintenance-plans"></a><span data-ttu-id="19d28-103">Hoolduskavade plaanimine</span><span class="sxs-lookup"><span data-stu-id="19d28-103">Schedule maintenance plans</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="19d28-104">Ennetav hoolduskavade plaanimine loob kalendri varade kohta seadistatud hooldusplaanide põhjal kanded varade kohta.</span><span class="sxs-lookup"><span data-stu-id="19d28-104">Preventive maintenance scheduling generates calendar entries on assets, based on the maintenance plans set up on the assets.</span></span> <span data-ttu-id="19d28-105">Saate plaanida kalendri kandeid valitud hoolduskavade, vara tüüpide ja varade põhjal.</span><span class="sxs-lookup"><span data-stu-id="19d28-105">You can schedule calendar entries based on selected maintenance plans, asset types, and assets.</span></span>

1. <span data-ttu-id="19d28-106">Klõpsake suvandil **Varahaldus** > **Perioodiline** > **Ennetav hooldus** > **Hoolduskavade plaanimine**.</span><span class="sxs-lookup"><span data-stu-id="19d28-106">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance plans**.</span></span>

2. <span data-ttu-id="19d28-107">Intervalli saate valida väljadel **Periood** ja **Perioodi sagedus**.</span><span class="sxs-lookup"><span data-stu-id="19d28-107">You can select a time interval in the **Period** and **Period frequency** fields.</span></span>

>[!NOTE]
><span data-ttu-id="19d28-108">Väljad **Periood** ja **Perioodi sagedus** näitavad kui palju aega ette soovite hooldusgraafiku ridu luua tuginedes loodud hoolduskavadele (ajapõhised või loenduripõhised).</span><span class="sxs-lookup"><span data-stu-id="19d28-108">The **Period** and **Period frequencey** fields indicate how far ahead in time you want maintenance schedule lines to be created, based on the maintenance plans you have created (time-based or counter-based).</span></span> <span data-ttu-id="19d28-109">Alloleval joonisel olevad hooldusgraafiku read (= töökäsu ettepanekud) on loodud alates praegusest kuupäevast ja kolm kuud pärast seda.</span><span class="sxs-lookup"><span data-stu-id="19d28-109">In the figure below, maintenance schedule lines (= work order proposals) are created from the current date and three months onwards.</span></span>

3. <span data-ttu-id="19d28-110">Valige tumblernupu **Loo automaatselt, kui real on täpsustatud** väärtuseks "Jah", kui hoolduskava rea põhjal tuleks automaatselt luua töökäsud.</span><span class="sxs-lookup"><span data-stu-id="19d28-110">Select "Yes" on the **Auto create if specified in the line** toggle button if work orders should automatically be created according to the maintenance plan line.</span></span>

>[!NOTE]
><span data-ttu-id="19d28-111">Kui tumblernupp on seatud väärtusele "Jah" *ja* märkeruut **Loo automaatselt** on hoolduskavade ridadel valitud vormil **Hoolduskavad**, luuakse töökäsud hoolduskava ridade põhjal ja samuti luuakse hooldusgraafiku read olekuga "Töökäsu loodud".</span><span class="sxs-lookup"><span data-stu-id="19d28-111">If this toggle button is set to "Yes", *and* the **Auto create** check box is also selected on maintenance plan lines in **Maintenance plans**, work orders are created based on the maintenance plan lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="19d28-112">Kui ainult üks suvand on valitud (selles dialoogis tumblernupp **Loo automaatselt, kui real on täpsustatud** või märkeruut **Loo automaatselt** vormil **Hoolduskavad**), luuakse ainult hooldusgraafiku read olekuga "Loodud".</span><span class="sxs-lookup"><span data-stu-id="19d28-112">If only one option is selected (**Auto create if specified in the line** toggle button in this dialog or **Auto create** check box in **Maintenance plans** form), only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="19d28-113">Sellisel juhul töökäske ei looda.</span><span class="sxs-lookup"><span data-stu-id="19d28-113">In that case, no work orders are created.</span></span>

4. <span data-ttu-id="19d28-114">Kalendri kandeid on võimalik luua hoolduskavade (aja- ja loenduripõhiseid), varade, vara tüüpida, töö asukohtade ja töö asukohatüüpide põhjal.</span><span class="sxs-lookup"><span data-stu-id="19d28-114">It is possible to generate calendar entries based on maintenance plans (time or counter), assets, asset types, functional locations, and functional location types.</span></span> <span data-ttu-id="19d28-115">Klõpsake nuppu **Filter** ja tehke oma valikud, kui seda nõutakse.</span><span class="sxs-lookup"><span data-stu-id="19d28-115">Click the **Filter** button and make your selections, if required.</span></span>

- <span data-ttu-id="19d28-116">Töö asukohtade põhjal hoolduskavade plaanimisest: kui värskendate vara tüüpide, tootjate ja mudelite seadistust hoolduskavadel kiirkaardil **Kõik töö asukohad** > **Hoolduskavad**, pärast seda, kui olete plaaninud hoolduskavad, kustutatakse automaatselt selle töö asukohaga seotud olemasolevad hooldusgraafiku kanded.</span><span class="sxs-lookup"><span data-stu-id="19d28-116">Regarding scheduling of maintenance plans on functional locations: If you update the setup of asset types, manufacturers, and models on maintenance plans in **All functional locations** > **Maintenance plans** FastTab after you have scheduled maintenance plans, existing maintenance schedule entries related to that functional location are automatically deleted.</span></span> <span data-ttu-id="19d28-117">Selleks, et luua uusi kalendri kandeid, mis on vastavuses värskendatud hoolduskava seadistusega töö asukoha jaoks, peate selle töö asukoha jaoks käivitama uue hoolduskava plaanimise.</span><span class="sxs-lookup"><span data-stu-id="19d28-117">In order to create new calendar entries, which correspond with the updated maintenance plan setup on the functional location, you must run a new maintenance plan schedule for that functional location.</span></span> <span data-ttu-id="19d28-118">Vara tüüpida, tootjate ja mudelite seadistuse kohta lugege täpsemalt teemast [Töö asukohtade loomine](../functional-locations/create-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="19d28-118">Read more about the setup of asset types, manufacturers, and models on functional locations in [Create functional locations](../functional-locations/create-functional-locations.md).</span></span>

><span data-ttu-id="19d28-119">*Näide*: soovite luua hoolduskava konkreetse töö asukoha jaoks, mis tähendab, et kui plaanite hoolduskava, kaasatakse kõik mis tahes ajal selle töö asukoha jaoks seadistatud varad.</span><span class="sxs-lookup"><span data-stu-id="19d28-119">*Example:* You want to create a maintenance plan for a specific functional location, meaning all assets set up on that functional location at any given time will be included when you schedule the maintenance plan.</span></span> <span data-ttu-id="19d28-120">Sellisel juhul loote hoolduskava ja valite konkreetse töö asukoha, kuid te EI lisa hoolduskavasse ühtegi objekti.</span><span class="sxs-lookup"><span data-stu-id="19d28-120">In that case, you create a maintenance plan and select the specific functional location, but you do NOT add any objects in the maintenance plan.</span></span> <span data-ttu-id="19d28-121">Tulemuseks on see, et kui te plaanite seda hoolduskava, luuakse hooldusgraafiku read kõigi töö asukohaga seotud varade kohta mis tahes ajal.</span><span class="sxs-lookup"><span data-stu-id="19d28-121">The result is that when you schedule that maintenance plan, maintenance schedule lines will be created for all the assets related to the functional location at that time.</span></span>

- <span data-ttu-id="19d28-122">Kui teete muudatusi vara tüüpide, tootjate ja mudelite kohta vormil **Vara tüübid**, mõjutavad need muudatused ainult uusi varasid, mis kasutavad värskendatud vara tüüpi.</span><span class="sxs-lookup"><span data-stu-id="19d28-122">If you make changes to asset types, manufacturers and models in **Asset types**, those changes only affect new assets that use the updated asset type.</span></span> <span data-ttu-id="19d28-123">Vara tüüpide seadistuse kohta lugege täpsemalt teemast [Vara tüübid](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="19d28-123">Read more about asset type setup in [Asset types](../setup-for-objects/object-types.md).</span></span>  

5. <span data-ttu-id="19d28-124">Klõpsake **OK**, et alustada hooldusgraafiku kannete loomist varade kohta.</span><span class="sxs-lookup"><span data-stu-id="19d28-124">Click **OK** to start the generation of maintenance schedule entries on assets.</span></span> <span data-ttu-id="19d28-125">Loodud kandeid näidatakse loendilehel **Kõik hooldusgraafikud**.</span><span class="sxs-lookup"><span data-stu-id="19d28-125">The generated entries will be shown in the **All maintenance schedule** list page.</span></span>

![Joonis 1](media/09-preventive-maintenance.png)

- <span data-ttu-id="19d28-127">Dialoogis **Plaani hoolduskavad** saate seadistada pakett-tööd kiirkaardil **Käivita taustal**, et kalendri kannete loomine toimuks automaatselt regulaarsete intervallidega.</span><span class="sxs-lookup"><span data-stu-id="19d28-127">In the **Schedule maintenance plans** dialog, you can set up batch jobs on the **Run in the background** FastTab to automatically generate calendar entries at regular intervals.</span></span>  
- <span data-ttu-id="19d28-128">Kui plaanite ennetava hoolduse, ei looda hooldusgraafiku ridu, mille oodatav alguskuupäev ja kellaaeg on varasemad kui süsteemi kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="19d28-128">When you schedule preventive maintenance, maintenance schedule lines with expected start date and time earlier than the system date and time will not be created.</span></span>  

<span data-ttu-id="19d28-129">Alloleval joonisel on kujutatud graafiline illustratsioon ajapõhisest hoolduskava arvutusest.</span><span class="sxs-lookup"><span data-stu-id="19d28-129">The figure below provides a graphic illustration of a time-based maintenance plan calculation.</span></span>  

![Joonis 2](media/10-preventive-maintenance.jpg)

<span data-ttu-id="19d28-131">Loenduripõhistest hoolduskavadest: allolevatel joonistel kuvatakse kahte erinevat loenduri registreerimise tsüklit.</span><span class="sxs-lookup"><span data-stu-id="19d28-131">Regarding counter-based maintenance plans: In the figures below, two different counter registration cycles are shown.</span></span> <span data-ttu-id="19d28-132">Need põhinevad hoolduskaval, mis on seadistatud vara "V0001" jaoks ja eeldatakse, et vara (auto) sõidab iga kuu ligikaudu 2000 km.</span><span class="sxs-lookup"><span data-stu-id="19d28-132">They are based on a maintenance plan set up for asset "V0001", expecting the asset (a car) to run approx. 2,000 km every month.</span></span>

<span data-ttu-id="19d28-133">Esimeses näites ei läbita iga kuu eeldatavat 2000 km.</span><span class="sxs-lookup"><span data-stu-id="19d28-133">In the first example, the expected 2,000 km are not reached every month.</span></span> <span data-ttu-id="19d28-134">Vastavalt loenduripõhisele hoolduskavale on lävi 2000 km, mis tähendab, et kui käivitate hoolduskava plaanimise, peaks hooldusgraafiku rida olema loodud iga kord, kui jõutakse 2000 km läveni.</span><span class="sxs-lookup"><span data-stu-id="19d28-134">According to the counter-based maintenance plan, the threshold is 2,000 km, meaning when you run a maintenance plan scheduling, a maintenance schedule line should be created each time the 2,000-kilometer threshold is reached.</span></span> <span data-ttu-id="19d28-135">Näites 1 on 4 registreerimise rida, kuid 2000 km läveni on jõutud ainult ühel korral.</span><span class="sxs-lookup"><span data-stu-id="19d28-135">In example 1, there are 4 registration lines, but the 2,000-kilometer threshold is only reached once.</span></span> <span data-ttu-id="19d28-136">See tähendab, et kui käivitate selle vara jaoks hoolduskavade plaanimise, näiteks kolmekuulise perioodi jaoks, luuakse ainult üks hooldusgraafiku rida.</span><span class="sxs-lookup"><span data-stu-id="19d28-136">This means that when you run schedule maintenance plans this asset, for example for a 3-month period, only one maintenance schedule line will be created.</span></span>

<span data-ttu-id="19d28-137">Järgmisel joonisel registreeritakse igal kuul 2000 või enam km.</span><span class="sxs-lookup"><span data-stu-id="19d28-137">In the next figure, 2,000 km or more are registered every month.</span></span> <span data-ttu-id="19d28-138">Seetõttu luuakse selle vara kohta kolmekuulise perioodiga hoolduskavade plaanimise käigus kolm hoolduse rida.</span><span class="sxs-lookup"><span data-stu-id="19d28-138">Therefore, three maintenance lines would be created if you schedule maintenance plans for this asset for a 3-month period.</span></span> 

<span data-ttu-id="19d28-139">Siin kirjeldatud näidete põhjal on näha, et kõik vara kohta tehtud loenduri registreeringud näitavad tendentsi, mis kirjeldab vara kulumist.</span><span class="sxs-lookup"><span data-stu-id="19d28-139">The examples described here show that all counter registrations made on an asset show a trend describing wear and tear on the asset.</span></span> <span data-ttu-id="19d28-140">Seda tendentsi kasutatakse arvutuse aluseks hoolduskava plaanimise ajal.</span><span class="sxs-lookup"><span data-stu-id="19d28-140">That trend is used as calculation basis at the time of maintenance plan scheduling.</span></span>

![Joonis 3](media/11-preventive-maintenance.png)

![Joonis 4](media/12-preventive-maintenance.png)
