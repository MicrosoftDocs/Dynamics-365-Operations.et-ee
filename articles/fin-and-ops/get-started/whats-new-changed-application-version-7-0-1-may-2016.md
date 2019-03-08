---
title: Mis on uut või mida on muudetud rakenduse Dynamics AX versioonis 7.0.1 (mai 2016)
description: Selles artiklis kirjeldatakse rakenduse Microsoft Dynamics AX versiooni 7.0.1 uusi või muutunud funktsioone. See versioon ilmus mais 2016 ja selle number on 7.0.1265.23014.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: c830952b5d9e4887a816b5ab66d0944bddf5b505
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "314505"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a><span data-ttu-id="14319-104">Mis on uut või mida on muudetud rakenduse Dynamics AX versioonis 7.0.1 (mai 2016)</span><span class="sxs-lookup"><span data-stu-id="14319-104">What's new or changed in Dynamics AX application version 7.0.1 (May 2016)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14319-105">Selles artiklis kirjeldatakse rakenduse Microsoft Dynamics AX versiooni 7.0.1 uusi või muutunud funktsioone.</span><span class="sxs-lookup"><span data-stu-id="14319-105">This article describes features that are either new or changed in Microsoft Dynamics AX application version 7.0.1.</span></span> <span data-ttu-id="14319-106">See versioon ilmus mais 2016 ja selle number on 7.0.1265.23014.</span><span class="sxs-lookup"><span data-stu-id="14319-106">This version was released in May 2016 and has a build number of 7.0.1265.23014.</span></span>

## <a name="electronic-reporting-er"></a><span data-ttu-id="14319-107">Elektrooniline aruandlus (ER)</span><span class="sxs-lookup"><span data-stu-id="14319-107">Electronic reporting (ER)</span></span>

| <span data-ttu-id="14319-108">Mida saate teha?</span><span class="sxs-lookup"><span data-stu-id="14319-108">What can you do?</span></span> | <span data-ttu-id="14319-109">Miks on see oluline?</span><span class="sxs-lookup"><span data-stu-id="14319-109">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="14319-110">Saate konfigureerida käitusaja dialoogiboksi elektroonilise aruandluse (ER) aruannete kujundamiseks, et kasutajad saaksid soovitud finantsdimensioone valida.</span><span class="sxs-lookup"><span data-stu-id="14319-110">Configure a run-time dialog box for designing Electronic reporting (ER) reports, so that users can select the financial dimensions that they want.</span></span> | <span data-ttu-id="14319-111">Käitusajal saab kasutaja ER-aruande käitamise dialoogiboksis valida mitu finantsdimensiooni.</span><span class="sxs-lookup"><span data-stu-id="14319-111">At run time, in the dialog box for running an ER report, users can select multiple financial dimensions.</span></span> <span data-ttu-id="14319-112">Valitud finantsdimensioonide üksikasjad kuvatakse koostatava elektroonilises dokumendis.</span><span class="sxs-lookup"><span data-stu-id="14319-112">The details of the selected financial dimensions will be displayed in the electronic document that is generated.</span></span> |
| <span data-ttu-id="14319-113">Saate konfigureerida ER-aruande koostamise ajal juurdepääsu mitmele finantsdimensioonile ühe vastenduse abil soovitud andmeallikaga.</span><span class="sxs-lookup"><span data-stu-id="14319-113">Configure access to multiple financial dimensions during the design of an ER report, via a single mapping to the desired data source.</span></span> | <span data-ttu-id="14319-114">Sama elektroonilise aruandluse aruande konfiguratsiooni saab kasutada, et luua elektroonilisi dokumente, mis esitavad kandeandmeid koos finantsdimensioonide üksikasjadega, hoolimata nende finantsdimensioonide arvust, mida valib kasutaja või mis on konfigureeritud praeguse juriidilise isiku või eksemplari jaoks.</span><span class="sxs-lookup"><span data-stu-id="14319-114">The same ER report configuration can be used to generate electronic documents that present transactional data together with details of financial dimensions, regardless of the number of financial dimensions that are either selected by the user or configured for the current legal entity or instance.</span></span> |
| <span data-ttu-id="14319-115">Saate konfigureerida ER-i aruannet andmete sisestamiseks OPENXML-i töölehe vormingus loodud elektroonilise dokumendi dünaamiliselt loodud veergudesse.</span><span class="sxs-lookup"><span data-stu-id="14319-115">Configure an ER report to enter data in dynamically generated columns of an electronic document that is created in OPENXML worksheet format.</span></span> | <span data-ttu-id="14319-116">ER-aruanne saab sisestada andmeid OPENXML-töölehele, mis luuakse veergude horisontaalse paljundamise teel.</span><span class="sxs-lookup"><span data-stu-id="14319-116">An ER report can enter data in an OPENXML worksheet that is generated, via horizontally replicating columns.</span></span> <span data-ttu-id="14319-117">Seetõttu saab sama ER-aruande konfiguratsiooni uuesti kasutada, et koostada elektroonilisi dokumente, millel on erinev arv dünaamiliselt loodud veerge.</span><span class="sxs-lookup"><span data-stu-id="14319-117">Therefore, the same ER report configuration can be reused to generate electronic documents that have a different number of dynamically generated columns.</span></span> |
| <span data-ttu-id="14319-118">Saate konfigureerida elektroonilise aruandluse sihtkohti, nii et vormingu väljundtulemus on suunatud konkreetsele sihtkohale: fail, meil või arhiiv (Microsoft SharePointti kaust või Microsoft Azure’i salvestusruum).</span><span class="sxs-lookup"><span data-stu-id="14319-118">Configure ER destinations so that the output result of a format is directed to specific destination: file, email, or archive (Microsoft SharePoint folder or Microsoft Azure Storage).</span></span> | <span data-ttu-id="14319-119">Varem, kui käivitasite ER-konfiguratsiooni, kuvati teateväli, mis nõudis kasutaja tegevust faili salvestamiseks või avamiseks.</span><span class="sxs-lookup"><span data-stu-id="14319-119">Previously, when you ran an ER configuration, a message box appeared that required user action to save or open a file.</span></span> <span data-ttu-id="14319-120">Nüüd saate eelkonfigureerida sihtkoha igale vormingu konfiguratsioonile ja igale väljundi komponendile (kaust või fail) eraldi.</span><span class="sxs-lookup"><span data-stu-id="14319-120">You can now pre-configure a destination for each format configuration and for each output component (a folder or a file) separately.</span></span> <span data-ttu-id="14319-121">Kasutajad, kellel on sobilikud juurdepääsuõigused, võivad sihtkoha sätteid ka käitusajal muuta.</span><span class="sxs-lookup"><span data-stu-id="14319-121">Users who have appropriate access rights can also modify destination settings at run time.</span></span> |

