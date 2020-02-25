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
ms.openlocfilehash: ca10b01268b5dcd4c6fe448d90cd0ebd65a2673b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001250"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="32e75-103">Tervitussõnumi lisamine</span><span class="sxs-lookup"><span data-stu-id="32e75-103">Add a welcome message</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="32e75-104">See teema kirjeldab, kuidas lisada oma Microsoft Dynamics 365 Commerce veebisaidile tervitussõnum.</span><span class="sxs-lookup"><span data-stu-id="32e75-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="32e75-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="32e75-105">Overview</span></span>

<span data-ttu-id="32e75-106">E-kaubanduse veebisaidi tervitussõnum võib teavitada külastajaid käimasolevatest allahindlustest, saidi uuendustest või hooajaliste kollektsioonide saadavusest.</span><span class="sxs-lookup"><span data-stu-id="32e75-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="32e75-107">Tervitussõnum määratakse teatisemooduli abil.</span><span class="sxs-lookup"><span data-stu-id="32e75-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="32e75-108">Teatisemoodul tuleks lisada päise fragmendi pessa **Tõrke-/teabeteated**.</span><span class="sxs-lookup"><span data-stu-id="32e75-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="32e75-109">Teatisemoodul võimaldab teil määrata kuvatava teksti, teksti värvi ja joonduse.</span><span class="sxs-lookup"><span data-stu-id="32e75-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="32e75-110">Samuti võimaldab see määrata, kas saidi külastajad võivad sõnumi lõpetada.</span><span class="sxs-lookup"><span data-stu-id="32e75-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="32e75-111">Kui jagatud päise fragmenti on lisatud tervitussõnum, kuvatakse see igal lehel, mis kasutab malli, kus seda jagatud päise fragmenti kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="32e75-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="32e75-112">Oma saidile tervitussõnumi lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="32e75-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="32e75-113">Avage rakenduses Dynamics 365 Commerce oma sait.</span><span class="sxs-lookup"><span data-stu-id="32e75-113">In Dynamics 365 Commerce, go to your site.</span></span>
1. <span data-ttu-id="32e75-114">Valige suvand **Fragmendid**.</span><span class="sxs-lookup"><span data-stu-id="32e75-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="32e75-115">Valige päise fragment, millele sõnum lisada.</span><span class="sxs-lookup"><span data-stu-id="32e75-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="32e75-116">Laiendage liigendpuus suvandit **Tõrke-/teabeteated**.</span><span class="sxs-lookup"><span data-stu-id="32e75-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="32e75-117">Valige teatise moodul.</span><span class="sxs-lookup"><span data-stu-id="32e75-117">Select the alert module.</span></span>

    <span data-ttu-id="32e75-118">Kui teatise moodulit pole veel olemas, valige kolmikpunkti nupp (**...**) suvandi **Tõrke-/teabeteated** kõrval ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="32e75-118">If an alert module doesn't yet exist, select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span> <span data-ttu-id="32e75-119">Valige teatise moodul ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="32e75-119">Select the alert module, and then select **OK**.</span></span>

1. <span data-ttu-id="32e75-120">Valige parempoolsel atribuudipaanil vahekaardil **Andmed** suvand **Lisa andmeallikas**ja valige seejärel suvand **Sisu**.</span><span class="sxs-lookup"><span data-stu-id="32e75-120">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="32e75-121">Sisestage väljale **Sisendtekst** tervitussõnumi tekst.</span><span class="sxs-lookup"><span data-stu-id="32e75-121">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="32e75-122">Salvestage pease fragment, kontrollige seda ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="32e75-122">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="32e75-123">Iga valitud päise fragmenti kasutava saidi lehe ülaosas ilmub nüüd tervitussõnum.</span><span class="sxs-lookup"><span data-stu-id="32e75-123">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="32e75-124">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="32e75-124">Additional resources</span></span>

[<span data-ttu-id="32e75-125">Logo lisamine</span><span class="sxs-lookup"><span data-stu-id="32e75-125">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="32e75-126">Saidi kujunduse valimine</span><span class="sxs-lookup"><span data-stu-id="32e75-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="32e75-127">CSS-i alistusfailidega töötamine</span><span class="sxs-lookup"><span data-stu-id="32e75-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="32e75-128">Leheikooni lisamine</span><span class="sxs-lookup"><span data-stu-id="32e75-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="32e75-129">Autoriõiguste teatise lisamine</span><span class="sxs-lookup"><span data-stu-id="32e75-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="32e75-130">Saidile keelte lisamine</span><span class="sxs-lookup"><span data-stu-id="32e75-130">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="32e75-131">Telemeetria toetamiseks saidile skriptikoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="32e75-131">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

