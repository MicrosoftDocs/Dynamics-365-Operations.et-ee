---
title: Veebikanali häälestamine
description: Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus veebikanal.
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
ms.openlocfilehash: 9b7a2b8fd157df8b39e9e227d188a3802cacb4e3
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002423"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="adbb9-103">Veebikanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="adbb9-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="adbb9-104">Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus veebikanal.</span><span class="sxs-lookup"><span data-stu-id="adbb9-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="adbb9-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="adbb9-105">Overview</span></span>

<span data-ttu-id="adbb9-106">Dynamics 365 Commerce toetab mitut jaemüügikanalit.</span><span class="sxs-lookup"><span data-stu-id="adbb9-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="adbb9-107">Jaemüügikanalid hõlmavad võrgupoode, kõnekeskusi ja jaekauplusi (neid nimetatakse ka füüsilisteks kauplusteks).</span><span class="sxs-lookup"><span data-stu-id="adbb9-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="adbb9-108">Võrgupoed annavad kliendile võimaluse osta tooteid lisaks oma jaekauplustele ka jaemüüja veebipoest.</span><span class="sxs-lookup"><span data-stu-id="adbb9-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="adbb9-109">Commerce'is veebipoe loomiseks peate esmalt looma võrgukanali.</span><span class="sxs-lookup"><span data-stu-id="adbb9-109">To create an online store in Commerce, you must first create an online channel.</span></span> 

