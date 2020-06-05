---
title: Rakendus Human Resources Teamsis
description: Selles teemas tutvustatakse Microsoft Teamsi rakendust Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 423ec36a73e8af9d915c5cfe16bd4d552448e2b6
ms.sourcegitcommit: d1541831d556b722a71aed442043ffb4a4576d87
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/20/2020
ms.locfileid: "3388112"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="3618b-103">Rakendus Human Resources Teamsis</span><span class="sxs-lookup"><span data-stu-id="3618b-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="3618b-104">Microsoft Teamsi rakendus Microsoft Dynamics 365 Human Resources võimaldab töövõtjatel kiirelt esitada vaba aja taotlust ja kuvada vaba aja saldo teavet otse Microsoft Teamsis.</span><span class="sxs-lookup"><span data-stu-id="3618b-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="3618b-105">Teabe taotlemiseks saavad töövõtjad suhelda robotiga.</span><span class="sxs-lookup"><span data-stu-id="3618b-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="3618b-106">Vahekaart **Vaba aeg** annab üksikasjalikumat teavet.</span><span class="sxs-lookup"><span data-stu-id="3618b-106">The **Time off** tab provides more detailed information.</span></span>

![Human Resources Teamsi puhkuste rakenduse robot](./media/hr-admin-teams-leave-app-bot.png)

