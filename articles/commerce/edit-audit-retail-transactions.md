---
title: Kaupluse kannete redigeerimine ja auditeerimine
description: Selles teemas kirjeldatakse kaupluse kannete redigeerimise ja auditeerimise funktsiooni.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 97211ee36dbaa704d3a967e9b742ff1cae708707
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004385"
---
# <a name="edit-and-audit-retail-store-transactions"></a><span data-ttu-id="88ae2-103">Kaupluse kannete redigeerimine ja auditeerimine</span><span class="sxs-lookup"><span data-stu-id="88ae2-103">Edit and audit retail store transactions</span></span>

[!include [banner](includes/banner.md)]



<span data-ttu-id="88ae2-104">Dynamics 365 Commerce'i kliendid kasutavad nii esimese kui ka kolmanda osapoole kassarakendusi.</span><span class="sxs-lookup"><span data-stu-id="88ae2-104">Dynamics 365 Commerce customers use first-party as well as third-party point of sale (POS) applications.</span></span> <span data-ttu-id="88ae2-105">Esimese osapoole kassarakendusega lisatakse kaupluse kanded kanalitest peakontorisse pakktöötluse kaudu.</span><span class="sxs-lookup"><span data-stu-id="88ae2-105">With the first-party POS application, store transactions are pulled into Headquarters from the channels through a batch process.</span></span> <span data-ttu-id="88ae2-106">Kolmanda osapoole rakendustega lisatakse kanded peakontorisse integratsiooni kaudu.</span><span class="sxs-lookup"><span data-stu-id="88ae2-106">With third-party applications, transactions are pulled into Headquarters through integration.</span></span> <span data-ttu-id="88ae2-107">Mõlemal juhul tuleb pärast kannete lisamist peakontorisse teostada süsteemsuskontrolli protsess, mis teeb kannetele mitu kontrolli, et peakontorisse sisestatavasse väljavõttesse lisataks ainult kinnituse läbinud kanded.</span><span class="sxs-lookup"><span data-stu-id="88ae2-107">In both cases, after transactions are pulled into Headquarters, a consistency check process needs to be executed that runs multiple validations on the transactions so that only successfully validated transactions are pulled into the statement to be posted in Headquarters.</span></span> 

<span data-ttu-id="88ae2-108">Kaubanduse kannete kinnitamine nurjub eri põhjustel.</span><span class="sxs-lookup"><span data-stu-id="88ae2-108">Commerce transactions fail validation for various reasons.</span></span> <span data-ttu-id="88ae2-109">Näiteks võib integratsioonikoodi või kassarakenduse programmiviga põhjustada vastuolulisi andmeid. Samuti võib vastuolulisi andmeid põhjustada kasutaja viga (nt toote kustutamine pärast kanaliga sünkroonimist või rahandusperioodi sulgemine ilma selle perioodi kandeid sisestamata).</span><span class="sxs-lookup"><span data-stu-id="88ae2-109">For example, a bug in the integration code or a bug in the POS application may cause inconsistent data, or a user error, such as deleting a product after it was synchronized to the channel or closing a fiscal period without posting transactions for that period, can cause inconsistent data.</span></span>

<span data-ttu-id="88ae2-110">Kuigi need kanded märgitakse lipuga ja jäetakse väljavõtetest välja, võivad kanded häirida kasutaja igapäevast protsessi, millega ta sisestab igapäevast müügiteavet finantssüsteemi.</span><span class="sxs-lookup"><span data-stu-id="88ae2-110">While these transactions get flagged and are excluded from the statements, the transactions can disrupt a customer’s daily process of posting daily sales to the financials.</span></span>

<span data-ttu-id="88ae2-111">Kaubanduses saate redigeerida konkreetseid nurjunud kinnitusega kandeid, kuid samal ajal säilitada kõigi muudatuste auditi.</span><span class="sxs-lookup"><span data-stu-id="88ae2-111">In Commerce, you can edit the specific transactions that fail validation while maintaining audit of all the changes.</span></span> 

