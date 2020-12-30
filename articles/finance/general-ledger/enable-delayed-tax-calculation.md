---
title: Luba töölehtedel viivitusega maksuarvutus
description: See teema selgitab, kuidas lülitada sisse funktsioon Hilinenud maksu arvutamine, et parandada maksuarvutuste jõudlust, kui töölehe ridade arv on väga suur.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: d4ce0343ac766b30d532be0866a381dc520fd462
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442468"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a><span data-ttu-id="95f0d-103">Luba töölehtedel viivitusega maksuarvutus</span><span class="sxs-lookup"><span data-stu-id="95f0d-103">Enable delayed tax calculation on journals</span></span>
[!include [banner](../includes/banner.md)]


<span data-ttu-id="95f0d-104">Selles teemas selgitatakse, kuidas viivitada käibemaksu arvutamist töölehtedel.</span><span class="sxs-lookup"><span data-stu-id="95f0d-104">This topic explains how you can delay sales tax calculation on journals.</span></span> <span data-ttu-id="95f0d-105">See võimalus aitab parandada maksuarvutuste jõudlust, kui töölehe ridu on palju.</span><span class="sxs-lookup"><span data-stu-id="95f0d-105">This capability helps improve the performance of tax calculations when there are many journal lines.</span></span>

<span data-ttu-id="95f0d-106">Vaikimisi arvutatakse töölehe ridadel käibemaksu summad iga kord, kui maksudega seotud välju uuendatakse.</span><span class="sxs-lookup"><span data-stu-id="95f0d-106">By default, sales tax amounts on journal lines are calculated whenever tax-related fields are updated.</span></span> <span data-ttu-id="95f0d-107">Need väljad hõlmavad käibemaksugruppide ja kauba käibemaksugruppide välju.</span><span class="sxs-lookup"><span data-stu-id="95f0d-107">These fields include the fields for sales tax groups and item sales tax groups.</span></span> <span data-ttu-id="95f0d-108">Iga tööleherea uuendamine põhjustab maksusummade ümberarvutamist kõigi tööleheridade puhul.</span><span class="sxs-lookup"><span data-stu-id="95f0d-108">Any update to a journal line causes tax amounts to be recalculated for all journal lines.</span></span> <span data-ttu-id="95f0d-109">Kuigi selline käitumine aitab kasutajal näha reaalajas arvutatud maksusummasid, võib see mõjutada ka jõudlust, kui tööleheridade arv on väga suur.</span><span class="sxs-lookup"><span data-stu-id="95f0d-109">Although this behavior helps user see tax amounts calculated in real time, it can also affect performance if the number of journal lines is very large.</span></span>

<span data-ttu-id="95f0d-110">Viivitusega maksuarvutuse funktsioon võimaldab teil viivitada maksude arvutamisega töölehtedel ja aitab seega parandada jõudlusprobleeme.</span><span class="sxs-lookup"><span data-stu-id="95f0d-110">The Delayed tax calculation feature lets you delay tax calculation on journals and therefore helps fix performance issues.</span></span> <span data-ttu-id="95f0d-111">Kui see funktsioon on sisse lülitatud, arvutatakse maksusummad ainult siis, kui kasutaja valib käsu **Käibemaks** või sisestab töölehe.</span><span class="sxs-lookup"><span data-stu-id="95f0d-111">When this feature is turned on, tax amounts are calculated only when a user selects **Sales Tax** or posts the journal.</span></span>

<span data-ttu-id="95f0d-112">Käibemaksu arvutamisega saate viivitada kolmel tasandil:</span><span class="sxs-lookup"><span data-stu-id="95f0d-112">You can delay the calculation of sales taxes at three levels:</span></span>

- <span data-ttu-id="95f0d-113">Juriidiline isik</span><span class="sxs-lookup"><span data-stu-id="95f0d-113">Legal entity</span></span>
- <span data-ttu-id="95f0d-114">Töölehe nimi</span><span class="sxs-lookup"><span data-stu-id="95f0d-114">Journal name</span></span>
- <span data-ttu-id="95f0d-115">Töölehe päis</span><span class="sxs-lookup"><span data-stu-id="95f0d-115">Journal header</span></span>

