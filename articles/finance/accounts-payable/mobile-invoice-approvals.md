---
title: Mobiilsed arvete heakskiidud
description: See teema on mõeldud praktilise lähenemise pakkumiseks mobiilistsenaariumide kujundamisele, võttes mobiilse hankija arvete kinnitamise kasutusnäiteks.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5d3b85e076292b9d41de6a4cf3198ed9b38d27c8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828030"
---
# <a name="mobile-invoice-approvals"></a><span data-ttu-id="dc33b-103">Mobiilsed arvete heakskiidud</span><span class="sxs-lookup"><span data-stu-id="dc33b-103">Mobile invoice approvals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc33b-104">Mobiilsed võimalused võimaldavad ärikasutajatel mobiilikogemusi kujundada.</span><span class="sxs-lookup"><span data-stu-id="dc33b-104">Mobile capabilities let a business user design mobile experiences.</span></span> <span data-ttu-id="dc33b-105">Täpsemate stsenaariumide puhul võimaldab platvorm arendajatel võimalusi oma soovi kohaselt laiendada.</span><span class="sxs-lookup"><span data-stu-id="dc33b-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="dc33b-106">Kõige tulemuslikum viis mõningaid neist uutest mobiilikontseptsioonidest tundma õppida on läbi mõne stsenaariumi kujundamise protsessis.</span><span class="sxs-lookup"><span data-stu-id="dc33b-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="dc33b-107">See teema on mõeldud praktilise lähenemise pakkumiseks mobiilistsenaariumide kujundamisele, võttes mobiilse hankija arvete kinnitamise kasutusnäiteks.</span><span class="sxs-lookup"><span data-stu-id="dc33b-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="dc33b-108">See teema aitab teil kujundada stsenaariumide muid variatsioone ja seda saab rakendada ka muudele stsenaariumidele, mis pole hankija arvetega seotud.</span><span class="sxs-lookup"><span data-stu-id="dc33b-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="dc33b-109">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="dc33b-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="dc33b-110">Eeltingimus</span><span class="sxs-lookup"><span data-stu-id="dc33b-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="dc33b-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="dc33b-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc33b-112">Mobiili käsiraamat eelnevaks lugemiseks</span><span class="sxs-lookup"><span data-stu-id="dc33b-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="dc33b-113">Mobiiliplatvorm</span><span class="sxs-lookup"><span data-stu-id="dc33b-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="dc33b-114">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="dc33b-114">Dynamics 365 Finance</span></span>                                                                              | <span data-ttu-id="dc33b-115">Keskkond, millesse on installitud versioon 1611 ja platvormivärskendus 3 (november 2016)</span><span class="sxs-lookup"><span data-stu-id="dc33b-115">An environment that has version 1611 and Platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="dc33b-116">Installige kiirparandus KB 3204341.</span><span class="sxs-lookup"><span data-stu-id="dc33b-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="dc33b-117">Tegevuse salvestaja võib kogemata salvestada rippdialoogidele kaks sulgemiskäsku platvormi värskenduses 3 (2016. aasta novembri värskendus).</span><span class="sxs-lookup"><span data-stu-id="dc33b-117">Task recorder can erroneously record two Close commands for dropdown dialogs; this is included in Platform update 3 (November 2016 update).</span></span> |
| <span data-ttu-id="dc33b-118">Installige kiirparandus KB 3207800.</span><span class="sxs-lookup"><span data-stu-id="dc33b-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="dc33b-119">See kiirparandus võimaldab vaadata manuseid mobiilikliendil, mis sisaldub platvormi värskenduses 3 (2016. aasta novembri värskendus).</span><span class="sxs-lookup"><span data-stu-id="dc33b-119">This hotfix enables attachments to be viewed on the mobile client; this is included in Platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="dc33b-120">Installige kiirparandus KB 3208224.</span><span class="sxs-lookup"><span data-stu-id="dc33b-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="dc33b-121">Rakenduse kood mobiilse hankija arve kinnitamise rakenduse jaoks, mis sisaldub versioonis 7.0.1 (mai 2016).</span><span class="sxs-lookup"><span data-stu-id="dc33b-121">Application code for the mobile vendor invoice approval application; this is included in version 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="dc33b-122">Androidi, iOS-i või Windowsi seade, millesse on installitud mobiilirakendus.</span><span class="sxs-lookup"><span data-stu-id="dc33b-122">An Android or iOS or a Windows device that has the mobile app installed.</span></span> | <span data-ttu-id="dc33b-123">Otsige rakendust vastavast rakenduste poest.</span><span class="sxs-lookup"><span data-stu-id="dc33b-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="dc33b-124">Sissejuhatus</span><span class="sxs-lookup"><span data-stu-id="dc33b-124">Introduction</span></span>
<span data-ttu-id="dc33b-125">Hankija arvete mobiilsed kinnitused nõuavad kolme kiirparandust, mis on nimetatud jaotises „Eeltingimused”.</span><span class="sxs-lookup"><span data-stu-id="dc33b-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="dc33b-126">Need kiirparandused ei paku tööruumi arvete kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="dc33b-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="dc33b-127">Seda, mis on mobiili kontekstis tööruum, saate lugeda jaotises „Eeltingimused” nimetatud mobiili käsiraamatust.</span><span class="sxs-lookup"><span data-stu-id="dc33b-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="dc33b-128">Arvete kinnitamise tööruum vajab kujundamist.</span><span class="sxs-lookup"><span data-stu-id="dc33b-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="dc33b-129">Iga organisatsioon korraldab ja määratleb hankija arvete äriprotsessi erinevalt.</span><span class="sxs-lookup"><span data-stu-id="dc33b-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="dc33b-130">Enne hankija arvete kinnituste jaoks mobiilikogemuse kujundamist tuleks arvestada järgimisi äriprotsessi aspekte.</span><span class="sxs-lookup"><span data-stu-id="dc33b-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="dc33b-131">Kasutajakogemuse optimeerimiseks seadmel tuleks neid andmepunkte kasutada võimalikult palju.</span><span class="sxs-lookup"><span data-stu-id="dc33b-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="dc33b-132">Milliseid arve päise välju soovib kasutaja mobiiliversioonis näha ja millises järjekorras?</span><span class="sxs-lookup"><span data-stu-id="dc33b-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="dc33b-133">Milliseid arve ridade välju soovib kasutaja mobiiliversioonis näha ja millises järjekorras?</span><span class="sxs-lookup"><span data-stu-id="dc33b-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="dc33b-134">Mitu arverida arvel on?</span><span class="sxs-lookup"><span data-stu-id="dc33b-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="dc33b-135">Rakendage siin 80-20 reeglit ja optimeerige 80 protsendi jaoks.</span><span class="sxs-lookup"><span data-stu-id="dc33b-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="dc33b-136">Kas kasutajad soovivad arvestuse jaotusi (arvekoode) ülevaatamise ajal mobiilsel seadmel näha?</span><span class="sxs-lookup"><span data-stu-id="dc33b-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="dc33b-137">Kui vastus sellele küsimusele on jah, siis kaaluge järgmisi küsimusi.</span><span class="sxs-lookup"><span data-stu-id="dc33b-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="dc33b-138">Kui palju arvestuse jaotusi (laiendatud hind, käibemaks, tasud, jagamised jne) arve real on?</span><span class="sxs-lookup"><span data-stu-id="dc33b-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="dc33b-139">Rakendage jällegi 80-20 reeglit.</span><span class="sxs-lookup"><span data-stu-id="dc33b-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="dc33b-140">Kas arvete päises on ka arvestuse jaotused?</span><span class="sxs-lookup"><span data-stu-id="dc33b-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="dc33b-141">Kui nii, siis kas need arvestuse jaotused peaksid seadmel kättesaadavad olema?</span><span class="sxs-lookup"><span data-stu-id="dc33b-141">If so, should these accounting distributions be available on the device?</span></span>

    > [!NOTE]
    > <span data-ttu-id="dc33b-142">Selles teemas ei selgitata, kuidas arvestuse jaotusi redigeerida, kuna seda funktsiooni ei toetata praegu mobiilistsenaariumide puhul.</span><span class="sxs-lookup"><span data-stu-id="dc33b-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="dc33b-143">Kas kasutajad soovivad seadmel arve manuseid näha?</span><span class="sxs-lookup"><span data-stu-id="dc33b-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="dc33b-144">Arvete kinnitamise mobiiliversioon on erinev, olenevalt nende küsimuste vastustest.</span><span class="sxs-lookup"><span data-stu-id="dc33b-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="dc33b-145">Eesmärk on optimeerida organisatsioonis kasutaja äriprotsessi kogemust mobiilil.</span><span class="sxs-lookup"><span data-stu-id="dc33b-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="dc33b-146">Ülejäänud teemas vaatame kahte stsenaariumivarianti, mis põhinevad erinevatel vastustel eelnevatele küsimustele.</span><span class="sxs-lookup"><span data-stu-id="dc33b-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="dc33b-147">Üldise juhisena veenduge mobiilikujundajaga töötamisel, et avaldaksite muudatused, et vältida nende kaotsiminekut.</span><span class="sxs-lookup"><span data-stu-id="dc33b-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="dc33b-148">Lihtsa arve kinnitamise stsenaariumi kujundamine Contoso jaoks</span><span class="sxs-lookup"><span data-stu-id="dc33b-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dc33b-149">Stsenaariumi atribuut</span><span class="sxs-lookup"><span data-stu-id="dc33b-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="dc33b-150">Vastus</span><span class="sxs-lookup"><span data-stu-id="dc33b-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc33b-151">Milliseid arve päise välju soovib kasutaja mobiiliversioonis näha ja millises järjekorras?</span><span class="sxs-lookup"><span data-stu-id="dc33b-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="dc33b-152">Hankija nimi</span><span class="sxs-lookup"><span data-stu-id="dc33b-152">Vendor name</span></span></li>
