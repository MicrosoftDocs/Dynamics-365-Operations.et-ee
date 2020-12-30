---
title: Pakkumiste halduse seadistamine rakenduses Attract
description: Selles teemas kirjeldatakse, kuidas rakenduses Microsoft Dynamics 365 Talent pakkumisi seadistada.
author: andreabichsel
manager: AnnBe
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc91a83afd5ce1627376685bcf612d6998ddbc02
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460914"
---
# <a name="set-up-offer-management-in-attract"></a><span data-ttu-id="e8b06-103">Pakkumiste halduse seadistamine rakenduses Attract</span><span class="sxs-lookup"><span data-stu-id="e8b06-103">Set up offer management in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e8b06-104">Kui kandidaat viiakse rakenduses Dynamics 365 Talent: Attract pakkumise etappi, peate tagama, et pakkumisi saab kandidaadi jaoks kiiresti luua, vajadusel kinnitada ja kandidaadile saata.</span><span class="sxs-lookup"><span data-stu-id="e8b06-104">When a candidate is moved to the offer stage in Dynamics 365 Talent: Attract, you need to ensure that the offers can be quickly created for the candidate, approved as necessary, and sent out to the candidate.</span></span> <span data-ttu-id="e8b06-105">Kuna enamik pakkumisi on standardsed, saab neid luua korduvkasutatavate mallidega.</span><span class="sxs-lookup"><span data-stu-id="e8b06-105">Because most offers are standard, they can be created from reusable templates.</span></span> <span data-ttu-id="e8b06-106">Rakenduses Attract on kõik pakkumised koos pakkumise paketis, mis on ühest või enama pakkumisdokumendiga kogum.</span><span class="sxs-lookup"><span data-stu-id="e8b06-106">In Attract, all offers are rolled into an offer package, which is a collection of one or more offer documents.</span></span> 

<span data-ttu-id="e8b06-107">Selles teemas loetletakse kõik etapid, mida Attracti administraator peab järgima, et seadistada erinevad pakkumise paketi mallid osana Attracti pakkumiste haldamise võimalusest.</span><span class="sxs-lookup"><span data-stu-id="e8b06-107">This topic lists all the steps that an Attract administrator would follow to set up different offer package templates as part of the offer management capability in Attract.</span></span> <span data-ttu-id="e8b06-108">Administraatori rollita kasutajatel puudub juurdepääs nendele võimalustele.</span><span class="sxs-lookup"><span data-stu-id="e8b06-108">Users with non-administrator roles will not have access to these capabilities.</span></span>

>[!NOTE]
> <span data-ttu-id="e8b06-109">Pakkumise haldamise võimalused on saadaval osana tervikliku värbamise lisandmoodulist.</span><span class="sxs-lookup"><span data-stu-id="e8b06-109">Offer management capabilities are available as part of the Comprehensive Hiring Add-On.</span></span>

## <a name="offer-data"></a><span data-ttu-id="e8b06-110">Pakkumisandmed</span><span class="sxs-lookup"><span data-stu-id="e8b06-110">Offer data</span></span> 

<span data-ttu-id="e8b06-111">Pakkumisandmed on pakkumise paketi malli väikseim üksus.</span><span class="sxs-lookup"><span data-stu-id="e8b06-111">Offer data is the smallest unit inside the offer package template.</span></span> <span data-ttu-id="e8b06-112">Tavaline pakkumine koosneb standardsest tekstist ja väärtuste komplektist.</span><span class="sxs-lookup"><span data-stu-id="e8b06-112">A typical offer consists of standard text and a set of values.</span></span> <span data-ttu-id="e8b06-113">Väärtuste komplektid on ainsad asjad, mis võivad pakkumiste vahel muutuda.</span><span class="sxs-lookup"><span data-stu-id="e8b06-113">The sets of values are the only pieces that could change between offers.</span></span> <span data-ttu-id="e8b06-114">Pakkumise loomise ajal on kõige olulisem aspekt, millele pakkumise looja saab keskenduda, pakkumise paketi mallis olev pakkumisandmete kohatäidete loend.</span><span class="sxs-lookup"><span data-stu-id="e8b06-114">During the offer creation, the most important aspect that the offer creator can focus on is the list of offer data placeholders present in an offer package template.</span></span> <span data-ttu-id="e8b06-115">Pakkumisandmete seadistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e8b06-115">To set up offer data, do the following.</span></span>

