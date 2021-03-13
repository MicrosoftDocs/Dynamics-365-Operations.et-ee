---
title: Kliendikonto makseviisi konfigureerimine B2B e-kaubanduse saitide jaoks
description: Selles teemas kirjeldatakse, kuidas konfigureerida kliendikonto makseviisi ettevõtetevahelise (B2B) e-kaubanduse saitide jaoks.
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
ms.openlocfilehash: 754e2f83d6c8ff5d3698d98062e54bba7ccd9836
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035896"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a><span data-ttu-id="595cd-103">Kliendikonto makseviisi konfigureerimine B2B e-kaubanduse saitide jaoks</span><span class="sxs-lookup"><span data-stu-id="595cd-103">Configure the customer account payment method for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="595cd-104">Selles teemas kirjeldatakse, kuidas konfigureerida kliendikonto makseviisi ettevõtetevahelise (B2B) e-kaubanduse saitide jaoks.</span><span class="sxs-lookup"><span data-stu-id="595cd-104">This topic describes how to configure the customer account payment method for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="595cd-105">Jaemüüjad võivad võtta e-kaubanduse kanalis müüdavate toodete ja teenuste eest tasu erinevat tüüpi maksemeetoditega.</span><span class="sxs-lookup"><span data-stu-id="595cd-105">Retailers can accept various types of payment in exchange for the products and services that they sell in an e-commerce channel.</span></span> <span data-ttu-id="595cd-106">Kõik jaemüüja aktsepteeritavad maksetüübid tuleb konfigureerida süsteemi seadistamisel rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="595cd-106">Each payment type that a retailer accepts must be configured in Microsoft Dynamics 365 Commerce when the system is set up.</span></span> <span data-ttu-id="595cd-107">B2B e-kaubanduse saitidel peab toetama kliendikonto (või "ettemaksi") makseviisi.</span><span class="sxs-lookup"><span data-stu-id="595cd-107">The customer account (or "on account") payment method must be supported on B2B e-commerce sites.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="595cd-108">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="595cd-108">Prerequisites</span></span>

1. <span data-ttu-id="595cd-109">Lisage kliendikonto makseviis Commerce'i peakontoris.</span><span class="sxs-lookup"><span data-stu-id="595cd-109">Add the customer account payment method in Commerce headquarters.</span></span>
2. <span data-ttu-id="595cd-110">Siduge kliendikonto makseviis e-kaubanduse kanaliga.</span><span class="sxs-lookup"><span data-stu-id="595cd-110">Associate the customer account payment method with the e-commerce channel.</span></span>
3. <span data-ttu-id="595cd-111">Veenduge, et säte **Luba kontol** on kliendi jaoks Commerce'i peakontori jaotises **Jaemüük ja kaubandus \> Kliendid \> Kõik kliendid \> Makse vaikesätted** lubatud.</span><span class="sxs-lookup"><span data-stu-id="595cd-111">Make sure that **Allow on account** is enabled for the customer at **Retail and Commerce \> Customers \> All customers \> Payment defaults** in Commerce headquarters.</span></span> <span data-ttu-id="595cd-112">Veenduga ka, et parameetrid **Krediidilimiit** on kliendi jaoks õigesti seadistatud Commerce'i peakontori jaotises **Jaemüük ja kaubandus \> Kliendid \> Kõik kliendid \> Krediit ja võlanõuded**.</span><span class="sxs-lookup"><span data-stu-id="595cd-112">Also make sure that **Credit limit** parameters are set appropriately for the customer at **Retail and Commerce \> Customers \> All customers \> Credit and Collections** in Commerce headquarters.</span></span> 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a><span data-ttu-id="595cd-113">Kliendikonto makseviisi lubamine Commerce'i saidiehitajas</span><span class="sxs-lookup"><span data-stu-id="595cd-113">Enable the customer account payment method in Commerce site builder</span></span> 

