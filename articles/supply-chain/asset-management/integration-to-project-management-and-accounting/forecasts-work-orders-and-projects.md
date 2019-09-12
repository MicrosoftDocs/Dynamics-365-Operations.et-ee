---
title: Ennustused, töökäsud ja projektid
description: Selles teemas kirjeldatakse ennustuste ja töökäsu integratsiooni projekti halduse ja varahalduse raamatupidamismooduliga.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886812"
---
# <a name="forecasts-work-orders-and-projects"></a><span data-ttu-id="8b4a5-103">Ennustused, töökäsud ja projektid</span><span class="sxs-lookup"><span data-stu-id="8b4a5-103">Forecasts, work orders, and projects</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="8b4a5-104">Varahalduses integreeritakse mooduliga **Projekti haldus ja raamatupidamine**, et optimeerida kulu, võimaldades kasutajatel jälgida hooldustöö tüübi ennustuste ja töökäsu tööde kulusid.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-104">In Asset Management, integration to the **Project management and accounting** module is done to optimize cost control, allowing users to track costs on maintenance job type forecasts and work order jobs.</span></span>

<span data-ttu-id="8b4a5-105">Hooldustöö tüübi ennustuste jälgimiseks peab seadistama kahte seadet:</span><span class="sxs-lookup"><span data-stu-id="8b4a5-105">To track maintenance job type forecasts, two settings must be made:</span></span>

1. <span data-ttu-id="8b4a5-106">valige projekt kohas **Varahaldus** > **Seadistus** > **Varahalduse näitajad** > **Varad** link > **Projekt** FastTab > asuvas väljas **Hoolduse ennustamisprojekt**;</span><span class="sxs-lookup"><span data-stu-id="8b4a5-106">Select a project in **Asset management** > **Setup** > **Asset management parameters** > **Assets** link > **Project** FastTab > **Maintenance forecast project** field.</span></span>

2. <span data-ttu-id="8b4a5-107">hooldustöö tüübi tavarea loomisel luuakse valikus **Hooldustöö tavatüübid** rea tegevuse number automaatselt (**Varahaldus** > **Seadistus** > **Tööd** > **Hooldustöö tavatüübid**).</span><span class="sxs-lookup"><span data-stu-id="8b4a5-107">In **Maintenance job type defaults**, when you create a mainteance job type default line, an activity number is automatically created for the line (**Asset management** > **Setup** > **Jobs** > **Maintenance job type defaults**).</span></span>

<span data-ttu-id="8b4a5-108">Hooldustöö tüübi ennustamisel on kaks eesmärki: saate jälgida hooldustöö tüübi ennustuste kulusid moodulis **Projekti haldus ja raamatupidamine**.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-108">Maintenance job type forecasts serve two purposes: You are able to track costs on maintenance job type forecasts in the **Project management and accounting** module.</span></span> <span data-ttu-id="8b4a5-109">Lisaks edastatakse ennustused automaatselt töökäsu töö projekti, kui valite töökäsu töö hooldustöö tüübi.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-109">Furthermore, forecasts are automatically transferred to a work order job project when you select a maintenance job type on a work order job.</span></span>

<span data-ttu-id="8b4a5-110">Töökäsu tööde kulud jälgimiseks peate esmalt seadistama töökäsu projektid.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-110">To track costs on work order jobs, you must first set up work order projects.</span></span> <span data-ttu-id="8b4a5-111">Tegevuse kirjeldust vt jaotisest [Töökäsu projekti seadistamine](../setup-for-work-orders/work-order-project-setup.md).</span><span class="sxs-lookup"><span data-stu-id="8b4a5-111">Refer to the [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) section for a description of the procedure.</span></span>

## <a name="work-order-job-projects"></a><span data-ttu-id="8b4a5-112">Töökäsu töö projektid</span><span class="sxs-lookup"><span data-stu-id="8b4a5-112">Work order job projects</span></span>

