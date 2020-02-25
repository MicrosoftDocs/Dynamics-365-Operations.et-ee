---
title: Sularaha nimiväärtuste konfigureerimine kassa jaoks
description: Poe kassas müüjate, müügiassistentide ja juhatajate poolt kasutatavate rahatähtede ja müntide nimiväärtused saab määratleda kontoris.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a34ae8084c0ad55221f4ab93eb8c6481fa8c4771
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022226"
---
# <a name="configure-cash-denominations-for-the-point-of-sale-pos"></a><span data-ttu-id="53c0a-103">Sularaha nimiväärtuste konfigureerimine kassa jaoks</span><span class="sxs-lookup"><span data-stu-id="53c0a-103">Configure cash denominations for the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="53c0a-104">Poe kassas müüjate, müügiassistentide ja juhatajate poolt kasutatavate rahatähtede ja müntide nimiväärtused saab määratleda kontoris.</span><span class="sxs-lookup"><span data-stu-id="53c0a-104">Cash denominations for notes and coins can be defined in the back office to be used by cashiers, sales associates, and managers at the store from within the POS.</span></span> <span data-ttu-id="53c0a-105">Nimiväärtustest võib olla abi päeva lõpus müügiaruande koostamiseks sularaha lugemisel või maksete kiirel töötlemisel.</span><span class="sxs-lookup"><span data-stu-id="53c0a-105">These denominations can be used to aid in counting cash for end of day tender declarations or for quickly tendering a sale.</span></span>

## <a name="define-denominations"></a><span data-ttu-id="53c0a-106">Määratlege nimiväärtused</span><span class="sxs-lookup"><span data-stu-id="53c0a-106">Define denominations</span></span>

<span data-ttu-id="53c0a-107">Nimiväärtuste seadistamine iga poe kohta toimub lehel **Seadistamine** \> **Sularaha deklaratsiooni suvand**.</span><span class="sxs-lookup"><span data-stu-id="53c0a-107">The denominations are set up per store on the **Set up** \> **Cash declaration** option from the store property page.</span></span>

![Sularaha deklaratsiooni suvand](./media/image1-denomination.png)

<span data-ttu-id="53c0a-109">Nimiväärtuse määratlemiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="53c0a-109">To define a denomination:</span></span>

1. <span data-ttu-id="53c0a-110">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="53c0a-110">Click **New**.</span></span>
1. <span data-ttu-id="53c0a-111">Määrake tüüp (münt või rahatäht).</span><span class="sxs-lookup"><span data-stu-id="53c0a-111">Specify the type (coin or note).</span></span>
1. <span data-ttu-id="53c0a-112">Määrake summa (väärtus).</span><span class="sxs-lookup"><span data-stu-id="53c0a-112">Specify the amount (value).</span></span>

![Sularahadeklaratsiooni põhivaluutade leht](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a><span data-ttu-id="53c0a-114">Seadistage funktsiooniprofiil.</span><span class="sxs-lookup"><span data-stu-id="53c0a-114">Configure the functionality profile</span></span>

<span data-ttu-id="53c0a-115">Sularahamakse korral saab kassa kasutaja kliendi makstud summa kiireks sisestamiseks kasutada rahatähtede nimiväärtuseid.</span><span class="sxs-lookup"><span data-stu-id="53c0a-115">When paying by cash in POS, the user can use the note denominations to quickly enter the amount paid by the customer.</span></span> <span data-ttu-id="53c0a-116">Funktsiooniprofiilis saate saate seadistada kassas nimiväärtuse kuvamise kaks suvandit.</span><span class="sxs-lookup"><span data-stu-id="53c0a-116">In the functionality profile, you can configure the two options for showing the denomination in POS.</span></span>

- <span data-ttu-id="53c0a-117">**Suurem või võrdne summa**: vaikimisi kuvatakse kassas ainult makstavast summast suuremaid nimiväärtuseid, mis võimaldab makseid töödelda ühe puutega.</span><span class="sxs-lookup"><span data-stu-id="53c0a-117">**Greater or equal to amount due** – By default, POS will only show the note denominations that are greater than the amount due, which allows for one-touch tendering.</span></span> <span data-ttu-id="53c0a-118">Näiteks kui tasumisele kuuluv summa on 7,50 $,näitab kassa järgmiseid nimiväärtuseid: 10 $, 20 $, 50 $ ja 100 $.</span><span class="sxs-lookup"><span data-stu-id="53c0a-118">For example, if the amount due is $7.50, POS would show the following denominations: $10, $20, $50, and $100.</span></span> <span data-ttu-id="53c0a-119">Kui puudutada ühte nendest summadest, töödeldakse makse vastavast summast lähtudes.</span><span class="sxs-lookup"><span data-stu-id="53c0a-119">Touching any of these amounts will automatically tender the sale for that amount.</span></span> <span data-ttu-id="53c0a-120">Nimiväärtuseid 1 $ ja 5 $ ei kuvata, sest nende väärtus on maksmisele kuuluvast summast väiksem.</span><span class="sxs-lookup"><span data-stu-id="53c0a-120">The $1 and $5 notes are not shown since these amounts are less than the amount due.</span></span>
- <span data-ttu-id="53c0a-121">**Kõik nimiväärtused**: maksmisele kuuluvast summast olenemata kassas alati kõikide nimiväärtuste kuvamiseks valige see suvand.</span><span class="sxs-lookup"><span data-stu-id="53c0a-121">**All denominations** – Select this option to always show all note denominations in POS, regardless of the amount due.</span></span> <span data-ttu-id="53c0a-122">See tähendab, et kasutaja saab maksmisele kuuluva summa tasumiseks kasutada rahatähtede kombinatsioone.</span><span class="sxs-lookup"><span data-stu-id="53c0a-122">This means that the user can use a combination of notes to reach the amount due.</span></span> <span data-ttu-id="53c0a-123">Näiteks, kui tasumisele kuuluv summa on 25,00 $, saab kasutaja valida müügi lõpetamiseks valikud 20 $ ja 5 $.</span><span class="sxs-lookup"><span data-stu-id="53c0a-123">For example, if the amount due is $25.00, the user can choose $20 and $5 to complete the sale.</span></span>