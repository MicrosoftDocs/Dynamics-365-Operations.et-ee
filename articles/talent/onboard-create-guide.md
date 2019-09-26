---
title: Sisseelamisjuhendi loomine ja saatmine, kasutades Dynamics 365 for Talent - Onboard
description: Selles teemas selgitatakse, kuidas kasutada Microsoft Dynamics 365 for Talent - Onboard rakendust, et luua uutele töötajatele sisseelamisjuhend. See ülesanne on oluline esimene samm personalijuhtimise personalistrateegias.
author: andreabichsel
manager: ''
ms.date: 05/02/2019
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
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: de5d584e3b7edba2751aa0c83b0465df2c3e4f7d
ms.sourcegitcommit: 9f762fa89c5b432667aa156c22d679a7f601952d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/08/2019
ms.locfileid: "1731442"
---
# <a name="create-and-send-an-onboarding-guide-by-using-dynamics-365-for-talent-onboard"></a><span data-ttu-id="2bdf7-104">Sisseelamisjuhendi loomine ja saatmine, kasutades Dynamics 365 for Talent: Onboard</span><span class="sxs-lookup"><span data-stu-id="2bdf7-104">Create and send an onboarding guide by using Dynamics 365 for Talent: Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2bdf7-105">Microsoft Dynamics 365 for Talent: Onboardis saate luua enda loodud mallidest sisseelamisjuhedeid, mis on saadaval galeriis või nullist.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-105">Microsoft Dynamics 365 for Talent: Onboard lets you create onboarding guides from templates that you created yourself, from templates that are available in a gallery, or from scratch.</span></span>

<span data-ttu-id="2bdf7-106">Kui olete loonud sisseelamisjuhendi, saate selle saata uuele töötajale.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-106">After you've created an onboarding guide, you can send it to a new hire.</span></span> <span data-ttu-id="2bdf7-107">Teise võimalusena saate saata selle mitmele uuele töötajale, mille määrate Microsoft Excel failis, mille saab alla laadida Onboardi rakendusest.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-107">Alternatively, you can send it to multiple new hires that you specify in a Microsoft Excel file that you download from the Onboard app.</span></span>

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-a-single-new-hire"></a><span data-ttu-id="2bdf7-108">Looge sisseelamisjuhend mallist ja saatke see ühele uuele töötajale</span><span class="sxs-lookup"><span data-stu-id="2bdf7-108">Create an onboarding guide from a template and send it to a single new hire</span></span>

1. <span data-ttu-id="2bdf7-109">Valige vasakpoolses menüüs **Mallid**.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-109">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="2bdf7-110">Valige jaotises **Minu mallid** mall, mida soovite seadistada uue töötaja sisseelamisjuhendi jaoks.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-110">Under **My templates**, select the template that you want to set up as an onboarding guide for the new hire.</span></span>
3. <span data-ttu-id="2bdf7-111">Redigeerige malli, kui soovite.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-111">Edit the template as you desire.</span></span> <span data-ttu-id="2bdf7-112">Ärge unustage oma tööd regulaarselt salvestada.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-112">Be sure to save your work as you go.</span></span>
4. <span data-ttu-id="2bdf7-113">Kui olete malli redigeerimise lõpetanud, valige käsk **Loo juhend.**</span><span class="sxs-lookup"><span data-stu-id="2bdf7-113">When you've finished editing the template, select **Create guide**.</span></span>

    <span data-ttu-id="2bdf7-114">[![Sisseelamisjuhendi loomine malli põhjal](./media/onboard-create-guide.png)](./media/onboard-create-guide.png)</span><span class="sxs-lookup"><span data-stu-id="2bdf7-114">[![Creating an onboarding guide from a template](./media/onboard-create-guide.png)](./media/onboard-create-guide.png)</span></span>

