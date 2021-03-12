---
title: Töövoos automaatsete ülesannete konfigureerimine
description: See teema selgitab, kuidas konfigureerida automatiseeritud ülesande atribuute.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 003a5d2332aaf12ee7e9352ecb61ef190c04a41f
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798901"
---
# <a name="configure-automated-tasks-in-a-workflow"></a><span data-ttu-id="4142c-103">Töövoos automaatsete ülesannete konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="4142c-103">Configure automated tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4142c-104">See teema selgitab, kuidas konfigureerida automatiseeritud ülesande atribuute.</span><span class="sxs-lookup"><span data-stu-id="4142c-104">This topic explains how to configure the properties for an automated task.</span></span>

<span data-ttu-id="4142c-105">Töövoo redaktoris automatiseeritud ülesande loomiseks paremklõpsake ülesannet ja seejärel klõpsake suvandit **Atribuudid**, et avada lehekülg **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="4142c-105">To configure an automated task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="4142c-106">Seejärel kasutage järgmisi protseduure, et konfigureerida automatiseeritud ülesande atribuudid.</span><span class="sxs-lookup"><span data-stu-id="4142c-106">Then use the following procedures to configure the properties for the automated task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="4142c-107">Ülesandele nime andmine</span><span class="sxs-lookup"><span data-stu-id="4142c-107">Name the task</span></span>

<span data-ttu-id="4142c-108">Sisestage automatiseeritud ülesandele nimi järgmisi juhiseid järgides.</span><span class="sxs-lookup"><span data-stu-id="4142c-108">Follow these steps to enter a name for the automated task.</span></span>

1. <span data-ttu-id="4142c-109">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="4142c-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="4142c-110">Sisestage ülesande kordumatu nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="4142c-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="4142c-111">Määrake, millal teatisi saadetakse</span><span class="sxs-lookup"><span data-stu-id="4142c-111">Specify when notifications are sent</span></span>

<span data-ttu-id="4142c-112">Saate saate inimestele teatisi, kui automatiseeritud ülesannet käitatakse või see tühistatakse.</span><span class="sxs-lookup"><span data-stu-id="4142c-112">You can send notifications to people when an automated task has been run or canceled.</span></span> <span data-ttu-id="4142c-113">Tehke järgmist, et määrata, millal ja kellele teatisi saadetakse.</span><span class="sxs-lookup"><span data-stu-id="4142c-113">Follow these steps to specify when notifications are sent, and who they are sent to.</span></span>

1. <span data-ttu-id="4142c-114">Vasakul paanil klõpsake suvandit **Teatised**.</span><span class="sxs-lookup"><span data-stu-id="4142c-114">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="4142c-115">Märkige ruut sündmuste kõrval, mille puhul saadetakse teatis.</span><span class="sxs-lookup"><span data-stu-id="4142c-115">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="4142c-116">**Käivitamine** – teatised saadetakse ülesande käitamisel.</span><span class="sxs-lookup"><span data-stu-id="4142c-116">**Execution** – Notifications are sent when the task has been run.</span></span>
    - <span data-ttu-id="4142c-117">**Tühistatud** – teatised saadetakse ülesande tühistamisel.</span><span class="sxs-lookup"><span data-stu-id="4142c-117">**Canceled** – Notifications are sent when the task has been canceled.</span></span>

3. <span data-ttu-id="4142c-118">Valige 2. etapis valitud sündmuse rida.</span><span class="sxs-lookup"><span data-stu-id="4142c-118">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="4142c-119">Sisestage teatise tekst vahekaardil **Teatise tekst** olevale tekstiväljale.</span><span class="sxs-lookup"><span data-stu-id="4142c-119">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="4142c-120">Teatise isikupärastamiseks võite sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="4142c-120">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="4142c-121">Kohatäitjad asendatakse teatise kasutajatele kuvamisel sobivate andmetega.</span><span class="sxs-lookup"><span data-stu-id="4142c-121">Placeholders are replaced with appropriate data when the notification is shown to users.</span></span> <span data-ttu-id="4142c-122">Kohatäitja sisestamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="4142c-122">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="4142c-123">Tekstiboksis klõpsake seal, kuhu kohatäitja peaks ilmuma.</span><span class="sxs-lookup"><span data-stu-id="4142c-123">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="4142c-124">Klõpsake nuppu **Sisesta kohatäide**.</span><span class="sxs-lookup"><span data-stu-id="4142c-124">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="4142c-125">Ilmuvas loendis valige sisestamiseks kohatäitja.</span><span class="sxs-lookup"><span data-stu-id="4142c-125">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="4142c-126">Klõpsake nuppu **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="4142c-126">Click **Insert**.</span></span>

