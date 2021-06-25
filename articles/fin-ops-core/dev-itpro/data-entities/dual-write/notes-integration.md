---
title: Integratsiooni teatis
description: Selles teemas kirjeldatakse maksuandmete integreerimist rakenduse ja teenuse vahel.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: ceb5b7c90cc7efa0049d0278e2c245228e5b52bd
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186782"
---
# <a name="note-integration"></a><span data-ttu-id="d275a-103">Integratsiooni teatis</span><span class="sxs-lookup"><span data-stu-id="d275a-103">Note integration</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d275a-104">Äriprotsesside jooksul Microsoft Dynamics 365 kasutajad koguvad sageli teavet oma klientide kohta.</span><span class="sxs-lookup"><span data-stu-id="d275a-104">During business processes, Microsoft Dynamics 365 users often gather information about their customers.</span></span> <span data-ttu-id="d275a-105">See teave kirjendatakse tegevuste ja märkustena.</span><span class="sxs-lookup"><span data-stu-id="d275a-105">This information is recorded as activities and notes.</span></span> <span data-ttu-id="d275a-106">Selles teemas kirjeldatakse maksuandmete integreerimist rakenduse ja teenuse vahel.</span><span class="sxs-lookup"><span data-stu-id="d275a-106">This topic describes the integration of note data in dual-write.</span></span>

<span data-ttu-id="d275a-107">Kliendi teavet saab klassifitseerida järgmiselt:</span><span class="sxs-lookup"><span data-stu-id="d275a-107">Customer information can be classified in the following ways:</span></span>

