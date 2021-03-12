---
title: Komplekteerimise ja pakkimise tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada komplekteerimisel ja pakkimisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2cce1038ed393fc8a7bb489a37fc0921b0ac755e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993925"
---
# <a name="troubleshoot-picking-and-packing"></a><span data-ttu-id="64870-103">Komplekteerimise ja pakkimise tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="64870-103">Troubleshoot picking and packing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64870-104">Selles teemas kirjeldatakse, kuidas lahendada komplekteerimisel ja pakkimisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.</span><span class="sxs-lookup"><span data-stu-id="64870-104">This topic describes how to fix common issues that you might encounter while you pick and pack in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a><span data-ttu-id="64870-105">Kuvatakse järgmine tõrketeade: "Dimensiooni asukohta ei saa jätta tühjaks, kui on seatud dimensiooni seerianumber."</span><span class="sxs-lookup"><span data-stu-id="64870-105">I receive the following error message: "Dimension location can't be left blank if dimension serial number is set."</span></span>

### <a name="issue-description"></a><span data-ttu-id="64870-106">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="64870-106">Issue description</span></span>

<span data-ttu-id="64870-107">See tõrketeade kuvatakse, kui loote seeriaüksusele üleviimistellimuse, kasutades ladu, mis on lubatud täiustatud laohalduse (WMS) jaoks, ja proovite pärast töö lõpetamist saadetist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="64870-107">You receive this error message if you create a transfer order for a serial item by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="64870-108">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="64870-108">Issue resolution</span></span>

<span data-ttu-id="64870-109">**Lao vastuvõtu vaikimisi asukoht** on "päritolu" lao transiidilao jaoks on tühi.</span><span class="sxs-lookup"><span data-stu-id="64870-109">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="64870-110">Probleemi lahendamiseks määrake transiidilaos vaikimisi vastuvõtu asukoht.</span><span class="sxs-lookup"><span data-stu-id="64870-110">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="64870-111">Veenduge, et see asukoht on identifitseerimisnumbritega kontrollitav.</span><span class="sxs-lookup"><span data-stu-id="64870-111">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a><span data-ttu-id="64870-112">Kuvatakse järgmine tõrketeade: "Vigane identifitseerimisnumber".</span><span class="sxs-lookup"><span data-stu-id="64870-112">I receive the following error message: "Invalid license plate."</span></span>

### <a name="issue-description"></a><span data-ttu-id="64870-113">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="64870-113">Issue description</span></span>

<span data-ttu-id="64870-114">See tõrketeade kuvatakse laorakenduses, kui skaneerite identifitseerimisnumbri või asukoha.</span><span class="sxs-lookup"><span data-stu-id="64870-114">You receive this error message in the warehouse app when you scan a license plate ID.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="64870-115">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="64870-115">Issue resolution</span></span>

