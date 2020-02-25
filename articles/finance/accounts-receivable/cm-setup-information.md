---
title: Krediidihalduse seadistamine
description: See teema kirjeldab kreeditihalduseks vajalikku seadistust.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c54c74af6f2c1be9aedfa792d0676d1165fb0ab8
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015194"
---
# <a name="credit-management-setup"></a><span data-ttu-id="47441-103">Krediidihalduse seadistamine</span><span class="sxs-lookup"><span data-stu-id="47441-103">Credit management setup</span></span> 

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="credit-management-workflows"></a><span data-ttu-id="47441-104">Krediidihalduse töövood</span><span class="sxs-lookup"><span data-stu-id="47441-104">Credit management workflows</span></span>

<span data-ttu-id="47441-105">Krediidilimiidi korrigeerimiste haldamiseks kasutatavate töövoogude määratlemiseks avage **Krediit ja võlanõuded \> Seadistus \> Krediidihalduse töövood**.</span><span class="sxs-lookup"><span data-stu-id="47441-105">Go to **Credit and collections \> Setup \> Credit management workflows** to define the workflows that are used to manage credit limit adjustments.</span></span>

- <span data-ttu-id="47441-106">Saate luua töövoo, mis võimaldab teil üheainsa kinnitamisega kinnitada krediidilimiitide korrigeerimiste partii.</span><span class="sxs-lookup"><span data-stu-id="47441-106">You can create a workflow that lets you approve a batch of credit limits adjustments through a single approval.</span></span>
- <span data-ttu-id="47441-107">Saate lisada töövoo rea tasemel, nii et krediidilimiidi korrigeerimisi saab kinnitada ükshaaval.</span><span class="sxs-lookup"><span data-stu-id="47441-107">You can add a workflow at the line level, so that credit limit adjustments can be approved individually.</span></span>
- <span data-ttu-id="47441-108">Saate luua väljalaske töövoo, mis suunab ootelolekud automaatselt töövoo protsessi.</span><span class="sxs-lookup"><span data-stu-id="47441-108">You can create a release workflow that automatically routes holds to a workflow process.</span></span>

## <a name="blocking-rules"></a><span data-ttu-id="47441-109">Blokeerimise reeglid</span><span class="sxs-lookup"><span data-stu-id="47441-109">Blocking rules</span></span>

### <a name="ranking-payment-terms"></a><span data-ttu-id="47441-110">Maksetingimuste hindamine</span><span class="sxs-lookup"><span data-stu-id="47441-110">Ranking payment terms</span></span>

<span data-ttu-id="47441-111">Saate müügitellimuse ootele panna, kui tellimuse maksetingimused ei vasta kliendi vaikimisi maksetingimustele.</span><span class="sxs-lookup"><span data-stu-id="47441-111">You can put a sales order on hold if the payment terms on the order don't match the default payment terms for the customer.</span></span> <span data-ttu-id="47441-112">Siiski on vahel maksetingimused erinevad, kuid siiski piisavalt sarnased, et te ei soovi tellimust ootele panna.</span><span class="sxs-lookup"><span data-stu-id="47441-112">However, sometimes the payment terms differ but are similar enough that you don't want to put the order on hold.</span></span> <span data-ttu-id="47441-113">Saate järjestada maksetingimusi nii, et mõnel neist on sama aste, samas kui teistel on kõrgem või madalam aste.</span><span class="sxs-lookup"><span data-stu-id="47441-113">You can rank payment terms so that some of them have the same rank, whereas others have a higher or lower rank.</span></span>

<span data-ttu-id="47441-114">Kui maksetingimuste reitingud on aktiivsed, pannakse müügitellimused ootele, kui tellimuse maksetingimustel on kõrgem aste kui kliendi vaikimisi maksetingimustel.</span><span class="sxs-lookup"><span data-stu-id="47441-114">If the rankings for payment terms are active, the sales orders will be put on hold if the payment terms on the order have a higher rank than the default payment terms for the customer.</span></span>

### <a name="ranking-settlement-discounts"></a><span data-ttu-id="47441-115">Tasakaalustuse allahindluste hindamine</span><span class="sxs-lookup"><span data-stu-id="47441-115">Ranking settlement discounts</span></span>

