---
title: Lehe Kauba hind vahekaardil Aktiivsed hinnad ei ole alguskuupäeva
description: Lehe Kauba hind vahekaardil Aktiivsed hinnad ei ole alguskuupäeva.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026454"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a><span data-ttu-id="95775-103">Lehe Kauba hind vahekaardil Aktiivsed hinnad ei ole alguskuupäeva</span><span class="sxs-lookup"><span data-stu-id="95775-103">There is no From date value on the Active prices tab of the Item price page</span></span>

<span data-ttu-id="95775-104">KB number: 4613548</span><span class="sxs-lookup"><span data-stu-id="95775-104">KB number: 4613548</span></span>

## <a name="symptoms"></a><span data-ttu-id="95775-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="95775-105">Symptoms</span></span>

<span data-ttu-id="95775-106">Ei ole **Alguskuupäev** väärtust **Kauba hind** vahekaardil **Ühiku hind** lehel.</span><span class="sxs-lookup"><span data-stu-id="95775-106">There is no **From date** value on the **Active prices** tab of the **Item price** page.</span></span>

## <a name="resolution"></a><span data-ttu-id="95775-107">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="95775-107">Resolution</span></span>

<span data-ttu-id="95775-108">Ootele määratud hinna **alguskuupäeva** väärtust (kehtiv kuupäev) ei kanta üle aktiivsesse hinda.</span><span class="sxs-lookup"><span data-stu-id="95775-108">The **From date** value (effective date) that is set on the pending price isn't transferred to the active price.</span></span>

<span data-ttu-id="95775-109">Kauba kulukirje esmakordsel sisestamisel on sellel olek *Ootel* ja plaanitav jõustumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="95775-109">When an item cost record is first entered, it has a status of *Pending* and an intended effective date.</span></span> <span data-ttu-id="95775-110">Kauba kulukirje aktiveerimisel määratakse olekuks *Aktiivne* ja jõustumiskuupäevaks määratakse aktiveerimiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="95775-110">When you activate the item cost record, the status is updated to *Active*, and the effective date is updated to the activation date.</span></span> <span data-ttu-id="95775-111">Seetõttu on aktiivse hinna aktiveerimiskuupäev alati tegelik aktiveerimise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="95775-111">Therefore, the active price's activation date is always the actual date of the activation.</span></span>

<span data-ttu-id="95775-112">Lisateavet leiate teemast [Kulude versioonide ülevaade](../../cost-management/costing-versions.md).</span><span class="sxs-lookup"><span data-stu-id="95775-112">For more information, see [Costing versions overview](../../cost-management/costing-versions.md).</span></span>
