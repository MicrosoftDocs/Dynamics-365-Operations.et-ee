---
title: Käibemaksu konfigureerimine veebitellimuste jaoks
description: Selles teemas antakse ülevaade käibemaksugrupi valikust erinevate veebitellimuse tüüpide puhul rakenduses Dynamics 365 Commerce.
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 40c20bf13779f73289e43df21b763e1b864686a7
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530193"
---
# <a name="configure-sales-tax-for-online-orders"></a><span data-ttu-id="9ddda-103">Käibemaksu konfigureerimine veebitellimuste jaoks</span><span class="sxs-lookup"><span data-stu-id="9ddda-103">Configure sales tax for online orders</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="9ddda-104">Selles teemas antakse ülevaade käibemaksugrupi valikust erinevate veebitellimuse tüüpide puhul.</span><span class="sxs-lookup"><span data-stu-id="9ddda-104">This topic provides an overview of sales tax group selection for different online order types.</span></span> 

<span data-ttu-id="9ddda-105">Teie e-kaubanduse kanal võib soovida toetada selliseid võimalusi nagu veebitellimuste kohaletoimetamine või peale võtmine.</span><span class="sxs-lookup"><span data-stu-id="9ddda-105">Your e-commerce channel may want to support options like delivery or pickup for online orders.</span></span> <span data-ttu-id="9ddda-106">Käibemaksu kohaldatavus põhineb teie võrgukasutajate poolt valitud suvandil.</span><span class="sxs-lookup"><span data-stu-id="9ddda-106">The sales tax applicability is based on the option selected by your online users.</span></span> <span data-ttu-id="9ddda-107">Kui saidi klient otsustab osta kauba veebis ja lähetab selle aadressile, määratakse käibemaks kliendi lähetusaadressi maksugrupi sätte põhjal.</span><span class="sxs-lookup"><span data-stu-id="9ddda-107">When a site customer chooses to buy an item online and gets it shipped to an address, the sales tax is determined based on the customer's shipping address tax group setting.</span></span> <span data-ttu-id="9ddda-108">Kui klient otsustab ostetud kauba poest peale võtta, määratakse käibemaks peale võtmise poe maksugrupi sätte alusel.</span><span class="sxs-lookup"><span data-stu-id="9ddda-108">When a customer opts to pick up a purchased item at a store, the sales tax is determined based on the pickup store's tax group setting.</span></span> 

## <a name="orders-shipped-to-a-customer-address"></a><span data-ttu-id="9ddda-109">Kliendi aadressile lähetatud tellimused</span><span class="sxs-lookup"><span data-stu-id="9ddda-109">Orders shipped to a customer address</span></span> 

<span data-ttu-id="9ddda-110">Üldiselt määratleb kliendi aadressidele lähetatavate veebitellimuste maksud sihtkoht.</span><span class="sxs-lookup"><span data-stu-id="9ddda-110">In general, taxes for online orders that ship to customer addresses are defined by the destination.</span></span> <span data-ttu-id="9ddda-111">Igal käibemaksugrupil on jaemüügi sihtkohapõhine maksukonfiguratsioon, kus teie ettevõte saab hierarhilisel kujul määratleda sihtkoha üksikasjad (nt maakond/regioon, maakond, maakond ja linn).</span><span class="sxs-lookup"><span data-stu-id="9ddda-111">Every sales tax group has a retail destination-based tax configuration in which your business can define destination details such as county/region, state, county, and city in a hierarchical form.</span></span> <span data-ttu-id="9ddda-112">Kui veebitellimus on sisestatud, kasutab kaubanduse maksumootor tellimuse iga reakauba tarneaadressi ja leiab käibemaksugrupid vastavate sihtkohapõhiste maksukriteeriumidega.</span><span class="sxs-lookup"><span data-stu-id="9ddda-112">When an online order is placed, the Commerce tax engine uses the delivery address of every line item in the order, and finds sales tax groups with matching destination-based tax criteria.</span></span> <span data-ttu-id="9ddda-113">Näiteks online-tellimuse puhul, mille rea kauba tarneaadress on San Francisco, California, leiab maksumootor California käibemaksugrupi ja käibemaksukoodi ning arvutab seejärel vastavalt iga reakauba maksu.</span><span class="sxs-lookup"><span data-stu-id="9ddda-113">For example, for an online order with a line item delivery address to San Francisco, California, the tax engine will find the sales tax group and sales tax code for California and then calculate tax for each line item accordingly.</span></span>  

## <a name="customer-based-tax-groups"></a><span data-ttu-id="9ddda-114">Kliendipõhised maksugrupid</span><span class="sxs-lookup"><span data-stu-id="9ddda-114">Customer-based tax groups</span></span>

<span data-ttu-id="9ddda-115">Kaubanduse peakorteris on kaks kohta, kus kliendi maksugrupid on konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="9ddda-115">In Commerce headquarters, there are two places where customer tax groups are configured:</span></span>

- <span data-ttu-id="9ddda-116">**Kliendi profiil**</span><span class="sxs-lookup"><span data-stu-id="9ddda-116">**Customer's profile**</span></span>
- <span data-ttu-id="9ddda-117">**Kliendi tarneaadress**</span><span class="sxs-lookup"><span data-stu-id="9ddda-117">**Customer's shipping address**</span></span>

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a><span data-ttu-id="9ddda-118">Kui kliendi profiilil on maksugrupp konfigureeritud</span><span class="sxs-lookup"><span data-stu-id="9ddda-118">If a customer's profile has a tax group configured</span></span>