<span data-ttu-id="47441-116">Saate müügitellimuse ootele panna, kui tellimuse skonto ei vasta kliendi vaikimisi skontole.</span><span class="sxs-lookup"><span data-stu-id="47441-116">You can put a sales order on hold if the cash discount on the order doesn't match the default cash discount for the customer.</span></span> <span data-ttu-id="47441-117">Siiski on vahel skontod erinevad, kuid siiski piisavalt sarnased, et te ei soovi tellimust ootele panna.</span><span class="sxs-lookup"><span data-stu-id="47441-117">However, sometimes the cash discounts differ but are similar enough that you don't want to put the order on hold.</span></span> <span data-ttu-id="47441-118">Saate järjestada skontosid nii, et mõnel neist on sama aste, samas kui teistel on kõrgem või madalam aste.</span><span class="sxs-lookup"><span data-stu-id="47441-118">You can rank cash discounts so that some of them have the same rank, whereas others have a higher or lower rank.</span></span>

<span data-ttu-id="47441-119">Kui tasakaalustuste allahindlused on aktiivsed, pannakse müügitellimused ootele, kui tellimuse skontol on kõrgem aste kui kliendi vaikimisi skontol.</span><span class="sxs-lookup"><span data-stu-id="47441-119">If rankings for settlement discounts are active, the sales orders will be put on hold if the cash discount on the order has a higher rank than the default cash discount for the customer.</span></span>

## <a name="reasons"></a><span data-ttu-id="47441-120">Põhjused</span><span class="sxs-lookup"><span data-stu-id="47441-120">Reasons</span></span>

<span data-ttu-id="47441-121">Krediidihalduses kasutatakse mitut tüüpi põhjuseid.</span><span class="sxs-lookup"><span data-stu-id="47441-121">Several types of reasons are used in Credit management:</span></span>

- <span data-ttu-id="47441-122">Ootelepaneku põhjused näitavad, miks müügitellimus ootele pandi.</span><span class="sxs-lookup"><span data-stu-id="47441-122">Hold reasons indicate why a sales order was put on hold.</span></span>
- <span data-ttu-id="47441-123">Vabastamise põhjused määratakse tellimusele, kui see ootelt vabastatakse.</span><span class="sxs-lookup"><span data-stu-id="47441-123">Release reasons are assigned to an order when it's released from hold.</span></span>
- <span data-ttu-id="47441-124">Oleku põhjused näitavad, miks kliendile teatud konto olek määrati.</span><span class="sxs-lookup"><span data-stu-id="47441-124">Status reasons indicate why an account status was assigned to a customer.</span></span>

<span data-ttu-id="47441-125">Põhjuseid saate seadistada lehel **Krediidihalduse põhjused** (**Krediidihaldus \> Seadistus \> Krediidihaldus \> Krediidihalduse põhjused**).</span><span class="sxs-lookup"><span data-stu-id="47441-125">You can set up reasons on the **Credit management reasons** page (**Credit management \> Setup \> Credit management \> Credit management reasons**).</span></span>

1. <span data-ttu-id="47441-126">Valige väljal **Põhjuse tüüp** põhjuse tüüp: **Ootel**, **Vabasta**või **Olek**.</span><span class="sxs-lookup"><span data-stu-id="47441-126">In the **Reason type** field, select the type of reason: **Hold**, **Release**, or **Status**.</span></span>
2. <span data-ttu-id="47441-127">Sisestage väljale **Põhjus** põhjuse nimi.</span><span class="sxs-lookup"><span data-stu-id="47441-127">In the **Reason** field, enter a name for the reason.</span></span>
3. <span data-ttu-id="47441-128">Sisestage välja **Kirjeldus** põhjusekoodi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="47441-128">In the **Description** field, enter a description of the reason code.</span></span>

## <a name="credit-management-groups"></a><span data-ttu-id="47441-129">Krediidihalduse grupid</span><span class="sxs-lookup"><span data-stu-id="47441-129">Credit management groups</span></span>

<span data-ttu-id="47441-130">Krediidihalduse gruppe kasutatakse nende klientide või kliendigruppide tuvastamiseks, kellel on samad krediidihalduse atribuudid.</span><span class="sxs-lookup"><span data-stu-id="47441-130">Credit management groups are used to identify customers or groups of customers that have the same credit management properties.</span></span> <span data-ttu-id="47441-131">Näiteks saab krediidihalduse gruppe kasutada klientide blokeerimise ja välistamise krediidihalduse reeglite määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="47441-131">For example, credit management groups can be used to determine the blocking and exclusion credit management rules for customers.</span></span>

