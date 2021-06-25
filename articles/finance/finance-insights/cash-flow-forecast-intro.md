---
title: Rahavoo prognoos (eelversioon)
description: See teema kirjeldab rahavoo prognoosimise võimekust.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 64935db3b50e7598f2076ecbec72aba020d4f908
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186536"
---
# <a name="cash-flow-forecast-preview"></a><span data-ttu-id="076a6-103">Rahavoo prognoos (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="076a6-103">Cash flow forecast (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="076a6-104">Rahavoog on igale ärile kriitilise tähtsusega.</span><span class="sxs-lookup"><span data-stu-id="076a6-104">Cash flow is critical to any business.</span></span> <span data-ttu-id="076a6-105">Isegi tulusatel ettevõtetel võib tekkida maksejõuetus, kui nad ei säilita vahetute vajaduste täitmiseks rahavoogu.</span><span class="sxs-lookup"><span data-stu-id="076a6-105">Even profitable companies can face insolvency if they don't maintain the cash flow to meet immediate needs.</span></span> <span data-ttu-id="076a6-106">Finantsülevaadete rahavoo prognoosimise võimalus võib aidata ettevõtetel tõhusalt jälgida ja hallata oma sularahasaldot.</span><span class="sxs-lookup"><span data-stu-id="076a6-106">The cash flow forecasting capability in Finance insights can help companies monitor and manage their cash balances effectively.</span></span> <span data-ttu-id="076a6-107">See funktsioon kasutab masinõppimist, et aidata ettevõtetel prognoosida rahavoogusid täpsemalt kui varem.</span><span class="sxs-lookup"><span data-stu-id="076a6-107">This feature uses machine learning to help businesses forecast cash flows more accurately than they have previously.</span></span> <span data-ttu-id="076a6-108">Samuti võib see aidata juhtidel teha otsuseid, mis optimeerivad võimalusi oma praeguse sularahajäägi kontekstis.</span><span class="sxs-lookup"><span data-stu-id="076a6-108">It can also help managers make decisions that optimize opportunities in the context of their current cash position.</span></span> 

<span data-ttu-id="076a6-109">Enamiku ettevõtete puhul on rahavoo haldamine ja rahavoo prognoosimine tüütu, korduv ja käsitsi protsess.</span><span class="sxs-lookup"><span data-stu-id="076a6-109">For most companies, managing cash flow and running cash flow forecasting is a tedious, repetitive, and manual process.</span></span> <span data-ttu-id="076a6-110">Enamik ettevõtteid tuginevad Microsoft Exceli lahendustele, mis võib olla erineva keerukuse astmega.</span><span class="sxs-lookup"><span data-stu-id="076a6-110">Most companies rely on Microsoft Excel solutions that have varying degrees of complexity.</span></span> <span data-ttu-id="076a6-111">Rahavoogude täpse prognoosimise väljakutsed hõlmavad järgmist.</span><span class="sxs-lookup"><span data-stu-id="076a6-111">The challenges of accurately forecasting cash flow include the following:</span></span>

- <span data-ttu-id="076a6-112">Andmed ei ole otsustajate jaoks kättesaadavad, kuna need on mitmes kohas hajutatud, sealhulgas järgnevates kohtades.</span><span class="sxs-lookup"><span data-stu-id="076a6-112">Data isn't available to decision makers because it's scattered in multiple places, including:</span></span> 
  - <span data-ttu-id="076a6-113">Raamatupidamise või ettevõtte ressursside planeerimise süsteem</span><span class="sxs-lookup"><span data-stu-id="076a6-113">The accounting or enterprise resource planning system</span></span>
  - <span data-ttu-id="076a6-114">Finantsplaneerimise tarkvara</span><span class="sxs-lookup"><span data-stu-id="076a6-114">Financial planning software</span></span>
  - <span data-ttu-id="076a6-115">Excel</span><span class="sxs-lookup"><span data-stu-id="076a6-115">Excel</span></span>
  - <span data-ttu-id="076a6-116">Täiendavad tarkvararakendused</span><span class="sxs-lookup"><span data-stu-id="076a6-116">Additional software applications</span></span> 
