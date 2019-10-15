---
title: Kaupade tagastamine mitme klienditellimuse ja -arve alusel
description: Selles teemas kirjeldatakse funktsiooni, mis võimaldab teenuses Dynamics 365 Retail tagastada mitme klienditellimuse ja -arved alusel.
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
ms.openlocfilehash: 25a1081e5f903076e23089c41dda7437f8a70124
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017985"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="217c3-103">Kaupade tagastamine mitme klienditellimuse ja -arve alusel</span><span class="sxs-lookup"><span data-stu-id="217c3-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="217c3-104">Tagastamisi saab teha mitme tellimuse ja arve alusel.</span><span class="sxs-lookup"><span data-stu-id="217c3-104">Returns can be made across multiple orders and invoices.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="217c3-105">Retaili konfigureerimine mitme klienditellimuse ja -arve alusel tagastuste toetamiseks</span><span class="sxs-lookup"><span data-stu-id="217c3-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="217c3-106">Valige **Retaili parameetrid \> Klienditellimused**.</span><span class="sxs-lookup"><span data-stu-id="217c3-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="217c3-107">Lülitage sisse parameeter **Luba mitme tellimuse tagastamine**.</span><span class="sxs-lookup"><span data-stu-id="217c3-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="217c3-108">Tagastuste töötlemine</span><span class="sxs-lookup"><span data-stu-id="217c3-108">Process returns</span></span>

<span data-ttu-id="217c3-109">Pärast seda, kui parameeter on sisse lülitatud ja muudatused on kauplustega sünkroonitud, võib kaupluse kassapidaja tagastamiseks valida mitu kliendi müügitellimust.</span><span class="sxs-lookup"><span data-stu-id="217c3-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="217c3-110">Tellimuste valimisel kuvatakse kõikide tellimuste arvete kõik tagastatavad tooted.</span><span class="sxs-lookup"><span data-stu-id="217c3-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="217c3-111">Kassapidaja võib seejärel valida tagastatavad tooted.</span><span class="sxs-lookup"><span data-stu-id="217c3-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="217c3-112">Valitud toodete kohta luuakse üks tagastustellimus.</span><span class="sxs-lookup"><span data-stu-id="217c3-112">A single return order will be created for all the selected products.</span></span>