<span data-ttu-id="595cd-114">Kliendikonto makseviisi lubamiseks Commerce'i saidiehitajas toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="595cd-114">To enable the customer account payment method in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="595cd-115">Avage **Saidi sätted \> Laiendused**.</span><span class="sxs-lookup"><span data-stu-id="595cd-115">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="595cd-116">Seadke atribuut **Luba kliendikonto maksed** väärtusele **B2B-klientidele lubatud**.</span><span class="sxs-lookup"><span data-stu-id="595cd-116">Set the **Enable customer account payments** property to **Enabled for B2B customers**.</span></span> 
1. <span data-ttu-id="595cd-117">Valige suvand **Salvesta ja avalda**.</span><span class="sxs-lookup"><span data-stu-id="595cd-117">Select **Save and Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="595cd-118">Uued saidi sätted jõustuvad alles pärast faili app.settings.json värskendamist.</span><span class="sxs-lookup"><span data-stu-id="595cd-118">The new site settings take effect only after the app.settings.json file is updated.</span></span> <span data-ttu-id="595cd-119">Lisateabe saamiseks vt [SDK ja mooduliteegi värskendused](../e-commerce-extensibility/sdk-updates.md).</span><span class="sxs-lookup"><span data-stu-id="595cd-119">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md).</span></span>

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a><span data-ttu-id="595cd-120">Kliendikonto makseviisi lubamine B2B e-kaubanduse saidi kassa lehel</span><span class="sxs-lookup"><span data-stu-id="595cd-120">Enable the customer account payment method on the checkout page for the B2B e-commerce site</span></span>

<span data-ttu-id="595cd-121">Kliendikonto makseviisi lubamiseks B2B e-kaubanduse saidi kassa lehel toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="595cd-121">To enable the customer account payment method on the checkout page for the B2B e-commerce site, follow these steps.</span></span>

1. <span data-ttu-id="595cd-122">Leidke ja redigeeride Commerce'i saidiehitajas kassa lehte või fragmenti, mis sisaldab kassamoodulit B2B e-kaubanduse saidi jaoks.</span><span class="sxs-lookup"><span data-stu-id="595cd-122">In Commerce site builder, find and edit the checkout page or fragment that contains the checkout module for the B2B e-commerce site.</span></span>
1. <span data-ttu-id="595cd-123">Valige lahtrist **Kassa jaotise konteiner** käsk **Lisa moodul** ja seejärel lisage moodul **Kliendikonto makse**.</span><span class="sxs-lookup"><span data-stu-id="595cd-123">In the **Checkout section container** slot, select **Add Module**, and then add a **Customer account payment** module.</span></span>
1. <span data-ttu-id="595cd-124">Paigutage moodul **Kliendikonto makse** valides kolmikpunkti (**...**) ja seejärel valides vastavalt vajadusele kas **Nihuta üles** või **Nihuta alla**.</span><span class="sxs-lookup"><span data-stu-id="595cd-124">Position the **Customer account payment** module by selecting the ellipsis (**...**), and then selecting **Move Up** or **Move Down** as required.</span></span>
1. <span data-ttu-id="595cd-125">Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="595cd-125">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a><span data-ttu-id="595cd-126">Kinnitage, et kliendikonto makseviis on lubatud ja avaldatud.</span><span class="sxs-lookup"><span data-stu-id="595cd-126">Confirm that the customer account payment method has been enabled and published</span></span>

<span data-ttu-id="595cd-127">Kinnitamiseks, et kliendikonto makseviis on lubatud ja avaldatud, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="595cd-127">To confirm that the customer account payment method has been enabled, follow these steps.</span></span>

1. <span data-ttu-id="595cd-128">Logige e-kaubanduse saidile sisse.</span><span class="sxs-lookup"><span data-stu-id="595cd-128">Sign in to the e-commerce site.</span></span>
1. <span data-ttu-id="595cd-129">Lisage toode ostukorvi.</span><span class="sxs-lookup"><span data-stu-id="595cd-129">Add a product to the cart.</span></span>
1. <span data-ttu-id="595cd-130">Minge kassa lehele.</span><span class="sxs-lookup"><span data-stu-id="595cd-130">Go to the checkout page.</span></span> <span data-ttu-id="595cd-131">Peaksite nägema uut makseviisi **Kliendikonto**.</span><span class="sxs-lookup"><span data-stu-id="595cd-131">You should see the new **Customer Account** payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="595cd-132">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="595cd-132">Additional resources</span></span>

[<span data-ttu-id="595cd-133">B2B e-kaubanduse saidi seadistamine</span><span class="sxs-lookup"><span data-stu-id="595cd-133">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="595cd-134">B2B organisatsioonidele organisatsiooni modelleerimise hierarhiate loomine.</span><span class="sxs-lookup"><span data-stu-id="595cd-134">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="595cd-135">Äripartnerist kasutajate haldamine B2B e-kaubanduse saitidel</span><span class="sxs-lookup"><span data-stu-id="595cd-135">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="595cd-136">Toote koguse piirangute määramine B2B e-kaubanduse saitide jaoks</span><span class="sxs-lookup"><span data-stu-id="595cd-136">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)

[<span data-ttu-id="595cd-137">SDK ja mooduliteegi värskendused</span><span class="sxs-lookup"><span data-stu-id="595cd-137">SDK and Module library updates</span></span>](../e-commerce-extensibility/sdk-updates.md)
