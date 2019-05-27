---
title: Sisestamine tuletatud raamatute kaudu
description: Selles artiklis kirjeldatakse tuletatud raamatute kasutamist.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ff1dbf67a53a5639e448da707898b55cd00cba94
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546866"
---
# <a name="post-with-derived-books"></a><span data-ttu-id="cac15-103">Sisestamine tuletatud raamatute kaudu</span><span class="sxs-lookup"><span data-stu-id="cac15-103">Post with derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cac15-104">Selles artiklis kirjeldatakse tuletatud raamatute kasutamist.</span><span class="sxs-lookup"><span data-stu-id="cac15-104">This article describes how to use derived books.</span></span>

<span data-ttu-id="cac15-105">Kui sisestate tuletatud raamatuid sisaldava raamatu kandeid, sisestatakse tuletatud raamatu kanded töölehtedele, ostutellimustele või vabas vormis arvetele automaatselt.</span><span class="sxs-lookup"><span data-stu-id="cac15-105">When you post transactions for a book that contains derived books, the derived book transactions are posted automatically in journals, purchase orders, or free text invoices.</span></span> <span data-ttu-id="cac15-106">Kui aga valmistate põhivara töölehele sisestamiseks ette esmase raamatu kandeid, saate enne sisestamist vaadata ja muuta ka tuletatud kannete summasid.</span><span class="sxs-lookup"><span data-stu-id="cac15-106">However, if you prepare the primary book transactions in the Fixed assets journal, you can view and modify the amounts of the derived transactions before you post them.</span></span>
-   <span data-ttu-id="cac15-107">Kindlaid kontosid, nagu käibemaksu- või kliendi- ja hankijakontod, värskendatakse esmase raamatu sisestamisel vaid üks kord.</span><span class="sxs-lookup"><span data-stu-id="cac15-107">Certain accounts, such as sales tax and customer or vendor accounts, are updated only once by postings of the primary book.</span></span> <span data-ttu-id="cac15-108">Tuletatud raamatu kanded sisestatakse neile kontodele, mis on lehel Põhivara sisestusreeglid tuletatud raamatu jaoks määratletud.</span><span class="sxs-lookup"><span data-stu-id="cac15-108">The derived book transactions are posted to the accounts that have been defined for the derived book in the Fixed asset posting profiles page.</span></span>
-   <span data-ttu-id="cac15-109">Tuletatud raamatute puhul on kande tüüp sageli Soetamine.</span><span class="sxs-lookup"><span data-stu-id="cac15-109">Acquisition is often used as the transaction type for the derived books.</span></span> <span data-ttu-id="cac15-110">Kasutage seda varianti, kui see raamat ja tuletatud raamat määratakse põhivarale alates selle soetusest.</span><span class="sxs-lookup"><span data-stu-id="cac15-110">You use this when the book and the derived book should be applied to the fixed asset from the time of the acquisition of the fixed asset.</span></span>
-   <span data-ttu-id="cac15-111">Kande tüüp võib olla ka muu väärtusega.</span><span class="sxs-lookup"><span data-stu-id="cac15-111">Other values for the transaction type can also apply.</span></span> <span data-ttu-id="cac15-112">Näiteks kui esmasel raamatul ja tuletatud raamatul on samad müügi- ja likvideerimisintervallid, saab tuletatud raamatu seadistamisel kasutada kõiki põhivara kandetüüpe.</span><span class="sxs-lookup"><span data-stu-id="cac15-112">For example, if the primary book and the derived books have the same intervals regarding sale or disposal, all fixed asset transaction types are available for the setup of a derived book.</span></span>

> [!WARNING]
> <span data-ttu-id="cac15-113">Tuletatud raamatusse sisestatava kulumi summa on sama, mis sisestati esmase raamatu puhul.</span><span class="sxs-lookup"><span data-stu-id="cac15-113">Depreciation posted in the derived book will be the same amount as was posted for the primary book.</span></span> <span data-ttu-id="cac15-114">Kui raamatute puhul kasutatakse erinevaid kulumiarvestuse meetodeid, ei tohi kulumikandeid tuletatud protsessi abil luua.</span><span class="sxs-lookup"><span data-stu-id="cac15-114">If the depreciation methods are different between the books, you should not generate depreciation transactions using the derived process.</span></span> |

## <a name="example"></a><span data-ttu-id="cac15-115">Näide</span><span class="sxs-lookup"><span data-stu-id="cac15-115">Example</span></span> 
<span data-ttu-id="cac15-116">Järgmine teave kirjeldab, kuidas seadistada tuletatud raamatu funktsiooni abil soetamiskandeid.</span><span class="sxs-lookup"><span data-stu-id="cac15-116">The following information describes how to set up acquisition transactions with the derived book functionality.</span></span>

1.  <span data-ttu-id="cac15-117">Looge raamatud lehel Raamatud.</span><span class="sxs-lookup"><span data-stu-id="cac15-117">Create the books on the Books page.</span></span>
    -   <span data-ttu-id="cac15-118">Raamatupidamise raamat: VM 1, praegune sisestuskiht</span><span class="sxs-lookup"><span data-stu-id="cac15-118">The book for accounting: VM 1, Current posting layer</span></span>
    -   <span data-ttu-id="cac15-119">Maksu raamat: VM 2, maksu sisestuskiht</span><span class="sxs-lookup"><span data-stu-id="cac15-119">The book for tax purposes: VM 2, Tax posting layer</span></span>

2.  <span data-ttu-id="cac15-120">Klõpsake jaotises VM 1 vahekaarti Tuletatud raamatud. Valige väljal Raamat suvand VM 2 ja väljal Kande tüüp suvand Soetamine.</span><span class="sxs-lookup"><span data-stu-id="cac15-120">On VM 1, click the Derived books tab. Select VM 2 in the Book field, and Acquisition in the Transaction type field.</span></span>

<span data-ttu-id="cac15-121">Seejärel saab raamatud kindlate põhivaradega siduda.</span><span class="sxs-lookup"><span data-stu-id="cac15-121">The books then can be attached to specific fixed assets.</span></span> 

<span data-ttu-id="cac15-122">Raamatuga VM 1 põhivara soetamise sisestamisel sisestatakse see mitte ainult raamatusse VM 1, vaid ka tuletatud raamatusse VM 2.</span><span class="sxs-lookup"><span data-stu-id="cac15-122">When an acquisition is posted for a fixed asset with book VM 1, the acquisition is posted not only on VM 1, but also on the derived book VM 2.</span></span> <span data-ttu-id="cac15-123">Mõlema põhivara raamatu olekuks muutub Avatud.</span><span class="sxs-lookup"><span data-stu-id="cac15-123">The status of both fixed asset books is updated to Open.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="cac15-124">Kui te tuletatud raamatuid ei kasuta, tuleb teil soetamine sisestada nii raamatu VM 1 kui raamatu VM 2 kohta.</span><span class="sxs-lookup"><span data-stu-id="cac15-124">If you do not use derived books, you must post the acquisition of the fixed asset both for book VM 1 and book VM 2.</span></span>

<span data-ttu-id="cac15-125">Lisateavet vt teemast [Tuletatud raamatud](derived-books.md)</span><span class="sxs-lookup"><span data-stu-id="cac15-125">For more information, see [Derived books](derived-books.md)</span></span>



