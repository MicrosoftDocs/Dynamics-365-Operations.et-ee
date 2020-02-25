---
title: Kõnekeskuse kanali seadistamine
description: Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus kõnekeskus.
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
ms.openlocfilehash: 6ec42ab920868f541eeac54556f4f24cb1efaa3a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002446"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="62e83-103">Kõnekeskuse kanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="62e83-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="62e83-104">Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus kõnekeskus.</span><span class="sxs-lookup"><span data-stu-id="62e83-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="62e83-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="62e83-105">Overview</span></span>

<span data-ttu-id="62e83-106">Rakenduse Dynamics 365 Commerce kõnekeskus on sellist tüüpi kanal, mille saab määratleda rakenduses.</span><span class="sxs-lookup"><span data-stu-id="62e83-106">In Dynamics 365 Commerce, a call center is a type of retail channel that can be defined in the application.</span></span> <span data-ttu-id="62e83-107">Kõnekeskuse üksustele kanali määratlemine võimaldab süsteemil siduda konkreetsed andmed ja tellimuse töötlemise vaikesätted müügitellimustega.</span><span class="sxs-lookup"><span data-stu-id="62e83-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="62e83-108">Ettevõte saab määratleda Commerce'is mitu kõnekeskuse kanalit.</span><span class="sxs-lookup"><span data-stu-id="62e83-108">A company can define multiple call center channels in Commerce.</span></span> 

