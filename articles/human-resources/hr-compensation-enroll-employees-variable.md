---
title: Töötaja liitmine tulemustasu plaaniga
description: Lisatasu ja soodustuste haldur saab lisada töötajaid ergutussüsteemi plaanidesse töötajate rahaliste ja mitterahaliste preemiate arvutamiseks.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompVarEnrollEmpl
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2e591f471036c4b7f314155f1b56e87094ef1031
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008754"
---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a><span data-ttu-id="17747-103">Töötaja liitmine tulemustasu plaaniga</span><span class="sxs-lookup"><span data-stu-id="17747-103">Enroll an employee in a variable compensation plan</span></span>

<span data-ttu-id="17747-104">Lisatasu ja soodustuste haldur saab lisada töötajaid ergutussüsteemi plaanidesse töötajate rahaliste ja mitterahaliste preemiate arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="17747-104">The Compensation and Benefits manager can enroll employees in variable compensation plans to calculate cash and non-cash awards for employees.</span></span> <span data-ttu-id="17747-105">See protseduur eeldab, et ergutussüsteemi plaan on loodud nii, et väli Võimalda registreerimine on seatud suvandile Jah ja sobivuse reeglid on selle ergutussüsteemi plaani puhul loodud.</span><span class="sxs-lookup"><span data-stu-id="17747-105">This procedure assumes that a variable compensation plan has been created with the Enable enrolment field set to Yes, and that eligibility rules have been created for that variable compensation plan.</span></span> <span data-ttu-id="17747-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="17747-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="17747-107">Selle protseduuri alustamiseks avage Personaliarvestus > Töötajad > Töötajad > Hüvitus > Muutuva plaaniga registreerimine</span><span class="sxs-lookup"><span data-stu-id="17747-107">To begin this procedure, go to Human resources > Workers > Employees > Compensation > Variable plan enrolment</span></span>

1. <span data-ttu-id="17747-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="17747-108">Click New.</span></span>
2. <span data-ttu-id="17747-109">Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="17747-109">In the Plan field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="17747-110">Plaani otsing filtritakse kuvama vaid ergutussüsteemi plaane, millele töötajal on sobivuse reeglite põhjal õigus.</span><span class="sxs-lookup"><span data-stu-id="17747-110">The plan lookup will be filtered to only show the variable compensation plans that the employee is eligible for based on the eligibility rules.</span></span>  
3. <span data-ttu-id="17747-111">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="17747-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="17747-112">Lülitage jaotise Üldine laiendamist.</span><span class="sxs-lookup"><span data-stu-id="17747-112">Toggle the expansion of the General section.</span></span>
5. <span data-ttu-id="17747-113">Sisestage kuupäev väljale Jõustumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="17747-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="17747-114">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="17747-114">Click Save.</span></span>
7. <span data-ttu-id="17747-115">Lülitage jaotise Erandid laiendamist.</span><span class="sxs-lookup"><span data-stu-id="17747-115">Toggle the expansion of the Overrides section.</span></span>
    * <span data-ttu-id="17747-116">Lisaks on võimalik seadistada reegli kuupäeva töötaja palkamise kuupäeva alistamiseks, kui valitud muutuva plaani puhul määratud palkamise reegliks on Protsent.</span><span class="sxs-lookup"><span data-stu-id="17747-116">Optionally, a hire rule date can be set to override the hire date for an employee when the hire rule specified for the selected variable plan is Percent.</span></span>  
    * <span data-ttu-id="17747-117">Kui muutuv plaan on põhiplaani protsent, saab preemia protsendi töötaja puhul alistada.</span><span class="sxs-lookup"><span data-stu-id="17747-117">If the variable plan is a percent of basis plan, the award percentage can be overridden for the employee.</span></span> <span data-ttu-id="17747-118">Kui ergutussüsteemi plaan on ühikute arvu plaan, saab ühikute arvu töötaja puhul alistada.</span><span class="sxs-lookup"><span data-stu-id="17747-118">If the variable compensation plan is a number of units plan, the number of units can be overridden for the employee.</span></span>  
    * <span data-ttu-id="17747-119">Kui töötajale tuleks preemiaks anda kindel summa, saate selle määrata siin.</span><span class="sxs-lookup"><span data-stu-id="17747-119">If the employee should be given a flat amount for their award, the amount can be set here.</span></span>  
8. <span data-ttu-id="17747-120">Laiendage jaotise Organisatoorsed erandid laiendamist.</span><span class="sxs-lookup"><span data-stu-id="17747-120">Toggle the expansion of the Organizational overrides section.</span></span>
    * <span data-ttu-id="17747-121">Kui arvestada tuleks töötaja jõudlust, eri osakondade või muu kui töötaja ametikohas määratud osakonna jõudlust, saab osakonna alistada.</span><span class="sxs-lookup"><span data-stu-id="17747-121">If the employee's performance should take into consideration, the performance of different departments, or a department other than the one assigned on the employee's position, the department can be overridden.</span></span> <span data-ttu-id="17747-122">Protsendi veeru kogusummaks peab olema 100.</span><span class="sxs-lookup"><span data-stu-id="17747-122">The Percent column should total 100.</span></span>  
