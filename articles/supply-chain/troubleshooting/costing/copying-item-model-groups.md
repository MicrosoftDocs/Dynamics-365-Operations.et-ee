---
title: Puuduvad väljaseaded kauba mudeligruppide kopeerimisel teise juriidilisse isikusse
description: Väljaseaded puuduvad kauba mudeligruppide kopeerimisel teise juriidilisse isikusse.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f6fdfef0bc377418ed8a9c8830e74526a0b95eb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026434"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a><span data-ttu-id="80381-103">Puuduvad väljaseaded kauba mudeligruppide kopeerimisel teise juriidilisse isikusse</span><span class="sxs-lookup"><span data-stu-id="80381-103">Missing field settings when item model groups are copied to another legal entity</span></span>

<span data-ttu-id="80381-104">KB number: 4612800</span><span class="sxs-lookup"><span data-stu-id="80381-104">KB number: 4612800</span></span>

## <a name="symptoms"></a><span data-ttu-id="80381-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="80381-105">Symptoms</span></span>

<span data-ttu-id="80381-106">Kui kopeerite kauba mudeligrupid teisele juriidilisele isikule (ettevõttele), kasutades *kauba mudeligrupi laopoliitika üksust*, puuduvad sihtjuriidilise isiku uues mudeligrupis mõned väljasätted (nt laomudel ja kirjeldus).</span><span class="sxs-lookup"><span data-stu-id="80381-106">When you copy item model groups to another legal entity (company) by using the *Item model group inventory policies* entity, some field settings (for example, the inventory model and description) are missing in the new model group in the destination legal entity.</span></span>

## <a name="resolution"></a><span data-ttu-id="80381-107">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="80381-107">Resolution</span></span>

<span data-ttu-id="80381-108">Kauba mudeligrupi täieliku koopia loomiseks teisele juriidilisele isikule peate valima ka nii kauba mudeligrupi laopoliitikad (`InventInventoryPolicyEntity`) kui ka kauba mudeligrupiga seotud kuluvoo eelduste (`InventCostFlowAssumptionPolicyEntity`) poliitikad, mis on seotud kauba mudeligrupiga.</span><span class="sxs-lookup"><span data-stu-id="80381-108">To create a complete copy of an item model group to another legal entity, you must also select both the item model group inventory policies (`InventInventoryPolicyEntity`) and the cost flow assumption policies (`InventCostFlowAssumptionPolicyEntity`) that are associated with the item model group.</span></span>