<span data-ttu-id="64870-116">Veenduge, et identifitseerimisnumbri ID on olemas identifitseerimisnumbrite tabelis ja et identifitseerimisnumbril olevad kaubad ja kogused on saadaval (ehk need ei ole blokeeritud).</span><span class="sxs-lookup"><span data-stu-id="64870-116">Make sure that the license plate ID exists in the license plates table, and that the items and quantities on the license plate are available (in other words, they aren't blocked).</span></span>

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a><span data-ttu-id="64870-117">Kuvatakse järgmine tõrketeade: "Välja 'koorma kaal' (=-%1) võib sisaldada ainult positiivseid numbreid.</span><span class="sxs-lookup"><span data-stu-id="64870-117">I receive the following error message: "Field 'Load weight'(=-%1) can only contain positive numbers.</span></span> <span data-ttu-id="64870-118">Uuendus on tühistatud."</span><span class="sxs-lookup"><span data-stu-id="64870-118">Update has been canceled."</span></span>

### <a name="issue-description"></a><span data-ttu-id="64870-119">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="64870-119">Issue description</span></span>

<span data-ttu-id="64870-120">Te saate selle tõrketeate, kui on avatud töö töödeldes tööd pakkimisasukohtadest vaheasukohtadesse või vaheasukohtadest dokkimisasukohtadesse.</span><span class="sxs-lookup"><span data-stu-id="64870-120">You receive this error message if there is open work when you process work from packing locations to staging locations, or from staging locations to dock locations.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="64870-121">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="64870-121">Issue resolution</span></span>

<span data-ttu-id="64870-122">Selle probleemi lahendamiseks minge **Süsteemi administreerimise \> Perioodilised ülesanded \> Andmebaas \> Järjepidevuse kontroll** ja käivitage protsess **Lao koormuse kaalu järjepidevuse kontrollimiseks**.</span><span class="sxs-lookup"><span data-stu-id="64870-122">To fix this issue, go to **System administration \> Periodic tasks \> Database \> Consistency check**, and run the process for **Warehouse load weight consistency check**.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="64870-123">Kuvatakse järgmine tõrketeade: "Kogus on kehtetu kauba %1 korral."</span><span class="sxs-lookup"><span data-stu-id="64870-123">I receive the following error message: "The quantity is not valid for unit %1."</span></span>

### <a name="issue-description"></a><span data-ttu-id="64870-124">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="64870-124">Issue description</span></span>

<span data-ttu-id="64870-125">Te saate selle tõrketeate, kui püüate sooritada *tükeldatud komplekteerimist* mitme partii üleselt.</span><span class="sxs-lookup"><span data-stu-id="64870-125">You receive this error message when you try to perform a *split pick* across multiple batches.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="64870-126">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="64870-126">Issue resolution</span></span>

<span data-ttu-id="64870-127">Laotööline peab laorakenduses kasutama *Lühikese komplekteerimise* protsessi.</span><span class="sxs-lookup"><span data-stu-id="64870-127">The warehouse worker must use the *Short picking* process in the warehouse app.</span></span> <span data-ttu-id="64870-128">Kui proovite komplekteerida mitut partiid samast asukohast, saate laorakenduses kasutada ka **Täielikku** valikut.</span><span class="sxs-lookup"><span data-stu-id="64870-128">If you're trying to pick multiple batches from the same location, you can also use the **Full** option in the warehouse app.</span></span>

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a><span data-ttu-id="64870-129">Ma ei saa liigutada kaupa asukohta, mis on identifitseerimisnumbri järgi kontrollitud.</span><span class="sxs-lookup"><span data-stu-id="64870-129">I can't move inventory to a location that is license plate–controlled.</span></span>

### <a name="issue-description"></a><span data-ttu-id="64870-130">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="64870-130">Issue description</span></span>

<span data-ttu-id="64870-131">Koormal ei saa vähendada komplekteeritud koguseid.</span><span class="sxs-lookup"><span data-stu-id="64870-131">You can't reduce picked quantities on a load.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="64870-132">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="64870-132">Issue resolution</span></span>

<span data-ttu-id="64870-133">Varasematel versioonidel ei saa koormal vähendada komplekteeritud koguseid.</span><span class="sxs-lookup"><span data-stu-id="64870-133">In earlier versions, you can't reduce picked quantities on a load.</span></span> <span data-ttu-id="64870-134">Siiski saate nüüd komplekteerimise tühistada identifitseerimisnumbri järgi kontrollitud asukohta.</span><span class="sxs-lookup"><span data-stu-id="64870-134">However, you can now unpick to a license plate–controlled location.</span></span> <span data-ttu-id="64870-135">Peate koormaliinile määrama nii **Asukoha** väärtuse kui ka **Identifitseerimisnumbri** väärtuse **Komplekteeritud koguse vähendamise** lehel.</span><span class="sxs-lookup"><span data-stu-id="64870-135">You must specify both a **Location** value and a **License plate** value for the load line on the **Reduce picked quantity** page.</span></span>

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a><span data-ttu-id="64870-136">Kas ma saan printida saatelehe või pakkimise sisu lao järgi?</span><span class="sxs-lookup"><span data-stu-id="64870-136">Can I print a delivery note or packing content by warehouse?</span></span>

### <a name="issue-description"></a><span data-ttu-id="64870-137">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="64870-137">Issue description</span></span>

<span data-ttu-id="64870-138">Soovite printida saatelehe või pakendi sisu lao või saidi alusel **Töö auditi malli rea uuendamise** lehel.</span><span class="sxs-lookup"><span data-stu-id="64870-138">You want to print a delivery note or packing content by warehouse or site on the **Work audit template line update** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="64870-139">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="64870-139">Issue resolution</span></span>

<span data-ttu-id="64870-140">Kui prindite dokumendi prindihalduse sätete abil, piirake prindihalduse kaudu ulatus (sait/ladu), selle asemel, et valida **Redigeeri printimissätted** käsk **Töö auditi malli rea uuendamise** lehel.</span><span class="sxs-lookup"><span data-stu-id="64870-140">When you print a document by using Print management settings, limit the scope (site/warehouse) through Print management instead of by selecting **Edit print settings** on the **Work audit template line update** page.</span></span>

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a><span data-ttu-id="64870-141">Pärast müügitellimusest sisestamist ei saa saatelehte tühistada.</span><span class="sxs-lookup"><span data-stu-id="64870-141">I can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="64870-142">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="64870-142">Issue description</span></span>

<span data-ttu-id="64870-143">Kui komplekteerimislehe ja saatmise protsessid on WMS-i jaoks lubatud, ei saa te saatelehte pärast müügitellimusest sisestamist tühistada.</span><span class="sxs-lookup"><span data-stu-id="64870-143">When picking and shipping processes are enabled for WMS, you can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="64870-144">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="64870-144">Issue resolution</span></span>

<span data-ttu-id="64870-145">WMS-i jaoks lubatud kaupade sisestatud saatelehtede korrigeerimiseks peab sisestus olema tehtud koormast, mitte otse tellimusest.</span><span class="sxs-lookup"><span data-stu-id="64870-145">To correct posted packing slips for items that are enabled for WMS, the posting must occur from the load, not from the order.</span></span> <span data-ttu-id="64870-146">Microsoft on seda probleemi hinnanud ja on määranud, et see on funktsiooni piirang.</span><span class="sxs-lookup"><span data-stu-id="64870-146">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="64870-147">Üldiselt võib Müügitellimus, mis on komplekteeritud ja veetud laohalduse protsesside kaudu, olla saatelehega – uuendatud koormast või saadetisest ja müügitellimuse dokumendist.</span><span class="sxs-lookup"><span data-stu-id="64870-147">In general, a sales order that has been picked and shipped through warehouse management processes can be packing slip–updated from the load or shipment and the sales order document itself.</span></span> <span data-ttu-id="64870-148">Kuid saatelehe uuendamisel müügitellimuse dokumendilt ei saa saatelehe tühistamist siiski teha koorma-või müügitellimusest.</span><span class="sxs-lookup"><span data-stu-id="64870-148">However, if you packing slip–update the sales order from the sales order document, packing slip reversal still can't be done from the load or sales order.</span></span> <span data-ttu-id="64870-149">Seetõttu soovitame kasutada koormast saatelehe sisestamist.</span><span class="sxs-lookup"><span data-stu-id="64870-149">Therefore, we recommend that you use the packing slip posting from the load.</span></span> <span data-ttu-id="64870-150">Sellisel juhul lubatakse tagasivõttu, mis tuleb teha koormast.</span><span class="sxs-lookup"><span data-stu-id="64870-150">In this case, the reversal that must be done from the load will be enabled.</span></span>

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a><span data-ttu-id="64870-151">Kuvatakse järgmine veateade: „Kogumi jaoks ei leidu piisavalt tööd”.</span><span class="sxs-lookup"><span data-stu-id="64870-151">I receive the following error message: "Not enough work can be found for cluster."</span></span>

### <a name="issue-description"></a><span data-ttu-id="64870-152">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="64870-152">Issue description</span></span>

<span data-ttu-id="64870-153">Kui kasutate *Süsteemi suunatud kogumi komplekteerimise* protsessi, kui konfigureerite kogumi profiili, kus näiteks 10 positsiooni saab komplekteerida, toimib protsess plaanipäraselt, kui on piisavalt tööd, et komplekteerida 10 positsiooni.</span><span class="sxs-lookup"><span data-stu-id="64870-153">When you use the *System directed cluster picking* process, if you configure a cluster profile where, for example, 10 positions can be picked, the process works as planned when there is enough work to pick to 10 positions.</span></span> <span data-ttu-id="64870-154">Kuid kui komplekteerimiseks on ainult kaheksa positsiooni, kuvatakse see tõrketeade, sest ühe kogumi jaoks ei ole piisavalt tööd.</span><span class="sxs-lookup"><span data-stu-id="64870-154">However, if there are only eight positions to pick, you receive this error message, because there isn't enough work for one cluster.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="64870-155">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="64870-155">Issue resolution</span></span>

<span data-ttu-id="64870-156">Probleemi lahendamiseks redigeerige kogumi profiili ja seadke suvandi **Aktiveeri positsioone** väärtuseks *Ei*.</span><span class="sxs-lookup"><span data-stu-id="64870-156">To fix this issue, edit the cluster profile, and set the **Activate positions** option to *No*.</span></span>
