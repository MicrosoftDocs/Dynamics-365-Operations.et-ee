---
title: Komisjonitasude jälgimine kassas müügigruppide abil
description: Jaekaubanduses on tavapärane müügi jälgimine kliendiga töötanud müüja järgi, kes osutab abi, teeb lisa- ja ristmüüki ning töötleb kannet.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7e4820fa02ce66198e1f363ae46f944e3f24146c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243861"
---
# <a name="track-commissions-in-the-point-of-sale-pos-by-using-sales-groups"></a><span data-ttu-id="562fd-103">Komisjonitasude jälgimine kassas müügigruppide abil</span><span class="sxs-lookup"><span data-stu-id="562fd-103">Track commissions in the point of sale (POS) by using sales groups</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="562fd-104">Jaekaubanduses on tavapärane müügi jälgimine kliendiga töötanud müüja järgi, kes osutab abi, teeb lisa- ja ristmüüki ning töötleb kannet.</span><span class="sxs-lookup"><span data-stu-id="562fd-104">It's a common retail practice to track sales by the associate who worked with the customer by—providing assistance, up-selling, cross-selling, and processing the transaction.</span></span>

<span data-ttu-id="562fd-105">Müügi jälgimine müügiesindaja järgi mõõdab müüja müügivõimeid, samas kui müügi mõõtmine kassapidaja järgi mõõdab tema kiirust ja tõhusust.</span><span class="sxs-lookup"><span data-stu-id="562fd-105">Tracking sales by sales representative is a measure of the associates selling abilities, while sales by cashier is a measure of speed and efficiency.</span></span> <span data-ttu-id="562fd-106">Müügiesindaja järgi jälgitavat müüki kasutatakse samuti sageli komisjonitasude või muude lisatasude arvestamiseks.</span><span class="sxs-lookup"><span data-stu-id="562fd-106">Sales tracked by sales representative are also often used to calculate commissions or other incentives.</span></span>

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a><span data-ttu-id="562fd-107">Töötaja müügiesindajaks konfigureerimine kassas</span><span class="sxs-lookup"><span data-stu-id="562fd-107">Configuring a worker to be a sales representative in POS</span></span>

<span data-ttu-id="562fd-108">Kui töötaja lisatakse müügigruppi, tekib tal õigus komisjonitasule ja ta saab süsteemis müügiesindajaks märkida.</span><span class="sxs-lookup"><span data-stu-id="562fd-108">When a worker is added to a sales group, they become eligible for commission and can be identified as a sales representative in the system.</span></span> <span data-ttu-id="562fd-109">Töötajal, kes müügigruppi ei kuulu, puudub komisjonitasu saamise õigus ja teda ei registreerita kassarakenduses müügiesindajaks.</span><span class="sxs-lookup"><span data-stu-id="562fd-109">A worker who isn't in a sales group isn't eligible for commission and won't be listed as a sales representative in the point of sale (POS) application.</span></span> <span data-ttu-id="562fd-110">Kassas tuletatakse müügiesindajate nimekiri kõigist müügigruppidest, mis sisaldavad vähemalt ühte kauplusele määratud töötajat.</span><span class="sxs-lookup"><span data-stu-id="562fd-110">In POS, the list of sales representatives is derived from all sales groups that contain at least one worker assigned to the store.</span></span> <span data-ttu-id="562fd-111">Loend kuvatakse kassas müügigrupi ID ja nime kombinatsioonina (ID : Nimi).</span><span class="sxs-lookup"><span data-stu-id="562fd-111">The list is shown in POS as a combination of Sales group ID and Name (ID : Name).</span></span> <span data-ttu-id="562fd-112">Vaike-müügigrupi saab määrata töötajatele selliste stsenaariumide toetuseks, kus jaemüüja otsustab määrata müügiesindaja kassaridadele automaatselt.</span><span class="sxs-lookup"><span data-stu-id="562fd-112">A default sales group can be assigned to workers to support scenarios where the retailer chooses to set the sales representative on POS lines automatically.</span></span> <span data-ttu-id="562fd-113">Kasutajad saavad valida mis tahes müügigruppidest, mille liige töötaja on.</span><span class="sxs-lookup"><span data-stu-id="562fd-113">Users can select from any sales group that the worker is a member of.</span></span>

