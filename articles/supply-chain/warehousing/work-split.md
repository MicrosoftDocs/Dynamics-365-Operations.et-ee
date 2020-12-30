---
title: Töö tükeldamine
description: Selles teemas kirjeldatakse töö jaotamise funktsiooni. See funktsioon võimaldab teil tükeldada suured töötellimused mitmeks väiksemaks töötellimuseks, mille saate määrata mitmele lao töötajale. Sel viisil saab sama tööd üheaegselt komplekteerida mitu lao töötajat.
author: mirzaab
manager: tfehr
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e74b630e72d70829938f0f34efd624509b1ba7c3
ms.sourcegitcommit: 531be324bf706ca727d777720df899d6ddd3c2d7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/05/2020
ms.locfileid: "4426732"
---
# <a name="work-split"></a><span data-ttu-id="93cf1-105">Töö tükeldamine</span><span class="sxs-lookup"><span data-stu-id="93cf1-105">Work split</span></span>

<span data-ttu-id="93cf1-106">Töö jaotamise funktsioon võimaldab teil tükeldada suured töö ID-d (mitmete ridadega töötellimused) mitmeks väiksemaks töö ID-deks, mille saate määrata mitmele lao töötajale.</span><span class="sxs-lookup"><span data-stu-id="93cf1-106">Work split functionality lets you split large work IDs (that is, work orders that have several lines) into several smaller work IDs that you can then assign to multiple warehouse workers.</span></span> <span data-ttu-id="93cf1-107">Sel viisil saab sama töönumbrit üheaegselt komplekteerida mitu lao töötajat.</span><span class="sxs-lookup"><span data-stu-id="93cf1-107">In this way, the same work creation number can be picked simultaneously by several warehouse workers.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="93cf1-108">Saate tükeldada ainult töötellimusi, mille olek on *Avatud* või *Töös*.</span><span class="sxs-lookup"><span data-stu-id="93cf1-108">You can split only work orders that have a status of *Open* or *In-progress*.</span></span>

## <a name="turn-on-the-work-split-functionality"></a><span data-ttu-id="93cf1-109">Töö tükeldamise funktsioonide sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="93cf1-109">Turn on the work split functionality</span></span>

<span data-ttu-id="93cf1-110">Enne töö tükeldamise funktsiooni kasutamist peate oma süsteemis sisse lülitama funktsiooni ja selle eeltingimuse funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="93cf1-110">Before you can use the work split functionality, you must turn on the feature and its prerequisite feature in your system.</span></span> <span data-ttu-id="93cf1-111">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsioonide olekut ja vajadusel neid sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="93cf1-111">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on as required.</span></span>

<span data-ttu-id="93cf1-112">Esmalt lülitage sisse eeltingimuste *Organisatsiooniülene töö blokeerimise* funktsioon, kui see ei ole juba sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="93cf1-112">First, turn on the prerequisite *Organization-wide work blocking* feature if it isn't already turned on.</span></span> <span data-ttu-id="93cf1-113">Tööruumis **Funktsioonihaldus** loetletakse seda funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="93cf1-113">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="93cf1-114">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="93cf1-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="93cf1-115">**Funktsiooni nimi:** *Organisatsiooniülene töö blokeerimine*</span><span class="sxs-lookup"><span data-stu-id="93cf1-115">**Feature name:** *Organization-wide work blocking*</span></span>

> [!NOTE]
> <span data-ttu-id="93cf1-116">Kui see funktsioon on aktiveeritud, rakendatakse automaatset uuendamist pärast seda, kui funktsioon on kõigis juriidilistes isikutes sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="93cf1-116">When this feature is activated, a data upgrade is automatically applied after the feature is turned on across all legal entities.</span></span>

<span data-ttu-id="93cf1-117">Järgmisena lülitage sisse *Töö tükeldamise* funktsioon, mis on loetletud järgmisel viisil:</span><span class="sxs-lookup"><span data-stu-id="93cf1-117">Next, turn on the *Work split* feature, which is listed in the following way:</span></span>

- <span data-ttu-id="93cf1-118">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="93cf1-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="93cf1-119">**Funktsiooni nimi:** *Töö tükeldamine*</span><span class="sxs-lookup"><span data-stu-id="93cf1-119">**Feature name:** *Work split*</span></span>

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a><span data-ttu-id="93cf1-120">Töö üksikasjade ja kõigi töölehtede täiustused</span><span class="sxs-lookup"><span data-stu-id="93cf1-120">Enhancements to the Work details and All work pages</span></span>

