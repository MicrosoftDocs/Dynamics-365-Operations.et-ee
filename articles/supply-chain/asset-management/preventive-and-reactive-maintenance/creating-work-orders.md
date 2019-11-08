---
title: Töökäskude loomine
description: Selles teemas tutvustatakse, kuidas luua töökäske varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
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
ms.openlocfilehash: 6e910b2400106baf9f9dc06f6bc0d3daee8e4a43
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570072"
---
# <a name="creating-work-orders"></a><span data-ttu-id="b2160-103">Töökäskude loomine</span><span class="sxs-lookup"><span data-stu-id="b2160-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b2160-104">Kui olete plaaninud ennetavaid hooldustöid, on järgmine etapp luua tööde jaoks töökäsud.</span><span class="sxs-lookup"><span data-stu-id="b2160-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="b2160-105">Seda saab teha ühes hooldusgraafikus.</span><span class="sxs-lookup"><span data-stu-id="b2160-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="b2160-106">Plaanitud töödel võib hooldusgraafikus olla eri viitetüüp.</span><span class="sxs-lookup"><span data-stu-id="b2160-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="b2160-107">Viite tüüp</span><span class="sxs-lookup"><span data-stu-id="b2160-107">Reference type</span></span> | <span data-ttu-id="b2160-108">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b2160-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2160-109">Hoolduskavad</span><span class="sxs-lookup"><span data-stu-id="b2160-109">Maintenance plans</span></span>     | <span data-ttu-id="b2160-110">Ennetavad hooldustööd põhinevad hoolduskava tüüpidel "Aeg" või "Loendur".</span><span class="sxs-lookup"><span data-stu-id="b2160-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="b2160-111">Hoolduskorrad</span><span class="sxs-lookup"><span data-stu-id="b2160-111">Maintenance rounds</span></span>    | <span data-ttu-id="b2160-112">Ennetavad hooldustööd, mis sisaldavad mitut vara, nõuavad sarnast tüüpi hooldust.</span><span class="sxs-lookup"><span data-stu-id="b2160-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="b2160-113">Hooldusnõue</span><span class="sxs-lookup"><span data-stu-id="b2160-113">Maintenance request</span></span>   | <span data-ttu-id="b2160-114">Käsitsi loodud nõue vara hoolduseks või paranduseks, mille saab teisendada töökäsuks.</span><span class="sxs-lookup"><span data-stu-id="b2160-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="b2160-115">Klõpsake **Varahaldus** > **Üldine** > **Kõik hooldusgraafikud** või **Avatud hooldusgraafiku read** või **Avatud hooldusgraafiku kaustad**.</span><span class="sxs-lookup"><span data-stu-id="b2160-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="b2160-116">Valige plaanitud hooldustööd, mille jaoks soovite luua töökäsu ja klõpsake **Töökäsk**.</span><span class="sxs-lookup"><span data-stu-id="b2160-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="b2160-117">Dialoogis **Töökäskude loomine** kuvatakse eelarve tundide koguarvu valitud ridade kohta väljal **Hoolduse eelarve tunnid**.</span><span class="sxs-lookup"><span data-stu-id="b2160-117">In the **Create work orders** dialog, the total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="b2160-118">Jaotises **Parameetrid** valige mitu töökäsku soovite luua.</span><span class="sxs-lookup"><span data-stu-id="b2160-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="b2160-119">Saate ühe hooldusgraafiku rea kohta luua ühe töökäsu või mitu töökäsku, sõltuvalt teie valikutest jaotises **Üks töökäsk**.</span><span class="sxs-lookup"><span data-stu-id="b2160-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="b2160-120">Valige **Töökäsu tüüp**, mida kasutatakse kõigi teie loodavate töökäskude puhul.</span><span class="sxs-lookup"><span data-stu-id="b2160-120">Select a **Work order type** that will be used on all the work orders you create.</span></span> <span data-ttu-id="b2160-121">Allolevalt jooniselt näete näidet dialoogist **Töökäskude loomine**.</span><span class="sxs-lookup"><span data-stu-id="b2160-121">The illustration below shows an example of the **Create work orders** dialog.</span></span>

![Joonis 1](media/18-preventive-maintenance.png)

5. <span data-ttu-id="b2160-123">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2160-123">Click **OK**.</span></span> <span data-ttu-id="b2160-124">Luuakse üks või mitu töökäsku.</span><span class="sxs-lookup"><span data-stu-id="b2160-124">One or more work orders are created.</span></span>

