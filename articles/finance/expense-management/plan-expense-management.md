---
title: Kuluhalduse konfigureerimine
description: Selles artiklis kirjeldatakse kaalutlusi ja otsuseid, mille peate protsessi plaanimise käigus tegema, enne kui Microsoft Dynamics 365 Finance'is kuluhaldust konfigureerite.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 57a7cf4f6e6aaebd5d2a0ade84e0e9399e9086e1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187517"
---
# <a name="configure-expense-management"></a><span data-ttu-id="821cf-103">Kuluhalduse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="821cf-103">Configure expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="821cf-104">Selles teemas kirjeldatakse kaalutlusi ja otsuseid, mille peate protsessi plaanimise käigus tegema, enne kui kuluhaldust konfigureerite.</span><span class="sxs-lookup"><span data-stu-id="821cf-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="821cf-105">Kuluhalduses saate salvestada teavet makseviiside, reisitellimuste, kuluaruannete, poliitikate jne kohta.</span><span class="sxs-lookup"><span data-stu-id="821cf-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="821cf-106">Kuna paljud otsused, mida kuluhalduse konfiguratsiooni plaanimisel langetate, põhinevad organisatsiooni hierarhial ja finantsstruktuuril, tuleb juhinduda nende valdkondade plaanimisdokumentidest.</span><span class="sxs-lookup"><span data-stu-id="821cf-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="821cf-107">Kontsernisisesed kulud</span><span class="sxs-lookup"><span data-stu-id="821cf-107">Intercompany expenses</span></span>

<span data-ttu-id="821cf-108">Kui lubate ettevõttesisesed kulud, lubate juriidilistele isikutel ja töötajatel tekitada kulusid teise juriidilise isiku nimel ja koguda oma organisatsiooni kuuluvalt tööandjast juriidiliselt isikult makseid.</span><span class="sxs-lookup"><span data-stu-id="821cf-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="821cf-109">Näiteks juriidilise isiku A töötaja viib läbi projekti juriidilisele isikule B ja projektiga kaasnevad reisimisega seotud kulud.</span><span class="sxs-lookup"><span data-stu-id="821cf-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="821cf-110">Kui ettevõttesisesed kulud on lubatud, võib töötaja siis esitada juriidilisele isikule B kuluaruande ja kulud peab kandma siis juriidiline isik A. Kui teie organisatsioonis pole mitut juriidilist isikut, pole vaja ettevõttesiseseid kulusid lubada.</span><span class="sxs-lookup"><span data-stu-id="821cf-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="821cf-111">**Otsus:** kas soovite lubada ettevõttesisesed kulud?</span><span class="sxs-lookup"><span data-stu-id="821cf-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="821cf-112">Finantshaldus</span><span class="sxs-lookup"><span data-stu-id="821cf-112">Financial management</span></span>

<span data-ttu-id="821cf-113">Kuluhaldus on tihedalt seotud organisatsiooni finantshaldusega.</span><span class="sxs-lookup"><span data-stu-id="821cf-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="821cf-114">Suur osa kuluhalduse konfiguratsioonist põhineb otsustel, mille olete oma organisatsiooni finantside kohta langetanud.</span><span class="sxs-lookup"><span data-stu-id="821cf-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="821cf-115">Järgmised jaotised kirjeldavad mitmesuguseid valdkondi, kus on vajalik plaanimine ja otsustamine organisatsiooni rahaliste otsuste ja juhtkonna juhiste põhjal.</span><span class="sxs-lookup"><span data-stu-id="821cf-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="821cf-116">Päevarahad</span><span class="sxs-lookup"><span data-stu-id="821cf-116">Per diems</span></span>

<span data-ttu-id="821cf-117">Peate määratlema töötajate päevarahad, mida teie organisatsioon maksab.</span><span class="sxs-lookup"><span data-stu-id="821cf-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="821cf-118">Kuna päevarahasid kasutatakse tavaliselt selliste kulude katmiseks nagu toitlustus, majutus ja muud ettenägematud kulud, saate koostada ettevõtte makstavate päevarahade reeglid.</span><span class="sxs-lookup"><span data-stu-id="821cf-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="821cf-119">Päevaraha määrade aluseks võib olla aastaaeg, reisisiht või mõlemad.</span><span class="sxs-lookup"><span data-stu-id="821cf-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="821cf-120">Päevaraha reegli määratlemisel saate valida päevaraha määrast mingi protsendi kinnipidamise, kui töötaja saab tasuta eineid või teenuseid.</span><span class="sxs-lookup"><span data-stu-id="821cf-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="821cf-121">Saate määratleda ka päevaraha määrade järgud, määrates minimaalse ja maksimaalse tundide arvu, millele päevaraha määr töötaja reisi ajal rakendatakse.</span><span class="sxs-lookup"><span data-stu-id="821cf-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="821cf-122">**Otsused.**</span><span class="sxs-lookup"><span data-stu-id="821cf-122">**Decisions:**</span></span>

