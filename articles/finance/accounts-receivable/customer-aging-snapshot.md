---
title: 'Kliendi aegumise hetktõmmised '
description: Selles teemas kirjeldatakse kliendi aegumise hetktõmmiseid. Aegumise hetktõmmis sisaldab arvutatud aegunud saldosid kliendi kohta kindlal ajahetkel.
author: JodiChristiansen
ms.date: 05/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b88d3fe97d14d3e2f766367de501148063582000
ms.sourcegitcommit: 16376a301a0f121f384d77f9976638f701f8e88e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6123358"
---
# <a name="customer-aging-snapshots"></a><span data-ttu-id="cbdd1-104">Kliendi aegumise hetktõmmised </span><span class="sxs-lookup"><span data-stu-id="cbdd1-104">Customer aging snapshots</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cbdd1-105">Selles teemas kirjeldatakse kliendi aegumise hetktõmmiseid.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-105">This topic provides information about customer aging snapshots.</span></span> <span data-ttu-id="cbdd1-106">Aegumise hetktõmmis sisaldab arvutatud aegunud saldosid kliendi kohta kindlal ajahetkel.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-106">An aging snapshot calculates aged balances for a group of customers at a point in time.</span></span> <span data-ttu-id="cbdd1-107">Looge aegumise hetktõmmise kirjed kõigile klientidele või kliendikausta klientidele.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-107">You can create aging snapshot records either for all customers or for the customers in a customer pool.</span></span>

<span data-ttu-id="cbdd1-108">Aegumise hetktõmmise teave kuvatakse loendilehel **Aegunud saldod** ja lehel **Sissenõuded**.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-108">Information from aging snapshots is shown on the **Aged balances** list page and the **Collections** page.</span></span> <span data-ttu-id="cbdd1-109">Enne kui saate **Aegunud saldod** loendilehte kasutada, peate looma aegumise hetktõmmise.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-109">You must create an aging snapshot before you can use the **Aged balances** list page.</span></span> <span data-ttu-id="cbdd1-110">Loendilehel kuvatakse teavet vaid püsiklientidele, kelle jaoks on aegumise hetktõmmis loodud.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-110">The list page lists only customers that an aging snapshot has been created for.</span></span>

<span data-ttu-id="cbdd1-111">**Kliendi krediidi ja sissenõuete** tööruum näitab ka kliendi aegumist.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-111">The **Customer credit and collections** workspace also shows the customer aging.</span></span> <span data-ttu-id="cbdd1-112">Lisateavet vt [krediidi ja sissenõuete halduse Power BI sisust](credit-collections-power-bi.md).</span><span class="sxs-lookup"><span data-stu-id="cbdd1-112">For more information, see [Credit and collections management Power BI content](credit-collections-power-bi.md).</span></span>

> [!NOTE]
> <span data-ttu-id="cbdd1-113">Aegumise hetktõmmise loomiseks vajaliku aja vähendamiseks lülitage sisse **Kliendi aegumise jõudluse** funktsioon **Funktsioonihalduse** tööruumis.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-113">To help reduce the time that is required to create an aging snapshot, turn on the **Customer aging performance enhancement** feature in the **Feature management** workspace.</span></span> <span data-ttu-id="cbdd1-114">Ärge siiski kasutage kliendikaustu, kui see funktsioon on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-114">However, don't use customer pools when this feature is turned on.</span></span> <span data-ttu-id="cbdd1-115">Kliendikausta valimisel funktsioon ei tööta, kuid saate aegumise hetktõmmise siiski luua.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-115">If a customer pool is selected, the feature won't work, but you can still create an aging snapshot.</span></span>

<span data-ttu-id="cbdd1-116">Kliendi aegumise hetktõmmise loomisel kasutage selle kohta teabe sisestamiseks järgmisi välju:</span><span class="sxs-lookup"><span data-stu-id="cbdd1-116">When you create a customer aging snapshot, use the following fields to enter information about it:</span></span>

