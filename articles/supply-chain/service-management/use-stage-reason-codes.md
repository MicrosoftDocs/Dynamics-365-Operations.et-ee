---
title: Etapi põhjuse koodide kasutamine
description: Teenindustaseme lepingu (SLA) tühistamise või SLA-s kehtestatud ajalimiidi ületamise põhjuse näitamiseks kasutate te põhjusekoodi.
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33fa7e5f08f09fe109d0507d686315d01e043928
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "323912"
---
# <a name="use-stage-reason-codes"></a><span data-ttu-id="5bc40-103">Etapi põhjuse koodide kasutamine</span><span class="sxs-lookup"><span data-stu-id="5bc40-103">Use stage reason codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="5bc40-104">Teenindustaseme lepingu (SLA) tühistamise või SLA-s kehtestatud ajalimiidi ületamise põhjuse näitamiseks kasutate te põhjusekoodi.</span><span class="sxs-lookup"><span data-stu-id="5bc40-104">You use a reason code to indicate why a service level agreement (SLA) has been canceled, or why a service order has exceeded the time limit that is you define in the SLA.</span></span>

<span data-ttu-id="5bc40-105">Samuti saate määrata, et põhjusekood on nõutav SLA tühistamisel või kui tähtaeg ületab hooldustellimuse SLA jaoks määratu.</span><span class="sxs-lookup"><span data-stu-id="5bc40-105">You can also specify that a reason code is required when an SLA is canceled, or when the time limit exceeds the time that is specified in the SLA for the service order.</span></span>

<span data-ttu-id="5bc40-106">Kui määrasite, et põhjuse tähis on nõutav, tuleb põhjusekood sisestada järgmistes olukordades:</span><span class="sxs-lookup"><span data-stu-id="5bc40-106">If you have specified that a reason code is required, you must enter a reason code in the following situations:</span></span>

  - <span data-ttu-id="5bc40-107">Kui teenustellimus viiakse üle etappi, kus SLA-põhise teenustellimuse aja kirjendamise seiskub.</span><span class="sxs-lookup"><span data-stu-id="5bc40-107">When a service order is moved to a stage that stops time recording against the SLA for the service order.</span></span>

  - <span data-ttu-id="5bc40-108">Kui teenustellimusest on välja logitud.</span><span class="sxs-lookup"><span data-stu-id="5bc40-108">When the service order is signed off.</span></span>

  - <span data-ttu-id="5bc40-109">Kui aja kirjendamine peatatakse käsitsi.</span><span class="sxs-lookup"><span data-stu-id="5bc40-109">When time recording is manually stopped.</span></span>

## <a name="set-up-reason-codes"></a><span data-ttu-id="5bc40-110">Põhjusekoodide häälestamine</span><span class="sxs-lookup"><span data-stu-id="5bc40-110">Set up reason codes</span></span>

1.  <span data-ttu-id="5bc40-111">Klõpsake valikuid **Teeninduse haldus** \> **Häälestus** \> **Hooldustellimused** \> **Etapi põhjuse koodid**.</span><span class="sxs-lookup"><span data-stu-id="5bc40-111">Click **Service management** \> **Setup** \> **Service orders** \> **Stage reason codes**.</span></span>

2.  <span data-ttu-id="5bc40-112">Klõpsake vormis **Etapi põhjusekoodid** uue põhjusekoodi loomiseks valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="5bc40-112">In the **Stage reason codes** form, click **New** to create a new reason code.</span></span>

3.  <span data-ttu-id="5bc40-113">Sisestage välja **Etapi põhjusekood** unikaalne etapi põhjusekood.</span><span class="sxs-lookup"><span data-stu-id="5bc40-113">In the **Stage reason code** field, enter a unique stage reason code.</span></span>

4.  <span data-ttu-id="5bc40-114">Sisestage välja **Kirjeldus** etapi põhjusekoodi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="5bc40-114">In the **Description** field, enter a description of the stage reason code.</span></span>

5.  <span data-ttu-id="5bc40-115">Muudatuste salvestamiseks sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="5bc40-115">Close the form to save your changes.</span></span>

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a><span data-ttu-id="5bc40-116">Põhjusekoodide nõudmine teenindustaseme lepingu tühistamisel</span><span class="sxs-lookup"><span data-stu-id="5bc40-116">Require reason codes when a service level agreement is canceled</span></span>

1.  <span data-ttu-id="5bc40-117">Klõpsake valikul **Hooldushaldus** \> **Häälestus** \> **Teenuste halduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="5bc40-117">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="5bc40-118">Klõpsake vormis **Teenuste halduse parameetrid** linki **Üldine** ja valige märkeruut **Tühistamise põhjusekood**.</span><span class="sxs-lookup"><span data-stu-id="5bc40-118">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on canceling** check box.</span></span>

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a><span data-ttu-id="5bc40-119">Põhjusekoodide nõudmine teenindustaseme lepingus kehtestatud teenusetellimuse ajalimiidi ületamisel</span><span class="sxs-lookup"><span data-stu-id="5bc40-119">Require reason codes when the a service order exceeds the time limit that is set by the service level agreement</span></span>

1.  <span data-ttu-id="5bc40-120">Klõpsake valikul **Hooldushaldus** \> **Häälestus** \> **Teenuste halduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="5bc40-120">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="5bc40-121">Klõpsake vormis **Teenuste halduse parameetrid** linki **Üldine** ja valige märkeruut **Aja ületamise põhjusekood**.</span><span class="sxs-lookup"><span data-stu-id="5bc40-121">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on exceeding time** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="5bc40-122">Vt ka</span><span class="sxs-lookup"><span data-stu-id="5bc40-122">See also</span></span>

[<span data-ttu-id="5bc40-123">teenustellimuses aja salvestuse käivitamine ja salvestamine</span><span class="sxs-lookup"><span data-stu-id="5bc40-123">Start and stop time recording on a service order</span></span>](start-and-stop-time-recording-on-a-service-order.md)

  


