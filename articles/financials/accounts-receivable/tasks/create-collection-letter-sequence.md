---
title: Märgukirjaseeria loomine
description: Kasutage seda ülesande juhendit märgukirjaseeria loomiseks.
author: mikefalkner
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db5264f6d8d7723ff01d13e99728c2bfebcb4515
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "311561"
---
# <a name="create-a-collection-letter-sequence"></a><span data-ttu-id="3e4f1-103">Märgukirjaseeria loomine</span><span class="sxs-lookup"><span data-stu-id="3e4f1-103">Create a collection letter sequence</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3e4f1-104">Kasutage seda ülesande juhendit märgukirjaseeria loomiseks.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-104">Use this task guide to create a collection letter sequence.</span></span> <span data-ttu-id="3e4f1-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="3e4f1-106">Avage Krediit ja sissenõuded > Seadistus > Märgukirjaseeria seadistamine.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-106">Go to Credit and collections > Setup > Set up collection letter sequence.</span></span>
2. <span data-ttu-id="3e4f1-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-107">Click New.</span></span>
3. <span data-ttu-id="3e4f1-108">Sisestage seeriat tähistav seeria ID väljale Märgukirjaseeria.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-108">In the Collection letter sequence field, enter a sequence ID that will represent the sequence.</span></span> <span data-ttu-id="3e4f1-109">Seda kasutatakse sisestusreeglite seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-109">It will be used when you set up a posting profile.</span></span>
4. <span data-ttu-id="3e4f1-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="3e4f1-111">Maksetingimused on valikulised.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-111">The terms of payment is optional.</span></span> <span data-ttu-id="3e4f1-112">Kui sisestate väärtuse siia, kasutab märgukirja tasu arve neid maksetingimusi kliendi puhul salvestatud maksetingimuste asemel.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-112">If you enter a value here, the collection letter fee invoice will use these terms of payment instead of the terms of payment stored with the customer.</span></span>  
5. <span data-ttu-id="3e4f1-113">Valige märgukirja koodi väljalt esimese märgukirja kood, mille soovite saata.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-113">In the collection letter code field, select the code for the first collection letter that you want to send.</span></span>
    * <span data-ttu-id="3e4f1-114">Esimene märgukiri luuakse arve maksetähtaja, selle rea väljale Päevad ajapikendusperioodi puhul sisestatud väärtuse ja muu sellele reale sisestatud teabe järgi.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-114">The first collection letter is created according to the due date on the invoice, the value that you enter for the grace period in the Days field on this line, and other information that you enter on this line.</span></span>  
6. <span data-ttu-id="3e4f1-115">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="3e4f1-116">Tasu valuuta on vaikimisi kliendi valuutas.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-116">The currency for the fee defaults to the customer currency.</span></span> <span data-ttu-id="3e4f1-117">Valuutakood võib arve valuutast erineda.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-117">This currency code can be different than the invoice currency.</span></span>  
7. <span data-ttu-id="3e4f1-118">Seerias järgmisena saadetava märgukirja lisamiseks klõpsake nuppu Lisa</span><span class="sxs-lookup"><span data-stu-id="3e4f1-118">Click Add to add the next collection letter that will be sent in the sequence</span></span>
    * <span data-ttu-id="3e4f1-119">Paljudel juhtudel on esimene märgukiri ainult hoiatus.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-119">In many cases, the first collection letter is just a warning.</span></span> <span data-ttu-id="3e4f1-120">Vajaduse korral saate lisada tasud.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-120">You can add fees if needed.</span></span>  
