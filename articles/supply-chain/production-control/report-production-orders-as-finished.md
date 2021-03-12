---
title: Tootmistellimuste lõpetatuks kinnitamine
description: Lõpetatuks kinnitamine on tootmisetapp. Selles etapid kinnitatakse valmistoode ja see teisaldatakse tootmistellimusest varudesse.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: kamaybac
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f044b7640bda168485798316171fdd0b66c4c84
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986475"
---
# <a name="report-production-orders-as-finished"></a><span data-ttu-id="f037b-104">Tootmistellimuste lõpetatuks kinnitamine</span><span class="sxs-lookup"><span data-stu-id="f037b-104">Report production orders as finished</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f037b-105">Lõpetatuks kinnitamine on tootmisetapp.</span><span class="sxs-lookup"><span data-stu-id="f037b-105">Report as finished is a production stage.</span></span> <span data-ttu-id="f037b-106">Selles etapid kinnitatakse valmistoode ja see teisaldatakse tootmistellimusest varudesse.</span><span class="sxs-lookup"><span data-stu-id="f037b-106">At this stage, a finished product is reported and moved from the production order to the inventory.</span></span>

<span data-ttu-id="f037b-107">Kui lõpetatud kaupade kogus on kinnitatud tootmistellimusel lõpetatuks, uuendatakse see varudes laoseisuna.</span><span class="sxs-lookup"><span data-stu-id="f037b-107">When a quantity of the finished goods is reported as finished on a production order it is updated as on-hand in the inventory.</span></span> <span data-ttu-id="f037b-108">Algselt plaanitud tellimuse koguse osalised kogused saab kinnitada lõpetatuks.</span><span class="sxs-lookup"><span data-stu-id="f037b-108">Partial quantities of the originally planned order quantity can be reported as finished.</span></span> <span data-ttu-id="f037b-109">Samuti on võimalik kinnitada vigased kogused koos seostatud vea põhjusega, kui koguste lõpetamist kinnitatakse.</span><span class="sxs-lookup"><span data-stu-id="f037b-109">It is also possible to report error quantities with an associated error reason when reporting quantities as finished.</span></span> <span data-ttu-id="f037b-110">Kui tootmistellimus jõuab etappi Lõpetamine kinnitatud, näitab see, et tootmistellimuses rohkem koguseid ei kinnitata.</span><span class="sxs-lookup"><span data-stu-id="f037b-110">When the production order reach the stage Reported as finished it indicates that no more quantity is going to be reported at the production  order.</span></span>
<span data-ttu-id="f037b-111">Järgmised omadused seostatakse ka protsessiga **Kinnita lõpetamine**.</span><span class="sxs-lookup"><span data-stu-id="f037b-111">The following characteristics are also associated with the **Report as finished** process:</span></span>
-   <span data-ttu-id="f037b-112">On võimalik seadistada toormaterjali tarbimine ja kinnitatud kogusega proportsionaalne aeg (tagantjärele)</span><span class="sxs-lookup"><span data-stu-id="f037b-112">It is possible to set up consumption of raw material and time that are proportional to the reported quantity (back-flushing)</span></span>
-   <span data-ttu-id="f037b-113">Laoprotsessideks lubatud kaupadele saab luua ladustamistöö.</span><span class="sxs-lookup"><span data-stu-id="f037b-113">Put-away work can be generated for items that are enabled for warehouse processes.</span></span>
-   <span data-ttu-id="f037b-114">Saab seadistada, et pearaamatukontodele teatatakse lõpetatud kaupade plaanitud või standardne kuluväärtus.</span><span class="sxs-lookup"><span data-stu-id="f037b-114">The planned or standard cost value of the finished goods can be set up to be reported to ledger accounts.</span></span>
-   <span data-ttu-id="f037b-115">Kinnitatud kogusele saab luua kvaliteettellimuse kvaliteediseose seadistuse alusel.</span><span class="sxs-lookup"><span data-stu-id="f037b-115">A quality order can be created for the reported quantity based on the setup of a quality association.</span></span>

<span data-ttu-id="f037b-116">Kogus kinnitatakse väljastuskohta.</span><span class="sxs-lookup"><span data-stu-id="f037b-116">The quantity is reported to the output location.</span></span> <span data-ttu-id="f037b-117">Seejärel luuakse laotöö, et teisaldada kogus väljastuskohast selle lõppsihtkohta, mille määratleb ladustamistöö asukoha korraldus.</span><span class="sxs-lookup"><span data-stu-id="f037b-117">Warehouse work is then generated to move the quantity from the output location to its final destination defined by the location directive for the put-away work.</span></span>

-   <span data-ttu-id="f037b-118">Kvaliteettellimuse saab luua, kui tootmistellimuse kinnitatakse lõpetatuks, kui kvaliteediseos on seadistatud.</span><span class="sxs-lookup"><span data-stu-id="f037b-118">A quality order can be created when a production order is reported as finished if a quality association has been set up.</span></span>

## <a name="set-a-production-order-to-reporting-as-finished"></a><span data-ttu-id="f037b-119">Tootmistellimuse lõpetatuks kinnitamise määramine</span><span class="sxs-lookup"><span data-stu-id="f037b-119">Set a production order to Reporting as finished</span></span>
<span data-ttu-id="f037b-120">Saate määrata tootmistellimuse väärtuseks **Kinnita lõpetamine** standardse tootmistellimuse värskendamisfunktsiooni kaudu või protsessikaardi ja töökaardi töölehtede kaudu või töölehe **Kinnita lõpetamine** kaudu.</span><span class="sxs-lookup"><span data-stu-id="f037b-120">You can set a production order to **Report as finished** through the standard production order update function, or through the route and job card journals, or through the journal **Report as finished**.</span></span> <span data-ttu-id="f037b-121">Saate oleku värskendada ka väärtusele **Kinnita lõpetamine** töökaardi terminali ja töökaardi seadme lehtede kaudu, kui kinnitate tootmistellimuse viimase töö.</span><span class="sxs-lookup"><span data-stu-id="f037b-121">You can also update the stage to **Report as finished** through the job card terminal and job card device pages, when you report on the last job of the production order.</span></span> <span data-ttu-id="f037b-122">Lõpuks saate lubada suvandi **Kinnita lõpetamine** kaasaskantava laoseadme lahenduse protsessina.</span><span class="sxs-lookup"><span data-stu-id="f037b-122">Finally, you can enable the **Report as finished** option as a process for the handheld warehouse device solution.</span></span>  



