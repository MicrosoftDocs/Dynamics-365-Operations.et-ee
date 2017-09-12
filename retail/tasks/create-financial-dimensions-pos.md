--- 
title: " Kassaregistrite jaoks finantsdimensioonide loomine ja registrites dimensiooniväärtuste konfigureerimine"
description: "See protseduur selgitab finantsdimensioonide loomist kassaregistritele ja näitab, kuidas konfigureerida kassaregistrites finantsdimensiooni väärtusi."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8a3a6abc19bae20b7899628d0463cf458955671a
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="2ac6c-103"> Kassaregistrite jaoks finantsdimensioonide loomine ja registrites dimensiooniväärtuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="2ac6c-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="2ac6c-104">See protseduur selgitab finantsdimensioonide loomist kassaregistritele ja näitab, kuidas konfigureerida kassaregistrites finantsdimensiooni väärtusi.</span><span class="sxs-lookup"><span data-stu-id="2ac6c-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="2ac6c-105">Protseduur ei sisalda muid seotud etappe, näiteks dimensioonikogumite ja kontostruktuuride loomist.</span><span class="sxs-lookup"><span data-stu-id="2ac6c-105">This procedure doesn’t include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="2ac6c-106">Need ülesanded leiate teistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="2ac6c-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="2ac6c-107">Salvestises kasutatakse demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="2ac6c-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="2ac6c-108">Avage Pearaamat > Kontoplaan > Dimensioonid > Finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="2ac6c-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="2ac6c-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="2ac6c-109">Click New.</span></span>
3. <span data-ttu-id="2ac6c-110">Valige suvand väljal Kasuta väärtusi allikast.</span><span class="sxs-lookup"><span data-stu-id="2ac6c-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="2ac6c-111">Sisestage väärtus väljale Dimensiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="2ac6c-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="2ac6c-112">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="2ac6c-112">Click Activate.</span></span>
6. <span data-ttu-id="2ac6c-113">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="2ac6c-113">Click Close.</span></span>
7. <span data-ttu-id="2ac6c-114">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="2ac6c-114">Click Activate.</span></span>
8. <span data-ttu-id="2ac6c-115">Klõpsake suvandit Dimensiooniväärtused.</span><span class="sxs-lookup"><span data-stu-id="2ac6c-115">Click Dimension values.</span></span>
9. <span data-ttu-id="2ac6c-116">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2ac6c-116">Close the page.</span></span>
10. <span data-ttu-id="2ac6c-117">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="2ac6c-117">Click Save.</span></span>
11. <span data-ttu-id="2ac6c-118">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2ac6c-118">Close the page.</span></span>
12. <span data-ttu-id="2ac6c-119">Avage Jaemüük ja kaubandus > Kanali häälestus > Kassa Seadistus > Registrid.</span><span class="sxs-lookup"><span data-stu-id="2ac6c-119">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="2ac6c-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="2ac6c-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="2ac6c-121">Laiendage jaotist Finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="2ac6c-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="2ac6c-122">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="2ac6c-122">Click Edit.</span></span>
16. <span data-ttu-id="2ac6c-123">Klõpsake väljal Terminal otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="2ac6c-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="2ac6c-124">Leidke ja valige loendist värskendatava registri dimensiooniväärtus.</span><span class="sxs-lookup"><span data-stu-id="2ac6c-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="2ac6c-125">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="2ac6c-125">Click Save.</span></span>


