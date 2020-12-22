---
title: Kaupade tagastamine mitme klienditellimuse ja -arve alusel
description: Selles teemas kirjeldatakse funktsiooni, mis võimaldab teenuses Dynamics 365 Commerce tagastusi mitme klienditellimuse ja -arve alusel.
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
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
ms.openlocfilehash: e95f06ffaaf2d250b02a8458faa2d9e0b5ef5631
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458827"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="85e6f-103">Kaupade tagastamine mitme klienditellimuse ja -arve alusel</span><span class="sxs-lookup"><span data-stu-id="85e6f-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="85e6f-104">Selles artiklis kirjeldatakse kaht funktsiooni, millega optimeeritakse klienditellimuse tagastusi mitme arve korral.</span><span class="sxs-lookup"><span data-stu-id="85e6f-104">This article describes two features that optimize customer order returns over multiple invoices.</span></span> 

## <a name="enable-refunds-over-multiple-captures"></a><span data-ttu-id="85e6f-105">Tagasimaksete lubamine mitme hõive korral</span><span class="sxs-lookup"><span data-stu-id="85e6f-105">Enable refunds over multiple captures</span></span>

<span data-ttu-id="85e6f-106">See funktsioon võimaldab mitut lingitud tagasimakset sama klienditellimuse alusel.</span><span class="sxs-lookup"><span data-stu-id="85e6f-106">This feature enables multiple linked refunds against the same customer order.</span></span> 

1. <span data-ttu-id="85e6f-107">Avage tööruum **Funktsioonihaldus** ja otsige märksõna **Tagasimaksete lubamine mitme hõive korral**.</span><span class="sxs-lookup"><span data-stu-id="85e6f-107">Go to the **Feature management** workspace and search for **Enable refunds over multiple captures**.</span></span>
2. <span data-ttu-id="85e6f-108">Valige **Tagasimaksete lubamine mitme tellimuse korral** ja seejärel klõpsake nuppu **Luba**.</span><span class="sxs-lookup"><span data-stu-id="85e6f-108">Select **Enable refunds over multiple orders** and then click **Enable**.</span></span> 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a><span data-ttu-id="85e6f-109">Luba osalise kogusega tagastuste korral nõuetekohane maksuarvutus</span><span class="sxs-lookup"><span data-stu-id="85e6f-109">Enable proper tax calculation for returns with partial quantity</span></span>

<span data-ttu-id="85e6f-110">Funktsioon tagab selle, et kui tellimus tagastatakse mitme arvega, võrduvad maksud lõpuks algselt tasutud maksusummaga.</span><span class="sxs-lookup"><span data-stu-id="85e6f-110">This feature ensures that when an order is returned using multiple invoices, the taxes will ultimately be equal to the tax amount originally charged.</span></span> 

1. <span data-ttu-id="85e6f-111">Avage tööruum **Funktsioonihaldus** ja otsige märksõna **Luba osalise kogusega tagastuste korral nõuetekohane maksuarvutus**.</span><span class="sxs-lookup"><span data-stu-id="85e6f-111">Go to the **Feature management** workspace and search for **Enable proper tax calculation for returns with partial quantity**.</span></span>
2. <span data-ttu-id="85e6f-112">Valige **Luba osalise kogusega tagastuste korral nõuetekohane maksuarvutus** ja klõpsake seejärel nuppu **Luba**.</span><span class="sxs-lookup"><span data-stu-id="85e6f-112">Select **Enable proper tax calculation for returns with partial quantity** and then click **Enable**.</span></span> 


## <a name="process-returns"></a><span data-ttu-id="85e6f-113">Tagastuste töötlemine</span><span class="sxs-lookup"><span data-stu-id="85e6f-113">Process returns</span></span>

<span data-ttu-id="85e6f-114">Pärast seda, kui need funktsioonid on sisse lülitatud ja muudatused on kauplustega sünkroonitud, võib kaupluse kassapidaja tagastamiseks valida mitu kliendi müügitellimust.</span><span class="sxs-lookup"><span data-stu-id="85e6f-114">After these features are turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="85e6f-115">Tellimuste valimisel kuvatakse kõikide tellimuste arvete kõik tagastatavad tooted.</span><span class="sxs-lookup"><span data-stu-id="85e6f-115">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="85e6f-116">Kassapidaja võib seejärel valida tagastatavad tooted.</span><span class="sxs-lookup"><span data-stu-id="85e6f-116">The cashier can then select the products to return.</span></span> <span data-ttu-id="85e6f-117">Valitud toodete kohta luuakse üks tagastustellimus.</span><span class="sxs-lookup"><span data-stu-id="85e6f-117">A single return order will be created for all the selected products.</span></span>

<span data-ttu-id="85e6f-118">Kui tellimus on täielikult tagastatud, võrdub kliendile tagastatav maksude summa algselt tasutud maksusummaga.</span><span class="sxs-lookup"><span data-stu-id="85e6f-118">If the order is fully returned, the amount of taxes returned to the customer will be equal to the amount of tax originally charged.</span></span>

