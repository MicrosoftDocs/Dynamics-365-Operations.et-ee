---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (25. veebruar 2020)
description: Selles artiklis kirjeldatakse Microsoft Dynamics 365 Human Resourcesi uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 02/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e5bc232bef257e757086d37d56b0f68b80114749
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555071"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a><span data-ttu-id="b99bb-103">Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (25. veebruar 2020)</span><span class="sxs-lookup"><span data-stu-id="b99bb-103">What's new or changed in Dynamics 365 Human Resources (February 25, 2020)</span></span>

<span data-ttu-id="b99bb-104">Selles artiklis kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone.</span><span class="sxs-lookup"><span data-stu-id="b99bb-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b99bb-105">Muudatused rakenduvad versioonile number 8.1.2927.</span><span class="sxs-lookup"><span data-stu-id="b99bb-105">Changes apply to build number 8.1.2927.</span></span> <span data-ttu-id="b99bb-106">Sulgudes olevad numbrid mõnedes pealkirjades viitavad LCS-i toenumbritele viitamise jaoks.</span><span class="sxs-lookup"><span data-stu-id="b99bb-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a><span data-ttu-id="b99bb-107">Juhtumihalduse navigeerimise ja andmete haldamise raamistiku (DMF) üksuse lubamine (414754)</span><span class="sxs-lookup"><span data-stu-id="b99bb-107">Enable Case Management navigation and data management framework (DMF) entity (414754)</span></span>

<span data-ttu-id="b99bb-108">See eelvaate funktsioon lubab juhtumihalduse juhtumite täiendava navigeerimise.</span><span class="sxs-lookup"><span data-stu-id="b99bb-108">This preview feature enables additional navigation to case management cases.</span></span> <span data-ttu-id="b99bb-109">Saate lubada selle eelvaate funktsiooni tööruumis **Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="b99bb-109">You can enable this preview feature in the **Feature Management** workspace.</span></span> <span data-ttu-id="b99bb-110">Need menüü üksused kuvatakse Dynamics 365 Human Resourcesi tööruumis **Vastavus**.</span><span class="sxs-lookup"><span data-stu-id="b99bb-110">These menu items appear in the **Compliance** workspace of Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b99bb-111">Selle muudatusega on Human Resourcesil juurdepääs järgnevale:</span><span class="sxs-lookup"><span data-stu-id="b99bb-111">With this change, Human Resources can access:</span></span>

- <span data-ttu-id="b99bb-112">Kõik juhtumid</span><span class="sxs-lookup"><span data-stu-id="b99bb-112">All cases</span></span>
- <span data-ttu-id="b99bb-113">Minu juhtumid</span><span class="sxs-lookup"><span data-stu-id="b99bb-113">My cases</span></span>
- <span data-ttu-id="b99bb-114">Minu avatud juhtumid</span><span class="sxs-lookup"><span data-stu-id="b99bb-114">My open cases</span></span>
- <span data-ttu-id="b99bb-115">Minu tähtaja ületanud juhtumid</span><span class="sxs-lookup"><span data-stu-id="b99bb-115">My overdue cases</span></span>
- <span data-ttu-id="b99bb-116">Mulle töövoo kaudu määratud juhtumid</span><span class="sxs-lookup"><span data-stu-id="b99bb-116">Cases assigned to me through workflow</span></span>

<span data-ttu-id="b99bb-117">Koos uute vaadetega juhtumitele on saadaval ka DMF-i üksus **Juhtumi üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="b99bb-117">Along with these new views into cases, the **Case detail** DMF entity is also available.</span></span>

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a><span data-ttu-id="b99bb-118">Seoste määratluste lubamine globaalses aadressiraamatus (414762)</span><span class="sxs-lookup"><span data-stu-id="b99bb-118">Enable Relationship definitions in global address bBook (414762)</span></span>

<span data-ttu-id="b99bb-119">Seosed on nüüd globaalses aadressiraamatus lubatud.</span><span class="sxs-lookup"><span data-stu-id="b99bb-119">Relationships are now enabled in the global address book.</span></span> <span data-ttu-id="b99bb-120">Enne selle nädala väljalaset kuvati kiirinfos **Seos** kõik süsteemi määratletud seosed.</span><span class="sxs-lookup"><span data-stu-id="b99bb-120">Prior to this week's release, the **Relationship** fact box displayed any system-defined relationships.</span></span> <span data-ttu-id="b99bb-121">Nüüd saate määratleda need seosed globaalse aadressiraamatu lehel.</span><span class="sxs-lookup"><span data-stu-id="b99bb-121">Now you can define those relationships within the global address book page.</span></span>

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a><span data-ttu-id="b99bb-122">Ametikoha saab eemaldada, kui selle jaoks on olemas aktiivsed kompensatsioonikirjed (414568)</span><span class="sxs-lookup"><span data-stu-id="b99bb-122">A position can be removed when active compensation records exist for the position (414568)</span></span>