<span data-ttu-id="62e83-109">Enne uue kõnekeskuse kanali loomist veenduge, et olete lõpuni viinud [Kanali eeltingimuste häälestamise](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="62e83-109">Before you create a new call center channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="62e83-110">Uue kõnekeskuse kanali loomine ja konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="62e83-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="62e83-111">Uue kõnekeskuse kanali loomiseks ja konfigureerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="62e83-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="62e83-112">Avage navigeerimispaanil **Moodulid \> Kanalid \> Kõnekeskused \> Kõik kõnekeskused**.</span><span class="sxs-lookup"><span data-stu-id="62e83-112">In the navigation pane, go to **Modules \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="62e83-113">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="62e83-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="62e83-114">Sisestage väljale **Nimi** uue kanali nimi.</span><span class="sxs-lookup"><span data-stu-id="62e83-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="62e83-115">Valige ripploendist sobiv **Juriidiline isik**.</span><span class="sxs-lookup"><span data-stu-id="62e83-115">Select the appropriate **Legal entity** from the drop down.</span></span>
1. <span data-ttu-id="62e83-116">Valige ripploendist sobiv **Lao** asukoht.</span><span class="sxs-lookup"><span data-stu-id="62e83-116">Select the appropriate **Warehouse** location from the drop down.</span></span>
1. <span data-ttu-id="62e83-117">Sisestage väljale **Vaikeklient** kehtiv vaikeklient.</span><span class="sxs-lookup"><span data-stu-id="62e83-117">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="62e83-118">Sisestage väljale **Meiliteavituse profiil** kehtiv meiliteavituse profiil.</span><span class="sxs-lookup"><span data-stu-id="62e83-118">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="62e83-119">Esitage **Hinnaerandi** teabekood.</span><span class="sxs-lookup"><span data-stu-id="62e83-119">Provide a **Price override** info code.</span></span> <span data-ttu-id="62e83-120">Pidage meeles, et peate selleks teabekoodi looma.</span><span class="sxs-lookup"><span data-stu-id="62e83-120">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="62e83-121">Sisestage **Ootelepaneku koodi** teabekood.</span><span class="sxs-lookup"><span data-stu-id="62e83-121">Provide a **Hold code** info code.</span></span> <span data-ttu-id="62e83-122">Pidage meeles, et peate selleks teabekoodi looma.</span><span class="sxs-lookup"><span data-stu-id="62e83-122">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="62e83-123">Sisestage **Krediidi** teabekood.</span><span class="sxs-lookup"><span data-stu-id="62e83-123">Provide a **Credit** info code.</span></span> <span data-ttu-id="62e83-124">Pidage meeles, et peate selleks teabekoodi looma.</span><span class="sxs-lookup"><span data-stu-id="62e83-124">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="62e83-125">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="62e83-125">Select **Save**.</span></span>

<span data-ttu-id="62e83-126">Järgmine pilt näitab uue kõnekeskuse kanali loomist.</span><span class="sxs-lookup"><span data-stu-id="62e83-126">The following image shows the creation of a new call center channel.</span></span>

![Uus kõnekeskuse kanal](media/channel-setup-callcenter-1.png)

<span data-ttu-id="62e83-128">Järgmine pilt näitab kõnekeskuse kanali näidet.</span><span class="sxs-lookup"><span data-stu-id="62e83-128">The following image shows an example call center channel.</span></span>

![Kõnekeskuse kanali näide](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="62e83-130">Täiendava kanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="62e83-130">Additional channel setup</span></span>

<span data-ttu-id="62e83-131">Kõnekeskuse kanali häälestamiseks nõutavad täiendavad toimingud hõlmavad makseviiside ja tarneviiside seadistamist.</span><span class="sxs-lookup"><span data-stu-id="62e83-131">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="62e83-132">Järgmine pilt näitab seadistuste **Tarneviisid** ja **Makseviisid** suvandeid vahekaardil **Seadistus**.</span><span class="sxs-lookup"><span data-stu-id="62e83-132">The following image shows **Modes of delivery** and **Payment methods** set up options on the **Set up** tab.</span></span>

![Täiendavad kõnekeskuse kanali seadistamise toimingud](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="62e83-134">Seadistada maksemeetodid</span><span class="sxs-lookup"><span data-stu-id="62e83-134">Set up payment methods</span></span>

<span data-ttu-id="62e83-135">Kõigi selles kanalis toetatud maksetüübi makseviiside seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="62e83-135">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="62e83-136">Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Makseviisid**.</span><span class="sxs-lookup"><span data-stu-id="62e83-136">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="62e83-137">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="62e83-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="62e83-138">Valige navigeerimispaanil soovitud makseviis.</span><span class="sxs-lookup"><span data-stu-id="62e83-138">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="62e83-139">Sisestage jaotises **Üldine** **Toimingu nimi** ja konfigureerige muud soovitud sätted.</span><span class="sxs-lookup"><span data-stu-id="62e83-139">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="62e83-140">Konfigureerige kõik maksetüübi jaoks vajalikud lisasätted.</span><span class="sxs-lookup"><span data-stu-id="62e83-140">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="62e83-141">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="62e83-141">On the action pane, select **Save**.</span></span>

<span data-ttu-id="62e83-142">Järgmine pilt näitab sularaha makseviisi näidet.</span><span class="sxs-lookup"><span data-stu-id="62e83-142">The following image shows an example of a cash payment method.</span></span>

![Makseviiside näited](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="62e83-144">Tarneviiside häälestamine</span><span class="sxs-lookup"><span data-stu-id="62e83-144">Set up modes of delivery</span></span>

<span data-ttu-id="62e83-145">Konfigureeritud tarneviise saate näha valides **Tarneviisid** vahekaardilt **Seadistus** **Tegevuspaani** alt.</span><span class="sxs-lookup"><span data-stu-id="62e83-145">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="62e83-146">Tarneviisi muutmiseks või lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="62e83-146">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="62e83-147">Avage navigeerimispaanil **Moodulid \> Varude haldus \> Tarneviisid**.</span><span class="sxs-lookup"><span data-stu-id="62e83-147">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="62e83-148">Valige tegevuspaanilt **Uus**, et luua uus tarneviis, või valige olemasolev režiim.</span><span class="sxs-lookup"><span data-stu-id="62e83-148">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="62e83-149">Kanali lisamiseks valige jaotisest **Jaemüügikanalid** käsk **Lisa rida**.</span><span class="sxs-lookup"><span data-stu-id="62e83-149">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="62e83-150">Kanalite lisamine kasutades organisatsiooni sõlmpunkte, mitte iga kanalit ükshaaval lisades, täiustab kanalite lisamist veelgi.</span><span class="sxs-lookup"><span data-stu-id="62e83-150">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="62e83-151">Järgmine pilt näitab tarneviisi näidet.</span><span class="sxs-lookup"><span data-stu-id="62e83-151">The following image shows an example of a mode of delivery.</span></span>

![Tarneviiside häälestamine](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a><span data-ttu-id="62e83-153">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="62e83-153">Additional resources</span></span>

[<span data-ttu-id="62e83-154">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="62e83-154">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="62e83-155">Kõnekeskuse müügifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="62e83-155">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="62e83-156">Kõnekeskuse tellimuse töötlemise suvandite seadistamine</span><span class="sxs-lookup"><span data-stu-id="62e83-156">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="62e83-157">Kõnekeskuse kataloogid</span><span class="sxs-lookup"><span data-stu-id="62e83-157">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="62e83-158">Pettuseteatiste seadistamine ja nendega töötamine</span><span class="sxs-lookup"><span data-stu-id="62e83-158">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="62e83-159">Kõnekeskuste järjepidevusprogrammide seadistamine</span><span class="sxs-lookup"><span data-stu-id="62e83-159">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