## <a name="pos--microsoft-dynamics-ax-retail"></a><span data-ttu-id="14319-122">Kassa – Microsoft Dynamics AX Retail</span><span class="sxs-lookup"><span data-stu-id="14319-122">POS – Microsoft Dynamics AX Retail</span></span>

| <span data-ttu-id="14319-123">Mida saate teha?</span><span class="sxs-lookup"><span data-stu-id="14319-123">What can you do?</span></span> | <span data-ttu-id="14319-124">Miks on see oluline?</span><span class="sxs-lookup"><span data-stu-id="14319-124">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="14319-125">Kasutage Google Chrome’i brauserit.</span><span class="sxs-lookup"><span data-stu-id="14319-125">Use the Google Chrome browser.</span></span> | <span data-ttu-id="14319-126">Jaemüüjad saavad nüüd käivitada pilvekassa Chrome’i brauserist ja kasutada kõiki funktsioone, mis on saadaval pilvekassa Microsoft Edge’i ja Internet Exploreri versioonis.</span><span class="sxs-lookup"><span data-stu-id="14319-126">Retailers can now start Cloud POS from the Chrome browser, and can experience all the functionality that is available in the Microsoft Edge and Internet Explorer version of Cloud POS.</span></span> |

## <a name="financial-reporting"></a><span data-ttu-id="14319-127">Finantsaruandlus</span><span class="sxs-lookup"><span data-stu-id="14319-127">Financial reporting</span></span>

