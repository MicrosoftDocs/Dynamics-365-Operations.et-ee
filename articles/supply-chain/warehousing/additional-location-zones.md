---
title: Täiendavad asukohatsoonid
description: Selles teemas antakse ülevaate uutest Microsoft Dynamics 365 Supply Chain Managementi lisatud asukohatsoonidest.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: ee6e0b824ff16bf757159da5198a4215f4f5d121
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808938"
---
# <a name="additional-location-zones"></a><span data-ttu-id="082c7-103">Täiendavad asukohatsoonid</span><span class="sxs-lookup"><span data-stu-id="082c7-103">Additional location zones</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="082c7-104">Microsoft Dynamics 365 Supply Chain Managementis on saadaval kolm uut tsoonivälja.</span><span class="sxs-lookup"><span data-stu-id="082c7-104">Three new zone fields are available in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="082c7-105">Laohaldurid saavad määratleda nende abil täiendavaid ladude organisatsioone või paigutusi.</span><span class="sxs-lookup"><span data-stu-id="082c7-105">Warehouse managers can use them to define additional warehouse organizations or layouts.</span></span> <span data-ttu-id="082c7-106">Uusi tsoonivälju saab seadistada käsitsi või viisardi **Asukoha häälestus** abil.</span><span class="sxs-lookup"><span data-stu-id="082c7-106">The new zone fields can be set either manually or by using the **Location setup** wizard.</span></span> <span data-ttu-id="082c7-107">Neid saab kasutada mis tahes päringus või filtreerimises, mis kasutab tabelit Asukohad.</span><span class="sxs-lookup"><span data-stu-id="082c7-107">They can be used in any query or filtering that uses the Locations table.</span></span>

<span data-ttu-id="082c7-108">Tsooniväljade kasutamiseks pole vaja täiendavat häälestust.</span><span class="sxs-lookup"><span data-stu-id="082c7-108">No additional setup is required to use the zone fields.</span></span>

## <a name="turn-on-the-additional-location-zone-feature"></a><span data-ttu-id="082c7-109">Funktsiooni Täiendav asukohatsoon sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="082c7-109">Turn on the Additional location zone feature</span></span>

<span data-ttu-id="082c7-110">Enne funktsiooni *Täiendav asukohatsoon* kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="082c7-110">Before you can use the *Additional location zone* feature, it must be turned on in your system.</span></span> <span data-ttu-id="082c7-111">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="082c7-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="082c7-112">Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="082c7-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="082c7-113">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="082c7-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="082c7-114">**Funktsiooni nimi:** *Täiendav asukohatsoon*</span><span class="sxs-lookup"><span data-stu-id="082c7-114">**Feature name:** *Additional location zone*</span></span>

## <a name="use-location-zones"></a><span data-ttu-id="082c7-115">Asukohatsoonide kasutamine</span><span class="sxs-lookup"><span data-stu-id="082c7-115">Use location zones</span></span>

1. <span data-ttu-id="082c7-116">Minge asukohta **Laohaldus \> Seadistus \> Ladu \> Asukoha häälestuse viisard**.</span><span class="sxs-lookup"><span data-stu-id="082c7-116">Go to **Warehouse management \> Setup \> Warehouse \> Location setup wizard**.</span></span>
2. <span data-ttu-id="082c7-117">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="082c7-117">Set the following values:</span></span>

    - <span data-ttu-id="082c7-118">Valige väljal **Ladu** väärtus _62_.</span><span class="sxs-lookup"><span data-stu-id="082c7-118">In the **Warehouse** field, select _62_.</span></span>
    - <span data-ttu-id="082c7-119">Valige väljal **Tsooni ID** väärtus _FLOOR_.</span><span class="sxs-lookup"><span data-stu-id="082c7-119">In the **Zone ID** field, select _FLOOR_.</span></span>
    - <span data-ttu-id="082c7-120">Valige väljal **Täiendav tsoon 1** väärtus _PICKZONE1_.</span><span class="sxs-lookup"><span data-stu-id="082c7-120">In the **Additional Zone 1** field, select _PICKZONE1_.</span></span>
    - <span data-ttu-id="082c7-121">Valige väljal **Täiendav tsoon 2** väärtus _WEBSHOP1_.</span><span class="sxs-lookup"><span data-stu-id="082c7-121">In the **Additional Zone 2** field, select _WEBSHOP1_.</span></span>
    - <span data-ttu-id="082c7-122">Valige väljal **Asukoha profiili ID** väärtus _FLOOR_.</span><span class="sxs-lookup"><span data-stu-id="082c7-122">In the **Location profile ID** field, select _FLOOR_.</span></span>

3. <span data-ttu-id="082c7-123">Valige rida **Korrus**.</span><span class="sxs-lookup"><span data-stu-id="082c7-123">Select the **Floor** line.</span></span>
4. <span data-ttu-id="082c7-124">Sisestage väljale **Alates numbrist** väärtus _1_.</span><span class="sxs-lookup"><span data-stu-id="082c7-124">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="082c7-125">Sisestage väljale **Kuni numbrini** väärtus _3_.</span><span class="sxs-lookup"><span data-stu-id="082c7-125">In the **To number** field, enter _3_.</span></span>
5. <span data-ttu-id="082c7-126">Valige rida **Riiulirida**.</span><span class="sxs-lookup"><span data-stu-id="082c7-126">Select the **Aisle** line.</span></span>
6. <span data-ttu-id="082c7-127">Sisestage väljale **Alates numbrist** väärtus _1_.</span><span class="sxs-lookup"><span data-stu-id="082c7-127">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="082c7-128">Sisestage väljale **Kuni numbrini** väärtus _5_.</span><span class="sxs-lookup"><span data-stu-id="082c7-128">In the **To number** field, enter _5_.</span></span>
7. <span data-ttu-id="082c7-129">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="082c7-129">Select **Create**.</span></span>
8. <span data-ttu-id="082c7-130">Teile kuvatakse teateid selle kohta, et uued asukohad on lisatud.</span><span class="sxs-lookup"><span data-stu-id="082c7-130">You receive messages that state that new locations have been added.</span></span> <span data-ttu-id="082c7-131">Teadete nägemiseks valige nupp **Kuva sõnumid**.</span><span class="sxs-lookup"><span data-stu-id="082c7-131">Select the **Show messages** button to view the messages.</span></span>
9. <span data-ttu-id="082c7-132">Avage **Laohaldus \> Seadistus \> Ladu \> Asukohad**.</span><span class="sxs-lookup"><span data-stu-id="082c7-132">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span> <span data-ttu-id="082c7-133">Uued asukohad kuvatakse loendis ja kõik tsooniväljad on saadaval (st olemasolev tsooniväli ja uued täiendavad tsooniväljad).</span><span class="sxs-lookup"><span data-stu-id="082c7-133">The new locations appear in the list, and all zone fields are available (that is, the existing zone field and the new additional zone fields).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]