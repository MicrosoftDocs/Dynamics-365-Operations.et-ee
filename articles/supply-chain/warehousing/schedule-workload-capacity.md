---
title: Graafiku töökoormuse võimsus
description: Selles teemas kirjeldatakse, kuidas seadistada ja planeerida töökoormuse võimsust lao töötajatele või kogu laole.
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5d878b0fe4e6b65aa2439d7ef7312eda1895823
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814923"
---
# <a name="schedule-workload-capacity"></a><span data-ttu-id="610f7-103">Töökoormuse võimsuse plaanimine</span><span class="sxs-lookup"><span data-stu-id="610f7-103">Schedule workload capacity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="610f7-104">Saate plaanida töökoormuse võimsuse ladudele ning kavandada praegused ja tulevased töökoormused üksikutes ladudes olevatele töötajatele.</span><span class="sxs-lookup"><span data-stu-id="610f7-104">You can schedule workload capacity for warehouses, and you can also project the current and future workloads for the workers in individual warehouses.</span></span> <span data-ttu-id="610f7-105">Saate kavandada kogu lao töökoormuse või saate sissetulevate ja väljaminevate töökoormuste jaoks töökoormuse eraldi kavandada.</span><span class="sxs-lookup"><span data-stu-id="610f7-105">You can project the workload for the whole warehouse, or you can project the workload separately for incoming and outgoing workloads.</span></span>

<span data-ttu-id="610f7-106">Valitud ladudele töökoormuse väljundi kavandamiseks peavad koondplaneerimise andmed nende ladude kohta saadaval olema.</span><span class="sxs-lookup"><span data-stu-id="610f7-106">To project workload output for selected warehouses, master scheduling data must be available for those warehouses.</span></span> <span data-ttu-id="610f7-107">Lisateavet vt teemast [Koondplaanide ülevaade](../master-planning/master-plans.md).</span><span class="sxs-lookup"><span data-stu-id="610f7-107">For more information, see [Master plans overview](../master-planning/master-plans.md).</span></span>

## <a name="schedule-and-view-workloads-for-a-warehouse"></a><span data-ttu-id="610f7-108">Lao töökoormuste plaanimine ja vaatamine</span><span class="sxs-lookup"><span data-stu-id="610f7-108">Schedule and view workloads for a warehouse</span></span>

<span data-ttu-id="610f7-109">Lao töökoormuse võimsuse plaanimiseks saate luua töökoormuse seadistuse ühele või mitmele laole ja seostada seejärel töökoormuse seadistuse koondplaaniga.</span><span class="sxs-lookup"><span data-stu-id="610f7-109">To schedule workload capacity for a warehouse, you create a workload setup for one or more warehouses, and then associate the workload setup with a master plan.</span></span> <span data-ttu-id="610f7-110">Töökoormuse võimsuse seadistamises saate määratleda piirangud sissetulevate ja väljaminevate kannete kaalu või mahu jaoks.</span><span class="sxs-lookup"><span data-stu-id="610f7-110">In the workload capacity setup, you can define limits for the weight or volume for incoming and outgoing transactions.</span></span> <span data-ttu-id="610f7-111">Saate luua ka rohkem kui ühe seadistuse igale laole ja seejärel seostada seadistuse üksikute koondplaanidega.</span><span class="sxs-lookup"><span data-stu-id="610f7-111">You can also create more than one setup for each warehouse and then associate the setup with individual master plans.</span></span> <span data-ttu-id="610f7-112">Näiteks võite seda lähenemist kasutada hooajaliste muudatuste kohandamiseks tööjõus.</span><span class="sxs-lookup"><span data-stu-id="610f7-112">For example, you might use this approach to accommodate seasonal changes in the workforce.</span></span>

<span data-ttu-id="610f7-113">Kui lao töötajad töötavad nii sissetulevate kui ka väljaminevate töökoormuste kannetega, saate konfigureerida lao võimsuse seadistuse, nii et töökoormus kavandatakse kombineeritud vaates.</span><span class="sxs-lookup"><span data-stu-id="610f7-113">If the workers for a warehouse work with transactions for both incoming and outgoing workloads, you can configure the warehouse capacity setup so that the workload is projected in a combined view.</span></span>

<span data-ttu-id="610f7-114">Ladude töökoormuste plaanimiseks ja vaatamiseks peate läbima järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="610f7-114">To schedule and view workloads for warehouses, you must complete the following tasks:</span></span>

