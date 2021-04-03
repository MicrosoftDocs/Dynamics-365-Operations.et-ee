---
title: Vaikekliendi loomine
description: See teema kirjeldab, kuidas luua vaikeklienti, mida Microsoft Dynamics 365 Commerce' kanali loomisel kasutada.
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
ms.openlocfilehash: f988732549ce82919f02c87b320623d8d4218735
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477896"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="e9bdf-103">Vaikekliendi loomine</span><span class="sxs-lookup"><span data-stu-id="e9bdf-103">Create a default customer</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e9bdf-104">See teema kirjeldab, kuidas luua vaikeklienti, mida Microsoft Dynamics 365 Commerce' kanali loomisel kasutada.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e9bdf-105">Kanali loomisel peate sisestama vaikekliendi.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-105">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="e9bdf-106">Vaikeklienti on lihtne luua pärast kliendigrupi ja kliendi aadressiraamatu loomist.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-106">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="e9bdf-107">Kliendigrupi loomine</span><span class="sxs-lookup"><span data-stu-id="e9bdf-107">Create a customer group</span></span>

<span data-ttu-id="e9bdf-108">Kui ühtegi kliendigruppi pole veel olemas, saate selle luua.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-108">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="e9bdf-109">Näiteks võib tuua erinevaid kliendigruppe esindavad grupid, nagu näiteks hulgimüük, jaemüük, internet, töötajad, jne.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-109">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="e9bdf-110">Kliendigrupi loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-110">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="e9bdf-111">Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Kliendid \> Kliendigrupid**.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-111">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="e9bdf-112">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="e9bdf-113">Sisestage väljale **Kliendigrupp** kliendigrupi ID.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-113">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="e9bdf-114">Sisestage väljale **Kirjeldus** sobiv kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-114">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="e9bdf-115">Sisestage väljale **Maksetingimused** sobiv väärtus.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-115">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="e9bdf-116">Sisestage väljale **Aeg arve tähtaja ja maksekuupäeva vahel** sobiv väärtus.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-116">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="e9bdf-117">Sisestage väljale **Vaikemaksugrupp** maksugrupp, kui see on kohaldatav.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-117">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="e9bdf-118">Valige märkeruut **Hinnad sisaldavad käibemaksu**, kui see on kohaldatav.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-118">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="e9bdf-119">Sisestage väljale **Vaikimisi mahakandmise põhjus** sobiv väärtus, kui see on kohaldatav.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-119">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="e9bdf-120">Järgmine pilt näitab mitmeid konfigureeritud kliendigruppe.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-120">The following image shows several configured customer groups.</span></span>

![Kliendigrupid](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="e9bdf-122">Kliendi aadressiraamatu loomine</span><span class="sxs-lookup"><span data-stu-id="e9bdf-122">Create a customer address book</span></span>

<span data-ttu-id="e9bdf-123">Klient peab olema aadressiraamatuga seotud.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-123">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="e9bdf-124">Kui seda pole veel loodud, peate selle looma.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-124">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="e9bdf-125">Kliendi aadressiraamatu loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-125">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="e9bdf-126">Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Aadressiraamatud**.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-126">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="e9bdf-127">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-127">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="e9bdf-128">Sisestage nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-128">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="e9bdf-129">Sisestage kirjeldus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-129">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="e9bdf-130">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-130">On the action pane, select **Save**.</span></span>

<span data-ttu-id="e9bdf-131">Järgmine pilt näitab aadressiraamatu näidet.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-131">The following image shows an example address book.</span></span>

![Aadressiraamat](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="e9bdf-133">Vaikekliendi loomine</span><span class="sxs-lookup"><span data-stu-id="e9bdf-133">Create a default customer</span></span>

<span data-ttu-id="e9bdf-134">Vaikekliendi loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-134">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="e9bdf-135">Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Kliendid \> Kõik kliendid**.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-135">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="e9bdf-136">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="e9bdf-137">Valige ripploendist **Tüüp** valik "Isik".</span><span class="sxs-lookup"><span data-stu-id="e9bdf-137">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="e9bdf-138">Valige ripploendist **Kliendi konto** või sisestage sinna kontonumber (näiteks "100001").</span><span class="sxs-lookup"><span data-stu-id="e9bdf-138">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="e9bdf-139">Valige ripploendist **Eesnimi** nimi või sisestage see (näiteks "Vaikimisi").</span><span class="sxs-lookup"><span data-stu-id="e9bdf-139">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="e9bdf-140">Valige ripploendist **Teine eesnimi**, või sisestage see (näiteks "Jaemüük").</span><span class="sxs-lookup"><span data-stu-id="e9bdf-140">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="e9bdf-141">Valige ripploendist **Perekonnanimi** nimi, või sisestage see (näiteks "Klient").</span><span class="sxs-lookup"><span data-stu-id="e9bdf-141">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="e9bdf-142">Valige või sisestage ripploendisse **Valuuta** valuuta (näiteks "USD").</span><span class="sxs-lookup"><span data-stu-id="e9bdf-142">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="e9bdf-143">Valige ripploendist **Valuuta** eelnevalt loodud kliendigrupp.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-143">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="e9bdf-144">Valige ripploendist **Aadressiraamatud** olemasolev kliendi aadressiraamat.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-144">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="e9bdf-145">Valige **Salvesta**, et salvestada ja naasta kliendi üksikasjade ekraanile uue kliendi jaoks.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-145">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="e9bdf-146">Vaikekliendile ei ole vaja aadressi lisada.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-146">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="e9bdf-147">Järgmine pilt näitab kliendi loomise näidet.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-147">The following image shows an example of customer creation.</span></span>

![Vaikekliendi loomine](media/default-customer-creation.png)

<span data-ttu-id="e9bdf-149">Järgmine pilt näitab vaikekliendi konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-149">The following image shows a default customer configuration.</span></span>

![Kliendi konfiguratsiooni näide](media/default-customer-configuration1.png)

<span data-ttu-id="e9bdf-151">Enamik kliendiandmete kuva vaikeväärtusi võib jääda, kuid muuta tuleb kaht väärtust.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-151">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="e9bdf-152">Laiendage kliendiandmete kuval jaotist **Müügitellimuse vaikesätteid**.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-152">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="e9bdf-153">Valige või sisestage ripploendis **Sait** eelkonfigureeritud sait.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-153">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="e9bdf-154">Valige või sisestage ripploendis **Ladu** eelkonfigureeritud ladu.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-154">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="e9bdf-155">Järgmine pilt näitab kliendi konfiguratsiooni näidet.</span><span class="sxs-lookup"><span data-stu-id="e9bdf-155">The following image shows an example customer configuration.</span></span>

![Kliendi konfiguratsiooni näide](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="e9bdf-157">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e9bdf-157">Additional resources</span></span>

[<span data-ttu-id="e9bdf-158">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="e9bdf-158">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="e9bdf-159">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="e9bdf-159">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
