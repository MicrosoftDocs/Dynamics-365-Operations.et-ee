---
title: Vooetapi koodid
description: See teema annab ülevaate vooetapi koodidest ja nende kasutamisest.
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992353"
---
# <a name="wave-step-codes"></a><span data-ttu-id="776ce-103">Vooetapi koodid</span><span class="sxs-lookup"><span data-stu-id="776ce-103">Wave step codes</span></span>

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a><span data-ttu-id="776ce-104">Vooetapi koodid</span><span class="sxs-lookup"><span data-stu-id="776ce-104">About wave step codes</span></span>

<span data-ttu-id="776ce-105">Vooetapi koodid on koodid, mida kasutajad saavad seadistada ja kasutada vastavale mallile konkreetsete juhtumite linkimiseks.</span><span class="sxs-lookup"><span data-stu-id="776ce-105">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="776ce-106">Mallid sisaldavad malle täiendamiseks, konteineritesse panemiseks, siltide printimiseks, koormuste loomiseks ja sortimiseks.</span><span class="sxs-lookup"><span data-stu-id="776ce-106">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="776ce-107">Kui voo etapi koode ei kasutata, peavad kasutajad sisestama vaba teksti, et viidata kindlale mallile laine meetodi eksemplarist.</span><span class="sxs-lookup"><span data-stu-id="776ce-107">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="776ce-108">Vabal tekstil on kalduvus vigadeks, kuna kasutajad peavad veenduma, et voo-etapi tekst, mida nad lisavad konkreetse vooetapi meetodi jaoks voo malli puhul, vastab täpselt sihtmalli tekstile.</span><span class="sxs-lookup"><span data-stu-id="776ce-108">Free text is prone to error, because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="776ce-109">Konkreetse vooetapi tüübi vooetapi koodid seadistatakse eraldi lehel.</span><span class="sxs-lookup"><span data-stu-id="776ce-109">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="776ce-110">Voomalli iga vooetabi meetodi eksemplari korral, mis vajab vooetapi koodi, tuleb vooetapi kood valida ripploendist.</span><span class="sxs-lookup"><span data-stu-id="776ce-110">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="776ce-111">Ripploendi valik asendab vaba tekstisisestuse ja aitab vähendada inimlike vigade riski ja mõju.</span><span class="sxs-lookup"><span data-stu-id="776ce-111">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="776ce-112">Seadistuse koode kasutatakse vooetapi meetodi sidumiseks voomallis meetodi sihtmalliga.</span><span class="sxs-lookup"><span data-stu-id="776ce-112">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="776ce-113">Vooetabi koodide funktsiooni kasutamine on valikuline ja kasutamine käib iga juriidilise isiku kohta eraldi.</span><span class="sxs-lookup"><span data-stu-id="776ce-113">Use of the wave step codes feature is optional, and uptake is per legal entity.</span></span> <span data-ttu-id="776ce-114">Seetõttu, kui konkreetne juriidiline isik kasutab funktsiooni, uuendatakse kõik selle juriidilise isiku olemasolevad voo etapikoodid uude struktuuri.</span><span class="sxs-lookup"><span data-stu-id="776ce-114">Therefore, if a specific legal entity uses the feature, all existing wave step codes in that legal entity are upgraded to the new structure.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="776ce-115">Häälestuse demo</span><span class="sxs-lookup"><span data-stu-id="776ce-115">Setup demo</span></span> 

<span data-ttu-id="776ce-116">Selle demo jaoks peavad olema installitud demo andmed ja peate kasutama testandmete ettevõtet **USMF**.</span><span class="sxs-lookup"><span data-stu-id="776ce-116">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="776ce-117">Luba vooetapi koodid</span><span class="sxs-lookup"><span data-stu-id="776ce-117">Enable wave step codes</span></span>

<span data-ttu-id="776ce-118">Järgige neid samme, et lülitada sisse voo etapi koodide funktsioon.</span><span class="sxs-lookup"><span data-stu-id="776ce-118">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="776ce-119">Avage **Laohaldus \> Seadistus \> Laohalduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="776ce-119">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
2. <span data-ttu-id="776ce-120">Määrake vahekaardil **Üldine** kiirkaardil **Vootöötlus** suvand **Luba voo etapikoodid** olekusse **Jah**.</span><span class="sxs-lookup"><span data-stu-id="776ce-120">On the **General** tab, on the **Wave processing** FastTab, set the **Enable wave step codes** option to **Yes**.</span></span>

<span data-ttu-id="776ce-121">Kõik olemasolevad vooetappide vabad tekstid värskendatakse uuele struktuurile.</span><span class="sxs-lookup"><span data-stu-id="776ce-121">All existing wave step free texts are upgraded to the new structure.</span></span> <span data-ttu-id="776ce-122">Pärast seda, kui see värskendus on juriidilise isiku jaoks lõppenud, ei ole suvand **Luba voo etapikoodid** lehel **Laohalduse parameetrid** enam saadaval.</span><span class="sxs-lookup"><span data-stu-id="776ce-122">After this upgrade is completed for a legal entity, the **Enable wave step codes** option is no longer available on the **Warehouse management parameters** page.</span></span>