- <span data-ttu-id="cbdd1-117">**Aegumisperioodi definitsioon** – Valige väljal loodud aegumisperioodi definitsioon.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-117">**Aging period definition** – Select the aging period definition for the aging snapshot.</span></span> <span data-ttu-id="cbdd1-118">Iga aegumisperioodi määratluse kohta saab olla üks aktiivne hetketõmmis.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-118">You can have one aging snapshot for each aging period definition.</span></span> <span data-ttu-id="cbdd1-119">Aegumise hetktõmmis ja aegumisperioodi definitsioon tuleb eraldi luua.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-119">The aging snapshot and the aging period definition must be created separately.</span></span>
- <span data-ttu-id="cbdd1-120">**Kausta ID** – Väli on valikuline.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-120">**Pool ID** – This field is optional.</span></span> <span data-ttu-id="cbdd1-121">Saate kasutada kausta, et määrata klientide komplekt, mis tuleb aegumise hetktõmmises töödelda.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-121">You can use a pool to define the set of customers that should be processed in the aging snapshot.</span></span> <span data-ttu-id="cbdd1-122">Kliendikausta valimisel rakendatakse aegumise hetktõmmise töötlemist ainult kliendikausta kuuluvatele kliendikontodele.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-122">If you select a customer pool in this field, an aging snapshot is created only for the customer accounts that are part of that customer pool.</span></span> <span data-ttu-id="cbdd1-123">Valitud kliendi kaust peab olema **Aegumise hetktõmmis** tüüpi.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-123">The selected customer pool must be of the **Aging snapshot** type.</span></span> <span data-ttu-id="cbdd1-124">Kui jätate selle välja tühjaks, luuakse aegumise hetktõmmis kõigi kliendikontode jaoks.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-124">If you leave this field blank, an aging snapshot is created for all customer accounts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cbdd1-125">Kui kliendi **Aegumisjõudluse täiustuse** funktsioon on sisse lülitatud, ärge valige kliendikausta.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-125">If the **Customer aging performance enhancement** feature is turned on, don't select a customer pool.</span></span>

- <span data-ttu-id="cbdd1-126">**Kriteeriumid** – Aegumise hetktõmmis aegub valitud kuupäeva alusel:</span><span class="sxs-lookup"><span data-stu-id="cbdd1-126">**Criteria** – The aging snapshot will age based on the date that you select:</span></span>

    - <span data-ttu-id="cbdd1-127">**Kande kuupäev** – Iga kande aegumine põhineb selle kande kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-127">**Transaction date** – Each transaction is aged based on its transaction date.</span></span>
    - <span data-ttu-id="cbdd1-128">**Tähtaeg** – Iga kande aegumine põhineb selle tähtajal.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-128">**Due date** – Each transaction is aged based on its due date.</span></span>
    - <span data-ttu-id="cbdd1-129">**Dokumendi kuupäev** – Iga kande aegumine põhineb selle dokumendi kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-129">**Document date** – Each transaction is aged based on its document date.</span></span>

- <span data-ttu-id="cbdd1-130">**Vanus alates** – Valige kuupäev, mida kasutada aegumise hetktõmmise **Praeguse kuupäevana**.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-130">**Aging as of** – Select the date to use in the **Current date** field for the aging snapshot.</span></span> <span data-ttu-id="cbdd1-131">Aegumisperioodid arvutatakse selle kuupäeva alusel.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-131">Aging periods are then calculated based on that date.</span></span> 

    - <span data-ttu-id="cbdd1-132">**Tänane kuupäev** – Kasutage süsteemi kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-132">**Today's date** – Use the system date.</span></span> <span data-ttu-id="cbdd1-133">Tehke see valik, kui töötlemine on seadistatud toimuma korduva partiina.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-133">Select this option if processing is set up to run in a recurring batch.</span></span> <span data-ttu-id="cbdd1-134">Seejärel kasutatakse iga kord partii käitamisel selle käituse süsteemikuupäeva.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-134">Then, every time that the batch is run, the system date of that run is used.</span></span>
    - <span data-ttu-id="cbdd1-135">**Valitud kuupäev** - Kasutage enda määratud kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-135">**Selected date** – Use a date that you specify.</span></span> <span data-ttu-id="cbdd1-136">Selle valiku korral peate sisestama aegumise kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-136">If you select this option, you must enter an aging date.</span></span>

    <span data-ttu-id="cbdd1-137">Näiteks on praegune aegumisperiood 30 päeva.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-137">For example, the current aging period is 30 days.</span></span> <span data-ttu-id="cbdd1-138">Kui valite sellel väljal väärtuse **Tänane kuupäev** algab praegune aegumisperiood tänasest kuupäevast ja kaasab siis eelmised 29 päeva.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-138">If you select **Today's date** in this field, the current aging period starts on today's date and then includes the previous 29 days.</span></span> <span data-ttu-id="cbdd1-139">Kui valite sellel väljal väärtuse **Valitud kuupäev** algab praegune aegumisperiood tänasest kuupäevast ja kaasab siis eelmised 29 päeva.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-139">If you select **Selected date** and enter a date, the current aging period starts on the specified date and then includes the previous 29 days.</span></span>

