---
title: "Ametikoha eelarvestamise tõrkeotsing"
description: "Selles artiklis on vastused küsimustele, mis võivad teil ametikoha eelarvestuse konfigureerimisel tekkida. Käsitletud on korduma kippuvaid küsimusi selle kohta, kuidas luua eelarve kuluelemente, hüvitusgruppe ja hüvitusruudustikke."
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 77ee178ddc942a3ae4d5669e5efbf29337648df1
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="position-budgeting-troubleshooting"></a><span data-ttu-id="ce2e6-104">Ametikoha eelarvestamise tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="ce2e6-104">Position budgeting troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce2e6-105">Selles artiklis on vastused küsimustele, mis võivad teil ametikoha eelarvestuse konfigureerimisel tekkida.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-105">This article provides answers to questions that you might have when you configure position budgeting.</span></span> <span data-ttu-id="ce2e6-106">Käsitletud on korduma kippuvaid küsimusi selle kohta, kuidas luua eelarve kuluelemente, hüvitusgruppe ja hüvitusruudustikke.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-106">It addresses frequently asked questions about how to create budget cost elements, compensation groups, and compensation grids.</span></span> 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a><span data-ttu-id="ce2e6-107">Miks ma ei leia inimressursside moodulis prognoositavat ametikohta?</span><span class="sxs-lookup"><span data-stu-id="ce2e6-107">Why can’t I find the forecast position page in Human resources?</span></span>
---------------------------------------------------------------

<span data-ttu-id="ce2e6-108">Prognoositavad ametikohad on teisaldatud eelarvestamise moodulisse.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-108">Forecast positions have been moved to Budgeting.</span></span>

