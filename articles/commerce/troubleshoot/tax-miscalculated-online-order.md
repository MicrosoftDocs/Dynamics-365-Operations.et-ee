---
title: Võrgutellimuste maksud on valesti arvutatud
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui võrgutellimuste maksud on valesti arvutatud või kui müügirea maksugrupp pole õigesti seatud.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7f71add679e1d24f80db8ce3990058b591128ec1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801407"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a><span data-ttu-id="a0b6d-103">Võrgutellimuste maksud on valesti arvutatud</span><span class="sxs-lookup"><span data-stu-id="a0b6d-103">Taxes on online orders are incorrectly calculated</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a0b6d-104">See teema annab tõrkeotsingu juhised, mis aitavad, kui võrgutellimuste maksud on valesti arvutatud või kui müügirea maksugrupp pole õigesti seatud.</span><span class="sxs-lookup"><span data-stu-id="a0b6d-104">This topic provides troubleshooting guidance that can help when taxes on online orders are incorrectly calculated, or when the tax group on the sales line isn't correctly set.</span></span>

## <a name="description"></a><span data-ttu-id="a0b6d-105">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a0b6d-105">Description</span></span>

<span data-ttu-id="a0b6d-106">Kui e-äri tellimus on esitatud, siis on maksud valesti arvutatud või on müügirea maksugrupp valesti seatud.</span><span class="sxs-lookup"><span data-stu-id="a0b6d-106">When an e-commerce order is placed, the taxes are incorrectly calculated, or the tax group on the sales line is incorrectly set.</span></span>

## <a name="resolution"></a><span data-ttu-id="a0b6d-107">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="a0b6d-107">Resolution</span></span>

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a><span data-ttu-id="a0b6d-108">Commerce Headquartersi kaupluse käibemaksu konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="a0b6d-108">Configure the sales tax for a retail store in Commerce headquarters</span></span>

