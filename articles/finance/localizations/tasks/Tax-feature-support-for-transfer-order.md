---
title: Maksufunktsiooni tugi üleviimistellimuste jaoks
description: See teema selgitab uut maksufunktsiooni tuge üleviimistellimustele, kasutades maksuarvutuse teenust.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3a5c2b6fb48d98ba045c77ed034d976f7d89af98
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021365"
---
# <a name="tax-feature-support-for-transfer-orders"></a><span data-ttu-id="0c956-103">Maksufunktsiooni tugi üleviimistellimuste jaoks</span><span class="sxs-lookup"><span data-stu-id="0c956-103">Tax feature support for transfer orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0c956-104">Selles teemas antakse teavet maksuarvutuse ja üleviimistellimuste sisestuse kohta.</span><span class="sxs-lookup"><span data-stu-id="0c956-104">This topic provides information about tax calculation and posting integration in transfer orders.</span></span> <span data-ttu-id="0c956-105">Selle funktsiooniga saate seadistada laoülekannete maksuarvestust ja üleviimistellimuste sisestamist.</span><span class="sxs-lookup"><span data-stu-id="0c956-105">This functionality lets you set up tax calculation and posting in transfer orders for stock transfers.</span></span> <span data-ttu-id="0c956-106">Euroopa Liidu (EL) käibemaksu määruste kohaselt peetakse laoülekandeid EL-i siseseks tarneks ja EL-siseseks soetamiseks.</span><span class="sxs-lookup"><span data-stu-id="0c956-106">Under European Union (EU) value-added tax (VAT) regulations, stock transfers are considered intra-community supply and intra-community acquisitions.</span></span>

<span data-ttu-id="0c956-107">Selle funktsiooni konfigureerimiseks ja kasutamiseks tuleb läbida kolm peamist sammu.</span><span class="sxs-lookup"><span data-stu-id="0c956-107">To configure and use this functionality, you must complete three main steps:</span></span>

1. <span data-ttu-id="0c956-108">**RCS-i seadistus:** seadistage regulatiivses konfiguratsiooniteenuses maksufunktsioon, maksukoodid ja maksukoodide kohaldatavus maksukoodi määramise jaoks üleviimistellimustes.</span><span class="sxs-lookup"><span data-stu-id="0c956-108">**RCS setup:** In Regulatory Configuration Service, set up the tax feature, tax codes, and tax codes applicability for tax code determination in transfer orders.</span></span>
2. <span data-ttu-id="0c956-109">**Finantside häälestamine:** lülitage rakenduses Microsoft Dynamics 365 Finance sisse **Üleviimistellimuse maksu** funktsioon, seadistage lao maksuteenuse parameetrid ja tuummaksu parameetrid.</span><span class="sxs-lookup"><span data-stu-id="0c956-109">**Finance setup:** In Microsoft Dynamics 365 Finance, turn on the **Tax in transfer order** feature, set up the tax service parameters for inventory, and set up core tax parameters.</span></span>
3. <span data-ttu-id="0c956-110">**Lao seadistus:** seadistage üleviimistellimuse kannete laokonfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="0c956-110">**Inventory setup:** Set up the inventory configuration for transfer order transactions.</span></span>

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a><span data-ttu-id="0c956-111">Maksu- ja üleviimistellimuse kannete RCS-i loomine</span><span class="sxs-lookup"><span data-stu-id="0c956-111">Set up RCS for tax and transfer order transactions</span></span>

<span data-ttu-id="0c956-112">Järgige neid samme üleviimistellimusse lisatava maksu seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="0c956-112">Follow these steps to set up the tax that is involved in a transfer order.</span></span> <span data-ttu-id="0c956-113">Siin kuvatud näites on üleviimistellimus Hollandist Belgiasse.</span><span class="sxs-lookup"><span data-stu-id="0c956-113">In the example that is shown here, the transfer order is from the Netherlands to Belgium.</span></span>

1. <span data-ttu-id="0c956-114">**Maksufunktsioonide** lehe vahekaardil **Versioonid** valige mustandi funktsiooni versioon ja seejärel valige käsk **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="0c956-114">On the **Tax features** page, on the **Versions** tab, select the draft feature version, and then select **Edit**.</span></span>

    ![Redigeerimise valimine](../media/tax-feature-support-01.png)

