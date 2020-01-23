---
title: Talenti keskkondade eemaldamine
description: See teema selgitab proovi- või tootmiskeskkonna eemaldamise protsessi rakenduse Microsoft Dynamics 365 Talent puhul.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: e752d658388fc6cb6f4b84ac83cb12a71522199b
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898106"
---
# <a name="remove-talent-environments"></a><span data-ttu-id="29043-103">Talenti keskkondade eemaldamine</span><span class="sxs-lookup"><span data-stu-id="29043-103">Remove Talent environments</span></span>

<span data-ttu-id="29043-104">See teema selgitab proovi- või tootmiskeskkonna eemaldamise protsessi rakenduse Microsoft Dynamics 365 Talent puhul.</span><span class="sxs-lookup"><span data-stu-id="29043-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="29043-105">Proovikeskkonna eemaldamine</span><span class="sxs-lookup"><span data-stu-id="29043-105">Removing a test drive environment</span></span>

<span data-ttu-id="29043-106">Talenti proovikeskkonnad on ette valmistatud 60-päevase aegumispoliitikaga.</span><span class="sxs-lookup"><span data-stu-id="29043-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="29043-107">Kuid proovikeskkondade omanikel on võimalus lõpetada prooviversioon varakult, tehes järgmist.</span><span class="sxs-lookup"><span data-stu-id="29043-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="29043-108">Avage [Power Apps Halduskeskus](https://admin.businessplatform.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="29043-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="29043-109">Valige **Keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="29043-109">Select **Environments**.</span></span>
3. <span data-ttu-id="29043-110">Valige proovikeskkond, millel on vormingult sarnane nimi järgmisega: TestDrive – alias@domain</span><span class="sxs-lookup"><span data-stu-id="29043-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="29043-111">Valige **Kustuta** ja kinnitage otsus.</span><span class="sxs-lookup"><span data-stu-id="29043-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="29043-112">Olemasolev proovikeskkond eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="29043-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="29043-113">Kui see on eemaldatud, saate registreerida uue proovikeskkonna.</span><span class="sxs-lookup"><span data-stu-id="29043-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="29043-114">Tootmiskeskkonna eemaldamine</span><span class="sxs-lookup"><span data-stu-id="29043-114">Removing a production environment</span></span>

<span data-ttu-id="29043-115">See teema eeldab, et olete ostnud rakenduse Talent pilvelahenduse pakkuja (CSP) või ettevõtte arhitektuuri (AE) lepingu kaudu.</span><span class="sxs-lookup"><span data-stu-id="29043-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="29043-116">Kuna üks Talenti keskkond asub ühes Power Appsi keskkonnas, on kaks suvandit.</span><span class="sxs-lookup"><span data-stu-id="29043-116">Since a single Talent environment is “contained” within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="29043-117">Esimene valik hõlmab kogu Power Appsi keskkonna eemaldamist; teine hõlmab ainult Talenti eemaldamist.</span><span class="sxs-lookup"><span data-stu-id="29043-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="29043-118">Esimene suvand on soovitatav, kui lõite Power Appsi keskkonna spetsiaalselt Talenti ettevalmistamiseks ja olete just juurutamisega alustanud või te pole loonud integratsioone.</span><span class="sxs-lookup"><span data-stu-id="29043-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="29043-119">Teine suvand on sobiv, kui teil on loodud Power Appsi keskkond, mis on täidetud rikasandmetega, mida kasutatakse Power Appsis ja Power Automate’is.</span><span class="sxs-lookup"><span data-stu-id="29043-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="29043-120">Enne Power Appsi keskkonna eemaldamist veenduge, et seda ei kasutata rikasandmete integreerimiseks väljaspool Talenti ulatust.</span><span class="sxs-lookup"><span data-stu-id="29043-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="29043-121">Pange tähele, et Power Appsi vaikekeskkondasid ei saa eemaldada.</span><span class="sxs-lookup"><span data-stu-id="29043-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="29043-122">Kogu Power Appsi keskkonna eemaldamiseks koos Talenti ning seotud rakenduste ja voogudega tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="29043-122">To remove the entire Power Apps environment, including Talent and the associated apps and flows:</span></span>

1. <span data-ttu-id="29043-123">Avage [Power Apps Halduskeskus](https://admin.businessplatform.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="29043-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="29043-124">Valige **Keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="29043-124">Select **Environments**.</span></span>
3. <span data-ttu-id="29043-125">Valige eemaldatav keskkond.</span><span class="sxs-lookup"><span data-stu-id="29043-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="29043-126">Valige **Kustuta** ja kinnitage otsus.</span><span class="sxs-lookup"><span data-stu-id="29043-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="29043-127">Oodake, kuni kustutamine on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="29043-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="29043-128">Logige teenusesse [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) sisse, kasutades kontot, mida kasutasite Talenti tellimiseks.</span><span class="sxs-lookup"><span data-stu-id="29043-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="29043-129">Valige keskkonda sisaldav Talenti projekt.</span><span class="sxs-lookup"><span data-stu-id="29043-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="29043-130">Valige oma LCS-i projektis paan **Talenti rakendusehaldus**.</span><span class="sxs-lookup"><span data-stu-id="29043-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="29043-131">Valige eemaldatav eksemplar.</span><span class="sxs-lookup"><span data-stu-id="29043-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="29043-132">Valige **Eemalda eksemplar** ja kinnitage otsus.</span><span class="sxs-lookup"><span data-stu-id="29043-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="29043-133">Talenti eemaldamiseks olemasolevast Power Appsi keskkonnast tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="29043-133">To remove a Talent environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="29043-134">Pange tähele, et tugimeeskonna kaasamine ja Talenti DevOpsi töörühmaga ühenduse võtmine on ajutine, kuni see funktsioon on lubatud otse LCS-is.</span><span class="sxs-lookup"><span data-stu-id="29043-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="29043-135">Eemaldamistaotluse käivitamiseks võtke ühendust toega.</span><span class="sxs-lookup"><span data-stu-id="29043-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="29043-136">Tugimeeskond edastab eemaldamise taotluse Talenti DevOpsi töörühmale.</span><span class="sxs-lookup"><span data-stu-id="29043-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="29043-137">Jätkake siis, kui olete saanud kinnituse, et keskkond on eemaldatud.</span><span class="sxs-lookup"><span data-stu-id="29043-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="29043-138">Logige LCS-i sisse, kasutades kontot, mida kasutasite Talenti tellimiseks.</span><span class="sxs-lookup"><span data-stu-id="29043-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="29043-139">Valige keskkonda sisaldav Talenti projekt.</span><span class="sxs-lookup"><span data-stu-id="29043-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="29043-140">Valige oma LCS-i projektis paan **Talenti rakendusehaldus**.</span><span class="sxs-lookup"><span data-stu-id="29043-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="29043-141">Valige eksemplar, mille soovite eemaldada (selle juures peaks olema märgitud juurutuse olek **Nurjus**).</span><span class="sxs-lookup"><span data-stu-id="29043-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="29043-142">Valige **Eemalda eksemplar** ja kinnitage otsus.</span><span class="sxs-lookup"><span data-stu-id="29043-142">Select **Remove instance** and confirm your decision.</span></span> 

