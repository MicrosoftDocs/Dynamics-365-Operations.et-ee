---
title: Varahalduse mobiilse tööruumi häälestamine
description: Selles teemas kirjeldatakse, kuidas häälestada rakendus Microsoft Dynamics 365 Supply Chain Management ja mobiilirakendus Finance and Operations (Dynamics 365) käitama varahalduse mobiilset tööruumi, mida töötajad saavad kasutada varahalduse ülesannete täitmiseks.
author: johanhoffmann
manager: tfehr
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 54da27a022dcc800438b96224370228aa8eed261
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226143"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a><span data-ttu-id="2895a-103">Varahalduse mobiilse tööruumi häälestamine</span><span class="sxs-lookup"><span data-stu-id="2895a-103">Set up the Asset management mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2895a-104">Selles teemas kirjeldatakse, kuidas häälestada rakendus Microsoft Dynamics 365 Supply Chain Management ja mobiilirakendus Finance and Operations (Dynamics 365) käitama mobiilset tööruumi **Varahaldus**, mida töötajad saavad kasutada varahalduse ülesannete täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="2895a-104">This topic describes how to set up Microsoft Dynamics 365 Supply Chain Management and the Finance and Operations (Dynamics 365) mobile app to run an **Asset management** mobile workspace that workers can use to perform asset management tasks.</span></span>

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a><span data-ttu-id="2895a-105">Hooldustöötajate häälestamine teenuses Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="2895a-105">Set up maintenance worker users in Supply Chain Management</span></span>

<span data-ttu-id="2895a-106">Iga kasutaja kes vajab juurdepääsu **varahalduse** mobiilsele tööruumile, järgib järgmisi juhiseid.</span><span class="sxs-lookup"><span data-stu-id="2895a-106">For each user that requires access to the **Asset management** mobile workspace, follow these steps.</span></span>

1. <span data-ttu-id="2895a-107">Avage teenuses Supply Chain Management suvand **Inimressursid \> Töötajad** ja veenduge, et kasutaja jaoks, kellele soovite selle häälestada, oleks töötaja kirje olemas.</span><span class="sxs-lookup"><span data-stu-id="2895a-107">In Supply Chain Management, go to **Human resources \> Workers**, and make sure that a worker record exists for the user that you want to set up.</span></span> <span data-ttu-id="2895a-108">Looge vajaduse korral uus töötaja kirje.</span><span class="sxs-lookup"><span data-stu-id="2895a-108">Create a new worker record as required.</span></span>
1. <span data-ttu-id="2895a-109">Avage **Varahaldus \> Seadistus \> Töötajad \> Töötajad** ja veenduge, et töötaja kirje, mille te eelmises etapid tuvastasite (või lõite), oleks vastendatud hooldustöötaja kirjega.</span><span class="sxs-lookup"><span data-stu-id="2895a-109">Go to **Asset management \> Setup \> Workers \> Workers**, and make sure that the worker record that you identified (or created) in the previous step is mapped to a maintenance worker record.</span></span> <span data-ttu-id="2895a-110">Looge vajaduse korral uus hooldustöötaja kirje ja määrake väli **Töötaja** eelmise etapi töötaja kirjele.</span><span class="sxs-lookup"><span data-stu-id="2895a-110">Create a new maintenance worker record as required, and set the **Worker** field to the worker record from the previous step.</span></span>
1. <span data-ttu-id="2895a-111">Avage **Varahaldus \> Seadistus \> Töötajad \> Hooldustöötajate grupid** ja veenduge, et hooldustöötaja kirje, mille te eelmises etapid tuvastasite (või lõite), kuuluks hooldustöötajate gruppi.</span><span class="sxs-lookup"><span data-stu-id="2895a-111">Go to **Asset management \> Setup \> Workers \> Maintenance worker groups**, and make sure that the maintenance worker record that you identified (or created) in the previous step belongs to a maintenance worker group.</span></span>
1. <span data-ttu-id="2895a-112">Avage **Süsteemihaldus \> Kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="2895a-112">Go to **System administration \> Users**.</span></span>
1. <span data-ttu-id="2895a-113">Valige ruudustikust asjakohane kasutaja.</span><span class="sxs-lookup"><span data-stu-id="2895a-113">Select the relevant user in the grid.</span></span>
1. <span data-ttu-id="2895a-114">Määrake kiirkaardil **Kasutaja üksikasjad** väli **Isik** töötaja kontole, kelle soovite praeguse kasutajakontoga seostada.</span><span class="sxs-lookup"><span data-stu-id="2895a-114">On the **User Details** FastTab, set the **Person** field to the worker account that you want to associate with the current user account.</span></span> <span data-ttu-id="2895a-115">See töötaja konto peaks olema töötaja kirje, mille 1. etapis tuvastasite (või lõite) ja vastendasite hooldustöötaja kirjega 2. etapis.</span><span class="sxs-lookup"><span data-stu-id="2895a-115">This worker account should be the worker record that you identified (or created) in step 1 and mapped to a maintenance worker record in step 2.</span></span>

