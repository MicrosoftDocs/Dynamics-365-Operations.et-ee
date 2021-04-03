---
title: Töötajatele laenatud kaupade haldamine
description: Laenuartiklid on kirjed, mis aitavad juhtidel jälgida füüsilisi kaupu, mida ettevõte töötajatele laenab.
author: andreabichsel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 5517ee621f1c41b6348dc965e8846d677aa1bb56
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464810"
---
# <a name="manage-items-that-are-lent-to-workers"></a><span data-ttu-id="450f6-103">Töötajatele laenatud kaupade haldamine</span><span class="sxs-lookup"><span data-stu-id="450f6-103">Manage items that are lent to workers</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="450f6-104">Laenuartiklid on kirjed, mis aitavad juhtidel jälgida füüsilisi kaupu, mida ettevõte töötajatele laenab.</span><span class="sxs-lookup"><span data-stu-id="450f6-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="450f6-105">Järgmistes punktides on loetletud artiklite näited, mida ettevõte võib töötajatele laenata.</span><span class="sxs-lookup"><span data-stu-id="450f6-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="450f6-106">mobiiltelefonid,</span><span class="sxs-lookup"><span data-stu-id="450f6-106">Mobile telephones</span></span>
-   <span data-ttu-id="450f6-107">autod,</span><span class="sxs-lookup"><span data-stu-id="450f6-107">Automobiles</span></span>
-   <span data-ttu-id="450f6-108">Arvutiseadmed</span><span class="sxs-lookup"><span data-stu-id="450f6-108">Computer equipment</span></span>

<span data-ttu-id="450f6-109">Iga füüsiline kaup peab laenuartiklile vastama.</span><span class="sxs-lookup"><span data-stu-id="450f6-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="450f6-110">Iga laenuartikli kirje peaks kirjeldama, mida laenatakse, kes on laenu eest vastutav ja mitmeks päevaks võib artiklit töötajale laenata.</span><span class="sxs-lookup"><span data-stu-id="450f6-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="450f6-111">Saate luua kaupadele nagu võtmed, pääsukaardid või vormirõivad üheaegselt mitu laenuartiklit.</span><span class="sxs-lookup"><span data-stu-id="450f6-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="450f6-112">Artiklit laenates sisestage laenamise kuupäev ja plaanitav tagastamise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="450f6-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="450f6-113">Artikli tagastamisel sisestage tegelik tagastamise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="450f6-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="450f6-114">Töötajad saavad vaadata neile laenatud artiklite kirjeid, kasutades töötaja iseteeninduse tööruumi.</span><span class="sxs-lookup"><span data-stu-id="450f6-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="450f6-115">Nad saavad redigeerida ka olemasolevaid kirjeid või sisestada uusi laenuartikleid, kui nad on saanud veel füüsilisi kaupu.</span><span class="sxs-lookup"><span data-stu-id="450f6-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="450f6-116">Uute või olemasolevate laenuartiklite muudatuste suunamiseks läbi kinnitusprotsessi saab seadistada töövoo.</span><span class="sxs-lookup"><span data-stu-id="450f6-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="450f6-117">Juhatajad saavad vaadata oma otseste alluvate laenatud artikleid.</span><span class="sxs-lookup"><span data-stu-id="450f6-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="450f6-118">Neile saab anda ka õiguse oma töötajate nimel uusi laenuartikleid lisada.</span><span class="sxs-lookup"><span data-stu-id="450f6-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="450f6-119"> Kaotatud ja kadunud artiklite konto</span><span class="sxs-lookup"><span data-stu-id="450f6-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="450f6-120">Kui artikkel on kahjustatud või kadunud, sisestage fiktiivne tagastuskirje.</span><span class="sxs-lookup"><span data-stu-id="450f6-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="450f6-121">Seejärel kustutage artikkel või sälitage see ülevaates ja muutke kirjeldust, mis näitab, et artikkel pole saadaval.</span><span class="sxs-lookup"><span data-stu-id="450f6-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>


<a name="additional-resources"></a><span data-ttu-id="450f6-122">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="450f6-122">Additional resources</span></span>
--------

[<span data-ttu-id="450f6-123">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="450f6-123">Human resources</span></span>](index.md)





[!INCLUDE[footer-include](../includes/footer-banner.md)]