1.  <span data-ttu-id="e8b06-116">Valige **Pakkumise haldamine**</span><span class="sxs-lookup"><span data-stu-id="e8b06-116">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="e8b06-117">Laiendage jaotist **Teek** vasakul navigeerimispaanil, seejärel avage **Pakkumisandmed**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-117">Expand the **Library** section in the left navigation pane, then go to **Offer data**.</span></span>

    >[!NOTE]
    > <span data-ttu-id="e8b06-118">**Pakkumisandmete** lehel on **Kandidaadi andmete** ja **Töö üksikasjade** jaotised.</span><span class="sxs-lookup"><span data-stu-id="e8b06-118">On the **Offer data** page are the **Candidate details** and **Job details** sections.</span></span> <span data-ttu-id="e8b06-119">Attract pakub ka mõned nö. kastist väljaspool pakkumisandmete kohatäited.</span><span class="sxs-lookup"><span data-stu-id="e8b06-119">Attract provides a few offer data placeholders out-of-the-box.</span></span>
    > 
    > <span data-ttu-id="e8b06-120">Lehel on jaotised erinevate pakkumisandmete kohatäidete korraldamiseks loogilistesse gruppidesse.</span><span class="sxs-lookup"><span data-stu-id="e8b06-120">There are sections on the page to organize different offer data placeholders together in logical groups.</span></span> <span data-ttu-id="e8b06-121">Need jaotised aitavad pakkumise loomise protsessis säilitada pakkumisandmeid ja andmeid asustada.</span><span class="sxs-lookup"><span data-stu-id="e8b06-121">These sections can help with maintenance of offer data and population of data during the offer creation process.</span></span>
    > 
    > <span data-ttu-id="e8b06-122">Kohatäitele väärtuste loendi loomiseks laadige üles Exceli arvutustabel, kus on üks veerg kohatäitega veeru pealkirjana ja valikute loendiga all olevatel ridadel.</span><span class="sxs-lookup"><span data-stu-id="e8b06-122">To create a list of values for a placeholder, upload an Excel spreadsheet that has one column with the placeholder as the column title and the list of choices in the rows underneath.</span></span> <span data-ttu-id="e8b06-123">Kui samale kohatäitele viidatakse teises andmete reeglistikus, veenduge, et neil oleks ühine väärtuste kogum.</span><span class="sxs-lookup"><span data-stu-id="e8b06-123">If the same placeholder is referenced in another data rule set, ensure they have a common set of values.</span></span>
    
1.  <span data-ttu-id="e8b06-124">Uue pakkumisandmete jaotise loomiseks klõpsake **Jaotise lisamine** ja sisestage jaotisele kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="e8b06-124">To create a new offer data section, click **Add a section** and enter a unique name for the section.</span></span>

1.  <span data-ttu-id="e8b06-125">Mis tahes jaotisele pakkumisandmete kohatäite lisamiseks klõpsake **Pakkumisandmete lisamine** ja sisestage kohatäitele kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="e8b06-125">To add offer data placeholders to any section, click **Add offer data** and enter a unique name for the placeholder.</span></span>

1.  <span data-ttu-id="e8b06-126">Jaotise nime muutmiseks liikuge hiirega üle jaotise nime ja värskendage seda.</span><span class="sxs-lookup"><span data-stu-id="e8b06-126">To edit the name of any section, hover over the section name and update the name.</span></span>

1.  <span data-ttu-id="e8b06-127">Mis tahes olemasoleva pakkumisandmete kohatäite nime muutmiseks veenduge kõigepealt, et kohatäide ei ole juba osa mõnest mallist.</span><span class="sxs-lookup"><span data-stu-id="e8b06-127">To edit the name of any existing offer data placeholder, first make sure that the placeholder is not already part of any template.</span></span> <span data-ttu-id="e8b06-128">Seejärel liikuge hiirega üle pakkumisandmete kohatäite nime ja värskendage seda vajadusel.</span><span class="sxs-lookup"><span data-stu-id="e8b06-128">Then, hover over the name of the offer data placeholder and update the name as needed.</span></span>

1. <span data-ttu-id="e8b06-129">Mis tahes olemasoleva pakkumisandmete kohatäite kustutamiseks veenduge kõigepealt, et kohatäide ei ole osa mõnest teisest mallist.</span><span class="sxs-lookup"><span data-stu-id="e8b06-129">To delete an existing offer data placeholder, first make sure that the placeholder is not part of any other template.</span></span> <span data-ttu-id="e8b06-130">Seejärel liikuga hiirega üle kohatäite ja prügikastiikooni kuvamisel klõpsake pakkumisandmete kohatäite kustutamiseks prügikastiikoonil.</span><span class="sxs-lookup"><span data-stu-id="e8b06-130">Then, hover over the placeholder and when the trash can icon appears, click the trash can to delete the offer data placeholder.</span></span>
    >[!NOTE]
    > <span data-ttu-id="e8b06-131">Saate iga pakkumisandme kõrval oleva numbri järgi vaadata, mitme malli osa pakkumisandmete kohatäide on.</span><span class="sxs-lookup"><span data-stu-id="e8b06-131">You can see how many templates an offer data placeholder is part of by the number indicator next to each offer data.</span></span> 

