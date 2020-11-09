---
title: Juhised topeltkirjutuse häälestamiseks
description: Selle teema all kirjeldatakse stsenaariume, mida toetatakse kaksikkirjutamise seadistuseks.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 2d77a1458f3f4c79b231e6a6d7cc320b8ee1fad9
ms.sourcegitcommit: ee643d651d57560bccae2f99238faa39881f5c64
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088502"
---
# <a name="guidance-for-how-to-set-up-dual-write"></a><span data-ttu-id="22900-103">Juhised topeltkirjutuse häälestamiseks</span><span class="sxs-lookup"><span data-stu-id="22900-103">Guidance for how to set up dual-write</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="22900-104">Saate seadistada kaksikkirjutamise seose Finance and Operations keskkonna ja Common Data Service keskkonna vahel.</span><span class="sxs-lookup"><span data-stu-id="22900-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="22900-105">**Finance and Operationsi keskkond** pakub platvormi **Finance and Operationsi rakendustele** (nt Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management ja Dynamics 365 Retail).</span><span class="sxs-lookup"><span data-stu-id="22900-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Retail).</span></span>
+ <span data-ttu-id="22900-106">**Common Data Service'i keskkond** loob aluseks oleva platvormi **rakendustekomplekti Customer Engagement** jaoks (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing ja Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="22900-106">A **Common Data Service environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

>[!IMPORTANT]
><span data-ttu-id="22900-107">Finance and Operationsi rakendus Human Resources toetab topeltkirjutuse ühendusi, kuid rakendus Dynamics 365 Human Resources ei luba seda.</span><span class="sxs-lookup"><span data-stu-id="22900-107">Human Resources in Finance and Operations supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="22900-108">Seadistuse mehhanism erineb sõltuvalt teie tellimusest ja keskkonnast.</span><span class="sxs-lookup"><span data-stu-id="22900-108">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="22900-109">Uute Finance and Operations rakenduste puhul algab kaksikkirjutamise ühenduse seadistus Microsoft Dynamics Lifecycle Servicesiga (LCS).</span><span class="sxs-lookup"><span data-stu-id="22900-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="22900-110">Kui teil on Power Platformi litsents, saate uue Common Data Service'i keskkonna, kui teie rentnikul seda ei ole.</span><span class="sxs-lookup"><span data-stu-id="22900-110">If you have a license for Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="22900-111">Olemasolevate Finance and Operations rakenduste puhul algab kaksikkirjutamise ühenduse seadistus Finance and Operations keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="22900-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="22900-112">Enne kui käivitate üksuse topeltkirjutuse, saate käitada algse sünkroonimise, et hallata olemasolevaid andmeid Finance and Operationsi ja Customer Engagementi rakenduste mõlemal poolel.</span><span class="sxs-lookup"><span data-stu-id="22900-112">Before you start dual-write on an entity, you can run an initial sync to handle existing data on both sides of Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="22900-113">Kui te ei pea nende kahe keskkonna vahel andmeid sünkroonima, saate algse sünkroonimise vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="22900-113">You can skip the initial sync if you don't need to synchronize data between the two environments.</span></span>

<span data-ttu-id="22900-114">Algse sünkroonimisega saate kopeerida olemasolevad andmed kahesuunaliselt ühest rakendusest teise.</span><span class="sxs-lookup"><span data-stu-id="22900-114">An initial sync lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="22900-115">Sõltuvalt sellest, millised keskkonnad teil on olemas ja millist tüüpi andmeid on nendes keskkondades, on mitu erinevat seadistuse stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="22900-115">There are several different setup scenarios depending on which environments you already have and what type of data is in the environments.</span></span>

