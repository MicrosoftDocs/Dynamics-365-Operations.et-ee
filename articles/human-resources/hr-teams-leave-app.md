---
title: Puhkusetaotluste haldamine Teamsis
description: Selles teemas kirjeldatakse, kuidas esitada puhkusetaotlust Microsoft Teamsi rakenduses Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c7b74983cbddf661456b0a65939e272078d59f6d
ms.sourcegitcommit: e27510ba52623c801353eed4853f8c0aeea3bb2d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/22/2020
ms.locfileid: "3828940"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="532b7-103">Puhkusetaotluste haldamine Teamsis</span><span class="sxs-lookup"><span data-stu-id="532b7-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="532b7-104">Microsoft Teamsi rakendus Microsoft Dynamics 365 Human Resources võimaldab teil kiirelt esitada vaba aja taotlust ja kuvada vaba aja saldo teavet otse Microsoft Teamsis.</span><span class="sxs-lookup"><span data-stu-id="532b7-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="532b7-105">Saate suhelda robotiga, et taotleda teavet ja algatada puhkusetaotlus.</span><span class="sxs-lookup"><span data-stu-id="532b7-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="532b7-106">Vahekaart **Vaba aeg** annab üksikasjalikumat teavet.</span><span class="sxs-lookup"><span data-stu-id="532b7-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="532b7-107">Lisaks saate saata inimestele teavet eelseisva eemaloleku kohta töörühmades ja vestlustes väljaspool rakendust Human Resources.</span><span class="sxs-lookup"><span data-stu-id="532b7-107">In addition, you can send people information about your upcoming time off in teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="532b7-108">Rakenduse installimine</span><span class="sxs-lookup"><span data-stu-id="532b7-108">Install the app</span></span>

