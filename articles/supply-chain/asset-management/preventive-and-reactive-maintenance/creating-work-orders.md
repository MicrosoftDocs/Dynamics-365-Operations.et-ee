---
title: Töökäskude loomine
description: Selles teemas tutvustatakse, kuidas luua töökäske varahalduses.
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b23ed3251b2f6cf4f34b423ce2f85301d6ab31a1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875604"
---
# <a name="creating-work-orders"></a><span data-ttu-id="77d48-103">Töökäskude loomine</span><span class="sxs-lookup"><span data-stu-id="77d48-103">Creating work orders</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="77d48-104">Kui olete plaaninud ennetavaid hooldustöid, on järgmine etapp luua tööde jaoks töökäsud.</span><span class="sxs-lookup"><span data-stu-id="77d48-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="77d48-105">Seda saab teha ühes hooldusgraafikus.</span><span class="sxs-lookup"><span data-stu-id="77d48-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="77d48-106">Plaanitud töödel võib hooldusgraafikus olla eri viitetüüp.</span><span class="sxs-lookup"><span data-stu-id="77d48-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="77d48-107">Viite tüüp</span><span class="sxs-lookup"><span data-stu-id="77d48-107">Reference type</span></span> | <span data-ttu-id="77d48-108">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="77d48-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77d48-109">Hoolduskavad</span><span class="sxs-lookup"><span data-stu-id="77d48-109">Maintenance plans</span></span>     | <span data-ttu-id="77d48-110">Ennetavad hooldustööd põhinevad hoolduskava tüüpidel "Aeg" või "Loendur".</span><span class="sxs-lookup"><span data-stu-id="77d48-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="77d48-111">Hoolduskorrad</span><span class="sxs-lookup"><span data-stu-id="77d48-111">Maintenance rounds</span></span>    | <span data-ttu-id="77d48-112">Ennetavad hooldustööd, mis sisaldavad mitut vara, nõuavad sarnast tüüpi hooldust.</span><span class="sxs-lookup"><span data-stu-id="77d48-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="77d48-113">Hooldusnõue</span><span class="sxs-lookup"><span data-stu-id="77d48-113">Maintenance request</span></span>   | <span data-ttu-id="77d48-114">Käsitsi loodud nõue vara hoolduseks või paranduseks, mille saab teisendada töökäsuks.</span><span class="sxs-lookup"><span data-stu-id="77d48-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="77d48-115">Klõpsake **Varahaldus** > **Üldine** > **Kõik hooldusgraafikud** või **Avatud hooldusgraafiku read** või **Avatud hooldusgraafiku kaustad**.</span><span class="sxs-lookup"><span data-stu-id="77d48-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="77d48-116">Valige plaanitud hooldustööd, mille jaoks soovite luua töökäsu ja klõpsake **Töökäsk**.</span><span class="sxs-lookup"><span data-stu-id="77d48-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="77d48-117">Eelarve tundide koguarvu valitud ridade kohta kuvatakse väljale **Hoolduse eelarve tunnid**.</span><span class="sxs-lookup"><span data-stu-id="77d48-117">The total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="77d48-118">Jaotises **Parameetrid** valige mitu töökäsku soovite luua.</span><span class="sxs-lookup"><span data-stu-id="77d48-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="77d48-119">Saate ühe hooldusgraafiku rea kohta luua ühe töökäsu või mitu töökäsku, sõltuvalt teie valikutest jaotises **Üks töökäsk**.</span><span class="sxs-lookup"><span data-stu-id="77d48-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="77d48-120">Valige **Töökäsu tüüp**, mida kasutatakse kõigi teie loodavate töökäskude puhul.</span><span class="sxs-lookup"><span data-stu-id="77d48-120">Select a **Work order type** that will be used on all the work orders you create.</span></span>

5. <span data-ttu-id="77d48-121">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="77d48-121">Click **OK**.</span></span> <span data-ttu-id="77d48-122">Luuakse üks või mitu töökäsku.</span><span class="sxs-lookup"><span data-stu-id="77d48-122">One or more work orders are created.</span></span>

![Joonis 1](media/18-preventive-maintenance.png)

