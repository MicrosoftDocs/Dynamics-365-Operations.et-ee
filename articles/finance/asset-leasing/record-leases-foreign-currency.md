---
title: Rendi kirjendamine välisvaluutas
description: Selles teemas selgitatakse, kuidas kirjendada rendilepinguid muudes valuutades peale arvestusvaluuta või aruandlusvaluuta.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7f70442450cc1c814ae23e41a1feb3a63f2aade8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992885"
---
# <a name="record-leases-in-foreign-currencies"></a><span data-ttu-id="17f7a-103">Rendi kirjendamine välisvaluutas</span><span class="sxs-lookup"><span data-stu-id="17f7a-103">Record leases in foreign currencies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17f7a-104">Vara rentimise kontod rentidele, mis on muud valuutas kui arvestusvaluuta või aruandevaluuta luuakse lehel **Pearaamatu seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="17f7a-104">Asset leasing accounts for leases that are in currencies other than the accounting currency or the reporting currency are established on the **Ledger setup** page.</span></span> <span data-ttu-id="17f7a-105">Kõik rendid tuleb sisestada nende tehingu valuutas.</span><span class="sxs-lookup"><span data-stu-id="17f7a-105">All leases should be entered in their transaction currency.</span></span> <span data-ttu-id="17f7a-106">Teisisõnu tuleb need sisestada rendilepingus määratud valuutas.</span><span class="sxs-lookup"><span data-stu-id="17f7a-106">In other words, they should be entered in the currency that is specified in the lease contract.</span></span> <span data-ttu-id="17f7a-107">Selles teemas selgitatakse, kuidas kirjendada rendilepinguid muudes valuutades peale arvestusvaluuta või aruandlusvaluuta.</span><span class="sxs-lookup"><span data-stu-id="17f7a-107">This topic explains how to record leases in currencies other than the accounting or reporting currency.</span></span>

<span data-ttu-id="17f7a-108">Kui sisestate rendilepingu välisvaluutas, amortiseeritakse kasutamisõiguse esemeks olev vara nii arvestusvaluutas kui ka aruandevaluutas.</span><span class="sxs-lookup"><span data-stu-id="17f7a-108">If you enter a lease in a foreign currency, the right-of-use (ROU) asset is depreciated in both the accounting currency and the reporting currency.</span></span> <span data-ttu-id="17f7a-109">Need valuutad konfigureeritakse lehel **Pearaamatu seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="17f7a-109">These currencies are configured on the **Ledger setup** page.</span></span> <span data-ttu-id="17f7a-110">Seda käitumist kasutatakse ka põhivarades.</span><span class="sxs-lookup"><span data-stu-id="17f7a-110">This behavior is also used in Fixed assets.</span></span> <span data-ttu-id="17f7a-111">Kui loote rendilepingu välisvaluutas, valige tehingu valuuta väljal **Valuuta**.</span><span class="sxs-lookup"><span data-stu-id="17f7a-111">When you create a lease in a foreign currency, select the transaction currency in the **Currency** field.</span></span>

<span data-ttu-id="17f7a-112">Arvestusvaluuta vahetuskurss on vaikimisi välja **Arvestusvaluuta vahetuskurss** väärtus.</span><span class="sxs-lookup"><span data-stu-id="17f7a-112">The exchange rate of the accounting currency is the default value in **Accounting currency exchange rate** field.</span></span> <span data-ttu-id="17f7a-113">Aruandlusvaluuta vahetuskurss on vaikimisi välja **Aruandlusvaluuta vahetuskurss** väärtus.</span><span class="sxs-lookup"><span data-stu-id="17f7a-113">The exchange rate of the reporting currency is the default value in the **Reporting currency exchange rate** field.</span></span> <span data-ttu-id="17f7a-114">Need vahetuskursid kehtisid rendilepingu alguskuupäeval.</span><span class="sxs-lookup"><span data-stu-id="17f7a-114">These exchange rates were effective on the commencement date of the lease.</span></span> <span data-ttu-id="17f7a-115">Väljad **Arvestusvaluuta vahetuskurss** ja **Aruandlusvaluuta vahetuskurss** asuvad kiirkaadil **Arvestus- ja aruandlusvaluuta vahetuskursi teave**, mis asub lehel **Rendi üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="17f7a-115">The **Accounting currency exchange rate** and **Reporting currency exchange rate** fields, are in the **Financial and reporting exchange information** FastTab, on the **Lease details** page.</span></span>