<span data-ttu-id="8b4a5-113">Kui loote töökäsu töö, määratakse töökäsu projekt töökäskude ülemprojekti seadistamisega kohas **Varahaldus** > **Seadistamine** > **Töökäsud** > **Projekti seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-113">When you create a work order job on a work order, the work order project is determined by the setup of the parent project for work orders in **Asset management** > **Setup** > **Work orders** > **Project setup**.</span></span>

<span data-ttu-id="8b4a5-114">Töökäsu töö projekte luuakse järgmise töökäsu teabe kombinatsiooni alusel:</span><span class="sxs-lookup"><span data-stu-id="8b4a5-114">Work order job projects are created by using a combination of the following work order information:</span></span>

- <span data-ttu-id="8b4a5-115">töökäsus valitud tüüp;</span><span class="sxs-lookup"><span data-stu-id="8b4a5-115">The Work order type selected on the work order</span></span> 
- <span data-ttu-id="8b4a5-116">töökäsu varaga seotud töö asukoht;</span><span class="sxs-lookup"><span data-stu-id="8b4a5-116">The functional location related to the asset on the work order job</span></span>
- <span data-ttu-id="8b4a5-117">töökäsu varaga seotud vara tüüp;</span><span class="sxs-lookup"><span data-stu-id="8b4a5-117">The Asset type related to the asset on the work order job</span></span>  
- <span data-ttu-id="8b4a5-118">töökäsu eeldatav algus- ja lõpuaeg.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-118">The Expected start and end time set on the work order</span></span>  

<span data-ttu-id="8b4a5-119">Võimalik, et töökäsus pole kogu allpool nimetatud teavet.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-119">It is possible that not all of the information mentioned above is found on a work order.</span></span> <span data-ttu-id="8b4a5-120">Seega otsitakse töökäsu ülemprojekti saadaval andmete kombinatsiooni alusel ja valides projekti ID, mis vastab töökäsu andmetele.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-120">Therefore, the search for a work order parent project is done by using the available combination of data and selecting the project ID that corresponds with work order data.</span></span>

<span data-ttu-id="8b4a5-121">Näide: alumises joonises tähendab vara tüübi „Sõiduki mootor“ seadistus seda, et iga selle vara tüübiga loodud töökäsu töö on projekti ID „000186“ alamprojekt.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-121">Example: In the figure below, the setup of asset type "Truck Engine" means that every work order job created with that asset type will be a sub project of Project ID "000186".</span></span>

![Joonis 1](media/01-integration-to-pma.png)

<span data-ttu-id="8b4a5-123">Töökäsu töö projekti ID ja asjakohase tegevuse numbri (**Vara haldus** > **Ühine** > **Töökäsud** > **Kõik töökäsud** > valige loendist töökäsk > **Rea andmed** FastTab > väli **Projekti ID** ja väli **Tegevuse number**) eesmärk on jälgida moodul **Projekti haldus ja raamatupidamine** töökäsu tööga seotud kulutusi ja töökäsu töös valitud vara.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-123">The purpose of the project ID on the work order job, and the related activity number (**Asset management** > **Common** > **Work orders** > **All Work orders** > select work order in list > **Line details** FastTab > **Project ID** field and **Activity number** field), is to track costs related to the work order job, and the asset selected on the work order job, in the **Project management and accounting** module.</span></span> 

<span data-ttu-id="8b4a5-124">Alumisel joonisel näete töökäsu projektide ja asjakohaste projektide toimingute graafilist ülevaadet.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-124">In the figure below, you see a graphic overview of work order projects and related project activities.</span></span>

![Joonis 2](media/02-integration-to-pma.png)