- <span data-ttu-id="821cf-123">Esimese ja viimase päeva vaikepäevaraha reeglid:</span><span class="sxs-lookup"><span data-stu-id="821cf-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="821cf-124">Milline on minimaalne tundide arv, mida töötaja saab ühes päevas taotleda ja siiski päevaraha saada?</span><span class="sxs-lookup"><span data-stu-id="821cf-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="821cf-125">Kas esimese ja viimase päeva puhul vähendatakse toitlustusele kuluvat summat?</span><span class="sxs-lookup"><span data-stu-id="821cf-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="821cf-126">Kui nii, siis milline on vähendamise protsent?</span><span class="sxs-lookup"><span data-stu-id="821cf-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="821cf-127">Kas esimese ja viimase päeva puhul vähendatakse hotellile kuluvat summat?</span><span class="sxs-lookup"><span data-stu-id="821cf-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="821cf-128">Kui nii, siis milline on vähendamise protsent?</span><span class="sxs-lookup"><span data-stu-id="821cf-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="821cf-129">Kas esimese ja viimase päeva puhul vähendatakse muude kulude summat?</span><span class="sxs-lookup"><span data-stu-id="821cf-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="821cf-130">Kui nii, siis milline on vähendamise protsent?</span><span class="sxs-lookup"><span data-stu-id="821cf-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="821cf-131">Päevaraha vaikereeglid:</span><span class="sxs-lookup"><span data-stu-id="821cf-131">Default per diem rules:</span></span>

    - <span data-ttu-id="821cf-132">Kas päevaraha vähendatakse protsentuaalselt iga toidukorra kohta, kui näiteks tasuta toitlustust pakutakse?</span><span class="sxs-lookup"><span data-stu-id="821cf-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="821cf-133">Kui nii, siis milline on vähendamise protsent iga toidukorra kohta?</span><span class="sxs-lookup"><span data-stu-id="821cf-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="821cf-134">Kas toitlustamisega seotud vähendamine arvutatakse päeva, reisi või päevase toidukordade arvu alusel?</span><span class="sxs-lookup"><span data-stu-id="821cf-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="821cf-135">Kas päevarahasummad tuleks ümardada tavalisel viisil või üles?</span><span class="sxs-lookup"><span data-stu-id="821cf-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="821cf-136">Kas päevarahade arvutused põhinevad 24-tunnisel perioodil või kalendripäeval?</span><span class="sxs-lookup"><span data-stu-id="821cf-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="821cf-137">Päevaraha reeglid asukoha alusel.</span><span class="sxs-lookup"><span data-stu-id="821cf-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="821cf-138">Kas päevarahamäärad erinevad asukoha järgi?</span><span class="sxs-lookup"><span data-stu-id="821cf-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="821cf-139">Milliseid asukohti arvestatakse?</span><span class="sxs-lookup"><span data-stu-id="821cf-139">What locations are included?</span></span>
    - <span data-ttu-id="821cf-140">Kui päevarahamäärade erinevad asukohtade järgi, siis milline protsendisumma järgmist tüüpi kulude puhul määratakse.</span><span class="sxs-lookup"><span data-stu-id="821cf-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="821cf-141">Toitlustus</span><span class="sxs-lookup"><span data-stu-id="821cf-141">Meals</span></span>
        - <span data-ttu-id="821cf-142">Hotell</span><span class="sxs-lookup"><span data-stu-id="821cf-142">Hotel</span></span>
        - <span data-ttu-id="821cf-143">Muud kulud</span><span class="sxs-lookup"><span data-stu-id="821cf-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="821cf-144">Kuluhalduse töölehed ja kontod</span><span class="sxs-lookup"><span data-stu-id="821cf-144">Expense management journals and accounts</span></span>

<span data-ttu-id="821cf-145">Kuluhaldus nõuab, et kasutaksite mitut töölehte ja kontot.</span><span class="sxs-lookup"><span data-stu-id="821cf-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="821cf-146">Peate näiteks otsustama, kas avansimaksete ja krediitkaardivaidluste jaoks kasutatakse sama kontot.</span><span class="sxs-lookup"><span data-stu-id="821cf-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="821cf-147">**Otsused.**</span><span class="sxs-lookup"><span data-stu-id="821cf-147">**Decisions:**</span></span>

