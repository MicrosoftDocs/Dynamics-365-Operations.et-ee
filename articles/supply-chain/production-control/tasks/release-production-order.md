---
title: Tootmistellimuse vabastamine
description: See protseduur näitab, kuidas tootmistellimust väljastada.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmRelease, SrsReportViewerForm, ProdSetupRelease
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f5c5ca5ebf51d0722318c455e6ca59d3a893793
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831958"
---
# <a name="release-a-production-order"></a><span data-ttu-id="5f50a-103">Tootmistellimuse vabastamine</span><span class="sxs-lookup"><span data-stu-id="5f50a-103">Release a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5f50a-104">See protseduur näitab, kuidas tootmistellimust väljastada.</span><span class="sxs-lookup"><span data-stu-id="5f50a-104">This procedure shows how to release a production order.</span></span> <span data-ttu-id="5f50a-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="5f50a-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5f50a-106">See on neljas protseduur seitsmest, mis selgitab tootmistellimuse elutsüklit.</span><span class="sxs-lookup"><span data-stu-id="5f50a-106">This is the fourth procedure out of seven which explains the production order lifecycle.</span></span>

1. <span data-ttu-id="5f50a-107">Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="5f50a-107">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="5f50a-108">Valige ruudustikus tootmistellimus, mille olekuks on Plaanitud.</span><span class="sxs-lookup"><span data-stu-id="5f50a-108">In the grid, select a production order that has the Scheduled status.</span></span>  
2. <span data-ttu-id="5f50a-109">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="5f50a-109">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="5f50a-110">Klõpsake valikut Vabasta.</span><span class="sxs-lookup"><span data-stu-id="5f50a-110">Click Release.</span></span>
    * <span data-ttu-id="5f50a-111">Sellel lehel saate kinnitada tootmistellimuste valitud vahemiku väljastamise.</span><span class="sxs-lookup"><span data-stu-id="5f50a-111">On this page, you can confirm the release of the selected range of production orders.</span></span> <span data-ttu-id="5f50a-112">Kui soovite tellimusi lisada, klõpsake suvandit Vali.</span><span class="sxs-lookup"><span data-stu-id="5f50a-112">Click Select if you want to add orders.</span></span>  
    * <span data-ttu-id="5f50a-113">Etapp Väljastus näitab, millal tootmistellimus on tootmistöödesse väljastatud, nii et tööde operaatorid saavad tootmistööde edenemisest aru anda.</span><span class="sxs-lookup"><span data-stu-id="5f50a-113">The Release step indicates when the production order is released to the production shop floor so that the shop floor operators can report progress on the production jobs.</span></span> <span data-ttu-id="5f50a-114">Väljastada saab olulist tööde töötlemise teavet sisaldavaid tootmisdokumente.</span><span class="sxs-lookup"><span data-stu-id="5f50a-114">Production papers that contain relevant information about processing the jobs can be issued.</span></span> <span data-ttu-id="5f50a-115">Toormaterjalide komplekteerimise laotööd luuakse laoprotsessiks seadistatud kaupade puhul.</span><span class="sxs-lookup"><span data-stu-id="5f50a-115">The warehouse work for raw material picking is generated for the items that are set up for the warehouse process.</span></span>  
4. <span data-ttu-id="5f50a-116">Klõpsake vahekaarti Üldine.</span><span class="sxs-lookup"><span data-stu-id="5f50a-116">Click the General tab.</span></span>
    * <span data-ttu-id="5f50a-117">Valige, millised tootmisaruanded tuleks printida.</span><span class="sxs-lookup"><span data-stu-id="5f50a-117">Select which production reports should be printed.</span></span> <span data-ttu-id="5f50a-118">Töökaardi aruanne prindib iga plaanitud töö lehe ja nõuab tootmistellimuse plaanimist töö tasemel.</span><span class="sxs-lookup"><span data-stu-id="5f50a-118">The Job card report prints a page for each scheduled job and requires the production order to be scheduled at the job level.</span></span> <span data-ttu-id="5f50a-119">Aruanne sisaldab teavet plaanitud algus- ja lõppaja, toodetava koguse ja selle kohta, milline ressurss tööd töötleb.</span><span class="sxs-lookup"><span data-stu-id="5f50a-119">The report contains information about the scheduled start and end time, the quantity to produce, and which resource processes the job.</span></span> <span data-ttu-id="5f50a-120">Protsessi tööaruanne kogub sama teavet samale lehele, kuid ei prindi lehte iga töö puhul.</span><span class="sxs-lookup"><span data-stu-id="5f50a-120">The Route job report collects the same information on the same page, but does not print a page for each job.</span></span> <span data-ttu-id="5f50a-121">Protsessikaardi aruanne kuvab ainult toimingud, kuid mitte tööd.</span><span class="sxs-lookup"><span data-stu-id="5f50a-121">The Route card report only shows the operations but not the jobs.</span></span> <span data-ttu-id="5f50a-122">Seetõttu ei nõuta selles aruandes tööde plaanimist, kuid seda saab kasutada tootmistellimuste plaanimisel toimingu tasandil.</span><span class="sxs-lookup"><span data-stu-id="5f50a-122">Therefore, this report does not require job scheduling, but can be used when production orders are scheduled at the operation level.</span></span>  
5. <span data-ttu-id="5f50a-123">Märkige ruut Prindi protsessi kaart.</span><span class="sxs-lookup"><span data-stu-id="5f50a-123">Click the Print route card checkbox.</span></span>
6. <span data-ttu-id="5f50a-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5f50a-124">Click OK.</span></span>
7. <span data-ttu-id="5f50a-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5f50a-125">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]