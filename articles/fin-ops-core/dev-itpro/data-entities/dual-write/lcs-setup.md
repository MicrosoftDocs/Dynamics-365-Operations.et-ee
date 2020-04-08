---
title: Topeltkirjutuse seadistamine teenuses Lifecycle Services
description: Selles teemas kirjeldatakse, kuidas seadistada topeltkirjutust uue Finance and Operationsi ja uue Common Data Service'i keskkonna vahel teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c78752aa1544b12f61071fa06617af4ac2809233
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172988"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="319b8-103">Topeltkirjutuse seadistamine teenuses Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="319b8-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="319b8-104">Selles teemas kirjeldatakse, kuidas seadistada topeltkirjutust uue Finance and Operationsi ja uue Common Data Service'i keskkonna vahel teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu.</span><span class="sxs-lookup"><span data-stu-id="319b8-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Common Data Service environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="319b8-105">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="319b8-105">Prerequisites</span></span>

<span data-ttu-id="319b8-106">Topeltkirjutuse ühenduse seadistamiseks peate olema administraator.</span><span class="sxs-lookup"><span data-stu-id="319b8-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="319b8-107">Teil peab olema juurdepääs rentnikule.</span><span class="sxs-lookup"><span data-stu-id="319b8-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="319b8-108">Peate olema administraator nii Finance and Operationsi kui ka Common Data Service'i keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="319b8-108">You must be an admin in both Finance and Operations environments and Common Data Service environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="319b8-109">Topeltkirjutuse ühenduse seadistamine</span><span class="sxs-lookup"><span data-stu-id="319b8-109">Set up a dual-write connection</span></span>

<span data-ttu-id="319b8-110">Topeltkirjutuse ühenduse seadistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="319b8-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="319b8-111">Avage LCS-is oma projekt.</span><span class="sxs-lookup"><span data-stu-id="319b8-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="319b8-112">Uue keskkonna juurutamiseks valige **Konfigureeri**.</span><span class="sxs-lookup"><span data-stu-id="319b8-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="319b8-113">Valige versioon.</span><span class="sxs-lookup"><span data-stu-id="319b8-113">Select the version.</span></span> 
4. <span data-ttu-id="319b8-114">Valige topoloogia.</span><span class="sxs-lookup"><span data-stu-id="319b8-114">Select the topology.</span></span> <span data-ttu-id="319b8-115">Kui saadaval on ainult üks topoloogia, valitakse see automaatselt.</span><span class="sxs-lookup"><span data-stu-id="319b8-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="319b8-116">Viige lõpule esimesed toimingud viisardis **Juurutussätted**.</span><span class="sxs-lookup"><span data-stu-id="319b8-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="319b8-117">Vahekaardil **Common Data Service** järgige ühte järgnevatest toimingutest.</span><span class="sxs-lookup"><span data-stu-id="319b8-117">On the **Common Data Service** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="319b8-118">Kui teie rentniku jaoks on Common Data Service'i keskkond juba ette valmistatud, saate selle valida.</span><span class="sxs-lookup"><span data-stu-id="319b8-118">If a Common Data Service environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="319b8-119">Määrake suvandi **Common Data Service'i konfigureerimine** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="319b8-119">Set the **Configure Common Data Service** option to **Yes**.</span></span>
        2. <span data-ttu-id="319b8-120">Väljal **Saadaolevad keskkonnad** valige oma Finance and Operationsi andmetega integreeritav keskkond.</span><span class="sxs-lookup"><span data-stu-id="319b8-120">In the **Available environments** field, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="319b8-121">Loend hõlmab kõiki keskkondi, kus teil on administraatori privileegid.</span><span class="sxs-lookup"><span data-stu-id="319b8-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="319b8-122">Tingimustega nõustumise näitamiseks märkige ruut **Nõustu**.</span><span class="sxs-lookup"><span data-stu-id="319b8-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Vahekaart Common Data Service, kui teie rentniku jaoks on 'Common Data Servicei keskkond juba ette valmistatud](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="319b8-124">Kui teie rentnikul ei ole veel Common Data Service'i keskkonda, luuakse uus keskkond.</span><span class="sxs-lookup"><span data-stu-id="319b8-124">If your tenant doesn't already have a Common Data Service environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="319b8-125">Määrake suvandi **Common Data Service'i konfigureerimine** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="319b8-125">Set the **Configure Common Data Service** option to **Yes**.</span></span>
        2. <span data-ttu-id="319b8-126">Sisestage Common Data Service'i keskkonnale nimi.</span><span class="sxs-lookup"><span data-stu-id="319b8-126">Enter a name for the Common Data Service environment.</span></span>
        3. <span data-ttu-id="319b8-127">Valige keskkonna juurutamise piirkond.</span><span class="sxs-lookup"><span data-stu-id="319b8-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="319b8-128">Valida keskkonna vaikekeel ja -valuuta.</span><span class="sxs-lookup"><span data-stu-id="319b8-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="319b8-129">Keelt ja valuutat ei saa hiljem muuta.</span><span class="sxs-lookup"><span data-stu-id="319b8-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="319b8-130">Tingimustega nõustumise näitamiseks märkige ruut **Nõustu**.</span><span class="sxs-lookup"><span data-stu-id="319b8-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Vahekaart Common Data Service, kui teie rentnikul ei ole veel Common Data Service'i keskkonda](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="319b8-132">Viige lõpule järelejäänud toimingud viisardis **Juurutussätted**.</span><span class="sxs-lookup"><span data-stu-id="319b8-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="319b8-133">Kui keskkonna olekuks on **Juurutatud**, avage keskkonna üksikasjade leht.</span><span class="sxs-lookup"><span data-stu-id="319b8-133">After the environment has a status of **Deployed**, open the environment details page.</span></span> <span data-ttu-id="319b8-134">Jaotises **Common Data Service'i keskkonna teave** kuvatakse lingitud Finance and Operationsi ja Common Data Service'i keskkonna nimed.</span><span class="sxs-lookup"><span data-stu-id="319b8-134">The **Common Data Service environment information** section shows the names of the Finance and Operations environment and the Common Data Service environment that are linked.</span></span>

    ![Common Data Service keskkonna teabe jaotis](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="319b8-136">Keskkonna Finance and Operations administraator peab linkimise lõpule viimiseks logima sisse LCS-i ja valima **Lingi CDS rakendustele**.</span><span class="sxs-lookup"><span data-stu-id="319b8-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="319b8-137">Keskkonna üksikasjade lehel kuvatakse administraatori kontaktteave.</span><span class="sxs-lookup"><span data-stu-id="319b8-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="319b8-138">Kui linkimine on lõpule viidud, uuendatakse olekuks **Keskonna linkimine on edukalt lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="319b8-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="319b8-139">Tööruumi **Andmete integratsioon** avamiseks Finance and Operationsi keskkonnas ja saadaolevate mallide juhtimiseks valige **Lingi CDS rakendustele**.</span><span class="sxs-lookup"><span data-stu-id="319b8-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![Nupp Lingi CDS rakendusele keskkonna Common Data Service teabe jaotises](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="319b8-141">LCS-i abil ei saa keskkondade linkimist tühistada.</span><span class="sxs-lookup"><span data-stu-id="319b8-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="319b8-142">Keskkonna linkimise tühistamiseks avage tööruum **Andmete integratsioon** keskkonnas Finance and Operations ja seejärel valige käsk **Tühista linkimine**.</span><span class="sxs-lookup"><span data-stu-id="319b8-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>
