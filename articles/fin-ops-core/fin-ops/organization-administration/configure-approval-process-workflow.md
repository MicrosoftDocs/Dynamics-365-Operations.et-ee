---
title: Töövoo kinnitusprotsesside konfigureerimine
description: Kinnitusprotsessi atribuutide konfigureerimiseks tehke järgmist.
author: ChrisGarty
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5738c5993c129f9bb4932180916befaf6f6377a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751796"
---
# <a name="configure-approval-processes-in-a-workflow"></a><span data-ttu-id="c3cc1-103">Töövoo kinnitusprotsesside konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="c3cc1-103">Configure approval processes in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3cc1-104">Kinnitusprotsessi atribuutide konfigureerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="c3cc1-105">Kinnitusprotsessi konfigureerimiseks paremklõpsake töövooredaktoris kinnitamise elementi ja klõpsake seejärel valikut **Atribuudid**, et avada vorm **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-the-approval-process"></a><span data-ttu-id="c3cc1-106">Kinnitusprotsessile nime andmine</span><span class="sxs-lookup"><span data-stu-id="c3cc1-106">Name the approval process</span></span>

<span data-ttu-id="c3cc1-107">Kinnitusprotsessi nime sisestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-107">Follow these steps to enter a name for the approval process.</span></span>

1. <span data-ttu-id="c3cc1-108">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-108">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="c3cc1-109">Väljale **Nimi** sisestage kinnitusprotsessile kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="c3cc1-110">Määramine, millal süsteem dokumendiga automaatselt toimingu teeb</span><span class="sxs-lookup"><span data-stu-id="c3cc1-110">Specify when the system automatically acts on the document</span></span>

<span data-ttu-id="c3cc1-111">Saate konfigureerida süsteemi automaatselt dokumendiga tegelema, kui teatud tingimused on täidetud.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="c3cc1-112">Näiteks saab süsteem kinnitada kuluaruanded, mille kogusumma on väiksem kui 100 USA dollarit.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="c3cc1-113">Selleks et määrata, millal süsteem dokumendi puhul toimingu teeb, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-113">Follow these steps to specify when the system acts on the document.</span></span>

1. <span data-ttu-id="c3cc1-114">Klõpsake vasakpoolsel paanil suvandit **Automaatsed tegevused**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-114">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="c3cc1-115">Märkige ruut **Luba automaatsed tegevused**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-115">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="c3cc1-116">Klõpsake valikut **Lisa tingimus**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-116">Click **Add condition**.</span></span>
4. <span data-ttu-id="c3cc1-117">Sisestage tingimus.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-117">Enter a condition.</span></span>
5. <span data-ttu-id="c3cc1-118">Vajadusel lisage lisatingimused.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-118">Enter additional conditions, if necessary.</span></span>
6. <span data-ttu-id="c3cc1-119">Kontrollimaks, kas teie sisestatud tingimused on õigesti konfigureeritud, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="c3cc1-120">Klõpsake valikut **Katseta**, et avada leht **Katseta töövoo tingimust**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="c3cc1-121">Valige vormi alal kirje **Kontrolli tingimust**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-121">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="c3cc1-122">Klõpsake nuppu **Test**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-122">Click **Test**.</span></span> <span data-ttu-id="c3cc1-123">Süsteem hindab kirjet otsustamaks, kas see vastab teie määratud tingimustele.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="c3cc1-124">Klõpsake valikut **OK** või **Tühista**, et naasta vormile **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7. <span data-ttu-id="c3cc1-125">Loendist **Automaatne tegevus** valige tegevus, mille süsteem peaks ülesande puhul tegema.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="c3cc1-126">Määrake, millal teatisi saadetakse</span><span class="sxs-lookup"><span data-stu-id="c3cc1-126">Specify when notifications are sent</span></span>

