---
title: Rahavoo prognoosimises välisandmete kasutamine (eelversioon)
description: See teema kirjeldab seadistuse etappe, mille peate täitma, et välisandmeid saaks sisestada või importida rahavoo prognoosidesse.
author: rcarlson
manager: AnnBe
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ae0eba6d397725cf425d9781a597d904e1958d44
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009387"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="3e63f-103">Rahavoo prognoosimises välisandmete kasutamine (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="3e63f-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="3e63f-104">Välisandmeid saab sisestada või importida rahavoo prognoosidesse.</span><span class="sxs-lookup"><span data-stu-id="3e63f-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="3e63f-105">See teema kirjeldab seadistuse etappe, mis on omased välisandmete kasutamisele ja võimaldavad kaasata välisandmed rahavoo prognoosimisse.</span><span class="sxs-lookup"><span data-stu-id="3e63f-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="3e63f-106">Välisandmete häälestus</span><span class="sxs-lookup"><span data-stu-id="3e63f-106">External data setup</span></span>

<span data-ttu-id="3e63f-107">Kasutage vahekaarti **Väline allikas** lehel **Rahavoo prognoosi häälestamine** (**Sularaha- ja pangahaldus \> Rahavoo prognoosimine**), et sisestada sätted, mis toetavad rahavoo prognoosimises välisandmete kasutamist.</span><span class="sxs-lookup"><span data-stu-id="3e63f-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="3e63f-108">Lisateavet häälestamise kohta vaadake jaotisest [Rahavoo prognoosimine](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span><span class="sxs-lookup"><span data-stu-id="3e63f-108">For more information about the setup, see [Cash flow forecasting](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span></span>

<span data-ttu-id="3e63f-109">Rahavoo prognoosimisse välisandmete sisestamiseks saate kasutada välisandmete sisestamiseks ja muutmiseks Excelis avamise kasutuskogemust.</span><span class="sxs-lookup"><span data-stu-id="3e63f-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="3e63f-110">Valige nupp **Välisandmed** ja valige seejärel kas **Lisa välisandmed** või **Redigeeri olemasolevaid välisandmeid**.</span><span class="sxs-lookup"><span data-stu-id="3e63f-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="3e63f-111">Kui Microsoft Exceli fail on avatud, saate sisestada teavet järgmistele väljadele.</span><span class="sxs-lookup"><span data-stu-id="3e63f-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="3e63f-112">**Kirje ID**</span><span class="sxs-lookup"><span data-stu-id="3e63f-112">**Entry ID**</span></span>
- <span data-ttu-id="3e63f-113">**Kirjeldus** (valikuline)</span><span class="sxs-lookup"><span data-stu-id="3e63f-113">**Description** (optional)</span></span>
- <span data-ttu-id="3e63f-114">**Välise allika nimi** – valige loendist üks väärtustest, mille finantsülevaadete seadistamisel määrasite.</span><span class="sxs-lookup"><span data-stu-id="3e63f-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="3e63f-115">**Juriidiline isik**</span><span class="sxs-lookup"><span data-stu-id="3e63f-115">**Legal Entity**</span></span>
- <span data-ttu-id="3e63f-116">**Kuupäev**</span><span class="sxs-lookup"><span data-stu-id="3e63f-116">**Date**</span></span>
- <span data-ttu-id="3e63f-117">**Summa kandevaluutas**</span><span class="sxs-lookup"><span data-stu-id="3e63f-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="3e63f-118">**Valuutakood**</span><span class="sxs-lookup"><span data-stu-id="3e63f-118">**Currency Code**</span></span>
- <span data-ttu-id="3e63f-119">**Vaikedimensioon** (valikuline)</span><span class="sxs-lookup"><span data-stu-id="3e63f-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="3e63f-120">**Dokumendi number** (valikuline)</span><span class="sxs-lookup"><span data-stu-id="3e63f-120">**Document number** (optional)</span></span>
- <span data-ttu-id="3e63f-121">**Kontonumber** (valikuline)</span><span class="sxs-lookup"><span data-stu-id="3e63f-121">**Account number** (optional)</span></span>
- <span data-ttu-id="3e63f-122">**Konto nimi** (valikuline)</span><span class="sxs-lookup"><span data-stu-id="3e63f-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="3e63f-123">Välisandmete importimine andmehalduse raamistikku kasutades</span><span class="sxs-lookup"><span data-stu-id="3e63f-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="3e63f-124">Saate rahavoo prognoosimiseks importida välisandmed, kasutades tööruumi **Andmehaldus** ja olemit, mille nimi on **Rahavoo prognoosimise välisallika kirje**.</span><span class="sxs-lookup"><span data-stu-id="3e63f-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="3e63f-125">Lisaks kui peate teisaldama häälestuse andmed ühest keskkonnast teise, siis on häälestamise tabelite jaoks saadaval järgmised nõutavad olemid.</span><span class="sxs-lookup"><span data-stu-id="3e63f-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="3e63f-126">Likviidsuse planeerimise välise allika seadistus</span><span class="sxs-lookup"><span data-stu-id="3e63f-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="3e63f-127">Likviidsuse planeerimise välise allika juriidilise isiku seadistus</span><span class="sxs-lookup"><span data-stu-id="3e63f-127">Cash flow forecast external source legal entity setup</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="3e63f-128">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="3e63f-128">Privacy notice</span></span>
<span data-ttu-id="3e63f-129">Eelvaated 1) võivad kasutada vähem privaatsus- ja turbemeetmeid kui rakenduse Dynamics 365 Finance and Operations teenus; 2) ei ole hõlmatud selle teenuse teenusetaseme leppes; 3) ei tohi olla kasutusel isiklike andmete ega muude andmete töötlemiseks, mis on seaduste või määrustega kaitstud; 4) on piiratud toega.</span><span class="sxs-lookup"><span data-stu-id="3e63f-129">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