<span data-ttu-id="93cf1-121">Funktsioon *Töö tükeldamine* lisab järgmised kaks nuppu tegumiriba **Töö** vahekaardil **Töö üksikasjade** ja **Kogu töö** lehtedele:</span><span class="sxs-lookup"><span data-stu-id="93cf1-121">The *Work split* feature adds the following two buttons to the **Work** tab on the Action Pane of the **Work details** and **All work** pages:</span></span>

- <span data-ttu-id="93cf1-122">**Töö tükeldamine** – Tükeldage käesolev töö ID mitmeks väiksemaks töö ID-ks, mida saavad töödelda erinevad töötajad.</span><span class="sxs-lookup"><span data-stu-id="93cf1-122">**Split work** – Split the current work ID into multiple smaller work IDs that can be processed by separate workers.</span></span>
- <span data-ttu-id="93cf1-123">**Tühista töö tükeldamise seanss** – Tühistage töö tükeldamise seanss ja tehke töö töötlemiseks saadaolevaks.</span><span class="sxs-lookup"><span data-stu-id="93cf1-123">**Cancel work split session** – Cancel the work split session, and make the work available for processing.</span></span>

<span data-ttu-id="93cf1-124">![Töö tükeldamise ja töö tükeldamise seansi tühistamise nupud](media/Work_split_buttons.png "Töö tükeldamise ja töö tükeldamise seansi tühistamise nupud")</span><span class="sxs-lookup"><span data-stu-id="93cf1-124">![Split work and Cancel work split session buttons](media/Work_split_buttons.png "Split work and Cancel work split session buttons")</span></span>

