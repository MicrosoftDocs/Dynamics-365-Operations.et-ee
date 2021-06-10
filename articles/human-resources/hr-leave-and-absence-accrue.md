---
title: Puhkuse ja puudumise plaanide juurdekasv
description: Rakenduses Dynamics 365 Human Resources saate koondada puhkuseid ja puudumisi mitme töövõtja või ühe jaoks.
author: andreabichsel
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 86ca63b1703faa6f57ed2e5591c89a5e84363481
ms.sourcegitcommit: 318e406b84d43381d450272eb83c5eea9c5cf1c0
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059469"
---
# <a name="accrue-leave-and-absence-plans"></a><span data-ttu-id="772d4-103">Puhkuse ja puudumise plaanide juurdekasv</span><span class="sxs-lookup"><span data-stu-id="772d4-103">Accrue leave and absence plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="772d4-104">Rakenduses Dynamics 365 Human Resources saate koondada puhkuseid ja puudumisi mitme töövõtja või ühe jaoks.</span><span class="sxs-lookup"><span data-stu-id="772d4-104">You can accrue leave and absence in Dynamics 365 Human Resources for multiple employees or for an individual.</span></span>

## <a name="accrue-leave-and-absence-for-multiple-employees"></a><span data-ttu-id="772d4-105">Mitme töötaja puhkuste ja puudumiste koondamine</span><span class="sxs-lookup"><span data-stu-id="772d4-105">Accrue leave and absence for multiple employees</span></span>

1. <span data-ttu-id="772d4-106">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="772d4-106">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="772d4-107">Jaotises **Puhkuse haldamine** valige suvand **Puhkuse ja puudumise plaanide koondamine**.</span><span class="sxs-lookup"><span data-stu-id="772d4-107">Under **Manage leave**, select **Accrue leave and absence plans**.</span></span>

3. <span data-ttu-id="772d4-108">Kuvatakse dialoogiboks **Puhkuse ja puudumise plaanide juurdekasv**.</span><span class="sxs-lookup"><span data-stu-id="772d4-108">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="772d4-109">Jaotises **Koonda seisuga** valige kas **Tänane kuupäev** või **Kohandatud kuupäev** ja sisestage kohandatud kuupäev.</span><span class="sxs-lookup"><span data-stu-id="772d4-109">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="772d4-110">Kui soovite käitada viitvõlad kõigi ettevõtete jaoks, valige **Kõik ettevõtted**.</span><span class="sxs-lookup"><span data-stu-id="772d4-110">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="772d4-111">Kui soovite töödelda ühe puhkuseplaani viitvõlgu, valige suvandi **Kõigi plaanid** jaoks **Ei** ja seejärel valige **Puhkuseplaan**.</span><span class="sxs-lookup"><span data-stu-id="772d4-111">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="772d4-112">Kui valite kõik ettevõtted, siis ei saa te valida üksikuid puhkuseplaane.</span><span class="sxs-lookup"><span data-stu-id="772d4-112">If you select all companies, you can't select an individual leave plan.</span></span>

5. <span data-ttu-id="772d4-113">Kui soovite lisandumisprotsessi käitada taustal, valige suvand **Käivita taustal** ja tehke järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="772d4-113">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

    1. <span data-ttu-id="772d4-114">Sisestage teave lisandumisprotsessi kohta.</span><span class="sxs-lookup"><span data-stu-id="772d4-114">Enter information for the accrual process.</span></span>
    2. <span data-ttu-id="772d4-115">Korduva töö seadistamiseks valige suvand **Kordumine**, sisestage kordumise teave ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="772d4-115">To set up a recurring job, select **Recurrence**, enter the recurrence information, and then select **OK**.</span></span>
    3. <span data-ttu-id="772d4-116">Töö teatise seadistamiseks valige suvand **teatised**, valige milliseid teatisi saada ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="772d4-116">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>
    4. <span data-ttu-id="772d4-117">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="772d4-117">Select **OK**.</span></span> <span data-ttu-id="772d4-118">Lisandumisprotsess töötab teie määratud parameetritega.</span><span class="sxs-lookup"><span data-stu-id="772d4-118">The accrual process will run with the parameters you set.</span></span> 

