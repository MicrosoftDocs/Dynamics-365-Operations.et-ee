---
title: Tasud mittevastavusega toimingute eest
description: See teema kirjeldab, kuidas luua kvaliteeditasusid, mida saab kasutada mittevastavuse toimingute puhul.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfa424e94048aa9eb1ce4da9aa69e8d4df71cefb
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956622"
---
# <a name="charges-for-nonconformance-operations"></a><span data-ttu-id="0b406-103">Tasud mittevastavusega toimingute eest</span><span class="sxs-lookup"><span data-stu-id="0b406-103">Charges for nonconformance operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b406-104">See teema kirjeldab, kuidas luua kvaliteeditasusid, mida saab kasutada mittevastavuse toimingute puhul.</span><span class="sxs-lookup"><span data-stu-id="0b406-104">This topic describes how to create quality charges that can be used with operations for a nonconformance.</span></span>

<span data-ttu-id="0b406-105">Kasutage lehte **Kvaliteedikulud**, et määratleda tasude klassifikatsioon, mida kasutatakse mittevastavustega seotud toimingutes.</span><span class="sxs-lookup"><span data-stu-id="0b406-105">You use the **Quality charges** page to define the types of charges that can be added to operations for a nonconformance.</span></span> <span data-ttu-id="0b406-106">Tasud võimaldavad teil jälgida üksikasju tasude kohta, mida võlgnete kliendile nõuetele mittevastavate toodete eest või mida hankija võlgneb teile mittevastavate toodete eest.</span><span class="sxs-lookup"><span data-stu-id="0b406-106">Charges let you track details about fees or charges that you owe to a customer for nonconforming products, or that a vendor owes to you for nonconforming products that you received.</span></span> <span data-ttu-id="0b406-107">Võite kasutada ka tasusid kulude jälgimiseks, mis on vajalikud välistele hankijatele või teenustele toimingu sooritamiseks.</span><span class="sxs-lookup"><span data-stu-id="0b406-107">You might also use charges to track costs that are required for external vendors or services to perform an operation.</span></span>

## <a name="examples-of-quality-charges"></a><span data-ttu-id="0b406-108">Kvaliteeditasude näited</span><span class="sxs-lookup"><span data-stu-id="0b406-108">Examples of quality charges</span></span>

<span data-ttu-id="0b406-109">Te töötate tootmisettevõttes.</span><span class="sxs-lookup"><span data-stu-id="0b406-109">You work for a manufacturing company.</span></span> <span data-ttu-id="0b406-110">Teie ettevõttel on lepingud mitme hankijaga.</span><span class="sxs-lookup"><span data-stu-id="0b406-110">Your company has contracts with several vendors.</span></span> <span data-ttu-id="0b406-111">Nendes lepingutes esitatakse kaupadele tähtajalise saadetise, kahjude ja toote kvaliteedi normid.</span><span class="sxs-lookup"><span data-stu-id="0b406-111">Those contracts outline standards for on-time shipment, damages, and product quality for items.</span></span> <span data-ttu-id="0b406-112">Näiteks on mitmel kliendil teie ettevõttega sõlmitud kokkulepped tagastuste, kahjude ja toote kvaliteedi kohta.</span><span class="sxs-lookup"><span data-stu-id="0b406-112">Likewise, several of your customers have agreements with your company about returns, damages, and product quality.</span></span>

<span data-ttu-id="0b406-113">Tasustruktuur määratakse igale lepingule ja täpsustatakse lepingus.</span><span class="sxs-lookup"><span data-stu-id="0b406-113">A fee structure is defined for each circumstance and specified in the contract.</span></span> <span data-ttu-id="0b406-114">Saate konfigureerida kvaliteeditasud liigendatult erinevat tüüpi tasude eristamiseks, nagu *Kahjud*, *Hilinenud saadetis* ja *Kvaliteet*.</span><span class="sxs-lookup"><span data-stu-id="0b406-114">You can configure quality charges to outline the various types of charges, such as *Damages*, *Late shipment*, and *Quality*.</span></span> <span data-ttu-id="0b406-115">Seejärel mittevastavuse loomisel lisate ühe või mitu toimingu.</span><span class="sxs-lookup"><span data-stu-id="0b406-115">Then, when you create a nonconformance, you add one or more operations.</span></span> <span data-ttu-id="0b406-116">Iga toimingu puhul valite **Tasud**, et määratleda tasude üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="0b406-116">For each operation, you select **Charges** to define the details about the fees.</span></span>

## <a name="create-a-quality-charge"></a><span data-ttu-id="0b406-117">Kvaliteeditasu loomine</span><span class="sxs-lookup"><span data-stu-id="0b406-117">Create a quality charge</span></span>

1. <span data-ttu-id="0b406-118">Avage **Laohaldus \> Seadistus \> Kvaliteedijuhtimine \> Kvaliteeditasud**.</span><span class="sxs-lookup"><span data-stu-id="0b406-118">Go to **Inventory management \> Setup \> Quality management \> Quality charges**.</span></span>
1. <span data-ttu-id="0b406-119">Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="0b406-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="0b406-120">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="0b406-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="0b406-121">**Tasude kood** – sisestage kvaliteeditasu kordumatu ID või nimi.</span><span class="sxs-lookup"><span data-stu-id="0b406-121">**Charges code** – Enter a unique ID or name for the quality charge.</span></span>
    - <span data-ttu-id="0b406-122">**Kirjeldus** – sisestage kvaliteeditasu detailne kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="0b406-122">**Description** – Enter a detailed description of the quality charge.</span></span>

1. <span data-ttu-id="0b406-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0b406-123">Close the page.</span></span>

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a><span data-ttu-id="0b406-124">Mittevastavuse toimingule kvaliteeditasu lisamine</span><span class="sxs-lookup"><span data-stu-id="0b406-124">Add a quality charge to an operation for a nonconformance</span></span>

<span data-ttu-id="0b406-125">Mittevastavustele toimingute lisamise ja nende kulude lisamise üksikasju vt [Mittevastavuse toimingud](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="0b406-125">For details about how to add operations to a nonconformance and apply charges to them, see [Operations for nonconformances](quality-operations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0b406-126">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0b406-126">Additional resources</span></span>

- [<span data-ttu-id="0b406-127">Kvaliteedijuhtimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="0b406-127">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="0b406-128">Kvaliteedi ja mittevastavuse haldamise lubamine</span><span class="sxs-lookup"><span data-stu-id="0b406-128">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="0b406-129">Mittevastavuste kinnitamise eest vastutavad töötajad</span><span class="sxs-lookup"><span data-stu-id="0b406-129">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="0b406-130">Mittevastavuste garantiitsoonid</span><span class="sxs-lookup"><span data-stu-id="0b406-130">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="0b406-131">Mittevastavuste diagnostika tüübid</span><span class="sxs-lookup"><span data-stu-id="0b406-131">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="0b406-132">Kvaliteeditasud mittevastavustele</span><span class="sxs-lookup"><span data-stu-id="0b406-132">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="0b406-133">MIttevastavuste toimingud</span><span class="sxs-lookup"><span data-stu-id="0b406-133">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="0b406-134">Laoprotsesside kvaliteedijuhtimine</span><span class="sxs-lookup"><span data-stu-id="0b406-134">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
