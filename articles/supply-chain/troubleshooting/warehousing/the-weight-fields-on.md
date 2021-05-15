---
title: Laadungi ridade kaaluväljad ei vasta laadungi kaaluväljadele
description: Laadungi ridade kaaluväljad ei vasta laadungi kaaluväljadele
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 639b82a9d46b74f179d6904d2c3b8e7dfb813b58
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924347"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a><span data-ttu-id="c5680-103">Laadungi ridade kaaluväljad ei vasta laadungi kaaluväljadele</span><span class="sxs-lookup"><span data-stu-id="c5680-103">The weight fields on load lines don't match the weight fields on the load</span></span>

<span data-ttu-id="c5680-104">Tõrkekoodid: WHSLaadungKaalRidadelEiKlapiLaadungHoiatus</span><span class="sxs-lookup"><span data-stu-id="c5680-104">Error codes: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span></span>

## <a name="symptoms"></a><span data-ttu-id="c5680-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="c5680-105">Symptoms</span></span>

<span data-ttu-id="c5680-106">Süsteem näitab järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="c5680-106">The system shows the following error message:</span></span>

> <span data-ttu-id="c5680-107">Laadungi ridade kaaluväljad ei vasta laadungi kaaluväljadele %1.</span><span class="sxs-lookup"><span data-stu-id="c5680-107">The weight fields on load lines do not match the weight fields on load %1.</span></span> <span data-ttu-id="c5680-108">Käivitage lao laadungi kaalu ühtsuse kontroll kaaluväljade uuesti arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="c5680-108">Run the Warehouse load weight consistency check to recalculate the weight fields.</span></span>

## <a name="cause"></a><span data-ttu-id="c5680-109">Põhjus</span><span class="sxs-lookup"><span data-stu-id="c5680-109">Cause</span></span>

<span data-ttu-id="c5680-110">**Netokaal** ja **Tühikaal** väljad on laadungireal seatud väärtusele *0* (null).</span><span class="sxs-lookup"><span data-stu-id="c5680-110">The **Net weight** and **Tara weight** fields are set to *0* (zero) on the load line.</span></span> <span data-ttu-id="c5680-111">Kaaluväljade väärtuseks ei ole aga toote kaalu mõõtmiste puhul seatud *0*.</span><span class="sxs-lookup"><span data-stu-id="c5680-111">However, the weight fields aren't set to *0* for the weight measurements on the product.</span></span> <span data-ttu-id="c5680-112">Kui laadungireal pole kaaluvälju seatud, võivad mis tahes laadungirea koguse parandused põhjustada laadungi kaalu vale arvutust.</span><span class="sxs-lookup"><span data-stu-id="c5680-112">When weight fields aren't set on the load line, any corrections of the quantity on the load line might cause incorrect weight calculation on the load.</span></span> <span data-ttu-id="c5680-113">See probleem võib ilmneda, kui toote kaalu on pärast laadungirea loomist muudetud.</span><span class="sxs-lookup"><span data-stu-id="c5680-113">This issue might occur if the weights on the product have been changed since the load line was created.</span></span>

## <a name="resolution"></a><span data-ttu-id="c5680-114">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="c5680-114">Resolution</span></span>

<span data-ttu-id="c5680-115">Laadungirea loomisel sisestatakse vaikimisi toote kaaluväljad.</span><span class="sxs-lookup"><span data-stu-id="c5680-115">By default, when a load line is created, the weight fields from the product are entered on it.</span></span> <span data-ttu-id="c5680-116">Kui kaal on null, saate selle *Lao koormuse kaalu ühtsuse kontrolli* funktsiooni abil ümber arvutada.</span><span class="sxs-lookup"><span data-stu-id="c5680-116">If the weight is zero, you can recalculate it by using the *Warehouse load weight consistency check* functionality.</span></span>