## <a name="edit-and-audit-transactions"></a><span data-ttu-id="88ae2-112">Kannete redigeerimine ja auditeerimine</span><span class="sxs-lookup"><span data-stu-id="88ae2-112">Edit and audit transactions</span></span>

<span data-ttu-id="88ae2-113">Retaili versioonis 10.0.5 on sularaha- ja vedamiskanded (nt müük ja tagastused) ainsad kanded, mida saab redigeerida.</span><span class="sxs-lookup"><span data-stu-id="88ae2-113">In Retail version 10.0.5, cash and carry transactions like sales and returns are the only transactions that can be edited.</span></span> <span data-ttu-id="88ae2-114">Klienditellimuste või võrgutellimuste redigeerimist ei toetata.</span><span class="sxs-lookup"><span data-stu-id="88ae2-114">Editing customer orders or online orders is not supported.</span></span> <span data-ttu-id="88ae2-115">Retaili versioonis 10.0.6 ja uuemas toetatakse ka sularahahalduse kannete redigeerimist.</span><span class="sxs-lookup"><span data-stu-id="88ae2-115">In Retail version 10.0.6 and higher, editing cash management transactions is also supported.</span></span>

1. <span data-ttu-id="88ae2-116">Installige Dynamicsi Exceli lisandmoodul.</span><span class="sxs-lookup"><span data-stu-id="88ae2-116">Install the Dynamics Excel Add-in.</span></span>

2. <span data-ttu-id="88ae2-117">Avage tööruum **Kaupluse rahandus**.</span><span class="sxs-lookup"><span data-stu-id="88ae2-117">Go to the **Store financials** workspace.</span></span> <span data-ttu-id="88ae2-118">Paanil **Kande kinnitamise tõrked** kuvatakse eelfiltreeritud vaade kandevormist, mille üks või mitu kinnitusreeglit nurjusid.</span><span class="sxs-lookup"><span data-stu-id="88ae2-118">The **Transaction validation failures** tile provides a pre-filtered view of the transaction form that failed one or more of the validation rules.</span></span>
 
3. <span data-ttu-id="88ae2-119">Avage vorm.</span><span class="sxs-lookup"><span data-stu-id="88ae2-119">Open the form.</span></span> <span data-ttu-id="88ae2-120">Klõpsake kirjet, mille kinnitamine nurjus, klõpsake valikut **Office'i lisandmoodul** ja siis klõpsake valikut **Redigeeri valitud kannet**.</span><span class="sxs-lookup"><span data-stu-id="88ae2-120">Click the record that failed validation, click **Office Add in**, and then click **Edit selected transaction**.</span></span> <span data-ttu-id="88ae2-121">Avatakse valitud kande üksikasjadega Exceli fail, kus on järgmised töölehed.</span><span class="sxs-lookup"><span data-stu-id="88ae2-121">An Excel file with the details of the selected transaction opens, with the following worksheets:</span></span>

    - <span data-ttu-id="88ae2-122">Read: sellel töölehel on kande päise- ja tooteread ning seotud andmed.</span><span class="sxs-lookup"><span data-stu-id="88ae2-122">Lines: This worksheet has the header and product lines and related data for the transaction.</span></span>
    - <span data-ttu-id="88ae2-123">Maksed: sellel töölehel on kande makseridade üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="88ae2-123">Payments: This worksheet has the details of the payment lines for the transaction.</span></span>
    - <span data-ttu-id="88ae2-124">Allahindlused: sellel töölehel on kande allahindlusega seotud üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="88ae2-124">Discounts: This worksheet has the discount-related details for the transaction.</span></span>
    - <span data-ttu-id="88ae2-125">Maksud: sellel töölehel on kande maksudega seotud üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="88ae2-125">Taxes: This worksheet has the tax-related details for the transaction.</span></span>
    - <span data-ttu-id="88ae2-126">Tasud: sellel töölehel on kande tasudega seotud andmed.</span><span class="sxs-lookup"><span data-stu-id="88ae2-126">Charges: This worksheet has the charges-related data for the transaction.</span></span>

