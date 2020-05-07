---
title: Kanali tagastuste ja tagasimaksete poliitika loomine ja värskendamine
description: See teema selgitab, kuidas seadistada kanali tagastuste ja tagasimaksete poliitikat.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: c2a9325f09ffe43c3436b7e0ca2ab511e1f57f83
ms.sourcegitcommit: 02640a0f63daa9e509146641824ed623c4d69c7f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/16/2020
ms.locfileid: "3265574"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="31c86-103">Kanali tagastuste ja tagasimaksete poliitika loomine ja värskendamine</span><span class="sxs-lookup"><span data-stu-id="31c86-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="31c86-104">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="31c86-104">Overview</span></span>

<span data-ttu-id="31c86-105">Kanali tagastuspoliitika rakenduses Dynamics 365 Commerce võimaldab jaemüüjatel määrata rakendamisi, mille alusel saab lubada maksevahendeid kassaseadmes tagastuse töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="31c86-105">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="31c86-106">See teema kirjeldab etappe, kuidas seadistada kanali tagastuste ja tagasimaksete poliitikat.</span><span class="sxs-lookup"><span data-stu-id="31c86-106">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="31c86-107">Poliitika ulatus piirdub hetkel maksevahendi määramisega, mida saab kanali jaoks lubada.</span><span class="sxs-lookup"><span data-stu-id="31c86-107">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="31c86-108">Lubatute loend põhineb ostu sooritamiseks kasutatavatel makseviisidel.</span><span class="sxs-lookup"><span data-stu-id="31c86-108">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="31c86-109">Näide:</span><span class="sxs-lookup"><span data-stu-id="31c86-109">For example:</span></span>

- <span data-ttu-id="31c86-110">Kui ost tehti kinkekaardi abil, on kaupluse poliitika töödelda tagasimakseid ainult uuele kinkekaardile või anda kaupluse krediiti.</span><span class="sxs-lookup"><span data-stu-id="31c86-110">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="31c86-111">Kui tehing on tehtud sularaha kasutades, on tagasimakse lubatud valikud sularaha, kinkekaart ja kliendikonto, kuid mitte krediitkaart.</span><span class="sxs-lookup"><span data-stu-id="31c86-111">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="31c86-112">Tagastuspoliitika lubamine</span><span class="sxs-lookup"><span data-stu-id="31c86-112">Enable return policy</span></span>

<span data-ttu-id="31c86-113">Kanali tagastuspoliitika funktsiooni lubamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="31c86-113">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="31c86-114">Avage tööruum **Funktsioonihaldus** rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="31c86-114">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="31c86-115">Otsige funktsiooni nimede loendist funktsiooni **Luba kanali tagastuspoliitikad**.</span><span class="sxs-lookup"><span data-stu-id="31c86-115">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="31c86-116">Valige **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="31c86-116">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="31c86-117">Tagastuspoliitika konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="31c86-117">Configure return policy</span></span>

