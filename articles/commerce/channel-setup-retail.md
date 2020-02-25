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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8ac01f36912fa5e8a09bb4f324ef272cec737aa1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002377"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="7d397-103">Jaemüügikanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="7d397-103">Set up a retail channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7d397-104">Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus jaemüügikanal.</span><span class="sxs-lookup"><span data-stu-id="7d397-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7d397-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="7d397-105">Overview</span></span>

<span data-ttu-id="7d397-106">Dynamics 365 Commerce toetab mitut jaemüügikanalit.</span><span class="sxs-lookup"><span data-stu-id="7d397-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="7d397-107">Jaemüügikanalid hõlmavad võrgupoode, kõnekeskusi ja jaekauplusi (neid nimetatakse ka füüsilisteks kauplusteks).</span><span class="sxs-lookup"><span data-stu-id="7d397-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="7d397-108">Igal kaupluse kanalil võivad olla oma makseviisid, hinnagrupid, kassaregistrid, tulu- ja kulukontod ning personal.</span><span class="sxs-lookup"><span data-stu-id="7d397-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="7d397-109">Enne jaekaupluse kanali loomist tuleb seadistada kõik need elemendid.</span><span class="sxs-lookup"><span data-stu-id="7d397-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="7d397-110">Enne jaemüügikanali loomist veenduge, et järgite [kanali eeltingimusi](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="7d397-110">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="7d397-111">Uue jaemüügikanali loomine ja konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="7d397-111">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="7d397-112">Avage navigatsioonipaneelil **Moodulid \> Kanalid \> Kauplused \> Kõik kauplused**.</span><span class="sxs-lookup"><span data-stu-id="7d397-112">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="7d397-113">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="7d397-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7d397-114">Sisestage väljale **Nimi** uue kanali nimi.</span><span class="sxs-lookup"><span data-stu-id="7d397-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="7d397-115">Sisestage väljale **Kaupluse number** kordumatu kaupluse number.</span><span class="sxs-lookup"><span data-stu-id="7d397-115">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="7d397-116">See number võib olla tähtnumbriline ja kuni 10 tähemärgi pikkune.</span><span class="sxs-lookup"><span data-stu-id="7d397-116">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="7d397-117">Sisestage ripploendisse **Juriidiline isik** sobiv juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="7d397-117">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="7d397-118">Sisestage ripploendisse **Ladu** sobiv ladu.</span><span class="sxs-lookup"><span data-stu-id="7d397-118">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="7d397-119">Valige sobiv ajavöönd väljal **Kaupluse ajavöönd**.</span><span class="sxs-lookup"><span data-stu-id="7d397-119">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="7d397-120">Valige ripploendist **Käibemaksugrupp** kauplusele sobiv käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="7d397-120">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="7d397-121">Valige väljal **Valuuta** sobiv valuuta.</span><span class="sxs-lookup"><span data-stu-id="7d397-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="7d397-122">Sisestage väljale **Kliendi aadressiraamat** kehtiv aadressiraamat.</span><span class="sxs-lookup"><span data-stu-id="7d397-122">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="7d397-123">Sisestage väljale **Vaikeklient** kehtiv vaikeklient.</span><span class="sxs-lookup"><span data-stu-id="7d397-123">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="7d397-124">Valige väljal **Funktsiooniprofiil** funktsiooniprofiil, kui see on kohaldatav.</span><span class="sxs-lookup"><span data-stu-id="7d397-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="7d397-125">Sisestage väljale **Meiliteavituse profiil** kehtiv meiliteavituse profiil.</span><span class="sxs-lookup"><span data-stu-id="7d397-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="7d397-126">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7d397-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7d397-127">Järgmine pilt näitab uue jaemüügikanali loomist.</span><span class="sxs-lookup"><span data-stu-id="7d397-127">The following image shows the creation of a new retail channel.</span></span>

![Uus jaemüügikanal](media/channel-setup-retail-1.png)

<span data-ttu-id="7d397-129">Järgmine pilt näitab jaemüügikanali näidet.</span><span class="sxs-lookup"><span data-stu-id="7d397-129">The following image shows an example retail channel.</span></span>

![Jaemüügikanali näide](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="7d397-131">Muud sätted</span><span class="sxs-lookup"><span data-stu-id="7d397-131">Other settings</span></span>

<span data-ttu-id="7d397-132">On mitmeid muid valikulisi sätteid, mida saab jaotistes **Väljavõte/sulgemine** ja **Mitmesugust** vastavalt jaemüügikaupluse vajadustele seadistada.</span><span class="sxs-lookup"><span data-stu-id="7d397-132">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="7d397-133">Lisaks vt jaotist [Kassa ekraanipaigutused](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json), et saada lisainfot vaikimisi ekraanipaigutuse seadistamise kohta jaotises **Ekraani paigutus** ja jaotist [Jaemüügi riistvarajaama konfigureerimine ja installimine](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation), et saada seadistamise infot **Riistvarajaamade** jaotise kohta.</span><span class="sxs-lookup"><span data-stu-id="7d397-133">In addition, see [Screen layouts for the point of sale (POS)](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="7d397-134">Järgmine pilt näitab jaemüügikanali seadistuse konfiguratsiooni näidet.</span><span class="sxs-lookup"><span data-stu-id="7d397-134">The following image shows an example retail channel setup configuration.</span></span>

![Jaemüügikanali konfiguratsiooni näide](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="7d397-136">Täiendava kanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="7d397-136">Additional channel set up</span></span>

<span data-ttu-id="7d397-137">Et kanalit saaks leida **Tegevuspaanil** jaotise **Seadistus** alt, tuleb seadistada täiendavad elemendid.</span><span class="sxs-lookup"><span data-stu-id="7d397-137">There are additional items that need to be set up for a channel that can be found on the **Action pane** under the **Set up** section.</span></span>

<span data-ttu-id="7d397-138">Veebikanali häälestamiseks nõutavad täiendavad toimingud hõlmavad makseviiside, sularaha deklaratsiooni, tarneviiside, tulu/kulu konto, jaotiste, täitmisgrupi määramise ja seifide seadistamist.</span><span class="sxs-lookup"><span data-stu-id="7d397-138">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="7d397-139">Järgmine pilt näitab erinevaid täiendavaid jaemüügikanali seadistamise suvandeid vahekaardil **Seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="7d397-139">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Kanali seadistamine](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="7d397-141">Seadistada maksemeetodid</span><span class="sxs-lookup"><span data-stu-id="7d397-141">Set up payment methods</span></span>

<span data-ttu-id="7d397-142">Kõigi selles kanalis toetatud maksetüübi makseviiside seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="7d397-142">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="7d397-143">Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Makseviisid**.</span><span class="sxs-lookup"><span data-stu-id="7d397-143">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="7d397-144">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="7d397-144">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7d397-145">Valige navigeerimispaanil soovitud makseviis.</span><span class="sxs-lookup"><span data-stu-id="7d397-145">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="7d397-146">Sisestage jaotises **Üldine** **Toimingu nimi** ja konfigureerige muud soovitud sätted.</span><span class="sxs-lookup"><span data-stu-id="7d397-146">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="7d397-147">Konfigureerige kõik maksetüübi jaoks vajalikud lisasätted.</span><span class="sxs-lookup"><span data-stu-id="7d397-147">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="7d397-148">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7d397-148">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7d397-149">Järgmine pilt näitab sularaha makseviisi näidet.</span><span class="sxs-lookup"><span data-stu-id="7d397-149">The following image shows an example of a cash payment method.</span></span>

![Makseviiside näited](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="7d397-151">Sularaha deklaratsiooni seadistamine</span><span class="sxs-lookup"><span data-stu-id="7d397-151">Set up cash declaration</span></span>

1. <span data-ttu-id="7d397-152">Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Sularaha deklaratsioon**.</span><span class="sxs-lookup"><span data-stu-id="7d397-152">On the action pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="7d397-153">Valige tegevuspaanil **Uus** ja seejärel looge kõik kohaldatavad **Mündi** ja **Paberraha** nominaalväärtused.</span><span class="sxs-lookup"><span data-stu-id="7d397-153">On the action pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="7d397-154">Järgmine pilt näitab sularaha deklaratsiooni näidet.</span><span class="sxs-lookup"><span data-stu-id="7d397-154">The following image shows an example of a cash declaration.</span></span>

![Sularaha deklaratsioonide seadistamine](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="7d397-156">Tarneviiside häälestamine</span><span class="sxs-lookup"><span data-stu-id="7d397-156">Set up modes of delivery</span></span>

<span data-ttu-id="7d397-157">Konfigureeritud tarneviise saate näha valides **Tarneviisid** vahekaardilt **Seadistus** **Tegevuspaani** alt.</span><span class="sxs-lookup"><span data-stu-id="7d397-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="7d397-158">Tarneviisi muutmiseks või lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="7d397-158">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="7d397-159">Avage navigeerimispaanil **Moodulid \> Varude haldus \> Tarneviisid**.</span><span class="sxs-lookup"><span data-stu-id="7d397-159">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="7d397-160">Valige tegevuspaanilt **Uus**, et luua uus tarneviis, või valige olemasolev režiim.</span><span class="sxs-lookup"><span data-stu-id="7d397-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="7d397-161">Kanali lisamiseks valige jaotisest **Jaemüügikanalid** käsk **Lisa rida**.</span><span class="sxs-lookup"><span data-stu-id="7d397-161">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="7d397-162">Kanalite lisamine kasutades organisatsiooni sõlmpunkte, mitte iga kanalit ükshaaval lisades, täiustab kanalite lisamist veelgi.</span><span class="sxs-lookup"><span data-stu-id="7d397-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="7d397-163">Järgmine pilt näitab tarneviisi näidet.</span><span class="sxs-lookup"><span data-stu-id="7d397-163">The following image shows an example of a mode of delivery.</span></span>

![Tarneviiside häälestamine](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="7d397-165">Tulu/kulu konto seadistamine</span><span class="sxs-lookup"><span data-stu-id="7d397-165">Set up income/expense account</span></span>

<span data-ttu-id="7d397-166">Tulu/kulu konto seadistamiseks läbige need etapid.</span><span class="sxs-lookup"><span data-stu-id="7d397-166">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="7d397-167">Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Tulu/kulu konto**.</span><span class="sxs-lookup"><span data-stu-id="7d397-167">On the action pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="7d397-168">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="7d397-168">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7d397-169">Sisestage nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="7d397-169">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="7d397-170">Sisestage otsingunimi väljale **Otsingunimi**.</span><span class="sxs-lookup"><span data-stu-id="7d397-170">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="7d397-171">Sisestage kontotüüp väljale **Kontotüüp**.</span><span class="sxs-lookup"><span data-stu-id="7d397-171">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="7d397-172">Vajadusel sisestage tekst väljadele **Teate rida 1**, **Teate rida 2**, **Saatelehe tekst 1** ja **Saatelehe tekst 2**.</span><span class="sxs-lookup"><span data-stu-id="7d397-172">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="7d397-173">Sisestage jaotisse **Sisestamine** sisestamise andmed.</span><span class="sxs-lookup"><span data-stu-id="7d397-173">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="7d397-174">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7d397-174">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7d397-175">Järgmine pilt näitab tulu/kulu konto näidet.</span><span class="sxs-lookup"><span data-stu-id="7d397-175">The following image shows an example of an income/expense account.</span></span>

![Tulu/kulu kontode seadistamine](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="7d397-177">Jaotiste seadistamine</span><span class="sxs-lookup"><span data-stu-id="7d397-177">Set up sections</span></span>

<span data-ttu-id="7d397-178">Jaotiste seadistamiseks läbige need etapid.</span><span class="sxs-lookup"><span data-stu-id="7d397-178">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="7d397-179">Valige tegevuspaanil vahekaart **Seadista** ja seejärel klõpsa **Jaotised**.</span><span class="sxs-lookup"><span data-stu-id="7d397-179">On the action pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="7d397-180">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="7d397-180">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7d397-181">Sisestage väljale **Jaotise number** jaotise number.</span><span class="sxs-lookup"><span data-stu-id="7d397-181">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="7d397-182">Sisestage kirjeldus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="7d397-182">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="7d397-183">Sisestage väljale **Jaotise suurus** jaotise suurus.</span><span class="sxs-lookup"><span data-stu-id="7d397-183">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="7d397-184">Vajadusel konfigureerige jaotiste **Üldine** ja **Müügistatistika** sätteid.</span><span class="sxs-lookup"><span data-stu-id="7d397-184">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="7d397-185">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7d397-185">On the action pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="7d397-186">Täitmisgrupi määramise seadistamine</span><span class="sxs-lookup"><span data-stu-id="7d397-186">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="7d397-187">Täitmisgrupi määramise seadistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="7d397-187">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="7d397-188">Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Täitmisgrupi määramine**.</span><span class="sxs-lookup"><span data-stu-id="7d397-188">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="7d397-189">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="7d397-189">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7d397-190">Valige täitmisgrupp ripploendist **Täitmisgrupp**.</span><span class="sxs-lookup"><span data-stu-id="7d397-190">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="7d397-191">Sisestage kirjeldus ripploendisse **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="7d397-191">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="7d397-192">Valige toimingupaanil nupp **Salvesta**</span><span class="sxs-lookup"><span data-stu-id="7d397-192">On the action pane, select **Save**</span></span>

<span data-ttu-id="7d397-193">Järgmine pilt näitab täitmisgrupi määramise seadistuse näidet.</span><span class="sxs-lookup"><span data-stu-id="7d397-193">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Täitmisgrupi määramiste seadistamine](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="7d397-195">Seifide seadistamine</span><span class="sxs-lookup"><span data-stu-id="7d397-195">Set up safes</span></span>

<span data-ttu-id="7d397-196">Seifide seadistamiseks läbige need etapid.</span><span class="sxs-lookup"><span data-stu-id="7d397-196">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="7d397-197">Valige tegevuspaanil vahekaart **Seadista** ja seejärel klõpsa **Seifid**.</span><span class="sxs-lookup"><span data-stu-id="7d397-197">On the action pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="7d397-198">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="7d397-198">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7d397-199">Sisestage seifi nimi.</span><span class="sxs-lookup"><span data-stu-id="7d397-199">Enter a name for the safe.</span></span>
1. <span data-ttu-id="7d397-200">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7d397-200">On the action pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d397-201">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="7d397-201">Additional resources</span></span>

[<span data-ttu-id="7d397-202">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="7d397-202">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="7d397-203">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="7d397-203">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="7d397-204">Veebikanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="7d397-204">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="7d397-205">Kõnekeskuse kanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="7d397-205">Set up a call center channel</span></span>](channel-setup-callcenter.md)
