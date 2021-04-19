---
title: Planeerimise optimeerimise tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada planeerimise optimeerimisega töötamisel tekkivaid probleeme.
author: ChristianRytt
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 2100235fadabe6af87849aab7d9ec55d85ea66fa
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812879"
---
# <a name="troubleshoot-planning-optimization"></a><span data-ttu-id="ae416-103">Planeerimise optimeerimise tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="ae416-103">Troubleshoot Planning Optimization</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ae416-104">Selles teemas kirjeldatakse, kuidas lahendada planeerimise optimeerimisega töötamisel tekkivaid levinumaid probleeme.</span><span class="sxs-lookup"><span data-stu-id="ae416-104">This topic describes how to fix common issues that you might encounter while working with Planning Optimization.</span></span>

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a><span data-ttu-id="ae416-105">Planeerimise optimeerimise lisandmooduli installimist ei saa lõpule viia</span><span class="sxs-lookup"><span data-stu-id="ae416-105">Installation of the Planning Optimization add-in doesn't complete</span></span>

<span data-ttu-id="ae416-106">Planeerimise optimeerimine nõuab Lifecycle Servicesi (LCS) loaga suure kättesaadavusega keskkonda, järk 2 või kõrgem, (mitte OneBoxi keskkond) koos Dynamics 365 Supply Chain Managementi versiooniga 10.0.7 või hilisem.</span><span class="sxs-lookup"><span data-stu-id="ae416-106">Planning Optimization requires a Lifecycle Services (LCS) enabled, high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="ae416-107">Kui proovite installida lisandmoodulit OneBoxi keskkonnas, ei viida installimist lõpule.</span><span class="sxs-lookup"><span data-stu-id="ae416-107">If you try to install the add-in on a OneBox environment, the installation won't complete.</span></span>

<span data-ttu-id="ae416-108">**Lahendus**: tühistage installimine ja kasutage suure kättesaadavusega keskkonda, järk 2 või kõrgem (mitte Oneboxi keskkond).</span><span class="sxs-lookup"><span data-stu-id="ae416-108">**Fix**: Cancel the installation and use a high-availability environment, tier 2 or higher (not a OneBox environment).</span></span>

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a><span data-ttu-id="ae416-109">Pakett-tööde planeerimine nurjub, kui planeerimise optimeerimine on lubatud</span><span class="sxs-lookup"><span data-stu-id="ae416-109">Planning of batch jobs fails when Planning Optimization is enabled</span></span>

<span data-ttu-id="ae416-110">Planeerimise optimeerimise lubamisel keelatakse automaatselt sisseehitatud koondplaneerimise mootor.</span><span class="sxs-lookup"><span data-stu-id="ae416-110">When you enable Planning Optimization, the built-in master planning engine is automatically disabled.</span></span> <span data-ttu-id="ae416-111">Koondplaneerimise pakett-tööd, mis loodi sisseehitatud Supply Chain Managementi planeerimismootori jaoks, nurjuvad käivitamisel, kui planeerimise optimeerimine on lubatud.</span><span class="sxs-lookup"><span data-stu-id="ae416-111">Master planning batch jobs that were created for the built-in Supply Chain Management planning engine will fail if they are triggered while Planning Optimization is enabled.</span></span> <span data-ttu-id="ae416-112">Teile võidakse kuvada tõrketeadet, nt *See toiming käivitas koondplaneerimise, mida ei toetata, kui planeerimise optimeerimine on lubatud*.</span><span class="sxs-lookup"><span data-stu-id="ae416-112">You may receive an error message such as *This operation triggered master planning that isn't supported when Planning Optimization is enabled*.</span></span>

<span data-ttu-id="ae416-113">**Lahendus**: tühistage kõik koondplaneerimise pakett-tööd, mis loodi sisseehitatud Supply Chain Managementi planeerimismootori jaoks.</span><span class="sxs-lookup"><span data-stu-id="ae416-113">**Fix**: Cancel all master planning batch jobs that were created for the built-in Supply Chain Management planning engine.</span></span>

