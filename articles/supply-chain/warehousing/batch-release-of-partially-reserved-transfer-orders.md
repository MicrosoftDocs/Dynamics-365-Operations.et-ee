---
title: "Osaliselt reserveeritud üleviimistellimuste hulgiväljastamine"
description: "Selles teemas kirjeldatakse, kuidas seadistada ja rakendada mobiilselt seadmelt osaliselt reserveeritud üleviimistellimuste hulgiväljastamist."
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 273ced77a61d485426c0830556e4401e782e86c4
ms.openlocfilehash: 369afe3f4bae223c8d4f9fc55e9cd9744590b6d3
ms.contentlocale: et-ee
ms.lasthandoff: 10/24/2017

---

# <a name="batch-release-of-partially-reserved-transfer-orders"></a><span data-ttu-id="28a4b-103">Osaliselt reserveeritud üleviimistellimuste hulgiväljastamine</span><span class="sxs-lookup"><span data-stu-id="28a4b-103">Batch release of partially reserved transfer orders</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="28a4b-104">Osaliselt reserveeritud üleviimistellimuste hulgiväljastamise funktsioon võimaldab pakett-töö abil üleviimistellimusi osaliselt lattu väljastada.</span><span class="sxs-lookup"><span data-stu-id="28a4b-104">The functionality for batch release of partially reserved transfer orders lets you partially release transfer orders to a warehouse by using a batch job.</span></span>
<span data-ttu-id="28a4b-105">Kuna on olemas osalise koguse väljastamise võimalus, ei pea enne tellimuse väljastamist ootama, et terve tellimuse kogus laos kättesaadav oleks.</span><span class="sxs-lookup"><span data-stu-id="28a4b-105">Because you have the option to release a partial quantity, you don’t have to wait for the whole order quantity to be available in the warehouse before you release an order.</span></span>

<span data-ttu-id="28a4b-106">Tellimuste väljastamine lattu on täpsem laohalduse protsess.</span><span class="sxs-lookup"><span data-stu-id="28a4b-106">The release of orders to a warehouse is an advanced warehouse management process.</span></span> <span data-ttu-id="28a4b-107">See protsess hõlmab tegevusi, nagu komplekteerimine, pakkimine ja saatmine, mida laotöötaja saab mobiilse seadme abil teha.</span><span class="sxs-lookup"><span data-stu-id="28a4b-107">This process involves activities, such as picking, packing, and shipping, that a warehouse worker can perform by using a mobile device.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="28a4b-108">Kus see kehtib</span><span class="sxs-lookup"><span data-stu-id="28a4b-108">Where it applies</span></span>

<span data-ttu-id="28a4b-109">Selle funktsiooni puhul väljastatakse üleviimistellimused lattu pakett-töö abil.</span><span class="sxs-lookup"><span data-stu-id="28a4b-109">For this functionality, transfer orders are released to a warehouse by using a batch job.</span></span> <span data-ttu-id="28a4b-110">See funktsioon on abiks, kui teil pole laos piisavalt varusid, kuid soovite siiski kaupu ühest laost teise üle viia.</span><span class="sxs-lookup"><span data-stu-id="28a4b-110">This functionality is useful when you don’t have enough inventory in the warehouse, but you still want to transfer items from one warehouse to another.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="28a4b-111">Kuidas see seadistatakse</span><span class="sxs-lookup"><span data-stu-id="28a4b-111">How it is set up</span></span>

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="28a4b-112">Määrake üleviimistellimuste ja müügitellimuste täitmise kriteeriumid</span><span class="sxs-lookup"><span data-stu-id="28a4b-112">Specify fulfillment criteria for transfer orders and sales orders</span></span>

<span data-ttu-id="28a4b-113">Enne, kui tellimuse saab osaliselt partiina lattu väljastada, peavad täitmise kriteeriumid olema täidetud.</span><span class="sxs-lookup"><span data-stu-id="28a4b-113">Before an order can be partially released to a warehouse in a batch, the fulfillment criteria must be met.</span></span> <span data-ttu-id="28a4b-114">Need täitmise kriteeriumid määratakse täitmispoliitikaga.</span><span class="sxs-lookup"><span data-stu-id="28a4b-114">These fulfillment criteria are determined by the fulfillment policy.</span></span>

<span data-ttu-id="28a4b-115">Üleviimistellimuste ja müügitellimuste täitmispoliitikad määratakse ettevõtte tasandil.</span><span class="sxs-lookup"><span data-stu-id="28a4b-115">Fulfillment policies for transfer orders and sales orders are specified at the company level.</span></span> <span data-ttu-id="28a4b-116">Olenevalt täitmispoliitika seadistusest võetakse tellimuste väljastamine partiina vastu või lükatakse tagasi.</span><span class="sxs-lookup"><span data-stu-id="28a4b-116">Depending on the setup of the fulfillment policy, the release of orders in a batch will be accepted or rejected.</span></span> <span data-ttu-id="28a4b-117">Seejärel töödeldakse tellimusi vastavalt.</span><span class="sxs-lookup"><span data-stu-id="28a4b-117">The orders will then be processed accordingly.</span></span>

