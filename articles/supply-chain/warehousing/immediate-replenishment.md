---
title: "Viivitamatu täiendamine"
description: "Selles teemas kirjeldatakse, kuidas kasutada viivitamatut täiendamist varude täiendamiseks, kui asukohakorraldusel varude eraldamine nurjub."
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLocDirTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a11a26df85647aa36cd30c42f81be4ec2af4409b
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="immediate-replenishment"></a><span data-ttu-id="025f0-103">Viivitamatu täiendamine</span><span class="sxs-lookup"><span data-stu-id="025f0-103">Immediate replenishment</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="025f0-104">Viivitamatu täiendamine võimaldab teil varusid täiendada kohe, kui asukohakorralduse real varude eraldamine nurjub.</span><span class="sxs-lookup"><span data-stu-id="025f0-104">Immediate replenishment lets you replenish inventory immediately after a location directive line fails to allocate inventory.</span></span> <span data-ttu-id="025f0-105">Täiendamine põhineb asukohakorralduse seadistuse ühel real.</span><span class="sxs-lookup"><span data-stu-id="025f0-105">The replenishment is based on a single line in the setup of the location directive.</span></span> <span data-ttu-id="025f0-106">Kui varude laoseis pole rea jaoks määratud mõõtühikus, toimub selle mõõtühiku täiendamine kohe.</span><span class="sxs-lookup"><span data-stu-id="025f0-106">If inventory isn't on hand in the unit of measure that is specified by that line, replenishment of that unit of measure occurs immediately.</span></span>

<span data-ttu-id="025f0-107">Viivitamatu täiendamine pakub alternatiivi meetodile, kus varude eraldamine põhineb asukohakorralduses mitmel real, ja kus nõudlus eraldamise lõpus summeeritakse ning täiendatakse mõõtühikus, mille määrab asukohakorralduse viimane rida.</span><span class="sxs-lookup"><span data-stu-id="025f0-107">Immediate replenishment provides an alternative to the method where the allocation of inventory is based on more lines in the location directive, and where the demand is summed at the end of the allocation and replenished in the unit of measure that is specified by the last line in the location directive.</span></span>

<span data-ttu-id="025f0-108">Viivitamatu täiendamise eeliseks on, et täiendamist saab piirata teatud ühikutega ja koguse saab suunata kindlatesse asukohtadesse.</span><span class="sxs-lookup"><span data-stu-id="025f0-108">The benefits of using immediate replenishment are that replenishment can be limited by specific units and the quantity can be directed to specific locations.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="025f0-109">Äristsenaarium</span><span class="sxs-lookup"><span data-stu-id="025f0-109">Business scenario</span></span>

<span data-ttu-id="025f0-110">Näiteks on teil ladu, kus on eraldi komplekteerimisalad mõõtühikutele „kast” ja „iga”.</span><span class="sxs-lookup"><span data-stu-id="025f0-110">For example, you have a warehouse that has separate picking areas for the "box" and "each" units of measure.</span></span> <span data-ttu-id="025f0-111">Soovite komplekteerimisprotsessi optimeerida, komplekteerides võimalikult palju kaste ja seejärel komplekteerides järelejäänud koguse, mis on väiksem kui kast, alal „iga”.</span><span class="sxs-lookup"><span data-stu-id="025f0-111">You want to optimize the picking process by picking as many boxes as possible and then picking any remaining quantity that is less than a box from the "each" area.</span></span>

