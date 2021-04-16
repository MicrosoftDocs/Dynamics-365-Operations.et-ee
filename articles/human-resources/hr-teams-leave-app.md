---
title: Puhkusetaotluste haldamine Teamsis
description: Selles teemas kirjeldatakse, kuidas esitada puhkusetaotlust Microsoft Teamsi rakenduses Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 72fa3309b77717d0291b8b6828ed5bc4c65e95ab
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790568"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="15d94-103">Puhkusetaotluste haldamine Teamsis</span><span class="sxs-lookup"><span data-stu-id="15d94-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="15d94-104">Microsoft Teamsi rakendus Dynamics 365 Human Resources võimaldab teil kiiresti taotleda puhkepäevi ja vaadata vaba aja saldo teavet otse Microsoft Teamsis.</span><span class="sxs-lookup"><span data-stu-id="15d94-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="15d94-105">Saate suhelda robotiga, et taotleda teavet ja algatada puhkusetaotlus.</span><span class="sxs-lookup"><span data-stu-id="15d94-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="15d94-106">Vahekaart **Vaba aeg** annab üksikasjalikumat teavet.</span><span class="sxs-lookup"><span data-stu-id="15d94-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="15d94-107">Lisaks saate inimestele saata teavet eelseisva eemaloleku kohta Teamsis ja vestlustes väljaspool rakendust Human Resources.</span><span class="sxs-lookup"><span data-stu-id="15d94-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="15d94-108">Rakenduse installimine</span><span class="sxs-lookup"><span data-stu-id="15d94-108">Install the app</span></span>

