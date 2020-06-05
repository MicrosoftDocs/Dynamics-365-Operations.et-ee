---
title: Kontsernisisesed kulud
description: Töötaja, kes töötab ühes organisatsiooni juriidilises isikus, võib teha tööd sama organisatsiooni teise juriidilise isiku heaks. Selles olukorras võite kontsernisisese kulu funktsiooni abil määrata töötaja kulud sellele juriidilisele isikule, kelle heaks töö tehti.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390880"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="60154-104">Kontsernisisesed kulud</span><span class="sxs-lookup"><span data-stu-id="60154-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60154-105">Töötaja, kes töötab ühes organisatsiooni juriidilises isikus, võib teha tööd sama organisatsiooni teise juriidilise isiku heaks.</span><span class="sxs-lookup"><span data-stu-id="60154-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="60154-106">Selles olukorras võite kontsernisisese kulu funktsiooni abil määrata töötaja kulud sellele juriidilisele isikule, kelle heaks töö tehti.</span><span class="sxs-lookup"><span data-stu-id="60154-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="60154-107">Juriidilist isikut, mis töötajale tööd annab, nimetatakse välja laenavaks juriidiliseks isikuks.</span><span class="sxs-lookup"><span data-stu-id="60154-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="60154-108">Juriidilist isikut, millele töötaja kulusid tekitab, nimetakse laenavaks juriidiliseks isikuks.</span><span class="sxs-lookup"><span data-stu-id="60154-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="60154-109">Enne, kui töötaja saab luua ja esitada kulusid töö kohta, mida tehakse teise juriidilise isiku heaks, tehke välja laenavas juriidilises isikus lehel **Kuluhalduse parameetrid** valik **Luba kontsernisiseseid kuluridu**.</span><span class="sxs-lookup"><span data-stu-id="60154-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="60154-110">Kontsernisiseste kulude maksu sisestamine</span><span class="sxs-lookup"><span data-stu-id="60154-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60154-111">Kui soovite kasutada kuluaruandes välja laenava (algne) juriidilise isiku maksugruppe laenava (sihtisik) juriidilise isiku asemel, peate selle konfigureerima pearaamatu käibemaksu seadistamisel.</span><span class="sxs-lookup"><span data-stu-id="60154-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="60154-112">Kui pearaamatu parameetri **Kontsernisisese maksu sisestamise juriidiline isik** väärtuseks on seatud **Algne** ja **Rakenda käibemaksuga maksustamise reeglid** väärtuseks **Ei**, kasutatakse välja laenava juriidilise isiku maksukombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="60154-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="60154-113">Kui selle parameetri väärtuseks on seatud **Sihtisik**, kasutatakse laenava juriidilise isiku maksukombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="60154-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="60154-114">Kui Ameerika Ühendriikide juriidilise isiku puhul on parameetri väärtuseks seatud **Algne**, peab ka väli **Saadaolev käibemaks** olema konfigureeritud uuel lehel **Pearaamatu sisestamisgrupid**.</span><span class="sxs-lookup"><span data-stu-id="60154-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="60154-115">Raamatupidamise mootor kasutab selle välja teavet maksuga seotud raamatupidamise kirje jaoks.</span><span class="sxs-lookup"><span data-stu-id="60154-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="60154-116">See käitumine on kooskõlas kuluridadega, mis on sisestatud projektiga või ilma.</span><span class="sxs-lookup"><span data-stu-id="60154-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
