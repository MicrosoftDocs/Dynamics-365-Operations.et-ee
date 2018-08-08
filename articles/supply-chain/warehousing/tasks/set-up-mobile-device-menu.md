--- 
title: "Mobiilse seadme menüükäsu seadistamine ostutellimuse töö lõpetamiseks"
description: "Selles protseduuris näidatakse, kuidas seadistada mobiilse seadme menüü-üksust."
author: ShylaThompson
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 31007031b761cfed6b5a97ebb829be4d200bc82d
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-in-a-purchase-order"></a><span data-ttu-id="43d62-103">Mobiilse seadme menüükäsu seadistamine ostutellimuse töö lõpetamiseks</span><span class="sxs-lookup"><span data-stu-id="43d62-103">Set up a mobile device menu item for completing work in a purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="43d62-104">Selles protseduuris näidatakse, kuidas seadistada mobiilse seadme menüü-üksust.</span><span class="sxs-lookup"><span data-stu-id="43d62-104">This procedure shows how to set up a Mobile device menu item.</span></span> <span data-ttu-id="43d62-105">Selles näites kasutatakse seda menüü-üksust ostutellimuse tüüpi töö tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="43d62-105">In this example, the menu item is used for performing work of type Purchase order.</span></span> <span data-ttu-id="43d62-106">Menüü-üksusega seotud töö klass määrab, milline töö on kehtiv.</span><span class="sxs-lookup"><span data-stu-id="43d62-106">The work class that’s associated with the menu item determines which work is valid.</span></span> <span data-ttu-id="43d62-107">Saate seda juhendit kasutada demoettevõtte USMF andmetega.</span><span class="sxs-lookup"><span data-stu-id="43d62-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="43d62-108">Tavaliselt viib selle protseduuri läbi laojuhataja.</span><span class="sxs-lookup"><span data-stu-id="43d62-108">This procedure is typically carried out by a warehouse manager.</span></span>


## <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="43d62-109">Mobiilse seadme menüü-üksuse loomine</span><span class="sxs-lookup"><span data-stu-id="43d62-109">Create a mobile device menu item</span></span>
1. <span data-ttu-id="43d62-110">Minge jaotisse Mobiilse seadme menüü-üksused.</span><span class="sxs-lookup"><span data-stu-id="43d62-110">Go to Mobile device menu items.</span></span>
2. <span data-ttu-id="43d62-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="43d62-111">Click New.</span></span>
3. <span data-ttu-id="43d62-112">Sisestage väärtus väljale Menüü-üksuse nimi.</span><span class="sxs-lookup"><span data-stu-id="43d62-112">In the Menu item name field, type a value.</span></span>
    * <span data-ttu-id="43d62-113">Sisestage kordumatu väärtus.</span><span class="sxs-lookup"><span data-stu-id="43d62-113">Enter a unique value.</span></span> <span data-ttu-id="43d62-114">Näiteks võite sisestada POMove.</span><span class="sxs-lookup"><span data-stu-id="43d62-114">For example, you could type POMove.</span></span> <span data-ttu-id="43d62-115">Jätke väärtus meelde, teil on seda hiljem vaja.</span><span class="sxs-lookup"><span data-stu-id="43d62-115">Remember the value, you'll need it later.</span></span>  
4. <span data-ttu-id="43d62-116">Sisestage väärtus väljale Pealkiri.</span><span class="sxs-lookup"><span data-stu-id="43d62-116">In the Title field, type a value.</span></span>
    * <span data-ttu-id="43d62-117">See on pealkiri, mis kuvatakse mobiilses seadmes.</span><span class="sxs-lookup"><span data-stu-id="43d62-117">This is the title which will be displayed on the mobile device.</span></span> <span data-ttu-id="43d62-118">Näiteks võite sisestada PO Move.</span><span class="sxs-lookup"><span data-stu-id="43d62-118">For example, you could type PO Move.</span></span>  
