---
title: Rendilepingute haldamine rendilepingu importimise raamistiku kaudu
description: Selles teemas selgitatakse, kuidas kasutada rendilepingu importimise raamistikku, et korrigeerida mitut rendilepingut samaaegselt.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7df2f55f596cab54315c2da2ec0492422514f49c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971299"
---
# <a name="manage-leases-through-the-lease-import-framework"></a><span data-ttu-id="cf0d1-103">Rendilepingute haldamine rendilepingu importimise raamistiku kaudu</span><span class="sxs-lookup"><span data-stu-id="cf0d1-103">Manage leases through the Lease import framework</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf0d1-104">Selles teemas selgitatakse, kuidas kasutada rendilepingu importimise raamistikku, et korrigeerida mitut rendilepingut ühe etapina.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-104">This topic explains how to use the Lease import framework to adjust multiple leases in one step.</span></span> <span data-ttu-id="cf0d1-105">Seda võimalust kasutades saate säästa aega ja samuti saate tagada täpsemaid korrigeerimisi, vähendades inimliku vea tõenäosust.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-105">By using this capability, you can save time, and you can also ensure more accurate adjustments by reducing the chance of human error.</span></span> <span data-ttu-id="cf0d1-106">Lisaks saab see võimalus ühendada Microsoft Dynamics 365 Finance'i väliste andmete üksustega, et andmeid tõhusalt üles laadida.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-106">Additionally, this capability can connect Microsoft Dynamics 365 Finance with external data entities to efficiently upload data.</span></span>

<span data-ttu-id="cf0d1-107">Vara rentimise integreerimiseks väliste süsteemidega saab kasutada järgmisi andmeüksusi.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-107">The following data entities can be used to integrate Asset leasing with external systems:</span></span>

- <span data-ttu-id="cf0d1-108">Rendi ajastamine</span><span class="sxs-lookup"><span data-stu-id="cf0d1-108">Lease staging</span></span>
- <span data-ttu-id="cf0d1-109">Makselepingu ajastamine</span><span class="sxs-lookup"><span data-stu-id="cf0d1-109">Payment contract staging</span></span>
- <span data-ttu-id="cf0d1-110">Täitelepingu ajastamine</span><span class="sxs-lookup"><span data-stu-id="cf0d1-110">Executory contract staging</span></span>

<span data-ttu-id="cf0d1-111">Saate kasutada impordi protsessi, et korrigeerida rendilepingut, värskendada mitte-finantsteavet või lisada uusi rendilepinguid.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-111">You can use the import process to adjust a lease, update non-financial information, or add new leases.</span></span> <span data-ttu-id="cf0d1-112">Enne importimist saate rendilepingu andmeid vaadata ja redigeerida.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-112">You can view and edit the leasing data before you import it.</span></span>

<span data-ttu-id="cf0d1-113">Süsteem võib rendilepingu importimise komplekti kaudu käivitada järgmised kolm protsessi.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-113">The system can run the following three processes through the lease import suite.</span></span>

| <span data-ttu-id="cf0d1-114">Protsessi tüüp</span><span class="sxs-lookup"><span data-stu-id="cf0d1-114">Process type</span></span>  | <span data-ttu-id="cf0d1-115">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="cf0d1-115">Description</span></span> |
|---------------|-------------|
| <span data-ttu-id="cf0d1-116">Lisa kirje</span><span class="sxs-lookup"><span data-stu-id="cf0d1-116">Add record</span></span>    | <span data-ttu-id="cf0d1-117">Selle protsessi tüübiga migreeritud rendilepingud loovad süsteemis rendilepingu.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-117">Migrated leases that have this process type create a lease in the system.</span></span> <span data-ttu-id="cf0d1-118">Maksegraafik tuleb käsitsi kinnitada ja algse tuvastuse töölehe kirje tuleb pärast migreerimist käsitsi sisestada.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-118">The payment schedule must be manually confirmed, and the initial recognition journal entry must be manually posted after the migration.</span></span> |
| <span data-ttu-id="cf0d1-119">Uuenda kirje</span><span class="sxs-lookup"><span data-stu-id="cf0d1-119">Update record</span></span> | <span data-ttu-id="cf0d1-120">Selle protsessitüübiga migreeritud rendilepingud uuendavad süsteemis juba olemas oleva rendilepingu väärtuseid.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-120">Migrated leases that have this process type update field values for a lease that is already in the system.</span></span> <span data-ttu-id="cf0d1-121">Uuendatakse ainult väljad, mis on valitud lehel **Uuenda väljade valikut**.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-121">Only the fields that have been selected on the **Update fields selection** page are updated.</span></span> <span data-ttu-id="cf0d1-122">Soovitatav on valida mitte-finantsilised väljad lehel **Uuenda väljade valikut**, kuna see protsessi tüüp ei korrigeeri üürilepingut.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-122">We recommended that you select non-financial fields on the **Update fields selection** page, because this process type doesn't adjust the lease.</span></span> |
| <span data-ttu-id="cf0d1-123">Kirje korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="cf0d1-123">Adjust record</span></span> | <span data-ttu-id="cf0d1-124">Selle protsessitüübiga migreeritud rendilepingud korrigeerivad rendilepingut.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-124">Migrated leases that have this process type adjust the lease.</span></span> <span data-ttu-id="cf0d1-125">See korrigeerimine põhjustab rendilepingu kapitalirendi muutumise.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-125">This adjustment causes a financial lease modification of the lease.</span></span> <span data-ttu-id="cf0d1-126">Pärast rendilepingu töötlemist loob süsteem uue maksegraafiku, kasutades uusi andmeid rendilepingu importimise komplektist.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-126">After the lease is processed, the system creates a new payment schedule by using the new data from the lease import suite.</span></span> <span data-ttu-id="cf0d1-127">Süsteem ei kinnita maksegraafikut ega sisesta korrigeerimise töölehe kirjet.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-127">The system doesn't confirm the payment schedule or post the adjustment journal entry.</span></span> |

