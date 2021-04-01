---
title: Hankijate otsimine
description: Saate uurida, kuidas otsida hankijaid kindlate kriteeriumite järgi.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendSearchCriterion, VendSearchAddCategory, VendSearchAddReviewCriterionGroup, VendSearchResults, VendSearchAddReviewCriterion
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf93307600aac6fa6e45524092ec4811742010e4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244035"
---
# <a name="search-for-vendors"></a><span data-ttu-id="1cb4c-103">Hankijate otsimine</span><span class="sxs-lookup"><span data-stu-id="1cb4c-103">Search for vendors</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1cb4c-104">Saate uurida, kuidas otsida hankijaid kindlate kriteeriumite järgi.</span><span class="sxs-lookup"><span data-stu-id="1cb4c-104">Learn how to search for vendors based on specific criteria.</span></span> <span data-ttu-id="1cb4c-105">See näide selgitab, kuidas otsida kindla hankekategooria jaoks kinnitatud hankijaid, kelle esmane aadress on teatud riigis.</span><span class="sxs-lookup"><span data-stu-id="1cb4c-105">This example shows you how to search for vendors that are approved for a particular procurement category and have their primary address in a specific country.</span></span> <span data-ttu-id="1cb4c-106">Saate seda protseduuri käitada demoettevõtte USMF andmetega või oma andmetega.</span><span class="sxs-lookup"><span data-stu-id="1cb4c-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="1cb4c-107">Seda ülesannet täidab tavaliselt hankespetsialist.</span><span class="sxs-lookup"><span data-stu-id="1cb4c-107">This task would usually be carried out by a procurement professional.</span></span>

1. <span data-ttu-id="1cb4c-108">Minge jaotisse Hanked > Hankijad > Hankija otsing.</span><span class="sxs-lookup"><span data-stu-id="1cb4c-108">Go to Procurement and sourcing > Vendors > Vendor search.</span></span>
2. <span data-ttu-id="1cb4c-109">Klõpsake plussmärki, et avada leht Hankekategooria valimine.</span><span class="sxs-lookup"><span data-stu-id="1cb4c-109">Click on the Plus icon to open the Procurement category selection page.</span></span>  
3. <span data-ttu-id="1cb4c-110">Valige puul üksus CORP PROCUREMENT CATEGORIES\OFFICE MACHINES.</span><span class="sxs-lookup"><span data-stu-id="1cb4c-110">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE MACHINES'.</span></span>
    * <span data-ttu-id="1cb4c-111">Kui käitate seda protseduuri ülesandejuhendina, peate võib-olla klõpsama nuppu Ava, enne kui saate õige sõlme valida.</span><span class="sxs-lookup"><span data-stu-id="1cb4c-111">If you're running this procedure as a task guide, you may have to click the Unlock button before you can select the correct node.</span></span> <span data-ttu-id="1cb4c-112">Kui te ei kasuta USMF-i, valige üks oma kategooriatest.</span><span class="sxs-lookup"><span data-stu-id="1cb4c-112">If you're not using USMF, select one of the categories that you have.</span></span>  
4. <span data-ttu-id="1cb4c-113">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="1cb4c-113">Click Add.</span></span>
    * <span data-ttu-id="1cb4c-114">Saate siin valida rohkem kui ühe kategooria.</span><span class="sxs-lookup"><span data-stu-id="1cb4c-114">It's possible to select more than one category here.</span></span> <span data-ttu-id="1cb4c-115">Sellisel juhul leitakse otsinguga kõik hankijad, kes on vähemalt ühe kategooria puhul kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="1cb4c-115">If you do so, the search will find all the vendors that are approved for at least one of the categories.</span></span>  
5. <span data-ttu-id="1cb4c-116">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1cb4c-116">Click OK.</span></span>
6. <span data-ttu-id="1cb4c-117">Sisestage väärtus väljale Riik/regioon.</span><span class="sxs-lookup"><span data-stu-id="1cb4c-117">In the Country/region field, type a value.</span></span>
7. <span data-ttu-id="1cb4c-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1cb4c-118">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]