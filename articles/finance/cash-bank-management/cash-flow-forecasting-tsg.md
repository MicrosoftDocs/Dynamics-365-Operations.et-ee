---
title: Rahavoo prognoosimise häälestuse tõrkeotsing
description: Selles teemas on toodud vastused küsimustele, mis võivad teil tekkida rahavoo prognoosimise konfigureerimisel. Selles käsitletakse korduma kippuvaid küsimusi (KKK) rahavoo häälestuse, rahavoo värskenduste ja rahavoo Power BI kohta.
author: panolte
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b4760d7a0d0c14e2df8df20c2f81ec41e077cc0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827310"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="06f23-104">Rahavoo prognoosimise häälestuse tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="06f23-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06f23-105">Selles teemas on toodud vastused küsimustele, mis võivad teil tekkida rahavoo prognoosimise konfigureerimisel.</span><span class="sxs-lookup"><span data-stu-id="06f23-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="06f23-106">Selles käsitletakse korduma kippuvaid küsimusi (KKK) rahavoo häälestuse, rahavoo värskenduste ja rahavoo Power BI kohta.</span><span class="sxs-lookup"><span data-stu-id="06f23-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="06f23-107">Miks kuvatakse rahavoog ainult ühe juriidilise isiku kohta?</span><span class="sxs-lookup"><span data-stu-id="06f23-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="06f23-108">Rahavoo prognoosimine konfigureeritakse ja arvutatakse juriidilise isiku kohta.</span><span class="sxs-lookup"><span data-stu-id="06f23-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="06f23-109">Tulemusi kuvab Power BI aruannete ja rahavoo prognoosimise funktsioon Finance'i ülevaadetes.</span><span class="sxs-lookup"><span data-stu-id="06f23-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="06f23-110">Rahavoo prognoosimine tuleb häälestada iga juriidilise isiku kohta, keda puudutavat prognoosi soovite näha.</span><span class="sxs-lookup"><span data-stu-id="06f23-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="06f23-111">Vaadake üle rahavoo prognoosimise konfiguratsioon kõigis oma juriidilistes isikutes.</span><span class="sxs-lookup"><span data-stu-id="06f23-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="06f23-112">Teise võimalusena vaadake üle kõigi juriidiliste isikute rahavoo prognoosimist puudutav konfiguratsioon ja veenduge, et see oleks häälestatud nii, nagu soovite.</span><span class="sxs-lookup"><span data-stu-id="06f23-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="06f23-113">Miks ei kuva Power BI kõiki rahavoo andmeid?</span><span class="sxs-lookup"><span data-stu-id="06f23-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="06f23-114">Enne rahavoo prognooside kuvamist Power BI vaadetes tuleb läbida mitu etappi.</span><span class="sxs-lookup"><span data-stu-id="06f23-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="06f23-115">Vaadake üle järgmine kontroll-loend ja veenduge, et iga etapp oleks läbitud.</span><span class="sxs-lookup"><span data-stu-id="06f23-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="06f23-116">Häälestage rahavoog iga juriidilise isiku jaoks.</span><span class="sxs-lookup"><span data-stu-id="06f23-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="06f23-117">Määrake pearaamatu parameetrites süsteemivaluuta ja süsteemi vahetuskursi tüüp.</span><span class="sxs-lookup"><span data-stu-id="06f23-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="06f23-118">Määrake pearaamatu arvestusvaluuta ja vahetuskursi tüüp.</span><span class="sxs-lookup"><span data-stu-id="06f23-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="06f23-119">Sisestage kandevaluuta ja arvestusvaluuta vaheline vahetuskurss.</span><span class="sxs-lookup"><span data-stu-id="06f23-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="06f23-120">Sisestage arvestusvaluuta ja süsteemivaluuta vaheline vahetuskurss.</span><span class="sxs-lookup"><span data-stu-id="06f23-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="06f23-121">Sisestage arvestusvaluuta ja iga pangavaluuta vaheline vahetuskurss.</span><span class="sxs-lookup"><span data-stu-id="06f23-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="06f23-122">Miks toimis Power BI rahavoog eelmistes versioonides, kuid on nüüd tühi?</span><span class="sxs-lookup"><span data-stu-id="06f23-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="06f23-123">Kontrollige, et üksuse kaupluse mõõtmised „Cash flow measure V2“ ja „LedgerCovLiquidityMeasurement“ oleksid konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="06f23-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="06f23-124">Lisateavet selle kohta, kuidas töötada andmeüksuse salvega leiate [Power BI integratsioonist Üksuse salvega](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="06f23-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="06f23-125">Kontrollige, et kõik sisu vaatamiseks vajalikud Power BI sammud on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="06f23-125">Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="06f23-126">Lisateabe saamiseks vt [Sularaha ülevaate Power BI sisu](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="06f23-126">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="06f23-127">Kas üksuse kaupluse üksused on värskendatud?</span><span class="sxs-lookup"><span data-stu-id="06f23-127">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="06f23-128">Andmete ajakohasuse ja täpsuse tagamiseks peate üksusi aeg-ajalt värskendama.</span><span class="sxs-lookup"><span data-stu-id="06f23-128">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="06f23-129">Konkreetse üksuse käsitsi värskendamiseks avage jaotis **Süsteemihaldus \> Häälestus \> Üksuse kauplus**, valige üksus ja seejärel tehke valik **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="06f23-129">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="06f23-130">Andmeid saab värskendada ka automaatselt.</span><span class="sxs-lookup"><span data-stu-id="06f23-130">The data can also be updated automatically.</span></span> <span data-ttu-id="06f23-131">Määrake lehe **Üksuse kauplus** suvandi **Automaatne värskendamine lubatud** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="06f23-131">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a><span data-ttu-id="06f23-132">Millist arvutusmeetodit tuleks kasutada rahavoo prognoosimisel?</span><span class="sxs-lookup"><span data-stu-id="06f23-132">Which calculation method should be used when calculating cash flow forecasts?</span></span>

<span data-ttu-id="06f23-133">Rahavoo prognoosi arvutusmeetodil on kaks olulist valikuvalikut.</span><span class="sxs-lookup"><span data-stu-id="06f23-133">The Cash flow forecast calculation method has two important selection options.</span></span> <span data-ttu-id="06f23-134">Valik **Uus** arvutab rahavoo prognoosi uutele dokumentidele ja neile dokumentidele, mis onpeale viimase pakett-töö käitamist muutunud.</span><span class="sxs-lookup"><span data-stu-id="06f23-134">The **New** option will calculate cash flow forecasts for new documents and documents that have changed since the last batch job ran.</span></span> <span data-ttu-id="06f23-135">See valik käivitub kiiremini, sest see töötleb väiksemat dokumentide alamkogumit.</span><span class="sxs-lookup"><span data-stu-id="06f23-135">This option tends to run faster because it processes a smaller subset of documents.</span></span> <span data-ttu-id="06f23-136">Valik **Kokku** arvutab rahavoo prognoosi ümber iga süsteemi dokumendi jaoks.</span><span class="sxs-lookup"><span data-stu-id="06f23-136">The **Total** option will recalculate cash flow forecasts for every document in the system.</span></span> <span data-ttu-id="06f23-137">See valik võtab rohkem aega, kuna selle lõpetamiseks on rohkem tööd.</span><span class="sxs-lookup"><span data-stu-id="06f23-137">This option takes more time because it has more work to complete.</span></span>

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a><span data-ttu-id="06f23-138">Kuidas parandada rahavoo prognoosi korduva pakett töö jõudlust?</span><span class="sxs-lookup"><span data-stu-id="06f23-138">How do I improve the performance of the cash flow forecasting recurring batch job?</span></span>

<span data-ttu-id="06f23-139">Soovitame uue käivitada oma rahavoo prognoos iga päev üks kord tipptunni väliselt kasutades arvutusmeetodit **Uus** .</span><span class="sxs-lookup"><span data-stu-id="06f23-139">We recommend running your cash flow forecast once each day during the off-peak hours using the **New** calculation method.</span></span> <span data-ttu-id="06f23-140">Soovitame seda lähenemist kasutada kuus päeva nädalas.</span><span class="sxs-lookup"><span data-stu-id="06f23-140">We recommend using this approach six days per week.</span></span> <span data-ttu-id="06f23-141">Seejärel käivitage likviidsuse prognoos iga nädal, kasutades **Kokku** arvutusmeetodit kõige vähema tegevusega päevadel.</span><span class="sxs-lookup"><span data-stu-id="06f23-141">Then run a cash flow forecast once each week using the **Total** calculation method on the day with the least amount of activity.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

