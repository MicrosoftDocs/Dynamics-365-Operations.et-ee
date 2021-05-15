---
title: Klassid "Vähem kui koormatäis" (LTL)
description: See teema kirjeldab, mis on "vähem kui koormatäis" (LTL) klassid ja kirjeldab, kuidas neid Microsoftis Dynamics 365 Supply Chain Management seadistada.
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941806"
---
# <a name="less-than-truckload-ltl-classes"></a><span data-ttu-id="a650e-103">Klassid "Vähem kui koormatäis" (LTL)</span><span class="sxs-lookup"><span data-stu-id="a650e-103">Less than truckload (LTL) classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a650e-104">Alla "Vähem kui koormatäis" (LTL) klass on veose lähetusklass, mida kasutatakse saadetavate kaupade klassifitseerimiseks.</span><span class="sxs-lookup"><span data-stu-id="a650e-104">A less than truckload (LTL) class is a freight shipping class that is used to classify items that can be shipped.</span></span> <span data-ttu-id="a650e-105">Üldiselt on igal toote või kauba tüübil riikliku autoveose klassifikatsiooni (NMFC) kood, mis vastab LTL-saadetiste konkreetsele veoklassi numbrile.</span><span class="sxs-lookup"><span data-stu-id="a650e-105">Generally, every type of product or commodity has a National Motor Freight Classification (NMFC) code that corresponds to a specific freight class number for LTL shipments.</span></span> <span data-ttu-id="a650e-106">LTL-veoseklassid esindavad kaupade kategooriaid, samas kui NMFC-koodid on seotud kindlate kaupadega igasühes 18 veose klassist.</span><span class="sxs-lookup"><span data-stu-id="a650e-106">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span>

<span data-ttu-id="a650e-107">See funktsioon võimaldab teil oma süsteemi kasutada, et teha järgmisi toiminguid.</span><span class="sxs-lookup"><span data-stu-id="a650e-107">This feature lets you use your system to perform the following tasks:</span></span>

