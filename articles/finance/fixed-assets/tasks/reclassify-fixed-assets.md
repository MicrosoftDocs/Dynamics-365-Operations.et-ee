---
title: Põhivarade ümberklassifitseerimine
description: Põhivara ümberklassifitseerimiseks peate edastama selle uuele põhivaragrupile või määrama sellele samas grupis uue põhivara numbri.
author: saraschi2
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbfb754459fad1f3b1509f4f9c65c20e0385b013
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944707"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="e30cb-103">Põhivarade ümberklassifitseerimine</span><span class="sxs-lookup"><span data-stu-id="e30cb-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e30cb-104">Põhivara ümberklassifitseerimiseks peate edastama selle uuele põhivaragrupile või määrama sellele samas grupis uue põhivara numbri.</span><span class="sxs-lookup"><span data-stu-id="e30cb-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="e30cb-105">Kui põhivara ümber klassifitseerida:</span><span class="sxs-lookup"><span data-stu-id="e30cb-105">When a fixed asset is reclassified:</span></span>

- <span data-ttu-id="e30cb-106">Uue põhivara jaoks on loodud kõik olemasoleva põhivararaamatud.</span><span class="sxs-lookup"><span data-stu-id="e30cb-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="e30cb-107">Kogu algse põhivara jaoks häälestatud teave on kopeeritud uude põhivarasse.</span><span class="sxs-lookup"><span data-stu-id="e30cb-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="e30cb-108">Raamatute algse põhivara olek on Suletud.</span><span class="sxs-lookup"><span data-stu-id="e30cb-108">The status of the books for the original fixed asset is Closed.</span></span> 

- <span data-ttu-id="e30cb-109">Uue põhivara uued raamatud sisaldavad ümberklassifitseerimise kuupäeva väljal **Soetamiskuupäev**.</span><span class="sxs-lookup"><span data-stu-id="e30cb-109">The new books for the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="e30cb-110">Kuupäev väljal **Amortiseerimise algus** on kopeeritud algsest vara puudutavast teabest.</span><span class="sxs-lookup"><span data-stu-id="e30cb-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="e30cb-111">Kui kulumiarvestus on juba alanud, kuvab väli **Viimase kulumiarvestuse kuupäev** ümberklassifitseerimise kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="e30cb-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

- <span data-ttu-id="e30cb-112">Algse põhivara olemasolevad põhivarakanded on tühistatud ja uue põhivara jaoks uuesti loodud.</span><span class="sxs-lookup"><span data-stu-id="e30cb-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

- <span data-ttu-id="e30cb-113">Kui vara, millel on ülekandetehing, on ümber klassifitseeritud, kuvab süsteem teadet **Tegevuskeskuses**, mis näitab, et ülekandetehingut ei viidud ümberklassifitseerimisprotsessi käigus lõpule.</span><span class="sxs-lookup"><span data-stu-id="e30cb-113">When an asset that has a transfer transaction has been reclassified, the system will display a message in the **Action center** to indicate that a transfer transaction wasn't completed during the reclassification process.</span></span> <span data-ttu-id="e30cb-114">Ülekandetehing on vaja lõpule viia, et viia olemasolev ümberklassifitseerimistehing sobivasse finantsdimensiooni.</span><span class="sxs-lookup"><span data-stu-id="e30cb-114">It's necessary to complete a transfer transaction to move the existing reclassification transactions to the appropriate financial dimensions.</span></span> 

   <span data-ttu-id="e30cb-115">Ümberklassifitseerimise protsessi ajal käivitab süsteem järgmised tegevused, et ümberklassifitseerida vara saldo algsest varast uueks varaks.</span><span class="sxs-lookup"><span data-stu-id="e30cb-115">During the reclassification process, the system runs the following actions to reclassify the asset balance from the original asset to the new asset.</span></span> 
   
   - <span data-ttu-id="e30cb-116">Ümberklassifitseerimisprotsess kopeerib andmed algsest põhivararaamatust uude põhivararaamatusse.</span><span class="sxs-lookup"><span data-stu-id="e30cb-116">The reclassification process copies the data from the original fixed asset book to the new fixed asset book.</span></span>

   - <span data-ttu-id="e30cb-117">Ümberklassifitseerimiskanne kasutab algselt sisestatud soetamise teavet, mis sisaldab soetuskandesse kaasatud finantsdimensiooni teavet.</span><span class="sxs-lookup"><span data-stu-id="e30cb-117">The reclassification transaction uses information from the original posted acquisition that includes financial dimension information that is included in the acquisition transaction.</span></span>  
   
   - <span data-ttu-id="e30cb-118">Samal ajal tühistab ümberklassifitseerimisprotsess algse vara soetamise ja vara üleviimise kande.</span><span class="sxs-lookup"><span data-stu-id="e30cb-118">At the same time, the reclassification process reverses the original asset acquisition and asset transfer transaction.</span></span> 

<span data-ttu-id="e30cb-119">Järgmine diagramm ja protseduur annavad näite ümberklassifitseerimise protsessi kohta.</span><span class="sxs-lookup"><span data-stu-id="e30cb-119">The following diagram and procedure provide an example of the reclassification process.</span></span> 

<span data-ttu-id="e30cb-120">[![Ümberklassifitseerimisprotsessi kuvav diagramm](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span><span class="sxs-lookup"><span data-stu-id="e30cb-120">[![Diagram showing the reclassicification process](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span></span>

<span data-ttu-id="e30cb-121">Põhivara ümberklassifitseerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e30cb-121">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="e30cb-122">Avage **Põhivarad > Perioodilised ülesanded > Ümberklassifitseerimine.**</span><span class="sxs-lookup"><span data-stu-id="e30cb-122">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="e30cb-123">Väljal **Põhivaragrupp** valige ümberklassifitseerimiseks grupp.</span><span class="sxs-lookup"><span data-stu-id="e30cb-123">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="e30cb-124">Väljal **Põhivara kood** valige ümberklassifitseerimiseks põhivara.</span><span class="sxs-lookup"><span data-stu-id="e30cb-124">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="e30cb-125">Valige väljal **Uus põhivaragrupp** see grupp, millele soovite põhivara üle kanda.</span><span class="sxs-lookup"><span data-stu-id="e30cb-125">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="e30cb-126">Kui uus põhivaragrupp on seotud numbriseeriaga, värskendatakse välja **Uue põhivara kood** numbriga uuest põhivaragrupi numbriseeriast.</span><span class="sxs-lookup"><span data-stu-id="e30cb-126">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="e30cb-127">Vastasel juhul värskendatakse välja **Uue põhivara kood** numbriga numbriseeriast, mis häälestatakse lehel **Põhivara parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="e30cb-127">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="e30cb-128">Kui numbriseeriat ei häälestata leheküljel **Põhivara parameetrid**, sisestage number väljale **Uus põhivara kood**.</span><span class="sxs-lookup"><span data-stu-id="e30cb-128">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="e30cb-129">Sisestage kuupäev väljale **Ümberklassifitseerimise kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="e30cb-129">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="e30cb-130">Sisestage või valige väärtus väljal **Kande seeria**.</span><span class="sxs-lookup"><span data-stu-id="e30cb-130">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="e30cb-131">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e30cb-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
