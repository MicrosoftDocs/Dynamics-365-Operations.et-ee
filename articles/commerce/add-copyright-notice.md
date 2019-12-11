---
title: Autoriõiguste teatise lisamine
description: Selles teemas kirjeldatakse kuidas oma e-kaubanduse veebisaidile autoriõiguse teatist lisada.
author: psimolin
manager: AnnBe
ms.date: 10/31/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 39135a2eca25336097ee9eddf06dc6709c102571
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696941"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="71c7f-103">Autoriõiguste teatise lisamine</span><span class="sxs-lookup"><span data-stu-id="71c7f-103">Add a copyright notice</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="71c7f-104">Selles teemas kirjeldatakse kuidas oma e-kaubanduse veebisaidile autoriõiguse teatist lisada.</span><span class="sxs-lookup"><span data-stu-id="71c7f-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="71c7f-105">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="71c7f-105">Prerequisites</span></span>

<span data-ttu-id="71c7f-106">Enne saidile autoriõiguse teatise lisamist peavad teil olema järgmised üksused.</span><span class="sxs-lookup"><span data-stu-id="71c7f-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="71c7f-107">Jagatud jaluse fragmenti sisaldav mall.</span><span class="sxs-lookup"><span data-stu-id="71c7f-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="71c7f-108">Seda malli kasutav leht.</span><span class="sxs-lookup"><span data-stu-id="71c7f-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="71c7f-109">Autoriõiguste teatise lisamine</span><span class="sxs-lookup"><span data-stu-id="71c7f-109">Add a copyright notice</span></span>

<span data-ttu-id="71c7f-110">Iga konkreetset malli kasutava lehe allossa autoriõiguse teatise lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="71c7f-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="71c7f-111">Avage suvand **Fragmendid** ja valige seejärel **Uus lehe fragment**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-111">Go to **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="71c7f-112">Valige dialoogiaknas moodul **Jalus** ja andke fragmendile nimi.</span><span class="sxs-lookup"><span data-stu-id="71c7f-112">In the dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="71c7f-113">Sisestage näiteks **Jalus-autoriõigus**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="71c7f-114">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-114">Select **OK**.</span></span>
1. <span data-ttu-id="71c7f-115">Navigeerimispaanil valige kolmikpunkti nupp (**...**) suvandi **Jalus** kõrval ja valige seejärel **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="71c7f-116">Dialoogiaknas valige suvand **Jaluse kategooria** ja seejärel valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="71c7f-117">Navigeerimispaanil valige kolmikpunkti nupp suvandi **Jaluse kategooria** kõrval ja valige seejärel **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="71c7f-118">Dialoogiaknas valige suvand **Sisurikka ploki üksus** ja seejärel valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-118">In the dialog box, select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="71c7f-119">Valige navigeerimispaanil suvand **Sisurikka ploki üksus**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-119">In the navigation pane, select **Content rich block item**.</span></span>
1. <span data-ttu-id="71c7f-120">Lisage paremal atribuutide paanil väljale **Lõik** oma autoriõiguse sõnum.</span><span class="sxs-lookup"><span data-stu-id="71c7f-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="71c7f-121">Sisestage näiteks **(C) Fabrikam 2019**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="71c7f-122">Valige **Salvesta**, valige **Registreeri**ja valige seejärel **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-122">Select **Save**, select **Check In**, and then select **Publish**.</span></span>
1. <span data-ttu-id="71c7f-123">Valige suvand **Mallid**, valige mall ja seejärel käsk **Registreeri välja**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-123">Go to **Templates**, select the template, and then select **Check Out**.</span></span>
1. <span data-ttu-id="71c7f-124">Jaotises **Lehe liigendus** laiendage suvandit **Kehatekst** ja laiendage seejärel suvandit **Vaikeleht**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="71c7f-125">Valige suvandi **Jaluse pesa** kõrval kolmikpunkti nupp ja seejärel valige käsk **Lisa fragment**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="71c7f-126">Valige varem loodud fragment ja seejärel valige käsk **Vali**.</span><span class="sxs-lookup"><span data-stu-id="71c7f-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="71c7f-127">Registreerige mall ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="71c7f-127">Check in the template, and publish it.</span></span>

<span data-ttu-id="71c7f-128">Autoriõiguse teatist sisaldav jalus kuvatakse automaatselt kõigi valitud malli kasutavate lehtede allosas.</span><span class="sxs-lookup"><span data-stu-id="71c7f-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71c7f-129">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="71c7f-129">Additional resources</span></span>

[<span data-ttu-id="71c7f-130">Logo lisamine</span><span class="sxs-lookup"><span data-stu-id="71c7f-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="71c7f-131">Saidi kujunduse valimine</span><span class="sxs-lookup"><span data-stu-id="71c7f-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="71c7f-132">Leheikooni lisamine</span><span class="sxs-lookup"><span data-stu-id="71c7f-132">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="71c7f-133">Tervitussõnumi lisamine</span><span class="sxs-lookup"><span data-stu-id="71c7f-133">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="71c7f-134">Saidile keelte lisamine</span><span class="sxs-lookup"><span data-stu-id="71c7f-134">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="71c7f-135">Telemeetria toetamiseks saidile skriptikoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="71c7f-135">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

