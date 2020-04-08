---
title: Hankija kujunduste vaheldumisi aktiveerimine
description: Selles teemas kirjeldatakse, kuidas lülitada hankija andmete integreerimist teenusekomplekti Finance and Operations rakenduste ja teenuse Common Data Service vahel.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: ffd7a4c01810578b4abb6942aeff76e5147fafa9
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173035"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="442a5-103">Hankija kujunduste vaheldumisi aktiveerimine</span><span class="sxs-lookup"><span data-stu-id="442a5-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="442a5-104">Hankijaandmete voog</span><span class="sxs-lookup"><span data-stu-id="442a5-104">Vendor data flow</span></span> 

<span data-ttu-id="442a5-105">Kui otsustate kasutada üksust **Konto** tüübiga **Organisatsioon** hankijate talletamiseks ja üksust **Kontakt** tüübiga **Isik** hankijate talletamiseks, konfigureerige järgmised töövood.</span><span class="sxs-lookup"><span data-stu-id="442a5-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="442a5-106">Vastasel juhul ei ole see konfiguratsioon nõutav.</span><span class="sxs-lookup"><span data-stu-id="442a5-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="442a5-107">Laiendatud hankija kujunduse kasutamine Organisatsiooni tüübiga hankijate puhul</span><span class="sxs-lookup"><span data-stu-id="442a5-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="442a5-108">Lahendusepakett **Dynamics365FinanceExtended** sisaldab järgmisi töövoo protsessi malle.</span><span class="sxs-lookup"><span data-stu-id="442a5-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="442a5-109">Iga malli jaoks luuakse töövoog.</span><span class="sxs-lookup"><span data-stu-id="442a5-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="442a5-110">Hankijate loomine kontode üksuses</span><span class="sxs-lookup"><span data-stu-id="442a5-110">Create Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="442a5-111">Hankijate loomine hankijate üksuses</span><span class="sxs-lookup"><span data-stu-id="442a5-111">Create Vendors in Vendors Entity</span></span>
+ <span data-ttu-id="442a5-112">Hankijate värskendamine kontode üksuses</span><span class="sxs-lookup"><span data-stu-id="442a5-112">Update Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="442a5-113">Hankijate värskendamine hankijate üksuses</span><span class="sxs-lookup"><span data-stu-id="442a5-113">Update Vendors in Vendors Entity</span></span>

<span data-ttu-id="442a5-114">Uute töövooprotsesside loomiseks töövooprotsessi mallide abil toimige järgnevalt.</span><span class="sxs-lookup"><span data-stu-id="442a5-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="442a5-115">Looge töövooprotsess üksusele **Hankija** ja valige töövooprotsessi mall **Hankijate loomine kontode üksuses**.</span><span class="sxs-lookup"><span data-stu-id="442a5-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="442a5-116">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="442a5-116">Then select **OK**.</span></span> <span data-ttu-id="442a5-117">See töövoog käsitseb üksuse **Konto** hankija loomise stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="442a5-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![Hankijate loomine kontode üksuse töövoo protsessis](media/create_process.png)

2. <span data-ttu-id="442a5-119">Looge töövooprotsess üksusele **Hankija** ja valige töövooprotsessi mall **Hankijate värskendamine kontode üksuses**.</span><span class="sxs-lookup"><span data-stu-id="442a5-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="442a5-120">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="442a5-120">Then select **OK**.</span></span> <span data-ttu-id="442a5-121">See töövoog käsitseb üksuse **Konto** hankija värskendamise stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="442a5-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="442a5-122">Looge töövooprotsess üksusele **Konto** ja valige töövooprotsessi mall **Hankijate loomine hankijate üksuses**.</span><span class="sxs-lookup"><span data-stu-id="442a5-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Entity** workflow process template.</span></span>
4. <span data-ttu-id="442a5-123">Looge töövooprotsess üksusele **Konto** ja valige töövooprotsessi mall **Hankijate värskendamine hankijate üksuses**.</span><span class="sxs-lookup"><span data-stu-id="442a5-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Entity** workflow process template.</span></span>
5. <span data-ttu-id="442a5-124">Saate konfigureerida töövoogusid kas reaalaja töövoogudena või taustatöövoogudena, olenevalt teie nõuetest.</span><span class="sxs-lookup"><span data-stu-id="442a5-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="442a5-125">Töövoo konfigureerimiseks taustatöövoona valige **Teisenda taustatöövooks**.</span><span class="sxs-lookup"><span data-stu-id="442a5-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Teisendamine taustatöövoo nupuks](media/background_workflow.png)

