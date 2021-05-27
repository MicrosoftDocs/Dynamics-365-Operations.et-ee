---
title: TaxTransi välja vale väärtus
description: Selles teemas antakse teavet TaxTransi valede väljaväärtuste tõrkeotsingu kohta.
author: bijian
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 488ff54f1dd99208db940024a2fe8b2d25861f44
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020159"
---
# <a name="incorrect-field-value-in-taxtrans"></a><span data-ttu-id="751fe-103">TaxTransi välja vale väärtus</span><span class="sxs-lookup"><span data-stu-id="751fe-103">Incorrect field value in TaxTrans</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="751fe-104">Kui **TaxTrans** välja väärtus on vale, kasutage probleemi lahendamiseks selle teema teavet.</span><span class="sxs-lookup"><span data-stu-id="751fe-104">If a field value in **TaxTrans** is incorrect, use the information in this topic to try to resolve the issue.</span></span>

## <a name="overview-of-values"></a><span data-ttu-id="751fe-105">Väärtuste ülevaade</span><span class="sxs-lookup"><span data-stu-id="751fe-105">Overview of values</span></span>
<span data-ttu-id="751fe-106">Järgmine loend näitab, kuidas **TaxTrans**, **TaxUncommitted** ja **TmpTaxWorkTrans** on sarnased andmekomplektid, kuid töös erinevad.</span><span class="sxs-lookup"><span data-stu-id="751fe-106">The following list shows how **TaxTrans**, **TaxUncommitted**, and **TmpTaxWorkTrans** are similar data sets, but in work differently.</span></span>

  - <span data-ttu-id="751fe-107">**TaxTrans** on andmebaasi kinnistatud lõplik sisestatud maksukanne.</span><span class="sxs-lookup"><span data-stu-id="751fe-107">**TaxTrans** is the final posted tax transaction result persisted in the database.</span></span>
  - <span data-ttu-id="751fe-108">**TaxUncommitted** on andmebaasis kinnistatud vahe arvutatud maksu tulemus (kui see on olemas), mida kasutatakse hiljem sisestamisel.</span><span class="sxs-lookup"><span data-stu-id="751fe-108">**TaxUncommitted** is the intermediate calculated tax result persisted in the database (if applicable), which will be used later in posting.</span></span>
  - <span data-ttu-id="751fe-109">**TmpTaxWorkTrans** on ajutine arvutatud maksu tulemus mälu tabelis (tabeli tüüp = InMemory).</span><span class="sxs-lookup"><span data-stu-id="751fe-109">**TmpTaxWorkTrans** is the temporary calculated tax result in the in-memory table (Table Type = InMemory).</span></span>

<span data-ttu-id="751fe-110">Kui leiate vale **TaxTrans** veeru algpõhjuse, olete leidnud ka vale **TaxUncommitted** või **TmpTaxWorkTrans** veeru algpõhjuse.</span><span class="sxs-lookup"><span data-stu-id="751fe-110">If you find the root cause of an incorrect **TaxTrans** column, you've also found the root cause of an incorrect **TaxUncommitted** or **TmpTaxWorkTrans** column.</span></span> <span data-ttu-id="751fe-111">Seda seetõttu, et kolm veergu on üksteisest kopeeritud.</span><span class="sxs-lookup"><span data-stu-id="751fe-111">This is because the three columns are copied from each other.</span></span>

<span data-ttu-id="751fe-112">Tavaliselt luuakse maksuarvestuse ajal **TmpTaxWorkTrans** ja seejärel (kui on olemas) **TaxUncommitted**.</span><span class="sxs-lookup"><span data-stu-id="751fe-112">Typically, during tax calculation, **TmpTaxWorkTrans** is generated, and then, if applicable, **TaxUncommitted** is generated.</span></span> <span data-ttu-id="751fe-113">Maksu sisestamisel luuakse **TaxTrans**.</span><span class="sxs-lookup"><span data-stu-id="751fe-113">During tax posting, **TaxTrans** is generated.</span></span>


