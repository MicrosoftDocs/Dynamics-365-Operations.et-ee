---
title: Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services
description: Selles teemas selgitatakse, kuidas laadida teenusest Microsoft Dynamics Lifecycle Services (LCS) alla elektroonilise aruandluse (ER) konfiguratsioone.
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a4411b25285128c849a715fdc7a2f5fe51580a3b
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="fc3e3-103">Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="fc3e3-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fc3e3-104">Selles teemas selgitatakse, kuidas laadida teenusest Microsoft Dynamics Lifecycle Services (LCS) alla elektroonilise aruandluse (ER) konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-104">This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="fc3e3-105">Selles õpikus selgitatakse, kuidas laadida teenusest Microsoft Dynamics Lifecycle Services (LCS) alla elektroonilise aruandluse (ER) konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-105">This tutorial guides you through the process of downloading the newest version of Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1.  <span data-ttu-id="fc3e3-106">Logige Finance and Operationsisse sisse, kasutades üht järgmistest rollidest.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-106">Sign in to Finance and Operations by using one of the following roles:</span></span>
    -   <span data-ttu-id="fc3e3-107">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="fc3e3-107">Electronic reporting developer</span></span>
    -   <span data-ttu-id="fc3e3-108">Elektroonilise aruandluse funktsionaalne konsultant</span><span class="sxs-lookup"><span data-stu-id="fc3e3-108">Electronic reporting functional consultant</span></span>
    -   <span data-ttu-id="fc3e3-109">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="fc3e3-109">System administrator</span></span>

2.  <span data-ttu-id="fc3e3-110">Minge jaotisse **Organisatsiooni haldamine** &gt; **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-110">Go to **Organization administration** &gt; **Electronic reporting**.</span></span>
3.  <span data-ttu-id="fc3e3-111">Valige jaotises **Konfiguratsiooni pakkujad** paan **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-111">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4.  <span data-ttu-id="fc3e3-112">Klõpsake paanil **Microsoft** suvandit **Hoidlad**.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-112">On the **Microsoft** tile, click **Repositories**.</span></span> <span data-ttu-id="fc3e3-113">[![ms-i-elektroonilise-aruandluse-värskendamine-lcs-ist-ms-i-hoidlate-loendi-avamine](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="fc3e3-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>
5.  <span data-ttu-id="fc3e3-114">Valige lehel **Konfiguratsioonihoidlad** ruudustikus olemasolev hoidla tüübiga **LCS**.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-114">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="fc3e3-115">Kui hoidlat ei kuvata ruudustikus, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-115">If this repository doesn't appear in the grid, follow these steps:</span></span>
    1.  <span data-ttu-id="fc3e3-116">Uue hoidla lisamiseks klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-116">Click **Add** to add a new repository.</span></span>
    2.  <span data-ttu-id="fc3e3-117">Valige hoidla tüüp **LCS**.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-117">Select **LCS** as the repository type.</span></span>
    3.  <span data-ttu-id="fc3e3-118">Klõpsake käsku **Loo hoidla**.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-118">Click **Create repository**.</span></span>
    4. <span data-ttu-id="fc3e3-119">Viiba kuvamisel järgige autoriseerimisjuhiseid.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-119">If prompted, follow the authorization instructions.</span></span>
    5.  <span data-ttu-id="fc3e3-120">Sisestage hoidla nimi ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-120">Enter a name and description for the repository.</span></span>
    6.  <span data-ttu-id="fc3e3-121">Uue hoidla kirje kinnitamiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-121">Click **OK** to confirm the new repository entry.</span></span>
    7.  <span data-ttu-id="fc3e3-122">Valige võrgustikus uus andmebaas tüübiga **LCS**.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-122">In the grid, select the new repository of the **LCS** type.</span></span>

6.  <span data-ttu-id="fc3e3-123">Valitud hoidla ER-i konfiguratsioonide loendi vaatamiseks klõpsake käsku **Ava**.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-123">Click **Open** to view the list of ER configurations for the selected repository.</span></span> <span data-ttu-id="fc3e3-124">[![ms-i-elektroonilise-aruandluse-värskendamine-lcs-ist-lcs-i-hoidla-loomine](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="fc3e3-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>
7.  <span data-ttu-id="fc3e3-125">Valige vasakul paanil konfiguratsioonide puus soovitud ER-i konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-125">In the configurations tree in the left pane, select the ER configuration that you require.</span></span>
8.  <span data-ttu-id="fc3e3-126">Kiirkaardil **Versioonid** valige valitud ER-i konfiguratsiooni nõutav versioon.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9.  <span data-ttu-id="fc3e3-127">Klõpsake käsku **Impordi**, et laadida valitud versioon LCS-ist alla Finance and Operationsi praegusesse eksemplari.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-127">Click **Import** to download the selected version from LCS to the current Finance and Operations instance.</span></span> <span data-ttu-id="fc3e3-128">**Märkus.** Nupp **Impordi** ei ole saadaval ER-i konfiguratsiooni versioonide puhul, mis on juba Dynamics 365 for Finance and Operationsi praeguses eksemplaris olemas.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-128">**Note:** The **Import** button is unavailable for ER configuration versions that are already present in the current Finance and Operations instance.</span></span> <span data-ttu-id="fc3e3-129">[![ms-i-elektroonilise-aruandluse-värskendamine-konfiguratsiooni-allalaadimine](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="fc3e3-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

<span data-ttu-id="fc3e3-130">**Märkus.** Olenevalt ER-i sätetest kontrollitakse konfiguratsioone pärast importimist.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-130">**Note:** Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="fc3e3-131">Võib-olla teavitatakse teid leitud vasturääkivustest.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="fc3e3-132">Probleemid tuleb enne imporditud konfiguratsiooni versiooni kasutamist lahendada.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="fc3e3-133">Lisateavet vaadaje selle teemaga seotud artiklite loendist.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-133">For more information, see the list of related articles for this topic.</span></span>

<a name="see-also"></a><span data-ttu-id="fc3e3-134">Vt ka</span><span class="sxs-lookup"><span data-stu-id="fc3e3-134">See also</span></span>
--------

[<span data-ttu-id="fc3e3-135">Elektroonilise aruandluse ülevaade</span><span class="sxs-lookup"><span data-stu-id="fc3e3-135">Electronic reporting overview</span></span>](general-electronic-reporting.md)




