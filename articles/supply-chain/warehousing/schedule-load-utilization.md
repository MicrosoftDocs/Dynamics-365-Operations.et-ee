---
title: Koormuse tulususe planeerimine
description: Selles teemas selgitatakse, kuidas seadistada ja planeerida lao koormust.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f88dc44b036f6d5535f7e83693a387149f94f37d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239250"
---
# <a name="schedule-load-utilization"></a><span data-ttu-id="f66c7-103">Koormuse tulususe planeerimine</span><span class="sxs-lookup"><span data-stu-id="f66c7-103">Schedule load utilization</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f66c7-104">Saate ajastada koormuse kasutamise valitud asukohatüüpide jaoks ning kavandada praegust ja tulevast koormuse kasutamist.</span><span class="sxs-lookup"><span data-stu-id="f66c7-104">You can schedule load utilization for selected location types, and you can also project the current and future load utilization.</span></span> <span data-ttu-id="f66c7-105">Saate kavandada koormust ühe või mitme laoala, koormuse üksuste (tsoon või ladu) või tsooni ja lao kombinatsiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="f66c7-105">You can project the load for one or more sites, for the load units (zone or warehouse), or for a combination of a zone and a warehouse.</span></span>

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a><span data-ttu-id="f66c7-106">Lao või saidi koormuse ajastamine ja vaatamine</span><span class="sxs-lookup"><span data-stu-id="f66c7-106">Schedule and view the load for a warehouse or site</span></span>

<span data-ttu-id="f66c7-107">Koormuse ajastamiseks saitidele, ladudele või tsoonidele peate looma ruumikasutuse seadistuse ja seostama selle koondplaaniga.</span><span class="sxs-lookup"><span data-stu-id="f66c7-107">To schedule the load for sites, warehouses, or zones, you create a space utilization setup and associate it with a master plan.</span></span>

<span data-ttu-id="f66c7-108">Ruumikasutuse seadistamisel kasutage asukohatüüpe, nt **Hulgiasukoht** ja **Komplekteerimiskoht**, et määrata, kuidas tuleb ruumikasutust kavandada.</span><span class="sxs-lookup"><span data-stu-id="f66c7-108">In the space utilization setup, you use location types, such as **Bulk location** and **Picking location**, to specify how space utilization should be projected.</span></span> <span data-ttu-id="f66c7-109">Saate ka määrata ladustamise koormuse režiimi, näiteks **Tsoon**.</span><span class="sxs-lookup"><span data-stu-id="f66c7-109">You also specify a storage load mode, such as **Zone**.</span></span>

<span data-ttu-id="f66c7-110">Tulevase ruumikasutuse kavandamise aluseks on teave, mis arvutatakse seotud koondplaanis.</span><span class="sxs-lookup"><span data-stu-id="f66c7-110">The projection of future space utilization is based on information that is calculated on the associated master plan.</span></span> <span data-ttu-id="f66c7-111">Koondplaanid prognoosivad ressursside kavandamist sissetulevate ja väljaminevate tellimuste jaoks tootmises ja operatsioonides.</span><span class="sxs-lookup"><span data-stu-id="f66c7-111">Master plans forecast the resource planning for incoming and outgoing orders for production and operations.</span></span> <span data-ttu-id="f66c7-112">Saadaoleva ruumi prognoos põhineb ruumi kasutamise seadistuse ja valitud koondplaani suhtel.</span><span class="sxs-lookup"><span data-stu-id="f66c7-112">The projection of available space is based on the relation between the space utilization setup and the selected master plan.</span></span>

<span data-ttu-id="f66c7-113">Ruumikasutuse seadistuses valitud ladustamise koormuse režiimi kasutades saate määrata, kas koormus tuleb kavandada iga lao või tsooni jaoks või kas kavandamisel peab kaasama korraga nii ladude kui ka tsoonide teabe.</span><span class="sxs-lookup"><span data-stu-id="f66c7-113">By using the storage load mode that you selected in the space utilization setup, you can specify whether the load should be projected for each warehouse or zone, or whether the projections should include information about both warehouses and zones.</span></span> <span data-ttu-id="f66c7-114">Saate ka määrata, kas blokeeritud asukohad tuleks koormuse kasutamise arvutamisest välja jätta.</span><span class="sxs-lookup"><span data-stu-id="f66c7-114">You also specify whether blocked locations should be excluded from the calculation of load utilization.</span></span>

