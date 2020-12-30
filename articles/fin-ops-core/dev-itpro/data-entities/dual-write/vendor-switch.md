---
title: Hankija kujunduste vaheldumisi aktiveerimine
description: Selles teemas kirjeldatakse, kuidas lülitada hankija andmete integreerimist teenusekomplekti Finance and Operations rakenduste ja teenuse Dataverse vahel.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 731efd3ae841960f3a2c0b9be210c5c68ac835f5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685505"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="74011-103">Hankija kujunduste vaheldumisi aktiveerimine</span><span class="sxs-lookup"><span data-stu-id="74011-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="74011-104">Hankijaandmete voog</span><span class="sxs-lookup"><span data-stu-id="74011-104">Vendor data flow</span></span> 

<span data-ttu-id="74011-105">Kui otsustate kasutada üksust **Konto** tüübiga **Organisatsioon** hankijate talletamiseks ja üksust **Kontakt** tüübiga **Isik** hankijate talletamiseks, konfigureerige järgmised töövood.</span><span class="sxs-lookup"><span data-stu-id="74011-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="74011-106">Vastasel juhul ei ole see konfiguratsioon nõutav.</span><span class="sxs-lookup"><span data-stu-id="74011-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="74011-107">Laiendatud hankija kujunduse kasutamine Organisatsiooni tüübiga hankijate puhul</span><span class="sxs-lookup"><span data-stu-id="74011-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="74011-108">Lahendusepakett **Dynamics365FinanceExtended** sisaldab järgmisi töövoo protsessi malle.</span><span class="sxs-lookup"><span data-stu-id="74011-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="74011-109">Iga malli jaoks luuakse töövoog.</span><span class="sxs-lookup"><span data-stu-id="74011-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="74011-110">Hankijate loomine kontode tabelis</span><span class="sxs-lookup"><span data-stu-id="74011-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="74011-111">Hankijate loomine hankijate tabelis</span><span class="sxs-lookup"><span data-stu-id="74011-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="74011-112">Hankijate värskendamine kontode tabelis</span><span class="sxs-lookup"><span data-stu-id="74011-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="74011-113">Hankijate värskendamine hankijate tabelis</span><span class="sxs-lookup"><span data-stu-id="74011-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="74011-114">Uute töövooprotsesside loomiseks töövooprotsessi mallide abil toimige järgnevalt.</span><span class="sxs-lookup"><span data-stu-id="74011-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="74011-115">Looge töövooprotsess üksusele **Hankija** ja valige töövooprotsessi mall **Hankijate loomine kontode tabelis**.</span><span class="sxs-lookup"><span data-stu-id="74011-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="74011-116">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="74011-116">Then select **OK**.</span></span> <span data-ttu-id="74011-117">See töövoog käsitseb üksuse **Konto** hankija loomise stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="74011-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![Hankijate loomine kontode tabeli töövoo protsessis](media/create_process.png)

2. <span data-ttu-id="74011-119">Looge töövooprotsess üksusele **Hankija** ja valige töövooprotsessi mall **Hankijate värskendamine kontode tabelis**.</span><span class="sxs-lookup"><span data-stu-id="74011-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="74011-120">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="74011-120">Then select **OK**.</span></span> <span data-ttu-id="74011-121">See töövoog käsitseb üksuse **Konto** hankija värskendamise stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="74011-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="74011-122">Looge töövooprotsess üksusele **Konto** ja valige töövooprotsessi mall **Hankijate loomine hankijate tabelis**.</span><span class="sxs-lookup"><span data-stu-id="74011-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="74011-123">Looge töövooprotsess üksusele **Konto** ja valige töövooprotsessi mall **Hankijate värskendamine hankijate tabelis**.</span><span class="sxs-lookup"><span data-stu-id="74011-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="74011-124">Saate konfigureerida töövoogusid kas reaalaja töövoogudena või taustatöövoogudena, olenevalt teie nõuetest.</span><span class="sxs-lookup"><span data-stu-id="74011-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="74011-125">Töövoo konfigureerimiseks taustatöövoona valige **Teisenda taustatöövooks**.</span><span class="sxs-lookup"><span data-stu-id="74011-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Teisendamine taustatöövoo nupuks](media/background_workflow.png)

