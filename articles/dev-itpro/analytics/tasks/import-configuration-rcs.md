---
title: (ER) Konfiguratsioonide importimine RCS-ist
description: Selles teemas kirjeldatakse, kuidas saab kasutaja importida elektroonilise aruandluse konfiguratsiooni uut versiooni RCS-ist.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c458cf815837fb7e4688c4c0443b7962cac403a5
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727002"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="79a54-103">(ER) Konfiguratsioonide importimine RCS-ist</span><span class="sxs-lookup"><span data-stu-id="79a54-103">(ER) Import configurations from RCS</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="79a54-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad importida uue elektroonilise aruandluse (ER) konfiguratsiooni teenusest Microsoft Regulatory Configuration Services (RCS).</span><span class="sxs-lookup"><span data-stu-id="79a54-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="79a54-105">Selles näites valite elektroonilise aruandluse konfiguratsiooni versiooni, mis on konfigureeritud RCS-i eksemplaris, ja impordite selle praegusesse Finance and Operationsi eksemplari näidisettevõtte Litware, Inc. jaoks. Neid etappe saab läbida igas ettevõttes, kuna elektroonilise aruandluse konfiguratsioonid on ettevõtete ühiskasutuses.</span><span class="sxs-lookup"><span data-stu-id="79a54-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current Finance and Operations instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="79a54-106">Etappide lõpuleviimiseks, peate esmalt läbima etapid teemas [Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="79a54-106">To complete these steps, you must first complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="79a54-107">Nende etappide läbimiseks peab teil olema ka juurdepääs RCS-i eksemplarile, mis sisaldab vähemalt üht elektroonilise aruandluse konfiguratsiooni olekuga **Lõpetatud** või **Ühine**.</span><span class="sxs-lookup"><span data-stu-id="79a54-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="79a54-108">Avage **Organisatsiooni haldamine** > **Tööruumid** > **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="79a54-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="79a54-109">Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja märgitud kui **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="79a54-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="79a54-110">Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima etapid teemas [Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="79a54-110">If you don’t see this configuration provider, complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="79a54-111">Kui teie ettevõtte jaoks pole RCS-i keskkonda eraldatud, klõpsake välist linki **Regulatory services – konfigureerimine** ja järgige juhiseid RCS-i keskkonna eraldamiseks.</span><span class="sxs-lookup"><span data-stu-id="79a54-111">If you have no RCS environment provisioned to your company, click **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="79a54-112">Klõpsake valikut **Elektroonilise aruandluse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="79a54-112">Click **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="79a54-113">Klõpsake vahekaarti **RCS**.</span><span class="sxs-lookup"><span data-stu-id="79a54-113">Click the **RCS** tab.</span></span> 
6. <span data-ttu-id="79a54-114">Kui RCS-i keskkond on juba teie ettevõtte jaoks eraldatud, kasutage sellele ligipääsemiseks lehe URL-i.</span><span class="sxs-lookup"><span data-stu-id="79a54-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="79a54-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="79a54-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="79a54-116">Registreerige uus elektroonilise aruandluse hoidla.</span><span class="sxs-lookup"><span data-stu-id="79a54-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="79a54-117">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="79a54-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="79a54-118">Valige pakkuja Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="79a54-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="79a54-119">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="79a54-119">Click Repositories.</span></span> 
4. <span data-ttu-id="79a54-120">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="79a54-120">Click Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="79a54-121">Sisestage väljale Konfiguratsioonihoidla tüüp valik RCS.</span><span class="sxs-lookup"><span data-stu-id="79a54-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="79a54-122">Klõpsake käsku Loo hoidla.</span><span class="sxs-lookup"><span data-stu-id="79a54-122">Click Create repository.</span></span> 
7. <span data-ttu-id="79a54-123">Valige või sisestage väärtus väljal RCS keskkonna kuvatav nimi.</span><span class="sxs-lookup"><span data-stu-id="79a54-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="79a54-124">Valige soovitud RCS-i eksemplar.</span><span class="sxs-lookup"><span data-stu-id="79a54-124">Select the desired RCS instance.</span></span> <span data-ttu-id="79a54-125">Pange tähele, et neid võib olla mitu.</span><span class="sxs-lookup"><span data-stu-id="79a54-125">Note that you can have several of them.</span></span> 
9. <span data-ttu-id="79a54-126">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="79a54-126">Click OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="79a54-127">Elektroonilise aruandluse konfiguratsioonide importimine RCS-põhisest hoidlast</span><span class="sxs-lookup"><span data-stu-id="79a54-127">Import ER configurations from RCS based repository</span></span>
1. <span data-ttu-id="79a54-128">Klõpsake nuppu **Näita filtreid**.</span><span class="sxs-lookup"><span data-stu-id="79a54-128">Click **Show filters**.</span></span> 
2. <span data-ttu-id="79a54-129">Sisestage filtri tehtemärgi **algab väärtusega** abil filtri väärtus **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="79a54-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="79a54-130">Kui avate valitud hoidla, klõpsake lehel **Loo ühendus teenusega Regulatory Configuration Services** linki **Klõpsake siin teenusega Regulatory Configuration Services ühenduse loomiseks**.</span><span class="sxs-lookup"><span data-stu-id="79a54-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, click **Click here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="79a54-131">Klõpsake nuppu **Ava**.</span><span class="sxs-lookup"><span data-stu-id="79a54-131">Click **Open**.</span></span> 
5. <span data-ttu-id="79a54-132">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="79a54-132">Click **Close**.</span></span> 
6. <span data-ttu-id="79a54-133">Valige elektroonilise aruandluse konfiguratsiooni sobiv versioon ja klõpsake nuppu **Impordi**, et viia see Finance and Operationsi praegusesse eksemplari.</span><span class="sxs-lookup"><span data-stu-id="79a54-133">Select the desired version of ER configuration and click **Import** to bring it in the current Finance and Operations instance.</span></span>
