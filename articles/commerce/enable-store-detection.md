---
title: Asukohapõhise poetuvastuse lubamine
description: Selles teemas kirjeldatakse, kuidas lülitada rakenduse Dynamics 365 Commerce saidil sisse asukohapõhine poetuvastus.
author: brianshook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3f7e9a3acde508f405ce85f125db552c3ae3656b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000718"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="c4a1e-103">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="c4a1e-103">Enable location-based store detection</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c4a1e-104">Selles teemas kirjeldatakse, kuidas lülitada rakenduse Dynamics 365 Commerce saidil sisse asukohapõhine poetuvastus.</span><span class="sxs-lookup"><span data-stu-id="c4a1e-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="c4a1e-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="c4a1e-105">Overview</span></span>

<span data-ttu-id="c4a1e-106">Commerce’i asukohapõhine poetuvastus võimaldab pakkuda klientidele asjakohast saidi sisu vastavalt nende asukohale.</span><span class="sxs-lookup"><span data-stu-id="c4a1e-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="c4a1e-107">Kui asukohapõhine poetuvastus on sisse lülitatud, kasutab Commerce’i renderdusteenus kliendi veebibrauseri IP-aadressi riigi/piirkonna teavet, et suunata klient parima saadaoleva geograafilise saidi konfiguratsiooni juurde.</span><span class="sxs-lookup"><span data-stu-id="c4a1e-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="c4a1e-108">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="c4a1e-108">Privacy notice</span></span>

<span data-ttu-id="c4a1e-109">Kui lülitate asukohapõhise poetuvastuse funktsiooni sisse, saadetakse kliendi brauseri teave Microsofti asukoha teenusele.</span><span class="sxs-lookup"><span data-stu-id="c4a1e-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="c4a1e-110">Seda teavet kasutatakse siis, et pakkuda kliendile sisu, mis on tema asukohaga seotud.</span><span class="sxs-lookup"><span data-stu-id="c4a1e-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="c4a1e-111">Nii kliendi brauserist saadetud teabele kui ka kliendilt saadud asukohapõhisele teabele kehtivad privaatsuse ja küpsiste vastavuse poliitikad.</span><span class="sxs-lookup"><span data-stu-id="c4a1e-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="c4a1e-112">Asukohapõhise poetuvastuse sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="c4a1e-112">Turn on location-based store detection</span></span>

<span data-ttu-id="c4a1e-113">Asukohapõhise poetuvastuse sisselülitamiseks Commerce’is toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="c4a1e-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="c4a1e-114">Avage autorluse tööriistas oma sait.</span><span class="sxs-lookup"><span data-stu-id="c4a1e-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="c4a1e-115">Valige navigeerimispaanilt vasakult suvand **Saidi haldus**.</span><span class="sxs-lookup"><span data-stu-id="c4a1e-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="c4a1e-116">Valige **Saidi sätted**.</span><span class="sxs-lookup"><span data-stu-id="c4a1e-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="c4a1e-117">Seadke suvand **Luba asukohapõhine poetuvastus** olekusse **Sees**.</span><span class="sxs-lookup"><span data-stu-id="c4a1e-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c4a1e-118">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c4a1e-118">Additional resources</span></span>

[<span data-ttu-id="c4a1e-119">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="c4a1e-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="c4a1e-120">Uue e-kaubanduse rentniku juurutamine</span><span class="sxs-lookup"><span data-stu-id="c4a1e-120">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="c4a1e-121">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="c4a1e-121">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="c4a1e-122">Dynamics 365 Commerce'i saidi seostamine võrgukanaliga</span><span class="sxs-lookup"><span data-stu-id="c4a1e-122">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="c4a1e-123">Robots.txt-failide haldamine</span><span class="sxs-lookup"><span data-stu-id="c4a1e-123">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="c4a1e-124">Üleslaadimise URL suunab ümber hulgi</span><span class="sxs-lookup"><span data-stu-id="c4a1e-124">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="c4a1e-125">B2C rentniku seadistus Kaubanduses</span><span class="sxs-lookup"><span data-stu-id="c4a1e-125">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="c4a1e-126">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="c4a1e-126">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="c4a1e-127">Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas</span><span class="sxs-lookup"><span data-stu-id="c4a1e-127">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="c4a1e-128">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="c4a1e-128">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