<span data-ttu-id="b99bb-123">Selle muudatusega kuvatakse hoiatus, kui proovite kustutada ametikohta, kuid töötajal on aktiivne kompensatsioonikirje sellel ametikohal.</span><span class="sxs-lookup"><span data-stu-id="b99bb-123">With this change, a warning appears when you attempt to delete a position and a worker has an active compensation record for that same position.</span></span> <span data-ttu-id="b99bb-124">Sel juhul peate enne ametikoha eemaldamist uuendama töötaja põhipalga kirje.</span><span class="sxs-lookup"><span data-stu-id="b99bb-124">When this happens, you must update the employee fixed compensation record before removing the position.</span></span>

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a><span data-ttu-id="b99bb-125">Tulemuslikkuse hindamise töövoog lisab aeg-ajalt nõusolekuid inimestelt, kes ei ole protsessi osa (414171)</span><span class="sxs-lookup"><span data-stu-id="b99bb-125">Performance review workflow occasionally adds sign-offs from people who are not part of the process (414171)</span></span>

<span data-ttu-id="b99bb-126">See muudatus lahendab probleemi, mille puhul lisatakse tulemuslikkuse hindamisse täiendavaid nõusoleku andnud osalejaid.</span><span class="sxs-lookup"><span data-stu-id="b99bb-126">This change corrects an issue where additional sign-off participants are added to the performance review.</span></span>

## <a name="worker-position-assignment-not-created-in-common-data-service-when-selected-on-the-new-worker-dialog-413479"></a><span data-ttu-id="b99bb-127">Töötaja ametikoha määramist ei looda Common Data Service'is, kui see valitakse uue töötaja dialoogis (413479)</span><span class="sxs-lookup"><span data-stu-id="b99bb-127">Worker position assignment not created in Common Data Service when selected on the New Worker dialog (413479)</span></span>

<span data-ttu-id="b99bb-128">See muudatus lahendab probleemi uue töötaja palkamisel ja talle ametikoha määramisel dialoogi **Uus töötaja** kaudu.</span><span class="sxs-lookup"><span data-stu-id="b99bb-128">This change corrects an issue when hiring a new worker and assigning the new hire to a position through the **New worker** dialog.</span></span> <span data-ttu-id="b99bb-129">Ametikoha määramine kajastub nüüd Common Data Service'is.</span><span class="sxs-lookup"><span data-stu-id="b99bb-129">Now the position assignment is reflected in Common Data Service.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="b99bb-130">Peagi tulekul</span><span class="sxs-lookup"><span data-stu-id="b99bb-130">Coming soon</span></span>

### <a name="updated-common-data-service-solution"></a><span data-ttu-id="b99bb-131">Värskendatud lahendus Common Data Service</span><span class="sxs-lookup"><span data-stu-id="b99bb-131">Updated Common Data Service solution</span></span>