<span data-ttu-id="cf0d1-128">Kui andmed on tööruumi **Andmehaldus** kaudu üles laaditud, avage leht **Impordi päis** (**Vara rentimine \> Rendilepingu importimise raamistik \> Impordi päis**).</span><span class="sxs-lookup"><span data-stu-id="cf0d1-128">After information is uploaded through the **Data management** workspace, open the **Import header** page (**Asset leasing \> Lease import framework \> Import header**).</span></span> <span data-ttu-id="cf0d1-129">Sellel lehel loetletakse kõik varem loetletud kolme andmeüksuse impordid.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-129">This page lists all imports of the three data entities that were listed earlier.</span></span>

<span data-ttu-id="cf0d1-130">Rendilepingu ajastamise andmete vaatamiseks enne töötluse käitamist valige **Ajastamise andmed**.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-130">To view the lease staging data before processing is run, select **Staging data**.</span></span>

<span data-ttu-id="cf0d1-131">Võrdlemise funktsioon võimaldab teil võrrelda kirjet, mida impordite vastava kirjega, mis on juba teie süsteemis olemas.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-131">The compare function lets you compare a record that you're importing with the corresponding record that's already in your system.</span></span> <span data-ttu-id="cf0d1-132">Üksiku rendilepingu kirje võrdlemiseks valige rendileping ja seejärel valige **Võrdle**.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-132">To compare an individual lease record, select a lease, and then select **Compare**.</span></span> <span data-ttu-id="cf0d1-133">See etapp tuleks **Erinevuste** aruande loomiseks lõpule viia enne rendilepingu kirjete migreerimist.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-133">You should complete this step to generate a **Differences** report before you migrate the lease records.</span></span> <span data-ttu-id="cf0d1-134">Võrdlemise funktsioon võrdle ajastamise andmete väärtusi praegu süsteemis olevate rendilepingute väärtustega.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-134">The Compare functionality compares the values in the staging data to the values for leases that are currently in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="cf0d1-135">Võrdlemise funktsioon ei toimi rendilepingute korral, millel on protsessitüübiks **Lisa kirje**, sest seda rendilepingut pole millegagi võrrelda.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-135">The Compare functionality doesn't work for leases that have the **Add record** process type, because there is nothing to compare against that lease.</span></span>
>
> <span data-ttu-id="cf0d1-136">Mitme rendilepingu üheaegseks võrdlemiseks minge jaotisse **Vara rentimine \> Rendilepingu importi raamistik \> Perioodiline \> Võrdlemine** ja valige **Võrdle**.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-136">To compare multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Compare**, and select **Compare**.</span></span>

<span data-ttu-id="cf0d1-137">Iga üksuse puhul saate vaadata praegu süsteemis olemasoleva ja ajastamise tabelites oleva erinevusi.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-137">For each entity, you can view the differences between what is currently in the system and what is in the staging tables.</span></span> <span data-ttu-id="cf0d1-138">Iga ajastamise tabelites oleva üksuse kohta valige **Vaata erinevusi**.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-138">For each entity in the staging tables, select **See differences**.</span></span> <span data-ttu-id="cf0d1-139">Kuvatavas dialoogiaknas on näha praegune väärtus ja pakutav ajastamise väärtus.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-139">The dialog box that appears shows the current value and the proposed staging value.</span></span>

