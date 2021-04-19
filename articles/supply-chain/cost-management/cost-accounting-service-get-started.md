---
title: Kuluarvestuse teenuse kasutamise alustamine (privaatne eelvaade)
description: See teema hõlmab kuluarvestuse teenuse litsentsi üksikasju ja installijuhiseid.
author: AndersGirke
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: b6756e3745aa4596bd5d63ad15aaf4385cfc4813
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813191"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a><span data-ttu-id="803be-103">Kuluarvestuse teenuse kasutamise alustamine (privaatne eelvaade)</span><span class="sxs-lookup"><span data-stu-id="803be-103">Get started with the cost accounting service (private preview)</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="803be-104">Selles teemas kirjeldatud funktsioon on saadaval privaatsete eelväljaannete osana.</span><span class="sxs-lookup"><span data-stu-id="803be-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="803be-105">Teema sisu ja selles kirjeldatav funktsioon võivad muutuda.</span><span class="sxs-lookup"><span data-stu-id="803be-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="803be-106">Lisateavet eelväljaannete kohta vt teemast [Ühe versiooni teenuse värskenduste KKK](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="803be-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="803be-107">Kuluarvestuse teenus võimaldab teil teha mitut laoarvestust teie seadistatud kuluarvestuse pearaamatutes.</span><span class="sxs-lookup"><span data-stu-id="803be-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="803be-108">Te seostate iga kuluarvestuse pearaamatu *reegliga*.</span><span class="sxs-lookup"><span data-stu-id="803be-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="803be-109">Reegel on järgmist tüüpi raamatupidamispoliitikate kogumik.</span><span class="sxs-lookup"><span data-stu-id="803be-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="803be-110">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="803be-110">Cost object</span></span>
- <span data-ttu-id="803be-111">Sisendi mõõtmise alus</span><span class="sxs-lookup"><span data-stu-id="803be-111">Input measurement basis</span></span>
- <span data-ttu-id="803be-112">Kuluvoo eeldus</span><span class="sxs-lookup"><span data-stu-id="803be-112">Cost flow assumption</span></span>
- <span data-ttu-id="803be-113">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="803be-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="803be-114">Isegi kui olete kuluarvestuse teenuse sisse lülitanud, saate jätkuvalt samamoodi Microsoft Dynamics 365 Supply Chain Managementis laoarvestust teha.</span><span class="sxs-lookup"><span data-stu-id="803be-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="803be-115">Kuluarvestuse teenus on lisandmoodul.</span><span class="sxs-lookup"><span data-stu-id="803be-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="803be-116">Selle funktsioonide kättesaadavaks tegemiseks peate selle installima teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu.</span><span class="sxs-lookup"><span data-stu-id="803be-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="803be-117">Seejärel saate valida, kas hinnata seda testimiskeskkonnas enne selle sisselülitamist töökeskkondades.</span><span class="sxs-lookup"><span data-stu-id="803be-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="803be-118">Kuluarvestuse teenus ei toeta praegu kõiki kulude haldamise funktsioone, mida Dynamics 365 Supply Chain Management hõlmab.</span><span class="sxs-lookup"><span data-stu-id="803be-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="803be-119">Seega on oluline, et hindaksite, kas hetkel saadaolev funktsioonide komplekt vastab teie nõuetele.</span><span class="sxs-lookup"><span data-stu-id="803be-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a><span data-ttu-id="803be-120">Kuluarvestuse teenuse hankimine (privaatne eelvaade)</span><span class="sxs-lookup"><span data-stu-id="803be-120">How to get the cost accounting service (private preview)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="803be-121">Kuluarvestuse teenuse kasutamiseks peab teil olema LCS-i toega suure kättesaadavusega keskkond (mitte OneBoxi keskkond) ning Dynamics 365 Supply Chain Managementi versioon 10.0.11 või uuem.</span><span class="sxs-lookup"><span data-stu-id="803be-121">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="803be-122">Kuluarvestuse teenuse privaatse eelvaate registreerimiseks saatke oma LCS-i keskkonna ID meili teel [Kuluarvestuse teenusele (privaatne eelvaade)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span><span class="sxs-lookup"><span data-stu-id="803be-122">To sign up for the cost accounting service private preview, please send your LCS environment ID by email to [Cost accounting service (private preview)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span></span> <span data-ttu-id="803be-123">Kui oleme kinnitanud teid programmi jaoks, saadame teile järeltegevuse meili, mis sisaldab kuluarvestuse teenuse beetavõtit.</span><span class="sxs-lookup"><span data-stu-id="803be-123">On approving you for the program, we will send you a follow up email that contains a cost accounting service beta key.</span></span> <span data-ttu-id="803be-124">Kui olete beetavõtme kätte saanud, saate jätkata [lisandmooduli installimisega](#install).</span><span class="sxs-lookup"><span data-stu-id="803be-124">On receiving the beta key, you can proceed by [installing the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="803be-125">Litsentsimine</span><span class="sxs-lookup"><span data-stu-id="803be-125">Licensing</span></span>

<span data-ttu-id="803be-126">Kuluarvestuse teenus litsentsitakse koos standardsete laoarvestuse funktsioonidega, mis on saadaval teenuse Supply Chain Management jaoks.</span><span class="sxs-lookup"><span data-stu-id="803be-126">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="803be-127">Te ei pea kuluarvestuse teenuse kasutamiseks ostma täiendavat litsentsi.</span><span class="sxs-lookup"><span data-stu-id="803be-127">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="803be-128">Lisandmooduli installimine</span><span class="sxs-lookup"><span data-stu-id="803be-128">Install the add-in</span></span>

