---
title: Teil palutakse kauba laovarude sätted salvestada ka siis, kui muudatusi pole tehtud
description: Teil palutakse kauba laovarude sätted salvestada ka siis, kui muudatusi pole tehtud.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049462"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a><span data-ttu-id="c6fe2-103">Teil palutakse kauba laovarude sätted salvestada ka siis, kui muudatusi pole tehtud</span><span class="sxs-lookup"><span data-stu-id="c6fe2-103">You're prompted to save item coverage settings even though you made no changes</span></span>

<span data-ttu-id="c6fe2-104">KB number: 4615588</span><span class="sxs-lookup"><span data-stu-id="c6fe2-104">KB number: 4615588</span></span>

## <a name="symptoms"></a><span data-ttu-id="c6fe2-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="c6fe2-105">Symptoms</span></span>

<span data-ttu-id="c6fe2-106">Mõnel juhul võite saada järgmise teate, kui avate **Kauba laovarude** lehe pärast kaupade importimist *Üksuse laovarude V2* kaudu:</span><span class="sxs-lookup"><span data-stu-id="c6fe2-106">In some scenarios, you might receive the following message when you open the **Item coverage** page after you import items through the *Item coverage V2* entity:</span></span>

> <span data-ttu-id="c6fe2-107">Kas soovite tehtud muudatused enne sulgemist salvestada?</span><span class="sxs-lookup"><span data-stu-id="c6fe2-107">Do you want to save your changes before closing?</span></span>

<span data-ttu-id="c6fe2-108">Te saate selle teate ka siis, kui te pole midagi teinud.</span><span class="sxs-lookup"><span data-stu-id="c6fe2-108">You receive this message even though you haven't made any changes.</span></span>

## <a name="resolution"></a><span data-ttu-id="c6fe2-109">Lahendus</span><span class="sxs-lookup"><span data-stu-id="c6fe2-109">Resolution</span></span>

<span data-ttu-id="c6fe2-110">**Kauba laovarude** leht hõlmab komplekset vaikeloogikat, mis võib põhjustada teate näitamise pärast andmebaasis otsemuudatuste tegemist, nt üksuse impordi kaudu.</span><span class="sxs-lookup"><span data-stu-id="c6fe2-110">The **Item coverage** page includes complex defaulting logic that might cause the message to be shown after direct changes have recently been made in the database, such as through entity import.</span></span> <span data-ttu-id="c6fe2-111">Näiteks on `AREGENERALSETTINGSOVERRIDDEN` üksuse välja väärtuseks seatud *Ei*, kuid te impordite faili, mis annab sellistele väljadele uued või muudetud väärtused `PRODUCTCOVERAGEGROUPID` ja/või `VENDORACCOUNTNUMBER`.</span><span class="sxs-lookup"><span data-stu-id="c6fe2-111">For example, the `AREGENERALSETTINGSOVERRIDDEN` entity field is set to *No*, but you import a file that provides new or modified values for fields such as `PRODUCTCOVERAGEGROUPID` and/or `VENDORACCOUNTNUMBER`.</span></span> <span data-ttu-id="c6fe2-112">Sellisel juhul, kuna `AREGENERALSETTINGSOVERRIDDEN` välja väärtuseks on seatud *Ei*, tühjendatakse väärtused automaatselt väljadelt, kui avate **Kauba laovarude lehe** peale importi esimest korda.</span><span class="sxs-lookup"><span data-stu-id="c6fe2-112">In this case, because the `AREGENERALSETTINGSOVERRIDDEN` field is set to *No*, the values are automatically cleared from the fields when you open the **Item coverage** page for the first time after the import.</span></span> <span data-ttu-id="c6fe2-113">Kui salvestate muudatused teateakna viipadega, talletatakse need andmebaasi.</span><span class="sxs-lookup"><span data-stu-id="c6fe2-113">If you save the changes as the message box prompts, they are stored in the database.</span></span> <span data-ttu-id="c6fe2-114">Vastasel juhul saate sama teate järgmisel korral, kui lehe avate.</span><span class="sxs-lookup"><span data-stu-id="c6fe2-114">Otherwise, you will receive the same message the next time that you open the page.</span></span>

<span data-ttu-id="c6fe2-115">Sellise käitumise vältimiseks, kuid ka väljade väärtuste kaasamiseks, nt üksuse `PRODUCTCOVERAGEGROUPID` impordi kaudu, seadke `AREGENERALSETTINGSOVERRIDDEN` importimiseks väärtusele *Jah*.</span><span class="sxs-lookup"><span data-stu-id="c6fe2-115">To prevent this behavior but also include values for fields such as `PRODUCTCOVERAGEGROUPID` through entity import, set `AREGENERALSETTINGSOVERRIDDEN` to *Yes* when you import.</span></span>
