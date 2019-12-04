---
title: Töövoo KKK
description: Teemas on toodud vastused korduma kippuvatele küsimustele töövoo süsteemi kohta.
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0188e8ed3cbbfd7dbccd7d13cf6129e146a919ac
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772693"
---
# <a name="workflow-faq"></a><span data-ttu-id="f5a6c-103">Töövoo KKK</span><span class="sxs-lookup"><span data-stu-id="f5a6c-103">Workflow FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5a6c-104">Teemas on toodud vastused korduma kippuvatele küsimustele töövoo süsteemi kohta.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-104">This topic answers frequently asked questions about the workflow system.</span></span>

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="f5a6c-105">Miks võetakse tööüksuse tagasilükkamisel vastu mitu teatist?</span><span class="sxs-lookup"><span data-stu-id="f5a6c-105">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="f5a6c-106">Tööüksuse tagasilükkamisel viiakse see tööüksus tagasilükatuna lõpuni.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-106">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="f5a6c-107">Algatajale luuakse ja määratakse teine tööüksus.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-107">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="f5a6c-108">See tähendab, et algataja saab teatise tagasilükatud tööüksuse kohta ja kasutaja, kellele määrati uus „taotletakse muudatust” tööüksus, saab eraldi teatise.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-108">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="f5a6c-109">Iga teatis on erineva tööüksuse jaoks, kuid nende sarnasus võib põhjustada segadust.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-109">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="f5a6c-110">Otsime võimalusi selle tulevases väljaandes parandamiseks.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-110">We are looking at ways to improve this in a future release.</span></span>

## <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="f5a6c-111">Miks minu töövoo eksport nurjub?</span><span class="sxs-lookup"><span data-stu-id="f5a6c-111">Why are my workflow exports failing?</span></span>
<span data-ttu-id="f5a6c-112">Praegu on töövoo ekspordi funktsioonil piirang, milles töövoo nimede pikkus ei tohi ületada 48 märki.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-112">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="f5a6c-113">Kasutades nime, mis on pikem kui 48 märki võib põhjustada tõrke "Server ei saanud taotlust autentida" ja/või takistada faili eksportimist failitüübita.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-113">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="f5a6c-114">Järgmine ajaveebipostitus sisaldab üksikasju [Töövoo ekspordi tõrkeotsingu](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting) kohta.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-114">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a><span data-ttu-id="f5a6c-115">Kas töövoo edastaja saab töövoo ka kinnitada?</span><span class="sxs-lookup"><span data-stu-id="f5a6c-115">Can the submitter of a workflow also approve the workflow?</span></span>
<span data-ttu-id="f5a6c-116">Jah, töövoo eedastaja saab töövoo ka kinnitada, kui see on nii konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-116">Yes, a submitter of a workflow can also approve the workflow if it is configured that way.</span></span> <span data-ttu-id="f5a6c-117">Selle käitumise vältimiseks seadistage **Töövoo parameetrid > Üldine > Kinnitaja > Keela edastaja tehtud kinnitamine** olekule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-117">To prevent this behavior, set **Workflow parameters > General > Approver > Disallow approval by submitter** to **Yes**.</span></span>

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a><span data-ttu-id="f5a6c-118">Kas ma saan töövoogudele märguandeid lisada, et kasutajatele teatiseid edastada?</span><span class="sxs-lookup"><span data-stu-id="f5a6c-118">Can I add alerts to workflows to provide notifications to users?</span></span>
<span data-ttu-id="f5a6c-119">Siin on mõned asjad, millele teatsite edastamiseks töövoogudele märguandeid lisades tähelepanu pöörata.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-119">Here are a few key areas to note about adding alerts to workflows to provide notifications:</span></span>
- <span data-ttu-id="f5a6c-120">Märguanded versus töövoo teatiste mehhanismid</span><span class="sxs-lookup"><span data-stu-id="f5a6c-120">Alerts versus workflow notification mechanisms</span></span>
    - <span data-ttu-id="f5a6c-121">Märguandeid saab seadistada kirje muudatustele.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-121">Alerts can be set up for record changes.</span></span> <span data-ttu-id="f5a6c-122">Töövood muudavad kirjeid, nii et võimalik on seadistada töövoo põhjustatud kirje muudatuse märguanne.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-122">Workflows change records, so it's possible to set up an alert related to a record change caused by a workflow.</span></span> <span data-ttu-id="f5a6c-123">Kuid kuna töövoogudel on erinevad sisse-ehitatud teatiste võimalused, ei ole märguannete kasutamine parim variant.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-123">However, because workflows have different built-in notification options, using alerts isn’t ideal.</span></span>
- <span data-ttu-id="f5a6c-124">Standardsed teatised töövoogudelt</span><span class="sxs-lookup"><span data-stu-id="f5a6c-124">Standard notifications from workflows</span></span> 
    - <span data-ttu-id="f5a6c-125">Töövoogudel on sisse-ehitatud e-posti teatised.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-125">Workflows have built in email notifications.</span></span> <span data-ttu-id="f5a6c-126">Klient saab konfigureerida teatiseid nii, et kasutajatele saadetakse e-kirjad.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-126">A customer can configure the notifications so that the users are sent emails.</span></span> <span data-ttu-id="f5a6c-127">Need teatised ei edasta kasutajatele tegevuskeskuse teateid.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-127">Those notifications don’t result in Action Center messages for users.</span></span>
    - <span data-ttu-id="f5a6c-128">Tulevases uuenduses lisame tegevuskeskuse teate, nii et kasutajale määratakse töövoo tööüksus.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-128">In a future update we will be adding an Action Center message so a user is assigned a workflow work item.</span></span> 
- <span data-ttu-id="f5a6c-129">Teatiste töövoogudesse lisamine</span><span class="sxs-lookup"><span data-stu-id="f5a6c-129">Adding notifications to workflows</span></span>
    - <span data-ttu-id="f5a6c-130">Tegevuskeskuse teateid saab luua kindlatele kasutajatele, nt töövoost X++ loodud sõnum.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-130">Action Center messages can be created for specific users, such as a message created from a workflow in X++.</span></span>
    - <span data-ttu-id="f5a6c-131">[Töövoogudel on ärisündmused](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow), mida klient saab kasutada Flowsi käivitamiseks, et saada nende otsitavad teatised.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-131">[Workflows have Business Events](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) that the customer could use to trigger Flows have the notifications that they are looking for.</span></span>   

<span data-ttu-id="f5a6c-132">Kokkuvõttes, kui kasutaja ei saa töövoo tööüksuse määramisel tegevuskeskusest nõuetekohast teatist, kasutage ära [Töövoo ärisündmuseid](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) koos rakendusega Microsoft Power Automate, et pakkuda täiendavaid või muid teatiseid.</span><span class="sxs-lookup"><span data-stu-id="f5a6c-132">In summary, if a user does not get the proper notification from the Action Center when they are assigned a workflow work item, then leverage [Workflow Business Events](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) with Microsoft Power Automate to provide additional or different notifications.</span></span>