6. <span data-ttu-id="442a5-127">Aktiveerige töövood, mille lõite üksustele **Konto** ja **Hankija**, et hakata kasutama üksust **Konto** tüübiga **Organisatsioon** hankijate teabe salvestamiseks.</span><span class="sxs-lookup"><span data-stu-id="442a5-127">Activate the workflows that you created for the **Account** and **Vendor** entities to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="442a5-128">Laiendatud hankija kujunduse kasutamine Isiku tüübiga hankijate puhul</span><span class="sxs-lookup"><span data-stu-id="442a5-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="442a5-129">Lahendusepakett **Dynamics365FinanceExtended** sisaldab järgmisi töövoo protsessi malle.</span><span class="sxs-lookup"><span data-stu-id="442a5-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="442a5-130">Iga malli jaoks luuakse töövoog.</span><span class="sxs-lookup"><span data-stu-id="442a5-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="442a5-131">Isiku tüübiga hankijate loomine hankijate olemis</span><span class="sxs-lookup"><span data-stu-id="442a5-131">Create Vendors of type Person in Vendors Entity</span></span>
+ <span data-ttu-id="442a5-132">Isiku tüübiga hankijate loomine kontaktide olemis</span><span class="sxs-lookup"><span data-stu-id="442a5-132">Create Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="442a5-133">Isiku tüübiga hankijate värskendamine kontaktide olemis</span><span class="sxs-lookup"><span data-stu-id="442a5-133">Update Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="442a5-134">Isiku tüübiga hankijate värskendamine hankijate olemis</span><span class="sxs-lookup"><span data-stu-id="442a5-134">Update Vendors of type Person in Vendors Entity</span></span>

<span data-ttu-id="442a5-135">Uute töövooprotsesside loomiseks töövooprotsessi mallide abil toimige järgnevalt.</span><span class="sxs-lookup"><span data-stu-id="442a5-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="442a5-136">Looge töövooprotsess üksusele **Hankija** ja valige töövooprotsessi mall **Isiku tüübiga hankijate loomine kontode üksuses**.</span><span class="sxs-lookup"><span data-stu-id="442a5-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="442a5-137">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="442a5-137">Then select **OK**.</span></span> <span data-ttu-id="442a5-138">See töövoog käsitseb üksuse **Kontakt** hankija loomise stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="442a5-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="442a5-139">Looge töövooprotsess üksusele **Hankija** ja valige töövooprotsessi mall **Isiku tüübiga hankijate värskendamine kontode üksuses**.</span><span class="sxs-lookup"><span data-stu-id="442a5-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="442a5-140">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="442a5-140">Then select **OK**.</span></span> <span data-ttu-id="442a5-141">See töövoog käsitseb üksuse **Kontakt** hankija värskendamise stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="442a5-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="442a5-142">Looge töövooprotsess üksusele **Kontakt** ja valige mall **Isiku tüübiga hankijate loomine hankijate üksuses**.</span><span class="sxs-lookup"><span data-stu-id="442a5-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Entity** template.</span></span>
4. <span data-ttu-id="442a5-143">Looge töövooprotsess üksusele **Kontakt** ja valige mall **Isiku tüübiga hankijate värskendamine hankijate üksuses**.</span><span class="sxs-lookup"><span data-stu-id="442a5-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Entity** template.</span></span>
5. <span data-ttu-id="442a5-144">Saate konfigureerida töövoogusid kas reaalaja töövoogudena või taustatöövoogudena, olenevalt teie nõuetest.</span><span class="sxs-lookup"><span data-stu-id="442a5-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="442a5-145">Töövoo konfigureerimiseks taustatöövoona valige **Teisenda taustatöövooks**.</span><span class="sxs-lookup"><span data-stu-id="442a5-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="442a5-146">Aktiveerige töövood, mille lõite üksustele **Kontakt** ja **Hankija**, et hakata kasutama üksust **Kontakt** tüübiga **Isik** hankijate teabe salvestamiseks.</span><span class="sxs-lookup"><span data-stu-id="442a5-146">Activate the workflows that you created on the **Contact** and **Vendor** entities to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
