---
title: ER-konfiguratsioonide värskendatud versioonide importimine
description: Selles teemas selgitatakse, kuidas importida konfiguratsiooniteenuse globaalsest hoidlast elektroonilise aruandluse (ER) konfiguratsioonide värskendatud versioone.
author: NickSelin
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4f167a0209713b5bca0cefe0135abd46a149a515
ms.sourcegitcommit: 1e6a7b50596eaf9d965e0155f3f2c50f7f50747e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/22/2020
ms.locfileid: "3498088"
---
# <a name="import-updated-versions-of-er-configurations"></a><span data-ttu-id="4ba54-103">ER-konfiguratsioonide värskendatud versioonide importimine</span><span class="sxs-lookup"><span data-stu-id="4ba54-103">Import updated versions of ER configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ba54-104">Elektroonilise aruandluse (ER) [hoidlaid](general-electronic-reporting.md#Repository) kasutatakse [ER-konfiguratsioonide](general-electronic-reporting.md#Configuration) ühiskasutusse andmiseks.</span><span class="sxs-lookup"><span data-stu-id="4ba54-104">Electronic reporting (ER) [repositories](general-electronic-reporting.md#Repository) are used to share [ER configurations](general-electronic-reporting.md#Configuration).</span></span> <span data-ttu-id="4ba54-105">Saate [importda](download-electronic-reporting-configuration-lcs.md) ER-konfiguratsioone erinevatest hoidlatest oma Microsoft Dynamics 365 Finance'i eksemplari.</span><span class="sxs-lookup"><span data-stu-id="4ba54-105">You can [import](download-electronic-reporting-configuration-lcs.md) ER configurations from different repositories into your instance of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="4ba54-106">ER-konfiguratsioonide importimisel saavad [konfiguratsioonipakkujad](general-electronic-reporting.md#Provider) avaldada hoidlate uusi [versioone](general-electronic-reporting.md#component-versioning), et neid saaks ühiskasutusse anda.</span><span class="sxs-lookup"><span data-stu-id="4ba54-106">When you import ER configurations, [configuration providers](general-electronic-reporting.md#Provider) can publish new [versions](general-electronic-reporting.md#component-versioning) repositories so that they can be shared.</span></span>

