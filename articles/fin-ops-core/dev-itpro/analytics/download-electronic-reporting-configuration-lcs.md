---
title: Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services
description: Selles teemas selgitatakse, kuidas laadida teenusest Microsoft Dynamics Lifecycle Services (LCS) alla elektroonilise aruandluse (ER) konfiguratsioone.
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 49785835ee2da911d7b8d1360e1c42f850f1153f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771489"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="816ce-103">Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="816ce-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="816ce-104">Selles teemas selgitatakse, kuidas laadida teenusest Microsoft Dynamics Lifecycle Services (LCS) alla elektroonilise aruandluse (ER) konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="816ce-104">This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="816ce-105">Selles õpikus selgitatakse, kuidas laadida teenusest Microsoft Dynamics Lifecycle Services (LCS) alla elektroonilise aruandluse (ER) konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="816ce-105">This tutorial guides you through the process of downloading the newest version of Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="816ce-106">Logige rakendusse sisse, kasutades üht järgmistest rollidest.</span><span class="sxs-lookup"><span data-stu-id="816ce-106">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="816ce-107">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="816ce-107">Electronic reporting developer</span></span>
    - <span data-ttu-id="816ce-108">Elektroonilise aruandluse funktsionaalne konsultant</span><span class="sxs-lookup"><span data-stu-id="816ce-108">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="816ce-109">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="816ce-109">System administrator</span></span>

2. <span data-ttu-id="816ce-110">Minge jaotisse **Organisatsiooni haldamine** &gt; **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="816ce-110">Go to **Organization administration** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="816ce-111">Valige jaotises **Konfiguratsiooni pakkujad** paan **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="816ce-111">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="816ce-112">Klõpsake paanil **Microsoft** suvandit **Hoidlad**.</span><span class="sxs-lookup"><span data-stu-id="816ce-112">On the **Microsoft** tile, click **Repositories**.</span></span>

    <span data-ttu-id="816ce-113">[![ms-i-elektroonilise-aruandluse-värskendamine-lcs-ist-ms-i-hoidlate-loendi-avamine](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="816ce-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="816ce-114">Valige lehel **Konfiguratsioonihoidlad** ruudustikus olemasolev hoidla tüübiga **LCS**.</span><span class="sxs-lookup"><span data-stu-id="816ce-114">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="816ce-115">Kui hoidlat ei kuvata ruudustikus, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="816ce-115">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="816ce-116">Uue hoidla lisamiseks klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="816ce-116">Click **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="816ce-117">Valige hoidla tüüp **LCS**.</span><span class="sxs-lookup"><span data-stu-id="816ce-117">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="816ce-118">Klõpsake käsku **Loo hoidla**.</span><span class="sxs-lookup"><span data-stu-id="816ce-118">Click **Create repository**.</span></span>
    4. <span data-ttu-id="816ce-119">Viiba kuvamisel järgige autoriseerimisjuhiseid.</span><span class="sxs-lookup"><span data-stu-id="816ce-119">If prompted, follow the authorization instructions.</span></span>
    5. <span data-ttu-id="816ce-120">Sisestage hoidla nimi ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="816ce-120">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="816ce-121">Uue hoidla kirje kinnitamiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="816ce-121">Click **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="816ce-122">Valige võrgustikus uus andmebaas tüübiga **LCS**.</span><span class="sxs-lookup"><span data-stu-id="816ce-122">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="816ce-123">Valitud hoidla ER-i konfiguratsioonide loendi vaatamiseks klõpsake käsku **Ava**.</span><span class="sxs-lookup"><span data-stu-id="816ce-123">Click **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="816ce-124">[![ms-i-elektroonilise-aruandluse-värskendamine-lcs-ist-lcs-i-hoidla-loomine](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="816ce-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

7. <span data-ttu-id="816ce-125">Valige vasakul paanil konfiguratsioonide puus soovitud ER-i konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="816ce-125">In the configurations tree in the left pane, select the ER configuration that you require.</span></span>
8. <span data-ttu-id="816ce-126">Kiirkaardil **Versioonid** valige valitud ER-i konfiguratsiooni nõutav versioon.</span><span class="sxs-lookup"><span data-stu-id="816ce-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="816ce-127">Klõpsake käsku **Impordi**, et laadida valitud versioon LCS-ist alla praegusesse eksemplari.</span><span class="sxs-lookup"><span data-stu-id="816ce-127">Click **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="816ce-128">Nupp **Impordi** ei ole saadaval ER-i konfiguratsiooni versioonide puhul, mis on juba praeguses eksemplaris olemas.</span><span class="sxs-lookup"><span data-stu-id="816ce-128">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="816ce-129">[![ms-i-elektroonilise-aruandluse-värskendamine-konfiguratsiooni-allalaadimine](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="816ce-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="816ce-130">Olenevalt ER-i sätetest kontrollitakse konfiguratsioone pärast importimist.</span><span class="sxs-lookup"><span data-stu-id="816ce-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="816ce-131">Võib-olla teavitatakse teid leitud vasturääkivustest.</span><span class="sxs-lookup"><span data-stu-id="816ce-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="816ce-132">Probleemid tuleb enne imporditud konfiguratsiooni versiooni kasutamist lahendada.</span><span class="sxs-lookup"><span data-stu-id="816ce-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="816ce-133">Lisateavet vaadaje selle teemaga seotud artiklite loendist.</span><span class="sxs-lookup"><span data-stu-id="816ce-133">For more information, see the list of related articles for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="816ce-134">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="816ce-134">Additional resources</span></span>

[<span data-ttu-id="816ce-135">Elektroonilise aruandluse (ER) ülevaade</span><span class="sxs-lookup"><span data-stu-id="816ce-135">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)