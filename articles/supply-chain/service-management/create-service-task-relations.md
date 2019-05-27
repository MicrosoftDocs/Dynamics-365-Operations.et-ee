---
title: teenustoimingute seoste loomine
description: Leppe või tellimuse käigus tehtava hooldustoimingu kirjeldamiseks saate hooldustoimingud hoolduslepete või -tellimustega siduda.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2aa0e5200ff2a6822e631c72124335e2dc556c14
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552111"
---
# <a name="create-service-task-relations"></a><span data-ttu-id="569d0-103">teenustoimingute seoste loomine</span><span class="sxs-lookup"><span data-stu-id="569d0-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="569d0-104">Leppe või tellimuse käigus tehtava hooldustoimingu kirjeldamiseks saate hooldustoimingud hoolduslepete või -tellimustega siduda.</span><span class="sxs-lookup"><span data-stu-id="569d0-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="569d0-105">See teave on saadaval nii hooldustehnikutele kui ka klientidele.</span><span class="sxs-lookup"><span data-stu-id="569d0-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="569d0-106">Seose loomine teenusleppega</span><span class="sxs-lookup"><span data-stu-id="569d0-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="569d0-107">Klõpsake valikut **Hooldushaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldusleppegrupid**.</span><span class="sxs-lookup"><span data-stu-id="569d0-107">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="569d0-108">Valige olemasolev teenuslepe või looge uus.</span><span class="sxs-lookup"><span data-stu-id="569d0-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="569d0-109">Klõpsake toimingupaanil nuppu **Hooldustoimingud**.</span><span class="sxs-lookup"><span data-stu-id="569d0-109">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="569d0-110">Klõpsake vormil **Hooldustoimingud** uue rea loomiseks klahvikombinatsiooni CTRL + N ja seejärel valige hooldusleppega seotav hooldustoiming loendist **Hooldustoiming**.</span><span class="sxs-lookup"><span data-stu-id="569d0-110">On the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="569d0-111">Sisestage vahekaardi **Kirjeldus** vabadele tekstiväljadele sise- või välismärgete kirjeldused.</span><span class="sxs-lookup"><span data-stu-id="569d0-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="569d0-112">Sulge vorm kirje salvestamiseks.</span><span class="sxs-lookup"><span data-stu-id="569d0-112">Close the form to save the record.</span></span>

<span data-ttu-id="569d0-113">Korrake seda protseduuri seni, kuni olete loonud kõik vajalikud teenustoimingute seosed teenusleppe jaoks.</span><span class="sxs-lookup"><span data-stu-id="569d0-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="569d0-114">Nüüd saate määrata need teenustoimingud igale lisatud leppereale.</span><span class="sxs-lookup"><span data-stu-id="569d0-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="569d0-115">Teenusleppele loodav teenustoimingute seos on saadaval kõikidelt teenusleppele lisatud teenustellimustelt.</span><span class="sxs-lookup"><span data-stu-id="569d0-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="569d0-116">Seose loomine teenustellimusega</span><span class="sxs-lookup"><span data-stu-id="569d0-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="569d0-117">Klõpsake valikuid **Teenusehaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldustellimused**.</span><span class="sxs-lookup"><span data-stu-id="569d0-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="569d0-118">Valige olemasolev teenustellimus või looge uus.</span><span class="sxs-lookup"><span data-stu-id="569d0-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="569d0-119">Klõpsake toimingupaanil nuppu **Hooldustoimingud**.</span><span class="sxs-lookup"><span data-stu-id="569d0-119">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="569d0-120">Klõpsake vormil **Hooldustoimingud** uue rea loomiseks klahvikombinatsiooni CTRL + N ja seejärel valige hooldustellimusega seotavad hooldustoimingud loendist **Hooldustoiming**.</span><span class="sxs-lookup"><span data-stu-id="569d0-120">From the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="569d0-121">Sisestage vahekaardi **Kirjeldus** vabadele tekstiväljadele sise- või välismärgete kirjeldused.</span><span class="sxs-lookup"><span data-stu-id="569d0-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="569d0-122">Sulge vorm kirje salvestamiseks.</span><span class="sxs-lookup"><span data-stu-id="569d0-122">Close the form to save the record.</span></span>

<span data-ttu-id="569d0-123">Korrake seda protseduuri seni, kuni olete loonud kõik vajalikud teenustoimingute seosed teenustellimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="569d0-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="569d0-124">Nüüd saate valida teenustoimingu, mille jaoks olete loonud seose teenustellimuste ridade loomisel.</span><span class="sxs-lookup"><span data-stu-id="569d0-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="569d0-125">Teenustellimusel loodavad teenustoimingute seosed on kättesaadavad konkreetse teenustellimuse puhul.</span><span class="sxs-lookup"><span data-stu-id="569d0-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="569d0-126">Vt ka</span><span class="sxs-lookup"><span data-stu-id="569d0-126">See also</span></span>

[<span data-ttu-id="569d0-127">Teenustoimingud</span><span class="sxs-lookup"><span data-stu-id="569d0-127">Service tasks</span></span>](service-tasks.md)


  