<span data-ttu-id="47441-132">Krediidihalduse gruppe saate luua lehel **Krediidihalduse grupid** (**Krediidihaldus \> Seadistus> Gruppide seadistus \> Krediidihalduse grupid**).</span><span class="sxs-lookup"><span data-stu-id="47441-132">You can create credit management groups on the **Credit management groups** page (**Credit management \> Setup> Groups setup \> Credit management groups**).</span></span>

1. <span data-ttu-id="47441-133">Valige uue rea loomiseks suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="47441-133">Select **New** to create a line.</span></span>
2. <span data-ttu-id="47441-134">Sisestage grupi ID.</span><span class="sxs-lookup"><span data-stu-id="47441-134">Enter an ID for the group.</span></span> <span data-ttu-id="47441-135">ID-l võib olla kuni 10 tähemärki.</span><span class="sxs-lookup"><span data-stu-id="47441-135">The ID can have up to 10 characters.</span></span>
3. <span data-ttu-id="47441-136">Sisestage väljale **Kirjeldus** grupi nimi.</span><span class="sxs-lookup"><span data-stu-id="47441-136">In the **Description** field, enter a name for the group.</span></span> <span data-ttu-id="47441-137">Nimes võib olla kuni 60 tähemärki.</span><span class="sxs-lookup"><span data-stu-id="47441-137">The name can have up to 60 characters.</span></span>

<span data-ttu-id="47441-138">Krediidihalduse grupp määratakse kliendile vahekaardil **Krediit ja võlanõuded** lehel **Kõik kliendid** (**Müügireskontro \> Kliendid \> Kõik kliendid**).</span><span class="sxs-lookup"><span data-stu-id="47441-138">The credit management group is assigned to a customer on the **Credit and collections** FastTab of the **All customers** page (**Account receivable \> Customers \> All customers**).</span></span>

## <a name="account-statuses"></a><span data-ttu-id="47441-139">Konto olekud</span><span class="sxs-lookup"><span data-stu-id="47441-139">Account statuses</span></span>

<span data-ttu-id="47441-140">Saate luua konto olekuid kliendi konto kreediti seisu tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="47441-140">You can create account statuses to identify the credit standing of a customer account.</span></span> <span data-ttu-id="47441-141">Saate määrata oleku ja selle mõju arveldamisele ning ootel kättetoimetamise protsessidele.</span><span class="sxs-lookup"><span data-stu-id="47441-141">You can define a status and its effect on the invoicing and delivery on-hold processes.</span></span> <span data-ttu-id="47441-142">Konto olekuid saab kasutada ka kliendi blokeerimise reeglite määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="47441-142">Account statuses can also be used to determine blocking rules for a customer.</span></span>

<span data-ttu-id="47441-143">Konto olekuid saate luua lehel **Konto olekud** (**Krediidihaldus \> Seadistus> Gruppide seadistus \> Konto olekud**).</span><span class="sxs-lookup"><span data-stu-id="47441-143">You can create account statuses on the **Account statuses** page (**Credit management \> Setup> Groups setup \> Account statuses**).</span></span>

1. <span data-ttu-id="47441-144">Lisage konto olek ja sisestage kirjeldus, mis tähistab kliendi krediidi seisu.</span><span class="sxs-lookup"><span data-stu-id="47441-144">Add an account status, and enter a description that represents the credit standing for a customer.</span></span> <span data-ttu-id="47441-145">Näiteks kasutage **Normaalne**, et näidata, et klient on heas seisus ja avatud tellimustele kehtib standardne krediidihalduse töötlemine.</span><span class="sxs-lookup"><span data-stu-id="47441-145">For example, use **Normal** to indicate that a customer is in good standing and open orders are subject to standard credit management processing.</span></span>
2. <span data-ttu-id="47441-146">Valige väljadel **Arveldamine** ja **Tarne ootel** ooteloleku tüüp, mis peaks kehtima selle konto olekuga klientide korral.</span><span class="sxs-lookup"><span data-stu-id="47441-146">In the **Invoicing** and **Delivery on Hold** fields, select the type of hold that should occur for customers who have this account status.</span></span> <span data-ttu-id="47441-147">Võite panna ootele kogu töötlemise, panna ootele ainult arve töötlemise või üldse töötlemist ootele mitte panna, kui rakendatakse krediidilimiidi reegleid.</span><span class="sxs-lookup"><span data-stu-id="47441-147">You can hold all processing, hold only invoice processing, or hold no processing when the credit limit rules are applied.</span></span>

