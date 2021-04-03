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
ms.openlocfilehash: b34f156642b23f7b9754dac1ee81c7d0004872d8
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478184"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="49587-103">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="49587-103">Enable location-based store detection</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="49587-104">Selles teemas kirjeldatakse, kuidas lülitada rakenduse Dynamics 365 Commerce saidil sisse asukohapõhine poetuvastus.</span><span class="sxs-lookup"><span data-stu-id="49587-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="49587-105">Commerce’i asukohapõhine poetuvastus võimaldab pakkuda klientidele asjakohast saidi sisu vastavalt nende asukohale.</span><span class="sxs-lookup"><span data-stu-id="49587-105">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="49587-106">Kui asukohapõhine poetuvastus on sisse lülitatud, kasutab Commerce’i renderdusteenus kliendi veebibrauseri IP-aadressi riigi/piirkonna teavet, et suunata klient parima saadaoleva geograafilise saidi konfiguratsiooni juurde.</span><span class="sxs-lookup"><span data-stu-id="49587-106">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="49587-107">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="49587-107">Privacy notice</span></span>

<span data-ttu-id="49587-108">Kui lülitate asukohapõhise poetuvastuse funktsiooni sisse, saadetakse kliendi brauseri teave Microsofti asukoha teenusele.</span><span class="sxs-lookup"><span data-stu-id="49587-108">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="49587-109">Seda teavet kasutatakse siis, et pakkuda kliendile sisu, mis on tema asukohaga seotud.</span><span class="sxs-lookup"><span data-stu-id="49587-109">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="49587-110">Nii kliendi brauserist saadetud teabele kui ka kliendilt saadud asukohapõhisele teabele kehtivad privaatsuse ja küpsiste vastavuse poliitikad.</span><span class="sxs-lookup"><span data-stu-id="49587-110">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="49587-111">Asukohapõhise poetuvastuse sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="49587-111">Turn on location-based store detection</span></span>

<span data-ttu-id="49587-112">Asukohapõhise poetuvastuse sisselülitamiseks Commerce’is toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="49587-112">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="49587-113">Avage autorluse tööriistas oma sait.</span><span class="sxs-lookup"><span data-stu-id="49587-113">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="49587-114">Valige navigeerimispaanilt vasakult suvand **Saidi haldus**.</span><span class="sxs-lookup"><span data-stu-id="49587-114">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="49587-115">Valige **Saidi sätted**.</span><span class="sxs-lookup"><span data-stu-id="49587-115">Select **Site Settings**.</span></span>
1. <span data-ttu-id="49587-116">Seadke suvand **Luba asukohapõhine poetuvastus** olekusse **Sees**.</span><span class="sxs-lookup"><span data-stu-id="49587-116">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="49587-117">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="49587-117">Additional resources</span></span>

[<span data-ttu-id="49587-118">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="49587-118">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="49587-119">Uue e-kaubanduse rentniku juurutamine</span><span class="sxs-lookup"><span data-stu-id="49587-119">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="49587-120">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="49587-120">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="49587-121">Dynamics 365 Commerce'i saidi seostamine võrgukanaliga</span><span class="sxs-lookup"><span data-stu-id="49587-121">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="49587-122">Robots.txt-failide haldamine</span><span class="sxs-lookup"><span data-stu-id="49587-122">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="49587-123">Üleslaadimise URL suunab ümber hulgi</span><span class="sxs-lookup"><span data-stu-id="49587-123">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="49587-124">B2C rentniku seadistus Kaubanduses</span><span class="sxs-lookup"><span data-stu-id="49587-124">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="49587-125">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="49587-125">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="49587-126">Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas</span><span class="sxs-lookup"><span data-stu-id="49587-126">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="49587-127">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="49587-127">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