2. <span data-ttu-id="0c956-116">Uute maksukoodide loomiseks valige **Maksufunktsiooni seadistamise** lehel vahekaardil **Maksukoodid** suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="0c956-116">On the **Tax features setup** page, on the **Tax codes** tab, select **Add** to create new tax codes.</span></span> <span data-ttu-id="0c956-117">Selles näites luuakse kolm maksukoodi: **NL-maksuvaba**, **BE-RC-21** ja **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="0c956-117">For this example, three tax codes are created: **NL-Exempt**, **BE-RC-21**, and **BE-RC+21**.</span></span>

    - <span data-ttu-id="0c956-118">Kui üleviimistellimus lähetatakse Hollandi laost, rakendatakse Hollandi käibemaksuvabastuse maksukoodi (**NL-maksuvaba**).</span><span class="sxs-lookup"><span data-stu-id="0c956-118">When a transfer order is shipped from a warehouse in the Netherlands, the Netherlands VAT exempted tax code (**NL-Exempt**) is applied.</span></span>
      
        <span data-ttu-id="0c956-119">Looge maksukood **NL-maksuvabastus**.</span><span class="sxs-lookup"><span data-stu-id="0c956-119">Create the tax code **NL-Exempt**.</span></span>
        1. <span data-ttu-id="0c956-120">Valige suvand **Lisa**, sisestage **NL-maksuvabastus** väljale **Maksukood**.</span><span class="sxs-lookup"><span data-stu-id="0c956-120">Select **Add**, enter **NL-Exempt** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="0c956-121">Valige käsk **Netosumma järgi** väljal **Maksukomponent**.</span><span class="sxs-lookup"><span data-stu-id="0c956-121">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="0c956-122">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0c956-122">Select **Save**.</span></span>
        4. <span data-ttu-id="0c956-123">Valige tabelis **Määr** suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="0c956-123">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="0c956-124">Lülitage valikul **On maksuvabastus** sisse nupp **Jah** jaotises **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="0c956-124">Swtich **Is Exempt** to **Yes** in the **General** section.</span></span>

        ![NL-maksuvabastuse maksukood](../media/tax-feature-support-02.png)

    - <span data-ttu-id="0c956-126">Kui üleviimistellimus on vastu võetud Belgia lattu, rakendatakse pöördtasu mehhanism, kasutades maksukoode **BE-RC-21** ja **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="0c956-126">When a transfer order is received at a Belgium warehouse, the reverse charge mechanism is applied by using the **BE-RC-21** and **BE-RC+21** tax codes.</span></span>
        
        <span data-ttu-id="0c956-127">Looge maksukood **BE-RC-21**.</span><span class="sxs-lookup"><span data-stu-id="0c956-127">Create the tax code **BE-RC-21**.</span></span>      
        1. <span data-ttu-id="0c956-128">Valige suvand **Lisa**, sisestage **BE-RC-21** väljale **Maksukood**.</span><span class="sxs-lookup"><span data-stu-id="0c956-128">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="0c956-129">Valige käsk **Netosumma järgi** väljal **Maksukomponent**.</span><span class="sxs-lookup"><span data-stu-id="0c956-129">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="0c956-130">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0c956-130">Select **Save**.</span></span>
        4. <span data-ttu-id="0c956-131">Valige tabelis **Määr** suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="0c956-131">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="0c956-132">Sisestage väljale **Maksumäär** väärtus **–21**.</span><span class="sxs-lookup"><span data-stu-id="0c956-132">Enter **-21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="0c956-133">Lülitage valikul **On pöördmaks** sisse nupp **Jah** jaotises **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="0c956-133">Swtich **Is Reverse Charge** to **Yes** in the **General** section.</span></span>
        7. <span data-ttu-id="0c956-134">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0c956-134">Select **Save**.</span></span>

        ![BE-RC-21 maksukood pöördmaksude jaoks](../media/tax-feature-support-03.png)
        
        <span data-ttu-id="0c956-136">Looge maksukood **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="0c956-136">Create the tax code **BE-RC+21**.</span></span>
        1. <span data-ttu-id="0c956-137">Valige suvand **Lisa**, sisestage **BE-RC-21** väljale **Maksukood**.</span><span class="sxs-lookup"><span data-stu-id="0c956-137">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="0c956-138">Valige käsk **Netosumma järgi** väljal **Maksukomponent**.</span><span class="sxs-lookup"><span data-stu-id="0c956-138">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="0c956-139">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0c956-139">Select **Save**.</span></span>
        4. <span data-ttu-id="0c956-140">Valige tabelis **Määr** suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="0c956-140">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="0c956-141">Sisestage väljale **Maksumäär** väärtus **21**.</span><span class="sxs-lookup"><span data-stu-id="0c956-141">Enter **21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="0c956-142">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0c956-142">Select **Save**.</span></span>

        ![BE-RC+21 maksukood pöördmaksude jaoks](../media/tax-feature-support-04.png)