## <a name="scoring-groups"></a><span data-ttu-id="47441-148">Hindamisgrupid</span><span class="sxs-lookup"><span data-stu-id="47441-148">Scoring groups</span></span>

<span data-ttu-id="47441-149">Saate seada sisse punktigrupid riskifaktorite määratlemiseks ning kriteeriumid nende mõõtmiseks.</span><span class="sxs-lookup"><span data-stu-id="47441-149">You can set up scoring groups to define risk factors and the criteria that are used to measure them.</span></span> <span data-ttu-id="47441-150">Kui punktigruppi lisatakse andmeid kliendi kohta, arvutatakse iga riskifaktori kohta punktisumma ja kasutatakse seda kliendi riskigruppi panemiseks.</span><span class="sxs-lookup"><span data-stu-id="47441-150">When information about a customer is applied to a scoring group, a score is calculated for each risk factor and used to put the customer in a risk group.</span></span> <span data-ttu-id="47441-151">Riskigruppi saab kasutada krediidiriski tuvastamiseks ja automaatsete krediidilimiitide arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="47441-151">The risk group can be used to identify credit worthiness and calculate automatic credit limits.</span></span>

<span data-ttu-id="47441-152">Punktigruppe saate luua lehel **Punktigrupid** (**Krediidihaldus \> Seadistus \> Riski seadistus \> Punktigrupid**).</span><span class="sxs-lookup"><span data-stu-id="47441-152">You can create scoring groups on the **Scoring groups** page (**Credit management \> Setup \> Risk setup \> Scoring groups**).</span></span>

1. <span data-ttu-id="47441-153">Looge punktigrupp ja sisestage sellele nimi.</span><span class="sxs-lookup"><span data-stu-id="47441-153">Create a scoring group, and enter a name for it.</span></span>
2. <span data-ttu-id="47441-154">Punktigrupi täiendavaks kirjeldamiseks sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="47441-154">Enter a description to further describe the scoring group.</span></span>
3. <span data-ttu-id="47441-155">Valige grupi tüüp.</span><span class="sxs-lookup"><span data-stu-id="47441-155">Select a group type.</span></span> <span data-ttu-id="47441-156">On kaheksa eelmääratletud tüüpi.</span><span class="sxs-lookup"><span data-stu-id="47441-156">There are eight predefined types.</span></span> <span data-ttu-id="47441-157">Saate valida ka **Kasutaja määratletud**, et määratleda teie organisatsioonile paremini sobiv grupi tüüp.</span><span class="sxs-lookup"><span data-stu-id="47441-157">You can also select **User defined** to define a group type that's better suited to your organization.</span></span>
4. <span data-ttu-id="47441-158">Valige punktisumma tüüp, et määratleda, kuidas punktgrupp riskiskoori arvutab.</span><span class="sxs-lookup"><span data-stu-id="47441-158">Select a score type to define how the scoring group calculates the risk score.</span></span> <span data-ttu-id="47441-159">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="47441-159">The following options are available:</span></span>

    - <span data-ttu-id="47441-160">**Vahemik** – kasutage seda valikut punktisumma arvutamiseks kasutatava väärtuste vahemiku määramiseks.</span><span class="sxs-lookup"><span data-stu-id="47441-160">**Range** – Use this option to define a range of values that should be used to calculate a score.</span></span>
    - <span data-ttu-id="47441-161">**Kasutaja määratletud** – kasutage seda valikut punktisumma juures kasutatavate väärtuste loendi käsitsi määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="47441-161">**User defined** – Use this option to manually define a list of values that should be used for the score.</span></span>