<span data-ttu-id="c3cc1-127">Saate saata inimestele teatisi dokumendi kinnitamisel, tagasilükkamisel, delegeerimisel või laiendamisel või muudatuse taotlemisel.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="c3cc1-128">Tehke järgmist, et määrata, millal ja kellele teatisi saadetakse.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="c3cc1-129">Vasakul paanil klõpsake suvandit **Teatised**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-129">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="c3cc1-130">Märkige ruut sündmuste kõrval, mille puhul saadetakse teatis.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-130">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="c3cc1-131">**Delegeeri** – kui dokument on määratud kinnitamiseks teisele kasutajale.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    - <span data-ttu-id="c3cc1-132">**Laienda** – kui määratud kasutaja pole dokumendi puhul nõutavat toimingut eraldatud aja jooksul teinud.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    - <span data-ttu-id="c3cc1-133">**Kinnita** – kui dokument on kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-133">**Approve** – When a document has been approved.</span></span>
    - <span data-ttu-id="c3cc1-134">**Lükka tagasi** – kui dokument on tagasi lükatud.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-134">**Reject** – When a document has been rejected.</span></span>
    - <span data-ttu-id="c3cc1-135">**Muudatuse taotlus** – kui määratud kasutaja on taotlenud esitatud dokumendi muutmist.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3. <span data-ttu-id="c3cc1-136">Valige 2. etapis valitud sündmuse rida.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-136">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="c3cc1-137">Klõpsake vahekaarti **Teatise tekst**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-137">Click the **Notification text** tab.</span></span>
5. <span data-ttu-id="c3cc1-138">Sisestage tekstiväljale teatise nimi.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-138">In the text box, enter the text for the notification.</span></span>
6. <span data-ttu-id="c3cc1-139">Teksti isikupärastamiseks saate sisestada kohatäitjad, mis asendatakse sobivate andmetega, kui need kuvatakse kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="c3cc1-140">Kohatäitja sisestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-140">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="c3cc1-141">Kohatäitja asukoha määramiseks klõpsake tekstiväljal soovitud kohta.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2. <span data-ttu-id="c3cc1-142">Klõpsake nuppu **Sisesta kohatäide**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-142">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="c3cc1-143">Valige kuvatavast loendist sisestatav kohatäitja.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="c3cc1-144">Klõpsake nuppu **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-144">Click **Insert**.</span></span>

7. <span data-ttu-id="c3cc1-145">Teatise tõlgete lisamiseks klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="c3cc1-146">Kuvataval vormil tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-146">In the form that is displayed, follow these steps:</span></span>

    1. <span data-ttu-id="c3cc1-147">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-147">Click **Add**.</span></span>
    2. <span data-ttu-id="c3cc1-148">Valige kuvatavast loendist keel, milles soovite teksti sisestada.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3. <span data-ttu-id="c3cc1-149">Tekstiväljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-149">In the **Translated text** text box, enter the text.</span></span>
    4. <span data-ttu-id="c3cc1-150">Teksti isikupärastamiseks sisestage kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-150">To personalize the text, insert placeholders.</span></span>
    5. <span data-ttu-id="c3cc1-151">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-151">Click **Close**.</span></span>

