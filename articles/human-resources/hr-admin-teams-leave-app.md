---
title: Rakendus Human Resources Teamsis
description: Selles teemas tutvustatakse Microsoft Teamsi rakendust Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3926acd07a68f59682c18f4f7bc290dc1e21d0b6
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889736"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="cfcef-103">Rakendus Human Resources Teamsis</span><span class="sxs-lookup"><span data-stu-id="cfcef-103">Human Resources app in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="cfcef-104">Microsoft Teamsi rakendus Microsoft Dynamics 365 Human Resources võimaldab töövõtjatel kiirelt esitada vaba aja taotlust ja kuvada vaba aja saldo teavet otse Microsoft Teamsis.</span><span class="sxs-lookup"><span data-stu-id="cfcef-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="cfcef-105">Teabe taotlemiseks saavad töövõtjad suhelda robotiga.</span><span class="sxs-lookup"><span data-stu-id="cfcef-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="cfcef-106">Vahekaart **Vaba aeg** annab üksikasjalikumat teavet.</span><span class="sxs-lookup"><span data-stu-id="cfcef-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="cfcef-107">Lisaks saavad nad saata inimestele teavet eelseisva eemaloleku kohta töörühmades ja vestlustes väljaspool rakendust Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cfcef-107">In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Human Resources Teamsi puhkuste rakenduse robot](./media/hr-teams-leave-app-bot.png)

![Human Resources Teamsi puhkuse rakenduse vahekaart Vaba aeg](./media/hr-teams-leave-app-timeoff-tab.png)

