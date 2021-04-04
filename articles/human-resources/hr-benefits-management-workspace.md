---
title: Soodustuse halduse tööruum
description: Selles teemas kirjeldatakse soodustuste halduse tööruumi rakenduses Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8f17685dab8159522ec88af0fa6ca9c99c346b7b
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5488193"
---
# <a name="benefits-management-workspace"></a><span data-ttu-id="686bd-103">Soodustuse halduse tööruum</span><span class="sxs-lookup"><span data-stu-id="686bd-103">Benefits management workspace</span></span>

[!include [applies to](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

<span data-ttu-id="686bd-104">Selles teemas kirjeldatakse **soodustuste halduse** tööruumi rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="686bd-104">This topic describes the **Benefits management** workspace in Dynamics 365 Human Resources.</span></span>

> [!NOTE]
> <span data-ttu-id="686bd-105">**Soodustuste halduse** tööruumi vaatamiseks peate esmalt funktsioonihalduse kaudu lubama funktsiooni **(Eelversioon) Soodustuste halduse tööruum**.</span><span class="sxs-lookup"><span data-stu-id="686bd-105">To view the **Benefits management** workspace, you must first enable the **(Preview) Benefits management workspace** feature in Feature management.</span></span> <span data-ttu-id="686bd-106">Lisateavet funktsioonide eelversioonide lubamise kohta vt [Funktsioonide haldamine](../hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="686bd-106">For more information about enabling preview features, see [Manage features](../hr-admin-manage-features.md).</span></span><br><br><span data-ttu-id="686bd-107">![Soodustuste halduse tööruumi lubamine](./media/hr-benefits-management-workspace-enable.png)</span><span class="sxs-lookup"><span data-stu-id="686bd-107">![Enable Benefits management workspace](./media/hr-benefits-management-workspace-enable.png)</span></span>

<span data-ttu-id="686bd-108">**Soodustuste halduse** tööruum annab teile kiiresti ülevaate soodustustest, mis nõuavad teie tähelepanu.</span><span class="sxs-lookup"><span data-stu-id="686bd-108">The **Benefits management** workspace gives you a quick view of benefits items that require your attention.</span></span> <span data-ttu-id="686bd-109">Sellel lehel näete järgmist teavet:</span><span class="sxs-lookup"><span data-stu-id="686bd-109">On this page, you can see:</span></span>

- <span data-ttu-id="686bd-110">sekkumist ootavate üksuste kogusummad</span><span class="sxs-lookup"><span data-stu-id="686bd-110">Totals for items awaiting action</span></span>
- <span data-ttu-id="686bd-111">kinnitamata valikutega töötajad</span><span class="sxs-lookup"><span data-stu-id="686bd-111">Workers with unconfirmed selections</span></span>
- <span data-ttu-id="686bd-112">hiljuti soodustuste saamiseks registreerunud töötajad</span><span class="sxs-lookup"><span data-stu-id="686bd-112">Workers who recently enrolled in benefits</span></span>
- <span data-ttu-id="686bd-113">ees ootavate elusündmustega töötajad</span><span class="sxs-lookup"><span data-stu-id="686bd-113">Workers with future life events</span></span>
- <span data-ttu-id="686bd-114">uued töötajad, kes pole registreeritud</span><span class="sxs-lookup"><span data-stu-id="686bd-114">New hires who aren't enrolled</span></span>
- <span data-ttu-id="686bd-115">aktiivsete elusündmustega töötajad</span><span class="sxs-lookup"><span data-stu-id="686bd-115">Workers with active life events</span></span>
- <span data-ttu-id="686bd-116">avatud registreerimistega töötajad, kes pole ühtegi lepingut valinud</span><span class="sxs-lookup"><span data-stu-id="686bd-116">Workers with open enrollments who haven't opted for any plans</span></span>

![Soodustuse halduse tööruum](./media/hr-benefits-management-workspace.png)

## <a name="view-action-items"></a><span data-ttu-id="686bd-118">Tegevusüksuste kuvamine</span><span class="sxs-lookup"><span data-stu-id="686bd-118">View action items</span></span>

<span data-ttu-id="686bd-119">Tegevusüksuste kuvamiseks võite valida paani või vahekaardi. Vahekaardi valimise korral saate töötajaid vaadata ja valida otse tööruumi lehel.</span><span class="sxs-lookup"><span data-stu-id="686bd-119">You can view your action items by either selecting a tile or a tab. If you select a tab, you can view and select workers right on the workspace page.</span></span>

![Tegevusüksused](./media/hr-benefits-management-workspace-action-items.png)

<span data-ttu-id="686bd-121">Kui valite paani, viiakse teid vastava ala lehele.</span><span class="sxs-lookup"><span data-stu-id="686bd-121">If you select a tile, you go to the page for that area.</span></span> <span data-ttu-id="686bd-122">Kui näiteks valite ühe neist paanidest, kuvatakse leht **Töötaja soodustuste plaanid**, kus on filtri abil esile tõstetud töötajad, kellega peate midagi tegema.</span><span class="sxs-lookup"><span data-stu-id="686bd-122">For example, selecting any of these tiles displays the **Worker benefits plans** page, filtered for employees you need to take action on:</span></span>

- <span data-ttu-id="686bd-123">**Kinnitamata valikud**</span><span class="sxs-lookup"><span data-stu-id="686bd-123">**Unconfirmed selections**</span></span>
- <span data-ttu-id="686bd-124">**Ava välja registreeritud plaanideta registreerimised**</span><span class="sxs-lookup"><span data-stu-id="686bd-124">**Open enrollments with no checked out plans**</span></span>
- <span data-ttu-id="686bd-125">**Soodustused registreeritud**</span><span class="sxs-lookup"><span data-stu-id="686bd-125">**Enrolled in benefits**</span></span>
- <span data-ttu-id="686bd-126">**Uus töötaja pole registreeritud**</span><span class="sxs-lookup"><span data-stu-id="686bd-126">**New hire not enrolled**</span></span>

![Töötaja soodustusplaanid](./media/hr-benefits-management-workspace-plans.png)

<span data-ttu-id="686bd-128">Kui valite paani **Aktiivsed elusündmused** või **Tulevased elusündmused**, viiakse teid aktiivsete või tulevaste elusündmuste loendisse.</span><span class="sxs-lookup"><span data-stu-id="686bd-128">Selecting the **Active life events** or **Future life events** tiles takes you to a list of active or future life events.</span></span>

![Elusündmused](./media/hr-benefits-management-workspace-life-events.png)

## <a name="processing"></a><span data-ttu-id="686bd-130">Töötlemisel</span><span class="sxs-lookup"><span data-stu-id="686bd-130">Processing</span></span>

<span data-ttu-id="686bd-131">Registreerimiseks sobivuse, elusündmuste või tariifimuutuste uuenduste töötlemiseks valige navigeerimisribal asjakohane üksus.</span><span class="sxs-lookup"><span data-stu-id="686bd-131">To process enrollment eligibility, life events, or rate change updates, select the appropriate item on the navigation bar.</span></span>

![Töötlemisel](./media/hr-benefits-management-workspace-processing.png)

<span data-ttu-id="686bd-133">Töötlemistulemuste kuvamiseks valige lehel **Protsessi tulemused**.</span><span class="sxs-lookup"><span data-stu-id="686bd-133">To view process results, select **Process results** on the page.</span></span>

![Protsessi tulemused](./media/hr-benefits-management-workspace-process-results.png)

<span data-ttu-id="686bd-135">Lisateavet soodustuste töötlemise kohta leiate siit:</span><span class="sxs-lookup"><span data-stu-id="686bd-135">For more information about benefits processing, see:</span></span>

- [<span data-ttu-id="686bd-136">Registreerimise sobivuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="686bd-136">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="686bd-137">Elusündmuste muudatuste töötlemine</span><span class="sxs-lookup"><span data-stu-id="686bd-137">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="686bd-138">Elusündmuste sobivuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="686bd-138">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="686bd-139">Elusündmuste töötlemine</span><span class="sxs-lookup"><span data-stu-id="686bd-139">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="686bd-140">Määra muudatuste töötlemine</span><span class="sxs-lookup"><span data-stu-id="686bd-140">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)

## <a name="change-period"></a><span data-ttu-id="686bd-141">Vaheta perioodi</span><span class="sxs-lookup"><span data-stu-id="686bd-141">Change period</span></span>

<span data-ttu-id="686bd-142">Muu soodustuste perioodi vaatamiseks valige see ripploendist **Periood**.</span><span class="sxs-lookup"><span data-stu-id="686bd-142">To view a different benefits period, select it from the **Period** dropdown.</span></span>

![Vaheta perioodi](./media/hr-benefits-management-workspace-period.png)

## <a name="view-more-options"></a><span data-ttu-id="686bd-144">Kuva rohkem variante</span><span class="sxs-lookup"><span data-stu-id="686bd-144">View more options</span></span>

<span data-ttu-id="686bd-145">Lisateabe ja muude võimalike toimingute vaatamiseks valige **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="686bd-145">To view more information and actions you can take, select **Links**.</span></span>

![Lingid](./media/hr-benefits-management-workspace-links.png)

## <a name="see-also"></a><span data-ttu-id="686bd-147">Vt ka</span><span class="sxs-lookup"><span data-stu-id="686bd-147">See also</span></span>

[<span data-ttu-id="686bd-148">Soodustuste halduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="686bd-148">Benefits management overview</span></span>](hr-benefits-management-overview.md)