<span data-ttu-id="776ce-123">Kinnitused tehakse värskendamise ajal ja kui värskendus nurjub, kuvatakse tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="776ce-123">Validations are done during the upgrade, and if the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="776ce-124">Värskendamine võib nurjuda järgmiste konfliktide tõttu.</span><span class="sxs-lookup"><span data-stu-id="776ce-124">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="776ce-125">Olemas on topelt vooetapi vabad tekstid.</span><span class="sxs-lookup"><span data-stu-id="776ce-125">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="776ce-126">Olemas on kohandused.</span><span class="sxs-lookup"><span data-stu-id="776ce-126">Customizations exist.</span></span>
- <span data-ttu-id="776ce-127">Vooetapi vaba tekst, mis on seotud vooetapi meetodi eksemplariga ei vasta oodatud mallitüübile.</span><span class="sxs-lookup"><span data-stu-id="776ce-127">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="776ce-128">Pärast võimalike valideerimise ajal tuvastatud konfliktide lahendamist saate värskendusprotsessi uuesti käivitada.</span><span class="sxs-lookup"><span data-stu-id="776ce-128">After you've resolved any conflicts that are identified during the validations, you can rerun the upgrade process.</span></span>

<span data-ttu-id="776ce-129">Kui värskendus on edukas, siis on saadaval leht **Voo etapikoodid** (**Laohaldus \> Seadistus \> Vood \> Voo etapikoodid**).</span><span class="sxs-lookup"><span data-stu-id="776ce-129">When the upgrade succeeds, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="776ce-130">Sellel lehel loetletakse voo etapikoodid, mida värskendati siis, kui voo etapikoodide funktsioon sisse lülitati.</span><span class="sxs-lookup"><span data-stu-id="776ce-130">This page lists the wave step codes that were upgraded when the wave step codes feature was turned on.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="776ce-131">Uute voo etapikoodid loomine</span><span class="sxs-lookup"><span data-stu-id="776ce-131">Create new wave step codes</span></span>

<span data-ttu-id="776ce-132">Saate kasutada lehte **Voo etapikoodid** voo etapikoodide loomiseks ja kustutamiseks.</span><span class="sxs-lookup"><span data-stu-id="776ce-132">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="776ce-133">Iga uus voo etapikood ja sellega seotud ID peab olema kordumatud kõigi voo etapitüüpide puhul ja need peavad olema määratletud konkreetse voo etapitüübi jaoks.</span><span class="sxs-lookup"><span data-stu-id="776ce-133">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="776ce-134">Voo etapikoodide rakendamine</span><span class="sxs-lookup"><span data-stu-id="776ce-134">Apply wave step codes</span></span>

<span data-ttu-id="776ce-135">Kui olete määranud sobivad voo etapikoodid, saab neid rakendada vooprotsessi meetoditele.</span><span class="sxs-lookup"><span data-stu-id="776ce-135">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="776ce-136">Voo etapikoodide rakendamiseks avage sobiv sihtmall.</span><span class="sxs-lookup"><span data-stu-id="776ce-136">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="776ce-137">Siin on sihtmallid, millele ona voo etapikoodid määratud osutama.</span><span class="sxs-lookup"><span data-stu-id="776ce-137">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="776ce-138">**Täiendamise mallid:** Laohaldus \> Seadistus \> Täiendamine \> Täiendamise mallid</span><span class="sxs-lookup"><span data-stu-id="776ce-138">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="776ce-139">**Koorma loomise mallid:** Laohaldus \> Seadistus \> Koorem \> Koorma loomise mallid</span><span class="sxs-lookup"><span data-stu-id="776ce-139">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="776ce-140">**Mallide sorteerimine:** Laohaldus \> Seadistus \> Pakkimine \> Väljaminevad sortimise mallid</span><span class="sxs-lookup"><span data-stu-id="776ce-140">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="776ce-141">**Konteineritesse panemise mallid:** Laohaldus \> Seadistus \> Konteinerid \> Konteinerite loomise mallid</span><span class="sxs-lookup"><span data-stu-id="776ce-141">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="776ce-142">**Siltide printimise mallid:** Laohaldus \> Seadistus \> Dokumendi marsruutimine \> Voo sildi mallid</span><span class="sxs-lookup"><span data-stu-id="776ce-142">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="776ce-143">Selle loendi malle rakendatakse, kui need on viidatud voo protsessi meetodist, mis on valitud voo mallis.</span><span class="sxs-lookup"><span data-stu-id="776ce-143">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="776ce-144">Kui voo etapikood voo malli voo protsessi meetodis vastb ühe mallitüübi voo etapikoodile, siis mall rakendatakse.</span><span class="sxs-lookup"><span data-stu-id="776ce-144">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="776ce-145">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="776ce-145">Sample scenario</span></span>

<span data-ttu-id="776ce-146">Järgmine protseduur aitab tagada, et loodud täiendamise mall rakendub voo mallile.</span><span class="sxs-lookup"><span data-stu-id="776ce-146">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="776ce-147">Avage **Laohaldus \> Seadistus \> Vood \> Voo etapikoodid**, ja looge voo etapikood tüübile **Täiendamine**.</span><span class="sxs-lookup"><span data-stu-id="776ce-147">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="776ce-148">Avage **Laohaldus \> Seadistus \> Täiendamine \> Täiendamise mallid** ja looge täiendamise mall.</span><span class="sxs-lookup"><span data-stu-id="776ce-148">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="776ce-149">Täiendamise mallis valige see voo etapikood, mille lõite tüübile **Täiendamine**.</span><span class="sxs-lookup"><span data-stu-id="776ce-149">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="776ce-150">Avage **Laohaldus \> Seadistus \> Vood \> Voo mallid** ja valige see voo mall, mida soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="776ce-150">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="776ce-151">Valige mallis kiirkaardil **Meetodid** meetod **Täiendamine**.</span><span class="sxs-lookup"><span data-stu-id="776ce-151">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="776ce-152">Valige väljal **Voo etapikood** see voo etapikood, mille valisite täiendamise mallis.</span><span class="sxs-lookup"><span data-stu-id="776ce-152">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>
