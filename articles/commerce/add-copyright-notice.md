---
title: Autoriõiguste teatise lisamine
description: Selles teemas kirjeldatakse kuidas oma e-kaubanduse veebisaidile autoriõiguse teatist lisada.
author: psimolin
manager: AnnBe
ms.date: 04/13/2020
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
ms.openlocfilehash: a2ed52dbd19508e07fcced92a7fad831180b1d1d
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269586"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="2d3bf-103">Autoriõiguste teatise lisamine</span><span class="sxs-lookup"><span data-stu-id="2d3bf-103">Add a copyright notice</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2d3bf-104">Selles teemas kirjeldatakse kuidas oma e-kaubanduse veebisaidile autoriõiguse teatist lisada.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2d3bf-105">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="2d3bf-105">Prerequisites</span></span>

<span data-ttu-id="2d3bf-106">Enne saidile autoriõiguse teatise lisamist peavad teil olema järgmised üksused.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="2d3bf-107">Jagatud jaluse fragmenti sisaldav mall.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="2d3bf-108">Seda malli kasutav leht.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="2d3bf-109">Autoriõiguste teatise lisamine</span><span class="sxs-lookup"><span data-stu-id="2d3bf-109">Add a copyright notice</span></span>

<span data-ttu-id="2d3bf-110">Iga konkreetset malli kasutava lehe allossa autoriõiguse teatise lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="2d3bf-111">Avage suvand **Fragmendid** ja valige seejärel **Uus lehe fragment**.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-111">Go to **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="2d3bf-112">Valige dialoogiaknas moodul **Jalus** ja andke fragmendile nimi.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-112">In the dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="2d3bf-113">Sisestage näiteks **Jalus-autoriõigus**.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="2d3bf-114">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-114">Select **OK**.</span></span>
1. <span data-ttu-id="2d3bf-115">Navigeerimispaanil valige kolmikpunkti nupp (**...**) suvandi **Jalus** kõrval ja valige seejärel **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="2d3bf-116">Dialoogiaknas valige suvand **Jaluse kategooria** ja seejärel valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="2d3bf-117">Navigeerimispaanil valige kolmikpunkti nupp suvandi **Jaluse kategooria** kõrval ja valige seejärel **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="2d3bf-118">Dialoogiaknas valige suvand **Tekstiplokk** ja seejärel valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-118">In the dialog box, select **Text block**, and then select **OK**.</span></span>
1. <span data-ttu-id="2d3bf-119">Valige navigeerimispaanil **Tekstiplokk**.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-119">In the navigation pane, select **Text block**.</span></span>
1. <span data-ttu-id="2d3bf-120">Lisage paremal atribuutide paanil väljale **Lõik** oma autoriõiguse sõnum.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="2d3bf-121">Sisestage näiteks **(C) Fabrikam 2019**.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="2d3bf-122">Valige **Salvesta**, valige **Lõpeta redigeerimine** ja valige seejärel **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-122">Select **Save**, select **Finish editing**, and then select **Publish**.</span></span>
1. <span data-ttu-id="2d3bf-123">Valige suvand **Mallid**, valige mall ja seejärel käsk **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-123">Go to **Templates**, select the template, and then select **Edit**.</span></span>
1. <span data-ttu-id="2d3bf-124">Jaotises **Lehe liigendus** laiendage suvandit **Kehatekst** ja laiendage seejärel suvandit **Vaikeleht**.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="2d3bf-125">Valige suvandi **Jaluse pesa** kõrval kolmikpunkti nupp ja seejärel valige käsk **Lisa fragment**.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="2d3bf-126">Valige varem loodud fragment ja seejärel valige käsk **Vali**.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="2d3bf-127">Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-127">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="2d3bf-128">Autoriõiguse teatist sisaldav jalus kuvatakse automaatselt kõigi valitud malli kasutavate lehtede allosas.</span><span class="sxs-lookup"><span data-stu-id="2d3bf-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2d3bf-129">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="2d3bf-129">Additional resources</span></span>

[<span data-ttu-id="2d3bf-130">Logo lisamine</span><span class="sxs-lookup"><span data-stu-id="2d3bf-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="2d3bf-131">Saidi kujunduse valimine</span><span class="sxs-lookup"><span data-stu-id="2d3bf-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="2d3bf-132">CSS-i alistusfailidega töötamine</span><span class="sxs-lookup"><span data-stu-id="2d3bf-132">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="2d3bf-133">Leheikooni lisamine</span><span class="sxs-lookup"><span data-stu-id="2d3bf-133">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="2d3bf-134">Tervitussõnumi lisamine</span><span class="sxs-lookup"><span data-stu-id="2d3bf-134">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="2d3bf-135">Saidile keelte lisamine</span><span class="sxs-lookup"><span data-stu-id="2d3bf-135">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="2d3bf-136">Telemeetria toetamiseks saidile skriptikoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="2d3bf-136">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

