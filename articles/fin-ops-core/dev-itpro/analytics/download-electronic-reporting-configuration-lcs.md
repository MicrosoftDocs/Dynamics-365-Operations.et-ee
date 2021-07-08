---
title: Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services
description: Selles teemas selgitatakse, kuidas laadida teenusest Microsoft Dynamics Lifecycle Services (LCS) alla elektroonilise aruandluse (ER) konfiguratsioone.
author: NickSelin
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 14f0f2b1a4d63101d432b1361379c61a70ac9345
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271179"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="03c48-103">Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="03c48-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03c48-104">Selles teemas selgitatakse, kuidas teenuse Microsoft Dynamics Lifecycle Services (LCS) [ühiste vahendite teegist](../lifecycle-services/asset-library.md) laadida alla [elektroonilise aruandluse (ER) konfiguratsioonide](general-electronic-reporting.md#Configuration) uusimat versiooni.</span><span class="sxs-lookup"><span data-stu-id="03c48-104">This topic explains how to download the newest version of [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the [Shared asset library](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03c48-105">LCS kasutamine elektroonilise aruandluse (ER) konfiguratsiooni talletushoidlana on [aegunud](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="03c48-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="03c48-106">Lisateavet vt jaotisest [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) ladustamise amortiseerimine](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="03c48-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

1. <span data-ttu-id="03c48-107">Logige rakendusse sisse, kasutades üht järgmistest rollidest.</span><span class="sxs-lookup"><span data-stu-id="03c48-107">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="03c48-108">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="03c48-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="03c48-109">Elektroonilise aruandluse funktsionaalne konsultant</span><span class="sxs-lookup"><span data-stu-id="03c48-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="03c48-110">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="03c48-110">System administrator</span></span>

2. <span data-ttu-id="03c48-111">Avage **Organisatsiooni haldamine** &gt; **Tööruumid** &gt; **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="03c48-111">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="03c48-112">Valige jaotises **Konfiguratsiooni pakkujad** paan **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="03c48-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="03c48-113">Valige paanil **Microsoft** suvand **Hoidlad**.</span><span class="sxs-lookup"><span data-stu-id="03c48-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    <span data-ttu-id="03c48-114">[![Paan Microsoft lokaliseerimise konfiguratsioonide lehel](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="03c48-114">[![Microsoft tile on the Localization configurations page](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="03c48-115">Valige lehel **Konfiguratsioonihoidlad** ruudustikus olemasolev hoidla tüübiga **LCS**.</span><span class="sxs-lookup"><span data-stu-id="03c48-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="03c48-116">Kui hoidlat ei kuvata ruudustikus, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="03c48-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="03c48-117">Hoidla lisamiseks valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="03c48-117">Select **Add** to add a repository.</span></span>
    2. <span data-ttu-id="03c48-118">Valige hoidla tüüp **LCS**.</span><span class="sxs-lookup"><span data-stu-id="03c48-118">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="03c48-119">Valige käsk **Loo hoidla**.</span><span class="sxs-lookup"><span data-stu-id="03c48-119">Select **Create repository**.</span></span>
    4. <span data-ttu-id="03c48-120">Kui teil palutakse end autoriseerida, järgige ekraanil kuvatavaid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="03c48-120">If you're prompted about authorization, follow the on-screen instructions.</span></span>
    5. <span data-ttu-id="03c48-121">Sisestage hoidla nimi ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="03c48-121">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="03c48-122">Uue hoidla kirje kinnitamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="03c48-122">Select **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="03c48-123">Valige võrgustikus uus andmebaas tüübiga **LCS**.</span><span class="sxs-lookup"><span data-stu-id="03c48-123">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="03c48-124">Valitud hoidla elektroonilise aruandluse konfiguratsioonide loendi vaatamiseks valige käsk **Ava**.</span><span class="sxs-lookup"><span data-stu-id="03c48-124">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="03c48-125">[![Konfiguratsioonihoidlate leht](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="03c48-125">[![Configuration repositories page](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

    > [!TIP]
    > <span data-ttu-id="03c48-126">Kui teil on probleeme LCS-i hoidlasse juurde pääsemisega konfiguratsioonide allalaadimiseks LCS-i ühiste vahendite teegist, saate selle asemel laadida konfiguratsioonid alla [globaalsest hoidlast](er-download-configurations-global-repo.md).</span><span class="sxs-lookup"><span data-stu-id="03c48-126">If you have trouble accessing the LCS repository to download configurations from the Shared asset library in LCS, you can download configurations from the [Global repository](er-download-configurations-global-repo.md) instead.</span></span>

7. <span data-ttu-id="03c48-127">Valige vasakul paanil konfiguratsioonide puus soovitud ER-i konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="03c48-127">In the configurations tree in the left pane, select the required ER configuration.</span></span>
8. <span data-ttu-id="03c48-128">Kiirkaardil **Versioonid** valige valitud ER-i konfiguratsiooni nõutav versioon.</span><span class="sxs-lookup"><span data-stu-id="03c48-128">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="03c48-129">Valige käsk **Impordi**, et laadida valitud versioon LCS-ist alla praegusesse eksemplari.</span><span class="sxs-lookup"><span data-stu-id="03c48-129">Select **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="03c48-130">Nupp **Impordi** ei ole saadaval ER-i konfiguratsiooni versioonide puhul, mis on juba praeguses eksemplaris olemas.</span><span class="sxs-lookup"><span data-stu-id="03c48-130">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="03c48-131">[![Konfiguratsioonihoidla leht](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="03c48-131">[![Configuration repository page](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="03c48-132">Olenevalt ER-i sätetest kontrollitakse konfiguratsioone pärast importimist.</span><span class="sxs-lookup"><span data-stu-id="03c48-132">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="03c48-133">Võib-olla teavitatakse teid leitud vasturääkivustest.</span><span class="sxs-lookup"><span data-stu-id="03c48-133">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="03c48-134">Probleemid tuleb enne imporditud konfiguratsiooni versiooni kasutamist lahendada.</span><span class="sxs-lookup"><span data-stu-id="03c48-134">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="03c48-135">Lisateavet vaadake selle teemaga seotud teemade loendist.</span><span class="sxs-lookup"><span data-stu-id="03c48-135">For more information, see the list of related topics for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="03c48-136">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="03c48-136">Additional resources</span></span>

[<span data-ttu-id="03c48-137">Elektroonilise aruandluse (ER) ülevaade</span><span class="sxs-lookup"><span data-stu-id="03c48-137">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="03c48-138">Elektroonilise aruandluse konfiguratsioonide allalaadimine konfiguratsiooniteenuse globaalsest hoidlast</span><span class="sxs-lookup"><span data-stu-id="03c48-138">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
