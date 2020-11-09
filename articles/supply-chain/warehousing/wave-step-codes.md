---
title: Vooetapi koodid
description: See teema annab ülevaate vooetapi koodidest ja nende kasutamisest.
author: josaw1
manager: tfehr
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveStepCode, WHSReplenishmentTemplates, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9332e45f7213ed815e4417969b617256778598db
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017801"
---
# <a name="wave-step-codes"></a><span data-ttu-id="6d6b7-103">Vooetapi koodid</span><span class="sxs-lookup"><span data-stu-id="6d6b7-103">Wave step codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d6b7-104">Vooetapi koodid on koodid, mida kasutajad saavad seadistada ja kasutada vastavale mallile konkreetsete juhtumite linkimiseks.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-104">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="6d6b7-105">Mallid sisaldavad malle täiendamiseks, konteineritesse panemiseks, siltide printimiseks, koormuste loomiseks ja sortimiseks.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-105">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="6d6b7-106">Kui voo etapi koode ei kasutata, peavad kasutajad sisestama vaba teksti, et viidata kindlale mallile laine meetodi eksemplarist.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-106">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="6d6b7-107">Vabal tekstil on kalduvus vigadeks, kuna kasutajad peavad veenduma, et vooetapi tekst, mida nad lisavad konkreetse vooetapi meetodi jaoks voo malli puhul, vastab täpselt sihtmalli tekstile.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-107">Free text is prone to errors because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="6d6b7-108">Konkreetse vooetapi tüübi vooetapi koodid seadistatakse eraldi lehel.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-108">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="6d6b7-109">Voomalli iga vooetabi meetodi eksemplari korral, mis vajab vooetapi koodi, tuleb vooetapi kood valida ripploendist.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-109">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="6d6b7-110">Ripploendi valik asendab vaba tekstisisestuse ja aitab vähendada inimlike vigade riski ja mõju.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-110">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="6d6b7-111">Seadistuse koode kasutatakse vooetapi meetodi sidumiseks voomallis meetodi sihtmalliga.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-111">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="6d6b7-112">Vooetapi koodide funktsiooni kasutamine on valikuline.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-112">Use of the wave step codes feature is optional.</span></span> <span data-ttu-id="6d6b7-113">See on organisatsiooniüleselt kõigi juriidiliste isikute jaoks lubatud.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-113">It is enabled organization-wide for all legal entities.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="6d6b7-114">Häälestuse demo</span><span class="sxs-lookup"><span data-stu-id="6d6b7-114">Setup demo</span></span> 

<span data-ttu-id="6d6b7-115">Selle demo jaoks peavad olema installitud demo andmed ja peate kasutama testandmete ettevõtet **USMF**.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-115">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="6d6b7-116">Luba vooetapi koodid</span><span class="sxs-lookup"><span data-stu-id="6d6b7-116">Enable wave step codes</span></span>

<span data-ttu-id="6d6b7-117">Järgige neid samme, et lülitada sisse voo etapi koodide funktsioon.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-117">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="6d6b7-118">Avage suvand **Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-118">Go to **Feature Management**.</span></span>
2. <span data-ttu-id="6d6b7-119">Valige, et lubada funktsioon nimega **Organisatsiooniülene vooetapi kood**.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-119">Select to enable the feature called **Organization-wide Wave Step Code**.</span></span>

<span data-ttu-id="6d6b7-120">Kõik olemasolevad vooetappide vabad tekstid kõikide juriidiliste isikute puhul värskendatakse uuele struktuurile.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-120">All existing wave step free texts in all legal entities are upgraded to the new structure.</span></span> <span data-ttu-id="6d6b7-121">Pärast seda, kui see värskendus on kõikide juriidiliste isikute jaoks lõpetatud, on see funktsioon lubatud.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-121">After this upgrade is completed for all legal entities, then the feature is enabled.</span></span> <span data-ttu-id="6d6b7-122">Kui funktsiooni ei saa ühe või mitme juriidilise isiku puhul lubada, siis pole funktsioon üheski juriidilises isikus lubatud.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-122">If the feature cannot be enabled for one or more legal entities, then the feature is not enabled for any legal entities.</span></span>

<span data-ttu-id="6d6b7-123">Lubamise ajal teostatakse andmete uuendamise ajal kinnitamised.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-123">During the enablement, validations are done during the data upgrade.</span></span> <span data-ttu-id="6d6b7-124">Kui uuendamine ebaõnnestub, kuvatakse tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-124">If the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="6d6b7-125">Värskendamine võib nurjuda järgmiste konfliktide tõttu.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-125">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="6d6b7-126">Olemas on topelt vooetapi vabad tekstid.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-126">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="6d6b7-127">Olemas on kohandused.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-127">Customizations exist.</span></span>
- <span data-ttu-id="6d6b7-128">Vooetapi vaba tekst, mis on seotud vooetapi meetodi eksemplariga ei vasta oodatud mallitüübile.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-128">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="6d6b7-129">Pärast võimalike kinnitamise ajal tuvastatud konfliktide lahendamist saate proovida funktsiooni uuesti lubada.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-129">After you've resolved any conflicts that are identified during the validations, you can retry to enable the feature.</span></span>