3. <span data-ttu-id="0c956-144">Määratlege maksukoodide kohaldatavus.</span><span class="sxs-lookup"><span data-stu-id="0c956-144">Define the applicability of the tax codes.</span></span>

    1. <span data-ttu-id="0c956-145">Valige suvand **Halda veerge** ja seejärel valige veerud, mida tuleks kasutada kohaldatavustabeli koostamiseks.</span><span class="sxs-lookup"><span data-stu-id="0c956-145">Select **Manage columns**, and then select columns that should be used to build the applicability table.</span></span>

        > [!NOTE]
        > <span data-ttu-id="0c956-146">Lisage kindlasti tabelisse **Äriprotsessi** ja **Maksusuundade** veerud.</span><span class="sxs-lookup"><span data-stu-id="0c956-146">Be sure to add the **Business process** and **Tax directions** columns to the table.</span></span> <span data-ttu-id="0c956-147">Mõlemad veerud on olulised üleviimistellimuste maksufunktsioonide jaoks.</span><span class="sxs-lookup"><span data-stu-id="0c956-147">Both columns are essential to the functionality for tax in transfer orders.</span></span>

    2. <span data-ttu-id="0c956-148">Rakendatavuse reeglite lisamine.</span><span class="sxs-lookup"><span data-stu-id="0c956-148">Add applicability rules.</span></span> <span data-ttu-id="0c956-149">Ärge jätke välju **Maksukoodid**, **Maksugrupp** ja **Kauba maksugrupp** tühjaks.</span><span class="sxs-lookup"><span data-stu-id="0c956-149">Don't leave the **Tax codes**, **Tax group**, and **Item tax group** fields blank.</span></span>
        
        <span data-ttu-id="0c956-150">Saate lisada üleviimistellimuse saadetisele uue reegli.</span><span class="sxs-lookup"><span data-stu-id="0c956-150">Add a new rule for transfer order shipment.</span></span>
        1. <span data-ttu-id="0c956-151">Valige tabelis **Rakendatavuse reeglid** suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="0c956-151">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="0c956-152">Väljal **Äriprotsess** valige **Ladu**, et muuta reegel üleviimistellimusel rakendatavaks.</span><span class="sxs-lookup"><span data-stu-id="0c956-152">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="0c956-153">Väljale **Riigist/regioonist lähetamine** sisestage **NLD**.</span><span class="sxs-lookup"><span data-stu-id="0c956-153">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="0c956-154">Väljale **Riiki/regiooni lähetamine** sisestage **BEL**.</span><span class="sxs-lookup"><span data-stu-id="0c956-154">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="0c956-155">Väljal **Maksusuund** valige **Väljastus**, et muuta reegel üleviimistellimuse saadetisele rakendatavaks.</span><span class="sxs-lookup"><span data-stu-id="0c956-155">In the **Tax direction** field, select **Output** to make the rule applicable to transfer order shipment.</span></span>
        6. <span data-ttu-id="0c956-156">Valige väljal **Maksukoodid** suvand **NL-maksuvabastus**.</span><span class="sxs-lookup"><span data-stu-id="0c956-156">In the **Tax codes** field, select **NL-Exempt**.</span></span>
        7. <span data-ttu-id="0c956-157">Sisestage väljadele **Maksugrupp** ja **Kauba maksugrupp** seotud käibemaksugrupp ja kauba käibemaksugrupp, mis on määratletud teie finantssüsteemis.</span><span class="sxs-lookup"><span data-stu-id="0c956-157">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>
        
        <span data-ttu-id="0c956-158">Saate lisada üleviimistellimuse sissetulekule muu reegli.</span><span class="sxs-lookup"><span data-stu-id="0c956-158">Add another rule for transfer order receipt.</span></span>
        1. <span data-ttu-id="0c956-159">Valige tabelis **Rakendatavuse reeglid** suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="0c956-159">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="0c956-160">Väljal **Äriprotsess** valige **Ladu**, et muuta reegel üleviimistellimusel rakendatavaks.</span><span class="sxs-lookup"><span data-stu-id="0c956-160">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="0c956-161">Väljale **Riigist/regioonist lähetamine** sisestage **NLD**.</span><span class="sxs-lookup"><span data-stu-id="0c956-161">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="0c956-162">Väljale **Riiki/regiooni lähetamine** sisestage **BEL**.</span><span class="sxs-lookup"><span data-stu-id="0c956-162">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="0c956-163">Väljal **Maksusuund** valige **Sisend**, et muuta reegel üleviimistellimuse sissetulekule rakendatavaks.</span><span class="sxs-lookup"><span data-stu-id="0c956-163">In the **Tax direction** field, select **Input** to make the rule applicable to transfer order receipt.</span></span>
        6. <span data-ttu-id="0c956-164">Valige väljal **Maksukoodid** suvandid **BE-RC+21** ja **BE-RC-21**.</span><span class="sxs-lookup"><span data-stu-id="0c956-164">In the **Tax codes** field, select **BE-RC+21** and **BE-RC-21**.</span></span>
        7. <span data-ttu-id="0c956-165">Sisestage väljadele **Maksugrupp** ja **Kauba maksugrupp** seotud käibemaksugrupp ja kauba käibemaksugrupp, mis on määratletud teie finantssüsteemis.</span><span class="sxs-lookup"><span data-stu-id="0c956-165">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>

        ![Kohaldatavusreeglid](../media/image5.png)