<span data-ttu-id="803be-129">Kuluarvestuse teenuse kasutamiseks installige kuluarvestuse teenuse lisandmoodul teenuse Supply Chain Management jaoks, nagu kirjeldatakse järgmises toimingus.</span><span class="sxs-lookup"><span data-stu-id="803be-129">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="803be-130">Kuluarvestuse teenuse hankimiseks [registreerumine](#sign-up) (privaatne eelvaade).</span><span class="sxs-lookup"><span data-stu-id="803be-130">[Sign up](#sign-up) for the cost accounting service (private preview).</span></span>

1. <span data-ttu-id="803be-131">Logige teenusesse LCS sisse.</span><span class="sxs-lookup"><span data-stu-id="803be-131">Sign in to LCS.</span></span>

1. <span data-ttu-id="803be-132">Avage suvand **Eelvaate funktsiooni haldamine**.</span><span class="sxs-lookup"><span data-stu-id="803be-132">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="803be-133">Valige plussmärk (**+**).</span><span class="sxs-lookup"><span data-stu-id="803be-133">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="803be-134">Sisestage väljale **Kood** kuluarvestuse teenuse lisandmooduli beetavõti.</span><span class="sxs-lookup"><span data-stu-id="803be-134">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="803be-135">(Võti saadeti teile e-posti teel.)</span><span class="sxs-lookup"><span data-stu-id="803be-135">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="803be-136">Valige **Tühista blokeerimine**.</span><span class="sxs-lookup"><span data-stu-id="803be-136">Select **Unblock**.</span></span>

1. <span data-ttu-id="803be-137">Avage LCS-i keskkond, kuhu soovite teenuse lisada.</span><span class="sxs-lookup"><span data-stu-id="803be-137">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="803be-138">Avage **Kõik üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="803be-138">Go to **Full details**.</span></span>

1. <span data-ttu-id="803be-139">Kerige alla kiirkaardini **Keskkonna lisandmoodulid**.</span><span class="sxs-lookup"><span data-stu-id="803be-139">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="803be-140">Valige **Installi uus lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="803be-140">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="803be-141">Valige **Kuluarvestuse teenus**.</span><span class="sxs-lookup"><span data-stu-id="803be-141">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="803be-142">Täitke paigaldusjuhendit ja nõustuge nõuete ja tingimustega.</span><span class="sxs-lookup"><span data-stu-id="803be-142">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="803be-143">Valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="803be-143">Select **Install**.</span></span>

1. <span data-ttu-id="803be-144">Peaksite nägema kiirkaardil **Keskkonna lisandmoodulid**, et kuluarvestuse teenust installitakse.</span><span class="sxs-lookup"><span data-stu-id="803be-144">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="803be-145">Mõne minuti pärast peaks olek **Installimine** muutuma olekuks **Installitud**.</span><span class="sxs-lookup"><span data-stu-id="803be-145">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="803be-146">(Selle muudatuse nägemiseks võib olla vaja lehte värskendada.) Pärast seda on kuluarvestuse teenus kasutamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="803be-146">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="803be-147">Integratsiooni seadistamine</span><span class="sxs-lookup"><span data-stu-id="803be-147">Set up the integration</span></span>

<span data-ttu-id="803be-148">Kuluarvestuse teenuse ja Dynamics 365 Supply Chain Managementi vahel integratsiooni seadistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="803be-148">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="803be-149">Avage **Süsteemihaldus > Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="803be-149">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="803be-150">Valige **Otsi värskendusi**.</span><span class="sxs-lookup"><span data-stu-id="803be-150">Select **Check for updates**.</span></span>

1. <span data-ttu-id="803be-151">Avage vahekaart **Kõik** ja otsige funktsiooni nimega *Kuluarvestuse teenus*.</span><span class="sxs-lookup"><span data-stu-id="803be-151">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="803be-152">Valige **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="803be-152">Select **Enable now**.</span></span>

1. <span data-ttu-id="803be-153">Avage **Kuluhaldus > Kuluarvestuse teenus > Seadistamine > Kuluarvestuse teenuse parameetrid > Integratsiooni parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="803be-153">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="803be-154">Sisestage väljale **Avalduse ID** järgmine kood:</span><span class="sxs-lookup"><span data-stu-id="803be-154">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="803be-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="803be-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="803be-156">Sisestage väljale **Andmeteenuse lõpp-punkt** järgmine URL:</span><span class="sxs-lookup"><span data-stu-id="803be-156">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="803be-157">Sisestage väljale **Kuluarvestuse teenuse lõpp-punkt** järgmine URL:</span><span class="sxs-lookup"><span data-stu-id="803be-157">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="803be-158">Kuluarvestuse teenus on nüüd kasutamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="803be-158">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="803be-159">Seotud ressursid</span><span class="sxs-lookup"><span data-stu-id="803be-159">Related resources</span></span>

[<span data-ttu-id="803be-160">Kuluarvestuse teenuse avaleht</span><span class="sxs-lookup"><span data-stu-id="803be-160">Cost accounting service home page</span></span>](cost-accounting-service-home.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]