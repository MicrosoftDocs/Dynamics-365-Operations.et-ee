---
title: Toodetud kauba püsikulude amortiseerimine
description: Toodetud kauba püsikulud peegeldavad operatsiooni seadistusaegu ja konstantse koguse või konstantse praagi summaga komponente.
author: AndersGirke
manager: tfehr
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 298b5cbbf955527edb399eae78a1c8e60a8b9ce3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426465"
---
# <a name="amortize-constant-costs-for-a-manufactured-item"></a><span data-ttu-id="70634-103">Toodetud kauba püsikulude amortiseerimine</span><span class="sxs-lookup"><span data-stu-id="70634-103">Amortize constant costs for a manufactured item</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70634-104">Toodetud kauba püsikulud peegeldavad operatsiooni seadistusaegu ja konstantse koguse või konstantse praagi summaga komponente.</span><span class="sxs-lookup"><span data-stu-id="70634-104">A manufactured item’s constant costs reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span> 

<span data-ttu-id="70634-105">Saatepartii suuruse kuluarvestuse kontseptsiooni kasutatakse nende konstantsete kulude amortiseerimiseks toodetud kauba kalkuleeritud kulus.</span><span class="sxs-lookup"><span data-stu-id="70634-105">The concept of a costing lot size is used to amortize these constant costs in the calculated cost of a manufactured item.</span></span> <span data-ttu-id="70634-106">Sellel kontseptsioonil on mitmeid sünonüüme, üks neist on saatepartii suuruse raamatupidamine.</span><span class="sxs-lookup"><span data-stu-id="70634-106">This concept has several synonyms, one of which is accounting lot size.</span></span> <span data-ttu-id="70634-107">Püsikulude amortiseerimise kontseptsioonil on samuti mitmeid sünonüüme, üks neist on proportsionaalsed püsikulud.</span><span class="sxs-lookup"><span data-stu-id="70634-107">The concept of amortizing constant costs also has several synonyms, one of which is proportional constant costs.</span></span>

<span data-ttu-id="70634-108">Toodetud kauba saatepartii suuruse kuluarvestuse kogust kasutatakse koosluse kalkulatsioonis.</span><span class="sxs-lookup"><span data-stu-id="70634-108">The quantity of a costing lot size for a manufactured item is used in a bill of material (BOM) calculation.</span></span> <span data-ttu-id="70634-109">Kogus sõltub sellest, kuidas käivitate ja teostate koosluse kalkulatsiooni, vastavalt alltoodud illustratsioonile:</span><span class="sxs-lookup"><span data-stu-id="70634-109">The quantity depends on how you initiate and perform the BOM calculation, as illustrated by the following:</span></span>

