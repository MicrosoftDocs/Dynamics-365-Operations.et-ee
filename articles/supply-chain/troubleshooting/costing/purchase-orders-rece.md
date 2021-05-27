---
title: Füüsiliselt sissetulnud ostutellimusi ei kuvata lao sulgemise aruandes
description: Füüsiliselt sissetulnud ostutellimusi ei kuvata Check open quantities lao sulgemise aruandes.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventOpenQtyCritical
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9508d6d75d8ebee7ca10140ed4c4215d7ad1dda7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026439"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a><span data-ttu-id="92002-103">Füüsiliselt sissetulnud ostutellimusi ei kuvata lao sulgemise aruandes</span><span class="sxs-lookup"><span data-stu-id="92002-103">Physically received purchase orders don't appear on the inventory closing report</span></span>

<span data-ttu-id="92002-104">KB number: 4612595</span><span class="sxs-lookup"><span data-stu-id="92002-104">KB number: 4612595</span></span>

## <a name="symptoms"></a><span data-ttu-id="92002-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="92002-105">Symptoms</span></span>

<span data-ttu-id="92002-106">Füüsiliselt sissetulnud ostutellimusi ei kuvata **Kontrolli avatud koguseid** lao sulgemise aruandes.</span><span class="sxs-lookup"><span data-stu-id="92002-106">Physically received purchase orders don't appear on the **Check open quantities** inventory closing report.</span></span>

## <a name="resolution"></a><span data-ttu-id="92002-107">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="92002-107">Resolution</span></span>

<span data-ttu-id="92002-108">Aruanne **Kontrolli avatud koguseid** näitab väljastamiskandeid, mida ei saa tasakaalustada finantsiliselt värskendatud lao sissetulekutega alates valitud sulgemiskuupäevast.</span><span class="sxs-lookup"><span data-stu-id="92002-108">The **Check open quantities** report shows issue transactions that can't be settled against financially updated inventory receipts as of the selected closing date.</span></span> <span data-ttu-id="92002-109">Võite füüsilised sissetulekud aruandesse kaasata.</span><span class="sxs-lookup"><span data-stu-id="92002-109">You can choose to include physical receipts on the report.</span></span> <span data-ttu-id="92002-110">Sel juhul näidatakse füüsilisi sissetulekuid, kui nad saavad katta väljamineku kandeid, mida ei saa tasakaalustada.</span><span class="sxs-lookup"><span data-stu-id="92002-110">In that case, physical receipts will be shown if they can cover the issue transactions that can't be settled.</span></span> <span data-ttu-id="92002-111">Lisateavet vt teemast [Ettevalmistamine varude sulgemise käivitamiseks](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).</span><span class="sxs-lookup"><span data-stu-id="92002-111">For more information, see [Preparing to run inventory close](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).</span></span>
