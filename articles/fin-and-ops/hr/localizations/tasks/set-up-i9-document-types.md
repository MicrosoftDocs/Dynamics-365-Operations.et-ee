--- 
title: "I-9 dokumenditüüpide seadistamine"
description: "See protseduur näitab, kuidas saate vaadata ja seadistada I-9 kontrollimiseks kasutatavaid dokumenditüüpe."
author: ShielaSogge
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a05fec7b79003d5b98470d85644d70bd1dbac285
ms.openlocfilehash: d3d2f38327ea82ecddf998161edf86bf32e04db0
ms.contentlocale: et-ee
ms.lasthandoff: 02/06/2018

---
# <a name="set-up-i-9-document-types"></a><span data-ttu-id="94474-103">I-9 dokumenditüüpide seadistamine</span><span class="sxs-lookup"><span data-stu-id="94474-103">Set up I-9 document types</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="94474-104">See protseduur näitab, kuidas saate vaadata ja seadistada I-9 kontrollimiseks kasutatavaid dokumenditüüpe.</span><span class="sxs-lookup"><span data-stu-id="94474-104">This procedure shows how to view and set up document types that are used for I-9 verification.</span></span> <span data-ttu-id="94474-105">Enne I-9 dokumenditüüpide seadistamist peate seadistama ka väljastavad asutused ja tuvastustüübid.</span><span class="sxs-lookup"><span data-stu-id="94474-105">Before you set up I-9 document types, you must also set up the issuing agencies and identification types.</span></span> <span data-ttu-id="94474-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF andmeid, mis hõlmab näiteid protseduuri lõpetamiseks vajalikest väljastavatest asutustest ja tuvastustüüpidest.</span><span class="sxs-lookup"><span data-stu-id="94474-106">The demo data company used to create this procedure is USMF, which includes examples of the issue agencies and identification types that are needed to complete the procedure.</span></span>

1. <span data-ttu-id="94474-107">Avage Personaliarvestus > Töötajad > I-9 > I-9 dokumenditüübid.</span><span class="sxs-lookup"><span data-stu-id="94474-107">Go to Human resources > Workers > I-9 > I-9 document types.</span></span>
2. <span data-ttu-id="94474-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="94474-108">Click New.</span></span>
3. <span data-ttu-id="94474-109">Sisestage väärtus väljale I-9 dokumenditüüp.</span><span class="sxs-lookup"><span data-stu-id="94474-109">In the I-9 document type field, type a value.</span></span>
    * <span data-ttu-id="94474-110">Näide: kooli ID.</span><span class="sxs-lookup"><span data-stu-id="94474-110">Example: School ID.</span></span>  
4. <span data-ttu-id="94474-111">Valige ID tüüp.</span><span class="sxs-lookup"><span data-stu-id="94474-111">Select the identification type.</span></span>  <span data-ttu-id="94474-112">Näide: kooli ID.</span><span class="sxs-lookup"><span data-stu-id="94474-112">Example:  School ID</span></span>
    * <span data-ttu-id="94474-113">Tuvastustüüpide näideteks on isikukood (SSN), viisa number, passi ID või juhiluba.</span><span class="sxs-lookup"><span data-stu-id="94474-113">Examples of identification types include a Social Security number (SSN), visa number, passport ID, or driver's license.</span></span>  
5. <span data-ttu-id="94474-114">Valige dokumenditüübi puhul kasutatav I-9 dokumendiloend.</span><span class="sxs-lookup"><span data-stu-id="94474-114">Select the I-9 document list that is used for the document type.</span></span>
    * <span data-ttu-id="94474-115">I-9 protsessi osana peavad töötajad esitama dokumente, mis näitavad tööandjale nende identiteeti ja tööluba.</span><span class="sxs-lookup"><span data-stu-id="94474-115">As part of the I-9 process, employees must present documentation that shows the employer their identity and employment authorization.</span></span> <span data-ttu-id="94474-116">USA Kodakondsus- ja immigratsiooniteenuste veebisait sisaldab teavet selle kohta, millised dokumendid on vastuvõetavad ja millisesse loendisse need kuuluvad.</span><span class="sxs-lookup"><span data-stu-id="94474-116">The US Citizenship and Immigration Services website contains information about which documents are acceptable, and which list they belong to.</span></span>  <span data-ttu-id="94474-117">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="94474-117">http://www.uscis.gov</span></span>  
6. <span data-ttu-id="94474-118">Sisestage dokumendi tüübi ametlik vormi number väljale Vorm.</span><span class="sxs-lookup"><span data-stu-id="94474-118">In the Form field, Enter the official form number for the document type.</span></span> <span data-ttu-id="94474-119">Näide: kooli ID.</span><span class="sxs-lookup"><span data-stu-id="94474-119">Example: School ID.</span></span>
    * <span data-ttu-id="94474-120">Ametlikud vormi numbrid leiate USA Kodakondsus- ja immigratsiooniteenuste veebisaidilt.</span><span class="sxs-lookup"><span data-stu-id="94474-120">The official form numbers can be found on the US Citizenship and Immigration Services website.</span></span>  <span data-ttu-id="94474-121">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="94474-121">http://www.uscis.gov</span></span>  
7. <span data-ttu-id="94474-122">Märkige või tühjendage ruut Aktiivne.</span><span class="sxs-lookup"><span data-stu-id="94474-122">Check or uncheck the Active checkbox.</span></span>
8. <span data-ttu-id="94474-123">Määrake väljal Aegumine kuupäevaks 27.10.2019.</span><span class="sxs-lookup"><span data-stu-id="94474-123">In the Expire field, set the date to '2019-10-27'.</span></span>
    * <span data-ttu-id="94474-124">Aegumiskuupäev on valikuline.</span><span class="sxs-lookup"><span data-stu-id="94474-124">The expiration date is optional.</span></span>  
9. <span data-ttu-id="94474-125">Valige dokumenditüübi väljastanud asutus.</span><span class="sxs-lookup"><span data-stu-id="94474-125">Select the agency that issued the document type.</span></span> <span data-ttu-id="94474-126">Näide: Provints/territoorium</span><span class="sxs-lookup"><span data-stu-id="94474-126">Example: Province/territory</span></span>
10. <span data-ttu-id="94474-127">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="94474-127">Click Save.</span></span>