-   <span data-ttu-id="70634-110">Vaikekalkulatsiooni kogus kauba koosluse kalkulatsioonis \– kauba standardse tellimuse kogus laovarude jaoks toimib vaikimisi selle saatepartii suuruse kuluarvestuse puhul, kuid vaikeväärtus võib olla suurem kogus, et peegeldada kauba tellimuskoguse kordühikut.</span><span class="sxs-lookup"><span data-stu-id="70634-110">Default calculation quantity in an item’s BOM calculation − The item’s standard order quantity for inventory acts as the costing lot size, but the default value might be a greater quantity to reflect the item’s order quantity multiple.</span></span> <span data-ttu-id="70634-111">Kauba standardset tellimuse kogust ja kordühikut saab määrata selle vaiketellimuse sätete või saidikohaste tellimuse sätete piires.</span><span class="sxs-lookup"><span data-stu-id="70634-111">The item’s standard order quantity and multiple can be defined within its default order settings or site-specific order settings.</span></span>
-   <span data-ttu-id="70634-112">Määratletud arvutuskogus kauba koosluse kalkulatsioonis ? määratletud arvutuskogus toimib kauba saatepartii suuruse kuluarvestusena.</span><span class="sxs-lookup"><span data-stu-id="70634-112">Specified calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item.</span></span> <span data-ttu-id="70634-113">Algselt kasutab kalkulatsiooni kogus määratud kauba standardse tellimuse kogust, kuid vaikeväärtust saab käsitsi alistada.</span><span class="sxs-lookup"><span data-stu-id="70634-113">The calculation quantity initially uses the item’s standard order quantity, but the default value can be manually overridden.</span></span> <span data-ttu-id="70634-114">Määratletud arvutuskogus tähistab määratletud kauba ja tootmise koosluse rea tüübiga toodetud komponentide puhul saatepartii suuruse kuluarvestust.</span><span class="sxs-lookup"><span data-stu-id="70634-114">The specified calculation quantity represents the costing lot size for the specified item, and for manufactured components that have a BOM line type of production.</span></span> <span data-ttu-id="70634-115">See põhineb eeldusel, et komponenti toodetakse täpne kogus.</span><span class="sxs-lookup"><span data-stu-id="70634-115">This is because it is assumed that the component will be produced to the exact quantity.</span></span> <span data-ttu-id="70634-116">Teiste toodetud komponentide, millel on koosluse rea tüüpi kaup, saatepartii suuruse kuluarvestus peegeldab nende standardset tellimuse kogust.</span><span class="sxs-lookup"><span data-stu-id="70634-116">The costing lot size for other manufactured components that have a BOM line type of item will reflect their standard order quantity.</span></span>
-   <span data-ttu-id="70634-117">Määratletud vastavalt tellimusele tehtud arvutuse kogus toote koosluse kalkulatsioonis ? määratletud arvutuskogus toimib kauba ja selle toodetud komponentide saatepartii suuruse kuluarvestusena, kui koosluse kalkulatsioonid kasutavad vastavalt tellimusele tehtud koosnevusarvutuse režiimi.</span><span class="sxs-lookup"><span data-stu-id="70634-117">Specified make-to-order calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item and its manufactured components when BOM calculations use a make-to-order explosion mode.</span></span> <span data-ttu-id="70634-118">Eeldatakse, et toodetud komponente toodetakse täpne kogus, just nagu toodetud komponendi puhul, mille koosluse rea tüüp on tootmine.</span><span class="sxs-lookup"><span data-stu-id="70634-118">It is assumed that the manufactured components will be produced to the exact quantity, just like a manufactured component that has a BOM line type of production.</span></span>
-   <span data-ttu-id="70634-119">Määratletud arvutuskogus tellimusekohases koosluse kalkulatsioonis ? tellimusekohast koosluse kalkulatsiooni saab teha rea üksuse puhul müügitellimusel, müügipakkumisel või teenusetellimusel.</span><span class="sxs-lookup"><span data-stu-id="70634-119">Specified calculation quantity in an order-specific BOM calculation − An order-specific BOM calculation can be performed for a line item on a sales order, sales quotation, or service order.</span></span> <span data-ttu-id="70634-120">Määratletud arvutuskogus kasutab algse rea kauba kogust, kuid vaikekogust saab alistada.</span><span class="sxs-lookup"><span data-stu-id="70634-120">The specified calculation quantity uses the quantity on the originating line item, but the default quantity can be overridden.</span></span> <span data-ttu-id="70634-121">Saate valida, kas tellimuse kohane koosluse kalkulatsioon kasutab vastavalt tellimusele tehtud või mitmetasandilist koosnevusarvutuse režiimi.</span><span class="sxs-lookup"><span data-stu-id="70634-121">You can select whether the order-specific BOM calculation uses a make-to-order or multilevel explosion mode.</span></span>

<span data-ttu-id="70634-122">Toodetud kauba amortiseeritud püsikulude arvutatud kogust nimetatakse terminiga tasud.</span><span class="sxs-lookup"><span data-stu-id="70634-122">The calculated amount of a manufactured item’s amortized constant costs is termed charges.</span></span>





