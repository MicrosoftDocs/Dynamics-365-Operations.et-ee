--- 
title: "Müügireskontro ajalise jaotuse teabe seadistamine ja genereerimine"
description: "See juhis aitab teil aegumisperioodi määratlust seadistada, kliendi saldosid aegunuks märkida ning vaadata saldosid loendist Aegunud saldo ja lehelt Sissenõuded."
author: mikefalkner
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0a793ff52fd5821fef68f1ae928664bbacb1305c
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a><span data-ttu-id="b2064-103">Müügireskontro ajalise jaotuse teabe seadistamine ja genereerimine</span><span class="sxs-lookup"><span data-stu-id="b2064-103">Set up and generate accounts receivable aging information</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b2064-104">See juhis aitab teil aegumisperioodi määratlust seadistada, kliendi saldosid aegunuks märkida ning vaadata saldosid loendist Aegunud saldo ja lehelt Sissenõuded.</span><span class="sxs-lookup"><span data-stu-id="b2064-104">This guide will help you set up an aging period definition, age customer balances, and view balances in the Aged balance list and the Collections page.</span></span> <span data-ttu-id="b2064-105">Salvestamisel kasutatakse demoettevõtte USMF-i.</span><span class="sxs-lookup"><span data-stu-id="b2064-105">This recording uses the USMF demo company.</span></span>


## <a name="create-an-aging-period-definition"></a><span data-ttu-id="b2064-106">Aegumisperioodi määratluse loomine</span><span class="sxs-lookup"><span data-stu-id="b2064-106">Create an aging period definition</span></span>
1. <span data-ttu-id="b2064-107">Tehke valik Krediit ja sissenõuded > Seadistus > Aegumisperioodi määratlused.</span><span class="sxs-lookup"><span data-stu-id="b2064-107">Go to Credit and collections > Setup > Aging period definitions.</span></span>
2. <span data-ttu-id="b2064-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b2064-108">Click New.</span></span>
3. <span data-ttu-id="b2064-109">Sisestage väärtus väljale Aegumisperioodi määratlus.</span><span class="sxs-lookup"><span data-stu-id="b2064-109">In the Aging period definition field, type a value.</span></span>
4. <span data-ttu-id="b2064-110">Sisestage väärtus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="b2064-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b2064-111">Uue aegumisperioodi lisamiseks klõpsake käsku Lisa allolevad.</span><span class="sxs-lookup"><span data-stu-id="b2064-111">Click Add below to insert a new aging period.</span></span>
6. <span data-ttu-id="b2064-112">Sisestage aegumisaruannetel kuvatav kirjeldus väljale Periood.</span><span class="sxs-lookup"><span data-stu-id="b2064-112">In the Period field, enter the description to show on aging reports.</span></span>
7. <span data-ttu-id="b2064-113">Sisestage arv väljale Ühik.</span><span class="sxs-lookup"><span data-stu-id="b2064-113">In the Unit field, enter a number.</span></span>
8. <span data-ttu-id="b2064-114">Valige suvand väljal Intervall.</span><span class="sxs-lookup"><span data-stu-id="b2064-114">In the Interval field, select an option.</span></span>
    * <span data-ttu-id="b2064-115">Pearaamatu periood vastab teie pearaamatu kalendrile.</span><span class="sxs-lookup"><span data-stu-id="b2064-115">Ledger period matches the period to your ledger calendar.</span></span> <span data-ttu-id="b2064-116">Päev, nädal, kuu, kvartal ja aastad määratlevad kuupäeva tüübi järgi intervalli pikkuse.</span><span class="sxs-lookup"><span data-stu-id="b2064-116">Day, week, month, quarter and years define the size of the interval by date type.</span></span> <span data-ttu-id="b2064-117">Valik Piiramatu valib kõik kanded enne või pärast eelmist perioodi, sõltuvalt sellest, kas see on esimene või viimane periood.</span><span class="sxs-lookup"><span data-stu-id="b2064-117">Unlimited selects all transactions before or after the previous period, depending on whether it is the first or last period.</span></span>  
9. <span data-ttu-id="b2064-118">Valige suvand väljal Aegumise indikaator.</span><span class="sxs-lookup"><span data-stu-id="b2064-118">In the Aging indicator field, select an option.</span></span>
10. <span data-ttu-id="b2064-119">Valige ruudustiku päisest periood.</span><span class="sxs-lookup"><span data-stu-id="b2064-119">Select the period at the top of the grid.</span></span> <span data-ttu-id="b2064-120">Aegumisperioodi määratluse vanima perioodi kirjeldamiseks värskendage kirjeldust.</span><span class="sxs-lookup"><span data-stu-id="b2064-120">Update the description to describe the oldest period in the aging period definition</span></span>
11. <span data-ttu-id="b2064-121">Sisestage aegumisperioodi uus kirjeldus väljale Periood.</span><span class="sxs-lookup"><span data-stu-id="b2064-121">In the Period field, enter the new description of the aging period.</span></span>
12. <span data-ttu-id="b2064-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b2064-122">Close the page.</span></span>

