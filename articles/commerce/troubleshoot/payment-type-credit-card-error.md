---
title: Maksetüübiks peab olema müügitellimuse lehel märgitud krediitkaarditõrge
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui müügitellimuse lehel näidatakse tõrketeadet, pärast tellimuse sünkroonimist.
author: Reza-Assadi
manager: AnnBe
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
ms.openlocfilehash: 20f18507dee330fd1affedeee092b3dfa7cc10bc
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585286"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a><span data-ttu-id="18ce7-103">"Maksetüübiks peab olema müügitellimuse lehel märgitud krediitkaarditõrge</span><span class="sxs-lookup"><span data-stu-id="18ce7-103">"Payment type must be credit card" error on the sales order page</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="18ce7-104">See teema annab tõrkeotsingu juhised, mis aitavad, kui müügitellimuse lehel näidatakse tõrketeadet, pärast tellimuse sünkroonimist.</span><span class="sxs-lookup"><span data-stu-id="18ce7-104">This topic provides troubleshooting guidance that can help when an error message is shown on the sales order page after an order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="18ce7-105">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="18ce7-105">Description</span></span>

<span data-ttu-id="18ce7-106">Kui avate müügitellimuse lehe pärast tellimuse sünkroonimist, kuvatakse järgmine tõrketeade: "Maksetüüp peab olema krediitkaart, kuna krediitkaardi number on määratud."</span><span class="sxs-lookup"><span data-stu-id="18ce7-106">When you open the sales order page after you sync an order, you receive the following error message: "The payment type must be credit card, since the credit card number has been specified."</span></span>

![Makse tüüp peab olema krediitkaardi tõrge](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a><span data-ttu-id="18ce7-108">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="18ce7-108">Resolution</span></span>

### <a name="set-the-payment-type-in-commerce-headquarters"></a><span data-ttu-id="18ce7-109">Häälestage maksetüüp Commerce Headquarters\`is</span><span class="sxs-lookup"><span data-stu-id="18ce7-109">Set the payment type in Commerce headquarters</span></span>

1. <span data-ttu-id="18ce7-110">Avage **Müügireskontro \> Maksete seadistus \> Maksetingimused**.</span><span class="sxs-lookup"><span data-stu-id="18ce7-110">Go to **Accounts receivable \> Payment setup \> Terms of payment**.</span></span>
1. <span data-ttu-id="18ce7-111">Valige vasakul navigeerimisribal oma maksetingimused.</span><span class="sxs-lookup"><span data-stu-id="18ce7-111">In the left navigation, select your terms of payment.</span></span>
1. <span data-ttu-id="18ce7-112">Veenduge, et **Maksetüüp** väljal on **Krediitkaart** valitud.</span><span class="sxs-lookup"><span data-stu-id="18ce7-112">In the **Payment type** field, make sure that **Credit card** is selected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18ce7-113">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="18ce7-113">Additional resources</span></span>

[<span data-ttu-id="18ce7-114">Veebimüügi ja -maksete sisestamine</span><span class="sxs-lookup"><span data-stu-id="18ce7-114">Posting of online sales and payments</span></span>](../tasks/posting-online-sales-payments.md)