1. <span data-ttu-id="e8b06-132">Mis tahes jaotise kustutamiseks liikuge hiirega üle selle nime.</span><span class="sxs-lookup"><span data-stu-id="e8b06-132">To delete any section, hover over the name.</span></span> <span data-ttu-id="e8b06-133">Kui ükski jaotises olevatest pakkumisandmete kohatäidetest ei ole üheski mallis, saate kustutamiseks klõpsata prügikastiikoonil.</span><span class="sxs-lookup"><span data-stu-id="e8b06-133">If none of the offer data placeholders inside the section appear in any template, you can click the trash can icon to delete it.</span></span> 
    >[!NOTE]
    > <span data-ttu-id="e8b06-134">Jaotise kustutamine kustutab ka kõik jaotises olevad pakkumisandmete kohatäited.</span><span class="sxs-lookup"><span data-stu-id="e8b06-134">Deleting the section will also delete all the offer data placeholders inside that section.</span></span>

<span data-ttu-id="e8b06-135">Kui pakkumisandmete kohatäited on seadistatud, saate neid kasutada igal dokumendimallil.</span><span class="sxs-lookup"><span data-stu-id="e8b06-135">After the offer data placeholders have been set up, you can use them across any document template.</span></span> <span data-ttu-id="e8b06-136">Pakkumisandmete kohatäited ei ole piiratud kindla malliga – sama komplekti saab kasutada kõikides mallides.</span><span class="sxs-lookup"><span data-stu-id="e8b06-136">Offer data placeholders are not restricted to a specific template -- the same set can be used across all templates.</span></span>

## <a name="offer-data-rules"></a><span data-ttu-id="e8b06-137">Pakkumisandmete reeglid</span><span class="sxs-lookup"><span data-stu-id="e8b06-137">Offer data rules</span></span>

<span data-ttu-id="e8b06-138">Enamikel organisatsioonidel on pakkumiste loomise reeglid.</span><span class="sxs-lookup"><span data-stu-id="e8b06-138">Most organization have rules for how offers must be created.</span></span> <span data-ttu-id="e8b06-139">Näiteks võib organisatsioon nõuda, et konkreetse asukoha ja staažitaseme kombinatsiooni maksimaalne aastapalga pakkumine peab olema teatud vahemikus või et uue töötaja pakkumistasemele saab lisada vaid mõned konkreetsed väärtused.</span><span class="sxs-lookup"><span data-stu-id="e8b06-139">For example, an organization may want to require that the maximum annual salary offer for a specific location and seniority level combination has to be within a certain range, or that there are only a few specific values possible for the offer level for the new hire.</span></span> <span data-ttu-id="e8b06-140">Rakendus Attract toetab praegu kõiki selliseid andmereegleid CSV-failiga.</span><span class="sxs-lookup"><span data-stu-id="e8b06-140">Attract currently supports all such data rules using a CSV file.</span></span>

<span data-ttu-id="e8b06-141">Andmereeglite CSV-faili loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e8b06-141">To prepare the data rules CSV file, do the following.</span></span>

1.  <span data-ttu-id="e8b06-142">Määratlege määratud reegli pakkumisandmete kohatäide.</span><span class="sxs-lookup"><span data-stu-id="e8b06-142">Determine the offer data placeholder for the rule set.</span></span> <span data-ttu-id="e8b06-143">Näiteks **Aastapalk**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-143">For example, **Annual Salary**.</span></span>

1.  <span data-ttu-id="e8b06-144">Tuvastage sõltuvad pakkumisandmete kohatäite väärtused.</span><span class="sxs-lookup"><span data-stu-id="e8b06-144">Identify the dependent offer data placeholder values.</span></span> <span data-ttu-id="e8b06-145">Näiteks **Töö asukoht** ja **Tase**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-145">For example, **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="e8b06-146">Määrake veerud 1 ja 2 kui **Töö asukoht** ja **Tase**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-146">Specify columns 1 and 2 as **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="e8b06-147">Vahemiku väärtuse üleslaadimiseks tehke veergudest 3 ja 4 **Aastapalk**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-147">To upload a range value, make columns 3 and 4 **Annual Salary**.</span></span> <span data-ttu-id="e8b06-148">Vahemiku asemel mõne kindla väärtuse üleslaadimiseks tehke vaid veerust 3 **Aastapalk**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-148">To upload a specific value instead of a range, only make column 3 **Annual Salary**.</span></span>