6. <span data-ttu-id="74011-127">Aktiveerige töövood, mille lõite tabelitele **Konto** ja **Hankija**, et hakata kasutama üksust **Konto** tüübiga **Organisatsioon** hankijate teabe salvestamiseks.</span><span class="sxs-lookup"><span data-stu-id="74011-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="74011-128">Laiendatud hankija kujunduse kasutamine Isiku tüübiga hankijate puhul</span><span class="sxs-lookup"><span data-stu-id="74011-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="74011-129">Lahendusepakett **Dynamics365FinanceExtended** sisaldab järgmisi töövoo protsessi malle.</span><span class="sxs-lookup"><span data-stu-id="74011-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="74011-130">Iga malli jaoks luuakse töövoog.</span><span class="sxs-lookup"><span data-stu-id="74011-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="74011-131">Isiku tüübiga hankijate loomine hankijate tabelis</span><span class="sxs-lookup"><span data-stu-id="74011-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="74011-132">Isiku tüübiga hankijate loomine kontaktide tabelis</span><span class="sxs-lookup"><span data-stu-id="74011-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="74011-133">Isiku tüübiga hankijate värskendamine kontaktide tabelis</span><span class="sxs-lookup"><span data-stu-id="74011-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="74011-134">Isiku tüübiga hankijate värskendamine hankijate tabelis</span><span class="sxs-lookup"><span data-stu-id="74011-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="74011-135">Uute töövooprotsesside loomiseks töövooprotsessi mallide abil toimige järgnevalt.</span><span class="sxs-lookup"><span data-stu-id="74011-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="74011-136">Looge töövooprotsess üksusele **Hankija** ja valige töövooprotsessi mall **Isiku tüübiga hankijate loomine kontaktide tabelis**.</span><span class="sxs-lookup"><span data-stu-id="74011-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="74011-137">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="74011-137">Then select **OK**.</span></span> <span data-ttu-id="74011-138">See töövoog käsitseb üksuse **Kontakt** hankija loomise stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="74011-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="74011-139">Looge töövooprotsess üksusele **Hankija** ja valige töövooprotsessi mall **Isiku tüübiga hankijate värskendamine kontaktide tabelis**.</span><span class="sxs-lookup"><span data-stu-id="74011-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="74011-140">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="74011-140">Then select **OK**.</span></span> <span data-ttu-id="74011-141">See töövoog käsitseb üksuse **Kontakt** hankija värskendamise stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="74011-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="74011-142">Looge töövooprotsess üksusele **Kontakt** ja valige mall **Isiku tüübiga hankijate loomine hankijate tabelis**.</span><span class="sxs-lookup"><span data-stu-id="74011-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="74011-143">Looge töövooprotsess üksusele **Kontakt** ja valige mall **Isiku tüübiga hankijate värskendamine hankijate tabelis**.</span><span class="sxs-lookup"><span data-stu-id="74011-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="74011-144">Saate konfigureerida töövoogusid kas reaalaja töövoogudena või taustatöövoogudena, olenevalt teie nõuetest.</span><span class="sxs-lookup"><span data-stu-id="74011-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="74011-145">Töövoo konfigureerimiseks taustatöövoona valige **Teisenda taustatöövooks**.</span><span class="sxs-lookup"><span data-stu-id="74011-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="74011-146">Aktiveerige töövood, mille lõite tabelitele **Kontakt** ja **Hankija**, et hakata kasutama üksust **Kontakt** tüübiga **Isik** hankijate teabe salvestamiseks.</span><span class="sxs-lookup"><span data-stu-id="74011-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
