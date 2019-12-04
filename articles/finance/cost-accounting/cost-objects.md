---
title: Kuluobjekti dimensioonid
description: Kulude analüüsimisel saate kasutada kuluelemendi dimensioone, et määrata, kuhu kulud voolavad. Saate kasutada kuluobjekti dimensioone, et määrata, kuhu peaksite kulud määrama. Teema sisaldab teavet kuluobjekti dimensioonide kohta.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6c15402993568c53eda8e03351fc2fccbcd82ab8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770823"
---
# <a name="cost-object-dimensions"></a><span data-ttu-id="1489a-105">Kuluobjekti dimensioonid</span><span class="sxs-lookup"><span data-stu-id="1489a-105">Cost object dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1489a-106">Kulude analüüsimisel saate kasutada kuluelemendi dimensioone, et määrata, kuhu kulud voolavad.</span><span class="sxs-lookup"><span data-stu-id="1489a-106">When you analyze costs, you use cost element dimensions to determine where costs flow to.</span></span> <span data-ttu-id="1489a-107">Saate kasutada kuluobjekti dimensioone, et määrata, kuhu peaksite kulud määrama.</span><span class="sxs-lookup"><span data-stu-id="1489a-107">You use cost object dimensions to determine where you should assign costs.</span></span> <span data-ttu-id="1489a-108">Teema sisaldab teavet kuluobjekti dimensioonide kohta.</span><span class="sxs-lookup"><span data-stu-id="1489a-108">This topic provides information about cost object dimensions.</span></span>

<span data-ttu-id="1489a-109">Kuluobjekt saab olla mis tahes tüüpi objekt, mida soovite hinnata, millele soovite kulusid eraldada või otseselt mõõta.</span><span class="sxs-lookup"><span data-stu-id="1489a-109">A cost object can be any type of object that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="1489a-110">Tüüpilised kuluobjektid hõlmavad tooteid, projekte, ressursse, osakondi, kulukeskuseid ja geograafilisi regioone.</span><span class="sxs-lookup"><span data-stu-id="1489a-110">Typical cost objects include products, projects, resources, departments, cost centers, and geographical regions.</span></span> <span data-ttu-id="1489a-111">Haldus kasutab kuluobjekte, et määrata kulude kogus, kuid samuti selleks, et juhtida tulususe analüüsi.</span><span class="sxs-lookup"><span data-stu-id="1489a-111">Management uses cost objects to quantify costs and also to drive profitability analysis.</span></span>

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a><span data-ttu-id="1489a-112">Kuluobjekti dimensioonid ja kuluobjekti dimensiooni liikmed</span><span class="sxs-lookup"><span data-stu-id="1489a-112">Cost object dimensions and cost object dimension members</span></span>
<span data-ttu-id="1489a-113">Kuluobjekte nimetatakse *kuluobjekti dimensioonideks*.</span><span class="sxs-lookup"><span data-stu-id="1489a-113">Cost objects are known as *cost object dimensions*.</span></span> <span data-ttu-id="1489a-114">Pärast seda, kui olete otsustanud, millisele olemile kuluobjekti dimensioon peaks viitama, peate määrama individuaalsed dimensiooniväärtused või importima need teistest lähtesüsteemidest kuluarvestusse.</span><span class="sxs-lookup"><span data-stu-id="1489a-114">After you’ve decided which entity the cost object dimension should refer to, you must specify the individual dimension values or import them into Cost accounting from other source systems.</span></span> <span data-ttu-id="1489a-115">Neid individuaalseid dimensiooniväärtuseid nimetatakse *kuluobjekti dimensiooni liikmeteks*.</span><span class="sxs-lookup"><span data-stu-id="1489a-115">These individual dimension values are known as *cost object dimension members*.</span></span> <span data-ttu-id="1489a-116">Näiteks soovite kasutada finantsdimensiooni, mida kulukeskuses nimetatakse kuluobjekti dimensiooniks.</span><span class="sxs-lookup"><span data-stu-id="1489a-116">For example, you want to use the financial dimension that is named Cost center as the cost object dimension.</span></span> <span data-ttu-id="1489a-117">Nägemaks, kuidas kulud voolavad individuaalsetesse kulukeskustesse, peate importima kuluobjekti dimensiooni liikmed.</span><span class="sxs-lookup"><span data-stu-id="1489a-117">To see how costs flow to the individual cost centers, you must import the cost object dimension members.</span></span> <span data-ttu-id="1489a-118">Sellisel juhul on kuluobjekti dimensiooni liikmed tegelikud kulukeskused, nagu Müük, Tootmine, Administreerimine ja Geograafilised asukohad.</span><span class="sxs-lookup"><span data-stu-id="1489a-118">In this case, the cost object dimension members are the actual cost centers, such as Sales, Production, Administration, and Geographic locations.</span></span> <span data-ttu-id="1489a-119">Järgmine kuvatõmmis näitab näidet kulukeskustest kuluobjekti dimensioonina, kus selle tegelikud kulukeskused on kuluobjekti dimensiooni liikmed.</span><span class="sxs-lookup"><span data-stu-id="1489a-119">The following screenshot shows an example of Cost Centers as the cost object dimension with its actual cost centers as cost object dimension members.</span></span> 

<span data-ttu-id="1489a-120">[![Kuvatõmmis kulukeskusest kui kuluobjekti dimensioonist](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="1489a-120">[![Screenshot showing Cost Centers as cost object dimension](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span></span>

## <a name="import-cost-object-dimension-members-through-data-connectors"></a><span data-ttu-id="1489a-121">Kuluobjekti dimensiooni liikmete importimine andmekonnektorite kaudu</span><span class="sxs-lookup"><span data-stu-id="1489a-121">Import cost object dimension members through data connectors</span></span>
<span data-ttu-id="1489a-122">Kuluobjekti dimensiooni liikmete lihtsamaks importimiseks saate kasutada andmekonnektoreid, et tuua väärtuseid üksustest, mida soovite kasutada kuluobjekti dimensioonidena.</span><span class="sxs-lookup"><span data-stu-id="1489a-122">To make the import of cost object dimension members easier, you use data connectors to retrieve the values from the entities that you want to use as cost object dimensions.</span></span> <span data-ttu-id="1489a-123">Saate kasutada eelnevalt ehitatud andmekonnektoreid või teie ehitatavaid kohandatud andmekonnektoreid.</span><span class="sxs-lookup"><span data-stu-id="1489a-123">You can use either the pre-built data connectors or custom data connectors that you build.</span></span>


