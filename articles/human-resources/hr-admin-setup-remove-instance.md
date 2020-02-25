---
title: Eksemplari eemaldamine
description: ''
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
ms.openlocfilehash: 5c5f875ad9361c31af4fbe863488b881cdd97a6e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008703"
---
# <a name="remove-an-instance"></a><span data-ttu-id="07ca2-102">Eksemplari eemaldamine</span><span class="sxs-lookup"><span data-stu-id="07ca2-102">Remove an instance</span></span>

<span data-ttu-id="07ca2-103">See artikkel selgitab proovi- või tootmiskeskkonna eemaldamise protsessi rakenduse Microsoft Dynamics 365 Human Resources puhul.</span><span class="sxs-lookup"><span data-stu-id="07ca2-103">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="07ca2-104">Proovikeskkonna eemaldamine</span><span class="sxs-lookup"><span data-stu-id="07ca2-104">Remove a test drive environment</span></span>

<span data-ttu-id="07ca2-105">Rakenduse Human Resources proovikeskkonnad on ette valmistatud 60-päevase aegumispoliitikaga.</span><span class="sxs-lookup"><span data-stu-id="07ca2-105">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="07ca2-106">Kuid proovikeskkondade omanikel on võimalus lõpetada prooviversioon varakult, tehes järgmist.</span><span class="sxs-lookup"><span data-stu-id="07ca2-106">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="07ca2-107">Avage [Power Apps Halduskeskus](https://admin.businessplatform.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="07ca2-107">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="07ca2-108">Valige **Keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="07ca2-108">Select **Environments**.</span></span>
3. <span data-ttu-id="07ca2-109">Valige proovikeskkond, millel on vormingult sarnane nimi järgmisega: TestDrive – alias@domain</span><span class="sxs-lookup"><span data-stu-id="07ca2-109">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="07ca2-110">Valige **Kustuta** ja kinnitage otsus.</span><span class="sxs-lookup"><span data-stu-id="07ca2-110">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="07ca2-111">Olemasolev proovikeskkond eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="07ca2-111">The existing test drive environment will be removed.</span></span> <span data-ttu-id="07ca2-112">Kui see on eemaldatud, saate registreerida uue proovikeskkonna.</span><span class="sxs-lookup"><span data-stu-id="07ca2-112">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="07ca2-113">Tootmiskeskkonna eemaldamine</span><span class="sxs-lookup"><span data-stu-id="07ca2-113">Remove a production environment</span></span>

<span data-ttu-id="07ca2-114">See artikkel eeldab, et olete ostnud rakenduse Human Resources pilvelahenduse pakkuja (CSP) või ettevõtte arhitektuuri (AE) lepingu kaudu.</span><span class="sxs-lookup"><span data-stu-id="07ca2-114">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="07ca2-115">Kuna üks Human Resourcesi keskkond asub ühes Power Appsi keskkonnas, on kaks valikut.</span><span class="sxs-lookup"><span data-stu-id="07ca2-115">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="07ca2-116">Esimene valik hõlmab kogu Power Appsi keskkonna eemaldamist; teine hõlmab ainult Human Resourcesi eemaldamist.</span><span class="sxs-lookup"><span data-stu-id="07ca2-116">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="07ca2-117">Esimene valik on soovitatav, kui lõite Power Appsi keskkonna spetsiaalselt Human Resourcesi ettevalmistamiseks ja olete just juurutamisega alustanud või te pole loonud integratsioone.</span><span class="sxs-lookup"><span data-stu-id="07ca2-117">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="07ca2-118">Teine suvand on sobiv, kui teil on loodud Power Appsi keskkond, mis on täidetud rikasandmetega, mida kasutatakse Power Appsis ja Power Automate’is.</span><span class="sxs-lookup"><span data-stu-id="07ca2-118">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="07ca2-119">Enne Power Appsi keskkonna eemaldamist veenduge, et seda ei kasutataks rikasandmete integreerimiseks väljaspool rakenduse Human Resources ulatust.</span><span class="sxs-lookup"><span data-stu-id="07ca2-119">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="07ca2-120">Pange tähele, et Power Appsi vaikekeskkondasid ei saa eemaldada.</span><span class="sxs-lookup"><span data-stu-id="07ca2-120">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="07ca2-121">Kogu Power Appsi keskkonna eemaldamiseks koos Human Resourcesi ja seotud rakenduste ning voogudega tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="07ca2-121">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="07ca2-122">Avage [Power Apps Halduskeskus](https://admin.businessplatform.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="07ca2-122">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="07ca2-123">Valige **Keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="07ca2-123">Select **Environments**.</span></span>
3. <span data-ttu-id="07ca2-124">Valige eemaldatav keskkond.</span><span class="sxs-lookup"><span data-stu-id="07ca2-124">Select the environment to be removed.</span></span>
4. <span data-ttu-id="07ca2-125">Valige **Kustuta** ja kinnitage otsus.</span><span class="sxs-lookup"><span data-stu-id="07ca2-125">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="07ca2-126">Oodake, kuni kustutamine on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="07ca2-126">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="07ca2-127">Logige teenusesse [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) sisse, kasutades kontot, mida kasutasite rakenduse Human Resources tellimiseks.</span><span class="sxs-lookup"><span data-stu-id="07ca2-127">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="07ca2-128">Valige keskkonda sisaldav Human Resourcesi projekt.</span><span class="sxs-lookup"><span data-stu-id="07ca2-128">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="07ca2-129">Valige oma LCS-i projektis paan **Rakenduse Human Resources haldus**.</span><span class="sxs-lookup"><span data-stu-id="07ca2-129">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="07ca2-130">Valige eemaldatav eksemplar.</span><span class="sxs-lookup"><span data-stu-id="07ca2-130">Select the instance to remove.</span></span> 
10. <span data-ttu-id="07ca2-131">Valige **Eemalda eksemplar** ja kinnitage otsus.</span><span class="sxs-lookup"><span data-stu-id="07ca2-131">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="07ca2-132">Rakenduse Human Resources eemaldamiseks olemasolevast Power Appsi keskkonnast tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="07ca2-132">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="07ca2-133">Pange tähele, et tugimeeskonna kaasamine ja Human Resourcesi DevOpsi töörühmaga ühenduse võtmine on ajutine, kuni see funktsioon on lubatud otse LCS-is.</span><span class="sxs-lookup"><span data-stu-id="07ca2-133">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="07ca2-134">Eemaldamistaotluse käivitamiseks võtke ühendust toega.</span><span class="sxs-lookup"><span data-stu-id="07ca2-134">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="07ca2-135">Tugimeeskond edastab eemaldamise taotluse Human Resourcesi DevOpsi töörühmale.</span><span class="sxs-lookup"><span data-stu-id="07ca2-135">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="07ca2-136">Jätkake siis, kui olete saanud kinnituse, et keskkond on eemaldatud.</span><span class="sxs-lookup"><span data-stu-id="07ca2-136">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="07ca2-137">Logige LCS-i sisse, kasutades kontot, mida kasutasite rakenduse Human Resources tellimiseks.</span><span class="sxs-lookup"><span data-stu-id="07ca2-137">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="07ca2-138">Valige keskkonda sisaldav Human Resourcesi projekt.</span><span class="sxs-lookup"><span data-stu-id="07ca2-138">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="07ca2-139">Valige oma LCS-i projektis paan **Rakenduse Human Resources haldus**.</span><span class="sxs-lookup"><span data-stu-id="07ca2-139">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="07ca2-140">Valige eksemplar, mille soovite eemaldada (selle juures peaks olema märgitud juurutuse olek **Nurjus**).</span><span class="sxs-lookup"><span data-stu-id="07ca2-140">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="07ca2-141">Valige **Eemalda eksemplar** ja kinnitage otsus.</span><span class="sxs-lookup"><span data-stu-id="07ca2-141">Select **Remove instance** and confirm your decision.</span></span> 