---
title: Töökäsule vea lisamine
description: See teema kirjeldab, kuidas lisada vea registreerimisi töökäskudele Varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875614"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="78832-103">Töökäsule vea lisamine</span><span class="sxs-lookup"><span data-stu-id="78832-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="78832-104">Vea kujundajas seadistatud vigu saate lisada töökäskudele.</span><span class="sxs-lookup"><span data-stu-id="78832-104">You can add faults set up in the fault designer to a work order.</span></span> <span data-ttu-id="78832-105">Töökäsus valitud vara peab sisaldama varade tüüpe, millega on seotud üks või rohkem veakirjet.</span><span class="sxs-lookup"><span data-stu-id="78832-105">The asset selected in the work order must contain asset types that have one or more fault records connected to it.</span></span> <span data-ttu-id="78832-106">Lisateavet häälestuse kohta leiate jaotisest [Veahaldus](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="78832-106">Read more about setup in the [Fault management](../setup-for-work-orders/fault-management.md) section.</span></span>

1. <span data-ttu-id="78832-107">Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik Töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="78832-107">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="78832-108">Valige loendist töökäsk, milles soovite vea registreerimist teha, ja klõpsake nuppu **Vara viga**.</span><span class="sxs-lookup"><span data-stu-id="78832-108">In the list, select the work order on which you want to make a fault registration and click **Asset fault**.</span></span>

3. <span data-ttu-id="78832-109">Kiirkaardil **Sümptomid** klõpsake valikut **Lisa rida**.</span><span class="sxs-lookup"><span data-stu-id="78832-109">On the **Symptoms** FastTab, click **Add line**.</span></span> <span data-ttu-id="78832-110">Järjestikune vea number sisestatakse automaatselt **Viga** väljale.</span><span class="sxs-lookup"><span data-stu-id="78832-110">A sequential fault number is automatically inserted in the **Fault** field.</span></span>

4. <span data-ttu-id="78832-111">Valige sobiv sümptom väljal **Vea sümptom**.</span><span class="sxs-lookup"><span data-stu-id="78832-111">Select the relevant symptom in the **Fault symptom** field.</span></span>

5. <span data-ttu-id="78832-112">Valige **Vea ala** ja **Vea tüüp**.</span><span class="sxs-lookup"><span data-stu-id="78832-112">Select **Fault area** and **Fault type**.</span></span>

6. <span data-ttu-id="78832-113">Väljale **Vea kuupäev** lisatakse automaatselt praegune kuupäev.</span><span class="sxs-lookup"><span data-stu-id="78832-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="78832-114">Vajadusel saate valida teise kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="78832-114">You can select another date, if necessary.</span></span>

7. <span data-ttu-id="78832-115">**Valitud sümptomi põhjused** kiirkaardil lisage probleemi põhjust kirjeldav rida.</span><span class="sxs-lookup"><span data-stu-id="78832-115">On the **Causes for selected symptom** FastTab, add a line describing the cause of the problem.</span></span>

8. <span data-ttu-id="78832-116">**Valitud sümptomi parandusmeetmed** kiirkaardil lisage võimalikku probleemi lahendust kirjeldav rida.</span><span class="sxs-lookup"><span data-stu-id="78832-116">On the **Remedies for selected symptom** FastTab, add a line describing a possible solution to the problem.</span></span>

9. <span data-ttu-id="78832-117">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="78832-117">Click **Save**.</span></span>

![Joonis 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="78832-119">Kuva vara vead</span><span class="sxs-lookup"><span data-stu-id="78832-119">View asset faults</span></span>

<span data-ttu-id="78832-120">**Vara vead** loendis saate ülevaate kõigist vigadest, mis on registreeritud varadesse.</span><span class="sxs-lookup"><span data-stu-id="78832-120">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="78832-121">Nimekirja avamiseks klõpsake **Varahaldus** > **Päringud** > **Vara viga** > **Vara vead**.</span><span class="sxs-lookup"><span data-stu-id="78832-121">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults** to open the list.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="78832-122">Prindi vara vea aruanne</span><span class="sxs-lookup"><span data-stu-id="78832-122">Print asset fault report</span></span>

<span data-ttu-id="78832-123">Loendilehelt **Kõik varad** saate printida vara vea aruande, kus kuvatakse kõik vea registreerimised, samuti vea statistika graafiline ülevaade.</span><span class="sxs-lookup"><span data-stu-id="78832-123">From the **All assets** list page, you can print an asset fault report displaying all fault registrations as well as a graphic overview of fault statistics.</span></span>

1. <span data-ttu-id="78832-124">Klõpsake **Varahaldus** > **Üldine** > **Varad** > **Kõik varad**.</span><span class="sxs-lookup"><span data-stu-id="78832-124">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="78832-125">Valige **Varad** loendist vara, mille kohta soovite vea aurannet printida.</span><span class="sxs-lookup"><span data-stu-id="78832-125">In the **Assets** list, select the asset for which you want to print a fault report.</span></span>

3. <span data-ttu-id="78832-126">Vahekaardil **Üldine** > **Aruannete osa** klõpsake **Vara viga**.</span><span class="sxs-lookup"><span data-stu-id="78832-126">On the **General** tab > **Reports section**, click **Asset fault**.</span></span>

4. <span data-ttu-id="78832-127">Sisestage kindel periood või valige vea tüüp.</span><span class="sxs-lookup"><span data-stu-id="78832-127">Insert a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="78832-128">Aruande printimiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="78832-128">Click **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="78832-129">Saate printida ka vea aruande mitme vara või vara tüüpide jaoks, kui klõpsate **Varahaldus** > **Aruanded** > **Varad** > **Vara viga**.</span><span class="sxs-lookup"><span data-stu-id="78832-129">You can also print a fault report for several assets or asset types by clicking **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