> [!IMPORTANT]
> <span data-ttu-id="93cf1-125">**Töö tükeldamise** nupp ei ole saadaval, kui on täidetud mõni järgmistest tingimustest:</span><span class="sxs-lookup"><span data-stu-id="93cf1-125">The **Split work** button won't be available if any of the following conditions are met:</span></span>
>
> - <span data-ttu-id="93cf1-126">Töö olek on midagi muud, kui *Avatud* või *Täitmisel*.</span><span class="sxs-lookup"><span data-stu-id="93cf1-126">The work status is something other than *Open* or *In progress*.</span></span>
> - <span data-ttu-id="93cf1-127">Konteineri ID on seotud töö ID-ga.</span><span class="sxs-lookup"><span data-stu-id="93cf1-127">A container ID is associated with the work ID.</span></span> <span data-ttu-id="93cf1-128">(Konteinerit ei saa süstemaatiliselt tükeldada, kuna see nõuab füüsilisi tegevusi.)</span><span class="sxs-lookup"><span data-stu-id="93cf1-128">(A container can't be systematically split, because it requires physical actions.)</span></span>
> - <span data-ttu-id="93cf1-129">Töö on seotud kogumiga.</span><span class="sxs-lookup"><span data-stu-id="93cf1-129">The work is associated with a cluster.</span></span>
> - <span data-ttu-id="93cf1-130">Töö tellimuse tüüp on midagi muud kui üks järgmistest tüüpidest:</span><span class="sxs-lookup"><span data-stu-id="93cf1-130">The work order type is something other than one of the following types:</span></span>
>
>    - <span data-ttu-id="93cf1-131">Müügitellimused</span><span class="sxs-lookup"><span data-stu-id="93cf1-131">Sales orders</span></span>
>    - <span data-ttu-id="93cf1-132">Toormaterjalide komplekteerimine</span><span class="sxs-lookup"><span data-stu-id="93cf1-132">Raw material picking</span></span>
>    - <span data-ttu-id="93cf1-133">Edastuse väljaminek</span><span class="sxs-lookup"><span data-stu-id="93cf1-133">Transfer issue</span></span>
>
> - <span data-ttu-id="93cf1-134">Töö on hetkel tükeldatud teise kasutaja poolt.</span><span class="sxs-lookup"><span data-stu-id="93cf1-134">The work is currently being split by another user.</span></span> <span data-ttu-id="93cf1-135">Kui proovite avada tükeldamise lehte töö jaoks, mida teine kasutaja juba tükeldab, kuvatakse järgmine tõrketeade: "Töö ID-ga \#\#\#\# on hetkel tükeldatud.</span><span class="sxs-lookup"><span data-stu-id="93cf1-135">If you try to open the splitting page for work that is already being split by another user, you receive the following error message: "The work with ID \#\#\#\# is currently being split.</span></span> <span data-ttu-id="93cf1-136">Proovige mõne minuti pärast uuesti.</span><span class="sxs-lookup"><span data-stu-id="93cf1-136">Retry in a few minutes.</span></span> <span data-ttu-id="93cf1-137">Kui saate pidevalt seda teadet, võtke ühendust juhendajaga."</span><span class="sxs-lookup"><span data-stu-id="93cf1-137">If you continue to receive this message, contact a supervisor."</span></span>

<span data-ttu-id="93cf1-138">Uus töö blokeerimise põhjus, *Tükeldatud töö*, näitab, millal on töö ID tükeldamise protsessis.</span><span class="sxs-lookup"><span data-stu-id="93cf1-138">A new work blocking reason, *Split work*, indicates when the work ID is in the process of being split.</span></span> <span data-ttu-id="93cf1-139">See kuvatakse **Töö tükeldamise** lehel kui ka laorakenduses, kui kasutaja proovib tööd teha.</span><span class="sxs-lookup"><span data-stu-id="93cf1-139">It's shown both on the **Split work** page and in the warehouse app if a user tries to run the work.</span></span> <span data-ttu-id="93cf1-140">Blokeerimise põhjuste kasutamisel muudetakse **Blokeeritud voo** välja nimi töö ID-lt olekusse **Blokeeritud**.</span><span class="sxs-lookup"><span data-stu-id="93cf1-140">When blocking reasons are used, the name of the **Blocked wave** field from the work ID is changed to **Blocked**.</span></span>

## <a name="initiate-a-work-split"></a><span data-ttu-id="93cf1-141">Alusta töö tükeldamist</span><span class="sxs-lookup"><span data-stu-id="93cf1-141">Initiate a work split</span></span>

<span data-ttu-id="93cf1-142">Funktsioon lisab uue **Töö tükeldamise** lehe, mis võimaldab kasutajatel tükeldada tööridu töö ID-st.</span><span class="sxs-lookup"><span data-stu-id="93cf1-142">The feature adds a new **Split work** page that lets users split work lines from the work ID.</span></span> <span data-ttu-id="93cf1-143">Kui leht avatakse esmakordselt, kuvatakse read, millel on tööolek *Avatud* ja mis on saadaval tükeldamiseks.</span><span class="sxs-lookup"><span data-stu-id="93cf1-143">When the page is first opened, it shows lines that have a work status of *Open* and that are available to be split.</span></span> <span data-ttu-id="93cf1-144">Valitud töö töötlemiseks valige tegumiribal **Töö tükeldamine**.</span><span class="sxs-lookup"><span data-stu-id="93cf1-144">On the Action Pane, select **Split work** to process the selected work.</span></span>

<span data-ttu-id="93cf1-145">Töö tükeldamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="93cf1-145">To split work, follow these steps.</span></span>

1. <span data-ttu-id="93cf1-146">Avage üks järgmistest töölehtedest:</span><span class="sxs-lookup"><span data-stu-id="93cf1-146">Open one of the following work pages:</span></span>

    - <span data-ttu-id="93cf1-147">**Töö üksikasjad** (**Laohaldus \> Töö \> Töö üksikasjad**)</span><span class="sxs-lookup"><span data-stu-id="93cf1-147">**Work details** (**Warehouse management \> Work \> Work details**)</span></span>
    - <span data-ttu-id="93cf1-148">**Kogu töö** (**Laohaldus \> Töö \> Kogu töö**)</span><span class="sxs-lookup"><span data-stu-id="93cf1-148">**All work** (**Warehouse management \> Work \> All work**)</span></span>

1. <span data-ttu-id="93cf1-149">Valige ruudustikus tükeldamiseks töö ID.</span><span class="sxs-lookup"><span data-stu-id="93cf1-149">In the grid, select a work ID to split.</span></span> <span data-ttu-id="93cf1-150">Välja **Töö tellimuse tüüp** väärtuseks peab olema seatud üks järgmistest väärtustest:</span><span class="sxs-lookup"><span data-stu-id="93cf1-150">The **Work order type** field must be set to one of the following values:</span></span>

    - <span data-ttu-id="93cf1-151">Müügitellimused</span><span class="sxs-lookup"><span data-stu-id="93cf1-151">Sales orders</span></span>
    - <span data-ttu-id="93cf1-152">Toormaterjalide komplekteerimine</span><span class="sxs-lookup"><span data-stu-id="93cf1-152">Raw material picking</span></span>
    - <span data-ttu-id="93cf1-153">Edastuse väljaminek</span><span class="sxs-lookup"><span data-stu-id="93cf1-153">Transfer issue</span></span>

1. <span data-ttu-id="93cf1-154">Valige tegumiribal **Töö** vahekaardil **Töö** grupis olev üksus **Töö tükeldamine**.</span><span class="sxs-lookup"><span data-stu-id="93cf1-154">On the Action Pane, on the **Work** tab, in the **Work** group, select **Split work**.</span></span>

    <span data-ttu-id="93cf1-155">Kuvatakse leht **Töö tükeldamine** ja kuvatakse avatud ja tükeldamiseks saadaolevad tööread.</span><span class="sxs-lookup"><span data-stu-id="93cf1-155">The **Split work** page appears and shows the work lines that are open and available to be split.</span></span> <span data-ttu-id="93cf1-156">Vaikimisi kuvatakse ainult saadaolevad tööread.</span><span class="sxs-lookup"><span data-stu-id="93cf1-156">By default, only available work lines are shown.</span></span> <span data-ttu-id="93cf1-157">Töö ID kõigi ridade vaatamiseks (näiteks read, millel on töö tüüp *Komplekteeri*), märkige ruudustiku kohal olev **Näita kõiki ridu** märkeruut.</span><span class="sxs-lookup"><span data-stu-id="93cf1-157">To view all lines for the work ID (for example, lines that have a work type of *Put*), select the **Show all lines** check box above the grid.</span></span>

    <span data-ttu-id="93cf1-158">Kuvatakse järgmine teade: "kasutajad ei saa töö ridu töödelda seni, kuni lõpetate selle lehe tükeldamise ja sulgete."</span><span class="sxs-lookup"><span data-stu-id="93cf1-158">The following message is shown: "Users can't process lines of the work until you finish splitting and close this page."</span></span>

    <span data-ttu-id="93cf1-159">**Töö blokeerimise põhjuse** väli praeguse töö jaoks seatakse olekusse *Töö tükeldamine* ja töö blokeeritakse.</span><span class="sxs-lookup"><span data-stu-id="93cf1-159">The **Work blocking reason** field for the current work will be set to *Split work*, and the work will be blocked.</span></span>

    <span data-ttu-id="93cf1-160">![Blokeerimise põhjus](media/Blocking_reason.png "Blokeerimise põhjus")</span><span class="sxs-lookup"><span data-stu-id="93cf1-160">![Blocking reason](media/Blocking_reason.png "Blocking reason")</span></span>

1. <span data-ttu-id="93cf1-161">Valige praeguse töö ID-lt eemaldatav rida ja lisage uus töö ID.</span><span class="sxs-lookup"><span data-stu-id="93cf1-161">Select the lines to remove from the current work ID and add to a new work ID.</span></span> <span data-ttu-id="93cf1-162">Toimub järgmine:</span><span class="sxs-lookup"><span data-stu-id="93cf1-162">The following events occur:</span></span>

    - <span data-ttu-id="93cf1-163">Kui tükeldate töö, tühistatakse valitud rida või read algsest töö ID-lt ja kopeeritakse seejärel uuele töö ID-le.</span><span class="sxs-lookup"><span data-stu-id="93cf1-163">When you split the work, the selected line or lines from the original work ID are canceled and then copied to a new work ID.</span></span>
    - <span data-ttu-id="93cf1-164">Säilitatakse olemasoleva töömalli struktuur ja pannakse (ja ka tulevaste komplekteerimise/komplekteerimispaari) asukoht.</span><span class="sxs-lookup"><span data-stu-id="93cf1-164">The existing work template structure and the location of the put (and also future pick/put pairs) are preserved.</span></span> <span data-ttu-id="93cf1-165">Järgmise töö ID väljade väärtused kopeeritakse algsest tööst uuele tööle:</span><span class="sxs-lookup"><span data-stu-id="93cf1-165">Values for the following work ID fields are copied from the original work to the new work:</span></span>

        - <span data-ttu-id="93cf1-166">Koorma ID</span><span class="sxs-lookup"><span data-stu-id="93cf1-166">Load ID</span></span>
        - <span data-ttu-id="93cf1-167">Saadetise ID</span><span class="sxs-lookup"><span data-stu-id="93cf1-167">Shipment ID</span></span>
        - <span data-ttu-id="93cf1-168">Töötellimuse tüüp</span><span class="sxs-lookup"><span data-stu-id="93cf1-168">Work order type</span></span>
        - <span data-ttu-id="93cf1-169">Tellimuse kood</span><span class="sxs-lookup"><span data-stu-id="93cf1-169">Order number</span></span>
        - <span data-ttu-id="93cf1-170">Laoala</span><span class="sxs-lookup"><span data-stu-id="93cf1-170">Site</span></span>
        - <span data-ttu-id="93cf1-171">Ladu</span><span class="sxs-lookup"><span data-stu-id="93cf1-171">Warehouse</span></span>
        - <span data-ttu-id="93cf1-172">Töö prioriteet</span><span class="sxs-lookup"><span data-stu-id="93cf1-172">Work priority</span></span>
        - <span data-ttu-id="93cf1-173">Töökausta ID</span><span class="sxs-lookup"><span data-stu-id="93cf1-173">Work pool ID</span></span>
        - <span data-ttu-id="93cf1-174">Voo ID</span><span class="sxs-lookup"><span data-stu-id="93cf1-174">Wave ID</span></span>
        - <span data-ttu-id="93cf1-175">Töö loomise number</span><span class="sxs-lookup"><span data-stu-id="93cf1-175">Work creation number</span></span>

    - <span data-ttu-id="93cf1-176">Järgmisi välju ei kopeerita uuele töö ID-le:</span><span class="sxs-lookup"><span data-stu-id="93cf1-176">The following fields aren't copied to the new work ID:</span></span>

        - <span data-ttu-id="93cf1-177">**Töö ID** – Uus töö ID luuakse vastavast numbriseeriast.</span><span class="sxs-lookup"><span data-stu-id="93cf1-177">**Work ID** – A new work ID is generated from the appropriate number sequence.</span></span>
        - <span data-ttu-id="93cf1-178">**Töö olek** – Selle välja väärtuseks on seatud *Ava*.</span><span class="sxs-lookup"><span data-stu-id="93cf1-178">**Work status** – This field is set to *Open*.</span></span>
        - <span data-ttu-id="93cf1-179">**Lukustatud** – Selle välja väärtus on algselt tühi.</span><span class="sxs-lookup"><span data-stu-id="93cf1-179">**Locked by** – This field is initially set to blank.</span></span>
        - <span data-ttu-id="93cf1-180">**Sihtkoha identifitseerimisnumber** – Väli jäetakse tühjaks.</span><span class="sxs-lookup"><span data-stu-id="93cf1-180">**Target license plate ID** – This field is left blank.</span></span>
        - <span data-ttu-id="93cf1-181">**Loomise kuupäev ja kellaaeg** – See väli seatakse praegusele kuupäevale ja kellaajale.</span><span class="sxs-lookup"><span data-stu-id="93cf1-181">**Created date and time** – This field is set to the current date and time.</span></span>
        - <span data-ttu-id="93cf1-182">**Blokeeritud voog/külmutatud** – See väli arvutatakse ümber algse töö ID ja uue töö ID jaoks.</span><span class="sxs-lookup"><span data-stu-id="93cf1-182">**Blocked wave/frozen** – This field is recomputed for the original work ID and the new work ID.</span></span>

1. <span data-ttu-id="93cf1-183">Valige toimingupaanilt suvand **Töö tükeldamine**.</span><span class="sxs-lookup"><span data-stu-id="93cf1-183">On the Action Pane, select **Split work**.</span></span>

<span data-ttu-id="93cf1-184">Kui tööd tükeldatakse, kuvatakse järgmine teade: "Töötlemise toiming – Töö tükeldamine".</span><span class="sxs-lookup"><span data-stu-id="93cf1-184">While the work is being split, the following message is shown: "Processing operation - Split work".</span></span> <span data-ttu-id="93cf1-185">Kui see teade on nähtav, saate toimingu tühistada, kui valite sõnumiaknas **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="93cf1-185">While this message is visible, you can cancel the operation by selecting **Cancel** in the message box.</span></span>

<span data-ttu-id="93cf1-186">Kui märkeruut **Kuva kõik read** on tühjendatud, ei kuvata enam ruudustikus tükeldatud ja tühistatud rida.</span><span class="sxs-lookup"><span data-stu-id="93cf1-186">If the **Show all lines** check box is cleared, the line that was split off and canceled will no longer appear in the grid.</span></span> <span data-ttu-id="93cf1-187">Kui see ruut on märgitud, peaksite nägema, et selle rea **Töö oleku** välja väärtus on muudetud olekusse *Tühistatud*.</span><span class="sxs-lookup"><span data-stu-id="93cf1-187">If the check box is selected, you should see that the value of the **Work status** field for that line has changed to *Canceled*.</span></span>

<span data-ttu-id="93cf1-188">Kuvatakse järgmine teatis, mis näitab, et uus töö ID on loodud: "Töö \#\#\#\# on loodud algsest tööst lahutamise teel \#\#\#\#."</span><span class="sxs-lookup"><span data-stu-id="93cf1-188">The following notification is shown to indicate that the new work ID has been created: "Work \#\#\#\# has been created by splitting off from original work \#\#\#\#."</span></span>

<span data-ttu-id="93cf1-189">Muid tööridu algsest töö ID-st (nt *Asetamise* read) korrigeeritakse vastavalt vajadusele, et kajastada tühistatud töö ridu.</span><span class="sxs-lookup"><span data-stu-id="93cf1-189">Other work lines from the original work ID (such as *Put* lines) will be adjusted as required to reflect the lines of work that have been canceled.</span></span> <span data-ttu-id="93cf1-190">Näiteks kui algse töö ID, millel oli *Liigutamise* rida kogusele 15 ja *Komplekteerimise* rea kogumahuga 10, tühistatakse, siis on algse töö *Liigutamise* uus kogus on nüüd 5.</span><span class="sxs-lookup"><span data-stu-id="93cf1-190">For example, if the original work ID had a *Put* line for a quantity of 15, and *Pick* lines that have a total quantity of 10 were canceled, the new *Put* quantity on the original work ID will now be 5.</span></span>

<span data-ttu-id="93cf1-191">Uut tööd ei määrata kohe ühelegi kasutajale.</span><span class="sxs-lookup"><span data-stu-id="93cf1-191">The new work won't immediately be assigned to any user.</span></span> <span data-ttu-id="93cf1-192">Saate siiski vastavalt vajadusele määrata selle kasutajale kohe, kasutades lehe **Töö üksikasjade** lehe standardfunktsioone.</span><span class="sxs-lookup"><span data-stu-id="93cf1-192">However, you can assign it to a user now, as required, by using the standard functionality of the **Work details** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="93cf1-193">Saate tükeldada ainult töö ID-sid, mis sisaldavad kaht või enamat saadaolevat töörida.</span><span class="sxs-lookup"><span data-stu-id="93cf1-193">You can split only work IDs that contain two or more available work lines.</span></span> <span data-ttu-id="93cf1-194">Kui valite **Töö tükeldamine**, kui on ainult üks töörida, kuvatakse järgmine tõrketeade: "Vähemalt üks töörida peab jääma algsele tööle."</span><span class="sxs-lookup"><span data-stu-id="93cf1-194">If you select **Split work** when there is only one work line, you will receive the following error message: "At least one work line must remain on initial work."</span></span> <span data-ttu-id="93cf1-195">Sel juhul tükeldamist ei toimu.</span><span class="sxs-lookup"><span data-stu-id="93cf1-195">In this case, no splitting will occur.</span></span>

## <a name="finish-a-work-split"></a><span data-ttu-id="93cf1-196">Lõpeta töö tükeldamine</span><span class="sxs-lookup"><span data-stu-id="93cf1-196">Finish a work split</span></span>

<span data-ttu-id="93cf1-197">Töö tükeldamise lõpetamiseks tuleb eemaldada *Töö tükeldamise* blokeerimise põhjus.</span><span class="sxs-lookup"><span data-stu-id="93cf1-197">To finish splitting work, the *Split work* blocking reason must be removed.</span></span> <span data-ttu-id="93cf1-198">Selle sammu läbimiseks on kaks võimalust:</span><span class="sxs-lookup"><span data-stu-id="93cf1-198">There are two ways to complete this step:</span></span>

- <span data-ttu-id="93cf1-199">Kasutaja, kes tükeldab tööd saab **Töö tükeldamise** lehe sulgeda, klõpsates **Sulge** nuppu (**X**) ülemises parempoolses nurgas.</span><span class="sxs-lookup"><span data-stu-id="93cf1-199">The user who is splitting the work closes the **Split work** page by selecting the **Close** button (**X**) in the upper-right corner.</span></span> <span data-ttu-id="93cf1-200">Kui leht on suletud, eemaldatakse *Töö tükeldamise* blokeerimise põhjus.</span><span class="sxs-lookup"><span data-stu-id="93cf1-200">When the page is closed, the *Split Work* blocking reason will be removed.</span></span> <span data-ttu-id="93cf1-201">Selle töö *Blokeeritud* olek arvutatakse ümber ja kui selle töö jaoks ei ole järelejäänud blokeerimise põhjusi, siis on töö blokeerimata.</span><span class="sxs-lookup"><span data-stu-id="93cf1-201">The *Blocked* state of this work will be recomputed and, if there are no remaining blocking reasons for this work, the work will be unblocked.</span></span>
- <span data-ttu-id="93cf1-202">Iga kasutaja avab töö ID ja valib tegumiribalt **Tühista töö tükeldamise sessioon** nupu.</span><span class="sxs-lookup"><span data-stu-id="93cf1-202">Any user opens the work ID and selects the **Cancel work split session** button on the Action Pane.</span></span> <span data-ttu-id="93cf1-203">*Töö tükeldamise* blokeerimise põhjus eemaldatakse ja selle töö *Blokeeringu* olek arvutatakse ümber, nagu ka siis, kui **Töö tükeldamise** lehekülg on suletud.</span><span class="sxs-lookup"><span data-stu-id="93cf1-203">The *Split work* blocking reason will be removed, and the *Blocked* state of this work will be recomputed, just as when the **Split work** page is closed.</span></span>

<span data-ttu-id="93cf1-204">Pärast *Töö tükeldamise* blokeerimise põhjuse eemaldamist saab tööd mobiilsel seadmel käitada tingimusel, et Töö ID **Blokeeritud** olekuks on määratud *Ei*.</span><span class="sxs-lookup"><span data-stu-id="93cf1-204">After the *Split work* blocking reason is removed, the work can be run on the mobile device, provided that the **Blocked** state is set to *No* on the work ID.</span></span>

## <a name="user-blocking-on-the-warehouse-app"></a><span data-ttu-id="93cf1-205">Kasutaja blokeerimine lao rakenduses</span><span class="sxs-lookup"><span data-stu-id="93cf1-205">User blocking on the warehouse app</span></span>

<span data-ttu-id="93cf1-206">Kui proovite laorakenduses avada tükeldamise lehte töö ID-ga, mida teine kasutaja juba tükeldab, kuvatakse järgmine tõrketeade: "Töö ID \#\#\#\# on hetkel tükeldatud."</span><span class="sxs-lookup"><span data-stu-id="93cf1-206">If you try to use the warehouse app to run picking work against a work ID that is being split, you will receive the following error message: "The work with ID \#\#\#\# is currently being split."</span></span> <span data-ttu-id="93cf1-207">Kui kuvatakse järgneb sõnum, vajutage **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="93cf1-207">If you receive this message, select **Cancel**.</span></span> <span data-ttu-id="93cf1-208">Seejärel saate jätkata teiste tööde töötlemist.</span><span class="sxs-lookup"><span data-stu-id="93cf1-208">You can then continue to process other work.</span></span>

## <a name="other-blocked-operations"></a><span data-ttu-id="93cf1-209">Muud blokeeritud toimingud</span><span class="sxs-lookup"><span data-stu-id="93cf1-209">Other blocked operations</span></span>

<span data-ttu-id="93cf1-210">Toimingud, mis muudavad tööridu, töö laokandeid või täiendamise linke, mis on seotud tööga, mis on tükeldatud, nurjuvad ja kuvatakse järgmine tõrketeade: "Töö ID-ga \#\#\#\# on praegu tükeldatud."</span><span class="sxs-lookup"><span data-stu-id="93cf1-210">Any operations that modify work lines, work inventory transactions, or replenishment links that are related to work that is being split will fail, and the following error message will be shown: "The work with ID \#\#\#\# is currently being split."</span></span>