<li><span data-ttu-id="dc33b-153">Arve summa</span><span class="sxs-lookup"><span data-stu-id="dc33b-153">Invoice total</span></span></li>
<li><span data-ttu-id="dc33b-154">Maksja</span><span class="sxs-lookup"><span data-stu-id="dc33b-154">Invoice account</span></span></li>
<li><span data-ttu-id="dc33b-155">Arve number</span><span class="sxs-lookup"><span data-stu-id="dc33b-155">Invoice number</span></span></li>
<li><span data-ttu-id="dc33b-156">Arve kuupäev</span><span class="sxs-lookup"><span data-stu-id="dc33b-156">Invoice date</span></span></li>
<li><span data-ttu-id="dc33b-157">Arve kirjeldus</span><span class="sxs-lookup"><span data-stu-id="dc33b-157">Invoice description</span></span></li>
<li><span data-ttu-id="dc33b-158">Tähtaeg</span><span class="sxs-lookup"><span data-stu-id="dc33b-158">Due date</span></span></li>
<li><span data-ttu-id="dc33b-159">Arve valuuta</span><span class="sxs-lookup"><span data-stu-id="dc33b-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc33b-160">Milliseid arve ridade välju soovib kasutaja mobiiliversioonis näha ja millises järjekorras?</span><span class="sxs-lookup"><span data-stu-id="dc33b-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="dc33b-161">Hankekategooria</span><span class="sxs-lookup"><span data-stu-id="dc33b-161">Procurement category</span></span></li>
<li><span data-ttu-id="dc33b-162">Kogus</span><span class="sxs-lookup"><span data-stu-id="dc33b-162">Quantity</span></span></li>
<li><span data-ttu-id="dc33b-163">Ühiku hind</span><span class="sxs-lookup"><span data-stu-id="dc33b-163">Unit price</span></span></li>
<li><span data-ttu-id="dc33b-164">Rea netosumma</span><span class="sxs-lookup"><span data-stu-id="dc33b-164">Line net amount</span></span></li>
<li><span data-ttu-id="dc33b-165">1099-summa</span><span class="sxs-lookup"><span data-stu-id="dc33b-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc33b-166">Mitu arverida arvel on?</span><span class="sxs-lookup"><span data-stu-id="dc33b-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="dc33b-167">Rakendage siin 80-20 reeglit ja optimeerige 80 protsendi jaoks.</span><span class="sxs-lookup"><span data-stu-id="dc33b-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="dc33b-168">1</span><span class="sxs-lookup"><span data-stu-id="dc33b-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc33b-169">Kas kasutajad soovivad arvestuse jaotusi (arvekoode) ülevaatamise ajal mobiilsel seadmel näha?</span><span class="sxs-lookup"><span data-stu-id="dc33b-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="dc33b-170">Jah</span><span class="sxs-lookup"><span data-stu-id="dc33b-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc33b-171">Kui palju arvestuse jaotusi (laiendatud hind, käibemaks, tasud jne) arve real on?</span><span class="sxs-lookup"><span data-stu-id="dc33b-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="dc33b-172">Rakendage jällegi 80-20 reeglit.</span><span class="sxs-lookup"><span data-stu-id="dc33b-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="dc33b-173">Laiendatud hind: 2 Käibemaks: 0 Tasud: 0</span><span class="sxs-lookup"><span data-stu-id="dc33b-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc33b-174">Kas arvete päises on ka arvestuse jaotused?</span><span class="sxs-lookup"><span data-stu-id="dc33b-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="dc33b-175">Kui nii, siis kas need arvestuse jaotused peaksid seadmel kättesaadavad olema?</span><span class="sxs-lookup"><span data-stu-id="dc33b-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="dc33b-176">Pole kasutusel</span><span class="sxs-lookup"><span data-stu-id="dc33b-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc33b-177">Kas kasutajad soovivad seadmel arve manuseid näha?</span><span class="sxs-lookup"><span data-stu-id="dc33b-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="dc33b-178">Jah</span><span class="sxs-lookup"><span data-stu-id="dc33b-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="dc33b-179">Tööruumi loomine</span><span class="sxs-lookup"><span data-stu-id="dc33b-179">Create the workspace</span></span>