1.  <span data-ttu-id="e8b06-149">Asustage nõutavate rollide põhjal Microsoft Exceli fail.</span><span class="sxs-lookup"><span data-stu-id="e8b06-149">Populate the Microsoft Excel file based on your required roles.</span></span>

1.  <span data-ttu-id="e8b06-150">Tagage, et iga rida on kõigi kokkupandud väärtuste kordumatu kombinatsioon.</span><span class="sxs-lookup"><span data-stu-id="e8b06-150">Ensure that each row is a unique combination of all the values put together.</span></span>

1.  <span data-ttu-id="e8b06-151">Salvestage fail CSV vormingus.</span><span class="sxs-lookup"><span data-stu-id="e8b06-151">Save the file as a CSV format.</span></span>

<span data-ttu-id="e8b06-152">Pakkumisandmete reeglite faili üleslaadimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e8b06-152">To upload the offer data rules file, do the following.</span></span>

1.  <span data-ttu-id="e8b06-153">Valige **Pakkumise haldamine**</span><span class="sxs-lookup"><span data-stu-id="e8b06-153">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="e8b06-154">Laiendage jaotist **Teek** vasakul navigeerimispaanil, seejärel avage **Pakkumisandmete reeglid**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-154">Expand the **Library** section in the left navigation panel, then go to **Offer data rules**.</span></span>

1.  <span data-ttu-id="e8b06-155">Klõpsake **Uus andmekogum**, et kuvada **Üleslaadimise** dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="e8b06-155">Click **New data set** to display the **Upload** dialog box.</span></span>

1.  <span data-ttu-id="e8b06-156">Määrake reeglistikule kordumatu nimi ja seejärel laadige salvestatud CSV-fail üles.</span><span class="sxs-lookup"><span data-stu-id="e8b06-156">Specify a unique name for the rule set and then upload the saved CSV file.</span></span>

1.  <span data-ttu-id="e8b06-157">Klõpsake vahekaarti **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-157">Click **Add**.</span></span>
    <span data-ttu-id="e8b06-158">Reeglistiku töödeldakse taustal ning teid teavitatakse rakenduses ja e-posti teel, kui see on lõpule jõudnud.</span><span class="sxs-lookup"><span data-stu-id="e8b06-158">The rule set will be processed in the background and you will be notified in-app and via email once it completes.</span></span>

    <span data-ttu-id="e8b06-159">Teid teavitatakse, kui üleslaadimise töötlemisel ilmneb tõrkeid.</span><span class="sxs-lookup"><span data-stu-id="e8b06-159">You will be notified if there are errors while processing the upload.</span></span> <span data-ttu-id="e8b06-160">Seejärel saate alla laadida tõrkelogi, faili ära parandada ja uuesti üles laadida.</span><span class="sxs-lookup"><span data-stu-id="e8b06-160">You can then download the error log, fix the file, and upload it again.</span></span>

1.  <span data-ttu-id="e8b06-161">Kasutage kolmikpunkti nupu (**...**) suvandit, kui soovite reeglistiku alla laadida ja väärtuste kogumit värskendada.</span><span class="sxs-lookup"><span data-stu-id="e8b06-161">Use the ellipses button (**…**) option if you want to download the rule set and update the set of values.</span></span> <span data-ttu-id="e8b06-162">Pärast värskendamist saate faili uuesti üles laadida.</span><span class="sxs-lookup"><span data-stu-id="e8b06-162">After updating, you can upload the file again.</span></span>

1.  <span data-ttu-id="e8b06-163">Saate olemasoleva üleslaetud reeglistiku kustutada, kui määratletud kohatäidet ei kasutata teistes dokumendimallides.</span><span class="sxs-lookup"><span data-stu-id="e8b06-163">You can delete an existing rule set upload if the placeholder being defined is not being used in another document template.</span></span>

>[!NOTE]
> - <span data-ttu-id="e8b06-164">Igal kohatäitel saab olla vaid üks kordumatu veergude komplekt, millest see sõltub.</span><span class="sxs-lookup"><span data-stu-id="e8b06-164">Each placeholder can only have one unique set of columns that it is dependent on.</span></span> <span data-ttu-id="e8b06-165">Näiteks kui **Aastapalk** sõltub **Töö asukohast** ja **Tasemest**, ei saa üles laadida teist reeglistikku, kus **Aastapalk** sõltub teistsugustest veergudest.</span><span class="sxs-lookup"><span data-stu-id="e8b06-165">For example, if **Annual Salary** is dependent on **Job Location** and **Level**, you can't upload another rule set where **Annual Salary** is dependent on a different set of columns.</span></span>