<span data-ttu-id="95f0d-116">Süsteem annab prioriteedi töölehe päise sättele.</span><span class="sxs-lookup"><span data-stu-id="95f0d-116">The system gives priority to the setting for the journal header.</span></span> <span data-ttu-id="95f0d-117">Vaikimisi võetakse see säte töölehe nimest.</span><span class="sxs-lookup"><span data-stu-id="95f0d-117">By default, this setting is taken from the journal name.</span></span> <span data-ttu-id="95f0d-118">Töölehe nime säte võetakse vaikimisi töölehe nime loomisel lehe **Pearaamatu parameetrid** sättest.</span><span class="sxs-lookup"><span data-stu-id="95f0d-118">By default, the setting for the journal name is taken from the setting on the **General ledger parameters** page when the journal name is created.</span></span> <span data-ttu-id="95f0d-119">Järgmistes jaotistes selgitatakse, kuidas lülitada sisse viivitusega maksuarvutust juriidiliste isikute, töölehe nimede ja töölehe päiste jaoks.</span><span class="sxs-lookup"><span data-stu-id="95f0d-119">The following sections explain how to turn on delayed tax calculation for legal entities, journal names, and journal headers.</span></span>

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a><span data-ttu-id="95f0d-120">Viivitusega maksuarvutuse sisselülitamine juriidilise isiku tasandil</span><span class="sxs-lookup"><span data-stu-id="95f0d-120">Turn on delayed tax calculation at the legal entity level</span></span>

1. <span data-ttu-id="95f0d-121">Avage **Pearaamat \> Pearaamatu seadistamine \> Pearaamatu parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="95f0d-121">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="95f0d-122">Määrake vahekaardi **Käibemaks** kiirkaardi **Üldine** valiku **Viivitusega maksuarvutus** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="95f0d-122">On the **Sales tax** tab, on the **General** FastTab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Pearaamatu parameetrite kujutis](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a><span data-ttu-id="95f0d-124">Viivitusega maksuarvutuse sisselülitamine töölehe nime tasandil</span><span class="sxs-lookup"><span data-stu-id="95f0d-124">Turn on delayed tax calculation at the journal name level</span></span>

1. <span data-ttu-id="95f0d-125">Avage **Pearaamat \> Töölehe seadistamine \> Töölehtede nimed**.</span><span class="sxs-lookup"><span data-stu-id="95f0d-125">Go to **General ledger \> Journal setup \> Journal names**.</span></span>
2. <span data-ttu-id="95f0d-126">Määrake kiirkaardi **Üldine** jaotises **Käibemaks** valiku **Viivitusega maksuarvutus** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="95f0d-126">On the **General** FastTab, in the **Sales tax** section, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Töölehe nimede kujutis](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a><span data-ttu-id="95f0d-128">Viivitusega maksuarvutuse sisselülitamine töölehe päise tasandil</span><span class="sxs-lookup"><span data-stu-id="95f0d-128">Turn on delayed tax calculation at the journal header level</span></span>

1. <span data-ttu-id="95f0d-129">Avage **Pearaamat \> Töölehekirjed \> Päevaraamatud**.</span><span class="sxs-lookup"><span data-stu-id="95f0d-129">Go to **General ledger \> Journal entries \> General journals**.</span></span>
2. <span data-ttu-id="95f0d-130">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="95f0d-130">Select **New**.</span></span>
3. <span data-ttu-id="95f0d-131">Valige töölehe nimi.</span><span class="sxs-lookup"><span data-stu-id="95f0d-131">Select a journal name.</span></span>
4. <span data-ttu-id="95f0d-132">Seadke vahekaardil **Seadistus** valiku **Viivitusega maksuarvutus** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="95f0d-132">On the **Setup** tab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Päevaraamatu lehe kujutis](media/delayed-tax-calculation-journal-header.png)
