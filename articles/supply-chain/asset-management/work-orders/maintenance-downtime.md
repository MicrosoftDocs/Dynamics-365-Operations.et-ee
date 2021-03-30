---
title: Töökäskude hoolduskatkestus
description: Selles teemas kirjeldatakse, kuidas saate luua hoolduskatkestuse registreeringuid töökäsus valitud varale.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ba24ae9e82debf9a67761e4e2ca0817e1645db28
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209727"
---
# <a name="maintenance-downtime-for-work-orders"></a><span data-ttu-id="ff5f6-103">Töökäskude hoolduskatkestus</span><span class="sxs-lookup"><span data-stu-id="ff5f6-103">Maintenance downtime for work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="ff5f6-104">Võite luua hoolduskatkestuse registreeringuid töökäsus valitud varale.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-104">You can create maintenance downtime registrations on the asset that is selected on a work order.</span></span> <span data-ttu-id="ff5f6-105">See funktsioon on kasulik, kui soovite registreerida hoolduskatkestuse ühele või enamale tootmisala masinale.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-105">This capability is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="ff5f6-106">Kõigepealt looge hoolduskatkestuse põhjuse koodid, mida soovite kasutada, näiteks **Katkiminek** ja **Planeeritud seiskamine**.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-106">You first create the maintenance downtime reason codes that you want to use, such as **Breakdown** and **Planned stop**.</span></span> <span data-ttu-id="ff5f6-107">Seda toimingut tehakse lehel **Hoolduskatkestuse põhjuste koodid**.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-107">This step is done on the **Maintenance downtime reason codes** page.</span></span> <span data-ttu-id="ff5f6-108">Järgmisena saate luua hoolduskatkestuse registreeringud lehel **Hoolduskatkestus** ja lisada asjakohased hoolduskatkestuse põhjuse koodid.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-108">You can then create maintenance downtime registrations on the **Maintenance downtime** page and add the relevant maintenance downtime reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="ff5f6-109">Hoolduskatkestuse põhjuse koodide loomine</span><span class="sxs-lookup"><span data-stu-id="ff5f6-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="ff5f6-110">Valige **Varahaldus** > **Seadistus** > **töökäsud** > **Hoolduskatkestuse põhjuse koodid**.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-110">Select **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="ff5f6-111">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-111">Select **New**.</span></span>

3. <span data-ttu-id="ff5f6-112">Sisestage väljale **Hoolduskatkestuse põhjuse kood** hoolduskatkestuse põhjuse koodi ID.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-112">In the **Maintenance downtime reason code** field, enter an ID for the maintenance downtime reason code.</span></span>

4. <span data-ttu-id="ff5f6-113">Väljale **Nimi** sisestage nimi.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-113">In the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="ff5f6-114">Märkige ruut **KPI sisaldus**, kui põhjuse kood tuleks kaasata vara peamiste tulemusnäitajate (KPI) arvutustesse.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-114">Select the **KPI include** check box if the reason code should be included in calculations of key performance indicators (KPIs) for the asset.</span></span> <span data-ttu-id="ff5f6-115">Üldiselt ei tulek planeeritud tootmisseisakuid KPI arvutustesse kaasata, sest need ei mõjuta eeldatavat jõudlust.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-115">In general, planned production stops should not be included in KPI calculations, because they don't affect expected performance.</span></span>

6. <span data-ttu-id="ff5f6-116">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-116">Select **Save**.</span></span>

<span data-ttu-id="ff5f6-117">Järgneval joonisel kuvatakse lehe **Hoolduskatkestuse põhjuse koodid** näide.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-117">The illustration below shows an example of the **Maintenance downtime reason codes** page.</span></span>

![Joonis 1](media/15-work-orders.png)

<span data-ttu-id="ff5f6-119">Kui olete loonud need hoolduskatkestuse põhjuse koodid, mida kasutada soovite, saate luua töökäskudele ja varadele hoolduskatkestuse registreeringuid.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-119">After you've created the maintenance downtime reason codes that you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="ff5f6-120">Hoolduskatkestuse registreeringute loomine</span><span class="sxs-lookup"><span data-stu-id="ff5f6-120">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="ff5f6-121">Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-121">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="ff5f6-122">Valige töökäsk ja seejärel tehke vahekaardi **Töökäsk** jaotises **Vara** valik **Hoolduskatkestus**.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-122">Select the work order, and then, on the **Work order** tab, in the **Asset** group, select **Maintenance downtime**.</span></span>

3. <span data-ttu-id="ff5f6-123">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-123">Select **New**.</span></span>

4. <span data-ttu-id="ff5f6-124">Määratlege hoolduskatkestuse registreeringu kuupäeva ja kellaaja intervall väljadel **Alates** ja **Kuni**.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-124">In the **From** and **To** fields, define the date and time interval for the maintenance downtime registration.</span></span>

>[!NOTE]
><span data-ttu-id="ff5f6-125">Kui lahkute väljalt **Kuni**, sisestatakse kestvus tundides automaatselt väljale **Kestvus**.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-125">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

5. <span data-ttu-id="ff5f6-126">Valige põhjuse kood väljal **Hoolduskatkestuse põhjuse kood**.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-126">In the **maintenance downtime reason code** field, select a reason code.</span></span>

6. <span data-ttu-id="ff5f6-127">Täiendavate registreeringute lisamiseks korrake samme 3 kuni 5.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-127">Repeat steps 3 through 5 to add more registrations.</span></span>

7. <span data-ttu-id="ff5f6-128">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-128">Select **Save**.</span></span>

<span data-ttu-id="ff5f6-129">Alljärgneval joonisel on esitatud hoolduskatkestuse registreerimise näide.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-129">The illustration below shows an example of maintenance downtime registration.</span></span>

![Joonis 2](media/16-work-orders.png)

<span data-ttu-id="ff5f6-131">Hoolduskatkestuse registreeringuteks kasutatav kalender oleneb teie varade ja parameetrite seadistustes tehtud valikust.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-131">The calendar that is used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="ff5f6-132">Kui varale on valitud ressurss lehe **Kõik varad** kiirkaardi **Põhivara** väljal **Ressurss**, kasutatakse seotud ressursirühma kalendri seadistust, nii nagu näidatud järgmisel joonisel.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-132">If a resource is selected on an asset in the **Resource** field on the **Fixed asset** FastTab of the **All assets** page, the calendar that is set up for the associated resource group is used, as shown in the following illustration.</span></span>

![Joonis 3](media/17-work-orders.png)

<span data-ttu-id="ff5f6-134">Kui varale ressurssi valitud ei ole, kasutatakse standardset kalendrit, mis on valitud lehel **Varahalduse parameetrid**, nii nagu näidatud järgmisel joonisel.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-134">If no resource is selected on the asset, the standard calendar that is selected on the **Asset management parameters** page is used, as shown in the following illustration.</span></span>

![Joonis 4](media/18-work-orders.png)

<span data-ttu-id="ff5f6-136">Kõigi hoolduskatkestuste registreeringute ülevaate vaatamiseks valige **Varahaldus** > **Päringud** > **Hoolduskatkestus**.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-136">To see an overview of all maintenance downtime registrations, click **Asset management** > **Inquiries** > **Maintenance downtime**.</span></span>

>[!NOTE]
><span data-ttu-id="ff5f6-137">Kõik moodulis **Varahaldus** kasutatud kalendrid seadistatakse jaotises **Organisatsiooni haldus** > **Seadistus** > **Kalendrid** > **Kalendrid**.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-137">All calendars that are used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]