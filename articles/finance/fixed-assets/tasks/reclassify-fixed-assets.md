---
title: Põhivarade ümberklassifitseerimine
description: Põhivara ümberklassifitseerimiseks peate edastama selle uuele põhivaragrupile või määrama sellele samas grupis uue põhivara numbri.
author: saraschi2
manager: AnnBe
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cfc1425aca7a62205e0c7c50237f206a179a0e7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968850"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="99e90-103">Põhivarade ümberklassifitseerimine</span><span class="sxs-lookup"><span data-stu-id="99e90-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="99e90-104">Põhivara ümberklassifitseerimiseks peate edastama selle uuele põhivaragrupile või määrama sellele samas grupis uue põhivara numbri.</span><span class="sxs-lookup"><span data-stu-id="99e90-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="99e90-105">Kui põhivara ümber klassifitseerida:</span><span class="sxs-lookup"><span data-stu-id="99e90-105">When a fixed asset is reclassified:</span></span>

* <span data-ttu-id="99e90-106">Uue põhivara jaoks on loodud kõik olemasoleva põhivararaamatud.</span><span class="sxs-lookup"><span data-stu-id="99e90-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="99e90-107">Kogu algse põhivara jaoks häälestatud teave on kopeeritud uude põhivarasse.</span><span class="sxs-lookup"><span data-stu-id="99e90-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="99e90-108">Raamatute algse põhivara olek on Suletud.</span><span class="sxs-lookup"><span data-stu-id="99e90-108">The status of the books for the original fixed asset is Closed.</span></span> 

* <span data-ttu-id="99e90-109">Uue põhivara uued raamatud sisaldavad ümberklassifitseerimise kuupäeva väljal **Soetamiskuupäev**.</span><span class="sxs-lookup"><span data-stu-id="99e90-109">The new books of the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="99e90-110">Kuupäev väljal **Amortiseerimise algus** on kopeeritud algsest vara puudutavast teabest.</span><span class="sxs-lookup"><span data-stu-id="99e90-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="99e90-111">Kui kulumiarvestus on juba alanud, kuvab väli **Viimase kulumiarvestuse kuupäev** ümberklassifitseerimise kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="99e90-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

* <span data-ttu-id="99e90-112">Algse põhivara olemasolevad põhivarakanded on tühistatud ja uue põhivara jaoks uuesti loodud.</span><span class="sxs-lookup"><span data-stu-id="99e90-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

<span data-ttu-id="99e90-113">Põhivara ümberklassifitseerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="99e90-113">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="99e90-114">Avage **Põhivarad > Perioodilised ülesanded > Ümberklassifitseerimine.**</span><span class="sxs-lookup"><span data-stu-id="99e90-114">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="99e90-115">Väljal **Põhivaragrupp** valige ümberklassifitseerimiseks grupp.</span><span class="sxs-lookup"><span data-stu-id="99e90-115">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="99e90-116">Väljal **Põhivara kood** valige ümberklassifitseerimiseks põhivara.</span><span class="sxs-lookup"><span data-stu-id="99e90-116">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="99e90-117">Valige väljal **Uus põhivaragrupp** see grupp, millele soovite põhivara üle kanda.</span><span class="sxs-lookup"><span data-stu-id="99e90-117">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="99e90-118">Kui uus põhivaragrupp on seotud numbriseeriaga, värskendatakse välja **Uue põhivara kood** numbriga uuest põhivaragrupi numbriseeriast.</span><span class="sxs-lookup"><span data-stu-id="99e90-118">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="99e90-119">Vastasel juhul värskendatakse välja **Uue põhivara kood** numbriga numbriseeriast, mis häälestatakse lehel **Põhivara parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="99e90-119">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="99e90-120">Kui numbriseeriat ei häälestata leheküljel **Põhivara parameetrid**, sisestage number väljale **Uus põhivara kood**.</span><span class="sxs-lookup"><span data-stu-id="99e90-120">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="99e90-121">Sisestage kuupäev väljale **Ümberklassifitseerimise kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="99e90-121">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="99e90-122">Sisestage või valige väärtus väljal **Kande seeria**.</span><span class="sxs-lookup"><span data-stu-id="99e90-122">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="99e90-123">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="99e90-123">Click **OK**.</span></span>
