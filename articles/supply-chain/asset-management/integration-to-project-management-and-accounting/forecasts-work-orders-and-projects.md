---
title: Ennustused, töökäsud ja projektid
description: Selles teemas kirjeldatakse ennustuste ja töökäsu integratsiooni projekti halduse ja varahalduse raamatupidamismooduliga.
author: josaw1
manager: tfehr
ms.date: 08/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f062b5463b54e9bcf32ed6f17263811c4bb24138
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021016"
---
# <a name="forecasts-work-orders-and-projects"></a><span data-ttu-id="f272c-103">Prognoosid, töökäsud ja projektid</span><span class="sxs-lookup"><span data-stu-id="f272c-103">Forecasts, work orders, and projects</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f272c-104">Varade halduses aitab integreerimine mooduliga **Projekti haldus ja raamatupidamine** optimeerida kulu, et kasutajad saaksid jälgida hooldustöö tüübi ennustuste ja töökäsu tööde kulusid.</span><span class="sxs-lookup"><span data-stu-id="f272c-104">In Asset Management, integration with the **Project management and accounting** module helps optimize cost control, so that users can track costs on maintenance job type forecasts and work order jobs.</span></span>

<span data-ttu-id="f272c-105">Hooldustöö tüübi ennustuste jälgimiseks peab seadistama kahte seadet:</span><span class="sxs-lookup"><span data-stu-id="f272c-105">Tracking of maintenance job type forecasts requires two settings:</span></span>

1. <span data-ttu-id="f272c-106">Valige projekt **Varade haldus** > **Seadistus** > **Varade halduse parameetrid** ja seejärel vahekaardil **Varad** > **Projekti** vahelehel, väljal **Hooldusprognoosi projekt** valige projekt.</span><span class="sxs-lookup"><span data-stu-id="f272c-106">Select a project in **Asset management** > **Setup** > **Asset management parameters**, and then, on the **Assets** tab > on the **Project** FastTab, in the **Maintenance forecast project** field, select a project.</span></span>

2. <span data-ttu-id="f272c-107">Hooldustöö tüübi tavarea loomisel luuakse automaatselt **Hooldustöö tavatüübid** lehel olevale reale tegevuse number (**Varahaldus** > **Seadistus** > **Tööd** > **Hooldustöö tavatüübid**).</span><span class="sxs-lookup"><span data-stu-id="f272c-107">When you create a maintenance job type default line, an activity number is automatically created for the line on the **Maintenance job type defaults** page (**Asset management** > **Setup** > **Jobs** > **Maintenance job type defaults**).</span></span>

<span data-ttu-id="f272c-108">Hooldustöö tüübi prognoosidel on kaks eesmärki:</span><span class="sxs-lookup"><span data-stu-id="f272c-108">Maintenance job type forecasts serve two purposes:</span></span> 

- <span data-ttu-id="f272c-109">Hooldustöö tüübi prognooside kulusid saate jälgida moodulis **Projektihaldus ja -arvestus**.</span><span class="sxs-lookup"><span data-stu-id="f272c-109">You can track costs on maintenance job type forecasts in the **Project management and accounting** module.</span></span> 
- <span data-ttu-id="f272c-110">Prognoosid edastatakse automaatselt töökäsu töö projekti, kui valite töökäsu töö hooldustöö tüübi.</span><span class="sxs-lookup"><span data-stu-id="f272c-110">Forecasts are automatically transferred to a work order job project when you select a maintenance job type on a work order job.</span></span>

<span data-ttu-id="f272c-111">Töökäsu tööde kulud jälgimiseks peate esmalt seadistama töökäsu projektid.</span><span class="sxs-lookup"><span data-stu-id="f272c-111">To track costs on work order jobs, you must first set up work order projects.</span></span> <span data-ttu-id="f272c-112">Lisateavet leiate jaotisest [Töökäsu projekti seadistamine](../setup-for-work-orders/work-order-project-setup.md).</span><span class="sxs-lookup"><span data-stu-id="f272c-112">For more information, see [Work order project setup](../setup-for-work-orders/work-order-project-setup.md).</span></span>

## <a name="work-order-job-projects"></a><span data-ttu-id="f272c-113">Töökäsu töö projektid</span><span class="sxs-lookup"><span data-stu-id="f272c-113">Work order job projects</span></span>

