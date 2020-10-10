---
title: Plaanitud tellimuste haldamine
description: See teema pakub teavet plaanitud tellimuste haldamise kohta. See kirjeldab, kuidas plaanitud tellimuste olekut värskendada, neid kinnitada ja filtreerida plaanitud tellimusi, millel on sama olek, nagu valitud plaanitud tellimusel.
author: roxanadiaconu
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b0becf73ddde6add4076bd5b47a49eb3a0976206
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/24/2020
ms.locfileid: "3886892"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="bb625-104">Plaanitud tellimuste haldamine</span><span class="sxs-lookup"><span data-stu-id="bb625-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb625-105">See teema pakub teavet plaanitud tellimuste haldamise kohta.</span><span class="sxs-lookup"><span data-stu-id="bb625-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="bb625-106">See kirjeldab, kuidas plaanitud tellimuste olekut värskendada, neid kinnitada ja filtreerida plaanitud tellimusi, millel on sama olek, nagu valitud plaanitud tellimusel.</span><span class="sxs-lookup"><span data-stu-id="bb625-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="bb625-107">Saate planeeritud tellimusi hallata tööruumis **Koondplaneerimine**, loendis **Plaanitud tellimus** või loendites **Plaanitud tootmistellimused**, **Plaanitud ostutellimused** ja **Plaanitud üleviimised**.</span><span class="sxs-lookup"><span data-stu-id="bb625-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="bb625-108">Plaanitud tellimuse olek</span><span class="sxs-lookup"><span data-stu-id="bb625-108">Planned order status</span></span>
<span data-ttu-id="bb625-109">Saate edenemist jälgida välja **Olek** abil.</span><span class="sxs-lookup"><span data-stu-id="bb625-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="bb625-110">Kasutatakse järgmisi väärtusi.</span><span class="sxs-lookup"><span data-stu-id="bb625-110">The following values are used:</span></span>

-   <span data-ttu-id="bb625-111">Kui koondplaneerimine loob plaanitud tellimused, on nende olek **Töötlemata**.</span><span class="sxs-lookup"><span data-stu-id="bb625-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="bb625-112">Kui otsustate plaanitud tellimust mitte kinnitada, saate sellele määrata oleku **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="bb625-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="bb625-113">Kui soovite kinnitada plaanitud tellimuse, saate määrata selle olekuks **Kinnitatud**.</span><span class="sxs-lookup"><span data-stu-id="bb625-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="bb625-114">Olekuga **Kinnitatud** plaanitud tellimusi arvestatakse koondplaneerimisel, nii et neid ei muudeta ega kustutata hilisema koondplaneerimise käivitamise ajal.</span><span class="sxs-lookup"><span data-stu-id="bb625-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted during a later master planning run.</span></span> <span data-ttu-id="bb625-115">Selle saavutamiseks kopeerib planeerimisloogika koondplaneerimise ajal **kinnitatud** plaanitud tellimused vana plaani versioonist uude plaani versiooni.</span><span class="sxs-lookup"><span data-stu-id="bb625-115">To achieve this, the planning logic copies the **Approved** planned orders from the old plan version to the new plan version during master planning.</span></span>

## <a name="firming-planned-orders"></a><span data-ttu-id="bb625-116">Plaanitud tellimuste kinnitamine</span><span class="sxs-lookup"><span data-stu-id="bb625-116">Firming planned orders</span></span> 
<span data-ttu-id="bb625-117">Plaanitud tellimuste kinnitamisega luuakse tegelikud tellimused.</span><span class="sxs-lookup"><span data-stu-id="bb625-117">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="bb625-118">Need on tuntud ka kui *väljastatud* või *avatud tellimused*.</span><span class="sxs-lookup"><span data-stu-id="bb625-118">These are also known as *released* or *open orders*.</span></span> <span data-ttu-id="bb625-119">Kui plaanitud tellimus on kinnitatud, teisaldatakse see asjakohase mooduli tellimuste jaotisse.</span><span class="sxs-lookup"><span data-stu-id="bb625-119">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="bb625-120">Lehel **Plaanitud tellimused** saate valida kaks kinnitamissuvandit.</span><span class="sxs-lookup"><span data-stu-id="bb625-120">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="bb625-121">**Kinnita** – sellega kinnitatakse üks või mitu valitud plaanitud tellimust.</span><span class="sxs-lookup"><span data-stu-id="bb625-121">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="bb625-122">**Kinnita kõik** – sellega kinnitatakse kõik filtris olevad plaanitud tellimused.</span><span class="sxs-lookup"><span data-stu-id="bb625-122">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="bb625-123">Valides suvandi **Kinnita kõik** ei pea te valima plaanitud tellimust, kõiki filtris olevad plaanitud tellimused kinnitatakse.</span><span class="sxs-lookup"><span data-stu-id="bb625-123">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="bb625-124">See suvand võib olla kasulik juhul, kui kinnitate suure hulga plaanitud tellimusi.</span><span class="sxs-lookup"><span data-stu-id="bb625-124">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="bb625-125">**Kinnitamise ajaloo** jaotises **Plaanitud tellimuste vorm > Vaade > Kinnitamise ajalugu** saate jälgida kinnitatud plaanitud tellimust.</span><span class="sxs-lookup"><span data-stu-id="bb625-125">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="bb625-126">Paralleelne kinnitamine</span><span class="sxs-lookup"><span data-stu-id="bb625-126">Parallelize firming</span></span>
<span data-ttu-id="bb625-127">Kui plaanite kinnitada korraga mitu tellimust, võib käituse paralleelimine parandada käitusaega või jõudlust.</span><span class="sxs-lookup"><span data-stu-id="bb625-127">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="bb625-128">See valik on saadaval mitme plaanitud tellimuse kinnitamisel kas suvandiga **Kinnita** või **Kinnita kõik**.</span><span class="sxs-lookup"><span data-stu-id="bb625-128">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="bb625-129">Saadaval on järgmised parameetrid.</span><span class="sxs-lookup"><span data-stu-id="bb625-129">The following parameters are available:</span></span>

-   <span data-ttu-id="bb625-130">**Kinnitamise paralleelimine** – kui **Jah**, siis paralleelitakse kinnitamisprotsessi lõimede arvuga, mis on määratletud väärtusega **Lõimede arv**.</span><span class="sxs-lookup"><span data-stu-id="bb625-130">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="bb625-131">**Lõimede arv** – reguleerib kinnitamise paralleelimiseks kasutatavate lõimede arvu.</span><span class="sxs-lookup"><span data-stu-id="bb625-131">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="bb625-132">Parameeter kuvatakse ainult siis, kui valiku **Kinnitamise paralleelimine** väärtuseks on seatud **Jah**.</span><span class="sxs-lookup"><span data-stu-id="bb625-132">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>

> [!NOTE]
> <span data-ttu-id="bb625-133">Suvandi **Kinnitamise paralleelimine** valikut näidatakse ainult siis, kui teil on kinnitamiseks valitud rohkem kui üks plaanitud tellimus.</span><span class="sxs-lookup"><span data-stu-id="bb625-133">The option for **Parallelize firming** is only shown when you have more than one planned order selected for firming.</span></span>

<a name="additional-resources"></a><span data-ttu-id="bb625-134">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="bb625-134">Additional resources</span></span>
--------

[<span data-ttu-id="bb625-135">Koondplaanide ülevaade</span><span class="sxs-lookup"><span data-stu-id="bb625-135">Master plans overview</span></span>](master-plans.md)