6. <span data-ttu-id="4142c-127">Teatise tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="4142c-127">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="4142c-128">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="4142c-128">Click **Translations**.</span></span>
    2. <span data-ttu-id="4142c-129">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="4142c-129">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="4142c-130">Ilmuvas loendis valige see keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="4142c-130">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="4142c-131">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="4142c-131">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="4142c-132">Teksti isikupärastamiseks saate sisestada kohatäitjad, nagu on kirjeldatud etapis 5.</span><span class="sxs-lookup"><span data-stu-id="4142c-132">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="4142c-133">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="4142c-133">Click **Close**.</span></span>

7. <span data-ttu-id="4142c-134">Määrake vahekaardil **Adressaat**, kellele teatised saadetakse.</span><span class="sxs-lookup"><span data-stu-id="4142c-134">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="4142c-135">Valige järgmises tabelis üks valikutest ja seejärel järgige selle valiku täiendavaid etappe, enne kui jätkate 8. etapiga.</span><span class="sxs-lookup"><span data-stu-id="4142c-135">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="4142c-136">Suvand</span><span class="sxs-lookup"><span data-stu-id="4142c-136">Option</span></span></th>
    <th><span data-ttu-id="4142c-137">Teatise adressaadid</span><span class="sxs-lookup"><span data-stu-id="4142c-137">Notification recipients</span></span></th>
    <th><span data-ttu-id="4142c-138">Täiendavad etapid</span><span class="sxs-lookup"><span data-stu-id="4142c-138">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="4142c-139">Osaleja</span><span class="sxs-lookup"><span data-stu-id="4142c-139">Participant</span></span></td>
    <td><span data-ttu-id="4142c-140">Kasutajad, kes on määratud teatud grupile või rollile</span><span class="sxs-lookup"><span data-stu-id="4142c-140">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="4142c-141">Kui olete valinud suvandi <strong>Osaleja</strong> vahekaardil <strong>Rollipõhine</strong> loendis <strong>Osaleja tüüp</strong>, valige grupi või rolli tüüp, millele teatisi saata.</span><span class="sxs-lookup"><span data-stu-id="4142c-141">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="4142c-142">Loendis <strong>Osaleja</strong> valige grupp või roll, millele teatisi saata.</span><span class="sxs-lookup"><span data-stu-id="4142c-142">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="4142c-143">Töövoo kasutaja</span><span class="sxs-lookup"><span data-stu-id="4142c-143">Workflow user</span></span></td>
    <td><span data-ttu-id="4142c-144">Kasutajad, kes osalevad praeguses töövoos</span><span class="sxs-lookup"><span data-stu-id="4142c-144">Users who participate in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="4142c-145">Kui olete valinud suvandi <strong>Töövoo kasutaja</strong> vahekaardil <strong>Töövoo kasutaja</strong> loendis <strong>Töövoo kasutaja</strong> valige kasutaja, kes osaleb töövoos.</span><span class="sxs-lookup"><span data-stu-id="4142c-145">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="4142c-146">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="4142c-146">User</span></span></td>
    <td><span data-ttu-id="4142c-147">Kindlad kasutajad</span><span class="sxs-lookup"><span data-stu-id="4142c-147">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="4142c-148">Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="4142c-148">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="4142c-149">Loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki kasutajaid.</span><span class="sxs-lookup"><span data-stu-id="4142c-149">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="4142c-150">Valige kasutajad, kellele teatisi saata, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</span><span class="sxs-lookup"><span data-stu-id="4142c-150">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="4142c-151">Korrake 3.–7. toimingut iga sündmuse puhul, mille 2. etapis valisite.</span><span class="sxs-lookup"><span data-stu-id="4142c-151">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>
