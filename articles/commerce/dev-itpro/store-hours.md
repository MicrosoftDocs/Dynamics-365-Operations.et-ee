---
title: Kaupluse lahtiolekuaegade loomine ja värskendamine
description: See teema kirjeldab kaupluse lahtiolekuaegade loomist ja värskendamist Commerce Headquartersis.
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 4706432234437d2dc7943fb194cd01004ab7e6b7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687507"
---
# <a name="create-and-update-store-hours"></a><span data-ttu-id="461d1-103">Kaupluse lahtiolekuaegade loomine ja värskendamine</span><span class="sxs-lookup"><span data-stu-id="461d1-103">Create and update store hours</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="461d1-104">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="461d1-104">Overview</span></span>

<span data-ttu-id="461d1-105">Ühest asukohast saavad jaemüüjad luua, hooldada ja hallata erinevate kaupluste lahtiolekuaegu geograafiliste piirkondade lõikes.</span><span class="sxs-lookup"><span data-stu-id="461d1-105">From a single place, retailers can create, maintain, and manage the store hours for different stores across geographic regions.</span></span> <span data-ttu-id="461d1-106">Kaupluse lahtiolekuajad saab seejärel kuvada müügikoha (POS) terminalis.</span><span class="sxs-lookup"><span data-stu-id="461d1-106">The store hours can then be shown on point of sale (POS) terminals.</span></span> <span data-ttu-id="461d1-107">Sel viisil saavad kassapidajad klientidega jagada kaupluse lahtiolekuaegu ja paremini aidata ostjaid, kes on teistest kaupluste varudest huvitatud.</span><span class="sxs-lookup"><span data-stu-id="461d1-107">In this way, cashiers can share store hours with customers and better help shoppers who are interested in inventory in other stores.</span></span> <span data-ttu-id="461d1-108">Kaupluse lahtiolekuajad saab printida ka tšekkidele, kui kliendid soovivad hiljem kauplusse naasta.</span><span class="sxs-lookup"><span data-stu-id="461d1-108">The store hours can also be printed on receipts, in case customers want to return to the store later.</span></span>

<span data-ttu-id="461d1-109">Erinevate kanalite vahel saab konfigureerida mitu lahtiolekuaega.</span><span class="sxs-lookup"><span data-stu-id="461d1-109">Multiple store hours can be configured across different channels.</span></span> <span data-ttu-id="461d1-110">Need kanalid hõlmavad tellis-ja mördi kauplusi, kõnekeskusi, mobiiliseadmeid ja e-kaubanduse saite.</span><span class="sxs-lookup"><span data-stu-id="461d1-110">These channels include brick-and-mortar stores, call centers, mobile devices, and e-Commerce sites.</span></span>

<span data-ttu-id="461d1-111">Kui kliendil on teise kaupluse tellimus, saab kassapidaja valida kuupäevad, millal üleskorje on selles poes saadaval.</span><span class="sxs-lookup"><span data-stu-id="461d1-111">If a customer has a pickup order for a different store, the cashier can select dates when the pickup will be available in that store.</span></span> <span data-ttu-id="461d1-112">Kaupluse otsing annab viite kuupäevadele ja kaupluse lahtiolekuaegadele.</span><span class="sxs-lookup"><span data-stu-id="461d1-112">The store lookup will provide a reference to the dates and store times.</span></span> <span data-ttu-id="461d1-113">Kassapidaja saab valida kuupäeva ja asukoha ning printida ka üleskorje kviitungi, mis sisaldab kaupluse lahtiolekuaegu.</span><span class="sxs-lookup"><span data-stu-id="461d1-113">The cashier can select a date and location, and can also print a pickup receipt that includes the store hours.</span></span>

<span data-ttu-id="461d1-114">See funktsioon on saadaval tarkvara Microsoft Dynamics 365 Retail versioonides 8.1.2 ja uuemad.</span><span class="sxs-lookup"><span data-stu-id="461d1-114">This functionality is available in Microsoft Dynamics 365 Retail versions 8.1.2 and later.</span></span>

