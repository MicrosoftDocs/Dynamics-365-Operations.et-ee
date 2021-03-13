---
title: Veebitegevuse sündmuste kogumisest loobumine
description: See teema selgitab, kuidas saate lubada veebisaidi külastajatel loobuda rakenduses Microsoft Dynamics 365 Commerce veebitegevuse sündmuste kogumisest.
author: aamiral
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2c396060017db6d7ce830b350f242d3097876e50
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012309"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="9ef23-103">Veebitegevuse sündmuste kogumisest loobumine</span><span class="sxs-lookup"><span data-stu-id="9ef23-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="9ef23-104">See teema selgitab, kuidas saate lubada klientidel loobuda rakenduses Microsoft Dynamics 365 Commerce veebitegevuse sünduste kogumisest.</span><span class="sxs-lookup"><span data-stu-id="9ef23-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9ef23-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="9ef23-105">Overview</span></span>

<span data-ttu-id="9ef23-106">Dynamics 365 Commerce võimaldab saidi administraatoritel analüüsida oma e-kaubanduse saitide kasutajate tegevust veebis.</span><span class="sxs-lookup"><span data-stu-id="9ef23-106">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="9ef23-107">Seeläbi mõistavad nad paremini, kuidas nende saite kasutatakse ja saavad optimeerida saite, et need pakuksid täiustatud kasutuskogemust ja täidaksid ärieesmärke.</span><span class="sxs-lookup"><span data-stu-id="9ef23-107">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="9ef23-108">Administraatorite loobumiskogemuse rakendamise viisid</span><span class="sxs-lookup"><span data-stu-id="9ef23-108">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="9ef23-109">Administraatoritel on loobumiskogemuse rakendamiseks kolm viisi.</span><span class="sxs-lookup"><span data-stu-id="9ef23-109">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="9ef23-110">Kasutajate nimel loobumine</span><span class="sxs-lookup"><span data-stu-id="9ef23-110">Opt out on behalf of users</span></span>

<span data-ttu-id="9ef23-111">Commerce’i peakontori (HQ) kontohalduses saavad administraatorid loobuda kasutajate nimel.</span><span class="sxs-lookup"><span data-stu-id="9ef23-111">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="9ef23-112">Otsige üles ja valige klient HQ-kliendi lehel **Kõik kliendid**.</span><span class="sxs-lookup"><span data-stu-id="9ef23-112">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="9ef23-113">Määrake kliendi üksikasjade lehe kiirkaardi **Jaemüük** jaotises **Privaatsus** suvandi **Ära jälgi veebitegevust** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="9ef23-113">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![Privaatsussätted](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="9ef23-115">Valige **Salvesta** ja sulgege seejärel leht.</span><span class="sxs-lookup"><span data-stu-id="9ef23-115">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="9ef23-116">Moodulipõhine loobumise kogemus</span><span class="sxs-lookup"><span data-stu-id="9ef23-116">Module-based opt-out experience</span></span>

<span data-ttu-id="9ef23-117">Administraatorid saavad lubada autenditud kasutajatel loobuda ise veebitegevuse sündmuste kogumisest.</span><span class="sxs-lookup"><span data-stu-id="9ef23-117">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="9ef23-118">Selle loobumiskogemuse pakkumiseks lisage kasutaja loobumise moodul konto profiili lehtedele.</span><span class="sxs-lookup"><span data-stu-id="9ef23-118">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="9ef23-119">Kohandatud laiendid</span><span class="sxs-lookup"><span data-stu-id="9ef23-119">Custom extensions</span></span>

<span data-ttu-id="9ef23-120">Administraatorid saavad luua oma laiendid, et hallata kasutajate loobumise kogemust.</span><span class="sxs-lookup"><span data-stu-id="9ef23-120">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="9ef23-121">Lisateavet vt [Jaemüügiserveri API-de kutsumine](e-commerce-extensibility/call-retail-server-apis.md) ja [Võrgukanali laiendatavus](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="9ef23-121">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
