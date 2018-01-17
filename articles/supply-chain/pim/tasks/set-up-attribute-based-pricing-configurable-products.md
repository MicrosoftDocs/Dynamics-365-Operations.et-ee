--- 
title: "Atribuudipõhise hinnakujunduse loomine konfigureeritavatele toodetele"
description: "See protseduur näitab, kuidas seadistada atribuudipõhist hinnakujundust."
author: YuyuScheller
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: b4cddb3427e3e94d9db9a095a8e8c60bdeb9cc95
ms.contentlocale: et-ee
ms.lasthandoff: 01/17/2018

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="9c1f6-103">Atribuudipõhise hinnakujunduse loomine konfigureeritavatele toodetele</span><span class="sxs-lookup"><span data-stu-id="9c1f6-103">Set up attribute-based pricing for configurable products</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9c1f6-104">See protseduur näitab, kuidas seadistada atribuudipõhist hinnakujundust.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-104">This procedure shows how to set up attribute-based pricing.</span></span> <span data-ttu-id="9c1f6-105">Eeltingimusena peab teil olema tootekonfiguratsiooni mudel, millel on vähemalt üks komponent ja atribuut.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="9c1f6-106">Selles näites kasutatakse demoettevõtte USMF tipptasemel kõlari tootemudelit.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="9c1f6-107">Tavaliselt kasutab seda protseduuri tootejuht.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="9c1f6-108">Uue hinnamudeli loomine</span><span class="sxs-lookup"><span data-stu-id="9c1f6-108">Create a new price model</span></span>
1. <span data-ttu-id="9c1f6-109">Klõpsake valikut Tootevariandi mudeli määratlus.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="9c1f6-110">Klõpsake valikut Toote konfiguratsioonimudelid.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="9c1f6-111">Valige loendist tipptasemel kõlari rida, kuid ärge klõpsake nime linki.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-111">In the list, select the High End Speaker line, but don’t click the link for the name.</span></span>
4. <span data-ttu-id="9c1f6-112">Klõpsake tegumiribal valikut Mudel.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="9c1f6-113">Klõpsake valikut Hinnamudelid.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-113">Click Price models.</span></span>
6. <span data-ttu-id="9c1f6-114">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-114">Click New.</span></span>
7. <span data-ttu-id="9c1f6-115">Tippige väärtus väljale Hinnamudeli nimi.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-115">In the Price model name field, type a value.</span></span>
    * <span data-ttu-id="9c1f6-116">Kasutage nime, mille abil on mudelit kerge tuvastada.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="9c1f6-117">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-117">In the Description field, type a value.</span></span>
9. <span data-ttu-id="9c1f6-118">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-118">Click Save.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="9c1f6-119">Hinnaelementide lisamine</span><span class="sxs-lookup"><span data-stu-id="9c1f6-119">Add price elements</span></span>
1. <span data-ttu-id="9c1f6-120">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-120">Click Edit.</span></span>
    * <span data-ttu-id="9c1f6-121">Igal tootemudeli komponendil võib olla baashinna element ja mis tahes arv hinnaavaldise reegleid.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="9c1f6-122">Saate lisada hindu ka erinevates valuutades.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="9c1f6-123">Tippige väärtus väljale Baashinna avaldis.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-123">In the Base price expression field, type a value.</span></span>
    * <span data-ttu-id="9c1f6-124">Tippige näiteks 100.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-124">For example, type 100.</span></span>   <span data-ttu-id="9c1f6-125">Baashinna avaldis võib olla arvväärtus või koosneda aritmeetilisest tehtest, mis sisaldab vähemalt ühte atribuuti.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="9c1f6-126">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-126">Click Add.</span></span>
4. <span data-ttu-id="9c1f6-127">Tippige Rosewood väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-127">In the Name field, type ‘Rosewood’.</span></span>
    * <span data-ttu-id="9c1f6-128">Hinnaavaldise nimi aitab tuvastada, mida hinnaelement tähistab.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="9c1f6-129">Selles näites loome hinnaelemendi Rosewoodi kõlari korpuse viimistluse valikule.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="9c1f6-130">Klõpsake nuppu Muuda tingimust.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-130">Click Edit condition.</span></span>
    * <span data-ttu-id="9c1f6-131">Hinnatingimus aitab tagada hinnaavaldise elemendi lisamise müügihinda ainult juhul, kui on olemas konkreetne atribuutide kombinatsioon.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="9c1f6-132">Sisestage väljale ConstraintBody tekst CabinetFinish=="Rosewood".</span><span class="sxs-lookup"><span data-stu-id="9c1f6-132">In the ConstraintBody field, enter 'CabinetFinish=="Rosewood"'.</span></span>
7. <span data-ttu-id="9c1f6-133">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-133">Click OK.</span></span>
8. <span data-ttu-id="9c1f6-134">Tippige väärtus väljale Avaldis.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-134">In the Expression field, type a value.</span></span>
    * <span data-ttu-id="9c1f6-135">Tippige näiteks 50.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-135">For example, type 50.</span></span>  
9. <span data-ttu-id="9c1f6-136">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-136">Close the page.</span></span>
10. <span data-ttu-id="9c1f6-137">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9c1f6-137">Close the page.</span></span>


