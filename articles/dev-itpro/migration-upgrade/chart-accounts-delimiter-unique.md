---
title: Kontoplaani eraldaja peab olema kordumatu
description: "Rakenduses Dynamics 365 for Finance and Operations ei saa kontoplaani ja dimensiooniväärtuste eraldaja sama olla. Pärast versiooniuuendust peate eraldaja väärtusi muutma."
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e12c47e4acd6aa8a92a909d490da9e590b5fcd20
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="chart-of-accounts-delimiter-must-be-unique"></a><span data-ttu-id="ce248-104">Kontoplaani eraldaja peab olema kordumatu</span><span class="sxs-lookup"><span data-stu-id="ce248-104">Chart of accounts delimiter must be unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce248-105">Rakenduses Microsoft Dynamics AX 2012 saate kasutada kontoplaani ja dimensiooniväärtuste puhul sama eraldajat.</span><span class="sxs-lookup"><span data-stu-id="ce248-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="ce248-106">Rakenduses Dynamics 365 for Finance and Operations ei saa kontoplaani ja dimensiooniväärtuste eraldaja sama olla.</span><span class="sxs-lookup"><span data-stu-id="ce248-106">In Dynamics 365 for Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="ce248-107">Topelteraldaja korral saate seda pärast versiooniuuendust muuta.</span><span class="sxs-lookup"><span data-stu-id="ce248-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="ce248-108">See funktsioon on saadaval järgmistes rakenduste versioonides.</span><span class="sxs-lookup"><span data-stu-id="ce248-108">This feature is available in:</span></span>
- <span data-ttu-id="ce248-109">Dynamics 365 for Finance and Operationsi versioon 8.0</span><span class="sxs-lookup"><span data-stu-id="ce248-109">Dynamics 365 for Finance and Operations version 8.0</span></span>
- <span data-ttu-id="ce248-110">Dynamics 365 for Finance and Operationsi versioon 7.1, KB 4094701 puhul ei saa finantsdimensioone sisestada, kui dimensiooniväärtused sisaldavad kontoplaani eraldajat</span><span class="sxs-lookup"><span data-stu-id="ce248-110">Dynamics 365 for Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="ce248-111">Dynamics 365 for Finance and Operations versioon 7.2 KB 4092967 puhul ei saa valida alamprojekti dimensioonina, kui alamprojekti vorming sisaldab dimensiooni eraldajat</span><span class="sxs-lookup"><span data-stu-id="ce248-111">Dynamics 365 for Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="ce248-112">Eraldaja värskendamine</span><span class="sxs-lookup"><span data-stu-id="ce248-112">Update delimiter</span></span>
<span data-ttu-id="ce248-113">Kontoplaani konflikti korral saab muuta kontoplaani eraldaja ja projekti/alamprojekti ID vormingut.</span><span class="sxs-lookup"><span data-stu-id="ce248-113">If there is a conflict with the Chart of Accounts, the Chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="ce248-114">Ühtegi teist dimensiooni eraldajat muuta ei saa.</span><span class="sxs-lookup"><span data-stu-id="ce248-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="ce248-115">Kontoplaani eraldajat saate muuta pärast üleminekut Finance and Operationsile, kui valite **Üldised pearaamatu parameetrid** > **Kontoplaan ja dimensioonid** > **Muuda eraldajat**.</span><span class="sxs-lookup"><span data-stu-id="ce248-115">You can change the chart of accounts delimiter after upgrade to Finance and Operations in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="ce248-116">Kui konfliktne on ainult projekti/alamprojekti ID vorming, saate selle väärtust muuta, valides **Projektihalduse ja -arvestuse parameetrid** > **Üldine** > **Alamprojekti vormingu muutmine**.</span><span class="sxs-lookup"><span data-stu-id="ce248-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="ce248-117">Kuidas teha kindlaks, kas teie keskkonna puhul on nõutud eraldajate värskendamine?</span><span class="sxs-lookup"><span data-stu-id="ce248-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="ce248-118">Kui täiendatud keskkonnas esineb eraldajatega seoses konflikte, võib segmenditud sisestamise või dimensiooni kirje juhtimises väärtuste sisestamisel ilmneda ebastabiilsus.</span><span class="sxs-lookup"><span data-stu-id="ce248-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="ce248-119">See tähendab, et teil tuleb alati konto ja dimensiooni kombinatsioonide sisestamisel kasutada otsinguid või hüpikmenüüd.</span><span class="sxs-lookup"><span data-stu-id="ce248-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>

