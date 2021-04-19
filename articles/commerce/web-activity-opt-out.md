---
title: Veebitegevuse sündmuste kogumisest loobumine
description: See teema selgitab, kuidas saate lubada veebisaidi külastajatel loobuda rakenduses Microsoft Dynamics 365 Commerce veebitegevuse sündmuste kogumisest.
author: aamiral
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 86f475cc0b78c620309301516b6c3b525b640637
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791553"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="fb34e-103">Veebitegevuse sündmuste kogumisest loobumine</span><span class="sxs-lookup"><span data-stu-id="fb34e-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="fb34e-104">See teema selgitab, kuidas saate lubada klientidel loobuda rakenduses Microsoft Dynamics 365 Commerce veebitegevuse sündmuste kogumisest.</span><span class="sxs-lookup"><span data-stu-id="fb34e-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="fb34e-105">Dynamics 365 Commerce võimaldab saidi administraatoritel analüüsida oma e-kaubanduse saitide kasutajate tegevust veebis.</span><span class="sxs-lookup"><span data-stu-id="fb34e-105">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="fb34e-106">Seeläbi mõistavad nad paremini, kuidas nende saite kasutatakse ja saavad optimeerida saite, et need pakuksid täiustatud kasutuskogemust ja täidaksid ärieesmärke.</span><span class="sxs-lookup"><span data-stu-id="fb34e-106">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="fb34e-107">Administraatorite loobumiskogemuse rakendamise viisid</span><span class="sxs-lookup"><span data-stu-id="fb34e-107">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="fb34e-108">Administraatoritel on loobumiskogemuse rakendamiseks kolm viisi.</span><span class="sxs-lookup"><span data-stu-id="fb34e-108">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="fb34e-109">Kasutajate nimel loobumine</span><span class="sxs-lookup"><span data-stu-id="fb34e-109">Opt out on behalf of users</span></span>

<span data-ttu-id="fb34e-110">Commerce’i peakontori (HQ) kontohalduses saavad administraatorid loobuda kasutajate nimel.</span><span class="sxs-lookup"><span data-stu-id="fb34e-110">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="fb34e-111">Otsige üles ja valige klient HQ-kliendi lehel **Kõik kliendid**.</span><span class="sxs-lookup"><span data-stu-id="fb34e-111">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="fb34e-112">Määrake kliendi üksikasjade lehe kiirkaardi **Jaemüük** jaotises **Privaatsus** suvandi **Ära jälgi veebitegevust** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="fb34e-112">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![Privaatsussätted](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="fb34e-114">Valige **Salvesta** ja sulgege seejärel leht.</span><span class="sxs-lookup"><span data-stu-id="fb34e-114">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="fb34e-115">Moodulipõhine loobumise kogemus</span><span class="sxs-lookup"><span data-stu-id="fb34e-115">Module-based opt-out experience</span></span>

<span data-ttu-id="fb34e-116">Administraatorid saavad lubada autenditud kasutajatel loobuda ise veebitegevuse sündmuste kogumisest.</span><span class="sxs-lookup"><span data-stu-id="fb34e-116">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="fb34e-117">Selle loobumiskogemuse pakkumiseks lisage kasutaja loobumise moodul konto profiili lehtedele.</span><span class="sxs-lookup"><span data-stu-id="fb34e-117">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="fb34e-118">Kohandatud laiendid</span><span class="sxs-lookup"><span data-stu-id="fb34e-118">Custom extensions</span></span>

<span data-ttu-id="fb34e-119">Administraatorid saavad luua oma laiendid, et hallata kasutajate loobumise kogemust.</span><span class="sxs-lookup"><span data-stu-id="fb34e-119">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="fb34e-120">Lisateavet vt [Jaemüügiserveri API-de kutsumine](e-commerce-extensibility/call-retail-server-apis.md) ja [Võrgukanali laiendatavus](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="fb34e-120">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
