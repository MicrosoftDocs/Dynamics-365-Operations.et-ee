---
title: Toote koguse piirangute määramine B2B e-kaubanduse saitide jaoks
description: Selles teemas kirjeldatakse ettevõtetevahelise (B2B) e-kaubanduse saitidele toote koguse piirangute seadistamist.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1208b968e476ccbc7a726facf1db896c7bf3c36f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211173"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a><span data-ttu-id="5e3b8-103">Toote koguse piirangute määramine B2B e-kaubanduse saitide jaoks</span><span class="sxs-lookup"><span data-stu-id="5e3b8-103">Set product quantity limits for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5e3b8-104">Selles teemas kirjeldatakse ettevõtetevahelise (B2B) e-kaubanduse saitidele toote koguse piirangute seadistamist.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-104">This topic describes how to set product quantity limits for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="5e3b8-105">Enamikel toodetel on mõõtühik, mis määratleb nende grupeerimise.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-105">Most products have a unit of measure that defines their grouping.</span></span> <span data-ttu-id="5e3b8-106">Grupeerimine mõjutab seda, kuidas tooteid saab müüa.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-106">The grouping affects how the products can be sold.</span></span> <span data-ttu-id="5e3b8-107">Mõnel tootel võib koguste jaoks olla täiendav grupeerimine.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-107">Some products might have an additional grouping for quantities.</span></span> <span data-ttu-id="5e3b8-108">See grupeerimine määrab, kas tooteid saab müüa üksikult või kordühikuna ja kas on olemas minimaalne või maksimaalne tellimuse koguse piirang, mida tuleb järgida.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-108">This grouping determines whether the products can be sold as individual units or multiples, and whether there is a minimum or maximum order quantity limit that must be followed.</span></span>

