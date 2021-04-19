---
title: Hinnakorrigeerimised ja allahindlused
description: Selles artiklis käsitletakse hinna korrigeerimisi ja allahindlusi Dynamics 365 Commerceis.
author: scott-tucker
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 2d3e8025c5ab28296713634094694156f9addf62
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802787"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="f1156-103">Hinnakorrigeerimised ja allahindlused</span><span class="sxs-lookup"><span data-stu-id="f1156-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f1156-104">Selles artiklis käsitletakse hinna korrigeerimisi ja allahindlusi Dynamics 365 Commerceis.</span><span class="sxs-lookup"><span data-stu-id="f1156-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f1156-105">Rakenduses Commerce saate korrigeerida toodete hindu ja seadistada allahindlusi, mida rakendatakse kassas, kõnekeskuse müügitellimuses või võrgutellimuses rea kaubale või kandele.</span><span class="sxs-lookup"><span data-stu-id="f1156-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="f1156-106">Hinna korrigeerimisi ja allahindlusi saab siduda hinnagruppidega.</span><span class="sxs-lookup"><span data-stu-id="f1156-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="f1156-107">Nii hinnakorrigeerimiste kui ka allahindluste puhul saate määrata ühe alguskuupäeva ja lõppkuupäeva või korduva perioodi, allahindluskoodi ja veel mõningaid atribuute.</span><span class="sxs-lookup"><span data-stu-id="f1156-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="f1156-108">Hinna korrigeerimisi ja allahindlusi saab rakendada toodetele, variantidele või kategooriatele.</span><span class="sxs-lookup"><span data-stu-id="f1156-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="f1156-109">Kui tootele rakendub rohkem kui üks allahindlus, võib klient saada ühe allahindlustest või kombineeritud allahindluse, olenevalt allahindluse konfiguratsioonist.</span><span class="sxs-lookup"><span data-stu-id="f1156-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="f1156-110">Commerce rakendab automaatselt allahindluse või allahindluste kombinatsiooni, mis annab kliendile parima hinna.</span><span class="sxs-lookup"><span data-stu-id="f1156-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="f1156-111">Hinna korrigeerimise või allahindluse seadistamisel kontrollige kindlasti, kas hinnagrupid on määratud õigetele kanalitele, kataloogidele, alluvustele või püsikliendiprogrammidele, millele soovite allahindluse rakendada.</span><span class="sxs-lookup"><span data-stu-id="f1156-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="f1156-112">Ning kui soovite automaatselt allahindluse ID luua, saate enne uue hinna korrigeerimise või allahindluse määratlemist lehel **Kaubanduse parameetrid** seadistada numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="f1156-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="f1156-113">Saate hinna korrigeerimist või allahindlust kustutada.</span><span class="sxs-lookup"><span data-stu-id="f1156-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="f1156-114">Statistiline teave läheb siiski kaduma.</span><span class="sxs-lookup"><span data-stu-id="f1156-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="f1156-115">Allahindluste tüübid</span><span class="sxs-lookup"><span data-stu-id="f1156-115">Types of discounts</span></span>

<span data-ttu-id="f1156-116">Allahindlusi on mitut tüüpi.</span><span class="sxs-lookup"><span data-stu-id="f1156-116">There are many types of discounts:</span></span>

- <span data-ttu-id="f1156-117">**Lihtne allahindlus** – üksik protsent või summa.</span><span class="sxs-lookup"><span data-stu-id="f1156-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="f1156-118">**Koguse allahindlus** – allahindlus, mis rakendub kahe või enama toote ostmisel.</span><span class="sxs-lookup"><span data-stu-id="f1156-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="f1156-119">**Segamise ja sobitamise allahindlus** – allahindlus, mis rakendub teatud tootekombinatsiooni ostmisel.</span><span class="sxs-lookup"><span data-stu-id="f1156-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="f1156-120">**Läve allahindlus** – allahindlus, mis rakendub, kui kande kogusumma on teatud summast suurem.</span><span class="sxs-lookup"><span data-stu-id="f1156-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>
- <span data-ttu-id="f1156-121">**Maksevahendil põhinev allahindlus** – allahindlus, mis rakendub, kui kande kogusumma on suurem kui määratud summa ja makse puhul kasutatakse kindlat maksetüüpi (nt sularaha, krediit- või deebetkaarti).</span><span class="sxs-lookup"><span data-stu-id="f1156-121">**Tender-based discount** – A discount that is applied when the transaction total is more than a specified amount and a specific payment type (for example, cash, credit, or debit card) is used for payment.</span></span>
- <span data-ttu-id="f1156-122">**Saatmise allahindlus** – allahindlus, mis rakendub, kui kande kogusumma on suurem kui määratud summa ja tellimusel kasutatakse kindlat tarneviisi (nt kahepäevane saatmine või öine saatmine).</span><span class="sxs-lookup"><span data-stu-id="f1156-122">**Shipping discount** – A discount that is applied when the transaction total is more than a specified amount and a specific mode of delivery (for example, two day shipping or overnight shipping) is used on the order.</span></span>

<span data-ttu-id="f1156-123">Nii hinna korrigeerimisi kui ka allahindlusi saab seostada hinnagruppidega.</span><span class="sxs-lookup"><span data-stu-id="f1156-123">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="f1156-124">Seejärel saab hinnagruppe seostada kanalite, kataloogide, alluvuste ja püsikliendiprogrammidega.</span><span class="sxs-lookup"><span data-stu-id="f1156-124">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]