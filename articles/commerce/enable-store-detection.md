---
title: Asukohapõhise poetuvastuse lubamine
description: Selles teemas kirjeldatakse, kuidas lülitada rakenduse Dynamics 365 Commerce saidil sisse asukohapõhine poetuvastus.
author: brianshook
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c5fb59a9798e2cddfb75b71235ee7754e54b0e28
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945763"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="54807-103">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="54807-103">Enable location-based store detection</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="54807-104">Selles teemas kirjeldatakse, kuidas lülitada rakenduse Dynamics 365 Commerce saidil sisse asukohapõhine poetuvastus.</span><span class="sxs-lookup"><span data-stu-id="54807-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="54807-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="54807-105">Overview</span></span>

<span data-ttu-id="54807-106">Commerce’i asukohapõhine poetuvastus võimaldab pakkuda klientidele asjakohast saidi sisu vastavalt nende asukohale.</span><span class="sxs-lookup"><span data-stu-id="54807-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="54807-107">Kui asukohapõhine poetuvastus on sisse lülitatud, kasutab Commerce’i renderdusteenus kliendi veebibrauseri IP-aadressi riigi/piirkonna teavet, et suunata klient parima saadaoleva geograafilise saidi konfiguratsiooni juurde.</span><span class="sxs-lookup"><span data-stu-id="54807-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="54807-108">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="54807-108">Privacy notice</span></span>

<span data-ttu-id="54807-109">Kui lülitate asukohapõhise poetuvastuse funktsiooni sisse, saadetakse kliendi brauseri teave Microsofti asukoha teenusele.</span><span class="sxs-lookup"><span data-stu-id="54807-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="54807-110">Seda teavet kasutatakse siis, et pakkuda kliendile sisu, mis on tema asukohaga seotud.</span><span class="sxs-lookup"><span data-stu-id="54807-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="54807-111">Nii kliendi brauserist saadetud teabele kui ka kliendilt saadud asukohapõhisele teabele kehtivad privaatsuse ja küpsiste vastavuse poliitikad.</span><span class="sxs-lookup"><span data-stu-id="54807-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="54807-112">Asukohapõhise poetuvastuse sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="54807-112">Turn on location-based store detection</span></span>

<span data-ttu-id="54807-113">Asukohapõhise poetuvastuse sisselülitamiseks Commerce’is toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="54807-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="54807-114">Avage autorluse tööriistas oma sait.</span><span class="sxs-lookup"><span data-stu-id="54807-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="54807-115">Valige navigeerimispaanilt vasakult suvand **Saidi haldus**.</span><span class="sxs-lookup"><span data-stu-id="54807-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="54807-116">Valige **Saidi sätted**.</span><span class="sxs-lookup"><span data-stu-id="54807-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="54807-117">Seadke suvand **Luba asukohapõhine poetuvastus** olekusse **Sees**.</span><span class="sxs-lookup"><span data-stu-id="54807-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="54807-118">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="54807-118">Additional resources</span></span>

[<span data-ttu-id="54807-119">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="54807-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="54807-120">Uue e-kaubanduse saidi juurutamine</span><span class="sxs-lookup"><span data-stu-id="54807-120">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="54807-121">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="54807-121">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="54807-122">Veebisaidi seostamine kanaliga</span><span class="sxs-lookup"><span data-stu-id="54807-122">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="54807-123">Robots.txt-failide haldamine</span><span class="sxs-lookup"><span data-stu-id="54807-123">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="54807-124">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="54807-124">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="54807-125">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="54807-125">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