<span data-ttu-id="9ddda-119">Kliendi profiilikirjel võib peakorteris olla konfigureeritud käibemaksugrupp, kuid internetitellimuste puhul ei kasuta maksumootor kliendi profiilis konfigureeritud käibemaksugruppi.</span><span class="sxs-lookup"><span data-stu-id="9ddda-119">A customer's profile record in headquarters may have a sales tax group configured, however for online orders the sales tax group configured in a customer's profile will not be used by the tax engine.</span></span> 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a><span data-ttu-id="9ddda-120">Kui kliendi tarneaadressil on maksugrupp konfigureeritud</span><span class="sxs-lookup"><span data-stu-id="9ddda-120">If a customer's shipping address has a tax group configured</span></span>

<span data-ttu-id="9ddda-121">Kui kliendi tarneaadressi kirjel on konfigureeritud maksugrupp ja internetitellimus (või reakaup) saadetakse kliendi tarneaadressile, kasutab maksumootor maksu arvutamisel kliendi aadressikirjes konfigureeritud maksugruppi.</span><span class="sxs-lookup"><span data-stu-id="9ddda-121">If a customer's shipping address record has a tax group configured and an online order (or line item) is shipped to the customer's shipping address, the tax group configured in the customer's address record will be used by the tax engine for tax calculations.</span></span>

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a><span data-ttu-id="9ddda-122">Konfigureeri kliendi tarneaadressi kirjele maksugrupp</span><span class="sxs-lookup"><span data-stu-id="9ddda-122">Configure a tax group for a customer's shipping address record</span></span>

<span data-ttu-id="9ddda-123">Kliendi tarneaadressi kirje maksugrupi konfigureerimiseks kaubanduse peakorteris toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="9ddda-123">To configure a tax group for a customer's shipping address record in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="9ddda-124">Avage **Kõik kliendid** ja valige soovitud klient.</span><span class="sxs-lookup"><span data-stu-id="9ddda-124">Go to **All customers**, and then select the desired customer.</span></span> 
1. <span data-ttu-id="9ddda-125">Valige **Aadressid** FastTab-is soovitud aadress ja seejärel valige **Veel suvandeid \> Täpsem**.</span><span class="sxs-lookup"><span data-stu-id="9ddda-125">On the **Addresses** FastTab, select the desired address, and then select **More options \> Advanced**.</span></span> 
1. <span data-ttu-id="9ddda-126">Määrake **Üldine** vahekaardil **Halda aadresse** lehel käibemaksu väärtus vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="9ddda-126">Under the **General** tab on the **Manage addresses** page, set the sales tax value as needed.</span></span>

> [!NOTE]
> <span data-ttu-id="9ddda-127">Maksugrupp määratletakse tellimuserea tarneaadressi abil ja sihtkohapõhised maksud konfigureeritakse maksugrupis.</span><span class="sxs-lookup"><span data-stu-id="9ddda-127">The tax group is defined using the delivery address of the order line and the destination-based taxes are configured at the tax group itself.</span></span> <span data-ttu-id="9ddda-128">Lisateavet vt teemast [Seadista maksud veebipoodidele vastavalt asukohale](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="9ddda-128">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="order-pickup-in-store"></a><span data-ttu-id="9ddda-129">Tellimusele järgi tulemine kauplusesse</span><span class="sxs-lookup"><span data-stu-id="9ddda-129">Order pickup in store</span></span>

<span data-ttu-id="9ddda-130">Kauplusesse järgi tulemise või tellimuse peale võtmise tellimuseridade puhul rakendatakse valitud peale võtmise kaupluse maksugrupp.</span><span class="sxs-lookup"><span data-stu-id="9ddda-130">For order lines with pickup in store or curbside pickup specified, the tax group from the selected pickup store will be applied.</span></span> <span data-ttu-id="9ddda-131">Lisateavet antud kaupluse maksugrupi konfigureerimise kohta leiate teemast [Kaupluste muude maksusuvandite määramine](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="9ddda-131">For details about how to configure the tax group for a given store, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

> [!NOTE]
> <span data-ttu-id="9ddda-132">Kui tellimusele tullakse kauplusesse järgi, ignoreerib maksumootor kliendi aadressi maksusätteid (kui see on seadistatud) ja rakendatakse peale võtmise kaupluse maksu konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="9ddda-132">When an order line is picked up at a store, a customer's address tax settings (if set up) will be ignored by the tax engine and the pickup store's tax configuration will be applied.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="9ddda-133">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="9ddda-133">Additional resources</span></span>

[<span data-ttu-id="9ddda-134">Käibemaksu ülevaade</span><span class="sxs-lookup"><span data-stu-id="9ddda-134">Sales tax overview</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="9ddda-135">Käibemaksuarvutusmeetodid väljal Päritolu</span><span class="sxs-lookup"><span data-stu-id="9ddda-135">Sales tax calculation methods in the Origin field</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="9ddda-136">Käibemaksu määramine ja tühistamised</span><span class="sxs-lookup"><span data-stu-id="9ddda-136">Sales tax assignment and overrides</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="9ddda-137">Kogusumma ja intervalli arvutamise valikud käibemaksukoodide puhul</span><span class="sxs-lookup"><span data-stu-id="9ddda-137">Whole amount and Interval calculation options for sales tax codes</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="9ddda-138">Maksuvabastuse arvutamine</span><span class="sxs-lookup"><span data-stu-id="9ddda-138">Calculation of tax exemption</span></span>](tax-exempt-price-inclusive.md) 

