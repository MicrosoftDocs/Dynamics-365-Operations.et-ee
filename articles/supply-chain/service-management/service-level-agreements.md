---
title: Teenusetaseme lepingute ülevaade
description: Teenindustaseme lepingus nõustub klient minimaalse reageerimisajaga, mille arvestamise aluseks on ajavahemik teenusettevõte probleemi registreerimise ja probleemi lahendamise vahel.
author: ShylaThompson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 90915502100c6165838f7eb2ebc620c7b15e6ec8
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865917"
---
# <a name="service-level-agreements-overview"></a><span data-ttu-id="0fd83-103">Teenusetaseme lepingute ülevaade</span><span class="sxs-lookup"><span data-stu-id="0fd83-103">Service level agreements overview</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0fd83-104">Teenusetaseme lepe (SLA) on teenusettevõtte ja teenuskliendi vaheline leping.</span><span class="sxs-lookup"><span data-stu-id="0fd83-104">A service level agreement (SLA) is an agreement between a service company and a service customer.</span></span> <span data-ttu-id="0fd83-105">Teenusetaseme leppes nõustub klient minimaalse reageerimisajaga, mille arvestamise aluseks on ajavahemik teenusettevõte probleemi registreerimise ja probleemi lahendamise vahel.</span><span class="sxs-lookup"><span data-stu-id="0fd83-105">In a SLA, the customer agrees to a minimum response time based on when the service company records the issue and when the issue is resolved.</span></span>

<span data-ttu-id="0fd83-106">Teenusetaseme lepe kehtestab klientidele pakutava standardse teenusetaseme, samuti muudab see teenusettevõtte jaoks selgeks, millal teenusetöö tuleb lõpetada.</span><span class="sxs-lookup"><span data-stu-id="0fd83-106">A SLA enforces a standard level of service that is offered to customers, and also makes it transparent to a service company when a service job should be completed.</span></span>

<span data-ttu-id="0fd83-107">Kliendile erinevate teenusetasemete pakkumiseks saab luua mis tahes arvu teenusetaseme leppeid.</span><span class="sxs-lookup"><span data-stu-id="0fd83-107">Any number of SLAs can be created to offer service customers different levels of service.</span></span>

## <a name="create-a-service-level-agreement"></a><span data-ttu-id="0fd83-108">Teenusetaseme leppe loomine</span><span class="sxs-lookup"><span data-stu-id="0fd83-108">Create a service level agreement</span></span>

1.  <span data-ttu-id="0fd83-109">Klõpsake valikut **Teenuste haldus** \> **Häälestamine** \> **Hoolduslepped** \> **Teenindustaseme lepingud**.</span><span class="sxs-lookup"><span data-stu-id="0fd83-109">Click **Service management** \> **Setup** \> **Service agreements** \> **Service level agreements**.</span></span>

2.  <span data-ttu-id="0fd83-110">Sisestage väljale **Teenindustaseme leping** teenindustaseme lepingu nimi.</span><span class="sxs-lookup"><span data-stu-id="0fd83-110">Type a name for the service level agreement in the **Service level agreement** field.</span></span>

3.  <span data-ttu-id="0fd83-111">Sisestage aeg, millal soovite lubada teenindustaseme lepinguga seotud lõpetatud teenuse kõned.</span><span class="sxs-lookup"><span data-stu-id="0fd83-111">Type the time that you want to allow for completion of service calls that are attached to the service level agreement.</span></span> <span data-ttu-id="0fd83-112">Seejärel valige kalender, kui soovite teenindustaseme lepingu aluseks võtta konkreetse kalendri.</span><span class="sxs-lookup"><span data-stu-id="0fd83-112">Then select a calendar if you want to base the service level agreement on a specific calendar.</span></span>

## <a name="apply-a-service-level-agreement"></a><span data-ttu-id="0fd83-113">Teenusetaseme leppe rakendamine</span><span class="sxs-lookup"><span data-stu-id="0fd83-113">Apply a service level agreement</span></span>

<span data-ttu-id="0fd83-114">Teenusetaseme lepe rakendatakse otse teenuselepingule.</span><span class="sxs-lookup"><span data-stu-id="0fd83-114">The SLA is applied directly to a service agreement.</span></span>

<span data-ttu-id="0fd83-115">Hooldustellimused, mille loote käsitsi ja seote teenusetaseme leppega teenuselepingusse antud teenusetaseme leppe alusel.</span><span class="sxs-lookup"><span data-stu-id="0fd83-115">Service orders that you create manually and attach to a service agreement that has an SLA are measured against that SLA.</span></span>

