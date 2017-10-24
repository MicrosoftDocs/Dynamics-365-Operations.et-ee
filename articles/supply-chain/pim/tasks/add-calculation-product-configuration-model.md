--- 
title: Arvutuse lisamine toote konfiguratsioonimudelile
description: "See protseduur näitab, kuidas lisada toote konfiguratsioonimudelile uut arvutust."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2db8fb922b085a7f118822ef4fd974ac338f4d99
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="1e37c-103">Arvutuse lisamine toote konfiguratsioonimudelile</span><span class="sxs-lookup"><span data-stu-id="1e37c-103">Add a calculation to a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1e37c-104">See protseduur näitab, kuidas lisada toote konfiguratsioonimudelile uut arvutust.</span><span class="sxs-lookup"><span data-stu-id="1e37c-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="1e37c-105">See näitab, kuidas saate koostada loogikaavaldise, määrates tehtemärgiga „If” kõlari kõrguseks 10 valgete kõlarite ja 15 kõigi muude korpuse viimistluste puhul.</span><span class="sxs-lookup"><span data-stu-id="1e37c-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="1e37c-106">See protseduur kasutab komponenti Tipptasemel kõlar demoettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="1e37c-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="1e37c-107">Arvutuse lisamine</span><span class="sxs-lookup"><span data-stu-id="1e37c-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="1e37c-108">Arvutusavaldise koostamine</span><span class="sxs-lookup"><span data-stu-id="1e37c-108">Create calculation expression</span></span>
1. <span data-ttu-id="1e37c-109">Klõpsake käsku Muuda avaldist.</span><span class="sxs-lookup"><span data-stu-id="1e37c-109">Click Edit expression.</span></span>
2. <span data-ttu-id="1e37c-110">Sisestage väljale ConstraintBody tekst If[CabinetFinish=="White", 10, 15].</span><span class="sxs-lookup"><span data-stu-id="1e37c-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="1e37c-111">Klõpsake suvandit Kinnita.</span><span class="sxs-lookup"><span data-stu-id="1e37c-111">Click Validate.</span></span>
4. <span data-ttu-id="1e37c-112">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="1e37c-112">Click Close.</span></span>
5. <span data-ttu-id="1e37c-113">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1e37c-113">Click OK.</span></span>