5. <span data-ttu-id="47441-162">Kui valisite punktisumma tüübiks **Vahemiku**, lisage read väärtuste vahemiku ja vastavate punktisummade määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="47441-162">If you selected **Range** as the score type, add lines to define the range of values and the corresponding scores.</span></span>

    1. <span data-ttu-id="47441-163">Määrake väljal **Väärtusest** vahemiku madalaim väärtus.</span><span class="sxs-lookup"><span data-stu-id="47441-163">In the **From value** field, specify the lowest value in the range.</span></span>
    2. <span data-ttu-id="47441-164">Määrake väljal **Väärtuseni** vahemiku kõrgeim väärtus.</span><span class="sxs-lookup"><span data-stu-id="47441-164">In the **To value** field, specify the highest value in the range.</span></span>
    3. <span data-ttu-id="47441-165">Sisestage väljale **Punktisumma** see punktisumma, mis tuleks määrata siis, kui esitatud väärtus langeb "väärtusest"/"väärtuseni" vahemikku.</span><span class="sxs-lookup"><span data-stu-id="47441-165">In the **Score** field, enter the score that should be assigned when the value that is provided is in the "from"/"to" range.</span></span>

    <span data-ttu-id="47441-166">Kui valisite punktisumma tüübiks **Kasutaja määratletud**, lisage read kasutaja määratletud väärtuste ja vastavate punktisummade määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="47441-166">If you selected **User defined** as the score type, add lines to define the user-defined values and the corresponding scores.</span></span>

    1. <span data-ttu-id="47441-167">Sisestage väljale **Väärtus** kasutaja määratud väärtus, mis tuleks kliendi andmetest esitada.</span><span class="sxs-lookup"><span data-stu-id="47441-167">In the **Value** field, enter the user-defined value that should be provided from the customer information.</span></span>
    2. <span data-ttu-id="47441-168">Sisestage väljale **Punktisumma** see punktisumma, mis tuleks määrata siis, kui esitatud väärtus langeb "väärtusest"/"väärtuseni" vahemikku.</span><span class="sxs-lookup"><span data-stu-id="47441-168">In the **Score** field, enter the score that should be assigned when the value that is provided is in the "from"/"to" range.</span></span>

## <a name="risk-assessments"></a><span data-ttu-id="47441-169">Riskihindamine</span><span class="sxs-lookup"><span data-stu-id="47441-169">Risk assessments</span></span>

<span data-ttu-id="47441-170">Saate määratleda riskihindamised, mida saab klientidele nende riskiskoori põhjal määrata.</span><span class="sxs-lookup"><span data-stu-id="47441-170">You can define risk assessments that can be assigned to customers, based on their risk score.</span></span> <span data-ttu-id="47441-171">Riskiskoori arvutamiseks võrreldakse kliendi andmeid iga punktigrupiga.</span><span class="sxs-lookup"><span data-stu-id="47441-171">A risk score is calculated by comparing customer information to each scoring group.</span></span> <span data-ttu-id="47441-172">Punktiskummad liidetakse kokku ja lõppskoori võrreldakse riskigrupi seadistuse väärtustega, et tuvastada riskigrupp, kuhu klient kuulub.</span><span class="sxs-lookup"><span data-stu-id="47441-172">The scores are summed, and the total score is compared to the values in the risk group setup to identify the risk group that the customer belongs to.</span></span> <span data-ttu-id="47441-173">Seejärel kasutatakse riskigrupi punktisummat kliendile krediidihalduse blokeerimise ja välistamise reeglite määramiseks.</span><span class="sxs-lookup"><span data-stu-id="47441-173">The risk group score is then used to define credit management blocking and exclusion rules for the customer.</span></span>

<span data-ttu-id="47441-174">Riskigruppe saate seadistada lehel **Riskihindamine** (**Krediidihaldus \> Seadistus \> Riski seadistus \> Riskihindamine**).</span><span class="sxs-lookup"><span data-stu-id="47441-174">You can set up risk groups on the **Risk assessments** page (**Credit management \> Setup \> Risk setup \> Risk assessments**).</span></span>

