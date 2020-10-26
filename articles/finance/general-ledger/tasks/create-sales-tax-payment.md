---
title: Käibemaksumakse loomine
description: Käibemaksu tasakaalustamise ja sisestamise töö tasakaalustab käibemaksukontode käibemaksu saldod ja tasakaalustab need käibemaksu tasakaalustuskontoga kindla perioodi jooksul.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e41217d26239cf704709d1d48666c382e1e2e824
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985704"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="90862-103">Käibemaksumakse loomine</span><span class="sxs-lookup"><span data-stu-id="90862-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="90862-104">Käibemaksu tasakaalustamise ja sisestamise töö tasakaalustab käibemaksukontode käibemaksu saldod ja tasakaalustab need käibemaksu tasakaalustuskontoga kindla perioodi jooksul.</span><span class="sxs-lookup"><span data-stu-id="90862-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="90862-105">Avage Maksud > Deklaratsioonid > Käibemaks > Käibemaksu tasakaalustamine ja sisestamine.</span><span class="sxs-lookup"><span data-stu-id="90862-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="90862-106">Klõpsake väljal Tasakaalustusperiood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="90862-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="90862-107">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="90862-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="90862-108">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="90862-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="90862-109">Kui suvand Kaasa parandused pole lehel Pearaamatu parameetrid valitud, saab tasakaalustuse eri versioone töödelda.</span><span class="sxs-lookup"><span data-stu-id="90862-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="90862-110">Originaal on perioodivahemiku esimene tasakaalustus ja seda saab töödelda perioodivahemiku kohta ainult üks kord.</span><span class="sxs-lookup"><span data-stu-id="90862-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="90862-111">Viimased parandused tasakaalustavad käibemaksukanded, mis on sisestatud pärast algversiooni loomist.</span><span class="sxs-lookup"><span data-stu-id="90862-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="90862-112">Sisestage kuupäev väljale Kande kuupäev.</span><span class="sxs-lookup"><span data-stu-id="90862-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="90862-113">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="90862-113">Click OK.</span></span>