4. <span data-ttu-id="0c956-167">Viige uus maksufunktsiooni versioon lõpule ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="0c956-167">Complete and publish the new tax feature version.</span></span>

    <span data-ttu-id="0c956-168">[![Uue versiooni oleku muutmine](../media/image6.png)](../media/image6.png)</span><span class="sxs-lookup"><span data-stu-id="0c956-168">[![Changing the status of the new version](../media/image6.png)](../media/image6.png)</span></span>

## <a name="set-up-finance-for-transfer-order-transactions"></a><span data-ttu-id="0c956-169">Finantsülevaadete seadistamine kannete üleviimiseks</span><span class="sxs-lookup"><span data-stu-id="0c956-169">Set up Finance for transfer order transactions</span></span>

<span data-ttu-id="0c956-170">Üleviimistellimuste lubamiseks ja maksude seadistamiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="0c956-170">Follow these steps to enable and set up taxes for transfer orders.</span></span>

1. <span data-ttu-id="0c956-171">Jaotises Finantsid avage **Tööruumid** \> **Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="0c956-171">In Finance, go to **Workspaces** \> **Feature management**.</span></span>
2. <span data-ttu-id="0c956-172">Leidke ja valige loendist funktsioon **Üleviimistellimuse maks** ning seejärel valige **Luba kohe**, et see sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="0c956-172">In the list, find and select the **Tax in transfer order** feature, and then select **Enable now** to turn it on.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="0c956-173">Funktsioon **Üleviimistellimuse maks** sõltub täielikult maksuteenusest.</span><span class="sxs-lookup"><span data-stu-id="0c956-173">The **Tax in transfer order** feature is fully dependent on the tax service.</span></span> <span data-ttu-id="0c956-174">Seetõttu saab seda sisse lülitada alles pärast maksuteenuse installimist.</span><span class="sxs-lookup"><span data-stu-id="0c956-174">Therefore, it can be turned on only after you've installed the tax service.</span></span>

    ![Maks funktsioonis üleviimistellimus](../media/image7.png)

3. <span data-ttu-id="0c956-176">Lubage maksuteenus ja valige äriprotsess **Ladu**.</span><span class="sxs-lookup"><span data-stu-id="0c956-176">Enable the tax service, and select the **Inventory** business process.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="0c956-177">Peate selle etapi jaotises Finants lõpule viima iga juriidilise isiku puhul, kus soovite, et maksuteenus ja üleviimistellimuste maksufunktsioonid oleks saadaval.</span><span class="sxs-lookup"><span data-stu-id="0c956-177">You must complete this step for each legal entity in Finance where you want the tax service and the functionality for tax in transfer orders to be available.</span></span>

    1. <span data-ttu-id="0c956-178">Avage menüü **Maks** \> **Seadistamine** \> **Maksu konfiguratsioon** \> **Maksuteenuse häälestus**.</span><span class="sxs-lookup"><span data-stu-id="0c956-178">Go to **Tax** \> **Setup** \> **Tax configuration** \> **Tax service setup**.</span></span>
    2. <span data-ttu-id="0c956-179">Väljal **Äriprotsess** valige **Ladu**.</span><span class="sxs-lookup"><span data-stu-id="0c956-179">In the **Business process** field, select **Inventory**.</span></span>

    ![Äriprotsessi välja seadistamine](../media/image8.png)

