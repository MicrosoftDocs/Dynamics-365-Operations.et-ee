---
title: Täiendavad asukohatsoonid
description: Selles teemas antakse ülevaate uutest Microsoft Dynamics 365 Supply Chain Managementi lisatud asukohatsoonidest.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 6cf81939989b8faffcda51bbbd5bc6b27aec7eea
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4426624"
---
# <a name="additional-location-zones"></a><span data-ttu-id="4b474-103">Täiendavad asukohatsoonid</span><span class="sxs-lookup"><span data-stu-id="4b474-103">Additional location zones</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b474-104">Microsoft Dynamics 365 Supply Chain Managementis on saadaval kolm uut tsoonivälja.</span><span class="sxs-lookup"><span data-stu-id="4b474-104">Three new zone fields are available in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="4b474-105">Laohaldurid saavad määratleda nende abil täiendavaid ladude organisatsioone või paigutusi.</span><span class="sxs-lookup"><span data-stu-id="4b474-105">Warehouse managers can use them to define additional warehouse organizations or layouts.</span></span> <span data-ttu-id="4b474-106">Uusi tsoonivälju saab seadistada käsitsi või viisardi **Asukoha häälestus** abil.</span><span class="sxs-lookup"><span data-stu-id="4b474-106">The new zone fields can be set either manually or by using the **Location setup** wizard.</span></span> <span data-ttu-id="4b474-107">Neid saab kasutada mis tahes päringus või filtreerimises, mis kasutab tabelit Asukohad.</span><span class="sxs-lookup"><span data-stu-id="4b474-107">They can be used in any query or filtering that uses the Locations table.</span></span>

<span data-ttu-id="4b474-108">Tsooniväljade kasutamiseks pole vaja täiendavat häälestust.</span><span class="sxs-lookup"><span data-stu-id="4b474-108">No additional setup is required to use the zone fields.</span></span>

## <a name="turn-on-the-additional-location-zone-feature"></a><span data-ttu-id="4b474-109">Funktsiooni Täiendav asukohatsoon sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="4b474-109">Turn on the Additional location zone feature</span></span>

<span data-ttu-id="4b474-110">Enne funktsiooni *Täiendav asukohatsoon* kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="4b474-110">Before you can use the *Additional location zone* feature, it must be turned on in your system.</span></span> <span data-ttu-id="4b474-111">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="4b474-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="4b474-112">Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="4b474-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="4b474-113">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="4b474-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="4b474-114">**Funktsiooni nimi:** *Täiendav asukohatsoon*</span><span class="sxs-lookup"><span data-stu-id="4b474-114">**Feature name:** *Additional location zone*</span></span>

## <a name="use-location-zones"></a><span data-ttu-id="4b474-115">Asukohatsoonide kasutamine</span><span class="sxs-lookup"><span data-stu-id="4b474-115">Use location zones</span></span>

1. <span data-ttu-id="4b474-116">Minge asukohta **Laohaldus \> Seadistus \> Ladu \> Asukoha häälestuse viisard**.</span><span class="sxs-lookup"><span data-stu-id="4b474-116">Go to **Warehouse management \> Setup \> Warehouse \> Location setup wizard**.</span></span>
2. <span data-ttu-id="4b474-117">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="4b474-117">Set the following values:</span></span>

    - <span data-ttu-id="4b474-118">Valige väljal **Ladu** väärtus _62_.</span><span class="sxs-lookup"><span data-stu-id="4b474-118">In the **Warehouse** field, select _62_.</span></span>
    - <span data-ttu-id="4b474-119">Valige väljal **Tsooni ID** väärtus _FLOOR_.</span><span class="sxs-lookup"><span data-stu-id="4b474-119">In the **Zone ID** field, select _FLOOR_.</span></span>
    - <span data-ttu-id="4b474-120">Valige väljal **Täiendav tsoon 1** väärtus _PICKZONE1_.</span><span class="sxs-lookup"><span data-stu-id="4b474-120">In the **Additional Zone 1** field, select _PICKZONE1_.</span></span>
    - <span data-ttu-id="4b474-121">Valige väljal **Täiendav tsoon 2** väärtus _WEBSHOP1_.</span><span class="sxs-lookup"><span data-stu-id="4b474-121">In the **Additional Zone 2** field, select _WEBSHOP1_.</span></span>
    - <span data-ttu-id="4b474-122">Valige väljal **Asukoha profiili ID** väärtus _FLOOR_.</span><span class="sxs-lookup"><span data-stu-id="4b474-122">In the **Location profile ID** field, select _FLOOR_.</span></span>

3. <span data-ttu-id="4b474-123">Valige rida **Korrus**.</span><span class="sxs-lookup"><span data-stu-id="4b474-123">Select the **Floor** line.</span></span>
4. <span data-ttu-id="4b474-124">Sisestage väljale **Alates numbrist** väärtus _1_.</span><span class="sxs-lookup"><span data-stu-id="4b474-124">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="4b474-125">Sisestage väljale **Kuni numbrini** väärtus _3_.</span><span class="sxs-lookup"><span data-stu-id="4b474-125">In the **To number** field, enter _3_.</span></span>
5. <span data-ttu-id="4b474-126">Valige rida **Riiulirida**.</span><span class="sxs-lookup"><span data-stu-id="4b474-126">Select the **Aisle** line.</span></span>
6. <span data-ttu-id="4b474-127">Sisestage väljale **Alates numbrist** väärtus _1_.</span><span class="sxs-lookup"><span data-stu-id="4b474-127">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="4b474-128">Sisestage väljale **Kuni numbrini** väärtus _5_.</span><span class="sxs-lookup"><span data-stu-id="4b474-128">In the **To number** field, enter _5_.</span></span>
7. <span data-ttu-id="4b474-129">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="4b474-129">Select **Create**.</span></span>
8. <span data-ttu-id="4b474-130">Teile kuvatakse teateid selle kohta, et uued asukohad on lisatud.</span><span class="sxs-lookup"><span data-stu-id="4b474-130">You receive messages that state that new locations have been added.</span></span> <span data-ttu-id="4b474-131">Teadete nägemiseks valige nupp **Kuva sõnumid**.</span><span class="sxs-lookup"><span data-stu-id="4b474-131">Select the **Show messages** button to view the messages.</span></span>
9. <span data-ttu-id="4b474-132">Avage **Laohaldus \> Seadistus \> Ladu \> Asukohad**.</span><span class="sxs-lookup"><span data-stu-id="4b474-132">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span> <span data-ttu-id="4b474-133">Uued asukohad kuvatakse loendis ja kõik tsooniväljad on saadaval (st olemasolev tsooniväli ja uued täiendavad tsooniväljad).</span><span class="sxs-lookup"><span data-stu-id="4b474-133">The new locations appear in the list, and all zone fields are available (that is, the existing zone field and the new additional zone fields).</span></span>