<span data-ttu-id="31c86-118">Jaekaupluse või jaemüügi võrgukanali tagastuspoliitika konfigureerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="31c86-118">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="31c86-119">Avage **Jaemüük ja kaubandus** \> **Kanali seadistus** \> **Tagastused** \> **Kanali tagastuspoliitika**.</span><span class="sxs-lookup"><span data-stu-id="31c86-119">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="31c86-120">Valige **Uus**, et luua uus tagastuspoliitika mall.</span><span class="sxs-lookup"><span data-stu-id="31c86-120">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="31c86-121">Olemasoleva malli kasutamiseks valige vasakul paneelil mall.</span><span class="sxs-lookup"><span data-stu-id="31c86-121">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="31c86-122">Uute mallide jaoks lisage nimi ja kirjeldus, mis aitab teil tuvastada poliitika, kui seda kanalile rakendatakse.</span><span class="sxs-lookup"><span data-stu-id="31c86-122">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="31c86-123">![Uue tagastuspoliitika lisamine](media/Return-policy-page1.png "Uue tagastuspoliitika lisamine")</span><span class="sxs-lookup"><span data-stu-id="31c86-123">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="31c86-124">Jaotises **Lubatud tagasimakse viisid** määratlege **lubatud** tagastamise maksevahendid, mis on igale makseviisile omased.</span><span class="sxs-lookup"><span data-stu-id="31c86-124">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="31c86-125">![Makseviiside lisamine](media/Return-policy-page2.PNG "Lubatud makseviiside määramine makse tüübi kohta")</span><span class="sxs-lookup"><span data-stu-id="31c86-125">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="31c86-126">Makseviisid tuletatakse organisatsiooni jaoks määratud makseviisidest.</span><span class="sxs-lookup"><span data-stu-id="31c86-126">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="31c86-127">Iga loetletud makseviisi jaoks lubatud tagastuse maksevahendi tüübi lisamine tagab, et tagastuse saab teha lubatud tagastuse maksevahendi tüübile.</span><span class="sxs-lookup"><span data-stu-id="31c86-127">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="31c86-128">Seostage tagastuspoliitika mall kauplustega, kus seda kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="31c86-128">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="31c86-129">Valige suvand **Lisa** vahekaardil **Jaemüügikanalid** ja seostage saadaolevad kanalid.</span><span class="sxs-lookup"><span data-stu-id="31c86-129">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="31c86-130">Valige dialoogikastis **Vali organisatsiooni sõlmed** kauplused, regioonid ja organisatsioonid, millega mall peaks seotud olema.</span><span class="sxs-lookup"><span data-stu-id="31c86-130">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="31c86-131">Iga kauplusega saab seostada ainult ühe tagastuspoliitika malli.</span><span class="sxs-lookup"><span data-stu-id="31c86-131">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="31c86-132">Kasutage noolenuppe, et valida kauplusi, regioone või organisatsioone.</span><span class="sxs-lookup"><span data-stu-id="31c86-132">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="31c86-133">Poliitika jõustumiskuupäev on kuupäev, mil poliitikad rakendatakse kanalitele ja kanali töid käitatakse.</span><span class="sxs-lookup"><span data-stu-id="31c86-133">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="31c86-134">![Organisatsioonisõlmede dialoogiakna valimine](media/Return-policy-page3.PNG "Organisatsioonisõlmede dialoogiakna valimine")</span><span class="sxs-lookup"><span data-stu-id="31c86-134">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="31c86-135">Lehel **Jaotusgraafik** käitage tööd **1070**, et muuta kanali tagastuspoliitika kassa jaoks kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="31c86-135">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="31c86-136">Kanali tagastuspoliitika eelvaate vaatamine kassas</span><span class="sxs-lookup"><span data-stu-id="31c86-136">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="31c86-137">Järgige etappe ühes järgmistest näidetest, et vaadata kassas lubatud tagastuse maksevahendi tüüpe.</span><span class="sxs-lookup"><span data-stu-id="31c86-137">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="31c86-138">Logige kassasse kassapidaja või juhina sisse.</span><span class="sxs-lookup"><span data-stu-id="31c86-138">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="31c86-139">Jaotises **Vahetus ja sahtel** valige käsk **Näita töölehte**.</span><span class="sxs-lookup"><span data-stu-id="31c86-139">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="31c86-140">Valige tagastuse osaks olev kanne.</span><span class="sxs-lookup"><span data-stu-id="31c86-140">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="31c86-141">Valige tagastuseks kaubad ja valige makseviis.</span><span class="sxs-lookup"><span data-stu-id="31c86-141">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="31c86-142">Kui valitud maksevahendi tüüp on tagastuse maksevahendi tüüpide lubatud loendis, saab kassapidaja kande lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="31c86-142">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="31c86-143">Kui valitud maksevahend pole lubatud, kuvatakse veateade.</span><span class="sxs-lookup"><span data-stu-id="31c86-143">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="31c86-144">Valige suvand **Võlgnevus**, et kuvada kõikide lubatud tagastuse maksevahendi tüüpide loend.</span><span class="sxs-lookup"><span data-stu-id="31c86-144">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="31c86-145">- või -</span><span class="sxs-lookup"><span data-stu-id="31c86-145">-or-</span></span>

1. <span data-ttu-id="31c86-146">Logige kassasse kassapidaja või juhina sisse.</span><span class="sxs-lookup"><span data-stu-id="31c86-146">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="31c86-147">Valige **Tagastuskanne** ja sisestage kviitungi ID vöötkoodi skannimise või käsitsi sisestamisega.</span><span class="sxs-lookup"><span data-stu-id="31c86-147">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="31c86-148">Valige tagastuse osaks olev kanne.</span><span class="sxs-lookup"><span data-stu-id="31c86-148">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="31c86-149">Valige tagastuseks kaubad ja valige makseviis.</span><span class="sxs-lookup"><span data-stu-id="31c86-149">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="31c86-150">Kui valitud maksevahendi tüüp on tagastuse maksevahendi tüüpide lubatud loendis, saab kassapidaja kande lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="31c86-150">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="31c86-151">Kui valitud maksevahend pole lubatud, kuvatakse veateade.</span><span class="sxs-lookup"><span data-stu-id="31c86-151">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="31c86-152">Valige suvand **Võlgnevus**, et kuvada kõikide lubatud tagastuse maksevahendi tüüpide loend.</span><span class="sxs-lookup"><span data-stu-id="31c86-152">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="31c86-153">![Tagasimakse pole lubatud](media/Return-policy-page6.png "Tagasimakse tüüp ei ole lubatud")</span><span class="sxs-lookup"><span data-stu-id="31c86-153">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="31c86-154">![Makseviiside loend](media/Return-policy-page5.PNG "Tagasimakse tüübid on lubatud")</span><span class="sxs-lookup"><span data-stu-id="31c86-154">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>