1. <span data-ttu-id="47441-175">Sisestage riskigrupi ID.</span><span class="sxs-lookup"><span data-stu-id="47441-175">Enter a risk group ID.</span></span>
2. <span data-ttu-id="47441-176">Riskigrupi täiendavaks selgitamiseks sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="47441-176">Enter a description to further explain the risk group.</span></span>
3. <span data-ttu-id="47441-177">Sisestage see punktisummade vahemik, mida kasutatakse, et määrata, millised kliendid riskigruppi kuuluvad.</span><span class="sxs-lookup"><span data-stu-id="47441-177">Enter a range of scores that is used to determine which customers belong to the risk group.</span></span>
4. <span data-ttu-id="47441-178">Valige riskigrupi indikaator, et määratleda riskigruppi tähistav sümbol.</span><span class="sxs-lookup"><span data-stu-id="47441-178">Select a risk group indicator to specify the symbol that represents the risk group.</span></span>

## <a name="guaranteeinsurance-types"></a><span data-ttu-id="47441-179">Garantii/kindlustuse tüübid</span><span class="sxs-lookup"><span data-stu-id="47441-179">Guarantee/insurance types</span></span>

<span data-ttu-id="47441-180">Garantii/kindlustuse tüüpe saate seadistada lehel **Garantii/kindlustuse tüübid** (**Krediidihaldus \> Seadistus \> Garantii/kindlustuse seadistus \> Garantii/kindlustuse tüübid**).</span><span class="sxs-lookup"><span data-stu-id="47441-180">You can set up guarantee/insurance types on the **Guarantee/insurance types** page (**Credit management \> Setup \> Guarantee/insurance setup \> Guarantee/insurance types**).</span></span>

1. <span data-ttu-id="47441-181">Sisestage garantii või kindlustuse tüüp, mis määratleb käendaja või kindlustusmaakleri nime.</span><span class="sxs-lookup"><span data-stu-id="47441-181">Enter a guarantee or insurance type that identifies the name of the guarantor or insurance broker.</span></span>
2. <span data-ttu-id="47441-182">Sisestage kirjeldus käendaja/kindlustusmaakleri kirjeldamiseks.</span><span class="sxs-lookup"><span data-stu-id="47441-182">Enter a description to describe the guarantor/insurance broker.</span></span>

## <a name="coverage-types"></a><span data-ttu-id="47441-183">Laovarude tüübid</span><span class="sxs-lookup"><span data-stu-id="47441-183">Coverage types</span></span>

<span data-ttu-id="47441-184">Kindlustuskatte tüüpe saab kasutada kindlustuspoliiside täiendavaks liigitamiseks.</span><span class="sxs-lookup"><span data-stu-id="47441-184">Coverage types can be used to further classify insurance policies.</span></span> <span data-ttu-id="47441-185">Neid ei saa kasutada garantiidega.</span><span class="sxs-lookup"><span data-stu-id="47441-185">They can't be used with guarantees.</span></span>

<span data-ttu-id="47441-186">Kindlustuskatte tüüpe saate lisada lehel **Kindlustuskatte tüübid** (**Krediidihaldus \> Seadistus \> Garantii/kindlustuse seadistus \> Kindlustuskatte tüübid**).</span><span class="sxs-lookup"><span data-stu-id="47441-186">You can add coverage types on the **Coverage types** page (**Credit management \> Setup \> Guarantee/insurance setup \> Coverage types**).</span></span>

1. <span data-ttu-id="47441-187">Sisestage kindlustuskatte tüüp, et määratleda kindlustuskatte tüüp, mis tuleks lisada kindlustuse või garantiina.</span><span class="sxs-lookup"><span data-stu-id="47441-187">Enter a coverage type to identify the type of coverage that should be added as insurance or a guarantee.</span></span>
2. <span data-ttu-id="47441-188">Sisestage kirjeldus kindlustuskatte tüübi kirjeldamiseks.</span><span class="sxs-lookup"><span data-stu-id="47441-188">Enter a description to describe of the coverage type.</span></span>

## <a name="automatic-credit-limits"></a><span data-ttu-id="47441-189">Automaatselt määratud krediidilimiidid</span><span class="sxs-lookup"><span data-stu-id="47441-189">Automatic credit limits</span></span>

<span data-ttu-id="47441-190">Automaatsetele krediidilimiitidele saate luua kriteeriumid lehel **Automaatsed krediidilimiidid** (**Krediidihaldus \> Seadistus \> Riski seadistus \> Automaatsed krediidilimiidid**).</span><span class="sxs-lookup"><span data-stu-id="47441-190">You can create criteria for automatic credit limits on the **Automatic credit limits** page (**Credit management \> Setup \> Risk setup \> Automatic credit limits**).</span></span>