<span data-ttu-id="8b4a5-126">Kui töökäsus luuakse uus töö, luuakse selle jaoks automaatselt projekt.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-126">When a new work order job is created on a work order, a work order project is automatically created for the job.</span></span> <span data-ttu-id="8b4a5-127">Töökäsu tööga seotud vara finantsdimensioonid edastatakse automaatselt töökäsu projekti.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-127">The financial dimensions for the asset related to the work order job are automatically transferred to the work order project.</span></span> <span data-ttu-id="8b4a5-128">Töökäsu töö jaoks loodud projekti aktiivsuses on manustatud asjakohane teave hooldustöö tüübi, selle variandi ja müügi kohta.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-128">The project activity created for a work order job has related information attached to it regarding maintenance job type, maintenance job type variant, and trade.</span></span> <span data-ttu-id="8b4a5-129">Nendest andmetest on kasu näiteks töökäsu ostutellimuse loomisel (vt [Hankimine](../work-orders/procurement.md)) või mooduli **Projekti haldus ja raamatupidamine** kasutamisel aja registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-129">Those data are useful if, for example, you create a purchase order from a work order (see [Procurement](../work-orders/procurement.md)), or if you use the **Project management and accounting** module for time registration.</span></span>  

<span data-ttu-id="8b4a5-130">Kui vara paigaldati töö asukohta ja see vara paigaldatakse hiljem teise töö asukohta, värskendatakse automaatselt uue töö asukohaga seotud vara finantsilisi dimensioone</span><span class="sxs-lookup"><span data-stu-id="8b4a5-130">If the asset was installed on a functional location, and that asset is later installed on another functional location, the financial dimensions related to the new functional location is automatically updated on the asset.</span></span> <span data-ttu-id="8b4a5-131">Hiljem, kui loote vara töökäsu töö, saab töökäsu töö projekt automaatselt nüüd varaga seotud finantsilised dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-131">Subsequently, when you create a work order job for the asset, the work order project for the work order job automatically gets the financial dimensions that are now related to the asset.</span></span> <span data-ttu-id="8b4a5-132">See tähendab seda, et kui kasutate töö asukohti, saab alati jälgida töö asukohtade, kuhu vara paigaldati mistahes ajal, kulusid.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-132">This means that when you use functional locations, costs can always be tracked on the functional locations on which an asset was installed at any given time.</span></span> <span data-ttu-id="8b4a5-133">Finantsiliste dimensioonide automaatne värskendamine tagab kulude põhjaliku jälgitavuse projekti haldamise ja aruandluse jaoks.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-133">The automatic update of financial dimensions ensures complete traceability of costs for project controlling and reporting.</span></span>  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a><span data-ttu-id="8b4a5-134">Töökäsu projektid, töökäsu tsükli olekud, projekti etapid ja projekti tüübid</span><span class="sxs-lookup"><span data-stu-id="8b4a5-134">Work order projects, work order lifecycle states, project stages, and project types</span></span>

<span data-ttu-id="8b4a5-135">Töökäsu tsükli olekute ja töökäskude asjakohase projekti etappide õige kasutamise tagamiseks pidage silmas sõltuvusi vastavalt moodulile **Projekti haldus ja raamatupidamine**:</span><span class="sxs-lookup"><span data-stu-id="8b4a5-135">To ensure correct use of work order lifecycle states and related project stages on work orders, consider the dependencies in relation to the **Project management and accounting** module:</span></span>