<span data-ttu-id="22900-116">Toetatud on järgmised seadistusstsenaariumid:</span><span class="sxs-lookup"><span data-stu-id="22900-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="22900-117">Uus Finance and Operationsi rakenduse eksemplar ja uus Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="22900-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="22900-118">Uus Finance and Operationsi rakenduse eksemplar ja olemasolev Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="22900-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="22900-119">Uus Finance and Operationsi rakenduse eksemplar, millel on andmed, ja uus Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="22900-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="22900-120">Uus Finance and Operationsi rakenduse eksemplar, millel on andmed, ja olemasolev Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="22900-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="22900-121">Olemasolev Finance and Operationsi rakenduse eksemplar ja uus Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="22900-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="22900-122">Olemasolev Finance and Operationsi rakenduse eksemplar ja olemasolev Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="22900-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="22900-123">Uus Finance and Operationsi rakenduse eksemplar ja uus Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="22900-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="22900-124">Topeltkirjutuse ühenduse seadmiseks Finance and Operationsi rakenduse uue eksemplari, millel puuduvad andmed, ja Customer Engagementi rakenduse uue eksemplari vahel, järgige etappe jaotises [Topeltkirjutuse seadistus teenuses Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="22900-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="22900-125">Kui ühenduse seadistus on lõpule viidud, toimuvad automaatselt järgmised toimingud:</span><span class="sxs-lookup"><span data-stu-id="22900-125">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="22900-126">Valmistatakse ette uus tühi Finance and Operations keskkond.</span><span class="sxs-lookup"><span data-stu-id="22900-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="22900-127">On ette valmistatud Customer Engagementi rakenduse uus tühi eksemplar, kus on installitud CRM-i pealahendus.</span><span class="sxs-lookup"><span data-stu-id="22900-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="22900-128">Kaksikkirjutamise ühendus on loodud DAT-ettevõtte andmetele.</span><span class="sxs-lookup"><span data-stu-id="22900-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="22900-129">Üksuse vastendused on lubatud reaalajas sünkroonimiseks.</span><span class="sxs-lookup"><span data-stu-id="22900-129">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="22900-130">Mõlemad keskkonnad on seejärel valmis reaalaja andmete sünkroonimiseks.</span><span class="sxs-lookup"><span data-stu-id="22900-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="22900-131">Uus Finance and Operationsi rakenduse eksemplar ja olemasolev Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="22900-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="22900-132">Topeltkirjutuse ühenduse seadmiseks Finance and Operationsi rakenduse uude eksemplari, millel puuduvad andmed, ja olemasoleva Customer Engagementi rakenduse eksemplari vahel, järgige etappe jaotises [Topeltkirjutuse seadistus teenuses Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="22900-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="22900-133">Kui ühenduse seadistus on lõpule viidud, toimuvad automaatselt järgmised toimingud:</span><span class="sxs-lookup"><span data-stu-id="22900-133">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="22900-134">Valmistatakse ette uus tühi Finance and Operations keskkond.</span><span class="sxs-lookup"><span data-stu-id="22900-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="22900-135">Kaksikkirjutamise ühendus on loodud DAT-ettevõtte andmetele.</span><span class="sxs-lookup"><span data-stu-id="22900-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="22900-136">Üksuse vastendused on lubatud reaalajas sünkroonimiseks.</span><span class="sxs-lookup"><span data-stu-id="22900-136">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="22900-137">Mõlemad keskkonnad on seejärel valmis reaalaja andmete sünkroonimiseks.</span><span class="sxs-lookup"><span data-stu-id="22900-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="22900-138">Olemasolevate Common Data Service andmete sünkroonimiseks Finance and Operations rakendusega toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="22900-138">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="22900-139">Looge Finance and Operations rakenduses uus ettevõte.</span><span class="sxs-lookup"><span data-stu-id="22900-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="22900-140">Lisage ettevõte kaksikkirjutamise ühenduse seadistusse.</span><span class="sxs-lookup"><span data-stu-id="22900-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="22900-141">Rakendage[Bootstrap](bootstrap-company-data.md) Common Data Service andmetele, kasutades kolmetähelist Rahvusvahelise standardiorganisatsiooni (ISO) ettevõttekoodi.</span><span class="sxs-lookup"><span data-stu-id="22900-141">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="22900-142">Käivitage **Esmase sünkroonimise** funktsionaalsus üksustel, millele soovite andmeid sünkroonida.</span><span class="sxs-lookup"><span data-stu-id="22900-142">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="22900-143">Näite ja alternatiivse lähenemise saamiseks vt [Näide](#example).</span><span class="sxs-lookup"><span data-stu-id="22900-143">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="22900-144">Uus Finance and Operationsi rakenduse eksemplar, millel on andmed, ja uus Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="22900-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="22900-145">Topeltkirjutuse seose seadistamiseks Finance and Operationsi rakenduse uue eksemplari, millel on andmed, ja Customer Engagementi rakenduse uue eksemplari vahel, järgige selle teema all varem kirjeldatud etappe jaotises [Uus Finance and Operationsi rakenduse eksemplar ja uus Customer Engagementi rakenduse eksemplar](#new-new) .</span><span class="sxs-lookup"><span data-stu-id="22900-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="22900-146">Kui ühenduse häälestus on lõpule viidud, kui soovite andmeid sünkroonida Customer Engagementi rakendusega, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="22900-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="22900-147">Avage Finance and Operations rakendus LCS lehelt, logige sisse ja seejärel avage **Andmehaldus \> Kaksikkirjutamine**.</span><span class="sxs-lookup"><span data-stu-id="22900-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="22900-148">Käivitage **Esmase sünkroonimise** funktsionaalsus üksustel, millele soovite andmeid sünkroonida.</span><span class="sxs-lookup"><span data-stu-id="22900-148">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="22900-149">Näite ja alternatiivse lähenemise saamiseks vt [Näide](#example).</span><span class="sxs-lookup"><span data-stu-id="22900-149">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="22900-150">Uus Finance and Operationsi rakenduse eksemplar, millel on andmed, ja olemasolev Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="22900-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="22900-151">Topeltkirjutuse seose seadistamiseks Finance and Operationsi rakenduse uue eksemplari, millel on andmed, ja Customer Engagementi rakenduse olemasoleva eksemplari vahel, järgige selle teema all varem kirjeldatud etappe jaotises [Uus Finance and Operationsi rakenduse eksemplar ja olemasolev Customer Engagementi rakenduse eksemplar](#new-existing) .</span><span class="sxs-lookup"><span data-stu-id="22900-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="22900-152">Kui ühenduse häälestus on lõpule viidud, kui soovite andmeid sünkroonida Customer Engagementi rakendusega, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="22900-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="22900-153">Avage Finance and Operations rakendus LCS lehelt, logige sisse ja seejärel avage **Andmehaldus \> Kaksikkirjutamine**.</span><span class="sxs-lookup"><span data-stu-id="22900-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="22900-154">Käivitage **Esmase sünkroonimise** funktsionaalsus üksustel, millele soovite andmeid sünkroonida.</span><span class="sxs-lookup"><span data-stu-id="22900-154">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="22900-155">Olemasolevate Common Data Service andmete sünkroonimiseks Finance and Operations rakendusega toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="22900-155">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="22900-156">Looge Finance and Operations rakenduses uus ettevõte.</span><span class="sxs-lookup"><span data-stu-id="22900-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="22900-157">Lisage ettevõte kaksikkirjutamise ühenduse seadistusse.</span><span class="sxs-lookup"><span data-stu-id="22900-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="22900-158">Rakendage[Bootstrap](bootstrap-company-data.md) Common Data Service andmetele, kasutades kolmetähelist Rahvusvahelise standardiorganisatsiooni (ISO) ettevõttekoodi.</span><span class="sxs-lookup"><span data-stu-id="22900-158">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="22900-159">Käivitage **Esmase sünkroonimise** funktsionaalsus üksustel, millele soovite andmeid sünkroonida.</span><span class="sxs-lookup"><span data-stu-id="22900-159">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="22900-160">Näite ja alternatiivse lähenemise saamiseks vt [Näide](#example).</span><span class="sxs-lookup"><span data-stu-id="22900-160">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="22900-161">Olemasolev Finance and Operationsi rakenduse eksemplar ja uus Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="22900-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="22900-162">Olemasoleva Finance and Operationsi rakenduse eksemplari ja uue Customer Engagementi rakenduse eksemplari vahelise ühenduse topeltkirjutuse seadistus toimub keskkonnas Finance and Operation.</span><span class="sxs-lookup"><span data-stu-id="22900-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="22900-163">[Seadistage ühendus Finance and Operationsi rakendusest](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="22900-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="22900-164">Käivitage **Esmase sünkroonimise** funktsionaalsus üksustel, millele soovite andmeid sünkroonida.</span><span class="sxs-lookup"><span data-stu-id="22900-164">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="22900-165">Näite ja alternatiivse lähenemise saamiseks vt [Näide](#example).</span><span class="sxs-lookup"><span data-stu-id="22900-165">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="22900-166">Olemasolev Finance and Operationsi rakenduse eksemplar ja olemasolev Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="22900-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="22900-167">Olemasoleva Finance and Operationsi rakenduse eksemplari ja olemasoleva Customer Engagementi rakenduse eksemplari vahelise ühenduse topeltkirjutuse seadistus toimub keskkonnas Finance and Operation.</span><span class="sxs-lookup"><span data-stu-id="22900-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app  occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="22900-168">Seadistage ühendus Finance and Operations rakendusest.</span><span class="sxs-lookup"><span data-stu-id="22900-168">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="22900-169">Olemasolevate Common Data Service andmete Finance and Operations rakendusega sünkroonimiseks rakendage [bootstrap](bootstrap-company-data.md) Common Data Service andmetele, kasutades kolmetähelist ettevõtte ISO-koodi.</span><span class="sxs-lookup"><span data-stu-id="22900-169">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="22900-170">Käivitage **Esmase sünkroonimise** funktsionaalsus üksustel, millele soovite andmeid sünkroonida.</span><span class="sxs-lookup"><span data-stu-id="22900-170">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="22900-171">Näite ja alternatiivse lähenemise saamiseks vt [Näide](#example).</span><span class="sxs-lookup"><span data-stu-id="22900-171">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="example"></a><span data-ttu-id="22900-172">Näide</span><span class="sxs-lookup"><span data-stu-id="22900-172">Example</span></span>

<span data-ttu-id="22900-173">Näite leiate teemast [Klientide lubamine V3 – kontaktide üksuse vastenduse](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)</span><span class="sxs-lookup"><span data-stu-id="22900-173">For an example, see [Enabling the Customers V3—Contacts entity map](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)</span></span>

<span data-ttu-id="22900-174">Alternatiivse lähenemise saamiseks andmemahtude põhjal igas üksuses, millel tuleb käitada esialgne sünkroonimine, vaadake teemat [Algse sünkroonimise kaalutlused](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="22900-174">For an alternative approach based on data volumes in each entity that need to run initial sync, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>