<span data-ttu-id="f272c-114">Kui loote töökäsu töö, määratakse töökäsu projekt töökäskude ülemprojekti seadistamisega lehel **Töökäsu projekti seadistamine** (**Varade haldus** > **Seadistamine** > **Töökäsud** > **Projekti seadistamine**).</span><span class="sxs-lookup"><span data-stu-id="f272c-114">When you create a work order job on a work order, the work order project is determined by the setup of the parent project for work orders on the **Work order project setup** page (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>

<span data-ttu-id="f272c-115">Töökäsu töö projekte luuakse järgmise töökäsu teabe kombinatsiooni alusel:</span><span class="sxs-lookup"><span data-stu-id="f272c-115">Work order job projects are created by using a combination of the following work order information:</span></span>

- <span data-ttu-id="f272c-116">Töökäsus valitud tüüp</span><span class="sxs-lookup"><span data-stu-id="f272c-116">The work order type selected on the work order</span></span> 
- <span data-ttu-id="f272c-117">töökäsu varaga seotud töö asukoht;</span><span class="sxs-lookup"><span data-stu-id="f272c-117">The functional location related to the asset on the work order job</span></span>
- <span data-ttu-id="f272c-118">Vara tüüp, mis on seotud töökäsu varaga</span><span class="sxs-lookup"><span data-stu-id="f272c-118">The asset type that is related to the asset on the work order job</span></span>  
- <span data-ttu-id="f272c-119">Töökäsule seatud eeldatavad algus- ja lõpuajad</span><span class="sxs-lookup"><span data-stu-id="f272c-119">The expected start and end times that are set on the work order</span></span>  

<span data-ttu-id="f272c-120">Osa sellest teabest ei pruugi töökäsul leida.</span><span class="sxs-lookup"><span data-stu-id="f272c-120">Some of this information might not be found on a work order.</span></span> <span data-ttu-id="f272c-121">Seega otsitakse töökäsu ülemprojekti saadaval andmete kombinatsiooni alusel ja valides projekti ID, mis vastab töökäsu andmetele.</span><span class="sxs-lookup"><span data-stu-id="f272c-121">Therefore, the search for a work order parent project is done by using the available combination of data and selecting the project ID that corresponds to work order data.</span></span>

<span data-ttu-id="f272c-122">Näiteks järgmisel joonisel on varatüübi **Veoki mootor** seadistamise viisi tõttu iga töökäsu töö, mis luuakse varatüübiga **Veoki mootor** projekti ID 000186 alamprojekt.</span><span class="sxs-lookup"><span data-stu-id="f272c-122">For example, in the following illustration, because of the way that the **Truck Engine** asset type is set up, every work order job that is created with the **Truck Engine** asset type will be a sub-project of project ID 000186.</span></span>

![Joonis 1](media/01-integration-to-pma.png)

<span data-ttu-id="f272c-124">Projekti ID eesmärk töökäsu tööl ja sellega seotud tegevuse numbri eesmärk on jälgida töökäsu tööga seotud kulusid ja sellel valitud vara moodulis **Projektihaldus ja -arvestus**.</span><span class="sxs-lookup"><span data-stu-id="f272c-124">The purpose of the project ID on the work order job, and the related activity number, is to track costs that are related to the work order job, and the asset that is selected on it, in the **Project management and accounting** module.</span></span> <span data-ttu-id="f272c-125">(Projekti ID ja tegevuse numbri vaatamiseks **Varade haldus** > **Üldine** > **Töökäsud** > **Kõik töökäsud** ja valige töökäsk.</span><span class="sxs-lookup"><span data-stu-id="f272c-125">(To view the project ID and activity number, select **Asset management** > **Common** > **Work orders** > **All work orders**, and then select the work order.</span></span> <span data-ttu-id="f272c-126">Vahekaardil **Rea üksikasjad** kuvatakse väljal **Projekti ID** projekti ID ja väljal **Tegevuse number** kuvatakse tegevuse number.) Lisateavet varade haldamise kulukontrolli kohta vt [Kulude ja kuupäeva kontroll](../controlling-and-reporting/cost-and-date-control.md).</span><span class="sxs-lookup"><span data-stu-id="f272c-126">On the **Line details** FastTab, the **Project ID** field shows the project ID, and the **Activity number** field shows the activity number.) For more information about cost control in Asset Management, see [Cost and date control](../controlling-and-reporting/cost-and-date-control.md).</span></span>

<span data-ttu-id="f272c-127">Järgmisel joonisel on kujutatud graafiline ülevaade töökäsu projektidest ja sellega seotud projektitegevustest.</span><span class="sxs-lookup"><span data-stu-id="f272c-127">The following illustration shows a graphical overview of work order projects and related project activities.</span></span>

![Joonis 2](media/02-integration-to-pma.png)

<span data-ttu-id="f272c-129">Kui töökäsus luuakse uus töö, luuakse selle jaoks automaatselt projekt.</span><span class="sxs-lookup"><span data-stu-id="f272c-129">When a new work order job is created on a work order, a work order project is automatically created for the job.</span></span> <span data-ttu-id="f272c-130">Töökäsu tööga seotud vara finantsdimensioonid edastatakse automaatselt töökäsu projekti.</span><span class="sxs-lookup"><span data-stu-id="f272c-130">The financial dimensions for the asset that is related to the work order job are automatically transferred to the work order project.</span></span>

<span data-ttu-id="f272c-131">Töökäsu töö jaoks loodud projektitegevusel on sellega seotud teave.</span><span class="sxs-lookup"><span data-stu-id="f272c-131">The project activity that is created for a work order job has related information attached to it.</span></span> <span data-ttu-id="f272c-132">See teave on hooldustöö tüübi, hooldustöö tüübi variandi ja kaubanduse kohta.</span><span class="sxs-lookup"><span data-stu-id="f272c-132">This information is about the maintenance job type, maintenance job type variant, and trade.</span></span> <span data-ttu-id="f272c-133">Sellest on kasu näiteks töökäsu ostutellimuse loomisel (vt [Hankimine](../work-orders/procurement.md)) või mooduli **Projekti haldus ja raamatupidamine** kasutamisel aja registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="f272c-133">It's useful if, for example, you create a purchase order from a work order (see [Procurement](../work-orders/procurement.md)), or if you use the **Project management and accounting** module for time registration.</span></span>

<span data-ttu-id="f272c-134">Kui vara paigaldati funktsionaalsesse asukohta, kuid hiljem paigaldati teisele funktsionaalsele asukohale, värskendatakse selle varaga automaatselt uue funktsionaalse asukohaga seotud finantsilisi dimensioone.</span><span class="sxs-lookup"><span data-stu-id="f272c-134">If the asset was installed on a functional location but is later installed on a different functional location, the financial dimensions that are related to the new functional location are automatically updated on the asset.</span></span> <span data-ttu-id="f272c-135">Seejärel, kui loote vara töökäsu töö, saab töökäsu töö projekt automaatselt nüüd varaga seotud finantsilised dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="f272c-135">Then, when you create a work order job for the asset, the work order project for the work order job automatically gets the financial dimensions that are now related to the asset.</span></span> <span data-ttu-id="f272c-136">Seega kui kasutate töö asukohti, saab alati jälgida töö asukohtade, kuhu vara paigaldati mistahes ajal, kulusid.</span><span class="sxs-lookup"><span data-stu-id="f272c-136">Therefore, when you use functional locations, costs can always be tracked on the functional locations that an asset was installed on at any given time.</span></span> <span data-ttu-id="f272c-137">Finantsiliste dimensioonide automaatne värskendamine aitab tagada projekti kontrolli ja aruandluse kulude täieliku jälgitavuse.</span><span class="sxs-lookup"><span data-stu-id="f272c-137">The automatic update of financial dimensions helps guarantee complete traceability of costs for project control and reporting.</span></span>

## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a><span data-ttu-id="f272c-138">Töökäsu projektid, töökäsu tsükli olekud, projekti etapid ja projekti tüübid</span><span class="sxs-lookup"><span data-stu-id="f272c-138">Work order projects, work order lifecycle states, project stages, and project types</span></span>

<span data-ttu-id="f272c-139">Et tagada töökäsu tsükli olekute ja nendega seotud projekti etappide õiget kasutamist, kaaluge mooduliga **Projektihaldus ja -arvestus** seotud sõltuvusi:</span><span class="sxs-lookup"><span data-stu-id="f272c-139">To help guarantee that work order lifecycle states and related project stages on work orders are used correctly, consider the dependencies in relation to the **Project management and accounting** module:</span></span>

- <span data-ttu-id="f272c-140">Mooduli **Projekti haldus ja -arvestus** projekti etapid on seadistatud projekti tüüpidega lehel **Projektihalduse ja -arvestuse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="f272c-140">In the **Project management and accounting** module, project stages are set up on project types on the **Project management and accounting parameters** page.</span></span>  
- <span data-ttu-id="f272c-141">Valige lehel **Projektihalduse ja -arvestuse parameetrid** märkeruudud, et valida kõigi kasutatavate projektitüüpide jaoks asjakohased projektietapid.</span><span class="sxs-lookup"><span data-stu-id="f272c-141">On the **Project management and accounting parameters** page, use the check boxes to select relevant project stages for all the project types that you will use.</span></span> <span data-ttu-id="f272c-142">Järgmistel joonistel on valitud viis etappi projektitüüpide **Aeg ja materjal** ja **Sisemine** jaoks (**Loodud**, **Hinnatud**, **Ajastatud**, **Pooleli** ja **Valmis**) .</span><span class="sxs-lookup"><span data-stu-id="f272c-142">In the following illustrations, five stages (**Created**, **Estimated**, **Scheduled**, **In process**, and **Finished**) have been selected for the **Time and material** and **Internal** project types.</span></span> <span data-ttu-id="f272c-143">Need viis etappi on vajalikud nii sisemiste hooldustööde kui ka teenuse hoolduse töödele.</span><span class="sxs-lookup"><span data-stu-id="f272c-143">Those five stages are relevant to both internal maintenance jobs and service maintenance jobs.</span></span>
- <span data-ttu-id="f272c-144">Moodulis **Varade haldus** määratletakse projektitüübid projektigruppidega, mille seadistate **Töökäsu projekti seadistuse** lehel > vahekaardil **Projektigrupp** (**Varade haldus** > **Seadistus** > **Töökäsud** > **Projekti seadistus**).</span><span class="sxs-lookup"><span data-stu-id="f272c-144">In the **Asset Management** module, project types are defined by the project groups that you set up on the **Work order project setup** page > **Project group** tab (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>  
- <span data-ttu-id="f272c-145">Valiku **Töökäsu projekti seadistus** lehel olevat projekti rühmade seadistust kasutatakse uute töökäskude loomisel.</span><span class="sxs-lookup"><span data-stu-id="f272c-145">The project groups that are set up on the **Work order project setup** page are used when you create work orders.</span></span> <span data-ttu-id="f272c-146">Kui luuakse töökäsk, koostatakse selle jaoks automaatselt projekt.</span><span class="sxs-lookup"><span data-stu-id="f272c-146">When a work order is created, a work order project is automatically created for the work order.</span></span>  
- <span data-ttu-id="f272c-147">Iga töökäsu tsükli olek peab olema seotud projekti etapiga.</span><span class="sxs-lookup"><span data-stu-id="f272c-147">Every work order lifecycle state must have a related project stage.</span></span>  
- <span data-ttu-id="f272c-148">Projekti etapp, mis on seotud töökäsu elutsükli olekuga, tuleb määratleda töökäsu projektis määratletud projektigrupi aktiivse etapina.</span><span class="sxs-lookup"><span data-stu-id="f272c-148">The project stage that is related to a work order lifecycle state must be defined as an active stage for the project group that is defined in the work order project.</span></span> <span data-ttu-id="f272c-149">Töökäsu projekt koostatakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="f272c-149">The work order project is automatically created on a work order.</span></span>
- <span data-ttu-id="f272c-150">Uue töökäsu loomisel põhineb töökäsu projekti automaatne eraldamine lehel **Töökäsu projekti seadistamine** oleval seadistusel.</span><span class="sxs-lookup"><span data-stu-id="f272c-150">When you create a new work order, the automatic allocation of a work order project is based on the setup on the **Work order project setup** page.</span></span>  

<span data-ttu-id="f272c-151">Järgmised joonised näitavad seoseid töökäsu projekti gruppide, seotud projektitüüpide, projekti etappide ja töökäsu tsükli olekute vahel.</span><span class="sxs-lookup"><span data-stu-id="f272c-151">The following illustrations show the associations between work order project groups, related project types, project stages, and work order lifecycle states.</span></span>

![Joonis 3](media/03-integration-to-pma.png)

![Joonis 4](media/04-integration-to-pma.png)

![Joonis 5](media/05-integration-to-pma.png)

<span data-ttu-id="f272c-155">Lisateavet töökäsu projektide seadistamise kohta vt [Töökäsu projektide seadistus](../setup-for-work-orders/work-order-project-setup.md).</span><span class="sxs-lookup"><span data-stu-id="f272c-155">For information about how to set up work order projects, see [Work order project setup](../setup-for-work-orders/work-order-project-setup.md).</span></span> <span data-ttu-id="f272c-156">Lisateavet töökäsu elutsükli olekute loomise kohta vt [Töökäsu elutsükli olekud](../setup-for-work-orders/work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="f272c-156">For information about how to create work order lifecycle states, see [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md).</span></span>

<span data-ttu-id="f272c-157">Järgmisel joonisel on kujutatud erinevate projektide graafiline ülevaade, mis on loodud moodulis **Varade haldus**, et võimaldada integreerimist mooduliga **Projektihaldus ja -arvestus**.</span><span class="sxs-lookup"><span data-stu-id="f272c-157">The following illustration shows a graphical overview of the various projects that are created in the **Asset management** module to enable integration with the **Project management and accounting** module.</span></span> <span data-ttu-id="f272c-158">See näitab ka tööprotsesse, millega projektid on seotud.</span><span class="sxs-lookup"><span data-stu-id="f272c-158">It also shows the work processes that the projects are related to.</span></span>

![Joonis 6](media/06-integration-to-pma.png)