## <a name="functionality-profile-settings"></a><span data-ttu-id="562fd-114">Funktsiooniprofiilide seaded</span><span class="sxs-lookup"><span data-stu-id="562fd-114">Functionality profile settings</span></span>

<span data-ttu-id="562fd-115">Kauplusel on mitmesuguseid funktsiooniprofiili sätteid, mis määravad kassas müügiesindajaid hõlmava voo ja protsessi.</span><span class="sxs-lookup"><span data-stu-id="562fd-115">There are a number of functionality profile settings for a store that will determine the flow and process in POS that involve sales representatives.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="562fd-116">Reeglid</span><span class="sxs-lookup"><span data-stu-id="562fd-116">Profile</span></span></th>
<th><span data-ttu-id="562fd-117">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="562fd-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="562fd-118">Vaikimisi kassapidaja, kui võimalik</span><span class="sxs-lookup"><span data-stu-id="562fd-118">Default to cashier when available</span></span></td>
<td><span data-ttu-id="562fd-119">Kui see valik on lubatud, täidab kassa automaatselt kande read praeguse kassapidaja vaike-müügigrupiga.</span><span class="sxs-lookup"><span data-stu-id="562fd-119">If this option is enabled, POS will automatically populate transaction lines with the current cashier's default sales group.</span></span> <span data-ttu-id="562fd-120">Kui kassapidajale pole vaike-müügigruppi määratud, siis väärtust ei määrata.</span><span class="sxs-lookup"><span data-stu-id="562fd-120">If a cashier doesn't have a default sales group specified, the value won't be set.</span></span> <span data-ttu-id="562fd-121">Kasutaja saab müügigrupi siiski käsitsi määrata, kasutades kassa nupupaneeli nuppu.</span><span class="sxs-lookup"><span data-stu-id="562fd-121">A user could still manually set the sales group by using a POS button grid button.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="562fd-122">Müügiesindaja määramine</span><span class="sxs-lookup"><span data-stu-id="562fd-122">Prompt for sales representative</span></span></td>
<td><span data-ttu-id="562fd-123">Sellel valikul on kolm võimalikku väärtust:</span><span class="sxs-lookup"><span data-stu-id="562fd-123">This option has three possible values:</span></span>
<ul>
<li><span data-ttu-id="562fd-124"><strong>Ei</strong> - selle valiku korral ei paluta kasutajal müügigruppi valida.</span><span class="sxs-lookup"><span data-stu-id="562fd-124"><strong>No</strong> – If this option is selected, the user won't be prompted to select a sales group.</span></span> <span data-ttu-id="562fd-125">Väärtuse saab siiski määrata, kasutades kassapidaja vaike-müügigruppi, või käsitsi, kasutades kassa nupupaneeli nuppu.</span><span class="sxs-lookup"><span data-stu-id="562fd-125">The value could still be set by using a cashier's default Sales group or manually by using a POS button grid button.</span></span></li>
<li><span data-ttu-id="562fd-126"><strong>Kande algus</strong> – selle valiku korral, kui valikut <strong>Vaikimisi kassapidaja</strong> pole lubatud või praegusel kassapidajal pole vaike-müügigruppi, palutakse kasutajal valida müügigrupp iga kande alguses.</span><span class="sxs-lookup"><span data-stu-id="562fd-126"><strong>Start of transaction</strong> – If this option is selected, and either the <strong>Default to cashier</strong> option isn't enabled or the current cashier doesn't have a default sales group, the user will be prompted to select a sales group at the beginning of each transaction.</span></span> <span data-ttu-id="562fd-127">Müügigrupi valimisel sellest viibast lähtestatakse kõik järgnevad read valitud müügigrupiks.</span><span class="sxs-lookup"><span data-stu-id="562fd-127">Selecting a sales group from this prompt will default all subsequent lines to the selected sales group.</span></span> <span data-ttu-id="562fd-128">Kasutaja saab müügigrupi siiski käsitsi määrata, kasutades kassa nupupaneeli nuppu.</span><span class="sxs-lookup"><span data-stu-id="562fd-128">A user could still manually set the sales group by using a POS button grid button.</span></span></li>
<li><span data-ttu-id="562fd-129"><strong>Iga rea puhul</strong> – selle valiku korral, kui valikut <strong>Vaikimisi kassapidaja</strong> pole lubatud või praegusel kassapidajal pole vaike-müügigruppi, palutakse kasutajal valida müügigrupp pärast iga rea lisamist.</span><span class="sxs-lookup"><span data-stu-id="562fd-129"><strong>For each line</strong> – If this option is selected, and either the <strong>Default to cashier</strong> option isn't enabled or the current cashier doesn't have a default sales group, the user will be prompted to select a sales group after adding each line.</span></span> <span data-ttu-id="562fd-130">Kasutaja saab müügigrupi siiski käsitsi määrata, kasutades kassa nupupaneeli nuppu.</span><span class="sxs-lookup"><span data-stu-id="562fd-130">A user could still manually set the Sales group by using a POS button grid button.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="562fd-131">Nõua</span><span class="sxs-lookup"><span data-stu-id="562fd-131">Require</span></span></td>
<td><span data-ttu-id="562fd-132">See valik kehtib ainult siis, kui kassa on konfigureeritud müügiesindajat küsima.</span><span class="sxs-lookup"><span data-stu-id="562fd-132">This option is only applicable when POS is configured to prompt for a sales representative.</span></span> <span data-ttu-id="562fd-133">Kui see on lubatud, siis nõutakse, et kasutaja valiks enne jätkamist müügigrupi.</span><span class="sxs-lookup"><span data-stu-id="562fd-133">If enabled, the user will be required to choose a sales group before continuing.</span></span> <span data-ttu-id="562fd-134">Muidu kuvatakse kasutajale viip, kuid ta võib tühistada ja jätkata valikut tegemata.</span><span class="sxs-lookup"><span data-stu-id="562fd-134">Otherwise, the user will be prompted, but can cancel and continue without making a selection.</span></span> <span data-ttu-id="562fd-135">Pärast rea lisamist saab piisavate õigustega kasutaja siiski müügigrupi realt eemaldada.</span><span class="sxs-lookup"><span data-stu-id="562fd-135">After the line is added, a user with sufficient permissions could still remove the sales group from the line.</span></span> <span data-ttu-id="562fd-136">Selles olukorras ei rakendata valikut „Nõua müügiesindajat”.</span><span class="sxs-lookup"><span data-stu-id="562fd-136">"Require sales representative" is not enforced in this situation.</span></span></td>
</tr>
</tbody>
</table>

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a><span data-ttu-id="562fd-137">Müügiesindaja andmete kuvamine kassa kannete ekraanil</span><span class="sxs-lookup"><span data-stu-id="562fd-137">Displaying the Sales representative information on the POS transactions screen</span></span>