## <a name="accrue-leave-and-absence-for-an-employee"></a><span data-ttu-id="772d4-119">Ühe töötaja puhkuste ja puudumiste lisamine</span><span class="sxs-lookup"><span data-stu-id="772d4-119">Accrue leave and absence for an employee</span></span>

1. <span data-ttu-id="772d4-120">Töövõtja kirjes valige suvand **Puhkus**.</span><span class="sxs-lookup"><span data-stu-id="772d4-120">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="772d4-121">Valige suvand **Puhkuste ja puudumiste koondamine**.</span><span class="sxs-lookup"><span data-stu-id="772d4-121">Select **Accrue leave and absence**.</span></span>

3. <span data-ttu-id="772d4-122">Kuvatakse dialoogiboks **Puhkuse ja puudumise plaanide juurdekasv**.</span><span class="sxs-lookup"><span data-stu-id="772d4-122">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="772d4-123">Jaotises **Koonda seisuga** valige kas **Tänane kuupäev** või **Kohandatud kuupäev** ja sisestage kohandatud kuupäev.</span><span class="sxs-lookup"><span data-stu-id="772d4-123">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="772d4-124">Kui soovite käitada viitvõlad kõigi ettevõtete jaoks, valige **Kõik ettevõtted**.</span><span class="sxs-lookup"><span data-stu-id="772d4-124">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="772d4-125">Kui soovite töödelda ühe puhkuseplaani viitvõlgu, valige suvandi **Kõigi plaanid** jaoks **Ei** ja seejärel valige **Puhkuseplaan**.</span><span class="sxs-lookup"><span data-stu-id="772d4-125">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="772d4-126">Kui valite kõik ettevõtted, siis ei saa te valida üksikuid puhkuseplaane.</span><span class="sxs-lookup"><span data-stu-id="772d4-126">If you select all companies, you can't select an individual leave plan.</span></span>

5. <span data-ttu-id="772d4-127">Kui soovite lisandumisprotsessi käitada taustal, valige suvand **Käivita taustal** ja tehke järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="772d4-127">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="772d4-128">Sisestage teave lisandumisprotsessi kohta.</span><span class="sxs-lookup"><span data-stu-id="772d4-128">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="772d4-129">Korduva töö seadistamiseks valige suvand **Kordumine**, sisestage kordumise teave ja valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="772d4-129">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="772d4-130">Töö teatise seadistamiseks valige suvand **teatised**, valige milliseid teatisi saada ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="772d4-130">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="772d4-131">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="772d4-131">Select **OK**.</span></span> <span data-ttu-id="772d4-132">Lisandumisprotsess töötab teie määratud parameetritega.</span><span class="sxs-lookup"><span data-stu-id="772d4-132">The accrual process will run with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a><span data-ttu-id="772d4-133">Mitme töövõtja puhkuste ja puudumiste lisamiste kustutamine</span><span class="sxs-lookup"><span data-stu-id="772d4-133">Delete leave and absence accruals for multiple employees</span></span>

<span data-ttu-id="772d4-134">Kustutage kindla plaani ja kuupäevavahemiku lisandumise kirjed.</span><span class="sxs-lookup"><span data-stu-id="772d4-134">Delete accrual records for a specific plan and date range.</span></span> <span data-ttu-id="772d4-135">Lisandumise kuupäevad peavad olema tänase või tulevikus oleva kuupäevaga.</span><span class="sxs-lookup"><span data-stu-id="772d4-135">Accrual dates must be dated today or in the future.</span></span>

1. <span data-ttu-id="772d4-136">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="772d4-136">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="772d4-137">Jaotises **Puhkuse haldamine** valige suvand **Puhkuse- ja puudumise plaani viitvõlgade kustutamine**.</span><span class="sxs-lookup"><span data-stu-id="772d4-137">Under **Manage leave**, select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="772d4-138">Dialoogiboksis **Puhkuse- ja puudumise plaani viitvõlgade kustutamine** valige **Puhkuse plaan**.</span><span class="sxs-lookup"><span data-stu-id="772d4-138">In the **Delete leave and absence plan accruals** dialog box, select the **Leave plan**.</span></span>