![Human Resources Teamsi puhkuse rakenduse vahekaart Vaba aeg](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="3618b-109">Installimine ja häälestus</span><span class="sxs-lookup"><span data-stu-id="3618b-109">Install and setup</span></span>

<span data-ttu-id="3618b-110">Rakenduse Human Resources leiate Teamsi poest.</span><span class="sxs-lookup"><span data-stu-id="3618b-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="3618b-111">Lisateabe saamiseks Teamsi rakenduse installimise kohta, vaadake teemat [Puhkusetaotluste haldamine Teamsis](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="3618b-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="3618b-112">Lisateabe saamiseks rakenduse lubade haldamise kohta Teamsis, vaadake teemat [Rakenduse lubade poliitikate haldamine Microsoft Teamsis](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="3618b-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="known-issues"></a><span data-ttu-id="3618b-113">Teadaolevad probleemid</span><span class="sxs-lookup"><span data-stu-id="3618b-113">Known issues</span></span>

| <span data-ttu-id="3618b-114">Väljastus</span><span class="sxs-lookup"><span data-stu-id="3618b-114">Issue</span></span> | <span data-ttu-id="3618b-115">Olek</span><span class="sxs-lookup"><span data-stu-id="3618b-115">Status</span></span> |
| --- | --- |
| <span data-ttu-id="3618b-116">Tulevaks kuupäevaks vaba aja taotlemisel on vale saldo.</span><span class="sxs-lookup"><span data-stu-id="3618b-116">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="3618b-117">Prognoosimine pole veel saadaval.</span><span class="sxs-lookup"><span data-stu-id="3618b-117">Forecasting isn't yet available.</span></span> <span data-ttu-id="3618b-118">Kuvatakse praeguse kuupäeva saldo.</span><span class="sxs-lookup"><span data-stu-id="3618b-118">The balance displays for the current date.</span></span> |
| <span data-ttu-id="3618b-119">Olemasolevas taotluses võetud tundide arvu vähendamisel, muutub **Jääksaldo** väiksemaks, mitte suuremaks.</span><span class="sxs-lookup"><span data-stu-id="3618b-119">When reducing the number of hours taken in an existing request, the **Remaining balance** goes down instead of up.</span></span> | <span data-ttu-id="3618b-120">Tegeleme selle teadaoleva probleemiga tulevikus.</span><span class="sxs-lookup"><span data-stu-id="3618b-120">We'll address this known issue in the future.</span></span> <span data-ttu-id="3618b-121">Kuva on vale, kuid õiged summad kohandatakse pärast esitamist.</span><span class="sxs-lookup"><span data-stu-id="3618b-121">The display is incorrect, but the correct amounts are adjusted upon submission.</span></span> |
| <span data-ttu-id="3618b-122">Samadele kuupäevadele kuvatakse kaks kaarti **Eesolev vaba aeg**.</span><span class="sxs-lookup"><span data-stu-id="3618b-122">Two **Upcoming time off** cards display for the same dates.</span></span> | <span data-ttu-id="3618b-123">Kaardid esindavad erinevaid esitamisi.</span><span class="sxs-lookup"><span data-stu-id="3618b-123">The cards represent individual submissions.</span></span> <span data-ttu-id="3618b-124">Jätkame tagasiside vastuvõtmist ja teeme korrigeerimisi.</span><span class="sxs-lookup"><span data-stu-id="3618b-124">We'll continue to take feedback and make adjustments.</span></span> |
| <span data-ttu-id="3618b-125">Taotlust **Läbivaatamisel** ei saa tühistada.</span><span class="sxs-lookup"><span data-stu-id="3618b-125">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="3618b-126">See funktsioon ei ole praegu toetatud ja lisatakse tulevasse väljalaskesse.</span><span class="sxs-lookup"><span data-stu-id="3618b-126">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="3618b-127">Saldo teavet arvutatakse alates tänasest.</span><span class="sxs-lookup"><span data-stu-id="3618b-127">Balance information is calculated as of today.</span></span> | <span data-ttu-id="3618b-128">Süsteem ei kuva praegu puhkuseperioodi seisuga saldosid, isegi kui see on konfigureeritud puhkuste ja puudumiste parameetrites.</span><span class="sxs-lookup"><span data-stu-id="3618b-128">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="3618b-129">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="3618b-129">Privacy notice</span></span>

<span data-ttu-id="3618b-130">Kui Dynamics 365 Human Resourcesi robot on kasutusel Microsoft Teamsis, analüüsitakse kasutaja tekstisisestusi, et mõista aluseks olevat päringut/eesmärki.</span><span class="sxs-lookup"><span data-stu-id="3618b-130">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="3618b-131">Kasutaja sisestus (nt „otsing konto Contoso”) suunatakse Microsofti kognitiivsesse teenusesse nimega Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="3618b-131">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="3618b-132">Lugege lisateavet LUIS-i kohta  [siin](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="3618b-132">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="3618b-133">Teenus LUIS eristab või mõistab kasutaja sisestuse kavatsust (antud juhul on eesmärgiks teabe leidmine) ja sihtüksust (antud juhul on soovitud üksuseks konto nimega Contoso).</span><span class="sxs-lookup"><span data-stu-id="3618b-133">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="3618b-134">Seejärel edastatakse see teave Microsofti [Azure'i roboti raamistikule](https://azure.microsoft.com/services/bot-service/) , mis suhtleb Dynamics 365 Human Resourcesi andmetega ja toob kasutaja päringu vastuseks soovitud teabe.</span><span class="sxs-lookup"><span data-stu-id="3618b-134">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/) which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="3618b-135">Kui installite ja lubate juurdepääsu roboti kasutamiseks, annate teenusele LUIS ja Azure'i roboti raamistikule nõusoleku töödelda sisestuse kavatsust, mille tulemuseks on täiustatud vestlusvaatega kasutuskogemus.</span><span class="sxs-lookup"><span data-stu-id="3618b-135">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="3618b-136">Teenusel LUIS ja Azure'i roboti raamistikul võib olla võrreldes Dynamics 365 Human Resourcesiga erinev vastavuse tase.</span><span class="sxs-lookup"><span data-stu-id="3618b-136">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="3618b-137">Kui teenusel LUIS on juurdepääs ainult kasutaja päringutele ja ei ole mõeldud ühendamiseks kasutaja Dynamics 365 Human Resourcesi andmete või kontoga, siis Dynamics 365 Human Resourcesi roboti kasutaja saab vabatahtlikult sisestada kliendiandmeid, isikuandmeid või muid andmeid sisaldavaid päringuid ja selle päringu sisu võidakse saata teenusesse LUIS ja Azure'i roboti raamistikku.</span><span class="sxs-lookup"><span data-stu-id="3618b-137">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="3618b-138">Kasutaja päringute ja sõnumite sisu säilitatakse süsteemis LUIS maksimaalselt 30 päeva, krüptitakse passiivsena ja seda ei kasutata koolituse või teenuse täiustamiseks.</span><span class="sxs-lookup"><span data-stu-id="3618b-138">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="3618b-139">Lisateavet kognitiivsete teenuste kohta leiate [siit](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="3618b-139">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="3618b-140">Microsoft Teamsi rakenduste administraatori sätete haldamiseks minge [Microsoft Teamsi halduskeskusesse](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="3618b-140">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span> 

## <a name="see-also"></a><span data-ttu-id="3618b-141">Vt ka</span><span class="sxs-lookup"><span data-stu-id="3618b-141">See also</span></span> 

[<span data-ttu-id="3618b-142">Microsoft Teamsi allalaadimine ja installimine</span><span class="sxs-lookup"><span data-stu-id="3618b-142">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="3618b-143">Microsoft Teams spikrikeskus</span><span class="sxs-lookup"><span data-stu-id="3618b-143">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="3618b-144">Puhkusetaotluste haldamine Teamsis</span><span class="sxs-lookup"><span data-stu-id="3618b-144">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