-   <span data-ttu-id="28a4b-118">Üleviimis- ja müügitellimuste täitmispoliitikate koostamiseks klõpsake valikuid **Laohaldus** \> **Seadistus** \> **Lattu väljastamine** \> **Täitmispoliitika** ja koostage siis täitmispoliitika, sisestades nime ja kirjelduse.</span><span class="sxs-lookup"><span data-stu-id="28a4b-118">To create fulfillment policies for transfer orders and sales orders, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then create a fulfillment policy by entering a name and a description.</span></span>

-   <span data-ttu-id="28a4b-119">Et määrata täitmise määr, väärtuse tüüp ja sõnum, mis kuvatakse, kui täitmispoliitikat rikutakse, klõpsake välju **Laohaldus** \> **Seadistus** \> **Lattu väljastamine** \> **Täitmispoliitika** ja määrake siis **Täitmismäär**, **Väärtuse tüüp** ja **Täitmise rikkumise teade**.</span><span class="sxs-lookup"><span data-stu-id="28a4b-119">To specify a fulfillment rate, a value type, and the message that is shown if the fulfillment policy is violated, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then set the **Fulfillment rate**, **Value type**, and **Fulfillment violation message** fields.</span></span>

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="28a4b-120">Määrake üleviimistellimuste ja müügitellimuste täitmise poliitikad</span><span class="sxs-lookup"><span data-stu-id="28a4b-120">Set the fulfillment policies for transfer orders and sales orders</span></span>

-   <span data-ttu-id="28a4b-121">Üleviimistellimuste täitmise poliitikate määramiseks klõpsake valikuid **Varude haldus** \> **Seadistus** \> **Varude ja laohalduse parameetrid** \> **Üleviimistellimused** \> **Laohaldus** ja valige siis üleviimistellimuse täitmise poliitika.</span><span class="sxs-lookup"><span data-stu-id="28a4b-121">To set the fulfillment policies for transfer orders, click **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters** \> **Transfer orders** \> **Warehouse management**, and then select a transfer order fulfillment policy.</span></span>

-   <span data-ttu-id="28a4b-122">Müügitellimuste täitmise poliitikate määramiseks klõpsake valikuid **Müügireskontro** \> **Seadistus** \> **Müügireskontro parameetrid** \> **Laohaldus** ja valige siis müügitellimuse täitmise poliitika.</span><span class="sxs-lookup"><span data-stu-id="28a4b-122">To set the fulfillment policies for sales orders, click **Accounts receivable** \> **Setup** \> **Accounts receivable parameters** \> **Warehouse management**, and then select a sales order fulfillment policy.</span></span>

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a><span data-ttu-id="28a4b-123">Lubage partiina väljastamine ja määrake kogus, mis tuleks partiina väljastada</span><span class="sxs-lookup"><span data-stu-id="28a4b-123">Allow release in a batch and specify the quantity that should be release in a batch</span></span>

<span data-ttu-id="28a4b-124">Laost tellimuste partiina väljastamiseks kasutatakse pakett-tööd.</span><span class="sxs-lookup"><span data-stu-id="28a4b-124">A batch job is used to release orders to a warehouse in a batch.</span></span> <span data-ttu-id="28a4b-125">Parameetrid, mis eristavad tellimusi, mis tuleks pakett-tööna käivitada, määratakse pakett-töös eneses.</span><span class="sxs-lookup"><span data-stu-id="28a4b-125">The parameters that distinguish the orders that should be run in a batch job are set on the batch job itself.</span></span>

<span data-ttu-id="28a4b-126">Parameeter **Kogus** määrab, kas partiina tuleks väljastada terve kogus või füüsiliselt reserveeritud kogus.</span><span class="sxs-lookup"><span data-stu-id="28a4b-126">The **Quantity** parameter specifies whether the whole quantity or the physically reserved quantity should be released in the batch.</span></span> <span data-ttu-id="28a4b-127">Parameeter **Luba osaliselt väljastatud tellimuste väljastamine** määrab, kas partii tellimused tuleks vastu võtta või tagasi lükata, kui nad varem osaliselt väljastati.</span><span class="sxs-lookup"><span data-stu-id="28a4b-127">The **Allow release of partially released orders** parameter determines whether orders in the batch should be accepted or rejected if they were partially released earlier.</span></span>

-   <span data-ttu-id="28a4b-128">Parameetrite **Kogus** ja **Luba osaliselt väljastatud tellimuste väljastamine** määramiseks üleviimistellimustele klõpsake valikuid **Laohaldus** \> **Lattu väljastamine** \> **Üleviimistellimuste automaatne väljastamine**.</span><span class="sxs-lookup"><span data-stu-id="28a4b-128">To set the **Quantity** and **Allow release of partially released orders** parameters for transfer orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of transfer orders**.</span></span>

-   <span data-ttu-id="28a4b-129">Parameetrite **Kogus** ja **Luba osaliselt väljastatud tellimuste väljastamine** määramiseks müügitellimustele klõpsake valikuid **Laohaldus** \> **Lattu väljastamine** \> **Müügitellimuste automaatne väljastamine**.</span><span class="sxs-lookup"><span data-stu-id="28a4b-129">To set the **Quantity** and **Allow release of partially released orders** parameters for sales orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of sales orders**.</span></span>

