---
title: Jaemüügikanali seadistamine
description: Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus jaemüügikanal.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: a5d0a081cff9fab8dc0a513496e6a5eccd03c871
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478256"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="d085d-103">Jaemüügikanali häälestus</span><span class="sxs-lookup"><span data-stu-id="d085d-103">Set up a retail channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d085d-104">Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus jaemüügikanal.</span><span class="sxs-lookup"><span data-stu-id="d085d-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d085d-105">Dynamics 365 Commerce toetab mitut jaemüügikanalit.</span><span class="sxs-lookup"><span data-stu-id="d085d-105">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="d085d-106">Jaemüügikanalid hõlmavad võrgupoode, kõnekeskusi ja jaekauplusi (neid nimetatakse ka füüsilisteks kauplusteks).</span><span class="sxs-lookup"><span data-stu-id="d085d-106">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="d085d-107">Igal kaupluse kanalil võivad olla oma makseviisid, hinnagrupid, kassaregistrid, tulu- ja kulukontod ning personal.</span><span class="sxs-lookup"><span data-stu-id="d085d-107">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="d085d-108">Enne jaekaupluse kanali loomist tuleb seadistada kõik need elemendid.</span><span class="sxs-lookup"><span data-stu-id="d085d-108">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="d085d-109">Enne jaemüügikanali loomist veenduge, et järgite [kanali eeltingimusi](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="d085d-109">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="d085d-110">Uue jaemüügikanali loomine ja konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d085d-110">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="d085d-111">Avage navigatsioonipaneelil **Moodulid \> Kanalid \> Kauplused \> Kõik kauplused**.</span><span class="sxs-lookup"><span data-stu-id="d085d-111">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="d085d-112">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d085d-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d085d-113">Sisestage väljale **Nimi** uue kanali nimi.</span><span class="sxs-lookup"><span data-stu-id="d085d-113">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="d085d-114">Sisestage väljale **Kaupluse number** kordumatu kaupluse number.</span><span class="sxs-lookup"><span data-stu-id="d085d-114">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="d085d-115">See number võib olla tähtnumbriline ja kuni 10 tähemärgi pikkune.</span><span class="sxs-lookup"><span data-stu-id="d085d-115">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="d085d-116">Sisestage ripploendisse **Juriidiline isik** sobiv juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="d085d-116">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="d085d-117">Sisestage ripploendisse **Ladu** sobiv ladu.</span><span class="sxs-lookup"><span data-stu-id="d085d-117">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="d085d-118">Valige sobiv ajavöönd väljal **Kaupluse ajavöönd**.</span><span class="sxs-lookup"><span data-stu-id="d085d-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="d085d-119">Valige ripploendist **Käibemaksugrupp** kauplusele sobiv käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="d085d-119">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="d085d-120">Valige väljal **Valuuta** sobiv valuuta.</span><span class="sxs-lookup"><span data-stu-id="d085d-120">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="d085d-121">Sisestage väljale **Kliendi aadressiraamat** kehtiv aadressiraamat.</span><span class="sxs-lookup"><span data-stu-id="d085d-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="d085d-122">Sisestage väljale **Vaikeklient** kehtiv vaikeklient.</span><span class="sxs-lookup"><span data-stu-id="d085d-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="d085d-123">Valige väljal **Funktsiooniprofiil** funktsiooniprofiil, kui see on kohaldatav.</span><span class="sxs-lookup"><span data-stu-id="d085d-123">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="d085d-124">Sisestage väljale **Meiliteavituse profiil** kehtiv meiliteavituse profiil.</span><span class="sxs-lookup"><span data-stu-id="d085d-124">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="d085d-125">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d085d-125">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d085d-126">Järgmine pilt näitab uue jaemüügikanali loomist.</span><span class="sxs-lookup"><span data-stu-id="d085d-126">The following image shows the creation of a new retail channel.</span></span>

![Uus jaemüügikanal](media/channel-setup-retail-1.png)

<span data-ttu-id="d085d-128">Järgmine pilt näitab jaemüügikanali näidet.</span><span class="sxs-lookup"><span data-stu-id="d085d-128">The following image shows an example retail channel.</span></span>

![Jaemüügikanali näide](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="d085d-130">Muud sätted</span><span class="sxs-lookup"><span data-stu-id="d085d-130">Other settings</span></span>

<span data-ttu-id="d085d-131">On mitmeid muid valikulisi sätteid, mida saab jaotistes **Väljavõte/sulgemine** ja **Mitmesugust** vastavalt jaemüügikaupluse vajadustele seadistada.</span><span class="sxs-lookup"><span data-stu-id="d085d-131">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="d085d-132">Lisaks vt jaotist [Kassa ekraanipaigutused](pos-screen-layouts.md), et saada lisainfot vaikimisi ekraanipaigutuse seadistamise kohta jaotises **Ekraani paigutus** ja jaotist [Jaemüügi riistvarajaama konfigureerimine ja installimine](retail-hardware-station-configuration-installation.md), et saada seadistamise infot **Riistvarajaamade** jaotise kohta.</span><span class="sxs-lookup"><span data-stu-id="d085d-132">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="d085d-133">Järgmine pilt näitab jaemüügikanali seadistuse konfiguratsiooni näidet.</span><span class="sxs-lookup"><span data-stu-id="d085d-133">The following image shows an example retail channel setup configuration.</span></span>

![Jaemüügikanali konfiguratsiooni näide](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="d085d-135">Täiendava kanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="d085d-135">Additional channel set up</span></span>

<span data-ttu-id="d085d-136">Et kanalit saaks leida **Tegevuspaanil** jaotise **Seadistus** alt, tuleb seadistada täiendavad elemendid.</span><span class="sxs-lookup"><span data-stu-id="d085d-136">There are additional items that need to be set up for a channel that can be found on the **Action pane** under the **Set up** section.</span></span>

<span data-ttu-id="d085d-137">Veebikanali häälestamiseks nõutavad täiendavad toimingud hõlmavad makseviiside, sularaha deklaratsiooni, tarneviiside, tulu/kulu konto, jaotiste, täitmisgrupi määramise ja seifide seadistamist.</span><span class="sxs-lookup"><span data-stu-id="d085d-137">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="d085d-138">Järgmine pilt näitab erinevaid täiendavaid jaemüügikanali seadistamise suvandeid vahekaardil **Seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="d085d-138">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Kanali seadistamine](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="d085d-140">Seadistada maksemeetodid</span><span class="sxs-lookup"><span data-stu-id="d085d-140">Set up payment methods</span></span>

<span data-ttu-id="d085d-141">Kõigi selles kanalis toetatud maksetüübi makseviiside seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="d085d-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="d085d-142">Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Makseviisid**.</span><span class="sxs-lookup"><span data-stu-id="d085d-142">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="d085d-143">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d085d-143">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d085d-144">Valige navigeerimispaanil soovitud makseviis.</span><span class="sxs-lookup"><span data-stu-id="d085d-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="d085d-145">Sisestage jaotises **Üldine** **Toimingu nimi** ja konfigureerige muud soovitud sätted.</span><span class="sxs-lookup"><span data-stu-id="d085d-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="d085d-146">Konfigureerige kõik maksetüübi jaoks vajalikud lisasätted.</span><span class="sxs-lookup"><span data-stu-id="d085d-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="d085d-147">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d085d-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d085d-148">Järgmine pilt näitab sularaha makseviisi näidet.</span><span class="sxs-lookup"><span data-stu-id="d085d-148">The following image shows an example of a cash payment method.</span></span>

![Makseviiside näited](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="d085d-150">Sularaha deklaratsiooni seadistamine</span><span class="sxs-lookup"><span data-stu-id="d085d-150">Set up cash declaration</span></span>

1. <span data-ttu-id="d085d-151">Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Sularaha deklaratsioon**.</span><span class="sxs-lookup"><span data-stu-id="d085d-151">On the action pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="d085d-152">Valige tegevuspaanil **Uus** ja seejärel looge kõik kohaldatavad **Mündi** ja **Paberraha** nominaalväärtused.</span><span class="sxs-lookup"><span data-stu-id="d085d-152">On the action pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="d085d-153">Järgmine pilt näitab sularaha deklaratsiooni näidet.</span><span class="sxs-lookup"><span data-stu-id="d085d-153">The following image shows an example of a cash declaration.</span></span>

![Sularaha deklaratsioonide seadistamine](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="d085d-155">Tarneviiside häälestamine</span><span class="sxs-lookup"><span data-stu-id="d085d-155">Set up modes of delivery</span></span>

<span data-ttu-id="d085d-156">Konfigureeritud tarneviise saate näha valides **Tarneviisid** vahekaardilt **Seadistus** **Tegevuspaani** alt.</span><span class="sxs-lookup"><span data-stu-id="d085d-156">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="d085d-157">Tarneviisi muutmiseks või lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="d085d-157">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="d085d-158">Avage navigeerimispaanil **Moodulid \> Varude haldus \> Tarneviisid**.</span><span class="sxs-lookup"><span data-stu-id="d085d-158">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="d085d-159">Valige tegevuspaanilt **Uus**, et luua uus tarneviis, või valige olemasolev režiim.</span><span class="sxs-lookup"><span data-stu-id="d085d-159">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="d085d-160">Kanali lisamiseks valige jaotisest **Jaemüügikanalid** käsk **Lisa rida**.</span><span class="sxs-lookup"><span data-stu-id="d085d-160">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="d085d-161">Kanalite lisamine kasutades organisatsiooni sõlmpunkte, mitte iga kanalit ükshaaval lisades, täiustab kanalite lisamist veelgi.</span><span class="sxs-lookup"><span data-stu-id="d085d-161">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="d085d-162">Järgmine pilt näitab tarneviisi näidet.</span><span class="sxs-lookup"><span data-stu-id="d085d-162">The following image shows an example of a mode of delivery.</span></span>

![Tarneviiside häälestamine](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="d085d-164">Tulu/kulu konto seadistamine</span><span class="sxs-lookup"><span data-stu-id="d085d-164">Set up income/expense account</span></span>

<span data-ttu-id="d085d-165">Tulu/kulu konto seadistamiseks läbige need etapid.</span><span class="sxs-lookup"><span data-stu-id="d085d-165">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="d085d-166">Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Tulu/kulu konto**.</span><span class="sxs-lookup"><span data-stu-id="d085d-166">On the action pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="d085d-167">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d085d-167">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d085d-168">Sisestage nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="d085d-168">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="d085d-169">Sisestage otsingunimi väljale **Otsingunimi**.</span><span class="sxs-lookup"><span data-stu-id="d085d-169">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="d085d-170">Sisestage kontotüüp väljale **Kontotüüp**.</span><span class="sxs-lookup"><span data-stu-id="d085d-170">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="d085d-171">Vajadusel sisestage tekst väljadele **Teate rida 1**, **Teate rida 2**, **Saatelehe tekst 1** ja **Saatelehe tekst 2**.</span><span class="sxs-lookup"><span data-stu-id="d085d-171">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="d085d-172">Sisestage jaotisse **Sisestamine** sisestamise andmed.</span><span class="sxs-lookup"><span data-stu-id="d085d-172">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="d085d-173">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d085d-173">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d085d-174">Järgmine pilt näitab tulu/kulu konto näidet.</span><span class="sxs-lookup"><span data-stu-id="d085d-174">The following image shows an example of an income/expense account.</span></span>

![Tulu/kulu kontode seadistamine](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="d085d-176">Jaotiste seadistamine</span><span class="sxs-lookup"><span data-stu-id="d085d-176">Set up sections</span></span>

<span data-ttu-id="d085d-177">Jaotiste seadistamiseks läbige need etapid.</span><span class="sxs-lookup"><span data-stu-id="d085d-177">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="d085d-178">Valige tegevuspaanil vahekaart **Seadista** ja seejärel klõpsa **Jaotised**.</span><span class="sxs-lookup"><span data-stu-id="d085d-178">On the action pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="d085d-179">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d085d-179">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d085d-180">Sisestage väljale **Jaotise number** jaotise number.</span><span class="sxs-lookup"><span data-stu-id="d085d-180">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="d085d-181">Sisestage kirjeldus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="d085d-181">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="d085d-182">Sisestage väljale **Jaotise suurus** jaotise suurus.</span><span class="sxs-lookup"><span data-stu-id="d085d-182">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="d085d-183">Vajadusel konfigureerige jaotiste **Üldine** ja **Müügistatistika** sätteid.</span><span class="sxs-lookup"><span data-stu-id="d085d-183">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="d085d-184">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d085d-184">On the action pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="d085d-185">Täitmisgrupi määramise seadistamine</span><span class="sxs-lookup"><span data-stu-id="d085d-185">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="d085d-186">Täitmisgrupi määramise seadistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="d085d-186">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="d085d-187">Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Täitmisgrupi määramine**.</span><span class="sxs-lookup"><span data-stu-id="d085d-187">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="d085d-188">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d085d-188">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d085d-189">Valige täitmisgrupp ripploendist **Täitmisgrupp**.</span><span class="sxs-lookup"><span data-stu-id="d085d-189">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="d085d-190">Sisestage kirjeldus ripploendisse **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="d085d-190">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="d085d-191">Valige toimingupaanil nupp **Salvesta**</span><span class="sxs-lookup"><span data-stu-id="d085d-191">On the action pane, select **Save**</span></span>

<span data-ttu-id="d085d-192">Järgmine pilt näitab täitmisgrupi määramise seadistuse näidet.</span><span class="sxs-lookup"><span data-stu-id="d085d-192">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Täitmisgrupi määramiste seadistamine](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="d085d-194">Seifide seadistamine</span><span class="sxs-lookup"><span data-stu-id="d085d-194">Set up safes</span></span>

<span data-ttu-id="d085d-195">Seifide seadistamiseks läbige need etapid.</span><span class="sxs-lookup"><span data-stu-id="d085d-195">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="d085d-196">Valige tegevuspaanil vahekaart **Seadista** ja seejärel klõpsa **Seifid**.</span><span class="sxs-lookup"><span data-stu-id="d085d-196">On the action pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="d085d-197">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d085d-197">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d085d-198">Sisestage seifi nimi.</span><span class="sxs-lookup"><span data-stu-id="d085d-198">Enter a name for the safe.</span></span>
1. <span data-ttu-id="d085d-199">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d085d-199">On the action pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d085d-200">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="d085d-200">Additional resources</span></span>

[<span data-ttu-id="d085d-201">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="d085d-201">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="d085d-202">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="d085d-202">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="d085d-203">Veebikanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="d085d-203">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="d085d-204">Kõnekeskuse kanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="d085d-204">Set up a call center channel</span></span>](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
