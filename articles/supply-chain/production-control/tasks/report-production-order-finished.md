---
title: Tootmistellimuse lõpuleviimisest teatamine
description: See protseduur näitab, kuidas tootmistellimust lõpetatuks kinnitada.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 97e67ff51e4bc4533aeb2485c34cd5ec8a882bb6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558430"
---
# <a name="report-a-production-order-as-finished"></a><span data-ttu-id="0a4ed-103">Tootmistellimuse lõpuleviimisest teatamine</span><span class="sxs-lookup"><span data-stu-id="0a4ed-103">Report a production order as finished</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0a4ed-104">See protseduur näitab, kuidas tootmistellimust lõpetatuks kinnitada.</span><span class="sxs-lookup"><span data-stu-id="0a4ed-104">This procedure shows how to report a production order as finished.</span></span> <span data-ttu-id="0a4ed-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="0a4ed-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0a4ed-106">See on kuues protseduur seitsmest, mis selgitab tootmistellimuse elutsüklit.</span><span class="sxs-lookup"><span data-stu-id="0a4ed-106">This is the sixth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="report-a-production-order-as-finished"></a><span data-ttu-id="0a4ed-107">Tootmistellimuse lõpuleviimisest teatamine</span><span class="sxs-lookup"><span data-stu-id="0a4ed-107">Report a production order as finished</span></span>
1. <span data-ttu-id="0a4ed-108">Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="0a4ed-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="0a4ed-109">Valige tootmistellimus, mille olek on Alustatud.</span><span class="sxs-lookup"><span data-stu-id="0a4ed-109">Select a production order that has the Started status.</span></span>  
2. <span data-ttu-id="0a4ed-110">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="0a4ed-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="0a4ed-111">Klõpsake valikut Kinnita lõpetamine.</span><span class="sxs-lookup"><span data-stu-id="0a4ed-111">Click Report as finished.</span></span>
    * <span data-ttu-id="0a4ed-112">Sellel lehel saate kinnitada valmis toote koguse, mille lõpetamine kinnitatakse.</span><span class="sxs-lookup"><span data-stu-id="0a4ed-112">On this page, you can confirm the quantity of the finished product to be reported as finished.</span></span>  
4. <span data-ttu-id="0a4ed-113">Klõpsake vahekaarti Üldine.</span><span class="sxs-lookup"><span data-stu-id="0a4ed-113">Click the General tab.</span></span>
5. <span data-ttu-id="0a4ed-114">Määrake valiku Õige kogus väärtuseks 18.</span><span class="sxs-lookup"><span data-stu-id="0a4ed-114">Set Good quantity to '18'.</span></span>
6. <span data-ttu-id="0a4ed-115">Määrake valiku Veakogus väärtuseks 2.</span><span class="sxs-lookup"><span data-stu-id="0a4ed-115">Set Error quantity to '2'.</span></span>
7. <span data-ttu-id="0a4ed-116">Tehke väljal Vea põhjus valik Materjal.</span><span class="sxs-lookup"><span data-stu-id="0a4ed-116">In the Error cause field, select 'Material'.</span></span>
8. <span data-ttu-id="0a4ed-117">Märkige või tühjendage ruut Lõpeta töö.</span><span class="sxs-lookup"><span data-stu-id="0a4ed-117">Select or clear the End job check box.</span></span>
9. <span data-ttu-id="0a4ed-118">Valige või tühjendage märkeruut Aktsepteeri viga.</span><span class="sxs-lookup"><span data-stu-id="0a4ed-118">Select or clear the Accept error check box.</span></span>
10. <span data-ttu-id="0a4ed-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0a4ed-119">Click OK.</span></span>

## <a name="verify-the-report-as-finished-journal"></a><span data-ttu-id="0a4ed-120">Kinnitage tööleht Kinnita lõpetamine</span><span class="sxs-lookup"><span data-stu-id="0a4ed-120">Verify the Report as finished journal</span></span>
1. <span data-ttu-id="0a4ed-121">Klõpsake toimingupaanil valikut Kuva.</span><span class="sxs-lookup"><span data-stu-id="0a4ed-121">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="0a4ed-122">Klõpsake valikut Lõpetatuna kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="0a4ed-122">Click Reported as finished.</span></span>
3. <span data-ttu-id="0a4ed-123">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="0a4ed-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="0a4ed-124">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="0a4ed-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0a4ed-125">Tööleht Kinnita lõpetamine on sisestatud.</span><span class="sxs-lookup"><span data-stu-id="0a4ed-125">The Report as finished journal is posted.</span></span> <span data-ttu-id="0a4ed-126">Kui soovite töölehte korrigeerida, saate koostada käsitsi uue töölehe, millel saab muudatusi teha.</span><span class="sxs-lookup"><span data-stu-id="0a4ed-126">If you want to make adjustments to the journal, you can manually create  a new journal where you can make changes.</span></span>  

