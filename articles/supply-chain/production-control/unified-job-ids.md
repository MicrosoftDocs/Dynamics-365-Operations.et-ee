---
title: Töö ID-de ühtsed numbrijärjestused
description: See funktsioon pakub ühte ühtset numbriseeriat, mis loob töö ID-d tootmisjuhtimise, tootmise käivitamise ja aja ja kohaloleku moodulite jaoks.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 00212803c46d898a39eafbc5c62016eb829535e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824937"
---
# <a name="unified-number-sequence-for-job-ids"></a><span data-ttu-id="984f1-103">Töö ID-de ühtsed numbrijärjestused</span><span class="sxs-lookup"><span data-stu-id="984f1-103">Unified number sequence for job IDs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="984f1-104">See funktsioon pakub ühte ühtset numbriseeriat, mis loob töö ID-d tootmisjuhtimise, tootmise käivitamise ja aja ja kohaloleku moodulite jaoks.</span><span class="sxs-lookup"><span data-stu-id="984f1-104">This feature provides a single, unified number sequence that generates job IDs for the Production control, Manufacturing execution, and Time and attendance modules.</span></span> <span data-ttu-id="984f1-105">Varem oli teil võimalik valida iga mooduli jaoks erinev numbriseeria, mis võib põhjustada vastuolulisi töö ID-sid, kui vähemalt kaks nendest seeriatest kasutab identset vormingut.</span><span class="sxs-lookup"><span data-stu-id="984f1-105">Previously, you were able to choose a different number sequence for each of these modules, which could result in conflicting job IDs if two or more of these sequences used an identical format.</span></span> <span data-ttu-id="984f1-106">Selline konflikt võib põhjustada andmete rikkumist.</span><span class="sxs-lookup"><span data-stu-id="984f1-106">Such a conflict can cause data corruption.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="984f1-107">Selle funktsiooni sisselülitamine teie süsteemi jaoks</span><span class="sxs-lookup"><span data-stu-id="984f1-107">Turn on this feature for your system</span></span>

<span data-ttu-id="984f1-108">Kui teie süsteemis ei ole veel selles teemas kirjeldatud funktsiooni, avage [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja lülitage funktsioon *Töö ID-de ühtne numbrijärjestus* sisse.</span><span class="sxs-lookup"><span data-stu-id="984f1-108">If your system doesn't already include the feature described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Unified number sequence for job IDs* feature.</span></span>

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a><span data-ttu-id="984f1-109">Töö ID-de jaoks seadistage ühtne numbrijada</span><span class="sxs-lookup"><span data-stu-id="984f1-109">Set up the unified number sequence for job IDs</span></span>

<span data-ttu-id="984f1-110">Pärast selle funktsiooni lubamist tühistatakse tootmise juhtimise, tootmise teostamise ning aja ja kohaloleku moodulite parameetrite lehtedel olevad **Töö identifitseerimine** numbrijada sätted ja uus **Ühtne töö ID** väli lisatakse.</span><span class="sxs-lookup"><span data-stu-id="984f1-110">After enabling this feature, the existing **Job identification** number-sequence settings located on the parameters pages for the Production control, Manufacturing execution, and Time and attendance modules will be deprecated and a new **Unified job ID** field will be added.</span></span> <span data-ttu-id="984f1-111">**Ühtne töö ID** väärtus jagatakse kõigi kolme mooduliga, mis tagab, et kõik moodulid viitavad samale numbriseeriale.</span><span class="sxs-lookup"><span data-stu-id="984f1-111">The **Unified job ID** value is shared by all three modules, thus ensuring that all modules reference the same number sequence.</span></span> <span data-ttu-id="984f1-112">Töö ID-d on seetõttu kõigi kolme mooduli osas unikaalsed ja konflikti ei teki kunagi.</span><span class="sxs-lookup"><span data-stu-id="984f1-112">Job IDs will therefore be unique across all three modules and a conflict will never occur.</span></span>

<span data-ttu-id="984f1-113">Töö ID-de jaoks ühtse numbrijada seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="984f1-113">To set up the unified number sequence for job IDs:</span></span>

1. <span data-ttu-id="984f1-114">Lülitage funktsioon sisse, nagu kirjeldatud eelmises jaotises.</span><span class="sxs-lookup"><span data-stu-id="984f1-114">Turn on the feature as described in the previous section.</span></span>
1. <span data-ttu-id="984f1-115">Määrake numbriseeria, mida soovite kasutada oma ühtsete töö ID-de jaoks, või looge uus.</span><span class="sxs-lookup"><span data-stu-id="984f1-115">Either identify the number sequence you want to use for your unified job IDs, or create a new one.</span></span> <span data-ttu-id="984f1-116">Lisateabe saamiseks vt teemat [Numbriseeriate ülevaade](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="984f1-116">For more information, see [Number sequences overview](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span></span>
1. <span data-ttu-id="984f1-117">Minge **Tootmise juhtimise parameetrid**, **Tootmise käivitamise parameetrid** või **Kellaaja ja kohalviibimise parameetrid** lehele.</span><span class="sxs-lookup"><span data-stu-id="984f1-117">Go to the **Production control parameters**, **Manufacturing execution parameters**, or **Time and attendance parameters** page.</span></span> <span data-ttu-id="984f1-118">Pole tähtis, kumba valite, sest kui teete selle sätte mõnel neist lehtedest, värskendatakse kõiki teisi lehti automaatselt.</span><span class="sxs-lookup"><span data-stu-id="984f1-118">It doesn't matter which one you choose because when you make this setting on any of those pages, all of the other pages will update automatically.</span></span>
1. <span data-ttu-id="984f1-119">Avage valitud parameetrite lehel vahekaart **Numbriseeriad**.</span><span class="sxs-lookup"><span data-stu-id="984f1-119">Open the **Number sequences** tab on your selected parameters page.</span></span>
1. <span data-ttu-id="984f1-120">Määrake **numbriseeria kood**, mille määratlesite eelnevalt ruudustiku reale **Ühtne töö ID**.</span><span class="sxs-lookup"><span data-stu-id="984f1-120">Assign the **Number sequence code** that you identified previously to the **Unified job IDs** row of the grid.</span></span>