<span data-ttu-id="15d94-109">Rakenduse Dynamics 365 Human Resources leiate Teamsi poest.</span><span class="sxs-lookup"><span data-stu-id="15d94-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="15d94-110">Valige kolmikpunktid Microsoft Teamsis.</span><span class="sxs-lookup"><span data-stu-id="15d94-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Human Resources Teamsi puhkuse rakenduse kolmikpunktid](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="15d94-112">Otsige üles Dynamics 365 Human Resources ja seejärel valige paan **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="15d94-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Human Resources Teamsi puhkuse rakenduse paan HR](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="15d94-114">Rakenduse installimiseks valige nupp **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="15d94-114">Select the **Add** button to install the app.</span></span>

   ![Human Resources Teamsi puhkuse rakenduse installimine](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="15d94-116">Kui rakendus ei logi teid automaatselt sisse, valige sisselogimiseks vahekaart **Sätted**.</span><span class="sxs-lookup"><span data-stu-id="15d94-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Human Resources Teamsi puhkuse rakenduse vahekaart Sätted](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="15d94-118">Kui sisselogimise dialoogiboksi ei kuvata, kontrollige oma brauseri sätteid hüpikakende lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="15d94-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="15d94-119">Kui teil on juurdepääs rohkem kui ühele Human Resourcesi eksemplarile, saate valida vahekaardil **Sätted** keskkonna, millega soovite ühenduse luua.</span><span class="sxs-lookup"><span data-stu-id="15d94-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="15d94-120">Rakendus toetab nüüd süsteemiadministraatori turberolli.</span><span class="sxs-lookup"><span data-stu-id="15d94-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="15d94-121">Roboti kasutamine</span><span class="sxs-lookup"><span data-stu-id="15d94-121">Use the bot</span></span>

<span data-ttu-id="15d94-122">Pärast rakenduse installimist kuvatakse tervitussõnum, mis teavitab teid tegevuste tüüpidest, mida robot saab teie eest teha.</span><span class="sxs-lookup"><span data-stu-id="15d94-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Human Resources Teamsi puhkuse rakenduse roboti tervitussõnum](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="15d94-124">Esmakordsel suhtlemisel robotiga peate tõenäoliselt sisse logima.</span><span class="sxs-lookup"><span data-stu-id="15d94-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="15d94-125">Kui sisselogimise dialoogiboksi ei kuvata, kontrollige oma brauseri sätteid hüpikakende lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="15d94-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="15d94-126">Võite paluda robotil teha järgnevat.</span><span class="sxs-lookup"><span data-stu-id="15d94-126">You can ask the bot to:</span></span>

- <span data-ttu-id="15d94-127">Puhkusetaotluse alustamine teie eest.</span><span class="sxs-lookup"><span data-stu-id="15d94-127">Start a leave request for you.</span></span>

  ![Puhkusetaotluse alustamine Teamsi vestluses](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="15d94-129">Vestlusrobot sisestab puhkusetaotluse andmed teie eest.</span><span class="sxs-lookup"><span data-stu-id="15d94-129">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="15d94-130">Valige **Vaba aja taotlemine** ja redigeerige taotluse üksikasju.</span><span class="sxs-lookup"><span data-stu-id="15d94-130">Select **Request time off** and edit the details for your request.</span></span>

  ![Puhkusetaotluse üksikasjade redigeerimine](./media/hr-teams-leave-app-details.png)

- <span data-ttu-id="15d94-132">Kui olete puhkusetaotluse üksikasjade redigeerimise lõpetanud, valige **Edasta**, et saata taotlus kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="15d94-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![Puhkusetaotluse edastamine](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="15d94-134">Puhkuse haldamine Teamsis</span><span class="sxs-lookup"><span data-stu-id="15d94-134">Manage your leave in Teams</span></span>

<span data-ttu-id="15d94-135">Vahekaardil **Vaba aeg** saate kuvada järgnevat.</span><span class="sxs-lookup"><span data-stu-id="15d94-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="15d94-136">Saldo teabe iga registreeritud puhkuse tüübi kohta</span><span class="sxs-lookup"><span data-stu-id="15d94-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="15d94-137">Tulevased puhkusetaotlused</span><span class="sxs-lookup"><span data-stu-id="15d94-137">Upcoming leave requests</span></span>

- <span data-ttu-id="15d94-138">Vaba aja taotlused</span><span class="sxs-lookup"><span data-stu-id="15d94-138">Time-off requests</span></span>

- <span data-ttu-id="15d94-139">Puhkusetaotluste mustandid</span><span class="sxs-lookup"><span data-stu-id="15d94-139">Draft leave requests</span></span>

![Human Resources Teamsi puhkuse rakenduse vahekaart Vaba aeg](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="15d94-141">Uue taotluse loomine</span><span class="sxs-lookup"><span data-stu-id="15d94-141">Create a new request</span></span>

1. <span data-ttu-id="15d94-142">Valige uue puhkusetaotluse loomiseks **Uus taotlus**.</span><span class="sxs-lookup"><span data-stu-id="15d94-142">To create a new leave request, select **New request**.</span></span>

   ![Human Resources Teamsi puhkuse rakenduse uus taotlus](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="15d94-144">Sisestage päev või päevad, mida soovite vabaks võtta ja seejärel valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="15d94-144">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Human Resources Teamsi puhkuse rakenduse vaba aja lisamine](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="15d94-146">Vajadusel sisestage põhjusekood.</span><span class="sxs-lookup"><span data-stu-id="15d94-146">If applicable, enter a reason code.</span></span> <span data-ttu-id="15d94-147">Sisestage ka vajalikud kommentaarid ja lisage manused.</span><span class="sxs-lookup"><span data-stu-id="15d94-147">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="15d94-148">Kui olete lõpetanud teabe sisestamise, tippige **Esita**, et esitada see heakskiitmiseks.</span><span class="sxs-lookup"><span data-stu-id="15d94-148">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="15d94-149">Saate tippida ka **Salvesta mustandina**, et hiljem jätkata.</span><span class="sxs-lookup"><span data-stu-id="15d94-149">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="15d94-150">Taotluste mustandite haldamine</span><span class="sxs-lookup"><span data-stu-id="15d94-150">Manage draft requests</span></span>

1. <span data-ttu-id="15d94-151">Valige vahekaart **Mustandid**.</span><span class="sxs-lookup"><span data-stu-id="15d94-151">Select the **Drafts** tab.</span></span>

   ![Human Resources Teamsi puhkuse rakenduse vahekaart Mustandid](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="15d94-153">Taotluse redigeerimiseks valige pliiats või selle kustutamiseks prügikast.</span><span class="sxs-lookup"><span data-stu-id="15d94-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="15d94-154">Tehke vajalikud muudatused.</span><span class="sxs-lookup"><span data-stu-id="15d94-154">Make any necessary changes.</span></span> <span data-ttu-id="15d94-155">Kui olete lõpetanud teabe sisestamise, tippige **Esita**, et esitada see heakskiitmiseks.</span><span class="sxs-lookup"><span data-stu-id="15d94-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="15d94-156">Saate valida ka **Salvesta mustandina**, et hiljem jätkata.</span><span class="sxs-lookup"><span data-stu-id="15d94-156">You can also select **Save as draft** to come back to it later.</span></span>

   ![Human Resources Teamsi puhkuse rakenduse mustandi redigeerimine](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="15d94-158">Rakenduse Teams teatistele vastamine</span><span class="sxs-lookup"><span data-stu-id="15d94-158">Respond to Teams notifications</span></span>

<span data-ttu-id="15d94-159">Kui teie või töötaja olete puhkusetaotluse esitamise kinnitaja, kuvatakse teile Teamsi rakenduses Human Resources vastav teatis.</span><span class="sxs-lookup"><span data-stu-id="15d94-159">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="15d94-160">Saate valida teatise, et seda vaadata.</span><span class="sxs-lookup"><span data-stu-id="15d94-160">You can select the notification to view it.</span></span> <span data-ttu-id="15d94-161">Teatised kuvatakse ka alal **Vestlus**.</span><span class="sxs-lookup"><span data-stu-id="15d94-161">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="15d94-162">Kui olete kinnitaja, saate teatises valida **Kinnita** või **Keeldu** .</span><span class="sxs-lookup"><span data-stu-id="15d94-162">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="15d94-163">Saate ka esitada valikulise teate.</span><span class="sxs-lookup"><span data-stu-id="15d94-163">You can also provide an optional message.</span></span>

![Teamsi rakenduse Human Resources puhkusetaotluse teatis](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="15d94-165">Eelseisva eemaloleku teabe saatmine oma kaastöötajatele</span><span class="sxs-lookup"><span data-stu-id="15d94-165">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="15d94-166">Pärast rakenduse Human Resources installimist rakenduse Teamsi jaoks saate hõlpsalt saata teavet eelseisva eemaloleku kohta oma kaastöötajatele töörühmades või vestlustes.</span><span class="sxs-lookup"><span data-stu-id="15d94-166">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="15d94-167">Valige rakenduse Teams töörühmas või vestluses selle vestlusakna all olev nupp Human Resources.</span><span class="sxs-lookup"><span data-stu-id="15d94-167">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Nupp Human Resources vestlusakna all](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="15d94-169">Valige puhkusetaotlus, mida soovite jagada.</span><span class="sxs-lookup"><span data-stu-id="15d94-169">Select the leave request you want to share.</span></span> <span data-ttu-id="15d94-170">Kui soovite jagada puhkusetaotluse mustandit, valige enne **Mustandid**.</span><span class="sxs-lookup"><span data-stu-id="15d94-170">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Eelseisva puhkusetaotluse valimine jagamiseks](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="15d94-172">Teie puhkusetaotlus kuvatakse vestluses.</span><span class="sxs-lookup"><span data-stu-id="15d94-172">Your leave request will display in the chat.</span></span>

![Rakenduse Human Resources puhkusetaotluse kaart](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="15d94-174">Kui jagasite taotluse mustandit, kuvatakse see mustandina.</span><span class="sxs-lookup"><span data-stu-id="15d94-174">If you shared a draft request, it will display as a draft:</span></span>

![Rakenduse Human Resources puhkusetaotluse mustandi kaart](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="15d94-176">Oma töörühma puhkusekalendri vaatamine</span><span class="sxs-lookup"><span data-stu-id="15d94-176">View your team's leave calendar</span></span>

<span data-ttu-id="15d94-177">Kui olete otseste alluvatega juht, saate vaadata oma töörühma kinnitatud ja ootelolevaid vabu aegu.</span><span class="sxs-lookup"><span data-stu-id="15d94-177">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="15d94-178">Tehke Teamsi rakenduses Human Resources valik **Vaba aeg**.</span><span class="sxs-lookup"><span data-stu-id="15d94-178">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="15d94-179">Valige **Töörühma kalender**.</span><span class="sxs-lookup"><span data-stu-id="15d94-179">Select **Team calendar**.</span></span> <span data-ttu-id="15d94-180">Kalendris kuvatakse teie otsesed aruanded, mis on kinnitatud ja ootel vaba ajaga.</span><span class="sxs-lookup"><span data-stu-id="15d94-180">The calendar displays your direct reports' approved and pending time off.</span></span>

   ![Kalendri kuvamine Teamsi rakenduses Human Resources](./media/hr-teams-leave-app-view-calendar.png)

   > [!NOTE]
   > <span data-ttu-id="15d94-182">Kui te ei näe töörühma kalendrit, paluge administraatoril see lubada.</span><span class="sxs-lookup"><span data-stu-id="15d94-182">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="15d94-183">Lisateabe saamiseks vt teemat [Installimine ja häälestus](hr-admin-teams-leave-app.md#install-and-setup).</span><span class="sxs-lookup"><span data-stu-id="15d94-183">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="15d94-184">Toetatud keeled</span><span class="sxs-lookup"><span data-stu-id="15d94-184">Supported languages</span></span>

<span data-ttu-id="15d94-185">Teamsi rakendus Dynamics 365 Human Resources toetab järgmisi keeli:</span><span class="sxs-lookup"><span data-stu-id="15d94-185">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="15d94-186">Lokaadi ID</span><span class="sxs-lookup"><span data-stu-id="15d94-186">Locale ID</span></span> | <span data-ttu-id="15d94-187">Keel</span><span class="sxs-lookup"><span data-stu-id="15d94-187">Language</span></span> |
| --- | --- |
| <span data-ttu-id="15d94-188">de-DE</span><span class="sxs-lookup"><span data-stu-id="15d94-188">de-DE</span></span> | <span data-ttu-id="15d94-189">saksa (Saksamaa)</span><span class="sxs-lookup"><span data-stu-id="15d94-189">German (Germany)</span></span> |
| <span data-ttu-id="15d94-190">es-ES</span><span class="sxs-lookup"><span data-stu-id="15d94-190">es-ES</span></span> | <span data-ttu-id="15d94-191">hispaania (Hispaania)</span><span class="sxs-lookup"><span data-stu-id="15d94-191">Spanish (Spain)</span></span> |
| <span data-ttu-id="15d94-192">es-MX</span><span class="sxs-lookup"><span data-stu-id="15d94-192">es-MX</span></span> | <span data-ttu-id="15d94-193">Hispaania (Mehhiko)</span><span class="sxs-lookup"><span data-stu-id="15d94-193">Spanish (Mexico)</span></span> |
| <span data-ttu-id="15d94-194">fr-CA</span><span class="sxs-lookup"><span data-stu-id="15d94-194">fr-CA</span></span> | <span data-ttu-id="15d94-195">Prantsuse (Kanada)</span><span class="sxs-lookup"><span data-stu-id="15d94-195">French (Canada)</span></span> |
| <span data-ttu-id="15d94-196">fr-FR</span><span class="sxs-lookup"><span data-stu-id="15d94-196">fr-FR</span></span> | <span data-ttu-id="15d94-197">prantsuse (Prantsusmaa)</span><span class="sxs-lookup"><span data-stu-id="15d94-197">French (France)</span></span> |
| <span data-ttu-id="15d94-198">it-IT</span><span class="sxs-lookup"><span data-stu-id="15d94-198">it-IT</span></span> | <span data-ttu-id="15d94-199">itaalia (Itaalia)</span><span class="sxs-lookup"><span data-stu-id="15d94-199">Italian (Italy)</span></span> |
| <span data-ttu-id="15d94-200">nl-NL</span><span class="sxs-lookup"><span data-stu-id="15d94-200">nl-NL</span></span> | <span data-ttu-id="15d94-201">hollandi (Holland)</span><span class="sxs-lookup"><span data-stu-id="15d94-201">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="15d94-202">pt-BR</span><span class="sxs-lookup"><span data-stu-id="15d94-202">pt-BR</span></span> | <span data-ttu-id="15d94-203">portugali (Brasiilia)</span><span class="sxs-lookup"><span data-stu-id="15d94-203">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="15d94-204">tr-TR</span><span class="sxs-lookup"><span data-stu-id="15d94-204">tr-TR</span></span> | <span data-ttu-id="15d94-205">türgi (Türgi)</span><span class="sxs-lookup"><span data-stu-id="15d94-205">Turkish (Turkey)</span></span> |
| <span data-ttu-id="15d94-206">zh-CN</span><span class="sxs-lookup"><span data-stu-id="15d94-206">zh-CN</span></span> | <span data-ttu-id="15d94-207">Hiina (lihtsustatud)</span><span class="sxs-lookup"><span data-stu-id="15d94-207">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="15d94-208">Tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="15d94-208">Troubleshooting</span></span>

<span data-ttu-id="15d94-209">Kui teil on probleeme Teamsis rakendusse Dynamics 365 Human Resources sisselogimisega või selle kasutamisega, proovige neid tõrkeotsingujuhiseid.</span><span class="sxs-lookup"><span data-stu-id="15d94-209">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="15d94-210">Kui teil on pärast tõrkeotsingut endiselt probleeme, siis võtke ühendust tugiteenusega.</span><span class="sxs-lookup"><span data-stu-id="15d94-210">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="15d94-211">Lisateavet leiate teemast [Toe hankimine](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="15d94-211">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="15d94-212">Ma ei saa Teamsis rakendusse Human Resources sisse logida</span><span class="sxs-lookup"><span data-stu-id="15d94-212">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="15d94-213">Kui te ei saa rakendusse sisse logida, siis on võimalik, et konto, mida kasutate rakendusse Microsoft Teams sisse logimiseks, ei ole seotud töötajakirjega rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="15d94-213">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="15d94-214">Võtke ühendust oma süsteemiadministraatoriga, et teha kindlaks, et teie töötajakirje on korralikult seotud.</span><span class="sxs-lookup"><span data-stu-id="15d94-214">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="15d94-215">Tõlkeid ei kuvata õigesti</span><span class="sxs-lookup"><span data-stu-id="15d94-215">Translations don't display correctly</span></span>

<span data-ttu-id="15d94-216">Kui tõlkeid ei kuvata ootuspäraselt, veenduge, et Teamsis valitud keel ühtiks inimressursside mooduli lehel **Kasutaja valikud** valitud keelega.</span><span class="sxs-lookup"><span data-stu-id="15d94-216">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="15d94-217">Otsige Teamsis aknas **Sätted** üles **Rakenduse keel**.</span><span class="sxs-lookup"><span data-stu-id="15d94-217">In Teams, look at **App language** in **Settings**.</span></span>

![Teamsi sätted](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="15d94-219">Valige inimressursside moodulis **Sätted** ja seejärel **Kasutaja valikud**.</span><span class="sxs-lookup"><span data-stu-id="15d94-219">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="15d94-220">Veenduge, et väljal **Keel** oleks valitud sama keel, mis Teamsi väljal **Rakenduse keel**.</span><span class="sxs-lookup"><span data-stu-id="15d94-220">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![Inimressursside mooduli kasutajavalikud](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="15d94-222">Kui tõlkeprobleemid ei lahene, andke meile teada.</span><span class="sxs-lookup"><span data-stu-id="15d94-222">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="15d94-223">Teavet leiate teemast [Finance and Operationsi rakenduste või teenuse Lifecycle Services (LCS) tugi](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-support?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="15d94-223">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-support?toc=/dynamics365/human-resources/toc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="15d94-224">Tõrge puhkusetaotluste kinnitamise korral Teamsis rakenduses Human Resources</span><span class="sxs-lookup"><span data-stu-id="15d94-224">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="15d94-225">Kui saate Teamsi rakenduses puhkusetaotluste kinnitamise katsel tõrke, proovige järgmisi tõrkeotsingutoiminguid.</span><span class="sxs-lookup"><span data-stu-id="15d94-225">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="15d94-226">Veenduge, et konto, mida kasutate rakendusse Microsoft Teams sisse logimiseks, oleks sama, mida kasutate rakendusele Dynamics 365 Human Resources juurde pääsemiseks.</span><span class="sxs-lookup"><span data-stu-id="15d94-226">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="15d94-227">Kontrollige, et te oleks taotluse puhul sobiv kinnitaja, kontrollides puhkuse kinnitamise töövoo sätteid.</span><span class="sxs-lookup"><span data-stu-id="15d94-227">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="15d94-228">Lisateavet puhkusetaotluse töövoogude kohta leiate teemast [Puhkusetaotluse töövoo loomine](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="15d94-228">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="15d94-229">Teadaolevad hõlbustusprobleemid</span><span class="sxs-lookup"><span data-stu-id="15d94-229">Known accessibility issues</span></span>

<span data-ttu-id="15d94-230">Teamsi rakendusel Human Resources on järgmised hõlbustusprobleemid, mille lahendamise nimel teeme tööd, et neid tulevastes väljaannetes poleks.</span><span class="sxs-lookup"><span data-stu-id="15d94-230">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="15d94-231">Väljasta</span><span class="sxs-lookup"><span data-stu-id="15d94-231">Issue</span></span> | <span data-ttu-id="15d94-232">Lahendus või selgitus</span><span class="sxs-lookup"><span data-stu-id="15d94-232">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="15d94-233">400% suumimine töölaual peidab vaates mõned tegevusnupud.</span><span class="sxs-lookup"><span data-stu-id="15d94-233">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="15d94-234">Selle asemel soovitame kasutada luupi, kuni saame sellel tasemel suumi toetada.</span><span class="sxs-lookup"><span data-stu-id="15d94-234">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="15d94-235">VoiceOver teatab vahekaardil **Vaba aeg** nuputoimingust, lugedes ette vaba aja ruudustiku päist.</span><span class="sxs-lookup"><span data-stu-id="15d94-235">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="15d94-236">Ruudustiku päis ja elemendid rühmitatakse aasta kaupa ja need on ahendatavad.</span><span class="sxs-lookup"><span data-stu-id="15d94-236">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="15d94-237">VoiceOver tõlgendab seda kui tegevusüksust, kuid see pole seda.</span><span class="sxs-lookup"><span data-stu-id="15d94-237">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="15d94-238">Vahekaardil **Vaba aeg** saab teha lisaks veel ühe nipsamise, kui valitakse uue taotluse **põhjuse kood**.</span><span class="sxs-lookup"><span data-stu-id="15d94-238">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="15d94-239">See nipsamine ei ava siiski ühtki peidetud juhtelementi.</span><span class="sxs-lookup"><span data-stu-id="15d94-239">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="15d94-240">Kui nipsate vahekaardil **Vaba aeg** avatud kalendri korral, liigutakse uue taotluse korral või taotluse redigeerimisel ülaosa asemel hoopis juhtelemendist välja.</span><span class="sxs-lookup"><span data-stu-id="15d94-240">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="15d94-241">Kui jõuate valikuni **Liigu tänase juurde**, võtke arvesse, et see on juhtelemendi lõpp ja nipske vastassuunas, et tagasi algusse saada.</span><span class="sxs-lookup"><span data-stu-id="15d94-241">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="15d94-242">Vahekaardil **Vestlus** viiakse fookus tagasi algusse, kui sisestate kuupäeva abistavat tööriista kaustades või klaviatuuri abil valides.</span><span class="sxs-lookup"><span data-stu-id="15d94-242">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="15d94-243">Vajutage tabeldusklahvi, kuni jõuate uuesti sisendi juurde.</span><span class="sxs-lookup"><span data-stu-id="15d94-243">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="15d94-244">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="15d94-244">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="15d94-245">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="15d94-245">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="15d94-246">Kui Dynamics 365 Human Resourcesi robot on kasutusel Microsoft Teamsis, analüüsitakse kasutaja tekstisisestusi, et mõista aluseks olevat päringut/eesmärki.</span><span class="sxs-lookup"><span data-stu-id="15d94-246">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="15d94-247">Kasutaja sisestus (nt „otsing konto Contoso”) suunatakse Microsofti kognitiivsesse teenusesse nimega Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="15d94-247">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="15d94-248">Lugege lisateavet LUIS-i kohta  [siin](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="15d94-248">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="15d94-249">Teenus LUIS eristab või mõistab kasutaja sisestuse kavatsust (antud juhul on eesmärgiks teabe leidmine) ja sihtüksust (antud juhul on soovitud üksuseks konto nimega Contoso).</span><span class="sxs-lookup"><span data-stu-id="15d94-249">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="15d94-250">Seejärel edastatakse see teave Microsofti  [Azure'i roboti raamistikule](https://azure.microsoft.com/services/bot-service/), mis suhtleb Dynamics 365 Human Resourcesi andmetega ja toob kasutaja päringu vastuseks soovitud teabe.</span><span class="sxs-lookup"><span data-stu-id="15d94-250">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="15d94-251">Kui installite ja lubate juurdepääsu roboti kasutamiseks, annate teenusele LUIS ja Azure'i roboti raamistikule nõusoleku töödelda sisestuse kavatsust, mille tulemuseks on täiustatud vestlusvaatega kasutuskogemus.</span><span class="sxs-lookup"><span data-stu-id="15d94-251">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="15d94-252">Teenusel LUIS ja Azure'i roboti raamistikul võib olla võrreldes Dynamics 365 Human Resourcesiga erinev vastavuse tase.</span><span class="sxs-lookup"><span data-stu-id="15d94-252">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="15d94-253">Kui teenusel LUIS on juurdepääs ainult kasutaja päringutele ja ei ole mõeldud ühendamiseks kasutaja Dynamics 365 Human Resourcesi andmete või kontoga, siis Dynamics 365 Human Resourcesi roboti kasutaja saab vabatahtlikult sisestada kliendiandmeid, isikuandmeid või muid andmeid sisaldavaid päringuid ja selle päringu sisu võidakse saata teenusesse LUIS ja Azure'i roboti raamistikku.</span><span class="sxs-lookup"><span data-stu-id="15d94-253">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="15d94-254">Kasutaja päringute ja sõnumite sisu säilitatakse süsteemis LUIS maksimaalselt 30 päeva, krüptitakse passiivsena ja seda ei kasutata koolituse või teenuse täiustamiseks.</span><span class="sxs-lookup"><span data-stu-id="15d94-254">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="15d94-255">Lisateavet kognitiivsete teenuste kohta leiate [siit](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="15d94-255">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="15d94-256">Microsoft Teamsi rakenduste administraatori sätete haldamiseks minge [Microsoft Teamsi halduskeskusesse](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="15d94-256">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="15d94-257">Microsoft Teams, Azure Event Grid ja Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="15d94-257">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="15d94-258">Rakenduse Dynamics 365 Human Resources kasutamisel rakenduses Microsoft Teams võivad mõned kliendiandmed liikuda väljapoole geograafilist piirkonda, kus teie rentniku teenus Human Resources on juurutatud.</span><span class="sxs-lookup"><span data-stu-id="15d94-258">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="15d94-259">Dynamics 365 Human Resources edastab töötaja puhkusetaotluse ja töövoo ülesande üksikasjad Microsoft Azure Event Gridi ja Microsoft Teamsi.</span><span class="sxs-lookup"><span data-stu-id="15d94-259">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="15d94-260">Neid andmeid võidakse säilitada teenuses Microsoft Azure Event Grid kuni 24 tundi ja töödelda Ameerika Ühendriikides, need krüptitakse edastamisel ja passiivsena ning Microsoft ega selle alamtöötlejad ei kasuta neid koolituste või teenuste täiustamiseks.</span><span class="sxs-lookup"><span data-stu-id="15d94-260">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="15d94-261">Lisateavet selle kohta, kus teie andmeid rakenduses Teams talletatakse, leiate teemast [Andmete asukoht rakenduses Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="15d94-261">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="15d94-262">Vestlusrobotiga suhtlemisel rakenduses Human Resources võidakse vestluse sisu teenuses Azure Cosmos DB talletada ja edastada rakendusele Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="15d94-262">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="15d94-263">Neid andmeid võidakse talletada teenuses Azure Cosmos DB kuni 24 tundi ja töödelda väljaspool geograafilist piirkonda, kus teie rentniku teenus Human Resources on juurutatud, need krüptitakse edastamisel ja passiivsena ning Microsoft ega selle alamtöötlejad ei kasuta neid koolituste või teenuste täiustamiseks.</span><span class="sxs-lookup"><span data-stu-id="15d94-263">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="15d94-264">Lisateavet selle kohta, kus teie andmeid rakenduses Teams talletatakse, leiate teemast [Andmete asukoht rakenduses Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="15d94-264">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="15d94-265">Et piirata oma organisatsiooni või selles olevate kasutajate juurdepääsu rakendusele Human Resources, mis asub rakenduses Microsoft Teams, lugege teemat [Rakenduse lubade poliitika haldamine rakenduses Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="15d94-265">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="15d94-266">Vt ka</span><span class="sxs-lookup"><span data-stu-id="15d94-266">See also</span></span>

[<span data-ttu-id="15d94-267">Microsoft Teamsi allalaadimine ja installimine</span><span class="sxs-lookup"><span data-stu-id="15d94-267">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="15d94-268">Microsoft Teams spikrikeskus</span><span class="sxs-lookup"><span data-stu-id="15d94-268">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="15d94-269">Rakendus Human Resources Teamsis</span><span class="sxs-lookup"><span data-stu-id="15d94-269">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]