| <span data-ttu-id="14319-128">Mida saate teha?</span><span class="sxs-lookup"><span data-stu-id="14319-128">What can you do?</span></span> | <span data-ttu-id="14319-129">Miks on see oluline?</span><span class="sxs-lookup"><span data-stu-id="14319-129">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="14319-130">Saate koostada uuesti finantsaruandluse andmevaka.</span><span class="sxs-lookup"><span data-stu-id="14319-130">Rebuild the Financial reporting data mart.</span></span> | <span data-ttu-id="14319-131">Dynamics AX-i andmebaaside liigutamiseks keskkondade vahel või keskkonnale muude invasiivsete muudatuste tegemiseks tuleb finantsaruandluse andmebaasid uuesti luua.</span><span class="sxs-lookup"><span data-stu-id="14319-131">When you move Dynamics AX databases between environments or make other invasive changes to the environment, the Financial reporting database might have to be rebuilt.</span></span> <span data-ttu-id="14319-132">Nüüd on olemas Windows PowerShelli skript, mis loob andmebaasi teie eest.</span><span class="sxs-lookup"><span data-stu-id="14319-132">A Windows PowerShell script is now provided to rebuild the database for you.</span></span> |
| <span data-ttu-id="14319-133">Te ei saa enam valida kehtetuid aruandekoosturi valikuid.</span><span class="sxs-lookup"><span data-stu-id="14319-133">You can no longer select report designer options that aren't valid.</span></span> | <span data-ttu-id="14319-134">Mitu aruandekoosturi valikut, mida kasutati turul olevate Management Reporteri versioonides, ei kehti selle Dynamics AX-i versiooni puhul.</span><span class="sxs-lookup"><span data-stu-id="14319-134">Several report designer options that were used in the in-market versions of Management reporter don't apply to this version of Dynamics AX.</span></span> <span data-ttu-id="14319-135">Need suvandid olid seotud finantsaruande kujunduse, väljundi ja linkimisega.</span><span class="sxs-lookup"><span data-stu-id="14319-135">These options were related to financial report design, output, and linking.</span></span> <span data-ttu-id="14319-136">Need suvandid on kasutajatõrgete vältimiseks finantsaruande kujundajast eemaldatud.</span><span class="sxs-lookup"><span data-stu-id="14319-136">These options have been removed from the financial report designer to prevent user errors.</span></span> |

## <a name="financial-management"></a><span data-ttu-id="14319-137">Finantshaldus</span><span class="sxs-lookup"><span data-stu-id="14319-137">Financial management</span></span>

| <span data-ttu-id="14319-138">Mida saate teha?</span><span class="sxs-lookup"><span data-stu-id="14319-138">What can you do?</span></span> | <span data-ttu-id="14319-139">Miks on see oluline?</span><span class="sxs-lookup"><span data-stu-id="14319-139">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="14319-140">Saate luua ostureskontro maksete jaoks positiivseid maksefaile.</span><span class="sxs-lookup"><span data-stu-id="14319-140">Generate positive pay files for accounts payable payments.</span></span> | <span data-ttu-id="14319-141">Positiivseid maksefaile saab luua tšekipettuste vältimiseks.</span><span class="sxs-lookup"><span data-stu-id="14319-141">Positive pay files can be generated to help prevent check fraud.</span></span> |