## <a name="configure-store-hours"></a><span data-ttu-id="461d1-115">Konfigureeri lahtiolekuaegu</span><span class="sxs-lookup"><span data-stu-id="461d1-115">Configure store hours</span></span>

<span data-ttu-id="461d1-116">Kaupluse lahtiolekuaegade konfigureerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="461d1-116">Follow these steps to configure store hours.</span></span>

1. <span data-ttu-id="461d1-117">Minge jaotisse **Jaemüük ja kaubandus** \> **Kanali seadistus** \> **Lahtiolekuajad**.</span><span class="sxs-lookup"><span data-stu-id="461d1-117">Go to **Retail and Commerce** \> **Channel Setup** \> **Store hours**.</span></span>
2. <span data-ttu-id="461d1-118">Valige **Uus**, et luua uus kaupluse lahtiolekuaegade mall.</span><span class="sxs-lookup"><span data-stu-id="461d1-118">Select **New** to create a new store hours template.</span></span> <span data-ttu-id="461d1-119">Olemasoleva malli kasutamiseks valige vasakul paneelil mall.</span><span class="sxs-lookup"><span data-stu-id="461d1-119">To use an existing template, select the template in the left pane.</span></span>
3. <span data-ttu-id="461d1-120">Dialoogiaknas **Lisa vahemik** Määratlege kuupäevavahemik, kaupluse lahtiolekuajad ja kõik nõutavad pühad.</span><span class="sxs-lookup"><span data-stu-id="461d1-120">In the **Add range** dialog box, define the date range, the store hours, and any holidays that are required.</span></span>

    - <span data-ttu-id="461d1-121">Kui kaupluse lahtiolekuajad ei muutu, valige **Ei lõpe** väljas **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="461d1-121">If store hours don't change, select **Never ends** in the **End date** field.</span></span>
    - <span data-ttu-id="461d1-122">Kui kaupluse lahtiolekuajad on kindla kuu, nädala või päeva jaoks, seadke vastavad kuupäevad väljades **Alguskuupäev** ja **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="461d1-122">If the store hours are for a specific month, week, or day, set the appropriate dates in the **Start Date** and **End date** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="461d1-123">Saate luua mitu malli, millel on kattuvad algus-ja lõppkuupäevad.</span><span class="sxs-lookup"><span data-stu-id="461d1-123">You can create multiple templates that have overlapping start and end dates.</span></span> <span data-ttu-id="461d1-124">Seetõttu saate erinevate ajavööndite kaupluste lahtiolekuaegu määratleda.</span><span class="sxs-lookup"><span data-stu-id="461d1-124">Therefore, you can, for example, define store hours for stores in different time zones.</span></span>

    <span data-ttu-id="461d1-125">![Vahemiku dialoogiakna lisamine](../dev-itpro/media/Storehours1.png "Vahemiku dialoogiakna lisamine")</span><span class="sxs-lookup"><span data-stu-id="461d1-125">![Add range dialog box](../dev-itpro/media/Storehours1.png "Add range dialog box")</span></span>

