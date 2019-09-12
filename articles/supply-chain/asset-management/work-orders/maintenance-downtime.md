---
title: Hoolduskatkestus
description: Selles teemas kirjeldatakse hoolduskatkestusi varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918240"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="426c2-103">Hoolduskatkestus</span><span class="sxs-lookup"><span data-stu-id="426c2-103">Maintenance downtime</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="426c2-104">Võite luua hoolduskatkestuse registreeringuid töökäsus valitud varale.</span><span class="sxs-lookup"><span data-stu-id="426c2-104">You can create maintenance downtime registrations on the asset selected on a work order.</span></span> <span data-ttu-id="426c2-105">See on kasulik, kui soovite registreerida hoolduskatkestuse ühele või enamale tootmisala masinale.</span><span class="sxs-lookup"><span data-stu-id="426c2-105">This is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="426c2-106">Kõigepealt loote hoolduskatkestuse põhjuse koodid, mida soovite kasutada, näiteks katkiminek ja planeeritud seiskamine.</span><span class="sxs-lookup"><span data-stu-id="426c2-106">First, you create the maintenance downtime reason codes that you want to use, for example, breakdown and planned stop.</span></span> <span data-ttu-id="426c2-107">Seda tehakse jaotises **Hoolduskatkestuse põhjuste koodid**.</span><span class="sxs-lookup"><span data-stu-id="426c2-107">This is done in **Maintenance downtime reason codes**.</span></span> <span data-ttu-id="426c2-108">Järgmisena loote hoolduskatkestuse registreeringud jaotises **Hoolduskatkestus** ja lisate asjakohase põhjuse koodid.</span><span class="sxs-lookup"><span data-stu-id="426c2-108">Next, you can create maintenance downtime registrations in **Maintenance downtime** and add the relevant reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="426c2-109">Hoolduskatkestuse põhjuse koodide loomine</span><span class="sxs-lookup"><span data-stu-id="426c2-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="426c2-110">Klõpsake suvandil **Varahaldus** > **Seadistus** > **töökäsud** > **Hoolduskatkestuse põhjuse koodid**.</span><span class="sxs-lookup"><span data-stu-id="426c2-110">Click **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="426c2-111">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="426c2-111">Click **New**.</span></span>

3. <span data-ttu-id="426c2-112">Sisestage ID väljale **Hoolduskatkestuse põhjuse kood**.</span><span class="sxs-lookup"><span data-stu-id="426c2-112">Insert an ID in the **Maintenance downtime reason code** field.</span></span>

4. <span data-ttu-id="426c2-113">Sisestage põhjuse koodi nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="426c2-113">Insert a name for the reason code in the **Name** field.</span></span>

5. <span data-ttu-id="426c2-114">Valige märkeruut **KPI sisaldus**, kui põhjuse kood peaks sisalduma vara KPI arvutustes.</span><span class="sxs-lookup"><span data-stu-id="426c2-114">Select the **KPI include** check box if the reason code should be included in asset KPI calculations.</span></span> <span data-ttu-id="426c2-115">Üldiselt ei peaks planeeritud tootmisseisakuid KPI arvutustesse kaasama, sest need ei mõjuta oodatavat jõudlust.</span><span class="sxs-lookup"><span data-stu-id="426c2-115">Generally, planned production stops should not be included in KPI calculations as they do not impact expected performance.</span></span>

6. <span data-ttu-id="426c2-116">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="426c2-116">Click **Save**.</span></span>

![Joonis 1](media/15-work-orders.png)


<span data-ttu-id="426c2-118">Kui olete loonud need hoolduskatkestuse põhjuse koodid, mida kasutada soovite, saate luua töökäskudele ja varadele hoolduskatkestuse registreeringuid.</span><span class="sxs-lookup"><span data-stu-id="426c2-118">When you have created the maintenance downtime reason codes you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="426c2-119">Hoolduskatkestuse registreeringute loomine</span><span class="sxs-lookup"><span data-stu-id="426c2-119">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="426c2-120">Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="426c2-120">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="426c2-121">Valige töökäsk ja klõpsake **Hoolduskatkestus**.</span><span class="sxs-lookup"><span data-stu-id="426c2-121">Select the work order and click **Maintenance downtime**.</span></span>

3. <span data-ttu-id="426c2-122">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="426c2-122">Click **New**.</span></span>

4. <span data-ttu-id="426c2-123">Sisestage hoolduskatkestuse registreeringu kuupäeva ja kellaaja intervall väljadele **Alates** ja **Kuni**.</span><span class="sxs-lookup"><span data-stu-id="426c2-123">Insert date and time interval for the maintenance downtime registration in the **From** and **To** fields.</span></span>

5. <span data-ttu-id="426c2-124">Kui lahkute väljalt **Kuni**, sisestatakse kestvus tundides automaatselt väljale **Kestvus**.</span><span class="sxs-lookup"><span data-stu-id="426c2-124">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

6. <span data-ttu-id="426c2-125">Sisestage põhjuse kood väljale **hoolduskatkestuse põhjuse kood**.</span><span class="sxs-lookup"><span data-stu-id="426c2-125">Select a reason code in the **maintenance downtime reason code** field.</span></span>

7. <span data-ttu-id="426c2-126">Kui soovite lisada rohkem registreeringuid, korrake ülaltoodud juhiseid 3–6.</span><span class="sxs-lookup"><span data-stu-id="426c2-126">Repeat steps 3-6 if you want to add more registrations.</span></span>

8. <span data-ttu-id="426c2-127">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="426c2-127">Click **Save**.</span></span>


![Joonis 2](media/16-work-orders.png)


<span data-ttu-id="426c2-129">Hoolduskatkestuse registreeringuteks kasutatav kalender oleneb teie varade ja parameetrite seadistustes tehtud valikust.</span><span class="sxs-lookup"><span data-stu-id="426c2-129">The calendar used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="426c2-130">Kui varale on valitud ressurss jaotise **Kõik varad** > **Põhivara** kiirkaardil > väljal **Ressurss**, kasutatakse seotud ressursirühma kalendri seadistust, nii nagu näidatud järgmisel joonisel.</span><span class="sxs-lookup"><span data-stu-id="426c2-130">If a resource is selected on an asset in **All assets** > **Fixed asset** FastTab > **Resource** field, the calendar set up for the associated resource group is used, as shown in the following figure.</span></span>

![Joonis 3](media/17-work-orders.png)


<span data-ttu-id="426c2-132">Kui varale ressurssi valitud ei ole, kasutatakse standardset kalendrit, mis on valitud jaotises **Varahalduse parameetrid**, nii nagu näidatud järgmisel joonisel.</span><span class="sxs-lookup"><span data-stu-id="426c2-132">If no resource is selected on the asset, the standard calendar selected in **Asset management parameters** is used, as shown in the following figure.</span></span>

![Joonis 4](media/18-work-orders.png)


<span data-ttu-id="426c2-134">Klõpsake **Ettevõtte varahaldus** > **Päringud** > **Hoolduskatkestus**, et näha kõigi hoolduskatkestuste registreeringute ülevaadet.</span><span class="sxs-lookup"><span data-stu-id="426c2-134">Click **Enterprise asset management** > **Inquiries** > **Maintenance downtime** to see an overview of all maintenance downtime registrations.</span></span>

>[!NOTE]
><span data-ttu-id="426c2-135">Kõik moodulis **Varahaldus** kasutatud kalendrid seadistatakse jaotises **Organisatsiooni haldus** > **Seadistus** > **Kalendrid** > **Kalendrid**.</span><span class="sxs-lookup"><span data-stu-id="426c2-135">All calendars used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