4. <span data-ttu-id="88ae2-127">Exceli failis saate muuta asjakohaseid välju ja seejärel laadida andmed uuesti üles peakontorisse, kasutades Dynamicsi Exceli lisandmooduli avaldamisfunktsiooni.</span><span class="sxs-lookup"><span data-stu-id="88ae2-127">In the Excel file, you modify the appropriate fields and then upload the data back into Headquarters using the Dynamics Excel Add-in publish functionality.</span></span> <span data-ttu-id="88ae2-128">Pärast avaldamist kajastatakse muudatused süsteemis.</span><span class="sxs-lookup"><span data-stu-id="88ae2-128">Once published, the changes will be reflected in the system.</span></span> <span data-ttu-id="88ae2-129">Avaldamise ajal ei läbi kasutajate muudatused ühtegi kinnitamist.</span><span class="sxs-lookup"><span data-stu-id="88ae2-129">During publish, no validation is done on changes that users make.</span></span>

5. <span data-ttu-id="88ae2-130">Muudatuste täieliku kontrolljälje vaatamiseks klõpsake päises **Jaemüügikanne** (päisetaseme muudatuste nägemiseks) ning asjakohase kande lehe asjakohases jaotises ja kirjes valikut **Kuva kontrolljälg**.</span><span class="sxs-lookup"><span data-stu-id="88ae2-130">A complete audit trail of the changes can be viewed by clicking **View audit trail** in the **Retail transaction** header for the header-level changes and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="88ae2-131">Kõik müügiridadega seotud muudatused on näiteks nähtavad lehel **Müügikanded**, maksetega seotud muudatused on nähtavad lehel **Maksekanded** jne. Auditi andmed, mida muudatuste puhul hallatakse, on järgmised.</span><span class="sxs-lookup"><span data-stu-id="88ae2-131">For example, all changes relating to sales lines will be visible on the **Sales transactions** page, changes relating to payments will be visible on the **Payment transactions** page, etc. The audit details that are maintained for the changes are as follows.</span></span>

   - <span data-ttu-id="88ae2-132">Muutmise kuupäev ja kellaaeg</span><span class="sxs-lookup"><span data-stu-id="88ae2-132">Modified date and time</span></span>
   - <span data-ttu-id="88ae2-133">Väli</span><span class="sxs-lookup"><span data-stu-id="88ae2-133">Field</span></span> 
   - <span data-ttu-id="88ae2-134">Varasem väärtus</span><span class="sxs-lookup"><span data-stu-id="88ae2-134">Old value</span></span>
   - <span data-ttu-id="88ae2-135">Uus väärtus</span><span class="sxs-lookup"><span data-stu-id="88ae2-135">New value</span></span>
   - <span data-ttu-id="88ae2-136">Muutja:</span><span class="sxs-lookup"><span data-stu-id="88ae2-136">Modified by</span></span>

6. <span data-ttu-id="88ae2-137">Pärast muudatuste tegemist ja avaldamist käivitage uuesti suvand **Kinnita kaupluse kanded**, et kontrollida, kas teie tehtud muudatused on süsteemsed ja kehtivad.</span><span class="sxs-lookup"><span data-stu-id="88ae2-137">After your changes are made and published, run the **Validate store transactions** option again to validate that the changes you made are consistent and valid.</span></span>

> [!NOTE]
> <span data-ttu-id="88ae2-138">Saate redigeerida ainult kinnituse mitteläbinud kandeid.</span><span class="sxs-lookup"><span data-stu-id="88ae2-138">You can only edit transactions that failed validation.</span></span> <span data-ttu-id="88ae2-139">Kui soovite redigeerida kinnituse läbinud kandeid, määrake muudetava kande kinnitamise olekuks **Tõrge** või **Pole** ja siis saate seda redigeerida.</span><span class="sxs-lookup"><span data-stu-id="88ae2-139">If you want to edit transactions that passed validation, change the validation status of the transaction you want to change to **Error** or **None** and then you will be able to edit it.</span></span> 


