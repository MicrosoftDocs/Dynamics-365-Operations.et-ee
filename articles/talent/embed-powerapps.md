---
title: Power Apps rakenduste manustamine Dynamics 365 – Core HR-is
description: Selles teemas selgitatakse, kuidas lahendada probleemi, mille käigus Microsoft Power Appsi menüükäsk on süsteemihalduse moodulist kadunud.
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
ms.openlocfilehash: b1dd1756be349d85af8e6d7159623a2a95e75526
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898708"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a><span data-ttu-id="cad2c-103">Power Apps rakenduste manustamine Dynamics 365 – Core HR-is</span><span class="sxs-lookup"><span data-stu-id="cad2c-103">Embed Power Apps apps in Dynamics 365 - Core HR</span></span>

<span data-ttu-id="cad2c-104">**Väljastamine**</span><span class="sxs-lookup"><span data-stu-id="cad2c-104">**Issue**</span></span>

<span data-ttu-id="cad2c-105">Menüükäsk **Power Apps** on moodulist **Süsteemihaldus** kadunud.</span><span class="sxs-lookup"><span data-stu-id="cad2c-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="cad2c-106">**Põhjus**</span><span class="sxs-lookup"><span data-stu-id="cad2c-106">**Cause**</span></span>

<span data-ttu-id="cad2c-107">Kasutajaliidese (UI) kujundust muudeti ja Microsoft Power Apps on nüüd kaasatud standardsesse isikupärastamismudelisse.</span><span class="sxs-lookup"><span data-stu-id="cad2c-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="cad2c-108">**Eraldusvõime**</span><span class="sxs-lookup"><span data-stu-id="cad2c-108">**Resolution**</span></span>

<span data-ttu-id="cad2c-109">Muudeti Power Appsi manustamise viisi.</span><span class="sxs-lookup"><span data-stu-id="cad2c-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="cad2c-110">Power Apps lisatakse nüüd isikupärastamismudeli kaudu.</span><span class="sxs-lookup"><span data-stu-id="cad2c-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="cad2c-111">Rakenduses Microsoft Dynamics 365 Talent saab Power Appsi lisada peaaegu kõigile lehtedele.</span><span class="sxs-lookup"><span data-stu-id="cad2c-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="cad2c-112">Üksikasjalikku teavet Power Appsi rakenduste manustamise kohta Talentis vt jaotisest [Microsoft Power Appsi manustamine](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="cad2c-112">For information about how to embed Power Apps in Talent, see [Embed Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="cad2c-113">Enne muutust rakendused manustanud Power Appsi kliendid tuleb viia vastavusse uue mudeliga.</span><span class="sxs-lookup"><span data-stu-id="cad2c-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="cad2c-114">Nupp **Power Apps** asub peaaegu igas Talenti lehe ülemises parempoolses nurgas.</span><span class="sxs-lookup"><span data-stu-id="cad2c-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="cad2c-115">Seda nuppu saab kasutada Power Appsi sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="cad2c-115">You can use this button to insert Power Apps.</span></span>

<span data-ttu-id="cad2c-116">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="cad2c-116">Here is an example.</span></span>

1. <span data-ttu-id="cad2c-117">Minge jaotisse **Personalihaldus \> Lingid \> Töötajad \> Töövõtjad**.</span><span class="sxs-lookup"><span data-stu-id="cad2c-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="cad2c-118">Valige nupp **Power Apps** ja seejärel valige **Lisa PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="cad2c-118">Select the **Power Apps** button, and then select **Insert a PowerApp**.</span></span>

    ![Power Appsi nupp](media/png.png)

3. <span data-ttu-id="cad2c-120">Täitke väljad dialoogiboksis **Lisa PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="cad2c-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Dialoogiboks Lisa PowerApp](media/insert-powerapp.png)

<span data-ttu-id="cad2c-122">Teise võimalusena tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="cad2c-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="cad2c-123">Tehke lehe toimingupaani vahekaardi **Suvandid** grupis **Isikupärasta** valik **Vormi isikupärastamine**.</span><span class="sxs-lookup"><span data-stu-id="cad2c-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Grupp Isikupärasta vahekaardil Suvandid](media/options.png)

    <span data-ttu-id="cad2c-125">Ilmub isikupärastamise tööriistariba.</span><span class="sxs-lookup"><span data-stu-id="cad2c-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="cad2c-126">Valige tööriistaribal **Lisa \> PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="cad2c-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![Power Appsi rakenduse lisamine isikupärastamise tööriistariba kasutades](media/powerapp-bar.png)
