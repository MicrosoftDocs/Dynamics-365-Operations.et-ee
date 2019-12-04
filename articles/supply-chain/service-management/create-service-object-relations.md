---
title: teenusobjektide seoste loomine
description: Teemas kirjeldatakse, kuidas luua teenuseleppe ja teenusetellimuse jaoks teenuseobjekti seoseid.
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
ms.openlocfilehash: 05d770234beb486eb3a8181b160967c802c15e8f
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813151"
---
# <a name="create-service-object-relations"></a><span data-ttu-id="883f4-103">teenusobjektide seoste loomine</span><span class="sxs-lookup"><span data-stu-id="883f4-103">Create service object relations</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="883f4-104">Teemas kirjeldatakse, kuidas luua teenuseleppe ja teenusetellimuse jaoks teenuseobjekti seoseid.</span><span class="sxs-lookup"><span data-stu-id="883f4-104">This topic describes how to create service object relations for a service agreement and a service order.</span></span> <span data-ttu-id="883f4-105">Teenuseobjekti seose loomisel seostate teenuseobjekti teenuseleppe või teenusetellimusega.</span><span class="sxs-lookup"><span data-stu-id="883f4-105">When you a create service object relation, you associate the service object to a service agreement or service order.</span></span> <span data-ttu-id="883f4-106">Kui klient taotleb teenust kauba puhul, mis on teenuseobjekti, saate valida teenuseobjekti seoste loendist.</span><span class="sxs-lookup"><span data-stu-id="883f4-106">When a customer requests service for an item that is a service object, you can select the service object from the list of service object relations.</span></span>

## <a name="create-a-service-object-relation-for-a-service-agreement"></a><span data-ttu-id="883f4-107">Teenuseobjekti seose loomine teenuseleppe jaoks</span><span class="sxs-lookup"><span data-stu-id="883f4-107">Create a service object relation for a service agreement</span></span>

<span data-ttu-id="883f4-108">Teenuseleppe jaoks teenuseobjekti seose loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="883f4-108">Use the following steps to create a service object relation for a service agreement:</span></span>

1.  <span data-ttu-id="883f4-109">Klõpsake valikut **Hooldushaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldusleppegrupid**.</span><span class="sxs-lookup"><span data-stu-id="883f4-109">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="883f4-110">Valige loendis **Hoolduslepped** olemasolev hoolduslepe või klõpsake uue hooldusleppe loomiseks valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="883f4-110">In the **Service agreements** list, select an existing service agreement, or click **New** to create a new service agreement.</span></span>

3.  <span data-ttu-id="883f4-111">Klõpsake vormi **Hoolduslepped** **toimingupaani** vahekaardi **Hoolduslepe** grupis **Seosed** valikut **Teenuse objektid**.</span><span class="sxs-lookup"><span data-stu-id="883f4-111">In the **Service agreements** form, on the **Action Pane**, on the **Service agreement** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="883f4-112">Klõpsake vormil **Teenuse objektid** valikut **Uus** ja seejärel valige hooldusleppe jaoks hooldusobjekt.</span><span class="sxs-lookup"><span data-stu-id="883f4-112">In the **Service objects** form, click **New**, and then select a service object for this service agreement.</span></span>

5.  <span data-ttu-id="883f4-113">Hooldusleppele mallkoosluse (BOM) määramiseks klõpsake valikut **Funktsioonid** ja seejärel valige **Lisa mallkooslus**.</span><span class="sxs-lookup"><span data-stu-id="883f4-113">To assign a template bill of materials (BOM) to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="883f4-114">Valige mall vormi **Lisa mallkooslus** väljal **Mallkooslus**.</span><span class="sxs-lookup"><span data-stu-id="883f4-114">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 

## <a name="create-a-service-object-relation-for-a-service-order"></a><span data-ttu-id="883f4-115">Teenuseobjekti seose loomine teenusetellimuse jaoks</span><span class="sxs-lookup"><span data-stu-id="883f4-115">Create a service object relation for a service order</span></span>

<span data-ttu-id="883f4-116">Teenusetellimuse jaoks teenuseobjekti seose loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="883f4-116">Use the following steps to create a service object relation for a service order:</span></span>

1.  <span data-ttu-id="883f4-117">Klõpsake valikuid **Teenusehaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldustellimused**.</span><span class="sxs-lookup"><span data-stu-id="883f4-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="883f4-118">Valige loendis **Hooldustellimused** olemasolev hooldustellimus või looge uus.</span><span class="sxs-lookup"><span data-stu-id="883f4-118">In the **Service orders** list, select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="883f4-119">Klõpsake vormi **Hooldustellimused** **toimingupaani** vahekaardi **Hooldustellimus** grupis **Seosed** valikut **Teenuse objektid**.</span><span class="sxs-lookup"><span data-stu-id="883f4-119">In the **Service orders** form, on the **Action Pane**, on the **Service order** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="883f4-120">Klõpsake vormil **Teenuse objektid** valikut **Uus** ja seejärel valige hooldustellimuse jaoks hooldusobjekt.</span><span class="sxs-lookup"><span data-stu-id="883f4-120">In the **Service objects** form, click **New**, and then select a service object for this service order.</span></span>

5.  <span data-ttu-id="883f4-121">Hooldusleppele mallkoosluse määramiseks klõpsake valikut **Funktsioonid** ja seejärel valige **Lisa mallkooslus**.</span><span class="sxs-lookup"><span data-stu-id="883f4-121">To assign a template BOM to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="883f4-122">Valige mall vormi **Lisa mallkooslus** väljal **Mallkooslus**.</span><span class="sxs-lookup"><span data-stu-id="883f4-122">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 


## <a name="see-also"></a><span data-ttu-id="883f4-123">Vt ka</span><span class="sxs-lookup"><span data-stu-id="883f4-123">See also</span></span>

[<span data-ttu-id="883f4-124">Teenuseobjektide ülevaade</span><span class="sxs-lookup"><span data-stu-id="883f4-124">Service objects overview</span></span>](service-objects.md)

[<span data-ttu-id="883f4-125">Hooldusobjekti seosed</span><span class="sxs-lookup"><span data-stu-id="883f4-125">Service object relations</span></span>](service-object-relations.md)

[<span data-ttu-id="883f4-126">Mallkooslused</span><span class="sxs-lookup"><span data-stu-id="883f4-126">Template BOMs</span></span>](template-boms.md)

  


