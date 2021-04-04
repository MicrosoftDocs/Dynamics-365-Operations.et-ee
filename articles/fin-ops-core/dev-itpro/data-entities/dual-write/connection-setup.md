---
title: Topeltkirjutuse häälestamise juhend
description: Selle teema all kirjeldatakse stsenaariume, mida toetatakse kaksikkirjutamise seadistuseks.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
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
ms.openlocfilehash: dee6bc52a0967dfd6134258d3a02dc18feb404a5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560221"
---
# <a name="guidance-for-dual-write-setup"></a><span data-ttu-id="d753e-103">Topeltkirjutuse häälestamise juhend</span><span class="sxs-lookup"><span data-stu-id="d753e-103">Guidance for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d753e-104">Saate seadistada kaksikkirjutamise seose Finance and Operations keskkonna ja Dataverse keskkonna vahel.</span><span class="sxs-lookup"><span data-stu-id="d753e-104">You can set up a dual-write connection between a Finance and Operations environment and a Dataverse environment.</span></span>

+ <span data-ttu-id="d753e-105">**Finance and Operations keskkond** pakub platvormi **Finance and Operations rakendustele** (nt Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce ja Dynamics 365 Human Resources).</span><span class="sxs-lookup"><span data-stu-id="d753e-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="d753e-106">**Teenuse Dataverse keskkond** loob aluseks oleva platvormi **klientide kaasamise rakenduste** jaoks (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing ja Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="d753e-106">A **Dataverse environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d753e-107">Dynamics 365 Financei inimressursside moodul toetab topeltkirjutuse ühendusi, kuid rakendus Dynamics 365 Human Resources ei luba seda.</span><span class="sxs-lookup"><span data-stu-id="d753e-107">The Human Resources module in Dynamics 365 Finance supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="d753e-108">Seadistuse mehhanism erineb sõltuvalt teie tellimusest ja keskkonnast.</span><span class="sxs-lookup"><span data-stu-id="d753e-108">The setup mechanism varies, depending on your subscription and the environment:</span></span>

+ <span data-ttu-id="d753e-109">Uute Finance and Operations rakenduste puhul algab kaksikkirjutamise ühenduse seadistus Microsoft Dynamics Lifecycle Servicesiga (LCS).</span><span class="sxs-lookup"><span data-stu-id="d753e-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="d753e-110">Kui teil on Microsoft Power Platformi litsents, saate uue Dataverse'i keskkonna, kui teie rentnikul seda ei ole.</span><span class="sxs-lookup"><span data-stu-id="d753e-110">If you have a license for Microsoft Power Platform, you will get a new Dataverse environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="d753e-111">Olemasolevate Finance and Operations rakenduste puhul algab kaksikkirjutamise ühenduse seadistus Finance and Operations keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="d753e-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="d753e-112">Enne kui käivitate üksuse topeltkirjutuse, saate käitada algse sünkroonimise, et hallata olemasolevaid andmeid mõlemal poolel: Finance and Operationsi rakendustes ja Customer Engagementi rakendustes.</span><span class="sxs-lookup"><span data-stu-id="d753e-112">Before you start dual-write on an entity, you can run an initial synchronization to handle existing data on both sides: Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="d753e-113">Kui te ei pea nende kahe keskkonna vahel andmeid sünkroonima, saate algse sünkroonimise vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="d753e-113">You can skip the initial synchronization if you don't have to sync data between the two environments.</span></span>

<span data-ttu-id="d753e-114">Algse sünkroonimisega saate kopeerida olemasolevad andmed kahesuunaliselt ühest rakendusest teise.</span><span class="sxs-lookup"><span data-stu-id="d753e-114">An initial synchronization lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="d753e-115">Sõltuvalt sellest, millised keskkonnad teil on olemas ja millist tüüpi andmeid on nendes olemas, on mitu seadistuse stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="d753e-115">There are several setup scenarios, depending on the environments that you already have and the type of data in them.</span></span>