- <span data-ttu-id="076a6-117">Prognoosimine põhineb sisemistel teadmistel, mis paiknevad iga domeeni või osakonna nn hoidlates.</span><span class="sxs-lookup"><span data-stu-id="076a6-117">Forecasting is based on internal knowledge that resides in "silos" within each domain or department.</span></span>
- <span data-ttu-id="076a6-118">Rahavoo prognoosimise täpsuse mõõtmine pärast finantside realiseerimist on ebakorrapärane ja keeruline.</span><span class="sxs-lookup"><span data-stu-id="076a6-118">Measuring the accuracy of cash flow forecasting after the financials have been realized is uncertain and difficult.</span></span>
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a><span data-ttu-id="076a6-119">Rahavoo prognoosimise võimaluse üksikasjad</span><span class="sxs-lookup"><span data-stu-id="076a6-119">Details of the Cash flow forecasts capability</span></span>
<span data-ttu-id="076a6-120">Rahavoo prognoosimise funktsioon sisaldab järgmisi võimalusi.</span><span class="sxs-lookup"><span data-stu-id="076a6-120">The Cash flow forecasts feature includes the following functionality.</span></span> 

- <span data-ttu-id="076a6-121">Muudab rahavoo andmete integreerimise välistest süsteemidest rakendusse Dynamics 365 Finance lihtsaks.</span><span class="sxs-lookup"><span data-stu-id="076a6-121">Makes it easy to integrate cash flow data from external systems to Dynamics 365 Finance.</span></span> <span data-ttu-id="076a6-122">Rahavoo prognoosid võivad kasutada ka andmete importimise ja eksportimise raamistikku.</span><span class="sxs-lookup"><span data-stu-id="076a6-122">Cash flow forecasts can also use the data import-export framework.</span></span> <span data-ttu-id="076a6-123">Selle raamistiku abil on Exceli ODataga integreerimine lihtne.</span><span class="sxs-lookup"><span data-stu-id="076a6-123">This framework makes it easy to integrate with Excel OData.</span></span> <span data-ttu-id="076a6-124">Samuti saate kombineerida mitmest allikast pärinevaid andmeid, et luua terviklik rahavoo lahendus.</span><span class="sxs-lookup"><span data-stu-id="076a6-124">You can also combine data from multiple sources to create a comprehensive cash flow solution.</span></span> 

- <span data-ttu-id="076a6-125">Tutvustab nutikat sularahajääki.</span><span class="sxs-lookup"><span data-stu-id="076a6-125">Introduces intelligent cash position.</span></span> <span data-ttu-id="076a6-126">Sularahajääl luuakse kliendi maksekäitumise põhjal, et prognoosida aja, millal ettevõte võib oodata sularaha saabumist oma kontodele.</span><span class="sxs-lookup"><span data-stu-id="076a6-126">Cash position is created  based on customer’s payment behavior to predict when a company can expect cash to arrive in their accounts.</span></span> <span data-ttu-id="076a6-127">Samuti analüüsitakse maksvate hankijate ajaloolisi mustreid, et ennustada tulevaste arvete ja tellimuste eest tasumist.</span><span class="sxs-lookup"><span data-stu-id="076a6-127">It also analyzes the historical patterns of paying vendors, to predict when future invoices and orders are likely to be paid.</span></span> 

- <span data-ttu-id="076a6-128">Tutvustab nutikat rahavoo prognoosimist pikaajaliseks prognoosimiseks, kasutades ajaseeriate prognoosimist läbi automaatset integreerimist AI Builderiga.</span><span class="sxs-lookup"><span data-stu-id="076a6-128">Introduces intelligent cash flow forecasting for long-term forecasting, using time series forecasting through automated integration with AI Builder.</span></span>

- <span data-ttu-id="076a6-129">Võimaldab salvestada kindla rahavoo positsiooni või prognoosid, neid redigeerida ning seejärel lihtsalt võrrelda ja mõõta prognoosi jõudlust võrreldes tegelike finantsnäitajatega.</span><span class="sxs-lookup"><span data-stu-id="076a6-129">Provides the ability to save specific cash flow position or forecasts, edit them, and then easily compare and measure the forecast performance to the actual financials.</span></span>

