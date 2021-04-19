---
title: Võrgukanali häälestamine
description: Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus veebikanal.
author: samjarawan
ms.date: 07/02/2020
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
ms.openlocfilehash: b6bf158361f95b6551b29f195616cf21f908b802
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800635"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="daf39-103">Võrgukanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="daf39-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="daf39-104">Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus veebikanal.</span><span class="sxs-lookup"><span data-stu-id="daf39-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="daf39-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="daf39-105">Overview</span></span>

<span data-ttu-id="daf39-106">Dynamics 365 Commerce toetab mitut jaemüügikanalit.</span><span class="sxs-lookup"><span data-stu-id="daf39-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="daf39-107">Jaemüügikanalid hõlmavad võrgupoode, kõnekeskusi ja jaekauplusi (neid nimetatakse ka füüsilisteks kauplusteks).</span><span class="sxs-lookup"><span data-stu-id="daf39-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="daf39-108">Võrgupoed annavad kliendile võimaluse osta tooteid lisaks oma jaekauplustele ka jaemüüja veebipoest.</span><span class="sxs-lookup"><span data-stu-id="daf39-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="daf39-109">Commerce'is veebipoe loomiseks peate esmalt looma võrgukanali.</span><span class="sxs-lookup"><span data-stu-id="daf39-109">To create an online store in Commerce, you must first create an online channel.</span></span> <span data-ttu-id="daf39-110">Enne uue võrgukanali loomist veenduge, et olete lõpuni viinud [Kanali eeltingimuste häälestamise](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="daf39-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