<span data-ttu-id="f66c7-115">Saate kavandada ruumikasutuse, luues aruande **Lao koormuse kasutus**.</span><span class="sxs-lookup"><span data-stu-id="f66c7-115">You can project the space utilization by generating the **Warehouse load utilization** report.</span></span> <span data-ttu-id="f66c7-116">Selle aruande loomisel saate määrata, kas koormuse kasutamine tuleb prognoosida iga saidi kohta, kõigi saitide kohta või valitud koormuse üksuse kohta, näiteks tsoon või ladu.</span><span class="sxs-lookup"><span data-stu-id="f66c7-116">When you generate this report, you can specify whether the load utilization should be projected for each site, across sites, or for the selected load unit, such as zone or warehouse.</span></span>

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a><span data-ttu-id="f66c7-117">Ruumi kasutamise seadistuse loomine lao jaoks</span><span class="sxs-lookup"><span data-stu-id="f66c7-117">Create a space utilization setup for a warehouse</span></span>

1. <span data-ttu-id="f66c7-118">Valige **Varude haldamine** \> **Seadistamine** \> **Lao jälgimine** \> **Ruumikasutus**.</span><span class="sxs-lookup"><span data-stu-id="f66c7-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Space utilization**.</span></span>
2. <span data-ttu-id="f66c7-119">Valige suvand **Uus**, et luua ruumikasutusele seadistus.</span><span class="sxs-lookup"><span data-stu-id="f66c7-119">Select **New** to create a space utilization setup.</span></span> <span data-ttu-id="f66c7-120">Määrake uuele seadistusele ID ja nimi.</span><span class="sxs-lookup"><span data-stu-id="f66c7-120">Specify an ID and a name for the new setup.</span></span>
3. <span data-ttu-id="f66c7-121">Väljas **Ladustamise koormuse režiim** valige, kas ruumikasutuse ülevaade peaks kuvama teavet lao, tsooni või mõlema järgi.</span><span class="sxs-lookup"><span data-stu-id="f66c7-121">In the **Storage load mode** field, select whether the overview of space utilization should show information by warehouse, zone, or warehouse and zone.</span></span>
4. <span data-ttu-id="f66c7-122">Määrake suvandi **Blokeeritud asukohtade välistamine** valikule **Jah**, et välistada blokeeritud lao asukohad vaba ruumi arvutusest.</span><span class="sxs-lookup"><span data-stu-id="f66c7-122">Set the **Exclude blocked locations** option to **Yes** to exclude blocked inventory locations from the calculation of available space.</span></span> <span data-ttu-id="f66c7-123">Saate blokeerida lao asukoha sissetulekute ja väljaminekute puhul, määrates asukoha blokeerimise põhjuse lehe **Lao asukohad** kiirkaardi **Muu** väljas **Saabumine blokeeritud** või **Väljastus blokeeritud**.</span><span class="sxs-lookup"><span data-stu-id="f66c7-123">You can block an inventory location for input and output by specifying a blocking cause for the location in the **Input blocked** or **Output blocked** field on the **Other** FastTab on the **Inventory locations** page.</span></span>
5. <span data-ttu-id="f66c7-124">Valige kiirkaardil **Asukoha tüüp** asukohatüübid kaasamiseks ruumikasutuse arvutamisse.</span><span class="sxs-lookup"><span data-stu-id="f66c7-124">On the **Location type** FastTab, select the location types to include in the space utilization calculation.</span></span> <span data-ttu-id="f66c7-125">Peate prognoosimiseks valima vähemalt ühe asukohatüübi.</span><span class="sxs-lookup"><span data-stu-id="f66c7-125">You must select at least one location type for the projection.</span></span>

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a><span data-ttu-id="f66c7-126">Ruumi kasutamise seadistuse seostamine koondplaaniga</span><span class="sxs-lookup"><span data-stu-id="f66c7-126">Associate a space utilization setup with a master plan</span></span>

1. <span data-ttu-id="f66c7-127">Valige **Varude haldamine** \> **Perioodilised ülesanded** \> **Koormuse tulususe planeerimine**.</span><span class="sxs-lookup"><span data-stu-id="f66c7-127">Select **Inventory management** \> **Periodic tasks** \> **Schedule load utilization**.</span></span>
2. <span data-ttu-id="f66c7-128">Valige koondplaan väljalt **Koondplaan**.</span><span class="sxs-lookup"><span data-stu-id="f66c7-128">In the **Master plan** field, select a master plan.</span></span>
3. <span data-ttu-id="f66c7-129">Määrake väljal **Päevade arv** praeguse ja tulevase töökoormuse prognoosi kaasatavate päevade arv.</span><span class="sxs-lookup"><span data-stu-id="f66c7-129">In the **Number of days** field, specify the number of days to include in the projection of current and future workloads.</span></span>
4. <span data-ttu-id="f66c7-130">Valige väljal **Ruumikasutus** ruumikasutuse seadistus, mida kasutada praeguste ja tulevaste töökoormuste prognoosimisel.</span><span class="sxs-lookup"><span data-stu-id="f66c7-130">In the **Space utilization** field, select the space utilization setup to use for the projection of current and future workloads.</span></span>

