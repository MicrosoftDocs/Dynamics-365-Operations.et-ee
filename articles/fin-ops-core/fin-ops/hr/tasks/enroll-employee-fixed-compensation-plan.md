---
title: Töötaja liitmine fikseeritud hüvitusplaaniga
description: Lisatasu ja eeliste haldur saab määrata töötajad põhipalga plaani nende põhipalga haldamiseks.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee0ba197ee47d2a2da2372b12291e5625ddc9ba1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190507"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a><span data-ttu-id="3f920-103">Töötaja liitmine fikseeritud hüvitusplaaniga</span><span class="sxs-lookup"><span data-stu-id="3f920-103">Enroll an employee in a fixed compensation plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3f920-104">Lisatasu ja eeliste haldur saab määrata töötajad põhipalga plaani nende põhipalga haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="3f920-104">The compensation and benefits manager can assign employees to fixed compensation plans to manage their base pay.</span></span> <span data-ttu-id="3f920-105">See protseduur eeldab, et fikseeritud plaan on loodud ja aktiivne ning plaani sobivuse reeglid on seadistatud.</span><span class="sxs-lookup"><span data-stu-id="3f920-105">This procedure assumes that a fixed plan has been created and is active, and that eligibility rules have been set for the plan.</span></span> <span data-ttu-id="3f920-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="3f920-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3f920-107">Protseduuri alustamiseks avage Inimressursid > Töötajad > Töötajad > Hüvitus > Fikseeritud plaan</span><span class="sxs-lookup"><span data-stu-id="3f920-107">To begin the procedure, go to Human resources > Workers > Employees > Compensation > Fixed plan</span></span>

1. <span data-ttu-id="3f920-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="3f920-108">Click New.</span></span>
2. <span data-ttu-id="3f920-109">Valige väljal Tegevus suvand Põhipalga tegevus tüübiga Palka/Palka uuesti, et kirjeldada muutust töötaja lisatasus.</span><span class="sxs-lookup"><span data-stu-id="3f920-109">In the Action field, select a Fixed compensation action of type Hire/Rehire to describe the change in the employee's compensation.</span></span>
3. <span data-ttu-id="3f920-110">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="3f920-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3f920-111">Klõpsake väljal Ametikoht otsingu avamiseks rippmenüü nuppu.</span><span class="sxs-lookup"><span data-stu-id="3f920-111">In the Position field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="3f920-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="3f920-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3f920-113">Kuvatav tase on ametikoha töö lisatasu tase.</span><span class="sxs-lookup"><span data-stu-id="3f920-113">The level that's displayed is from the Compensation Level of the Job on the Position.</span></span> <span data-ttu-id="3f920-114">Tase tuleb tööle seadistada enne, kui töötajale saab lisatasu määrata.</span><span class="sxs-lookup"><span data-stu-id="3f920-114">The level must be set on the Job before compensation can be assigned to the employee.</span></span>  
6. <span data-ttu-id="3f920-115">Valige väljal Plaan töötaja põhipalga plaan.</span><span class="sxs-lookup"><span data-stu-id="3f920-115">In the Plan field, select the fixed compensation plan for the employee.</span></span> <span data-ttu-id="3f920-116">Plaani otsing on filtritud kuvama vaid plaane, millele töötajal on sobivuse reeglite põhjal õigus.</span><span class="sxs-lookup"><span data-stu-id="3f920-116">The Plan lookup is filtered to show only the plans that the employee is eligible for based on the Eligibility rules.</span></span>
7. <span data-ttu-id="3f920-117">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="3f920-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3f920-118">Lisatasu jõustumis- ja aegumiskuupäevad tulenevad vaikimisi töötaja ametikoha määramise algus- ja lõppkuupäevadest.</span><span class="sxs-lookup"><span data-stu-id="3f920-118">The Effective and Expiration dates for the compensation default from the start and end dates for the worker's position assignment.</span></span> <span data-ttu-id="3f920-119">Vajaduse korral saate neid kuupäevi muuta.</span><span class="sxs-lookup"><span data-stu-id="3f920-119">You can adjust these dates as needed.</span></span>  
    * <span data-ttu-id="3f920-120">Kui Põhipalgaplaan on etapiplaan, valige etapp, mis sisaldab töötaja õiget palgamäära.</span><span class="sxs-lookup"><span data-stu-id="3f920-120">If the Fixed compensation plan is a step plan, select the step containing the correct pay rate for the employee.</span></span> <span data-ttu-id="3f920-121">Kui põhipalgaplaan on taseme- või palgaastmiku plaan, sisestage töötaja palgamäär.</span><span class="sxs-lookup"><span data-stu-id="3f920-121">If the fixed compensation plan is a grade or a band plan, enter the pay rate for the employee.</span></span> <span data-ttu-id="3f920-122">Palgamäära kontrollitakse plaani kõikumise sätetega ja töö lisatasu taseme minimaalsete ja maksimaalsete viitepunktidega.</span><span class="sxs-lookup"><span data-stu-id="3f920-122">The pay rate will be validated against the tolerance settings for the plan, and the minimum and maximum reference points for the job's compensation level.</span></span>  
8. <span data-ttu-id="3f920-123">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3f920-123">Click OK.</span></span>

