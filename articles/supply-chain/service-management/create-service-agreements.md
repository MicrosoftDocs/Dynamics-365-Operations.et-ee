---
title: Hoolduslepete loomine
description: See teema kirjeldab, kuidas kasutada funktsioone moodulites Hooldushaldus ning Projektihaldus ja raamatupidamine hoolduslepete loomiseks.
author: ShylaThompson
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
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
ms.openlocfilehash: a094ce9f0d9323b089055e74d41cf1f45323a7d4
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---

# <a name="create-service-agreements"></a><span data-ttu-id="c3bf0-103">Hoolduslepete loomine</span><span class="sxs-lookup"><span data-stu-id="c3bf0-103">Create service agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3bf0-104">See teema kirjeldab, kuidas kasutada funktsioone moodulites Hooldushaldus ning Projektihaldus ja raamatupidamine hoolduslepete loomiseks.</span><span class="sxs-lookup"><span data-stu-id="c3bf0-104">This topic describes how to use features in the Service management and the Project management and accounting modules to create service agreements.</span></span>

## <a name="create-a-service-agreement-from-service-management"></a><span data-ttu-id="c3bf0-105">Hooldusleppe loomine hooldushaldusest</span><span class="sxs-lookup"><span data-stu-id="c3bf0-105">Create a service agreement from Service management</span></span>

1. <span data-ttu-id="c3bf0-106">Navigeerige jaotisesse **Hooldushaldus**.</span><span class="sxs-lookup"><span data-stu-id="c3bf0-106">Navigate to **Service management**.</span></span>
2. <span data-ttu-id="c3bf0-107">Klõpsake valikut **Hoolduslepped** uue hooldusleppe rea loomiseks lehe päises.</span><span class="sxs-lookup"><span data-stu-id="c3bf0-107">Click **Service agreements** to create a new service agreement line in the page header.</span></span> 
3. <span data-ttu-id="c3bf0-108">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c3bf0-108">Click **New**.</span></span> <span data-ttu-id="c3bf0-109">Sisestage kirjeldus, valige viide projektile väljal **Projekti ID** ja täitke hooldusleppe ülejäänud väljad ja read.</span><span class="sxs-lookup"><span data-stu-id="c3bf0-109">Enter a description, select a reference to a project in the **Project ID** field, and fill in the rest of the fields and lines for the service agreement.</span></span> <span data-ttu-id="c3bf0-110">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c3bf0-110">Click **Save**.</span></span>
4. <span data-ttu-id="c3bf0-111">Vahekaardil **Seosed** klõpsake valikuid **Hooldusobjektid** või **Hooldustoimingud**, et luua hooldusleppe jaoks hooldusobjekti seosed või hooldusetoimingu seosed.</span><span class="sxs-lookup"><span data-stu-id="c3bf0-111">On the **Relations** tab, select **Service objects** or **Service tasks** to create service object relations or service task relations for the service agreement.</span></span> <span data-ttu-id="c3bf0-112">Hooldusobjekte ja ülesandeid, millele olete loonud seosed, saab kinnitada hooldusleppe ridadele.</span><span class="sxs-lookup"><span data-stu-id="c3bf0-112">The service objects and tasks that you have created relations for can be attached on the lines of the service agreement.</span></span>
5. <span data-ttu-id="c3bf0-113">Lehe alumises pooles looge hooldusleppe ridu, kopeerides hooldusmalli või teise hooldusleppe ridu või looge neid käsitsi.</span><span class="sxs-lookup"><span data-stu-id="c3bf0-113">In the lower half of the page, create service agreement lines by copying lines from a service template, another service agreement, or manually creating the service-agreement lines.</span></span>

