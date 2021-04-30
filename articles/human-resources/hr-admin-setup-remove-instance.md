---
title: Eemalda eksemplar
description: See artikkel selgitab proovi- või tootmiskeskkonna eemaldamise protsessi rakenduse Microsoft Dynamics 365 Human Resources puhul.
author: andreabichsel
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a6f23adedc287b85018fe0b0af445677f6dc597c
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889904"
---
# <a name="remove-an-instance"></a><span data-ttu-id="eab11-103">Eemalda eksemplar</span><span class="sxs-lookup"><span data-stu-id="eab11-103">Remove an instance</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="eab11-104">See artikkel selgitab proovi- või tootmiskeskkonna eemaldamise protsessi rakenduse Microsoft Dynamics 365 Human Resources puhul.</span><span class="sxs-lookup"><span data-stu-id="eab11-104">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="eab11-105">Proovikeskkonna eemaldamine</span><span class="sxs-lookup"><span data-stu-id="eab11-105">Remove a test drive environment</span></span>

<span data-ttu-id="eab11-106">Rakenduse Human Resources proovikeskkonnad on ette valmistatud 60-päevase aegumispoliitikaga.</span><span class="sxs-lookup"><span data-stu-id="eab11-106">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="eab11-107">Kuid proovikeskkondade omanikel on võimalus lõpetada prooviversioon varakult, tehes järgmist.</span><span class="sxs-lookup"><span data-stu-id="eab11-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="eab11-108">Avage [Power Apps Halduskeskus](https://admin.businessplatform.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="eab11-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="eab11-109">Valige **Keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="eab11-109">Select **Environments**.</span></span>
3. <span data-ttu-id="eab11-110">Valige proovikeskkond, millel on vormingult sarnane nimi järgmisega: TestDrive – alias@domain</span><span class="sxs-lookup"><span data-stu-id="eab11-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="eab11-111">Valige **Kustuta** ja kinnitage otsus.</span><span class="sxs-lookup"><span data-stu-id="eab11-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="eab11-112">Olemasolev proovikeskkond eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="eab11-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="eab11-113">Kui see on eemaldatud, saate registreerida uue proovikeskkonna.</span><span class="sxs-lookup"><span data-stu-id="eab11-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="eab11-114">Tootmiskeskkonna eemaldamine</span><span class="sxs-lookup"><span data-stu-id="eab11-114">Remove a production environment</span></span>

