---
title: Eemalda eksemplar
description: See artikkel selgitab proovi- või tootmiskeskkonna eemaldamise protsessi rakenduse Microsoft Dynamics 365 Human Resources puhul.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a40b9619e92b81272208ad4241a2455330a342a7
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124424"
---
# <a name="remove-an-instance"></a><span data-ttu-id="e2c05-103">Eemalda eksemplar</span><span class="sxs-lookup"><span data-stu-id="e2c05-103">Remove an instance</span></span>

<span data-ttu-id="e2c05-104">See artikkel selgitab proovi- või tootmiskeskkonna eemaldamise protsessi rakenduse Microsoft Dynamics 365 Human Resources puhul.</span><span class="sxs-lookup"><span data-stu-id="e2c05-104">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="e2c05-105">Proovikeskkonna eemaldamine</span><span class="sxs-lookup"><span data-stu-id="e2c05-105">Remove a test drive environment</span></span>

<span data-ttu-id="e2c05-106">Rakenduse Human Resources proovikeskkonnad on ette valmistatud 60-päevase aegumispoliitikaga.</span><span class="sxs-lookup"><span data-stu-id="e2c05-106">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="e2c05-107">Kuid proovikeskkondade omanikel on võimalus lõpetada prooviversioon varakult, tehes järgmist.</span><span class="sxs-lookup"><span data-stu-id="e2c05-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="e2c05-108">Avage [Power Apps Halduskeskus](https://admin.businessplatform.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="e2c05-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="e2c05-109">Valige **Keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="e2c05-109">Select **Environments**.</span></span>
3. <span data-ttu-id="e2c05-110">Valige proovikeskkond, millel on vormingult sarnane nimi järgmisega: TestDrive – alias@domain</span><span class="sxs-lookup"><span data-stu-id="e2c05-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="e2c05-111">Valige **Kustuta** ja kinnitage otsus.</span><span class="sxs-lookup"><span data-stu-id="e2c05-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="e2c05-112">Olemasolev proovikeskkond eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="e2c05-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="e2c05-113">Kui see on eemaldatud, saate registreerida uue proovikeskkonna.</span><span class="sxs-lookup"><span data-stu-id="e2c05-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="e2c05-114">Tootmiskeskkonna eemaldamine</span><span class="sxs-lookup"><span data-stu-id="e2c05-114">Remove a production environment</span></span>

<span data-ttu-id="e2c05-115">See artikkel eeldab, et olete ostnud rakenduse Human Resources pilvelahenduse pakkuja (CSP) või ettevõtte arhitektuuri (AE) lepingu kaudu.</span><span class="sxs-lookup"><span data-stu-id="e2c05-115">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="e2c05-116">Kuna üks Human Resourcesi keskkond asub ühes Power Appsi keskkonnas, on kaks valikut.</span><span class="sxs-lookup"><span data-stu-id="e2c05-116">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="e2c05-117">Esimene valik hõlmab kogu Power Appsi keskkonna eemaldamist; teine hõlmab ainult Human Resourcesi eemaldamist.</span><span class="sxs-lookup"><span data-stu-id="e2c05-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="e2c05-118">Esimene valik on soovitatav, kui lõite Power Appsi keskkonna spetsiaalselt Human Resourcesi ettevalmistamiseks ja olete just juurutamisega alustanud või te pole loonud integratsioone.</span><span class="sxs-lookup"><span data-stu-id="e2c05-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="e2c05-119">Teine suvand on sobiv, kui teil on loodud Power Appsi keskkond, mis on täidetud rikasandmetega, mida kasutatakse Power Appsis ja Power Automate’is.</span><span class="sxs-lookup"><span data-stu-id="e2c05-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="e2c05-120">Enne Power Appsi keskkonna eemaldamist veenduge, et seda ei kasutataks rikasandmete integreerimiseks väljaspool rakenduse Human Resources ulatust.</span><span class="sxs-lookup"><span data-stu-id="e2c05-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="e2c05-121">Pange tähele, et Power Appsi vaikekeskkondasid ei saa eemaldada.</span><span class="sxs-lookup"><span data-stu-id="e2c05-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="e2c05-122">Kogu Power Appsi keskkonna eemaldamiseks koos Human Resourcesi ja seotud rakenduste ning voogudega tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e2c05-122">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="e2c05-123">Avage [Power Apps Halduskeskus](https://admin.businessplatform.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="e2c05-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="e2c05-124">Valige **Keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="e2c05-124">Select **Environments**.</span></span>
3. <span data-ttu-id="e2c05-125">Valige eemaldatav keskkond.</span><span class="sxs-lookup"><span data-stu-id="e2c05-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="e2c05-126">Valige **Kustuta** ja kinnitage otsus.</span><span class="sxs-lookup"><span data-stu-id="e2c05-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="e2c05-127">Oodake, kuni kustutamine on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="e2c05-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="e2c05-128">Logige teenusesse [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) sisse, kasutades kontot, mida kasutasite rakenduse Human Resources tellimiseks.</span><span class="sxs-lookup"><span data-stu-id="e2c05-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="e2c05-129">Valige keskkonda sisaldav Human Resourcesi projekt.</span><span class="sxs-lookup"><span data-stu-id="e2c05-129">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="e2c05-130">Valige oma LCS-i projektis paan **Rakenduse Human Resources haldus**.</span><span class="sxs-lookup"><span data-stu-id="e2c05-130">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="e2c05-131">Valige eemaldatav eksemplar.</span><span class="sxs-lookup"><span data-stu-id="e2c05-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="e2c05-132">Valige **Eemalda eksemplar** ja kinnitage otsus.</span><span class="sxs-lookup"><span data-stu-id="e2c05-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="e2c05-133">Rakenduse Human Resources eemaldamiseks olemasolevast Power Appsi keskkonnast tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e2c05-133">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="e2c05-134">Pange tähele, et tugimeeskonna kaasamine ja Human Resourcesi DevOpsi töörühmaga ühenduse võtmine on ajutine, kuni see funktsioon on lubatud otse LCS-is.</span><span class="sxs-lookup"><span data-stu-id="e2c05-134">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="e2c05-135">Eemaldamistaotluse käivitamiseks võtke ühendust toega.</span><span class="sxs-lookup"><span data-stu-id="e2c05-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="e2c05-136">Tugimeeskond edastab eemaldamise taotluse Human Resourcesi DevOpsi töörühmale.</span><span class="sxs-lookup"><span data-stu-id="e2c05-136">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="e2c05-137">Jätkake siis, kui olete saanud kinnituse, et keskkond on eemaldatud.</span><span class="sxs-lookup"><span data-stu-id="e2c05-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="e2c05-138">Logige LCS-i sisse, kasutades kontot, mida kasutasite rakenduse Human Resources tellimiseks.</span><span class="sxs-lookup"><span data-stu-id="e2c05-138">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="e2c05-139">Valige keskkonda sisaldav Human Resourcesi projekt.</span><span class="sxs-lookup"><span data-stu-id="e2c05-139">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="e2c05-140">Valige oma LCS-i projektis paan **Rakenduse Human Resources haldus**.</span><span class="sxs-lookup"><span data-stu-id="e2c05-140">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="e2c05-141">Valige eksemplar, mille soovite eemaldada (selle juures peaks olema märgitud juurutuse olek **Nurjus**).</span><span class="sxs-lookup"><span data-stu-id="e2c05-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="e2c05-142">Valige **Eemalda eksemplar** ja kinnitage otsus.</span><span class="sxs-lookup"><span data-stu-id="e2c05-142">Select **Remove instance** and confirm your decision.</span></span> 
