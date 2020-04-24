---
title: Mallkooslused
description: Mallkoosluses (BOM) on pidevalt kasutatavate teenuseobjekti komponentide standardnimekiri.
author: ShylaThompson
manager: tfehr
ms.date: 09/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8842a293a50efb24590784cc52ef0254eca10e3a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206538"
---
# <a name="template-boms"></a><span data-ttu-id="8d926-103">Mallkooslused</span><span class="sxs-lookup"><span data-stu-id="8d926-103">Template BOMs</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="8d926-104">Mallkoosluses (BOM) on pidevalt kasutatavate teenuseobjekti komponentide standardnimekiri.</span><span class="sxs-lookup"><span data-stu-id="8d926-104">A template bill of materials (BOM) provides you with a standardized list of components for service objects that are serviced regularly.</span></span> <span data-ttu-id="8d926-105">Mallkoosluses loetletud komponendid kujutavad endast teenuseobjekti eraldiseisvaid alamkomponente.</span><span class="sxs-lookup"><span data-stu-id="8d926-105">The components that are listed in the template BOM represent the individual subcomponents of the service object.</span></span> <span data-ttu-id="8d926-106">Kui te rakendate mallkooslust teenuseobjektil, saate säilitada teenuseobjektil vahetatud alamkomponentide kirjet.</span><span class="sxs-lookup"><span data-stu-id="8d926-106">By applying a template BOM to a service object, you can keep a record of the subcomponents that have been replaced on the service object.</span></span>

<span data-ttu-id="8d926-107">Teenuseleppes ja teenusetellimuses mallkoosluse rakendamiseks tuleb teil see lisada teenuseobjekti seosesse.</span><span class="sxs-lookup"><span data-stu-id="8d926-107">To apply a template BOM to a service agreement or a service order, you attach it to a service object relation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="8d926-108">Teenuseobjektile saate rakendada ainult ühe mallkoosluse.</span><span class="sxs-lookup"><span data-stu-id="8d926-108">You can apply only one template BOM to a service object.</span></span></P>

## <a name="create-a-template-bom"></a><span data-ttu-id="8d926-109">Käsitsi koostatava mallkoosluse loomine</span><span class="sxs-lookup"><span data-stu-id="8d926-109">Create a template BOM</span></span>

<span data-ttu-id="8d926-110">Järgmises tabelis on toodud teave mitmesuguste meetodite kohta, mida saate kasutada mallkoosluse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="8d926-110">The following table contains information about the various methods that you can use to create a template BOM.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d926-111">Meetod</span><span class="sxs-lookup"><span data-stu-id="8d926-111">Method</span></span></p></th>
<th><p><span data-ttu-id="8d926-112">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8d926-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d926-113">Tootmine</span><span class="sxs-lookup"><span data-stu-id="8d926-113">Production</span></span></p></td>
<td><p><span data-ttu-id="8d926-114">Mallkooslus põhineb tootmistellimusel.</span><span class="sxs-lookup"><span data-stu-id="8d926-114">The template BOM is based on a production order.</span></span> <span data-ttu-id="8d926-115">See valik on rakendatav vaid siis, kui töötate tootmiskeskkonnas.</span><span class="sxs-lookup"><span data-stu-id="8d926-115">This option is applicable only if you operate in a production environment.</span></span> <span data-ttu-id="8d926-116">Eeliseks on teil kehtiv, üksikasjalik loetelu komponentidest, millest kaup koosneb.</span><span class="sxs-lookup"><span data-stu-id="8d926-116">The benefit is that you have a current, detailed listing of the components that make up an item.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d926-117">Kaup BOM</span><span class="sxs-lookup"><span data-stu-id="8d926-117">Item BOM</span></span></p></td>
<td><p><span data-ttu-id="8d926-118">Mallkooslus põhineb kauba kooslusel.</span><span class="sxs-lookup"><span data-stu-id="8d926-118">The template BOM is based on an item BOM.</span></span> <span data-ttu-id="8d926-119">Kauba kooslus on erinevalt tootmiskooslusest staatiline nimekiri komponentidest, mis moodustavad kauba.</span><span class="sxs-lookup"><span data-stu-id="8d926-119">The item BOM, unlike the production BOM, is a static list of the components that make up an item.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d926-120">Olemasolev mall</span><span class="sxs-lookup"><span data-stu-id="8d926-120">Existing template</span></span></p></td>
<td><p><span data-ttu-id="8d926-121">Mall põhineb olemasoleval mallkooslusel.</span><span class="sxs-lookup"><span data-stu-id="8d926-121">The template is based on an existing template BOM.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d926-122">Käsitsi</span><span class="sxs-lookup"><span data-stu-id="8d926-122">Manual</span></span></p></td>
<td><p><span data-ttu-id="8d926-123">Kui te teate, milliseid varuosi tavaliselt teenuseobjektil vahetatakse, saate luua oma mallkoosluse käsitsi.</span><span class="sxs-lookup"><span data-stu-id="8d926-123">If you know what spare parts are typically replaced on a service object, you can create your template BOM manually.</span></span> <span data-ttu-id="8d926-124">See meetod aitab tagada, et mallis sisalduvad komponendid peegeldavad teie töökoha praegusi nõudeid.</span><span class="sxs-lookup"><span data-stu-id="8d926-124">This method helps make sure that the components that are included in the template reflect the actual requirements of your workplace.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a><span data-ttu-id="8d926-125">Mallkoosluse rakendamine teenuseleppele või hooldustellimusele</span><span class="sxs-lookup"><span data-stu-id="8d926-125">Apply the template BOM to a service agreement or service order</span></span>

