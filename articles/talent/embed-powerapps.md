---
title: PowerAppsi rakenduste manustamine Core HR-is
description: Selles teemas selgitatakse, kuidas lahendada probleemi, mille käigus PowerAppsi menüükäsk on süsteemihalduse moodulist kadunud.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e3b20e1d0a873c32b8f6f5e28f786febf62db355
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/19/2019
ms.locfileid: "859547"
---
# <a name="embed-powerapps-apps-in-core-hr"></a><span data-ttu-id="bdbbc-103">PowerAppsi rakenduste manustamine Core HR-is</span><span class="sxs-lookup"><span data-stu-id="bdbbc-103">Embed PowerApps apps in Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bdbbc-104">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="bdbbc-104">**Issue**</span></span>

<span data-ttu-id="bdbbc-105">Menüükäsk **PowerApps** on moodulist **Süsteemihaldus** kadunud.</span><span class="sxs-lookup"><span data-stu-id="bdbbc-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="bdbbc-106">**Põhjus**</span><span class="sxs-lookup"><span data-stu-id="bdbbc-106">**Cause**</span></span>

<span data-ttu-id="bdbbc-107">Kasutajaliidese (UI) kujundust muudeti ja Microsoft PowerApps on nüüd kaasatud standardsesse isikupärastamismudelisse.</span><span class="sxs-lookup"><span data-stu-id="bdbbc-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="bdbbc-108">**Eraldusvõime**</span><span class="sxs-lookup"><span data-stu-id="bdbbc-108">**Resolution**</span></span>

<span data-ttu-id="bdbbc-109">Muudeti PowerAppsi rakenduste manustamise viisi.</span><span class="sxs-lookup"><span data-stu-id="bdbbc-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="bdbbc-110">PowerAppsi rakendusi lisatakse nüüd isikupärastamismudeli kaudu.</span><span class="sxs-lookup"><span data-stu-id="bdbbc-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="bdbbc-111">Rakenduses Microsoft Dynamics 365 for Talent saab PowerAppsi rakendusi lisada peaaegu kõigile lehtedele.</span><span class="sxs-lookup"><span data-stu-id="bdbbc-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 for Talent.</span></span>

<span data-ttu-id="bdbbc-112">Üksikasjalikku teavet PowerAppsi rakenduse manustamise kohta Talentis vt jaotisest [PowerAppsi rakenduste manustamine](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="bdbbc-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="bdbbc-113">Enne muutust rakendused manustanud PowerAppsi kliendid tuleb viia vastavusse uue mudeliga.</span><span class="sxs-lookup"><span data-stu-id="bdbbc-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="bdbbc-114">Nupp **PowerApps** asub peaaegu igas Talenti lehe ülemises parempoolses nurgas.</span><span class="sxs-lookup"><span data-stu-id="bdbbc-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="bdbbc-115">Seda nuppu saab kasutada PowerAppsi rakenduse sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="bdbbc-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="bdbbc-116">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="bdbbc-116">Here is an example.</span></span>

1. <span data-ttu-id="bdbbc-117">Minge jaotisse **Personalihaldus \> Lingid \> Töötajad \> Töövõtjad**.</span><span class="sxs-lookup"><span data-stu-id="bdbbc-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="bdbbc-118">Valige nupp **PowerApps** ja seejärel valige **Lisa PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="bdbbc-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![Nupp PowerApps](media/png.png)

3. <span data-ttu-id="bdbbc-120">Täitke väljad dialoogiboksis **Lisa PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="bdbbc-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Dialoogiboks Lisa PowerApp](media/insert-powerapp.png)

<span data-ttu-id="bdbbc-122">Teise võimalusena tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="bdbbc-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="bdbbc-123">Tehke lehe toimingupaani vahekaardi **Suvandid** grupis **Isikupärasta** valik **Vormi isikupärastamine**.</span><span class="sxs-lookup"><span data-stu-id="bdbbc-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Grupp Isikupärasta vahekaardil Suvandid](media/options.png)

    <span data-ttu-id="bdbbc-125">Ilmub isikupärastamise tööriistariba.</span><span class="sxs-lookup"><span data-stu-id="bdbbc-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="bdbbc-126">Valige tööriistaribal **Lisa \> PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="bdbbc-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![PowerAppsi rakenduse lisamine isikupärastamise tööriistariba kasutades](media/powerapp-bar.png)