5. <span data-ttu-id="43d62-119">Valige väljal Režiim suvand Töö.</span><span class="sxs-lookup"><span data-stu-id="43d62-119">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="43d62-120">Valige suvand Jah väljal Kasuta olemasolevat tööd.</span><span class="sxs-lookup"><span data-stu-id="43d62-120">Select Yes in the Use existing work field.</span></span>
    * <span data-ttu-id="43d62-121">Seda mobiilse seadme menüüelementi kasutatakse olemasoleva töö tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="43d62-121">This mobile device menu item is used to perform existing work.</span></span> <span data-ttu-id="43d62-122">Seega tuleb määrata selle väärtuseks Jah.</span><span class="sxs-lookup"><span data-stu-id="43d62-122">Therefore you must set this value to Yes.</span></span>  
    * <span data-ttu-id="43d62-123">Väli Kuva varude olek määrab, kas vaba kaubavaru olek kuvatakse laotöötajale mobiilsel seadmel.</span><span class="sxs-lookup"><span data-stu-id="43d62-123">The Display inventory status field determines whether the inventory status of the on-hand inventory will be displayed to the warehouse worker on the mobile device.</span></span>  
7. <span data-ttu-id="43d62-124">Tehke väljal Suunaja valik Süsteemi rühmitamine.</span><span class="sxs-lookup"><span data-stu-id="43d62-124">In the Directed by field, select 'System grouping'.</span></span>
    * <span data-ttu-id="43d62-125">Kui valite midagi väljalt Suunaja, kuvatakse selle lehe jaotises Üldine lisaväljad.</span><span class="sxs-lookup"><span data-stu-id="43d62-125">When you select something in the Directed by field, additional fields appear in the General section on this page.</span></span> <span data-ttu-id="43d62-126">Kuvatavad väljad sõltuvad sellest, mida valisite.</span><span class="sxs-lookup"><span data-stu-id="43d62-126">The fields that appear depend on what you selected.</span></span> <span data-ttu-id="43d62-127">Kui teete valiku Süsteemi rühmitamine, lisatakse kaks uut välja.</span><span class="sxs-lookup"><span data-stu-id="43d62-127">When you select System grouping, two new fields are added.</span></span> <span data-ttu-id="43d62-128">Neid selgitatakse allpool.</span><span class="sxs-lookup"><span data-stu-id="43d62-128">These are explained below.</span></span>  
8. <span data-ttu-id="43d62-129">Valige väljalt Süsteemi rühmitamine väärtus WorkPoolId.</span><span class="sxs-lookup"><span data-stu-id="43d62-129">In the System grouping field, select 'WorkPoolId'.</span></span>
    * <span data-ttu-id="43d62-130">Kui laotöötajad selle menüü-üksuse avavad, palutakse neil töökausta ID skannida.</span><span class="sxs-lookup"><span data-stu-id="43d62-130">When warehouse workers open this menu item, they’ll be asked to scan a Work pool ID.</span></span> <span data-ttu-id="43d62-131">Kõik selle töökausta ID-ga töötellimused ja ühe sellele menüü-üksusele lisatud tööklassiga avatud töötellimuse read suunatakse kasutajale.</span><span class="sxs-lookup"><span data-stu-id="43d62-131">All work orders with this Work pool ID and open work order lines with one of the work classes added to this menu item will be pushed to the user.</span></span>  
9. <span data-ttu-id="43d62-132">Sisestage väärtus väljale Süsteemi rühmitussilt.</span><span class="sxs-lookup"><span data-stu-id="43d62-132">In the System grouping label field, type a value.</span></span>
    * <span data-ttu-id="43d62-133">See tekst kuvatakse mobiilsel seadmel kasutajale.</span><span class="sxs-lookup"><span data-stu-id="43d62-133">This is the text displayed to the user on the mobile device.</span></span> <span data-ttu-id="43d62-134">Näiteks võite sisestada valiku Töökaust.</span><span class="sxs-lookup"><span data-stu-id="43d62-134">For example, you could type Work pool.</span></span>  
