---
title: Numbriseeriate häälestamine viisardi abil
description: See teema selgitab, kuidas seadistada nõutavaid numbriseeriaid viisardi abil korraga.
author: sericks007
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 76dc32f2254ffd2a2e33eef594d6e602092bcb6f
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140489"
---
# <a name="set-up-number-sequences-using-a-wizard"></a><span data-ttu-id="3da71-103">Numbriseeriate häälestamine viisardi abil</span><span class="sxs-lookup"><span data-stu-id="3da71-103">Set up number sequences using a wizard</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3da71-104">Numbriseeriaid kasutatakse loetavate ainuidentifikaatorite loomiseks koondandmetele ja kandekirjetele, mis neid nõuavad.</span><span class="sxs-lookup"><span data-stu-id="3da71-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="3da71-105">Koondandmeid või kandekirjet, mis nõuavad identifikaatorit, nimetatakse viiteks.</span><span class="sxs-lookup"><span data-stu-id="3da71-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="3da71-106">Enne kui saate viite jaoks uusi kirjeid luua, peate seadistama numbriseeria ja selle viitega siduma.</span><span class="sxs-lookup"><span data-stu-id="3da71-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="3da71-107">See teema selgitab, kuidas seadistada nõutavaid numbriseeriaid viisardi abil korraga.</span><span class="sxs-lookup"><span data-stu-id="3da71-107">This topic explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="3da71-108">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="3da71-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="3da71-109">Avage **Navigeerimispaneel > Moodulid > Organisatsiooni haldus > Numbriseeriad > Numbriseeriad**.</span><span class="sxs-lookup"><span data-stu-id="3da71-109">Go to **Navigation > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="3da71-110">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="3da71-110">Select **Generate**.</span></span>
3. <span data-ttu-id="3da71-111">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="3da71-111">Select **Next**.</span></span>

   - <span data-ttu-id="3da71-112">Sellel lehel saate muuta ID-koodi, madalaimat väärtust ja kõrgeimat väärtust.</span><span class="sxs-lookup"><span data-stu-id="3da71-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="3da71-113">Lisaks saate märkida, kas numbriseeria peab olema pidev.</span><span class="sxs-lookup"><span data-stu-id="3da71-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
   - <span data-ttu-id="3da71-114">Ärge valige suvandit **Pidev**, kui peate numbreid numbriseeriale eelnevalt eraldama.</span><span class="sxs-lookup"><span data-stu-id="3da71-114">Do not select the **Continuous** option if you must preallocate numbers for the number sequence.</span></span> <span data-ttu-id="3da71-115">Ulatuse segmendi lisamiseks numbriseeria vormingule valige loendist vorming ja klõpsake seejärel suvandit **Kaasa ulatus vormingus**.</span><span class="sxs-lookup"><span data-stu-id="3da71-115">To add a scope segment to the format of a number sequence, select the format in the list, and then select **Include scope in format**.</span></span> <span data-ttu-id="3da71-116">Ulatuse segmendi eemaldamiseks numbriseeria vormingust valige vorming loendist ja klõpsake seejärel nuppu **Eemalda ulatus vormingust**.</span><span class="sxs-lookup"><span data-stu-id="3da71-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then select **Remove scope from format**.</span></span> <span data-ttu-id="3da71-117">Numbriseeria väljajätmiseks automaatsest loomisest valige loendist numbriseeria ja klõpsake seejärel nuppu **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="3da71-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then select **Delete**.</span></span>  

4. <span data-ttu-id="3da71-118">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="3da71-118">Select **Next**.</span></span>
5. <span data-ttu-id="3da71-119">Valige **Lõpeta**.</span><span class="sxs-lookup"><span data-stu-id="3da71-119">Select **Finish**.</span></span>

