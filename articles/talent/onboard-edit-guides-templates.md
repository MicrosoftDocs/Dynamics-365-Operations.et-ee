---
title: Sisseelamisjuhendite ja mallide redigeerimine rakenduses Dynamics 365 for Talent - Onboard
description: See teema selgitab, kuidas lisada Microsoftis sisseelamisjuhendite ja mallide jaoks tegevusi ja muud teavet rakenduses Dynamics 365 for Talent - Onboard.
author: andreabichsel
manager: ''
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 68afc5d789d1f4af67cd2ec73eb0e073efad0761
ms.sourcegitcommit: 4ff8c2c2f3705d8045df66f2c4393253e05b49ed
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864389"
---
# <a name="edit-onboarding-guides-and-templates-in-dynamics-365-for-talent-onboard"></a><span data-ttu-id="9aff7-103">Sisseelamisjuhendite ja mallide redigeerimine rakenduses Dynamics 365 for Talent: Onboard</span><span class="sxs-lookup"><span data-stu-id="9aff7-103">Edit onboarding guides and templates in Dynamics 365 for Talent: Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9aff7-104">Pärast seda, kui olete Microsoftis Dynamics 365 for Talent: Onboard käivitanud juhendi või malli, tuleb teil lisada sissejuhatus, tegevused, kontaktid ja ressursid.</span><span class="sxs-lookup"><span data-stu-id="9aff7-104">After you create an onboarding guide or template in Microsoft Dynamics 365 for Talent: Onboard, you must add an introduction, activities, contacts, and resources.</span></span> <span data-ttu-id="9aff7-105">Onboard võimaldab teil lisada rikkalikku sisu sisseelamisjuhenditesse, sealhulgas:</span><span class="sxs-lookup"><span data-stu-id="9aff7-105">Onboard lets you include rich content in your onboarding guides, including:</span></span>

- <span data-ttu-id="9aff7-106">YouTube'i videod</span><span class="sxs-lookup"><span data-stu-id="9aff7-106">YouTube videos</span></span>
- <span data-ttu-id="9aff7-107">Microsoft Sway esitlusi</span><span class="sxs-lookup"><span data-stu-id="9aff7-107">Microsoft Sway presentations</span></span>
- <span data-ttu-id="9aff7-108">Microsoft PowerApps rakendused</span><span class="sxs-lookup"><span data-stu-id="9aff7-108">Microsoft PowerApps apps</span></span>
- <span data-ttu-id="9aff7-109">Microsoft Streami videod</span><span class="sxs-lookup"><span data-stu-id="9aff7-109">Microsoft Stream videos</span></span>
- <span data-ttu-id="9aff7-110">Microsoft Formsi vormid</span><span class="sxs-lookup"><span data-stu-id="9aff7-110">Microsoft Forms forms</span></span>
- <span data-ttu-id="9aff7-111">Veebisisu sisaldavad iframe'id</span><span class="sxs-lookup"><span data-stu-id="9aff7-111">Iframes that contains web content</span></span>

## <a name="edit-introductions-or-activities-imported-from-a-template"></a><span data-ttu-id="9aff7-112">Mallist imporditud asustamise või tegevuste redigeerimine</span><span class="sxs-lookup"><span data-stu-id="9aff7-112">Edit introductions or activities imported from a template</span></span>

<span data-ttu-id="9aff7-113">Kui loote sisseelamisjuhendi mallist või kui impordite tegevusi ühest mallist teise, märkate imporditud tegevuste **Lukustamise** nuppu.</span><span class="sxs-lookup"><span data-stu-id="9aff7-113">If you create an onboarding guide from a template, or if you import activities from one template into another, you'll notice a **Lock** button on the imported activities.</span></span> <span data-ttu-id="9aff7-114">Neid kutsutakse *Hallatavaks tegevuseks*.</span><span class="sxs-lookup"><span data-stu-id="9aff7-114">These are called *managed activities*.</span></span>