> [!NOTE]
> <span data-ttu-id="2895a-116">Kasutajaõigused ja turberollid rakenduvad mobiilse tööruumi **Varahaldus** funktsioonidele samamoodi nagu need rakenduvad teenuse Supply Chain Management kasutajaliidese funktsioonidele.</span><span class="sxs-lookup"><span data-stu-id="2895a-116">User permissions and security roles apply to the features of the **Asset management** mobile workspace just as they apply to the features of the Supply Chain Management user interface.</span></span> <span data-ttu-id="2895a-117">Seetõttu peavad igal kasutajal, kelle jaoks mobiilse tööruumi **Varahaldus** juurdepääsu häälestate, omama turberolle, mis on vajalikud sarnaste toimingute tegemiseks otse teenuses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2895a-117">Therefore, every user that you set up to access the **Asset management** mobile workspace must have the security roles that are required to perform similar operations directly in Supply Chain Management.</span></span>

## <a name="publish-the-asset-management-mobile-workspace"></a><span data-ttu-id="2895a-118">Varahalduse mobiilse tööruumi avaldamine</span><span class="sxs-lookup"><span data-stu-id="2895a-118">Publish the Asset management mobile workspace</span></span>

<span data-ttu-id="2895a-119">Varahalduse funktsioonide mobiilirakenduses Finance and Operations (Dynamics 365) kättesaadavaks tegemiseks peate avaldama mobiilse tööruumi **Varahaldus**.</span><span class="sxs-lookup"><span data-stu-id="2895a-119">To make asset management features available in the Finance and Operations (Dynamics 365) mobile app, you must publish the **Asset management** mobile workspace.</span></span>

1. <span data-ttu-id="2895a-120">Valige teenuses Supply Chain Management nupp **Sätted** (ülemises parempoolses nurgas olev hammasratta sümbol) ja valige seejärel menüüst suvand **Mobiilirakendus**.</span><span class="sxs-lookup"><span data-stu-id="2895a-120">In Supply Chain Management, select the **Settings** button (the gear symbol in upper-right corner), and then select **Mobile app** on the menu.</span></span>
1. <span data-ttu-id="2895a-121">Leidke dialoogiboksis **Mobiilirakenduse haldamine** paan **Varahaldus**.</span><span class="sxs-lookup"><span data-stu-id="2895a-121">In the **Manage mobile app** dialog box, find the **Asset Management** tile.</span></span> <span data-ttu-id="2895a-122">Kui see sisaldab teksti „Metaandmetes – pole avaldatud”, ei ole tööruumi veel avaldatud.</span><span class="sxs-lookup"><span data-stu-id="2895a-122">If it contains the text "In metadata - not published," the workspace hasn't yet been published.</span></span> <span data-ttu-id="2895a-123">Kui see sisaldab teksti „Metaandmetes - avaldatud”, on tööruum juba avaldatud ja saate selle protseduuri ülejäänud osa vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="2895a-123">If it contains the text "In metadata - published," the workspace has already been published, and you can skip the rest of this procedure.</span></span>

    <span data-ttu-id="2895a-124">![Dialoogiboks Mobiilirakenduse haldamine](media/mobile-workspaces.png "Dialoogiboks Mobiilirakenduse haldamine")</span><span class="sxs-lookup"><span data-stu-id="2895a-124">![Manage mobile app dialog box](media/mobile-workspaces.png "Manage mobile app dialog box")</span></span>

