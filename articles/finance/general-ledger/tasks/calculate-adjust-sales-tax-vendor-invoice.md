---
title: Käibemaksu arvutamine ja korrigeerimine hankija arvel
description: Selles teemas selgitatakse, kuidas kohandada müügimaksu tarnija arvel rakenduses Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a68e0df78516875168d977f78adf023887b2362d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186275"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="d7482-103">Käibemaksu arvutamine ja korrigeerimine hankija arvel</span><span class="sxs-lookup"><span data-stu-id="d7482-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d7482-104">Selles teemas selgitatakse, kuidas kohandada müügimaksu tarnija arvel.</span><span class="sxs-lookup"><span data-stu-id="d7482-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="d7482-105">Kui algne lähtedokument kuvab erinevad arvutatud maksusummade, saate neid summasid enne sisestamist korrigeerida.</span><span class="sxs-lookup"><span data-stu-id="d7482-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="d7482-106">See ülesanne kasutab demoettevõtte DEMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="d7482-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="d7482-107">Avage navigeerimispaanil **Moodulid > Ostureskontro > Arved > Arve tööleht**.</span><span class="sxs-lookup"><span data-stu-id="d7482-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="d7482-108">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d7482-108">Select **New**.</span></span>
3. <span data-ttu-id="d7482-109">Uue veeru väljal **Nimi** valige ripploendist suvand.</span><span class="sxs-lookup"><span data-stu-id="d7482-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="d7482-110">Toimingupaanil valige nupp **Alused**.</span><span class="sxs-lookup"><span data-stu-id="d7482-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="d7482-111">Täpsustage soovitud väärtusi väljal **Konto**.</span><span class="sxs-lookup"><span data-stu-id="d7482-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="d7482-112">Sisestage väärtus väljale **Arve**.</span><span class="sxs-lookup"><span data-stu-id="d7482-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="d7482-113">Sisestage number väljale **Kreedit**.</span><span class="sxs-lookup"><span data-stu-id="d7482-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="d7482-114">Määratlega väljal **Vastaskonto** soovitud väärtused.</span><span class="sxs-lookup"><span data-stu-id="d7482-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="d7482-115">Valige **Käibemaks**.</span><span class="sxs-lookup"><span data-stu-id="d7482-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="d7482-116">Sisestage number väljale **Tegeliku käibemaksu kogusumma**.</span><span class="sxs-lookup"><span data-stu-id="d7482-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="d7482-117">Vahekaardil **Korrigeerimine** saab korrigeerida käibemaksusummat käibemaksukoodi kohta.</span><span class="sxs-lookup"><span data-stu-id="d7482-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="d7482-118">Valige **Tegeliku väärtuse lähtestamine arvutatud summadest**.</span><span class="sxs-lookup"><span data-stu-id="d7482-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="d7482-119">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="d7482-119">Select **OK**.</span></span>
14. <span data-ttu-id="d7482-120">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d7482-120">Select **Save**.</span></span>