<span data-ttu-id="cf0d1-140">Saate ajastamise väärtust uuendada nii, et vahetate selle veerus **Uus väärtus** ja valite käsu **Uuenda ajastamine**.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-140">You can also update the staging value by changing it in the **New Value** column and then selecting **Update staging**.</span></span>

<span data-ttu-id="cf0d1-141">Saate rendilepinguid valideerida, veendumaks, et kirjed saab ilma vigu tekitamata süsteemi tuua.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-141">You can validate leases to ensure that the records can be brought into the system without introducing errors.</span></span> <span data-ttu-id="cf0d1-142">Enne rendilepingu kirje migreerimist käitab süsteem mitu valideerimist, et tagada kirje edukas importimine.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-142">Before a lease record is migrated, the system runs several validations to ensure that the record will be successfully imported.</span></span> <span data-ttu-id="cf0d1-143">Üksiku rendilepingu valideerimiseks valige käsk **Valideeri**.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-143">To validate an individual lease, select **Validate**.</span></span>

> [!NOTE]
> <span data-ttu-id="cf0d1-144">Mitme rendilepingu üheaegseks valideerimiseks minge jaotisse **Vara rentimine \> Rendilepingu importi raamistik \> Perioodiline \> Valideerimine** ja valige **Võrdle**.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-144">To validate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Validate**, and select **Compare**.</span></span>

<span data-ttu-id="cf0d1-145">Üksiku rendilepingu töötlemiseks valige käsk **Migreeri rendilepingu kirjed** lehel **Impordi päis**.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-145">To process an individual lease, select **Migrate lease records** on the **Import header** page.</span></span> <span data-ttu-id="cf0d1-146">Kui rendileping on migreeritud, teostab süsteem toimingu, mis on määratletud väljal **Protsessi tüüp**.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-146">When a lease is migrated, the system performs the action that is specified in the **Process type** field.</span></span>

> [!NOTE]
> <span data-ttu-id="cf0d1-147">Mitme rendilepingu üheaegseks valideerimiseks minge jaotisse **Vara rentimine \> Rendilepingu importi raamistik \> Perioodiline \> Valideerimine** ja valige **Võrdle**.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-147">To validate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Validate**, and select **Compare**.</span></span>

<span data-ttu-id="cf0d1-148">Pärast rendilepingute võrdlemist saate käitada aruannet, et vaadata iga impordi ID-s sisalduva rendilepingu erinevusi.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-148">After the leases are compared, you can run a report to view the differences for each lease that is included in the import ID.</span></span> <span data-ttu-id="cf0d1-149">Ühe rendilepingu kohta aruande loomiseks valige see rendileping ajastamise andmetest ja seejärel avage jaotis **Võrdle ja kuva aruanne \> Erinevuste aruanne**.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-149">To run the report for one lease, select that lease in the staging data, and then select **Compare and view report \> Differences report**.</span></span>

> [!NOTE]
> <span data-ttu-id="cf0d1-150">Mitme rendilepingu üheaegseks valideerimiseks minge jaotisse **Vara rentimine \> Päringud ja aruanded \> Erinevuste aruanne** ja valige **Võrdle**.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-150">To validate multiple leases at the same time, go to **Asset leasing \> Inquiries and reports \> Differences report**, and select **Compare**.</span></span>

## <a name="set-up-update-fields"></a><span data-ttu-id="cf0d1-151">Uuendusväljade seadistamine</span><span class="sxs-lookup"><span data-stu-id="cf0d1-151">Set up update fields</span></span>

<span data-ttu-id="cf0d1-152">Kui kasutate rendilepingute uuendamiseks rendilepingute importimise raamistikku ja protsessi tüübiks on **Uuenda kirje**, saate valida uuendamiseks kindlad väljad.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-152">If you're using the Lease import framework to update leases, and the process type is **Update record**, you can select specific fields to update.</span></span>

1. <span data-ttu-id="cf0d1-153">Avage **Vara rentimine \> Rendilepingu importimise raamistik \> Seadistus \> Uuendatava välja valik**.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-153">Go to **Asset leasing \> Lease import framework \> Setup \> Update field selection**.</span></span>
2. <span data-ttu-id="cf0d1-154">Valige kuvataval leheküljel väljad, mida uuendada, ja seejärel valige roheline nool, et teisaldada need loendisse **Valitud väljad**.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-154">On the page that appears, select the fields to update, and then select the green arrow to move them to the **Selected fields** list.</span></span> <span data-ttu-id="cf0d1-155">Ainult loendis **Valitud väljad** olevaid välju saab rendilepingu importimise komplektiga uuendada.</span><span class="sxs-lookup"><span data-stu-id="cf0d1-155">Only fields in the **Selected fields** list can be updated by using the lease import suite.</span></span>