## <a name="warehouse-and-production"></a><span data-ttu-id="14319-142">Ladu ja tootmine</span><span class="sxs-lookup"><span data-stu-id="14319-142">Warehouse and production</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="14319-143">Mida saate teha?</span><span class="sxs-lookup"><span data-stu-id="14319-143">What can you do?</span></span></th>
<th><span data-ttu-id="14319-144">Miks on see oluline?</span><span class="sxs-lookup"><span data-stu-id="14319-144">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14319-145">Määratlege lao tööpoliitika, mis juhib töö loomist toodete kogumile konkreetsetes asukohtades.</span><span class="sxs-lookup"><span data-stu-id="14319-145">Define a warehouse work policy that controls the creation of work for a set of products at specific locations.</span></span></td>
<td><span data-ttu-id="14319-146">Laoprotsessid ei hõlma alati tööd.</span><span class="sxs-lookup"><span data-stu-id="14319-146">Warehouse processes don't always include work.</span></span> <span data-ttu-id="14319-147">Uut lao tööpoliitikat kasutades saate vältida töö loomist toormaterjali komplekteerimise puhul ja lõpetatud kaupade ladustamist toodete kogumi puhul kindlates asukohtades.</span><span class="sxs-lookup"><span data-stu-id="14319-147">By using the new warehouse work policy, you can prevent work from being created for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14319-148">Määrake, et tootmise väljundi asukoht pole litsentsiplaadiga juhitud.</span><span class="sxs-lookup"><span data-stu-id="14319-148">Specify that a production output location isn't license plate–controlled.</span></span></td>
<td><span data-ttu-id="14319-149">Saate nüüd määrata, et toote väljundi asukoht pole litsentsiplaadiga juhitud.</span><span class="sxs-lookup"><span data-stu-id="14319-149">You can now specify that a product output location isn't license plate–controlled.</span></span> <span data-ttu-id="14319-150">Näiteks on see funktsioon kasulik, kui ülesvoolu tootmistellimus registreerib kaupade valmisoleku otse asukohas, mis toimib allavoolu tootmistellimuse tootmise sisendkohana.</span><span class="sxs-lookup"><span data-stu-id="14319-150">For example, this feature is useful when an upstream production order reports items as finished directly to a location that acts as production input location for a downstream production order.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14319-151">Saate toetada kooslusi, mis sisaldavad kaupu, millel on sama kauba erinevad tootedimensioonid.</span><span class="sxs-lookup"><span data-stu-id="14319-151">Support BOMs that include items with different product dimensions of the same item.</span></span></td>
<td><span data-ttu-id="14319-152">Kui kasutate tootmises ühte või mitut tootedimensiooni, võib teil olla olukordi, kus soovite toota kauba sama kauba teistsuguse variandi põhjal.</span><span class="sxs-lookup"><span data-stu-id="14319-152">When using one or multiple of the product dimensions in production, you can have situations where you would like to produce an item, based on a different variant of the same item.</span></span> <span data-ttu-id="14319-153">Lisateavet leiate <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">sellest ajaveebist</a>.</span><span class="sxs-lookup"><span data-stu-id="14319-153">For more information, see <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">this blog</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14319-154">Ümmarguse struktuuriga tootmistellimused nende koosluste esimesel tasemel jäetakse materjali ressursiplaanimise koosluse tasandi arvutusest välja.</span><span class="sxs-lookup"><span data-stu-id="14319-154">Production orders with circular structures at the first level of their BOMs are excluded from BOM level calculation for material resource planning.</span></span></td>
<td><span data-ttu-id="14319-155">Pole võimalik määrata õigeid koosluse tasemeid tootevariantidele selliste tootmistellimuste puhul, mis põhjustavad koosluse hierarhias ringviiteid.</span><span class="sxs-lookup"><span data-stu-id="14319-155">It is not possible to assign correct BOM levels to product variants for production orders that cause circularity in the BOM hierarchy.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14319-156">Saate arvutada eraldi koosluse tasemeid materjali ressursiplaanimise ja kuluarvutuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="14319-156">Calculate separate BOM levels for material resource planning and cost calculation:</span></span>
<ul>
<li><span data-ttu-id="14319-157">Materjali ressursiplaanimiseks arvutatakse koosluse tasemed uues tabelis <strong>ReqItemLevel</strong>.</span><span class="sxs-lookup"><span data-stu-id="14319-157">For material resource planning, BOM levels are calculated in the new <strong>ReqItemLevel</strong> table.</span></span> <span data-ttu-id="14319-158">Lõpetatud tootmistellimusi ei arvestata arvutuses.</span><span class="sxs-lookup"><span data-stu-id="14319-158">Ended production orders are ignored in the calculation.</span></span></li>
<li><span data-ttu-id="14319-159">Tootmiskulu arvutamiseks arvutatakse koosluse tasemed tabelis <strong>InventTable</strong>.</span><span class="sxs-lookup"><span data-stu-id="14319-159">For production cost calculation, BOM levels are calculated in the <strong>InventTable</strong>.</span></span> <span data-ttu-id="14319-160">Lõpetatud tootmistellimusi arvestatakse arvutuses.</span><span class="sxs-lookup"><span data-stu-id="14319-160">Ended production orders are included in the calculation.</span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="14319-161">Materjali ressursiplaanimise käivitamisel (nt koondplaanimise plaani koostamisel ja jaotamisel) tuleb arvutada ümber ainult materjali ressursiplaanimiseks kasutatud koosluse tasemed.</span><span class="sxs-lookup"><span data-stu-id="14319-161">When running material resource planning, for example, master planning plan scheduling and explosion, only BOM levels used for material resource planning need to be recalculated.</span></span> <span data-ttu-id="14319-162">Teisisõnu: tootmise kuluarvutuse jaoks kasutatud koosluse tasemeid pole vaja arvutada.</span><span class="sxs-lookup"><span data-stu-id="14319-162">In other words, there is no need to calculate BOM levels used for production costing calculation.</span></span></li>
<li><span data-ttu-id="14319-163">Kui kasutatakse kuluarvutuse toiminguid (nt lao sulgemist), tuleb arvutada ümber ainult tootmise kuluarvutuse jaoks kasutatud koosluse tasemed.</span><span class="sxs-lookup"><span data-stu-id="14319-163">When running costing operations, for example, inventory closing, only BOM levels used for production costing calculation need to be recalculated.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="14319-164">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="14319-164">Additional resources</span></span>

[<span data-ttu-id="14319-165">Mis on uus või muudetud?</span><span class="sxs-lookup"><span data-stu-id="14319-165">What's new or changed</span></span>](whats-new-changed.md)

[<span data-ttu-id="14319-166">Uued või värskendatud ülesande juhised (mai 2016)</span><span class="sxs-lookup"><span data-stu-id="14319-166">New or updated task guides (May 2016)</span></span>](new-updated-task-guides-available-may-2016.md)
