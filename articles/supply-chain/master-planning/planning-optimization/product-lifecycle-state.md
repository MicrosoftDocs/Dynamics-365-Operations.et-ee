---
title: Kindlate toote töötsükli olekutega toodete välistamine
description: Selles teemas selgitatakse, kuidas välistada optimeerimise planeerimise funktsiooni kasutamisel töötsükli olekul põhinevaid tooteid.
author: ChristianRytt
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 02c31aa3862df8dabc2b8c065dc3a94877d237f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992416"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a><span data-ttu-id="46c0b-103">Kindlate toote töötsükli olekutega toodete välistamine</span><span class="sxs-lookup"><span data-stu-id="46c0b-103">Exclude products that have specific product lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="46c0b-104">Väljastatud toodetel ja väljastatud tooteversioonidel on väli **Toote töötsükli olek**.</span><span class="sxs-lookup"><span data-stu-id="46c0b-104">Released products and released product versions include a **Product lifecycle state** field.</span></span> <span data-ttu-id="46c0b-105">See väli võimaldab teil muu hulgas kontrollida, millised tooted on koondplaneerimise käigus kaasatud.</span><span class="sxs-lookup"><span data-stu-id="46c0b-105">This field lets you control, among other things, which products are included during master planning.</span></span> <span data-ttu-id="46c0b-106">Te saate lisada, eemaldada ja redigeerida töötsükli olekuid vastavalt vajadusele, tehes valiku **Tooteteabe haldus \> Häälestus \> Toote töötsükli olek**.</span><span class="sxs-lookup"><span data-stu-id="46c0b-106">You can add, remove, and edit lifecycle states as required by going to **Product information management \> Setup \> Product lifecycle state**.</span></span> <span data-ttu-id="46c0b-107">Määrake iga toote elutsükli oleku jaoks suvandi **On planeerimiseks aktiivne** väärtuseks *Jah*, kui selle olekuga tooted tuleks koondplaneerimise käigus kaasata.</span><span class="sxs-lookup"><span data-stu-id="46c0b-107">For each product lifecycle state, set the **Is active for planning** option to *Yes* if products that have that state should be included during master planning.</span></span> <span data-ttu-id="46c0b-108">Kui suvandi väärtuseks on määratud *Ei*, välistatakse seotud tooted ja variandid kõigi koondandmete ja kõigi koosluse tasemel arvutustest.</span><span class="sxs-lookup"><span data-stu-id="46c0b-108">When the option is set to *No*, the associated products and variants will be excluded from all master planning and all calculations at the bill of materials (BOM) level.</span></span>

<span data-ttu-id="46c0b-109">Väljastatud tooteid ja variante, mille puhul jäetakse väli **Toote töötsükli olek** tühjaks, käsitletakse nii, nagu oleks neil toote töötsükli olek, kus suvandi **On planeerimiseks aktiivne** väärtuseks on määratud *Jah*.</span><span class="sxs-lookup"><span data-stu-id="46c0b-109">Released products and variants where the **Product lifecycle state** field is left blank are treated as though they have a product lifecycle state where the **Is active for planning** option is set to *Yes*.</span></span> <span data-ttu-id="46c0b-110">Teisisõnu kaasatakse need koondplaneerimise käigus.</span><span class="sxs-lookup"><span data-stu-id="46c0b-110">In other words, they will be included during master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="46c0b-111">Et vältida tarbetuid tarnesoovitusi, soovitame teil seostada kõik iganenud väljastatud tooted ja variandid toote töötsükli olekuga, kus suvandi **On planeerimiseks aktiivne** väärtuseks on määratud *Ei*.</span><span class="sxs-lookup"><span data-stu-id="46c0b-111">To help avoid unnecessary supply suggestions, we strongly recommend that you associate all obsolete released products and variants with a product lifecycle state where the **Is active for planning** option is set to *No*.</span></span> <span data-ttu-id="46c0b-112">See lähenemine on eriti oluline, kui töötate toote konfiguratsiooni variantidega, mis ei ole korduvkasutatavad, kuna see aitab ennetada jäätmete teket.</span><span class="sxs-lookup"><span data-stu-id="46c0b-112">This approach is especially important when you work with product configuration variants that aren't reusable, because it will help prevent waste.</span></span>

## <a name="related-resources"></a><span data-ttu-id="46c0b-113">Seotud ressursid</span><span class="sxs-lookup"><span data-stu-id="46c0b-113">Related resources</span></span>

<span data-ttu-id="46c0b-114">Lisateavet toote töötsükli olekute kohta leiate teemast [Toote töötsüklite ülevaade](../../pim/product-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="46c0b-114">For more information about product lifecycle states, see [Product lifecycle state overview](../../pim/product-lifecycle.md).</span></span>

<span data-ttu-id="46c0b-115">Täpsema teabe saamiseks selle kohta, kuidas kasutada toote töötsükli olekut toodete välistamiseks koondplaneerimisest ja koosluse taseme arvutustest, lugege teemat [Toote töötsükli oleku loomine toote välistamiseks koondplaneerimisest](../../pim/tasks/exclude-products-master-planning.md).</span><span class="sxs-lookup"><span data-stu-id="46c0b-115">For detailed information that includes steps for using product lifecycle states to exclude products from master planning and BOM-level calculations, see [Create a product lifecycle state to exclude products from Master planning](../../pim/tasks/exclude-products-master-planning.md).</span></span>