- <span data-ttu-id="821cf-148">Millistele pearaamatukontodele kinnitatud kuluaruanded sisestatakse?</span><span class="sxs-lookup"><span data-stu-id="821cf-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="821cf-149">Millist kontot kasutatakse avansimaksete puhul?</span><span class="sxs-lookup"><span data-stu-id="821cf-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="821cf-150">Kas avansimaksed tuleks kohe sisestada?</span><span class="sxs-lookup"><span data-stu-id="821cf-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="821cf-151">Makseviisid</span><span class="sxs-lookup"><span data-stu-id="821cf-151">Payment methods</span></span>

<span data-ttu-id="821cf-152">Kui lubate töötajatel ettevõtte nimel kulusid tekitada, peate määratlema makseviisid, mida töötajatel on lubatud kasutada.</span><span class="sxs-lookup"><span data-stu-id="821cf-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="821cf-153">Näiteks võite lubada töötajatel kasutada sularaha või ettevõtte krediitkaarti.</span><span class="sxs-lookup"><span data-stu-id="821cf-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="821cf-154">Võib lubada töötajatel kasutada ka isiklikku krediitkaarti ja seejärel töötajatele kulud korvata.</span><span class="sxs-lookup"><span data-stu-id="821cf-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="821cf-155">Iga lubatud makseviisi puhul tuleb teha järgmised otsused.</span><span class="sxs-lookup"><span data-stu-id="821cf-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="821cf-156">**Otsused:**</span><span class="sxs-lookup"><span data-stu-id="821cf-156">**Decisions:**</span></span>

- <span data-ttu-id="821cf-157">Millised makseviisid on lubatud?</span><span class="sxs-lookup"><span data-stu-id="821cf-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="821cf-158">Kellele kuuluvad makseviisi kulud?</span><span class="sxs-lookup"><span data-stu-id="821cf-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="821cf-159">Kas on olemas vastaskonto tüüp?</span><span class="sxs-lookup"><span data-stu-id="821cf-159">Is there an offset account type?</span></span> <span data-ttu-id="821cf-160">Kui on olemas vastaskonto tüüp, siis mis see on?</span><span class="sxs-lookup"><span data-stu-id="821cf-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="821cf-161">Kui on olemas vastaskonto, milline see konto on?</span><span class="sxs-lookup"><span data-stu-id="821cf-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="821cf-162">Kui makseviis on krediitkaart, kas makseviisi tuleks kasutada ainult imporditud kannetega?</span><span class="sxs-lookup"><span data-stu-id="821cf-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="821cf-163">Kulukategooriad ja jagatud kategooriad</span><span class="sxs-lookup"><span data-stu-id="821cf-163">Expense categories and shared categories</span></span>

<span data-ttu-id="821cf-164">Kui töötajad koostavad kuluaruande, tuleb iga kulu, mille nad seal kajastavad, seostada kulukategooriaga.</span><span class="sxs-lookup"><span data-stu-id="821cf-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="821cf-165">Kulukategooriad on tuletatud jagatud kategooriatest, mida saab jagada kõigi organisatsiooni juriidiliste isikute vahel.</span><span class="sxs-lookup"><span data-stu-id="821cf-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="821cf-166">Neid kategooriaid saab jagada ka projektijuhtimise ja raamatupidamise moodulites, olenevalt sellest, kuidas teie organisatsioon on määratletud.</span><span class="sxs-lookup"><span data-stu-id="821cf-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="821cf-167">Organisatsiooni määratluse ja rakendustöörühma juhtimise alusel saate määrata, kas kuluhalduses kasutatavaid kategooriaid kasutatakse ainult kuluhalduses või neid tuleks projektihalduse ja raamatupidamise ning kuluhalduse vahel jagada.</span><span class="sxs-lookup"><span data-stu-id="821cf-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="821cf-168">Arvestage, et neid kategooriaid saab jagada projekti ja kulu või projekti ja tootmise vahel, kuid mitte kulu ja tootmise vahel.</span><span class="sxs-lookup"><span data-stu-id="821cf-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="821cf-169">Peate langetama iga kulukategooria kohta järgmised otsused.</span><span class="sxs-lookup"><span data-stu-id="821cf-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="821cf-170">**Otsused.**</span><span class="sxs-lookup"><span data-stu-id="821cf-170">**Decisions:**</span></span>