- <span data-ttu-id="076a6-130">Võimaldab põhjuste ja tagajärgede analüüsi hetktõmmise võrdluse kaudu.</span><span class="sxs-lookup"><span data-stu-id="076a6-130">Enables what-if analysis through snapshot comparison.</span></span> <span data-ttu-id="076a6-131">Näiteks saate luua mitu hetktõmmist, mis esindavad teie rahavoogude optimistlikke, pessimistlikke ja kõige realistlikumaid vaateid ning võrrelda ja vaadata seejärel erinevusi.</span><span class="sxs-lookup"><span data-stu-id="076a6-131">For example, you can create multiple snapshots that represent optimistic, pessimistic, and the most realistic views of your cash flow, and then compare and view the differences.</span></span>

- <span data-ttu-id="076a6-132">Pakub võimalust vaadata rahavoo prognoosi mitmes valuutas, erinevates juriidilistes olemites ning filtreerida ja vaadata rahavoogu konkreetsel pangakontol.</span><span class="sxs-lookup"><span data-stu-id="076a6-132">Provides the ability to view the cash flow forecast in multiple currencies, across legal entities, and filter and view cash flow related to a bank account.</span></span> 

- <span data-ttu-id="076a6-133">Võimaldab filtreerida ja vaadata finantsdimensiooniga seotud pangakontosid.</span><span class="sxs-lookup"><span data-stu-id="076a6-133">Lets you filter and view bank accounts that are related to financial dimensions.</span></span>

<span data-ttu-id="076a6-134">Rakenduse Dynamics 365 Finance rahavoo prognoosimise funktsioon võimaldab teie organisatsioonil muuta tüütu, keeruline ja korduv rahavoo prognoosimine lihtsaks automatiseeritud protsessiks.</span><span class="sxs-lookup"><span data-stu-id="076a6-134">The cash flow forecasting functionality in Dynamics 365 Finance will empower your organization to transform tedious, complex, yet repetitive cash flow projection to a simple, automated process.</span></span> <span data-ttu-id="076a6-135">Rahavoo prognoosimise kõige tüütumate aspektide automatiseerimine võimaldab teil keskenduda kriitilise otsuse tegemisele, et saavutada soovitud äritulemusi.</span><span class="sxs-lookup"><span data-stu-id="076a6-135">Automating the most tedious aspects of cash flow forecasting lets you focus on critical decision making to drive desired business outcomes.</span></span>

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a><span data-ttu-id="076a6-136">Rahavoo prognoosimise jaoks dimensioonide seadistamine</span><span class="sxs-lookup"><span data-stu-id="076a6-136">Setting up Dimensions for Cash flow forecasting</span></span>
<span data-ttu-id="076a6-137">Lehe **Rahavoo prognoosimise seadistus** uus vahekaart võimaldab teil juhtida, milliseid finantsdimensioone tööruumis **Rahavoo prognoosimine** kasutada.</span><span class="sxs-lookup"><span data-stu-id="076a6-137">A new tab on the **Cash flow forecasting setup** page lets you control what financial dimensions to use for filtering in the **Cash flow forecasting** workspace.</span></span> <span data-ttu-id="076a6-138">See vahekaart ilmub ainult siis, kui rahavoo prognoosimise funktsioon on lubatud.</span><span class="sxs-lookup"><span data-stu-id="076a6-138">This tab will only appear when the Cash flow forecasts feature is enabled.</span></span> 

<span data-ttu-id="076a6-139">Vahekaardil **Dimensioonid** tehke dimensioonide loendis filtreerimiseks valik ja kasutage nooleklahve, et liigutada need parempoolsesse veergu.</span><span class="sxs-lookup"><span data-stu-id="076a6-139">On the **Dimensions** tab, choose from the list of dimensions to use for filtering, and use the arrow keys to move them to the right-hand column.</span></span> <span data-ttu-id="076a6-140">Rahavoo prognoosimise andmete filtreerimiseks saab valida ainult kaks dimensiooni.</span><span class="sxs-lookup"><span data-stu-id="076a6-140">Only two dimensions can be selected for filtering cash flow forecast data.</span></span> 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