> - <span data-ttu-id="e8b06-166">Saate **Näidiste** vahekaardilt **Pakkumisandmete reeglite** lehel alla laadida pakkumisandmete reeglistiku näidised.</span><span class="sxs-lookup"><span data-stu-id="e8b06-166">You can download sample offer data rule sets on the **Samples** tab on the **Offer data rules** page.</span></span>

> - <span data-ttu-id="e8b06-167">Kui pakkumise looja asendab pakkumisandmete reeglite soovitatud väärtused, märgistatakse pakkumine ebastandardseks ja volitatakse pakkumise kinnitamise töövoog.</span><span class="sxs-lookup"><span data-stu-id="e8b06-167">When an offer creator overrides the values that are recommended by the offer data rules, the offer is flagged as non-standard and offer approval workflow will be mandated.</span></span>

## <a name="document-templates"></a><span data-ttu-id="e8b06-168">Dokumendimallid</span><span class="sxs-lookup"><span data-stu-id="e8b06-168">Document templates</span></span>

<span data-ttu-id="e8b06-169">Pakkumise dokumendimall aitab administraatoritel pakkumiskirju koostada.</span><span class="sxs-lookup"><span data-stu-id="e8b06-169">An offer document template can help administrators create offer letters.</span></span> <span data-ttu-id="e8b06-170">Pakkumise dokumendimall on nii pakkumise osaks oleva teksti kui ka määratud pakkumisandmete kohatäidete kombinatsioon.</span><span class="sxs-lookup"><span data-stu-id="e8b06-170">The offer document template is a combination of the text that will be part of the offer as well as the defined offer data placeholders.</span></span> 

<span data-ttu-id="e8b06-171">Pakkumise dokumendimalli loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e8b06-171">To create an offer document template, do the following.</span></span>

1.  <span data-ttu-id="e8b06-172">Valige **Pakkumise haldamine**</span><span class="sxs-lookup"><span data-stu-id="e8b06-172">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="e8b06-173">Laiendage jaotist **Teek** vasakul navigeerimispaanil ja seejärel avage **Mallid**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-173">Expand the **Library** section in the left navigation pane and go to **Templates**.</span></span>

    <span data-ttu-id="e8b06-174">**Mallide** lehekülg kuvab loendi juba määratletud dokumendimallidest.</span><span class="sxs-lookup"><span data-stu-id="e8b06-174">The **Templates** page will display a list of document templates that have already been defined.</span></span>

1.  <span data-ttu-id="e8b06-175">Uue dokumendimalli loomiseks klõpsake **Uus mall**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-175">To create a new document template, click **New Template**.</span></span>

1.  <span data-ttu-id="e8b06-176">Sisestage malli jaoks kordumatu nimi ja klõpsake **Loo**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-176">Enter a unique name for the template and click **Create**.</span></span>

1.  <span data-ttu-id="e8b06-177">Pakkumise dokumendi sisu lisamiseks või redigeerimiseks kasutage RTF-redaktorit.</span><span class="sxs-lookup"><span data-stu-id="e8b06-177">Use the rich text editor to insert or edit the offer document content.</span></span> <span data-ttu-id="e8b06-178">Saate tekstiredaktori ülaosas olevate suvanditega lisada tabeleid, pilte ja hüperlinke.</span><span class="sxs-lookup"><span data-stu-id="e8b06-178">You can insert tables, images, and hyperlinks using the options available at the top of the text editor.</span></span>

