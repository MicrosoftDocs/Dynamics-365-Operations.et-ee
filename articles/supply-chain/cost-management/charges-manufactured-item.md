---
title: Toodetud kauba kulude kuvamine
description: Toodetud kauba püsikulud kajastavad toimingu seadistusaegu ja konstantse koguse või konstantse praagi summaga komponente.
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: b8fcfc1a9386d05c2adbcb4208e7ef5d01644430
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "316667"
---
# <a name="display-charges-for-a-manufactured-item"></a><span data-ttu-id="49eca-103">Toodetud kauba kulude kuvamine</span><span class="sxs-lookup"><span data-stu-id="49eca-103">Display charges for a manufactured item</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49eca-104">Toodetud kauba püsikulud kajastavad toimingu seadistusaegu ja konstantse koguse või konstantse praagi summaga komponente.</span><span class="sxs-lookup"><span data-stu-id="49eca-104">The constant costs of a manufactured item reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span>

<span data-ttu-id="49eca-105">Kauba tasude arvutatud summat saab kuvada koos kauba ühiku hindadega.</span><span class="sxs-lookup"><span data-stu-id="49eca-105">The calculated amount of an item's charges can be displayed with the item's unit costs.</span></span> <span data-ttu-id="49eca-106">Siiski kuvatakse tasud mõnikord eraldi väljadena ning need ei sisaldu kauba ühiku hindades.</span><span class="sxs-lookup"><span data-stu-id="49eca-106">However, the charges are sometimes displayed as separate fields, and they are not included in the item's unit costs.</span></span> <span data-ttu-id="49eca-107">Kui tasud kuvatakse eraldi väljadena, kuvatakse ühel väljal tasude kogusumma ja teisel väljal kuvatakse saatepartii kuluarvestuse suurus, mida kasutatakse summa amortiseerimiseks.</span><span class="sxs-lookup"><span data-stu-id="49eca-107">When the charges appear as separate fields, one field displays the total amount of charges, and another field displays the costing lot size that is used to amortize the amount.</span></span> <span data-ttu-id="49eca-108">Kauba hinna leht kuvab näiteks tasusid kahe eraldi väljana.</span><span class="sxs-lookup"><span data-stu-id="49eca-108">The Item price page, for example, displays the charges as two separate fields.</span></span> <span data-ttu-id="49eca-109">Siiski kuvab leht Lõpetatud kauba ühiku kogukulu ja amortiseeritud kulud on kaasatud ühiku hindades.</span><span class="sxs-lookup"><span data-stu-id="49eca-109">However, the Complete page displays the item's total cost per unit, and the amortized costs are included in the unit costs.</span></span>

<span data-ttu-id="49eca-110">Toodetud kauba tasud sisalduvad alati standardkulude jaoks kauba ühiku hinnas.</span><span class="sxs-lookup"><span data-stu-id="49eca-110">The charges for a manufactured item are always included in the item's unit cost for standard cost purposes.</span></span> <span data-ttu-id="49eca-111">Valikuliselt saab neid hõlmata plaanitud kulude eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="49eca-111">They can optionally be included for planned cost purposes.</span></span> <span data-ttu-id="49eca-112">Kuluversioonisisene poliitika jõustab tasude kaasamise toodetud kauba hinnas.</span><span class="sxs-lookup"><span data-stu-id="49eca-112">A policy in the costing version enforces the inclusion of charges in the cost of a manufactured item.</span></span> <span data-ttu-id="49eca-113">Kui aktiveerite kauba kulukirje, värskendate kauba baasmaksumuse teabe tasusid, mida kuvatakse lehel Kauba hind.</span><span class="sxs-lookup"><span data-stu-id="49eca-113">When you activate an item's cost record, you update the charges for the item's base cost information, which is displayed in the Item price page.</span></span> <span data-ttu-id="49eca-114">Tasud kuvatakse mõnikord kahe eraldi väljana ning need ei sisaldu kauba ühiku hinnas.</span><span class="sxs-lookup"><span data-stu-id="49eca-114">The charges are displayed as two separate fields, and they are not included in the item's unit cost.</span></span> <span data-ttu-id="49eca-115">Iga aktiveerimine värskendab kauba baasmaksumuse teavet isegi siis, kui aktiveerimine kajastab eri tegevuskohti.</span><span class="sxs-lookup"><span data-stu-id="49eca-115">Each activation updates the item's base cost information, even if the activation reflects different sites.</span></span> <span data-ttu-id="49eca-116">Seega peaksite vaatama baasmaksumuse teavet viiteteabena.</span><span class="sxs-lookup"><span data-stu-id="49eca-116">Therefore, you should view the base cost information as reference information.</span></span>