<span data-ttu-id="d753e-116">Toetatud on järgmised seadistusstsenaariumid:</span><span class="sxs-lookup"><span data-stu-id="d753e-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="d753e-117">Uus Finance and Operationsi rakenduse eksemplar ja uus Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="d753e-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="d753e-118">Uus Finance and Operationsi rakenduse eksemplar ja olemasolev Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="d753e-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="d753e-119">Uus Finance and Operationsi rakenduse eksemplar, millel on andmed, ja uus Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="d753e-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="d753e-120">Uus Finance and Operationsi rakenduse eksemplar, millel on andmed, ja olemasolev Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="d753e-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="d753e-121">Olemasolev Finance and Operationsi rakenduse eksemplar ja uus Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="d753e-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="d753e-122">Olemasolev Finance and Operationsi rakenduse eksemplar ja olemasolev Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="d753e-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="d753e-123">Uus Finance and Operationsi rakenduse eksemplar ja uus Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="d753e-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="d753e-124">Topeltkirjutuse ühenduse seadmiseks Finance and Operationsi rakenduse uue eksemplari, millel puuduvad andmed, ja Customer Engagementi rakenduse uue eksemplari vahel, järgige etappe jaotises [Topeltkirjutuse seadistus teenuses Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="d753e-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="d753e-125">Kui ühenduse seadistus on lõpule viidud, toimuvad automaatselt järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="d753e-125">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="d753e-126">Valmistatakse ette uus tühi Finance and Operations keskkond.</span><span class="sxs-lookup"><span data-stu-id="d753e-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="d753e-127">On ette valmistatud Customer Engagementi rakenduse uus tühi eksemplar, kus on installitud CRM-i pealahendus.</span><span class="sxs-lookup"><span data-stu-id="d753e-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="d753e-128">Kaksikkirjutamise ühendus on loodud DAT-ettevõtte andmetele.</span><span class="sxs-lookup"><span data-stu-id="d753e-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="d753e-129">Tabeli vastendused on lubatud reaalajas sünkroonimiseks.</span><span class="sxs-lookup"><span data-stu-id="d753e-129">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="d753e-130">Mõlemad keskkonnad on seejärel valmis reaalaja andmete sünkroonimiseks.</span><span class="sxs-lookup"><span data-stu-id="d753e-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="d753e-131">Uus Finance and Operationsi rakenduse eksemplar ja olemasolev Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="d753e-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="d753e-132">Topeltkirjutuse ühenduse seadmiseks Finance and Operationsi rakenduse uude eksemplari, millel puuduvad andmed, ja olemasoleva Customer Engagementi rakenduse eksemplari vahel, järgige etappe jaotises [Topeltkirjutuse seadistus teenuses Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="d753e-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="d753e-133">Kui ühenduse seadistus on lõpule viidud, toimuvad automaatselt järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="d753e-133">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="d753e-134">Valmistatakse ette uus tühi Finance and Operations keskkond.</span><span class="sxs-lookup"><span data-stu-id="d753e-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="d753e-135">Kaksikkirjutamise ühendus on loodud DAT-ettevõtte andmetele.</span><span class="sxs-lookup"><span data-stu-id="d753e-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="d753e-136">Tabeli vastendused on lubatud reaalajas sünkroonimiseks.</span><span class="sxs-lookup"><span data-stu-id="d753e-136">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="d753e-137">Mõlemad keskkonnad on seejärel valmis reaalaja andmete sünkroonimiseks.</span><span class="sxs-lookup"><span data-stu-id="d753e-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="d753e-138">Olemasolevate Dataverse andmete sünkroonimiseks Finance and Operations rakendusega toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="d753e-138">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="d753e-139">Looge Finance and Operations rakenduses uus ettevõte.</span><span class="sxs-lookup"><span data-stu-id="d753e-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="d753e-140">Lisage ettevõte kaksikkirjutamise ühenduse seadistusse.</span><span class="sxs-lookup"><span data-stu-id="d753e-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="d753e-141">Rakendage[Bootstrap](bootstrap-company-data.md) Dataverse andmetele, kasutades kolmetähelist Rahvusvahelise standardiorganisatsiooni (ISO) ettevõttekoodi.</span><span class="sxs-lookup"><span data-stu-id="d753e-141">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="d753e-142">Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.</span><span class="sxs-lookup"><span data-stu-id="d753e-142">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="d753e-143">Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake selles teemas hiljem jaotist [Näide](#example).</span><span class="sxs-lookup"><span data-stu-id="d753e-143">For links to an example and an alternative approach, see the [Example](#example) section later in this topic.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="d753e-144">Uus Finance and Operationsi rakenduse eksemplar, millel on andmed, ja uus Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="d753e-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="d753e-145">Topeltkirjutuse seose seadistamiseks Finance and Operationsi rakenduse uue eksemplari, millel on andmed, ja Customer Engagementi rakenduse uue eksemplari vahel, järgige selle teema all varem kirjeldatud etappe jaotises [Uus Finance and Operationsi rakenduse eksemplar ja uus Customer Engagementi rakenduse eksemplar](#new-new) .</span><span class="sxs-lookup"><span data-stu-id="d753e-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="d753e-146">Kui ühenduse häälestus on lõpule viidud, kui soovite andmeid sünkroonida Customer Engagementi rakendusega, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="d753e-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="d753e-147">Avage Finance and Operations rakendus LCS lehelt, logige sisse ja seejärel avage **Andmehaldus \> Kaksikkirjutamine**.</span><span class="sxs-lookup"><span data-stu-id="d753e-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="d753e-148">Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.</span><span class="sxs-lookup"><span data-stu-id="d753e-148">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="d753e-149">Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake jaotist [Näide](#example).</span><span class="sxs-lookup"><span data-stu-id="d753e-149">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="d753e-150">Uus Finance and Operationsi rakenduse eksemplar, millel on andmed, ja olemasolev Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="d753e-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="d753e-151">Topeltkirjutuse seose seadistamiseks Finance and Operationsi rakenduse uue eksemplari, millel on andmed, ja Customer Engagementi rakenduse olemasoleva eksemplari vahel, järgige selle teema all varem kirjeldatud etappe jaotises [Uus Finance and Operationsi rakenduse eksemplar ja olemasolev Customer Engagementi rakenduse eksemplar](#new-existing) .</span><span class="sxs-lookup"><span data-stu-id="d753e-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="d753e-152">Kui ühenduse häälestus on lõpule viidud, kui soovite andmeid sünkroonida Customer Engagementi rakendusega, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="d753e-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="d753e-153">Avage Finance and Operations rakendus LCS lehelt, logige sisse ja seejärel avage **Andmehaldus \> Kaksikkirjutamine**.</span><span class="sxs-lookup"><span data-stu-id="d753e-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="d753e-154">Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.</span><span class="sxs-lookup"><span data-stu-id="d753e-154">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="d753e-155">Olemasolevate Dataverse andmete sünkroonimiseks Finance and Operations rakendusega toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="d753e-155">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="d753e-156">Looge Finance and Operations rakenduses uus ettevõte.</span><span class="sxs-lookup"><span data-stu-id="d753e-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="d753e-157">Lisage ettevõte kaksikkirjutamise ühenduse seadistusse.</span><span class="sxs-lookup"><span data-stu-id="d753e-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="d753e-158">Rakendage[Bootstrap](bootstrap-company-data.md) Dataverse andmetele, kasutades kolmetähelist Rahvusvahelise standardiorganisatsiooni (ISO) ettevõttekoodi.</span><span class="sxs-lookup"><span data-stu-id="d753e-158">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="d753e-159">Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.</span><span class="sxs-lookup"><span data-stu-id="d753e-159">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="d753e-160">Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake jaotist [Näide](#example).</span><span class="sxs-lookup"><span data-stu-id="d753e-160">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="d753e-161">Olemasolev Finance and Operationsi rakenduse eksemplar ja uus Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="d753e-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="d753e-162">Olemasoleva Finance and Operationsi rakenduse eksemplari ja uue Customer Engagementi rakenduse eksemplari vahelise ühenduse topeltkirjutuse seadistus toimub keskkonnas Finance and Operation.</span><span class="sxs-lookup"><span data-stu-id="d753e-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="d753e-163">[Seadistage ühendus Finance and Operationsi rakendusest](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="d753e-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="d753e-164">Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.</span><span class="sxs-lookup"><span data-stu-id="d753e-164">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="d753e-165">Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake jaotist [Näide](#example).</span><span class="sxs-lookup"><span data-stu-id="d753e-165">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="d753e-166">Olemasolev Finance and Operationsi rakenduse eksemplar ja olemasolev Customer Engagementi rakenduse eksemplar</span><span class="sxs-lookup"><span data-stu-id="d753e-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="d753e-167">Olemasoleva Finance and Operationsi rakenduse eksemplari ja olemasoleva Customer Engagementi rakenduse eksemplari vahelise ühenduse topeltkirjutuse seadistus toimub keskkonnas Finance and Operation.</span><span class="sxs-lookup"><span data-stu-id="d753e-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="d753e-168">[Seadistage ühendus Finance and Operationsi rakendusest](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="d753e-168">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="d753e-169">Olemasolevate Dataverse andmete Finance and Operations rakendusega sünkroonimiseks rakendage [bootstrap](bootstrap-company-data.md) Dataverse andmetele, kasutades kolmetähelist ettevõtte ISO-koodi.</span><span class="sxs-lookup"><span data-stu-id="d753e-169">To sync the existing Dataverse data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="d753e-170">Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.</span><span class="sxs-lookup"><span data-stu-id="d753e-170">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="d753e-171">Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake jaotist [Näide](#example).</span><span class="sxs-lookup"><span data-stu-id="d753e-171">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="example"></a><span data-ttu-id="d753e-172">Näide</span><span class="sxs-lookup"><span data-stu-id="d753e-172">Example</span></span>

<span data-ttu-id="d753e-173">Näite leiate teemast [Klientide lubamine V3 – kontaktide tabeli vastendus](enable-entity-map.md#enable-table-map)</span><span class="sxs-lookup"><span data-stu-id="d753e-173">For an example, see [Enabling the Customers V3—Contacts table map](enable-entity-map.md#enable-table-map)</span></span>

<span data-ttu-id="d753e-174">Alternatiivse lähenemise saamiseks, mis põhineb igas üksuse andmemahtudel, millel tuleb käitada esialgne sünkroonimine, vaadake teemat [Algse sünkroonimise kaalutlused](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="d753e-174">For an alternative approach that is based on data volumes in each entity that must run an initial synchronization, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]