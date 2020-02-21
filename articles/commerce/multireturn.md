---
title: Kaupade tagastamine mitme klienditellimuse ja -arve alusel
description: Selles teemas kirjeldatakse funktsiooni, mis võimaldab teenuses Dynamics 365 Commerce tagastusi mitme klienditellimuse ja -arve alusel.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: c5f17424f0837344030f9ce2d2d037cde08c4e49
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004454"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="edea9-103">Kaupade tagastamine mitme klienditellimuse ja -arve alusel</span><span class="sxs-lookup"><span data-stu-id="edea9-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="edea9-104">Tagastamisi saab teha mitme tellimuse ja arve alusel.</span><span class="sxs-lookup"><span data-stu-id="edea9-104">Returns can be made across multiple orders and invoices.</span></span> 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="edea9-105">Kaubanduse konfigureerimine mitme klienditellimuse ja -arve alusel tagastuste toetamiseks</span><span class="sxs-lookup"><span data-stu-id="edea9-105">Configure Commerce to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="edea9-106">Valige **Kaubanduse parameetrid \> Klienditellimused**.</span><span class="sxs-lookup"><span data-stu-id="edea9-106">Go to **Commerce parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="edea9-107">Lülitage sisse parameeter **Luba mitme tellimuse tagastamine**.</span><span class="sxs-lookup"><span data-stu-id="edea9-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="edea9-108">Tagastuste töötlemine</span><span class="sxs-lookup"><span data-stu-id="edea9-108">Process returns</span></span>

<span data-ttu-id="edea9-109">Pärast seda, kui parameeter on sisse lülitatud ja muudatused on kauplustega sünkroonitud, võib kaupluse kassapidaja tagastamiseks valida mitu kliendi müügitellimust.</span><span class="sxs-lookup"><span data-stu-id="edea9-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="edea9-110">Tellimuste valimisel kuvatakse kõikide tellimuste arvete kõik tagastatavad tooted.</span><span class="sxs-lookup"><span data-stu-id="edea9-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="edea9-111">Kassapidaja võib seejärel valida tagastatavad tooted.</span><span class="sxs-lookup"><span data-stu-id="edea9-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="edea9-112">Valitud toodete kohta luuakse üks tagastustellimus.</span><span class="sxs-lookup"><span data-stu-id="edea9-112">A single return order will be created for all the selected products.</span></span>
