---
title: Koondplaneerimise kaupu ei saa filtreerida seotud laovarude grupi väärtuste alusel
description: Koondplaneerimise kaupu ei saa filtreerida seotud laovarude grupi väärtuste alusel.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049463"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a><span data-ttu-id="74388-103">Koondplaneerimise kaupu ei saa filtreerida seotud laovarude grupi väärtuste alusel</span><span class="sxs-lookup"><span data-stu-id="74388-103">You can't filter master planning items by their related coverage group values</span></span>

<span data-ttu-id="74388-104">KB number: 4612572</span><span class="sxs-lookup"><span data-stu-id="74388-104">KB number: 4612572</span></span>

## <a name="symptoms"></a><span data-ttu-id="74388-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="74388-105">Symptoms</span></span>

<span data-ttu-id="74388-106">Te soovite filtreerida kaupu, mis kaasatakse koondplaneerimise pakett-töösse, mis põhineb kauba laovarude tabeli seotud kirjete väärtustel.</span><span class="sxs-lookup"><span data-stu-id="74388-106">You want to filter the items that will be included in a master planning batch job, based on the values of related records from the item coverage table.</span></span> <span data-ttu-id="74388-107">(Näiteks soovite üksusi filtreerida nende järgi **Hankija** ja/või **laovarude grupi** väärtus).</span><span class="sxs-lookup"><span data-stu-id="74388-107">(For example, you want to filter items by their **Vendor** and/or **Coverage group** value).</span></span> <span data-ttu-id="74388-108">Pakktöö filtri seadistus võimaldab luua ühenduse tabelist **Kaubad** laovarude tabeliga **Laovarude tabeliga** ja seejärel määrata päringu kauba laovarude tabeli väljaväärtused.</span><span class="sxs-lookup"><span data-stu-id="74388-108">The filter setup for the batch job lets you create a join from the **Items** table to the **Item coverage** table, and then specify field values from the item coverage table in your query.</span></span> <span data-ttu-id="74388-109">Kuid pärast selle seadistuse lõpule viimist loob süsteem siiski plaanitud tellimused kogu kauba laovarudele, mitte ainult kaupadele, mis vastavad kauba laovarude tabeli määratud välja väärtustele.</span><span class="sxs-lookup"><span data-stu-id="74388-109">However, after you complete this setup, the system still creates planned orders for the whole item coverage, not just for the items that match the specified field values from the item coverage table.</span></span>

## <a name="resolution"></a><span data-ttu-id="74388-110">Lahendus</span><span class="sxs-lookup"><span data-stu-id="74388-110">Resolution</span></span>

<span data-ttu-id="74388-111">Pakett-töö filter saab filtreerida ainult kaupade puhul.</span><span class="sxs-lookup"><span data-stu-id="74388-111">The batch job filter can filter only on items.</span></span> <span data-ttu-id="74388-112">Kuigi saate lisada liitmise **kauba laovarude tabelile** ei mõjuta selle tabeli suhtes soovitudfiltrisätted päringu väljundit.</span><span class="sxs-lookup"><span data-stu-id="74388-112">Although you can add a join to the **Item coverage** table, filter settings that you make against that table won't affect the query output.</span></span> <span data-ttu-id="74388-113">Käitusajal käitab süsteem kõigi laovarude gruppide ja kõigi filtreeritud kaupade variatsioonide planeerimist.</span><span class="sxs-lookup"><span data-stu-id="74388-113">At runtime, the system runs planning for all the coverage groups and all the variations that the filtered items have.</span></span> <span data-ttu-id="74388-114">Kui kaup on juba käituse kaasatud, ei mõjuta ükski kaubafiltrisse kaasatud laovarude grupp plaanimise väljundit.</span><span class="sxs-lookup"><span data-stu-id="74388-114">After an item is already included in the run, any coverage groups that are included in the item filter a won't affect the planning output.</span></span>