<span data-ttu-id="0fd83-116">Automaatselt loodud teenusetellimusi teenusetaseme leppega ei seota.</span><span class="sxs-lookup"><span data-stu-id="0fd83-116">Service orders that you create automatically are not attached to an SLA.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a><span data-ttu-id="0fd83-117">Teenusetaseme leppe rakendamine teenuseleppele</span><span class="sxs-lookup"><span data-stu-id="0fd83-117">Apply the service level agreement to the service agreement</span></span>

1.  <span data-ttu-id="0fd83-118">Klõpsake valikut **Hooldushaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldusleppegrupid**.</span><span class="sxs-lookup"><span data-stu-id="0fd83-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="0fd83-119">Valige teenuselepe, millele soovite teenusetaseme leppe rakendada, ja klõpsake **toimingupaanil** valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="0fd83-119">Select the service agreement that you want to apply the SLA to, and then click **Edit** on the **Action Pane**.</span></span>

2.  <span data-ttu-id="0fd83-120">Valige väljal **Teenindustaseme leping** teenindustaseme leping, mida soovite määrata.</span><span class="sxs-lookup"><span data-stu-id="0fd83-120">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a><span data-ttu-id="0fd83-121">Teenusetaseme leppe rakendamine teenuselepingu grupile</span><span class="sxs-lookup"><span data-stu-id="0fd83-121">Apply the service level agreement to the service agreement group</span></span>

1.  <span data-ttu-id="0fd83-122">Klõpsake valikut **Hooldushaldus** \> **Häälestamine** \> **Hooldustellimused** \> **Hooldusleppegrupid**.</span><span class="sxs-lookup"><span data-stu-id="0fd83-122">Click **Service management** \> **Setup** \> **Service agreements** \> **Service agreement groups**.</span></span>

2.  <span data-ttu-id="0fd83-123">Valige väljal **Teenindustaseme leping** teenindustaseme leping, mida soovite määrata.</span><span class="sxs-lookup"><span data-stu-id="0fd83-123">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="track-time-on-a-service-order-against-an-sla"></a><span data-ttu-id="0fd83-124">Teenusetellimuse aja jälgimine teenusetaseme leppe alusel</span><span class="sxs-lookup"><span data-stu-id="0fd83-124">Track time on a service order against an SLA</span></span>

<span data-ttu-id="0fd83-125">Kui loote uue hooldustellimuse teenuseleppele, millele on määratud teenindustaseme leping, käivitatakse teenuse tarnimise ajaintervall ja süsteem hakkab tarneaega jälgima.</span><span class="sxs-lookup"><span data-stu-id="0fd83-125">When you create a new service order for a service agreement that an SLA is assigned to, the time interval for the delivery of the service is initiated, and the system starts to track the delivery time.</span></span> <span data-ttu-id="0fd83-126">Peale selle saate seada järgmised valikud.</span><span class="sxs-lookup"><span data-stu-id="0fd83-126">Additionally, you can set the following options:</span></span>

  - <span data-ttu-id="0fd83-127">Saate alustada ja lõpetada teenusetellimuse aja registreerimise, et registreerida teenusetellimustele kulutatud aja kogusumma.</span><span class="sxs-lookup"><span data-stu-id="0fd83-127">You can start and stop time recording on the service order to register the total amount of time that is spent on service orders.</span></span>

  - <span data-ttu-id="0fd83-128">Saate jälgida kokkulangevust teenindustaseme lepingus seatud ajaintervalliga.</span><span class="sxs-lookup"><span data-stu-id="0fd83-128">You can monitor compliance with the time interval that is set in the service level agreement.</span></span>

  - <span data-ttu-id="0fd83-129">Saate määratleda põhjuse koodid, mis tuleb seadistada, kui teenindustaseme lepingus seatud ajaintervall ületatakse.</span><span class="sxs-lookup"><span data-stu-id="0fd83-129">You can define reason codes that must be set if the time interval of the service level agreement is exceeded.</span></span>

## <a name="see-also"></a><span data-ttu-id="0fd83-130">Vt ka</span><span class="sxs-lookup"><span data-stu-id="0fd83-130">See also</span></span>

[<span data-ttu-id="0fd83-131">teenustaseme lepingute vastavuse vaatamine</span><span class="sxs-lookup"><span data-stu-id="0fd83-131">View compliance with service level agreements</span></span>](view-compliance-with-service-level-agreements.md)

  


