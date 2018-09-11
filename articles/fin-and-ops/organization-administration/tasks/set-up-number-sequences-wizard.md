--- 
title: Numbriseeriate seadistamine viisardit kasutades
description: "Numbriseeriaid kasutatakse loetavate ainuidentifikaatorite loomiseks koondandmetele ja kandekirjetele, mis neid nõuavad."
author: sericks007
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 1aaea94678e9ddfa771c21063f53aefa172b5e97
ms.contentlocale: et-ee
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-number-sequences-by-using-a-wizard"></a><span data-ttu-id="5329f-103">Numbriseeriate seadistamine viisardit kasutades</span><span class="sxs-lookup"><span data-stu-id="5329f-103">Set up number sequences by using a wizard</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5329f-104">Numbriseeriaid kasutatakse loetavate ainuidentifikaatorite loomiseks koondandmetele ja kandekirjetele, mis neid nõuavad.</span><span class="sxs-lookup"><span data-stu-id="5329f-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="5329f-105">Koondandmeid või kandekirjet, mis nõuavad identifikaatorit, nimetatakse viiteks.</span><span class="sxs-lookup"><span data-stu-id="5329f-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="5329f-106">Enne kui saate viite jaoks uusi kirjeid luua, peate seadistama numbriseeria ja selle viitega siduma.</span><span class="sxs-lookup"><span data-stu-id="5329f-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="5329f-107">See protseduur selgitab, kuidas seadistada nõutavaid numbriseeriaid viisardi abil korraga.</span><span class="sxs-lookup"><span data-stu-id="5329f-107">This procedure explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="5329f-108">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="5329f-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="5329f-109">Avage Organisatsiooni haldus > Numbriseeriad > Numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="5329f-109">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="5329f-110">Klõpsake suvandit Loo.</span><span class="sxs-lookup"><span data-stu-id="5329f-110">Click Generate.</span></span>
3. <span data-ttu-id="5329f-111">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="5329f-111">Click Next.</span></span>
    * <span data-ttu-id="5329f-112">Sellel lehel saate muuta ID-koodi, madalaimat väärtust ja kõrgeimat väärtust.</span><span class="sxs-lookup"><span data-stu-id="5329f-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="5329f-113">Lisaks saate märkida, kas numbriseeria peab olema pidev.</span><span class="sxs-lookup"><span data-stu-id="5329f-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
    * <span data-ttu-id="5329f-114">Ärge valige suvandit Pidev, kui peate numbreid numbriseeriale eelnevalt eraldama.</span><span class="sxs-lookup"><span data-stu-id="5329f-114">Do not select the Continuous option if you must preallocate numbers for the number sequence.</span></span>     <span data-ttu-id="5329f-115">Ulatuse segmendi lisamiseks numbriseeria vormingule valige loendist vorming ja klõpsake seejärel suvandit Kaasa ulatus vormingus.</span><span class="sxs-lookup"><span data-stu-id="5329f-115">To add a scope segment to the format of a number sequence, select the format in the list, and then click Include scope in format.</span></span>     <span data-ttu-id="5329f-116">Ulatuse segmendi eemaldamiseks numbriseeria vormingust valige vorming loendist ja klõpsake seejärel nuppu Eemalda ulatus vormingust.</span><span class="sxs-lookup"><span data-stu-id="5329f-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then click Remove scope from format.</span></span>     <span data-ttu-id="5329f-117">Numbriseeria väljajätmiseks automaatsest loomisest valige loendist numbriseeria ja klõpsake seejärel nuppu Kustuta.</span><span class="sxs-lookup"><span data-stu-id="5329f-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then click Delete.</span></span>  
4. <span data-ttu-id="5329f-118">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="5329f-118">Click Next.</span></span>
5. <span data-ttu-id="5329f-119">Klõpsake Lõpeta.</span><span class="sxs-lookup"><span data-stu-id="5329f-119">Click Finish.</span></span>