4. <span data-ttu-id="772d4-139">Vajadusel valige **Kustuta saldo korrigeerimised**.</span><span class="sxs-lookup"><span data-stu-id="772d4-139">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="772d4-140">Sisestage või valige **Puhkuse viitvõla kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="772d4-140">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="772d4-141">See kuupäev peab olema kas täna või tulevikus.</span><span class="sxs-lookup"><span data-stu-id="772d4-141">This date has to be either today or in the future.</span></span>

6. <span data-ttu-id="772d4-142">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="772d4-142">Select **OK**.</span></span> <span data-ttu-id="772d4-143">Lisandumisprotsess kustutab viitvõlad teie määratud parameetritega.</span><span class="sxs-lookup"><span data-stu-id="772d4-143">The accrual process will delete accruals with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a><span data-ttu-id="772d4-144">Ühe töövõtja puhkuste ja puudumiste lisamiste kustutamine</span><span class="sxs-lookup"><span data-stu-id="772d4-144">Delete leave and absence accruals for a single employee</span></span>

1. <span data-ttu-id="772d4-145">Töövõtja kirjes valige suvand **Puhkus**.</span><span class="sxs-lookup"><span data-stu-id="772d4-145">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="772d4-146">Valige **Puhkuse- ja puudumise plaani viitvõlgade kustutamine**.</span><span class="sxs-lookup"><span data-stu-id="772d4-146">Select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="772d4-147">Dialoogiboksis **Puhkuse- ja puudumise plaani viitvõlgade kustutamine** valige **Puhkuse plaan**.</span><span class="sxs-lookup"><span data-stu-id="772d4-147">In the **Delete leave and absence plan accruals** dialog box, select **Leave plan**.</span></span>

4. <span data-ttu-id="772d4-148">Vajadusel valige **Kustuta saldo korrigeerimised**.</span><span class="sxs-lookup"><span data-stu-id="772d4-148">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="772d4-149">Sisestage või valige **Puhkuse viitvõla kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="772d4-149">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="772d4-150">See kuupäev peab olema kas täna või tulevikus.</span><span class="sxs-lookup"><span data-stu-id="772d4-150">This date must be either today or in the future.</span></span>

6. <span data-ttu-id="772d4-151">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="772d4-151">Select **OK**.</span></span> <span data-ttu-id="772d4-152">Lisandumisprotsess kustutab viitvõlad teie määratud parameetritega.</span><span class="sxs-lookup"><span data-stu-id="772d4-152">The accrual process will delete accruals with the parameters you set.</span></span>

## <a name="review-leave-accrual-and-deletion-processes"></a><span data-ttu-id="772d4-153">Puhkuse viitvõla ja kustutamise protsesside läbivaatamine</span><span class="sxs-lookup"><span data-stu-id="772d4-153">Review leave accrual and deletion processes</span></span>

<span data-ttu-id="772d4-154">**Puhkuse viitvõla audit** kuvatakse iga kord, kui käivitate või kustutate ühe või kõigi töövõtjate viitvõlad.</span><span class="sxs-lookup"><span data-stu-id="772d4-154">**Leave accrual audit** displays each time you run or delete an accrual for one or all employees.</span></span> <span data-ttu-id="772d4-155">Kuvatakse ka toimingu kuupäev ja selle teinud isik.</span><span class="sxs-lookup"><span data-stu-id="772d4-155">The date and person who performed the action also displays.</span></span>

1. <span data-ttu-id="772d4-156">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="772d4-156">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="772d4-157">Jaotises **Puhkuse haldamine** valige suvand **Puhkuse viitvõla auditi kustutamine**.</span><span class="sxs-lookup"><span data-stu-id="772d4-157">Under **Manage leave**, select **Delete leave accrual audit**.</span></span>