<span data-ttu-id="8d926-126">Saate rakendada mallkooslust teenuseleppele, hooldustellimusele või mõlemale.</span><span class="sxs-lookup"><span data-stu-id="8d926-126">You can apply a template BOM to a service agreement, a service order, or both.</span></span> <span data-ttu-id="8d926-127">Teenuselepe hõlmab tavaliselt pikaajalist suhet kliendiga.</span><span class="sxs-lookup"><span data-stu-id="8d926-127">The service agreement usually covers a long-term relationship with a customer.</span></span> <span data-ttu-id="8d926-128">Teenusekoosluses salvestatud asenduste ajalugu on kasulik teave teenuseleppe jaoks.</span><span class="sxs-lookup"><span data-stu-id="8d926-128">The history of replacements that is recorded in the service BOM is useful data to have for the service agreement.</span></span>

<span data-ttu-id="8d926-129">Saate mallkooslust rakendada ka hooldustellimusele, et salvestada teenuseobjektil tehtud teenuste ajalugu.</span><span class="sxs-lookup"><span data-stu-id="8d926-129">You can also apply a template BOM to a service order to record the history of the service that has been performed on a service object.</span></span>

## <a name="copy-the-history-of-a-service-bom"></a><span data-ttu-id="8d926-130">Teenusekoosluse ajaloo kopeerimine</span><span class="sxs-lookup"><span data-stu-id="8d926-130">Copy the history of a service BOM</span></span>

<span data-ttu-id="8d926-131">Teenusekoosluse rea ajaloo saate kopeerida ühest teenuseleppest teise.</span><span class="sxs-lookup"><span data-stu-id="8d926-131">You can copy the history of a service BOM line from one service agreement to another service agreement.</span></span> <span data-ttu-id="8d926-132">Kopeerides teenuse ajalugu ühest teenuseleppest teise, saate säilitada kaubal tehtud asenduste kirje.</span><span class="sxs-lookup"><span data-stu-id="8d926-132">By copying the service history between service agreements, you can preserve the record of replacements for an item.</span></span>

<span data-ttu-id="8d926-133">**Näide**</span><span class="sxs-lookup"><span data-stu-id="8d926-133">**Example**</span></span>

<span data-ttu-id="8d926-134">Olete koostanud 3-aastase teenuseleppe kliendi auto kohta.</span><span class="sxs-lookup"><span data-stu-id="8d926-134">You have set up a three-year service agreement for a customer's car.</span></span> <span data-ttu-id="8d926-135">Selle perioodi jooksul harjub klient ettevõtte pakutava hea teenindusega.</span><span class="sxs-lookup"><span data-stu-id="8d926-135">During that period, the customer becomes accustomed to the good service that the company provides.</span></span> <span data-ttu-id="8d926-136">Seega soovib klient pärast leppe aegumist sõlmida uue.</span><span class="sxs-lookup"><span data-stu-id="8d926-136">Therefore, after the agreement expires, the customer wants to set up a new one.</span></span> <span data-ttu-id="8d926-137">Nüüd on teil võimalik läbi rääkida ettevõtte jaoks kasulikuma lepingu suhtes.</span><span class="sxs-lookup"><span data-stu-id="8d926-137">You are now able to negotiate a more favorable agreement for the company.</span></span> <span data-ttu-id="8d926-138">Kuna asendatud komponentide kirje võib tulevikus olla kasulik, võite kopeerida teenusekoosluse ajaloo uude leppesse.</span><span class="sxs-lookup"><span data-stu-id="8d926-138">Because the record of replaced components might be useful in the future, you copy the history of the service BOM to the new agreement.</span></span>

