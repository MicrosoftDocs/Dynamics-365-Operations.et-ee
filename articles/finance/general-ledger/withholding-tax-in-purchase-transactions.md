---
title: Kinnipeetav maks ostutehingutes
description: Hankijatele, kellele on kohustuslik kinnipeetav maks, saab määrata vaikimisi **Kinnipeetava maksu grupi** lehel **Kõik hankijad**.
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
ms.openlocfilehash: faeaf0746532875d3517a208c9c338c112bf2c77
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816879"
---
# <a name="withholding-tax-in-purchase-transactions"></a><span data-ttu-id="43244-103">Kinnipeetav maks ostutehingutes</span><span class="sxs-lookup"><span data-stu-id="43244-103">Withholding tax in purchase transactions</span></span>

<span data-ttu-id="43244-104">Hankijatele, kellele on kohustuslik kinnipeetav maks, saab määrata vaikimisi **Kinnipeetava maksu grupi** lehel **Kõik hankijad**.</span><span class="sxs-lookup"><span data-stu-id="43244-104">For vendors who are liable to withholding tax, you can assign the default **Withholding tax group** on the **All vendors** page.</span></span>

1. <span data-ttu-id="43244-105">Avage **Navigeerimispaan > Moodulid > Ostureskontro > Hankijad > Kõik hankijad**.</span><span class="sxs-lookup"><span data-stu-id="43244-105">Go to **Navigation pane > Modules > Accounts payable > Vendors > All vendors**.</span></span>

2. <span data-ttu-id="43244-106">Klõpsake vastavat hankija kontot ja seejärel käsku **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="43244-106">Click the respective Vendor account, click **Edit**.</span></span>

3. <span data-ttu-id="43244-107">Seadke vahekaardil **Arve ja tarne** väli **Kinnipeetava maksu arvutamine** väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="43244-107">In **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="43244-108">Kinnipeetavat maksu ei arvutata, kui **Kinnipeetava maksu arvutamine** ei ole selle hankija jaoks sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="43244-108">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this vendor in the data.</span></span>

4. <span data-ttu-id="43244-109">Valige kinnipeetava maksu grupp loendist **Kinnipeetava maksu grupp**.</span><span class="sxs-lookup"><span data-stu-id="43244-109">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="43244-110">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="43244-110">Click **Save**.</span></span>

<span data-ttu-id="43244-111">Kaupadele/teenustele, millelt kinnipeetav maks on kohustuslik, saate määrata vaikimisi **Kauba kinnipeetava maksu grupi** jaotises **Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="43244-111">For items/services which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="43244-112">Avage **Navigeerimispaan > Moodulid > Tooteteabe haldus > Tooted > Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="43244-112">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="43244-113">Klõpsake vastavat üksuse numbrit ja seejärel käsku **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="43244-113">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="43244-114">Klõpsake vahekaardil **Ost** käsku **Arvuta kinnipeetav maks**.</span><span class="sxs-lookup"><span data-stu-id="43244-114">In **Purchase** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="43244-115">Kinnipeetavat maksu ei arvutata, kui suvand **Arvuta kinnipeetav maks** ei ole määratud selle kauba jaoks olekusse **Jah** vahekaardil **Ost**, mis asub lehel **Väljastatud toode**.</span><span class="sxs-lookup"><span data-stu-id="43244-115">Withholding tax will not be calculated if **Calculate withholding tax** isn't set to **Yes** for this Item in the **Purchase** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="43244-116">Valige kauba kinnipeetava maksu grupp loendist **Kauba kinnipeetava maksu grupp**.</span><span class="sxs-lookup"><span data-stu-id="43244-116">Select an item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="43244-117">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="43244-117">Click **Save**.</span></span>

<span data-ttu-id="43244-118">Kinnipeetava maksu gruppe ja kauba kinnipeetava maksu gruppe saab määrata järgmistel lehtedel.</span><span class="sxs-lookup"><span data-stu-id="43244-118">Withholding tax groups and Item withholding tax groups can be assigned in pages:</span></span> 

- <span data-ttu-id="43244-119">**Ostutellimus**</span><span class="sxs-lookup"><span data-stu-id="43244-119">**Purchase order**</span></span>
- <span data-ttu-id="43244-120">**Hankija arve**</span><span class="sxs-lookup"><span data-stu-id="43244-120">**Vendor invoice**</span></span>
- <span data-ttu-id="43244-121">**Arve tööleht**</span><span class="sxs-lookup"><span data-stu-id="43244-121">**Invoice journal**</span></span>

<span data-ttu-id="43244-122">Kinnipeetava maksu grupi ja kauba kinnipeetava maksu grupi vaikeväärtused viiakse **Ostutellimuste** ja/või **Ootel hankija arvete** loomisel ridadele.</span><span class="sxs-lookup"><span data-stu-id="43244-122">The default Withholding tax group and Item withholding tax group will be carried into the lines when creating **Purchase orders** and/or **Pending Vendor invoices**.</span></span> <span data-ttu-id="43244-123">**Hankija arve töölehe** korral võite lülitada suvandi **Kinnipeetava maksu arvutamine** sisse ja seejärel valida **Kauba kinnipeetava maksu grupi** töölehe vahekaardil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="43244-123">For **Vendor invoice journal**, you can switch on **Calculate withholding tax** and select **Item withholding tax group** in the **General** tab in the journal.</span></span>

<span data-ttu-id="43244-124">Kinnipeetava maksu ajutine summa on saadaval lehe **Ostutellimus** vahekaardi **Kogusummad** väljal **Korrigeeritud kinnipeetav maks**.</span><span class="sxs-lookup"><span data-stu-id="43244-124">The temporary amount of withholding tax is available in the field **Adjusted withholding tax** of the **Totals** tab on the **Purchase order** page.</span></span>

![Kinnipeetav maks sisaldub ostutellimuses](media/withholding-tax-adjusted.png)

<span data-ttu-id="43244-126">Kinnipeetav maks arvutatakse **Hankija makse töölehel**.</span><span class="sxs-lookup"><span data-stu-id="43244-126">Withholding tax is calculated on **Vendor payment journal**.</span></span> <span data-ttu-id="43244-127">Saate kohaldatavat kinnipeetava maksu koode ja ka tegelikku kinnipeetava maksu summasid käsitsi reguleerida vahekaardil **Kinnipeetav maks** lehel **Kannete tasakaalustamine**.</span><span class="sxs-lookup"><span data-stu-id="43244-127">You can manually adjust the applicable withholding tax codes as well as the actual withholding tax amounts in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

![Kinnipeetavat maksu saab käsitsi korrigeerida lehel Kannete tasakaalustamine](media/withholding-tax-vendor-payment-tab.png)

<span data-ttu-id="43244-129">Saadud kinnipeetava maksu summa arvatakse hankija maksest maha ja sisestatakse seotud kande **Kinnipeetava maksu kontole**.</span><span class="sxs-lookup"><span data-stu-id="43244-129">The derived withholding tax amount will be deducted from the vendor payment and posted to the **Withholding tax account** in a related voucher.</span></span>

![Kinnipeetava maksu konto, kus kuvatakse seostuv kanne](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]