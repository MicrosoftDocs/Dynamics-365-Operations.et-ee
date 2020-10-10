---
title: Rakendus Human Resources Teamsis
description: Selles teemas tutvustatakse Microsoft Teamsi rakendust Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 33322b9b553076125695f257b201463e9d8275c6
ms.sourcegitcommit: e27510ba52623c801353eed4853f8c0aeea3bb2d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/22/2020
ms.locfileid: "3828910"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="f0110-103">Rakendus Human Resources Teamsis</span><span class="sxs-lookup"><span data-stu-id="f0110-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="f0110-104">Microsoft Teamsi rakendus Microsoft Dynamics 365 Human Resources võimaldab töövõtjatel kiirelt esitada vaba aja taotlust ja kuvada vaba aja saldo teavet otse Microsoft Teamsis.</span><span class="sxs-lookup"><span data-stu-id="f0110-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="f0110-105">Teabe taotlemiseks saavad töövõtjad suhelda robotiga.</span><span class="sxs-lookup"><span data-stu-id="f0110-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="f0110-106">Vahekaardil **Eemalolek** on üksikasjalikum teave. Lisaks saavad nad saata inimestele teavet eelseisva eemaloleku kohta töörühmades ja vestlustes väljaspool rakendust Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f0110-106">The **Time off** tab provides more detailed information.In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Human Resources Teamsi puhkuste rakenduse robot](./media/hr-admin-teams-leave-app-bot.png)

![Human Resources Teamsi puhkuse rakenduse vahekaart Vaba aeg](./media/hr-teams-leave-app-timeoff-tab.png)