<span data-ttu-id="9aff7-115">[![Hallatud tegevused](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span><span class="sxs-lookup"><span data-stu-id="9aff7-115">[![Managed activities](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span></span>

<span data-ttu-id="9aff7-116">Hallatud tegevuste valimisel saate kuvada allikamalli tegevuste ülaosas.</span><span class="sxs-lookup"><span data-stu-id="9aff7-116">When you select a managed activity, you can see the source template at the top of the activity.</span></span>

<span data-ttu-id="9aff7-117">[![Hallatud tegevuste allikas](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span><span class="sxs-lookup"><span data-stu-id="9aff7-117">[![Managed activity source](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span></span>

<span data-ttu-id="9aff7-118">Kui redigeerite mõnda tegevust mallis, lükkab Onboard muudatused ümber kõigile mallil põhinevatele mallidele ja saatmata juhenditele.</span><span class="sxs-lookup"><span data-stu-id="9aff7-118">If you edit an activity in a template, Onboard will push the changes to all templates and unsent guides that are based on that template.</span></span> <span data-ttu-id="9aff7-119">Kui valite saatmata juhendi, mis põhineb redigeeritud mallil ja valite seejärel vahekaardi **Tegevused**, kuvatakse teade, et teie juhend on muutunud.</span><span class="sxs-lookup"><span data-stu-id="9aff7-119">If you select an unsent guide based on a template you edited and then select the **Activities** tab in the guide, you will see a notice that your guide has changed.</span></span> <span data-ttu-id="9aff7-120">Teatise lõpetamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="9aff7-120">To dismiss the notification, select **OK**.</span></span> 

<span data-ttu-id="9aff7-121">[![Teatise muutmine.](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span><span class="sxs-lookup"><span data-stu-id="9aff7-121">[![Change notification](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span></span>

<span data-ttu-id="9aff7-122">Kuvatakse värskendatud tegevuste kõrval must täpp.</span><span class="sxs-lookup"><span data-stu-id="9aff7-122">You'll see a black dot next to the updated activities.</span></span>

<span data-ttu-id="9aff7-123">[![Muudetud tegevus](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span><span class="sxs-lookup"><span data-stu-id="9aff7-123">[![Changed activity](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span></span>

<span data-ttu-id="9aff7-124">Hallatavaid tegevusi ei saa redigeerida algsest mallist väljaspool, välja arvatud selleks, et lisada õiguste, tähtaja või muu teave tegevuse parempoolses jaotises.</span><span class="sxs-lookup"><span data-stu-id="9aff7-124">You can't edit managed activities outside of the original template, except to add an assignee, due date, or other information in the right-hand section of the activity.</span></span>

<span data-ttu-id="9aff7-125">Kui soovite hallatavate tegevuste redigeerimist või kui te ei soovi, et see võtaks vastu värskendusi mallist, kust see pärineb, valige selle toimingu jaoks **Lukustamise** nupp.</span><span class="sxs-lookup"><span data-stu-id="9aff7-125">If you want to edit a managed activity, or if you don't want an activity to receive updates from the template it came from, select the **Lock** button for that activity.</span></span> <span data-ttu-id="9aff7-126">**Lukustuse** nupp kaob.</span><span class="sxs-lookup"><span data-stu-id="9aff7-126">The **Lock** button will disappear.</span></span> <span data-ttu-id="9aff7-127">Algne mall ei halda enam seda tööd ja see ei saa enam selle malli värskendusi.</span><span class="sxs-lookup"><span data-stu-id="9aff7-127">The activity will no longer be managed by the original template, and it will no longer receive updates from that template.</span></span> <span data-ttu-id="9aff7-128">Tegevused, mida teete, ei mõjuta algset malli.</span><span class="sxs-lookup"><span data-stu-id="9aff7-128">Updates you make to an activity do not affect the original template.</span></span>

<span data-ttu-id="9aff7-129">Kui kustutate tegevuse juhendist ja vajutate selle juhendi mallist muudatusi, jääb tegevus juhendist kustutatuks.</span><span class="sxs-lookup"><span data-stu-id="9aff7-129">If you delete an activity from a guide and push changes from that guide's template, the activity will remain deleted in the guide.</span></span>

> [!NOTE]
> <span data-ttu-id="9aff7-130">Mallid ei halda kontakte ja ressursse.</span><span class="sxs-lookup"><span data-stu-id="9aff7-130">Contacts and resources aren't managed by templates.</span></span> <span data-ttu-id="9aff7-131">Lisaks ei hallata sektsioone, nii et kui lisate või redigeerite malli jaotist, ei lükatata muudatusi selle malli kasutavatele juhenditele või mallidele.</span><span class="sxs-lookup"><span data-stu-id="9aff7-131">In addition, sections aren't managed, so if you add or edit a section in a template, the changes won't be pushed to any guides or templates that use that template.</span></span>
> 
> <span data-ttu-id="9aff7-132">Kui lisate mallile uusi tegevusi, lükatakse uued tegevused selle malli põhjal juhenditele ja mallidele ning uued tegevused kuvatakse ülaosas.</span><span class="sxs-lookup"><span data-stu-id="9aff7-132">If you add new activities to a template, the new activities are pushed to guides and templates based on that template, and the new activities display at the top.</span></span>

## <a name="import-activities-from-another-template"></a><span data-ttu-id="9aff7-133">Tegevuste importimine muust mallist</span><span class="sxs-lookup"><span data-stu-id="9aff7-133">Import activities from another template</span></span>

<span data-ttu-id="9aff7-134">Saate importida tegevusi ühest või mitmest mallist juhendisse või malli.</span><span class="sxs-lookup"><span data-stu-id="9aff7-134">You can import activities from one or more templates into a guide or template.</span></span>

1. <span data-ttu-id="9aff7-135">Valige juhend või mall, mida soovite redigeerida.</span><span class="sxs-lookup"><span data-stu-id="9aff7-135">Select the guide or template you want to edit.</span></span>

2. <span data-ttu-id="9aff7-136">Valige vahekaart **Toimingud**.</span><span class="sxs-lookup"><span data-stu-id="9aff7-136">Select the **Activities** tab.</span></span>

3. <span data-ttu-id="9aff7-137">Valige parempoolse jaotise vahekaart **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="9aff7-137">Select the **Import** tab in the section on the right.</span></span>

   <span data-ttu-id="9aff7-138">[![Impordi tegevused](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span><span class="sxs-lookup"><span data-stu-id="9aff7-138">[![Import activities](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span></span>

4. <span data-ttu-id="9aff7-139">Ülesannete eelvaate kuvamiseks brauseri uuel vahekaardil valige iga malli puhul nupp **Ava uuel vahekaardil.**</span><span class="sxs-lookup"><span data-stu-id="9aff7-139">To preview the tasks in a new tab in your browser, select the **Open in new tab** button on any template.</span></span>

   <span data-ttu-id="9aff7-140">[![Impordi tegevused](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span><span class="sxs-lookup"><span data-stu-id="9aff7-140">[![Import activities](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span></span>

5. <span data-ttu-id="9aff7-141">Lohistage ja kukutage soovitud mall juhendi mallil kohta, kus soovite tegevused kuvada.</span><span class="sxs-lookup"><span data-stu-id="9aff7-141">Drag and drop the desired template to the place in your guide template where you want the activities to appear.</span></span> <span data-ttu-id="9aff7-142">Jätkake juhendi või malli redigeerimist.</span><span class="sxs-lookup"><span data-stu-id="9aff7-142">Continue editing your guide or template.</span></span>

<span data-ttu-id="9aff7-143">Imporditud tegevused sisaldavad **Lukustamise** nuppu, mis näitab, et neid tegevusi haldab teie imporditud mall.</span><span class="sxs-lookup"><span data-stu-id="9aff7-143">The imported activities will contain a **Lock** button, which indicates those activities are managed by the template you imported from.</span></span> <span data-ttu-id="9aff7-144">Kui teete imporditud mallile muudatusi, värskendatakse need tegevused malli, kuhu te need impordite.</span><span class="sxs-lookup"><span data-stu-id="9aff7-144">When you make changes to the template you imported, those activities will update in the template you imported them to.</span></span> <span data-ttu-id="9aff7-145">Kuid muudatusi ei lükata automaatselt mis tahes juhenditele, mis on loodud teie poolt imporditava malli põhjal.</span><span class="sxs-lookup"><span data-stu-id="9aff7-145">However, the changes will not be pushed automatically to any guides created from the template you imported to.</span></span>

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a><span data-ttu-id="9aff7-146">Muude mallide või juhendite muutmine mallist</span><span class="sxs-lookup"><span data-stu-id="9aff7-146">Push changes from a template to other templates or guides</span></span>

<span data-ttu-id="9aff7-147">Kui redigeerite malli, mis sisaldab muudes mallides või juhendites kasutatavaid tegevusi, peate muudatustele vajutama, kui soovite, et need kuvataks muudes mallides või juhendites.</span><span class="sxs-lookup"><span data-stu-id="9aff7-147">If you edit a template that contains activities that are used in other templates or guides, you must push the changes if you want them to appear in the other templates or guides.</span></span>

<span data-ttu-id="9aff7-148">Kui te pole kindel, kas teie malli tegevusi kasutatakse muudes mallides või juhendites, valige vahekaardil **Kasutatav**, et vaadata, kus need tegevused ilmuvad.</span><span class="sxs-lookup"><span data-stu-id="9aff7-148">If you're not sure whether your template's activities are used in other templates or guides, select the **Used in** tab to view where those activities appear.</span></span>

   <span data-ttu-id="9aff7-149">[![Vaadake juhendeid ja mallide tegevusi rakenduses](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span><span class="sxs-lookup"><span data-stu-id="9aff7-149">[![View guides and templates activities are used in](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span></span>

<span data-ttu-id="9aff7-150">Muudatustele vajutamine:</span><span class="sxs-lookup"><span data-stu-id="9aff7-150">To push your changes:</span></span>

1. <span data-ttu-id="9aff7-151">Salvestage muudatused, klõpsates nuppu **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9aff7-151">Save your changes by selecting the **Save** button.</span></span> <span data-ttu-id="9aff7-152">Kui te seda ei tee, palutakse teil muudatused salvestada järgmises etapis.</span><span class="sxs-lookup"><span data-stu-id="9aff7-152">If you don't do this, you'll be prompted to save your changes in the next step.</span></span>

2. <span data-ttu-id="9aff7-153">Valige käsk **Lükake need muudatused sisse**.</span><span class="sxs-lookup"><span data-stu-id="9aff7-153">Select **Push these changes**.</span></span>

   
## <a name="add-or-edit-an-introduction"></a><span data-ttu-id="9aff7-154">Sissejuhatuse lisamine või muutmine</span><span class="sxs-lookup"><span data-stu-id="9aff7-154">Add or edit an introduction</span></span>

1. <span data-ttu-id="9aff7-155">Sisestage vahekaardil **Sissejuhatus** oma juhendi pealkiri ja avasõnum.</span><span class="sxs-lookup"><span data-stu-id="9aff7-155">On the **Introduction** tab, enter a title for your guide and an opening message.</span></span> <span data-ttu-id="9aff7-156">Näidisteksti kasutamiseks valige **Kasuta seda teadet.**</span><span class="sxs-lookup"><span data-stu-id="9aff7-156">To use the sample text, select **Use this message**.</span></span>

    <span data-ttu-id="9aff7-157">[![Sissejuhatuse vahekaart Onboardi mallis](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span><span class="sxs-lookup"><span data-stu-id="9aff7-157">[![Introduction tab in an Onboard template](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span></span>

2. <span data-ttu-id="9aff7-158">Kasutage vormingunuppe, et saata tekst välja nii, nagu vaja, või lisada pilte või linke.</span><span class="sxs-lookup"><span data-stu-id="9aff7-158">Use the formatting buttons to call out text as you require, or to add images or links.</span></span>
3. <span data-ttu-id="9aff7-159">Oma töö salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9aff7-159">Select **Save** to save your work.</span></span>

## <a name="add-or-edit-activities"></a><span data-ttu-id="9aff7-160">Tegevuste lisamine või redigeerimine</span><span class="sxs-lookup"><span data-stu-id="9aff7-160">Add or edit activities</span></span>

1. <span data-ttu-id="9aff7-161">Vahekaardil **Tegevused** lohistage üksused paremalt redigeerimise alale.</span><span class="sxs-lookup"><span data-stu-id="9aff7-161">On the **Activities** tab, drag items from the right to the editing area.</span></span>
2. <span data-ttu-id="9aff7-162">Juhendite sektsioonideks korraldamiseks lohistage üksus **Uus sektsioon** redigeerimise alale ja sisestage jaotise nimi ja valikuline kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="9aff7-162">To organize your guide into sections, drag the **New section** item to the editing area, and enter a name and an optional description for the section.</span></span>

    ![[Uue jaotise lisamine sisseelamisjuhendisse või -mallile] (./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. <span data-ttu-id="9aff7-164">Uue töötaja tegevuste lõpuleviimisel tegevuste lisamiseks lohistage üksus **Uus tegevus** redigeerimise alale ja sisestage tegevuse nimi ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="9aff7-164">To add activities for your new hire to complete, drag the **New activity** item to the editing area, and enter a name and description for the activity.</span></span>

    ![[<span data-ttu-id="9aff7-165">Uue tegevuse lisamine sisseelamisjuhendisse või -mallile</span><span class="sxs-lookup"><span data-stu-id="9aff7-165">Adding a new activity to an onboarding guide or template</span></span>](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. <span data-ttu-id="9aff7-166">Lisage sisseelamisjuhendisse rikkalik sisu:</span><span class="sxs-lookup"><span data-stu-id="9aff7-166">Add rich content to your onboarding guide:</span></span>

    - <span data-ttu-id="9aff7-167">YouTube'i video lisamiseks lohistage **YouTube**'i üksus redigeerimise alale, sisestage tegevuse nimi ja kirjeldus ning sisestage YouTube'i video URL.</span><span class="sxs-lookup"><span data-stu-id="9aff7-167">To add a YouTube video, drag the **YouTube** item to the editing area, enter a name and description for the activity, and enter the URL for the YouTube video.</span></span>
    - <span data-ttu-id="9aff7-168">Sway esitluse või infolehe lisamiseks lohistage **Sway** üksus redigeerimise alale, sisestage tegevuse nimi ja kirjeldus ning sisestage Sway esitluse või infolehe varjatud URL.</span><span class="sxs-lookup"><span data-stu-id="9aff7-168">To add a Sway presentation or newsletter, drag the **Sway** item to the editing area, enter a name and description for the activity, and enter the embedded URL for the Sway presentation or newsletter.</span></span>
    - <span data-ttu-id="9aff7-169">PowerApps rakenduse lisamiseks lohistage **PowerApps** üksus redigeerimise alale, sisestage tegevuse nimi ja kirjeldus ning valige kas PowerApps rakendus või sisestage PowerApps rakenduse ID.</span><span class="sxs-lookup"><span data-stu-id="9aff7-169">To add a PowerApps app, drag the **PowerApps** item to the editing area, enter a name and description for the activity, and either select the PowerApps app or enter the PowerApps app ID.</span></span>
    - <span data-ttu-id="9aff7-170">Microsoft Streami video lisamiseks lohistage **Microsoft Stream**i üksus redigeerimise alale, sisestage tegevuse nimi ja kirjeldus ning sisestage Microsoft Streami video URL.</span><span class="sxs-lookup"><span data-stu-id="9aff7-170">To add a Microsoft Stream video, drag the **Microsoft Stream** item to the editing area, enter a name and description for the activity, and enter the URL for the Microsoft Stream video.</span></span>
    - <span data-ttu-id="9aff7-171">Microsofti vormide vormi lisamiseks lohistage **Microsoft Forms** üksus redigeerimise alale, sisestage tegevuse nimi ja kirjeldus, sisestage vormi Microsoft Forms URL ja määrake ekraani ala suurus.</span><span class="sxs-lookup"><span data-stu-id="9aff7-171">To add a Microsoft Forms form, drag the **Microsoft Forms** item to the editing area, enter a name and description for the activity, enter the URL for the Microsoft Forms form, and specify the size of the screen area.</span></span>
    - <span data-ttu-id="9aff7-172">Veebisisu sisaldava iframe'i lisamiseks lohistage **Veebisisu (iframe)** üksus redigeerimise alale, sisestage tegevuse nimi ja kirjeldus, sisestage veebisisu URL ja määrake ekraani ala suurus.</span><span class="sxs-lookup"><span data-stu-id="9aff7-172">To add an iframe that contains web content, drag the **Web Content (iframe)** item to the editing area, enter a name and description for the activity, enter the URL for the web content, and specify the size of the screen area.</span></span>

    ![[<span data-ttu-id="9aff7-173">Rikkaliku sisu lisamine sisseelamisjuhendile või -mallile</span><span class="sxs-lookup"><span data-stu-id="9aff7-173">Adding rich content to an onboarding guide or template</span></span>](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. <span data-ttu-id="9aff7-174">Valikuline: määrake iga tegevuse paremal alal tegevus kindlale isikule või rollile, lisage tähtaeg ja kontaktisik ning määrake kategooria värv.</span><span class="sxs-lookup"><span data-stu-id="9aff7-174">Optional: In the area on the right of each activity, assign the activity to a specific person or role, add a due date and contact person, and assign a category color.</span></span> <span data-ttu-id="9aff7-175">Kui määrate tegevuse isikule või rollile, luuakse ülesanne igale üksikisikule.</span><span class="sxs-lookup"><span data-stu-id="9aff7-175">When you assign an activity to a person or role, a task is created for each individual.</span></span> <span data-ttu-id="9aff7-176">See ülesanne kuvatakse Onboardi menüüs **Ülesanded**.</span><span class="sxs-lookup"><span data-stu-id="9aff7-176">This task appears on the **Tasks** menu in Onboard.</span></span>

    <span data-ttu-id="9aff7-177">[![Tegevuse määramine sisseelamisjuhendis või -mallis](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span><span class="sxs-lookup"><span data-stu-id="9aff7-177">[![Assigning an activity in an onboarding guide or template](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span></span>

3. <span data-ttu-id="9aff7-178">Oma töö salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9aff7-178">Select **Save** to save your work.</span></span>

<span data-ttu-id="9aff7-179">Tegevuse või sektsiooni kustutamiseks valige tegevuse või sektsiooni ülemises parempoolses nurgas nupp **Kustuta** (prügikasti sümbol).</span><span class="sxs-lookup"><span data-stu-id="9aff7-179">To delete an activity or section, select the **Delete** button (the trash can symbol) in the upper-right corner of the activity or section.</span></span>

<span data-ttu-id="9aff7-180">Tegevuste ja sektsioonide ümberkorraldamiseks lohistage need uude asukohta.</span><span class="sxs-lookup"><span data-stu-id="9aff7-180">To rearrange activities and sections, drag them to a new location.</span></span>

## <a name="add-or-edit-contacts"></a><span data-ttu-id="9aff7-181">Kontaktide lisamine või redigeerimine</span><span class="sxs-lookup"><span data-stu-id="9aff7-181">Add or edit contacts</span></span>

<span data-ttu-id="9aff7-182">Saate lisada kontaktisikuid, kes saavad aidata teie uuel töötajal algusest peale edu saavutada.</span><span class="sxs-lookup"><span data-stu-id="9aff7-182">You can add contact people who can help your new hire succeed from day one.</span></span> <span data-ttu-id="9aff7-183">Need kontaktid võivad olla värbajad, meeskonnakaaslased, sisseelamissõbrad, mentorid, administraatorid ja IT-toe töötajad.</span><span class="sxs-lookup"><span data-stu-id="9aff7-183">These contacts can be recruiters, teammates, onboarding buddies, mentors, admins, and IT support staff.</span></span>

1. <span data-ttu-id="9aff7-184">Vahekaardil **Kontaktid** valige **Uus kontakt**.</span><span class="sxs-lookup"><span data-stu-id="9aff7-184">On the **Contacts** tab, select **New contact**.</span></span>
2. <span data-ttu-id="9aff7-185">Sisestage dialoogiboksi **Lisa meeskonnaliige** kontaktisiku nimi või meiliaadress, sisestage lühikirjeldus, mis selgitab, kuidas kontaktisik saab uut töötajat aidata ja seejärel valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="9aff7-185">In the **Add team member** dialog box, enter the contact person's name or email address, enter a short description that explains how the contact person can help the new hire, and then select **Add**.</span></span> 

    ![[<span data-ttu-id="9aff7-186">Kontaktide lisamine sisseelamisjuhendile või -mallile</span><span class="sxs-lookup"><span data-stu-id="9aff7-186">Adding contacts to an onboarding guide or template</span></span>](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    <span data-ttu-id="9aff7-187">Teise võimalusena saate valida ühe või mitu kontakti jaotises **Soovitused**.</span><span class="sxs-lookup"><span data-stu-id="9aff7-187">Alternately, you can select one or more contacts under **Suggestions**.</span></span>

3. <span data-ttu-id="9aff7-188">Oma töö salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9aff7-188">Select **Save** to save your work.</span></span>

<span data-ttu-id="9aff7-189">Kontaktkirje kustutamiseks valige nupp **Kustuta** (prügikasti sümbol), mis on kontaktkirjest paremal.</span><span class="sxs-lookup"><span data-stu-id="9aff7-189">To delete a contact, select the **Delete** button (the trash can symbol) to the right of the contact.</span></span>

<span data-ttu-id="9aff7-190">Kontaktkirje redigeerimiseks valige nupp **Redigeeri** (pliiatsi sümbol), mis on kontaktkirjest paremal.</span><span class="sxs-lookup"><span data-stu-id="9aff7-190">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the contact.</span></span>

## <a name="add-or-edit-resources"></a><span data-ttu-id="9aff7-191">Ressursside lisamine või redigeerimine</span><span class="sxs-lookup"><span data-stu-id="9aff7-191">Add or edit resources</span></span>

<span data-ttu-id="9aff7-192">Saate lisada kasulikke faile, kaarte ja linke sisseelamisjuhendis olevasse jaotisse **Ressursid**.</span><span class="sxs-lookup"><span data-stu-id="9aff7-192">You can add useful files, maps, and links to the **Resources** section of your onboarding guide.</span></span>

1. <span data-ttu-id="9aff7-193">Vahekaardil **Ressursid** valige **Uus ressurss**.</span><span class="sxs-lookup"><span data-stu-id="9aff7-193">On the **Resources** tab, select **New resource**.</span></span>
2. <span data-ttu-id="9aff7-194">Järgige üht neist sammudest.</span><span class="sxs-lookup"><span data-stu-id="9aff7-194">Follow one of these steps:</span></span>

    - <span data-ttu-id="9aff7-195">Faili lisamiseks valige vahekaart **Fail** ja lohistage fail määratud alale.</span><span class="sxs-lookup"><span data-stu-id="9aff7-195">To add a file, select the **File** tab, and drag the file into the designated area.</span></span> <span data-ttu-id="9aff7-196">(Teise võimalusena klõpsake sellel alal suvalist kohta, et sirvida faili arvutis või valige **Sirvi OneDrive**.) Sisestage faili nimi ja seejärel valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="9aff7-196">(Alternatively, click anywhere in that area to browse for the file on your computer, or select **Browse OneDrive**.) Enter a name for the file, and then select **Add**.</span></span>
    - <span data-ttu-id="9aff7-197">Lingi lisamiseks valige vahekaart **Link**, sisestage lingile nimi ja aadress ning seejärel valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="9aff7-197">To add a link, select the **Link** tab, enter a name and address for the link, and then select **Add**.</span></span>
    - <span data-ttu-id="9aff7-198">Kaardi lisamiseks valige vahekaart **Kaart**, sisestage kaardile nimi ja aadress ning seejärel valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="9aff7-198">To add a map, select the **Map** tab, enter a name and address for the map, and then select **Add**.</span></span> <span data-ttu-id="9aff7-199">Onboard sisaldab teie määratud aadressi kaarti.</span><span class="sxs-lookup"><span data-stu-id="9aff7-199">Onboard will include a map of the address that you specify.</span></span>

    ![[<span data-ttu-id="9aff7-200">Ressursi lisamine sisseelamisjuhendisse või -mallile</span><span class="sxs-lookup"><span data-stu-id="9aff7-200">Adding a resource to an onboarding guide or template</span></span>](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. <span data-ttu-id="9aff7-201">Oma töö salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9aff7-201">Select **Save** to save your work.</span></span>

<span data-ttu-id="9aff7-202">Ressursi kustutamiseks valige nupp **Kustuta** (prügikasti sümbol), mis on ressursikirjest paremal.</span><span class="sxs-lookup"><span data-stu-id="9aff7-202">To delete a resource, select the **Delete** button (the trash can symbol) to the right of the resource.</span></span>

<span data-ttu-id="9aff7-203">Ressursikirje redigeerimiseks valige nupp **Redigeeri** (pliiatsi sümbol), mis on ressursikirjest paremal.</span><span class="sxs-lookup"><span data-stu-id="9aff7-203">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the resource.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9aff7-204">Järgmised etapid</span><span class="sxs-lookup"><span data-stu-id="9aff7-204">Next steps</span></span>

- [<span data-ttu-id="9aff7-205">Sisu jagamine teiste kaasautoritega</span><span class="sxs-lookup"><span data-stu-id="9aff7-205">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="9aff7-206">Vaadake tööülesannete ja töötajate töölevõtmise olekut</span><span class="sxs-lookup"><span data-stu-id="9aff7-206">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="9aff7-207">Looge Onboardis värbamismeeskonnad</span><span class="sxs-lookup"><span data-stu-id="9aff7-207">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="9aff7-208">Vt ka</span><span class="sxs-lookup"><span data-stu-id="9aff7-208">See also</span></span>

- [<span data-ttu-id="9aff7-209">Proovige või ostke Onboardi rakendus</span><span class="sxs-lookup"><span data-stu-id="9aff7-209">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="9aff7-210">Mis on uut?</span><span class="sxs-lookup"><span data-stu-id="9aff7-210">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="9aff7-211">Väljalaskemärkmed</span><span class="sxs-lookup"><span data-stu-id="9aff7-211">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="9aff7-212">Toe hankimine</span><span class="sxs-lookup"><span data-stu-id="9aff7-212">Get support</span></span>](./talent-support.md)
