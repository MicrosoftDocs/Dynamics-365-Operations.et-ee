---
title: Pakett-töödes väljaminevate saadetiste kinnitamine
description: Selles teemas kirjeldatakse, kuidas seadistada pakett-tööd, mis kinnitab automaatselt väljaminevad üleviimistellimuse saadetised saatmisvalmis koorma jaoks.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 41dbfb90b7b19c964e725ee0a4c769402414fb17
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426023"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a><span data-ttu-id="ed633-103">Pakett-töödes väljaminevate saadetiste kinnitamine</span><span class="sxs-lookup"><span data-stu-id="ed633-103">Confirm outbound shipments from batch jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed633-104">Selles teemas kirjeldatakse, kuidas seadistada pakett-tööd, mis kinnitab automaatselt väljaminevad üleviimistellimuse saadetised saatmisvalmis koorma jaoks.</span><span class="sxs-lookup"><span data-stu-id="ed633-104">This topic describes how to set up a batch job that automatically confirms outbound transfer-order shipments for ready-to-ship loads.</span></span> <span data-ttu-id="ed633-105">Siin kirjeldatud pakett-tööd rakendatakse ainult üleviimistellimuste saadetiste, mitte müügitellimuste puhul.</span><span class="sxs-lookup"><span data-stu-id="ed633-105">The batch job described here only applies to transfer order shipments, not to sales orders.</span></span>

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a><span data-ttu-id="ed633-106">Funktsiooni „Pakett-töödes väljaminevate saadetiste kinnitamine” lubamine</span><span class="sxs-lookup"><span data-stu-id="ed633-106">Enable the Confirm outbound shipments from batch jobs feature</span></span>

<span data-ttu-id="ed633-107">Enne selle funktsiooni kasutamist tuleb see teie süsteemis lubada.</span><span class="sxs-lookup"><span data-stu-id="ed633-107">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="ed633-108">Administraatorid saavad kasutada [funktsioonide halduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lehte, et kontrollida funktsiooni olekut ja vajaduse korral see lubada.</span><span class="sxs-lookup"><span data-stu-id="ed633-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="ed633-109">Funktsioon on loetletud järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ed633-109">The feature is listed as:</span></span>

- <span data-ttu-id="ed633-110">**Moodul** - *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="ed633-110">**Module** - *Warehouse management*</span></span>
- <span data-ttu-id="ed633-111">**Funktsiooni nimi** - *Pakett-töödes väljaminevate saadetiste kinnitamine*</span><span class="sxs-lookup"><span data-stu-id="ed633-111">**Feature name** - *Confirm outbound shipments from batch jobs*</span></span>

## <a name="process-outbound-shipments"></a><span data-ttu-id="ed633-112">Väljaminevate saadetiste töötlemine</span><span class="sxs-lookup"><span data-stu-id="ed633-112">Process outbound shipments</span></span>

<span data-ttu-id="ed633-113">Selleks, et seadistada planeeritud pakett-töö kinnitama väljaminevaid saadetisi koormate jaoks, mis on saatmiseks valmis, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="ed633-113">To set up a scheduled batch job to run the outbound shipment confirmation for loads that are ready to ship:</span></span>

1. <span data-ttu-id="ed633-114">Avage **Laohaldus \> Perioodilised ülesanded \> Väljaminevate saadetiste töötlemine**.</span><span class="sxs-lookup"><span data-stu-id="ed633-114">Go to **Warehouse management \> Periodic tasks \> Process outbound shipments**.</span></span>
1. <span data-ttu-id="ed633-115">Avaneb dialoogiboks **Saadetise kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="ed633-115">The **Confirm shipment** dialog box opens.</span></span> <span data-ttu-id="ed633-116">Valige kiirkaardil **Kaasatavad kirjed** suvand **Filter**.</span><span class="sxs-lookup"><span data-stu-id="ed633-116">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="ed633-117">Avaneb päringuredaktori dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="ed633-117">The query editor dialog box opens.</span></span> <span data-ttu-id="ed633-118">Lisage vahekaardil **Vahemik** järgmiste väärtustega uus rida.</span><span class="sxs-lookup"><span data-stu-id="ed633-118">On the **Range** tab, add a row with the following values:</span></span>
    - <span data-ttu-id="ed633-119">**Tabel** - *Koormad*</span><span class="sxs-lookup"><span data-stu-id="ed633-119">**Table** - *Loads*</span></span>
    - <span data-ttu-id="ed633-120">**Tuletatud tabel** - *Koormad*</span><span class="sxs-lookup"><span data-stu-id="ed633-120">**Derived table** - *Loads*</span></span>
    - <span data-ttu-id="ed633-121">**Väli** - *Koorma olek*</span><span class="sxs-lookup"><span data-stu-id="ed633-121">**Field** - *Load status*</span></span>
    - <span data-ttu-id="ed633-122">**Kriteerium** - *Laaditud*</span><span class="sxs-lookup"><span data-stu-id="ed633-122">**Criteria** - *Loaded*</span></span>
1. <span data-ttu-id="ed633-123">Valige **OK**, et naasta dialoogiboksi **Saadetise kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="ed633-123">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="ed633-124">Seadke kiirkaardil **Käivita taustal** suvandi **Pakktöötlus** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="ed633-124">On the **Run in the background** FastTab, set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="ed633-125">Valige kiirkaardil **Käivita taustal** suvand **Kordumine**.</span><span class="sxs-lookup"><span data-stu-id="ed633-125">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="ed633-126">Avaneb dialoogiboks **Kordumise määratlemine**.</span><span class="sxs-lookup"><span data-stu-id="ed633-126">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="ed633-127">Seadistage käivitusgraafik oma ettevõtte vajaduste järgi.</span><span class="sxs-lookup"><span data-stu-id="ed633-127">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="ed633-128">Valige **OK**, et naasta dialoogiboksi **Saadetise kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="ed633-128">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="ed633-129">Valige **OK** dialoogiboksis **Saadetise kinnitamine**, et lisada pakett-töö pakktöötluse järjekorda.</span><span class="sxs-lookup"><span data-stu-id="ed633-129">Select **OK** on the **Confirm shipment** dialog box to add the batch job to the batch queue.</span></span>

<span data-ttu-id="ed633-130">Lisateavet leiate teemast [Pakktöötluse ülevaade](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ed633-130">For more information, see [Batch processing overview](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span></span>
