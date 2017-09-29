--- 
title: Tootmistellimuse vabastamine
description: "See protseduur näitab, kuidas tootmistellimust väljastada."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2ae2d84bd12d338c9bada5518c43178b22112006
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="release-a-production-order"></a><span data-ttu-id="51232-103">Tootmistellimuse vabastamine</span><span class="sxs-lookup"><span data-stu-id="51232-103">Release a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="51232-104">See protseduur näitab, kuidas tootmistellimust väljastada.</span><span class="sxs-lookup"><span data-stu-id="51232-104">This procedure shows how to release a production order.</span></span> <span data-ttu-id="51232-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="51232-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="51232-106">See on neljas protseduur seitsmest, mis selgitab tootmistellimuse elutsüklit.</span><span class="sxs-lookup"><span data-stu-id="51232-106">This is the fourth procedure out of seven which explains the production order lifecycle.</span></span>

1. <span data-ttu-id="51232-107">Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="51232-107">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="51232-108">Valige ruudustikus tootmistellimus, mille olekuks on Plaanitud.</span><span class="sxs-lookup"><span data-stu-id="51232-108">In the grid, select a production order that has the Scheduled status.</span></span>  
2. <span data-ttu-id="51232-109">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="51232-109">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="51232-110">Klõpsake valikut Vabasta.</span><span class="sxs-lookup"><span data-stu-id="51232-110">Click Release.</span></span>
    * <span data-ttu-id="51232-111">Sellel lehel saate kinnitada tootmistellimuste valitud vahemiku väljastamise.</span><span class="sxs-lookup"><span data-stu-id="51232-111">On this page, you can confirm the release of the selected range of production orders.</span></span> <span data-ttu-id="51232-112">Kui soovite tellimusi lisada, klõpsake suvandit Vali.</span><span class="sxs-lookup"><span data-stu-id="51232-112">Click Select if you want to add orders.</span></span>  
    * <span data-ttu-id="51232-113">Etapp Väljastus näitab, millal tootmistellimus on tootmistöödesse väljastatud, nii et tööde operaatorid saavad tootmistööde edenemisest aru anda.</span><span class="sxs-lookup"><span data-stu-id="51232-113">The Release step indicates when the production order is released to the production shop floor so that the shop floor operators can report progress on the production jobs.</span></span> <span data-ttu-id="51232-114">Väljastada saab olulist tööde töötlemise teavet sisaldavaid tootmisdokumente.</span><span class="sxs-lookup"><span data-stu-id="51232-114">Production papers that contain relevant information about processing the jobs can be issued.</span></span> <span data-ttu-id="51232-115">Toormaterjalide komplekteerimise laotööd luuakse laoprotsessiks seadistatud kaupade puhul.</span><span class="sxs-lookup"><span data-stu-id="51232-115">The warehouse work for raw material picking is generated for the items that are set up for the warehouse process.</span></span>  
4. <span data-ttu-id="51232-116">Klõpsake vahekaarti Üldine.</span><span class="sxs-lookup"><span data-stu-id="51232-116">Click the General tab.</span></span>
    * <span data-ttu-id="51232-117">Valige, millised tootmisaruanded tuleks printida.</span><span class="sxs-lookup"><span data-stu-id="51232-117">Select which production reports should be printed.</span></span> <span data-ttu-id="51232-118">Töökaardi aruanne prindib iga plaanitud töö lehe ja nõuab tootmistellimuse plaanimist töö tasemel.</span><span class="sxs-lookup"><span data-stu-id="51232-118">The Job card report prints a page for each scheduled job and requires the production order to be scheduled at the job level.</span></span> <span data-ttu-id="51232-119">Aruanne sisaldab teavet plaanitud algus- ja lõppaja, toodetava koguse ja selle kohta, milline ressurss tööd töötleb.</span><span class="sxs-lookup"><span data-stu-id="51232-119">The report contains information about the scheduled start and end time, the quantity to produce, and which resource processes the job.</span></span> <span data-ttu-id="51232-120">Protsessi tööaruanne kogub sama teavet samale lehele, kuid ei prindi lehte iga töö puhul.</span><span class="sxs-lookup"><span data-stu-id="51232-120">The Route job report collects the same information on the same page, but does not print a page for each job.</span></span> <span data-ttu-id="51232-121">Protsessikaardi aruanne kuvab ainult toimingud, kuid mitte tööd.</span><span class="sxs-lookup"><span data-stu-id="51232-121">The Route card report only shows the operations but not the jobs.</span></span> <span data-ttu-id="51232-122">Seetõttu ei nõuta selles aruandes tööde plaanimist, kuid seda saab kasutada tootmistellimuste plaanimisel toimingu tasandil.</span><span class="sxs-lookup"><span data-stu-id="51232-122">Therefore, this report does not require job scheduling, but can be used when production orders are scheduled at the operation level.</span></span>  
5. <span data-ttu-id="51232-123">Märkige ruut Prindi protsessi kaart.</span><span class="sxs-lookup"><span data-stu-id="51232-123">Click the Print route card checkbox.</span></span>
6. <span data-ttu-id="51232-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="51232-124">Click OK.</span></span>
7. <span data-ttu-id="51232-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="51232-125">Close the page.</span></span>


