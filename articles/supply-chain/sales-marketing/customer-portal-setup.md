---
title: Kliendiportaali installimine, seadistamine ja värskendamine
description: See teema hõlmab kliendiportaali litsentside üksikasju ja seadistamise juhiseid.
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e61fc5f7151a0bb61d496d47f4ad4e727a2a1d65
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529526"
---
# <a name="install-set-up-and-update-the-customer-portal"></a><span data-ttu-id="704be-103">Kliendiportaali installimine, seadistamine ja värskendamine</span><span class="sxs-lookup"><span data-stu-id="704be-103">Install, set up, and update the Customer portal</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a><span data-ttu-id="704be-104">Litsentsimisnõuded</span><span class="sxs-lookup"><span data-stu-id="704be-104">Licensing requirements</span></span>

<span data-ttu-id="704be-105">Kliendiportaali kasutamiseks peavad teil olema järgmised litsentsid.</span><span class="sxs-lookup"><span data-stu-id="704be-105">To implement the Customer portal, you must have the following licenses:</span></span>

- <span data-ttu-id="704be-106">**Power Appsi portaalid** – see litsents on vajalik kliendiportaali majutamiseks.</span><span class="sxs-lookup"><span data-stu-id="704be-106">**Power Apps portals** – This license is required to host the Customer portal.</span></span> <span data-ttu-id="704be-107">Portaalide litsentsid põhinevad kasutusel.</span><span class="sxs-lookup"><span data-stu-id="704be-107">Portals are licensed based on usage.</span></span> <span data-ttu-id="704be-108">Lisateavet vt teemast [Power Appsi portaalide litsentsimisnõuded](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span><span class="sxs-lookup"><span data-stu-id="704be-108">For more information, see the [Power Apps portals licensing requirements](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span></span>
- <span data-ttu-id="704be-109">**Topeltkirjutus** – teil peavad olema vajalikud litsentsid, et võimaldada Supply Chain Managementi üksuste topeltkirjutust.</span><span class="sxs-lookup"><span data-stu-id="704be-109">**Dual-write** – You must have the necessary licenses to enable dual-write for Supply Chain Management entities.</span></span> <span data-ttu-id="704be-110">Lisateavet vt teemast [topeltkirjutuse süsteeminõuded](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span><span class="sxs-lookup"><span data-stu-id="704be-110">For more information, see the [system requirements for dual-write](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span></span>

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a><span data-ttu-id="704be-111">Topeltkirjutuse ja Power Appsi portaalide sõltuvused</span><span class="sxs-lookup"><span data-stu-id="704be-111">Dependencies on dual-write and Power Apps portals</span></span>

<span data-ttu-id="704be-112">Kliendiportaal sõltub Power Appsi portaalidest ja topeltkirjutusest, nagu on näidatud järgmisel pildil.</span><span class="sxs-lookup"><span data-stu-id="704be-112">The Customer portal depends on Power Apps portals and dual-write, as shown in the following illustration.</span></span>

<span data-ttu-id="704be-113">![Kliendiportaali sõltuvused](media/customer-portal-elements.png "Kliendiportaali sõltuvused")</span><span class="sxs-lookup"><span data-stu-id="704be-113">![Customer portal dependencies](media/customer-portal-elements.png "Customer portal dependencies")</span></span>

<span data-ttu-id="704be-114">Erinevalt teenuse Supply Chain Management teistest funktsioonidest paikneb kliendiportaali mall Power Appsi portaalides.</span><span class="sxs-lookup"><span data-stu-id="704be-114">Unlike other features from Supply Chain Management, the Customer portal template resides in Power Apps portals.</span></span> <span data-ttu-id="704be-115">Seega on kliendiportaali funktsionaalsus ja võimalused piiratud Power Appsi portaalide ning topeltkirjutuse üksuste pakutavatega.</span><span class="sxs-lookup"><span data-stu-id="704be-115">Therefore, the Customer portal is limited by the functionality and capabilities that are provided by Power Apps portals and the entities in dual-write.</span></span>

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a><span data-ttu-id="704be-116">Vajalikud seadistused kliendiportaali lubamiseks</span><span class="sxs-lookup"><span data-stu-id="704be-116">Required setup to enable the Customer portal</span></span>

<span data-ttu-id="704be-117">Kui olete veendunud, et teil on vajalikud litsentsid, siis võite seadistada topeltkirjutamise, nagu on kirjeldatud jaotises [topeltkirjutamise esmase sünkroonimise juhised](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span><span class="sxs-lookup"><span data-stu-id="704be-117">After you've made sure that you have the required licenses, you can set up dual-write as described in the [dual-write initial synchronization instructions](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span></span>

<span data-ttu-id="704be-118">Veenduge, et topeltkirjutamise puhul oleksid lubatud järgmised üksuse vastendused.</span><span class="sxs-lookup"><span data-stu-id="704be-118">Be sure to enable the following entity mappings in dual-write:</span></span>

- <span data-ttu-id="704be-119">Müügitellimuse päis</span><span class="sxs-lookup"><span data-stu-id="704be-119">Sales Order Header</span></span>
- <span data-ttu-id="704be-120">Müügitellimuse üksikasjad</span><span class="sxs-lookup"><span data-stu-id="704be-120">Sales Order Details</span></span>
- <span data-ttu-id="704be-121">Kontod</span><span class="sxs-lookup"><span data-stu-id="704be-121">Accounts</span></span>
- <span data-ttu-id="704be-122">Kontaktid</span><span class="sxs-lookup"><span data-stu-id="704be-122">Contacts</span></span>
- <span data-ttu-id="704be-123">Tooted</span><span class="sxs-lookup"><span data-stu-id="704be-123">Products</span></span>

<span data-ttu-id="704be-124">Pärast seadistuse lõpule viimist saate valmistada ette kliendiportaali malli.</span><span class="sxs-lookup"><span data-stu-id="704be-124">After this setup is completed, you can provision the Customer portal template.</span></span>

## <a name="provision-the-customer-portal"></a><span data-ttu-id="704be-125">Kliendiportaali ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="704be-125">Provision the Customer portal</span></span>

<span data-ttu-id="704be-126">Enne alustamist veenduge, et oleksite [nõutud seadistused](#required-setup) juba lõpule viinud.</span><span class="sxs-lookup"><span data-stu-id="704be-126">Before you begin, make sure that you've already completed the [required setup](#required-setup).</span></span> <span data-ttu-id="704be-127">Seejärel toimige kliendiportaali ette valmistamiseks järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="704be-127">Then follow these steps to provision the Customer portal.</span></span>

1. <span data-ttu-id="704be-128">Avage [make.powerapps.com](https://make.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="704be-128">Go to [make.powerapps.com](https://make.powerapps.com/).</span></span>
2. <span data-ttu-id="704be-129">Veenduge, et kasutaksite keskkonda, kus te topeltkirjutamise lubasite.</span><span class="sxs-lookup"><span data-stu-id="704be-129">Make sure that you're using the environment where you enabled dual-write.</span></span>
3. <span data-ttu-id="704be-130">Kerige vahekaardil **Loo** allapoole kuni jaotiseni **Alusta mallist** ja valige seejärel mall nimega **Kliendiportaal**.</span><span class="sxs-lookup"><span data-stu-id="704be-130">On the **Create** tab, scroll down to the **Start from template** section, and select the template that is named **Customer Portal**.</span></span>
4. <span data-ttu-id="704be-131">Järgige ekraanil toodud juhiseid.</span><span class="sxs-lookup"><span data-stu-id="704be-131">Follow the on-screen instructions.</span></span>

<span data-ttu-id="704be-132">Pärast ettevalmistuse lõpule viimist saate avada kliendiportaali lehel **Avaleht** jaotises **Teie rakendused**.</span><span class="sxs-lookup"><span data-stu-id="704be-132">After provisioning is completed, you can access the Customer portal in the **Your apps** section of the **Home** page.</span></span>

> [!NOTE]
> <span data-ttu-id="704be-133">Kui keskkonnas, kus te töötate, ei ole paigaldatud topeltkirjutamise lahendust, siis kuvatakse teile tõrketeade ja kliendiportaali ei saa ette valmistada.</span><span class="sxs-lookup"><span data-stu-id="704be-133">If the dual-write solution isn't installed in the environment that you're working in, you will receive an error message, and the Customer portal won't be provisioned.</span></span>

## <a name="update-the-customer-portal"></a><span data-ttu-id="704be-134">Kliendiportaali uuendamine</span><span class="sxs-lookup"><span data-stu-id="704be-134">Update the Customer portal</span></span>

<span data-ttu-id="704be-135">Kliendiportaalile võidakse hiljem lisada uusi funktsioone.</span><span class="sxs-lookup"><span data-stu-id="704be-135">More functionality might be added to the Customer portal later.</span></span> <span data-ttu-id="704be-136">Kõik Microsofti tehtavad lahenduse põhikomponentide muudatused ilmuvad teie keskkonda automaatselt.</span><span class="sxs-lookup"><span data-stu-id="704be-136">Any changes that Microsoft makes to the underlying solution components will automatically appear in your environment.</span></span> <span data-ttu-id="704be-137">Samas ei kajastu teie keskkonnas ettevalmistatud veebisaidil automaatselt konfiguratsiooniandmetes tehtud muudatused.</span><span class="sxs-lookup"><span data-stu-id="704be-137">However, the website that is provisioned in your environment won't automatically reflect changes that are made to the configuration data.</span></span> <span data-ttu-id="704be-138">Need muudatused tuleb rakendada käsitsi, hankides uuest mallist koodi ja ühendades selle ettevalmistatud veebisaidiga.</span><span class="sxs-lookup"><span data-stu-id="704be-138">You will have to manually apply those changes by getting the code from the new template and merging it with the provisioned website.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="704be-139">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="704be-139">Additional resources</span></span>

<span data-ttu-id="704be-140">Kliendiportaali seadistamise ja kohandamise lähemalt tundma õppimiseks peaksite alustama alltoodud alustehnoloogiaid käsitleva dokumentatsiooni läbivaatamisest.</span><span class="sxs-lookup"><span data-stu-id="704be-140">To learn how you can set up and customize the Customer portal, you should start by reviewing the following documentation for the underlying technologies:</span></span>

- [<span data-ttu-id="704be-141">Power Appsi portaalide dokumentatsioon</span><span class="sxs-lookup"><span data-stu-id="704be-141">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="704be-142">Topeltkirjutuse dokumentatsioon</span><span class="sxs-lookup"><span data-stu-id="704be-142">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

<span data-ttu-id="704be-143">Portaalide tõhusaks haldamiseks peate mõistma Power Appsi portaalide ja Common Data Service'i töötsüklit.</span><span class="sxs-lookup"><span data-stu-id="704be-143">To effectively manage your portals, you must understand the Power Apps portals and Common Data Service lifecycle.</span></span> <span data-ttu-id="704be-144">Lisateavet vt järgmistest allikatest.</span><span class="sxs-lookup"><span data-stu-id="704be-144">For more information, see the following resources:</span></span>

- [<span data-ttu-id="704be-145">Portaali töötsükkel</span><span class="sxs-lookup"><span data-stu-id="704be-145">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="704be-146">Portaali uuendamine</span><span class="sxs-lookup"><span data-stu-id="704be-146">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="704be-147">Portaali konfiguratsiooni migreerimine</span><span class="sxs-lookup"><span data-stu-id="704be-147">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="704be-148">Lahenduse töötsükli haldus: Dynamics 365 for Customer Engagementi rakendused</span><span class="sxs-lookup"><span data-stu-id="704be-148">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)