8. <span data-ttu-id="c3cc1-152">Klõpsake vahekaarti **Adressaat**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-152">Click the **Recipient** tab.</span></span>
9. <span data-ttu-id="c3cc1-153">Määrake, kellele teatised saadetakse.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="c3cc1-154">Valige järgmises tabelis üks suvanditest ja seejärel järgige selle suvandi täiendavaid etappe, enne kui jätkate 10. etapiga.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="c3cc1-155">Suvand</span><span class="sxs-lookup"><span data-stu-id="c3cc1-155">Option</span></span></th>
    <th><span data-ttu-id="c3cc1-156">Teatise adressaadid</span><span class="sxs-lookup"><span data-stu-id="c3cc1-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="c3cc1-157">Täiendavad etapid</span><span class="sxs-lookup"><span data-stu-id="c3cc1-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="c3cc1-158"><strong>Osaleja</strong></span><span class="sxs-lookup"><span data-stu-id="c3cc1-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="c3cc1-159">Kasutajad, kes on määratud teatud grupile või rollile</span><span class="sxs-lookup"><span data-stu-id="c3cc1-159">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="c3cc1-160">Pärast suvandi <strong>Osaleja</strong> valimist klõpsake vahekaarti <strong>Rollil põhinev</strong>.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="c3cc1-161">Loendis <strong>Osaleja tüüp</strong> valige grupi või rolli tüüp, millele teatisi saata.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="c3cc1-162">Loendis <strong>Osaleja</strong> valige grupp või roll, millele teatisi saata.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="c3cc1-163"><strong>Töövoo kasutaja</strong></span><span class="sxs-lookup"><span data-stu-id="c3cc1-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="c3cc1-164">Kasutajad, kes osalevad praeguses töövoos</span><span class="sxs-lookup"><span data-stu-id="c3cc1-164">Users who participate in the current workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="c3cc1-165">Kui olete valinud suvandi <strong>Töövoo kasutaja</strong>, klõpsake vahekaarti <strong>Töövoo kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="c3cc1-166">Loendist <strong>Töövoo kasutaja</strong> valige töövoos osalev kasutaja.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="c3cc1-167"><strong>Kasutaja</strong></span><span class="sxs-lookup"><span data-stu-id="c3cc1-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="c3cc1-168">Kindlad kasutajad</span><span class="sxs-lookup"><span data-stu-id="c3cc1-168">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="c3cc1-169">Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="c3cc1-170">Valige kasutajad, kellele teatisi saata, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-170">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="c3cc1-171">Korrake etappe 3–9 iga sündmuse puhul, mille 2. etapis valisite.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-171">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="c3cc1-172"> Lõpliku kinnitaja määramine</span><span class="sxs-lookup"><span data-stu-id="c3cc1-172">Specify a final approver</span></span>

<span data-ttu-id="c3cc1-173">Saate määrata lõpliku kinnitaja stsenaariumite jaoks, kus kinnitaja on dokumendi kinnitamiseks esitanud isik ja kasutatakse nõuet "keela esitaja kinnitus".</span><span class="sxs-lookup"><span data-stu-id="c3cc1-173">You can designate a final approver for scenarios where the approver is the person who submitted the document for approval and the "disallow approval by submitter" is being used.</span></span> <span data-ttu-id="c3cc1-174">Lõpliku kinnitaja määramiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-174">Follow these steps to specify a final approver.</span></span>

1. <span data-ttu-id="c3cc1-175">Paremklõpsake töövooredaktoris kinnitamise elementi ja valige seejärel **Atribuudid**, et avada vorm **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-175">In the workflow editor, right-click the approval element, and then select **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="c3cc1-176">Klõpsake vasakpoolsel paanil suvandit **Täpsemad sätted**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-176">In the left pane, click **Advanced settings**.</span></span>
3. <span data-ttu-id="c3cc1-177">Märkige ruut **Kasuta lõplikku kinnitajat**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-177">Select the **Use final approver** check box.</span></span>
4. <span data-ttu-id="c3cc1-178">Valige loendist lõplikuks kinnitajaks määratav kasutaja.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-178">In the list, select a user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="c3cc1-179">Ajalimiidi seadmine</span><span class="sxs-lookup"><span data-stu-id="c3cc1-179">Set a time limit</span></span>

<span data-ttu-id="c3cc1-180">Kui kinnitusprotsess tuleb teatud ajaks lõpule viia, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-180">Follow these steps if the approval process must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="c3cc1-181">Neis etappides valitavad suvandid tühistavad iga kinnitusetapi aladel **Määramine** ja **Laiendus** valitud suvandid.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-181">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span>