## <a name="bulk-edit-transactions"></a><span data-ttu-id="88ae2-140">Kannete hulgiredigeerimine</span><span class="sxs-lookup"><span data-stu-id="88ae2-140">Bulk edit transactions</span></span>

<span data-ttu-id="88ae2-141">Retaili versioonis 10.0.6 ja uuemates toetatakse kannete hulgiredigeerimist väljavõtte tasemel.</span><span class="sxs-lookup"><span data-stu-id="88ae2-141">In Retail version 10.0.6 and higher, the option to bulk edit transactions at a statement level is supported.</span></span> 

1. <span data-ttu-id="88ae2-142">Avage Exceli lisandmooduli abil väljavõte, milles on kanded, mida soovite muuta. Selleks täitke eespool nimetatud juhised 1–3.</span><span class="sxs-lookup"><span data-stu-id="88ae2-142">Use the Excel Add-in to open a statement that has transactions you want to modify using steps 1-3 above.</span></span>

2. <span data-ttu-id="88ae2-143">Valige üks allolevatest suvanditest.</span><span class="sxs-lookup"><span data-stu-id="88ae2-143">Choose one of the options below.</span></span>

    - <span data-ttu-id="88ae2-144">**Redigeeri sularaha- ja vedamiskandeid**.</span><span class="sxs-lookup"><span data-stu-id="88ae2-144">**Edit cash and carry transactions**.</span></span> <span data-ttu-id="88ae2-145">See suvand võimaldab teil redigeerida kõiki väljavõttes sisalduvaid sularaha- ja vedamiskandeid.</span><span class="sxs-lookup"><span data-stu-id="88ae2-145">This option enables you to edit all the cash and carry transactions included in the statement.</span></span> <span data-ttu-id="88ae2-146">Saadaval on järgmised Exceli töölehed.</span><span class="sxs-lookup"><span data-stu-id="88ae2-146">The following Excel worksheets are available.</span></span>
    
       - <span data-ttu-id="88ae2-147">**Kanne**: sellel töölehel on kogu müügikannete päisetaseme teave.</span><span class="sxs-lookup"><span data-stu-id="88ae2-147">**Transaction**: This worksheet has all the header-level information for the sales transactions.</span></span>
       - <span data-ttu-id="88ae2-148">**Müügikanne**: sellel töölehel on kogu müügikannete reataseme teave.</span><span class="sxs-lookup"><span data-stu-id="88ae2-148">**Sales transaction**: This worksheet has all the lines-level information for the sales transactions.</span></span>
       - <span data-ttu-id="88ae2-149">**Maksekanded**: sellel töölehel on kogu müügikannete makseridade teave.</span><span class="sxs-lookup"><span data-stu-id="88ae2-149">**Payment transactions**: This worksheet has all the payment lines information for the sales transactions.</span></span>
       - <span data-ttu-id="88ae2-150">**Allahindluskanded**: sellel töölehel on kogu müügikannete allahindlusridade teave.</span><span class="sxs-lookup"><span data-stu-id="88ae2-150">**Discount transactions**: This worksheet has all the discount lines information for the sales transactions.</span></span>
       - <span data-ttu-id="88ae2-151">**Maksukanded**: sellel töölehel on kogu müügikannete maksuridade teave.</span><span class="sxs-lookup"><span data-stu-id="88ae2-151">**Tax transactions**: This worksheet has all the tax lines information for the sales transactions.</span></span>
       - <span data-ttu-id="88ae2-152">**Tasukanded**: sellel töölehel on kogu müügikannete tasuridade teave.</span><span class="sxs-lookup"><span data-stu-id="88ae2-152">**Charge transactions**: This worksheet has all the charge lines information for the sales transactions.</span></span>

    - <span data-ttu-id="88ae2-153">**Muuda kassahalduskandeid**.</span><span class="sxs-lookup"><span data-stu-id="88ae2-153">**Edit cash management transactions**.</span></span> <span data-ttu-id="88ae2-154">See suvand võimaldab teil redigeerida kõiki väljavõttes sisalduvaid kassahalduskandeid.</span><span class="sxs-lookup"><span data-stu-id="88ae2-154">This option enables you to edit all the cash management transactions included in the statement.</span></span> <span data-ttu-id="88ae2-155">Saadaval on järgmised Exceli töölehed.</span><span class="sxs-lookup"><span data-stu-id="88ae2-155">The following Excel worksheets are available.</span></span>
     
       - <span data-ttu-id="88ae2-156">**Kanne**: sellel töölehel on kogu kassahalduskannete päisetaseme teave.</span><span class="sxs-lookup"><span data-stu-id="88ae2-156">**Transaction**: This worksheet has all the header-level information for the cash management transactions.</span></span>
       - <span data-ttu-id="88ae2-157">**Panka hoiustatud maksevahendi kanded**: sellel töölehel on kõik panka hoiustamise kande üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="88ae2-157">**Bank tender transactions**: This worksheet has all the bank drop transaction details.</span></span>
       - <span data-ttu-id="88ae2-158">**Seifi maksevahendi kanded**: sellel töölehel on kõik seifi hoiustamise kande üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="88ae2-158">**Safe tender transactions**: This worksheet has all the safe drop transaction details.</span></span>
       - <span data-ttu-id="88ae2-159">**Päevakassa**: sellel töölehel on kõik päevakassa kande üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="88ae2-159">**Tender declaration**: This worksheet has all the tender declaration transaction details.</span></span>
       - <span data-ttu-id="88ae2-160">**Tulu/kulu kanne**: sellel töölehel on kõik tulu/-kulu kande rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="88ae2-160">**Income-expense transaction**: This worksheet has all the income-expense transaction line details.</span></span>
       - <span data-ttu-id="88ae2-161">**Maksekanded**: sellel töölehel on kogu toimingu **Arve tasumine** ja samuti tulu/kulu kande maksega seotud teave.</span><span class="sxs-lookup"><span data-stu-id="88ae2-161">**Payment transactions**: This worksheet has all the payment-related information for the **Pay invoice** operation as well as the income-expense transaction.</span></span>