+ <span data-ttu-id="d275a-108">**Käivitatav teave, mida Dynamics 365 kasutaja kliendi eest käsitseb** – näiteks Contoso (Dynamics 365 kasutaja) viib läbi värskendusseansi.</span><span class="sxs-lookup"><span data-stu-id="d275a-108">**Actionable information that a Dynamics 365 user handles on behalf of a customer** – For example, Contoso (a Dynamics 365 user) is conducting a game show.</span></span> <span data-ttu-id="d275a-109">Üks Contoso klientidest (klient) soovib osaleda mängu show\`s.</span><span class="sxs-lookup"><span data-stu-id="d275a-109">One of Contoso's customers (a customer) wants to attend the game show.</span></span> <span data-ttu-id="d275a-110">Klient palub Contoso töötajal reserveerida nende jaoks mängu show\`s pesa.</span><span class="sxs-lookup"><span data-stu-id="d275a-110">The customer asks a Contoso employee to book a slot in the game show for them.</span></span> <span data-ttu-id="d275a-111">Reserveerimine toimub Contoso sündmuses osaleja kalendris.</span><span class="sxs-lookup"><span data-stu-id="d275a-111">The booking occurs in Contoso's event attendee's calendar.</span></span>
+ <span data-ttu-id="d275a-112">**Dynamics 365 kasutaja toimingu teave** – näiteks klient, kes ostab Surface'i ühikut, sisestab erijuhised, mis näitavad, et seade peaks enne tarnet olemakingituseks.</span><span class="sxs-lookup"><span data-stu-id="d275a-112">**Actionable information for a Dynamics 365 user** – For example, a customer who is purchasing a Surface unit enters special instructions that indicate that the device should be gift wrapped before delivery.</span></span> <span data-ttu-id="d275a-113">Need juhised on kasutatav teave, mida peaks käsitsema Contoso töötaja, kes vastutab pakendamise eest.</span><span class="sxs-lookup"><span data-stu-id="d275a-113">These instructions are actionable information that should be handled by the Contoso employee who is responsible for packaging.</span></span>
+ <span data-ttu-id="d275a-114">**Mittetegevuslik teave** – näiteks klient külastab Contoso kauplust ja väljendab vestluse ajal kauplusepartneriga huvi *Halo* mängu ja mängutarvikute vastu.</span><span class="sxs-lookup"><span data-stu-id="d275a-114">**Non-actionable information** – For example, a customer visits the Contoso store and, during their conversation with a store associate, expresses interest in *Halo* games and gaming accessories.</span></span> <span data-ttu-id="d275a-115">Kaupluse seostamine teeb selle teabe kohta märkuse.</span><span class="sxs-lookup"><span data-stu-id="d275a-115">The store associate makes a note of this information.</span></span> <span data-ttu-id="d275a-116">Tootesoovituste mootor kasutab seda siis kliendile soovituste andmiseks.</span><span class="sxs-lookup"><span data-stu-id="d275a-116">The product recommendations engine then uses it to make recommendations to the customer.</span></span>

<span data-ttu-id="d275a-117">Üldiselt on tegutsetav teave hõivatud *tegevustena* Finance and Operations rakendustes ja kliendikogemuste rakenduses.</span><span class="sxs-lookup"><span data-stu-id="d275a-117">In general, actionable information is captured as *activities* in Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="d275a-118">Mittetegutsetav teave on hõivatud *teadetena* Finance and Operations rakenduses ja *märkustena* kliendikogemuse rakendustes.</span><span class="sxs-lookup"><span data-stu-id="d275a-118">Non-actionable information is captured as *notes* in Finance and Operations apps, and as *annotations* in customer engagement apps.</span></span>

> [!TIP]
> <span data-ttu-id="d275a-119">Ehkki märkused on mõeldud mittetegevustava teabe jaoks, ei takista rakendused teil neid kasutamast talletada ja käsitseda tegevustavat teavet, kui soovite neid sel viisil kasutada.</span><span class="sxs-lookup"><span data-stu-id="d275a-119">Although notes are intended for non-actionable information, the apps won't prevent you from using them to store and handle actionable information if you want to use them in that way.</span></span>

<span data-ttu-id="d275a-120">Microsoft vabastab praegu funktsiooni märkuse integreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="d275a-120">Microsoft is currently releasing functionality for note integration.</span></span> <span data-ttu-id="d275a-121">(Tegevuse integreerimise funktsioon vabastatakse hiljem.) Märkuse integreerimine on saadaval klientide, hankijate, müügitellimuste ja ostutellimuste puhul.</span><span class="sxs-lookup"><span data-stu-id="d275a-121">(Functionality for activity integration will be released later.) Note integration is available for customers, vendors, sales orders, and purchase orders.</span></span>

## <a name="create-a-note-in-a-customer-engagement-app"></a><span data-ttu-id="d275a-122">Märkuse loomine kliendikogemuse rakenduses</span><span class="sxs-lookup"><span data-stu-id="d275a-122">Create a note in a customer engagement app</span></span>

<span data-ttu-id="d275a-123">Märkuse loomiseks kliendi teenuse rakendusesse ja seejärel sünkroonige see Finance and Operations rakendusega, järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="d275a-123">To create a note in a customer engagement app and then sync it to a Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="d275a-124">Kliendi kaasamise rakenduses avage kliendi kontokirje.</span><span class="sxs-lookup"><span data-stu-id="d275a-124">In the customer engagement app, open the account record for a customer.</span></span>
2. <span data-ttu-id="d275a-125">Paanil **Ajajoon** valige plussmärk (**+**) ja seejärel valige **Märkus** märkuse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="d275a-125">In the **Timeline** pane, select the plus sign (**+**), and then select **Note** to create a note.</span></span>

    ![Märkuse loomine kliendikogemuse rakenduses](media/notes-ce-1.png)

3. <span data-ttu-id="d275a-127">Sisestage pealkiri ja kirjeldus ning seejärel valige käsk **Lisa märkus**.</span><span class="sxs-lookup"><span data-stu-id="d275a-127">Enter a title and description, and then select **Add note**.</span></span>

    ![Sisestage pealkiri ja kirjeldus](media/notes-ce-2.png)

    <span data-ttu-id="d275a-129">Uus märkus lisatakse kliendi ajajoonele.</span><span class="sxs-lookup"><span data-stu-id="d275a-129">The new note is added to the customer timeline.</span></span>

    ![Uus märkus kliendi ajajoonel](media/notes-ce-3.png)

4. <span data-ttu-id="d275a-131">Logige sisse Finance and Operations rakendusse ja avage sama kliendikirje.</span><span class="sxs-lookup"><span data-stu-id="d275a-131">Sign in to the Finance and Operations app, and open the same customer record.</span></span> <span data-ttu-id="d275a-132">Pange tähele, et **Ma nused** nupp (paberi märkide sümbol) ülemises parempoolses nurgas näitab, et kirje on manusega.</span><span class="sxs-lookup"><span data-stu-id="d275a-132">Notice that the **Attachments** button (paperclip symbol) in the upper-right corner indicates that the record has an attachment.</span></span>

    ![Manuse teatis](media/notes-ce-4.png)

5. <span data-ttu-id="d275a-134">Lehe **Manused** avamiseks valige nupp **Manused** lehel.</span><span class="sxs-lookup"><span data-stu-id="d275a-134">Select the **Attachments** button to open the **Attachments** page.</span></span> <span data-ttu-id="d275a-135">Peaksite leidma teate, mille lõite Customer Engagementi rakenduses.</span><span class="sxs-lookup"><span data-stu-id="d275a-135">You should find the note that you created in the customer engagement app.</span></span>

    ![Märkus kliendikogemuse rakendusest](media/notes-ce-5.png)

<span data-ttu-id="d275a-137">Kõik märkuse uuendused sünkroonitakse edasi-tagasi rakenduse Finance and Operations ja kliendikogemuse rakenduse vahel.</span><span class="sxs-lookup"><span data-stu-id="d275a-137">Any updates to the note are synced back and forth between the Finance and Operations app and the customer engagement app.</span></span>

## <a name="create-a-note-in-a-finance-and-operations-app"></a><span data-ttu-id="d275a-138">Märkuse loomine Finance and Operations kliendikogemuse rakenduses</span><span class="sxs-lookup"><span data-stu-id="d275a-138">Create a note in a Finance and Operations app</span></span>

<span data-ttu-id="d275a-139">Saate luua Finance and Operations rakendusse märkuse ja seejärel see sünkroonitakse kliendikogemuse rakendusega.</span><span class="sxs-lookup"><span data-stu-id="d275a-139">You can also create a note in a Finance and Operations app, and it will be synced to a customer engagement app.</span></span>

<span data-ttu-id="d275a-140">Märkuse loomiseks Finance and Operations rakenduses ja seejärel selle kliendikogemuse sünkroniseerimiseks, järgige järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="d275a-140">To create a note in a Finance and Operations app and then sync it to a customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="d275a-141">Valige Finance and Operations rakenduse lehel **Manused** suvand **Uus** \> **Märkus**.</span><span class="sxs-lookup"><span data-stu-id="d275a-141">In the Finance and Operations app, on the **Attachments** page, select **New** \> **Note**.</span></span>

    ![Märkuse loomine Finance and Operations rakenduses](media/notes-fo-1.png)

2. <span data-ttu-id="d275a-143">Sisestage pealkiri ja lühikirjeldus ning seejärel valige **Salvestamine**.</span><span class="sxs-lookup"><span data-stu-id="d275a-143">Enter a title and a brief set of instructions, and then select **Save**.</span></span>

    ![Sisestage pealkiri ja kirjeldus](media/notes-fo-2.png)

3. <span data-ttu-id="d275a-145">Kliendikogemuse rakenduses värskendage kirjet.</span><span class="sxs-lookup"><span data-stu-id="d275a-145">In the customer engagement app, update the record.</span></span> <span data-ttu-id="d275a-146">Uue märkuse leiate ajajoonelt.</span><span class="sxs-lookup"><span data-stu-id="d275a-146">You should find the new note on the timeline.</span></span>

    ![Uus märkus kliendi kaasamise rakenduse ajajoones](media/notes-fo-3.png)

<span data-ttu-id="d275a-148">Te saate liigitada märkuse nii sisemiseks kui väliseks.</span><span class="sxs-lookup"><span data-stu-id="d275a-148">You can classify a note as either internal or external.</span></span>

- <span data-ttu-id="d275a-149">Avage Finance and Operations rakenduses **Manused** leheküljel märkus ja seejärel valige suvand **Piirang** väljal **Sisemine** või **Väline**.</span><span class="sxs-lookup"><span data-stu-id="d275a-149">In the Finance and Operations app, on the **Attachments** page, open the note, and then, in the **Restriction** field, select **Internal** or **External**.</span></span>

    ![Piiranguväli](media/notes-fo-4.png)

<span data-ttu-id="d275a-151">Samuti saate luua URLi.</span><span class="sxs-lookup"><span data-stu-id="d275a-151">You can also create a URL.</span></span>

1. <span data-ttu-id="d275a-152">Valige Finance and Operations rakenduse lehel **Manused** suvand **Uus** \> **url**.</span><span class="sxs-lookup"><span data-stu-id="d275a-152">In the Finance and Operations app, on the **Attachments** page, select **New** \> **URL**.</span></span>
2. <span data-ttu-id="d275a-153">Sisestage pealkiri ja URL.</span><span class="sxs-lookup"><span data-stu-id="d275a-153">Enter a title and the URL.</span></span>
3. <span data-ttu-id="d275a-154">Väljal **Piirang** valige **Sisemine** või **Väline**.</span><span class="sxs-lookup"><span data-stu-id="d275a-154">In the **Restriction** field, select **Internal** or **External**.</span></span>

    ![URLi loomine Finance and Operations rakenduses](media/notes-fo-5.png)

4. <span data-ttu-id="d275a-156">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d275a-156">Select **Save**.</span></span>

    <span data-ttu-id="d275a-157">Kuna klienditeenuse rakendustel ei ole URL-i tüüpi, integreeritakse URL märkusena topeltkirjutusega.</span><span class="sxs-lookup"><span data-stu-id="d275a-157">Because customer engagement apps don't have a URL type, the URL is integrated with dual-write as a note.</span></span>

    ![URLi loomine kliendikogemuse rakenduses](media/notes-ce-6.png)

> [!NOTE]
> <span data-ttu-id="d275a-159">Failimanuseid ei toetata.</span><span class="sxs-lookup"><span data-stu-id="d275a-159">File attachments aren't supported.</span></span>

## <a name="templates"></a><span data-ttu-id="d275a-160">Mallid</span><span class="sxs-lookup"><span data-stu-id="d275a-160">Templates</span></span>

<span data-ttu-id="d275a-161">Maksuandmed sisaldavad tabeli kaartide kogumit, mis töötavad andmete suhtluse ajal koos, nagu on näha järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="d275a-161">Note integration includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="d275a-162">Finance and Operations rakendus</span><span class="sxs-lookup"><span data-stu-id="d275a-162">Finance and Operations app</span></span> | <span data-ttu-id="d275a-163">Klientide kaasamise rakendus</span><span class="sxs-lookup"><span data-stu-id="d275a-163">Customer engagement app</span></span> | <span data-ttu-id="d275a-164">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d275a-164">Description</span></span> |
|----------------------------|-------------------------|-------------|
| [<span data-ttu-id="d275a-165">Kliendi manused</span><span class="sxs-lookup"><span data-stu-id="d275a-165">Customer Attachments</span></span>](mapping-reference.md#230) | <span data-ttu-id="d275a-166">Märkused</span><span class="sxs-lookup"><span data-stu-id="d275a-166">Annotations</span></span> | <span data-ttu-id="d275a-167">Ettevõtted, mis kasutavad kliendispetsiifilise teabe kogumiseks (nii organisatsioonide kui ka isikute puhul) lihtteksti ja URL-e.</span><span class="sxs-lookup"><span data-stu-id="d275a-167">Businesses that use plain text and URLs to capture customer-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="d275a-168">Hankija dokumendimanused</span><span class="sxs-lookup"><span data-stu-id="d275a-168">Vendor document attachments</span></span>](mapping-reference.md#231) | <span data-ttu-id="d275a-169">Märkused</span><span class="sxs-lookup"><span data-stu-id="d275a-169">Annotations</span></span> | <span data-ttu-id="d275a-170">Ettevõtted, mis kasutavad kliendispetsiifilise teabe kogumiseks (nii organisatsioonide kui ka isikute puhul) lihtteksti ja URL-e.</span><span class="sxs-lookup"><span data-stu-id="d275a-170">Businesses that use plain text and URLs to capture vendor-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="d275a-171">Müügitellimuse päise dokumendi manused</span><span class="sxs-lookup"><span data-stu-id="d275a-171">Sales order header document attachments</span></span>](mapping-reference.md#229) | <span data-ttu-id="d275a-172">Märkused</span><span class="sxs-lookup"><span data-stu-id="d275a-172">Annotations</span></span> | <span data-ttu-id="d275a-173">Ettevõtted, mis kasutavad müügitellimuse teabe kogumiseks lihtteksti ja URL-e.</span><span class="sxs-lookup"><span data-stu-id="d275a-173">Businesses that use plain text and URLs to capture sales order–specific information.</span></span> |
| [<span data-ttu-id="d275a-174">Ostutellimuse päise dokumendi manused</span><span class="sxs-lookup"><span data-stu-id="d275a-174">Purchase order header document attachments</span></span>](mapping-reference.md#232) | <span data-ttu-id="d275a-175">Märkused</span><span class="sxs-lookup"><span data-stu-id="d275a-175">Annotations</span></span> | <span data-ttu-id="d275a-176">Ettevõtted, mis kasutavad müügitellimuse teabe kogumiseks lihtteksti ja URL-e.</span><span class="sxs-lookup"><span data-stu-id="d275a-176">Businesses that use plain text and URLs to capture purchase order–specific information.</span></span> |

## <a name="limitations"></a><span data-ttu-id="d275a-177">Kitsendused</span><span class="sxs-lookup"><span data-stu-id="d275a-177">Limitations</span></span>

<span data-ttu-id="d275a-178">Pärast märkmelahenduse installimist ei saa te seda desinstallida.</span><span class="sxs-lookup"><span data-stu-id="d275a-178">Once you install the notes solution, you cannot uninstall it.</span></span> 

<span data-ttu-id="d275a-179">Lisateavet vt [topeltkirjutuse vastendamise viitest](mapping-reference.md).</span><span class="sxs-lookup"><span data-stu-id="d275a-179">For more information, see [Dual-write mapping reference](mapping-reference.md).</span></span>