4. <span data-ttu-id="0c956-181">Kontrollige, kas pöördmaksu mehhanism on seadistatud.</span><span class="sxs-lookup"><span data-stu-id="0c956-181">Verify that the reverse charge mechanism is set up.</span></span> <span data-ttu-id="0c956-182">Avage menüü **Pearaamat** \> **Seadistus** \> **Parameetrid** ja seejärel veenduge, et vahekaardil **Pöördmaks** on valik **Luba pöördmaks** seatud väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="0c956-182">Go to **General ledger** \> **Setup** \> **Parameters**, and then, on the **Reverse charge** tab, verify that the **Enable reverse charge** option is set to **Yes**.</span></span>

    ![Pöördmaksu valiku lubamine](../media/image9.png)

5. <span data-ttu-id="0c956-184">Kontrollige, et seotud maksukoodid, maksugrupid, kauba maksugrupid ja KM-i registreerimisnumbrid on jaotises Finants seadistatud vastavalt maksuteenuste juhistele.</span><span class="sxs-lookup"><span data-stu-id="0c956-184">Verify that the related tax codes, tax groups, item tax groups, and VAT registration numbers have been set up in Finance according to the tax service guidance.</span></span>
6. <span data-ttu-id="0c956-185">Seadistage vahetransiidi konto.</span><span class="sxs-lookup"><span data-stu-id="0c956-185">Set up an interim transit account.</span></span> <span data-ttu-id="0c956-186">See samm on nõutav ainult juhul, kui üleviimistellimusele rakendatav maks ei ole rakendatav maksuvabastuse või pöördmaksumehhanismi puhul.</span><span class="sxs-lookup"><span data-stu-id="0c956-186">This step is required only when the tax that is applied to a transfer order isn't applicable to a tax exempted or reverse charge mechanism.</span></span>

    1. <span data-ttu-id="0c956-187">Avage **Maks** \> **Seadistus** \> **Käibemaks** \> **Pearaamatu sisestusgrupid**.</span><span class="sxs-lookup"><span data-stu-id="0c956-187">Go to **Tax** \> **Setup** \> **Sales tax** \> **Ledger posting groups**.</span></span>
    2. <span data-ttu-id="0c956-188">Valige väljal **Vahetransiidid** pearaamatu konto.</span><span class="sxs-lookup"><span data-stu-id="0c956-188">In the **Interim transit** field, select a ledger account.</span></span>

    ![Vahetransiidi konto valimine](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a><span data-ttu-id="0c956-190">Peamiste varude seadistamine kannete üleviimiseks</span><span class="sxs-lookup"><span data-stu-id="0c956-190">Set up basic inventory for transfer order transactions</span></span>

<span data-ttu-id="0c956-191">Järgige neid samme, et seadistada peamised varud, et lubada üleviimistellimuse kanded.</span><span class="sxs-lookup"><span data-stu-id="0c956-191">Follow these steps to set up basic inventory to enable transfer order transactions.</span></span>

1. <span data-ttu-id="0c956-192">Looge erinevates riikides või regioonides oma ladude jaoks saatmis- ja lähetuskohad ning lisage iga asukoha esmane aadress.</span><span class="sxs-lookup"><span data-stu-id="0c956-192">Create ship-from and ship-to sites for your warehouses in different countries or regions, and add the primary address for each site.</span></span>

    1. <span data-ttu-id="0c956-193">Avage jaotis **Laohaldus** \> **Seadistus** \> **Ladu** \> **Asukohad**.</span><span class="sxs-lookup"><span data-stu-id="0c956-193">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Sites**.</span></span>
    2. <span data-ttu-id="0c956-194">Valige suvand **Uus** asukoha loomiseks, mille hiljem määrate laole.</span><span class="sxs-lookup"><span data-stu-id="0c956-194">Select **New** to create the site that you will assign to a warehouse later.</span></span>
    3. <span data-ttu-id="0c956-195">Korrake 2. sammu kõigi teiste asukohta puhul, mille peate looma.</span><span class="sxs-lookup"><span data-stu-id="0c956-195">Repeat step 2 for all the other sites that you must create.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0c956-196">Ühe teie valitud asukoha nimi peab olema **Transiit**.</span><span class="sxs-lookup"><span data-stu-id="0c956-196">One of the sites that you create should be named **Transit**.</span></span> <span data-ttu-id="0c956-197">Selle protseduuri hilisemates sammudes määrate selle asukoha transiitlaole, nii et maksudega seotud laokandeid saab sisestada üleviimistellimuste "läheta" ja "vastuvõtu" kannetesse.</span><span class="sxs-lookup"><span data-stu-id="0c956-197">In later steps of this procedure, you will assign this site to the transit warehouse, so that tax-related inventory vouchers can be posted in "ship" and "receive" transactions for transfer orders.</span></span> <span data-ttu-id="0c956-198">Transiidikoha aadress pole maksuarvestuses oluline.</span><span class="sxs-lookup"><span data-stu-id="0c956-198">The address of the transit site is irrelevant to tax calculation.</span></span> <span data-ttu-id="0c956-199">Seetõttu saate selle tühjaks jätta.</span><span class="sxs-lookup"><span data-stu-id="0c956-199">Therefore, you can leave it blank.</span></span>

    ![Asukohtade seadistamine](../media/image11.png)

2. <span data-ttu-id="0c956-201">Looge lähetamis-, transiit- ja sihtlaod.</span><span class="sxs-lookup"><span data-stu-id="0c956-201">Create ship-from, transit, and ship-to warehouses.</span></span> <span data-ttu-id="0c956-202">Kogu laos säilitatav aadressiteave alistab maksuarvestuse ajal asukoha aadressi.</span><span class="sxs-lookup"><span data-stu-id="0c956-202">Any address information that is maintained in a warehouse will override the site address during tax calculation.</span></span>

    1. <span data-ttu-id="0c956-203">Avage **Laohaldus** \> **Seadistus** \> **Ladu** \> **Laod**.</span><span class="sxs-lookup"><span data-stu-id="0c956-203">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Warehouses**.</span></span>
    2. <span data-ttu-id="0c956-204">Valige suvand **Uus** lao loomiseks ja määrake see vastavale asukohale.</span><span class="sxs-lookup"><span data-stu-id="0c956-204">Select **New** to create a warehouse, and assign it to the corresponding site.</span></span>
    3. <span data-ttu-id="0c956-205">Korrake 2. sammu, et luua ladu igale asukohale vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="0c956-205">Repeat step 2 to create a warehouse for each site as required.</span></span>

    ![Ladude seadistamine](../media/image12.png)

    > [!NOTE]
    > <span data-ttu-id="0c956-207">Lähetamislaost üleviimistellimuse kannete jaoks peab transiitladu olema väljal **Transiitladu** valitud.</span><span class="sxs-lookup"><span data-stu-id="0c956-207">For a ship-from warehouse, a transit warehouse must be selected in the **Transit warehouse** field for transfer order transactions.</span></span>
    >
    > ![Transiitlao valimine](../media/image13.png)

3. <span data-ttu-id="0c956-209">Veenduge, et üleviimistellimuste kannete varude sisestuste konfiguratsioon on seadistatud.</span><span class="sxs-lookup"><span data-stu-id="0c956-209">Verify that the inventory posting configuration is set up for transfer order transactions.</span></span>

    1. <span data-ttu-id="0c956-210">Avage **Varude haldus** \> **Seadistus** \> **Sisestus** \> **Sisestus**.</span><span class="sxs-lookup"><span data-stu-id="0c956-210">Go to **Inventory management** \> **Setup** \> **Posting** \> **Posting**.</span></span>
    2. <span data-ttu-id="0c956-211">Kontrollige vahekaardil **Varud**, et pearaamatukontol on seadistatud nii **Lao väljamineku** kui ka **Lao sissetuleku** sisestamine.</span><span class="sxs-lookup"><span data-stu-id="0c956-211">On the **Inventory** tab, verify that a ledger account is set up for both **Inventory issue** and **Inventory receipt** posting.</span></span>

        ![Lao väljamineku ja lao sissetuleku sisestamise seadistamine](../media/image14.png)

    3. <span data-ttu-id="0c956-213">Kontrollige, kas pearaamatukonto on seadistatud **Üksusesiseseks ostureskonto** sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="0c956-213">Verify that a ledger account is set up for **Inter-unit payable** posting.</span></span>

        ![Üksusesisese ostureskonto sisestuse seadistamine](../media/image15.png)

    4. <span data-ttu-id="0c956-215">Kontrollige, kas pearaamatukonto on seadistatud **Üksusesiseseks müügireskonto** sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="0c956-215">Verify that a ledger account is set up for **Inter-unit receivable** posting.</span></span>

        ![Üksusesisese müügireskonto sisestuse seadistamine](../media/image16.png)