1. <span data-ttu-id="610f7-115">Looge töökoormuse võimsuse seadistus ja määratlege töökoormuse võimsuse piirangud ühele või mitmele laole.</span><span class="sxs-lookup"><span data-stu-id="610f7-115">Create a workload capacity setup and define workload capacity limits for one or more warehouses.</span></span>
2. <span data-ttu-id="610f7-116">Seostage töökoormuse võimsuse seadistus koondplaaniga, et luua töökoormuse kavandid ja määrata, kui kaua need kavandid kehtivad.</span><span class="sxs-lookup"><span data-stu-id="610f7-116">Associate the workload capacity setup with a master plan to create workload projections and specify how long those projections will apply.</span></span>

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a><span data-ttu-id="610f7-117">Töökoormuse võimsuse seadistuse loomine laole</span><span class="sxs-lookup"><span data-stu-id="610f7-117">Create a workload capacity setup for a warehouse</span></span>

1. <span data-ttu-id="610f7-118">Valige **Varude haldamine** \> **Seadistamine** \> **Lao jälgimine** \> **Töökoormuse võimsus**.</span><span class="sxs-lookup"><span data-stu-id="610f7-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="610f7-119">Valige toimingupaanilt suvand **Uus**, et luua töökoormuse võimsuse seadistus.</span><span class="sxs-lookup"><span data-stu-id="610f7-119">On the Action Pane, select **New** to create a workload capacity setup.</span></span>
3. <span data-ttu-id="610f7-120">Kiirkaardil **Laod** valige suvand **Uus** ja sisestage seejärel väärtused reale, et seostada ladu töökoormuse võimsuse seadistusega.</span><span class="sxs-lookup"><span data-stu-id="610f7-120">On the **Warehouses** FastTab, select **New**, and then enter values on the line to associate a warehouse with the workload capacity setup.</span></span>
4. <span data-ttu-id="610f7-121">Valige märkeruut **Kombineeritud sissetulev ja väljaminev töökoormus**, kui aruanne **Töökoormuse võimsus** peaks kuvama sissetulevate ja väljaminevate kannete kogutöökoormust ühel vaatel.</span><span class="sxs-lookup"><span data-stu-id="610f7-121">Select the **Combined inbound and outbound workload** check box if the **Workload capacity** report should show the total workload for incoming and outgoing transactions in one view.</span></span>
5. <span data-ttu-id="610f7-122">Kiirkaardil **Kandetüübid** valige sissetulevate ja väljaminevate kannete tüübid, millele töökoormuse piirangud kehtivad.</span><span class="sxs-lookup"><span data-stu-id="610f7-122">On the **Transaction types** FastTab, select the types of incoming and outgoing transactions that the workload limits will apply to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="610f7-123">Peate valima vähemalt ühe kande tüübi nii sissetulevale kui ka väljaminevale töökoormusele.</span><span class="sxs-lookup"><span data-stu-id="610f7-123">You must select at least one transaction type for both the incoming workload and the outgoing workload.</span></span>

#### <a name="define-limits-for-volume-or-weight"></a><span data-ttu-id="610f7-124">Mahu- või kaalupiirangute määramine</span><span class="sxs-lookup"><span data-stu-id="610f7-124">Define limits for volume or weight</span></span>

<span data-ttu-id="610f7-125">Saate seadistada piirangud mahule või kaalule olenevalt piirangust, mis on lao tööjõu seisukohalt olulised.</span><span class="sxs-lookup"><span data-stu-id="610f7-125">You can set up limits for volume or weight, depending on the limitation that is relevant for the warehouse workforce.</span></span> <span data-ttu-id="610f7-126">Määratud piirangud sisalduvad töökoormuse võimsuse kavandis, mida saate vaadata aruandes **Töökoormuse võimsus**.</span><span class="sxs-lookup"><span data-stu-id="610f7-126">The limits that you specify are included in the workload capacity projection that you can view on the **Workload capacity** report.</span></span>

<span data-ttu-id="610f7-127">Kaupade mahu ja kaalu teabe kavandamiseks peavad ühe laokauba standardne maht ja ühe laokauba kaal kõikidele toodetele määratud olema.</span><span class="sxs-lookup"><span data-stu-id="610f7-127">To project information about volume and weight for items, the standard volume of one inventory item and the weight of one inventory item must be specified for all products.</span></span> <span data-ttu-id="610f7-128">Vajalikud väljad on saadaval järgmistes väljagruppides lehe **Väljastatud toote üksikasjad** kiirkaardil **Varude haldus**.</span><span class="sxs-lookup"><span data-stu-id="610f7-128">The fields that are required are available in the following field groups on the **Manage inventory** FastTab of the **Released product details** page:</span></span>