<span data-ttu-id="eab11-115">See artikkel eeldab, et olete ostnud rakenduse Human Resources pilvelahenduse pakkuja (CSP) või ettevõtte arhitektuuri (AE) lepingu kaudu.</span><span class="sxs-lookup"><span data-stu-id="eab11-115">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="eab11-116">Kuna üks Human Resourcesi keskkond asub ühes Power Appsi keskkonnas, on kaks valikut.</span><span class="sxs-lookup"><span data-stu-id="eab11-116">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="eab11-117">Esimene valik hõlmab kogu Power Appsi keskkonna eemaldamist; teine hõlmab ainult Human Resourcesi eemaldamist.</span><span class="sxs-lookup"><span data-stu-id="eab11-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="eab11-118">Esimene valik on soovitatav, kui lõite Power Appsi keskkonna spetsiaalselt Human Resourcesi ettevalmistamiseks ja olete just juurutamisega alustanud või te pole loonud integratsioone.</span><span class="sxs-lookup"><span data-stu-id="eab11-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="eab11-119">Teine suvand on sobiv, kui teil on loodud Power Appsi keskkond, mis on täidetud rikasandmetega, mida kasutatakse Power Appsis ja Power Automate’is.</span><span class="sxs-lookup"><span data-stu-id="eab11-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="eab11-120">Enne Power Appsi keskkonna eemaldamist veenduge, et seda ei kasutataks rikasandmete integreerimiseks väljaspool rakenduse Human Resources ulatust.</span><span class="sxs-lookup"><span data-stu-id="eab11-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="eab11-121">Pange tähele, et Power Appsi vaikekeskkondasid ei saa eemaldada.</span><span class="sxs-lookup"><span data-stu-id="eab11-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="eab11-122">Kogu Power Appsi keskkonna eemaldamiseks koos Human Resourcesi ja seotud rakenduste ning voogudega tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="eab11-122">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="eab11-123">Avage [Power Apps Halduskeskus](https://admin.businessplatform.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="eab11-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="eab11-124">Valige **Keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="eab11-124">Select **Environments**.</span></span>
3. <span data-ttu-id="eab11-125">Valige eemaldatav keskkond.</span><span class="sxs-lookup"><span data-stu-id="eab11-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="eab11-126">Valige **Kustuta** ja kinnitage otsus.</span><span class="sxs-lookup"><span data-stu-id="eab11-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="eab11-127">Oodake, kuni kustutamine on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="eab11-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="eab11-128">Logige teenusesse [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) sisse, kasutades kontot, mida kasutasite rakenduse Human Resources tellimiseks.</span><span class="sxs-lookup"><span data-stu-id="eab11-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="eab11-129">Valige keskkonda sisaldav Human Resourcesi projekt.</span><span class="sxs-lookup"><span data-stu-id="eab11-129">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="eab11-130">Valige oma LCS-i projektis paan **Rakenduse Human Resources haldus**.</span><span class="sxs-lookup"><span data-stu-id="eab11-130">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="eab11-131">Valige eemaldatav eksemplar.</span><span class="sxs-lookup"><span data-stu-id="eab11-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="eab11-132">Valige **Eemalda eksemplar** ja kinnitage otsus.</span><span class="sxs-lookup"><span data-stu-id="eab11-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="eab11-133">Rakenduse Human Resources eemaldamiseks olemasolevast Power Appsi keskkonnast tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="eab11-133">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="eab11-134">Pange tähele, et tugimeeskonna kaasamine ja Human Resourcesi DevOpsi töörühmaga ühenduse võtmine on ajutine, kuni see funktsioon on lubatud otse LCS-is.</span><span class="sxs-lookup"><span data-stu-id="eab11-134">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="eab11-135">Eemaldamistaotluse käivitamiseks võtke ühendust toega.</span><span class="sxs-lookup"><span data-stu-id="eab11-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="eab11-136">Tugimeeskond edastab eemaldamise taotluse Human Resourcesi DevOpsi töörühmale.</span><span class="sxs-lookup"><span data-stu-id="eab11-136">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="eab11-137">Jätkake siis, kui olete saanud kinnituse, et keskkond on eemaldatud.</span><span class="sxs-lookup"><span data-stu-id="eab11-137">Continue after you receive word that the environment has been removed.</span></span>
4. <span data-ttu-id="eab11-138">Logige LCS-i sisse, kasutades kontot, mida kasutasite rakenduse Human Resources tellimiseks.</span><span class="sxs-lookup"><span data-stu-id="eab11-138">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="eab11-139">Valige keskkonda sisaldav Human Resourcesi projekt.</span><span class="sxs-lookup"><span data-stu-id="eab11-139">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="eab11-140">Valige oma LCS-i projektis paan **Rakenduse Human Resources haldus**.</span><span class="sxs-lookup"><span data-stu-id="eab11-140">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="eab11-141">Valige eksemplar, mille soovite eemaldada (selle juures peaks olema märgitud juurutuse olek **Kustutatud**).</span><span class="sxs-lookup"><span data-stu-id="eab11-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Deleted**.</span></span>
8. <span data-ttu-id="eab11-142">Valige **Eemalda eksemplar** ja kinnitage otsus.</span><span class="sxs-lookup"><span data-stu-id="eab11-142">Select **Remove instance** and confirm your decision.</span></span> 

## <a name="recover-a-soft-deleted-environment"></a><span data-ttu-id="eab11-143">Ajutiselt kustutatud keskkonna taastamine</span><span class="sxs-lookup"><span data-stu-id="eab11-143">Recover a soft-deleted environment</span></span>

<span data-ttu-id="eab11-144">Kui kustutate Power Appsi keskkonna, millega on ühendatud teie Human Resourcesi keskkond, kustutatakse Human Resourcesi olek teenuses Lifecycle Services **ajutiselt**.</span><span class="sxs-lookup"><span data-stu-id="eab11-144">If you delete the Power Apps environment that your Human Resources environment is connected to, the status of the Human Resources environment in Lifecycle Services will be **Soft deleted**.</span></span> <span data-ttu-id="eab11-145">Sel juhul ei saa kasutajad Human Resourcesiga ühendust luua.</span><span class="sxs-lookup"><span data-stu-id="eab11-145">In this case, users can't connect to Human Resources.</span></span>

<span data-ttu-id="eab11-146">Keskkonna taastamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="eab11-146">To restore the environment:</span></span>

1. <span data-ttu-id="eab11-147">Järgige teemas [Power Appsi keskkonna taastamine](/power-platform/admin/recover-environment.md) toodud juhiseid.</span><span class="sxs-lookup"><span data-stu-id="eab11-147">Follow the instructions in [Recover the Power Apps environment](/power-platform/admin/recover-environment.md).</span></span>

2. <span data-ttu-id="eab11-148">Human Resourcesi keskkonna taastamiseks võtke ühendust tugiteenusega.</span><span class="sxs-lookup"><span data-stu-id="eab11-148">Contact Support to restore the Human Resources environment.</span></span> <span data-ttu-id="eab11-149">Lisateavet leiate teemast [Toe hankimine](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="eab11-149">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

> [!Warning]
> <span data-ttu-id="eab11-150">Power Appsi keskkondi salvestatakse ainult seitse päeva pärast kustutamist.</span><span class="sxs-lookup"><span data-stu-id="eab11-150">Power Apps environments are only saved for seven days after deletion.</span></span> <span data-ttu-id="eab11-151">Peate taastama keskkonna seitsme päeva jooksul.</span><span class="sxs-lookup"><span data-stu-id="eab11-151">You must recover the environment within the seven day period.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]