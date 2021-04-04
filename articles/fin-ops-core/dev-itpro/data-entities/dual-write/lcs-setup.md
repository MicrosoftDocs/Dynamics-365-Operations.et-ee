---
title: Topeltkirjutuse häälestus teenustest Lifecycle Services
description: Selles teemas selgitatakse, kuidas häälestada topeltkirjutuse ühendust teenusest Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6971c8e2d5fa03c2991b9a3054c638cff6322c8b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567716"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="bdb55-103">Topeltkirjutuse häälestus teenustest Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="bdb55-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="bdb55-104">Selles teemas kirjeldatakse, kuidas seadistada topeltkirjutust uue Finance and Operationsi ja uue Dataverse'i keskkonna vahel teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu.</span><span class="sxs-lookup"><span data-stu-id="bdb55-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Dataverse environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bdb55-105">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="bdb55-105">Prerequisites</span></span>

<span data-ttu-id="bdb55-106">Topeltkirjutuse ühenduse seadistamiseks peate olema administraator.</span><span class="sxs-lookup"><span data-stu-id="bdb55-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="bdb55-107">Teil peab olema juurdepääs rentnikule.</span><span class="sxs-lookup"><span data-stu-id="bdb55-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="bdb55-108">Peate olema administraator nii Finance and Operationsi kui ka Dataverse'i keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="bdb55-108">You must be an admin in both Finance and Operations environments and Dataverse environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="bdb55-109">Topeltkirjutuse ühenduse seadistamine</span><span class="sxs-lookup"><span data-stu-id="bdb55-109">Set up a dual-write connection</span></span>

<span data-ttu-id="bdb55-110">Topeltkirjutuse ühenduse seadistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="bdb55-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="bdb55-111">Avage LCS-is oma projekt.</span><span class="sxs-lookup"><span data-stu-id="bdb55-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="bdb55-112">Uue keskkonna juurutamiseks valige **Konfigureeri**.</span><span class="sxs-lookup"><span data-stu-id="bdb55-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="bdb55-113">Valige versioon.</span><span class="sxs-lookup"><span data-stu-id="bdb55-113">Select the version.</span></span> 
4. <span data-ttu-id="bdb55-114">Valige topoloogia.</span><span class="sxs-lookup"><span data-stu-id="bdb55-114">Select the topology.</span></span> <span data-ttu-id="bdb55-115">Kui saadaval on ainult üks topoloogia, valitakse see automaatselt.</span><span class="sxs-lookup"><span data-stu-id="bdb55-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="bdb55-116">Viige lõpule esimesed toimingud viisardis **Juurutussätted**.</span><span class="sxs-lookup"><span data-stu-id="bdb55-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="bdb55-117">Vahekaardil **Dataverse** järgige ühte järgnevatest toimingutest.</span><span class="sxs-lookup"><span data-stu-id="bdb55-117">On the **Dataverse** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="bdb55-118">Kui teie rentniku jaoks on Dataverse'i keskkond juba ette valmistatud, saate selle valida.</span><span class="sxs-lookup"><span data-stu-id="bdb55-118">If a Dataverse environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="bdb55-119">Määrake suvandi **Dataverse'i konfigureerimine** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="bdb55-119">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="bdb55-120">Veerus **Saadaolevad keskkonnad** valige oma Finance and Operationsi andmetega integreeritav keskkond.</span><span class="sxs-lookup"><span data-stu-id="bdb55-120">In the **Available environments** column, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="bdb55-121">Loend hõlmab kõiki keskkondi, kus teil on administraatori privileegid.</span><span class="sxs-lookup"><span data-stu-id="bdb55-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="bdb55-122">Tingimustega nõustumise näitamiseks märkige ruut **Nõustu**.</span><span class="sxs-lookup"><span data-stu-id="bdb55-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Vahekaart Dataverse, kui teie rentniku jaoks on 'Dataversei keskkond juba ette valmistatud](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="bdb55-124">Kui teie rentnikul ei ole veel Dataverse'i keskkonda, luuakse uus keskkond.</span><span class="sxs-lookup"><span data-stu-id="bdb55-124">If your tenant doesn't already have a Dataverse environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="bdb55-125">Määrake suvandi **Dataverse'i konfigureerimine** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="bdb55-125">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="bdb55-126">Sisestage Dataverse'i keskkonnale nimi.</span><span class="sxs-lookup"><span data-stu-id="bdb55-126">Enter a name for the Dataverse environment.</span></span>
        3. <span data-ttu-id="bdb55-127">Valige keskkonna juurutamise piirkond.</span><span class="sxs-lookup"><span data-stu-id="bdb55-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="bdb55-128">Valida keskkonna vaikekeel ja -valuuta.</span><span class="sxs-lookup"><span data-stu-id="bdb55-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="bdb55-129">Keelt ja valuutat ei saa hiljem muuta.</span><span class="sxs-lookup"><span data-stu-id="bdb55-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="bdb55-130">Tingimustega nõustumise näitamiseks märkige ruut **Nõustu**.</span><span class="sxs-lookup"><span data-stu-id="bdb55-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Vahekaart Dataverse, kui teie rentnikul ei ole veel Dataverse'i keskkonda](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="bdb55-132">Viige lõpule järelejäänud toimingud viisardis **Juurutussätted**.</span><span class="sxs-lookup"><span data-stu-id="bdb55-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="bdb55-133">Kui keskkonna olekuks on **Juurutatud**, avage keskkonna üksikasjade leht.</span><span class="sxs-lookup"><span data-stu-id="bdb55-133">After the environment has a status of **Deployed**, open the environment details page.</span></span> <span data-ttu-id="bdb55-134">Jaotises **Power Platformi integreerimine** kuvatakse lingitud Finance and Operationsi ja Dataverse’i keskkonna nimed.</span><span class="sxs-lookup"><span data-stu-id="bdb55-134">The **Power Platform Integration** section shows the names of the Finance and Operations environment and the Dataverse environment that are linked.</span></span>

    ![Power Platformi integreerimise jaotis](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="bdb55-136">Keskkonna Finance and Operations administraator peab linkimise lõpule viimiseks logima sisse LCS-i ja valima **Lingi CDS rakendustele**.</span><span class="sxs-lookup"><span data-stu-id="bdb55-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="bdb55-137">Keskkonna üksikasjade lehel kuvatakse administraatori kontaktteave.</span><span class="sxs-lookup"><span data-stu-id="bdb55-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="bdb55-138">Kui linkimine on lõpule viidud, uuendatakse olekuks **Keskonna linkimine on edukalt lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="bdb55-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="bdb55-139">Tööruumi **Andmete integratsioon** avamiseks Finance and Operationsi keskkonnas ja saadaolevate mallide juhtimiseks valige **Lingi CDS rakendustele**.</span><span class="sxs-lookup"><span data-stu-id="bdb55-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![Nupp Lingi CDS rakendustele Power Platformi teabe jaotises](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="bdb55-141">LCS-i abil ei saa keskkondade linkimist tühistada.</span><span class="sxs-lookup"><span data-stu-id="bdb55-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="bdb55-142">Keskkonna linkimise tühistamiseks avage tööruum **Andmete integratsioon** keskkonnas Finance and Operations ja seejärel valige käsk **Tühista linkimine**.</span><span class="sxs-lookup"><span data-stu-id="bdb55-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]