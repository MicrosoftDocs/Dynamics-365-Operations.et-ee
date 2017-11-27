---
title: Mobiilsed arvete heakskiidud
description: "See teema on mõeldud praktilise lähenemise pakkumiseks mobiilistsenaariumide kujundamisele rakenduses Dynamics 365 for Finance and Operations, võttes mobiilse hankija arvete kinnitamise kasutusnäiteks."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c579db5a922d81a2781ec2011e148db54fac288d
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="mobile-invoice-approvals"></a><span data-ttu-id="ce446-103">Mobiilsed arvete heakskiidud</span><span class="sxs-lookup"><span data-stu-id="ce446-103">Mobile invoice approvals</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ce446-104">Mobiilsed võimalused Microsoft Dynamics 365 for Finance and Operations, Enterprise editionis lasevad ärikasutajatel mobiilikogemusi kujundada.</span><span class="sxs-lookup"><span data-stu-id="ce446-104">Mobile capabilities in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition let a business user design mobile experiences.</span></span> <span data-ttu-id="ce446-105">Täpsemate stsenaariumide puhul võimaldab platvorm arendajatel võimalusi oma soovi kohaselt laiendada.</span><span class="sxs-lookup"><span data-stu-id="ce446-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="ce446-106">Kõige tulemuslikum viis mõningaid neist uutest mobiilikontseptsioonidest tundma õppida on läbi mõne stsenaariumi kujundamise protsessis.</span><span class="sxs-lookup"><span data-stu-id="ce446-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="ce446-107">See teema on mõeldud praktilise lähenemise pakkumiseks mobiilistsenaariumide kujundamisele, võttes mobiilse hankija arvete kinnitamise kasutusnäiteks.</span><span class="sxs-lookup"><span data-stu-id="ce446-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="ce446-108">See teema aitab teil kujundada stsenaariumide muid variatsioone ja seda saab rakendada ka muudele stsenaariumidele, mis pole hankija arvetega seotud.</span><span class="sxs-lookup"><span data-stu-id="ce446-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="ce446-109">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="ce446-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="ce446-110">Eeltingimus</span><span class="sxs-lookup"><span data-stu-id="ce446-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="ce446-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ce446-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce446-112">Mobiili käsiraamat eelnevaks lugemiseks</span><span class="sxs-lookup"><span data-stu-id="ce446-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="ce446-113">Mobiilne platvorm</span><span class="sxs-lookup"><span data-stu-id="ce446-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="ce446-114">Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ce446-114">Dynamics 365 for Finance and Operations</span></span>                                                                             | <span data-ttu-id="ce446-115">Keskkond, millesse on installitud Microsoft Dynamics 365 for Operationsi versioon 1611 ja Microsoft Dynamics for Operationsi platvormivärskendus 3 (november 2016).</span><span class="sxs-lookup"><span data-stu-id="ce446-115">An environment that has Microsoft Dynamics 365 for Operations version 1611 and Microsoft Dynamics for Operations platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="ce446-116">Installige kiirparandus KB 3204341.</span><span class="sxs-lookup"><span data-stu-id="ce446-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="ce446-117">Tegevuse salvestaja võib kogemata salvestada rippdialoogidele kaks sulgemiskäsku Dynamics 365 for Operationsi platvormi värskenduses 3 (2016. aasta novembri värskendus)</span><span class="sxs-lookup"><span data-stu-id="ce446-117">Task recorder can erroneously record two Close commands for dropdown dialogs this is included in Dynamics 365 for Operation platform update 3 (November 2016 update)</span></span> |
| <span data-ttu-id="ce446-118">Installige kiirparandus KB 3207800.</span><span class="sxs-lookup"><span data-stu-id="ce446-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="ce446-119">See kiirparandus võimaldab vaadata manuseid mobiilikliendil, mis sisaldub Dynamics 365 for Operationsi platvormi värskenduses 3 (2016. aasta novembri värskendus).</span><span class="sxs-lookup"><span data-stu-id="ce446-119">This hotfix enables attachments to be viewed on the mobile client this is included in Dynamics 365 for Operation platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="ce446-120">Installige kiirparandus KB 3208224.</span><span class="sxs-lookup"><span data-stu-id="ce446-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="ce446-121">Rakenduse kood mobiilse hankija arve kinnitamise rakenduse jaoks, mis sisaldub Microsoft Dynamics AX-i rakenduses 7.0.1 (mai 2016).</span><span class="sxs-lookup"><span data-stu-id="ce446-121">Application code for the mobile vendor invoice approval application this is included in Microsoft Dynamics AX application 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="ce446-122">Androidi või iOS-i või Windowsi seade, millesse on installitud Finance and Operationsi mobiilirakendus</span><span class="sxs-lookup"><span data-stu-id="ce446-122">An Android or iOS or a Windows device that has the mobile app installed for Finance and Operations</span></span> | <span data-ttu-id="ce446-123">Otsige rakendust vastavast rakenduste poest.</span><span class="sxs-lookup"><span data-stu-id="ce446-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="ce446-124">Sissejuhatus</span><span class="sxs-lookup"><span data-stu-id="ce446-124">Introduction</span></span>
<span data-ttu-id="ce446-125">Hankija arvete mobiilsed kinnitused nõuavad kolme kiirparandust, mis on nimetatud jaotises „Eeltingimused”.</span><span class="sxs-lookup"><span data-stu-id="ce446-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="ce446-126">Need kiirparandused ei paku tööruumi arvete kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="ce446-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="ce446-127">Seda, mis on mobiili kontekstis tööruum, saate lugeda jaotises „Eeltingimused” nimetatud mobiili käsiraamatust.</span><span class="sxs-lookup"><span data-stu-id="ce446-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="ce446-128">Arvete kinnitamise tööruum vajab kujundamist.</span><span class="sxs-lookup"><span data-stu-id="ce446-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="ce446-129">Iga organisatsioon korraldab ja määratleb hankija arvete äriprotsessi erinevalt.</span><span class="sxs-lookup"><span data-stu-id="ce446-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="ce446-130">Enne hankija arvete kinnituste jaoks mobiilikogemuse kujundamist tuleks arvestada järgimisi äriprotsessi aspekte.</span><span class="sxs-lookup"><span data-stu-id="ce446-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="ce446-131">Kasutajakogemuse optimeerimiseks seadmel tuleks neid andmepunkte kasutada võimalikult palju.</span><span class="sxs-lookup"><span data-stu-id="ce446-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="ce446-132">Milliseid arve päise välju soovib kasutaja mobiiliversioonis näha ja millises järjekorras?</span><span class="sxs-lookup"><span data-stu-id="ce446-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="ce446-133">Milliseid arve ridade välju soovib kasutaja mobiiliversioonis näha ja millises järjekorras?</span><span class="sxs-lookup"><span data-stu-id="ce446-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="ce446-134">Mitu arverida arvel on?</span><span class="sxs-lookup"><span data-stu-id="ce446-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="ce446-135">Rakendage siin 80-20 reeglit ja optimeerige 80 protsendi jaoks.</span><span class="sxs-lookup"><span data-stu-id="ce446-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="ce446-136">Kas kasutajad soovivad arvestuse jaotusi (arvekoode) ülevaatamise ajal mobiilsel seadmel näha?</span><span class="sxs-lookup"><span data-stu-id="ce446-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="ce446-137">Kui vastus sellele küsimusele on jah, siis kaaluge järgmisi küsimusi.</span><span class="sxs-lookup"><span data-stu-id="ce446-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="ce446-138">Kui palju arvestuse jaotusi (laiendatud hind, käibemaks, tasud, jagamised jne) arve real on?</span><span class="sxs-lookup"><span data-stu-id="ce446-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="ce446-139">Rakendage jällegi 80-20 reeglit.</span><span class="sxs-lookup"><span data-stu-id="ce446-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="ce446-140">Kas arvete päises on ka arvestuse jaotused?</span><span class="sxs-lookup"><span data-stu-id="ce446-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="ce446-141">Kui nii, siis kas need arvestuse jaotused peaksid seadmel kättesaadavad olema?</span><span class="sxs-lookup"><span data-stu-id="ce446-141">If so, should these accounting distributions be available on the device?</span></span>