## <a name="modify-the-template-bom"></a><span data-ttu-id="8d926-139">Mallkoosluse muutmine</span><span class="sxs-lookup"><span data-stu-id="8d926-139">Modify the template BOM</span></span>

<span data-ttu-id="8d926-140">Kui mallkooslus ei ole teenuseobjektiga seotud, saate selle ridu muuta või kustutada.</span><span class="sxs-lookup"><span data-stu-id="8d926-140">If a template BOM has not been attached to a service object, you can modify or delete lines in it.</span></span> <span data-ttu-id="8d926-141">Pärast mallkoosluse sidumist teenuseobjektiga saate muuta ainult koosluse kohalikku versiooni.</span><span class="sxs-lookup"><span data-stu-id="8d926-141">After the template BOM is attached to a service object, you can modify only the local version of the BOM.</span></span> <span data-ttu-id="8d926-142">Kui te soovite mallkoosluse kohaliku versiooni seadistust duplitseerida, saate luua uue kohalikul versioonil põhineva mallkoosluse.</span><span class="sxs-lookup"><span data-stu-id="8d926-142">If you want to duplicate the setup of a local version of a template BOM, you can create a new template BOM based on the local version.</span></span> <span data-ttu-id="8d926-143">Lisateavet vt teemast [Teenusekoosluse muutmine](modify-service-bom.md).</span><span class="sxs-lookup"><span data-stu-id="8d926-143">For more information, see [Modify a Service BOM](modify-service-bom.md).</span></span>

<span data-ttu-id="8d926-144">Kui te asendate koosluses kauba, saate asenduse registreerida koosluse koostaja kooslusereal.</span><span class="sxs-lookup"><span data-stu-id="8d926-144">If you replace an item in the BOM, you can register the replacement on the BOM line in the BOM designer.</span></span> <span data-ttu-id="8d926-145">Võite asenduskauba jaoks luua ka hooldustellimuse rea.</span><span class="sxs-lookup"><span data-stu-id="8d926-145">Optionally, you can create a service order line for the replacement object.</span></span> <span data-ttu-id="8d926-146">Kui loote hooldustellimuse rea, saate asenduskauba arveldada.</span><span class="sxs-lookup"><span data-stu-id="8d926-146">If you create a service order line, you can invoice the replacement item.</span></span> <span data-ttu-id="8d926-147">Kui te asendusele hooldustellimuse rida ei loo, säilitatakse asenduse registreering teenuseobjekti ajaloo jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="8d926-147">If you do not create a service order line for a replacement, the replacement registration is kept to track the history of the service object.</span></span>

## <a name="change-how-information-on-the-bom-line-is-displayed"></a><span data-ttu-id="8d926-148">Kooslusereal kuvatava teabe muutmine</span><span class="sxs-lookup"><span data-stu-id="8d926-148">Change how information on the BOM line is displayed</span></span>

<span data-ttu-id="8d926-149">Saate muuta viisi, kuidas kuvatakse koosluserida kõigis malli- ja teenusekooslustes.</span><span class="sxs-lookup"><span data-stu-id="8d926-149">You can change the way that information on the BOM line is displayed for all template and service BOMs.</span></span> <span data-ttu-id="8d926-150">Muudatused rakendatakse kõikidele malli- ja teenusekooslustele.</span><span class="sxs-lookup"><span data-stu-id="8d926-150">The changes are applied to all template BOMs and service BOMs.</span></span> <span data-ttu-id="8d926-151">See hõlmab ka teenuseobjektidega seotud kooslusi.</span><span class="sxs-lookup"><span data-stu-id="8d926-151">This includes those that are attached to service objects.</span></span>

