---
title: Uue toote loomine
description: See teema kirjeldab uue konfiguratsiooni loomist.
author: ShylaThompson
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6d33a13920e1881cdc69ad7c100180d3b3b441d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820030"
---
# <a name="create-a-new-product"></a><span data-ttu-id="cedd0-103">Uue toote loomine</span><span class="sxs-lookup"><span data-stu-id="cedd0-103">Create a new product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cedd0-104">See teema kirjeldab uue konfiguratsiooni loomist.</span><span class="sxs-lookup"><span data-stu-id="cedd0-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="cedd0-105">Tavaliselt teeb seda toote koostaja.</span><span class="sxs-lookup"><span data-stu-id="cedd0-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="cedd0-106">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="cedd0-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="cedd0-107">Toote loomine</span><span class="sxs-lookup"><span data-stu-id="cedd0-107">Create a product</span></span>
1. <span data-ttu-id="cedd0-108">Avage navigeerimispaanil **Moodulid > Tooteteabe haldus > Tooted > Tooted**.</span><span class="sxs-lookup"><span data-stu-id="cedd0-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="cedd0-109">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="cedd0-109">Select **New**.</span></span>
3. <span data-ttu-id="cedd0-110">Sisestage väärtus väljale **Toote number**.</span><span class="sxs-lookup"><span data-stu-id="cedd0-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="cedd0-111">Kui toote koodile ei ole numbriseeriat seadistatud, tuleb see sisestada käsitsi.</span><span class="sxs-lookup"><span data-stu-id="cedd0-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="cedd0-112">Sisestage väärtus väljale **Toote nimi**.</span><span class="sxs-lookup"><span data-stu-id="cedd0-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="cedd0-113">Toote nimi on vaikimisi otsingu nimi.</span><span class="sxs-lookup"><span data-stu-id="cedd0-113">The product name defaults to the search name.</span></span> <span data-ttu-id="cedd0-114">Saate seda vajaduse korral muuta.</span><span class="sxs-lookup"><span data-stu-id="cedd0-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="cedd0-115">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="cedd0-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="cedd0-116">Dimensioonigruppide seadistamine</span><span class="sxs-lookup"><span data-stu-id="cedd0-116">Set up dimension groups</span></span>
1. <span data-ttu-id="cedd0-117">Klõpsake rippdialoogi avamiseks suvandit **Dimensiooni rühmad**.</span><span class="sxs-lookup"><span data-stu-id="cedd0-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="cedd0-118">Sisestage või valige väärtus väljal **Ladustamisdimensiooni rühm**.</span><span class="sxs-lookup"><span data-stu-id="cedd0-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="cedd0-119">Laoala dimensiooni grupp määrab, millised laoala dimensioonid peate sisestama iga toote kande kohta ja kuidas seda varudes jälgitakse.</span><span class="sxs-lookup"><span data-stu-id="cedd0-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="cedd0-120">Sisestage või valige väärtus väljal **Jälgimisdimensiooni rühm**.</span><span class="sxs-lookup"><span data-stu-id="cedd0-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="cedd0-121">Jälgimisdimensiooni grupp määrab, millised jälgimisdimensioonid peate sisestama iga toote kande kohta ja kuidas seda varudes käsitletakse.</span><span class="sxs-lookup"><span data-stu-id="cedd0-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="cedd0-122">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="cedd0-122">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]