- <span data-ttu-id="cbdd1-140">**Värskendage märgukirja olekut** – Määrake selle valiku väärtuseks **Jah** et värskendada kannete sissenõude olekut **Sissenõuete** lehel **Lubadus maksta** **Lubadus maksta jaotatuna** kui aegumiskuupäev on pärast kuupäeva, mis on märgitud **Makse lubaduse kuupäeva** väljal.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-140">**Update collection status** – Set this option to **Yes** to update the collection status of transactions on the **Collections** page from **Promise to pay** to **Promise to pay broken** if the aging date is beyond the date in the **Promise to pay date** field.</span></span> <span data-ttu-id="cbdd1-141">Määrake selle valiku väärtuseks **Ei** kui soovite jätta sissenõuete kogumi oleku muutmata **Sissenõuete** lehel.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-141">Set this option to **No** to leave the collection status unchanged on the **Collections** page.</span></span>
- <span data-ttu-id="cbdd1-142">**Kaasa nullsaldoga kliendid** – Määrake selle suvandi väärtuseks **Jah** et kaasata kõik kliendid olenemata nende saldost.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-142">**Include customers with zero balance** – Set this option to **Yes** to include all customers, regardless of their balance.</span></span> <span data-ttu-id="cbdd1-143">Kui kaasate kõik kliendid, on soovitatav lülitada sisse **Kliendi aegumise jõudluse täiustus** funktsioon ja mitte kasutada kliendikaustu.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-143">If you include all customers, we recommend that you to turn on the **Customer aging performance enhancement** feature, and that you not use customer pools.</span></span> <span data-ttu-id="cbdd1-144">Ainult saldoga klientide kaasamiseks määrake selle valiku väärtuseks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-144">Set this option to **No** to include only customers that have a balance.</span></span> <span data-ttu-id="cbdd1-145">See säte aitab jõudlust kiirendada, kuna tasakaaluta kliendid jäetakse vahele.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-145">This setting helps speed up performance, because customers that don't have a balance are skipped.</span></span>
- <span data-ttu-id="cbdd1-146">**Ettevõtte vahemik** – Valige vahekaardil **Ettevõtte vahemik** juriidilised isikud (ettevõtted), kes kaasatakse aegumise hetktõmmisse.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-146">**Company range** – On the **Company range** tab, select the legal entities (companies) to include in the aging snapshot.</span></span> <span data-ttu-id="cbdd1-147">Valida saab ainult tsentraliseeritud maksete jaoks seadistatud juriidilisi isikuid.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-147">Only legal entities that are set up for centralized payments are available for selection.</span></span> <span data-ttu-id="cbdd1-148">Valitud juriidiliste isikute kanded kaasatakse siis aegumisperioodidesse klientide puhul, kellel on kõigis juriidilistes isikutes sama osapoole ID.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-148">Transactions from the selected legal entities are then included in the aging periods for customers that have the same party ID in all those legal entities.</span></span> <span data-ttu-id="cbdd1-149">Summad talletatakse aegumise hetktõmmise uuendamise ajal sisselogitud juriidilise isiku arvestusvaluutas.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-149">Currency amounts are converted to the currency of the legal entity that you're signed in to when you create the aging snapshot.</span></span>

<span data-ttu-id="cbdd1-150">Soovitame teil planeerida see protsess pakktöötlusena.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-150">We recommend that you schedule this process to run in a batch.</span></span>

> [!NOTE]
> <span data-ttu-id="cbdd1-151">Partii jõudluse parandamiseks aegumise hetktõmmiste loomisel sisestage number **Partiiülesannete maksimumarv** väljal **Sissenõuete vaikekaardile** kiirkaardil **Sissenõuded** vahekaardil **Müügireskontro parameetrite** lehel.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-151">To help improve batch performance when aging snapshots are created, enter a number in the **Maximum number of batch tasks** field on the **Collections defaults** FastTab on the **Collections** tab of the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="cbdd1-152">Väljal **Kliendi vanus saldod** on soovitatav alustada vaikeväärtusega **100** ja seejärel korrigeerida väärtust, et optimeerida oma olukorra töötlemist.</span><span class="sxs-lookup"><span data-stu-id="cbdd1-152">In the **Age customer balances** field, we recommend that you start with the default value of **100** and then adjust the value to optimize processing for your situation.</span></span>