8. <span data-ttu-id="3e4f1-121">Valige märgukirja koodi väljalt seerias järgmisena saadetav märgukiri.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-121">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
9. <span data-ttu-id="3e4f1-122">Sisestage väärtus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="3e4f1-123">Valige põhikonto väljalt tasude puhul kasutatav tulukonto.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-123">In the main account field, select the revenue account that will be used for fees.</span></span>
11. <span data-ttu-id="3e4f1-124">Sisestage tasu, mis tuleb maksta selle märgukirja sisestamisel.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-124">Enter the fee that will be charged when this collection letter is posted.</span></span>
12. <span data-ttu-id="3e4f1-125">Klõpsake väljal Kauba käibemaksugrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-125">In the Item sales tax group field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="3e4f1-126">Kui tasu puhul tuleb arvutada käibemaksu, valige kauba käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-126">Select an item sales tax group if sales taxes must be calculated on the fee.</span></span>  
13. <span data-ttu-id="3e4f1-127">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="3e4f1-128">Sisestage minimaalne tähtaja ületanud saldo, mis on nõutav enne märgukirja saatmist.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-128">Enter the minimum overdue balance required before a collection letter is sent.</span></span>
15. <span data-ttu-id="3e4f1-129">Sisestage teie lubatavate ajapikenduspäevade arv.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-129">Enter the number of grace days that you will allow.</span></span>
    * <span data-ttu-id="3e4f1-130">See on päevade arv pärast maksetähtaega, mil saab luua märgukirja.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-130">This is the number of days after the due date that a collection letter can be generated.</span></span> <span data-ttu-id="3e4f1-131">Arvutuses kasutatav tähtaeg oleneb märgukirja paigutusest märgukirjade järjestuses: ⦁ 1. märgukirja ajapikenduse periood on seotud arve maksetähtajaga.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-131">The due date that is used for the calculation depends on the position of the collection letter in the collection letter sequence:   ⦁    The grace period for collection letter 1 is relative to the due date on the invoice.</span></span>  <span data-ttu-id="3e4f1-132">⦁ 2. ja edasiste märgukirjade ajapikenduse periood on seotud eelmise märgukirja sisestamise või printimise kuupäevaga, olenevalt välja Värskenda märgukirja koodi valikust lehel Müügireskontro parameetrid.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-132">⦁ The grace period for collection letters 2 and higher is relative to the date that the previous collection letter is posted or printed, depending on the selection in the Update collection letter code field in the Accounts receivable parameters page.</span></span>  
16. <span data-ttu-id="3e4f1-133">Seerias viimase märgukirja lisamiseks klõpsake nuppu Lisa.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-133">Click Add to add the last collection letter in the sequence.</span></span>
    * <span data-ttu-id="3e4f1-134">Saate märgukirjaseeria puhul lisada kuni viis märgukirjakoodi.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-134">You can add up to five collection letter codes for a collection letter sequence.</span></span>  
17. <span data-ttu-id="3e4f1-135">Valige märgukirja koodi väljalt seerias järgmisena saadetav märgukiri.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-135">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
18. <span data-ttu-id="3e4f1-136">Sisestage väärtus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-136">In the Description field, type a value.</span></span>
19. <span data-ttu-id="3e4f1-137">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-137">In the Main account field, specify the desired values.</span></span>
20. <span data-ttu-id="3e4f1-138">Sisestage number väljale Tasu valuutas.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-138">In the Fee in currency field, enter a number.</span></span>
21. <span data-ttu-id="3e4f1-139">Klõpsake väljal Kauba käibemaksugrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-139">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="3e4f1-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="3e4f1-141">Sisestage number väljale Minimaalne tähtaja ületanud saldo.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-141">In the Minimum overdue balance field, enter a number.</span></span>
24. <span data-ttu-id="3e4f1-142">Sisestage number väljale Päevad.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-142">In the Days field, enter a number.</span></span>
25. <span data-ttu-id="3e4f1-143">Märkige see ruut kliendi jaoks täiendavate tarnete ja arvelduste peatamiseks.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-143">Select this check box to stop the customer from additional deliveries and invoicing.</span></span>
    * <span data-ttu-id="3e4f1-144">Kontolt blokeeringu eemaldamiseks tehke lehe Kliendid väljal Arveldamine ja tarne ootel valik Ei.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-144">To unblock the account, select No in the Invoicing and delivery on hold field in the Customers page.</span></span>  
26. <span data-ttu-id="3e4f1-145">Laiendage kiirkaarti Märkus.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-145">Expand the Note fasttab.</span></span>
27. <span data-ttu-id="3e4f1-146">Sisestage valitud märgukirjakoodi puhul märgukirjas kuvatav tekst.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-146">Enter the text to appear on the collection letter for the selected collection letter code.</span></span>
    * <span data-ttu-id="3e4f1-147">Saate selle teksti tõlkida mitmesse keelde, kasutades märkuse kasti kohal olevat menüüd Tõlked.</span><span class="sxs-lookup"><span data-stu-id="3e4f1-147">You can translate this text in to multiple languages using the Translations menu above the note box.</span></span>  