10. <span data-ttu-id="43d62-135">Valige Jah väljal Tühista litsentsiplaat paneku käigus.</span><span class="sxs-lookup"><span data-stu-id="43d62-135">Select Yes in the Override license plate during put field.</span></span>
    * <span data-ttu-id="43d62-136">See valik võimaldab laotöötajatel alistada sihtlitsentsiplaadi, kui kaubad paigutatakse litsentsiplaadiga juhitavasse asukohta.</span><span class="sxs-lookup"><span data-stu-id="43d62-136">This option allows warehouse workers to override the target license plate when items are put down on a license plate controlled location.</span></span>  
11. <span data-ttu-id="43d62-137">Valige Jah väljal Grupi kõrvalepanek.</span><span class="sxs-lookup"><span data-stu-id="43d62-137">Select Yes in the Group put away field.</span></span>
    * <span data-ttu-id="43d62-138">Kui kõik asetamise read töötellimusel on sama asukohaga, saab kasutaja kõigi ridade kohta ühe kombineeritud asetamise juhise.</span><span class="sxs-lookup"><span data-stu-id="43d62-138">If all the Put lines on the work order share the same location, the user will receive one combined Put instruction for all lines.</span></span>  
    * <span data-ttu-id="43d62-139">Auditimalli ID: töö auditimall võimaldab määratleda, et menüü-üksuse tööprotsess tuleks teise toimingu tegemiseks katkestada.</span><span class="sxs-lookup"><span data-stu-id="43d62-139">Audit template ID: A work audit template allows you to specify that the work process for a menu item should be interrupted so that another operation can be performed.</span></span> <span data-ttu-id="43d62-140">Kui näiteks menüüelement käib sissetuleva töö kohta, võib auditimall nõuda, et töötaja kontrolliks temperatuuri.</span><span class="sxs-lookup"><span data-stu-id="43d62-140">For example, if this menu item is for inbound work, the audit template might require that the worker checks the temperature.</span></span> <span data-ttu-id="43d62-141">Hetk, millal protsess katkestatakse, tuleb määrata auditi mallis, ja see võib olla näiteks siis, kui tööd alustatakse või lõpetatakse või kui selle olek muutub.</span><span class="sxs-lookup"><span data-stu-id="43d62-141">The point at which the process is interrupted is specified on the audit template and can be, for example, when work is started or completed, or when its status changes.</span></span>  
12. <span data-ttu-id="43d62-142">Laiendage jaotist Tööklassid.</span><span class="sxs-lookup"><span data-stu-id="43d62-142">Expand the Work classes section.</span></span>
13. <span data-ttu-id="43d62-143">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="43d62-143">Click New.</span></span>
14. <span data-ttu-id="43d62-144">Sisestage väljale Tööklassi ID sõna Ost.</span><span class="sxs-lookup"><span data-stu-id="43d62-144">In the Work class ID field, type 'Purchase'.</span></span>
    * <span data-ttu-id="43d62-145">Töökaust piirab tööd, mille jaoks seda menüüelementi võib kasutada.</span><span class="sxs-lookup"><span data-stu-id="43d62-145">The work pool restricts the work that the menu item can be used for.</span></span> <span data-ttu-id="43d62-146">Praegusel juhul kasutatakse seda avatud töötellimuse ridade jaoks, millel on ostutöö klassi ID.</span><span class="sxs-lookup"><span data-stu-id="43d62-146">In this case it will be used for open work order lines that have the Purchase work class ID.</span></span>  
15. <span data-ttu-id="43d62-147">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="43d62-147">Click Save.</span></span>