- <span data-ttu-id="821cf-171">Milline on kulukategooria?</span><span class="sxs-lookup"><span data-stu-id="821cf-171">What is the expense category?</span></span> <span data-ttu-id="821cf-172">Näited hõlmavad lendude, hotelli või läbisõidu kategooriaid.</span><span class="sxs-lookup"><span data-stu-id="821cf-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="821cf-173">Kas seda kulukategooriat saab kasutada ka moodulis Projektihaldus ja raamatupidamine?</span><span class="sxs-lookup"><span data-stu-id="821cf-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="821cf-174">Milline on kulutüüp?</span><span class="sxs-lookup"><span data-stu-id="821cf-174">What is the expense type?</span></span>
- <span data-ttu-id="821cf-175">Milline on kulukategooria vaikemakseviis?</span><span class="sxs-lookup"><span data-stu-id="821cf-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="821cf-176">Kas kulukategoorias olevad kulud tuleb loetleda üksikasjalikult?</span><span class="sxs-lookup"><span data-stu-id="821cf-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="821cf-177">Milline on kulukategooria peamine vaikekonto?</span><span class="sxs-lookup"><span data-stu-id="821cf-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="821cf-178">Mis on selle kulukategooria kauba käibemaksu vaikegrupp?</span><span class="sxs-lookup"><span data-stu-id="821cf-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="821cf-179">Kas selle kulukategooria puhul on lubatud täiendavad makseviisid?</span><span class="sxs-lookup"><span data-stu-id="821cf-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="821cf-180">Kui on lubatud täiendavad makseviisid, siis mis need on?</span><span class="sxs-lookup"><span data-stu-id="821cf-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="821cf-181">Kas selles kulukategoorias on alamkategooriaid?</span><span class="sxs-lookup"><span data-stu-id="821cf-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="821cf-182">Kui on alamkategooriaid, siis tuleb teha ka järgmised otsused.</span><span class="sxs-lookup"><span data-stu-id="821cf-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="821cf-183">kas mõni alamkategooria on maksu korvamisest välja jäetud?</span><span class="sxs-lookup"><span data-stu-id="821cf-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="821cf-184">Milline on alamkategooriate kauba käibemaksugrupp?</span><span class="sxs-lookup"><span data-stu-id="821cf-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="821cf-185">Kui seda kulukategooriat kasutatakse ka moodulis Projektihaldus ja raamatupidamine, siis vastake ülejäänud küsimustele.</span><span class="sxs-lookup"><span data-stu-id="821cf-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="821cf-186">Vastasel korral minge edasi järgmisse jaotisse.</span><span class="sxs-lookup"><span data-stu-id="821cf-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="821cf-187">Milliseid kulukontosid järgmiste kulude puhul kasutatakse?</span><span class="sxs-lookup"><span data-stu-id="821cf-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="821cf-188">Kulu</span><span class="sxs-lookup"><span data-stu-id="821cf-188">Cost</span></span>
    - <span data-ttu-id="821cf-189">Palga eraldamine</span><span class="sxs-lookup"><span data-stu-id="821cf-189">Payroll allocation</span></span>
    - <span data-ttu-id="821cf-190">Lõpetamata toodang - omahind</span><span class="sxs-lookup"><span data-stu-id="821cf-190">WIP-cost value</span></span>
    - <span data-ttu-id="821cf-191">Kulu – kaup</span><span class="sxs-lookup"><span data-stu-id="821cf-191">Cost-item</span></span>
    - <span data-ttu-id="821cf-192">Lõpetamata toodang - Omahind - Kaup</span><span class="sxs-lookup"><span data-stu-id="821cf-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="821cf-193">Tekkepõhine kahjum</span><span class="sxs-lookup"><span data-stu-id="821cf-193">Accrued loss</span></span>
    - <span data-ttu-id="821cf-194">Lõpetamata toodang – Tekkepõhine kahjum</span><span class="sxs-lookup"><span data-stu-id="821cf-194">WIP-accrued loss</span></span>