1. <span data-ttu-id="17f7a-116">Märkige märkeruut **Fikseeritud kurss**, et alistada automaatselt sisestatud vahetuskurss ja seejärel sisestage uus kurss.</span><span class="sxs-lookup"><span data-stu-id="17f7a-116">Select the **Fixed rate** check box to override the exchange rate that was automatically entered, and then enter the new rate.</span></span>
2. <span data-ttu-id="17f7a-117">Teistes väljades sisestage rendi jaoks nõutav teave ja seejärel valige **Loo graafikud**.</span><span class="sxs-lookup"><span data-stu-id="17f7a-117">In the other fields, enter the information that is required for the lease, and then select **Create schedules**.</span></span>
3. <span data-ttu-id="17f7a-118">Valige uuel lehel **Rendi üksikasjad** suvand **Raamatud**.</span><span class="sxs-lookup"><span data-stu-id="17f7a-118">On the new **Lease details** page, select **Books**.</span></span>
4. <span data-ttu-id="17f7a-119">Kinnitage lehel **Rendiraamat**, mis asub vahekaardil **Arvestus- ja aruandlusvaluuta vahetuskursi teave** väljade **Arvestusvaluuta algne kasutamisõiguse esemeks olev vara** ja **Aruandlusvaluuta algne kasutamisõiguse esemeks olev vara** väärtused.</span><span class="sxs-lookup"><span data-stu-id="17f7a-119">On the **Lease book** page, on the **Financial and reporting exchange information** tab, verify the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span> <span data-ttu-id="17f7a-120">Kõik need väljad näitavad tõlgitud kasutamisõiguse esemeks oleva vara saldot vastavas valuutas.</span><span class="sxs-lookup"><span data-stu-id="17f7a-120">Each of these fields shows the translated ROU asset balance in the corresponding currency.</span></span> <span data-ttu-id="17f7a-121">Neid välju uuendatakse iga kord, kui muudate finantsteavet.</span><span class="sxs-lookup"><span data-stu-id="17f7a-121">These fields are updated whenever you change any financial information.</span></span> <span data-ttu-id="17f7a-122">Enne maksegraafiku kinnitamist valige **Loo graafikud**.</span><span class="sxs-lookup"><span data-stu-id="17f7a-122">Select **Create schedules** before you confirm the payment schedule.</span></span>

    <span data-ttu-id="17f7a-123">Algne tunnustamise töölehe kirje kirjendab kasutamisõiguse esemeks olevat vara, mis kasutab rendilepingus loetletud valuutakursse.</span><span class="sxs-lookup"><span data-stu-id="17f7a-123">The initial recognition journal entry records the ROU asset that uses the currency exchange rates that are listed on the lease.</span></span> <span data-ttu-id="17f7a-124">Töölehe kirje hõlmab ka väljade **Arvestusvaluuta algne kasutamisõiguse esemeks olev vara** ja **Aruandlusvaluuta algne kasutamisõiguse esemeks olev vara** väärtusi.</span><span class="sxs-lookup"><span data-stu-id="17f7a-124">The journal entry also includes the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span>

## <a name="subsequent-measurement-for-foreign-currency-leases"></a><span data-ttu-id="17f7a-125">Välisvaluutas rentide järgnev mõõtmine</span><span class="sxs-lookup"><span data-stu-id="17f7a-125">Subsequent measurement for foreign currency leases</span></span>

<span data-ttu-id="17f7a-126">Kulumi graafik näitab eeldatavat kulumi kulu summasid aruandevaluutas, arvestusvaluutas ja tehingu valuutas.</span><span class="sxs-lookup"><span data-stu-id="17f7a-126">The depreciation schedule shows the expected depreciation expense amounts in the reporting currency, the accounting currency, and the transaction currency.</span></span>

<span data-ttu-id="17f7a-127">Kasutamisõiguse esemeks oleva vara saldode ja kulumi summade vaatamiseks kas aruandevaluutas või arvestusvaluutas avage leht **Vara kulumi graafik** ja valige märkeruut **Kuva arvestusvaluuta summad** või **Kuva aruandevaluuta summad**.</span><span class="sxs-lookup"><span data-stu-id="17f7a-127">To view the ROU asset balances and depreciation amounts in either the reporting currency or the accounting currency, open the **Asset depreciation schedule** page, and select the **Show accounting currency amounts** or **Show reporting currency amounts** check box.</span></span>

<span data-ttu-id="17f7a-128">Kui loote kulumiarvestuse kulu töölehe kanded välisvaluutas nomineeritud rendilepingule, kasutab kanne rendilepingus loetletud valuutakursse.</span><span class="sxs-lookup"><span data-stu-id="17f7a-128">When you create the depreciation expense journal entries against a lease that is denominated in a foreign currency, the entry uses the exchange rates that are listed on the lease.</span></span> <span data-ttu-id="17f7a-129">See kasutab ka väljade **Arvestusvaluuta algne kasutamisõiguse esemeks olev vara** ja **Aruandlusvaluuta algne kasutamisõiguse esemeks olev vara** väärtusi.</span><span class="sxs-lookup"><span data-stu-id="17f7a-129">It also uses the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span>

<span data-ttu-id="17f7a-130">Lõpliku kulumi summa saab arvutada veidi erineva vahetuskursi abil, nii et kasutamisõiguse esemeks olev vara amortiseeritakse täielikult nii arvestusvaluuta kui ka aruandevaluuta puhul.</span><span class="sxs-lookup"><span data-stu-id="17f7a-130">The final depreciation expense amount can be calculated by using a slightly different exchange rate, so that the ROU asset is fully depreciated in both the accounting currency and the reporting currency.</span></span>

<span data-ttu-id="17f7a-131">Kui rendileping on ümberklassifitseeritud kui **Edasilükatud rent**, tühjendab süsteem automaatselt arvestus- ja aruandlusvaluutad, kui need on juba määratletud.</span><span class="sxs-lookup"><span data-stu-id="17f7a-131">If the lease has been reclassified as **Deferred rent**, the system automatically clears the exchange rates of the accounting and reporting currencies, if they have already been defined.</span></span>
