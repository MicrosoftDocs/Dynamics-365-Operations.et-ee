---
title: Kviitungita tagastuste makseviiside piiramine
description: Selles teemas kirjeldatakse, kuidas saab teatud maksetüüpide puhul tagasimakse keelata, kui tagastus toimub ilma kviitungita.
author: rapraj
manager: AnnBe
ms.date: 013/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 6e2c32aae06ce7bbdde30809d7a197f43b856af1
ms.sourcegitcommit: bacec397ee48ac583596be156c87ead474ee07df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/05/2019
ms.locfileid: "777173"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="33030-103">Kviitungita tagastuste makseviiside piiramine</span><span class="sxs-lookup"><span data-stu-id="33030-103">Restrict payment methods for returns without a receipt</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="33030-104">Kõik jaemüüja aktsepteeritavad maksetüübid tuleb konfigureerida süsteemi seadistamisel.</span><span class="sxs-lookup"><span data-stu-id="33030-104">Each payment type that a retailer accepts must be configured when the system is set up.</span></span> <span data-ttu-id="33030-105">Selles teemas kirjeldatakse, kuidas saab teatud maksetüüpide puhul tagasimakse keelata, kui tagastus toimub ilma kviitungita.</span><span class="sxs-lookup"><span data-stu-id="33030-105">This topic describes how certain payment types can be restricted for refund if the returns are made without a receipt.</span></span>

## <a name="set-up-payment-methods"></a><span data-ttu-id="33030-106">Seadistada maksemeetodid</span><span class="sxs-lookup"><span data-stu-id="33030-106">Set up payment methods</span></span>

<span data-ttu-id="33030-107">Makseviiside seadistamiseks täitke järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="33030-107">To set up payment methods, the following tasks must be completed.</span></span>
1. <span data-ttu-id="33030-108">Looge makseviisid, mida aktsepteerib kogu organisatsioon.</span><span class="sxs-lookup"><span data-stu-id="33030-108">Create the payment methods that are accepted by the entire organization.</span></span>
2. <span data-ttu-id="33030-109">Üleorganisatsiooniliste kaarditüüpide ja kaardi numbrite loomine.</span><span class="sxs-lookup"><span data-stu-id="33030-109">Create organization-wide card types and card numbers.</span></span> <span data-ttu-id="33030-110">Kui aktsepteeritakse krediit- või deebetkaarte, peate looma ühe makseviisi kaartidele ja looma seejärel üleorganisatsioonilised kaarditüübid ja kaardi numbrid.</span><span class="sxs-lookup"><span data-stu-id="33030-110">If credit cards or debit cards are accepted, you must create one payment method for cards, and then create the organization-wide card types and card numbers.</span></span>
3. <span data-ttu-id="33030-111">Seadistage kaupluse makseviisid.</span><span class="sxs-lookup"><span data-stu-id="33030-111">Set up store payment methods.</span></span> <span data-ttu-id="33030-112">Seostage makseviisid iga kauplusega ja seejärel sisestage iga kaupluse makseviisile kauplusepõhised sätted.</span><span class="sxs-lookup"><span data-stu-id="33030-112">Associate payment methods with each store, and then enter the store-specific settings for each payment method.</span></span>
4. <span data-ttu-id="33030-113">Seadistage kauplustele kaardimakseviisid.</span><span class="sxs-lookup"><span data-stu-id="33030-113">Set up card payment methods for stores.</span></span> <span data-ttu-id="33030-114">Tehke kaardiseadistus kõikidele kaardimakseviisidele, mida kauplus aktsepteerib.</span><span class="sxs-lookup"><span data-stu-id="33030-114">For any card payment methods that the store accepts, complete the card setup.</span></span>

<span data-ttu-id="33030-115">![Kaupluse seadistus](media/NoReceiptReturns1.png "Kaupluse seadistus")</span><span class="sxs-lookup"><span data-stu-id="33030-115">![Retail Store Setup](media/NoReceiptReturns1.png "Retail Store Setup")</span></span> 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="33030-116">Kviitungita tagastuste makseviiside piiramine</span><span class="sxs-lookup"><span data-stu-id="33030-116">Restrict payment methods for returns without a receipt</span></span>

<span data-ttu-id="33030-117">Kaupluse iga makseviisi puhul valige lehel **Kaupluse haldus** jaotises **Kviitungita tagastused** suvandi **Keela kviitungita tagasimaksed** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="33030-117">For each store payment method, on the **Retail store management** page, under **Non receipt returns**, set **Restrict for refunds without receipt** to **Yes**.</span></span> 

<span data-ttu-id="33030-118">Ümberlülitusklahvi vaikeväärtus on **Ei**, mis tagab, et tagasimaksete puhul on makseviis lubatud.</span><span class="sxs-lookup"><span data-stu-id="33030-118">The default value of the toggle is **No**, which ensures that the payment method is allowed for refunds.</span></span> 

<span data-ttu-id="33030-119">Kui suvandi **Keela kviitungita tagasimaksed** sätteks on valitud **Jah**, ei lubata valitud makseviisi tagasimaksete puhul.</span><span class="sxs-lookup"><span data-stu-id="33030-119">When **Restrict for refunds without receipt** is set to **Yes**, the selected payment method will not be allowed for refunds.</span></span> 

<span data-ttu-id="33030-120">![Kaupluse makseviis](media/NoReceiptReturns3.png "Kaupluse makseviis")</span><span class="sxs-lookup"><span data-stu-id="33030-120">![Retail Store payment method](media/NoReceiptReturns3.png "Retail Store Payment Method")</span></span> 

> [!NOTE]
> <span data-ttu-id="33030-121">Kui kassapidaja valib makseviisi, mille puhul on kviitungita tagasimakse keelatud, kuvatakse teade, mis palub kontrollida lubatud makseviise.</span><span class="sxs-lookup"><span data-stu-id="33030-121">When a cashier selects a payment method that is restricted for refund without a receipt, a message displays to verify the acceptable payment methods.</span></span>

<span data-ttu-id="33030-122">![Lubatud makseviisid](media/NoReceiptReturns4.png "Lubatud makseviisid")</span><span class="sxs-lookup"><span data-stu-id="33030-122">![Acceptable payment methods](media/NoReceiptReturns4.png "Acceptable payment methods")</span></span> 

<span data-ttu-id="33030-123">Kui kandel on nii kviitungiga tagastus kui ka kviitungita tagastus, siis piirangutingimusi ei rakendata, kuna kanne on kviitungiga tagastusvoog.</span><span class="sxs-lookup"><span data-stu-id="33030-123">If a transaction has both a receipted return and a return without a receipt, the restriction conditions will not be enforced because the transaction will be a return workflow with a receipt.</span></span> 

