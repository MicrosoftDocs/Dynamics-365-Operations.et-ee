---
title: Töökäskude loomine
description: Selles teemas tutvustatakse, kuidas luua töökäske varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f94f8bc20753e38ce1cb6eccdfbc85c2e491ffad
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426298"
---
# <a name="creating-work-orders"></a><span data-ttu-id="10f7c-103">Töökäskude loomine</span><span class="sxs-lookup"><span data-stu-id="10f7c-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="10f7c-104">Kui olete plaaninud ennetavaid hooldustöid, on järgmine etapp luua tööde jaoks töökäsud.</span><span class="sxs-lookup"><span data-stu-id="10f7c-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="10f7c-105">Seda saab teha ühes hooldusgraafikus.</span><span class="sxs-lookup"><span data-stu-id="10f7c-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="10f7c-106">Plaanitud töödel võib hooldusgraafikus olla eri viitetüüp.</span><span class="sxs-lookup"><span data-stu-id="10f7c-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="10f7c-107">Viite tüüp</span><span class="sxs-lookup"><span data-stu-id="10f7c-107">Reference type</span></span> | <span data-ttu-id="10f7c-108">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="10f7c-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10f7c-109">Hoolduskavad</span><span class="sxs-lookup"><span data-stu-id="10f7c-109">Maintenance plans</span></span>     | <span data-ttu-id="10f7c-110">Ennetavad hooldustööd põhinevad hoolduskava tüüpidel "Aeg" või "Loendur".</span><span class="sxs-lookup"><span data-stu-id="10f7c-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="10f7c-111">Hoolduskorrad</span><span class="sxs-lookup"><span data-stu-id="10f7c-111">Maintenance rounds</span></span>    | <span data-ttu-id="10f7c-112">Ennetavad hooldustööd, mis sisaldavad mitut vara, nõuavad sarnast tüüpi hooldust.</span><span class="sxs-lookup"><span data-stu-id="10f7c-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="10f7c-113">Hooldusnõue</span><span class="sxs-lookup"><span data-stu-id="10f7c-113">Maintenance request</span></span>   | <span data-ttu-id="10f7c-114">Käsitsi loodud nõue vara hoolduseks või paranduseks, mille saab teisendada töökäsuks.</span><span class="sxs-lookup"><span data-stu-id="10f7c-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="10f7c-115">Klõpsake **Varahaldus** > **Üldine** > **Kõik hooldusgraafikud** või **Avatud hooldusgraafiku read** või **Avatud hooldusgraafiku kaustad**.</span><span class="sxs-lookup"><span data-stu-id="10f7c-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="10f7c-116">Valige plaanitud hooldustööd, mille jaoks soovite luua töökäsu ja klõpsake **Töökäsk**.</span><span class="sxs-lookup"><span data-stu-id="10f7c-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="10f7c-117">Dialoogis **Töökäskude loomine** kuvatakse eelarve tundide koguarvu valitud ridade kohta väljal **Hoolduse eelarve tunnid**.</span><span class="sxs-lookup"><span data-stu-id="10f7c-117">In the **Create work orders** dialog, the total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="10f7c-118">Jaotises **Parameetrid** valige mitu töökäsku soovite luua.</span><span class="sxs-lookup"><span data-stu-id="10f7c-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="10f7c-119">Saate ühe hooldusgraafiku rea kohta luua ühe töökäsu või mitu töökäsku, sõltuvalt teie valikutest jaotises **Üks töökäsk**.</span><span class="sxs-lookup"><span data-stu-id="10f7c-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="10f7c-120">Valige **Töökäsu tüüp**, mida kasutatakse kõigi teie loodavate töökäskude puhul.</span><span class="sxs-lookup"><span data-stu-id="10f7c-120">Select a **Work order type** that will be used on all the work orders you create.</span></span> <span data-ttu-id="10f7c-121">Allolevalt jooniselt näete näidet dialoogist **Töökäskude loomine**.</span><span class="sxs-lookup"><span data-stu-id="10f7c-121">The illustration below shows an example of the **Create work orders** dialog.</span></span>

![Joonis 1](media/18-preventive-maintenance.png)

5. <span data-ttu-id="10f7c-123">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="10f7c-123">Click **OK**.</span></span> <span data-ttu-id="10f7c-124">Luuakse üks või mitu töökäsku.</span><span class="sxs-lookup"><span data-stu-id="10f7c-124">One or more work orders are created.</span></span>

