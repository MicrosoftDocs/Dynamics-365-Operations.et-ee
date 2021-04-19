---
title: Kõnekeskuse kanali seadistamine
description: Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus kõnekeskus.
author: samjarawan
ms.date: 03/13/2020
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
ms.openlocfilehash: e89c63c90aa8d46fd23900897a54165e14fb635d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800659"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="18fc4-103">Kõnekeskuse kanali häälestus</span><span class="sxs-lookup"><span data-stu-id="18fc4-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="18fc4-104">Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus kõnekeskus.</span><span class="sxs-lookup"><span data-stu-id="18fc4-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="18fc4-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="18fc4-105">Overview</span></span>


<span data-ttu-id="18fc4-106">Rakenduse Dynamics 365 Commerce kõnekeskus on sellist tüüpi Commerce'i kanal, mille saab määratleda rakenduses.</span><span class="sxs-lookup"><span data-stu-id="18fc4-106">In Dynamics 365 Commerce, a call center is a type of Commerce channel that can be defined in the application.</span></span> <span data-ttu-id="18fc4-107">Kõnekeskuse üksustele kanali määratlemine võimaldab süsteemil siduda konkreetsed andmed ja tellimuse töötlemise vaikesätted müügitellimustega.</span><span class="sxs-lookup"><span data-stu-id="18fc4-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="18fc4-108">Kui ettevõttel on võimalik määratleda mitu kõnekeskuse kanalit Commerce'is, on oluline märkida, et üks kasutaja võib olla seotud ainult ühe kõnekeskuse kanaliga.</span><span class="sxs-lookup"><span data-stu-id="18fc4-108">While a company can define multiple call center channels in Commerce, it is important to note that an individual user may only be linked to one call center channel.</span></span> 