- <span data-ttu-id="a650e-108">Määratlege LTL-veoklassid, mida kasutatakse teie ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="a650e-108">Define the LTL freight classes that are used at your company.</span></span>
- <span data-ttu-id="a650e-109">Määrake igale NMFC-koodile **NMFC-koodide** lehel LTL-klass.</span><span class="sxs-lookup"><span data-stu-id="a650e-109">Assign each LTL class to an NMFC code on the **NMFC Codes** page.</span></span> <span data-ttu-id="a650e-110">Lisateavet vt [riikliku autoveose klassifikatsiooni (NMFC) koodidest](nmfc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a650e-110">For more information, see [National Motor Freight Classification (NMFC) codes](nmfc-codes.md).</span></span>
- <span data-ttu-id="a650e-111">Määrake NMFC-kood (ja seega ka LTL-kood) igale tootele lehel **Tooted**.</span><span class="sxs-lookup"><span data-stu-id="a650e-111">Assign an NMFC code (and therefore its associated LTL code) to each product on the **Products** page.</span></span>
- <span data-ttu-id="a650e-112">Hinnake täpselt iga toote LTL-klassi, millele NMFC-kood on määratud.</span><span class="sxs-lookup"><span data-stu-id="a650e-112">Accurately assess the LTL class of each product that an NMFC code is assigned to.</span></span>
- <span data-ttu-id="a650e-113">Määratlege iga LTL-klassi pakkimisnõuded, kontrollides rahvusvahelisi LTL-standardeid.</span><span class="sxs-lookup"><span data-stu-id="a650e-113">Determine packing requirements for each LTL class by checking the international LTL standards.</span></span> <span data-ttu-id="a650e-114">Sel viisil tagate, et teie tooted on hästi kaitstud ja turvaliselt saadetud.</span><span class="sxs-lookup"><span data-stu-id="a650e-114">In this way, you ensure that your products will be well protected and safely shipped.</span></span>
- <span data-ttu-id="a650e-115">Saate täpsed saadetise hinnangud, mis põhinevad iga toote LTL-veoklassil.</span><span class="sxs-lookup"><span data-stu-id="a650e-115">Get accurate shipping estimates, based on the LTL freight class for each product.</span></span>

<span data-ttu-id="a650e-116">Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Supply Chain Management LTL-klasse.</span><span class="sxs-lookup"><span data-stu-id="a650e-116">This topic describes how to create LTL classes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="create-an-ltl-class"></a><span data-ttu-id="a650e-117">LTL-klassi loomine</span><span class="sxs-lookup"><span data-stu-id="a650e-117">Create an LTL class</span></span>

<span data-ttu-id="a650e-118">LTL-klassi loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="a650e-118">To create an LTL class, follow these steps.</span></span>

1. <span data-ttu-id="a650e-119">Järgige üht neist sammudest.</span><span class="sxs-lookup"><span data-stu-id="a650e-119">Follow one of these steps:</span></span>

    - <span data-ttu-id="a650e-120">Minge jaotisse **Laohaldus \> Seadistus \> Inventar \> LTL-klassid**.</span><span class="sxs-lookup"><span data-stu-id="a650e-120">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
    - <span data-ttu-id="a650e-121">Avage **Transpordihaldus \> Seadistused \> Transpordistandardid \> LTL-klassid**.</span><span class="sxs-lookup"><span data-stu-id="a650e-121">Go to **Transportation management \> Setup \> Transportation standards \> LTL classes**.</span></span>

2. <span data-ttu-id="a650e-122">LTL-klassi loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a650e-122">On the Action Pane, select **New** to create an LTL class.</span></span> <span data-ttu-id="a650e-123">Seejärel määrake järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="a650e-123">Then set the following fields:</span></span>

    - <span data-ttu-id="a650e-124">**LTL-klass** – sisestage oma ettevõtte sisemine LTL-klassi kood (ID) artiklitüübi puhul.</span><span class="sxs-lookup"><span data-stu-id="a650e-124">**LTL class** – Enter your company's internal LTL class identifier (ID) for the commodity type.</span></span> <span data-ttu-id="a650e-125">Enamik ettevõtteid kasutab seda rahvusvahelist standardit.</span><span class="sxs-lookup"><span data-stu-id="a650e-125">Most companies use the international standard.</span></span> <span data-ttu-id="a650e-126">Sellisel juhul vastab selle välja väärtus välja **Klass** väärtusele.</span><span class="sxs-lookup"><span data-stu-id="a650e-126">In that case, the value of this field will match the value of the **Class** field.</span></span> <span data-ttu-id="a650e-127">Kui teie ettevõte kasutab siiski oma standardit, sisestage sellele standardile vastav kood.</span><span class="sxs-lookup"><span data-stu-id="a650e-127">However, if your company uses its own standard, enter a code that conforms to that standard.</span></span>
    - <span data-ttu-id="a650e-128">**Nimi** – sisestage kirjeldav nimi, mis aitab teil ja teistel kasutajatel valida iga NMFC-koodi jaoks õige LTL-klassi.</span><span class="sxs-lookup"><span data-stu-id="a650e-128">**Name** – Enter a descriptive name that will help you and other users select the correct LTL class for each NMFC code.</span></span>
    - <span data-ttu-id="a650e-129">**Klass** – sisestage kaubatüübi rahvusvaheline standardne LTL-klassi ID-kood.</span><span class="sxs-lookup"><span data-stu-id="a650e-129">**Class** – Enter the international standard LTL class ID for the commodity type.</span></span> <span data-ttu-id="a650e-130">Siia sisestav kood peab vastama ametlikule standardile.</span><span class="sxs-lookup"><span data-stu-id="a650e-130">The code that you enter here must conform to the official standard.</span></span>

## <a name="example-set-up-ltl-classes"></a><span data-ttu-id="a650e-131">Näide: LTL-klasside häälestamine</span><span class="sxs-lookup"><span data-stu-id="a650e-131">Example: Set up LTL classes</span></span>

<span data-ttu-id="a650e-132">Järgmine näide näitab, kuidas seadistada kahte erinevat LTL-klassi, mida saate kasutada erinevat tüüpi toodetega.</span><span class="sxs-lookup"><span data-stu-id="a650e-132">The following example shows how to set up two different LTL classes that you can use with different types of products.</span></span>

1. <span data-ttu-id="a650e-133">Minge jaotisse **Laohaldus \> Seadistus \> Inventar \> LTL-klassid**.</span><span class="sxs-lookup"><span data-stu-id="a650e-133">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
1. <span data-ttu-id="a650e-134">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a650e-134">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a650e-135">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="a650e-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a650e-136">**LTL klass:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="a650e-136">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="a650e-137">**Nimi:** *arvutid, monitorid, külmikud*</span><span class="sxs-lookup"><span data-stu-id="a650e-137">**Name:** *Computers, monitors, refrigerators*</span></span>
    - <span data-ttu-id="a650e-138">**Klass:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="a650e-138">**Class:** *92.5*</span></span>

1. <span data-ttu-id="a650e-139">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="a650e-139">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="a650e-140">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a650e-140">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a650e-141">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="a650e-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a650e-142">**LTL klass:** *125*</span><span class="sxs-lookup"><span data-stu-id="a650e-142">**LTL class:** *125*</span></span>
    - <span data-ttu-id="a650e-143">**Nimi:** *väikesed kodumajapidamisseadmed*</span><span class="sxs-lookup"><span data-stu-id="a650e-143">**Name:** *Small household appliances*</span></span>
    - <span data-ttu-id="a650e-144">**Klass:** *125*</span><span class="sxs-lookup"><span data-stu-id="a650e-144">**Class:** *125*</span></span>

1. <span data-ttu-id="a650e-145">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="a650e-145">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a650e-146">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a650e-146">Additional resources</span></span>

- [<span data-ttu-id="a650e-147">Riikliku autoveose klassifikatsiooni (NMFC) koodid</span><span class="sxs-lookup"><span data-stu-id="a650e-147">National Motor Freight Classification (NMFC) codes</span></span>](nmfc-codes.md)
- [<span data-ttu-id="a650e-148">Veokirja loomine</span><span class="sxs-lookup"><span data-stu-id="a650e-148">Create a bill of lading</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
