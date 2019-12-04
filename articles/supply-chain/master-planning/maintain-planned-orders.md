---
title: Plaanitud tellimuste haldamine
description: See teema pakub teavet plaanitud tellimuste haldamise kohta. See kirjeldab, kuidas plaanitud tellimuste olekut värskendada, neid kinnitada ja filtreerida plaanitud tellimusi, millel on sama olek, nagu valitud plaanitud tellimusel.
author: roxanadiaconu
manager: AnnBe
ms.date: 11/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68bccb632255eac975dc150cf322d4c579ff2f24
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813772"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="7e497-104">Plaanitud tellimuste haldamine</span><span class="sxs-lookup"><span data-stu-id="7e497-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e497-105">See teema pakub teavet plaanitud tellimuste haldamise kohta.</span><span class="sxs-lookup"><span data-stu-id="7e497-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="7e497-106">See kirjeldab, kuidas plaanitud tellimuste olekut värskendada, neid kinnitada ja filtreerida plaanitud tellimusi, millel on sama olek, nagu valitud plaanitud tellimusel.</span><span class="sxs-lookup"><span data-stu-id="7e497-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="7e497-107">Saate planeeritud tellimusi hallata tööruumis **Koondplaneerimine**, loendis **Plaanitud tellimus** või loendites **Plaanitud tootmistellimused**, **Plaanitud ostutellimused** ja **Plaanitud üleviimised**.</span><span class="sxs-lookup"><span data-stu-id="7e497-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="7e497-108">Plaanitud tellimuse olek</span><span class="sxs-lookup"><span data-stu-id="7e497-108">Planned order status</span></span>
<span data-ttu-id="7e497-109">Saate edenemist jälgida välja **Olek** abil.</span><span class="sxs-lookup"><span data-stu-id="7e497-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="7e497-110">Kasutatakse järgmisi väärtusi.</span><span class="sxs-lookup"><span data-stu-id="7e497-110">The following values are used:</span></span>

-   <span data-ttu-id="7e497-111">Kui koondplaneerimine loob plaanitud tellimused, on nende olek **Töötlemata**.</span><span class="sxs-lookup"><span data-stu-id="7e497-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="7e497-112">Kui otsustate plaanitud tellimust mitte kinnitada, saate sellele määrata oleku **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="7e497-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="7e497-113">Kui soovite kinnitada plaanitud tellimuse, saate määrata selle olekuks **Kinnitatud**.</span><span class="sxs-lookup"><span data-stu-id="7e497-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="7e497-114">Olekuga **Kinnitatud** plaanitud tellimusi arvestatakse koondplaneerimisel, nii et neid ei muudeta ega kustutata hilisema koondplaneerimise käivitamise ajal.</span><span class="sxs-lookup"><span data-stu-id="7e497-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted during a later master planning run.</span></span> 

## <a name="firming-planned-orders"></a><span data-ttu-id="7e497-115">Plaanitud tellimuste kinnitamine</span><span class="sxs-lookup"><span data-stu-id="7e497-115">Firming planned orders</span></span> 
<span data-ttu-id="7e497-116">Plaanitud tellimuste kinnitamisega luuakse tegelikud tellimused.</span><span class="sxs-lookup"><span data-stu-id="7e497-116">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="7e497-117">Neid nimetatakse ka *väljastatud* või *avatud tellimusteks*.</span><span class="sxs-lookup"><span data-stu-id="7e497-117">These are also know as *released* or *open orders*.</span></span> <span data-ttu-id="7e497-118">Kui plaanitud tellimus on kinnitatud, teisaldatakse see asjakohase mooduli tellimuste jaotisse.</span><span class="sxs-lookup"><span data-stu-id="7e497-118">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="7e497-119">Lehel **Plaanitud tellimused** saate valida kaks kinnitamissuvandit.</span><span class="sxs-lookup"><span data-stu-id="7e497-119">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="7e497-120">**Kinnita** – sellega kinnitatakse üks või mitu valitud plaanitud tellimust.</span><span class="sxs-lookup"><span data-stu-id="7e497-120">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="7e497-121">**Kinnita kõik** – sellega kinnitatakse kõik filtris olevad plaanitud tellimused.</span><span class="sxs-lookup"><span data-stu-id="7e497-121">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="7e497-122">Valides suvandi **Kinnita kõik** ei pea te valima plaanitud tellimust, kõiki filtris olevad plaanitud tellimused kinnitatakse.</span><span class="sxs-lookup"><span data-stu-id="7e497-122">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="7e497-123">See suvand võib olla kasulik juhul, kui kinnitate suure hulga plaanitud tellimusi.</span><span class="sxs-lookup"><span data-stu-id="7e497-123">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="7e497-124">**Kinnitamise ajaloo** jaotises **Plaanitud tellimuste vorm > Vaade > Kinnitamise ajalugu** saate jälgida kinnitatud plaanitud tellimust.</span><span class="sxs-lookup"><span data-stu-id="7e497-124">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="7e497-125">Paralleelne kinnitamine</span><span class="sxs-lookup"><span data-stu-id="7e497-125">Parallelize firming</span></span>
<span data-ttu-id="7e497-126">Kui plaanite kinnitada korraga mitu tellimust, võib käituse paralleelimine parandada käitusaega või jõudlust.</span><span class="sxs-lookup"><span data-stu-id="7e497-126">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="7e497-127">See valik on saadaval mitme plaanitud tellimuse kinnitamisel kas suvandiga **Kinnita** või **Kinnita kõik**.</span><span class="sxs-lookup"><span data-stu-id="7e497-127">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="7e497-128">Saadaval on järgmised parameetrid.</span><span class="sxs-lookup"><span data-stu-id="7e497-128">The following parameters are available:</span></span>

-   <span data-ttu-id="7e497-129">**Kinnitamise paralleelimine** – kui **Jah**, siis paralleelitakse kinnitamisprotsessi lõimede arvuga, mis on määratletud väärtusega **Lõimede arv**.</span><span class="sxs-lookup"><span data-stu-id="7e497-129">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="7e497-130">**Lõimede arv** – reguleerib kinnitamise paralleelimiseks kasutatavate lõimede arvu.</span><span class="sxs-lookup"><span data-stu-id="7e497-130">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="7e497-131">Parameeter kuvatakse ainult siis, kui valiku **Kinnitamise paralleelimine** väärtuseks on seatud **Jah**.</span><span class="sxs-lookup"><span data-stu-id="7e497-131">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>


<a name="additional-resources"></a><span data-ttu-id="7e497-132">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="7e497-132">Additional resources</span></span>
--------

[<span data-ttu-id="7e497-133">Koondplaanide ülevaade</span><span class="sxs-lookup"><span data-stu-id="7e497-133">Master plans overview</span></span>](master-plans.md)