3.  <span data-ttu-id="88ae2-162">Kui avaldate hulgiredigeeritud kandeid, siis kinnitamisi ei tehta.</span><span class="sxs-lookup"><span data-stu-id="88ae2-162">Validations are not performed when you publish bulk edited transactions.</span></span> <span data-ttu-id="88ae2-163">Peate veenduma, et kõik teie muudatused on täpsed ja andmete kvaliteet on kõigil töölehtedel tagatud.</span><span class="sxs-lookup"><span data-stu-id="88ae2-163">You must ensure that all your edits are accurate and the fidelity of data across the worksheets is maintained.</span></span> <span data-ttu-id="88ae2-164">Kui soovite näiteks muuta kande kuupäeva, et hallata stsenaariume, kus avatud kannete rahandus- või laovarude periood suletakse, peate muutma kuupäeva kõigil Exceli töölehtedel, millel on veerg **Ärikuupäev**.</span><span class="sxs-lookup"><span data-stu-id="88ae2-164">For example, if you want to change the transaction date to manage the scenarios where the fiscal or inventory period for the open transactions is closed, you need to change the date on all the Excel worksheets that have the **Business date** column.</span></span> <span data-ttu-id="88ae2-165">Kannete kinnitamiseks pärast nende redigeerimist saate lehel **Väljavõtted** kasutada valikut **Kinnita kanded uuesti**.</span><span class="sxs-lookup"><span data-stu-id="88ae2-165">To validate transactions after they have been edited, you can use **Revalidate transactions** on the **Statements** page.</span></span>
