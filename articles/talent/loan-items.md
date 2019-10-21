---
title: Töötajatele laenatud kaupade haldamine
description: Laenuartiklid on kirjed, mis aitavad juhtidel jälgida füüsilisi kaupu, mida ettevõte töötajatele laenab.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 73ffe05d8c869418f7601025e8ce19e1b05c952f
ms.sourcegitcommit: 0dd8d0510214f92936a9dd214b404c5c8103587b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2419242"
---
# <a name="manage-items-that-are-lent-to-workers"></a><span data-ttu-id="c24a7-103">Töötajatele laenatud kaupade haldamine</span><span class="sxs-lookup"><span data-stu-id="c24a7-103">Manage items that are lent to workers</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c24a7-104">Laenuartiklid on kirjed, mis aitavad juhtidel jälgida füüsilisi kaupu, mida ettevõte töötajatele laenab.</span><span class="sxs-lookup"><span data-stu-id="c24a7-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="c24a7-105">Järgmistes punktides on loetletud artiklite näited, mida ettevõte võib töötajatele laenata.</span><span class="sxs-lookup"><span data-stu-id="c24a7-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="c24a7-106">mobiiltelefonid,</span><span class="sxs-lookup"><span data-stu-id="c24a7-106">Mobile telephones</span></span>
-   <span data-ttu-id="c24a7-107">autod,</span><span class="sxs-lookup"><span data-stu-id="c24a7-107">Automobiles</span></span>
-   <span data-ttu-id="c24a7-108">Arvutiseadmed</span><span class="sxs-lookup"><span data-stu-id="c24a7-108">Computer equipment</span></span>

<span data-ttu-id="c24a7-109">Iga füüsiline kaup peab laenuartiklile vastama.</span><span class="sxs-lookup"><span data-stu-id="c24a7-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="c24a7-110">Iga laenuartikli kirje peaks kirjeldama, mida laenatakse, kes on laenu eest vastutav ja mitmeks päevaks võib artiklit töötajale laenata.</span><span class="sxs-lookup"><span data-stu-id="c24a7-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="c24a7-111">Saate luua kaupadele nagu võtmed, pääsukaardid või vormirõivad üheaegselt mitu laenuartiklit.</span><span class="sxs-lookup"><span data-stu-id="c24a7-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="c24a7-112">Artiklit laenates sisestage laenamise kuupäev ja plaanitav tagastamise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="c24a7-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="c24a7-113">Artikli tagastamisel sisestage tegelik tagastamise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="c24a7-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="c24a7-114">Töötajad saavad vaadata neile laenatud artiklite kirjeid, kasutades töötaja iseteeninduse tööruumi.</span><span class="sxs-lookup"><span data-stu-id="c24a7-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="c24a7-115">Nad saavad redigeerida ka olemasolevaid kirjeid või sisestada uusi laenuartikleid, kui nad on saanud veel füüsilisi kaupu.</span><span class="sxs-lookup"><span data-stu-id="c24a7-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="c24a7-116">Uute või olemasolevate laenuartiklite muudatuste suunamiseks läbi kinnitusprotsessi saab seadistada töövoo.</span><span class="sxs-lookup"><span data-stu-id="c24a7-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="c24a7-117">Juhatajad saavad vaadata oma otseste alluvate laenatud artikleid.</span><span class="sxs-lookup"><span data-stu-id="c24a7-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="c24a7-118">Neile saab anda ka õiguse oma töötajate nimel uusi laenuartikleid lisada.</span><span class="sxs-lookup"><span data-stu-id="c24a7-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="c24a7-119"> Kaotatud ja kadunud artiklite konto</span><span class="sxs-lookup"><span data-stu-id="c24a7-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="c24a7-120">Kui artikkel on kahjustatud või kadunud, sisestage fiktiivne tagastuskirje.</span><span class="sxs-lookup"><span data-stu-id="c24a7-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="c24a7-121">Seejärel kustutage artikkel või sälitage see ülevaates ja muutke kirjeldust, mis näitab, et artikkel pole saadaval.</span><span class="sxs-lookup"><span data-stu-id="c24a7-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>


<a name="additional-resources"></a><span data-ttu-id="c24a7-122">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c24a7-122">Additional resources</span></span>
--------

[<span data-ttu-id="c24a7-123">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="c24a7-123">Human resources</span></span>](index.yml)