## <a name="add-breakpoints"></a><span data-ttu-id="751fe-114">Lisa katkestuspunktid</span><span class="sxs-lookup"><span data-stu-id="751fe-114">Add breakpoints</span></span>
<span data-ttu-id="751fe-115">Katkestuspuntide lisamiseks tehke järgmised toimingud:</span><span class="sxs-lookup"><span data-stu-id="751fe-115">To add breakpoints, complete the following steps:</span></span> 

1. <span data-ttu-id="751fe-116">Lisage laiendid ja katkestuspunktid *insert()* ja *update()* nagu alltoodud laiendites.</span><span class="sxs-lookup"><span data-stu-id="751fe-116">Add extensions and breakpoints in *insert()* and *update()* in the extensions as shown below.</span></span>

     - <span data-ttu-id="751fe-117">**TaxTrans**</span><span class="sxs-lookup"><span data-stu-id="751fe-117">**TaxTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="751fe-118">**TaxUncommitted**</span><span class="sxs-lookup"><span data-stu-id="751fe-118">**TaxUncommitted**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="751fe-119">**TmpTaxWorkTrans**</span><span class="sxs-lookup"><span data-stu-id="751fe-119">**TmpTaxWorkTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. <span data-ttu-id="751fe-120">Võite katkestuspunktid lisada ka otse, kui **TaxUncommitted** ei ole lisatud.</span><span class="sxs-lookup"><span data-stu-id="751fe-120">Alternatively, you can add breakpoints directly when **TaxUncommitted** is not included.</span></span>

     - <span data-ttu-id="751fe-121">*TaxTrans.insert()*, *TaxTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="751fe-121">*TaxTrans.insert()*, *TaxTrans.update()*</span></span>
     - <span data-ttu-id="751fe-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="751fe-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span></span>

## <a name="reproduce-and-debug"></a><span data-ttu-id="751fe-123">Taasesitamine ja vigade eemaldamine</span><span class="sxs-lookup"><span data-stu-id="751fe-123">Reproduce and debug</span></span>

<span data-ttu-id="751fe-124">Pärast katkestuspunktide seadistamist on vigade eemaldamise ajal nähtavad kõik andmete püsivuse muutused.</span><span class="sxs-lookup"><span data-stu-id="751fe-124">After the breakpoints are set, every data persistency change is visible during debugging.</span></span> <span data-ttu-id="751fe-125">Et leida **TaxTrans**, **TaxUncommitted** või **TmpTaxWorkTrans** vale veeru algpõhjus, vaadake üle ja märkige järgmised üksused:</span><span class="sxs-lookup"><span data-stu-id="751fe-125">To find the root cause of an incorrect column of **TaxTrans**, **TaxUncommitted**, or **TmpTaxWorkTrans**, review and note the following items:</span></span>

- <span data-ttu-id="751fe-126">Viimane katkestuspunkt, kus veerg on õige.</span><span class="sxs-lookup"><span data-stu-id="751fe-126">The last breakpoint where the column is correct.</span></span>
- <span data-ttu-id="751fe-127">Esimene katkestuspunkt, kus veerg on vale.</span><span class="sxs-lookup"><span data-stu-id="751fe-127">The first breakpoint where the column is incorrect.</span></span>
- <span data-ttu-id="751fe-128">Mis toimub nende kahe punkti vahel.</span><span class="sxs-lookup"><span data-stu-id="751fe-128">What happens in between those two points.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="751fe-129">Kohanduse olemasolu tuvastamine</span><span class="sxs-lookup"><span data-stu-id="751fe-129">Determine whether customization exists</span></span>
<span data-ttu-id="751fe-130">Kui olete eelmistes jaotistes kirjeldatud toimingud teinud, kuid pole probleemi lahendada õnnestunud, tehke kindlaks, kas kohandamine on võimalik.</span><span class="sxs-lookup"><span data-stu-id="751fe-130">If you've completed the steps in the previous sections but have not been able to resolve the issue, determine whether customization exists.</span></span> <span data-ttu-id="751fe-131">Kui kohandust ei ole, pöörduge abi saamiseks Microsoft Support'i poole.</span><span class="sxs-lookup"><span data-stu-id="751fe-131">If no customization exists, contact Microsoft Support for assistance.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