- <span data-ttu-id="610f7-129">Käsitsemine</span><span class="sxs-lookup"><span data-stu-id="610f7-129">Handling</span></span>
- <span data-ttu-id="610f7-130">Füüsilised dimensioonid</span><span class="sxs-lookup"><span data-stu-id="610f7-130">Physical dimensions</span></span>
- <span data-ttu-id="610f7-131">Kaaluühikud</span><span class="sxs-lookup"><span data-stu-id="610f7-131">Weight measurements</span></span>

<span data-ttu-id="610f7-132">Kui seda teavet pole õigesti määratud, saate aruande **Töökoormuse võimsus** loomisel sõnumi.</span><span class="sxs-lookup"><span data-stu-id="610f7-132">If this information isn't specified correctly, you receive a message when you generate the **Workload capacity** report.</span></span> <span data-ttu-id="610f7-133">Aruandes saate seejärel süvitsi minna, et tuvastada puuduv teave, mis on vajalik tulevase töökoormuse kavandamiseks.</span><span class="sxs-lookup"><span data-stu-id="610f7-133">From the report, you can then drill down to identify the missing information that is required in order to project the future workload.</span></span>

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a><span data-ttu-id="610f7-134">Töökoormuse võimsuse seadistuse seostamine koondplaaniga</span><span class="sxs-lookup"><span data-stu-id="610f7-134">Associate a workload capacity setup with a master plan</span></span>

1. <span data-ttu-id="610f7-135">Valige **Varude haldamine** \> **Perioodiline** \> **Töökoormuse plaanimine**.</span><span class="sxs-lookup"><span data-stu-id="610f7-135">Select **Inventory management** \> **Periodic** \> **Schedule workload**.</span></span>
2. <span data-ttu-id="610f7-136">Valige väljal **Koondplaan** töökoormuse kavandite jaoks kasutatav koondplaan.</span><span class="sxs-lookup"><span data-stu-id="610f7-136">In the **Master plan** field, select the master plan to use for workload projections.</span></span>
3. <span data-ttu-id="610f7-137">Määrake väljal **Koondplaan** päevade arv, mille vältel töökoormuse kavand kehtib.</span><span class="sxs-lookup"><span data-stu-id="610f7-137">In the **Number of days** field, specify the number of days that the workload projection covers.</span></span>
4. <span data-ttu-id="610f7-138">Valige väljal **Koondplaan** töökoormuse seadistus, mis seostatakse koondplaaniga.</span><span class="sxs-lookup"><span data-stu-id="610f7-138">In the **Workload** field, select the workload setup to associate with the master plan.</span></span>

### <a name="view-workload-capacity"></a><span data-ttu-id="610f7-139">Töökoormuse võimsuse vaatamine</span><span class="sxs-lookup"><span data-stu-id="610f7-139">View workload capacity</span></span>

1. <span data-ttu-id="610f7-140">Valige **Varude haldamine** \> **Päringud ja aruanded** \> **Füüsiliste varude aruanded** \> **Töökoormuse võimsus**.</span><span class="sxs-lookup"><span data-stu-id="610f7-140">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="610f7-141">Määrake väljal **Veergude arv** aruandes kuvatavate veergude arv.</span><span class="sxs-lookup"><span data-stu-id="610f7-141">In the **Number of columns** field, specify the number of columns to show on the report.</span></span>
3. <span data-ttu-id="610f7-142">Valige väljas **Tellimuse tüüp** suvand **Plaanitud ja kinnitatud**, **Plaanitud** või **Kinnitatud**, et näidata, mis tüüpi tellimusi aruandes kavandada.</span><span class="sxs-lookup"><span data-stu-id="610f7-142">In the **Order type** field, select **Planned and confirmed**, **Planned**, or **Confirmed** to indicate the type of orders to project on the report.</span></span>
4. <span data-ttu-id="610f7-143">Valige väljal **Koondplaan** koormuse tüüp, et määrata, kas töökoormuse võimsus tuleb kavandada mahule või kaalule.</span><span class="sxs-lookup"><span data-stu-id="610f7-143">In the **Load type** field, select a load type to specify whether the workload capacity should be projected for volume or weight.</span></span>
5. <span data-ttu-id="610f7-144">Valige väljal **Koondplaan** töökoormuse võimsuse seadistus.</span><span class="sxs-lookup"><span data-stu-id="610f7-144">In the **Workload capacity** field, select a workload capacity setup.</span></span>