> [!NOTE]
> <span data-ttu-id="ce446-142">Selles teemas ei selgitata, kuidas arvestuse jaotusi redigeerida, kuna seda funktsiooni ei toetata praegu mobiilistsenaariumide puhul.</span><span class="sxs-lookup"><span data-stu-id="ce446-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="ce446-143">Kas kasutajad soovivad seadmel arve manuseid näha?</span><span class="sxs-lookup"><span data-stu-id="ce446-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="ce446-144">Arvete kinnitamise mobiiliversioon on erinev, olenevalt nende küsimuste vastustest.</span><span class="sxs-lookup"><span data-stu-id="ce446-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="ce446-145">Eesmärk on optimeerida organisatsioonis kasutaja äriprotsessi kogemust mobiilil.</span><span class="sxs-lookup"><span data-stu-id="ce446-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="ce446-146">Ülejäänud teemas vaatame kahte stsenaariumivarianti, mis põhinevad erinevatel vastustel eelnevatele küsimustele.</span><span class="sxs-lookup"><span data-stu-id="ce446-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="ce446-147">Üldise juhisena veenduge mobiilikujundajaga töötamisel, et avaldaksite muudatused, et vältida nende kaotsiminekut.</span><span class="sxs-lookup"><span data-stu-id="ce446-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="ce446-148">Lihtsa arve kinnitamise stsenaariumi kujundamine Contoso jaoks</span><span class="sxs-lookup"><span data-stu-id="ce446-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce446-149">Stsenaariumi atribuut</span><span class="sxs-lookup"><span data-stu-id="ce446-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="ce446-150">Vastus</span><span class="sxs-lookup"><span data-stu-id="ce446-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce446-151">Milliseid arve päise välju soovib kasutaja mobiiliversioonis näha ja millises järjekorras?</span><span class="sxs-lookup"><span data-stu-id="ce446-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="ce446-152">Hankija nimi</span><span class="sxs-lookup"><span data-stu-id="ce446-152">Vendor name</span></span></li>
<li><span data-ttu-id="ce446-153">Arve summa</span><span class="sxs-lookup"><span data-stu-id="ce446-153">Invoice total</span></span></li>
<li><span data-ttu-id="ce446-154">Maksja</span><span class="sxs-lookup"><span data-stu-id="ce446-154">Invoice account</span></span></li>
<li><span data-ttu-id="ce446-155">Arve number</span><span class="sxs-lookup"><span data-stu-id="ce446-155">Invoice number</span></span></li>
<li><span data-ttu-id="ce446-156">Arve kuupäev</span><span class="sxs-lookup"><span data-stu-id="ce446-156">Invoice date</span></span></li>
<li><span data-ttu-id="ce446-157">Arve kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ce446-157">Invoice description</span></span></li>
<li><span data-ttu-id="ce446-158">Tähtaeg</span><span class="sxs-lookup"><span data-stu-id="ce446-158">Due date</span></span></li>
<li><span data-ttu-id="ce446-159">Arve valuuta</span><span class="sxs-lookup"><span data-stu-id="ce446-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce446-160">Milliseid arve ridade välju soovib kasutaja mobiiliversioonis näha ja millises järjekorras?</span><span class="sxs-lookup"><span data-stu-id="ce446-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="ce446-161">Hankekategooria</span><span class="sxs-lookup"><span data-stu-id="ce446-161">Procurement category</span></span></li>
<li><span data-ttu-id="ce446-162">Kogus</span><span class="sxs-lookup"><span data-stu-id="ce446-162">Quantity</span></span></li>
<li><span data-ttu-id="ce446-163">Ühiku hind</span><span class="sxs-lookup"><span data-stu-id="ce446-163">Unit price</span></span></li>
<li><span data-ttu-id="ce446-164">Rea netosumma</span><span class="sxs-lookup"><span data-stu-id="ce446-164">Line net amount</span></span></li>
<li><span data-ttu-id="ce446-165">1099-summa</span><span class="sxs-lookup"><span data-stu-id="ce446-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce446-166">Mitu arverida arvel on?</span><span class="sxs-lookup"><span data-stu-id="ce446-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="ce446-167">Rakendage siin 80-20 reeglit ja optimeerige 80 protsendi jaoks.</span><span class="sxs-lookup"><span data-stu-id="ce446-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="ce446-168">1</span><span class="sxs-lookup"><span data-stu-id="ce446-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce446-169">Kas kasutajad soovivad arvestuse jaotusi (arvekoode) ülevaatamise ajal mobiilsel seadmel näha?</span><span class="sxs-lookup"><span data-stu-id="ce446-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="ce446-170">Jah</span><span class="sxs-lookup"><span data-stu-id="ce446-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce446-171">Kui palju arvestuse jaotusi (laiendatud hind, käibemaks, tasud jne) arve real on?</span><span class="sxs-lookup"><span data-stu-id="ce446-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="ce446-172">Rakendage jällegi 80-20 reeglit.</span><span class="sxs-lookup"><span data-stu-id="ce446-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="ce446-173">Laiendatud hind: 2 Käibemaks: 0 Tasud: 0</span><span class="sxs-lookup"><span data-stu-id="ce446-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce446-174">Kas arvete päises on ka arvestuse jaotused?</span><span class="sxs-lookup"><span data-stu-id="ce446-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="ce446-175">Kui nii, siis kas need arvestuse jaotused peaksid seadmel kättesaadavad olema?</span><span class="sxs-lookup"><span data-stu-id="ce446-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="ce446-176">Pole kasutusel</span><span class="sxs-lookup"><span data-stu-id="ce446-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce446-177">Kas kasutajad soovivad seadmel arve manuseid näha?</span><span class="sxs-lookup"><span data-stu-id="ce446-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="ce446-178">Jah</span><span class="sxs-lookup"><span data-stu-id="ce446-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="ce446-179">Tööruumi loomine</span><span class="sxs-lookup"><span data-stu-id="ce446-179">Create the workspace</span></span>