<span data-ttu-id="5e3b8-109">Koguse piiramise funktsioon tagab, et minimaalsed, maksimaalsed, mitmekordsed ja standardkogused, mis on konfigureeritud rakenduses Microsoft Dynamics 365 Commerce (vaiketellimuse sätetes või Commerce'i saidiehitaja saidisätetes) rakendatakse klienditellimustele, e-kaubanduse saidil esitatakse.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-109">The quantity limiting feature ensures that the minimum, maximum, multiple, and standard quantities that are configured in Microsoft Dynamics 365 Commerce (in the default order settings or the Commerce site builder site settings) are applied to customer orders that are placed on an e-commerce site.</span></span> <span data-ttu-id="5e3b8-110">Toote koguse piiranguid praegu kassas ja kõnekeskustes ei toetata.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-110">Product quantity limits aren't currently supported for the point of sale (POS) and call centers.</span></span>

<span data-ttu-id="5e3b8-111">Paljud jaemüüjad pakuvad mitmesuguste toote- ja täitmisnõuete täitmiseks klienditellimuste (tuntud ka kui eritellimused) võimalust.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-111">Many retailers provide the option of customer orders (also known as special orders) to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="5e3b8-112">Tüüpilised stsenaariumid on näiteks järgmised.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-112">Here are some typical scenarios:</span></span>

- <span data-ttu-id="5e3b8-113">Klient soovib, et kindlate variantide tooteid müüdaks mitme kaupa.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-113">A customer wants products of specific variants to be sold in multiples of a few.</span></span>
- <span data-ttu-id="5e3b8-114">Klient soovib tooted kätte saada teisest poest või asukohast kui see, kust ta tooted ostis.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-114">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span> <span data-ttu-id="5e3b8-115">Kaupluste pakkimisstandardid erinevad siiski veebimüügi pakkimisstandarditest.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-115">However, the packing standards for the stores differ from the packing standards for online sales distribution.</span></span>
- <span data-ttu-id="5e3b8-116">Klient soovib osta piiratud versiooniga toodet, millel on maksimaalse ostetava koguse piirang.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-116">A customer wants to buy a limited-edition product that has a maximum quantity limit for items that can be purchased.</span></span>

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a><span data-ttu-id="5e3b8-117">Commerce'i peakontoris tellimuse vaikesätete funktsiooni sisse lülitamine</span><span class="sxs-lookup"><span data-stu-id="5e3b8-117">Turn on the default order settings feature in Commerce headquarters</span></span>

<span data-ttu-id="5e3b8-118">Enne toote kogusepiirangute seadmist tuleb tellimuse vaikesätete funktsioon Commerce'i peakontoris sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-118">Before you can set product quantity limits, the default order settings feature must be turned on in Commerce headquarters.</span></span>

<span data-ttu-id="5e3b8-119">Tellimuse vaikesätete sisselülitamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-119">To turn on the default order settings feature, follow these steps.</span></span>

1. <span data-ttu-id="5e3b8-120">Avage **Süsteemihaldus \> Tööruumid \> Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-120">Go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="5e3b8-121">Leidke ja valige funktsioon **Tellimuse saidi- ja vaikseätete toetamine klienditellimustes**.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-121">Find and select the **Support the Site and Default order settings in the customer order** feature.</span></span>
1. <span data-ttu-id="5e3b8-122">Valige parempoolse paani allosas suvand **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-122">At the bottom of the right pane, select **Enable now**.</span></span> 

## <a name="define-quantity-settings"></a><span data-ttu-id="5e3b8-123">Koguse sätete määratlemine</span><span class="sxs-lookup"><span data-stu-id="5e3b8-123">Define quantity settings</span></span> 

<span data-ttu-id="5e3b8-124">Lehel **Tellimuse vaikesätted** saate määratleda koguse sätted.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-124">You can define the quantity settings on the **Default order settings** page.</span></span>

<span data-ttu-id="5e3b8-125">Koguse sätete määratlemiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-125">To define the quantity settings, follow these steps.</span></span> 

1. <span data-ttu-id="5e3b8-126">Avage toote **Jaemüük ja kaubandus \> Tooted ja kategooriad \> Väljastatud tooted kategooria järgi**.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-126">Go to Product **Retail and Commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="5e3b8-127">Valige väljastatud toode.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-127">Select a released product.</span></span>
1. <span data-ttu-id="5e3b8-128">Valige toimingupaani vahekaardil **Varude haldus** grupis **Tellimuse sätted** suvand **Tellimuse vaikesätted**.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-128">On the Action Pane, on the **Manage inventory** tab, in the **Order settings** group, select **Default order settings**.</span></span> 
1. <span data-ttu-id="5e3b8-129">Seadke toote müügikogused jaotise **Müügikogus** kiirkaardil **Müügitellimus** lehel **Tellimuse vaikesätted**.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-129">On the **Default order settings** page, on the **Sales order** FastTab, in the **Sales quantity** section, set the product sales quantities:</span></span>

    - <span data-ttu-id="5e3b8-130">**Mitu** - kogus, mille kordades toodet osta saab.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-130">**Multiple** – The quantity that the product can be bought in multiples of.</span></span>
    - <span data-ttu-id="5e3b8-131">**Minimaalne tellimuse kogus** - minimaalne ostetavate toodete arv.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-131">**Minimum Order Quantity** – The minimum number of products that must be purchased.</span></span>
    - <span data-ttu-id="5e3b8-132">**Maksimaalne tellimuse kogus** - maksimaalne ostetavate toodete arv.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-132">**Maximum Order Quantity** – The maximum number of products that can be purchased.</span></span>
    - <span data-ttu-id="5e3b8-133">**Standardne toote kogus** - vaikekogus, mis sisestatakse automaatselt toote valimisel.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-133">**Standard Order Quantity** – The default quantity that is automatically entered when the product is selected.</span></span>

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a><span data-ttu-id="5e3b8-134">Commerce'i saidiehitajas B2B toote koguse piirangute funktsiooni sisse lülitamine</span><span class="sxs-lookup"><span data-stu-id="5e3b8-134">Turn on the B2B order quantity limits feature in Commerce site builder</span></span>

<span data-ttu-id="5e3b8-135">Commerce'i saidiehitajas B2B toote koguse piirangute funktsiooni sisse lülitamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-135">To turn on the B2B order quantity limits feature in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="5e3b8-136">Avage **Saidi sätted \> Laiendused**</span><span class="sxs-lookup"><span data-stu-id="5e3b8-136">Go to **Site settings \> Extensions**</span></span>
1. <span data-ttu-id="5e3b8-137">Valige jaotises **Luba tellimuse koguse piirangud** ripploendist **Lubatud B2B klientide jaoks**.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-137">Under **Enable Order Quantity Limits**, select **Enabled for B2B customers** in the drop-down menu.</span></span> 

> [!NOTE] 
> <span data-ttu-id="5e3b8-138">Värskendatud saidiehitaja sätted jõustuvad alles pärast faili app.settings.json värskendamist.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-138">Updated site builder settings take effect only after the app.settings.json file has been updated.</span></span> <span data-ttu-id="5e3b8-139">Lisateabe saamiseks vt [SDK ja mooduliteegi värskendused](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="5e3b8-139">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5e3b8-140">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="5e3b8-140">Additional resources</span></span>

[<span data-ttu-id="5e3b8-141">B2B e-kaubanduse saidi seadistamine</span><span class="sxs-lookup"><span data-stu-id="5e3b8-141">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="5e3b8-142">B2B organisatsioonidele organisatsiooni modelleerimise hierarhiate loomine.</span><span class="sxs-lookup"><span data-stu-id="5e3b8-142">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="5e3b8-143">Äripartnerkasutajate haldamine B2B e-kaubandussaitidel</span><span class="sxs-lookup"><span data-stu-id="5e3b8-143">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="5e3b8-144">Kliendikonto makseviisi konfigureerimine B2B e-kaubanduse saitide jaoks</span><span class="sxs-lookup"><span data-stu-id="5e3b8-144">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]