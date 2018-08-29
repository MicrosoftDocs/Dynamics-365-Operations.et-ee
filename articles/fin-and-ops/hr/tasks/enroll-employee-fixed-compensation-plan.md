--- 
title: "Töötajate liitmine põhipalga plaaniga"
description: "Lisatasu ja eeliste haldur saab määrata töötajad põhipalga plaani nende põhipalga haldamiseks."
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: d84567f0d74b2ab0078eaeda622768e241332043
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---
# <a name="enroll-employees-in-a-fixed-compensation-plan"></a><span data-ttu-id="7a0b1-103">Töötajate liitmine põhipalga plaaniga</span><span class="sxs-lookup"><span data-stu-id="7a0b1-103">Enroll employees in a fixed compensation plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7a0b1-104">Lisatasu ja eeliste haldur saab määrata töötajad põhipalga plaani nende põhipalga haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-104">The compensation and benefits manager can assign employees to fixed compensation plans to manage their base pay.</span></span> <span data-ttu-id="7a0b1-105">See protseduur eeldab, et fikseeritud plaan on loodud ja aktiivne ning plaani sobivuse reeglid on seadistatud.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-105">This procedure assumes that a fixed plan has been created and is active, and that eligibility rules have been set for the plan.</span></span> <span data-ttu-id="7a0b1-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7a0b1-107">Protseduuri alustamiseks avage Inimressursid > Töötajad > Töötajad > Hüvitus > Fikseeritud plaan</span><span class="sxs-lookup"><span data-stu-id="7a0b1-107">To begin the procedure, go to Human resources > Workers > Employees > Compensation > Fixed plan</span></span>

1. <span data-ttu-id="7a0b1-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-108">Click New.</span></span>
2. <span data-ttu-id="7a0b1-109">Valige väljal Tegevus suvand Põhipalga tegevus tüübiga Palka/Palka uuesti, et kirjeldada muutust töötaja lisatasus.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-109">In the Action field, select a Fixed compensation action of type Hire/Rehire to describe the change in the employee's compensation.</span></span>
3. <span data-ttu-id="7a0b1-110">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7a0b1-111">Klõpsake väljal Ametikoht otsingu avamiseks rippmenüü nuppu.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-111">In the Position field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="7a0b1-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7a0b1-113">Kuvatav tase on ametikoha töö lisatasu tase.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-113">The level that's displayed is from the Compensation Level of the Job on the Position.</span></span> <span data-ttu-id="7a0b1-114">Tase tuleb tööle seadistada enne, kui töötajale saab lisatasu määrata.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-114">The level must be set on the Job before compensation can be assigned to the employee.</span></span>  
6. <span data-ttu-id="7a0b1-115">Valige väljal Plaan töötaja põhipalga plaan.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-115">In the Plan field, select the fixed compensation plan for the employee.</span></span> <span data-ttu-id="7a0b1-116">Plaani otsing on filtritud kuvama vaid plaane, millele töötajal on sobivuse reeglite põhjal õigus.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-116">The Plan lookup is filtered to show only the plans that the employee is eligible for based on the Eligibility rules.</span></span>
7. <span data-ttu-id="7a0b1-117">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7a0b1-118">Lisatasu jõustumis- ja aegumiskuupäevad tulenevad vaikimisi töötaja ametikoha määramise algus- ja lõppkuupäevadest.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-118">The Effective and Expiration dates for the compensation default from the start and end dates for the worker's position assignment.</span></span> <span data-ttu-id="7a0b1-119">Vajaduse korral saate neid kuupäevi muuta.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-119">You can adjust these dates as needed.</span></span>  
    * <span data-ttu-id="7a0b1-120">Kui Põhipalgaplaan on etapiplaan, valige etapp, mis sisaldab töötaja õiget palgamäära.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-120">If the Fixed compensation plan is a step plan, select the step containing the correct pay rate for the employee.</span></span> <span data-ttu-id="7a0b1-121">Kui põhipalgaplaan on taseme- või palgaastmiku plaan, sisestage töötaja palgamäär.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-121">If the fixed compensation plan is a grade or a band plan, enter the pay rate for the employee.</span></span> <span data-ttu-id="7a0b1-122">Palgamäära kontrollitakse plaani kõikumise sätetega ja töö lisatasu taseme minimaalsete ja maksimaalsete viitepunktidega.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-122">The pay rate will be validated against the tolerance settings for the plan, and the minimum and maximum reference points for the job's compensation level.</span></span>  
8. <span data-ttu-id="7a0b1-123">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7a0b1-123">Click OK.</span></span>


