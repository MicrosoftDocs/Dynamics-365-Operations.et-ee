---
title: Hinnakorrigeerimised ja allahindlused
description: Selles artiklis käsitletakse hinna korrigeerimisi ja allahindlusi Dynamics 365 Commerceis.
author: scott-tucker
ms.date: 06/11/2021
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
ms.openlocfilehash: 44c03ae0a04d648e788a72d8f6dcc3671c5736c7
ms.sourcegitcommit: 7c9d6be464db058511df9cb6ba162d21dc0554e8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/11/2021
ms.locfileid: "6240938"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="0b678-103">Hinnakorrigeerimised ja allahindlused</span><span class="sxs-lookup"><span data-stu-id="0b678-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0b678-104">Selles artiklis käsitletakse hinna korrigeerimisi ja allahindlusi Dynamics 365 Commerceis.</span><span class="sxs-lookup"><span data-stu-id="0b678-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0b678-105">Rakenduses Commerce saate korrigeerida toodete hindu ja seadistada allahindlusi, mida rakendatakse kassas, kõnekeskuse müügitellimuses või võrgutellimuses rea kaubale või kandele.</span><span class="sxs-lookup"><span data-stu-id="0b678-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="0b678-106">Hinna korrigeerimisi ja allahindlusi saab siduda hinnagruppidega.</span><span class="sxs-lookup"><span data-stu-id="0b678-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="0b678-107">Nii hinnakorrigeerimiste kui ka allahindluste puhul saate määrata ühe alguskuupäeva ja lõppkuupäeva või korduva perioodi, allahindluskoodi ja veel mõningaid atribuute.</span><span class="sxs-lookup"><span data-stu-id="0b678-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="0b678-108">Hinna korrigeerimisi ja allahindlusi saab rakendada toodetele, variantidele või kategooriatele.</span><span class="sxs-lookup"><span data-stu-id="0b678-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="0b678-109">Kui tootele rakendub rohkem kui üks allahindlus, võib klient saada ühe allahindlustest või kombineeritud allahindluse, olenevalt allahindluse konfiguratsioonist.</span><span class="sxs-lookup"><span data-stu-id="0b678-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="0b678-110">Commerce rakendab automaatselt allahindluse või allahindluste kombinatsiooni, mis annab kliendile parima hinna.</span><span class="sxs-lookup"><span data-stu-id="0b678-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="0b678-111">Hinna korrigeerimise või allahindluse seadistamisel kontrollige kindlasti, kas hinnagrupid on määratud õigetele kanalitele, kataloogidele, alluvustele või püsikliendiprogrammidele, millele soovite allahindluse rakendada.</span><span class="sxs-lookup"><span data-stu-id="0b678-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="0b678-112">Ning kui soovite automaatselt allahindluse ID luua, saate enne uue hinna korrigeerimise või allahindluse määratlemist lehel **Kaubanduse parameetrid** seadistada numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="0b678-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="0b678-113">Saate hinna korrigeerimist või allahindlust kustutada.</span><span class="sxs-lookup"><span data-stu-id="0b678-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="0b678-114">Statistiline teave läheb siiski kaduma.</span><span class="sxs-lookup"><span data-stu-id="0b678-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="0b678-115">Allahindluste tüübid</span><span class="sxs-lookup"><span data-stu-id="0b678-115">Types of discounts</span></span>

<span data-ttu-id="0b678-116">Allahindlusi on mitut tüüpi.</span><span class="sxs-lookup"><span data-stu-id="0b678-116">There are many types of discounts:</span></span>

- <span data-ttu-id="0b678-117">**Lihtne allahindlus** – üksik protsent või summa.</span><span class="sxs-lookup"><span data-stu-id="0b678-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="0b678-118">**Koguse allahindlus** – allahindlus, mis rakendub kahe või enama toote ostmisel.</span><span class="sxs-lookup"><span data-stu-id="0b678-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="0b678-119">**Segamise ja sobitamise allahindlus** – allahindlus, mis rakendub teatud tootekombinatsiooni ostmisel.</span><span class="sxs-lookup"><span data-stu-id="0b678-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="0b678-120">**Läve allahindlus** – allahindlus, mis rakendub, kui kande kogusumma on teatud summast suurem.</span><span class="sxs-lookup"><span data-stu-id="0b678-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>
- <span data-ttu-id="0b678-121">**Maksevahendil põhinev allahindlus** – allahindlus, mis rakendub, kui kande kogusumma on suurem kui määratud summa ja makse puhul kasutatakse kindlat maksetüüpi (nt sularaha, krediit- või deebetkaarti).</span><span class="sxs-lookup"><span data-stu-id="0b678-121">**Tender-based discount** – A discount that is applied when the transaction total is more than a specified amount and a specific payment type (for example, cash, credit, or debit card) is used for payment.</span></span>
- <span data-ttu-id="0b678-122">**Saatmise allahindlus** – allahindlus, mis rakendub, kui kande kogusumma on suurem kui määratud summa ja tellimusel kasutatakse kindlat tarneviisi (nt kahepäevane saatmine või öine saatmine).</span><span class="sxs-lookup"><span data-stu-id="0b678-122">**Shipping discount** – A discount that is applied when the transaction total is more than a specified amount and a specific mode of delivery (for example, two day shipping or overnight shipping) is used on the order.</span></span>

