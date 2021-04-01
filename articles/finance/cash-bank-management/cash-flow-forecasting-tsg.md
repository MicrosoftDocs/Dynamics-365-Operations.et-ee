---
title: Rahavoo prognoosimise häälestuse tõrkeotsing
description: Selles teemas on toodud vastused küsimustele, mis võivad teil tekkida rahavoo prognoosimise konfigureerimisel. Selles käsitletakse korduma kippuvaid küsimusi (KKK) rahavoo häälestuse, rahavoo värskenduste ja rahavoo Power BI kohta.
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1cde9321259753bd0cacab3706c7f8455598ff3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232485"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="87e61-104">Rahavoo prognoosimise häälestuse tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="87e61-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87e61-105">Selles teemas on toodud vastused küsimustele, mis võivad teil tekkida rahavoo prognoosimise konfigureerimisel.</span><span class="sxs-lookup"><span data-stu-id="87e61-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="87e61-106">Selles käsitletakse korduma kippuvaid küsimusi (KKK) rahavoo häälestuse, rahavoo värskenduste ja rahavoo Power BI kohta.</span><span class="sxs-lookup"><span data-stu-id="87e61-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="87e61-107">Miks kuvatakse rahavoog ainult ühe juriidilise isiku kohta?</span><span class="sxs-lookup"><span data-stu-id="87e61-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="87e61-108">Rahavoo prognoosimine konfigureeritakse ja arvutatakse juriidilise isiku kohta.</span><span class="sxs-lookup"><span data-stu-id="87e61-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="87e61-109">Tulemusi kuvab Power BI aruannete ja rahavoo prognoosimise funktsioon Finance'i ülevaadetes.</span><span class="sxs-lookup"><span data-stu-id="87e61-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="87e61-110">Rahavoo prognoosimine tuleb häälestada iga juriidilise isiku kohta, keda puudutavat prognoosi soovite näha.</span><span class="sxs-lookup"><span data-stu-id="87e61-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="87e61-111">Vaadake üle rahavoo prognoosimise konfiguratsioon kõigis oma juriidilistes isikutes.</span><span class="sxs-lookup"><span data-stu-id="87e61-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="87e61-112">Teise võimalusena vaadake üle kõigi juriidiliste isikute rahavoo prognoosimist puudutav konfiguratsioon ja veenduge, et see oleks häälestatud nii, nagu soovite.</span><span class="sxs-lookup"><span data-stu-id="87e61-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="87e61-113">Miks ei kuva Power BI kõiki rahavoo andmeid?</span><span class="sxs-lookup"><span data-stu-id="87e61-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="87e61-114">Enne rahavoo prognooside kuvamist Power BI vaadetes tuleb läbida mitu etappi.</span><span class="sxs-lookup"><span data-stu-id="87e61-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="87e61-115">Vaadake üle järgmine kontroll-loend ja veenduge, et iga etapp oleks läbitud.</span><span class="sxs-lookup"><span data-stu-id="87e61-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="87e61-116">Häälestage rahavoog iga juriidilise isiku jaoks.</span><span class="sxs-lookup"><span data-stu-id="87e61-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="87e61-117">Määrake pearaamatu parameetrites süsteemivaluuta ja süsteemi vahetuskursi tüüp.</span><span class="sxs-lookup"><span data-stu-id="87e61-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="87e61-118">Määrake pearaamatu arvestusvaluuta ja vahetuskursi tüüp.</span><span class="sxs-lookup"><span data-stu-id="87e61-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="87e61-119">Sisestage kandevaluuta ja arvestusvaluuta vaheline vahetuskurss.</span><span class="sxs-lookup"><span data-stu-id="87e61-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="87e61-120">Sisestage arvestusvaluuta ja süsteemivaluuta vaheline vahetuskurss.</span><span class="sxs-lookup"><span data-stu-id="87e61-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="87e61-121">Sisestage arvestusvaluuta ja iga pangavaluuta vaheline vahetuskurss.</span><span class="sxs-lookup"><span data-stu-id="87e61-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="87e61-122">Miks toimis Power BI rahavoog eelmistes versioonides, kuid on nüüd tühi?</span><span class="sxs-lookup"><span data-stu-id="87e61-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="87e61-123">Kontrollige, et üksuse kaupluse mõõtmised „Cash flow measure V2“ ja „LedgerCovLiquidityMeasurement“ oleksid konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="87e61-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="87e61-124">Lisateavet üksuse kaupluses andmetega töötamise kohta leiate teemast [Power BI integreerimine üksuse kauplusega](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Veenduge, et kõik Power BI sisu kuvamiseks vajalikud etapid oleksid läbitud.</span><span class="sxs-lookup"><span data-stu-id="87e61-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="87e61-125">Lisateabe saamiseks vt [Sularaha ülevaate Power BI sisu](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="87e61-125">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="87e61-126">Kas üksuse kaupluse üksused on värskendatud?</span><span class="sxs-lookup"><span data-stu-id="87e61-126">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="87e61-127">Andmete ajakohasuse ja täpsuse tagamiseks peate üksusi aeg-ajalt värskendama.</span><span class="sxs-lookup"><span data-stu-id="87e61-127">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="87e61-128">Konkreetse üksuse käsitsi värskendamiseks avage jaotis **Süsteemihaldus \> Häälestus \> Üksuse kauplus**, valige üksus ja seejärel tehke valik **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="87e61-128">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="87e61-129">Andmeid saab värskendada ka automaatselt.</span><span class="sxs-lookup"><span data-stu-id="87e61-129">The data can also be updated automatically.</span></span> <span data-ttu-id="87e61-130">Määrake lehe **Üksuse kauplus** suvandi **Automaatne värskendamine lubatud** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="87e61-130">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]