<span data-ttu-id="532b7-109">Rakenduse Human Resources leiate Teamsi poest.</span><span class="sxs-lookup"><span data-stu-id="532b7-109">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="532b7-110">Valige kolmikpunktid Microsoft Teamsis.</span><span class="sxs-lookup"><span data-stu-id="532b7-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Human Resources Teamsi puhkuse rakenduse kolmikpunktid](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="532b7-112">Otsige üles Dynamics 365 Human Resources ja seejärel valige paan **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="532b7-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Human Resources Teamsi puhkuse rakenduse paan HR](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="532b7-114">Rakenduse installimiseks valige nupp **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="532b7-114">Select the **Add** button to install the app.</span></span>

   ![Human Resources Teamsi puhkuse rakenduse installimine](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="532b7-116">Kui rakendus ei logi teid automaatselt sisse, valige sisselogimiseks vahekaart **Sätted**.</span><span class="sxs-lookup"><span data-stu-id="532b7-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Human Resources Teamsi puhkuse rakenduse vahekaart Sätted](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="532b7-118">Kui sisselogimise dialoogiboksi ei kuvata, kontrollige oma brauseri sätteid hüpikakende lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="532b7-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="532b7-119">Kui teil on juurdepääs rohkem kui ühele Human Resourcesi eksemplarile, saate valida vahekaardil **Sätted** keskkonna, millega soovite ühenduse luua.</span><span class="sxs-lookup"><span data-stu-id="532b7-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="532b7-120">Rakendus toetab nüüd süsteemiadministraatori turberolli.</span><span class="sxs-lookup"><span data-stu-id="532b7-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="532b7-121">Roboti kasutamine</span><span class="sxs-lookup"><span data-stu-id="532b7-121">Use the bot</span></span>

<span data-ttu-id="532b7-122">Pärast rakenduse installimist kuvatakse tervitussõnum, mis teavitab teid tegevuste tüüpidest, mida robot saab teie eest teha.</span><span class="sxs-lookup"><span data-stu-id="532b7-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Human Resources Teamsi puhkuse rakenduse roboti tervitussõnum](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="532b7-124">Esmakordsel suhtlemisel robotiga peate tõenäoliselt sisse logima.</span><span class="sxs-lookup"><span data-stu-id="532b7-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="532b7-125">Kui sisselogimise dialoogiboksi ei kuvata, kontrollige oma brauseri sätteid hüpikakende lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="532b7-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="532b7-126">Võite paluda robotil teha järgnevat.</span><span class="sxs-lookup"><span data-stu-id="532b7-126">You can ask the bot to:</span></span>

- <span data-ttu-id="532b7-127">Vaba aja saldo teabe kuvamine iga registreeritud puhkuse tüübi kohta.</span><span class="sxs-lookup"><span data-stu-id="532b7-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Human Resources Teamsi puhkuse rakenduse saldode kuvamine](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="532b7-129">Konkreetse puhkuse tüübi täpsemate üksikasjade kuvamine.</span><span class="sxs-lookup"><span data-stu-id="532b7-129">Show additional details about a specific leave type.</span></span>

   ![Human Resources Teamsi puhkuse rakenduse üksikasjade kuvamine](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="532b7-131">Puhkusetaotluse alustamine teie eest.</span><span class="sxs-lookup"><span data-stu-id="532b7-131">Start a leave request for you.</span></span>

   ![Human Resources Teamsi puhkuse rakenduse puhkusetaotlus](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="532b7-133">Pärast puhkusetaotluse esitamist saate päevi muuta otse kaardi kaudu.</span><span class="sxs-lookup"><span data-stu-id="532b7-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![Human Resources Teamsi puhkuse rakenduse taotluse redigeerimine](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="532b7-135">Kui olete lõpetanud teabe sisestamise, valige **Esita**, et esitada see heakskiitmiseks.</span><span class="sxs-lookup"><span data-stu-id="532b7-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="532b7-136">Saate valida ka **Salvesta mustandina**, et hiljem jätkata.</span><span class="sxs-lookup"><span data-stu-id="532b7-136">You can also select **Save as draft** to come back to it later.</span></span>

![Human Resources Teamsi puhkuse rakenduse taotluse esitamine](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="532b7-138">Puhkuse haldamine Teamsis</span><span class="sxs-lookup"><span data-stu-id="532b7-138">Manage your leave in Teams</span></span>

<span data-ttu-id="532b7-139">Vahekaardil **Vaba aeg** saate kuvada järgnevat.</span><span class="sxs-lookup"><span data-stu-id="532b7-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="532b7-140">Saldo teabe iga registreeritud puhkuse tüübi kohta</span><span class="sxs-lookup"><span data-stu-id="532b7-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="532b7-141">Tulevased puhkusetaotlused</span><span class="sxs-lookup"><span data-stu-id="532b7-141">Upcoming leave requests</span></span>

- <span data-ttu-id="532b7-142">Vaba aja taotlused</span><span class="sxs-lookup"><span data-stu-id="532b7-142">Time-off requests</span></span>

- <span data-ttu-id="532b7-143">Puhkusetaotluste mustandid</span><span class="sxs-lookup"><span data-stu-id="532b7-143">Draft leave requests</span></span>

![Human Resources Teamsi puhkuse rakenduse vahekaart Vaba aeg](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="532b7-145">Uue taotluse loomine</span><span class="sxs-lookup"><span data-stu-id="532b7-145">Create a new request</span></span>

1. <span data-ttu-id="532b7-146">Valige uue puhkusetaotluse loomiseks **Uus taotlus**.</span><span class="sxs-lookup"><span data-stu-id="532b7-146">To create a new leave request, select **New request**.</span></span>

   ![Human Resources Teamsi puhkuse rakenduse uus taotlus](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="532b7-148">Sisestage päev või päevad, mida soovite vabaks võtta ja seejärel valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="532b7-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Human Resources Teamsi puhkuse rakenduse vaba aja lisamine](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="532b7-150">Vajadusel sisestage põhjusekood.</span><span class="sxs-lookup"><span data-stu-id="532b7-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="532b7-151">Sisestage ka vajalikud kommentaarid ja lisage manused.</span><span class="sxs-lookup"><span data-stu-id="532b7-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="532b7-152">Kui olete lõpetanud teabe sisestamise, tippige **Esita**, et esitada see heakskiitmiseks.</span><span class="sxs-lookup"><span data-stu-id="532b7-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="532b7-153">Saate tippida ka **Salvesta mustandina**, et hiljem jätkata.</span><span class="sxs-lookup"><span data-stu-id="532b7-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="532b7-154">Taotluste mustandite haldamine</span><span class="sxs-lookup"><span data-stu-id="532b7-154">Manage draft requests</span></span>

1. <span data-ttu-id="532b7-155">Valige vahekaart **Mustandid**.</span><span class="sxs-lookup"><span data-stu-id="532b7-155">Select the **Drafts** tab.</span></span>

   ![Human Resources Teamsi puhkuse rakenduse vahekaart Mustandid](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="532b7-157">Taotluse redigeerimiseks valige pliiats või selle kustutamiseks prügikast.</span><span class="sxs-lookup"><span data-stu-id="532b7-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="532b7-158">Tehke vajalikud muudatused.</span><span class="sxs-lookup"><span data-stu-id="532b7-158">Make any necessary changes.</span></span> <span data-ttu-id="532b7-159">Kui olete lõpetanud teabe sisestamise, tippige **Esita**, et esitada see heakskiitmiseks.</span><span class="sxs-lookup"><span data-stu-id="532b7-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="532b7-160">Saate valida ka **Salvesta mustandina**, et hiljem jätkata.</span><span class="sxs-lookup"><span data-stu-id="532b7-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Human Resources Teamsi puhkuse rakenduse mustandi redigeerimine](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="532b7-162">Rakenduse Teams teatistele vastamine</span><span class="sxs-lookup"><span data-stu-id="532b7-162">Respond to Teams notifications</span></span>

<span data-ttu-id="532b7-163">Kui teie või töötaja olete puhkusetaotluse esitamise kinnitaja, kuvatakse teile Teamsi rakenduses Human Resources vastav teatis.</span><span class="sxs-lookup"><span data-stu-id="532b7-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="532b7-164">Saate valida teatise, et seda vaadata.</span><span class="sxs-lookup"><span data-stu-id="532b7-164">You can select the notification to view it.</span></span> <span data-ttu-id="532b7-165">Teatised kuvatakse ka alal **Vestlus**.</span><span class="sxs-lookup"><span data-stu-id="532b7-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="532b7-166">Kui olete kinnitaja, saate teatises valida **Kinnita** või **Keeldu** .</span><span class="sxs-lookup"><span data-stu-id="532b7-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="532b7-167">Saate ka esitada valikulise teate.</span><span class="sxs-lookup"><span data-stu-id="532b7-167">You can also provide an optional message.</span></span>

![Teamsi rakenduse Human Resources puhkusetaotluse teatis](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="532b7-169">Eelseisva eemaloleku teabe saatmine oma kaastöötajatele</span><span class="sxs-lookup"><span data-stu-id="532b7-169">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="532b7-170">Pärast rakenduse Human Resources installimist rakenduse Teamsi jaoks saate hõlpsalt saata teavet eelseisva eemaloleku kohta oma kaastöötajatele töörühmades või vestlustes.</span><span class="sxs-lookup"><span data-stu-id="532b7-170">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="532b7-171">Valige rakenduse Teams töörühmas või vestluses selle vestlusakna all olev nupp Human Resources.</span><span class="sxs-lookup"><span data-stu-id="532b7-171">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Nupp Human Resources vestlusakna all](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="532b7-173">Valige puhkusetaotlus, mida soovite jagada.</span><span class="sxs-lookup"><span data-stu-id="532b7-173">Select the leave request you want to share.</span></span> <span data-ttu-id="532b7-174">Kui soovite jagada puhkusetaotluse mustandit, valige enne **Mustandid**.</span><span class="sxs-lookup"><span data-stu-id="532b7-174">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Eelseisva puhkusetaotluse valimine jagamiseks](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="532b7-176">Teie puhkusetaotlus kuvatakse vestluses.</span><span class="sxs-lookup"><span data-stu-id="532b7-176">Your leave request will display in the chat.</span></span>

![Rakenduse Human Resources puhkusetaotluse kaart](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="532b7-178">Kui jagasite taotluse mustandit, kuvatakse see mustandina.</span><span class="sxs-lookup"><span data-stu-id="532b7-178">If you shared a draft request, it will display as a draft:</span></span>

![Rakenduse Human Resources puhkusetaotluse mustandi kaart](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="532b7-180">Oma töörühma puhkusekalendri vaatamine</span><span class="sxs-lookup"><span data-stu-id="532b7-180">View your team's leave calendar</span></span>

<span data-ttu-id="532b7-181">Kui olete otseste alluvatega juht, saate vaadata oma töörühma kinnitatud ja ootelolevaid vabu aegu.</span><span class="sxs-lookup"><span data-stu-id="532b7-181">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="532b7-182">Tehke Teamsi rakenduses Human Resources valik **Vaba aeg**.</span><span class="sxs-lookup"><span data-stu-id="532b7-182">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="532b7-183">Valige **Töörühma kalender**.</span><span class="sxs-lookup"><span data-stu-id="532b7-183">Select **Team calendar**.</span></span>

   ![Kalendri kuvamine Teamsi rakenduses Human Resources](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="532b7-185">Kalendris kuvatakse teie otsesed aruanded, mis on kinnitatud ja ootel vaba ajaga.</span><span class="sxs-lookup"><span data-stu-id="532b7-185">The calendar displays your direct reports' approved and pending time off.</span></span>

![Vaba aja kalendri kuvamine Teamsi rakenduses Human Resources](./media/hr-teams-leave-app-calendar.png)

## <a name="privacy-notice"></a><span data-ttu-id="532b7-187">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="532b7-187">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="532b7-188">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="532b7-188">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="532b7-189">Kui Dynamics 365 Human Resourcesi robot on kasutusel Microsoft Teamsis, analüüsitakse kasutaja tekstisisestusi, et mõista aluseks olevat päringut/eesmärki.</span><span class="sxs-lookup"><span data-stu-id="532b7-189">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="532b7-190">Kasutaja sisestus (nt „otsing konto Contoso”) suunatakse Microsofti kognitiivsesse teenusesse nimega Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="532b7-190">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="532b7-191">Lugege lisateavet LUIS-i kohta  [siin](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="532b7-191">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="532b7-192">Teenus LUIS eristab või mõistab kasutaja sisestuse kavatsust (antud juhul on eesmärgiks teabe leidmine) ja sihtüksust (antud juhul on soovitud üksuseks konto nimega Contoso).</span><span class="sxs-lookup"><span data-stu-id="532b7-192">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="532b7-193">Seejärel edastatakse see teave Microsofti  [Azure'i roboti raamistikule](https://azure.microsoft.com/services/bot-service/), mis suhtleb Dynamics 365 Human Resourcesi andmetega ja toob kasutaja päringu vastuseks soovitud teabe.</span><span class="sxs-lookup"><span data-stu-id="532b7-193">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="532b7-194">Kui installite ja lubate juurdepääsu roboti kasutamiseks, annate teenusele LUIS ja Azure'i roboti raamistikule nõusoleku töödelda sisestuse kavatsust, mille tulemuseks on täiustatud vestlusvaatega kasutuskogemus.</span><span class="sxs-lookup"><span data-stu-id="532b7-194">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="532b7-195">Teenusel LUIS ja Azure'i roboti raamistikul võib olla võrreldes Dynamics 365 Human Resourcesiga erinev vastavuse tase.</span><span class="sxs-lookup"><span data-stu-id="532b7-195">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="532b7-196">Kui teenusel LUIS on juurdepääs ainult kasutaja päringutele ja ei ole mõeldud ühendamiseks kasutaja Dynamics 365 Human Resourcesi andmete või kontoga, siis Dynamics 365 Human Resourcesi roboti kasutaja saab vabatahtlikult sisestada kliendiandmeid, isikuandmeid või muid andmeid sisaldavaid päringuid ja selle päringu sisu võidakse saata teenusesse LUIS ja Azure'i roboti raamistikku.</span><span class="sxs-lookup"><span data-stu-id="532b7-196">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="532b7-197">Kasutaja päringute ja sõnumite sisu säilitatakse süsteemis LUIS maksimaalselt 30 päeva, krüptitakse passiivsena ja seda ei kasutata koolituse või teenuse täiustamiseks.</span><span class="sxs-lookup"><span data-stu-id="532b7-197">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="532b7-198">Lisateavet kognitiivsete teenuste kohta leiate [siit](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="532b7-198">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="532b7-199">Microsoft Teamsi rakenduste administraatori sätete haldamiseks minge [Microsoft Teamsi halduskeskusesse](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="532b7-199">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="532b7-200">Microsoft Teams, Azure Event Grid ja Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="532b7-200">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="532b7-201">Rakenduse Dynamics 365 Human Resources kasutamisel rakenduses Microsoft Teams võivad mõned kliendiandmed liikuda väljapoole geograafilist piirkonda, kus teie rentniku teenus Human Resources on juurutatud.</span><span class="sxs-lookup"><span data-stu-id="532b7-201">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="532b7-202">Dynamics 365 Human Resources edastab töötaja puhkusetaotluse ja töövoo ülesande üksikasjad Microsoft Azure Event Gridi ja Microsoft Teamsi.</span><span class="sxs-lookup"><span data-stu-id="532b7-202">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="532b7-203">Neid andmeid võidakse säilitada teenuses Microsoft Azure Event Grid kuni 24 tundi ja töödelda Ameerika Ühendriikides, need krüptitakse edastamisel ja passiivsena ning Microsoft ega selle alamtöötlejad ei kasuta neid koolituste või teenuste täiustamiseks.</span><span class="sxs-lookup"><span data-stu-id="532b7-203">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="532b7-204">Lisateavet selle kohta, kus teie andmeid rakenduses Teams talletatakse, leiate teemast [Andmete asukoht rakenduses Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="532b7-204">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="532b7-205">Vestlusrobotiga suhtlemisel rakenduses Human Resources võidakse vestluse sisu teenuses Azure Cosmos DB talletada ja edastada rakendusele Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="532b7-205">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="532b7-206">Neid andmeid võidakse talletada teenuses Azure Cosmos DB kuni 24 tundi ja töödelda väljaspool geograafilist piirkonda, kus teie rentniku teenus Human Resources on juurutatud, need krüptitakse edastamisel ja passiivsena ning Microsoft ega selle alamtöötlejad ei kasuta neid koolituste või teenuste täiustamiseks.</span><span class="sxs-lookup"><span data-stu-id="532b7-206">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="532b7-207">Lisateavet selle kohta, kus teie andmeid rakenduses Teams talletatakse, leiate teemast [Andmete asukoht rakenduses Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="532b7-207">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="532b7-208">Et piirata oma organisatsiooni või selles olevate kasutajate juurdepääsu rakendusele Human Resources, mis asub rakenduses Microsoft Teams, lugege teemat [Rakenduse lubade poliitika haldamine rakenduses Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="532b7-208">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="532b7-209">Vt ka</span><span class="sxs-lookup"><span data-stu-id="532b7-209">See also</span></span>

[<span data-ttu-id="532b7-210">Microsoft Teamsi allalaadimine ja installimine</span><span class="sxs-lookup"><span data-stu-id="532b7-210">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="532b7-211">Microsoft Teams spikrikeskus</span><span class="sxs-lookup"><span data-stu-id="532b7-211">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="532b7-212">Rakendus Human Resources Teamsis</span><span class="sxs-lookup"><span data-stu-id="532b7-212">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