<span data-ttu-id="adbb9-110">Enne uue võrgukanali loomist veenduge, et olete lõpuni viinud [Kanali eeltingimuste häälestamise](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="adbb9-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="adbb9-111">Uue võrgukanali loomine ja konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="adbb9-111">Create and configure a new online channel</span></span>

<span data-ttu-id="adbb9-112">Uue võrgukanali loomiseks ja konfigureerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="adbb9-112">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="adbb9-113">Avage navigatsioonipaneelil **Moodulid \> Kanalid \> Veebipoed**.</span><span class="sxs-lookup"><span data-stu-id="adbb9-113">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="adbb9-114">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="adbb9-114">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="adbb9-115">Sisestage väljale **Nimi** uue kanali nimi.</span><span class="sxs-lookup"><span data-stu-id="adbb9-115">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="adbb9-116">Sisestage ripploendisse **Juriidiline isik** sobiv juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="adbb9-116">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="adbb9-117">Sisestage ripploendisse **Ladu** sobiv ladu.</span><span class="sxs-lookup"><span data-stu-id="adbb9-117">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="adbb9-118">Valige sobiv ajavöönd väljal **Kaupluse ajavöönd**.</span><span class="sxs-lookup"><span data-stu-id="adbb9-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="adbb9-119">Valige väljal **Valuuta** sobiv valuuta.</span><span class="sxs-lookup"><span data-stu-id="adbb9-119">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="adbb9-120">Sisestage väljale **Vaikeklient** kehtiv vaikeklient.</span><span class="sxs-lookup"><span data-stu-id="adbb9-120">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="adbb9-121">Sisestage väljale **Kliendi aadressiraamat** kehtiv aadressiraamat.</span><span class="sxs-lookup"><span data-stu-id="adbb9-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="adbb9-122">Valige väljal **Funktsiooniprofiil** funktsiooniprofiil, kui see on kohaldatav.</span><span class="sxs-lookup"><span data-stu-id="adbb9-122">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="adbb9-123">Sisestage väljale **Meiliteavituse profiil** kehtiv meiliteavituse profiil.</span><span class="sxs-lookup"><span data-stu-id="adbb9-123">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="adbb9-124">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="adbb9-124">On the action pane, select **Save**.</span></span>

<span data-ttu-id="adbb9-125">Järgmine pilt näitab uue võrgukanali loomist.</span><span class="sxs-lookup"><span data-stu-id="adbb9-125">The following image shows the creation of a new online channel.</span></span>

![Uus võrgukanal](media/channel-setup-online-1.png)

<span data-ttu-id="adbb9-127">Järgmine pilt näitab võrgukanali näidet.</span><span class="sxs-lookup"><span data-stu-id="adbb9-127">The following image shows an example online channel.</span></span>

![Võrgukanali näide](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="adbb9-129">Keelte seadistamine</span><span class="sxs-lookup"><span data-stu-id="adbb9-129">Set up languages</span></span>

<span data-ttu-id="adbb9-130">Kui teie e-kaubanduse sait toetab mitut keelt, laiendage jaotist **Keeled** ja lisage vajadusel täiendavaid keeli.</span><span class="sxs-lookup"><span data-stu-id="adbb9-130">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="adbb9-131">Maksekonto seadistamine</span><span class="sxs-lookup"><span data-stu-id="adbb9-131">Set up payment account</span></span>

<span data-ttu-id="adbb9-132">Jaotisest **Maksekonto** saate lisada kolmanda osapoole maksepakkuja.</span><span class="sxs-lookup"><span data-stu-id="adbb9-132">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="adbb9-133">Lisateavet Adyen maksekonnektori seadistamise kohta vt teemast [Dynamics 365 maksekonnektor Adyeni jaoks](../retail/dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="adbb9-133">For information on settting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-set-up"></a><span data-ttu-id="adbb9-134">Täiendava kanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="adbb9-134">Additional channel set up</span></span>

<span data-ttu-id="adbb9-135">Veebikanali häälestamiseks nõutavad täiendavad toimingud hõlmavad makseviiside, tarneviiside ja täitmisgrupi määramist.</span><span class="sxs-lookup"><span data-stu-id="adbb9-135">Additional tasks required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="adbb9-136">Järgmine pilt näitab seadistuste **Tarneviisid**, **Makseviisid** ja **Täitmisgurpi määramine** suvandeid vahekaardil **Seadistus**.</span><span class="sxs-lookup"><span data-stu-id="adbb9-136">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![Täiendavad võrgukanali seadistamise toimingud](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="adbb9-138">Seadistada maksemeetodid</span><span class="sxs-lookup"><span data-stu-id="adbb9-138">Set up payment methods</span></span>

<span data-ttu-id="adbb9-139">Kõigi selles kanalis toetatud maksetüübi makseviiside seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="adbb9-139">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="adbb9-140">Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Makseviisid**.</span><span class="sxs-lookup"><span data-stu-id="adbb9-140">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="adbb9-141">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="adbb9-141">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="adbb9-142">Valige navigeerimispaanil soovitud makseviis.</span><span class="sxs-lookup"><span data-stu-id="adbb9-142">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="adbb9-143">Sisestage jaotises **Üldine** **Toimingu nimi** ja konfigureerige muud soovitud sätted.</span><span class="sxs-lookup"><span data-stu-id="adbb9-143">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="adbb9-144">Konfigureerige kõik maksetüübi jaoks vajalikud lisasätted.</span><span class="sxs-lookup"><span data-stu-id="adbb9-144">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="adbb9-145">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="adbb9-145">On the action pane, select **Save**.</span></span>

<span data-ttu-id="adbb9-146">Järgmine pilt näitab sularaha makseviisi näidet.</span><span class="sxs-lookup"><span data-stu-id="adbb9-146">The following image shows an example of a cash payment method.</span></span>

![Makseviiside näited](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="adbb9-148">Tarneviiside häälestamine</span><span class="sxs-lookup"><span data-stu-id="adbb9-148">Set up modes of delivery</span></span>

<span data-ttu-id="adbb9-149">Konfigureeritud tarneviise saate näha valides **Tarneviisid** vahekaardilt **Seadistus** **Tegevuspaani** alt.</span><span class="sxs-lookup"><span data-stu-id="adbb9-149">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="adbb9-150">Tarneviisi muutmiseks või lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="adbb9-150">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="adbb9-151">Avage navigeerimispaanil **Moodulid \> Varude haldus \> Tarneviisid**.</span><span class="sxs-lookup"><span data-stu-id="adbb9-151">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="adbb9-152">Valige tegevuspaanilt **Uus**, et luua uus tarneviis, või valige olemasolev režiim.</span><span class="sxs-lookup"><span data-stu-id="adbb9-152">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="adbb9-153">Kanali lisamiseks valige jaotisest **Jaemüügikanalid** käsk **Lisa rida**.</span><span class="sxs-lookup"><span data-stu-id="adbb9-153">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="adbb9-154">Kanalite lisamine kasutades organisatsiooni sõlmpunkte, mitte iga kanalit ükshaaval lisades, täiustab kanalite lisamist veelgi.</span><span class="sxs-lookup"><span data-stu-id="adbb9-154">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="adbb9-155">Järgmine pilt näitab tarneviisi näidet.</span><span class="sxs-lookup"><span data-stu-id="adbb9-155">The following image shows an example of a mode of delivery.</span></span>

![Tarneviiside häälestamine](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="adbb9-157">Täitmisgrupi määramise seadistamine</span><span class="sxs-lookup"><span data-stu-id="adbb9-157">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="adbb9-158">Täitmisgrupi määramise seadistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="adbb9-158">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="adbb9-159">Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Täitmisgrupi määramine**.</span><span class="sxs-lookup"><span data-stu-id="adbb9-159">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="adbb9-160">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="adbb9-160">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="adbb9-161">Valige täitmisgrupp ripploendist **Täitmisgrupp**.</span><span class="sxs-lookup"><span data-stu-id="adbb9-161">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="adbb9-162">Sisestage kirjeldus ripploendisse **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="adbb9-162">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="adbb9-163">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="adbb9-163">On the action pane, select **Save**.</span></span>

<span data-ttu-id="adbb9-164">Järgmine pilt näitab täitmisgrupi määramise seadistuse näidet.</span><span class="sxs-lookup"><span data-stu-id="adbb9-164">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Täitmisgrupi määramiste seadistamine](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="adbb9-166">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="adbb9-166">Additional resources</span></span>

[<span data-ttu-id="adbb9-167">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="adbb9-167">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="adbb9-168">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="adbb9-168">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="adbb9-169">Jaemüügikanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="adbb9-169">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="adbb9-170">Kõnekeskuse kanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="adbb9-170">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="adbb9-171">Dynamics 365 maksekonnektor Adyeni jaoks</span><span class="sxs-lookup"><span data-stu-id="adbb9-171">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)