1. <span data-ttu-id="47441-191">Valige riskigrupp, millele automaatne krediidilimiit tuleb määrata.</span><span class="sxs-lookup"><span data-stu-id="47441-191">Select a risk group that the automatic credit limit should be assigned to.</span></span>
2. <span data-ttu-id="47441-192">Valige automaatse krediidilimiidi valuuta.</span><span class="sxs-lookup"><span data-stu-id="47441-192">Select the currency for the automatic credit limit.</span></span> <span data-ttu-id="47441-193">Saate samale riskigrupile luua mitu automaatset krediidilimiiti erinevates valuutades.</span><span class="sxs-lookup"><span data-stu-id="47441-193">You can create multiple automatic credit limits in different currencies for the same risk group.</span></span>
3. <span data-ttu-id="47441-194">Sisestage tulu summa, mis tähistab maksimaalset ettevõtte tulu, mida saab selle automaatse krediidilimiidi puhul kasutada.</span><span class="sxs-lookup"><span data-stu-id="47441-194">Enter the revenue amount that represents the maximum company revenue that can be used for this automatic credit limit.</span></span> <span data-ttu-id="47441-195">Kui krediidilimiidid on loodud, võrreldakse tulu summat selle tulu väärtusega, mis asub lehel **Finantsid** (**Müügireskontro \> Kõik kliendid \> Kliendi valimine \> Üldine \> Statistika \> Finants**).</span><span class="sxs-lookup"><span data-stu-id="47441-195">When credit limits are created, the revenue amount is compared to a revenue value that is found on the **Financials** page (**Accounts receivable \> All customers \> Select a customer \> General \> Statistics \> Financial**).</span></span> <span data-ttu-id="47441-196">Süsteem kasutab jaotises **Ülevaade** uusimat väärtust.</span><span class="sxs-lookup"><span data-stu-id="47441-196">The system uses the latest value in the **Overview** section.</span></span>

<span data-ttu-id="47441-197">Järgige neid samme, et lisada ridu, mis esindavad krediidilimiiti, mis valitud kriteeriumide põhjal luuakse.</span><span class="sxs-lookup"><span data-stu-id="47441-197">Follow these steps to add lines that represent the credit limit that will be generated based on the selected criteria.</span></span>

1. <span data-ttu-id="47441-198">Valige punktigrupp, mis määratleb kliendi teabe, mida tuleks krediidilimiidi arvutamiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="47441-198">Select the scoring group that defines the customer information that should be used to calculate the credit limit.</span></span>
2. <span data-ttu-id="47441-199">Valige võrdlemise tehtemärk, mis määratleb, kuidas punktigrupi andmeid tuleks hinnata.</span><span class="sxs-lookup"><span data-stu-id="47441-199">Select the comparison operator that defines how the scoring group information should be evaluated.</span></span>
3. <span data-ttu-id="47441-200">Sisestage väärtus, mida tuleks võrrelda punktigrupile määratletud väärtusega.</span><span class="sxs-lookup"><span data-stu-id="47441-200">Enter the value that should be compared to the value that is specified for the scoring group.</span></span>
4. <span data-ttu-id="47441-201">Sisestage krediidilimiit, mis tuleb määrata, kui kliendi andmed vastavad punktigrupile määratletud väärtusele.</span><span class="sxs-lookup"><span data-stu-id="47441-201">Enter the credit limit that should be assigned if the customer information matches the value that is specified for the scoring group.</span></span> <span data-ttu-id="47441-202">Näiteks loote automaatse krediidilimiidi punktigrupile **Madal**.</span><span class="sxs-lookup"><span data-stu-id="47441-202">For example, you create an automatic credit limit for the **Low** scoring group.</span></span> <span data-ttu-id="47441-203">Kui ettevõtluses tegutsemise aastad on üks punktigruppidest, saate määratleda rea, mis määrab krediidilimiidi 100 000, kui klient on tegutsenud viis aastat ja teise rea, mis määrab krediidilimiidi 200 000, kui klient on tegutsenud 10 aastat.</span><span class="sxs-lookup"><span data-stu-id="47441-203">If the years in business is one of the scoring groups, you can define one line that assigns a 100,000 credit limit if the customer has been in business five years and another line that assigns a 200,000 credit limit if the customer has been in business for 10 years.</span></span>
