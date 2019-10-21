---
title: Müügireskontro ajalise jaotuse teabe seadistamine ja genereerimine
description: See juhis aitab teil aegumisperioodi määratlust seadistada, kliendi saldosid aegunuks märkida ning vaadata saldosid loendist Aegunud saldo ja lehelt Sissenõuded.
author: mikefalkner
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 77b5dd5feb16cc3bd6d64b6520cc47087c5b5224
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188644"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a><span data-ttu-id="b7c4f-103">Müügireskontro ajalise jaotuse teabe seadistamine ja genereerimine</span><span class="sxs-lookup"><span data-stu-id="b7c4f-103">Set up and generate accounts receivable aging information</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b7c4f-104">See juhis aitab teil aegumisperioodi määratlust seadistada, kliendi saldosid aegunuks märkida ning vaadata saldosid loendist Aegunud saldo ja lehelt Sissenõuded.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-104">This guide will help you set up an aging period definition, age customer balances, and view balances in the Aged balance list and the Collections page.</span></span> <span data-ttu-id="b7c4f-105">Salvestamisel kasutatakse demoettevõtte USMF-i.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-105">This recording uses the USMF demo company.</span></span>


## <a name="create-an-aging-period-definition"></a><span data-ttu-id="b7c4f-106">Aegumisperioodi määratluse loomine</span><span class="sxs-lookup"><span data-stu-id="b7c4f-106">Create an aging period definition</span></span>
1. <span data-ttu-id="b7c4f-107">Avage **Navigeerimispaan > Moodulid > Krediit ja sissenõudmised > Häälestus > Aegumisperioodi definitsioonid**.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Aging period definitions**.</span></span>
2. <span data-ttu-id="b7c4f-108">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-108">Click **New**.</span></span>
3. <span data-ttu-id="b7c4f-109">Sisestage väärtus väljale **Aegumisperioodi definitsioon**.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-109">In the **Aging period definition** field, type a value.</span></span>
4. <span data-ttu-id="b7c4f-110">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="b7c4f-111">Klõpsake nuppu **Lisa alla**, et sisestada uus aegumisperiood.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-111">Click **Add below** to insert a new aging period.</span></span>
6. <span data-ttu-id="b7c4f-112">Sisestage väljale **Periood** kirjeldus aegumisaruannetel kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-112">In the **Period** field, enter the description to show on aging reports.</span></span>
7. <span data-ttu-id="b7c4f-113">Sisestage arv väljale **Ühik**.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-113">In the **Unit** field, enter a number.</span></span>
8. <span data-ttu-id="b7c4f-114">Valige suvand väljal **Intervall**.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-114">In the **Interval** field, select an option.</span></span> <span data-ttu-id="b7c4f-115">Pearaamatu periood vastab teie pearaamatu kalendrile.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-115">Ledger period matches the period to your ledger calendar.</span></span> <span data-ttu-id="b7c4f-116">Päev, nädal, kuu, kvartal ja aastad määratlevad kuupäeva tüübi järgi intervalli pikkuse.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-116">Day, week, month, quarter and years define the size of the interval by date type.</span></span> <span data-ttu-id="b7c4f-117">Valik Piiramatu valib kõik kanded enne või pärast eelmist perioodi, sõltuvalt sellest, kas see on esimene või viimane periood.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-117">Unlimited selects all transactions before or after the previous period, depending on whether it is the first or last period.</span></span>  
9. <span data-ttu-id="b7c4f-118">Valige suvand väljal **Aegumise näidik**.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-118">In the **Aging indicator** field, select an option.</span></span>
10. <span data-ttu-id="b7c4f-119">Valige ruudustiku päisest periood.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-119">Select the period at the top of the grid.</span></span> <span data-ttu-id="b7c4f-120">Aegumisperioodi määratluse vanima perioodi kirjeldamiseks värskendage kirjeldust.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-120">Update the description to describe the oldest period in the aging period definition</span></span>
11. <span data-ttu-id="b7c4f-121">Sisestage väljale **Periood** uus aegumisperioodi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-121">In the **Period** field, enter the new description of the aging period.</span></span>
12. <span data-ttu-id="b7c4f-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-122">Close the page.</span></span>

