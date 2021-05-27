---
title: E-kaubanduse arenduskeskkonna häälestamine, et siluda järguga 1 jaemüügiserveri virtuaalmasin
description: E-kaubanduse arenduskeskkonna häälestamine, et siluda järguga 1 jaemüügiserveri virtuaalmasin (VM).
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 38a616c418c3b32490c9adaf69a69af0d47d3478
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019442"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a><span data-ttu-id="af802-103">E-kaubanduse arenduskeskkonna häälestamine, et siluda järguga 1 jaemüügiserveri virtuaalmasin</span><span class="sxs-lookup"><span data-stu-id="af802-103">Set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="af802-104">E-kaubanduse arenduskeskkonna häälestamine, et siluda järguga 1 jaemüügiserveri virtuaalmasin (VM).</span><span class="sxs-lookup"><span data-stu-id="af802-104">This topic explains how to set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine (VM).</span></span>

## <a name="description"></a><span data-ttu-id="af802-105">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="af802-105">Description</span></span>

<span data-ttu-id="af802-106">Microsoft Dynamics 365 Commerce Järgu 1 keskkonnad juurutatakse tavaliselt Commerce Runtime'i (CRT) ja kassa laienduse arendamiseks.</span><span class="sxs-lookup"><span data-stu-id="af802-106">Microsoft Dynamics 365 Commerce Tier 1 environments are typically deployed for Commerce runtime (CRT) and point of sale (POS) extension development.</span></span> <span data-ttu-id="af802-107">Need on eraldiseisev keskkond.</span><span class="sxs-lookup"><span data-stu-id="af802-107">They are standalone environments.</span></span> <span data-ttu-id="af802-108">Teenuse (SaaS) olemuse tõttu ei sisalda need e-kaubanduse komponente.</span><span class="sxs-lookup"><span data-stu-id="af802-108">Because of the software as a service (SaaS) nature of the architecture, they don't include e-commerce components.</span></span>

<span data-ttu-id="af802-109">Mõne stsenaariumi korral võite soovida katsetada laiendeid järguga 1 keskkonnas, nii et saate siluda laiendusi e-äri komponentidest.</span><span class="sxs-lookup"><span data-stu-id="af802-109">In some scenarios, you might want to test calls to extensions in a Tier 1 environment, so that you can debug extensions from e-commerce components.</span></span> <span data-ttu-id="af802-110">Üldiste juhiste saamiseks vaadake artiklit [Esimese järgu Commerce'i arenduskeskkonna silumine](../e-commerce-extensibility/debug-tier-1.md).</span><span class="sxs-lookup"><span data-stu-id="af802-110">For general instructions, see [Debug against a Tier 1 Commerce development environment](../e-commerce-extensibility/debug-tier-1.md).</span></span>

<span data-ttu-id="af802-111">Järgu 1 keskkonna suhtes silumisel, kuna sait kutsub nüüd teist jaemüügiserverit, võivad ristserveri kutsed põhjustada mitmesuguseid sisu turbepoliitikaga seotud tõrkeid.</span><span class="sxs-lookup"><span data-stu-id="af802-111">When you debug against a Tier 1 environment, because the site is now calling a different Retail Server, cross-server calls might cause various errors that are related to the content security policy.</span></span>

<span data-ttu-id="af802-112">Järgmisel joonisel on toodud näide tõrkest, mis võib ilmneda, kui toote üksikasjade lehel on valitud variant.</span><span class="sxs-lookup"><span data-stu-id="af802-112">The following illustration shows an example of an error that might occur when a variant is selected on a product details page.</span></span>

![Tõrge, kui toote üksikasjade lehel on valitud variant](media/unhandled-rejection-error.jpg)

<span data-ttu-id="af802-114">Järgmisel joonisel on näidatud sarnane tõrke näide brauseri siluritööriistades (F12 Arendustööriistad).</span><span class="sxs-lookup"><span data-stu-id="af802-114">The following illustration shows an example of a similar error in a browser's debugger tools (F12 Developer Tools).</span></span> <span data-ttu-id="af802-115">Veateade sisaldab sisu turbepoliitika direktiivi rikkumisi.</span><span class="sxs-lookup"><span data-stu-id="af802-115">The error message mentions violation of the content security policy directive.</span></span>

![Siluritööriistade tõrge](media/debugger-tools-error.JPG)

## <a name="resolution"></a><span data-ttu-id="af802-117">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="af802-117">Resolution</span></span>

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a><span data-ttu-id="af802-118">Commerce'i saidikonstruktori saidi jaoks sisu turbepoliitika keelamine</span><span class="sxs-lookup"><span data-stu-id="af802-118">Disable the content security policy for the site in Commerce site builder</span></span>

1. <span data-ttu-id="af802-119">Valige sait, millel te töötate.</span><span class="sxs-lookup"><span data-stu-id="af802-119">Select the site that you're working on.</span></span>
1. <span data-ttu-id="af802-120">Valige **Saidi sätted** ja seejärel valige suvand **Laiendused**.</span><span class="sxs-lookup"><span data-stu-id="af802-120">Select **Settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="af802-121">Valige vahekaardil **Sisu turbepoliitika** suvand **Keela sisu turbepoliitika**.</span><span class="sxs-lookup"><span data-stu-id="af802-121">On the **Content security policy** tab, select **Disable content security policy**.</span></span>
1. <span data-ttu-id="af802-122">Valige käsk **Salvesta ja avalda**.</span><span class="sxs-lookup"><span data-stu-id="af802-122">Select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="af802-123">Ettevõtetesse ja tarbekaupadesse (B2C) sisselogimine ei tööta kohalikus arenduskeskkonnas.</span><span class="sxs-lookup"><span data-stu-id="af802-123">Business-to-consumer (B2C) sign-in won't work in a local development environment.</span></span> <span data-ttu-id="af802-124">Kuid saate kasutada külalisi väljaregistreerimist või koostada lehekülje m nii, et simuleerida kasutaja sisselogimist vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="af802-124">However, you can use guest checkouts or build page mocks to simulate a user sign-in as required.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="af802-125">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="af802-125">Additional resources</span></span>

[<span data-ttu-id="af802-126">E-kaubanduse võrgupõhise laiendatavuse arendamise alustamine</span><span class="sxs-lookup"><span data-stu-id="af802-126">Get started with e-commerce online extensibility development</span></span>](../e-commerce-extensibility/sdk-getting-started.md)

[<span data-ttu-id="af802-127">Sisu turbepoliitika (CSP) haldamine e-äri saidil</span><span class="sxs-lookup"><span data-stu-id="af802-127">Manage content security policy (CSP) on e-commerce site</span></span>](../manage-csp.md)
