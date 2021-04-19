---
title: Toote elutsükli oleku määramine väljastatud tooteetalonile
description: See protseduur näitab, kuidas määrata toote elutsükli olek väljastatud tooteetalonile ja selle variantidele.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 66859c7f7f5be6eaadd9470fd9b792daa28ce33d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807879"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a><span data-ttu-id="2ef35-103">Toote elutsükli oleku määramine väljastatud tooteetalonile</span><span class="sxs-lookup"><span data-stu-id="2ef35-103">Assign a product lifecycle state to a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ef35-104">See protseduur näitab, kuidas määrata toote elutsükli olek väljastatud tooteetalonile ja selle variantidele.</span><span class="sxs-lookup"><span data-stu-id="2ef35-104">This procedure shows how to assign a product lifecycle state to a released product master and its variants.</span></span> <span data-ttu-id="2ef35-105">Eeltingimus: teil tuleb esmalt esitada tegevuse juhist „Uue toote elutsükli oleku loomine” ja veenduda, et vähemalt üks toote elutsükli olek oleks loodud, et saaksite tegevuse juhist esitada.</span><span class="sxs-lookup"><span data-stu-id="2ef35-105">Prerequisite: You need to play the task guide "Create a new product lifecycle state" first to make sure that you have at least one product lifecycle state created before you can play this task guide.</span></span>


## <a name="find-a-released-product-master"></a><span data-ttu-id="2ef35-106">Väljastatud tooteetaloni ülesotsimine</span><span class="sxs-lookup"><span data-stu-id="2ef35-106">Find a released product master</span></span>
1. <span data-ttu-id="2ef35-107">Avage Tooteteabe haldus > Tooted > Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="2ef35-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="2ef35-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="2ef35-108">In the list, find and select the desired record.</span></span>

> [!NOTE]
> <span data-ttu-id="2ef35-109">Tooteetaloni alamtüüp on Tooteetalon.</span><span class="sxs-lookup"><span data-stu-id="2ef35-109">A product master has the Product subtype Product master.</span></span>  

## <a name="update-the-lifecycle-state"></a><span data-ttu-id="2ef35-110">Elutsükli oleku värskendamine</span><span class="sxs-lookup"><span data-stu-id="2ef35-110">Update the lifecycle state</span></span>
1. <span data-ttu-id="2ef35-111">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="2ef35-111">Click Edit.</span></span>
2. <span data-ttu-id="2ef35-112">Väljal Toote elutsükli olek sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="2ef35-112">In the Product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="2ef35-113">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="2ef35-113">Click Save.</span></span>
4. <span data-ttu-id="2ef35-114">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="2ef35-114">Click Yes.</span></span>

> [!NOTE]
> <span data-ttu-id="2ef35-115">Kui valitud on Jah, värskendatakse toote uue elutsükli oleku alusel ka kõiki seotud väljastatud tootevariante, millel on sama algne olek mis väljastatud tooteetalonil.</span><span class="sxs-lookup"><span data-stu-id="2ef35-115">If Yes is selected, all the related released product variants that have the same original status as the released product master are also updated to the new product lifecycle state.</span></span> <span data-ttu-id="2ef35-116">Kui valitud on Ei, säilitatakse kõikide variantide praegune olek.</span><span class="sxs-lookup"><span data-stu-id="2ef35-116">If No is selected, all variants keep their actual state.</span></span> <span data-ttu-id="2ef35-117">Väljastatud tooteetalonist erineva elutsükli olekuga variante ei värskendata.</span><span class="sxs-lookup"><span data-stu-id="2ef35-117">Variants that have a different product lifecycle state from the released product master are not updated.</span></span>  

## <a name="verify-the-lifecycle-state-of-the-variants"></a><span data-ttu-id="2ef35-118">Variantide elutsükli oleku kontrollimine</span><span class="sxs-lookup"><span data-stu-id="2ef35-118">Verify the lifecycle state of the variants</span></span>
1. <span data-ttu-id="2ef35-119">Klõpsake valikut Väljastatud tootevariandid.</span><span class="sxs-lookup"><span data-stu-id="2ef35-119">Click Released product variants.</span></span>

> [!NOTE]
> <span data-ttu-id="2ef35-120">Pange tähele, et kõik variandid pärivad väljastatud tooteetaloni jaoks valitud elutsükli oleku.</span><span class="sxs-lookup"><span data-stu-id="2ef35-120">Note that all variants have inherited the selected lifecycle state from the released product master.</span></span>  

2. <span data-ttu-id="2ef35-121">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="2ef35-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="2ef35-122">Väljal Toote elutsükli olek sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="2ef35-122">In the Product lifecycle state field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]