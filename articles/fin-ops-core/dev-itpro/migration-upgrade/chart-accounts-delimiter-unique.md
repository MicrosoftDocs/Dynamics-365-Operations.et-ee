---
title: Diagrammi eraldaja kordumatuks muutmine
description: Selles teemas selgitatakse, kuidas kontoplaani ja dimensiooniväärtuste eraldaja ei saa sama olla. Pärast versiooniuuendust peate eraldaja väärtusi muutma.
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 2622245c7ce7213665ab32f4020c282df28cb886
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248776"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a><span data-ttu-id="13a32-104">Kontoplaani eraldaja kordumatuks muutmine</span><span class="sxs-lookup"><span data-stu-id="13a32-104">Make the chart of accounts delimiter unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13a32-105">Rakenduses Microsoft Dynamics AX 2012 saate kasutada kontoplaani ja dimensiooniväärtuste puhul sama eraldajat.</span><span class="sxs-lookup"><span data-stu-id="13a32-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="13a32-106">Finance and Operationsi praeguses versioonis ei saa kontoplaani ja dimensiooniväärtuste eraldaja sama olla.</span><span class="sxs-lookup"><span data-stu-id="13a32-106">In current versions of Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="13a32-107">Topelteraldaja korral saate seda pärast versiooniuuendust muuta.</span><span class="sxs-lookup"><span data-stu-id="13a32-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="13a32-108">Seda funktsiooni ei saa järgmistes versioonides kasutada.</span><span class="sxs-lookup"><span data-stu-id="13a32-108">This feature is available in the following versions:</span></span>
- <span data-ttu-id="13a32-109">Finance and Operationsi versioon 8.0</span><span class="sxs-lookup"><span data-stu-id="13a32-109">Finance and Operations version 8.0</span></span>
- <span data-ttu-id="13a32-110">Finance and Operationsi versiooni 7.1, KB 4094701 puhul ei saa finantsdimensioone sisestada, kui dimensiooniväärtused sisaldavad kontoplaani eraldajat</span><span class="sxs-lookup"><span data-stu-id="13a32-110">Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="13a32-111">Finance and Operationsi versiooni 7.2 KB 4092967 puhul ei saa valida alamprojekti dimensioonina, kui alamprojekti vorming sisaldab dimensiooni eraldajat</span><span class="sxs-lookup"><span data-stu-id="13a32-111">Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="13a32-112">Eraldaja värskendamine</span><span class="sxs-lookup"><span data-stu-id="13a32-112">Update delimiter</span></span>
<span data-ttu-id="13a32-113">Kontoplaani konflikti korral saab muuta kontoplaani eraldaja ja projekti/alamprojekti ID vormingut.</span><span class="sxs-lookup"><span data-stu-id="13a32-113">If there is a conflict with the chart of accounts, the chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="13a32-114">Ühtegi teist dimensiooni eraldajat muuta ei saa.</span><span class="sxs-lookup"><span data-stu-id="13a32-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="13a32-115">Kontoplaani eraldajat saate muuta pärast üleminekut, kui valite **Üldised pearaamatu parameetrid** > **Kontoplaan ja dimensioonid** > **Muuda eraldajat**.</span><span class="sxs-lookup"><span data-stu-id="13a32-115">You can change the chart of accounts delimiter after upgrade in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="13a32-116">Kui konfliktne on ainult projekti/alamprojekti ID vorming, saate selle väärtust muuta, valides **Projektihalduse ja -arvestuse parameetrid** > **Üldine** > **Alamprojekti vormingu muutmine**.</span><span class="sxs-lookup"><span data-stu-id="13a32-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="13a32-117">Kuidas teha kindlaks, kas teie keskkonna puhul on nõutud eraldajate värskendamine?</span><span class="sxs-lookup"><span data-stu-id="13a32-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="13a32-118">Kui täiendatud keskkonnas esineb eraldajatega seoses konflikte, võib segmenditud sisestamise või dimensiooni kirje juhtimises väärtuste sisestamisel ilmneda ebastabiilsus.</span><span class="sxs-lookup"><span data-stu-id="13a32-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="13a32-119">See tähendab, et teil tuleb alati konto ja dimensiooni kombinatsioonide sisestamisel kasutada otsinguid või hüpikmenüüd.</span><span class="sxs-lookup"><span data-stu-id="13a32-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>
