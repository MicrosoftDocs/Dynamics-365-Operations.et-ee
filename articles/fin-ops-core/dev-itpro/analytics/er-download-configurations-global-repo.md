---
title: Elektroonilise aruandluse konfiguratsioonide allalaadimine konfiguratsiooniteenuse globaalsest hoidlast
description: Selles teemas selgitatakse, kuidas laadida konfiguratsiooniteenuse globaalsest hoidlast alla elektroonilise aruandluse konfiguratsioone.
author: NickSelin
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a96e78a64fe0559ae5f3bfddabf3fe1cad8a3dcb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679554"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a><span data-ttu-id="e6712-103">Elektroonilise aruandluse konfiguratsioonide allalaadimine konfiguratsiooniteenuse globaalsest hoidlast</span><span class="sxs-lookup"><span data-stu-id="e6712-103">Download ER configurations from the Global repository of Configuration service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6712-104">Selles teemas selgitatakse, kuidas laadida konfiguratsiooniteenuse globaalsest hoidlast alla [elektroonilise aruandluse konfiguratsioone](general-electronic-reporting.md#Configuration).</span><span class="sxs-lookup"><span data-stu-id="e6712-104">This topic explains how to download [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the Global repository of configuration service.</span></span> <span data-ttu-id="e6712-105">Lisateavet vt teemast [Microsoft Dynamics 365 for Finance and Operations – Regulatory Services, konfiguratsiooniteenus](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="e6712-105">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="open-configurations-repository"></a><span data-ttu-id="e6712-106">Konfiguratsioonihoidla avamine</span><span class="sxs-lookup"><span data-stu-id="e6712-106">Open configurations repository</span></span>

1. <span data-ttu-id="e6712-107">Logige rakendusse Dynamics 365 Finance sisse, kasutades üht järgmistest rollidest.</span><span class="sxs-lookup"><span data-stu-id="e6712-107">Sign in to the Dynamics 365 Finance application using one of the following roles:</span></span>

    - <span data-ttu-id="e6712-108">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="e6712-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="e6712-109">Elektroonilise aruandluse funktsionaalne konsultant</span><span class="sxs-lookup"><span data-stu-id="e6712-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="e6712-110">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="e6712-110">System administrator</span></span>

2. <span data-ttu-id="e6712-111">Avage **Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="e6712-111">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="e6712-112">Valige jaotises **Konfiguratsiooni pakkujad** paan **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="e6712-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
3. <span data-ttu-id="e6712-113">Valige paanil **Microsoft** suvand **Hoidlad**.</span><span class="sxs-lookup"><span data-stu-id="e6712-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    ![Elektroonilise aruandluse tööruum](./media/er-download-configurations-global-repo-er-workspace.png)

4. <span data-ttu-id="e6712-115">Valige lehel **Konfiguratsioonihoidlad** ruudustikus olemasolev hoidla, mille tüüp on **Globaalne**.</span><span class="sxs-lookup"><span data-stu-id="e6712-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **Global** type.</span></span> <span data-ttu-id="e6712-116">Kui hoidlat ei kuvata ruudustikus, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e6712-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="e6712-117">Uue hoidla lisamiseks valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="e6712-117">Select **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="e6712-118">Valige hoidla tüübiks **Globaalne** ja seejärel **Loo hoidla**.</span><span class="sxs-lookup"><span data-stu-id="e6712-118">Select **Global** as the repository type, and then select **Create repository**.</span></span>
    3. <span data-ttu-id="e6712-119">Viiba kuvamisel järgige autoriseerimisjuhiseid.</span><span class="sxs-lookup"><span data-stu-id="e6712-119">If prompted, follow the authorization instructions.</span></span>
    4. <span data-ttu-id="e6712-120">Sisestage hoidla nimi ja kirjeldus ning seejärel valige uue hoidla kirje kinnitamiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6712-120">Enter a name and description for the repository and then select **OK** to confirm the new repository entry.</span></span>
    5. <span data-ttu-id="e6712-121">Valige ruudustikus uus hoidla, mille tüüp on **Globaalne**.</span><span class="sxs-lookup"><span data-stu-id="e6712-121">In the grid, select the new repository of the **Global** type.</span></span>

5. <span data-ttu-id="e6712-122">Valitud hoidla elektroonilise aruandluse konfiguratsioonide loendi vaatamiseks valige käsk **Ava**.</span><span class="sxs-lookup"><span data-stu-id="e6712-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    ![Konfiguratsioonihoidlate leht](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a><span data-ttu-id="e6712-124">Ühe konfiguratsiooni importimine</span><span class="sxs-lookup"><span data-stu-id="e6712-124">Import a single configuration</span></span>

1. <span data-ttu-id="e6712-125">Valige lehel **Konfiguratsioonihoidlad** konfiguratsioonide puult soovitud elektroonilise aruandluse konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="e6712-125">On the **Configuration repositories** page, in the configurations tree, select the ER configuration that you want.</span></span>
2. <span data-ttu-id="e6712-126">Kiirkaardil **Versioonid** valige valitud ER-i konfiguratsiooni nõutav versioon.</span><span class="sxs-lookup"><span data-stu-id="e6712-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
3. <span data-ttu-id="e6712-127">Valige käsk **Impordi**, et laadida valitud versioon globaalsest hoidlast alla Finance'i praegusesse eksemplari.</span><span class="sxs-lookup"><span data-stu-id="e6712-127">Select **Import** to download the selected version from Global repository to the current Finance instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e6712-128">Nupp **Impordi** ei ole saadaval elektroonilise aruandluse konfiguratsiooni versioonide puhul, mis on juba praeguses Finance'i eksemplaris olemas.</span><span class="sxs-lookup"><span data-stu-id="e6712-128">The **Import** button is unavailable for ER configuration versions that are already present in the current Finance instance.</span></span>

    ![Konfiguratsioonide hoidla leht](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a><span data-ttu-id="e6712-130">Filtreeritud konfiguratsioonide importimine</span><span class="sxs-lookup"><span data-stu-id="e6712-130">Import filtered configurations</span></span>

1. <span data-ttu-id="e6712-131">Laiendage lehel **Konfiguratsioonihoidlad** konfiguratsioonide puul kiirkaart **Filter**.</span><span class="sxs-lookup"><span data-stu-id="e6712-131">On the **Configuration repositories** page, in the configurations tree, expand the **Filter** FastTab.</span></span>
2. <span data-ttu-id="e6712-132">Sisestage ruudustikus **Sildid** kõik vajalikud sildid.</span><span class="sxs-lookup"><span data-stu-id="e6712-132">In the **Tags** grid, add any tags that are needed.</span></span>
3. <span data-ttu-id="e6712-133">Valige väljal **Riigi/piirkonna kohaldatavus** sobivad riigi/piirkonna koodid ja seejärel valige **Rakenda filter**.</span><span class="sxs-lookup"><span data-stu-id="e6712-133">In the **Country/region applicability** field, select the appropriate country/region codes, and then select  **Apply filter**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e6712-134">Kiirkaardil **Konfiguratsioonid** kuvatakse kõik konfiguratsioonid, mis vastavad määratletud valikutingimustele.</span><span class="sxs-lookup"><span data-stu-id="e6712-134">The **Configurations** FastTab shows all the configurations that satisfy the specified selection conditions.</span></span>

4. <span data-ttu-id="e6712-135">Valige kiirkaardil **Konfiguratsioonid** käsk **Impordi**, et laadida filtreeritud konfiguratsioonid globaalsest hoidlast praegusesse eksemplari.</span><span class="sxs-lookup"><span data-stu-id="e6712-135">On the **Configurations** FastTab, select **Import** to download the filtered configurations from the Global repository to the current instance.</span></span>
5. <span data-ttu-id="e6712-136">Valige kiirkaardil **Konfiguratsioonid** käsk **Lähtesta filter**, et puhastada määratletud valikutingimused.</span><span class="sxs-lookup"><span data-stu-id="e6712-136">On the **Configurations** FastTab, select **Reset filter** to clean up the specified selection conditions.</span></span>

    ![Konfiguratsioonihoidla leht](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> <span data-ttu-id="e6712-138">Olenevalt ER-i sätetest kontrollitakse konfiguratsioone pärast importimist.</span><span class="sxs-lookup"><span data-stu-id="e6712-138">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="e6712-139">Võib-olla teavitatakse teid leitud vasturääkivustest.</span><span class="sxs-lookup"><span data-stu-id="e6712-139">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="e6712-140">Probleemid tuleb enne imporditud konfiguratsiooni versiooni kasutamist lahendada.</span><span class="sxs-lookup"><span data-stu-id="e6712-140">Before you can use the imported configuration version, you must resolve the issues.</span></span> <span data-ttu-id="e6712-141">Lisateavet leiate selle teemaga seotud ressursside loendist.</span><span class="sxs-lookup"><span data-stu-id="e6712-141">For more information, see the list of related resources for this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="e6712-142">Elektroonilise aruandluse konfiguratsiooni saab konfigureerida teistest konfiguratsioonidest sõltuvana.</span><span class="sxs-lookup"><span data-stu-id="e6712-142">ER configurations can be configured as being dependent on other configurations.</span></span> <span data-ttu-id="e6712-143">Seetõttu võidakse valitud konfiguratsiooniga koos automaatselt importida ka muid konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="e6712-143">Therefore, along with a selected configuration, other configurations might be automatically imported.</span></span> <span data-ttu-id="e6712-144">Lisateavet konfiguratsioonide sõltuvuste kohta leiate jaotisest [ER-i konfiguratsioonide sõltuvuse määramine teistest komponentidest](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span><span class="sxs-lookup"><span data-stu-id="e6712-144">For more about configuration dependencies, see [Define the dependency of ER configurations on other components](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e6712-145">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e6712-145">Additional resources</span></span>

[<span data-ttu-id="e6712-146">Elektroonilise aruandluse (ER) ülevaade</span><span class="sxs-lookup"><span data-stu-id="e6712-146">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
