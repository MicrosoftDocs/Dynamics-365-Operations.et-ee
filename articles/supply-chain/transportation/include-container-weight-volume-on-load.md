---
title: Konteineri kaalu ja mahu lisamine laadimisel
description: Selles teemas kirjeldatakse koormatele konteineri kaalu ja mahu lisamise funktsiooni seadistamist ja rakendamist.
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5b0d8c8a3985d1f49a493615b3c69a9dbe65635f
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="include-container-weight-and-volume-on-load"></a><span data-ttu-id="fd8d9-103">Konteineri kaalu ja mahu lisamine laadimisel</span><span class="sxs-lookup"><span data-stu-id="fd8d9-103">Include container weight and volume on load</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd8d9-104">Koormatele konteineri kaalu ja mahu lisamise funktsioon kajastab täpselt koormatesse minevate konteinerite ja kaupade kogukaalu ning -mahtu.</span><span class="sxs-lookup"><span data-stu-id="fd8d9-104">The functionality for including the container weight and volume on a load gives a clear representation of the total weight and volume of containers and items that are going on a load.</span></span>

<span data-ttu-id="fd8d9-105">Koormas on üks või mitu saadetist ja neis saadetistes on eraldi kaubad, mis kuuluvad ühte või mitmesse müügitellimusse.</span><span class="sxs-lookup"><span data-stu-id="fd8d9-105">A load contains a single shipment or multiple shipments, and these shipments contain distinct items that belong to a single sales order or multiple sales orders.</span></span> <span data-ttu-id="fd8d9-106">Kaubad ladustatakse konteinerisse ja konteineris laaditakse koormasse.</span><span class="sxs-lookup"><span data-stu-id="fd8d9-106">The items are stored inside a container, and containers are loaded on a load.</span></span> <span data-ttu-id="fd8d9-107">Ka väljaspool konteinerit olevad kaubad võivad koorma hulka kuuluda.</span><span class="sxs-lookup"><span data-stu-id="fd8d9-107">Items that are outside a container can also be part of a load.</span></span> <span data-ttu-id="fd8d9-108">Nende tingimuste põhjal arvutab süsteem koorma kaalu ja mahu väärtused, arvestades nii konteinerite kui ka kaupade kaalu ja mahtu.</span><span class="sxs-lookup"><span data-stu-id="fd8d9-108">Based on these conditions, the system calculates values for the weight and volume on the load by considering the weight and volume of both containers and items.</span></span>

<span data-ttu-id="fd8d9-109">Kui arvutatud väärtused ei ole täpsed, saate neid kohandada, sisestades koorma kaalu ja mahu tegelikud väärtused.</span><span class="sxs-lookup"><span data-stu-id="fd8d9-109">If the calculated values aren’t precise, you can adjust them by entering the actual values for the weight and volume on the load.</span></span> <span data-ttu-id="fd8d9-110">Kaalu ja mahu väärtusi kasutatakse transpordihalduse protsessides.</span><span class="sxs-lookup"><span data-stu-id="fd8d9-110">The values for the weight and volume are used in transportation management processes.</span></span> <span data-ttu-id="fd8d9-111">Näiteks kasutatakse väärtusi määra marsruudi töölaual, kus need aitavad määratleda koormate määra ja marsruudi ning neid kasutatakse ka transpordi maksevahendite ja juhi sisseregistreerimise puhul.</span><span class="sxs-lookup"><span data-stu-id="fd8d9-111">For example, the values are used in the rate route workbench, where they help define the rate and route for loads, and they are also used for transportation tenders and driver check-in.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="fd8d9-112">Kus see kehtib</span><span class="sxs-lookup"><span data-stu-id="fd8d9-112">Where it applies</span></span>

<span data-ttu-id="fd8d9-113">Konteineri kaalu ja mahu lisamine koormale rakendub transpordihalduse protsessides, nt määra marsruudi töölaual, transpordi maksevahendite ja juhi sisseregistreerimise puhul.</span><span class="sxs-lookup"><span data-stu-id="fd8d9-113">The functionality for including the container weight and volume on a load applies in transportation management processes, such as the rate route workbench, transportation tenders, and driver check-in.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="fd8d9-114">Kuidas see seadistatakse</span><span class="sxs-lookup"><span data-stu-id="fd8d9-114">How it is set up</span></span>

<span data-ttu-id="fd8d9-115">Koorma puhul arvestatav konteinerite arv arvutatakse konteineri kaalu ja mahu ning konteineri kasutamise protsendi alusel.</span><span class="sxs-lookup"><span data-stu-id="fd8d9-115">The number of containers that should be considered for a load is calculated based on the weight and volume of the container, and on the percentage of the container is used.</span></span>

-   <span data-ttu-id="fd8d9-116">Konteineri kaalu ja mahu määramiseks klõpsake valikuid **Laohaldus** \> **Seadistus** \> **Konteinerid** \> **Konteineritüübid**.</span><span class="sxs-lookup"><span data-stu-id="fd8d9-116">To set the weight and volume for a container, click **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>

-   <span data-ttu-id="fd8d9-117">Konteineri kasutamise protsendi seadistamiseks klõpsake valikuid **Laohaldus** \> **Seadistus** \> **Konteinerid** \> **Konteinerigrupid** ja sisestage siis väärtus väljale **Konteineri kasutamise protsent**.</span><span class="sxs-lookup"><span data-stu-id="fd8d9-117">To set the container utilization percentage, click **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**, and then enter a value in the **Container utilization percentage** field.</span></span>