<span data-ttu-id="6d6b7-130">Kui funktsioon on lubatud, siis muutub leht **Voo etapikoodid** ( **Laohaldus \> Seadistus \> Vood \> Voo etapikoodid** ) kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-130">When the feature has been enabled, the **Wave step codes** page ( **Warehouse management \> Setup \> Waves \> Wave step codes** ) becomes available.</span></span> <span data-ttu-id="6d6b7-131">Sellel lehel loetletakse voo etapikoodid, mida värskendati siis, kui organisatsiooniülene voo etapikoodide funktsioon lubati.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-131">This page lists the wave step codes that were upgraded when the Organization-wide Wave Step Code feature was enabled.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="6d6b7-132">Uute voo etapikoodid loomine</span><span class="sxs-lookup"><span data-stu-id="6d6b7-132">Create new wave step codes</span></span>

<span data-ttu-id="6d6b7-133">Saate kasutada lehte **Voo etapikoodid** voo etapikoodide loomiseks ja kustutamiseks.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-133">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="6d6b7-134">Iga uus voo etapikood ja sellega seotud ID peab olema kordumatud kõigi voo etapitüüpide puhul ja need peavad olema määratletud konkreetse voo etapitüübi jaoks.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-134">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="6d6b7-135">Voo etapikoodide rakendamine</span><span class="sxs-lookup"><span data-stu-id="6d6b7-135">Apply wave step codes</span></span>

<span data-ttu-id="6d6b7-136">Kui olete määranud sobivad voo etapikoodid, saab neid rakendada vooprotsessi meetoditele.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-136">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="6d6b7-137">Voo etapikoodide rakendamiseks avage sobiv sihtmall.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-137">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="6d6b7-138">Siin on sihtmallid, millele ona voo etapikoodid määratud osutama.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-138">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="6d6b7-139">**Täiendamise mallid:** Laohaldus \> Seadistus \> Täiendamine \> Täiendamise mallid</span><span class="sxs-lookup"><span data-stu-id="6d6b7-139">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="6d6b7-140">**Koorma loomise mallid:** Laohaldus \> Seadistus \> Koorem \> Koorma loomise mallid</span><span class="sxs-lookup"><span data-stu-id="6d6b7-140">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="6d6b7-141">**Mallide sorteerimine:** Laohaldus \> Seadistus \> Pakkimine \> Väljaminevad sortimise mallid</span><span class="sxs-lookup"><span data-stu-id="6d6b7-141">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="6d6b7-142">**Konteineritesse panemise mallid:** Laohaldus \> Seadistus \> Konteinerid \> Konteinerite loomise mallid</span><span class="sxs-lookup"><span data-stu-id="6d6b7-142">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="6d6b7-143">**Siltide printimise mallid:** Laohaldus \> Seadistus \> Dokumendi marsruutimine \> Voo sildi mallid</span><span class="sxs-lookup"><span data-stu-id="6d6b7-143">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="6d6b7-144">Selle loendi malle rakendatakse, kui need on viidatud voo protsessi meetodist, mis on valitud voo mallis.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-144">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="6d6b7-145">Kui voo etapikood voo malli voo protsessi meetodis vastb ühe mallitüübi voo etapikoodile, siis mall rakendatakse.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-145">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="6d6b7-146">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="6d6b7-146">Sample scenario</span></span>

<span data-ttu-id="6d6b7-147">Järgmine protseduur aitab tagada, et loodud täiendamise mall rakendub voo mallile.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-147">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="6d6b7-148">Avage **Laohaldus \> Seadistus \> Vood \> Voo etapikoodid** , ja looge voo etapikood tüübile **Täiendamine**.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-148">Go to **Warehouse management \> Setup \> Waves \> Wave step codes** , and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="6d6b7-149">Avage **Laohaldus \> Seadistus \> Täiendamine \> Täiendamise mallid** ja looge täiendamise mall.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-149">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates** , and create a replenishment template.</span></span>
3. <span data-ttu-id="6d6b7-150">Täiendamise mallis valige see voo etapikood, mille lõite tüübile **Täiendamine**.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-150">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="6d6b7-151">Avage **Laohaldus \> Seadistus \> Vood \> Voo mallid** ja valige see voo mall, mida soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates** , and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="6d6b7-152">Valige mallis kiirkaardil **Meetodid** meetod **Täiendamine**.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-152">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="6d6b7-153">Valige väljal **Voo etapikood** see voo etapikood, mille valisite täiendamise mallis.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-153">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>

<span data-ttu-id="6d6b7-154">Sooritate need sammud iga juriidilise isiku puhul.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-154">You perform these steps for each legal entity.</span></span>