1.  <span data-ttu-id="e8b06-179">Saate pakkumise dokumendimalli pakkumisandmete kohatäiteid sisestada järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e8b06-179">You can insert offer data placeholders in the offer template document by:</span></span>

    - <span data-ttu-id="e8b06-180">Pukseerides parempoolselt paanilt.</span><span class="sxs-lookup"><span data-stu-id="e8b06-180">Dragging and dropping from the right pane.</span></span>

    - <span data-ttu-id="e8b06-181">Lisades pakkumisandmete kohatäite otse selle kohale.</span><span class="sxs-lookup"><span data-stu-id="e8b06-181">Hashtag the offer data placeholder directly into position.</span></span> <span data-ttu-id="e8b06-182">Sisestades **\#** ja hakates seejärel sisestama pakkumisandmete kohatäite nime.</span><span class="sxs-lookup"><span data-stu-id="e8b06-182">Type **\#** and then start typing the name of the offer data placeholder.</span></span> <span data-ttu-id="e8b06-183">Valikud ilmuvad rippmenüü loendis.</span><span class="sxs-lookup"><span data-stu-id="e8b06-183">Options will appear in the drop-down list.</span></span> <span data-ttu-id="e8b06-184">Pakkumisandmete kohatäite sisestamiseks klõpsake või vajutage **Sisestamine**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-184">Click or press **Enter** to insert the offer data placeholder.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="e8b06-185">Kohatäite seostamiseks pakkumise dokumendimalliga, selle väärtust kandidaadile avaldamata, liikuge hiirega üle pakkumisandmete kohatäite ja klõpsake ikooni **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-185">To associate a placeholder to the offer document template without exposing its value to the candidate, hover over the offer data placeholder and click the **Pin** icon.</span></span> <span data-ttu-id="e8b06-186">See lükkab kohatäite pakkumise dokumendimalli **Kinnitatud pakkumisandmete** jaotisesse.</span><span class="sxs-lookup"><span data-stu-id="e8b06-186">This will push the placeholder to the **Pinned offer data** section of the offer document template.</span></span> <span data-ttu-id="e8b06-187">Eemaldamiseks järgige samu juhiseid, kuid klõpsake pakkumisandmete kohatäidete loendis **Eemalda**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-187">To unpin, follow the same steps but click **Unpin** in the list of offer data placeholders.</span></span>

    > - <span data-ttu-id="e8b06-188">Aktiivsete pakkumisandmete kohatäidete kuvamiseks minge paempoolse paani vahekaardile **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-188">To view the list of active offer data placeholders, switch to the **Active** tab in the right pane.</span></span>

    > - <span data-ttu-id="e8b06-189">Lisades kohatäitja, mida juhib pakkumisandmete reeglistik, näete selle pakkumisandmete kohatäite sõltumist teistes väärtustes.</span><span class="sxs-lookup"><span data-stu-id="e8b06-189">If you insert a placeholder that is driven by an offer data rule set, you can see the dependency of that offer data placeholder on other values.</span></span>

    > - <span data-ttu-id="e8b06-190">Teise võimalusena saate **Importida** sisu .docx failist oma arvutisse ja vastavalt vajadusele redigeerida.</span><span class="sxs-lookup"><span data-stu-id="e8b06-190">Alternatively, you can **Import** the content from a .docx file on your local machine and edit as required.</span></span> <span data-ttu-id="e8b06-191">Nii ei ole teil vaja redaktoris kogu sisu trükkida.</span><span class="sxs-lookup"><span data-stu-id="e8b06-191">That way, you don’t have to type in all the content in the editor.</span></span>

1. <span data-ttu-id="e8b06-192">Pakkumise dokumendi eelvaate kuvamiseks kasutage **Eelvaate** suvandit lehe ülaosas.</span><span class="sxs-lookup"><span data-stu-id="e8b06-192">To preview the offer document, use the **Preview** option at the top of the page.</span></span>

1. <span data-ttu-id="e8b06-193">Määramaks, kas pakkumise looja saab pakkumise dokumendi sisu redigeerida, kasutage lehe ülaosas olevat suvandit **Loa haldamine**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-193">To control whether an offer creator can edit the offer document content, use the **Manage permission** option at the top of the page.</span></span> <span data-ttu-id="e8b06-194">Kui soovite, et pakkumise looja saaks sisestada vaid kohatäite väärtuseid, kuid mitte redigeerida teksti, määrake loa väärtuseks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-194">If you want the offer creator to only insert placeholder values and not edit text, set the permission value to **No**.</span></span>

1. <span data-ttu-id="e8b06-195">Progressi salvestamiseks klõpsake **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-195">Click **Save** to save your progress.</span></span> <span data-ttu-id="e8b06-196">Mall salvestatakse mustandi olekus.</span><span class="sxs-lookup"><span data-stu-id="e8b06-196">The template will be saved in a draft state.</span></span>

1. <span data-ttu-id="e8b06-197">Lõpetamiseks ja dokumendi avaldatuks märkimiseks klõpsake **Lõpeta**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-197">To finalize and mark the document as published, click **Finish**.</span></span>

1. <span data-ttu-id="e8b06-198">Saate dokumendimallide teegist vaadata, missugused dokumendimallid on aktiveeritud, mustandirežiimis ning missugused on arhiveeritud ja ei ole enam kasutuses.</span><span class="sxs-lookup"><span data-stu-id="e8b06-198">You can see which document templates are currently active, in draft mode, and have been archived and are no longer in use on the document templates library landing experience.</span></span>

>[!NOTE]
> <span data-ttu-id="e8b06-199">Saate kustutada mis tahes pakkumise dokumendimalli, mis ei ole osa olemasolevast pakkumise paketi mallist.</span><span class="sxs-lookup"><span data-stu-id="e8b06-199">You can delete any offer document template that is not part of an existing offer package template.</span></span>


## <a name="offer-package-templates"></a><span data-ttu-id="e8b06-200">Pakkumise paketi mallid</span><span class="sxs-lookup"><span data-stu-id="e8b06-200">Offer package templates</span></span>

