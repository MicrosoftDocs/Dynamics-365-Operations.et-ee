---
title: Talenti keskkondade eemaldamine
description: See teema selgitab proovi- või tootmiskeskkonna eemaldamise protsessi rakenduse Microsoft Dynamics 365 for Talent puhul.
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
ms.openlocfilehash: 904c8eb1254a65e1627c33f14488a1a8e12f7c2b
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517807"
---
# <a name="remove-talent-environments"></a><span data-ttu-id="cb5f9-103">Talenti keskkondade eemaldamine</span><span class="sxs-lookup"><span data-stu-id="cb5f9-103">Remove Talent environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cb5f9-104">See teema selgitab proovi- või tootmiskeskkonna eemaldamise protsessi rakenduse Microsoft Dynamics 365 for Talent puhul.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 for Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="cb5f9-105">Proovikeskkonna eemaldamine</span><span class="sxs-lookup"><span data-stu-id="cb5f9-105">Removing a test drive environment</span></span>

<span data-ttu-id="cb5f9-106">Talenti proovikeskkonnad on ette valmistatud 60-päevase aegumispoliitikaga.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="cb5f9-107">Kuid proovikeskkondade omanikel on võimalus lõpetada prooviversioon varakult, tehes järgmist.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="cb5f9-108">Avage [PowerAppsi administreerimiskeskus](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="cb5f9-108">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="cb5f9-109">Valige **Keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-109">Select **Environments**.</span></span>
3. <span data-ttu-id="cb5f9-110">Valige proovikeskkond, millel on vormingult sarnane nimi järgmisega: TestDrive – alias@domain</span><span class="sxs-lookup"><span data-stu-id="cb5f9-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="cb5f9-111">Valige **Kustuta** ja kinnitage otsus.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="cb5f9-112">Olemasolev proovikeskkond eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="cb5f9-113">Kui see on eemaldatud, saate registreerida uue proovikeskkonna.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="cb5f9-114">Tootmiskeskkonna eemaldamine</span><span class="sxs-lookup"><span data-stu-id="cb5f9-114">Removing a production environment</span></span>

<span data-ttu-id="cb5f9-115">See teema eeldab, et olete ostnud rakenduse Talent pilvelahenduse pakkuja (CSP) või ettevõtte arhitektuuri (AE) lepingu kaudu.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="cb5f9-116">Kuna üks Talenti keskkond asub ühes PowerAppsi keskkonnas, on kaks suvandit.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-116">Since a single Talent environment is “contained” within a single PowerApps environment, there are two options to consider.</span></span> <span data-ttu-id="cb5f9-117">Esimene valik hõlmab kogu PowerAppsi keskkonna eemaldamist; teine hõlmab ainult Talenti eemaldamist.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-117">The first option involves removing the entire PowerApps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="cb5f9-118">Esimene suvand on soovitatav, kui lõite PowerAppsi keskkonna spetsiaalselt Talenti ettevalmistamiseks ja olete just juurutamisega alustanud või te pole loonud integratsioone.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-118">The first option is preferred when you have created a PowerApps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="cb5f9-119">Teine suvand on sobiv, kui teil on PowerAppsi keskkond, mis on täidetud rikasandmetega, mida kasutatakse PowerAppsis ja voogudes.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-119">The second option is appropriate when you have an established PowerApps environment populated with rich data that's leveraged in PowerApps and Flows.</span></span>

> [!Important]
> <span data-ttu-id="cb5f9-120">Enne PowerAppsi keskkonna eemaldamist veenduge, et seda ei kasutata rikasandmete integreerimiseks väljaspool Talenti ulatust.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-120">Before removing the PowerApps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="cb5f9-121">Pange tähele, et PowerAppsi vaikekeskkondasid ei saa eemaldada.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-121">Also note that the default PowerApps environments cannot be removed.</span></span> 

<span data-ttu-id="cb5f9-122">Kogu PowerAppsi keskkonna eemaldamiseks koos Talenti ning seotud rakenduste ja voogudega tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-122">To remove the entire PowerApps environment, including Talent and the associated Apps and Flows:</span></span>

1. <span data-ttu-id="cb5f9-123">Avage [PowerAppsi administreerimiskeskus](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="cb5f9-123">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="cb5f9-124">Valige **Keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-124">Select **Environments**.</span></span>
3. <span data-ttu-id="cb5f9-125">Valige eemaldatav keskkond.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="cb5f9-126">Valige **Kustuta** ja kinnitage otsus.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="cb5f9-127">Oodake, kuni kustutamine on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="cb5f9-128">Logige teenusesse [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) sisse, kasutades kontot, mida kasutasite Talenti tellimiseks.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="cb5f9-129">Valige keskkonda sisaldav Talenti projekt.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="cb5f9-130">Valige oma LCS-i projektis paan **Talenti rakendusehaldus**.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="cb5f9-131">Valige eemaldatav eksemplar.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="cb5f9-132">Valige **Eemalda eksemplar** ja kinnitage otsus.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="cb5f9-133">Talenti eemaldamiseks olemasolevast PowerAppsi keskkonnast tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-133">To remove a Talent environment from an existing PowerApps environment, complete the following steps.</span></span> <span data-ttu-id="cb5f9-134">Pange tähele, et tugimeeskonna kaasamine ja Talenti DevOpsi töörühmaga ühenduse võtmine on ajutine, kuni see funktsioon on lubatud otse LCS-is.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="cb5f9-135">Eemaldamistaotluse käivitamiseks võtke ühendust toega.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="cb5f9-136">Tugimeeskond edastab eemaldamise taotluse Talenti DevOpsi töörühmale.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="cb5f9-137">Jätkake siis, kui olete saanud kinnituse, et keskkond on eemaldatud.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="cb5f9-138">Logige LCS-i sisse, kasutades kontot, mida kasutasite Talenti tellimiseks.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="cb5f9-139">Valige keskkonda sisaldav Talenti projekt.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="cb5f9-140">Valige oma LCS-i projektis paan **Talenti rakendusehaldus**.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="cb5f9-141">Valige eksemplar, mille soovite eemaldada (selle juures peaks olema märgitud juurutuse olek **Nurjus**).</span><span class="sxs-lookup"><span data-stu-id="cb5f9-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="cb5f9-142">Valige **Eemalda eksemplar** ja kinnitage otsus.</span><span class="sxs-lookup"><span data-stu-id="cb5f9-142">Select **Remove instance** and confirm your decision.</span></span> 