## <a name="set-up-number-sequences-for-template-boms"></a><span data-ttu-id="8d926-152">Mallkoosluste numbriseeriate seadistamine</span><span class="sxs-lookup"><span data-stu-id="8d926-152">Set up number sequences for template BOMs</span></span>

<span data-ttu-id="8d926-153">Mallkoosluste kasutamiseks peate seadistama kaks numbriseeriat.</span><span class="sxs-lookup"><span data-stu-id="8d926-153">To use template BOMs, you must set up two number sequences.</span></span> <span data-ttu-id="8d926-154">Seadistage üks numbriseeria mallkoosluse ja teine koosluse ajaloo rea numbri jaoks.</span><span class="sxs-lookup"><span data-stu-id="8d926-154">Set up one number sequence for the template BOM and one for the BOM history line number.</span></span>


> [!NOTE]
> <P><span data-ttu-id="8d926-155">Numbriseeriaid kasutatakse identifikaatorite eraldamiseks kirjetele, mis neid nõuavad.</span><span class="sxs-lookup"><span data-stu-id="8d926-155">Number sequences are used to allocate identifiers to records that require them.</span></span> <span data-ttu-id="8d926-156">Enne kui saate mallkooslusele või koosluse ajaloo rea numbrile numbriseeria määrata, peate seadistama numbriseeria koodid.</span><span class="sxs-lookup"><span data-stu-id="8d926-156">Before you can assign a number sequence to a template BOM or a BOM history line number, you must set up number sequences codes.</span></span></P>


## <a name="set-up-number-sequences"></a><span data-ttu-id="8d926-157">Seadista numbriseeriad</span><span class="sxs-lookup"><span data-stu-id="8d926-157">Set up number sequences</span></span>

1.  <span data-ttu-id="8d926-158">Looge loendilehel **Numbriseeriad** numbriseeriad mallkoosluste ja koosluse ajaloo raja numbri jaoks.</span><span class="sxs-lookup"><span data-stu-id="8d926-158">On the **Number sequences** list page, create number sequences for template BOMs and the BOM history line number.</span></span> 

2.  <span data-ttu-id="8d926-159">Klõpsake valikul **Hooldushaldus** \> **Häälestus** \> **Teenuste halduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="8d926-159">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

3.  <span data-ttu-id="8d926-160">Klõpsake valikut **Numbriseeriad** ja seejärel valige numbriseeria kood numbriseeria viidetele, mille lõite vormis **Numbriseeriad**.</span><span class="sxs-lookup"><span data-stu-id="8d926-160">Click **Number sequences**, and then select a number sequence code for the number sequence references that you created in the **Number sequences** form.</span></span>

4.  <span data-ttu-id="8d926-161">Muudatuste salvestamiseks sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="8d926-161">Close the form to save your changes.</span></span>


> [!NOTE]
> <P><span data-ttu-id="8d926-162">Koosluse ajaloo rea numbrit kasutab süsteem koosluse ajaloo kannete seostamiseks hooldusleppe või -tellimusega.</span><span class="sxs-lookup"><span data-stu-id="8d926-162">The BOM history line number is used by the system to associate the transactions in the BOM history with a service agreement or service order.</span></span> <span data-ttu-id="8d926-163">Numbrit ei kuvata kasutajaliideses.</span><span class="sxs-lookup"><span data-stu-id="8d926-163">The number is not displayed in the user interface.</span></span></P>



## <a name="see-also"></a><span data-ttu-id="8d926-164">Vt ka</span><span class="sxs-lookup"><span data-stu-id="8d926-164">See also</span></span>

[<span data-ttu-id="8d926-165">Käsitsi koostatava mallkoosluse loomine</span><span class="sxs-lookup"><span data-stu-id="8d926-165">Create a template BOM</span></span>](create-template-bom.md)

[<span data-ttu-id="8d926-166">teenuslepingute objektiseoste mallkoosluste haldamine</span><span class="sxs-lookup"><span data-stu-id="8d926-166">Manage template BOMs on object relations</span></span>](manage-template-boms-on-object-relations.md)

[<span data-ttu-id="8d926-167">Teenusekoosluse muutmine</span><span class="sxs-lookup"><span data-stu-id="8d926-167">Modify a Service BOM</span></span>](modify-service-bom.md)

 