> [!NOTE]
> <span data-ttu-id="c3bf0-114">Kui kopeerite read hooldusleppesse mõnest teisest hooldusleppest, saate näidata, kas soovite kopeerida ka hooldusobjekti ja hooldustoimingute seosed.</span><span class="sxs-lookup"><span data-stu-id="c3bf0-114">If you copy lines into the service agreement from another service agreement, you can indicate whether you also want to copy service object and service task relations.</span></span> <span data-ttu-id="c3bf0-115">Kui kopeerite need seosed, liidetakse need iga olemasoleva seosega hooldusleppes.</span><span class="sxs-lookup"><span data-stu-id="c3bf0-115">If you copy these relations, they are added to any existing relations on the service agreement.</span></span> <span data-ttu-id="c3bf0-116">Kui kopeerite hooldusleppe read hooldusmallist, kopeeritakse hooldusobjekti ja hooldustoimingute seosed automaatselt uue hooldusleppe ridadele kui hooldusobjekti seosed ja hooldustoimingute seosed.</span><span class="sxs-lookup"><span data-stu-id="c3bf0-116">If you copy service-agreement lines from a service template, the service-object and service-task relations are automatically copied as service-object relations and service-task relations on the new service-agreement lines.</span></span>

## <a name="create-service-agreement-lines-manually"></a><span data-ttu-id="c3bf0-117">Hooldusleppe ridade loomine käsitsi</span><span class="sxs-lookup"><span data-stu-id="c3bf0-117">Create service agreement lines manually</span></span>

1. <span data-ttu-id="c3bf0-118">Lisage lehelt **Hoolduslepped** ridade ruudistikku hooldusleppe rida.</span><span class="sxs-lookup"><span data-stu-id="c3bf0-118">From the **Service agreements** page, add a service agreement line in the lines grid.</span></span> 
2. <span data-ttu-id="c3bf0-119">Sisestage hooldusleppe rea vajalik teave.</span><span class="sxs-lookup"><span data-stu-id="c3bf0-119">Enter the appropriate information for the service agreement line.</span></span> 
3. <span data-ttu-id="c3bf0-120">Rea salvestamiseks vajutage klahve **CTRL+S** ja sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c3bf0-120">Press **CTRL+S** to save the line, and then close the page.</span></span>

## <a name="create-a-service-agreement-from-project"></a><span data-ttu-id="c3bf0-121">Projektist hooldusleppe loomine</span><span class="sxs-lookup"><span data-stu-id="c3bf0-121">Create a service agreement from Project</span></span>

1. <span data-ttu-id="c3bf0-122">Klõpsake valikut **Projektihaldus ja raamatupidamine**.</span><span class="sxs-lookup"><span data-stu-id="c3bf0-122">Click **Project management and accounting**.</span></span>
2. <span data-ttu-id="c3bf0-123">Klõpsake valikut **Kõik projektid**.</span><span class="sxs-lookup"><span data-stu-id="c3bf0-123">Click **All projects**.</span></span>
3. <span data-ttu-id="c3bf0-124">Valige loendist soovitud projekt.</span><span class="sxs-lookup"><span data-stu-id="c3bf0-124">Select the project from the list.</span></span>
4. <span data-ttu-id="c3bf0-125">Klõpsake **tegumireal** valikut **Haldamine**.</span><span class="sxs-lookup"><span data-stu-id="c3bf0-125">On the **Action Pane**, click **Manage**.</span></span> <span data-ttu-id="c3bf0-126">Tegevusgrupis **Uus** klõpsake valikut **Hooldus** ja seejärel **Hoolduslepe**.</span><span class="sxs-lookup"><span data-stu-id="c3bf0-126">In the **New** Action group, click **Service** and select **Service agreement**.</span></span>
5. <span data-ttu-id="c3bf0-127">Projekti viite sisestamiseks järgige jaotises **Hooldusleppe loomine** kirjeldatud protsessi.</span><span class="sxs-lookup"><span data-stu-id="c3bf0-127">Follow the steps in the section titled **Create a service agreement** as described earlier in this topic to enter the project reference.</span></span>


## <a name="related-topics"></a><span data-ttu-id="c3bf0-128">Seotud teemad</span><span class="sxs-lookup"><span data-stu-id="c3bf0-128">Related topics</span></span>

[<span data-ttu-id="c3bf0-129">Hoolduslepped</span><span class="sxs-lookup"><span data-stu-id="c3bf0-129">Service agreements</span></span>](service-agreements.md)



