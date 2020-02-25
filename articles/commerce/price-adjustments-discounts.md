---
title: Hinnakorrigeerimised ja allahindlused
description: Selles artiklis käsitletakse hinna korrigeerimisi ja allahindlusi Dynamics 365 Commerceis.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: dfaacfa7681258e3b2273083017c0c398d566651
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022308"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="dc527-103">Hinnakorrigeerimised ja allahindlused</span><span class="sxs-lookup"><span data-stu-id="dc527-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dc527-104">Selles artiklis käsitletakse hinna korrigeerimisi ja allahindlusi Dynamics 365 Commerceis.</span><span class="sxs-lookup"><span data-stu-id="dc527-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="dc527-105">Rakenduses Commerce saate korrigeerida toodete hindu ja seadistada allahindlusi, mida rakendatakse kassas, kõnekeskuse müügitellimuses või võrgutellimuses rea kaubale või kandele.</span><span class="sxs-lookup"><span data-stu-id="dc527-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="dc527-106">Hinna korrigeerimisi ja allahindlusi saab siduda hinnagruppidega.</span><span class="sxs-lookup"><span data-stu-id="dc527-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="dc527-107">Nii hinnakorrigeerimiste kui ka allahindluste puhul saate määrata ühe alguskuupäeva ja lõppkuupäeva või korduva perioodi, allahindluskoodi ja veel mõningaid atribuute.</span><span class="sxs-lookup"><span data-stu-id="dc527-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="dc527-108">Hinna korrigeerimisi ja allahindlusi saab rakendada toodetele, variantidele või kategooriatele.</span><span class="sxs-lookup"><span data-stu-id="dc527-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="dc527-109">Kui tootele rakendub rohkem kui üks allahindlus, võib klient saada ühe allahindlustest või kombineeritud allahindluse, olenevalt allahindluse konfiguratsioonist.</span><span class="sxs-lookup"><span data-stu-id="dc527-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="dc527-110">Commerce rakendab automaatselt allahindluse või allahindluste kombinatsiooni, mis annab kliendile parima hinna.</span><span class="sxs-lookup"><span data-stu-id="dc527-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="dc527-111">Hinna korrigeerimise või allahindluse seadistamisel kontrollige kindlasti, kas hinnagrupid on määratud õigetele kanalitele, kataloogidele, alluvustele või püsikliendiprogrammidele, millele soovite allahindluse rakendada.</span><span class="sxs-lookup"><span data-stu-id="dc527-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="dc527-112">Ning kui soovite automaatselt allahindluse ID luua, saate enne uue hinna korrigeerimise või allahindluse määratlemist lehel **Kaubanduse parameetrid** seadistada numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="dc527-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="dc527-113">Saate hinna korrigeerimist või allahindlust kustutada.</span><span class="sxs-lookup"><span data-stu-id="dc527-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="dc527-114">Statistiline teave läheb siiski kaduma.</span><span class="sxs-lookup"><span data-stu-id="dc527-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="dc527-115">Allahindluste tüübid</span><span class="sxs-lookup"><span data-stu-id="dc527-115">Types of discounts</span></span>

<span data-ttu-id="dc527-116">Allahindlusi on nelja tüüpi.</span><span class="sxs-lookup"><span data-stu-id="dc527-116">There are four types of discounts:</span></span>

- <span data-ttu-id="dc527-117">**Lihtne allahindlus** – üksik protsent või summa.</span><span class="sxs-lookup"><span data-stu-id="dc527-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="dc527-118">**Koguse allahindlus** – allahindlus, mis rakendub kahe või enama toote ostmisel.</span><span class="sxs-lookup"><span data-stu-id="dc527-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="dc527-119">**Segamise ja sobitamise allahindlus** – allahindlus, mis rakendub teatud tootekombinatsiooni ostmisel.</span><span class="sxs-lookup"><span data-stu-id="dc527-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="dc527-120">**Läve allahindlus** – allahindlus, mis rakendub, kui kande kogusumma on teatud summast suurem.</span><span class="sxs-lookup"><span data-stu-id="dc527-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>

<span data-ttu-id="dc527-121">Nii hinna korrigeerimisi kui ka allahindlusi saab seostada hinnagruppidega.</span><span class="sxs-lookup"><span data-stu-id="dc527-121">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="dc527-122">Seejärel saab hinnagruppe seostada kanalite, kataloogide, alluvuste ja püsikliendiprogrammidega.</span><span class="sxs-lookup"><span data-stu-id="dc527-122">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>