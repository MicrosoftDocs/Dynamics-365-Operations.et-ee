---
title: Atribuudipõhise hinnakujunduse loomine konfigureeritavatele toodetele
description: Selles teemas selgitatakse, kuidas seadistada atribuutidepõhist hinnastamist.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c30c520e7265c2676937f5191844f6789c364e6
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921237"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="2b586-103">Atribuudipõhise hinnakujunduse loomine konfigureeritavatele toodetele</span><span class="sxs-lookup"><span data-stu-id="2b586-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2b586-104">Selles teemas selgitatakse, kuidas seadistada atribuutidepõhist hinnastamist.</span><span class="sxs-lookup"><span data-stu-id="2b586-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="2b586-105">Eeltingimusena peab teil olema tootekonfiguratsiooni mudel, millel on vähemalt üks komponent ja atribuut.</span><span class="sxs-lookup"><span data-stu-id="2b586-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="2b586-106">Selles näites kasutatakse demoettevõtte USMF tipptasemel kõlari tootemudelit.</span><span class="sxs-lookup"><span data-stu-id="2b586-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="2b586-107">Tavaliselt kasutab seda protseduuri tootejuht.</span><span class="sxs-lookup"><span data-stu-id="2b586-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="2b586-108">Uue hinnamudeli loomine</span><span class="sxs-lookup"><span data-stu-id="2b586-108">Create a new price model</span></span>

1. <span data-ttu-id="2b586-109">Avage **Tooteteabe haldus \> Tooted \> Tootekonfiguratsiooni mudelid**.</span><span class="sxs-lookup"><span data-stu-id="2b586-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="2b586-110">Valige loendist rida **Kvaliteetkõlar**, aga ärge valige linki nimele.</span><span class="sxs-lookup"><span data-stu-id="2b586-110">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
1. <span data-ttu-id="2b586-111">Valige toiminguplaanil **Mudel**.</span><span class="sxs-lookup"><span data-stu-id="2b586-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="2b586-112">Valige **Hinnamudelid**.</span><span class="sxs-lookup"><span data-stu-id="2b586-112">Select **Price models**.</span></span>
1. <span data-ttu-id="2b586-113">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2b586-113">Select **New**.</span></span>
1. <span data-ttu-id="2b586-114">Sisestage väärtus väljale **Hinnamudeli nimi**.</span><span class="sxs-lookup"><span data-stu-id="2b586-114">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="2b586-115">Kasutage nime, mille abil on mudelit kerge tuvastada.</span><span class="sxs-lookup"><span data-stu-id="2b586-115">Use a name that makes the model easy to identify.</span></span>  
1. <span data-ttu-id="2b586-116">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="2b586-116">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="2b586-117">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="2b586-117">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="2b586-118">Hinnaelementide lisamine</span><span class="sxs-lookup"><span data-stu-id="2b586-118">Add price elements</span></span>

1. <span data-ttu-id="2b586-119">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="2b586-119">Select **Edit**.</span></span> <span data-ttu-id="2b586-120">Igal tootemudeli komponendil võib olla baashinna element ja mis tahes arv hinnaavaldise reegleid.</span><span class="sxs-lookup"><span data-stu-id="2b586-120">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="2b586-121">Saate lisada hindu ka erinevates valuutades.</span><span class="sxs-lookup"><span data-stu-id="2b586-121">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="2b586-122">Sisestage väärtus väljale **Baashinna väljend**.</span><span class="sxs-lookup"><span data-stu-id="2b586-122">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="2b586-123">Tippige näiteks 100.</span><span class="sxs-lookup"><span data-stu-id="2b586-123">For example, type 100.</span></span> <span data-ttu-id="2b586-124">Baashinna avaldis võib olla arvväärtus või koosneda aritmeetilisest tehtest, mis sisaldab vähemalt ühte atribuuti.</span><span class="sxs-lookup"><span data-stu-id="2b586-124">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="2b586-125">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="2b586-125">Select **Add**.</span></span>
4. <span data-ttu-id="2b586-126">Väljale **Nimi** sisestage `Rosewood`.</span><span class="sxs-lookup"><span data-stu-id="2b586-126">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="2b586-127">Hinnaavaldise nimi aitab tuvastada, mida hinnaelement tähistab.</span><span class="sxs-lookup"><span data-stu-id="2b586-127">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="2b586-128">Selles näites loome hinnaelemendi Rosewoodi kõlari korpuse viimistluse valikule.</span><span class="sxs-lookup"><span data-stu-id="2b586-128">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="2b586-129">Valige **Tingimuse redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="2b586-129">Select **Edit condition**.</span></span> <span data-ttu-id="2b586-130">Hinnatingimus aitab tagada hinnaavaldise elemendi lisamise müügihinda ainult juhul, kui on olemas konkreetne atribuutide kombinatsioon.</span><span class="sxs-lookup"><span data-stu-id="2b586-130">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="2b586-131">Sisestage **ConstraintBody** väljale `CabinetFinish=="Rosewood"`.</span><span class="sxs-lookup"><span data-stu-id="2b586-131">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="2b586-132">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="2b586-132">Select **OK**.</span></span>
8. <span data-ttu-id="2b586-133">Sisestage väärtus väljale **Avaldis**.</span><span class="sxs-lookup"><span data-stu-id="2b586-133">In the **Expression** field, type a value.</span></span> <span data-ttu-id="2b586-134">Sisestage näiteks `50`.</span><span class="sxs-lookup"><span data-stu-id="2b586-134">For example, type `50`.</span></span> 
9. <span data-ttu-id="2b586-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2b586-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]