1.  <span data-ttu-id="dc33b-180">Avage brauser ja logige rakendusse sisse.</span><span class="sxs-lookup"><span data-stu-id="dc33b-180">In a browser, and sign in to the application.</span></span>
2.  <span data-ttu-id="dc33b-181">Kui olete sisse loginud, lisage URL-ile **&mode=mobile**, nagu on näidatud järgmises näites, ja värskendage lehte: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="dc33b-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span></span>
3.  <span data-ttu-id="dc33b-182">Klõpsake nuppu **Sätted** (hammasratas) lehe ülemises paremas osas ja seejärel valikut **Mobiilirakendus**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="dc33b-183">Mobiilirakenduse kujundaja peaks ilmuma samamoodi, nagu ilmub tegevuse salvestaja.</span><span class="sxs-lookup"><span data-stu-id="dc33b-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="dc33b-184">Klõpsake uue tööruumi loomiseks nuppu **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="dc33b-185">Selle näite puhul andke tööruumile nimi **Minu kinnitused**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="dc33b-186">Sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="dc33b-186">Enter a description.</span></span>
6.  <span data-ttu-id="dc33b-187">Valige tööruumi värv.</span><span class="sxs-lookup"><span data-stu-id="dc33b-187">Select a workspace color.</span></span> <span data-ttu-id="dc33b-188">Tööruumi värvi kasutatakse selle tööruumi üldise mobiiliversiooni stiili puhul.</span><span class="sxs-lookup"><span data-stu-id="dc33b-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="dc33b-189">Valige tööruumi ikoon.</span><span class="sxs-lookup"><span data-stu-id="dc33b-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="dc33b-190">Klõpsake nuppu **Valmis**</span><span class="sxs-lookup"><span data-stu-id="dc33b-190">Click **Done**</span></span>
9.  <span data-ttu-id="dc33b-191">Muudatuste salvestamiseks klõpsake nuppu **Avalda tööruum**</span><span class="sxs-lookup"><span data-stu-id="dc33b-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="dc33b-192">Mulle määratud hankijaarved</span><span class="sxs-lookup"><span data-stu-id="dc33b-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="dc33b-193">Esimene mobiilne leht, mis vajab kujundamist, on kasutajale ülevaatamiseks määratud arvete loend.</span><span class="sxs-lookup"><span data-stu-id="dc33b-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="dc33b-194">Selle mobiilse lehe kujundamiseks kasutage lehte **VendMobileInvoiceAssignedToMeListPage**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page.</span></span> <span data-ttu-id="dc33b-195">Enne selle protseduuri läbimist veenduge, et teile oleks ülevaatamiseks määratud vähemalt üks hankija arve ja et arve real oleks kaks jaotust.</span><span class="sxs-lookup"><span data-stu-id="dc33b-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="dc33b-196">See seadistus vastab selle stsenaariumi nõuetele.</span><span class="sxs-lookup"><span data-stu-id="dc33b-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="dc33b-197">Asendage URL-is menüüelemendi nimi stringiga **VendMobileInvoiceAssignedToMeListPage**, et avada loendilehe **Mulle määratud ootel hankija arved** mobiiliversioon moodulis **Ostureskontro**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-197">In the URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="dc33b-198">Olenevalt sellest, kui palju arveid on teile teie süsteemis määratud, kuvatakse sellel lehel need arved.</span><span class="sxs-lookup"><span data-stu-id="dc33b-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="dc33b-199">Konkreetse arve otsimiseks võib kasutada vasakul olevat filtrit.</span><span class="sxs-lookup"><span data-stu-id="dc33b-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="dc33b-200">Kuid selle näite puhul pole meil konkreetset arvet vaja.</span><span class="sxs-lookup"><span data-stu-id="dc33b-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="dc33b-201">Meil on lihtsalt vaja, et teile oleks määratud mõni arve, mis võimaldaks teil mobiilset lehte kujundada.</span><span class="sxs-lookup"><span data-stu-id="dc33b-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="dc33b-202">Uued saadaolevad lehed on kujundatud spetsiaalselt hankija arve mobiilistsenaariumide väljatöötamiseks.</span><span class="sxs-lookup"><span data-stu-id="dc33b-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="dc33b-203">Seega tuleb kasutada neid lehti.</span><span class="sxs-lookup"><span data-stu-id="dc33b-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="dc33b-204">URL peab sarnanema järgmisele URL-ile ja kui olete selle sisestanud, peab avanema joonisel näidatud leht: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span><span class="sxs-lookup"><span data-stu-id="dc33b-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span></span> 

    <span data-ttu-id="dc33b-205">Leht [![Mulle määratud hankija ootel arved](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="dc33b-205">[![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
    
2.  <span data-ttu-id="dc33b-206">Klõpsake nuppu **Sätted** (hammasratas) lehe ülemises paremas osas ja seejärel valikut **Mobiilirakendus**</span><span class="sxs-lookup"><span data-stu-id="dc33b-206">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="dc33b-207">Valige oma tööruum ja klõpsake nuppu **Redigeeri**</span><span class="sxs-lookup"><span data-stu-id="dc33b-207">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="dc33b-208">Klõpsake esimese mobiilse lehe loomiseks nuppu **Lisa leht**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-208">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="dc33b-209">Sisestage nimi nagu **Minu hankija arved** ja kirjeldus nagu **Mulle ülevaatamiseks määratud hankija arved**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-209">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="dc33b-210">Klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-210">Click **Done**.</span></span>
7.  <span data-ttu-id="dc33b-211">Klõpsake mobiilse kujundaja vahekaardil **Väljad** nuppu **Vali väljad**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-211">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="dc33b-212">Loendilehe veerud peavad sarnanema järgmisele illustratsioonile.</span><span class="sxs-lookup"><span data-stu-id="dc33b-212">The columns on the list page must resemble the following illustration.</span></span> 

    <span data-ttu-id="dc33b-213">[![Veerud lehel Mulle määratud ootel hankija arved](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="dc33b-213">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
    
8.  <span data-ttu-id="dc33b-214">Lisage vajalikud veerud loendilehelt, mis tuleb mobiililehel kasutajatele kuvada.</span><span class="sxs-lookup"><span data-stu-id="dc33b-214">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="dc33b-215">Väljad kuvatakse lõppkasutajatele lisamise järjekorras.</span><span class="sxs-lookup"><span data-stu-id="dc33b-215">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="dc33b-216">Ainus võimalus väljade järjestust muuta on kõik väljad uuesti valida.</span><span class="sxs-lookup"><span data-stu-id="dc33b-216">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="dc33b-217">Selle stsenaariumi nõuete põhjal on vaja järgmist kaheksat välja.</span><span class="sxs-lookup"><span data-stu-id="dc33b-217">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="dc33b-218">Kuid mõned kasutajad võivad leida, et kaheksa välja on mobiilsel seadmel liiga palju teavet.</span><span class="sxs-lookup"><span data-stu-id="dc33b-218">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="dc33b-219">Seega näitame mobiili loendivaates ainult kõige olulisemaid välju.</span><span class="sxs-lookup"><span data-stu-id="dc33b-219">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="dc33b-220">Ülejäänud väljad kuvatakse üksikasjavaates, mille kujundame hiljem.</span><span class="sxs-lookup"><span data-stu-id="dc33b-220">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="dc33b-221">Praegu lisame järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="dc33b-221">For now, we will add the following fields.</span></span> <span data-ttu-id="dc33b-222">Klõpsake plussmärki (**+**) nende veergude mobiililehele lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="dc33b-222">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="dc33b-223">Hankija nimi</span><span class="sxs-lookup"><span data-stu-id="dc33b-223">Vendor name</span></span>
    - <span data-ttu-id="dc33b-224">Arve summa</span><span class="sxs-lookup"><span data-stu-id="dc33b-224">Invoice total</span></span>
    - <span data-ttu-id="dc33b-225">Maksja</span><span class="sxs-lookup"><span data-stu-id="dc33b-225">Invoice account</span></span>
    - <span data-ttu-id="dc33b-226">Arve number</span><span class="sxs-lookup"><span data-stu-id="dc33b-226">Invoice number</span></span>
    - <span data-ttu-id="dc33b-227">Arve kuupäev</span><span class="sxs-lookup"><span data-stu-id="dc33b-227">Invoice date</span></span>

    <span data-ttu-id="dc33b-228">Pärast väljade lisamist peab mobiilileht sarnanema järgmisele illustratsioonile.</span><span class="sxs-lookup"><span data-stu-id="dc33b-228">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    
    <span data-ttu-id="dc33b-229">[![Leht pärast väljade lisamist](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="dc33b-229">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>

9.  <span data-ttu-id="dc33b-230">Nüüd tuleb lisada ka järgmised väljad, et hiljem saaks töövootoimingud lubada.</span><span class="sxs-lookup"><span data-stu-id="dc33b-230">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="dc33b-231">Kuva lõpetamise ülesanne</span><span class="sxs-lookup"><span data-stu-id="dc33b-231">Show complete task</span></span>
    - <span data-ttu-id="dc33b-232">Kuva delegeerimise ülesanne</span><span class="sxs-lookup"><span data-stu-id="dc33b-232">Show delegate task</span></span>
    - <span data-ttu-id="dc33b-233">Kuva tagasikutsumise ülesanne</span><span class="sxs-lookup"><span data-stu-id="dc33b-233">Show recall task</span></span>
    - <span data-ttu-id="dc33b-234">Kuva tagasilükkamise ülesanne</span><span class="sxs-lookup"><span data-stu-id="dc33b-234">Show reject task</span></span>
    - <span data-ttu-id="dc33b-235">Kuva taotluse täitmise ülesanne</span><span class="sxs-lookup"><span data-stu-id="dc33b-235">Show request completion task</span></span>
    - <span data-ttu-id="dc33b-236">Kuva uuesti esitamise ülesanne</span><span class="sxs-lookup"><span data-stu-id="dc33b-236">Show resubmit task</span></span>

10. <span data-ttu-id="dc33b-237">Redigeerimisrežiimist väljumiseks klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-237">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="dc33b-238">Klõpsake nuppu **Tagasi** ja seejärel nuppu **Valmis** tööruumist väljumiseks</span><span class="sxs-lookup"><span data-stu-id="dc33b-238">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="dc33b-239">Töö salvestamiseks klõpsake nuppu **Avalda tööruum**</span><span class="sxs-lookup"><span data-stu-id="dc33b-239">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="dc33b-240">Lubage ostureskontro vormi jaotises **Arve** valik **Kuva ootel hankija arvete loendis arve koondsumma**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-240">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="dc33b-241">Pange tähele, et arve koondsummad arvutatakse ootel hankija arvete loendilehel kuvamiseks ainult selle parameetri lubamisel.</span><span class="sxs-lookup"><span data-stu-id="dc33b-241">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="dc33b-242">See on uus võimalus, mis kuulub eeltingimuseks olevasse kiirparandusse 3208224.</span><span class="sxs-lookup"><span data-stu-id="dc33b-242">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="dc33b-243">Hankija arve andmed</span><span class="sxs-lookup"><span data-stu-id="dc33b-243">Vendor invoice details</span></span>

<span data-ttu-id="dc33b-244">Arve üksikasjade lehe kujundamiseks mobiiliversioonile kasutage lehte **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-244">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="dc33b-245">Pange tähele, et olenevalt sellest, kui palju arveid on teile teie süsteemis määratud, kuvatakse sellel lehel vanim arve (esimesena koostatud arve).</span><span class="sxs-lookup"><span data-stu-id="dc33b-245">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="dc33b-246">Konkreetse arve otsimiseks võib kasutada vasakul olevat filtrit.</span><span class="sxs-lookup"><span data-stu-id="dc33b-246">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="dc33b-247">Kuid selle näite puhul pole meil konkreetset arvet vaja.</span><span class="sxs-lookup"><span data-stu-id="dc33b-247">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="dc33b-248">Meil on lihtsalt vaja mõningaid arveandmeid, et saaksime mobiilset lehte kujundada.</span><span class="sxs-lookup"><span data-stu-id="dc33b-248">We just require some invoice data so that we can design the mobile page.</span></span> 

<span data-ttu-id="dc33b-249">[![Töövoo leht](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="dc33b-249">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1. <span data-ttu-id="dc33b-250">Asendage URL-is menüüelemendi nimi stringiga **VendMobileInvoiceHeaderDetails** vormi avamiseks</span><span class="sxs-lookup"><span data-stu-id="dc33b-250">In the URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>

2. <span data-ttu-id="dc33b-251">Avage mobiilne kujundaja nupult **Sätted** (hammasratas).</span><span class="sxs-lookup"><span data-stu-id="dc33b-251">Open the mobile designer from the **Settings** (gear) button.</span></span>

3. <span data-ttu-id="dc33b-252">Klõpsake tööruumis redigeerimisrežiimi käivitamiseks nuppu **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-252">Click the **Edit** button to start edit mode in the workspace.</span></span>

4. <span data-ttu-id="dc33b-253">Valige eelnevalt loodud leht **Minu hankija arved** ja klõpsake siis nuppu **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-253">Select the **My vendor invoices** page that you created earlier, and then click **Edit**.</span></span>

5. <span data-ttu-id="dc33b-254">Klõpsake vahekaardil **Väljad** veerupäist **Ruudustik**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-254">On the **Fields** tab, click the **Grid** column heading.</span></span>

6. <span data-ttu-id="dc33b-255">Klõpsake valikuid **Atribuudid &gt; Lisa leht**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-255">Click **Properties &gt; Add page**.</span></span> <span data-ttu-id="dc33b-256">**Märkus.** Kui klõpsate pealkirja **Ruudustik** ja lisate lehe, luuakse automaatselt seos üksikasjade lehega.</span><span class="sxs-lookup"><span data-stu-id="dc33b-256">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>

7. <span data-ttu-id="dc33b-257">Sisestage lehe pealkiri, nt **Arve üksikasjad** ja kirjeldus, nt **Kuva arve päis ja rea üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-257">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>

8. <span data-ttu-id="dc33b-258">Klõpsake nuppu **Vali väljad**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-258">Click **Select fields**.</span></span> <span data-ttu-id="dc33b-259">Pange tähele, et väljad kuvatakse lõppkasutajatele lisamise järjekorras.</span><span class="sxs-lookup"><span data-stu-id="dc33b-259">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="dc33b-260">Ainus võimalus väljade järjestust muuta on kõik väljad uuesti valida.</span><span class="sxs-lookup"><span data-stu-id="dc33b-260">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 

9. <span data-ttu-id="dc33b-261">Lisage selle stsenaariumi nõuete põhjal päisest järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="dc33b-261">Add the following fields from the header, based on the requirements for this scenario:</span></span>
   - <span data-ttu-id="dc33b-262">Hankija nimi</span><span class="sxs-lookup"><span data-stu-id="dc33b-262">Vendor name</span></span>
   - <span data-ttu-id="dc33b-263">Arve summa</span><span class="sxs-lookup"><span data-stu-id="dc33b-263">Invoice total</span></span>
   - <span data-ttu-id="dc33b-264">Maksja</span><span class="sxs-lookup"><span data-stu-id="dc33b-264">Invoice account</span></span>
   - <span data-ttu-id="dc33b-265">Arve number</span><span class="sxs-lookup"><span data-stu-id="dc33b-265">Invoice number</span></span>
   - <span data-ttu-id="dc33b-266">Arve kuupäev</span><span class="sxs-lookup"><span data-stu-id="dc33b-266">Invoice date</span></span>
   - <span data-ttu-id="dc33b-267">Arve kirjeldus</span><span class="sxs-lookup"><span data-stu-id="dc33b-267">Invoice description</span></span>
   - <span data-ttu-id="dc33b-268">Tähtaeg</span><span class="sxs-lookup"><span data-stu-id="dc33b-268">Due date</span></span>
   - <span data-ttu-id="dc33b-269">Arve valuuta</span><span class="sxs-lookup"><span data-stu-id="dc33b-269">Invoice currency</span></span>

10. <span data-ttu-id="dc33b-270">Lisage lehel olevast ridade ruudustikust järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="dc33b-270">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="dc33b-271">Hankekategooria</span><span class="sxs-lookup"><span data-stu-id="dc33b-271">Procurement category</span></span>
    - <span data-ttu-id="dc33b-272">Kogus</span><span class="sxs-lookup"><span data-stu-id="dc33b-272">Quantity</span></span>
    - <span data-ttu-id="dc33b-273">Ühiku hind</span><span class="sxs-lookup"><span data-stu-id="dc33b-273">Unit price</span></span>
    - <span data-ttu-id="dc33b-274">Rea netosumma</span><span class="sxs-lookup"><span data-stu-id="dc33b-274">Line net amount</span></span>
    - <span data-ttu-id="dc33b-275">1099-summa</span><span class="sxs-lookup"><span data-stu-id="dc33b-275">1099 amount</span></span>

11. <span data-ttu-id="dc33b-276">Kui kõik väljad eelmisest kahest toimingust on lisatud, klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-276">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="dc33b-277">Leht peab sarnanema järgmisele illustratsioonile.</span><span class="sxs-lookup"><span data-stu-id="dc33b-277">The page must resemble the following illustration.</span></span>
    
    <span data-ttu-id="dc33b-278">[![Leht pärast väljade lisamist](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="dc33b-278">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>

12. <span data-ttu-id="dc33b-279">Redigeerimisrežiimist väljumiseks klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-279">Click **Done** to exit edit mode.</span></span>

13. <span data-ttu-id="dc33b-280">Klõpsake nuppu **Tagasi** ja seejärel nuppu **Valmis** tööruumist väljumiseks</span><span class="sxs-lookup"><span data-stu-id="dc33b-280">Click **Back** and then **Done** to exit the workspace</span></span>

14. <span data-ttu-id="dc33b-281">Töö salvestamiseks klõpsake nuppu **Avalda tööruum**</span><span class="sxs-lookup"><span data-stu-id="dc33b-281">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="dc33b-282">Töövoo tegevused</span><span class="sxs-lookup"><span data-stu-id="dc33b-282">Workflow actions</span></span>

<span data-ttu-id="dc33b-283">Töövootoimingute lisamiseks kasutage lehte **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-283">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="dc33b-284">Selle lehe avamiseks asendage menüüelemendi nimi URL-is nii, nagu varem tegite.</span><span class="sxs-lookup"><span data-stu-id="dc33b-284">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="dc33b-285">Seejärel avage mobiilne kujundaja nupult **Sätted** (hammasratas).</span><span class="sxs-lookup"><span data-stu-id="dc33b-285">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="dc33b-286">Tehke järgmist töövootoimingute lisamiseks üksikasjade lehel.</span><span class="sxs-lookup"><span data-stu-id="dc33b-286">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="dc33b-287">Teile peavad olema määratud sobivas olekus arved, mis teevad teile kättesaadavaks need töövootegevused, mille kujundamisega tegelete.</span><span class="sxs-lookup"><span data-stu-id="dc33b-287">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="dc33b-288">Töövoo tegevuste registreerimine</span><span class="sxs-lookup"><span data-stu-id="dc33b-288">Record workflow actions</span></span>
1.  <span data-ttu-id="dc33b-289">Klõpsake tööruumis redigeerimisrežiimi käivitamiseks nuppu **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-289">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="dc33b-290">Valige eelnevalt loodud leht **Arve üksikasjad** ja klõpsake siis nuppu **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-290">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="dc33b-291">Klõpsake vahekaardil **Tegevused** käsku **Lisa tegevus**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-291">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="dc33b-292">Sisestage tegevuse pealkiri, nt **Kinnitamine**, ja kirjeldus, nt **Arve kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-292">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="dc33b-293">Pange tähele, et sisestatud tegevuse pealkirjast saab tegevuse nimi, mida kasutajale mobiilirakenduses näidatakse.</span><span class="sxs-lookup"><span data-stu-id="dc33b-293">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="dc33b-294">Klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-294">Click **Done**.</span></span>
6.  <span data-ttu-id="dc33b-295">Klõpsake nuppu **Vali väljad**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-295">Click **Select fields**.</span></span>
7.  <span data-ttu-id="dc33b-296">Läbige töövooprotsess lehel **VendMobileInvoiceHeaderDetails** ja tehke tegevus, mida soovisite registreerida.</span><span class="sxs-lookup"><span data-stu-id="dc33b-296">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="dc33b-297">Veenduge, et sisestate selle protsessi käigus töövoo kommentaarid, nii et kommentaaride väli lisatakse samuti mobiiliversiooni.</span><span class="sxs-lookup"><span data-stu-id="dc33b-297">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="dc33b-298">Pärast töövootegevuse käitamist klõpsake väljade valimise ülesande lõpetamiseks nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-298">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="dc33b-299">Redigeerimisrežiimist väljumiseks klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-299">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="dc33b-300">Klõpsake nuppu **Tagasi** ja seejärel nuppu **Valmis** tööruumist väljumiseks</span><span class="sxs-lookup"><span data-stu-id="dc33b-300">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="dc33b-301">Töö salvestamiseks klõpsake nuppu **Avalda tööruum**</span><span class="sxs-lookup"><span data-stu-id="dc33b-301">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="dc33b-302">Korrake eelmisi toiminguid kõigi vajalike töövootegevuste registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="dc33b-302">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="dc33b-303">Looge JS-fail</span><span class="sxs-lookup"><span data-stu-id="dc33b-303">Create a .js file</span></span>
1. <span data-ttu-id="dc33b-304">Avage Notepad või Microsoft Visual Studio ja kleepige sinna järgmine kood.</span><span class="sxs-lookup"><span data-stu-id="dc33b-304">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="dc33b-305">Salvestage fail JS-failina.</span><span class="sxs-lookup"><span data-stu-id="dc33b-305">Save the file as a .js file.</span></span> <span data-ttu-id="dc33b-306">See kood teeb järgmist.</span><span class="sxs-lookup"><span data-stu-id="dc33b-306">This code does the following:</span></span>
    - <span data-ttu-id="dc33b-307">See peidab töövooga seotud lisaveerud, mille varem mobiili loendilehel lisasime.</span><span class="sxs-lookup"><span data-stu-id="dc33b-307">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="dc33b-308">Lisasime need veerud selleks, et rakendusel oleks see teave kontekstis olemas ja see saaks teha järgmise toimingu.</span><span class="sxs-lookup"><span data-stu-id="dc33b-308">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="dc33b-309">Aktiivse töövooetapi põhjal rakendab see loogikat ainult nende tegevuste näitamiseks.</span><span class="sxs-lookup"><span data-stu-id="dc33b-309">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dc33b-310">Lehtede ja muude juhtelementide nimed JS-koodis peavad olema samad, mis tööruumis.</span><span class="sxs-lookup"><span data-stu-id="dc33b-310">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }
    ```

2.  <span data-ttu-id="dc33b-311">Laadige koodifail tööruumi üles, valides vahekaardi **Loogika**</span><span class="sxs-lookup"><span data-stu-id="dc33b-311">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="dc33b-312">Redigeerimisrežiimist väljumiseks klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-312">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="dc33b-313">Klõpsake nuppu **Tagasi** ja seejärel nuppu **Valmis** tööruumist väljumiseks</span><span class="sxs-lookup"><span data-stu-id="dc33b-313">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="dc33b-314">Töö salvestamiseks klõpsake nuppu **Avalda tööruum**</span><span class="sxs-lookup"><span data-stu-id="dc33b-314">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="dc33b-315">Hankija arve manused</span><span class="sxs-lookup"><span data-stu-id="dc33b-315">Vendor invoice attachments</span></span>

1. <span data-ttu-id="dc33b-316">Klõpsake nuppu **Sätted** (hammasratas) lehe ülemises paremas osas ja seejärel valikut **Mobiilirakendus**</span><span class="sxs-lookup"><span data-stu-id="dc33b-316">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>

2. <span data-ttu-id="dc33b-317">Klõpsake tööruumis redigeerimisrežiimi käivitamiseks nuppu **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-317">Click the **Edit** button to start edit mode in the workspace.</span></span>

3. <span data-ttu-id="dc33b-318">Valige eelnevalt loodud leht <strong>Arve üksikasjad \*\*ja klõpsake siis nuppu \*\*Redigeeri</strong>.</span><span class="sxs-lookup"><span data-stu-id="dc33b-318">Select the <strong>Invoice details \*\*page that you created earlier, and then click \*\*Edit</strong>.</span></span>

4. <span data-ttu-id="dc33b-319">Määrake valiku **Dokumendihaldus** sätteks **Jah**, nagu allpool näidatud.</span><span class="sxs-lookup"><span data-stu-id="dc33b-319">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="dc33b-320">**Märkus.** Kui puuduvad nõuded mobiilsel seadmel manuste näitamiseks, võite jätta selle valiku sätteks **Ei**, mis on vaikesäte.</span><span class="sxs-lookup"><span data-stu-id="dc33b-320">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
   
   ![Dokumendihaldus](./media/docmanagement-216x300.png)

5. <span data-ttu-id="dc33b-322">Redigeerimisrežiimist väljumiseks klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-322">Click **Done** to exit edit mode.</span></span>

6. <span data-ttu-id="dc33b-323">Klõpsake nuppu **Tagasi** ja seejärel nuppu **Valmis** tööruumist väljumiseks</span><span class="sxs-lookup"><span data-stu-id="dc33b-323">Click **Back** and then **Done** to exit the workspace</span></span>

7. <span data-ttu-id="dc33b-324">Töö salvestamiseks klõpsake nuppu **Avalda tööruum**</span><span class="sxs-lookup"><span data-stu-id="dc33b-324">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="dc33b-325">Hankija arve rea jaotused</span><span class="sxs-lookup"><span data-stu-id="dc33b-325">Vendor invoice line distributions</span></span>

<span data-ttu-id="dc33b-326">Selle stsenaariumi nõudmised kinnitavad, et olemas on ainult rea tasemel jaotused ja et arvel on alati ainult üks rida.</span><span class="sxs-lookup"><span data-stu-id="dc33b-326">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="dc33b-327">Kuna see stsenaarium on lihtne, peab kasutaja kogemus mobiilsel seadmel olema samuti piisavalt lihtne, et kasutaja ei peaks jaotuste vaatamiseks mitme taseme võrra süvitsi minema.</span><span class="sxs-lookup"><span data-stu-id="dc33b-327">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="dc33b-328">Hankija arved sisaldavad võimalust kuvada kõik jaotused arve päisest.</span><span class="sxs-lookup"><span data-stu-id="dc33b-328">Vendor invoices include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="dc33b-329">Seda me mobiilistsenaariumi puhul vajamegi.</span><span class="sxs-lookup"><span data-stu-id="dc33b-329">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="dc33b-330">Seetõttu kasutame selle mobiilistsenaariumi osa kujundamiseks lehte **VendMobileInvoiceAllDistributionTree**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-330">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="dc33b-331">Nõuetega kursis olemine aitab meil stsenaariumi kujundamisel otsustada, millist konkreetset lehte kasutada ja kuidas täpselt kasutaja mobiilikogemust optimeerida.</span><span class="sxs-lookup"><span data-stu-id="dc33b-331">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="dc33b-332">Teises stsenaariumis kasutame teist lehte jaotuste näitamiseks, kuna selle stsenaariumi nõuded on erinevad.</span><span class="sxs-lookup"><span data-stu-id="dc33b-332">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="dc33b-333">Asendage menüüelemendi nimi URL-is nii, nagu enne tegite.</span><span class="sxs-lookup"><span data-stu-id="dc33b-333">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="dc33b-334">Kuvatav leht peab sarnanema järgmisele illustratsioonile.</span><span class="sxs-lookup"><span data-stu-id="dc33b-334">The page that appears should resemble the following illustration.</span></span>

    <span data-ttu-id="dc33b-335">[![Kõigi jaotuste leht](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="dc33b-335">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>

2.  <span data-ttu-id="dc33b-336">Avage mobiilne kujundaja nupult **Sätted** (hammasratas).</span><span class="sxs-lookup"><span data-stu-id="dc33b-336">Open the mobile designer from the **Settings** (gear) button.</span></span>

3.  <span data-ttu-id="dc33b-337">Klõpsake tööruumis redigeerimisrežiimi käivitamiseks nuppu **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-337">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="dc33b-338">**Märkus.** Näete, et automaatselt loodi kaks uut lehte.</span><span class="sxs-lookup"><span data-stu-id="dc33b-338">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="dc33b-339">Süsteem loob need lehed, kuna lülitasite eelmises jaotises sisse dokumendihalduse.</span><span class="sxs-lookup"><span data-stu-id="dc33b-339">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="dc33b-340">Võite neid uusi lehti eirata.</span><span class="sxs-lookup"><span data-stu-id="dc33b-340">You can ignore these new pages.</span></span>

4.  <span data-ttu-id="dc33b-341">Klõpsake nuppu **Lisa leht**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-341">Click **Add page**.</span></span>

5.  <span data-ttu-id="dc33b-342">Sisestage lehe pealkiri, nt **Arvestuse kuvamine** ja kirjeldus, nt **Arve arvestuse kuvamine**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-342">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>

6.  <span data-ttu-id="dc33b-343">Klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-343">Click **Done**.</span></span>

7.  <span data-ttu-id="dc33b-344">Klõpsake vahekaardil **Väljad** valikut **Vali väljad**, valige jaotuste lehelt järgmised väljad ja klõpsake seejärel nuppu **Valmis**:</span><span class="sxs-lookup"><span data-stu-id="dc33b-344">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="dc33b-345">Summa</span><span class="sxs-lookup"><span data-stu-id="dc33b-345">Amount</span></span>
    2.  <span data-ttu-id="dc33b-346">Valuuta</span><span class="sxs-lookup"><span data-stu-id="dc33b-346">Currency</span></span>
    3.  <span data-ttu-id="dc33b-347">Pearaamatukonto</span><span class="sxs-lookup"><span data-stu-id="dc33b-347">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="dc33b-348">Me ei valinud jaotuste ruudustikust veergu **Kirjeldus**, kuna selle stsenaariumi nõuded kinnitasid, et laiendatud hind on ainus summa, mille jaoks jaotused olemas on.</span><span class="sxs-lookup"><span data-stu-id="dc33b-348">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="dc33b-349">Seega ei vaja kasutaja teist välja summa tüübi määramiseks, mille jaoks jaotus on mõeldud.</span><span class="sxs-lookup"><span data-stu-id="dc33b-349">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="dc33b-350">Kuid järgmises stsenaariumis **kasutame** seda teavet, kuna selle stsenaariumi nõuded määravad, et teistel summatüüpidel on jaotused (nt käibemaks).</span><span class="sxs-lookup"><span data-stu-id="dc33b-350">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>

8.  <span data-ttu-id="dc33b-351">Redigeerimisrežiimist väljumiseks klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-351">Click **Done** to exit edit mode.</span></span>

9.  <span data-ttu-id="dc33b-352">Klõpsake nuppu **Tagasi** ja seejärel nuppu **Valmis** tööruumist väljumiseks</span><span class="sxs-lookup"><span data-stu-id="dc33b-352">Click **Back** and then **Done** to exit the workspace</span></span>

10. <span data-ttu-id="dc33b-353">Töö salvestamiseks klõpsake nuppu **Avalda tööruum**</span><span class="sxs-lookup"><span data-stu-id="dc33b-353">Click **Publish workspace** to save your work</span></span>

#### <a name="adding-navigation-to-view-accounting-page"></a><span data-ttu-id="dc33b-354">Lehele „Raamatupidamise kuvamine” navigeerimise lisamine</span><span class="sxs-lookup"><span data-stu-id="dc33b-354">Adding navigation to "View accounting" page</span></span>

<span data-ttu-id="dc33b-355">Mobiilileht **Arvestuse kuvamine** pole praegu seotud ühegi mobiililehega, mille seni kujundanud oleme.</span><span class="sxs-lookup"><span data-stu-id="dc33b-355">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="dc33b-356">Kuna kasutaja peab saama liikuda lehele **Arvestuse kuvamine** mobiilse seadme lehelt **Arve üksikasjad**, peame pakkuma võimalust liikuda lehelt **Arve üksikasjad** lehele **Arvestuse kuvamine**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-356">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="dc33b-357">Tekitame selle liikumisvõimaluse, kasutades JavaScripti kaudu lisaloogikat.</span><span class="sxs-lookup"><span data-stu-id="dc33b-357">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="dc33b-358">Avage varem loodud JS-fail ja lisage read, mis tõstetakse esile järgmises koodis.</span><span class="sxs-lookup"><span data-stu-id="dc33b-358">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="dc33b-359">See kood teeb kahte asja.</span><span class="sxs-lookup"><span data-stu-id="dc33b-359">This code does two things:</span></span>
    1.  <span data-ttu-id="dc33b-360">See aitab garanteerida, et kasutajad ei saa liikuda otse tööruumist lehele **Arvestuse kuvamine**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-360">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="dc33b-361">See tekitab navigeerimisnupu lehelt **Arve üksikasjad** lehele **Arvestuse kuvamine**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-361">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="dc33b-362">Lehtede ja muude juhtelementide nimed JS-koodis peavad olema samad, mis tööruumis.</span><span class="sxs-lookup"><span data-stu-id="dc33b-362">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }
    ```
    
2.  <span data-ttu-id="dc33b-363">Eelmise koodi ülekirjutamiseks laadige koodifail tööruumi üles, valides vahekaardi **Loogika**</span><span class="sxs-lookup"><span data-stu-id="dc33b-363">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="dc33b-364">Redigeerimisrežiimist väljumiseks klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-364">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="dc33b-365">Klõpsake nuppu **Tagasi** ja seejärel nuppu **Valmis** tööruumist väljumiseks</span><span class="sxs-lookup"><span data-stu-id="dc33b-365">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="dc33b-366">Töö salvestamiseks klõpsake nuppu **Avalda tööruum**</span><span class="sxs-lookup"><span data-stu-id="dc33b-366">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="dc33b-367">Kinnitamine</span><span class="sxs-lookup"><span data-stu-id="dc33b-367">Validation</span></span>

<span data-ttu-id="dc33b-368">Avage rakendus oma mobiilses seadmes ja looge ühendus oma eksemplariga.</span><span class="sxs-lookup"><span data-stu-id="dc33b-368">From your mobile device, open the app, and connect to your instance.</span></span> <span data-ttu-id="dc33b-369">Veenduge, et logiksite sisse ettevõttesse, kus teile on määratud ülevaatamiseks hankija arved.</span><span class="sxs-lookup"><span data-stu-id="dc33b-369">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="dc33b-370">Teil peaks olema võimalik teha järgmisi toiminguid.</span><span class="sxs-lookup"><span data-stu-id="dc33b-370">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="dc33b-371">Vaadake tööruumi **Minu kinnitused**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-371">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="dc33b-372">Minge tööruumis **Minu kinnitused** süvitsi ja vaadake lehte **Minu hankija arved**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-372">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="dc33b-373">Minge tööruumis **Minu hankija arved** süvitsi ja vaadake endale määratud arvete loendit.</span><span class="sxs-lookup"><span data-stu-id="dc33b-373">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="dc33b-374">Minge mõnes arves süvitsi ja vaadake arve päise üksikasju ja rea üksikasju.</span><span class="sxs-lookup"><span data-stu-id="dc33b-374">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="dc33b-375">Vaadake üksikasjade lehel linki manuste juurde ja minge selle lingi abil manuste loendisse ning vaadake manuseid.</span><span class="sxs-lookup"><span data-stu-id="dc33b-375">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="dc33b-376">Vaadake üksikasjade lehel linki lehele **Arvestuse kuvamine** ja minge selle lingi abil jaotuste lehele ning vaadake jaotusi.</span><span class="sxs-lookup"><span data-stu-id="dc33b-376">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="dc33b-377">Klõpsake üksikasjade lehe allosas menüüd **Tegevused** ja tehke töövooetappi puudutavad töövootegevused.</span><span class="sxs-lookup"><span data-stu-id="dc33b-377">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="dc33b-378">Keeruka arve kinnitamise stsenaariumi kujundamine Fabrikami jaoks</span><span class="sxs-lookup"><span data-stu-id="dc33b-378">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dc33b-379">Stsenaariumi atribuut</span><span class="sxs-lookup"><span data-stu-id="dc33b-379">Scenario attribute</span></span></th>
<th><span data-ttu-id="dc33b-380">Vastus</span><span class="sxs-lookup"><span data-stu-id="dc33b-380">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc33b-381">Milliseid arve päise välju soovib kasutaja mobiiliversioonis näha ja millises järjekorras?</span><span class="sxs-lookup"><span data-stu-id="dc33b-381">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="dc33b-382">Hankija nimi</span><span class="sxs-lookup"><span data-stu-id="dc33b-382">Vendor name</span></span></li>
<li><span data-ttu-id="dc33b-383">Arve summa</span><span class="sxs-lookup"><span data-stu-id="dc33b-383">Invoice amount</span></span></li>
<li><span data-ttu-id="dc33b-384">Maksja</span><span class="sxs-lookup"><span data-stu-id="dc33b-384">Invoice account</span></span></li>
<li><span data-ttu-id="dc33b-385">Arve number</span><span class="sxs-lookup"><span data-stu-id="dc33b-385">Invoice number</span></span></li>
<li><span data-ttu-id="dc33b-386">Arve kuupäev</span><span class="sxs-lookup"><span data-stu-id="dc33b-386">Invoice date</span></span></li>
<li><span data-ttu-id="dc33b-387">Arve kirjeldus</span><span class="sxs-lookup"><span data-stu-id="dc33b-387">Invoice description</span></span></li>
<li><span data-ttu-id="dc33b-388">Tähtaeg</span><span class="sxs-lookup"><span data-stu-id="dc33b-388">Due date</span></span></li>
<li><span data-ttu-id="dc33b-389">Arve valuuta</span><span class="sxs-lookup"><span data-stu-id="dc33b-389">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc33b-390">Milliseid arve ridade välju soovib kasutaja mobiiliversioonis näha ja millises järjekorras?</span><span class="sxs-lookup"><span data-stu-id="dc33b-390">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="dc33b-391">Hankekategooria</span><span class="sxs-lookup"><span data-stu-id="dc33b-391">Procurement category</span></span></li>
<li><span data-ttu-id="dc33b-392">Kogus</span><span class="sxs-lookup"><span data-stu-id="dc33b-392">Quantity</span></span></li>
<li><span data-ttu-id="dc33b-393">Ühiku hind</span><span class="sxs-lookup"><span data-stu-id="dc33b-393">Unit price</span></span></li>
<li><span data-ttu-id="dc33b-394">Rea netosumma</span><span class="sxs-lookup"><span data-stu-id="dc33b-394">Line net amount</span></span></li>
<li><span data-ttu-id="dc33b-395">1099-summa</span><span class="sxs-lookup"><span data-stu-id="dc33b-395">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc33b-396">Mitu arverida arvel on?</span><span class="sxs-lookup"><span data-stu-id="dc33b-396">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="dc33b-397">Rakendage siin 80-20 reeglit ja optimeerige 80 protsendi jaoks.</span><span class="sxs-lookup"><span data-stu-id="dc33b-397">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="dc33b-398">5</span><span class="sxs-lookup"><span data-stu-id="dc33b-398">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc33b-399">Kas kasutajad soovivad arvestuse jaotusi (arvekoode) ülevaatamise ajal mobiilsel seadmel näha?</span><span class="sxs-lookup"><span data-stu-id="dc33b-399">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="dc33b-400">Jah</span><span class="sxs-lookup"><span data-stu-id="dc33b-400">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc33b-401">Kui palju arvestuse jaotusi (laiendatud hind, käibemaks, tasud jne) arve real on?</span><span class="sxs-lookup"><span data-stu-id="dc33b-401">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="dc33b-402">Rakendage jällegi 80-20 reeglit.</span><span class="sxs-lookup"><span data-stu-id="dc33b-402">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="dc33b-403">Laiendatud hind: 2 Käibemaks: 2 Tasud: 2</span><span class="sxs-lookup"><span data-stu-id="dc33b-403">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc33b-404">Kas arvete päises on ka arvestuse jaotused?</span><span class="sxs-lookup"><span data-stu-id="dc33b-404">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="dc33b-405">Kui nii, siis kas need arvestuse jaotused peaksid seadmel kättesaadavad olema?</span><span class="sxs-lookup"><span data-stu-id="dc33b-405">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="dc33b-406">Pole kasutusel</span><span class="sxs-lookup"><span data-stu-id="dc33b-406">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc33b-407">Kas kasutajad soovivad seadmel arve manuseid näha?</span><span class="sxs-lookup"><span data-stu-id="dc33b-407">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="dc33b-408">Jah</span><span class="sxs-lookup"><span data-stu-id="dc33b-408">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="dc33b-409">Järgmised sammud</span><span class="sxs-lookup"><span data-stu-id="dc33b-409">Next steps</span></span>

<span data-ttu-id="dc33b-410">1. stsenaariumi puhul saab kasutada järgmisi variatsioone, tuginedes 2. stsenaariumi nõuetele.</span><span class="sxs-lookup"><span data-stu-id="dc33b-410">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="dc33b-411">Selle jaotise abil saate parandada oma mobiilirakenduse kogemust.</span><span class="sxs-lookup"><span data-stu-id="dc33b-411">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="dc33b-412">Kuna 2. stsenaariumi puhul eeldatakse suuremat arve ridade arvu, aitavad järgmised kujunduse muudatused kasutajakogemust mobiilsel seadmel optimeerida.</span><span class="sxs-lookup"><span data-stu-id="dc33b-412">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="dc33b-413">Arve ridade vaatamise asemel üksikasjade lehel (nagu 1. stsenaariumis) võivad kasutajad valida ridade vaatamise eraldi mobiililehel.</span><span class="sxs-lookup"><span data-stu-id="dc33b-413">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="dc33b-414">Kuna selles stsenaariumis eeldatakse mitut arve rida, siis kui mobiili jaotuste lehe kujundamiseks kasutatakse lehte **VendMobileInvoiceAllDistributionTree** (nagu 1. stsenaariumis), võib ridade seostamine jaotustega kasutajale segadust tekitada.</span><span class="sxs-lookup"><span data-stu-id="dc33b-414">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="dc33b-415">Seetõttu kasutage jaotuste lehe kujundamiseks lehte **VendMobileInvoiceLineDistributionTree**.</span><span class="sxs-lookup"><span data-stu-id="dc33b-415">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="dc33b-416">Ideaaljuhul tuleks jaotusi näidata selles stsenaariumis arve rea kontekstis.</span><span class="sxs-lookup"><span data-stu-id="dc33b-416">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="dc33b-417">Seega veenduge, et kasutaja saab jaotuste lehe vaatamiseks reas süvitsi minna.</span><span class="sxs-lookup"><span data-stu-id="dc33b-417">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="dc33b-418">Kasutage lehe lingivõimalust süvaaruande koostamiseks, nagu tegite päise ja üksikasjade lehtedel 1. stsenaariumis.</span><span class="sxs-lookup"><span data-stu-id="dc33b-418">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="dc33b-419">Kuna 2. stsenaariumi puhul eeldatakse mitut summa tüüpi (käibemaks, tasud jne), on kasulik näidata summa tüübi kirjeldust.</span><span class="sxs-lookup"><span data-stu-id="dc33b-419">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="dc33b-420">(Jätsime selle teabe 1. stsenaariumist välja.)</span><span class="sxs-lookup"><span data-stu-id="dc33b-420">(We omitted this information in scenario 1.)</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]