<span data-ttu-id="a0b6d-109">Commerce Headquarters\`i kaupluse käibemaksu konfigureerimine, järgige järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="a0b6d-109">To configure the sales tax for a retail store in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a0b6d-110">Minge jaotisse **Jaemüük ja kaubandus \> Kanalid \> Kõik kauplused**.</span><span class="sxs-lookup"><span data-stu-id="a0b6d-110">Go to **Retail and Commerce \> Channels \> All stores**.</span></span>
1. <span data-ttu-id="a0b6d-111">Valige kauplus, mille jaoks käibemaksu konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="a0b6d-111">Select the store to configure sales tax for.</span></span>
1. <span data-ttu-id="a0b6d-112">Jaotise **Üldine** **Käibemaks** kiirkaardil konfigureerige kaupluse käibemaksuteavet.</span><span class="sxs-lookup"><span data-stu-id="a0b6d-112">On the **General** FastTab, in the **Sales tax** section, configure the sales tax information for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="a0b6d-113">Toote kauplust peale võttes, tuleb maksugrupp kauplusest, mis on valitud peale võtmiseks.</span><span class="sxs-lookup"><span data-stu-id="a0b6d-113">For product pickup from a store, the tax group comes from the store that is selected for pickup.</span></span> <span data-ttu-id="a0b6d-114">Lisateavet vt jaotisest [Kaupluste muude maksuvalikute häälestamine](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="a0b6d-114">For more information, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a><span data-ttu-id="a0b6d-115">Commerce Headquarters\`i kaupluse käibemaksu konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="a0b6d-115">Configure the sales tax for a customer's address in Commerce headquarters</span></span>

<span data-ttu-id="a0b6d-116">Commerce Headquarters\`i kaupluse käibemaksu konfigureerimine, järgige järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="a0b6d-116">To configure the sales tax for a customer's address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a0b6d-117">Avage **Müügireskontro \> Kliendid \> Kõik kliendid**.</span><span class="sxs-lookup"><span data-stu-id="a0b6d-117">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="a0b6d-118">Valige klient, kelle jaoks müügitellimus luua.</span><span class="sxs-lookup"><span data-stu-id="a0b6d-118">Select the customer to configure sales taxes for.</span></span>
1. <span data-ttu-id="a0b6d-119">Valige **Aadressi** kiirkaardil aadress, mille jaoks käibemaks konfigureerida, valige suvand **Veel suvandeid** ja seejärel **Täpsem**.</span><span class="sxs-lookup"><span data-stu-id="a0b6d-119">On the **Addresses** FastTab, select the address to configure sales taxes for, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="a0b6d-120">Valige vahekaardil **Üldine** kiirkaart **Maksu grupp**.</span><span class="sxs-lookup"><span data-stu-id="a0b6d-120">On the **General** FastTab, select the **Tax group**.</span></span>
1. <span data-ttu-id="a0b6d-121">Valige väljal **Käibemaks** sobiv väärtus.</span><span class="sxs-lookup"><span data-stu-id="a0b6d-121">In the **Sales tax** field, select the appropriate value.</span></span>

> [!NOTE]
> <span data-ttu-id="a0b6d-122">Lähetamise puhul, mis hõlmab käibemaksu kliendi aadressil, määrab rea tarneaadress rea maksugrupi.</span><span class="sxs-lookup"><span data-stu-id="a0b6d-122">For shipping that involves sales tax on the customer's address, the delivery address of the line determines the tax group for the line.</span></span> <span data-ttu-id="a0b6d-123">Kui klient lähetab olemasolevale aadressile, kus on juba konfigureeritud maksugrupp, kasutatakse olemasolevat maksugruppi.</span><span class="sxs-lookup"><span data-stu-id="a0b6d-123">If the customer is shipping to an existing address that has a tax group that is already configured, the existing tax group will be used.</span></span> <span data-ttu-id="a0b6d-124">Vaikimisi ei ole aadressidel loomisel maksugruppi.</span><span class="sxs-lookup"><span data-stu-id="a0b6d-124">By default, addresses don't have a tax group when they are created.</span></span>

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a><span data-ttu-id="a0b6d-125">Üldiste käibemaksugruppide konfigureerimine Commerce Headquartersis</span><span class="sxs-lookup"><span data-stu-id="a0b6d-125">Configure general sales tax groups in Commerce headquarters</span></span>

<span data-ttu-id="a0b6d-126">Commerce headquarters\`is kannete redigeerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a0b6d-126">To configure general sales tax groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a0b6d-127">Avage **Maks \> Kaudsed maksud \> Käibemaks \> Käibemaksu grupid**.</span><span class="sxs-lookup"><span data-stu-id="a0b6d-127">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax group**.</span></span>
1. <span data-ttu-id="a0b6d-128">Valige vasakul navigeerimisl konfigureeritav maksugrupp.</span><span class="sxs-lookup"><span data-stu-id="a0b6d-128">In the left navigation, select the tax group to configure.</span></span>
1. <span data-ttu-id="a0b6d-129">Konfigureerige **Jaemüügipõhine maks** kiirvahekaardil maksud grupile käibemaks.</span><span class="sxs-lookup"><span data-stu-id="a0b6d-129">On the **Retail destination based tax** FastTab, configure the taxes for the sales tax group.</span></span>

> [!NOTE]
> <span data-ttu-id="a0b6d-130">Lähetamiseks, mis ei sisalda kliendi aadressi käibemaksu, määratlege maksugrupp rea tarneaadress ja maksugrupi jaoks konfigureeritud sihtkohapõhised maksud.</span><span class="sxs-lookup"><span data-stu-id="a0b6d-130">For shipping that doesn't involve sales tax on the customer's address, the delivery address of the line and the destination-based taxes that are configured for the tax group determine the tax group.</span></span> <span data-ttu-id="a0b6d-131">Lisateavet vt teemast [Seadista maksud veebipoodidele vastavalt asukohale](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="a0b6d-131">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a0b6d-132">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a0b6d-132">Additional resources</span></span>

[<span data-ttu-id="a0b6d-133">Käibemaksu konfigureerimine veebitellimuste jaoks</span><span class="sxs-lookup"><span data-stu-id="a0b6d-133">Configure sales tax for online orders</span></span>](../sales-tax-config.md)
