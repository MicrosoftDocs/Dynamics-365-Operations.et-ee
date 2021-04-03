---
title: Töökäsule vea lisamine
description: See teema kirjeldab, kuidas lisada vea registreerimisi töökäskudele Varahalduses.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 489add5befe3660ad49e238b659bc8adbe1418a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263754"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="dbd75-103">Töökäsule vea lisamine</span><span class="sxs-lookup"><span data-stu-id="dbd75-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="dbd75-104">Saate lisada töökäsule vea kujundajas seadistatud vigu.</span><span class="sxs-lookup"><span data-stu-id="dbd75-104">You can add faults that were set up in the fault designer to a work order.</span></span> <span data-ttu-id="dbd75-105">Vähemalt üks veakirje peab olema seotud varatüüpidega, mida kasutatakse töökäsus valitud vara korral.</span><span class="sxs-lookup"><span data-stu-id="dbd75-105">One or more fault records must be connected to the asset types that are used for the asset that is selected in the work order.</span></span> <span data-ttu-id="dbd75-106">Häälestuse kohta leiate lisateavet jaotisest [Veahaldus](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="dbd75-106">For more information about the setup, see [Fault management](../setup-for-work-orders/fault-management.md).</span></span>

1. <span data-ttu-id="dbd75-107">Valie **Varahaldus** > **Üldine** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="dbd75-107">Select **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="dbd75-108">Valige töökäsk, mille kohta registreerida viga ja seejärel valige toimingupaani vahekaardil **Töökäsk** rühma **Vara** alt valik **Vara viga**.</span><span class="sxs-lookup"><span data-stu-id="dbd75-108">Select the work order to make a fault registration on, and then, on the Action Pane, on the **Work order** tab, in the **Asset** group, select **Asset fault**.</span></span>

3. <span data-ttu-id="dbd75-109">Valige kiirkaardil **Sümptomid** valik **Lisa rida**.</span><span class="sxs-lookup"><span data-stu-id="dbd75-109">On the **Symptoms** FastTab, select **Add line**.</span></span> <span data-ttu-id="dbd75-110">Järjestikune vea number sisestatakse automaatselt väljale **Viga**.</span><span class="sxs-lookup"><span data-stu-id="dbd75-110">A sequential fault number is automatically entered in the **Fault** field.</span></span>

4. <span data-ttu-id="dbd75-111">Valige väljal **Vea sümptom** asjakohane sümptom.</span><span class="sxs-lookup"><span data-stu-id="dbd75-111">In the **Fault symptom** field, select the relevant symptom.</span></span>

5. <span data-ttu-id="dbd75-112">Valige väljadel **Vea ala** ja **Vea tüüp** asjakohased väärtused.</span><span class="sxs-lookup"><span data-stu-id="dbd75-112">In the **Fault area** and **Fault type** fields, select the appropriate values.</span></span>

6. <span data-ttu-id="dbd75-113">Väljale **Vea kuupäev** lisatakse automaatselt praegune kuupäev.</span><span class="sxs-lookup"><span data-stu-id="dbd75-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="dbd75-114">Vajadisel saate valida mõne muu kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="dbd75-114">You can select a different date as you require.</span></span>

7. <span data-ttu-id="dbd75-115">Lisage kiirkaardil **Valitud sümptomi põhjused** probleemi põhjust kirjeldav rida.</span><span class="sxs-lookup"><span data-stu-id="dbd75-115">On the **Causes for selected symptom** FastTab, add a line to describe the cause of the issue.</span></span>

8. <span data-ttu-id="dbd75-116">Lisage kiirkaardil **Valitud sümptomi parandusmeetmed** probleemi võimalikku lahendust kirjeldav rida.</span><span class="sxs-lookup"><span data-stu-id="dbd75-116">On the **Remedies for selected symptom** FastTab, add a line to describe a possible solution to the issue.</span></span>

9. <span data-ttu-id="dbd75-117">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dbd75-117">Select **Save**.</span></span>

<span data-ttu-id="dbd75-118">Alljärgneval joonisel on esitatud vea registreerimise näide.</span><span class="sxs-lookup"><span data-stu-id="dbd75-118">The illustration below shows an example of a fault registration.</span></span>

![Joonis 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="dbd75-120">Kuva vara vead</span><span class="sxs-lookup"><span data-stu-id="dbd75-120">View asset faults</span></span>

<span data-ttu-id="dbd75-121">**Vara vead** loendis saate ülevaate kõigist vigadest, mis on registreeritud varadesse.</span><span class="sxs-lookup"><span data-stu-id="dbd75-121">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="dbd75-122">Loendilehel **Vara vead** saate ülevaate kõigist vigadest, mis on varade kohta registreeritud.</span><span class="sxs-lookup"><span data-stu-id="dbd75-122">On the **Asset faults** list page, you can get an overview of all faults that have been registered on assets.</span></span> <span data-ttu-id="dbd75-123">Lehe avamiseks valige **Varahaldus** > **Päringud** > **Vara viga** > **Vara vead**.</span><span class="sxs-lookup"><span data-stu-id="dbd75-123">To open the page, select **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="dbd75-124">Prindi vara vea aruanne</span><span class="sxs-lookup"><span data-stu-id="dbd75-124">Print asset fault report</span></span>

<span data-ttu-id="dbd75-125">Loendilehelt **Kõik varad** saate printida vara vea aruande, kus kuvatakse kõik vea registreerimised ja veastatistika graafiline ülevaade.</span><span class="sxs-lookup"><span data-stu-id="dbd75-125">From the **All assets** list page, you can print an asset fault report that shows all fault registrations and a graphical overview of fault statistics.</span></span>

1. <span data-ttu-id="dbd75-126">Valige **Varahaldus** > **Ühised** > **Varad** > **Kõik varad**.</span><span class="sxs-lookup"><span data-stu-id="dbd75-126">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="dbd75-127">Valige vara, mille kohta printida aruanne.</span><span class="sxs-lookup"><span data-stu-id="dbd75-127">Select the asset to print a fault report for.</span></span>

3. <span data-ttu-id="dbd75-128">Valige toimingupaani vahekaardil **Üldine** grupis **Aruanded** valikut **Vara viga**.</span><span class="sxs-lookup"><span data-stu-id="dbd75-128">On the Action Pane, on the **General** tab, in the **Reports** group, select **Asset fault**.</span></span>

4. <span data-ttu-id="dbd75-129">Sisestage konkreetne periood või valige vea tüüp.</span><span class="sxs-lookup"><span data-stu-id="dbd75-129">Enter a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="dbd75-130">Aruande printimiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="dbd75-130">Select **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="dbd75-131">Veaaruande printimiseks mitme vara või varatüübi kohta valige **Varahaldus** > **Aruanded** > **Varad** > **Vara viga**.</span><span class="sxs-lookup"><span data-stu-id="dbd75-131">To print a fault report for several assets or asset types, select **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]