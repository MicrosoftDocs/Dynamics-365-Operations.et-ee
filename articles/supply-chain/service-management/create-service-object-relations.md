---
title: teenusobjektide seoste loomine
description: Teemas kirjeldatakse, kuidas luua teenuseleppe ja teenusetellimuse jaoks teenuseobjekti seoseid.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 792ceea52a9caa1a99217c77bb3fe4aafb80a0eb
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---

# <a name="create-service-object-relations"></a><span data-ttu-id="d4a5c-103">teenusobjektide seoste loomine</span><span class="sxs-lookup"><span data-stu-id="d4a5c-103">Create service object relations</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d4a5c-104">Teemas kirjeldatakse, kuidas luua teenuseleppe ja teenusetellimuse jaoks teenuseobjekti seoseid.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-104">This topic describes how to create service object relations for a service agreement and a service order.</span></span> <span data-ttu-id="d4a5c-105">Teenuseobjekti seose loomisel seostate teenuseobjekti teenuseleppe või teenusetellimusega.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-105">When you a create service object relation, you associate the service object to a service agreement or service order.</span></span> <span data-ttu-id="d4a5c-106">Kui klient taotleb teenust kauba puhul, mis on teenuseobjekti, saate valida teenuseobjekti seoste loendist.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-106">When a customer requests service for an item that is a service object, you can select the service object from the list of service object relations.</span></span>

## <a name="create-a-service-object-relation-for-a-service-agreement"></a><span data-ttu-id="d4a5c-107">Teenuseobjekti seose loomine teenuseleppe jaoks</span><span class="sxs-lookup"><span data-stu-id="d4a5c-107">Create a service object relation for a service agreement</span></span>

<span data-ttu-id="d4a5c-108">Teenuseleppe jaoks teenuseobjekti seose loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-108">Use the following steps to create a service object relation for a service agreement:</span></span>

1.  <span data-ttu-id="d4a5c-109">Klõpsake valikut **Hooldushaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldusleppegrupid**.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-109">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="d4a5c-110">Valige loendis **Hoolduslepped** olemasolev hoolduslepe või klõpsake uue hooldusleppe loomiseks valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-110">In the **Service agreements** list, select an existing service agreement, or click **New** to create a new service agreement.</span></span>

3.  <span data-ttu-id="d4a5c-111">Klõpsake vormi **Hoolduslepped** **toimingupaani** vahekaardi **Hoolduslepe** grupis **Seosed** valikut **Teenuse objektid**.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-111">In the **Service agreements** form, on the **Action Pane**, on the **Service agreement** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="d4a5c-112">Klõpsake vormil **Teenuse objektid** valikut **Uus** ja seejärel valige hooldusleppe jaoks hooldusobjekt.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-112">In the **Service objects** form, click **New**, and then select a service object for this service agreement.</span></span>

5.  <span data-ttu-id="d4a5c-113">Hooldusleppele mallkoosluse (BOM) määramiseks klõpsake valikut **Funktsioonid** ja seejärel valige **Lisa mallkooslus**.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-113">To assign a template bill of materials (BOM) to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="d4a5c-114">Valige mall vormi **Lisa mallkooslus** väljal **Mallkooslus**.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-114">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 

## <a name="create-a-service-object-relation-for-a-service-order"></a><span data-ttu-id="d4a5c-115">Teenuseobjekti seose loomine teenusetellimuse jaoks</span><span class="sxs-lookup"><span data-stu-id="d4a5c-115">Create a service object relation for a service order</span></span>

<span data-ttu-id="d4a5c-116">Teenusetellimuse jaoks teenuseobjekti seose loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-116">Use the following steps to create a service object relation for a service order:</span></span>

1.  <span data-ttu-id="d4a5c-117">Klõpsake valikuid **Teenusehaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldustellimused**.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="d4a5c-118">Valige loendis **Hooldustellimused** olemasolev hooldustellimus või looge uus.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-118">In the **Service orders** list, select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="d4a5c-119">Klõpsake vormi **Hooldustellimused** **toimingupaani** vahekaardi **Hooldustellimus** grupis **Seosed** valikut **Teenuse objektid**.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-119">In the **Service orders** form, on the **Action Pane**, on the **Service order** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="d4a5c-120">Klõpsake vormil **Teenuse objektid** valikut **Uus** ja seejärel valige hooldustellimuse jaoks hooldusobjekt.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-120">In the **Service objects** form, click **New**, and then select a service object for this service order.</span></span>

5.  <span data-ttu-id="d4a5c-121">Hooldusleppele mallkoosluse määramiseks klõpsake valikut **Funktsioonid** ja seejärel valige **Lisa mallkooslus**.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-121">To assign a template BOM to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="d4a5c-122">Valige mall vormi **Lisa mallkooslus** väljal **Mallkooslus**.</span><span class="sxs-lookup"><span data-stu-id="d4a5c-122">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 


## <a name="see-also"></a><span data-ttu-id="d4a5c-123">Vt ka</span><span class="sxs-lookup"><span data-stu-id="d4a5c-123">See also</span></span>

[<span data-ttu-id="d4a5c-124">Teenusobjektid</span><span class="sxs-lookup"><span data-stu-id="d4a5c-124">Service objects</span></span>](service-objects.md)

[<span data-ttu-id="d4a5c-125">teenuse objekti seosed</span><span class="sxs-lookup"><span data-stu-id="d4a5c-125">service object relations</span></span>](service-object-relations.md)

[<span data-ttu-id="d4a5c-126">Mallkooslused</span><span class="sxs-lookup"><span data-stu-id="d4a5c-126">Template BOMs</span></span>](template-boms.md)

  