<span data-ttu-id="e8b06-201">Pakkumise paketid pakkumise artefaktid, mida kandidaatidega jagatakse ning need koosnevad ühe või enama pakkumise dokumendimalli kombinatsioonist.</span><span class="sxs-lookup"><span data-stu-id="e8b06-201">Offer packages are the offer artifacts that are shared with the candidate and consist of a combination of one or more offer document templates.</span></span> <span data-ttu-id="e8b06-202">Pakkumise paketi loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e8b06-202">To create an offer package, do the following.</span></span>

1.  <span data-ttu-id="e8b06-203">Valige **Pakkumise haldamine**</span><span class="sxs-lookup"><span data-stu-id="e8b06-203">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="e8b06-204">Valige vasakult navigeerimispaneelilt **Paketid**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-204">Go to **Packages** from the left navigation pane.</span></span>

    <span data-ttu-id="e8b06-205">Kuvatakse loend pakkumise loojatele saadaolevatest aktiivsetest paketimallidest.</span><span class="sxs-lookup"><span data-stu-id="e8b06-205">A list of active package templates that are available for offer creators to use is displayed.</span></span>

1.  <span data-ttu-id="e8b06-206">Uue pakkumise paketi loomiseks klõpsake **Uus pakett**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-206">To create a new offer package, click **New Package**.</span></span>

1.  <span data-ttu-id="e8b06-207">Sisestage kordumatu nimi ja klõpsake **Loo**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-207">Enter a unique name and click **Create**.</span></span>

1.  <span data-ttu-id="e8b06-208">Klõpsake **Lisa mall**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-208">Click **Add template**.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="e8b06-209">Võite luua uue malli või valida olemasolevate seast.</span><span class="sxs-lookup"><span data-stu-id="e8b06-209">You can choose to create a new template or choose from an existing one.</span></span>

    > - <span data-ttu-id="e8b06-210">Kui soovite lisada olemasoleva malli, peate veenduma, et pakkumise dokumendimall salvestati, lõpetati ja selle olek märgiti aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="e8b06-210">If you choose to add an existing template, you need to make sure that the   offer document template was saved, finalized, and marked as   active.</span></span>
    
    > - <span data-ttu-id="e8b06-211">Saate valida nii palju dokumendimalle kui soovite.</span><span class="sxs-lookup"><span data-stu-id="e8b06-211">You can choose as many document templates as you want.</span></span> 
    
1.  <span data-ttu-id="e8b06-212">Klõpsake **Valmis**, et naasta **Pakettide haldamisse**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-212">Click **Done** to return to **Package management**.</span></span>

    <span data-ttu-id="e8b06-213">Saate konfigureerida dokumentide järjestuse ja märkida, kas konkreetne pakkumise dokument on pakkumise loomisel vajalik.</span><span class="sxs-lookup"><span data-stu-id="e8b06-213">You can configure the sequence of the documents and also mark whether the specific offer document is required during offer creation.</span></span> <span data-ttu-id="e8b06-214">Pakkumise loojal on võimalus kustutada dokumendid, mis on märgistatud kui **Pole nõutav**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-214">The offer creator will have an option to delete the documents marked as **Not required**.</span></span>

1. <span data-ttu-id="e8b06-215">Pakkumise paketimalli salvestamiseks nii, et seda saaksid kasutada kõik pakkumise loojad, klõpsake **Salvesta ja avalda**.</span><span class="sxs-lookup"><span data-stu-id="e8b06-215">To save the offer package template so that it's usable by all offer creators, click **Save and publish**.</span></span>

   <span data-ttu-id="e8b06-216">Pakkumise paketimallide mustandite vaatamiseks minge vahekaardile **Mustandid**. Kui pakkumise paketimalli muudetakse, tuleb see uuesti salvestada ja avaldada.</span><span class="sxs-lookup"><span data-stu-id="e8b06-216">To view draft offer package templates, go to the **Drafts** tab. If a change is made to the offer package template, it must be  saved and republished.</span></span>

## <a name="configure-an-offer-process"></a><span data-ttu-id="e8b06-217">Pakkumisprotsessi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="e8b06-217">Configure an offer process</span></span>

<span data-ttu-id="e8b06-218">Rakenduse Attract administraator saab konfigureerida mitut pakkumise loomise protsessi osa.</span><span class="sxs-lookup"><span data-stu-id="e8b06-218">There are several parts of the offer creation process that can be configured by an Attract administrator.</span></span>