1. <span data-ttu-id="2895a-125">Valige paan **Varahaldus** ja valige seejärel tööriistaribal käsk **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="2895a-125">Select the **Asset Management** tile, and then select **Publish** on the toolbar.</span></span> <span data-ttu-id="2895a-126">Mõne sekundi pärast peaksite saama teatise, mis ütleb, et tööruum on avaldatud.</span><span class="sxs-lookup"><span data-stu-id="2895a-126">After a few seconds, you should receive a notification that states that the workspace has been successfully published.</span></span> <span data-ttu-id="2895a-127">Lisaks peaks paanil olev tekst muutuma variandile „Metaandmetes – avaldatud”.</span><span class="sxs-lookup"><span data-stu-id="2895a-127">Additionally, the text on the tile should change to "In metadata - published."</span></span>

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a><span data-ttu-id="2895a-128">Mobiilirakenduse Finance and Operations (Dynamics 365) installimine ja häälestamine</span><span class="sxs-lookup"><span data-stu-id="2895a-128">Install and set up the Finance and Operations (Dynamics 365) mobile app</span></span>

1. <span data-ttu-id="2895a-129">Avage üks järgmistest rakendusepoodidest, et installida rakendus **Microsoft Finance and Operations (Dynamics 365)** oma mobiilseadmesse.</span><span class="sxs-lookup"><span data-stu-id="2895a-129">Go to one of the following app stores to install the **Microsoft Finance and Operations (Dynamics 365)** app on your mobile device:</span></span>

    - [<span data-ttu-id="2895a-130">Google’i Androidi seadmed</span><span class="sxs-lookup"><span data-stu-id="2895a-130">For Google Android devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
    - [<span data-ttu-id="2895a-131">Apple’i iOS-i seadmed</span><span class="sxs-lookup"><span data-stu-id="2895a-131">For Apple iOS devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

1. <span data-ttu-id="2895a-132">Avage rakendus Finance and Operations (Dynamics 365).</span><span class="sxs-lookup"><span data-stu-id="2895a-132">Open the Finance and Operations (Dynamics 365) app.</span></span> <span data-ttu-id="2895a-133">Ilmuma peaks sisselogimisleht.</span><span class="sxs-lookup"><span data-stu-id="2895a-133">The sign-in page should appear.</span></span> <span data-ttu-id="2895a-134">Sisestage **sisselogimise** väljale oma Supply Chain Managementi URL või valige loendist **Hiljutised keskkonnad** hiljutine URL ja puudutage seejärel valikut **Ühenda**.</span><span class="sxs-lookup"><span data-stu-id="2895a-134">In the **Sign in** field, enter your Supply Chain Management URL, or select a recent URL in the **Recent environments** list, and then tap **Connect**.</span></span>

    <span data-ttu-id="2895a-135">![Sisselogimise leht](media/mobile-app-sign-in.png "Sisselogimise leht")</span><span class="sxs-lookup"><span data-stu-id="2895a-135">![Sign-in page](media/mobile-app-sign-in.png "Sign-in page")</span></span>

1. <span data-ttu-id="2895a-136">Kui teil palutakse ühendus kinnitada, märkige ruut **Ma mõistan** ja puudutage suvandit **Ühenda**.</span><span class="sxs-lookup"><span data-stu-id="2895a-136">If you're prompted to confirm the connection, select the **I understand** check box, and then tap **Connect**.</span></span>
1. <span data-ttu-id="2895a-137">Kasutage lehel **Konto valimine** oma Microsofti kontot mobiilirakendusse sisselogimiseks.</span><span class="sxs-lookup"><span data-stu-id="2895a-137">On the **Pick an account** page, use your Microsoft account to sign in to the mobile application.</span></span>

    <span data-ttu-id="2895a-138">Kuvatakse leht **Tööruumid**.</span><span class="sxs-lookup"><span data-stu-id="2895a-138">The **Workspaces** page appears.</span></span> <span data-ttu-id="2895a-139">See loetleb kõik mobiilsed tööruumid, mille teie Supply Chain Managementi eksemplar on avaldanud.</span><span class="sxs-lookup"><span data-stu-id="2895a-139">It lists every mobile workspace that has been published by your Supply Chain Management instance.</span></span>

    <span data-ttu-id="2895a-140">![Tööruumide loend](media/mobile-app-workspaces.png "Tööruumide loend")</span><span class="sxs-lookup"><span data-stu-id="2895a-140">![List of workspaces](media/mobile-app-workspaces.png "List of workspaces")</span></span>

1. <span data-ttu-id="2895a-141">Kui peate juriidilist isikut (ettevõtet) muutma, puudutage ülemises vasakpoolses nurgas nuppu Menüü (vahel viidatakse sellele kui hamburger või hamburgeri nupp) ja puudutage seejärel nuppu **Muuda ettevõtet**.</span><span class="sxs-lookup"><span data-stu-id="2895a-141">If you must change the legal entity (company), tap the Menu button (sometimes referred to as the hamburger or the hamburger button) in the upper-left corner, and then tap **Change company**.</span></span>

    <span data-ttu-id="2895a-142">![Juriidilise isiku muutmine](media/mobile-app-change-comp.png "Juriidilise isiku muutmine")</span><span class="sxs-lookup"><span data-stu-id="2895a-142">![Changing the legal entity](media/mobile-app-change-comp.png "Changing the legal entity")</span></span>

1. <span data-ttu-id="2895a-143">Lehel **Tööruumid** valige avamiseks tööruum, millega soovite töötada.</span><span class="sxs-lookup"><span data-stu-id="2895a-143">On the **Workspaces** page, select the workspace that you want to work with to open it.</span></span>

    <span data-ttu-id="2895a-144">![Varahalduse mobiilne tööruum](media/mobile-app-asset-workspace.png "Varahalduse mobiilne tööruum")</span><span class="sxs-lookup"><span data-stu-id="2895a-144">![Asset management mobile workspace](media/mobile-app-asset-workspace.png "Asset management mobile workspace")</span></span>

## <a name="work-with-the-asset-management-mobile-workspace"></a><span data-ttu-id="2895a-145">Varahalduse mobiilse tööruumiga töötamine</span><span class="sxs-lookup"><span data-stu-id="2895a-145">Work with the Asset management mobile workspace</span></span>

<span data-ttu-id="2895a-146">Lisateavet selle kohta, kuidas mobiilse tööruumiga **Varahaldus** töötada, vt teemat [Varahalduse mobiilse tööruumi kasutamine](asset-management-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="2895a-146">For more information about how to work with the **Asset management** mobile workspace, see [Use the Asset management mobile workspace](asset-management-mobile-workspace.md).</span></span>

<span data-ttu-id="2895a-147">Lisateavet mobiilirakenduse Finance and Operations (Dynamics 365) kohta vt [mobiilirakenduse kodulehelt](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="2895a-147">For more information about the Finance and Operations (Dynamics 365) mobile app, see the [Mobile app home page](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]