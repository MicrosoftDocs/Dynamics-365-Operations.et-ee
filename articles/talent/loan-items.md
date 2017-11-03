---
title: "Töötajatele laenatud artiklite haldamine"
description: "Laenuartiklid on kirjed, mis aitavad juhtidel jälgida füüsilisi kaupu, mida ettevõte töötajatele laenab."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e7b29b1cca0b61f295449045a2d4e38abacf05b5
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="manage-items-lent-to-workers"></a><span data-ttu-id="eb741-103">Töötajatele laenatud artiklite haldamine</span><span class="sxs-lookup"><span data-stu-id="eb741-103">Manage items lent to workers</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="eb741-104">Laenuartiklid on kirjed, mis aitavad juhtidel jälgida füüsilisi kaupu, mida ettevõte töötajatele laenab.</span><span class="sxs-lookup"><span data-stu-id="eb741-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="eb741-105">Järgmistes punktides on loetletud artiklite näited, mida ettevõte võib töötajatele laenata.</span><span class="sxs-lookup"><span data-stu-id="eb741-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="eb741-106">mobiiltelefonid,</span><span class="sxs-lookup"><span data-stu-id="eb741-106">Mobile telephones</span></span>
-   <span data-ttu-id="eb741-107">autod,</span><span class="sxs-lookup"><span data-stu-id="eb741-107">Automobiles</span></span>
-   <span data-ttu-id="eb741-108">Arvutiseadmed</span><span class="sxs-lookup"><span data-stu-id="eb741-108">Computer equipment</span></span>

<span data-ttu-id="eb741-109">Iga füüsiline kaup peab laenuartiklile vastama.</span><span class="sxs-lookup"><span data-stu-id="eb741-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="eb741-110">Iga laenuartikli kirje peaks kirjeldama, mida laenatakse, kes on laenu eest vastutav ja mitmeks päevaks võib artiklit töötajale laenata.</span><span class="sxs-lookup"><span data-stu-id="eb741-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="eb741-111">Saate luua kaupadele nagu võtmed, pääsukaardid või vormirõivad üheaegselt mitu laenuartiklit.</span><span class="sxs-lookup"><span data-stu-id="eb741-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="eb741-112">Artiklit laenates sisestage laenamise kuupäev ja plaanitav tagastamise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="eb741-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="eb741-113">Artikli tagastamisel sisestage tegelik tagastamise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="eb741-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="eb741-114">Töötajad saavad vaadata neile laenatud artiklite kirjeid, kasutades töötaja iseteeninduse tööruumi.</span><span class="sxs-lookup"><span data-stu-id="eb741-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="eb741-115">Nad saavad redigeerida ka olemasolevaid kirjeid või sisestada uusi laenuartikleid, kui nad on saanud veel füüsilisi kaupu.</span><span class="sxs-lookup"><span data-stu-id="eb741-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="eb741-116">Uute või olemasolevate laenuartiklite muudatuste suunamiseks läbi kinnitusprotsessi saab seadistada töövoo.</span><span class="sxs-lookup"><span data-stu-id="eb741-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="eb741-117">Juhatajad saavad vaadata oma otseste alluvate laenatud artikleid.</span><span class="sxs-lookup"><span data-stu-id="eb741-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="eb741-118">Neile saab anda ka õiguse oma töötajate nimel uusi laenuartikleid lisada.</span><span class="sxs-lookup"><span data-stu-id="eb741-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="eb741-119"> Kaotatud ja kadunud artiklite konto</span><span class="sxs-lookup"><span data-stu-id="eb741-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="eb741-120">Kui artikkel on kahjustatud või kadunud, sisestage fiktiivne tagastuskirje.</span><span class="sxs-lookup"><span data-stu-id="eb741-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="eb741-121">Seejärel kustutage artikkel või sälitage see ülevaates ja muutke kirjeldust, mis näitab, et artikkel pole saadaval.</span><span class="sxs-lookup"><span data-stu-id="eb741-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>

 
<a name="see-also"></a><span data-ttu-id="eb741-122">Vt ka</span><span class="sxs-lookup"><span data-stu-id="eb741-122">See also</span></span>
--------

[<span data-ttu-id="eb741-123">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="eb741-123">Human resources</span></span>](index.md)