- <span data-ttu-id="821cf-195">Milliseid tulukontosid järgmiste puhul kasutatakse?</span><span class="sxs-lookup"><span data-stu-id="821cf-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="821cf-196">Arveldatud tulu</span><span class="sxs-lookup"><span data-stu-id="821cf-196">Invoiced revenue</span></span>
    - <span data-ttu-id="821cf-197">Viittulu – müügihind</span><span class="sxs-lookup"><span data-stu-id="821cf-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="821cf-198">Lõpetamata toodang – müügihind</span><span class="sxs-lookup"><span data-stu-id="821cf-198">WIP-sales value</span></span>
    - <span data-ttu-id="821cf-199">Viittulu – tootmine</span><span class="sxs-lookup"><span data-stu-id="821cf-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="821cf-200">Lõpetamata toodang – tootmine</span><span class="sxs-lookup"><span data-stu-id="821cf-200">WIP-production</span></span>
    - <span data-ttu-id="821cf-201">Viittulu – kasum</span><span class="sxs-lookup"><span data-stu-id="821cf-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="821cf-202">Lõpetamata toodang – kasum</span><span class="sxs-lookup"><span data-stu-id="821cf-202">WIP-profit</span></span>
    - <span data-ttu-id="821cf-203">Viittulu – kordustellimus</span><span class="sxs-lookup"><span data-stu-id="821cf-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="821cf-204">Lõpetamata toodang – kordustellimus</span><span class="sxs-lookup"><span data-stu-id="821cf-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="821cf-205">Maksud</span><span class="sxs-lookup"><span data-stu-id="821cf-205">Taxes</span></span>

<span data-ttu-id="821cf-206">Kuludega seotud maksude puhul tuleb määratleda, mis kuluaruannetes sisaldub või seal lubatud on.</span><span class="sxs-lookup"><span data-stu-id="821cf-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="821cf-207">**Otsused.**</span><span class="sxs-lookup"><span data-stu-id="821cf-207">**Decisions:**</span></span>

- <span data-ttu-id="821cf-208">Kas kulusummades sisaldub käibemaks?</span><span class="sxs-lookup"><span data-stu-id="821cf-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="821cf-209">Kas kulude puhul tuleks maksu korvamine lubada?</span><span class="sxs-lookup"><span data-stu-id="821cf-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="821cf-210">Kui otsustasite pearaamatu plaanimisel rakendada USA käibemaksu ja kasutada maksureegleid, siis ei saa kuludelt maksu korvamist lubada.</span><span class="sxs-lookup"><span data-stu-id="821cf-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="821cf-211">(USA käibemaksu rakendamiseks ja maksureeglite kasutamiseks määrake valiku **Rakenda käibemaksu maksustamisreeglid** väärtuseks **Jah**.)</span><span class="sxs-lookup"><span data-stu-id="821cf-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="821cf-212">Poliitikad</span><span class="sxs-lookup"><span data-stu-id="821cf-212">Policies</span></span>

<span data-ttu-id="821cf-213">Kuluaruande poliitikate loomisega saate aidata oma organisatsioonil säästa aega ja raha, kui töötajatel organisatsiooni nimel tegutsedes kulud tekivad.</span><span class="sxs-lookup"><span data-stu-id="821cf-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="821cf-214">Poliitikad aitavad tagada, et töötajad püsiksid eelarves, esitavad kõik vajaliku teabe ja kulutaksid raha ainult vajalikul viisil.</span><span class="sxs-lookup"><span data-stu-id="821cf-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="821cf-215">Iga loodava kuluaruande poliitika ja iga kuluaruande kinnitamispoliitika puhul tuleb teha järgmised otsused.</span><span class="sxs-lookup"><span data-stu-id="821cf-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="821cf-216">**Otsused.**</span><span class="sxs-lookup"><span data-stu-id="821cf-216">**Decisions:**</span></span>

- <span data-ttu-id="821cf-217">Mis on poliitika nimi?</span><span class="sxs-lookup"><span data-stu-id="821cf-217">What is the name of the policy?</span></span>
- <span data-ttu-id="821cf-218">Mille jaoks kulupoliitika mõeldud on?</span><span class="sxs-lookup"><span data-stu-id="821cf-218">What is the expense policy for?</span></span>
- <span data-ttu-id="821cf-219">Kui otsustasite eelnevalt lubada ettevõttesiseseid kulusid, siis millistele teie organisatsiooni ettevõtetele poliitika kehtib?</span><span class="sxs-lookup"><span data-stu-id="821cf-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="821cf-220">Millal poliitika jõustub?</span><span class="sxs-lookup"><span data-stu-id="821cf-220">When does the policy become effective?</span></span>
- <span data-ttu-id="821cf-221">Millal poliitika aegub?</span><span class="sxs-lookup"><span data-stu-id="821cf-221">When does the policy expire?</span></span>
- <span data-ttu-id="821cf-222">Mis see poliitikareegel on?</span><span class="sxs-lookup"><span data-stu-id="821cf-222">What is the policy rule?</span></span>
- <span data-ttu-id="821cf-223">Mis on selle poliitikareegli tulemus?</span><span class="sxs-lookup"><span data-stu-id="821cf-223">What is the outcome of the policy rule?</span></span>