## <a name="why-cant-i-delete-a-budget-cost-element"></a><span data-ttu-id="ce2e6-109">Miks ma ei saa kustutada eelarve kuluelementi?</span><span class="sxs-lookup"><span data-stu-id="ce2e6-109">Why can’t I delete a budget cost element?</span></span>
<span data-ttu-id="ce2e6-110">Prognoositavale ametikohale määratud eelarve kuluelementi ei saa kustutada.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-110">You can’t delete a budget cost element that is assigned to a forecast position.</span></span> <span data-ttu-id="ce2e6-111">Enne eelarvekulu elemendi kustutamist tuleb see kõigist prognoositavatest ametikohtadest eemaldada.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-111">Before you can delete a budget cost element, you must remove it from all forecast positions.</span></span> <span data-ttu-id="ce2e6-112">**Näpunäide:** kõigi ametikohtade leidmiseks, millele eelarve kuluelement on määratud, valige kuluelement lehelt **Eelarve kuluelemendid** ja klõpsake siis käsku **Uuenda ametikohti**.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-112">**Tip:** To find all the positions that a budget cost element is assigned to, select the cost element on the **Budget cost elements** page, and then click **Update positions**.</span></span> <span data-ttu-id="ce2e6-113">Kuluelementi kasutavad ametikohad on loetletud ülemisel ruudustikul.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-113">The positions that use the cost element are listed in the upper grid.</span></span>

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a><span data-ttu-id="ce2e6-114">Kuidas saan eemaldada kuluelemendi mitmelt prognoositavalt ametikohalt, ilma et peaks neid kõiki avama?</span><span class="sxs-lookup"><span data-stu-id="ce2e6-114">How can I remove a cost element from multiple forecast positions without opening each one?</span></span>
<span data-ttu-id="ce2e6-115">Kuluelementi ei saa eemaldada.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-115">You can’t remove a cost element.</span></span> <span data-ttu-id="ce2e6-116">Kuid kui muudate algus- ja lõppkuupäeva nii, et need jäävad väljapoole eelarve planeerimise tsükli kuupäevi, siis ei määrata kuluelementi enam eelarve planeerimise tsüklis prognoositavatele ametikohtadele.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-116">However, if you change the start and end dates so that they are outside the budget planning cycle dates, the cost element will no longer be assigned to the forecast positions in that budget planning cycle.</span></span> <span data-ttu-id="ce2e6-117">Selle muudatuse tegemiseks avage eelarve kuluelement ja klõpsake siis kiirkaardil **Kuluarvestus** käsku **Muuda kuupäevi** ning muutke jõustumiskuupäeva või aegumiskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-117">To make this change, open the budget cost element, and then, on the **Cost calculation** FastTab, click **Change dates**, and change the effective date or expiration date.</span></span> <span data-ttu-id="ce2e6-118">Seejärel klõpsake nuppu **OK**, et muuta automaatselt kõiki prognoositavaid ametikohti, millele kuluelement on määratud.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-118">Then click **OK** to automatically update all forecast positions that the cost element is assigned to.</span></span> <span data-ttu-id="ce2e6-119">**Näpunäide:** selle meetodi kasutamisel arvestage, et see eemaldab eelarve kuluelemendi **kõigilt** prognoositavatelt ametikohtadelt, kui alguse ja lõpu kuupäevad ei ole enam sobivas vahemikus.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-119">**Tip:** If you use this method, be aware that it removes the budget cost element from **all** forecast positions where the start and end dates are no longer within the appropriate range.</span></span> <span data-ttu-id="ce2e6-120">Kui te seda ei soovi, peate avama iga prognoositava ametikoha, millelt soovite eelarve kuluelementi eemaldada, ja tegema muudatuse käsitsi.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-120">If this effect isn't what you intend, you must open each forecast position that you want to remove the budget cost element from and manually make the change.</span></span>

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a><span data-ttu-id="ce2e6-121">Miks ma ei saa sisestada aasta summat eelarve kuluelemendi kiirkaardile Kulu kalkulatsioon?</span><span class="sxs-lookup"><span data-stu-id="ce2e6-121">Why can’t I enter an annual amount on the Cost calculation FastTab for the budget cost element?</span></span>
<span data-ttu-id="ce2e6-122">Te ei saa sisestada aasta summat, kui kiirkaardil **Kalkulatsiooni alus** on eelarve kuluelemendid, sest süsteem nõuab väärtuse arvutamiseks protsenti.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-122">You can’t enter an annual amount if there are budget cost elements on the **Calculation basis** FastTab, because the system requires a percentage in order to calculate the value.</span></span> <span data-ttu-id="ce2e6-123">Väärtuse muutmiseks eemaldage kiirkaardilt **Kalkulatsiooni alus** kõik eelarve kuluelemendid.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-123">To change the value, remove all budget cost elements from the **Calculation basis** FastTab.</span></span>

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a><span data-ttu-id="ce2e6-124">Miks ma ei saa muuta eelarve kulu tüüpi „teenimine” muuks eelarve kulu tüübiks?</span><span class="sxs-lookup"><span data-stu-id="ce2e6-124">Why can’t I change the budget cost type from earning to another budget cost type?</span></span>
<span data-ttu-id="ce2e6-125">Mõned eelarve kuluelemendid kasutavad kuluelementi „teenimine” arvutuse alusena.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-125">Some budget cost elements use the earning cost element as a calculation basis.</span></span> <span data-ttu-id="ce2e6-126">Välja **Eelarve kulu tüüp** muutmiseks eemaldage tulu kuluelement kõigi eelarve kuluelementide kiirkaardilt **Kalkulatsiooni alus**.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-126">To change the **Budget cost type** field, remove the earning cost element from the **Calculation basis** FastTab of all budget cost elements.</span></span>

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a><span data-ttu-id="ce2e6-127">Miks ma ei saa muuta eelarve kuluelemendi ridadel eelarve kuluelemendi kuupäeva?</span><span class="sxs-lookup"><span data-stu-id="ce2e6-127">Why can’t I change the date on budget cost element lines for a budget cost element?</span></span>
<span data-ttu-id="ce2e6-128">Eelarve kuluelemendi rea kuupäeva ei saa muuta siis, kui prognoositav ametikoht kasutab eelarve kuluelementi.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-128">You can’t change the date on the budget cost element line when a budget cost element is used by a forecast position.</span></span> <span data-ttu-id="ce2e6-129">See piirang aitab tagada, et prognoositavad ametikohad on alati eelarve kuluelemendi piires.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-129">This limitation helps guarantee that the forecast positions are always within the guidelines of the budget cost element.</span></span> <span data-ttu-id="ce2e6-130">Kuupäeva muutmiseks klõpsake kiirkaardil **Kulu kalkulatsioon** valikut **Muuda kuupäevi** ja sisestage uued kuupäevad.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-130">To change the date, on the **Cost calculation** FastTab, click **Change dates**, and enter the new dates.</span></span> <span data-ttu-id="ce2e6-131">Seejärel klõpsake nuppu **OK**, et muuta prognoositavaid ametikohti, millele kuluelement on määratud.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-131">Then click **OK** to update the positions that the cost element is assigned to.</span></span>

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a><span data-ttu-id="ce2e6-132">Miks ma ei saa muuta eelarve kuluelemendi kulusid lehel Hüvitusgrupp?</span><span class="sxs-lookup"><span data-stu-id="ce2e6-132">Why can’t I change the costs for a budget cost element on the Compensation group page?</span></span>
<span data-ttu-id="ce2e6-133">Eelarve kuluelemente saab luua ja muuta ainult lehel **Eelarve kuluelemendid**.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-133">You can create and change budget cost elements only on the **Budget cost elements** page.</span></span>

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a><span data-ttu-id="ce2e6-134">Miks ma saan tõrketeate, kui muudan prognoositava ametikoha kuluelemendi kuupäevi?</span><span class="sxs-lookup"><span data-stu-id="ce2e6-134">Why do I receive an error message when I change the dates for a cost element on a forecast position?</span></span>
<span data-ttu-id="ce2e6-135">Prognoositava ametikoha kuluelemendi real olevad kuupäevad peavad jääma järgmistesse vahemikesse.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-135">The dates on the forecast position cost element line must be within the following ranges:</span></span>

-   <span data-ttu-id="ce2e6-136">Ametikoha aktiveerimis- ja kõrvaldamiskuupäevad.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-136">The activation and retirement dates of the position.</span></span>
-   <span data-ttu-id="ce2e6-137">Eelarve kuluelemendi aktiveerimis- ja aegumiskuupäevad.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-137">The activation and expiration dates of the budget cost element.</span></span>
-   <span data-ttu-id="ce2e6-138">Prognoositava ametikoha eelarve planeerimise protsessiga seostatud eelarvetsükli algus- ja lõppkuupäevad.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-138">The start and end dates of the budget cycle that is associated with the budget planning process of the forecast position.</span></span>