<span data-ttu-id="b99bb-132">Uus lahendus Common Data Service on varsti saadaval järgmiste muudatustega.</span><span class="sxs-lookup"><span data-stu-id="b99bb-132">A new Common Data Service solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="b99bb-133">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b99bb-133">Description</span></span> | <span data-ttu-id="b99bb-134">Muutmine</span><span class="sxs-lookup"><span data-stu-id="b99bb-134">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="b99bb-135">Üksuse **Töö/ametikoht** muudatused</span><span class="sxs-lookup"><span data-stu-id="b99bb-135">**Job/Position** entity changes</span></span> | <span data-ttu-id="b99bb-136">Lisatud **Hüvituspiirkond**</span><span class="sxs-lookup"><span data-stu-id="b99bb-136">**Compensation region** added</span></span></br><span data-ttu-id="b99bb-137">Lisatud **Finantsdimensioonid**</span><span class="sxs-lookup"><span data-stu-id="b99bb-137">**Financial dimensions** added</span></span> |
| <span data-ttu-id="b99bb-138">Üksuse **Töötaja** muudatused</span><span class="sxs-lookup"><span data-stu-id="b99bb-138">**Worker** entity changes</span></span> | <span data-ttu-id="b99bb-139">Lisatud **Nimeseeria**</span><span class="sxs-lookup"><span data-stu-id="b99bb-139">**Name sequence** added</span></span></br><span data-ttu-id="b99bb-140">Lisatud **Töötab kodust**</span><span class="sxs-lookup"><span data-stu-id="b99bb-140">**Works from home** added</span></span></br><span data-ttu-id="b99bb-141">Lisatud **Keel**</span><span class="sxs-lookup"><span data-stu-id="b99bb-141">**Language** added</span></span></br><span data-ttu-id="b99bb-142">Lisatud **Staaži kuupäev**</span><span class="sxs-lookup"><span data-stu-id="b99bb-142">**Seniority date** added</span></span></br><span data-ttu-id="b99bb-143">Lisatud **Tähtpäeva kuupäev**</span><span class="sxs-lookup"><span data-stu-id="b99bb-143">**Anniversary date** added</span></span></br><span data-ttu-id="b99bb-144">Lisatud **Värbamise algne kuupäev**</span><span class="sxs-lookup"><span data-stu-id="b99bb-144">**Original hire date** added</span></span> |
| <span data-ttu-id="b99bb-145">Olemi **Tööhõive** muudatused</span><span class="sxs-lookup"><span data-stu-id="b99bb-145">**Employment** entity changes</span></span> | <span data-ttu-id="b99bb-146">Lisatud **Finantsdimensioonid**</span><span class="sxs-lookup"><span data-stu-id="b99bb-146">**Financial dimensions** added</span></span></br><span data-ttu-id="b99bb-147">Lisatud **Lõpetamise põhjus**</span><span class="sxs-lookup"><span data-stu-id="b99bb-147">**Termination reason** added</span></span></br><span data-ttu-id="b99bb-148">Suvand **Lõpetamiskuupäev** on nimetatud ümber suvandist **Üleviimise kuupäeva**</span><span class="sxs-lookup"><span data-stu-id="b99bb-148">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="b99bb-149">Lisatud **Katseaja kuupäev**</span><span class="sxs-lookup"><span data-stu-id="b99bb-149">**Probation date** added</span></span> |
| <span data-ttu-id="b99bb-150">Üksuse **Töötaja aadress** muudatused</span><span class="sxs-lookup"><span data-stu-id="b99bb-150">**Worker address** entity changes</span></span> | <span data-ttu-id="b99bb-151">Lisatud **Tänavanimi**</span><span class="sxs-lookup"><span data-stu-id="b99bb-151">**Street address** added</span></span></br><span data-ttu-id="b99bb-152">Suvandid **Aadressirida 1**, **Aadressirida 2** ja **Aadressirida 3** on märgistatud kasutuselt eemaldamiseks</span><span class="sxs-lookup"><span data-stu-id="b99bb-152">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="b99bb-153">Uued ergutussüsteemi seadistuse üksused</span><span class="sxs-lookup"><span data-stu-id="b99bb-153">New variable compensation setup entities</span></span> | <span data-ttu-id="b99bb-154">**Muutuva hüvitisplaani tüüp**</span><span class="sxs-lookup"><span data-stu-id="b99bb-154">**Compensation variable plan type**</span></span></br><span data-ttu-id="b99bb-155">**Kompensatsiooni tulemusplaan**</span><span class="sxs-lookup"><span data-stu-id="b99bb-155">**Compensation variable plan**</span></span></br><span data-ttu-id="b99bb-156">**Pensionireeglid**</span><span class="sxs-lookup"><span data-stu-id="b99bb-156">**Vesting rules**</span></span></br><span data-ttu-id="b99bb-157">**Muutuva hüvitisplaani tase**</span><span class="sxs-lookup"><span data-stu-id="b99bb-157">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="b99bb-158">Uus olem **Töötaja kalendri tööhõive**</span><span class="sxs-lookup"><span data-stu-id="b99bb-158">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="b99bb-159">Lisatud **Töökalendri üksus**</span><span class="sxs-lookup"><span data-stu-id="b99bb-159">**Work calendar entity** added</span></span> |
| <span data-ttu-id="b99bb-160">Uus olem **Palgaarvestuse ametikoha üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="b99bb-160">New **Payroll position detail** entity</span></span> | <span data-ttu-id="b99bb-161">Lisatud **Palgaarvestuse ametikoha üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="b99bb-161">**Payroll position detail** added</span></span> |
| <span data-ttu-id="b99bb-162">Uus üksus **Ametinimetus**</span><span class="sxs-lookup"><span data-stu-id="b99bb-162">New **Title** entity</span></span> | <span data-ttu-id="b99bb-163">Lisatud **Ametinimetus**.</span><span class="sxs-lookup"><span data-stu-id="b99bb-163">**Title** added.</span></span> <span data-ttu-id="b99bb-164">Uus üksus **Pealkiri** kaasatakse sünkroonimisprotsessi rakenduse Human Resources ja teenuse Common Data Service vahel.</span><span class="sxs-lookup"><span data-stu-id="b99bb-164">The new **Title** entity will be included in the sync process between Human Resources and Common Data Service.</span></span> <span data-ttu-id="b99bb-165">Kuid algselt ei viidata sellele üksustelt **Ametikoht** või **Töö**.</span><span class="sxs-lookup"><span data-stu-id="b99bb-165">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

