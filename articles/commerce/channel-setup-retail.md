---
title: Jaemüügikanali seadistamine
description: Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus jaemüügikanal.
author: samjarawan
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3f1f5dc2c8402d9b6b68a049f804932812eb74c0
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937530"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="5815e-103">Jaemüügikanali häälestus</span><span class="sxs-lookup"><span data-stu-id="5815e-103">Set up a retail channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5815e-104">Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus jaemüügikanal.</span><span class="sxs-lookup"><span data-stu-id="5815e-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5815e-105">Dynamics 365 Commerce toetab mitut jaemüügikanalit.</span><span class="sxs-lookup"><span data-stu-id="5815e-105">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="5815e-106">Jaemüügikanalid hõlmavad võrgupoode, kõnekeskusi ja jaekauplusi (neid nimetatakse ka füüsilisteks kauplusteks).</span><span class="sxs-lookup"><span data-stu-id="5815e-106">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="5815e-107">Igal kaupluse kanalil võivad olla oma makseviisid, hinnagrupid, kassaregistrid, tulu- ja kulukontod ning personal.</span><span class="sxs-lookup"><span data-stu-id="5815e-107">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="5815e-108">Enne jaekaupluse kanali loomist tuleb seadistada kõik need elemendid.</span><span class="sxs-lookup"><span data-stu-id="5815e-108">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="5815e-109">Enne jaemüügikanali loomist veenduge, et järgite [kanali eeltingimusi](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="5815e-109">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="5815e-110">Uue jaemüügikanali loomine ja konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="5815e-110">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="5815e-111">Avage navigatsioonipaneelil **Moodulid \> Kanalid \> Kauplused \> Kõik kauplused**.</span><span class="sxs-lookup"><span data-stu-id="5815e-111">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="5815e-112">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="5815e-112">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5815e-113">Sisestage väljale **Nimi** uue kanali nimi.</span><span class="sxs-lookup"><span data-stu-id="5815e-113">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="5815e-114">Sisestage väljale **Kaupluse number** kordumatu kaupluse number.</span><span class="sxs-lookup"><span data-stu-id="5815e-114">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="5815e-115">See number võib olla tähtnumbriline ja kuni 10 tähemärgi pikkune.</span><span class="sxs-lookup"><span data-stu-id="5815e-115">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="5815e-116">Sisestage ripploendisse **Juriidiline isik** sobiv juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="5815e-116">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="5815e-117">Sisestage ripploendisse **Ladu** sobiv ladu.</span><span class="sxs-lookup"><span data-stu-id="5815e-117">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="5815e-118">Valige sobiv ajavöönd väljal **Kaupluse ajavöönd**.</span><span class="sxs-lookup"><span data-stu-id="5815e-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="5815e-119">Valige ripploendist **Käibemaksugrupp** kauplusele sobiv käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="5815e-119">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="5815e-120">Valige väljal **Valuuta** sobiv valuuta.</span><span class="sxs-lookup"><span data-stu-id="5815e-120">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="5815e-121">Sisestage väljale **Kliendi aadressiraamat** kehtiv aadressiraamat.</span><span class="sxs-lookup"><span data-stu-id="5815e-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="5815e-122">Sisestage väljale **Vaikeklient** kehtiv vaikeklient.</span><span class="sxs-lookup"><span data-stu-id="5815e-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="5815e-123">Valige väljal **Funktsiooniprofiil** funktsiooniprofiil, kui see on kohaldatav.</span><span class="sxs-lookup"><span data-stu-id="5815e-123">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="5815e-124">Sisestage väljale **Meiliteavituse profiil** kehtiv meiliteavituse profiil.</span><span class="sxs-lookup"><span data-stu-id="5815e-124">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="5815e-125">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5815e-125">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="5815e-126">Järgmine pilt näitab uue jaemüügikanali loomist.</span><span class="sxs-lookup"><span data-stu-id="5815e-126">The following image shows the creation of a new retail channel.</span></span>

![Uus jaemüügikanal](media/channel-setup-retail-1.png)

<span data-ttu-id="5815e-128">Järgmine pilt näitab jaemüügikanali näidet.</span><span class="sxs-lookup"><span data-stu-id="5815e-128">The following image shows an example retail channel.</span></span>

![Jaemüügikanali näide](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="5815e-130">Muud sätted</span><span class="sxs-lookup"><span data-stu-id="5815e-130">Other settings</span></span>

<span data-ttu-id="5815e-131">On mitmeid muid valikulisi sätteid, mida saab jaotistes **Väljavõte/sulgemine** ja **Mitmesugust** vastavalt jaemüügikaupluse vajadustele seadistada.</span><span class="sxs-lookup"><span data-stu-id="5815e-131">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="5815e-132">Lisaks vt jaotist [Kassa ekraanipaigutused](pos-screen-layouts.md), et saada lisainfot vaikimisi ekraanipaigutuse seadistamise kohta jaotises **Ekraani paigutus** ja jaotist [Jaemüügi riistvarajaama konfigureerimine ja installimine](retail-hardware-station-configuration-installation.md), et saada seadistamise infot **Riistvarajaamade** jaotise kohta.</span><span class="sxs-lookup"><span data-stu-id="5815e-132">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="5815e-133">Järgmine pilt näitab jaemüügikanali seadistuse konfiguratsiooni näidet.</span><span class="sxs-lookup"><span data-stu-id="5815e-133">The following image shows an example retail channel setup configuration.</span></span>

![Jaemüügikanali konfiguratsiooni näide](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="5815e-135">Täiendava kanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="5815e-135">Additional channel set up</span></span>

<span data-ttu-id="5815e-136">Et kanalit saaks leida Tegevuspaanil jaotise **Seadistus** alt, tuleb seadistada täiendavad elemendid.</span><span class="sxs-lookup"><span data-stu-id="5815e-136">There are additional items that need to be set up for a channel that can be found on the Action Pane under the **Set up** section.</span></span>

<span data-ttu-id="5815e-137">Veebikanali häälestamiseks nõutavad täiendavad toimingud hõlmavad makseviiside, sularaha deklaratsiooni, tarneviiside, tulu/kulu konto, jaotiste, täitmisgrupi määramise ja seifide seadistamist.</span><span class="sxs-lookup"><span data-stu-id="5815e-137">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="5815e-138">Järgmine pilt näitab erinevaid täiendavaid jaemüügikanali seadistamise suvandeid vahekaardil **Seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="5815e-138">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Kanali seadistamine](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="5815e-140">Seadistada maksemeetodid</span><span class="sxs-lookup"><span data-stu-id="5815e-140">Set up payment methods</span></span>

<span data-ttu-id="5815e-141">Kõigi selles kanalis toetatud maksetüübi makseviiside seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="5815e-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="5815e-142">Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Makseviisid**.</span><span class="sxs-lookup"><span data-stu-id="5815e-142">On the Action Pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="5815e-143">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="5815e-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5815e-144">Valige navigeerimispaanil soovitud makseviis.</span><span class="sxs-lookup"><span data-stu-id="5815e-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="5815e-145">Sisestage jaotises **Üldine** **Toimingu nimi** ja konfigureerige muud soovitud sätted.</span><span class="sxs-lookup"><span data-stu-id="5815e-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="5815e-146">Konfigureerige kõik maksetüübi jaoks vajalikud lisasätted.</span><span class="sxs-lookup"><span data-stu-id="5815e-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="5815e-147">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5815e-147">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="5815e-148">Järgmine pilt näitab sularaha makseviisi näidet.</span><span class="sxs-lookup"><span data-stu-id="5815e-148">The following image shows an example of a cash payment method.</span></span>

![Makseviiside näited](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="5815e-150">Sularaha deklaratsiooni seadistamine</span><span class="sxs-lookup"><span data-stu-id="5815e-150">Set up cash declaration</span></span>

1. <span data-ttu-id="5815e-151">Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Sularaha deklaratsioon**.</span><span class="sxs-lookup"><span data-stu-id="5815e-151">On the Action Pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="5815e-152">Valige tegevuspaanil **Uus** ja seejärel looge kõik kohaldatavad **Mündi** ja **Paberraha** nominaalväärtused.</span><span class="sxs-lookup"><span data-stu-id="5815e-152">On the Action Pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="5815e-153">Järgmine pilt näitab sularaha deklaratsiooni näidet.</span><span class="sxs-lookup"><span data-stu-id="5815e-153">The following image shows an example of a cash declaration.</span></span>

![Sularaha deklaratsioonide seadistamine](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="5815e-155">Tarneviiside häälestamine</span><span class="sxs-lookup"><span data-stu-id="5815e-155">Set up modes of delivery</span></span>

<span data-ttu-id="5815e-156">Konfigureeritud tarneviise saate näha, valides **Tarneviisid** vahekaardilt **Seadistus** tegevuspaani alt.</span><span class="sxs-lookup"><span data-stu-id="5815e-156">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the Action Pane.</span></span>  

<span data-ttu-id="5815e-157">Tarneviisi muutmiseks või lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="5815e-157">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="5815e-158">Avage navigeerimispaanil **Moodulid \> Varude haldus \> Tarneviisid**.</span><span class="sxs-lookup"><span data-stu-id="5815e-158">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="5815e-159">Valige tegevuspaanilt suvand **Uus**, et luua uus tarneviis, või valige olemasolev režiim.</span><span class="sxs-lookup"><span data-stu-id="5815e-159">On the Action Pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="5815e-160">Kanali lisamiseks valige jaotisest **Jaemüügikanalid** käsk **Lisa rida**.</span><span class="sxs-lookup"><span data-stu-id="5815e-160">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="5815e-161">Kanalite lisamine kasutades organisatsiooni sõlmpunkte, mitte iga kanalit ükshaaval lisades, täiustab kanalite lisamist veelgi.</span><span class="sxs-lookup"><span data-stu-id="5815e-161">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="5815e-162">Järgmine pilt näitab tarneviisi näidet.</span><span class="sxs-lookup"><span data-stu-id="5815e-162">The following image shows an example of a mode of delivery.</span></span>

![Tarneviiside häälestamine](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="5815e-164">Tulu/kulu konto seadistamine</span><span class="sxs-lookup"><span data-stu-id="5815e-164">Set up income/expense account</span></span>

<span data-ttu-id="5815e-165">Tulu/kulu konto seadistamiseks läbige need etapid.</span><span class="sxs-lookup"><span data-stu-id="5815e-165">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="5815e-166">Valige tegevuspaanil vahekaart **Seadista** ja seejärel suvand **Tulu/kulu konto**.</span><span class="sxs-lookup"><span data-stu-id="5815e-166">On the Action Pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="5815e-167">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="5815e-167">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5815e-168">Sisestage nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="5815e-168">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="5815e-169">Sisestage otsingunimi väljale **Otsingunimi**.</span><span class="sxs-lookup"><span data-stu-id="5815e-169">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="5815e-170">Sisestage kontotüüp väljale **Kontotüüp**.</span><span class="sxs-lookup"><span data-stu-id="5815e-170">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="5815e-171">Vajadusel sisestage tekst väljadele **Teate rida 1**, **Teate rida 2**, **Saatelehe tekst 1** ja **Saatelehe tekst 2**.</span><span class="sxs-lookup"><span data-stu-id="5815e-171">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="5815e-172">Sisestage jaotisse **Sisestamine** sisestamise andmed.</span><span class="sxs-lookup"><span data-stu-id="5815e-172">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="5815e-173">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5815e-173">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="5815e-174">Järgmine pilt näitab tulu/kulu konto näidet.</span><span class="sxs-lookup"><span data-stu-id="5815e-174">The following image shows an example of an income/expense account.</span></span>

![Tulu/kulu kontode seadistamine](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="5815e-176">Jaotiste seadistamine</span><span class="sxs-lookup"><span data-stu-id="5815e-176">Set up sections</span></span>

<span data-ttu-id="5815e-177">Jaotiste seadistamiseks läbige need etapid.</span><span class="sxs-lookup"><span data-stu-id="5815e-177">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="5815e-178">Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Täitmisgrupi määramine**.</span><span class="sxs-lookup"><span data-stu-id="5815e-178">On the Action Pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="5815e-179">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="5815e-179">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5815e-180">Sisestage väljale **Jaotise number** jaotise number.</span><span class="sxs-lookup"><span data-stu-id="5815e-180">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="5815e-181">Sisestage kirjeldus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="5815e-181">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="5815e-182">Sisestage väljale **Jaotise suurus** jaotise suurus.</span><span class="sxs-lookup"><span data-stu-id="5815e-182">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="5815e-183">Vajadusel konfigureerige jaotiste **Üldine** ja **Müügistatistika** sätteid.</span><span class="sxs-lookup"><span data-stu-id="5815e-183">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="5815e-184">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5815e-184">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="5815e-185">Täitmisgrupi määramise seadistamine</span><span class="sxs-lookup"><span data-stu-id="5815e-185">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="5815e-186">Täitmisgrupi määramise seadistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="5815e-186">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="5815e-187">Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Täitmisgrupi määramine**.</span><span class="sxs-lookup"><span data-stu-id="5815e-187">On the Action Pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="5815e-188">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="5815e-188">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5815e-189">Valige täitmisgrupp ripploendist **Täitmisgrupp**.</span><span class="sxs-lookup"><span data-stu-id="5815e-189">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="5815e-190">Sisestage kirjeldus ripploendisse **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="5815e-190">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="5815e-191">Valige tegevuspaanil nupp **Salvesta**</span><span class="sxs-lookup"><span data-stu-id="5815e-191">On the Action Pane, select **Save**</span></span>

<span data-ttu-id="5815e-192">Järgmine pilt näitab täitmisgrupi määramise seadistuse näidet.</span><span class="sxs-lookup"><span data-stu-id="5815e-192">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Täitmisgrupi määramiste seadistamine](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="5815e-194">Seifide seadistamine</span><span class="sxs-lookup"><span data-stu-id="5815e-194">Set up safes</span></span>

<span data-ttu-id="5815e-195">Seifide seadistamiseks läbige need etapid.</span><span class="sxs-lookup"><span data-stu-id="5815e-195">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="5815e-196">Valige tegevuspaanil vahekaart **Seadista** ja seejärel klõpsake suvandile **Seifid**.</span><span class="sxs-lookup"><span data-stu-id="5815e-196">On the Action Pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="5815e-197">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="5815e-197">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5815e-198">Sisestage seifi nimi.</span><span class="sxs-lookup"><span data-stu-id="5815e-198">Enter a name for the safe.</span></span>
1. <span data-ttu-id="5815e-199">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5815e-199">On the Action Pane, select **Save**.</span></span>

### <a name="ensure-unique-transaction-ids"></a><span data-ttu-id="5815e-200">Kordumatute kande-ID-de tagamine</span><span class="sxs-lookup"><span data-stu-id="5815e-200">Ensure unique transaction IDs</span></span>

<span data-ttu-id="5815e-201">Äriversiooni 10.0.18 kohaselt on kassa (POS) jaoks loodud kannete ID-d järjestikused ja sisaldavad järgmisi osi.</span><span class="sxs-lookup"><span data-stu-id="5815e-201">As of the Commerce version 10.0.18 , transaction IDs generated for the point of sale (POS) are sequential and include the following parts:</span></span>

- <span data-ttu-id="5815e-202">Fikseeritud osa, mis on ühendatud kaupluse ID ja terminali ID-ga.</span><span class="sxs-lookup"><span data-stu-id="5815e-202">A fixed part, which is a concatenation of store ID and terminal ID.</span></span> 
- <span data-ttu-id="5815e-203">Seeriaosa, mis on numbrite jada.</span><span class="sxs-lookup"><span data-stu-id="5815e-203">A sequential part, which is a number sequence.</span></span> 

<span data-ttu-id="5815e-204">Täpsemalt on vorming *{store}{terminal} -{numbersequence}*.</span><span class="sxs-lookup"><span data-stu-id="5815e-204">Specifically, the format is *{store}-{terminal}-{numbersequence}*.</span></span> 

<span data-ttu-id="5815e-205">Kuna kande ID-sid saab luua ühenduseta ja võrguühenduseta režiimides, on olemas duplikaatkande ID-de genereerimise eksemplarid.</span><span class="sxs-lookup"><span data-stu-id="5815e-205">Because transaction IDs can be generated in offline and online modes, there have been instances of duplicate transaction IDs being generated.</span></span> <span data-ttu-id="5815e-206">Kande ID duplikaatide eemaldamiseks on vaja andmed käsitsi parandada.</span><span class="sxs-lookup"><span data-stu-id="5815e-206">Eliminating duplicate transaction IDs requires a lot of manual data fixing.</span></span> 

<span data-ttu-id="5815e-207">Rakenduse kommertsversiooniga 10.0.19 värskendati kande ID vormingut, et eemaldada seeriaosa ja selle asemel kasutatakse 13-numbrit, mis on loodud arvutades aja millisekundites alates 1970.</span><span class="sxs-lookup"><span data-stu-id="5815e-207">With Commerce version 10.0.19, the transaction ID format has been updated to remove the sequential part and instead uses a 13-digit number generated by calculating the time in milliseconds since 1970.</span></span> <span data-ttu-id="5815e-208">Selle muudatusega on uus kande ID vorming *{store} - {terminal} - {millisecondsSince1970}*.</span><span class="sxs-lookup"><span data-stu-id="5815e-208">With this change, the new transaction ID format is *{store}-{terminal}-{millisecondsSince1970}*.</span></span> <span data-ttu-id="5815e-209">See värskendus muudab kande ID mittejärjestatuks ja tagab, et kande ID-d on alati kordumatud.</span><span class="sxs-lookup"><span data-stu-id="5815e-209">This update makes the transaction ID non-sequential and ensures that transaction IDs are always unique.</span></span> 

> [!NOTE]
> <span data-ttu-id="5815e-210">Kannete ID-d on mõeldud ainult sisesüsteemi jaoks, nii et need ei pea olema järjestikused.</span><span class="sxs-lookup"><span data-stu-id="5815e-210">Transaction IDs are meant for internal system use only, so they are not required to be sequential.</span></span> <span data-ttu-id="5815e-211">Paljud riigid nõuavad siiski, et sissetuleku ID-d oleks järjestikused.</span><span class="sxs-lookup"><span data-stu-id="5815e-211">However, many countries require receipt IDs to be sequential.</span></span>

<span data-ttu-id="5815e-212">Uue kande ID vormingu funktsiooni saab lubada **funktsioonihalduse** tööruumis.</span><span class="sxs-lookup"><span data-stu-id="5815e-212">The new transaction ID format feature can be enabled from the **Feature management** workspace.</span></span> 

<span data-ttu-id="5815e-213">Uute kande-ID-de kasutamise lubamiseks järgige järgmiseid samme.</span><span class="sxs-lookup"><span data-stu-id="5815e-213">To enable the use of new transaction IDs, follow these steps:</span></span>

1. <span data-ttu-id="5815e-214">Avage Commerce'i peakorteris **Süsteemihaldus \> Tööruumid \> Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="5815e-214">In Commerce headquarters, go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="5815e-215">"Jaemüügi ja äri" mooduli filter.</span><span class="sxs-lookup"><span data-stu-id="5815e-215">Filter for the "retail and commerce" module.</span></span>
1. <span data-ttu-id="5815e-216">Otsige **"luba uut kande ID-d, et vältida topeltkande ID-de tekkimist"** funktsiooni nime.</span><span class="sxs-lookup"><span data-stu-id="5815e-216">Search for the **Enable new transaction id to avoid duplicate transaction ids** feature name.</span></span>
1. <span data-ttu-id="5815e-217">Valige funktsioon, mida soovite sisse lülitada, ja seejärel valige paremal paanil nupp **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="5815e-217">Select the feature, and then select **Enable Now** in the right pane.</span></span>  
1. <span data-ttu-id="5815e-218">Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.</span><span class="sxs-lookup"><span data-stu-id="5815e-218">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="5815e-219">Käitage **1070 kanali konfiguratsiooni** ja **1170 POS Task Recorderi** tööd, et sünkroonida lubatud funktsioon kauplustesse.</span><span class="sxs-lookup"><span data-stu-id="5815e-219">Run the **1070 Channel configuration** and **1170 POS task recorder** jobs to synchronize the enabled feature to the stores.</span></span>
1. <span data-ttu-id="5815e-220">Pärast muudatuste saatmist kauplustesse tuleb kassaterminalid sulgeda ja uuesti avada, et kasutada uut kande ID vormingut.</span><span class="sxs-lookup"><span data-stu-id="5815e-220">After the changes have been sent to the stores, POS terminals must be closed and reopened to use the new transaction ID format.</span></span> 

> [!NOTE]
> <span data-ttu-id="5815e-221">Pärast uue kande ID vormingu funktsiooni lubamist ei saa te seda funktsiooni keelata.</span><span class="sxs-lookup"><span data-stu-id="5815e-221">After the new transaction ID format feature is enabled, you will not be able to disable this feature.</span></span> <span data-ttu-id="5815e-222">Kui see tuleb keelata, pöörduge commerce Supporti poole.</span><span class="sxs-lookup"><span data-stu-id="5815e-222">If it must be disabled, please contact Commerce Support.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5815e-223">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="5815e-223">Additional resources</span></span>

[<span data-ttu-id="5815e-224">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="5815e-224">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="5815e-225">Kanali häälestuse eeltingimused</span><span class="sxs-lookup"><span data-stu-id="5815e-225">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="5815e-226">Veebikanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="5815e-226">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="5815e-227">Kõnekeskuse kanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="5815e-227">Set up a call center channel</span></span>](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