## <a name="age-the-balances"></a><span data-ttu-id="b2064-123">Saldode aegunuks märkimine</span><span class="sxs-lookup"><span data-stu-id="b2064-123">Age the balances</span></span>
1. <span data-ttu-id="b2064-124">Tehke valik Krediit ja sissenõuded > Perioodilised ülesanded > Klientide saldode aegumine.</span><span class="sxs-lookup"><span data-stu-id="b2064-124">Go to Credit and collections > Periodic tasks > Age customer balances.</span></span>
2. <span data-ttu-id="b2064-125">Valige loodud aegumisperioodi määratlus väljal Aegumisperiood.</span><span class="sxs-lookup"><span data-stu-id="b2064-125">In the Aging period definition field, select the aging period definition that you created.</span></span>
    * <span data-ttu-id="b2064-126">Iga aegumisperioodi määratluse kohta saab olla üks aktiivne hetketõmmis.</span><span class="sxs-lookup"><span data-stu-id="b2064-126">You can have one active snapshot for each aging period definition.</span></span>  
    * <span data-ttu-id="b2064-127">Vaikimisi töödeldakse kõiki kliente.</span><span class="sxs-lookup"><span data-stu-id="b2064-127">All customers are processed by default.</span></span> <span data-ttu-id="b2064-128">Saate seda valikut kasutada ühe kliendikausta sissenõuete arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="b2064-128">You can use this selection to calculate a single collections pool of customers.</span></span>  
    * <span data-ttu-id="b2064-129">Valige kandest kuupäev, mida aegumiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="b2064-129">Select the date from the transaction that you will use for the aging.</span></span>  
    * <span data-ttu-id="b2064-130">Valige aegumise jaoks „aegunud seisuga” kuupäev.</span><span class="sxs-lookup"><span data-stu-id="b2064-130">Select an "as of" date for aging.</span></span> <span data-ttu-id="b2064-131">Vaikimisi on valitud tänane kuupäev, ent kui muudate sellel väljal valikuks Valitud kuupäev, saate valida mistahes kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="b2064-131">The default is today but, if you change this field to Selected date, you will be able to pick the date that you want.</span></span> <span data-ttu-id="b2064-132">Pakktöötluseks kasutage tänast kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="b2064-132">For batch processing, use Today's date.</span></span>  
3. <span data-ttu-id="b2064-133">Laiendage valikut Ettevõtete vahemik.</span><span class="sxs-lookup"><span data-stu-id="b2064-133">Expand the Company range.</span></span> <span data-ttu-id="b2064-134">Saate valida hetketõmmisesse kaasatavad ettevõtted.</span><span class="sxs-lookup"><span data-stu-id="b2064-134">You can select the companies that will be included in the snapshot.</span></span> <span data-ttu-id="b2064-135">Praegune ettevõte on vaikimis valitud.</span><span class="sxs-lookup"><span data-stu-id="b2064-135">The current company is selected by default.</span></span>
4. <span data-ttu-id="b2064-136">Klõpsake nuppu OK hetketõmmise töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="b2064-136">Click Ok to process the snapshot.</span></span> <span data-ttu-id="b2064-137">See võtab veidi aega, nii et oodake, kuni liugur on kadunud, ja kontrollige, kas sõnumikeskuses on sõnum.</span><span class="sxs-lookup"><span data-stu-id="b2064-137">It will take some time so wait for the slider to disappear and check the message center for a message.</span></span>

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a><span data-ttu-id="b2064-138">Saldode vaatamine loendis Aegunud saldod ja lehel Sissenõue.</span><span class="sxs-lookup"><span data-stu-id="b2064-138">View the balances on the Aged balances list and on the Collection page</span></span>
1. <span data-ttu-id="b2064-139">Tehke valik Krediit ja sissenõuded > Sissenõuded > Aegunud saldod.</span><span class="sxs-lookup"><span data-stu-id="b2064-139">Go to Credit and collections > Collections > Aged balances.</span></span>
    * <span data-ttu-id="b2064-140">Loendilehel kuvatakse kliendi saldod.</span><span class="sxs-lookup"><span data-stu-id="b2064-140">The list page shows the balances for the customer.</span></span> <span data-ttu-id="b2064-141">Aegumise ikoon näitab vanima kande aegumisperioodi.</span><span class="sxs-lookup"><span data-stu-id="b2064-141">The aging icon shows the aging period for the oldest transaction.</span></span>  
2. <span data-ttu-id="b2064-142">Valige saldoga klient.</span><span class="sxs-lookup"><span data-stu-id="b2064-142">Select a customer with a balance.</span></span>
3. <span data-ttu-id="b2064-143">Laiendage jaotise Aegumine kiirinfo ala, et näha aegunud saldosid.</span><span class="sxs-lookup"><span data-stu-id="b2064-143">Expand the Aging fact box area to view the aged balances.</span></span>
    * <span data-ttu-id="b2064-144">Kiirinfo aegumisperioodi määratluse kohta võetakse parameetrites määratud aegumisperioodi vaikemääratlusest.</span><span class="sxs-lookup"><span data-stu-id="b2064-144">The aging period definition for the fact box is taken from the default aging period definition specified in the parameters.</span></span> <span data-ttu-id="b2064-145">Saate seda muuta menüüd Sissenõue kasutades.</span><span class="sxs-lookup"><span data-stu-id="b2064-145">You can change it using the Collect menu.</span></span>  


