---
title: Prognoosi mudeli parandamine (eelversioon)
description: See teema kirjeldab funktsioone, mida saate kasutada prognoosimise mudelite jõudluse parandamiseks.
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
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 184a1cb5d3851e26b41340b711c51ef38e06eb53
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186638"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="03d12-103">Prognoosi mudeli parandamine (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="03d12-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="03d12-104">See teema kirjeldab funktsioone, mida saate kasutada prognoosimise mudelite jõudluse parandamiseks.</span><span class="sxs-lookup"><span data-stu-id="03d12-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="03d12-105">Oma mudelit saate hakata täiustama tööruumis **Kliendimakse prognoosid** rakenduses Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="03d12-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="03d12-106">Parandamise sammud viiakse seejärel lõpule AI Builderis.</span><span class="sxs-lookup"><span data-stu-id="03d12-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="03d12-107">Ajalooliste tulemuste valimine</span><span class="sxs-lookup"><span data-stu-id="03d12-107">Select historical outcomes</span></span>

<span data-ttu-id="03d12-108">Esmalt valite ühe või mitu kolmest arve võimalikust tulemusest: **õigel ajal**, **hilja** ja **väga hilja**.</span><span class="sxs-lookup"><span data-stu-id="03d12-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="03d12-109">Valida tuleb kõik kolm tulemust.</span><span class="sxs-lookup"><span data-stu-id="03d12-109">All three outcomes should be selected.</span></span> <span data-ttu-id="03d12-110">Kui tühjendate mis tahes tulemuse valiku, filtreeritakse arved koolitusprotsessist välja ja prognoosi täpsus väheneb.</span><span class="sxs-lookup"><span data-stu-id="03d12-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="03d12-111">[![Tulemuste kinnitamine](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="03d12-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="03d12-112">Kui teie organisatsioon nõuab ainult kaht tulemust, muutke variantide **hilja** ja **väga hilja** lävendiks null (0) päeva.</span><span class="sxs-lookup"><span data-stu-id="03d12-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="03d12-113">Sel viisil saate ahendada prognoosid tõhusalt binaarsesse olekusse **õigel ajal** või **hilinenud**.</span><span class="sxs-lookup"><span data-stu-id="03d12-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="03d12-114">Vali väljad</span><span class="sxs-lookup"><span data-stu-id="03d12-114">Select fields</span></span>

<span data-ttu-id="03d12-115">Mudelisse kaasamiseks väljade valimisel olge teadlik, et loend sisaldab kõiki saadaolevaid välju tabelis Microsoft Dataverse, mis vastendatakse Azure’i andmejärve andmetega.</span><span class="sxs-lookup"><span data-stu-id="03d12-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Microsoft Dataverse table that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="03d12-116">Osasid nendest väljadest **ei** pea valima.</span><span class="sxs-lookup"><span data-stu-id="03d12-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="03d12-117">Väljad, mida ei peaks valima, jäävad ühte kolmest kategooriast.</span><span class="sxs-lookup"><span data-stu-id="03d12-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="03d12-118">Väli on tabeli Dataverse jaoks nõutav, kuid andmejärves pole selle jaoks toetavaid andmeid.</span><span class="sxs-lookup"><span data-stu-id="03d12-118">The field is required for the Dataverse table, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="03d12-119">Väli on ID ja pole masinõppe funktsiooni jaoks vajalik.</span><span class="sxs-lookup"><span data-stu-id="03d12-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="03d12-120">Väli sisaldab teavet, mis ei ole prognoosimise ajal saadaval.</span><span class="sxs-lookup"><span data-stu-id="03d12-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="03d12-121">Järgmistes jaotistes on näidatud väljad, mis on arve ja kliendi üksuste jaoks saadaval, ja loetleb väljad, mida **ei** peaks koolituse ajal valima.</span><span class="sxs-lookup"><span data-stu-id="03d12-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="03d12-122">Iga sellise välja jaoks määratud kategooria viitab eelmise loendi kategooriatele.</span><span class="sxs-lookup"><span data-stu-id="03d12-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-dataverse-table"></a><span data-ttu-id="03d12-123">Arve Dataverse'i tabel</span><span class="sxs-lookup"><span data-stu-id="03d12-123">Invoice Dataverse table</span></span>

<span data-ttu-id="03d12-124">Järgmisel joonisel on näidatud arve tabeli jaoks saadaolevad väljad.</span><span class="sxs-lookup"><span data-stu-id="03d12-124">The following illustration shows the fields that are available for the invoice table.</span></span>

<span data-ttu-id="03d12-125">[![Arve tabeli jaoks saadaolevad väljad](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="03d12-125">[![Available fields for the invoice table](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="03d12-126">Järgmisi välju ei peaks koolituse jaoks valima.</span><span class="sxs-lookup"><span data-stu-id="03d12-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="03d12-127">**Arve konto** (kategooria 2)</span><span class="sxs-lookup"><span data-stu-id="03d12-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="03d12-128">**On suletud** (kategooria 3) – seda välja kasutatakse koolituse (suletud) ja prognoosimise (pole suletud) arvete filtreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="03d12-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="03d12-129">**Nimi** (kategooria 1)</span><span class="sxs-lookup"><span data-stu-id="03d12-129">**Name** (category 1)</span></span>
- <span data-ttu-id="03d12-130">**Allika ID** (kategooria 2)</span><span class="sxs-lookup"><span data-stu-id="03d12-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="03d12-131">**Allika kirje** (kategooria 2)</span><span class="sxs-lookup"><span data-stu-id="03d12-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="03d12-132">**Allika tabel** (kategooria 2)</span><span class="sxs-lookup"><span data-stu-id="03d12-132">**Source table** (category 2)</span></span>

### <a name="customer-dataverse-table"></a><span data-ttu-id="03d12-133">Kliendi Dataverse'i tabel</span><span class="sxs-lookup"><span data-stu-id="03d12-133">Customer Dataverse table</span></span>

<span data-ttu-id="03d12-134">Järgmisel joonisel on näidatud kliendi tabeli jaoks saadaolevad väljad.</span><span class="sxs-lookup"><span data-stu-id="03d12-134">The following illustration shows the fields that are available for the customer table.</span></span>

<span data-ttu-id="03d12-135">[![Kliendi tabeli jaoks saadaolevad väljad](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="03d12-135">[![Available fields for the customer table](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="03d12-136">Järgmist välja ei peaks koolituse jaoks valima.</span><span class="sxs-lookup"><span data-stu-id="03d12-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="03d12-137">**Rea kordumatu võti** (kategooria 2)</span><span class="sxs-lookup"><span data-stu-id="03d12-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="03d12-138">Filtrid</span><span class="sxs-lookup"><span data-stu-id="03d12-138">Filters</span></span>

<span data-ttu-id="03d12-139">Filtrid ei toeta praegu kliendi makse prognoosimise stsenaariumit.</span><span class="sxs-lookup"><span data-stu-id="03d12-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="03d12-140">Seetõttu valige suvand **Jäta see samm vahele** ja jätkake kokkuvõttelehega.</span><span class="sxs-lookup"><span data-stu-id="03d12-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="03d12-141">[![Filtritega mudelil keskendumine](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="03d12-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
