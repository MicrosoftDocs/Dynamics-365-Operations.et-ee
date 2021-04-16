---
title: Kinnipeetav maks müügitehingutes
description: Selles teemas loetletakse valitud klientidele kinnipeetava maksu arvutamise vältimise etapid. Klientidele, kes määravad teile maksetes kinnipeetava maksu, saate määrata kinnipeetava maksu vaikegrupi.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 8e11ce10faa9b450b6f36a856b34b06b4ee1838d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842340"
---
# <a name="withholding-tax-in-sales-transactions"></a><span data-ttu-id="969cf-104">Kinnipeetav maks müügitehingutes</span><span class="sxs-lookup"><span data-stu-id="969cf-104">Withholding tax in sales transactions</span></span>

<span data-ttu-id="969cf-105">Selles teemas loetletakse valitud klientidele kinnipeetava maksu arvutamise vältimise etapid.</span><span class="sxs-lookup"><span data-stu-id="969cf-105">This topic lists the steps for avoiding the calculation of withholding tax for selected customers.</span></span> <span data-ttu-id="969cf-106">Klientidele, kes määravad teile maksetes kinnipeetava maksu, saate määrata vaikimisi **Kinnipeetava maksu grupi** lehel **Kliendid**.</span><span class="sxs-lookup"><span data-stu-id="969cf-106">For customers who specify withholding tax in their payments to you, you can assign the default **Withholding tax group** on the **Customers** page.</span></span> 

1. <span data-ttu-id="969cf-107">Avage **Navigeerimispaan > Moodulid > Müügireskontro > Kliendid > Kõik kliendid**.</span><span class="sxs-lookup"><span data-stu-id="969cf-107">Go to **Navigation pane > Modules > Accounts receivable > Customers > All customers**.</span></span>

2. <span data-ttu-id="969cf-108">Klõpsake vastavat kliendikontot ja seejärel käsku **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="969cf-108">Click the respective customer account, click **Edit**.</span></span>

3. <span data-ttu-id="969cf-109">Seadke vahekaardil **Arve ja tarne** väli **Kinnipeetava maksu arvutamine** väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="969cf-109">In the **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="969cf-110">Kinnipeetavat maksu ei arvutata, kui **Kinnipeetava maksu arvutamine** ei ole selle kliendi jaoks koondandmetes sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="969cf-110">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this customer in the master data.</span></span>

4. <span data-ttu-id="969cf-111">Valige kinnipeetava maksu grupp loendist **Kinnipeetava maksu grupp**.</span><span class="sxs-lookup"><span data-stu-id="969cf-111">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="969cf-112">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="969cf-112">Click **Save**.</span></span>

<span data-ttu-id="969cf-113">Kaupadele/teenustele, millelt kinnipeetav maks on kohustuslik, saate määrata vaikimisi **Kauba kinnipeetava maksu grupi** jaotises **Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="969cf-113">For items/services, which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="969cf-114">Avage **Navigeerimispaan > Moodulid > Tooteteabe haldus > Tooted > Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="969cf-114">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="969cf-115">Klõpsake vastavat üksuse numbrit ja seejärel käsku **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="969cf-115">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="969cf-116">Klõpsake vahekaardil **Müük** käsku **Arvuta kinnipeetav maks**.</span><span class="sxs-lookup"><span data-stu-id="969cf-116">In the **Sell** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="969cf-117">Kinnipeetavat maksu ei arvutata, kui suvand **Arvuta kinnipeetav maks** ei ole määratud selle kauba jaoks olekusse **Jah** vahekaardil **Müük**, mis asub lehel **Väljastatud toode**.</span><span class="sxs-lookup"><span data-stu-id="969cf-117">Withholding tax will not be calculated if **Calculate withholding tax** is not set to **Yes** for this Item in the **Sell** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="969cf-118">Valige kauba kinnipeetava maksu grupp loendist **Kauba kinnipeetava maksu grupp**.</span><span class="sxs-lookup"><span data-stu-id="969cf-118">Select an Item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="969cf-119">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="969cf-119">Click **Save**.</span></span>

<span data-ttu-id="969cf-120">Kinnipeetava maksu gruppe ja kauba kinnipeetava maksu gruppe saab määrata lehel **Müügitellimus**.</span><span class="sxs-lookup"><span data-stu-id="969cf-120">Withholding tax groups and Item withholding tax groups can be assigned using the **Sales order** page.</span></span> 

<span data-ttu-id="969cf-121">Vaikimisi kinnipeetava maksu gruppi ja kauba kinnipeetava maksu gruppi kasutatakse vaikekirjetena müügitellimuse ridadel uut müügitellimust luues.</span><span class="sxs-lookup"><span data-stu-id="969cf-121">The default Withholding tax group and Item withholding tax group will be used as default entries on sales order lines when you create a new sales order.</span></span>

<span data-ttu-id="969cf-122">Kinnipeetav maks arvutatakse ja sisestatakse koos **Kliendi makse töölehega**.</span><span class="sxs-lookup"><span data-stu-id="969cf-122">Withholding tax is calculated and posted with **Customer payment journal**.</span></span> <span data-ttu-id="969cf-123">Saate kohaldatavat kinnipeetava maksu koodi ja ka tegelikku kinnipeetava maksu summat käsitsi reguleerida vahekaardil **Kinnipeetav maks** lehel **Kannete tasakaalustamine**.</span><span class="sxs-lookup"><span data-stu-id="969cf-123">You can manually adjust the applicable withholding tax code, as well as the actual withholding tax amount in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

<span data-ttu-id="969cf-124">Arvutatud kinnipeetava maksu summa arvatakse kliendimaksest maha ja sisestatakse seotud kande **Kinnipeetava maksu** vastaskontole.</span><span class="sxs-lookup"><span data-stu-id="969cf-124">The calculated withholding tax amount will be deducted from the customer payment and posted to the **Withholding tax offset** account in a related voucher.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]