1.  <span data-ttu-id="ce446-180">Avage brauseris Finance and Operations ja logige sisse.</span><span class="sxs-lookup"><span data-stu-id="ce446-180">In a browser, open Finance and Operations, and sign in.</span></span>
2.  <span data-ttu-id="ce446-181">Kui olete sisse loginud, lisage URL-ile **&mode=mobile**, nagu on näidatud järgmises näites, ja värskendage lehte: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard**&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="ce446-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard**&mode=mobile**</span></span>
3.  <span data-ttu-id="ce446-182">Klõpsake nuppu **Sätted** (hammasratas) lehe ülemises paremas osas ja seejärel valikut **Mobiilirakendus**.</span><span class="sxs-lookup"><span data-stu-id="ce446-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="ce446-183">Mobiilirakenduse kujundaja peaks ilmuma samamoodi, nagu ilmub tegevuse salvestaja.</span><span class="sxs-lookup"><span data-stu-id="ce446-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="ce446-184">Klõpsake uue tööruumi loomiseks nuppu **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="ce446-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="ce446-185">Selle näite puhul andke tööruumile nimi **Minu kinnitused**.</span><span class="sxs-lookup"><span data-stu-id="ce446-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="ce446-186">Sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="ce446-186">Enter a description.</span></span>
6.  <span data-ttu-id="ce446-187">Valige tööruumi värv.</span><span class="sxs-lookup"><span data-stu-id="ce446-187">Select a workspace color.</span></span> <span data-ttu-id="ce446-188">Tööruumi värvi kasutatakse selle tööruumi üldise mobiiliversiooni stiili puhul.</span><span class="sxs-lookup"><span data-stu-id="ce446-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="ce446-189">Valige tööruumi ikoon.</span><span class="sxs-lookup"><span data-stu-id="ce446-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="ce446-190">Klõpsake nuppu **Valmis**</span><span class="sxs-lookup"><span data-stu-id="ce446-190">Click **Done**</span></span>
9.  <span data-ttu-id="ce446-191">Muudatuste salvestamiseks klõpsake nuppu **Avalda tööruum**</span><span class="sxs-lookup"><span data-stu-id="ce446-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="ce446-192">Mulle määratud hankijaarved</span><span class="sxs-lookup"><span data-stu-id="ce446-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="ce446-193">Esimene mobiilne leht, mis vajab kujundamist, on kasutajale ülevaatamiseks määratud arvete loend.</span><span class="sxs-lookup"><span data-stu-id="ce446-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="ce446-194">Selle mobiilse lehe kujundamiseks kasutage lehte **VendMobileInvoiceAssignedToMeListPage** rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ce446-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page in Finance and Operations.</span></span> <span data-ttu-id="ce446-195">Enne selle protseduuri läbimist veenduge, et teile oleks ülevaatamiseks määratud vähemalt üks hankija arve ja et arve real oleks kaks jaotust.</span><span class="sxs-lookup"><span data-stu-id="ce446-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="ce446-196">See seadistus vastab selle stsenaariumi nõuetele.</span><span class="sxs-lookup"><span data-stu-id="ce446-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="ce446-197">Asendage Finance and Operationsi URL-is menüüelemendi nimi stringiga **VendMobileInvoiceAssignedToMeListPage**, et avada loendilehe **Mulle määratud ootel hankija arved** mobiiliversioon moodulis **Ostureskontro**.</span><span class="sxs-lookup"><span data-stu-id="ce446-197">In the Finance and Operations URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="ce446-198">Olenevalt sellest, kui palju arveid on teile teie süsteemis määratud, kuvatakse sellel lehel need arved.</span><span class="sxs-lookup"><span data-stu-id="ce446-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="ce446-199">Konkreetse arve otsimiseks võib kasutada vasakul olevat filtrit.</span><span class="sxs-lookup"><span data-stu-id="ce446-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="ce446-200">Kuid selle näite puhul pole meil konkreetset arvet vaja.</span><span class="sxs-lookup"><span data-stu-id="ce446-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="ce446-201">Meil on lihtsalt vaja, et teile oleks määratud mõni arve, mis võimaldaks teil mobiilset lehte kujundada.</span><span class="sxs-lookup"><span data-stu-id="ce446-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="ce446-202">Uued saadaolevad lehed on kujundatud spetsiaalselt hankija arve mobiilistsenaariumide väljatöötamiseks.</span><span class="sxs-lookup"><span data-stu-id="ce446-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="ce446-203">Seega tuleb kasutada neid lehti.</span><span class="sxs-lookup"><span data-stu-id="ce446-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="ce446-204">URL peab sarnanema järgmisele URL-ile ja kui olete selle sisestanud, peab avanema joonisel näidatud leht: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Mulle määratud ootel hankija arvete leht](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="ce446-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
2.  <span data-ttu-id="ce446-205">Klõpsake nuppu **Sätted** (hammasratas) lehe ülemises paremas osas ja seejärel valikut **Mobiilirakendus**</span><span class="sxs-lookup"><span data-stu-id="ce446-205">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="ce446-206">Valige oma tööruum ja klõpsake nuppu **Redigeeri**</span><span class="sxs-lookup"><span data-stu-id="ce446-206">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="ce446-207">Klõpsake esimese mobiilse lehe loomiseks nuppu **Lisa leht**.</span><span class="sxs-lookup"><span data-stu-id="ce446-207">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="ce446-208">Sisestage nimi nagu **Minu hankija arved** ja kirjeldus nagu **Mulle ülevaatamiseks määratud hankija arved**.</span><span class="sxs-lookup"><span data-stu-id="ce446-208">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="ce446-209">Klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="ce446-209">Click **Done**.</span></span>
7.  <span data-ttu-id="ce446-210">Klõpsake mobiilse kujundaja vahekaardil **Väljad** nuppu **Vali väljad**.</span><span class="sxs-lookup"><span data-stu-id="ce446-210">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="ce446-211">Loendilehe veerud peavad sarnanema järgmisele illustratsioonile.</span><span class="sxs-lookup"><span data-stu-id="ce446-211">The columns on the list page must resemble the following illustration.</span></span> <span data-ttu-id="ce446-212">[![Veerud lehel Mulle määratud ootel hankija arved](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="ce446-212">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
8.  <span data-ttu-id="ce446-213">Lisage vajalikud veerud loendilehelt, mis tuleb mobiililehel kasutajatele kuvada.</span><span class="sxs-lookup"><span data-stu-id="ce446-213">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="ce446-214">Väljad kuvatakse lõppkasutajatele lisamise järjekorras.</span><span class="sxs-lookup"><span data-stu-id="ce446-214">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="ce446-215">Ainus võimalus väljade järjestust muuta on kõik väljad uuesti valida.</span><span class="sxs-lookup"><span data-stu-id="ce446-215">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="ce446-216">Selle stsenaariumi nõuete põhjal on vaja järgmist kaheksat välja.</span><span class="sxs-lookup"><span data-stu-id="ce446-216">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="ce446-217">Kuid mõned kasutajad võivad leida, et kaheksa välja on mobiilsel seadmel liiga palju teavet.</span><span class="sxs-lookup"><span data-stu-id="ce446-217">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="ce446-218">Seega näitame mobiili loendivaates ainult kõige olulisemaid välju.</span><span class="sxs-lookup"><span data-stu-id="ce446-218">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="ce446-219">Ülejäänud väljad kuvatakse üksikasjavaates, mille kujundame hiljem.</span><span class="sxs-lookup"><span data-stu-id="ce446-219">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="ce446-220">Praegu lisame järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="ce446-220">For now, we will add the following fields.</span></span> <span data-ttu-id="ce446-221">Klõpsake plussmärki (**+**) nende veergude mobiililehele lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="ce446-221">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="ce446-222">Hankija nimi</span><span class="sxs-lookup"><span data-stu-id="ce446-222">Vendor name</span></span>
    - <span data-ttu-id="ce446-223">Arve summa</span><span class="sxs-lookup"><span data-stu-id="ce446-223">Invoice total</span></span>
    - <span data-ttu-id="ce446-224">Maksja</span><span class="sxs-lookup"><span data-stu-id="ce446-224">Invoice account</span></span>
    - <span data-ttu-id="ce446-225">Arve number</span><span class="sxs-lookup"><span data-stu-id="ce446-225">Invoice number</span></span>
    - <span data-ttu-id="ce446-226">Arve kuupäev</span><span class="sxs-lookup"><span data-stu-id="ce446-226">Invoice date</span></span>

    <span data-ttu-id="ce446-227">Pärast väljade lisamist peab mobiilileht sarnanema järgmisele illustratsioonile.</span><span class="sxs-lookup"><span data-stu-id="ce446-227">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    <span data-ttu-id="ce446-228">[![Leht pärast väljade lisamist](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="ce446-228">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>
9.  <span data-ttu-id="ce446-229">Nüüd tuleb lisada ka järgmised väljad, et hiljem saaks töövootoimingud lubada.</span><span class="sxs-lookup"><span data-stu-id="ce446-229">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="ce446-230">Kuva lõpetamise ülesanne</span><span class="sxs-lookup"><span data-stu-id="ce446-230">Show complete task</span></span>
    - <span data-ttu-id="ce446-231">Kuva delegeerimise ülesanne</span><span class="sxs-lookup"><span data-stu-id="ce446-231">Show delegate task</span></span>
    - <span data-ttu-id="ce446-232">Kuva tagasikutsumise ülesanne</span><span class="sxs-lookup"><span data-stu-id="ce446-232">Show recall task</span></span>
    - <span data-ttu-id="ce446-233">Kuva tagasilükkamise ülesanne</span><span class="sxs-lookup"><span data-stu-id="ce446-233">Show reject task</span></span>
    - <span data-ttu-id="ce446-234">Kuva taotluse täitmise ülesanne</span><span class="sxs-lookup"><span data-stu-id="ce446-234">Show request completion task</span></span>
    - <span data-ttu-id="ce446-235">Kuva uuesti esitamise ülesanne</span><span class="sxs-lookup"><span data-stu-id="ce446-235">Show resubmit task</span></span>

10. <span data-ttu-id="ce446-236">Redigeerimisrežiimist väljumiseks klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="ce446-236">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="ce446-237">Klõpsake nuppu **Tagasi** ja seejärel nuppu **Valmis** tööruumist väljumiseks</span><span class="sxs-lookup"><span data-stu-id="ce446-237">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="ce446-238">Töö salvestamiseks klõpsake nuppu **Avalda tööruum**</span><span class="sxs-lookup"><span data-stu-id="ce446-238">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="ce446-239">Lubage ostureskontro vormi jaotises **Arve** valik **Kuva ootel hankija arvete loendis arve koondsumma**.</span><span class="sxs-lookup"><span data-stu-id="ce446-239">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="ce446-240">Pange tähele, et arve koondsummad arvutatakse ootel hankija arvete loendilehel kuvamiseks ainult selle parameetri lubamisel.</span><span class="sxs-lookup"><span data-stu-id="ce446-240">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="ce446-241">See on uus võimalus, mis kuulub eeltingimuseks olevasse kiirparandusse 3208224.</span><span class="sxs-lookup"><span data-stu-id="ce446-241">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="ce446-242">Hankija arve andmed</span><span class="sxs-lookup"><span data-stu-id="ce446-242">Vendor invoice details</span></span>

<span data-ttu-id="ce446-243">Arve üksikasjade lehe kujundamiseks mobiiliversioonile kasutage lehte **VendMobileInvoiceHeaderDetails** Finance and Operationsis.</span><span class="sxs-lookup"><span data-stu-id="ce446-243">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page in Finance and Operations.</span></span> <span data-ttu-id="ce446-244">Pange tähele, et olenevalt sellest, kui palju arveid on teile teie süsteemis määratud, kuvatakse sellel lehel vanim arve (esimesena koostatud arve).</span><span class="sxs-lookup"><span data-stu-id="ce446-244">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="ce446-245">Konkreetse arve otsimiseks võib kasutada vasakul olevat filtrit.</span><span class="sxs-lookup"><span data-stu-id="ce446-245">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="ce446-246">Kuid selle näite puhul pole meil konkreetset arvet vaja.</span><span class="sxs-lookup"><span data-stu-id="ce446-246">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="ce446-247">Meil on lihtsalt vaja mõningaid arveandmeid, et saaksime mobiilset lehte kujundada.</span><span class="sxs-lookup"><span data-stu-id="ce446-247">We just require some invoice data so that we can design the mobile page.</span></span> <span data-ttu-id="ce446-248">[![Töövoo leht](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="ce446-248">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1.  <span data-ttu-id="ce446-249">Asendage Finance and Operationsi URL-is menüüelemendi nimi stringiga **VendMobileInvoiceHeaderDetails** vormi avamiseks</span><span class="sxs-lookup"><span data-stu-id="ce446-249">In the Finance and Operations URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>
2.  <span data-ttu-id="ce446-250">Avage mobiilne kujundaja nupult **Sätted** (hammasratas).</span><span class="sxs-lookup"><span data-stu-id="ce446-250">Open the mobile designer from the **Settings** (gear) button.</span></span>
3.  <span data-ttu-id="ce446-251">Klõpsake tööruumis redigeerimisrežiimi käivitamiseks nuppu **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="ce446-251">Click the **Edit** button to start edit mode in the workspace.</span></span>
4.  <span data-ttu-id="ce446-252">Valige eelnevalt loodud leht **Minu hankija arved** ja klõpsake siis nuppu **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="ce446-252">Select the **My vendor invoices **page that you created earlier, and then click **Edit**.</span></span>
5.  <span data-ttu-id="ce446-253">Klõpsake vahekaardil **Väljad** veerupäist **Ruudustik**.</span><span class="sxs-lookup"><span data-stu-id="ce446-253">On the **Fields** tab, click the **Grid** column heading.</span></span>
6.  <span data-ttu-id="ce446-254">Klõpsake valikuid **Atribuudid** &gt; **Lisa leht**.</span><span class="sxs-lookup"><span data-stu-id="ce446-254">Click **Properties** &gt; **Add page**.</span></span> <span data-ttu-id="ce446-255">**Märkus.** Kui klõpsate pealkirja **Ruudustik** ja lisate lehe, luuakse automaatselt seos üksikasjade lehega.</span><span class="sxs-lookup"><span data-stu-id="ce446-255">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>
7.  <span data-ttu-id="ce446-256">Sisestage lehe pealkiri, nt **Arve üksikasjad** ja kirjeldus, nt **Kuva arve päis ja rea üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="ce446-256">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>
8.  <span data-ttu-id="ce446-257">Klõpsake nuppu **Vali väljad**.</span><span class="sxs-lookup"><span data-stu-id="ce446-257">Click **Select fields**.</span></span> <span data-ttu-id="ce446-258">Pange tähele, et väljad kuvatakse lõppkasutajatele lisamise järjekorras.</span><span class="sxs-lookup"><span data-stu-id="ce446-258">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="ce446-259">Ainus võimalus väljade järjestust muuta on kõik väljad uuesti valida.</span><span class="sxs-lookup"><span data-stu-id="ce446-259">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 
9.  <span data-ttu-id="ce446-260">Lisage selle stsenaariumi nõuete põhjal päisest järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="ce446-260">Add the following fields from the header, based on the requirements for this scenario:</span></span>
    - <span data-ttu-id="ce446-261">Hankija nimi</span><span class="sxs-lookup"><span data-stu-id="ce446-261">Vendor name</span></span>
    - <span data-ttu-id="ce446-262">Arve summa</span><span class="sxs-lookup"><span data-stu-id="ce446-262">Invoice total</span></span>
    - <span data-ttu-id="ce446-263">Maksja</span><span class="sxs-lookup"><span data-stu-id="ce446-263">Invoice account</span></span>
    - <span data-ttu-id="ce446-264">Arve number</span><span class="sxs-lookup"><span data-stu-id="ce446-264">Invoice number</span></span>
    - <span data-ttu-id="ce446-265">Arve kuupäev</span><span class="sxs-lookup"><span data-stu-id="ce446-265">Invoice date</span></span>
    - <span data-ttu-id="ce446-266">Arve kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ce446-266">Invoice description</span></span>
    - <span data-ttu-id="ce446-267">Tähtaeg</span><span class="sxs-lookup"><span data-stu-id="ce446-267">Due date</span></span>
    - <span data-ttu-id="ce446-268">Arve valuuta</span><span class="sxs-lookup"><span data-stu-id="ce446-268">Invoice currency</span></span>

10. <span data-ttu-id="ce446-269">Lisage lehel olevast ridade ruudustikust järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="ce446-269">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="ce446-270">Hankekategooria</span><span class="sxs-lookup"><span data-stu-id="ce446-270">Procurement category</span></span>
    - <span data-ttu-id="ce446-271">Kogus</span><span class="sxs-lookup"><span data-stu-id="ce446-271">Quantity</span></span>
    - <span data-ttu-id="ce446-272">Ühiku hind</span><span class="sxs-lookup"><span data-stu-id="ce446-272">Unit price</span></span>
    - <span data-ttu-id="ce446-273">Rea netosumma</span><span class="sxs-lookup"><span data-stu-id="ce446-273">Line net amount</span></span>
    - <span data-ttu-id="ce446-274">1099-summa</span><span class="sxs-lookup"><span data-stu-id="ce446-274">1099 amount</span></span>

11. <span data-ttu-id="ce446-275">Kui kõik väljad eelmisest kahest toimingust on lisatud, klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="ce446-275">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="ce446-276">Leht peab sarnanema järgmisele illustratsioonile.</span><span class="sxs-lookup"><span data-stu-id="ce446-276">The page must resemble the following illustration.</span></span>
<span data-ttu-id="ce446-277">[![Leht pärast väljade lisamist](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="ce446-277">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>
12. <span data-ttu-id="ce446-278">Redigeerimisrežiimist väljumiseks klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="ce446-278">Click **Done** to exit edit mode.</span></span>
13. <span data-ttu-id="ce446-279">Klõpsake nuppu **Tagasi** ja seejärel nuppu **Valmis** tööruumist väljumiseks</span><span class="sxs-lookup"><span data-stu-id="ce446-279">Click **Back** and then **Done** to exit the workspace</span></span>
14. <span data-ttu-id="ce446-280">Töö salvestamiseks klõpsake nuppu **Avalda tööruum**</span><span class="sxs-lookup"><span data-stu-id="ce446-280">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="ce446-281">Töövoo tegevused</span><span class="sxs-lookup"><span data-stu-id="ce446-281">Workflow actions</span></span>

<span data-ttu-id="ce446-282">Töövootoimingute lisamiseks kasutage lehte **VendMobileInvoiceHeaderDetails** Finance and Operationsis.</span><span class="sxs-lookup"><span data-stu-id="ce446-282">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page in Finance and Operations.</span></span> <span data-ttu-id="ce446-283">Selle lehe avamiseks asendage menüüelemendi nimi URL-is nii, nagu varem tegite.</span><span class="sxs-lookup"><span data-stu-id="ce446-283">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="ce446-284">Seejärel avage mobiilne kujundaja nupult **Sätted** (hammasratas).</span><span class="sxs-lookup"><span data-stu-id="ce446-284">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="ce446-285">Tehke järgmist töövootoimingute lisamiseks üksikasjade lehel.</span><span class="sxs-lookup"><span data-stu-id="ce446-285">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="ce446-286">Teile peavad olema määratud sobivas olekus arved, mis teevad teile kättesaadavaks need töövootegevused, mille kujundamisega tegelete.</span><span class="sxs-lookup"><span data-stu-id="ce446-286">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="ce446-287">Töövoo tegevuste registreerimine</span><span class="sxs-lookup"><span data-stu-id="ce446-287">Record workflow actions</span></span>
1.  <span data-ttu-id="ce446-288">Klõpsake tööruumis redigeerimisrežiimi käivitamiseks nuppu **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="ce446-288">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="ce446-289">Valige eelnevalt loodud leht **Arve üksikasjad** ja klõpsake siis nuppu **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="ce446-289">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="ce446-290">Klõpsake vahekaardil **Tegevused** käsku **Lisa tegevus**.</span><span class="sxs-lookup"><span data-stu-id="ce446-290">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="ce446-291">Sisestage tegevuse pealkiri, nt **Kinnitamine**, ja kirjeldus, nt **Arve kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="ce446-291">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="ce446-292">Pange tähele, et sisestatud tegevuse pealkirjast saab tegevuse nimi, mida kasutajale mobiilirakenduses näidatakse.</span><span class="sxs-lookup"><span data-stu-id="ce446-292">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="ce446-293">Klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="ce446-293">Click **Done**.</span></span>
6.  <span data-ttu-id="ce446-294">Klõpsake nuppu **Vali väljad**.</span><span class="sxs-lookup"><span data-stu-id="ce446-294">Click **Select fields**.</span></span>
7.  <span data-ttu-id="ce446-295">Läbige töövooprotsess lehel **VendMobileInvoiceHeaderDetails** ja tehke tegevus, mida soovisite registreerida.</span><span class="sxs-lookup"><span data-stu-id="ce446-295">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="ce446-296">Veenduge, et sisestate selle protsessi käigus töövoo kommentaarid, nii et kommentaaride väli lisatakse samuti mobiiliversiooni.</span><span class="sxs-lookup"><span data-stu-id="ce446-296">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="ce446-297">Pärast töövootegevuse käitamist klõpsake väljade valimise ülesande lõpetamiseks nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="ce446-297">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="ce446-298">Redigeerimisrežiimist väljumiseks klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="ce446-298">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="ce446-299">Klõpsake nuppu **Tagasi** ja seejärel nuppu **Valmis** tööruumist väljumiseks</span><span class="sxs-lookup"><span data-stu-id="ce446-299">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="ce446-300">Töö salvestamiseks klõpsake nuppu **Avalda tööruum**</span><span class="sxs-lookup"><span data-stu-id="ce446-300">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="ce446-301">Korrake eelmisi toiminguid kõigi vajalike töövootegevuste registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="ce446-301">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="ce446-302">Looge JS-fail</span><span class="sxs-lookup"><span data-stu-id="ce446-302">Create a .js file</span></span>
1. <span data-ttu-id="ce446-303">Avage Notepad või Microsoft Visual Studio ja kleepige sinna järgmine kood.</span><span class="sxs-lookup"><span data-stu-id="ce446-303">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="ce446-304">Salvestage fail JS-failina.</span><span class="sxs-lookup"><span data-stu-id="ce446-304">Save the file as a .js file.</span></span> <span data-ttu-id="ce446-305">See kood teeb järgmist.</span><span class="sxs-lookup"><span data-stu-id="ce446-305">This code does the following:</span></span>
    - <span data-ttu-id="ce446-306">See peidab töövooga seotud lisaveerud, mille varem mobiili loendilehel lisasime.</span><span class="sxs-lookup"><span data-stu-id="ce446-306">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="ce446-307">Lisasime need veerud selleks, et rakendusel oleks see teave kontekstis olemas ja see saaks teha järgmise toimingu.</span><span class="sxs-lookup"><span data-stu-id="ce446-307">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="ce446-308">Aktiivse töövooetapi põhjal rakendab see loogikat ainult nende tegevuste näitamiseks.</span><span class="sxs-lookup"><span data-stu-id="ce446-308">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

> [!NOTE]
> <span data-ttu-id="ce446-309">Lehtede ja muude juhtelementide nimed JS-koodis peavad olema samad, mis tööruumis.</span><span class="sxs-lookup"><span data-stu-id="ce446-309">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

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

2.  <span data-ttu-id="ce446-310">Laadige koodifail tööruumi üles, valides vahekaardi **Loogika**</span><span class="sxs-lookup"><span data-stu-id="ce446-310">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="ce446-311">Redigeerimisrežiimist väljumiseks klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="ce446-311">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="ce446-312">Klõpsake nuppu **Tagasi** ja seejärel nuppu **Valmis** tööruumist väljumiseks</span><span class="sxs-lookup"><span data-stu-id="ce446-312">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="ce446-313">Töö salvestamiseks klõpsake nuppu **Avalda tööruum**</span><span class="sxs-lookup"><span data-stu-id="ce446-313">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="ce446-314">Hankija arve manused</span><span class="sxs-lookup"><span data-stu-id="ce446-314">Vendor invoice attachments</span></span>

1.  <span data-ttu-id="ce446-315">Klõpsake nuppu **Sätted** (hammasratas) lehe ülemises paremas osas ja seejärel valikut **Mobiilirakendus**</span><span class="sxs-lookup"><span data-stu-id="ce446-315">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
2.  <span data-ttu-id="ce446-316">Klõpsake tööruumis redigeerimisrežiimi käivitamiseks nuppu **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="ce446-316">Click the **Edit** button to start edit mode in the workspace.</span></span>
3.  <span data-ttu-id="ce446-317">Valige eelnevalt loodud leht **Arve üksikasjad** ja klõpsake siis nuppu **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="ce446-317">Select the **Invoice details **page that you created earlier, and then click **Edit**.</span></span>
4.  <span data-ttu-id="ce446-318">Määrake valiku **Dokumendihaldus** sätteks **Jah**, nagu allpool näidatud.</span><span class="sxs-lookup"><span data-stu-id="ce446-318">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="ce446-319">**Märkus.** Kui puuduvad nõuded mobiilsel seadmel manuste näitamiseks, võite jätta selle valiku sätteks **Ei**, mis on vaikesäte.</span><span class="sxs-lookup"><span data-stu-id="ce446-319">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
<span data-ttu-id="ce446-320">![Dokumendihaldus](./media/docmanagement-216x300.png)</span><span class="sxs-lookup"><span data-stu-id="ce446-320">![Document management](./media/docmanagement-216x300.png)</span></span>
6.  <span data-ttu-id="ce446-321">Redigeerimisrežiimist väljumiseks klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="ce446-321">Click **Done** to exit edit mode.</span></span>
7.  <span data-ttu-id="ce446-322">Klõpsake nuppu **Tagasi** ja seejärel nuppu **Valmis** tööruumist väljumiseks</span><span class="sxs-lookup"><span data-stu-id="ce446-322">Click **Back** and then **Done** to exit the workspace</span></span>
8.  <span data-ttu-id="ce446-323">Töö salvestamiseks klõpsake nuppu **Avalda tööruum**</span><span class="sxs-lookup"><span data-stu-id="ce446-323">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="ce446-324">Hankija arve rea jaotused</span><span class="sxs-lookup"><span data-stu-id="ce446-324">Vendor invoice line distributions</span></span>

<span data-ttu-id="ce446-325">Selle stsenaariumi nõudmised kinnitavad, et olemas on ainult rea tasemel jaotused ja et arvel on alati ainult üks rida.</span><span class="sxs-lookup"><span data-stu-id="ce446-325">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="ce446-326">Kuna see stsenaarium on lihtne, peab kasutaja kogemus mobiilsel seadmel olema samuti piisavalt lihtne, et kasutaja ei peaks jaotuste vaatamiseks mitme taseme võrra süvitsi minema.</span><span class="sxs-lookup"><span data-stu-id="ce446-326">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="ce446-327">Hankija arved Finance and Operationsis sisaldavad võimalust kuvada kõik jaotused arve päisest.</span><span class="sxs-lookup"><span data-stu-id="ce446-327">Vendor invoices in Finance and Operations include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="ce446-328">Seda me mobiilistsenaariumi puhul vajamegi.</span><span class="sxs-lookup"><span data-stu-id="ce446-328">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="ce446-329">Seetõttu kasutame selle mobiilistsenaariumi osa kujundamiseks lehte **VendMobileInvoiceAllDistributionTree**.</span><span class="sxs-lookup"><span data-stu-id="ce446-329">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="ce446-330">Nõuetega kursis olemine aitab meil stsenaariumi kujundamisel otsustada, millist konkreetset lehte kasutada ja kuidas täpselt kasutaja mobiilikogemust optimeerida.</span><span class="sxs-lookup"><span data-stu-id="ce446-330">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="ce446-331">Teises stsenaariumis kasutame teist lehte jaotuste näitamiseks, kuna selle stsenaariumi nõuded on erinevad.</span><span class="sxs-lookup"><span data-stu-id="ce446-331">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="ce446-332">Asendage menüüelemendi nimi URL-is nii, nagu enne tegite.</span><span class="sxs-lookup"><span data-stu-id="ce446-332">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="ce446-333">Kuvatav leht peab sarnanema järgmisele illustratsioonile.</span><span class="sxs-lookup"><span data-stu-id="ce446-333">The page that appears should resemble the following illustration.</span></span>
<span data-ttu-id="ce446-334">[![Kõigi jaotuste leht](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="ce446-334">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>
2.  <span data-ttu-id="ce446-335">Avage mobiilne kujundaja nupult **Sätted** (hammasratas).</span><span class="sxs-lookup"><span data-stu-id="ce446-335">Open the mobile designer from the **Settings** (gear) button.</span></span>
3.  <span data-ttu-id="ce446-336">Klõpsake tööruumis redigeerimisrežiimi käivitamiseks nuppu **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="ce446-336">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="ce446-337">**Märkus.** Näete, et automaatselt loodi kaks uut lehte.</span><span class="sxs-lookup"><span data-stu-id="ce446-337">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="ce446-338">Süsteem loob need lehed, kuna lülitasite eelmises jaotises sisse dokumendihalduse.</span><span class="sxs-lookup"><span data-stu-id="ce446-338">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="ce446-339">Võite neid uusi lehti eirata.</span><span class="sxs-lookup"><span data-stu-id="ce446-339">You can ignore these new pages.</span></span>
4.  <span data-ttu-id="ce446-340">Klõpsake nuppu **Lisa leht**.</span><span class="sxs-lookup"><span data-stu-id="ce446-340">Click **Add page**.</span></span>
5.  <span data-ttu-id="ce446-341">Sisestage lehe pealkiri, nt **Arvestuse kuvamine** ja kirjeldus, nt **Arve arvestuse kuvamine**.</span><span class="sxs-lookup"><span data-stu-id="ce446-341">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>
6.  <span data-ttu-id="ce446-342">Klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="ce446-342">Click **Done**.</span></span>
7.  <span data-ttu-id="ce446-343">Klõpsake vahekaardil **Väljad** valikut **Vali väljad**, valige jaotuste lehelt järgmised väljad ja klõpsake seejärel nuppu **Valmis**:</span><span class="sxs-lookup"><span data-stu-id="ce446-343">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="ce446-344">Summa</span><span class="sxs-lookup"><span data-stu-id="ce446-344">Amount</span></span>
    2.  <span data-ttu-id="ce446-345">Valuuta</span><span class="sxs-lookup"><span data-stu-id="ce446-345">Currency</span></span>
    3.  <span data-ttu-id="ce446-346">Pearaamatukonto</span><span class="sxs-lookup"><span data-stu-id="ce446-346">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="ce446-347">Me ei valinud jaotuste ruudustikust veergu **Kirjeldus**, kuna selle stsenaariumi nõuded kinnitasid, et laiendatud hind on ainus summa, mille jaoks jaotused olemas on.</span><span class="sxs-lookup"><span data-stu-id="ce446-347">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="ce446-348">Seega ei vaja kasutaja teist välja summa tüübi määramiseks, mille jaoks jaotus on mõeldud.</span><span class="sxs-lookup"><span data-stu-id="ce446-348">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="ce446-349">Kuid järgmises stsenaariumis **kasutame** seda teavet, kuna selle stsenaariumi nõuded määravad, et teistel summatüüpidel on jaotused (nt käibemaks).</span><span class="sxs-lookup"><span data-stu-id="ce446-349">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>
8.  <span data-ttu-id="ce446-350">Redigeerimisrežiimist väljumiseks klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="ce446-350">Click **Done** to exit edit mode.</span></span>
9.  <span data-ttu-id="ce446-351">Klõpsake nuppu **Tagasi** ja seejärel nuppu **Valmis** tööruumist väljumiseks</span><span class="sxs-lookup"><span data-stu-id="ce446-351">Click **Back** and then **Done** to exit the workspace</span></span>
10. <span data-ttu-id="ce446-352">Töö salvestamiseks klõpsake nuppu **Avalda tööruum**</span><span class="sxs-lookup"><span data-stu-id="ce446-352">Click **Publish workspace** to save your work</span></span>

> [!NOTE] 
> <span data-ttu-id="ce446-353">Mobiilileht **Arvestuse kuvamine** pole praegu seotud ühegi mobiililehega, mille seni kujundanud oleme.</span><span class="sxs-lookup"><span data-stu-id="ce446-353">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="ce446-354">Kuna kasutaja peab saama liikuda lehele **Arvestuse kuvamine** mobiilse seadme lehelt **Arve üksikasjad**, peame pakkuma võimalust liikuda lehelt **Arve üksikasjad** lehele **Arvestuse kuvamine**.</span><span class="sxs-lookup"><span data-stu-id="ce446-354">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="ce446-355">Tekitame selle liikumisvõimaluse, kasutades JavaScripti kaudu lisaloogikat.</span><span class="sxs-lookup"><span data-stu-id="ce446-355">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="ce446-356">Avage varem loodud JS-fail ja lisage read, mis tõstetakse esile järgmises koodis.</span><span class="sxs-lookup"><span data-stu-id="ce446-356">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="ce446-357">See kood teeb kahte asja.</span><span class="sxs-lookup"><span data-stu-id="ce446-357">This code does two things:</span></span>
    1.  <span data-ttu-id="ce446-358">See aitab garanteerida, et kasutajad ei saa liikuda otse tööruumist lehele **Arvestuse kuvamine**.</span><span class="sxs-lookup"><span data-stu-id="ce446-358">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="ce446-359">See tekitab navigeerimisnupu lehelt **Arve üksikasjad** lehele **Arvestuse kuvamine**.</span><span class="sxs-lookup"><span data-stu-id="ce446-359">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

> [!NOTE] 
> <span data-ttu-id="ce446-360">Lehtede ja muude juhtelementide nimed JS-koodis peavad olema samad, mis tööruumis.</span><span class="sxs-lookup"><span data-stu-id="ce446-360">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

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

2.  <span data-ttu-id="ce446-361">Eelmise koodi ülekirjutamiseks laadige koodifail tööruumi üles, valides vahekaardi **Loogika**</span><span class="sxs-lookup"><span data-stu-id="ce446-361">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="ce446-362">Redigeerimisrežiimist väljumiseks klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="ce446-362">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="ce446-363">Klõpsake nuppu **Tagasi** ja seejärel nuppu **Valmis** tööruumist väljumiseks</span><span class="sxs-lookup"><span data-stu-id="ce446-363">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="ce446-364">Töö salvestamiseks klõpsake nuppu **Avalda tööruum**</span><span class="sxs-lookup"><span data-stu-id="ce446-364">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="ce446-365">Kinnitamine</span><span class="sxs-lookup"><span data-stu-id="ce446-365">Validation</span></span>

<span data-ttu-id="ce446-366">Avage rakendus oma mobiilses seadmes ja looge ühendus oma Finance and Operationsi eksemplariga.</span><span class="sxs-lookup"><span data-stu-id="ce446-366">From your mobile device, open the app, and connect to your Finance and Operations instance.</span></span> <span data-ttu-id="ce446-367">Veenduge, et logiksite sisse ettevõttesse, kus teile on määratud ülevaatamiseks hankija arved.</span><span class="sxs-lookup"><span data-stu-id="ce446-367">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="ce446-368">Teil peaks olema võimalik teha järgmisi toiminguid.</span><span class="sxs-lookup"><span data-stu-id="ce446-368">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="ce446-369">Vaadake tööruumi **Minu kinnitused**.</span><span class="sxs-lookup"><span data-stu-id="ce446-369">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="ce446-370">Minge tööruumis **Minu kinnitused** süvitsi ja vaadake lehte **Minu hankija arved**.</span><span class="sxs-lookup"><span data-stu-id="ce446-370">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="ce446-371">Minge tööruumis **Minu hankija arved** süvitsi ja vaadake endale määratud arvete loendit.</span><span class="sxs-lookup"><span data-stu-id="ce446-371">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="ce446-372">Minge mõnes arves süvitsi ja vaadake arve päise üksikasju ja rea üksikasju.</span><span class="sxs-lookup"><span data-stu-id="ce446-372">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="ce446-373">Vaadake üksikasjade lehel linki manuste juurde ja minge selle lingi abil manuste loendisse ning vaadake manuseid.</span><span class="sxs-lookup"><span data-stu-id="ce446-373">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="ce446-374">Vaadake üksikasjade lehel linki lehele **Arvestuse kuvamine** ja minge selle lingi abil jaotuste lehele ning vaadake jaotusi.</span><span class="sxs-lookup"><span data-stu-id="ce446-374">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="ce446-375">Klõpsake üksikasjade lehe allosas menüüd **Tegevused** ja tehke töövooetappi puudutavad töövootegevused.</span><span class="sxs-lookup"><span data-stu-id="ce446-375">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="ce446-376">Keeruka arve kinnitamise stsenaariumi kujundamine Fabrikami jaoks</span><span class="sxs-lookup"><span data-stu-id="ce446-376">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce446-377">Stsenaariumi atribuut</span><span class="sxs-lookup"><span data-stu-id="ce446-377">Scenario attribute</span></span></th>
<th><span data-ttu-id="ce446-378">Vastus</span><span class="sxs-lookup"><span data-stu-id="ce446-378">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce446-379">Milliseid arve päise välju soovib kasutaja mobiiliversioonis näha ja millises järjekorras?</span><span class="sxs-lookup"><span data-stu-id="ce446-379">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="ce446-380">Hankija nimi</span><span class="sxs-lookup"><span data-stu-id="ce446-380">Vendor name</span></span></li>
<li><span data-ttu-id="ce446-381">Arve summa</span><span class="sxs-lookup"><span data-stu-id="ce446-381">Invoice amount</span></span></li>
<li><span data-ttu-id="ce446-382">Maksja</span><span class="sxs-lookup"><span data-stu-id="ce446-382">Invoice account</span></span></li>
<li><span data-ttu-id="ce446-383">Arve number</span><span class="sxs-lookup"><span data-stu-id="ce446-383">Invoice number</span></span></li>
<li><span data-ttu-id="ce446-384">Arve kuupäev</span><span class="sxs-lookup"><span data-stu-id="ce446-384">Invoice date</span></span></li>
<li><span data-ttu-id="ce446-385">Arve kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ce446-385">Invoice description</span></span></li>
<li><span data-ttu-id="ce446-386">Tähtaeg</span><span class="sxs-lookup"><span data-stu-id="ce446-386">Due date</span></span></li>
<li><span data-ttu-id="ce446-387">Arve valuuta</span><span class="sxs-lookup"><span data-stu-id="ce446-387">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce446-388">Milliseid arve ridade välju soovib kasutaja mobiiliversioonis näha ja millises järjekorras?</span><span class="sxs-lookup"><span data-stu-id="ce446-388">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="ce446-389">Hankekategooria</span><span class="sxs-lookup"><span data-stu-id="ce446-389">Procurement category</span></span></li>
<li><span data-ttu-id="ce446-390">Kogus</span><span class="sxs-lookup"><span data-stu-id="ce446-390">Quantity</span></span></li>
<li><span data-ttu-id="ce446-391">Ühiku hind</span><span class="sxs-lookup"><span data-stu-id="ce446-391">Unit price</span></span></li>
<li><span data-ttu-id="ce446-392">Rea netosumma</span><span class="sxs-lookup"><span data-stu-id="ce446-392">Line net amount</span></span></li>
<li><span data-ttu-id="ce446-393">1099-summa</span><span class="sxs-lookup"><span data-stu-id="ce446-393">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce446-394">Mitu arverida arvel on?</span><span class="sxs-lookup"><span data-stu-id="ce446-394">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="ce446-395">Rakendage siin 80-20 reeglit ja optimeerige 80 protsendi jaoks.</span><span class="sxs-lookup"><span data-stu-id="ce446-395">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="ce446-396">5</span><span class="sxs-lookup"><span data-stu-id="ce446-396">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce446-397">Kas kasutajad soovivad arvestuse jaotusi (arvekoode) ülevaatamise ajal mobiilsel seadmel näha?</span><span class="sxs-lookup"><span data-stu-id="ce446-397">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="ce446-398">Jah</span><span class="sxs-lookup"><span data-stu-id="ce446-398">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce446-399">Kui palju arvestuse jaotusi (laiendatud hind, käibemaks, tasud jne) arve real on?</span><span class="sxs-lookup"><span data-stu-id="ce446-399">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="ce446-400">Rakendage jällegi 80-20 reeglit.</span><span class="sxs-lookup"><span data-stu-id="ce446-400">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="ce446-401">Laiendatud hind: 2 Käibemaks: 2 Tasud: 2</span><span class="sxs-lookup"><span data-stu-id="ce446-401">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce446-402">Kas arvete päises on ka arvestuse jaotused?</span><span class="sxs-lookup"><span data-stu-id="ce446-402">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="ce446-403">Kui nii, siis kas need arvestuse jaotused peaksid seadmel kättesaadavad olema?</span><span class="sxs-lookup"><span data-stu-id="ce446-403">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="ce446-404">Pole kasutusel</span><span class="sxs-lookup"><span data-stu-id="ce446-404">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce446-405">Kas kasutajad soovivad seadmel arve manuseid näha?</span><span class="sxs-lookup"><span data-stu-id="ce446-405">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="ce446-406">Jah</span><span class="sxs-lookup"><span data-stu-id="ce446-406">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="ce446-407">Järgmised sammud</span><span class="sxs-lookup"><span data-stu-id="ce446-407">Next steps</span></span>

<span data-ttu-id="ce446-408">1. stsenaariumi puhul saab kasutada järgmisi variatsioone, tuginedes 2. stsenaariumi nõuetele.</span><span class="sxs-lookup"><span data-stu-id="ce446-408">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="ce446-409">Selle jaotise abil saate parandada oma mobiilirakenduse kogemust.</span><span class="sxs-lookup"><span data-stu-id="ce446-409">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="ce446-410">Kuna 2. stsenaariumi puhul eeldatakse suuremat arve ridade arvu, aitavad järgmised kujunduse muudatused kasutajakogemust mobiilsel seadmel optimeerida.</span><span class="sxs-lookup"><span data-stu-id="ce446-410">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="ce446-411">Arve ridade vaatamise asemel üksikasjade lehel (nagu 1. stsenaariumis) võivad kasutajad valida ridade vaatamise eraldi mobiililehel.</span><span class="sxs-lookup"><span data-stu-id="ce446-411">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="ce446-412">Kuna selles stsenaariumis eeldatakse mitut arve rida, siis kui mobiili jaotuste lehe kujundamiseks kasutatakse lehte **VendMobileInvoiceAllDistributionTree** (nagu 1. stsenaariumis), võib ridade seostamine jaotustega kasutajale segadust tekitada.</span><span class="sxs-lookup"><span data-stu-id="ce446-412">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="ce446-413">Seetõttu kasutage jaotuste lehe kujundamiseks lehte **VendMobileInvoiceLineDistributionTree**.</span><span class="sxs-lookup"><span data-stu-id="ce446-413">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="ce446-414">Ideaaljuhul tuleks jaotusi näidata selles stsenaariumis arve rea kontekstis.</span><span class="sxs-lookup"><span data-stu-id="ce446-414">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="ce446-415">Seega veenduge, et kasutaja saab jaotuste lehe vaatamiseks reas süvitsi minna.</span><span class="sxs-lookup"><span data-stu-id="ce446-415">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="ce446-416">Kasutage lehe lingivõimalust süvaaruande koostamiseks, nagu tegite päise ja üksikasjade lehtedel 1. stsenaariumis.</span><span class="sxs-lookup"><span data-stu-id="ce446-416">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="ce446-417">Kuna 2. stsenaariumi puhul eeldatakse mitut summa tüüpi (käibemaks, tasud jne), on kasulik näidata summa tüübi kirjeldust.</span><span class="sxs-lookup"><span data-stu-id="ce446-417">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="ce446-418">(Jätsime selle teabe 1. stsenaariumist välja.)</span><span class="sxs-lookup"><span data-stu-id="ce446-418">(We omitted this information in scenario 1.)</span></span>