<span data-ttu-id="562fd-138">Kassa kannete ekraani paigutust ja sisu saab konfigureerida, kasutades ekraanipaigutuse kujundajat ja kauplustele, registritele või töötajatele määratud ekraanipaigutusi.</span><span class="sxs-lookup"><span data-stu-id="562fd-138">The POS transaction screen layout and contents are configurable using the screen layout designer and assigned screen layouts to stores, registers, or workers.</span></span> <span data-ttu-id="562fd-139">Välja **Müügiesindaja** saab lisada vahekaardile Read paanil Sissetulek.</span><span class="sxs-lookup"><span data-stu-id="562fd-139">The **Sales representative** field can be added to the Lines tab of the Receipt pane.</span></span>  <span data-ttu-id="562fd-140">Siis kuvatakse iga kande ekraani rea puhul määratud müügigrupi ID.</span><span class="sxs-lookup"><span data-stu-id="562fd-140">This will display the ID of the specified Sales group for each line on the transaction screen.</span></span>

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a><span data-ttu-id="562fd-141">Müügiesindaja toimingute lisamine kassa nupupaneelidele</span><span class="sxs-lookup"><span data-stu-id="562fd-141">Adding Sales representative operations to POS button grids</span></span>

<span data-ttu-id="562fd-142">Kassa võimaldab kasutajatel konfigureerida ekraanipaigutustes sisalduvaid nupupaneele juurdepääsu andmiseks kassatoimingutele.</span><span class="sxs-lookup"><span data-stu-id="562fd-142">POS allows users to configure button grids, which are included in screen layouts to provide access to POS operations.</span></span> <span data-ttu-id="562fd-143">Nupupaneeli nuppudele saab lisada järgmisi müügiesindajaid puudutavaid kassatoiminguid.</span><span class="sxs-lookup"><span data-stu-id="562fd-143">The following POS operations can be assigned to button grid buttons that pertain to Sales representatives.</span></span>

