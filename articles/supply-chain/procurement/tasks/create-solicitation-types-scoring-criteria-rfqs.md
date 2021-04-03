---
title: Pakkumiskutsete jaoks kutsetüüpide ja hindamiskriteeriumide loomine
description: See juhend näitab, kuidas kutse tüüpi luua ja seda hindamismeetodiga seostada.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf196711799b78d7f4106b6693127d7f356b1d4e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262209"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="d6ed6-103">Pakkumiskutsete jaoks kutsetüüpide ja hindamiskriteeriumide loomine</span><span class="sxs-lookup"><span data-stu-id="d6ed6-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d6ed6-104">See juhend näitab, kuidas kutse tüüpi luua ja seda hindamismeetodiga seostada.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="d6ed6-105">Samuti näitav see, kuidas kasutada kutse tüüpi pakkumiskutsel, mis siis vaike-hindamismeetodi määrab.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="d6ed6-106">Neid ülesandeid täidab üldjuhul ostujuht.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="d6ed6-107">Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="d6ed6-108">Enne alustamist peab teil olema hindamismeetod kättesaadav.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="d6ed6-109">Kutsetüübi loomine</span><span class="sxs-lookup"><span data-stu-id="d6ed6-109">Create a solicitation type</span></span>
1. <span data-ttu-id="d6ed6-110">Valige Hanked > Seadistus > Pakkumiskutse > Kutse tüüp.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="d6ed6-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-111">Click New.</span></span>
3. <span data-ttu-id="d6ed6-112">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d6ed6-113">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d6ed6-114">Valige väljalt Hindamismeetod hindamismeetod, mida soovite selle kutse tüübi puhul kasutada.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="d6ed6-115">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-115">Click Save.</span></span>
7. <span data-ttu-id="d6ed6-116">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="d6ed6-117">Kutse tüübi kasutamine</span><span class="sxs-lookup"><span data-stu-id="d6ed6-117">Use the solicitation type</span></span>
1. <span data-ttu-id="d6ed6-118">Avage Hanked > Pakkumiskutsed > Kõik pakkumiskutsed.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="d6ed6-119">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-119">Click New.</span></span>
3. <span data-ttu-id="d6ed6-120">Valige väljalt Kutse tüüp äsja loodud kutse tüüp.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
    *   
4. <span data-ttu-id="d6ed6-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-121">Click OK.</span></span>
5. <span data-ttu-id="d6ed6-122">Klõpsake valikut Hindamiskriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="d6ed6-123">Kuvatud hindamiskriteeriumid on kutse tüübiga seotud hindamismeetodi omad.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="d6ed6-124">Saate sellele lehele kriteeriume lisada või kustutada.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="d6ed6-125">Võimalik on ka uute kriteeriumide lisamine, kopeerides need muudest hindamismeetoditest.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="d6ed6-126">Klõpsake valikut Kopeeri kriteerium.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="d6ed6-127">Valige või sisestage väärtus väljal Hindamismeetod.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="d6ed6-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-128">Click OK.</span></span>
9. <span data-ttu-id="d6ed6-129">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d6ed6-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]