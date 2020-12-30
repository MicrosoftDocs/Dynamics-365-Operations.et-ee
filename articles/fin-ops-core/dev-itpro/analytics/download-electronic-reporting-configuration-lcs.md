---
title: Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services
description: Selles teemas selgitatakse, kuidas laadida teenusest Microsoft Dynamics Lifecycle Services (LCS) alla elektroonilise aruandluse (ER) konfiguratsioone.
author: NickSelin
manager: AnnBe
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 719b277fb828ea2085ea80bc4a36c2af3412f66b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683301"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="11698-103">Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="11698-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11698-104">Selles teemas selgitatakse, kuidas teenuse Microsoft Dynamics Lifecycle Services (LCS) [ühiste vahendite teegist](../lifecycle-services/asset-library.md) laadida alla [elektroonilise aruandluse (ER) konfiguratsioonide](general-electronic-reporting.md#Configuration) uusimat versiooni.</span><span class="sxs-lookup"><span data-stu-id="11698-104">This topic explains how to download the newest version of [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the [Shared asset library](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="11698-105">Logige rakendusse sisse, kasutades üht järgmistest rollidest.</span><span class="sxs-lookup"><span data-stu-id="11698-105">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="11698-106">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="11698-106">Electronic reporting developer</span></span>
    - <span data-ttu-id="11698-107">Elektroonilise aruandluse funktsionaalne konsultant</span><span class="sxs-lookup"><span data-stu-id="11698-107">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="11698-108">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="11698-108">System administrator</span></span>

2. <span data-ttu-id="11698-109">Avage **Organisatsiooni haldamine** &gt; **Tööruumid** &gt; **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="11698-109">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="11698-110">Valige jaotises **Konfiguratsiooni pakkujad** paan **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="11698-110">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="11698-111">Valige paanil **Microsoft** suvand **Hoidlad**.</span><span class="sxs-lookup"><span data-stu-id="11698-111">On the **Microsoft** tile, select **Repositories**.</span></span>

    <span data-ttu-id="11698-112">[![Paan Microsoft lokaliseerimise konfiguratsioonide lehel](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="11698-112">[![Microsoft tile on the Localization configurations page](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="11698-113">Valige lehel **Konfiguratsioonihoidlad** ruudustikus olemasolev hoidla tüübiga **LCS**.</span><span class="sxs-lookup"><span data-stu-id="11698-113">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="11698-114">Kui hoidlat ei kuvata ruudustikus, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="11698-114">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="11698-115">Hoidla lisamiseks valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="11698-115">Select **Add** to add a repository.</span></span>
    2. <span data-ttu-id="11698-116">Valige hoidla tüüp **LCS**.</span><span class="sxs-lookup"><span data-stu-id="11698-116">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="11698-117">Valige käsk **Loo hoidla**.</span><span class="sxs-lookup"><span data-stu-id="11698-117">Select **Create repository**.</span></span>
    4. <span data-ttu-id="11698-118">Kui teil palutakse end autoriseerida, järgige ekraanil kuvatavaid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="11698-118">If you're prompted about authorization, follow the on-screen instructions.</span></span>
    5. <span data-ttu-id="11698-119">Sisestage hoidla nimi ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="11698-119">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="11698-120">Uue hoidla kirje kinnitamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="11698-120">Select **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="11698-121">Valige võrgustikus uus andmebaas tüübiga **LCS**.</span><span class="sxs-lookup"><span data-stu-id="11698-121">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="11698-122">Valitud hoidla elektroonilise aruandluse konfiguratsioonide loendi vaatamiseks valige käsk **Ava**.</span><span class="sxs-lookup"><span data-stu-id="11698-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="11698-123">[![Konfiguratsioonihoidlate leht](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="11698-123">[![Configuration repositories page](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

    > [!TIP]
    > <span data-ttu-id="11698-124">Kui teil on probleeme LCS-i hoidlasse juurde pääsemisega konfiguratsioonide allalaadimiseks LCS-i ühiste vahendite teegist, saate selle asemel laadida konfiguratsioonid alla [globaalsest hoidlast](er-download-configurations-global-repo.md).</span><span class="sxs-lookup"><span data-stu-id="11698-124">If you have trouble accessing the LCS repository to download configurations from the Shared asset library in LCS, you can download configurations from the [Global repository](er-download-configurations-global-repo.md) instead.</span></span>

7. <span data-ttu-id="11698-125">Valige vasakul paanil konfiguratsioonide puus soovitud ER-i konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="11698-125">In the configurations tree in the left pane, select the required ER configuration.</span></span>
8. <span data-ttu-id="11698-126">Kiirkaardil **Versioonid** valige valitud ER-i konfiguratsiooni nõutav versioon.</span><span class="sxs-lookup"><span data-stu-id="11698-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="11698-127">Valige käsk **Impordi**, et laadida valitud versioon LCS-ist alla praegusesse eksemplari.</span><span class="sxs-lookup"><span data-stu-id="11698-127">Select **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="11698-128">Nupp **Impordi** ei ole saadaval ER-i konfiguratsiooni versioonide puhul, mis on juba praeguses eksemplaris olemas.</span><span class="sxs-lookup"><span data-stu-id="11698-128">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="11698-129">[![Konfiguratsioonihoidla leht](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="11698-129">[![Configuration repository page](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="11698-130">Olenevalt ER-i sätetest kontrollitakse konfiguratsioone pärast importimist.</span><span class="sxs-lookup"><span data-stu-id="11698-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="11698-131">Võib-olla teavitatakse teid leitud vasturääkivustest.</span><span class="sxs-lookup"><span data-stu-id="11698-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="11698-132">Probleemid tuleb enne imporditud konfiguratsiooni versiooni kasutamist lahendada.</span><span class="sxs-lookup"><span data-stu-id="11698-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="11698-133">Lisateavet vaadake selle teemaga seotud teemade loendist.</span><span class="sxs-lookup"><span data-stu-id="11698-133">For more information, see the list of related topics for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="11698-134">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="11698-134">Additional resources</span></span>

[<span data-ttu-id="11698-135">Elektroonilise aruandluse (ER) ülevaade</span><span class="sxs-lookup"><span data-stu-id="11698-135">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="11698-136">Elektroonilise aruandluse konfiguratsioonide allalaadimine konfiguratsiooniteenuse globaalsest hoidlast</span><span class="sxs-lookup"><span data-stu-id="11698-136">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)
