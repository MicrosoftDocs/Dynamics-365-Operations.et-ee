---
title: Kulukategooriad, mida kasutatakse moodulites Tootmise juhtimine ja Projektihalduse raamatupidamine
description: "Mõnda tüüpi tootmistöö võib rakenduda projekti ajaprognoosidele ja aruandlusele. See artikkel annab teavet kulukategooriate kohta, mis tuleb määratleda tootmise ja projekti puhul nende tootmistöö tüüpide jaoks."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjCategory
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 78253
ms.assetid: cfdd58a0-8afa-4a6f-a208-a76e2c162429
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d641ce950aed87b0cf6763fc9dae67ef47268b8d
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="cost-categories-used-in-production-control-and-project-management-accounting"></a><span data-ttu-id="6aa1d-104">Kulukategooriad, mida kasutatakse moodulites Tootmise juhtimine ja Projektihalduse raamatupidamine</span><span class="sxs-lookup"><span data-stu-id="6aa1d-104">Cost categories used in Production control and Project management accounting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6aa1d-105">Mõnda tüüpi tootmistöö võib rakenduda projekti ajaprognoosidele ja aruandlusele.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-105">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="6aa1d-106">See artikkel annab teavet kulukategooriate kohta, mis tuleb määratleda tootmise ja projekti puhul nende tootmistöö tüüpide jaoks.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-106">This article provides information about the cost categories that you must define for these types of production work for production and project purposes.</span></span>

<span data-ttu-id="6aa1d-107">Mõnda tüüpi tootmistöö võib rakenduda projekti ajaprognoosidele ja aruandlusele.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-107">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="6aa1d-108">Sellisel juhul on tootmise ja projekti jaoks vaja kulukategooriat.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-108">In this case, a cost category is required for production and project purposes.</span></span> <span data-ttu-id="6aa1d-109">Kui tootmises ja projektides kasutatakse kulukategooriat, tuleb määratleda täiendav projektiga seotud teave.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-109">When a cost category is used in production and projects, additional project-related information must be defined.</span></span> <span data-ttu-id="6aa1d-110">Näiteks projektidega seotud tunnikulud võivad erineda tootmisega seotud tunnikuludest.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-110">For example, the hourly costs that are associated with projects can differ from the hourly costs that are associated with production.</span></span> <span data-ttu-id="6aa1d-111">Lehte **Kulukategooriad** saab kasutada tootmise juhtimises ja projektihalduse raamatupidamises kasutatava kulukategooria määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-111">You can use the **Cost categories** page to define a cost category that is used in Production control and Project management accounting.</span></span> 

<span data-ttu-id="6aa1d-112">**Märkus:** kuluarvestusel on leht **Projekti kategooriad**, kuid sellel lehel puudub seos selles teemas kirjeldatud funktsioonidega.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-112">**Note:** Cost accounting has a **Project categories** page, but this page has no relationship to the functionality that is described in this topic.</span></span> <span data-ttu-id="6aa1d-113">Kulukategooria kasutamisel projektides on lehel **Kulukategooriad** täiendavad vahekaardid, mis kuvavad täiendava projektiga seotud teabe.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-113">When you use a cost category in projects, the **Cost categories** page has additional tabs that show additional project-related information.</span></span> <span data-ttu-id="6aa1d-114">See teave hõlmab kategooriagruppi, rea atribuuti ja pearaamatukontosid, mis on määratud kulukategooriale.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-114">This information includes the category group, a line property, and ledger accounts that are assigned to the cost category.</span></span>

-   <span data-ttu-id="6aa1d-115">Kulukategooria peab olema määratud kategooriagrupile, mis toetab kandetüüpi **Tunnid**.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-115">The cost category must be assigned to a category group that supports a transaction type of **Hours**.</span></span>
-   <span data-ttu-id="6aa1d-116">Rea atribuut näitab vaiketeavet selle kohta, kuidas teavitatud aeg on projektile arveldatav.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-116">The line property indicates default information about how reported time can be charged to a project.</span></span>
-   <span data-ttu-id="6aa1d-117">Tavaliselt määratletakse kulude ja müügiga seotud pearaamatukontod kulukategooriale määratud kategooriagrupi jaoks.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-117">Typically, the ledger accounts that are related to costs and sales are defined for the category group that is assigned to the cost category.</span></span> <span data-ttu-id="6aa1d-118">Kuid konkreetsed kontod saab määratleda eraldi kulukategooria puhul.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-118">However, specific accounts can be defined for an individual cost category.</span></span>

<span data-ttu-id="6aa1d-119">Täiendavad nupud lehel **Kulukategooriad** pakuvad juurdepääsu projektiga seotud teabele valitud kulukategooria kohta.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-119">Additional buttons on the **Cost categories** page let you access project-related information about a selected cost category.</span></span> <span data-ttu-id="6aa1d-120">Näiteks saate vaadata projektiga seotud kandeid, määrata töötajaid või projekte, määratleda tunnikulusid ja müügihindu ja vaadata aruandeid.</span><span class="sxs-lookup"><span data-stu-id="6aa1d-120">For example, you can view project-related transactions, define employees or projects, define hourly costs and sales prices, and view reports.</span></span>