![Rakenduse Human Resources puhkusetaotluse kaart](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="f0110-110">Installimine ja häälestus</span><span class="sxs-lookup"><span data-stu-id="f0110-110">Install and setup</span></span>

<span data-ttu-id="f0110-111">Rakenduse Human Resources leiate Teamsi poest.</span><span class="sxs-lookup"><span data-stu-id="f0110-111">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="f0110-112">Lisateabe saamiseks Teamsi rakenduse installimise kohta, vaadake teemat [Puhkusetaotluste haldamine Teamsis](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="f0110-112">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="f0110-113">Lisateabe saamiseks rakenduse lubade haldamise kohta Teamsis, vaadake teemat [Rakenduse lubade poliitikate haldamine Microsoft Teamsis](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="f0110-113">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="f0110-114">Teatiste lubamine rakenduse Human Resources jaoks Teamsis</span><span class="sxs-lookup"><span data-stu-id="f0110-114">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="f0110-115">Kui soovite, et kasutajad saaksid puhkusetaotluse teatisi rakenduses Teams, peate lubama teatised rakenduses Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f0110-115">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="f0110-116">Teatisi saavad ainult need kasutajad, kes on sisse logitud Teamsi ja kasutavad Teamsi rakendust Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f0110-116">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="f0110-117">Valige rakenduses Human Resources suvand **Süsteemihaldus**.</span><span class="sxs-lookup"><span data-stu-id="f0110-117">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="f0110-118">Valige **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="f0110-118">Select **Links**.</span></span>

3. <span data-ttu-id="f0110-119">Tehke jaotises **Seadistamine** valik **Süsteemi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="f0110-119">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="f0110-120">Seadke vahekaardil **Üldine** seade **Teatiste lubamine rakenduse Teams jaoks** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="f0110-120">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Teamsi rakenduse teatiste lubamine süsteemi parameetrites](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="f0110-122">Kõigi kasutajate jaoks Teamsi teatiste sisselülitamiseks valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="f0110-122">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Teamsi teatiste lubamine kõigi kasutajate jaoks](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="f0110-124">Üksikutele kasutajate jaoks Teamsi teatiste sisse- või väljalülitamine</span><span class="sxs-lookup"><span data-stu-id="f0110-124">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="f0110-125">Kui olete lubanud Teamsi rakenduse Human Resources teatised, saate teatised üksikute kasutajate jaoks sisse või välja lülitada.</span><span class="sxs-lookup"><span data-stu-id="f0110-125">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="f0110-126">Valige rakenduses Human Resources suvand **Süsteemihaldus**.</span><span class="sxs-lookup"><span data-stu-id="f0110-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="f0110-127">Valige **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="f0110-127">Select **Links**.</span></span>

3. <span data-ttu-id="f0110-128">Tehke jaotises **Kasutajad** valik **Kasutaja valikud**.</span><span class="sxs-lookup"><span data-stu-id="f0110-128">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="f0110-129">Valige vahekaart **Töövoog**.</span><span class="sxs-lookup"><span data-stu-id="f0110-129">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="f0110-130">Määrake seade **Teatiste lubamine rakenduse Teams jaoks** väärtuseks **Jah**, et lubada kasutajate jaoks teatiste kuvamine, või **Ei**, et keelata kasutajale teatiste kuvamine.</span><span class="sxs-lookup"><span data-stu-id="f0110-130">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Teamsi rakenduse teatiste lubamine kasutaja suvandite vahekaardil Töövoog](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="f0110-132">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="f0110-132">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="f0110-133">Teadaolevad probleemid</span><span class="sxs-lookup"><span data-stu-id="f0110-133">Known issues</span></span>

| <span data-ttu-id="f0110-134">Väljasta</span><span class="sxs-lookup"><span data-stu-id="f0110-134">Issue</span></span> | <span data-ttu-id="f0110-135">Olek</span><span class="sxs-lookup"><span data-stu-id="f0110-135">Status</span></span> |
| --- | --- |
| <span data-ttu-id="f0110-136">Horisontaalne kerimine ei tööta Androidi telefonides</span><span class="sxs-lookup"><span data-stu-id="f0110-136">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="f0110-137">Horisontaalne kerimine ei ole iOS-is või arvutites probleem.</span><span class="sxs-lookup"><span data-stu-id="f0110-137">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="f0110-138">Me töötame selle vea parandamise kallal Androidis.</span><span class="sxs-lookup"><span data-stu-id="f0110-138">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="f0110-139">Tulevaks kuupäevaks vaba aja taotlemisel on vale saldo.</span><span class="sxs-lookup"><span data-stu-id="f0110-139">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="f0110-140">Prognoosimine pole veel saadaval.</span><span class="sxs-lookup"><span data-stu-id="f0110-140">Forecasting isn't yet available.</span></span> <span data-ttu-id="f0110-141">Kuvatakse praeguse kuupäeva saldo.</span><span class="sxs-lookup"><span data-stu-id="f0110-141">The balance displays for the current date.</span></span> |
| <span data-ttu-id="f0110-142">Taotlust **Läbivaatamisel** ei saa tühistada.</span><span class="sxs-lookup"><span data-stu-id="f0110-142">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="f0110-143">See funktsioon ei ole praegu toetatud ja lisatakse tulevasse väljalaskesse.</span><span class="sxs-lookup"><span data-stu-id="f0110-143">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="f0110-144">Saldo teavet arvutatakse alates tänasest.</span><span class="sxs-lookup"><span data-stu-id="f0110-144">Balance information is calculated as of today.</span></span> | <span data-ttu-id="f0110-145">Süsteem ei kuva praegu puhkuseperioodi seisuga saldosid, isegi kui see on konfigureeritud puhkuste ja puudumiste parameetrites.</span><span class="sxs-lookup"><span data-stu-id="f0110-145">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="f0110-146">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="f0110-146">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="f0110-147">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="f0110-147">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="f0110-148">Kui Dynamics 365 Human Resourcesi robot on kasutusel Microsoft Teamsis, analüüsitakse kasutaja tekstisisestusi, et mõista aluseks olevat päringut/eesmärki.</span><span class="sxs-lookup"><span data-stu-id="f0110-148">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="f0110-149">Kasutaja sisestus (nt „otsing konto Contoso”) suunatakse Microsofti kognitiivsesse teenusesse nimega Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="f0110-149">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="f0110-150">Lugege lisateavet LUIS-i kohta  [siin](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="f0110-150">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="f0110-151">Teenus LUIS eristab või mõistab kasutaja sisestuse kavatsust (antud juhul on eesmärgiks teabe leidmine) ja sihtüksust (antud juhul on soovitud üksuseks konto nimega Contoso).</span><span class="sxs-lookup"><span data-stu-id="f0110-151">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="f0110-152">Seejärel edastatakse see teave Microsofti  [Azure'i roboti raamistikule](https://azure.microsoft.com/services/bot-service/), mis suhtleb Dynamics 365 Human Resourcesi andmetega ja toob kasutaja päringu vastuseks soovitud teabe.</span><span class="sxs-lookup"><span data-stu-id="f0110-152">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="f0110-153">Kui installite ja lubate juurdepääsu roboti kasutamiseks, annate teenusele LUIS ja Azure'i roboti raamistikule nõusoleku töödelda sisestuse kavatsust, mille tulemuseks on täiustatud vestlusvaatega kasutuskogemus.</span><span class="sxs-lookup"><span data-stu-id="f0110-153">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="f0110-154">Teenusel LUIS ja Azure'i roboti raamistikul võib olla võrreldes Dynamics 365 Human Resourcesiga erinev vastavuse tase.</span><span class="sxs-lookup"><span data-stu-id="f0110-154">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="f0110-155">Kui teenusel LUIS on juurdepääs ainult kasutaja päringutele ja ei ole mõeldud ühendamiseks kasutaja Dynamics 365 Human Resourcesi andmete või kontoga, siis Dynamics 365 Human Resourcesi roboti kasutaja saab vabatahtlikult sisestada kliendiandmeid, isikuandmeid või muid andmeid sisaldavaid päringuid ja selle päringu sisu võidakse saata teenusesse LUIS ja Azure'i roboti raamistikku.</span><span class="sxs-lookup"><span data-stu-id="f0110-155">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="f0110-156">Kasutaja päringute ja sõnumite sisu säilitatakse süsteemis LUIS maksimaalselt 30 päeva, krüptitakse passiivsena ja seda ei kasutata koolituse või teenuse täiustamiseks.</span><span class="sxs-lookup"><span data-stu-id="f0110-156">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="f0110-157">Lisateavet kognitiivsete teenuste kohta leiate [siit](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="f0110-157">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="f0110-158">Microsoft Teamsi rakenduste administraatori sätete haldamiseks minge [Microsoft Teamsi halduskeskusesse](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="f0110-158">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="f0110-159">Microsoft Teams, Azure Event Grid ja Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f0110-159">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="f0110-160">Rakenduse Dynamics 365 Human Resources kasutamisel rakenduses Microsoft Teams võivad mõned kliendiandmed liikuda väljapoole geograafilist piirkonda, kus teie rentniku teenus Human Resources on juurutatud.</span><span class="sxs-lookup"><span data-stu-id="f0110-160">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="f0110-161">Dynamics 365 Human Resources edastab töötaja puhkusetaotluse ja töövoo ülesande üksikasjad Microsoft Azure Event Gridi ja Microsoft Teamsi.</span><span class="sxs-lookup"><span data-stu-id="f0110-161">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="f0110-162">Neid andmeid võidakse säilitada teenuses Microsoft Azure Event Grid kuni 24 tundi ja töödelda Ameerika Ühendriikides, need krüptitakse edastamisel ja passiivsena ning Microsoft ega selle alamtöötlejad ei kasuta neid koolituste või teenuste täiustamiseks.</span><span class="sxs-lookup"><span data-stu-id="f0110-162">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="f0110-163">Lisateavet selle kohta, kus teie andmeid rakenduses Teams talletatakse, leiate teemast [Andmete asukoht rakenduses Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="f0110-163">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="f0110-164">Vestlusrobotiga suhtlemisel rakenduses Human Resources võidakse vestluse sisu teenuses Azure Cosmos DB talletada ja edastada rakendusele Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="f0110-164">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="f0110-165">Neid andmeid võidakse talletada teenuses Azure Cosmos DB kuni 24 tundi ja töödelda väljaspool geograafilist piirkonda, kus teie rentniku teenus Human Resources on juurutatud, need krüptitakse edastamisel ja passiivsena ning Microsoft ega selle alamtöötlejad ei kasuta neid koolituste või teenuste täiustamiseks.</span><span class="sxs-lookup"><span data-stu-id="f0110-165">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="f0110-166">Lisateavet selle kohta, kus teie andmeid rakenduses Teams talletatakse, leiate teemast [Andmete asukoht rakenduses Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="f0110-166">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="f0110-167">Et piirata oma organisatsiooni või selles olevate kasutajate juurdepääsu rakendusele Human Resources, mis asub rakenduses Microsoft Teams, lugege teemat [Rakenduse lubade poliitika haldamine rakenduses Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="f0110-167">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="f0110-168">Vt ka</span><span class="sxs-lookup"><span data-stu-id="f0110-168">See also</span></span> 

[<span data-ttu-id="f0110-169">Microsoft Teamsi allalaadimine ja installimine</span><span class="sxs-lookup"><span data-stu-id="f0110-169">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="f0110-170">Microsoft Teams spikrikeskus</span><span class="sxs-lookup"><span data-stu-id="f0110-170">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="f0110-171">Puhkusetaotluste haldamine Teamsis</span><span class="sxs-lookup"><span data-stu-id="f0110-171">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

