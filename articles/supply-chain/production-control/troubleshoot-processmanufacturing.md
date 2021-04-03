---
title: Protsesstootmise tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada protsesstootmisega töötamisel tekkivaid probleeme.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 71ff5eeb2065a67281393777937d50237ab78d5e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259718"
---
# <a name="troubleshoot-process-manufacturing"></a><span data-ttu-id="d647a-103">Protsesstootmise tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="d647a-103">Troubleshoot process manufacturing</span></span>

<span data-ttu-id="d647a-104">Selles teemas kirjeldatakse, kuidas lahendada protsesstootmisega töötamisel tekkivaid probleeme.</span><span class="sxs-lookup"><span data-stu-id="d647a-104">This topic describes how to fix issues that you might encounter while you work with process manufacturing.</span></span>

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a><span data-ttu-id="d647a-105">Kui ma kasutan töökaardi seadet, et teatada osalisest kogusest tootmistellimuse viimasel tööl, lõpetatakse automaatselt kõik selle tellimuse varasemad tööd, mille olekuks on seatud pooleli.</span><span class="sxs-lookup"><span data-stu-id="d647a-105">When I use the job card device to report a partial quantity on the last job in a production order, all the previous jobs on that order that have a status of In progress are automatically ended.</span></span>

<span data-ttu-id="d647a-106">Selline käitumine on nii kavandatud.</span><span class="sxs-lookup"><span data-stu-id="d647a-106">This behavior is by design.</span></span> <span data-ttu-id="d647a-107">**Tootmistellimuse vaikesätted** lehel **Kinnita lõpetatuks** vahekaardil on suvand nimega **Lõpp-märgistuse protsess**.</span><span class="sxs-lookup"><span data-stu-id="d647a-107">On the **Production order defaults** page, on the **Report as finished** tab, there is an option that is named **End-mark route**.</span></span> <span data-ttu-id="d647a-108">Kui see teema on seatud väärtusele *Jah*, sisestatakse protsessikaardi tööleht, kui töötaja kasutab viimase operatsiooni kohta töökaardi seadet või töökaardi terminali.</span><span class="sxs-lookup"><span data-stu-id="d647a-108">If this topic is set to *Yes*, a route card journal is posted when a worker uses the job card device or job card terminal to report the last operation.</span></span> <span data-ttu-id="d647a-109">See tööleht märgib kõik operatsioonid lõpetatuks ja lõpetab kõik tootmistööd.</span><span class="sxs-lookup"><span data-stu-id="d647a-109">This journal marks all the operations as completed and ends all the production jobs.</span></span> <span data-ttu-id="d647a-110">Kui **Lõpp-märgistamise protsessi** suvandi väärtuseks on seatud *Jah*, ei arvesta süsteem töö olekut, mille töötaja valis viimase operatsiooni käigus.</span><span class="sxs-lookup"><span data-stu-id="d647a-110">When the **End-mark route** option is set to *Yes*, the system doesn't consider the job status that the worker selected when they reported the last operation.</span></span> <span data-ttu-id="d647a-111">Süsteem ei võta arvesse ka seda, kas töötaja teatab täielikust või osalisest kogusest.</span><span class="sxs-lookup"><span data-stu-id="d647a-111">The system also doesn't consider whether the worker is reporting a full or partial quantity.</span></span>

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a><span data-ttu-id="d647a-112">Kui ma proovin ladu sulgeda, kuvatakse järgmine hoiatusteade: "Omahinna tagasiarvestuse arvutuse teostamist %1 kuupäevaga ühtiva perioodi lõpuga ei ole registreeritud."</span><span class="sxs-lookup"><span data-stu-id="d647a-112">When I attempt a stock closing, I receive the following warning message: "No execution of Backflush costing calculation with a date %1 matching period end has been registered."</span></span>

<span data-ttu-id="d647a-113">Kui kasutate varasemat versiooni kui 10.0.13, siis kui te ei kasuta minimaalsete tootmiskulude voogu, kuvatakse lao sulgemisel järgmine ekslik hoiatusteade.</span><span class="sxs-lookup"><span data-stu-id="d647a-113">In releases before release 10.0.13, if you aren't using the lean production costing flow, you receive the following erroneous warning message during inventory closing:</span></span>

> <span data-ttu-id="d647a-114">Olete käivitamas lao sulgemist kuupäevaga %1.</span><span class="sxs-lookup"><span data-stu-id="d647a-114">You are about to execute an Inventory close with a date %1.</span></span> <span data-ttu-id="d647a-115">Perioodi lõpukuupäevaga %1 sobivat omahinna tagasiarvestust ei ole registreeritud.</span><span class="sxs-lookup"><span data-stu-id="d647a-115">No execution of Backflush costing calculation with a date %1 matching period end has been registered.</span></span> <span data-ttu-id="d647a-116">Palun teostage perioodi lõpukuupäevaga %1 sobiv omahinna tagasiarvestus.</span><span class="sxs-lookup"><span data-stu-id="d647a-116">Please remember to execute a Backflush costing calculation with a date of %1 matching period end.</span></span> <span data-ttu-id="d647a-117">Varude hindamine, müüdud kaupade kulu ja erinevused ei pruugi olla abiraamatu või pearaamatu puhul õiged, kuni see on teostatud.</span><span class="sxs-lookup"><span data-stu-id="d647a-117">The valuation of inventories, cost of goods sold and variances might not be correct in Subledger or General ledger until this has been executed.</span></span>

<span data-ttu-id="d647a-118">See probleem on parandatud versioonis 10.0.13 ja hilisemates versioonides.</span><span class="sxs-lookup"><span data-stu-id="d647a-118">This issue has been fixed in release 10.0.13 and later.</span></span> <span data-ttu-id="d647a-119">Lisateavet leiad teemast [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span><span class="sxs-lookup"><span data-stu-id="d647a-119">For more information, see [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]