<span data-ttu-id="0b678-123">Nii hinna korrigeerimisi kui ka allahindlusi saab seostada hinnagruppidega.</span><span class="sxs-lookup"><span data-stu-id="0b678-123">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="0b678-124">Seejärel saab hinnagruppe seostada kanalite, kataloogide, alluvuste ja püsikliendiprogrammidega.</span><span class="sxs-lookup"><span data-stu-id="0b678-124">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>

> [!NOTE]
> <span data-ttu-id="0b678-125">Segamise ja sobitamise allahindlusel ning läve allahindlusel on omadused, mille nimed on vastavalt "Mitteallahindlusega toodete loendamine" ja "Mitteallahindluskõlblike toodete loendamine künnise suunas".</span><span class="sxs-lookup"><span data-stu-id="0b678-125">The mix and match discount and the threshold discount have properties named "Count non-discountable products" and "Count non-discountable products towards threshold", respectively.</span></span> <span data-ttu-id="0b678-126">Kui need atribuudid on lubatud, võib kaup, mis ei vasta allahindluse saamise tingimustele, siiski aidata allahindlust kvalifitseeruda, kuid abikõlbmatu kaup ei saa allahindlust.</span><span class="sxs-lookup"><span data-stu-id="0b678-126">If these properties are enabled, an item that is not eligible for any discount can still help qualify a transaction for the discount, but the ineligible item will not get the discount.</span></span> 
> 
> <span data-ttu-id="0b678-127">Näiteks kui loote segamis- ja sobitamishinnaalandi kahe reaga A ja B, kus klient peaks saama mõlemalt kaubalt 10% allahindlust, kuid kaubal A on märgitud konfiguratsioon "Takista kõiki allahindlusi", siis tavaliselt peataks see kauba A kaasamise allahindlusesse.</span><span class="sxs-lookup"><span data-stu-id="0b678-127">For example, if you create a mix and match discount with two lines, A and B, where a customer should get 10% off on both items, but item A has the configuration "Prevent all discounts" checked, then this would typically stop item A from being included in the discount.</span></span> <span data-ttu-id="0b678-128">Kui aga atribuut "Loenda mitteallahindlusega tooteid" on lubatud, saab kaupa A kasutada segamise ja sobitamise allahindluse saamiseks, kuid 10% allahindlust rakendatakse ainult kaubale B. Sarnane loogika kehtib läve allahindluse kohta.</span><span class="sxs-lookup"><span data-stu-id="0b678-128">However, if the "Count non-discountable products" property is enabled, then item A can be used to qualify for the mix and match discount, but the 10% discount will only be applied to item B. Similar logic applies to the threshold discount.</span></span> 
>
> <span data-ttu-id="0b678-129">Kuid omadusel "Loenda mitteallahindlusega tooted künnise suunas" on täiendav võimalus võrreldes segu omadusega "Loe mitteallahindlusega tooteid" ja sobita allahindlused.</span><span class="sxs-lookup"><span data-stu-id="0b678-129">However, the property "Count non-discountable products towards threshold" has an additional capability when compared to the "Count non-discountable products" property of the mix and match discounts.</span></span> <span data-ttu-id="0b678-130">Kui lävi hinnaaland on lubatud ja kui on olemas kaup, millel on olemasolev allahindlus, mis takistaks kaubal muid allahindlusi, siis kvalifitseeruks selle kauba eest makstud hind künnise saavutamisele, kuid see kaup ei saa täiendavat allahindlust.</span><span class="sxs-lookup"><span data-stu-id="0b678-130">If the threshold discount is enabled, and if there is an item that has an existing discount which would prevent the item from any other discounts, then  the price paid for this item would qualify towards meeting the threshold, but this item will not get the additional discount.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
