---
title: Tervitussõnumi lisamine
description: See teema kirjeldab, kuidas lisada oma Microsoft Dynamics 365 Commerce veebisaidile tervitussõnum.
author: psimolin
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4e9deeeaf491b77700ba0833e429f05d376a4392
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914512"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="aacc3-103">Tervitussõnumi lisamine</span><span class="sxs-lookup"><span data-stu-id="aacc3-103">Add a welcome message</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="aacc3-104">See teema kirjeldab, kuidas lisada oma Microsoft Dynamics 365 Commerce veebisaidile tervitussõnum.</span><span class="sxs-lookup"><span data-stu-id="aacc3-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="aacc3-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="aacc3-105">Overview</span></span>

<span data-ttu-id="aacc3-106">E-kaubanduse veebisaidi tervitussõnum võib teavitada külastajaid käimasolevatest allahindlustest, saidi uuendustest või hooajaliste kollektsioonide saadavusest.</span><span class="sxs-lookup"><span data-stu-id="aacc3-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="aacc3-107">Tervitussõnum määratakse teatisemooduli abil.</span><span class="sxs-lookup"><span data-stu-id="aacc3-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="aacc3-108">Teatisemoodul tuleks lisada päise fragmendi pessa **Tõrke-/teabeteated**.</span><span class="sxs-lookup"><span data-stu-id="aacc3-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="aacc3-109">Teatisemoodul võimaldab teil määrata kuvatava teksti, teksti värvi ja joonduse.</span><span class="sxs-lookup"><span data-stu-id="aacc3-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="aacc3-110">Samuti võimaldab see määrata, kas saidi külastajad võivad sõnumi lõpetada.</span><span class="sxs-lookup"><span data-stu-id="aacc3-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="aacc3-111">Kui jagatud päise fragmenti on lisatud tervitussõnum, kuvatakse see igal lehel, mis kasutab malli, kus seda jagatud päise fragmenti kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="aacc3-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="aacc3-112">Oma saidile tervitussõnumi lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="aacc3-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="aacc3-113">Avage rakenduses Dynamics 365 Commerce oma sait.</span><span class="sxs-lookup"><span data-stu-id="aacc3-113">In Dynamics 365 Commerce, go to your site.</span></span>
1. <span data-ttu-id="aacc3-114">Valige suvand **Fragmendid**.</span><span class="sxs-lookup"><span data-stu-id="aacc3-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="aacc3-115">Valige päise fragment, millele sõnum lisada.</span><span class="sxs-lookup"><span data-stu-id="aacc3-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="aacc3-116">Laiendage liigendpuus suvandit **Tõrke-/teabeteated**.</span><span class="sxs-lookup"><span data-stu-id="aacc3-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="aacc3-117">Valige teatise moodul.</span><span class="sxs-lookup"><span data-stu-id="aacc3-117">Select the alert module.</span></span>

    <span data-ttu-id="aacc3-118">Kui teatise moodulit pole veel olemas, valige kolmikpunkti nupp (**...**) suvandi **Tõrke-/teabeteated** kõrval ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="aacc3-118">If an alert module doesn't yet exist, select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span> <span data-ttu-id="aacc3-119">Valige teatise moodul ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="aacc3-119">Select the alert module, and then select **OK**.</span></span>

1. <span data-ttu-id="aacc3-120">Valige parempoolsel atribuudipaanil vahekaardil **Andmed** suvand **Lisa andmeallikas**ja valige seejärel suvand **Sisu**.</span><span class="sxs-lookup"><span data-stu-id="aacc3-120">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="aacc3-121">Sisestage väljale **Sisendtekst** tervitussõnumi tekst.</span><span class="sxs-lookup"><span data-stu-id="aacc3-121">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="aacc3-122">Salvestage pease fragment, kontrollige seda ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="aacc3-122">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="aacc3-123">Iga valitud päise fragmenti kasutava saidi lehe ülaosas ilmub nüüd tervitussõnum.</span><span class="sxs-lookup"><span data-stu-id="aacc3-123">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aacc3-124">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="aacc3-124">Additional resources</span></span>

[<span data-ttu-id="aacc3-125">Logo lisamine</span><span class="sxs-lookup"><span data-stu-id="aacc3-125">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="aacc3-126">Saidi kujunduse valimine</span><span class="sxs-lookup"><span data-stu-id="aacc3-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="aacc3-127">CSS-i alistusfailidega töötamine</span><span class="sxs-lookup"><span data-stu-id="aacc3-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="aacc3-128">Leheikooni lisamine</span><span class="sxs-lookup"><span data-stu-id="aacc3-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="aacc3-129">Autoriõiguste teatise lisamine</span><span class="sxs-lookup"><span data-stu-id="aacc3-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="aacc3-130">Saidile keelte lisamine</span><span class="sxs-lookup"><span data-stu-id="aacc3-130">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="aacc3-131">Telemeetria toetamiseks saidile skriptikoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="aacc3-131">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

