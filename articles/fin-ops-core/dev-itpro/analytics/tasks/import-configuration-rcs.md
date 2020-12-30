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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b591df3d384e8dc59646ebb9d0205001db040a55
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684183"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="21313-103">(ER) Konfiguratsioonide importimine RCS-ist</span><span class="sxs-lookup"><span data-stu-id="21313-103">(ER) Import configurations from RCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="21313-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad importida uue elektroonilise aruandluse (ER) konfiguratsiooni teenusest Microsoft Regulatory Configuration Services (RCS).</span><span class="sxs-lookup"><span data-stu-id="21313-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="21313-105">Selles näites valite elektroonilise aruandluse konfiguratsiooni versiooni, mis on konfigureeritud RCS-i eksemplaris, ja impordite selle praegusesse eksemplari näidisettevõtte Litware, Inc. jaoks. Neid etappe saab läbida igas ettevõttes, kuna elektroonilise aruandluse konfiguratsioonid on ettevõtete ühiskasutuses.</span><span class="sxs-lookup"><span data-stu-id="21313-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="21313-106">Etappide lõpuleviimiseks, peate esmalt läbima etapid teemas [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="21313-106">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="21313-107">Nende etappide läbimiseks peab teil olema ka juurdepääs RCS-i eksemplarile, mis sisaldab vähemalt üht elektroonilise aruandluse konfiguratsiooni olekuga **Lõpetatud** või **Ühine**.</span><span class="sxs-lookup"><span data-stu-id="21313-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="21313-108">Avage **Organisatsiooni haldamine** > **Tööruumid** > **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="21313-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="21313-109">Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja märgitud kui **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="21313-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="21313-110">Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima teemas [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md) toodud juhised.</span><span class="sxs-lookup"><span data-stu-id="21313-110">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="21313-111">Kui teie ettevõtte jaoks pole RCS-i keskkonda eraldatud, valige väline link **Regulatory services – konfigureerimine** ja järgige juhiseid RCS-i keskkonna eraldamiseks.</span><span class="sxs-lookup"><span data-stu-id="21313-111">If you have no RCS environment provisioned to your company, select **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="21313-112">Valige **Elektroonilise aruandluse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="21313-112">Select **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="21313-113">Valige vahekaart **RCS**.</span><span class="sxs-lookup"><span data-stu-id="21313-113">Select the **RCS** tab.</span></span> 
6. <span data-ttu-id="21313-114">Kui RCS-i keskkond on juba teie ettevõtte jaoks eraldatud, kasutage sellele ligipääsemiseks lehe URL-i.</span><span class="sxs-lookup"><span data-stu-id="21313-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="21313-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="21313-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="21313-116">Registreerige uus elektroonilise aruandluse hoidla.</span><span class="sxs-lookup"><span data-stu-id="21313-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="21313-117">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="21313-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="21313-118">Valige pakkuja Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="21313-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="21313-119">Valige Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="21313-119">Select Repositories.</span></span> 
4. <span data-ttu-id="21313-120">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="21313-120">Select Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="21313-121">Sisestage väljale Konfiguratsioonihoidla tüüp valik RCS.</span><span class="sxs-lookup"><span data-stu-id="21313-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="21313-122">Valige käsk Loo hoidla.</span><span class="sxs-lookup"><span data-stu-id="21313-122">Select Create repository.</span></span> 
7. <span data-ttu-id="21313-123">Valige või sisestage väärtus väljal RCS keskkonna kuvatav nimi.</span><span class="sxs-lookup"><span data-stu-id="21313-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="21313-124">Valige soovitud RCS-i eksemplar.</span><span class="sxs-lookup"><span data-stu-id="21313-124">Select the desired RCS instance.</span></span> <span data-ttu-id="21313-125">Teil võib neid olla mitu.</span><span class="sxs-lookup"><span data-stu-id="21313-125">You can have several of them.</span></span> 
9. <span data-ttu-id="21313-126">Valige nupp OK.</span><span class="sxs-lookup"><span data-stu-id="21313-126">Select OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="21313-127">Elektroonilise aruandluse konfiguratsioonide importimine RCS-põhisest hoidlast</span><span class="sxs-lookup"><span data-stu-id="21313-127">Import ER configurations from RCS-based repository</span></span>
1. <span data-ttu-id="21313-128">Valige **Kuva filtrid**.</span><span class="sxs-lookup"><span data-stu-id="21313-128">Select **Show filters**.</span></span> 
2. <span data-ttu-id="21313-129">Sisestage filtri tehtemärgi **algab väärtusega** abil filtri väärtus **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="21313-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="21313-130">Kui avate valitud hoidla, valige lehel **Loo ühendus teenusega Regulatory Configuration Services** link **Valige siin teenusega Regulatory Configuration Services ühenduse loomiseks**.</span><span class="sxs-lookup"><span data-stu-id="21313-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, select **Select here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="21313-131">Valige **Avamine**.</span><span class="sxs-lookup"><span data-stu-id="21313-131">Select **Open**.</span></span> 
5. <span data-ttu-id="21313-132">Valige suvand **Sule**.</span><span class="sxs-lookup"><span data-stu-id="21313-132">Select **Close**.</span></span> 
6. <span data-ttu-id="21313-133">Valige elektroonilise aruandluse konfiguratsiooni sobiv versioon ja valige nupp **Impordi**, et viia see praegusesse eksemplari.</span><span class="sxs-lookup"><span data-stu-id="21313-133">Select the desired version of ER configuration and select **Import** to bring it in the current instance.</span></span>