## <a name="planning-optimization-results-are-different-from-earlier-results"></a><span data-ttu-id="ae416-114">Planeerimise optimeerimise tulemused erinevad varasematest</span><span class="sxs-lookup"><span data-stu-id="ae416-114">Planning Optimization results are different from earlier results</span></span>

<span data-ttu-id="ae416-115">Planeerimise optimeerimine erineb sisseehitatud koondplaneerimise kujundusest mõnel alal.</span><span class="sxs-lookup"><span data-stu-id="ae416-115">Planning Optimization differs from the built-in master planning design in some areas.</span></span> <span data-ttu-id="ae416-116">Seda võivad põhjustada ka ootel funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="ae416-116">This can also be caused by pending features.</span></span>

<span data-ttu-id="ae416-117">**Lahendus**: käivitage planeerimise optimeerimise sobivuse analüüs ja analüüsige selle mõju mõistmiseks tulemusi, viidates sellega seotud dokumentatsioonile.</span><span class="sxs-lookup"><span data-stu-id="ae416-117">**Fix**: Run Planning Optimization fit analysis and then analyze the results while referring to the related documentation to understand the impact.</span></span> <span data-ttu-id="ae416-118">Lisateavet vt [Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ae416-118">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="cant-enable-planning-optimization"></a><span data-ttu-id="ae416-119">Planeerimise optimeerimist ei saa lubada</span><span class="sxs-lookup"><span data-stu-id="ae416-119">Can't enable Planning Optimization</span></span>

<span data-ttu-id="ae416-120">Suvandi **Ühenduse olek** väärtuseks peab olema määratud **Ühendatud** enne, kui saate määrata suvandi **Plaanimise optimeerimise kasutamine** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="ae416-120">The **Connection status** must be **Connected** before you can set **Use Planning Optimization** to **Yes**.</span></span> <span data-ttu-id="ae416-121">Lisateavet vt [Planeerimise optimeerimise kasutamise alustamine](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="ae416-121">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="ae416-122">**Lahendus**: veenduge, et planeerimise optimeerimise lisandmoodul on edukalt installitud.</span><span class="sxs-lookup"><span data-stu-id="ae416-122">**Fix**: Make sure that the Planning Optimization add-in was installed successfully.</span></span>

## <a name="error-message-is-shown-during-ctp"></a><span data-ttu-id="ae416-123">CTP ajal kuvatakse tõrketeade</span><span class="sxs-lookup"><span data-stu-id="ae416-123">Error message is shown during CTP</span></span>

<span data-ttu-id="ae416-124">Kui proovite käivitada müügitellimusest funktsiooni võimeline lubama (CTP), kui planeerimise optimeerimine on lubatud, kuvatakse järgmine tõrketeade: *See toiming käivitas koondplaneerimise, mida ei toetata, kui planeerimise optimeerimine on lubatud*.</span><span class="sxs-lookup"><span data-stu-id="ae416-124">If you try to run capable to promise (CTP) from a sales order when Planning Optimization is enabled, you will receive the following error message: *This operation triggered master planning that isn't supported when the Planning Optimization is enabled*.</span></span>

<span data-ttu-id="ae416-125">See on seotud ootel oleva funktsiooniga, mis on planeeritud tootmistellimuste toe osana.</span><span class="sxs-lookup"><span data-stu-id="ae416-125">This is related to a pending feature that is planned as part of the support for production orders.</span></span>

<span data-ttu-id="ae416-126">**Lahendus:** vältige CTP arvutamisi, kui planeerimise optimeerimine on lubatud, kuni CTP tugi on saadaval.</span><span class="sxs-lookup"><span data-stu-id="ae416-126">**Fix:** Avoid CTP calculations when Planning Optimization is enabled until CTP support is available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ae416-127">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ae416-127">Additional resources</span></span>

[<span data-ttu-id="ae416-128">Planeerimise optimeerimisega alustamine</span><span class="sxs-lookup"><span data-stu-id="ae416-128">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="ae416-129">Planeerimise optimeerimise sobivuse analüüs</span><span class="sxs-lookup"><span data-stu-id="ae416-129">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]