---
title: Numbriseeriate häälestamine viisardi abil
description: See teema selgitab, kuidas seadistada nõutavaid numbriseeriaid viisardi abil korraga.
author: sericks007
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b79924e2c8d94b5e5e160a123e9b0cde0971fd96
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560479"
---
# <a name="set-up-number-sequences-using-a-wizard"></a><span data-ttu-id="e06d3-103">Numbriseeriate häälestamine viisardi abil</span><span class="sxs-lookup"><span data-stu-id="e06d3-103">Set up number sequences using a wizard</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e06d3-104">Numbriseeriaid kasutatakse loetavate ainuidentifikaatorite loomiseks koondandmetele ja kandekirjetele, mis neid nõuavad.</span><span class="sxs-lookup"><span data-stu-id="e06d3-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="e06d3-105">Koondandmeid või kandekirjet, mis nõuavad identifikaatorit, nimetatakse viiteks.</span><span class="sxs-lookup"><span data-stu-id="e06d3-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="e06d3-106">Enne kui saate viite jaoks uusi kirjeid luua, peate seadistama numbriseeria ja selle viitega siduma.</span><span class="sxs-lookup"><span data-stu-id="e06d3-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="e06d3-107">See teema selgitab, kuidas seadistada nõutavaid numbriseeriaid viisardi abil korraga.</span><span class="sxs-lookup"><span data-stu-id="e06d3-107">This topic explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="e06d3-108">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="e06d3-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="e06d3-109">Avage **Navigeerimispaneel > Moodulid > Organisatsiooni haldus > Numbriseeriad > Numbriseeriad**.</span><span class="sxs-lookup"><span data-stu-id="e06d3-109">Go to **Navigation > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="e06d3-110">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="e06d3-110">Select **Generate**.</span></span>
3. <span data-ttu-id="e06d3-111">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e06d3-111">Select **Next**.</span></span>

   - <span data-ttu-id="e06d3-112">Sellel lehel saate muuta ID-koodi, madalaimat väärtust ja kõrgeimat väärtust.</span><span class="sxs-lookup"><span data-stu-id="e06d3-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="e06d3-113">Lisaks saate märkida, kas numbriseeria peab olema pidev.</span><span class="sxs-lookup"><span data-stu-id="e06d3-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
   - <span data-ttu-id="e06d3-114">Ärge valige suvandit **Pidev**, kui peate numbreid numbriseeriale eelnevalt eraldama.</span><span class="sxs-lookup"><span data-stu-id="e06d3-114">Do not select the **Continuous** option if you must preallocate numbers for the number sequence.</span></span> <span data-ttu-id="e06d3-115">Ulatuse segmendi lisamiseks numbriseeria vormingule valige loendist vorming ja klõpsake seejärel suvandit **Kaasa ulatus vormingus**.</span><span class="sxs-lookup"><span data-stu-id="e06d3-115">To add a scope segment to the format of a number sequence, select the format in the list, and then select **Include scope in format**.</span></span> <span data-ttu-id="e06d3-116">Ulatuse segmendi eemaldamiseks numbriseeria vormingust valige vorming loendist ja klõpsake seejärel nuppu **Eemalda ulatus vormingust**.</span><span class="sxs-lookup"><span data-stu-id="e06d3-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then select **Remove scope from format**.</span></span> <span data-ttu-id="e06d3-117">Numbriseeria väljajätmiseks automaatsest loomisest valige loendist numbriseeria ja klõpsake seejärel nuppu **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="e06d3-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then select **Delete**.</span></span>  

4. <span data-ttu-id="e06d3-118">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e06d3-118">Select **Next**.</span></span>
5. <span data-ttu-id="e06d3-119">Valige **Lõpeta**.</span><span class="sxs-lookup"><span data-stu-id="e06d3-119">Select **Finish**.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]