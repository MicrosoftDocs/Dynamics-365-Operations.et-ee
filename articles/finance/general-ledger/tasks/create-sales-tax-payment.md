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
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee69cfee672be1571fd5cc630e33601bb5a48eac
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186160"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="361b0-103">Käibemaksumakse loomine</span><span class="sxs-lookup"><span data-stu-id="361b0-103">Create a sales tax payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="361b0-104">Käibemaksu tasakaalustamise ja sisestamise töö tasakaalustab käibemaksukontode käibemaksu saldod ja tasakaalustab need käibemaksu tasakaalustuskontoga kindla perioodi jooksul.</span><span class="sxs-lookup"><span data-stu-id="361b0-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="361b0-105">Avage Maksud > Deklaratsioonid > Käibemaks > Käibemaksu tasakaalustamine ja sisestamine.</span><span class="sxs-lookup"><span data-stu-id="361b0-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="361b0-106">Klõpsake väljal Tasakaalustusperiood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="361b0-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="361b0-107">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="361b0-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="361b0-108">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="361b0-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="361b0-109">Kui suvand Kaasa parandused pole lehel Pearaamatu parameetrid valitud, saab tasakaalustuse eri versioone töödelda.</span><span class="sxs-lookup"><span data-stu-id="361b0-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="361b0-110">Originaal on perioodivahemiku esimene tasakaalustus ja seda saab töödelda perioodivahemiku kohta ainult üks kord.</span><span class="sxs-lookup"><span data-stu-id="361b0-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="361b0-111">Viimased parandused tasakaalustavad käibemaksukanded, mis on sisestatud pärast algversiooni loomist.</span><span class="sxs-lookup"><span data-stu-id="361b0-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="361b0-112">Sisestage kuupäev väljale Kande kuupäev.</span><span class="sxs-lookup"><span data-stu-id="361b0-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="361b0-113">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="361b0-113">Click OK.</span></span>
