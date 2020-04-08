---
title: " Kassaregistrite jaoks finantsdimensioonide loomine ja registrites dimensiooniväärtuste konfigureerimine"
description: See protseduur selgitab finantsdimensioonide loomist kassaregistritele ja näitab, kuidas konfigureerida kassaregistrites finantsdimensiooni väärtusi.
author: jashanno
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7be50eba098b7b28594c8e18c721579f4bb2e879
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140987"
---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="6219a-103"> Kassaregistrite jaoks finantsdimensioonide loomine ja registrites dimensiooniväärtuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="6219a-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6219a-104">See protseduur selgitab finantsdimensioonide loomist kassaregistritele ja näitab, kuidas konfigureerida kassaregistrites finantsdimensiooni väärtusi.</span><span class="sxs-lookup"><span data-stu-id="6219a-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="6219a-105">Protseduur ei sisalda muid seotud etappe, näiteks dimensioonikogumite ja kontostruktuuride loomist.</span><span class="sxs-lookup"><span data-stu-id="6219a-105">This procedure doesn't include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="6219a-106">Need ülesanded leiate teistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="6219a-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="6219a-107">Salvestises kasutatakse demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="6219a-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="6219a-108">Avage Pearaamat > Kontoplaan > Dimensioonid > Finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="6219a-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="6219a-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6219a-109">Click New.</span></span>
3. <span data-ttu-id="6219a-110">Valige suvand väljal Kasuta väärtusi allikast.</span><span class="sxs-lookup"><span data-stu-id="6219a-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="6219a-111">Sisestage väärtus väljale Dimensiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="6219a-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="6219a-112">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="6219a-112">Click Activate.</span></span>
6. <span data-ttu-id="6219a-113">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="6219a-113">Click Close.</span></span>
7. <span data-ttu-id="6219a-114">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="6219a-114">Click Activate.</span></span>
8. <span data-ttu-id="6219a-115">Klõpsake suvandit Dimensiooniväärtused.</span><span class="sxs-lookup"><span data-stu-id="6219a-115">Click Dimension values.</span></span>
9. <span data-ttu-id="6219a-116">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6219a-116">Close the page.</span></span>
10. <span data-ttu-id="6219a-117">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6219a-117">Click Save.</span></span>
11. <span data-ttu-id="6219a-118">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6219a-118">Close the page.</span></span>
12. <span data-ttu-id="6219a-119">Avage Jaemüük ja kaubandus > Kanali häälestus > Kassa Seadistus > Registrid.</span><span class="sxs-lookup"><span data-stu-id="6219a-119">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="6219a-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6219a-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="6219a-121">Laiendage jaotist Finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="6219a-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="6219a-122">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="6219a-122">Click Edit.</span></span>
16. <span data-ttu-id="6219a-123">Klõpsake väljal Terminal otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="6219a-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="6219a-124">Leidke ja valige loendist värskendatava registri dimensiooniväärtus.</span><span class="sxs-lookup"><span data-stu-id="6219a-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="6219a-125">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6219a-125">Click Save.</span></span>