| <span data-ttu-id="562fd-144">Toiming</span><span class="sxs-lookup"><span data-stu-id="562fd-144">Operation</span></span>                                 | <span data-ttu-id="562fd-145">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="562fd-145">Description</span></span> |
|-------------------------------------------|-------------|
| <span data-ttu-id="562fd-146">Määra reale müügiesindaja</span><span class="sxs-lookup"><span data-stu-id="562fd-146">Set sales representative on line</span></span>          | <span data-ttu-id="562fd-147">See kassatoiming kuvab loendi vastavatest kaupluse müügigruppidest (ID : Nimi).</span><span class="sxs-lookup"><span data-stu-id="562fd-147">This POS operation displays a list of eligible Sales groups (ID : Name) for the store.</span></span> <span data-ttu-id="562fd-148">Müügigrupi valimisel sellest loendist määratakse praegusel kande real väärtus.</span><span class="sxs-lookup"><span data-stu-id="562fd-148">Selecting a Sales group from this list will set the value on the current transaction line.</span></span> |
| <span data-ttu-id="562fd-149">Tühjenda realt müügiesindaja</span><span class="sxs-lookup"><span data-stu-id="562fd-149">Clear sales representative on line</span></span>        | <span data-ttu-id="562fd-150">See kassatoiming eemaldab praeguse müügigrupi väärtuse praeguselt kande realt.</span><span class="sxs-lookup"><span data-stu-id="562fd-150">This POS operation removes the current Sales group value from the current transaction line.</span></span> |
| <span data-ttu-id="562fd-151">Kande müügiesindaja määramine</span><span class="sxs-lookup"><span data-stu-id="562fd-151">Set sales representative on transaction</span></span>   | <span data-ttu-id="562fd-152">See kassatoiming kuvab loendi vastavatest kaupluse müügigruppidest (ID : Nimi).</span><span class="sxs-lookup"><span data-stu-id="562fd-152">This POS operation displays a list of eligible Sales groups (ID : Name) for the store.</span></span> <span data-ttu-id="562fd-153">Müügigrupi valimisel sellest loendist määratakse praeguse kande vaikeväärtus.</span><span class="sxs-lookup"><span data-stu-id="562fd-153">Selecting a Sales group from this list will set the default value on the current transaction.</span></span> <span data-ttu-id="562fd-154">Määratakse mis tahes olemasolevad read ilma määratud müügigrupita ning kõik hiljem lisatud read.</span><span class="sxs-lookup"><span data-stu-id="562fd-154">Any existing lines without a sales group assigned will be set, as well as any subsequently added lines.</span></span> |
| <span data-ttu-id="562fd-155">Kandest müügiesindaja kustutamine</span><span class="sxs-lookup"><span data-stu-id="562fd-155">Clear sales representative on transaction</span></span> | <span data-ttu-id="562fd-156">See kassatoiming eemaldab praeguse vaike-müügigrupi väärtuse praeguselt kandelt.</span><span class="sxs-lookup"><span data-stu-id="562fd-156">This POS operation removes the current default Sales group value from the current transaction.</span></span> <span data-ttu-id="562fd-157">See ei mõjuta kandes juba olemasolevaid ridu.</span><span class="sxs-lookup"><span data-stu-id="562fd-157">It does not impact any lines already existing in the transaction.</span></span> |

## <a name="calculating-commissions"></a><span data-ttu-id="562fd-158">Komisjonitasu arvutamine</span><span class="sxs-lookup"><span data-stu-id="562fd-158">Calculating commissions</span></span>

<span data-ttu-id="562fd-159">Komisjonitasu arvutatakse määratud müügigruppide töötajatele väljavõtte või müügitellimuse sisestamise ajal.</span><span class="sxs-lookup"><span data-stu-id="562fd-159">Commission is calculated for the workers in the specified sales groups at the time of statement posting or sales order posting.</span></span> <span data-ttu-id="562fd-160">Komisjonitasu summa määratakse kliendi ja/või kande toodete puhul müügigrupis määratletud töötaja komisjonitasu osakaalu ja seotud komisjonitasu arvutamise sätete alusel.</span><span class="sxs-lookup"><span data-stu-id="562fd-160">The commission amount is determined based on the worker's commission share, as defined in the sales group and the associated commission calculation settings for the customer and/or products on the transaction.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]