<span data-ttu-id="4ba54-107">Selles teemas selgitatakse, kuidas importida konfiguratsiooniteenuse globaalsest hoidlast ER-konfiguratsioonide värskendatud versioone.</span><span class="sxs-lookup"><span data-stu-id="4ba54-107">This topic explains how to import updated versions of ER configurations from the Global repository of the Configuration service.</span></span> <span data-ttu-id="4ba54-108">Lisateavet vt teemast [Microsoft Dynamics 365 for Finance and Operations – Regulatory Services, konfiguratsiooniteenus](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="4ba54-108">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="review-the-available-updated-versions"></a><span data-ttu-id="4ba54-109">Saadaolevate värskendatud versioonide ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="4ba54-109">Review the available updated versions</span></span>

1. <span data-ttu-id="4ba54-110">Logige Finance'i sisse, kasutades üht järgmistest rollidest.</span><span class="sxs-lookup"><span data-stu-id="4ba54-110">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="4ba54-111">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="4ba54-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="4ba54-112">Elektroonilise aruandluse funktsionaalne konsultant</span><span class="sxs-lookup"><span data-stu-id="4ba54-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="4ba54-113">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="4ba54-113">System administrator</span></span>

2. <span data-ttu-id="4ba54-114">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="4ba54-114">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="4ba54-115">Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Seostatud lingid** paan **Konfiguratsioonide versioonide värskenduste importimine**.</span><span class="sxs-lookup"><span data-stu-id="4ba54-115">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>

    ![Lokalisatsiooni konfiguratsioonide leht](./media/er-download-updated-versions-global-repo1.png)

4. <span data-ttu-id="4ba54-117">Valige dialoogiboksi **Elektroonilise aruandluse konfiguratsioonide versioonide värksenduste importimine** väljal **Käitusrežiim** suvand **Kuva ainult saadaolevad värskendused**.</span><span class="sxs-lookup"><span data-stu-id="4ba54-117">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Only show available updates**.</span></span> <span data-ttu-id="4ba54-118">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="4ba54-118">Then select **OK**.</span></span> 

    ![Käitusrežiimi välja väärtuseks on seatud Kuva ainult saadaolevad värskendused](./media/er-download-updated-versions-global-repo2.png)

5. <span data-ttu-id="4ba54-120">Vaadake üle vastuvõetud teated.</span><span class="sxs-lookup"><span data-stu-id="4ba54-120">Review the messages that you receive.</span></span> <span data-ttu-id="4ba54-121">Need teated annavad järgmist teavet praeguse Finance'i eksemplari ER-konfiguratsioonide kohta võrreldes globaalse hoidla sisuga.</span><span class="sxs-lookup"><span data-stu-id="4ba54-121">These messages provide the following information about the ER configurations in the current Finance instance and how they compare to the content of the Global repository:</span></span>

    - <span data-ttu-id="4ba54-122">ER-konfiguratsioonide koguarv</span><span class="sxs-lookup"><span data-stu-id="4ba54-122">The total number of ER configurations</span></span>
    - <span data-ttu-id="4ba54-123">ER-konfiguratsioonid, mida pole globaalses hoidlas</span><span class="sxs-lookup"><span data-stu-id="4ba54-123">ER configurations that aren't present in the Global repository</span></span>
    - <span data-ttu-id="4ba54-124">ER-konfiguratsioonid, mille uusim versioon on praeguses Finance'i eksemplaris juba saadaval (nende ER-konfiguratsioonide täieliku loendi kuvamiseks valige link **Teate üksikasjad**.)</span><span class="sxs-lookup"><span data-stu-id="4ba54-124">ER configurations for which the latest version is already available in the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![Teade „Järgmiste konfiguratsioonide uusimad versioonid on juba imporditud” ja teate üksikasjad](./media/er-download-updated-versions-global-repo3.png)

    - <span data-ttu-id="4ba54-126">ER-konfiguratsioonid, mille uusim versioon on saadaval globaalses hoidlas ja saab importida praegusesse Finance'i eksemplari (nende ER-konfiguratsioonide täieliku loendi kuvamiseks valige link **Teate üksikasjad**.)</span><span class="sxs-lookup"><span data-stu-id="4ba54-126">ER configurations for which the latest version is available in the Global repository and can be imported into the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![Teade „Saadaolevad värskendused” ja teate üksikasjad](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a><span data-ttu-id="4ba54-128">Saadaolevate värskendatud versioonide importimine</span><span class="sxs-lookup"><span data-stu-id="4ba54-128">Import available updated versions</span></span>

1. <span data-ttu-id="4ba54-129">Logige Finance'i sisse, kasutades üht järgmistest rollidest.</span><span class="sxs-lookup"><span data-stu-id="4ba54-129">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="4ba54-130">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="4ba54-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="4ba54-131">Elektroonilise aruandluse funktsionaalne konsultant</span><span class="sxs-lookup"><span data-stu-id="4ba54-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="4ba54-132">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="4ba54-132">System administrator</span></span>

2. <span data-ttu-id="4ba54-133">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="4ba54-133">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="4ba54-134">Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Seostatud lingid** paan **Konfiguratsioonide versioonide värskenduste importimine**.</span><span class="sxs-lookup"><span data-stu-id="4ba54-134">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>
4. <span data-ttu-id="4ba54-135">Valige dialoogiboksi **Elektroonilise aruandluse konfiguratsioonide versioonide värskenduste importimine** väljal **Käitusrežiim** suvand **Impordi uusimad värskendused**, et importida ER-konfiguratsioonide uusimad versioonid globaalsest hoidlast praegusesse Finance'i eksemplari.</span><span class="sxs-lookup"><span data-stu-id="4ba54-135">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Import latest updates** to import the latest versions of ER configurations from the Global repository into the current Finance instance.</span></span>
5. <span data-ttu-id="4ba54-136">Importimise jaoks pakett-töö plaanimiseks määrake kiirkaardi **Käivita taustal** suvandi **Pakktöötlus** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="4ba54-136">To schedule a batch job for the import, on the **Run in the background** FastTab, set the **Batch processing** option to **Yes**.</span></span> <span data-ttu-id="4ba54-137">Kui soovite korrata importimist regulaarselt, konfigureerige nõutav kordumine.</span><span class="sxs-lookup"><span data-stu-id="4ba54-137">If you want to repeat the import periodically, configure the required recurrence.</span></span>

    ![Käitusrežiimi välja väärtuseks on seatud Impordi uusimad värskendused](./media/er-download-updated-versions-global-repo5.png)

6. <span data-ttu-id="4ba54-139">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4ba54-139">Select **OK**.</span></span>
7. <span data-ttu-id="4ba54-140">Et teada saada, millised konfiguratsiooni versioonid on imporditud, järgige ühte järgmistest etappidest.</span><span class="sxs-lookup"><span data-stu-id="4ba54-140">To learn what configuration versions have been imported, follow one of these steps:</span></span>

    - <span data-ttu-id="4ba54-141">Kui käivitate importimise pakett-töö kasutamise asemel interaktiivselt, vaadake üle vastuvõetud teated.</span><span class="sxs-lookup"><span data-stu-id="4ba54-141">If you run the import interactively instead of using a batch job, review the messages that you receive.</span></span>

        ![Interaktiivse importimise käitamise ajal vastuvõetud teated](./media/er-download-updated-versions-global-repo6.png)

    - <span data-ttu-id="4ba54-143">Kui käivitate importimise partiirežiimis, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="4ba54-143">If you run the import in batch mode, follow these steps:</span></span>

        1. <span data-ttu-id="4ba54-144">Avage jaotis **Üldine** \> **Päringud** \> **Pakett-tööd** \> **Minu pakett-tööd**.</span><span class="sxs-lookup"><span data-stu-id="4ba54-144">Go to **Common** \> **Inquiries** \> **Batch jobs** \> **My batch jobs**.</span></span>
        2. <span data-ttu-id="4ba54-145">Otsige üles ja valige töö **Elektroonilise aruandluse konfiguratsiooni versioonide värskenduste importimine** ja seejärel valige toimingupaani vahekaardil **Pakett-töö** töö ajaloo kuvamiseks suvand **Pakett-töö ajalugu**.</span><span class="sxs-lookup"><span data-stu-id="4ba54-145">Find and select the **Import electronic reporting configurations versions updates** job, and then, on the Action Pane, on the **Batch job** tab, select **Batch job history** to view the job history.</span></span>
        3. <span data-ttu-id="4ba54-146">Valige lehel **Pakett-töö ajalugu** suvand **Logi**.</span><span class="sxs-lookup"><span data-stu-id="4ba54-146">On the **Batch job history** page, select **Log**.</span></span> <span data-ttu-id="4ba54-147">Seejärel valige töölogi kuvamiseks vastuvõetud teatest link **Teade üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="4ba54-147">Then, in the message that you receive, select the **Message details** link to view the job log.</span></span>

        ![Töölogi](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> <span data-ttu-id="4ba54-149">Me ei soovita korduva pakett-töö plaanimist, et importida ER-konfiguratsioonide värskendatud versioone globaalsest hoidlast otse töökeskkonda, kuna imporditud versioonid on kasutamiseks kohe saadaval.</span><span class="sxs-lookup"><span data-stu-id="4ba54-149">We don't recommend that you schedule a recurring batch job to import updated versions of ER configurations directly from the Global repository into a production environment, because the imported versions will immediately be available for use.</span></span> <span data-ttu-id="4ba54-150">Selle asemel kasutage seda lähenemist ER-konfiguratsioonide versioonide juurutamiseks liivakastikeskkonda.</span><span class="sxs-lookup"><span data-stu-id="4ba54-150">Instead, use this approach to deploy versions of ER configurations to a sandbox environment.</span></span> <span data-ttu-id="4ba54-151">Seejärel saab neid kõigepealt liivakastikeskkonnas hinnata enne töökeskkonda juurutamist.</span><span class="sxs-lookup"><span data-stu-id="4ba54-151">They can then be evaluated in the sandbox environment before they are deployed to a production environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4ba54-152">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="4ba54-152">Additional resources</span></span>

- [<span data-ttu-id="4ba54-153">Elektroonilise aruandluse (ER) ülevaade</span><span class="sxs-lookup"><span data-stu-id="4ba54-153">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="4ba54-154">Elektroonilise aruandluse konfiguratsioonide allalaadimine konfiguratsiooniteenuse globaalsest hoidlast</span><span class="sxs-lookup"><span data-stu-id="4ba54-154">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)
