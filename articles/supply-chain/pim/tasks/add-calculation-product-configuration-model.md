---
title: Arvutuse lisamine toote konfiguratsioonimudelile
description: See protseduur näitab, kuidas lisada toote konfiguratsioonimudelile uut arvutust.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32bc2ac5815c2739147664f1e1df2528178db51e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213396"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="820ae-103">Arvutuse lisamine toote konfiguratsioonimudelile</span><span class="sxs-lookup"><span data-stu-id="820ae-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="820ae-104">See protseduur näitab, kuidas lisada toote konfiguratsioonimudelile uut arvutust.</span><span class="sxs-lookup"><span data-stu-id="820ae-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="820ae-105">See näitab, kuidas saate koostada loogikaavaldise, määrates tehtemärgiga „If” kõlari kõrguseks 10 valgete kõlarite ja 15 kõigi muude korpuse viimistluste puhul.</span><span class="sxs-lookup"><span data-stu-id="820ae-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="820ae-106">See protseduur kasutab komponenti Tipptasemel kõlar demoettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="820ae-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="820ae-107">Arvutuse lisamine</span><span class="sxs-lookup"><span data-stu-id="820ae-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="820ae-108">Arvutusavaldise koostamine</span><span class="sxs-lookup"><span data-stu-id="820ae-108">Create calculation expression</span></span>
1. <span data-ttu-id="820ae-109">Klõpsake käsku Muuda avaldist.</span><span class="sxs-lookup"><span data-stu-id="820ae-109">Click Edit expression.</span></span>
2. <span data-ttu-id="820ae-110">Sisestage väljale ConstraintBody tekst If[CabinetFinish=="White", 10, 15].</span><span class="sxs-lookup"><span data-stu-id="820ae-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="820ae-111">Klõpsake suvandit Kinnita.</span><span class="sxs-lookup"><span data-stu-id="820ae-111">Click Validate.</span></span>
4. <span data-ttu-id="820ae-112">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="820ae-112">Click Close.</span></span>
5. <span data-ttu-id="820ae-113">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="820ae-113">Click OK.</span></span>