## <a name="age-the-balances"></a><span data-ttu-id="b7c4f-123">Saldode aegunuks märkimine</span><span class="sxs-lookup"><span data-stu-id="b7c4f-123">Age the balances</span></span>
1. <span data-ttu-id="b7c4f-124">Avage **Krediit ja sissenõudmised > Perioodilised ülesanded > Kliendisaldode ajatamine**.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-124">Go to **Credit and collections > Periodic tasks > Age customer balances**.</span></span>
2. <span data-ttu-id="b7c4f-125">Valige väljal **Aegumisperioodi definitsioon** loodud aegumisperioodi definitsioon.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-125">In the **Aging period definition** field, select the aging period definition that you created.</span></span>
    + <span data-ttu-id="b7c4f-126">Iga aegumisperioodi määratluse kohta saab olla üks aktiivne hetketõmmis.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-126">You can have one active snapshot for each aging period definition.</span></span>  
    + <span data-ttu-id="b7c4f-127">Vaikimisi töödeldakse kõiki kliente.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-127">All customers are processed by default.</span></span> <span data-ttu-id="b7c4f-128">Saate seda valikut kasutada ühe kliendikausta sissenõuete arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-128">You can use this selection to calculate a single collections pool of customers.</span></span>  
    + <span data-ttu-id="b7c4f-129">Valige kandest kuupäev, mida aegumiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-129">Select the date from the transaction that you will use for the aging.</span></span>  
    + <span data-ttu-id="b7c4f-130">Valige aegumise jaoks „aegunud seisuga” kuupäev.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-130">Select an "as of" date for aging.</span></span> <span data-ttu-id="b7c4f-131">Vaikimisi on valitud tänane kuupäev, ent kui muudate sellel väljal valikuks Valitud kuupäev, saate valida mistahes kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-131">The default is today but, if you change this field to Selected date, you will be able to pick the date that you want.</span></span> <span data-ttu-id="b7c4f-132">Pakktöötluseks kasutage tänast kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-132">For batch processing, use Today's date.</span></span>  
3. <span data-ttu-id="b7c4f-133">Laiendage **Ettevõtte** vahemikku.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-133">Expand the **Company** range.</span></span> <span data-ttu-id="b7c4f-134">Saate valida hetketõmmisesse kaasatavad ettevõtted.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-134">You can select the companies that will be included in the snapshot.</span></span> <span data-ttu-id="b7c4f-135">Praegune ettevõte on vaikimis valitud.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-135">The current company is selected by default.</span></span>
4. <span data-ttu-id="b7c4f-136">Klõpsake **Ok** hetktõmmise töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-136">Click **Ok** to process the snapshot.</span></span> <span data-ttu-id="b7c4f-137">See võtab veidi aega, nii et oodake, kuni liugur on kadunud, ja kontrollige, kas sõnumikeskuses on sõnum.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-137">It will take some time so wait for the slider to disappear and check the message center for a message.</span></span>

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a><span data-ttu-id="b7c4f-138">Saldode vaatamine loendis Aegunud saldod ja lehel Sissenõue.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-138">View the balances on the Aged balances list and on the Collection page</span></span>
1. <span data-ttu-id="b7c4f-139">Avage **Krediit ja sissenõudmised > Sissenõudmised > Aegunud kliendisaldod**.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-139">Go to **Credit and collections > Collections > Aged balances**.</span></span> <span data-ttu-id="b7c4f-140">Loendilehel kuvatakse kliendi saldod.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-140">The list page shows the balances for the customer.</span></span> <span data-ttu-id="b7c4f-141">Aegumise ikoon näitab vanima kande aegumisperioodi.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-141">The aging icon shows the aging period for the oldest transaction.</span></span>  
2. <span data-ttu-id="b7c4f-142">Valige saldoga klient.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-142">Select a customer with a balance.</span></span>
3. <span data-ttu-id="b7c4f-143">Laiendage kasti **Aegumise fakt** ala, et näha aegunud saldosid.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-143">Expand the **Aging fact** box area to view the aged balances.</span></span> <span data-ttu-id="b7c4f-144">Kiirinfo aegumisperioodi määratluse kohta võetakse parameetrites määratud aegumisperioodi vaikemääratlusest.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-144">The aging period definition for the fact box is taken from the default aging period definition specified in the parameters.</span></span> <span data-ttu-id="b7c4f-145">Saate seda muuta menüüd Sissenõue kasutades.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-145">You can change it using the Collect menu.</span></span>  