## <a name="set-up-work-confirmation"></a><span data-ttu-id="43d62-148">Töö kinnituse häälestamine</span><span class="sxs-lookup"><span data-stu-id="43d62-148">Set up work confirmation</span></span>
1. <span data-ttu-id="43d62-149">Klõpsake valikut Töö kinnituse häälestus.</span><span class="sxs-lookup"><span data-stu-id="43d62-149">Click Work confirmation setup.</span></span>
2. <span data-ttu-id="43d62-150">Tehke väljal Töö tüüp valik Komplekteeri.</span><span class="sxs-lookup"><span data-stu-id="43d62-150">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="43d62-151">Märkige ruut Automaatkinnitus.</span><span class="sxs-lookup"><span data-stu-id="43d62-151">Select the Auto confirm check box.</span></span>
    * <span data-ttu-id="43d62-152">Tööjuhis töö tüübiga Komplekteeri kinnitatakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="43d62-152">The work instruction with work type Pick will be auto-confirmed.</span></span> <span data-ttu-id="43d62-153">Seda juhist ei kuvata kasutajale.</span><span class="sxs-lookup"><span data-stu-id="43d62-153">This instruction will not be presented to the user.</span></span>  
4. <span data-ttu-id="43d62-154">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="43d62-154">Click New.</span></span>
5. <span data-ttu-id="43d62-155">Valige väljal Töö tüüp suvand Pane.</span><span class="sxs-lookup"><span data-stu-id="43d62-155">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="43d62-156">Märkige ruut Asukoha kinnitus.</span><span class="sxs-lookup"><span data-stu-id="43d62-156">Select the Location confirmation check box.</span></span>
    * <span data-ttu-id="43d62-157">Laotöötajal palutakse teha asukohast kinnitusskann, kui kaup on paigutatud.</span><span class="sxs-lookup"><span data-stu-id="43d62-157">The warehouse worker will be asked to perform a confirmation scan of the location, when the item is put down.</span></span>  
7. <span data-ttu-id="43d62-158">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="43d62-158">Click Save.</span></span>
8. <span data-ttu-id="43d62-159">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="43d62-159">Close the page.</span></span>
9. <span data-ttu-id="43d62-160">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="43d62-160">Close the page.</span></span>

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="43d62-161">Menüü-üksuse lisamine mobiilse seadme menüüsse</span><span class="sxs-lookup"><span data-stu-id="43d62-161">Add the menu item to a mobile device menu</span></span>
1. <span data-ttu-id="43d62-162">Minge jaotisse Mobiilse seadme menüü.</span><span class="sxs-lookup"><span data-stu-id="43d62-162">Go to Mobile device menu.</span></span>
2. <span data-ttu-id="43d62-163">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="43d62-163">Click Edit.</span></span>
3. <span data-ttu-id="43d62-164">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="43d62-164">Use the Quick Filter to find records.</span></span> <span data-ttu-id="43d62-165">Näiteks saate filtreerida välja Nimi väärtuse „sissetulev” järgi.</span><span class="sxs-lookup"><span data-stu-id="43d62-165">For example, filter on the Name field with a value of 'inbound'.</span></span>
    * <span data-ttu-id="43d62-166">Soovite leida menüüd, mida kasutate sissetulevate menüü-üksuste puhul.</span><span class="sxs-lookup"><span data-stu-id="43d62-166">You want to find the menu you use for inbound menu items.</span></span> <span data-ttu-id="43d62-167">USMF-is on selle nimetus Sissetulev.</span><span class="sxs-lookup"><span data-stu-id="43d62-167">In USMF this is called Inbound.</span></span>  
4. <span data-ttu-id="43d62-168">Valige puult „väärtus”.</span><span class="sxs-lookup"><span data-stu-id="43d62-168">In the tree, select 'a value'.</span></span>
5. <span data-ttu-id="43d62-169">Klõpsake paremale suunatud noolt.</span><span class="sxs-lookup"><span data-stu-id="43d62-169">Click on the arrow that points to the right.</span></span>
6. <span data-ttu-id="43d62-170">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="43d62-170">Click Save.</span></span>
7. <span data-ttu-id="43d62-171">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="43d62-171">Close the page.</span></span>


