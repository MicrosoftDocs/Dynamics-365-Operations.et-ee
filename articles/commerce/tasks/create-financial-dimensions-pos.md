---
title: " Kassaregistrite jaoks finantsdimensioonide loomine ja registrites dimensiooniväärtuste konfigureerimine"
description: See protseduur selgitab finantsdimensioonide loomist kassaregistritele ja näitab, kuidas konfigureerida kassaregistrites finantsdimensiooni väärtusi.
author: jashanno
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eecb126ae550d67310ada22bd7d91438f7a20cf2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790954"
---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="cd7d9-103"> Kassaregistrite jaoks finantsdimensioonide loomine ja registrites dimensiooniväärtuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="cd7d9-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd7d9-104">See protseduur selgitab finantsdimensioonide loomist kassaregistritele ja näitab, kuidas konfigureerida kassaregistrites finantsdimensiooni väärtusi.</span><span class="sxs-lookup"><span data-stu-id="cd7d9-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="cd7d9-105">Protseduur ei sisalda muid seotud etappe, näiteks dimensioonikogumite ja kontostruktuuride loomist.</span><span class="sxs-lookup"><span data-stu-id="cd7d9-105">This procedure doesn't include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="cd7d9-106">Need ülesanded leiate teistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="cd7d9-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="cd7d9-107">Salvestises kasutatakse demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="cd7d9-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="cd7d9-108">Avage Pearaamat > Kontoplaan > Dimensioonid > Finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="cd7d9-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="cd7d9-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="cd7d9-109">Click New.</span></span>
3. <span data-ttu-id="cd7d9-110">Valige suvand väljal Kasuta väärtusi allikast.</span><span class="sxs-lookup"><span data-stu-id="cd7d9-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="cd7d9-111">Sisestage väärtus väljale Dimensiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="cd7d9-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="cd7d9-112">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="cd7d9-112">Click Activate.</span></span>
6. <span data-ttu-id="cd7d9-113">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="cd7d9-113">Click Close.</span></span>
7. <span data-ttu-id="cd7d9-114">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="cd7d9-114">Click Activate.</span></span>
8. <span data-ttu-id="cd7d9-115">Klõpsake suvandit Dimensiooniväärtused.</span><span class="sxs-lookup"><span data-stu-id="cd7d9-115">Click Dimension values.</span></span>
9. <span data-ttu-id="cd7d9-116">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="cd7d9-116">Close the page.</span></span>
10. <span data-ttu-id="cd7d9-117">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="cd7d9-117">Click Save.</span></span>
11. <span data-ttu-id="cd7d9-118">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="cd7d9-118">Close the page.</span></span>
12. <span data-ttu-id="cd7d9-119">Avage Jaemüük ja kaubandus > Kanali häälestus > Kassa Seadistus > Registrid.</span><span class="sxs-lookup"><span data-stu-id="cd7d9-119">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="cd7d9-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="cd7d9-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="cd7d9-121">Laiendage jaotist Finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="cd7d9-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="cd7d9-122">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="cd7d9-122">Click Edit.</span></span>
16. <span data-ttu-id="cd7d9-123">Klõpsake väljal Terminal otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="cd7d9-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="cd7d9-124">Leidke ja valige loendist värskendatava registri dimensiooniväärtus.</span><span class="sxs-lookup"><span data-stu-id="cd7d9-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="cd7d9-125">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="cd7d9-125">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]