<span data-ttu-id="b99bb-166">Paari järgneva nädala jooksul on need üksusemuudatused saadaval kõikides keskkondades.</span><span class="sxs-lookup"><span data-stu-id="b99bb-166">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="b99bb-167">Human Resourcesi uusima Common Data Service'i lahenduse käsitsi installimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b99bb-167">To manually install the latest Common Data Service solution for Human Resources:</span></span>

1.  <span data-ttu-id="b99bb-168">Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="b99bb-168">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="b99bb-169">Valige **Keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="b99bb-169">Select **Environments**.</span></span>

3.  <span data-ttu-id="b99bb-170">Otsige üles keskkond, mida soovite uuendada.</span><span class="sxs-lookup"><span data-stu-id="b99bb-170">Find the environment you want to upgrade.</span></span> <span data-ttu-id="b99bb-171">See peab vastama **Keskkonna nimele** jaotises **Common Data Service'i teave** Human Resourcesi vormil **Teave**.</span><span class="sxs-lookup"><span data-stu-id="b99bb-171">This should correspond to **Environment name** in the **Common Data Service information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="b99bb-172">Keskkonna üksikasjade vaatamiseks valige keskkond.</span><span class="sxs-lookup"><span data-stu-id="b99bb-172">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="b99bb-173">Valige ülaosast toiminguribalt nupp **Halda lahendusi**.</span><span class="sxs-lookup"><span data-stu-id="b99bb-173">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="b99bb-174">Avaneb uus brauseri aken, seejärel liikuge oma keskkonna kontekstis jaotisesse **Dynamics 365 halduskeskus**.</span><span class="sxs-lookup"><span data-stu-id="b99bb-174">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="b99bb-175">Loendis **Lahendus** valige **Dynamics 365 Human Resourcesi ankurdaja**.</span><span class="sxs-lookup"><span data-stu-id="b99bb-175">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="b99bb-176">Uusima lahenduse rakendamiseks valige **Uuenda**.</span><span class="sxs-lookup"><span data-stu-id="b99bb-176">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="in-preview"></a><span data-ttu-id="b99bb-177">Eelvaates</span><span class="sxs-lookup"><span data-stu-id="b99bb-177">In preview</span></span>

<span data-ttu-id="b99bb-178">3. veebruarist 2020 on saadaval järgmised eelvaatefunktsioonid.</span><span class="sxs-lookup"><span data-stu-id="b99bb-178">The following preview features became available on February 3, 2020:</span></span>

- <span data-ttu-id="b99bb-179">**Puhkuste ja puudumiste eelvaatefunktsioonid** – lisateavet vt [Puhkuste ja puudumiste eelvaatefunktsioonid](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span><span class="sxs-lookup"><span data-stu-id="b99bb-179">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="b99bb-180">**Soodustuste halduse eelvaatefunktsioon** – lisateavet, sh teadaolevaid probleeme vt [Soodustuste halduse ülevaade](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b99bb-180">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b99bb-181">Vt ka</span><span class="sxs-lookup"><span data-stu-id="b99bb-181">See also</span></span>

[<span data-ttu-id="b99bb-182">Mis on uut või mida on muudetud rakenduses Human Resources?</span><span class="sxs-lookup"><span data-stu-id="b99bb-182">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="b99bb-183">Dynamics 365 Human Resources 2019 väljalaskevoo 2 ülevaade</span><span class="sxs-lookup"><span data-stu-id="b99bb-183">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="b99bb-184">Värskendamisprotsess</span><span class="sxs-lookup"><span data-stu-id="b99bb-184">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="b99bb-185">Funktsioonide haldamine</span><span class="sxs-lookup"><span data-stu-id="b99bb-185">Manage features</span></span>](hr-admin-manage-features.md)