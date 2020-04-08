---
title: Kaksikkirjutamise seadistuse toetatud stsenaariumid
description: Selle teema all kirjeldatakse stsenaariume, mida toetatakse kaksikkirjutamise seadistuseks.
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
ms.openlocfilehash: d7ff514768ee8e4797b591da89e190a855385885
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172850"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="22b9a-103">Kaksikkirjutamise seadistuse toetatud stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="22b9a-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="22b9a-104">Saate seadistada kaksikkirjutamise seose Finance and Operations keskkonna ja Common Data Service keskkonna vahel.</span><span class="sxs-lookup"><span data-stu-id="22b9a-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="22b9a-105">**Finance and Operations keskkond** pakub platvormi **Finance and Operations rakendustele** (nt Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail ja Dynamics 365 Human Resources).</span><span class="sxs-lookup"><span data-stu-id="22b9a-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="22b9a-106">**Common Data Service keskkond** loob aluseks oleva platvormi **mudeljuhitud Dynamics 365 rakenduste** jaoks (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing ja Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="22b9a-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

<span data-ttu-id="22b9a-107">Seadistuse mehhanism erineb sõltuvalt teie tellimusest ja keskkonnast.</span><span class="sxs-lookup"><span data-stu-id="22b9a-107">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="22b9a-108">Uute Finance and Operations rakenduste puhul algab kaksikkirjutamise ühenduse seadistus Microsoft Dynamics Lifecycle Servicesiga (LCS).</span><span class="sxs-lookup"><span data-stu-id="22b9a-108">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="22b9a-109">Kui teil on Microsoft Power Platformi litsents, saate uue Common Data Service'i keskkonna, kui teie rentnikul seda ei ole.</span><span class="sxs-lookup"><span data-stu-id="22b9a-109">If you have a license for Microsoft Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="22b9a-110">Olemasolevate Finance and Operations rakenduste puhul algab kaksikkirjutamise ühenduse seadistus Finance and Operations keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="22b9a-110">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="22b9a-111">Toetatud on järgmised seadistusstsenaariumid:</span><span class="sxs-lookup"><span data-stu-id="22b9a-111">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="22b9a-112">Uus Finance and Operations rakenduse eksemplar ja uus mudeljuhitud rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="22b9a-112">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="22b9a-113">Uus Finance and Operations rakenduse eksemplar ja olemasoleva mudeljuhitud rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="22b9a-113">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="22b9a-114">Uus Finance and Operations rakenduse eksemplar, millel on demoandmed, ja uus mudeljuhitud rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="22b9a-114">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="22b9a-115">Uus Finance and Operations rakenduse eksemplar, millel on demoandmed, ja olemasolev mudeljuhitud rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="22b9a-115">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="22b9a-116">Olemasolev Finance and Operations rakenduse eksemplar ja uus või olemasolev mudeljuhitud rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="22b9a-116">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="22b9a-117">Uus Finance and Operations rakenduse eksemplar ja uus mudeljuhitud rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="22b9a-117">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="22b9a-118">Kaksikkirjutamise ühenduse seadmiseks Finance and Operations rakenduse uue eksemplari, millel puuduvad andmed ja uue mudeljuhitud rakenduse eksemplari vahel rakenduses Dynamics 365 järgige [Kaksikkirjutamise seadistuse teenuse Lifecycle Services etappe](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="22b9a-118">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="22b9a-119">Kui ühenduse seadistus on lõpule viidud, toimuvad automaatselt järgmised toimingud:</span><span class="sxs-lookup"><span data-stu-id="22b9a-119">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="22b9a-120">Valmistatakse ette uus tühi Finance and Operations keskkond.</span><span class="sxs-lookup"><span data-stu-id="22b9a-120">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="22b9a-121">On ette valmistatud mudeljuhitud rakenduse uus tühi eksemplar, kus on installitud CRM pealahendus.</span><span class="sxs-lookup"><span data-stu-id="22b9a-121">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="22b9a-122">Kaksikkirjutamise ühendus on loodud DAT-ettevõtte andmetele.</span><span class="sxs-lookup"><span data-stu-id="22b9a-122">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="22b9a-123">Üksuse vastendused on lubatud reaalajas sünkroonimiseks.</span><span class="sxs-lookup"><span data-stu-id="22b9a-123">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="22b9a-124">Mõlemad keskkonnad on seejärel valmis reaalaja andmete sünkroonimiseks.</span><span class="sxs-lookup"><span data-stu-id="22b9a-124">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a><span data-ttu-id="22b9a-125">Uus Finance and Operations rakenduse eksemplar ja olemasoleva mudeljuhitud rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="22b9a-125">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="22b9a-126">Kaksikkirjutamise ühenduse seadmiseks Finance and Operations rakenduse uue eksemplari, millel puuduvad andmed ja olemasoleva mudeljuhitud rakenduse eksemplari vahel rakenduses Dynamics 365 järgige [Kaksikkirjutamise seadistuse Lifecycle Servicesi etappe](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="22b9a-126">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="22b9a-127">Kui ühenduse seadistus on lõpule viidud, toimuvad automaatselt järgmised toimingud:</span><span class="sxs-lookup"><span data-stu-id="22b9a-127">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="22b9a-128">Valmistatakse ette uus tühi Finance and Operations keskkond.</span><span class="sxs-lookup"><span data-stu-id="22b9a-128">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="22b9a-129">Kaksikkirjutamise ühendus on loodud DAT-ettevõtte andmetele.</span><span class="sxs-lookup"><span data-stu-id="22b9a-129">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="22b9a-130">Üksuse vastendused on lubatud reaalajas sünkroonimiseks.</span><span class="sxs-lookup"><span data-stu-id="22b9a-130">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="22b9a-131">Mõlemad keskkonnad on seejärel valmis reaalaja andmete sünkroonimiseks.</span><span class="sxs-lookup"><span data-stu-id="22b9a-131">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="22b9a-132">Olemasolevate Common Data Service andmete sünkroonimiseks Finance and Operations rakendusega toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="22b9a-132">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="22b9a-133">Looge Finance and Operations rakenduses uus ettevõte.</span><span class="sxs-lookup"><span data-stu-id="22b9a-133">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="22b9a-134">Lisage ettevõte kaksikkirjutamise ühenduse seadistusse.</span><span class="sxs-lookup"><span data-stu-id="22b9a-134">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="22b9a-135">Rakendage[Bootstrap](bootstrap-company-data.md) Common Data Service andmetele, kasutades kolmetähelist Rahvusvahelise standardiorganisatsiooni (ISO) ettevõttekoodi.</span><span class="sxs-lookup"><span data-stu-id="22b9a-135">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="22b9a-136">Kuna kaksikkirjutamine on reaalajas sünkroonimise režiimis, hakkavad Common Data Service andmed automaatselt liikuma Finance and Operations rakendusse.</span><span class="sxs-lookup"><span data-stu-id="22b9a-136">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a><span data-ttu-id="22b9a-137">Uus Finance and Operations rakenduse eksemplar, millel on demoandmed, ja uus mudeljuhitud rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="22b9a-137">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="22b9a-138">Kaksikkirjutamise seose seadistamiseks Finance and Operations rakenduse uue eksemplari, millel on demoandmed, ja mudeljuhitud rakenduse uus eksemplari vahel rakenduses Dynamics 365 järgige selles teema all varem kirjeldatud etappe jaotises [Uus Finance and Operations rakenduse eksemplar ja uus mudeljuhitud rakenduse eksemplar](#new-new) .</span><span class="sxs-lookup"><span data-stu-id="22b9a-138">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="22b9a-139">Kui ühenduse häälestus on lõpule viidud, kui soovite demoandmeid sünkroonida mudeljuhitud rakendusega, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="22b9a-139">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="22b9a-140">Avage Finance and Operations rakendus LCS lehelt, logige sisse ja seejärel avage **Andmehaldus \> Kaksikkirjutamine**.</span><span class="sxs-lookup"><span data-stu-id="22b9a-140">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="22b9a-141">Käivitage **Esmase sünkroonimise** funktsionaalsus üksustel, millele soovite andmeid sünkroonida.</span><span class="sxs-lookup"><span data-stu-id="22b9a-141">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a><span data-ttu-id="22b9a-142">Uus Finance and Operations rakenduse eksemplar, millel on demoandmed, ja olemasolev mudeljuhitud rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="22b9a-142">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="22b9a-143">Kaksikkirjutamise seose seadistamiseks Finance and Operations rakenduse uue eksemplari, millel on demoandmed, ja mudeljuhitud rakenduse olemasoleva eksemplari vahel rakenduses Dynamics 365 järgige selles teema all varem kirjeldatud etappe jaotises [Uus Finance and Operations rakenduse eksemplar ja olemasolev mudeljuhitud rakenduse eksemplar](#new-existing) .</span><span class="sxs-lookup"><span data-stu-id="22b9a-143">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="22b9a-144">Kui ühenduse häälestus on lõpule viidud, kui soovite demoandmeid sünkroonida mudeljuhitud rakendusega, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="22b9a-144">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="22b9a-145">Avage Finance and Operations rakendus LCS lehelt, logige sisse ja seejärel avage **Andmehaldus \> Kaksikkirjutamine**.</span><span class="sxs-lookup"><span data-stu-id="22b9a-145">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="22b9a-146">Käivitage **Esmase sünkroonimise** funktsionaalsus üksustel, millele soovite andmeid sünkroonida.</span><span class="sxs-lookup"><span data-stu-id="22b9a-146">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="22b9a-147">Olemasolevate Common Data Service andmete sünkroonimiseks Finance and Operations rakendusega toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="22b9a-147">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="22b9a-148">Looge Finance and Operations rakenduses uus ettevõte.</span><span class="sxs-lookup"><span data-stu-id="22b9a-148">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="22b9a-149">Lisage ettevõte kaksikkirjutamise ühenduse seadistusse.</span><span class="sxs-lookup"><span data-stu-id="22b9a-149">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="22b9a-150">Rakendage[Bootstrap](bootstrap-company-data.md) Common Data Service andmetele, kasutades kolmetähelist Rahvusvahelise standardiorganisatsiooni (ISO) ettevõttekoodi.</span><span class="sxs-lookup"><span data-stu-id="22b9a-150">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="22b9a-151">Kuna kaksikkirjutamine on reaalajas sünkroonimise režiimis, hakkavad Common Data Service andmed automaatselt liikuma Finance and Operations rakendusse.</span><span class="sxs-lookup"><span data-stu-id="22b9a-151">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="22b9a-152">Olemasolev Finance and Operations rakenduse eksemplar ja uus või olemasolev mudeljuhitud rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="22b9a-152">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="22b9a-153">Olemasoleva Finance and Operations rakenduse eksemplari ja rakenduses Dynamics 365 mudeljuhitud rakenduse uue või olemasoleva eksemplari vahelise ühenduse kaksikkirjutamise seadistus toimub Finants-ja töökeskkonnas.</span><span class="sxs-lookup"><span data-stu-id="22b9a-153">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="22b9a-154">Seadistage ühendus Finance and Operations rakendusest.</span><span class="sxs-lookup"><span data-stu-id="22b9a-154">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="22b9a-155">Olemasolevate Common Data Service andmete Finance and Operations rakendusega sünkroonimiseks rakendage [bootstrap](bootstrap-company-data.md) Common Data Service andmetele, kasutades kolmetähelist ettevõtte ISO-koodi.</span><span class="sxs-lookup"><span data-stu-id="22b9a-155">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="22b9a-156">Kuna kaksikkirjutamine on reaalajas sünkroonimise režiimis, hakkavad Common Data Service andmed automaatselt liikuma Finance and Operations rakendusse.</span><span class="sxs-lookup"><span data-stu-id="22b9a-156">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