1. <span data-ttu-id="c3cc1-182">Klõpsake vasakpoolsel paanil suvandit **Täpsemad sätted**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-182">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="c3cc1-183">Märkige ruut **Määra töövoo elemendi jaoks** **ajalimiit**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-183">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3. <span data-ttu-id="c3cc1-184">Määrake väljal **Kestus**, mis ajaks peab kinnitusprotsess olema lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-184">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="c3cc1-185">Tehke üks järgmistest valikutest:</span><span class="sxs-lookup"><span data-stu-id="c3cc1-185">Select one of the following options:</span></span>

    - <span data-ttu-id="c3cc1-186">**Tunnid** – sisestage tundide arv, mille jooksul tuleb kinnitusprotsess lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-186">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="c3cc1-187">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-187">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="c3cc1-188">**Päevad** – sisestage päevade arv, mille jooksul tuleb kinnitusprotsess lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-188">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="c3cc1-189">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-189">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="c3cc1-190">**Nädalad** – sisestage nädalate arv, mille jooksul tuleb kinnitusprotsess lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-190">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    - <span data-ttu-id="c3cc1-191">**Kuud** – valige päev ja nädal, milleks kinnitusprotsess peab olema lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-191">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="c3cc1-192">Näiteks võite soovida, et kinnitusprotsess oleks lõpule viidud kuu kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-192">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="c3cc1-193">**Aastad** – valige päev, nädal ja kuu, milleks kinnitusprotsess peab olema lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-193">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="c3cc1-194">Näiteks võite soovida, et kinnitusprotsess oleks valmis detsembri kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-194">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="c3cc1-195">Ajalimiidi ületamisel teeb süsteem dokumendiga tegevuse.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-195">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="c3cc1-196">Loendist **Tegevus** valige tegevus, mida süsteem peaks tegema.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-196">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="c3cc1-197">Määrake, millised tegevused on kasutaja jaoks saadaval</span><span class="sxs-lookup"><span data-stu-id="c3cc1-197">Specify which actions are available to the user</span></span>

<span data-ttu-id="c3cc1-198">Kasutaja peab talle määratud dokumendiga tegelema.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-198">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="c3cc1-199">Esitatud dokumendi puhul kasutajale saadaolevate tegevuste määramiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-199">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>

1. <span data-ttu-id="c3cc1-200">Klõpsake vasakpoolsel paanil suvandit **Täpsemad sätted**.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-200">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="c3cc1-201">Märkige ruut **Kinnita**, kui kasutaja võib dokumendi kinnitada.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-201">Select the **Approve** check box if the user can approve the document.</span></span>
3. <span data-ttu-id="c3cc1-202">Märkige ruut **Lükka tagasi**, kui kasutaja võib dokumendi tagasi lükata.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-202">Select the **Reject** check box the user can reject the document.</span></span>
4. <span data-ttu-id="c3cc1-203">Märkige ruut **Taotle muudatust**, kui kasutaja võib taotleda dokumendile muudatuste tegemist.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-203">Select the **Request change** check box the user can request changes to the document.</span></span>
5. <span data-ttu-id="c3cc1-204">Märkige ruut **Delegeeri**, kui kasutaja võib määrata dokumendile kinnitajaks teise kasutaja.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-204">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

> [!NOTE]
> <span data-ttu-id="c3cc1-205">Märkeruut **Tegevuste aktiveerimine ettevõtteportaali töödeloendist** pole soovitatav.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-205">The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="c3cc1-206"> Kinnitusetappide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="c3cc1-206">Configure the approval steps</span></span>

<span data-ttu-id="c3cc1-207">Kinnitusprotsess koosneb kinnitusetappidest.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-207">An approval process consists of approval steps.</span></span> <span data-ttu-id="c3cc1-208">Kinnitusprotsessi etappide lisamiseks ja konfigureerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-208">Complete the following procedure to add steps the approval process and configure the steps.</span></span>

1. <span data-ttu-id="c3cc1-209">Topeltklõpsake töövooredaktoris kinnitusprotsessi.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-209">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="c3cc1-210">Töövooredaktoris kuvatakse kinnitusprotsessi etapid.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-210">The workflow editor displays the steps of the approval process.</span></span>
2. <span data-ttu-id="c3cc1-211">Kinnitusetapi lisamiseks lohistage etapp alalt **Töövoo elemendid** lõuendile.</span><span class="sxs-lookup"><span data-stu-id="c3cc1-211">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3. <span data-ttu-id="c3cc1-212">Kinnitusetapi konfigureerimiseks vaadake jaotist [Töövoos kinnitusetappide konfigureerimine](configure-approval-step-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="c3cc1-212">To configure an approval step, see [Configure approval steps in a workflow](configure-approval-step-workflow.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]