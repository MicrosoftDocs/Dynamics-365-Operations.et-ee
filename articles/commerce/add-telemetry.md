---
title: Telemeetria toetamiseks saidile skriptikoodi lisamine
description: Selles teemas kirjeldatakse saidi lehtedele kliendipoolse skriptikoodi lisamist, et toetada kliendipoolset telemeetriat.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 674d00faf1b30f87a0b0062129e1b9fbff955dd4
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001273"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="b65d2-103">Telemeetria toetamiseks saidile skriptikoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="b65d2-103">Add script code to site pages to support telemetry</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b65d2-104">Selles teemas kirjeldatakse saidi lehtedele kliendipoolse skriptikoodi lisamist, et toetada kliendipoolset telemeetriat.</span><span class="sxs-lookup"><span data-stu-id="b65d2-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="b65d2-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="b65d2-105">Overview</span></span>

<span data-ttu-id="b65d2-106">Veebianalüüs on oluline tööriist, kui soovite mõista, kuidas kliendid teie saidiga suhtlevad, ja teha otsuseid, mis aitavad maksimaalse teisenduse kogemust optimeerida.</span><span class="sxs-lookup"><span data-stu-id="b65d2-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="b65d2-107">Saadaval on palju veebianalüüsi pakette, et aidata teid nende eesmärkide saavutamisel, nagu Google Analytics, Clicky, Moz Analytics ja KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="b65d2-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="b65d2-108">Enamik veebianalüüsi pakette nõuavad, et lisaksite oma saidi kõikidele lehtedele HTML-i elemendile **\<head\>** kliendipoolse skriptikoodi.</span><span class="sxs-lookup"><span data-stu-id="b65d2-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="b65d2-109">Selle teema juhised rakenduvad ka teistele kohandatud kliendipoolsetele funktsioonidele, mida Microsoft Dynamics 365 Commerce ei paku.</span><span class="sxs-lookup"><span data-stu-id="b65d2-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="b65d2-110">Skriptikoodi jaoks taaskasutatava fragmendi loomine</span><span class="sxs-lookup"><span data-stu-id="b65d2-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="b65d2-111">Pärast seda, kui loote oma skriptikoodi jaoks fragmenti, saate seda oma saidil kõikidel lehtedel uuesti kasutada.</span><span class="sxs-lookup"><span data-stu-id="b65d2-111">After you create a fragment for your script code, it can be reused across all pages on your site.</span></span>

1. <span data-ttu-id="b65d2-112">Avage **Fragmendid \> Uus lehe fragment**.</span><span class="sxs-lookup"><span data-stu-id="b65d2-112">Go to **Fragments \> New page fragment**.</span></span>
2. <span data-ttu-id="b65d2-113">Valige suvand **Väline skript**, sisestage fragmendi nimi ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="b65d2-113">Select **External Script**, enter a name for the fragment, and then select **OK**.</span></span>
3. <span data-ttu-id="b65d2-114">Valige fragmendi hierarhias äsja loodud fragmenti jaoks **skripti sisestaja** mooduli alam.</span><span class="sxs-lookup"><span data-stu-id="b65d2-114">In the fragment hierarchy, select the **script injector** module child of the fragment that you just created.</span></span>
4. <span data-ttu-id="b65d2-115">Lisage parempoolsel atribuudipaanil oma kliendipoolne skript ja määrake vastavalt vajadusele teised konfiguratsiooni suvandid.</span><span class="sxs-lookup"><span data-stu-id="b65d2-115">In the property pane on the right, add your client-side script, and set other configuration options as you require.</span></span>

## <a name="add-the-fragment-to-templates"></a><span data-ttu-id="b65d2-116">Mallile fragmendi lisamine</span><span class="sxs-lookup"><span data-stu-id="b65d2-116">Add the fragment to templates</span></span>

1. <span data-ttu-id="b65d2-117">Avage **Mallid** ja avage lehtede mall, millele soovite oma skriptikoodi lisada.</span><span class="sxs-lookup"><span data-stu-id="b65d2-117">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
2. <span data-ttu-id="b65d2-118">Laiendage vasakpoolsel paanil malli hierarhiat, et kuvada pesa **HTML-i pea**.</span><span class="sxs-lookup"><span data-stu-id="b65d2-118">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
3. <span data-ttu-id="b65d2-119">Valige pesa **HTML-i päis** jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa fragment**.</span><span class="sxs-lookup"><span data-stu-id="b65d2-119">Select the ellipsis button (**...**) for the **HTML Head** slot, and then select **Add fragment**.</span></span>
4. <span data-ttu-id="b65d2-120">Valige fragment, mille lõite oma skriptikoodi jaoks.</span><span class="sxs-lookup"><span data-stu-id="b65d2-120">Select the fragment that you created for your script code.</span></span>
5. <span data-ttu-id="b65d2-121">Salvestage mall ja registreerige see.</span><span class="sxs-lookup"><span data-stu-id="b65d2-121">Save the template, and check it in.</span></span>

> [!NOTE]
> <span data-ttu-id="b65d2-122">Pärast lõpetamist peate fragmendi ja põhimalli avaldama.</span><span class="sxs-lookup"><span data-stu-id="b65d2-122">After you've finished, you must publish the fragment and the master template.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="b65d2-123">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b65d2-123">Additional resources</span></span>

[<span data-ttu-id="b65d2-124">Logo lisamine</span><span class="sxs-lookup"><span data-stu-id="b65d2-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="b65d2-125">Saidi kujunduse valimine</span><span class="sxs-lookup"><span data-stu-id="b65d2-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="b65d2-126">CSS-i alistusfailidega töötamine</span><span class="sxs-lookup"><span data-stu-id="b65d2-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="b65d2-127">Leheikooni lisamine</span><span class="sxs-lookup"><span data-stu-id="b65d2-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="b65d2-128">Tervitussõnumi lisamine</span><span class="sxs-lookup"><span data-stu-id="b65d2-128">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="b65d2-129">Autoriõiguste teatise lisamine</span><span class="sxs-lookup"><span data-stu-id="b65d2-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="b65d2-130">Saidile keelte lisamine</span><span class="sxs-lookup"><span data-stu-id="b65d2-130">Add languages to your site</span></span>](add-languages-to-site.md)