- <span data-ttu-id="e8b06-219">**Pakkumise kinnitamised** – valige, kas pakkumise kinnitamised on enne pakkumise kliendile saatmist nõutud.</span><span class="sxs-lookup"><span data-stu-id="e8b06-219">**Offer approvals** - Choose whether offer approvals are required before the offer can be sent to the candidate.</span></span> <span data-ttu-id="e8b06-220">Adminstraatorina saate otsustada ka seda, kas kõik pakkumise kinnitamised toimuvad järjestikkusel viisil või paralleelse kinnitamise töövooga.</span><span class="sxs-lookup"><span data-stu-id="e8b06-220">As an administrator, you can also decide whether all offer approvals will happen in a sequential manner or parallel approval workflow.</span></span> <span data-ttu-id="e8b06-221">Samuti saate määrata, kas pakkumise kinnitajatel tuleb kinnitusele lisada kommentaar.</span><span class="sxs-lookup"><span data-stu-id="e8b06-221">You can also mandate whether offer approvers must add a comment along with their offer approval.</span></span> <span data-ttu-id="e8b06-222">Pakkumise kinnitamised on kohustuslikud kõigile ebastandardsetele pakkumistele.</span><span class="sxs-lookup"><span data-stu-id="e8b06-222">Offer approvals are mandatory for all non-standard offers.</span></span>

- <span data-ttu-id="e8b06-223">**Kandidaadi pakkumise kogemus** – administraatorina saate valida, kas määrata kõigile pakkumistele aegumiskuupäev ja kui, siis milline peaks olema aegumiskuupäeva vaikevastasus.</span><span class="sxs-lookup"><span data-stu-id="e8b06-223">**Candidate’s offer experience** - As administrator, you can choose to set whether all offers have an expiration date, and if so, what the default offset for the expiration date should be.</span></span> <span data-ttu-id="e8b06-224">Saate konfigureerida ka selle, kas kandidaat saab pakkumisest keelduda.</span><span class="sxs-lookup"><span data-stu-id="e8b06-224">You can also configure whether candidates can decline an offer.</span></span>

- <span data-ttu-id="e8b06-225">**Elektronallkirjad** -administraatorina saate määrata ka meetodi, mille abil kandidaatid saavad pakkumistele allkirju anda.</span><span class="sxs-lookup"><span data-stu-id="e8b06-225">**e-Signatures** - As an administrator, you can also choose the method that candidates can use to sign offers.</span></span>
    - <span data-ttu-id="e8b06-226">Adobe Sign - kõik pakkumispaketid saadetakse ja allkirjastatakse rakenduse Adobe Sign abil.</span><span class="sxs-lookup"><span data-stu-id="e8b06-226">Adobe Sign - All offer packages will be sent and signed via Adobe Sign.</span></span> <span data-ttu-id="e8b06-227">Iga pakkumise looja, kes pakkumise avaldab, peab ühendama oma Adobe Sign’i konto rakendusega Attract.</span><span class="sxs-lookup"><span data-stu-id="e8b06-227">Each offer creator publishing the offer needs to have their Adobe Sign account connected to Attract.</span></span> <span data-ttu-id="e8b06-228">Adobe Signi litsentside ja tasuta prooviperioodi puhul külastage seda [linki](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span><span class="sxs-lookup"><span data-stu-id="e8b06-228">For Adobe Sign licenses and a free Trial, please visit this [link](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span></span>

    - <span data-ttu-id="e8b06-229">DocuSign – kõik pakkumispaketid saadetakse ja allkirjastatakse rakenduse DocuSign abil.</span><span class="sxs-lookup"><span data-stu-id="e8b06-229">DocuSign - All offer packages will be sent and signed via DocuSign.</span></span> <span data-ttu-id="e8b06-230">Iga pakkumise looja, kes pakkumise avaldab, peab ühendama oma DocuSigni konto rakendusega Attract.</span><span class="sxs-lookup"><span data-stu-id="e8b06-230">Each offer creator publishing the offer needs to have their DocuSign account connected to Attract.</span></span> 
    
    - <span data-ttu-id="e8b06-231">ESign – see on valmiskujul esitatud vaikesäte, kus kasutaja saab oma nime ja initsiaalide sisestamisega pakkumise allkirjastada.</span><span class="sxs-lookup"><span data-stu-id="e8b06-231">ESign - This is the default option, provided out of the box, where the user can sign an offer by typing their name and initials.</span></span>


<span data-ttu-id="e8b06-232">Pakkumise loomisprotsessi kohta lisateabe saamiseks vt [Pakkumiste loomine, kinnitamine ja allkirjastamine](./creating-offers.md).</span><span class="sxs-lookup"><span data-stu-id="e8b06-232">To learn more about the offer creation process, see [Create, approve, and sign offers](./creating-offers.md).</span></span>