![Rakenduse Human Resources puhkusetaotluse kaart](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="cfcef-111">Installimine ja häälestus</span><span class="sxs-lookup"><span data-stu-id="cfcef-111">Install and setup</span></span>

<span data-ttu-id="cfcef-112">Rakenduse Dynamics 365 Human Resources leiate Teamsi poest.</span><span class="sxs-lookup"><span data-stu-id="cfcef-112">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span> <span data-ttu-id="cfcef-113">Lisateabe saamiseks Teamsi rakenduse installimise kohta, vaadake teemat [Puhkusetaotluste haldamine Teamsis](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="cfcef-113">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="cfcef-114">Lisateabe saamiseks rakenduse lubade haldamise kohta Teamsis, vaadake teemat [Rakenduse lubade poliitikate haldamine Microsoft Teamsis](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="cfcef-114">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

<span data-ttu-id="cfcef-115">Kui soovite, et kasutajad saaksid rakenduses vaadata puhkuste ja puudumise kalendrit, peate sätte **Puhkuste ja puudumiste kalender Teamsis** funktsioonihalduse kaudu lubama.</span><span class="sxs-lookup"><span data-stu-id="cfcef-115">If you want your users to view the Leave and absence calendar in the app, you'll need to enable the **Leave and absence calendar in Teams** in Feature management.</span></span> <span data-ttu-id="cfcef-116">Lisateavet funktsioonide lubamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="cfcef-116">For more information about enabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="cfcef-117">Teatiste lubamine rakenduse Human Resources jaoks Teamsis</span><span class="sxs-lookup"><span data-stu-id="cfcef-117">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="cfcef-118">Kui soovite, et kasutajad saaksid puhkusetaotluse teatisi Teamsis vastu võtta, peate lubama teatised rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cfcef-118">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Dynamics 365 Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="cfcef-119">Teatisi saavad ainult need kasutajad, kes on Teamsis sisse logitud ja kasutavad Teamsis rakendust Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cfcef-119">Only users who are signed into Teams and using the Dynamics 365 Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="cfcef-120">Valige rakenduses Human Resources suvand **Süsteemihaldus**.</span><span class="sxs-lookup"><span data-stu-id="cfcef-120">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="cfcef-121">Valige **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="cfcef-121">Select **Links**.</span></span>

3. <span data-ttu-id="cfcef-122">Tehke jaotises **Seadistamine** valik **Süsteemi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="cfcef-122">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="cfcef-123">Seadke vahekaardil **Üldine** seade **Teatiste lubamine rakenduse Teams jaoks** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="cfcef-123">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Teamsi rakenduse teatiste lubamine süsteemi parameetrites](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="cfcef-125">Kõigi kasutajate jaoks Teamsi teatiste sisselülitamiseks valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="cfcef-125">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Teamsi teatiste lubamine kõigi kasutajate jaoks](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="cfcef-127">Üksikutele kasutajate jaoks Teamsi teatiste sisse- või väljalülitamine</span><span class="sxs-lookup"><span data-stu-id="cfcef-127">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="cfcef-128">Kui olete lubanud Teamsis rakenduse Dynamics 365 Human Resources teatised, saate teatised üksikute kasutajate jaoks sisse või välja lülitada.</span><span class="sxs-lookup"><span data-stu-id="cfcef-128">After you've enabled notifications for the Dynamics 365 Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="cfcef-129">Valige rakenduses Human Resources suvand **Süsteemihaldus**.</span><span class="sxs-lookup"><span data-stu-id="cfcef-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="cfcef-130">Valige **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="cfcef-130">Select **Links**.</span></span>

3. <span data-ttu-id="cfcef-131">Tehke jaotises **Kasutajad** valik **Kasutaja valikud**.</span><span class="sxs-lookup"><span data-stu-id="cfcef-131">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="cfcef-132">Valige vahekaart **Töövoog**.</span><span class="sxs-lookup"><span data-stu-id="cfcef-132">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="cfcef-133">Määrake seade **Teatiste lubamine rakenduse Teams jaoks** väärtuseks **Jah**, et lubada kasutajate jaoks teatiste kuvamine, või **Ei**, et keelata kasutajale teatiste kuvamine.</span><span class="sxs-lookup"><span data-stu-id="cfcef-133">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Teamsi rakenduse teatiste lubamine kasutaja suvandite vahekaardil Töövoog](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="cfcef-135">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="cfcef-135">Select **Save**.</span></span>

## <a name="supported-languages"></a><span data-ttu-id="cfcef-136">Toetatud keeled</span><span class="sxs-lookup"><span data-stu-id="cfcef-136">Supported languages</span></span>

<span data-ttu-id="cfcef-137">Teamsi rakendus Dynamics 365 Human Resources toetab järgmisi keeli:</span><span class="sxs-lookup"><span data-stu-id="cfcef-137">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="cfcef-138">Lokaadi ID</span><span class="sxs-lookup"><span data-stu-id="cfcef-138">Locale ID</span></span> | <span data-ttu-id="cfcef-139">Keel</span><span class="sxs-lookup"><span data-stu-id="cfcef-139">Language</span></span> |
| --- | --- |
| <span data-ttu-id="cfcef-140">de-DE</span><span class="sxs-lookup"><span data-stu-id="cfcef-140">de-DE</span></span> | <span data-ttu-id="cfcef-141">saksa (Saksamaa)</span><span class="sxs-lookup"><span data-stu-id="cfcef-141">German (Germany)</span></span> |
| <span data-ttu-id="cfcef-142">es-ES</span><span class="sxs-lookup"><span data-stu-id="cfcef-142">es-ES</span></span> | <span data-ttu-id="cfcef-143">hispaania (Hispaania)</span><span class="sxs-lookup"><span data-stu-id="cfcef-143">Spanish (Spain)</span></span> |
| <span data-ttu-id="cfcef-144">es-MX</span><span class="sxs-lookup"><span data-stu-id="cfcef-144">es-MX</span></span> | <span data-ttu-id="cfcef-145">Hispaania (Mehhiko)</span><span class="sxs-lookup"><span data-stu-id="cfcef-145">Spanish (Mexico)</span></span> |
| <span data-ttu-id="cfcef-146">fr-CA</span><span class="sxs-lookup"><span data-stu-id="cfcef-146">fr-CA</span></span> | <span data-ttu-id="cfcef-147">Prantsuse (Kanada)</span><span class="sxs-lookup"><span data-stu-id="cfcef-147">French (Canada)</span></span> |
| <span data-ttu-id="cfcef-148">fr-FR</span><span class="sxs-lookup"><span data-stu-id="cfcef-148">fr-FR</span></span> | <span data-ttu-id="cfcef-149">prantsuse (Prantsusmaa)</span><span class="sxs-lookup"><span data-stu-id="cfcef-149">French (France)</span></span> |
| <span data-ttu-id="cfcef-150">it-IT</span><span class="sxs-lookup"><span data-stu-id="cfcef-150">it-IT</span></span> | <span data-ttu-id="cfcef-151">itaalia (Itaalia)</span><span class="sxs-lookup"><span data-stu-id="cfcef-151">Italian (Italy)</span></span> |
| <span data-ttu-id="cfcef-152">nl-NL</span><span class="sxs-lookup"><span data-stu-id="cfcef-152">nl-NL</span></span> | <span data-ttu-id="cfcef-153">hollandi (Holland)</span><span class="sxs-lookup"><span data-stu-id="cfcef-153">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="cfcef-154">pt-BR</span><span class="sxs-lookup"><span data-stu-id="cfcef-154">pt-BR</span></span> | <span data-ttu-id="cfcef-155">portugali (Brasiilia)</span><span class="sxs-lookup"><span data-stu-id="cfcef-155">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="cfcef-156">tr-TR</span><span class="sxs-lookup"><span data-stu-id="cfcef-156">tr-TR</span></span> | <span data-ttu-id="cfcef-157">türgi (Türgi)</span><span class="sxs-lookup"><span data-stu-id="cfcef-157">Turkish (Turkey)</span></span> |
| <span data-ttu-id="cfcef-158">zh-CN</span><span class="sxs-lookup"><span data-stu-id="cfcef-158">zh-CN</span></span> | <span data-ttu-id="cfcef-159">Hiina (lihtsustatud)</span><span class="sxs-lookup"><span data-stu-id="cfcef-159">Chinese (Simplified)</span></span> |

## <a name="notes"></a><span data-ttu-id="cfcef-160">Märkmed</span><span class="sxs-lookup"><span data-stu-id="cfcef-160">Notes</span></span>

<span data-ttu-id="cfcef-161">Järgmised tööüksused on kavas välja anda tulevastes väljalasetes:</span><span class="sxs-lookup"><span data-stu-id="cfcef-161">The following work items are slated for future releases:</span></span>

| <span data-ttu-id="cfcef-162">Tööüksus</span><span class="sxs-lookup"><span data-stu-id="cfcef-162">Work item</span></span> | <span data-ttu-id="cfcef-163">Olek</span><span class="sxs-lookup"><span data-stu-id="cfcef-163">Status</span></span> |
| --- | --- |
| <span data-ttu-id="cfcef-164">Tulevaks kuupäevaks vaba aja taotlemisel on vale saldo.</span><span class="sxs-lookup"><span data-stu-id="cfcef-164">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="cfcef-165">Prognoosimine pole veel saadaval.</span><span class="sxs-lookup"><span data-stu-id="cfcef-165">Forecasting isn't yet available.</span></span> <span data-ttu-id="cfcef-166">Kuvatakse praeguse kuupäeva saldo.</span><span class="sxs-lookup"><span data-stu-id="cfcef-166">The balance displays for the current date.</span></span> |
| <span data-ttu-id="cfcef-167">Taotlust **Läbivaatamisel** ei saa tühistada.</span><span class="sxs-lookup"><span data-stu-id="cfcef-167">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="cfcef-168">See funktsioon ei ole praegu toetatud ja lisatakse tulevasse väljalaskesse.</span><span class="sxs-lookup"><span data-stu-id="cfcef-168">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="cfcef-169">Saldo teavet arvutatakse alates tänasest.</span><span class="sxs-lookup"><span data-stu-id="cfcef-169">Balance information is calculated as of today.</span></span> | <span data-ttu-id="cfcef-170">Süsteem ei kuva praegu puhkuseperioodi seisuga saldosid, isegi kui see on konfigureeritud puhkuste ja puudumiste parameetrites.</span><span class="sxs-lookup"><span data-stu-id="cfcef-170">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="cfcef-171">Tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="cfcef-171">Troubleshooting</span></span>

<span data-ttu-id="cfcef-172">Kui kasutajal on probleeme Human Resources Teamsi rakendusse sisselogimisega või selle kasutamisega, proovige neid tõrkeotsingujuhiseid järgida.</span><span class="sxs-lookup"><span data-stu-id="cfcef-172">If a user is having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="cfcef-173">Kui teil on pärast tõrkeotsingut endiselt probleeme, siis võtke ühendust tugiteenusega.</span><span class="sxs-lookup"><span data-stu-id="cfcef-173">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="cfcef-174">Lisateavet leiate teemast [Toe hankimine](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="cfcef-174">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="cfcef-175">Ma ei saa Teamsis rakendusse Human Resources sisse logida</span><span class="sxs-lookup"><span data-stu-id="cfcef-175">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="cfcef-176">Kui kasutaja võtab teiega ühendust, kuna ta ei saa rakendusse sisse logida, veenduge, et tal oleks rakenduses Human Resources seotud töötajakirje.</span><span class="sxs-lookup"><span data-stu-id="cfcef-176">If a user contacts you because they can't sign into the app, verify that they have an associated employee record in Human Resources.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="cfcef-177">Tõrge puhkusetaotluste kinnitamise korral Teamsis rakenduses Human Resources</span><span class="sxs-lookup"><span data-stu-id="cfcef-177">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="cfcef-178">Kui kasutaja saab Teamsi rakenduses puhkusetaotluste kinnitamise katsel tõrke, proovige järgmisi tõrkeotsingutoiminguid.</span><span class="sxs-lookup"><span data-stu-id="cfcef-178">If a user receives an error while trying to approve,  leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="cfcef-179">Veenduge, et tema Teamsi konto oleks sama, mida ta kasutab rakendusele Human Resources juurdepääsemiseks.</span><span class="sxs-lookup"><span data-stu-id="cfcef-179">Verify that their Teams account is the same one they use for accessing Human Resources.</span></span>

2. <span data-ttu-id="cfcef-180">Kontrollige, et ta oleks taotluse puhul sobiv kinnitaja, kontrollides puhkuse kinnitamise töövoo sätteid.</span><span class="sxs-lookup"><span data-stu-id="cfcef-180">Verify that they're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="cfcef-181">Lisateavet puhkusetaotluse töövoogude kohta leiate teemast [Puhkusetaotluse töövoo loomine](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="cfcef-181">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="cfcef-182">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="cfcef-182">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="cfcef-183">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="cfcef-183">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="cfcef-184">Kui Dynamics 365 Human Resourcesi robot on kasutusel Microsoft Teamsis, analüüsitakse kasutaja tekstisisestusi, et mõista aluseks olevat päringut/eesmärki.</span><span class="sxs-lookup"><span data-stu-id="cfcef-184">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="cfcef-185">Kasutaja sisestus (nt „otsing konto Contoso”) suunatakse Microsofti kognitiivsesse teenusesse nimega Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="cfcef-185">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="cfcef-186">Lugege lisateavet LUIS-i kohta  [siin](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="cfcef-186">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="cfcef-187">Teenus LUIS eristab või mõistab kasutaja sisestuse kavatsust (antud juhul on eesmärgiks teabe leidmine) ja sihtüksust (antud juhul on soovitud üksuseks konto nimega Contoso).</span><span class="sxs-lookup"><span data-stu-id="cfcef-187">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="cfcef-188">Seejärel edastatakse see teave Microsofti  [Azure'i roboti raamistikule](https://azure.microsoft.com/services/bot-service/), mis suhtleb Dynamics 365 Human Resourcesi andmetega ja toob kasutaja päringu vastuseks soovitud teabe.</span><span class="sxs-lookup"><span data-stu-id="cfcef-188">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="cfcef-189">Kui installite ja lubate juurdepääsu roboti kasutamiseks, annate teenusele LUIS ja Azure'i roboti raamistikule nõusoleku töödelda sisestuse kavatsust, mille tulemuseks on täiustatud vestlusvaatega kasutuskogemus.</span><span class="sxs-lookup"><span data-stu-id="cfcef-189">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="cfcef-190">Teenusel LUIS ja Azure'i roboti raamistikul võib olla võrreldes Dynamics 365 Human Resourcesiga erinev vastavuse tase.</span><span class="sxs-lookup"><span data-stu-id="cfcef-190">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="cfcef-191">Kui teenusel LUIS on juurdepääs ainult kasutaja päringutele ja ei ole mõeldud ühendamiseks kasutaja Dynamics 365 Human Resourcesi andmete või kontoga, siis Dynamics 365 Human Resourcesi roboti kasutaja saab vabatahtlikult sisestada kliendiandmeid, isikuandmeid või muid andmeid sisaldavaid päringuid ja selle päringu sisu võidakse saata teenusesse LUIS ja Azure'i roboti raamistikku.</span><span class="sxs-lookup"><span data-stu-id="cfcef-191">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="cfcef-192">Kasutaja päringute ja sõnumite sisu säilitatakse süsteemis LUIS maksimaalselt 30 päeva, krüptitakse passiivsena ja seda ei kasutata koolituse või teenuse täiustamiseks.</span><span class="sxs-lookup"><span data-stu-id="cfcef-192">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="cfcef-193">Lisateavet kognitiivsete teenuste kohta leiate [siit](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="cfcef-193">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="cfcef-194">Microsoft Teamsi rakenduste administraatori sätete haldamiseks minge [Microsoft Teamsi halduskeskusesse](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="cfcef-194">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="cfcef-195">Microsoft Teams, Azure Event Grid ja Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="cfcef-195">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="cfcef-196">Rakenduse Dynamics 365 Human Resources kasutamisel rakenduses Microsoft Teams võivad mõned kliendiandmed liikuda väljapoole geograafilist piirkonda, kus teie rentniku teenus Human Resources on juurutatud.</span><span class="sxs-lookup"><span data-stu-id="cfcef-196">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="cfcef-197">Dynamics 365 Human Resources edastab töötaja puhkusetaotluse ja töövoo ülesande üksikasjad Microsoft Azure Event Gridi ja Microsoft Teamsi.</span><span class="sxs-lookup"><span data-stu-id="cfcef-197">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="cfcef-198">Neid andmeid võidakse säilitada teenuses Microsoft Azure Event Grid kuni 24 tundi ja töödelda Ameerika Ühendriikides, need krüptitakse edastamisel ja passiivsena ning Microsoft ega selle alamtöötlejad ei kasuta neid koolituste või teenuste täiustamiseks.</span><span class="sxs-lookup"><span data-stu-id="cfcef-198">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="cfcef-199">Lisateavet selle kohta, kus teie andmeid rakenduses Teams talletatakse, leiate teemast [Andmete asukoht rakenduses Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="cfcef-199">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="cfcef-200">Vestlusrobotiga suhtlemisel rakenduses Human Resources võidakse vestluse sisu teenuses Azure Cosmos DB talletada ja edastada rakendusele Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="cfcef-200">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="cfcef-201">Neid andmeid võidakse talletada teenuses Azure Cosmos DB kuni 24 tundi ja töödelda väljaspool geograafilist piirkonda, kus teie rentniku teenus Human Resources on juurutatud, need krüptitakse edastamisel ja passiivsena ning Microsoft ega selle alamtöötlejad ei kasuta neid koolituste või teenuste täiustamiseks.</span><span class="sxs-lookup"><span data-stu-id="cfcef-201">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="cfcef-202">Lisateavet selle kohta, kus teie andmeid rakenduses Teams talletatakse, leiate teemast [Andmete asukoht rakenduses Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="cfcef-202">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="cfcef-203">Et piirata oma organisatsiooni või selles olevate kasutajate juurdepääsu rakendusele Human Resources, mis asub rakenduses Microsoft Teams, lugege teemat [Rakenduse lubade poliitika haldamine rakenduses Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="cfcef-203">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="cfcef-204">Vt ka</span><span class="sxs-lookup"><span data-stu-id="cfcef-204">See also</span></span> 

[<span data-ttu-id="cfcef-205">Microsoft Teamsi allalaadimine ja installimine</span><span class="sxs-lookup"><span data-stu-id="cfcef-205">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="cfcef-206">Microsoft Teams spikrikeskus</span><span class="sxs-lookup"><span data-stu-id="cfcef-206">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="cfcef-207">Puhkusetaotluste haldamine Teamsis</span><span class="sxs-lookup"><span data-stu-id="cfcef-207">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]