## <a name="preview-leave-accrual-transaction-auditing"></a><span data-ttu-id="772d4-158">(Eelversioon) Puhkuse tekkepõhise kande auditeerimine</span><span class="sxs-lookup"><span data-stu-id="772d4-158">(Preview) Leave accrual transaction auditing</span></span>

[!include [Preview feature](includes/preview-feature.md)]

<span data-ttu-id="772d4-159">See eelvaate funktsioon aitab puhkuse- ja puudumistehalduritel mõista puhkuse- ja puudumiste viitvõlakandeid, mis on seotud töötaja konkreetse puhkusetüübi jaoks ajalt väljasaldoga.</span><span class="sxs-lookup"><span data-stu-id="772d4-159">This preview feature helps leave and absence managers understand the leave and absence accrual transactions related to an employee’s time off balances for a specific leave type.</span></span>

<span data-ttu-id="772d4-160">Kande üksikasjade vaatamiseks:</span><span class="sxs-lookup"><span data-stu-id="772d4-160">To view transaction details:</span></span>

1. <span data-ttu-id="772d4-161">Töövõtja kirjes valige suvand **Puhkus**.</span><span class="sxs-lookup"><span data-stu-id="772d4-161">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="772d4-162">Valige suvand **Kuva välja aeg** ja seejärel vahekaart **Saldod**.</span><span class="sxs-lookup"><span data-stu-id="772d4-162">Select **View time off**, and then select the **Balances** tab.</span></span>

<span data-ttu-id="772d4-163">Konkreetse puhkusetüübiga seotud tekkepõhiste kannete vaatamiseks valige arvväärtus veerus **Praegune salddo**.</span><span class="sxs-lookup"><span data-stu-id="772d4-163">To view the accrual transactions related to a specific leave type, select the numerical value in the **Current balance** column.</span></span>

<span data-ttu-id="772d4-164">Konkreetse viitvõlasumma kande üksikasjade vaatamiseks valige viitvõla rida, avage paremalt paneelilt **Seotud teave** jaotis ja seejärel valige avamiseks **Kande üksikasjad** jaotis.</span><span class="sxs-lookup"><span data-stu-id="772d4-164">To view the transaction details for a specific accrual amount, select an accrual row, open the **Related information** panel on the right, and then open the **Transaction details** section.</span></span> <span data-ttu-id="772d4-165">Kande üksikasjade jaotis kuvatakse:</span><span class="sxs-lookup"><span data-stu-id="772d4-165">The Transaction details section displays:</span></span>

- <span data-ttu-id="772d4-166">Töötaja puhkuse tüübi saldo muutmiseks</span><span class="sxs-lookup"><span data-stu-id="772d4-166">Changes to the employee’s leave type balance</span></span>
- <span data-ttu-id="772d4-167">Tööhõive üksikasjad selle kindlaksmääratud tekkepõhise perioodi kohta</span><span class="sxs-lookup"><span data-stu-id="772d4-167">Employment details for that specified accrual period</span></span>
- <span data-ttu-id="772d4-168">Kindlaksmääratud perioodi üksikasjad ja määrad</span><span class="sxs-lookup"><span data-stu-id="772d4-168">Details about the accrual period and rates</span></span>
- <span data-ttu-id="772d4-169">Puhkuseplaani konfiguratsioonidest tehtud muudatused</span><span class="sxs-lookup"><span data-stu-id="772d4-169">Any changes made to leave plan configurations</span></span>

![Puhkuse tekkepõhise kande auditeerimine](media/hr-leave-and-absence-accrue-audit.png)

## <a name="see-also"></a><span data-ttu-id="772d4-171">Vt ka</span><span class="sxs-lookup"><span data-stu-id="772d4-171">See also</span></span>

[<span data-ttu-id="772d4-172">Puhkuste ja puudumiste ülevaade</span><span class="sxs-lookup"><span data-stu-id="772d4-172">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="772d4-173">Puhkuste ja puudumiste plaani loomine</span><span class="sxs-lookup"><span data-stu-id="772d4-173">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