5. <span data-ttu-id="2bdf7-115">Sisestage akna **Loo juhend** jaotisesesse **Kes on sisse elamas** uue töötaja nimi või meiliaadress.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-115">In the **Create a guide** window, under **Who are you onboarding**, enter the new hire's name or email address.</span></span> <span data-ttu-id="2bdf7-116">Kui uus töötaja pole veel süsteemis olemas, valige käsk **Lisa kohe** ja sisestage töötaja teave.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-116">If the new hire isn't in the system yet, select **Add now**, and enter the employee's information.</span></span>

    ![[<span data-ttu-id="2bdf7-117">Sisseelamisjuhendisse teabe sisestamine</span><span class="sxs-lookup"><span data-stu-id="2bdf7-117">Entering information for the onboarding guide</span></span>](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

6. <span data-ttu-id="2bdf7-118">Valige jaotises **Millal nad alustavad** alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-118">Under **When do they start**, select a start date.</span></span>
7. <span data-ttu-id="2bdf7-119">Kui juhend tuleks saata automaatselt uuele tööle kindlal kuupäeval, veenduge, et **Automaatse saatmiskuupäeva ajastamine** on sisse lülitatud ja seejärel valige automaatne saatmiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-119">If the onboarding guide should be sent automatically to the new hire on a specific date, make sure that the **Schedule an automatic send date** option is turned on, and then select the automatic send date.</span></span> <span data-ttu-id="2bdf7-120">Juhendi koheseks saatmiseks lülitage välja valik **Automaatse saatmiskuupäeva ajastamine**.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-120">To send the guide immediately, turn off the **Schedule an automatic send date** option.</span></span>
8. <span data-ttu-id="2bdf7-121">Valige suvand **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-121">Select **Done**.</span></span>
9. <span data-ttu-id="2bdf7-122">Kui olete sisseelamisjuhendi redigeerimise lõpetanud, valige ülemises parempoolses nurgas käsk **Saada**.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-122">When you've finished editing the onboarding guide, select **Send** in the upper-right corner.</span></span> <span data-ttu-id="2bdf7-123">Seejärel järgige üht neist sammudest.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-123">Then follow one of these steps:</span></span>

    - <span data-ttu-id="2bdf7-124">Uuele töötajale lingi saatmiseks valige **Kopeeri link** ja seejärel valige **Kopeeri**.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-124">To send the new hire a link to the onboarding guide, select **copy a link**, and then select **Copy**.</span></span>
    - <span data-ttu-id="2bdf7-125">Sisseelamisjuhendi meili kohandamiseks enne selle saatmist valige **Meili kohandamine enne saatmist**, valige **Edasi**, kohandage meili nii, nagu soovite ja seejärel valige **Saada**.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-125">To customize the email for the onboarding guide before you send it, select **Customize the email before sending**, select **Next**, customize the email as you desire, and then select **Send**.</span></span>
    - <span data-ttu-id="2bdf7-126">Meili saatmiseks seda kohandamata valige **Edasi** ja seejärel valige **Saada**.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-126">To send the email without customizing it, select **Next**, and then select **Send**.</span></span>

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-multiple-new-hires"></a><span data-ttu-id="2bdf7-127">Looge sisseelamisjuhend mallist ja saatke see mitmele uuele töötajale</span><span class="sxs-lookup"><span data-stu-id="2bdf7-127">Create an onboarding guide from a template and send it to multiple new hires</span></span>

<span data-ttu-id="2bdf7-128">Onboardis saate saata sisseelamisjuhendi mitmele uuele töötajale samal ajal.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-128">Onboard lets you send an onboarding guide to multiple new hires at the same time.</span></span>

1. <span data-ttu-id="2bdf7-129">Valige vasakpoolses menüüs **Mallid**.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-129">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="2bdf7-130">Valige jaotises **Minu mallid** mall, mida soovite seadistada uute töötajate sisseelamisjuhendi jaoks.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-130">Under **My templates**, select the template that you want to set up as an onboarding guide for the new hires.</span></span>
3. <span data-ttu-id="2bdf7-131">Redigeerige malli, kui soovite.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-131">Edit the template as you desire.</span></span> <span data-ttu-id="2bdf7-132">Ärge unustage oma tööd regulaarselt salvestada.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-132">Be sure to save your work as you go.</span></span>
4. <span data-ttu-id="2bdf7-133">Kui olete malli redigeerimise lõpetanud, valige käsk **Loo juhend.**</span><span class="sxs-lookup"><span data-stu-id="2bdf7-133">When you've finished editing the template, select **Create guide**.</span></span>
5. <span data-ttu-id="2bdf7-134">Aknas **Loo juhend** valige **Sisseelamist vajab mitu inimest korraga**.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-134">In the **Create a guide** window, select **Need to onboard multiple people at once**.</span></span>

    <span data-ttu-id="2bdf7-135">[![Mitmele uuele töötajale sisseelamisjuhendi loomine](./media/onboard-send-guide-multiple-people.png)](./media/onboard-send-guide-multiple-people.png)</span><span class="sxs-lookup"><span data-stu-id="2bdf7-135">[![Creating an onboarding guide for multiple new hires](./media/onboard-send-guide-multiple-people.png)](./media/onboard-send-guide-multiple-people.png)</span></span>

6. <span data-ttu-id="2bdf7-136">Valige **Uue töötaja mall**.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-136">Select **new hire template**.</span></span>
7. <span data-ttu-id="2bdf7-137">Pärast xlsx-faili allalaadimist valige **Ava**, sisestage töötajate teave Exceli töövihikusse ja salvestage töövihik.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-137">After the .xlsx file is downloaded, select **Open**, enter the employees' information in the Excel workbook, and save the workbook.</span></span>

    <span data-ttu-id="2bdf7-138">[![Exceli malli allalaadimine, et saata sisseelamisjuhend mitmele uuele töötajale](./media/onboard-send-guide-download-spreadsheet.png)](./media/onboard-send-guide-download-spreadsheet.png)</span><span class="sxs-lookup"><span data-stu-id="2bdf7-138">[![Downloading the Excel template for sending the onboarding guide to multiple new hires](./media/onboard-send-guide-download-spreadsheet.png)](./media/onboard-send-guide-download-spreadsheet.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="2bdf7-139">Enne kui saate töövihikut redigeerida, peate valima suvandi **Luba redigeerimine** Excelis.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-139">Before you can edit the workbook, you must select **Enable editing** in Excel.</span></span>
    > 
    > <span data-ttu-id="2bdf7-140">[![Redigeerimise lubamine](./media/onboard-send-guide-enable-editing.png)](./media/onboard-send-guide-enable-editing.png)</span><span class="sxs-lookup"><span data-stu-id="2bdf7-140">[![Enabling editing](./media/onboard-send-guide-enable-editing.png)](./media/onboard-send-guide-enable-editing.png)</span></span>

8. <span data-ttu-id="2bdf7-141">Lohistage Exceli töövihik määratud alale aknas **Mitme juhendi loomine** või klõpsake sellel alal suvalist kohta, et sirvida faili oma arvutis.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-141">Drag the Excel workbook to the designated area in the **Create multiple guides** window, or click anywhere in that area to browse for the file on your computer.</span></span>

    <span data-ttu-id="2bdf7-142">[![Redigeeritud töövihiku lohistamine](./media/onboard-send-guide-drag-spreadsheet.png)](./media/onboard-send-guide-drag-spreadsheet.png)</span><span class="sxs-lookup"><span data-stu-id="2bdf7-142">[![Dragging the edited workbook](./media/onboard-send-guide-drag-spreadsheet.png)](./media/onboard-send-guide-drag-spreadsheet.png)</span></span>

9. <span data-ttu-id="2bdf7-143">Kui olete sisseelamisjuhendi redigeerimise lõpetanud, valige ülemises parempoolses nurgas käsk **Saada**.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-143">When you've finished editing the onboarding guide, select **Send** in the upper-right corner.</span></span> <span data-ttu-id="2bdf7-144">Seejärel järgige üht neist sammudest.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-144">Then follow one of these steps:</span></span>

    - <span data-ttu-id="2bdf7-145">Uutele töötajatele lingi saatmiseks valige **Kopeeri link** ja seejärel valige **Kopeeri**.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-145">To send the new hires a link to the onboarding guide, select **copy a link**, and then select **Copy**.</span></span>
    - <span data-ttu-id="2bdf7-146">Sisseelamisjuhendi meili kohandamiseks enne selle saatmist valige **Meili kohandamine enne saatmist**, valige **Edasi**, kohandage meili nii, nagu soovite ja seejärel valige **Saada**.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-146">To customize the email for the onboarding guide before you send it, select **Customize the email before sending**, select **Next**, customize the email as you desire, and then select **Send**.</span></span>
    - <span data-ttu-id="2bdf7-147">Meili saatmiseks seda kohandamata valige **Edasi** ja seejärel valige **Saada**.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-147">To send the email without customizing it, select **Next**, and then select **Send**.</span></span>

## <a name="create-a-guide-without-using-a-template"></a><span data-ttu-id="2bdf7-148">Looge juhend malli kasutamata</span><span class="sxs-lookup"><span data-stu-id="2bdf7-148">Create a guide without using a template</span></span>

<span data-ttu-id="2bdf7-149">Te ei pea alati mallist juhendit looma.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-149">You don't always have to create a guide from a template.</span></span> <span data-ttu-id="2bdf7-150">Soovi korral saate selle asemel luua juhise nullist.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-150">If you prefer, you can create a guide from scratch instead.</span></span>

1. <span data-ttu-id="2bdf7-151">Vasakul menüüs valige **Juhendid** ja seejärel valige nupp **Lisa** (plussmärk \[**+**\]).</span><span class="sxs-lookup"><span data-stu-id="2bdf7-151">On the left menu, select **Guides**, and then select the **Add** button (the plus sign \[**+**\]).</span></span>
2. <span data-ttu-id="2bdf7-152">Sisestage akna **Loo juhend** jaotisesesse **Kes on sisse elamas** uue töötaja nimi või meiliaadress.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-152">In the **Create a guide** window, under **Who are you onboarding**, enter the new hire's name or email address.</span></span> <span data-ttu-id="2bdf7-153">Kui uus töötaja pole veel süsteemis olemas, valige käsk **Lisa kohe** ja sisestage töötaja teave.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-153">If the new hire isn't in the system yet, select **Add now**, and enter the employee's information.</span></span>

    ![[<span data-ttu-id="2bdf7-154">Sisseelamisjuhendisse teabe sisestamine</span><span class="sxs-lookup"><span data-stu-id="2bdf7-154">Entering information for the onboarding guide</span></span>](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

3. <span data-ttu-id="2bdf7-155">Valige jaotises **Millal nad alustavad** alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-155">Under **When do they start**, select a start date.</span></span>
4. <span data-ttu-id="2bdf7-156">Kui juhend tuleks saata automaatselt uuele tööle kindlal kuupäeval, veenduge, et **Automaatse saatmiskuupäeva ajastamine** on sisse lülitatud ja seejärel valige automaatne saatmiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-156">If the onboarding guide should be sent automatically to the new hire on a specific date, make sure that the **Schedule an automatic send date** option is turned on, and then select the automatic send date.</span></span> <span data-ttu-id="2bdf7-157">Juhendi koheseks saatmiseks lülitage välja valik **Automaatse saatmiskuupäeva ajastamine**.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-157">To send the guide immediately, turn off the **Schedule an automatic send date** option.</span></span>
5. <span data-ttu-id="2bdf7-158">Valige suvand **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-158">Select **Done**.</span></span>

## <a name="save-a-guide-as-a-template"></a><span data-ttu-id="2bdf7-159">Saate salvestada juhendi mallina</span><span class="sxs-lookup"><span data-stu-id="2bdf7-159">Save a guide as a template</span></span>

<span data-ttu-id="2bdf7-160">Saate salvestada sisseeleamisjuhendi mallina.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-160">You can save an onboarding guide as a template.</span></span> <span data-ttu-id="2bdf7-161">Sel viisil saate säästa aega, kui peate hiljem rohkem juhendeid looma.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-161">In this way, you can save time when you must create more onboarding guides later.</span></span>

1. <span data-ttu-id="2bdf7-162">Valige vasakpoolses menüüs **Juhendid**.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-162">On the left menu, select **Guides**.</span></span>
2. <span data-ttu-id="2bdf7-163">Valige nupp **Veel** (kolmikpunkt \[**...**\]) juhendile, millest soovite malli luua, ja seejärel valige **Salvesta mallina**.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-163">Select the **More** button (the ellipsis \[**...**\]) for the guide that you want to create a template from, and then select **Save as template**.</span></span>

    ![[<span data-ttu-id="2bdf7-164">Sisseelamisjuhendi salvestamine mallina</span><span class="sxs-lookup"><span data-stu-id="2bdf7-164">Saving an onboarding guide as a template</span></span>](./media/onboard-save-guide-as-template.png)](./media/onboard-save-guide-as-template.png)

3. <span data-ttu-id="2bdf7-165">Sisestage aknas **Salvesta uue mallina** uue malli nimi ja seejärel valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-165">In the **Save as a new template** window, enter a name for your new template, and then select **Save**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="2bdf7-166">Järgmised etapid</span><span class="sxs-lookup"><span data-stu-id="2bdf7-166">Next steps</span></span>

- [<span data-ttu-id="2bdf7-167">Sisseelamisjuhendite ja mallide redigeerimine</span><span class="sxs-lookup"><span data-stu-id="2bdf7-167">Edit onboarding guides and templates</span></span>](./onboard-edit-guides-templates.md)
- [<span data-ttu-id="2bdf7-168">Sisu jagamine teiste kaasautoritega</span><span class="sxs-lookup"><span data-stu-id="2bdf7-168">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="2bdf7-169">Vaadake tööülesannete ja töötajate töölevõtmise olekut</span><span class="sxs-lookup"><span data-stu-id="2bdf7-169">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="2bdf7-170">Looge Onboardis värbamismeeskonnad</span><span class="sxs-lookup"><span data-stu-id="2bdf7-170">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="2bdf7-171">Vt ka</span><span class="sxs-lookup"><span data-stu-id="2bdf7-171">See also</span></span>

- [<span data-ttu-id="2bdf7-172">Proovige või ostke Onboardi rakendus</span><span class="sxs-lookup"><span data-stu-id="2bdf7-172">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="2bdf7-173">Mis on uut?</span><span class="sxs-lookup"><span data-stu-id="2bdf7-173">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="2bdf7-174">Väljalaskemärkmed</span><span class="sxs-lookup"><span data-stu-id="2bdf7-174">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="2bdf7-175">Toe hankimine</span><span class="sxs-lookup"><span data-stu-id="2bdf7-175">Get support</span></span>](./talent-support.md)