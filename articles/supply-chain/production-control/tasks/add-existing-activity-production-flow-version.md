--- 
title: Tootmisvoo versioonile olemasoleva tegevuse lisamine
description: "Tootmisvoogude uute versioonide loomisel võite otsustada lisada vanematele versioonidele loodud tegevused uude versiooni."
author: cvocph
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: cb185c1ec55346af7cfe0b950f0915072242e961
ms.contentlocale: et-ee
ms.lasthandoff: 09/11/2018

---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a><span data-ttu-id="9b436-103">Tootmisvoo versioonile olemasoleva tegevuse lisamine</span><span class="sxs-lookup"><span data-stu-id="9b436-103">Add an existing activity to a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9b436-104">Tootmisvoogude uute versioonide loomisel võite otsustada lisada vanematele versioonidele loodud tegevused uude versiooni.</span><span class="sxs-lookup"><span data-stu-id="9b436-104">When creating new versions of production flows, you can choose to add activities created for the older versions, to the new version.</span></span> <span data-ttu-id="9b436-105">See protseduur näitab, kuidas olemasolevale tootmisvoole luuakse uus versioon ilma tegevusi kopeerimata.</span><span class="sxs-lookup"><span data-stu-id="9b436-105">This procedure shows how a new version is created for an existing production flow, without copying the activities.</span></span> <span data-ttu-id="9b436-106">Järgmises etapis lisatakse uuele versioonile olemasolev tegevus.</span><span class="sxs-lookup"><span data-stu-id="9b436-106">In the next step, an existing activity is added to the new version.</span></span> 

<span data-ttu-id="9b436-107">See toiming nõuab tootmisvoogu, millele on juba loodud versioon ja tegevused.</span><span class="sxs-lookup"><span data-stu-id="9b436-107">This task requires production flow with version and activities already created.</span></span>


## <a name="create-a-new-production-flow-version"></a><span data-ttu-id="9b436-108">Loo uus tootmisvoo versioon</span><span class="sxs-lookup"><span data-stu-id="9b436-108">Create a new production flow version</span></span>
1. <span data-ttu-id="9b436-109">Minge jaotisse Tootmise juhtimine > Seadistus > Kulusäästlik tootmisvoog > Tootmisvood.</span><span class="sxs-lookup"><span data-stu-id="9b436-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="9b436-110">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="9b436-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9b436-111">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="9b436-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9b436-112">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="9b436-112">Click Edit.</span></span>
5. <span data-ttu-id="9b436-113">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="9b436-113">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="9b436-114">Sisestage kuupäev ja kellaaeg väljale Aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="9b436-114">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="9b436-115">Pange tähele, et enne uue tootmisvoo versiooni loomist tuleb kindlasti kontrollida aktiivse versiooni aegumiskuupäeva ja aega.</span><span class="sxs-lookup"><span data-stu-id="9b436-115">Note that before you create a new production flow version, make sure to check the expiration date and time of the active version.</span></span> <span data-ttu-id="9b436-116">Uus versioon luuakse kehtiva alguskuupäevaga, mis loob ühenduse valitud versiooni aegumiskuupäevaga.</span><span class="sxs-lookup"><span data-stu-id="9b436-116">The new version will be created with an effective start date, which connects to the expiry date of the selected version.</span></span>  
7. <span data-ttu-id="9b436-117">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="9b436-117">Click Add.</span></span>
8. <span data-ttu-id="9b436-118">Tehke väljal Kopeeri versioonist valik Ei.</span><span class="sxs-lookup"><span data-stu-id="9b436-118">Select No in the Copy from version field.</span></span>
    * <span data-ttu-id="9b436-119">Valige Ei, et alustada tühja versiooniga, kui enamik kopeeritud versiooni tegevustest asendatakse uute tegevustega.</span><span class="sxs-lookup"><span data-stu-id="9b436-119">Select No to start with an empty version if most of the activities of the copied version will be replaced by new activities.</span></span> <span data-ttu-id="9b436-120">Lisage muutmata tegevused käsitsi vormile Lisa olemasolev funktsioon tegevusele.</span><span class="sxs-lookup"><span data-stu-id="9b436-120">Add the unchanged activities to the Add existing function in the activity form manually.</span></span>  
9. <span data-ttu-id="9b436-121">Tehke väljal Kanban-reeglite dubleerimine valik Ei.</span><span class="sxs-lookup"><span data-stu-id="9b436-121">Select No in the Duplicate kanban rules field.</span></span>
    * <span data-ttu-id="9b436-122">Kui tegevusi ei kopeerita uude versiooni, pole uue versiooni loomise ajal võimalik kanban-reegleid kopeerida.</span><span class="sxs-lookup"><span data-stu-id="9b436-122">When the activities are not copied to the new version, it is not possible to copy the kanban rules at the time of creation of the new version.</span></span>   <span data-ttu-id="9b436-123">Selle asemel kasutatakse hiljem kanban-reegli vormil asendamise kanbani loomise funktsiooni, et asendada vana tootmisvoo versiooni kanban-reeglid kanban-reeglitega, mis kasutavad uue versiooni tegevusi.</span><span class="sxs-lookup"><span data-stu-id="9b436-123">Instead you will use the create replacement kanban function later in the kanban rule form, to replace kanban rules of the old production flow version with kanban rules using the activities of the new version.</span></span>  
10. <span data-ttu-id="9b436-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9b436-124">Click OK.</span></span>
11. <span data-ttu-id="9b436-125">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="9b436-125">In the list, find and select the desired record.</span></span>

## <a name="add-an-existing-activity"></a><span data-ttu-id="9b436-126">Olemasoleva tegevuse lisamine</span><span class="sxs-lookup"><span data-stu-id="9b436-126">Add an existing activity</span></span>
1. <span data-ttu-id="9b436-127">Klõpsake suvandit Tegevused.</span><span class="sxs-lookup"><span data-stu-id="9b436-127">Click Activities.</span></span>
2. <span data-ttu-id="9b436-128">Klõpsake valikut Lisa olemasolev rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="9b436-128">Click Add existing to open the drop dialog.</span></span>
    * <span data-ttu-id="9b436-129">Otsige üles ja valige olemasolev tegevus, mis tuleb lisada uuele tootmisvoo versioonile.</span><span class="sxs-lookup"><span data-stu-id="9b436-129">Find and select an existing activity to be added to the new production flow version.</span></span>  <span data-ttu-id="9b436-130">Pange tähele, et loendis kuvatakse kõik sellele tootmisvoole kõigi varasemate versioonide jaoks loodud tegevused.</span><span class="sxs-lookup"><span data-stu-id="9b436-130">Note that the list shows all activities that have been created for this production flow for all previous versions of the flow.</span></span>  
3. <span data-ttu-id="9b436-131">Valige või sisestage väärtus väljal Tegevus.</span><span class="sxs-lookup"><span data-stu-id="9b436-131">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="9b436-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9b436-132">Click OK.</span></span>