<span data-ttu-id="daf39-111">Enne uue saidi loomist peab olema rakenduses Commerce loodud vähemalt üks veebipood.</span><span class="sxs-lookup"><span data-stu-id="daf39-111">Before you can create a new site, at least one online store must be created in Commerce.</span></span> <span data-ttu-id="daf39-112">Lisateavet leiate teemast [E-kaubanduse saidi loomine](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="daf39-112">For more information, see [Create an e-Commerce site](create-ecommerce-site.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="daf39-113">Uue võrgukanali loomine ja konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="daf39-113">Create and configure a new online channel</span></span>

<span data-ttu-id="daf39-114">Uue võrgukanali loomiseks ja konfigureerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="daf39-114">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="daf39-115">Avage navigatsioonipaneelil **Moodulid \> Kanalid \> Veebipoed**.</span><span class="sxs-lookup"><span data-stu-id="daf39-115">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="daf39-116">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="daf39-116">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="daf39-117">Sisestage väljale **Nimi** uue kanali nimi.</span><span class="sxs-lookup"><span data-stu-id="daf39-117">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="daf39-118">Sisestage ripploendisse **Juriidiline isik** sobiv juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="daf39-118">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="daf39-119">Sisestage ripploendisse **Ladu** sobiv ladu.</span><span class="sxs-lookup"><span data-stu-id="daf39-119">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="daf39-120">Valige sobiv ajavöönd väljal **Kaupluse ajavöönd**.</span><span class="sxs-lookup"><span data-stu-id="daf39-120">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="daf39-121">Valige väljal **Valuuta** sobiv valuuta.</span><span class="sxs-lookup"><span data-stu-id="daf39-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="daf39-122">Sisestage väljale **Vaikeklient** kehtiv vaikeklient.</span><span class="sxs-lookup"><span data-stu-id="daf39-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="daf39-123">Sisestage väljale **Kliendi aadressiraamat** kehtiv aadressiraamat.</span><span class="sxs-lookup"><span data-stu-id="daf39-123">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="daf39-124">Valige väljal **Funktsiooniprofiil** funktsiooniprofiil, kui see on kohaldatav.</span><span class="sxs-lookup"><span data-stu-id="daf39-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="daf39-125">Sisestage väljale **Meiliteavituse profiil** kehtiv meiliteavituse profiil.</span><span class="sxs-lookup"><span data-stu-id="daf39-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="daf39-126">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="daf39-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="daf39-127">Järgmine pilt näitab uue võrgukanali loomist.</span><span class="sxs-lookup"><span data-stu-id="daf39-127">The following image shows the creation of a new online channel.</span></span>

![Uus võrgukanal](media/channel-setup-online-1.png)

<span data-ttu-id="daf39-129">Järgmine pilt näitab võrgukanali näidet.</span><span class="sxs-lookup"><span data-stu-id="daf39-129">The following image shows an example online channel.</span></span>

![Võrgukanali näide](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="daf39-131">Keelte seadistamine</span><span class="sxs-lookup"><span data-stu-id="daf39-131">Set up languages</span></span>

<span data-ttu-id="daf39-132">Kui teie e-kaubanduse sait toetab mitut keelt, laiendage jaotist **Keeled** ja lisage vajadusel täiendavaid keeli.</span><span class="sxs-lookup"><span data-stu-id="daf39-132">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="daf39-133">Maksekonto seadistamine</span><span class="sxs-lookup"><span data-stu-id="daf39-133">Set up payment account</span></span>

<span data-ttu-id="daf39-134">Jaotisest **Maksekonto** saate lisada kolmanda osapoole maksepakkuja.</span><span class="sxs-lookup"><span data-stu-id="daf39-134">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="daf39-135">Lisateavet Adyeni maksekonnektori seadistamise kohta vt teemast [Dynamics 365 maksekonnektor Adyeni jaoks](../retail/dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="daf39-135">For information on setting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-setup"></a><span data-ttu-id="daf39-136">Täiendava kanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="daf39-136">Additional channel setup</span></span>

<span data-ttu-id="daf39-137">Veebikanali häälestamiseks nõutavad täiendavad toimingud hõlmavad makseviiside, tarneviiside ja täitmisgrupi määramist.</span><span class="sxs-lookup"><span data-stu-id="daf39-137">Additional tasks that are required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="daf39-138">Järgmine pilt näitab seadistuste **Tarneviisid**, **Makseviisid** ja **Täitmisgurpi määramine** suvandeid vahekaardil **Seadistus**.</span><span class="sxs-lookup"><span data-stu-id="daf39-138">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![Täiendavad võrgukanali seadistamise toimingud](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="daf39-140">Seadistada maksemeetodid</span><span class="sxs-lookup"><span data-stu-id="daf39-140">Set up payment methods</span></span>

<span data-ttu-id="daf39-141">Kõigi selles kanalis toetatud maksetüübi makseviiside seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="daf39-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="daf39-142">Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Makseviisid**.</span><span class="sxs-lookup"><span data-stu-id="daf39-142">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="daf39-143">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="daf39-143">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="daf39-144">Valige navigeerimispaanil soovitud makseviis.</span><span class="sxs-lookup"><span data-stu-id="daf39-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="daf39-145">Sisestage jaotises **Üldine** **Toimingu nimi** ja konfigureerige muud soovitud sätted.</span><span class="sxs-lookup"><span data-stu-id="daf39-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="daf39-146">Konfigureerige kõik maksetüübi jaoks vajalikud lisasätted.</span><span class="sxs-lookup"><span data-stu-id="daf39-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="daf39-147">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="daf39-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="daf39-148">Järgmine pilt näitab sularaha makseviisi näidet.</span><span class="sxs-lookup"><span data-stu-id="daf39-148">The following image shows an example of a cash payment method.</span></span>

![Makseviiside näited](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="daf39-150">Tarneviiside häälestamine</span><span class="sxs-lookup"><span data-stu-id="daf39-150">Set up modes of delivery</span></span>

<span data-ttu-id="daf39-151">Konfigureeritud tarneviise saate näha valides **Tarneviisid** vahekaardilt **Seadistus** **Tegevuspaani** alt.</span><span class="sxs-lookup"><span data-stu-id="daf39-151">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="daf39-152">Tarneviisi muutmiseks või lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="daf39-152">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="daf39-153">Avage navigeerimispaanil **Moodulid \> Varude haldus \> Tarneviisid**.</span><span class="sxs-lookup"><span data-stu-id="daf39-153">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="daf39-154">Valige tegevuspaanilt **Uus**, et luua uus tarneviis, või valige olemasolev režiim.</span><span class="sxs-lookup"><span data-stu-id="daf39-154">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="daf39-155">Kanali lisamiseks valige jaotisest **Jaemüügikanalid** käsk **Lisa rida**.</span><span class="sxs-lookup"><span data-stu-id="daf39-155">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="daf39-156">Kanalite lisamine kasutades organisatsiooni sõlmpunkte, mitte iga kanalit ükshaaval lisades, täiustab kanalite lisamist veelgi.</span><span class="sxs-lookup"><span data-stu-id="daf39-156">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="daf39-157">Järgmine pilt näitab tarneviisi näidet.</span><span class="sxs-lookup"><span data-stu-id="daf39-157">The following image shows an example of a mode of delivery.</span></span>

![Tarneviiside häälestamine](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="daf39-159">Täitmisgrupi määramise seadistamine</span><span class="sxs-lookup"><span data-stu-id="daf39-159">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="daf39-160">Täitmisgrupi määramise seadistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="daf39-160">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="daf39-161">Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Täitmisgrupi määramine**.</span><span class="sxs-lookup"><span data-stu-id="daf39-161">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="daf39-162">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="daf39-162">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="daf39-163">Valige täitmisgrupp ripploendist **Täitmisgrupp**.</span><span class="sxs-lookup"><span data-stu-id="daf39-163">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="daf39-164">Sisestage kirjeldus ripploendisse **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="daf39-164">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="daf39-165">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="daf39-165">On the action pane, select **Save**.</span></span>

<span data-ttu-id="daf39-166">Järgmine pilt näitab täitmisgrupi määramise seadistuse näidet.</span><span class="sxs-lookup"><span data-stu-id="daf39-166">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Täitmisgrupi määramiste seadistamine](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="daf39-168">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="daf39-168">Additional resources</span></span>

[<span data-ttu-id="daf39-169">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="daf39-169">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="daf39-170">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="daf39-170">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="daf39-171">Jaemüügikanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="daf39-171">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="daf39-172">Kõnekeskuse kanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="daf39-172">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="daf39-173">Dynamics 365 maksekonnektor Adyeni jaoks</span><span class="sxs-lookup"><span data-stu-id="daf39-173">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]