- <span data-ttu-id="8b4a5-136">Mooduli **Projekti haldus ja raamatupidamine** projekti etapid on seadistatud valiku **Projekti haldus ja raamatupidamise näitajad** projekti tüüpidega.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-136">In the **Project management and accounting** module, project stages are set up on project types in **Project management and accounting parameters**.</span></span>  
- <span data-ttu-id="8b4a5-137">Pidage meeles, et valite moodulis **Projekti haldus ja raamatupidamine** kõikide kasutatavate projekti tüüpide asjakohase projekti etapi märkeruudud.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-137">In **Project management and accounting parameters**, remember to select relevant project stage check boxes for all the project types you are going to use.</span></span> <span data-ttu-id="8b4a5-138">Alumises joonises on valitud projekti tüüpide „Aeg ja materjal“ ja „Sisemine“ viis etappi: **Loodud** - **Hinnatud** - **Ajastatud** - **Pooleli** - **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-138">In the figure below, five stages **Created** - **Estimated** - **Scheduled** - **In process** - **Finished** have been selected for the project types "Time and material" and "Internal".</span></span> <span data-ttu-id="8b4a5-139">Need viis etappi on vajalikud nii sisemise hoolduse kui ka teenuse hoolduse töödele.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-139">Those five stages are relevant for both internal maintenance and service maintenance jobs.</span></span>  
- <span data-ttu-id="8b4a5-140">Valikus **Varahaldus** määratletakse projekti tüüpe projekti rühmade seadistate neid ankeedi **Töökäsu projekti seadistus** > lingi **Projekti rühm** järgi.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-140">In **Asset Management**, project types are defined by the project groups you set up in the **Work order project setup** form > **Project group** link.</span></span>  
- <span data-ttu-id="8b4a5-141">Valiku **Töökäsu projekti seadistus** projekti rühmade seadistust kasutatakse, uute töökäskude loomisel.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-141">The project groups setup in **Work order project setup** are used when you create work orders.</span></span> <span data-ttu-id="8b4a5-142">Kui luuakse töökäsk, koostatakse selle jaoks automaatselt projekt.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-142">When a work order is created, a work order project is automatically created for the work order.</span></span>  
- <span data-ttu-id="8b4a5-143">Töökäsu tsükli kõikidel olekutel peab olema asjakohane projekti etapp.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-143">Work order lifecycle states must each have a related project stage.</span></span>  
- <span data-ttu-id="8b4a5-144">Töötsükli olekuga seotud projekti etapp peab olema rühma aktiivne etapp.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-144">The project stage related to a work order lifecycle state must be defined as an active stage for the project group defined in the work order project.</span></span> <span data-ttu-id="8b4a5-145">Töökäsu projekt koostatakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-145">The work order project is automatically created on a work order.</span></span>  
- <span data-ttu-id="8b4a5-146">Kui loote uute töökäsu, põhineb töökäsu projekti automaatne eraldus valiku **Töökäsu projekti seadistamine** (**Varahaldus** > **Seadistamine** > **Töökäsud** > **Projekti seadistamine**).</span><span class="sxs-lookup"><span data-stu-id="8b4a5-146">When you create a new work order, the automatic allocation of a work order project is based on the setup in **Work order project setup** (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>  

<span data-ttu-id="8b4a5-147">Töökäsu projekti rühmade, asjakohaste projekti tüüpide, projekti etappide ja töökäsu tsükli olekute omavahelised seosed on kujutatud alumistes joonistes.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-147">Associations between work order project groups, related project types, project stages, and work order lifecycle states are shown in the figures below.</span></span>  

![Joonis 3](media/03-integration-to-pma.png)

![Joonis 4](media/04-integration-to-pma.png)

![Joonis 5](media/05-integration-to-pma.png)

<span data-ttu-id="8b4a5-151">Töökäsu projektide seadistamiseks vt [Töökäsu projekti seadistamine](../setup-for-work-orders/work-order-project-setup.md) ja töökäsu tsükli olekuid vt [Töökäsu tsükli olekud](../setup-for-work-orders/work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="8b4a5-151">Refer to [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) regarding how to set up work order projects, and to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) regarding how to create work order lifecycle states.</span></span>

<span data-ttu-id="8b4a5-152">Alumine joonis näitab moodulis **Varahaldus** loodud (et võimaldada integratsiooni mooduliga **Projekti haldus ja raamatupidamine**) erinevate projektid graafilist ülevaadet ja ka projektidega seotud töö toiminguid.</span><span class="sxs-lookup"><span data-stu-id="8b4a5-152">The figure below shows a graphic overview of the various projects that are created in the **Asset management** module to allow integration with the **Project management and accounting** module, as well as the work processes to which the projects are related.</span></span>

![Joonis 6](media/06-integration-to-pma.png)

