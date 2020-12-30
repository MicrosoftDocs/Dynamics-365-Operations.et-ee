---
title: Prognoosi mudeli parandamine (eelversioon)
description: See teema kirjeldab funktsioone, mida saate kasutada prognoosimise mudelite jõudluse parandamiseks.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 23c9062dcc13951792306c955b54cae6f656fec5
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646075"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="639ef-103">Prognoosi mudeli parandamine (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="639ef-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="639ef-104">See teema kirjeldab funktsioone, mida saate kasutada prognoosimise mudelite jõudluse parandamiseks.</span><span class="sxs-lookup"><span data-stu-id="639ef-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="639ef-105">Oma mudelit saate hakata täiustama tööruumis **Kliendimakse prognoosid** rakenduses Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="639ef-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="639ef-106">Parandamise sammud viiakse seejärel lõpule AI Builderis.</span><span class="sxs-lookup"><span data-stu-id="639ef-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="639ef-107">Ajalooliste tulemuste valimine</span><span class="sxs-lookup"><span data-stu-id="639ef-107">Select historical outcomes</span></span>

<span data-ttu-id="639ef-108">Esmalt valite ühe või mitu kolmest arve võimalikust tulemusest: **õigel ajal**, **hilja** ja **väga hilja**.</span><span class="sxs-lookup"><span data-stu-id="639ef-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="639ef-109">Valida tuleb kõik kolm tulemust.</span><span class="sxs-lookup"><span data-stu-id="639ef-109">All three outcomes should be selected.</span></span> <span data-ttu-id="639ef-110">Kui tühjendate mis tahes tulemuse valiku, filtreeritakse arved koolitusprotsessist välja ja prognoosi täpsus väheneb.</span><span class="sxs-lookup"><span data-stu-id="639ef-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="639ef-111">[![Tulemuste kinnitamine](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="639ef-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="639ef-112">Kui teie organisatsioon nõuab ainult kaht tulemust, muutke variantide **hilja** ja **väga hilja** lävendiks null (0) päeva.</span><span class="sxs-lookup"><span data-stu-id="639ef-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="639ef-113">Sel viisil saate ahendada prognoosid tõhusalt binaarsesse olekusse **õigel ajal** või **hilinenud**.</span><span class="sxs-lookup"><span data-stu-id="639ef-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="639ef-114">Vali väljad</span><span class="sxs-lookup"><span data-stu-id="639ef-114">Select fields</span></span>

<span data-ttu-id="639ef-115">Mudelisse kaasamiseks väljade valimisel olge teadlik, et loend sisaldab kõiki saadaolevaid välju üksuses Common Data Service, mis vastendatakse Azure’i andmejärve andmetega.</span><span class="sxs-lookup"><span data-stu-id="639ef-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Common Data Service entity that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="639ef-116">Osasid nendest väljadest **ei** pea valima.</span><span class="sxs-lookup"><span data-stu-id="639ef-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="639ef-117">Väljad, mida ei peaks valima, jäävad ühte kolmest kategooriast.</span><span class="sxs-lookup"><span data-stu-id="639ef-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="639ef-118">Väli on üksuse Common Data Service jaoks nõutav, kuid andmejärves pole selle jaoks toetavaid andmeid.</span><span class="sxs-lookup"><span data-stu-id="639ef-118">The field is required for the Common Data Service entity, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="639ef-119">Väli on ID ja pole masinõppe funktsiooni jaoks vajalik.</span><span class="sxs-lookup"><span data-stu-id="639ef-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="639ef-120">Väli sisaldab teavet, mis ei ole prognoosimise ajal saadaval.</span><span class="sxs-lookup"><span data-stu-id="639ef-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="639ef-121">Järgmistes jaotistes on näidatud väljad, mis on arve ja kliendi üksuste jaoks saadaval, ja loetleb väljad, mida **ei** peaks koolituse ajal valima.</span><span class="sxs-lookup"><span data-stu-id="639ef-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="639ef-122">Iga sellise välja jaoks määratud kategooria viitab eelmise loendi kategooriatele.</span><span class="sxs-lookup"><span data-stu-id="639ef-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-common-data-model-entity"></a><span data-ttu-id="639ef-123">Arve ühise andmemudeli üksus</span><span class="sxs-lookup"><span data-stu-id="639ef-123">Invoice Common Data Model entity</span></span>

<span data-ttu-id="639ef-124">Järgmisel joonisel on näidatud arve üksuse jaoks saadaolevad väljad.</span><span class="sxs-lookup"><span data-stu-id="639ef-124">The following illustration shows the fields that are available for the invoice entity.</span></span>

<span data-ttu-id="639ef-125">[![Arve üksuse jaoks saadaolevad väljad](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="639ef-125">[![Available fields for the invoice entity](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="639ef-126">Järgmisi välju ei peaks koolituse jaoks valima.</span><span class="sxs-lookup"><span data-stu-id="639ef-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="639ef-127">**Arve konto** (kategooria 2)</span><span class="sxs-lookup"><span data-stu-id="639ef-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="639ef-128">**On suletud** (kategooria 3) – seda välja kasutatakse koolituse (suletud) ja prognoosimise (pole suletud) arvete filtreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="639ef-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="639ef-129">**Nimi** (kategooria 1)</span><span class="sxs-lookup"><span data-stu-id="639ef-129">**Name** (category 1)</span></span>
- <span data-ttu-id="639ef-130">**Allika ID** (kategooria 2)</span><span class="sxs-lookup"><span data-stu-id="639ef-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="639ef-131">**Allika kirje** (kategooria 2)</span><span class="sxs-lookup"><span data-stu-id="639ef-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="639ef-132">**Allika tabel** (kategooria 2)</span><span class="sxs-lookup"><span data-stu-id="639ef-132">**Source table** (category 2)</span></span>

### <a name="customer-common-data-model-entity"></a><span data-ttu-id="639ef-133">Kliendi ühise andmemudeli üksus</span><span class="sxs-lookup"><span data-stu-id="639ef-133">Customer Common Data Model entity</span></span>

<span data-ttu-id="639ef-134">Järgmisel joonisel on näidatud kliendi üksuse jaoks saadaolevad väljad.</span><span class="sxs-lookup"><span data-stu-id="639ef-134">The following illustration shows the fields that are available for the customer entity.</span></span>

<span data-ttu-id="639ef-135">[![Kliendi üksuse jaoks saadaolevad väljad](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="639ef-135">[![Available fields for the customer entity](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="639ef-136">Järgmist välja ei peaks koolituse jaoks valima.</span><span class="sxs-lookup"><span data-stu-id="639ef-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="639ef-137">**Rea kordumatu võti** (kategooria 2)</span><span class="sxs-lookup"><span data-stu-id="639ef-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="639ef-138">Filtrid</span><span class="sxs-lookup"><span data-stu-id="639ef-138">Filters</span></span>

<span data-ttu-id="639ef-139">Filtrid ei toeta praegu kliendi makse prognoosimise stsenaariumit.</span><span class="sxs-lookup"><span data-stu-id="639ef-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="639ef-140">Seetõttu valige suvand **Jäta see samm vahele** ja jätkake kokkuvõttelehega.</span><span class="sxs-lookup"><span data-stu-id="639ef-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="639ef-141">[![Filtritega mudelil keskendumine](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="639ef-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="639ef-142">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="639ef-142">Privacy notice</span></span>
<span data-ttu-id="639ef-143">Eelvaated 1) võivad kasutada vähem privaatsus- ja turbemeetmeid kui rakenduse Dynamics 365 Finance and Operations teenus; 2) ei ole hõlmatud selle teenuse teenusetaseme leppes; 3) ei tohi olla kasutusel isiklike andmete ega muude andmete töötlemiseks, mis on seaduste või määrustega kaitstud; 4) on piiratud toega.</span><span class="sxs-lookup"><span data-stu-id="639ef-143">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
