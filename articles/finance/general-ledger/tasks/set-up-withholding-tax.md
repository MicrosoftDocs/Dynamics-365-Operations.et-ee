---
title: Kinnipeetava maksu seadistamine
description: Selles teemas selgitatakse, kuidas seadistada kinnipeetavat maksu.
author: twheeloc
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45ae7d6bb04dbf06b9b05d9f5610895fced650b0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994436"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="00a7c-103">Kinnipeetava maksu seadistamine</span><span class="sxs-lookup"><span data-stu-id="00a7c-103">Set up withholding tax</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="00a7c-104">Selles teemas selgitatakse, kuidas seadistada kinnipeetavat maksu.</span><span class="sxs-lookup"><span data-stu-id="00a7c-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="00a7c-105">*Kinnipeetav maks* on käibemaksu mitte loovate hankijate maks.</span><span class="sxs-lookup"><span data-stu-id="00a7c-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="00a7c-106">Hankija maksetelt arvutatav kinnipeetav maks on kohustus.</span><span class="sxs-lookup"><span data-stu-id="00a7c-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="00a7c-107">Seetõttu on kinnipeetava maksu sisestamisel kehtivad kontod ainult bilansikontod või kohustuste kontod.</span><span class="sxs-lookup"><span data-stu-id="00a7c-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="00a7c-108">See ülesande juhend näitab, kuidas kinnipeetavat maksu seadistada.</span><span class="sxs-lookup"><span data-stu-id="00a7c-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="00a7c-109">Avage **Navigeerimispaan > Moodulid > Maks > Kaudsed maksud > Kinnipeetav maks > Kinnipeetava maksu koodid**.</span><span class="sxs-lookup"><span data-stu-id="00a7c-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="00a7c-110">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="00a7c-110">Select **New**.</span></span>
3. <span data-ttu-id="00a7c-111">Sisestage väärtus väljale **Kinnipeetava maksu kood**.</span><span class="sxs-lookup"><span data-stu-id="00a7c-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="00a7c-112">Sisestage väljale **Kinnipeetava maksu nimi** kinnipeetava maksu koodi nimi.</span><span class="sxs-lookup"><span data-stu-id="00a7c-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="00a7c-113">Valige väljal **Põhikonto** peamine konto kinnipeetava maksukohustuse sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="00a7c-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="00a7c-114">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="00a7c-114">Select **Save**.</span></span>
7. <span data-ttu-id="00a7c-115">Valige **Väärtused** ja märgistage loendis soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="00a7c-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="00a7c-116">Sisestage väljale **Väärtus** kinnipeetava maksu arvutamiseks kasutatav protsent.</span><span class="sxs-lookup"><span data-stu-id="00a7c-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="00a7c-117">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="00a7c-117">Select **Save**.</span></span>
10. <span data-ttu-id="00a7c-118">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="00a7c-118">Close the page.</span></span>
11. <span data-ttu-id="00a7c-119">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="00a7c-119">Select **Save**.</span></span>
12. <span data-ttu-id="00a7c-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="00a7c-120">Close the page.</span></span>
13. <span data-ttu-id="00a7c-121">Avage **Navigeerimispaan > Moodulid > Maks > Kaudsed maksud > Kinnipeetav maks > Kinnipeetava maksu rühmad**.</span><span class="sxs-lookup"><span data-stu-id="00a7c-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="00a7c-122">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="00a7c-122">Select **New**.</span></span>
15. <span data-ttu-id="00a7c-123">Sisestage väljale **Kinnipeetava maksu rühm** kinnipeetava maksu rühma identifikaator.</span><span class="sxs-lookup"><span data-stu-id="00a7c-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="00a7c-124">Sisestage väljale **Kirjeldus** kinnipeetava maksu rühma nimi.</span><span class="sxs-lookup"><span data-stu-id="00a7c-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="00a7c-125">Valige väljal **Kinnipeetava maksu kood** kinnipeetava maksu kood.</span><span class="sxs-lookup"><span data-stu-id="00a7c-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="00a7c-126">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="00a7c-126">Select **Save**.</span></span>
19. <span data-ttu-id="00a7c-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="00a7c-127">Close the page.</span></span>