<span data-ttu-id="18fc4-109">Enne uue kõnekeskuse kanali loomist veenduge, et olete lõpetanud [Kanali eeltingimuste seadistuse](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="18fc4-109">Before you create a new call center channel, ensure that you have completed the [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="18fc4-110">Uue kõnekeskuse kanali loomine ja konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="18fc4-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="18fc4-111">Uue kõnekeskuse kanali loomiseks ja konfigureerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="18fc4-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="18fc4-112">Minge navigatsioonipaanil jaotisse **Jaemüük ja kaubandus \> Kanalid \> Kõnekeskused \> Kõik kõnekeskused**.</span><span class="sxs-lookup"><span data-stu-id="18fc4-112">In the navigation pane, go to **Retail and Commerce \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="18fc4-113">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="18fc4-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="18fc4-114">Sisestage väljale **Nimi** uue kanali nimi.</span><span class="sxs-lookup"><span data-stu-id="18fc4-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="18fc4-115">Valige ripploendist sobiv **Juriidiline isik**.</span><span class="sxs-lookup"><span data-stu-id="18fc4-115">Select the appropriate **Legal entity** from the drop-down.</span></span>
1. <span data-ttu-id="18fc4-116">Valige ripploendist sobiv **Lao** asukoht.</span><span class="sxs-lookup"><span data-stu-id="18fc4-116">Select the appropriate **Warehouse** location from the drop-down.</span></span> <span data-ttu-id="18fc4-117">Seda asukohta kasutatakse vaikimisi selle kõnekeskuse kanali jaoks loodud müügitellimuste puhul, kui kliendi või kauba tasemel pole määratud muid vaikesätteid.</span><span class="sxs-lookup"><span data-stu-id="18fc4-117">This location will be used as the default on sales orders created for this call center channel, unless other defaults have been defined at the customer or item level.</span></span>
1. <span data-ttu-id="18fc4-118">Sisestage väljale **Vaikeklient** kehtiv vaikeklient.</span><span class="sxs-lookup"><span data-stu-id="18fc4-118">In the **Default customer** field, provide a valid default customer.</span></span> <span data-ttu-id="18fc4-119">Neid andmeid kasutatakse uute kliendikirjete loomisel automaatseks asustamiseks vaikimisi.</span><span class="sxs-lookup"><span data-stu-id="18fc4-119">This data is used to assist in autopopulating defaults when new customer records are created.</span></span> <span data-ttu-id="18fc4-120">Kõnekeskuse tellimuste loomisel ei soovitata vaikekliendi jaoks tellimusi luua.</span><span class="sxs-lookup"><span data-stu-id="18fc4-120">When creating call center orders, it is not advisable to create orders for the default customer.</span></span>
1. <span data-ttu-id="18fc4-121">Sisestage väljale **Meiliteavituse profiil** kehtiv meiliteavituse profiil.</span><span class="sxs-lookup"><span data-stu-id="18fc4-121">In the **Email notification profile** field, provide a valid email notification profile.</span></span> <span data-ttu-id="18fc4-122">Kui kõnekeskuse tellimused on loodud ja töödeldud, kasutatakse e-posti teatise profiili, et vallandada automatiseeritud e-posti teatised klientidele teabega nende tellimuse oleku kohta.</span><span class="sxs-lookup"><span data-stu-id="18fc4-122">As call center orders are created and processed, the email notification profile is used to trigger automated email alerts to customers with information about their order status.</span></span>
1. <span data-ttu-id="18fc4-123">Esitage **Hinnaerandi** teabekood.</span><span class="sxs-lookup"><span data-stu-id="18fc4-123">Provide a **Price override** info code.</span></span> <span data-ttu-id="18fc4-124">Peate selleks esmalt looma teabekoodi.</span><span class="sxs-lookup"><span data-stu-id="18fc4-124">You may need to create an info code for this first.</span></span> <span data-ttu-id="18fc4-125">See teabekood moodustab põhjusetähiste hulga, millest kasutajal viibatakse valida, kui ta kasutab hinna tühistamise funktsionaalsust kõnekeskuse tellimusel.</span><span class="sxs-lookup"><span data-stu-id="18fc4-125">This info code provides the set of reason codes that the user will be prompted to choose from when using the price override functionality on a call center order.</span></span>
1. <span data-ttu-id="18fc4-126">Sisestage **Ootelepaneku koodi** teabekood.</span><span class="sxs-lookup"><span data-stu-id="18fc4-126">Provide a **Hold code** info code.</span></span> <span data-ttu-id="18fc4-127">Peate selleks esmalt looma teabekoodi.</span><span class="sxs-lookup"><span data-stu-id="18fc4-127">You may need to create an info code for this first.</span></span> <span data-ttu-id="18fc4-128">See teabekood moodustab valikulise põhjusetähiste hulga, millest kasutajal viibatakse valida, kui ta seab tellimuse ootele.</span><span class="sxs-lookup"><span data-stu-id="18fc4-128">This info code provides the set of optional reason codes that the user will be prompted to choose from when placing an order on hold.</span></span>
1. <span data-ttu-id="18fc4-129">Sisestage **Krediidi** teabekood.</span><span class="sxs-lookup"><span data-stu-id="18fc4-129">Provide a **Credit** info code.</span></span> <span data-ttu-id="18fc4-130">Peate selleks esmalt looma teabekoodi.</span><span class="sxs-lookup"><span data-stu-id="18fc4-130">You may need to create an info code for this first.</span></span> <span data-ttu-id="18fc4-131">See teabekood moodustab põhjusekoodide hulga, mille hulgast kasutaja saab valida, kui kasutab kõnekeskuse tellimuse kreeditfunktsiooni, et anda kliendile klienditeeninduse lisatagastusi.</span><span class="sxs-lookup"><span data-stu-id="18fc4-131">This info code provides the set of reason codes that the user can choose from when using the order credit functionality of call center to give misc refunds to the customer for customer service reasons.</span></span>
1. <span data-ttu-id="18fc4-132">Valikuline: finantsdimensioonide seadistus kiirvahekaardil **Finantsdimensioonid** .</span><span class="sxs-lookup"><span data-stu-id="18fc4-132">Optional: set up financial dimensions on the **Financial dimensions** FastTab.</span></span> <span data-ttu-id="18fc4-133">Siin sisestatud dimensioonid muutuvad vaikimisi säteteks selles kõnekeskuse kanalis loodud mistahes müügitellimusel.</span><span class="sxs-lookup"><span data-stu-id="18fc4-133">The dimensions entered here will default on any sales order created in this call center channel.</span></span>
1. <span data-ttu-id="18fc4-134">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="18fc4-134">Click **Save**.</span></span>

<span data-ttu-id="18fc4-135">Järgmine pilt näitab uue kõnekeskuse kanali loomist.</span><span class="sxs-lookup"><span data-stu-id="18fc4-135">The following image shows the creation of a new call center channel.</span></span>

![Uus kõnekeskuse kanal](media/channel-setup-callcenter-1.png)

<span data-ttu-id="18fc4-137">Järgmine pilt näitab kõnekeskuse kanali näidet.</span><span class="sxs-lookup"><span data-stu-id="18fc4-137">The following image shows an example call center channel.</span></span>

![Kõnekeskuse kanali näide](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="18fc4-139">Täiendava kanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="18fc4-139">Additional channel setup</span></span>

<span data-ttu-id="18fc4-140">Kõnekeskuse kanali häälestamiseks nõutavad täiendavad toimingud hõlmavad makseviiside ja tarneviiside seadistamist.</span><span class="sxs-lookup"><span data-stu-id="18fc4-140">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="18fc4-141">Järgmine pilt näitab seadistuste **Tarneviisid** ja **Makseviisid** suvandeid vahekaardil **Seadistus**.</span><span class="sxs-lookup"><span data-stu-id="18fc4-141">The following image shows **Modes of delivery** and **Payment methods** setup options on the **Set up** tab.</span></span>

![Täiendavad kõnekeskuse kanali seadistamise toimingud](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="18fc4-143">Seadistada maksemeetodid</span><span class="sxs-lookup"><span data-stu-id="18fc4-143">Set up payment methods</span></span>

<span data-ttu-id="18fc4-144">Kõigi selles kanalis toetatud maksetüüpide makseviiside seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="18fc4-144">To set up payment methods, follow these steps for each payment type supported on this channel.</span></span> <span data-ttu-id="18fc4-145">Kasutajad peavad valima eelnevalt määratletud makseviiside hulgast, et linkida need kõnekeskuse kanaliga.</span><span class="sxs-lookup"><span data-stu-id="18fc4-145">Users will be required to select from pre-defined payment methods to link them to the call center channel.</span></span> <span data-ttu-id="18fc4-146">Enne kõnekeskuse makseviiside seadistamist seadistage esmalt oma põhimakseviisid rakenduses **Jaemüük ja kaubandus \> Kanali seadistus \> Makseviisid \> Makseviisid**.</span><span class="sxs-lookup"><span data-stu-id="18fc4-146">Before setting up your call center payment methods, first set up your master methods of payment in **Retail and Commerce \> Channel setup \> Payment methods \> Payment methods**.</span></span>

1. <span data-ttu-id="18fc4-147">Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Makseviisid**.</span><span class="sxs-lookup"><span data-stu-id="18fc4-147">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="18fc4-148">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="18fc4-148">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="18fc4-149">Valige navigeerimispaanil makseviis, mis on saadaval saadaolevate eelnevalt määratletud maksete hulgast.</span><span class="sxs-lookup"><span data-stu-id="18fc4-149">In the navigation pane, select a payment method from the pre-defined payments available.</span></span>
1. <span data-ttu-id="18fc4-150">Konfigureerige kõik maksetüübi jaoks vajalikud lisasätted.</span><span class="sxs-lookup"><span data-stu-id="18fc4-150">Configure any additional settings as required for the payment type.</span></span> <span data-ttu-id="18fc4-151">Krediitkaartide, kinkekaartide või kliendikaardi korral on vajalik täiendav häälestus funktsiooni **Kaardi seaded** valimisega.</span><span class="sxs-lookup"><span data-stu-id="18fc4-151">For credit cards, gift cards, or loyalty cards, additional setup is required by selecting the **Card setup** function.</span></span> 
1. <span data-ttu-id="18fc4-152">Konfigureerige jaotises **Sisestus** maksetüübi õiged sisestuskontod.</span><span class="sxs-lookup"><span data-stu-id="18fc4-152">Configure proper posting accounts for the payment type in the **Posting** section.</span></span>
1. <span data-ttu-id="18fc4-153">Klõpsake toimingupaanil valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="18fc4-153">On the action pane, click **Save**.</span></span>

<span data-ttu-id="18fc4-154">Järgmine pilt näitab sularaha makseviisi näidet.</span><span class="sxs-lookup"><span data-stu-id="18fc4-154">The following image shows an example of a cash payment method.</span></span>

![Makseviiside näited](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="18fc4-156">Tarneviiside häälestamine</span><span class="sxs-lookup"><span data-stu-id="18fc4-156">Set up modes of delivery</span></span>

<span data-ttu-id="18fc4-157">Konfigureeritud tarneviise saate näha valides **Tarneviisid** vahekaardilt **Seadistus** **Tegevuspaani** alt.</span><span class="sxs-lookup"><span data-stu-id="18fc4-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="18fc4-158">Selleks, et muuta või lisada tarneviis, mis on seotud kõnekeskuse kanaliga, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="18fc4-158">To change or add a mode of delivery to be associated to the call center channel, follow these steps.</span></span>

1. <span data-ttu-id="18fc4-159">Valige tarnevormi kõnekeskuserežiimidest **Tarneviiside haldamine**</span><span class="sxs-lookup"><span data-stu-id="18fc4-159">From the Call center modes of delivery form, select **Manage modes of delivery**</span></span>
1. <span data-ttu-id="18fc4-160">Valige tegevuspaanilt **Uus**, et luua uus tarneviis, või valige olemasolev režiim.</span><span class="sxs-lookup"><span data-stu-id="18fc4-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="18fc4-161">Kõnekeskuse kanali lisamiseks valige jaotisest **Jaemüügikanalid** käsk **Lisa rida**.</span><span class="sxs-lookup"><span data-stu-id="18fc4-161">In the **Retail channels** section, click **Add line** to add the call center channel.</span></span> <span data-ttu-id="18fc4-162">Kanalite lisamine kasutades organisatsiooni sõlmpunkte, mitte iga kanalit ükshaaval lisades, täiustab kanalite lisamist veelgi.</span><span class="sxs-lookup"><span data-stu-id="18fc4-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>
1. <span data-ttu-id="18fc4-163">Veenduge, et tarneviis on konfigureeritud andmetega kiirvahekaardil **Tooted** ja kiirvahekaardil **Aadressid**.</span><span class="sxs-lookup"><span data-stu-id="18fc4-163">Ensure the mode of delivery has been configured with data on the **Products** FastTab and the **Addresses** FastTab.</span></span> <span data-ttu-id="18fc4-164">Kui tarneviisi puhul ei kehti ükski toode või tarneaadress, siis selle valimine tellimuse sisestamise ajal põhjustab tõrkeid.</span><span class="sxs-lookup"><span data-stu-id="18fc4-164">If no products or delivery addresses are valid for the mode of delivery, choosing it during order entry will result in errors.</span></span>
1. <span data-ttu-id="18fc4-165">Pärast seda, kui on tehtud muudatused kõnekeskuse tarneviisi konfiguratsioonides, tuleb käivitada ülesanne **Protsessi tarneviisid** , et aktiveerida muutuste maatriks.</span><span class="sxs-lookup"><span data-stu-id="18fc4-165">After any changes have been made to the call center mode of delivery configurations, the **Process delivery modes** job must be run to explode the change matrix.</span></span> <span data-ttu-id="18fc4-166">Selle ülesande leiate, kui navigeerite **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Protsessi tarneviisid**.</span><span class="sxs-lookup"><span data-stu-id="18fc4-166">This job can be found by navigating to **Retail and Commerce \> Retail and Commerce IT \> Process delivery modes**.</span></span>

<span data-ttu-id="18fc4-167">Järgmine pilt näitab tarneviisi näidet.</span><span class="sxs-lookup"><span data-stu-id="18fc4-167">The following image shows an example of a mode of delivery.</span></span>

![Tarneviiside häälestamine](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a><span data-ttu-id="18fc4-169">Kanali kasutajate seadistamine</span><span class="sxs-lookup"><span data-stu-id="18fc4-169">Set up channel users</span></span>

<span data-ttu-id="18fc4-170">Kui soovite luua müügitellimuse, mis on lingitud kõnekeskuse kanaliga Kaubanduse peakorterist, peab müügitellimuse loonud kasutaja olema lingitud kõnekeskuse kanaliga.</span><span class="sxs-lookup"><span data-stu-id="18fc4-170">To create a sales order that is linked to the call center channel from Commerce Headquarters, the user creating the sales order must be linked to the call center channel.</span></span> <span data-ttu-id="18fc4-171">Kasutaja ei saa kaubanduse peakorteris loodud müügitellimust kõnekeskuse kanaliga käsitsi linkida.</span><span class="sxs-lookup"><span data-stu-id="18fc4-171">The user cannot manually link a sales order created in Commerce Headquarters to the call center channel.</span></span> <span data-ttu-id="18fc4-172">Link on süstemaatiline ja põhineb kasutajal ja kasutaja suhtel kõnekeskuse kanaliga.</span><span class="sxs-lookup"><span data-stu-id="18fc4-172">The link is systematic, and is based on the user and the user's relationship to the call center channel.</span></span> <span data-ttu-id="18fc4-173">Kasutaja võib olla seotud ainult ühe kõnekeskuse kanaliga.</span><span class="sxs-lookup"><span data-stu-id="18fc4-173">A user may only be linked to one call center channel.</span></span>

1. <span data-ttu-id="18fc4-174">Valige toimingupaanil vahekaart **Kanal** ja seejärel **Kanalikasutajad**.</span><span class="sxs-lookup"><span data-stu-id="18fc4-174">On the action pane, select the **Channel** tab, and then select **Channel users**.</span></span>
1. <span data-ttu-id="18fc4-175">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="18fc4-175">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="18fc4-176">Valige ripploendi valikuloendist olemasolev **Kasutaja ID**, et linkida see kasutaja kõnekeskuse kanaliga</span><span class="sxs-lookup"><span data-stu-id="18fc4-176">Choose an existing **User ID** from the dropdown selection list to link this user to the call center channel</span></span>

<span data-ttu-id="18fc4-177">Pärast kanali kasutaja seadistust ja pärast kasutaja poolt uue müügitellimuse loomist kaubanduse peakorteris, lingitakse müügitellimus nendega seostatud kõnekeskuse kanaliga.</span><span class="sxs-lookup"><span data-stu-id="18fc4-177">After the channel user setup is done and the user creates a new sales order in Commerce Headquarters, the sales order will be linked to their associated call center channel.</span></span> <span data-ttu-id="18fc4-178">Selle kanali mis tahes konfiguratsioonid rakendatakse süstemaatiliselt müügitellimusele.</span><span class="sxs-lookup"><span data-stu-id="18fc4-178">Any configurations for this channel will be applied systematically to the sales order.</span></span> <span data-ttu-id="18fc4-179">Kasutaja saab kinnitada, millise kõnekeskuse kanaliga on müügitellimus lingitud, vaadates kanali nime viidet müügitellimuse päises.</span><span class="sxs-lookup"><span data-stu-id="18fc4-179">A user can confirm which call center channel the sales order is linked to by viewing the channel name reference on the sales order header.</span></span>


### <a name="set-up-price-groups"></a><span data-ttu-id="18fc4-180">Hinnagruppide häälestamine</span><span class="sxs-lookup"><span data-stu-id="18fc4-180">Set up price groups</span></span>

<span data-ttu-id="18fc4-181">Hinnarühmad on valikulised, kuid kui neid kasutatakse, saab kontrollida, milliseid müügihindu pakutakse klientidele, kes seavad tellimusi kõnekeskuse kanalis.</span><span class="sxs-lookup"><span data-stu-id="18fc4-181">Price groups are optional, but if used, can control which sales prices will be offered to customers placing orders in the call center channel.</span></span> <span data-ttu-id="18fc4-182">Kui hinnarühm pole kliendile konfigureeritud või kui kataloogi hinnarühmi ei rakendata müügitellimusele (kasutades kõnekeskuse tellimuse päise välja **Lähtekoodi ID** ), kasutatakse kauba otsimisel kanali hinnarühma.</span><span class="sxs-lookup"><span data-stu-id="18fc4-182">If a price group has not been configured for the customer, or if catalog price groups are not being applied to the sales order (using the **Source code ID** field on the call center order header), then the channel price group is used to locate item prices.</span></span> <span data-ttu-id="18fc4-183">Kui kõnekeskuse kanalis hinnarühma ei leita, kasutatakse vaikimisi kauba põhihindu.</span><span class="sxs-lookup"><span data-stu-id="18fc4-183">If a price group is not found on the call center channel, the default item master prices are used.</span></span> 

<span data-ttu-id="18fc4-184">Hinnarühma seadistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="18fc4-184">To set up a price group, do the following.</span></span>

1. <span data-ttu-id="18fc4-185">Valige toimingupaanil vahekaart **Kanal** ja seejärel **Hinnarühmad**.</span><span class="sxs-lookup"><span data-stu-id="18fc4-185">On the action pane, click the **Channel** tab, and then select **Price groups**.</span></span>
1. <span data-ttu-id="18fc4-186">Klõpsake toimingupaanil valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="18fc4-186">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="18fc4-187">Valige rippvalikuloendist **Jaemüügi hinnarühm** .</span><span class="sxs-lookup"><span data-stu-id="18fc4-187">Select a **Retail price group** from the dropdown selection list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18fc4-188">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="18fc4-188">Additional resources</span></span>

[<span data-ttu-id="18fc4-189">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="18fc4-189">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="18fc4-190">Kõnekeskuse müügifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="18fc4-190">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="18fc4-191">Kõnekeskuse tellimuse töötlemise suvandite seadistamine</span><span class="sxs-lookup"><span data-stu-id="18fc4-191">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="18fc4-192">Kõnekeskuse kataloogid</span><span class="sxs-lookup"><span data-stu-id="18fc4-192">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="18fc4-193">Pettuseteatiste seadistamine ja nendega töötamine</span><span class="sxs-lookup"><span data-stu-id="18fc4-193">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="18fc4-194">Kõnekeskuste järjepidevusprogrammide seadistamine</span><span class="sxs-lookup"><span data-stu-id="18fc4-194">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]