4. <span data-ttu-id="461d1-126">Seostage kaupluse lahtiolekuaegade mall kauplustega, kus seda kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="461d1-126">Associate the store hours template with the stores where it will be used.</span></span> <span data-ttu-id="461d1-127">Valige dialoogikastis **Vali organisatsiooni sõlmed** kauplused, regioonid ja organisatsioonid, millega mall peaks seotud olema.</span><span class="sxs-lookup"><span data-stu-id="461d1-127">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>

    - <span data-ttu-id="461d1-128">Iga kauplusega saab seostada ainult ühe kaupluse lahtiolekuaegade malli.</span><span class="sxs-lookup"><span data-stu-id="461d1-128">Only one store hours template can be associated with each store.</span></span>
    - <span data-ttu-id="461d1-129">Kasutage noolenuppe, et valida kauplusi, regioone või organisatsioone.</span><span class="sxs-lookup"><span data-stu-id="461d1-129">Use the arrow buttons to select stores, regions, or organizations.</span></span> <span data-ttu-id="461d1-130">Kalender on saadaval kauplustele või kauplusegruppidele ja see on viiteks nähtav kassas.</span><span class="sxs-lookup"><span data-stu-id="461d1-130">The calendar will be available to the stores or store groups, and it will be visible at the POS for reference.</span></span>

    <span data-ttu-id="461d1-131">![Organisatsioonisõlmede dialoogiakna valimine](../dev-itpro/media/Storehours2.png "Organisatsioonisõlmede dialoogiakna valimine")</span><span class="sxs-lookup"><span data-stu-id="461d1-131">![Choose organization nodes dialog box](../dev-itpro/media/Storehours2.png "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="461d1-132">Käivitage lehel **Jaotuse graafik** tööd **1070** ja **1090**, et muuta kaupluse lahtiolekuajad kassas kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="461d1-132">On the **Distribution schedule** page, run the **1070** and **1090** jobs to make the store hours available to the POS.</span></span>

## <a name="add-store-hours-to-printed-receipts"></a><span data-ttu-id="461d1-133">Kaupluse lahtiolekuaegade lisamine prinditud kviitungitele</span><span class="sxs-lookup"><span data-stu-id="461d1-133">Add store hours to printed receipts</span></span>

<span data-ttu-id="461d1-134">Järgige neid samme, et lisada kaupluse lahtiolekuajad prinditud kassa kviitungitele.</span><span class="sxs-lookup"><span data-stu-id="461d1-134">Follow these steps to add store hours to the printed POS receipts.</span></span>

1. <span data-ttu-id="461d1-135">Avage kviitungi kujundaja.</span><span class="sxs-lookup"><span data-stu-id="461d1-135">Open the receipt designer.</span></span>
2. <span data-ttu-id="461d1-136">Valige alumises vasakus nurgas **Jalus**.</span><span class="sxs-lookup"><span data-stu-id="461d1-136">Select **Footer** in the lower-left corner.</span></span>
3. <span data-ttu-id="461d1-137">Lohistage element **Kaupluse lahtiolekuajad** vasakul paneelilt jalusesse kviitungi malli allservas.</span><span class="sxs-lookup"><span data-stu-id="461d1-137">Drag the **Store hours** element from the left pane to the footer at the bottom of the receipt template.</span></span>
4. <span data-ttu-id="461d1-138">Elemendis saate redigeerida vaikimisi seatud silti **Kaupluse lahtiolekuajad** vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="461d1-138">You can edit the default label on the **Store hours** element as you require.</span></span>
5. <span data-ttu-id="461d1-139">Salvestage kviitung ja sulgege kviitungi kujundaja.</span><span class="sxs-lookup"><span data-stu-id="461d1-139">Save the receipt, and close the receipt designer.</span></span>
6. <span data-ttu-id="461d1-140">Käivitage lehel **Jaotuse graafik** tööd **1070** ja **1090**.</span><span class="sxs-lookup"><span data-stu-id="461d1-140">On the **Distribution schedule** page, run the **1070** and **1090** jobs.</span></span>
7. <span data-ttu-id="461d1-141">Logige kassasse sisse.</span><span class="sxs-lookup"><span data-stu-id="461d1-141">Sign in to the POS.</span></span>
8. <span data-ttu-id="461d1-142">Lõpetage müük ja valige kviitung printimiseks.</span><span class="sxs-lookup"><span data-stu-id="461d1-142">Complete a sale, and select to print a receipt.</span></span>

<span data-ttu-id="461d1-143">Kassa kviitungid sisaldavad nüüd kaupluse lahtiolekuaegu.</span><span class="sxs-lookup"><span data-stu-id="461d1-143">POS receipts now include the store hours.</span></span> <span data-ttu-id="461d1-144">Kui malli kaasatakse kõik pühad, kuvatakse need kviitungil.</span><span class="sxs-lookup"><span data-stu-id="461d1-144">If any holidays were included in the template, they are shown on the receipt.</span></span>

<span data-ttu-id="461d1-145">![Kviitungi näide](../dev-itpro/media/Storehours3.png "Kviitungi näide")</span><span class="sxs-lookup"><span data-stu-id="461d1-145">![Receipt example](../dev-itpro/media/Storehours3.png "Receipt example")</span></span>