### <a name="specify-the-load-utilization-projection-and-view-information"></a><span data-ttu-id="f66c7-131">Koormuse kasutamise prognoosimise määratlemine ja teabe kuvamine</span><span class="sxs-lookup"><span data-stu-id="f66c7-131">Specify the load utilization projection and view information</span></span>

1. <span data-ttu-id="f66c7-132">Valige **Varude haldamine** \> **Päringud ja aruanded** \> **Füüsiliste varude aruanded** \> **Lao koormuse tulusus**.</span><span class="sxs-lookup"><span data-stu-id="f66c7-132">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Warehouse load utilization**.</span></span>
2. <span data-ttu-id="f66c7-133">Valige väljal **Kuvamisalus:** ruumikasutuse prognoosi tase.</span><span class="sxs-lookup"><span data-stu-id="f66c7-133">In the **Show by** field, select the level of the space utilization projection:</span></span>

    - <span data-ttu-id="f66c7-134">**Tegevuskoht** – kavandab ruumikasutuse iga tegevuskoha kohta.</span><span class="sxs-lookup"><span data-stu-id="f66c7-134">**Site** – Project the space utilization for each site.</span></span> <span data-ttu-id="f66c7-135">See prognoos on kasulik, kui näiteks soovite vaadata saidi kõiki ladusid, et tasakaalustada ruumi kasutamist ladude vahel.</span><span class="sxs-lookup"><span data-stu-id="f66c7-135">This projection is useful if, for example, you want to view all the warehouses for a site so that you can balance the space utilization between the warehouses.</span></span>
    - <span data-ttu-id="f66c7-136">**Koormuse üksus** – kavandage ruumikasutus tsoonide või ladude jaoks.</span><span class="sxs-lookup"><span data-stu-id="f66c7-136">**Load unit** – Project the space utilization for zones or warehouses.</span></span> <span data-ttu-id="f66c7-137">Vaba ruum kavandatakse seejärel lehe **Ruumikasutus** väljal **Ladustamise koormuse režiim** valitud väärtuse järgi, kui lõite ruumikasutuse seadistuse.</span><span class="sxs-lookup"><span data-stu-id="f66c7-137">The available space is then projected according to the value that you selected in the **Storage load mode** field on the **Space utilization** page when you created the space utilization setup.</span></span>

3. <span data-ttu-id="f66c7-138">Järgige üht alltoodud etappidest, lähtudes väärtusest, mille valisite eelmises etapis.</span><span class="sxs-lookup"><span data-stu-id="f66c7-138">Follow one of these steps, depending on the value that you selected in the previous step:</span></span>

    - <span data-ttu-id="f66c7-139">Kui valisite väärtuse **Tegevuskoht** väljal **Kuvamisalus:**, on saadaval väli **Tegevuskoht**.</span><span class="sxs-lookup"><span data-stu-id="f66c7-139">If you selected **Site** in the **Show by** field, the **Site** field is available.</span></span> <span data-ttu-id="f66c7-140">Valige üks või mitu tegevuskohta prognoosi kaasamiseks.</span><span class="sxs-lookup"><span data-stu-id="f66c7-140">Select one or more sites to include in the projection.</span></span>
    - <span data-ttu-id="f66c7-141">Kui valisite väärtuse **Koormuse üksus** väljal **Kuvamisalus:**, on saadaval väli **Koormuse üksus**.</span><span class="sxs-lookup"><span data-stu-id="f66c7-141">If you selected **Load unit** in the **Show by** field, the **Load unit** field is available.</span></span> <span data-ttu-id="f66c7-142">Valige koormuse üksus.</span><span class="sxs-lookup"><span data-stu-id="f66c7-142">Select the load unit.</span></span>

4. <span data-ttu-id="f66c7-143">Valige väljal **Koormuse tüüp** suvand **Maht** või **Kaal**, et määrata lao tootmisüksus, mille jaoks ruumi kavandatakse.</span><span class="sxs-lookup"><span data-stu-id="f66c7-143">In the **Load type** field, select **Volume** or **Weight** to specify the warehouse operating unit to project space for.</span></span>
5. <span data-ttu-id="f66c7-144">Väljal **Ruumikasutuse seadistamine** valige ruumikasutuse seadistus, mille alusel prognoos tuleb teha.</span><span class="sxs-lookup"><span data-stu-id="f66c7-144">In the **Space utilization setup** field, select the space utilization setup that the projection should be based on.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]