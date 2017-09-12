--- 
title: "Põhivarade ümberklassifitseerimine"
description: "Põhivara ümberklassifitseerimiseks peate edastama selle uuele põhivaragrupile või määrama sellele samas grupis uue põhivara numbri."
author: saraschi2
manager: AnnBe
ms.date: 06/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: aed171004a43adbc504d74eb02c36df824a3e649
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="a0008-103">Põhivarade ümberklassifitseerimine</span><span class="sxs-lookup"><span data-stu-id="a0008-103">Reclassify fixed assets</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a0008-104">Põhivara ümberklassifitseerimiseks peate edastama selle uuele põhivaragrupile või määrama sellele samas grupis uue põhivara numbri.</span><span class="sxs-lookup"><span data-stu-id="a0008-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="a0008-105">Kui põhivara ümber klassifitseerida:</span><span class="sxs-lookup"><span data-stu-id="a0008-105">When a fixed asset is reclassified:</span></span>

<span data-ttu-id="a0008-106">• Uue põhivara jaoks on loodud kõik olemasoleva põhivara väärtusmudelid.</span><span class="sxs-lookup"><span data-stu-id="a0008-106">• All value models for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="a0008-107">Kogu algse põhivara jaoks häälestatud teave on kopeeritud uude põhivarasse.</span><span class="sxs-lookup"><span data-stu-id="a0008-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="a0008-108">Algse põhivara väärtusmudelite olekuks on Suletud.</span><span class="sxs-lookup"><span data-stu-id="a0008-108">The status of the value models for the original fixed asset is Closed.</span></span> 

<span data-ttu-id="a0008-109">• Uue põhivara uued väärtusmudelid sisaldavad ümberklassifitseerimise kuupäeva väljal Soetamiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="a0008-109">• The new value models of the new fixed asset contain the date of the reclassification in the Acquisition date field.</span></span> <span data-ttu-id="a0008-110">Kuupäev väljal Amortiseerimise algus on kopeeritud algsest vara puudutavast teabest.</span><span class="sxs-lookup"><span data-stu-id="a0008-110">The date in the Depreciation run date field is copied from the original asset information.</span></span> <span data-ttu-id="a0008-111">Kui kulumiarvestus on juba alanud, kuvab väli Viimase kulumiarvestuse kuupäev ümberklassifitseerimise kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="a0008-111">If the depreciation has already started, the Date when depreciation was last run field displays the date of the reclassification.</span></span> 

<span data-ttu-id="a0008-112">• Algse põhivara olemasolevad põhivarakanded on tühistatud ja uue põhivara jaoks uuesti loodud.</span><span class="sxs-lookup"><span data-stu-id="a0008-112">• The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

1. <span data-ttu-id="a0008-113">Avage Põhivarad > Perioodilised ülesanded > Ümberklassifitseerimine.</span><span class="sxs-lookup"><span data-stu-id="a0008-113">Go to Fixed assets > Periodic tasks > Reclassification.</span></span>
2. <span data-ttu-id="a0008-114">Väljal Põhivaragrupp valige ümberklassifitseerimiseks grupp.</span><span class="sxs-lookup"><span data-stu-id="a0008-114">In the Fixed asset group field, selet the group to reclassify.</span></span>
3. <span data-ttu-id="a0008-115">Väljal Põhivara kood valige ümberklassifitseerimiseks põhivara.</span><span class="sxs-lookup"><span data-stu-id="a0008-115">In the Fixed asset number field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="a0008-116">Valige väljal Uus põhivaragrupp see grupp, millele soovite põhivara üle kanda.</span><span class="sxs-lookup"><span data-stu-id="a0008-116">In the New fixed asset group field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="a0008-117">Kui uus põhivaragrupp on seotud numbriseeriaga, värskendatakse välja Uue põhivara kood numbriga uuest põhivaragrupi numbriseeriast.</span><span class="sxs-lookup"><span data-stu-id="a0008-117">If the new fixed asset group is attached to a number sequence, the New fixed asset number field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="a0008-118">Vastasel juhul värskendatakse välja Uue põhivara kood numbriga numbriseeriast, mis häälestatakse põhivara parameetrite leheküljel.</span><span class="sxs-lookup"><span data-stu-id="a0008-118">Otherwise, the New fixed asset number field is updated with the number from the number sequence that is set up in the Fixed asset parameters page.</span></span> <span data-ttu-id="a0008-119">Kui numbriseeriat ei häälestata põhivara parameetrite leheküljel, sisestage number väljale Uue põhivara kood.</span><span class="sxs-lookup"><span data-stu-id="a0008-119">If a number sequence is not set up in the Fixed asset parameters page, enter a number in the New fixed asset number field.</span></span>  
5. <span data-ttu-id="a0008-120">Sisestage kuupäev väljale Ümberklassifitseerimise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="a0008-120">In the Reclassification date field, enter a date.</span></span>
6. <span data-ttu-id="a0008-121">Sisestage või valige väärtus väljal Kande seeria.</span><span class="sxs-lookup"><span data-stu-id="a0008-121">In the Voucher series field, enter or select a value.</span></span>
7. <span data-ttu-id="a0008-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a0008-122">Click OK.</span></span>


