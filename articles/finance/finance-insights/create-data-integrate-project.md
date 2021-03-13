---
title: Andmeintegraatori projekti loomine (eelversioon)
description: See teema selgitab, kuidas luua andmeintegraatori projekti.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 0029e093f524c61ff17a480ee3b881b3994ba95a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009439"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="67849-103">Andmeintegraatori projekti loomine (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="67849-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="67849-104">See teema selgitab, kuidas luua andmeintegraatori projekti.</span><span class="sxs-lookup"><span data-stu-id="67849-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="67849-105">Rakenduse Microsoft Dynamics 365 Finance sisselogimine.</span><span class="sxs-lookup"><span data-stu-id="67849-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="67849-106">Minge jaotisse **Tööruumid \> Andmehaldus** ja valige suvand **Andmeüksused**.</span><span class="sxs-lookup"><span data-stu-id="67849-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="67849-107">Oodake, kuni kõik andmeüksused on värskendatud, enne kui liigute järgmisele etapile.</span><span class="sxs-lookup"><span data-stu-id="67849-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="67849-108">Avage [Power Appsi portaal](https://make.powerapps.com/) ja järgige järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="67849-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="67849-109">Valige sobiv keskkond.</span><span class="sxs-lookup"><span data-stu-id="67849-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="67849-110">Valige vasakpoolselt navigeerimispaanilt suvand **Andmed \> Ühendused**.</span><span class="sxs-lookup"><span data-stu-id="67849-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="67849-111">Looge ühendus järgmiste üksuste vastavate eksemplaridega.</span><span class="sxs-lookup"><span data-stu-id="67849-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="67849-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="67849-112">Dynamics 365</span></span>
        - <span data-ttu-id="67849-113">Dynamics 365 Findance and Operationsi jaoks</span><span class="sxs-lookup"><span data-stu-id="67849-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="67849-114">Avage [Power Appsi keskkonnad](https://admin.powerapps.com/environments) ja järgige järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="67849-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="67849-115">Valige **Andmeintegraator**.</span><span class="sxs-lookup"><span data-stu-id="67849-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="67849-116">Valige suvand **Ühenduskomplektid**.</span><span class="sxs-lookup"><span data-stu-id="67849-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="67849-117">Valige suvand **Uus ühenduskomplekt**.</span><span class="sxs-lookup"><span data-stu-id="67849-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="67849-118">Sisestage ühenduse nimi.</span><span class="sxs-lookup"><span data-stu-id="67849-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="67849-119">Valige järgmiste üksuste jaoks sobivad ühendused.</span><span class="sxs-lookup"><span data-stu-id="67849-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="67849-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="67849-120">Dynamics 365</span></span>
        - <span data-ttu-id="67849-121">Dynamics 365 Findance and Operationsi jaoks</span><span class="sxs-lookup"><span data-stu-id="67849-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="67849-122">Valige sobiv organisatsiooni vastendus.</span><span class="sxs-lookup"><span data-stu-id="67849-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="67849-123">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="67849-123">Select **Create**.</span></span>

5. <span data-ttu-id="67849-124">Avage [Power Appsi keskkonnad](https://admin.powerapps.com/environments) ja järgige järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="67849-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="67849-125">Looge järgmiste mallide jaoks andmeintegratsiooni projektid, kasutades äsja loodud ühenduse komplekti.</span><span class="sxs-lookup"><span data-stu-id="67849-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="67849-126">Kliendimakse ülevaadete tulemused (CDS-ist Finance and Operationsisse)</span><span class="sxs-lookup"><span data-stu-id="67849-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="67849-127">Rahavoo ajaseeria tulemid (CDS-ist Finance and Operationsisse)</span><span class="sxs-lookup"><span data-stu-id="67849-127">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="67849-128">Eelarve ajaseeria tulemid (CDS-ist Finance and Operationsisse)</span><span class="sxs-lookup"><span data-stu-id="67849-128">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="67849-129">Määrake igale projektile sobiv ajastamine.</span><span class="sxs-lookup"><span data-stu-id="67849-129">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="67849-130">Kui te nõutavaid üksusi CDS-is ei näe, avage suvand **Krediidihaldus ja võlanõuded > Seadistus > Finantsülevaated > Finantsülevaadete parameetrid**, lubage kliendimakse prognooside funktsioon ja klõpsake nuppu **Loo prognoosimise mudel**.</span><span class="sxs-lookup"><span data-stu-id="67849-130">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="67849-131">Kui AI-mudeli juurutamine on lõpetatud (edukas või nurjunud), juurutatakse CDS-is olemid, mis on vajalikud integratsiooni loomiseks.</span><span class="sxs-lookup"><span data-stu-id="67849-131">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="67849-132">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="67849-132">Privacy notice</span></span>

<span data-ttu-id="67849-133">Eelvaated 1) võivad kasutada vähem privaatsus- ja turbemeetmeid kui rakenduse Dynamics 365 Finance and Operations teenus; 2) ei ole hõlmatud selle teenuse teenusetaseme leppes; 3) ei tohi olla kasutusel isiklike andmete ega muude andmete töötlemiseks, mis on seaduste või määrustega kaitstud; 4) on piiratud toega.</span><span class="sxs-lookup"><span data-stu-id="67849-133">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