1. <span data-ttu-id="c5680-117">Minge **Süsteemi administreerimine \> Perioodilised ülesanded \> Andmebaas \> Ühtsuskontroll**.</span><span class="sxs-lookup"><span data-stu-id="c5680-117">Go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="c5680-118">Dialoogiboksis **Ühtsuse kontroll** seadke väli **Moodul** väärtusele *Laohaldus*.</span><span class="sxs-lookup"><span data-stu-id="c5680-118">In the **Consistency check** dialog box, set the **Module** field to *Warehouse management*.</span></span>
1. <span data-ttu-id="c5680-119">Seadke välja **Kontroll/parandus** väärtuseks *Paranda tõrge*.</span><span class="sxs-lookup"><span data-stu-id="c5680-119">Set the **Check/Fix** field to *Fix error*.</span></span>
1. <span data-ttu-id="c5680-120">Märkeruudu nimekirjas valge **Lao koormuse kaalu ühtsuse kontroll** märkeruut ja veenduge, et ainult see rida märkeruudul on esile tõstetud.</span><span class="sxs-lookup"><span data-stu-id="c5680-120">In the checkbox list, select the **Warehouse load weight consistency check** checkbox, and make sure that only the row for this checkbox is highlighted.</span></span>
1. <span data-ttu-id="c5680-121">Valige märkeruuduloendi ülaosas kolmikpunkti nupp (**...**) ja seejärel valige menüüst **Dialoog**.</span><span class="sxs-lookup"><span data-stu-id="c5680-121">At the top of the checkbox list, select the ellipsis button (**...**), and then select **Dialog** on the menu.</span></span>
1. <span data-ttu-id="c5680-122">Määrake dialoogiboksis **Lao koormuse kaalu ühtsuse kontroll** järgmised väljad, et määratleda kriteeriumid, mille puhul tuleks ühtsuskontrolli käitada:</span><span class="sxs-lookup"><span data-stu-id="c5680-122">In the **Warehouse load weight consistency check** dialog box, set the following fields to specify the criteria that the consistency check should run for:</span></span>

    - <span data-ttu-id="c5680-123">**Laadungi ID:** Määrake laadungi ID.</span><span class="sxs-lookup"><span data-stu-id="c5680-123">**Load ID:** Specify a load ID.</span></span> <span data-ttu-id="c5680-124">Jätke see tühjaks, et kontrollida kõiki laadungi ID-sid.</span><span class="sxs-lookup"><span data-stu-id="c5680-124">Leave this blank to check all load IDs.</span></span>
    - <span data-ttu-id="c5680-125">**Kaubakood:** Määrake kaubakood.</span><span class="sxs-lookup"><span data-stu-id="c5680-125">**Item number:** Specify an item number.</span></span> <span data-ttu-id="c5680-126">Jätke see tühjaks, et kontrollida kõiki kaupu.</span><span class="sxs-lookup"><span data-stu-id="c5680-126">Leave this blank to check all items.</span></span>
    - <span data-ttu-id="c5680-127">**Koormate kaalu ümberarvutamine alati** Määrake selle suvandi väärtuseks *Jah*.</span><span class="sxs-lookup"><span data-stu-id="c5680-127">**Always recalculate weight on loads:** Set this option to *Yes*.</span></span>
    - <span data-ttu-id="c5680-128">**Luba koormaridade kaalu ülekirjutamine:** Määrake selle suvandi väärtuseks *Jah*.</span><span class="sxs-lookup"><span data-stu-id="c5680-128">**Allow overwrite of weight on load lines:** Set this option to *Yes*.</span></span>

1. <span data-ttu-id="c5680-129">Valige **OK**, et sulgeda **Lao koorma kaalu ühtsuse kontroll** dialoogiaken.</span><span class="sxs-lookup"><span data-stu-id="c5680-129">Select **OK** to close the **Warehouse load weight consistency check** dialog box.</span></span>
1. <span data-ttu-id="c5680-130">Valige kolmikpunkt nupp ja seejärel valige menüüst **Teosta**.</span><span class="sxs-lookup"><span data-stu-id="c5680-130">Select the ellipsis button, and then select **Execute** on the menu.</span></span>

<span data-ttu-id="c5680-131">Kaal arvutatakse ümber teie määratud kriteeriumide alusel.</span><span class="sxs-lookup"><span data-stu-id="c5680-131">The weight is recalculated based on the criteria that you specified.</span></span> <span data-ttu-id="c5680-132">Valige **Sõnumi üksikasjade** link, et vaadata ühtsuskontrolli tulemust.</span><span class="sxs-lookup"><span data-stu-id="c5680-132">Select the **Message details** link to view the result of the consistency check.</span></span>
