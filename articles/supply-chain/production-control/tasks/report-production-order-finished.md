---
title: Tootmistellimuse lõpuleviimisest teatamine
description: See protseduur näitab, kuidas tootmistellimust lõpetatuks kinnitada.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd, ProdSetupReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 93193e6365bcf82fbbf93af81e2581a358899fa1
ms.sourcegitcommit: 175f9394021322c685c5b37317c2f649c81a731a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826282"
---
# <a name="report-a-production-order-as-finished"></a><span data-ttu-id="6e34e-103">Tootmistellimuse lõpuleviimisest teatamine</span><span class="sxs-lookup"><span data-stu-id="6e34e-103">Report a production order as finished</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6e34e-104">See protseduur näitab, kuidas tootmistellimust lõpetatuks kinnitada.</span><span class="sxs-lookup"><span data-stu-id="6e34e-104">This procedure shows how to report a production order as finished.</span></span> <span data-ttu-id="6e34e-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="6e34e-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6e34e-106">See on kuues protseduur seitsmest, mis selgitab tootmistellimuse elutsüklit.</span><span class="sxs-lookup"><span data-stu-id="6e34e-106">This is the sixth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="report-a-production-order-as-finished"></a><span data-ttu-id="6e34e-107">Tootmistellimuse lõpuleviimisest teatamine</span><span class="sxs-lookup"><span data-stu-id="6e34e-107">Report a production order as finished</span></span>
1. <span data-ttu-id="6e34e-108">Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="6e34e-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="6e34e-109">Valige tootmistellimus, mille olek on Alustatud.</span><span class="sxs-lookup"><span data-stu-id="6e34e-109">Select a production order that has the Started status.</span></span>  
2. <span data-ttu-id="6e34e-110">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="6e34e-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="6e34e-111">Klõpsake valikut Kinnita lõpetamine.</span><span class="sxs-lookup"><span data-stu-id="6e34e-111">Click Report as finished.</span></span>
    * <span data-ttu-id="6e34e-112">Sellel lehel saate kinnitada valmis toote koguse, mille lõpetamine kinnitatakse.</span><span class="sxs-lookup"><span data-stu-id="6e34e-112">On this page, you can confirm the quantity of the finished product to be reported as finished.</span></span>  
4. <span data-ttu-id="6e34e-113">Klõpsake vahekaarti Üldine.</span><span class="sxs-lookup"><span data-stu-id="6e34e-113">Click the General tab.</span></span>
5. <span data-ttu-id="6e34e-114">Määrake valiku Õige kogus väärtuseks 18.</span><span class="sxs-lookup"><span data-stu-id="6e34e-114">Set Good quantity to '18'.</span></span>
6. <span data-ttu-id="6e34e-115">Määrake valiku Veakogus väärtuseks 2.</span><span class="sxs-lookup"><span data-stu-id="6e34e-115">Set Error quantity to '2'.</span></span>
7. <span data-ttu-id="6e34e-116">Tehke väljal Vea põhjus valik Materjal.</span><span class="sxs-lookup"><span data-stu-id="6e34e-116">In the Error cause field, select 'Material'.</span></span>
8. <span data-ttu-id="6e34e-117">Märkige või tühjendage ruut Lõpeta töö.</span><span class="sxs-lookup"><span data-stu-id="6e34e-117">Select or clear the End job check box.</span></span>
9. <span data-ttu-id="6e34e-118">Valige või tühjendage märkeruut Aktsepteeri viga.</span><span class="sxs-lookup"><span data-stu-id="6e34e-118">Select or clear the Accept error check box.</span></span>
10. <span data-ttu-id="6e34e-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6e34e-119">Click OK.</span></span>

## <a name="verify-the-report-as-finished-journal"></a><span data-ttu-id="6e34e-120">Kinnitage tööleht Kinnita lõpetamine</span><span class="sxs-lookup"><span data-stu-id="6e34e-120">Verify the Report as finished journal</span></span>
1. <span data-ttu-id="6e34e-121">Klõpsake toimingupaanil valikut Kuva.</span><span class="sxs-lookup"><span data-stu-id="6e34e-121">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="6e34e-122">Klõpsake valikut Lõpetatuna kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="6e34e-122">Click Reported as finished.</span></span>
3. <span data-ttu-id="6e34e-123">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6e34e-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="6e34e-124">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6e34e-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6e34e-125">Tööleht Kinnita lõpetamine on sisestatud.</span><span class="sxs-lookup"><span data-stu-id="6e34e-125">The Report as finished journal is posted.</span></span> <span data-ttu-id="6e34e-126">Kui soovite töölehte korrigeerida, saate koostada käsitsi uue töölehe, millel saab muudatusi teha.</span><span class="sxs-lookup"><span data-stu-id="6e34e-126">If you want to make adjustments to the journal, you can manually create  a new journal where you can make changes.</span></span>  