<span data-ttu-id="025f0-112">Sel juhul saate kasutada viivitamatut täiendamist.</span><span class="sxs-lookup"><span data-stu-id="025f0-112">In this case, you can use immediate replenishment.</span></span> <span data-ttu-id="025f0-113">Asukohakorralduses saate seadistada viivitamatu täiendamise kastidele nii, et nõudluse tõttu täiendamist kasutatakse kohe, kui kaste, mida saab nõudluse koguse jaoks komplekteerida, tuleb puudu.</span><span class="sxs-lookup"><span data-stu-id="025f0-113">In the location directive, you can set up immediate replenishment for boxes so that demand replenishment is used as soon as there is a shortage of boxes that can be picked for the demand quantity.</span></span> <span data-ttu-id="025f0-114">Sel viisil optimeerite komplekteerimisprotsessi nii, et komplekteerimine sisaldab võimalikult palju kaste.</span><span class="sxs-lookup"><span data-stu-id="025f0-114">In this way, you optimize the picking process so that picking includes as many boxes as possible.</span></span> <span data-ttu-id="025f0-115">Viivitamatu täiendamise loob kastide täiendamise ja nõudlust ei edastata. Seega komplekteeritakse kogused mõõtühikus „iga”.</span><span class="sxs-lookup"><span data-stu-id="025f0-115">Immediate replenishment will generate replenishment of the boxes, and the demand won't be passed on so that the quantities are picked in the "each" unit of measure.</span></span> <span data-ttu-id="025f0-116">Teiste sõnadega, alalt „iga” komplekteeritakse ainult kogused, mis tuleb komplekteerida mõõtühikus „iga” (st, kogused on kastist väiksemad).</span><span class="sxs-lookup"><span data-stu-id="025f0-116">In other words, only the quantities that are supposed to be picked in the "each" unit of measure (that is, quantities that are less than a box) will be picked from the "each" area.</span></span> <span data-ttu-id="025f0-117">Kui alas „kast” ilmneb puudujääk, saate kogunõudlusest komplekteerida nii palju kaste, kui võimalik.</span><span class="sxs-lookup"><span data-stu-id="025f0-117">If a shortage occurs in the "box" area, you can pick as many boxes as possible out of the total demand.</span></span> <span data-ttu-id="025f0-118">Seejärel komplekteeritakse ülejäänud kogused alalt „iga”.</span><span class="sxs-lookup"><span data-stu-id="025f0-118">The remaining quantities will then be picked from the "each" area.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="025f0-119">Kus see kehtib</span><span class="sxs-lookup"><span data-stu-id="025f0-119">Where it applies</span></span>

<span data-ttu-id="025f0-120">Viivitamatut täiendamist kasutatakse laine käivitamise ajal, kui eraldamine nurjub asukohakorralduse rea puhul, millele on seadistatud täiendamise mall.</span><span class="sxs-lookup"><span data-stu-id="025f0-120">Immediate replenishment is used during wave execution if allocation fails for a location directive line that a replenishment template is set for.</span></span>

## <a name="set-up-immediate-replenishment"></a><span data-ttu-id="025f0-121">Viivitamatu täiendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="025f0-121">Set up immediate replenishment</span></span>

- <span data-ttu-id="025f0-122">Tehke valikud **Laohaldus** \> **Seadistus** \> **Asukohakorraldused**, seejärel valige voo nõude jaoks vahekaardi **Read** loendis **Viivitamatu täiendamise mall** täiendamise mall.</span><span class="sxs-lookup"><span data-stu-id="025f0-122">Go to **Warehouse management** \> **Setup** \> **Location directives**, and then, on the **Lines** tab, in the **Immediate replenishment template** list, select a replenishment template for wave demand.</span></span>

<span data-ttu-id="025f0-123">Täiendamise mall rakendatakse, kui asukohakorralduse real ei õnnestu sihtotstarbelist mõõtühikut eraldada.</span><span class="sxs-lookup"><span data-stu-id="025f0-123">The replenishment template is applied if the location directive line fails to allocate a dedicated unit of measure.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="025f0-124">Tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="025f0-124">Troubleshooting</span></span>

<span data-ttu-id="025f0-125">Kui asukohakorralduse rea jaoks on viivitamatu täiendamine valitud, kuid kui nõudluse täiendamismallide kasutamisel selle asukohakorralduse rea jaoks täiendustööd ei looda, tuleb uurida kahte peamist põhjust.</span><span class="sxs-lookup"><span data-stu-id="025f0-125">If immediate replenishment is selected for a location directive line, but no replenishment work is generated when you use demand replenishment templates for that location directive line, two main causes must be investigated:</span></span>

- <span data-ttu-id="025f0-126">Veenduge, et rakendatav nõudluse täiendamismall on seadistatud kasutama õigeid tüübi **Täiendamine** asukoha- ja töömalle.</span><span class="sxs-lookup"><span data-stu-id="025f0-126">Make sure that the demand replenishment template that is applied is set up to use the correct location templates and work templates of the **Replenishment** type.</span></span>
- <span data-ttu-id="025f0-127">Veenduge, et asukohtades, kus nõudluse täiendamismall otsib täiendamiseks vaba kaubavaru, oleks piisavalt vaba kaubavaru.</span><span class="sxs-lookup"><span data-stu-id="025f0-127">Make sure that there is enough on-hand inventory at the locations where the demand replenishment template searches for on-hand inventory for replenishment.</span></span>

