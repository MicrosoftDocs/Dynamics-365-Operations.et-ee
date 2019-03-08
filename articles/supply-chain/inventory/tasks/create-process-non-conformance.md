---
title: Vastavuse loomine ja töötlemine
description: Kasutage seda protseduuri mittevastavuse haldamiseks olemasoleva kvaliteettellimuse põhjal.
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16ed11bce92920fe8240fc85f706a2ac6ab0a04b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "336286"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="ce3d8-103">Vastavuse loomine ja töötlemine</span><span class="sxs-lookup"><span data-stu-id="ce3d8-103">Create and process a conformance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ce3d8-104">Kasutage seda protseduuri mittevastavuse haldamiseks olemasoleva kvaliteettellimuse põhjal.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-104">Use this procedure to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="ce3d8-105">Saate käivitada selle salvestise demoettevõttes USMF ja kasutada soovitatud väärtusi.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="ce3d8-106">Tavaliselt teostab selle protseduuri kvaliteediametnik.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="ce3d8-107">Eeltingimusena käivitage ülesandesalvestis „Kaupade kvaliteedi kontrollimine”.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-107">As a prerequisite, run the “Inspect the quality of goods” task recording.</span></span> <span data-ttu-id="ce3d8-108">Mittevastavuse kinnitamise töötlemiseks peab ülesandesalvestist käitavale kasutajale olema lehel Kasutajad määratud väärtus Nimi.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-108">To process the approval of a nonconformance, the user who runs the task recording must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="ce3d8-109">Dokumendi märkuste kasutamiseks peab kasutajal olema kasutajasuvandites aktiveeritud ka suvand Dokumenditöötlus.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="ce3d8-110">Kvaliteettellimuse valimine</span><span class="sxs-lookup"><span data-stu-id="ce3d8-110">Select a quality order</span></span>
1. <span data-ttu-id="ce3d8-111">Minge jaotisse Kvaliteettellimused.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-111">Go to Quality orders.</span></span>
2. <span data-ttu-id="ce3d8-112">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ce3d8-113">Valige kvaliteettellimus, mis loodi ülesandesalvestises „Kaupade kvaliteedi kontrollimine”.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-113">Select the quality order that was created from the "Inspect the quality of goods" task recording.</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="ce3d8-114">Mittevastavuse loomine</span><span class="sxs-lookup"><span data-stu-id="ce3d8-114">Create a nonconformance</span></span>
1. <span data-ttu-id="ce3d8-115">Klõpsake suvandit Päringud.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-115">Click Inquiries.</span></span>
2. <span data-ttu-id="ce3d8-116">Klõpsake suvandit Mittevastavused.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-116">Click Non conformances.</span></span>
3. <span data-ttu-id="ce3d8-117">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-117">Click New.</span></span>
4. <span data-ttu-id="ce3d8-118">Klõpsake väljal Probleemi tüüp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-118">In the Problem type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ce3d8-119">Valige kontrolliprotsessi käigus leitud probleem.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-119">Select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="ce3d8-120">Klõpsake väljal Probleemi tüüp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-120">In the Problem type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ce3d8-121">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ce3d8-122">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ce3d8-123">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-123">Click OK.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="ce3d8-124">Mittevastavuse kinnitamine/tagasilükkamine</span><span class="sxs-lookup"><span data-stu-id="ce3d8-124">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="ce3d8-125">Klõpsake suvandit Funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-125">Click Functions.</span></span>
2. <span data-ttu-id="ce3d8-126">Klõpsake suvandit Kinnita mittevastavus.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-126">Click Approve non conformance.</span></span>
    * <span data-ttu-id="ce3d8-127">Selles näites kinnitage mittevastavus.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-127">For this example, approve the nonconformance.</span></span> <span data-ttu-id="ce3d8-128">Kinnitatud mittevastavused saab seostada töö salvestamisega seotud toimingutega, mida tehakse osana mittevastavuse töötlemisest, ja (nagu selles ülesandesalvestises) paranduse käsitlemise töötlemisega.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-128">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this task recording, the processing of correction handling.</span></span>  
3. <span data-ttu-id="ce3d8-129">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-129">Click Yes.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="ce3d8-130">Parandustegevuse loomine</span><span class="sxs-lookup"><span data-stu-id="ce3d8-130">Create a correction action</span></span>
1. <span data-ttu-id="ce3d8-131">Klõpsake suvandit Parandused.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-131">Click Corrections.</span></span>
2. <span data-ttu-id="ce3d8-132">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-132">Click New.</span></span>
3. <span data-ttu-id="ce3d8-133">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="ce3d8-134">Klõpsake väljal Personalinumber otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-134">In the Personnel number field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ce3d8-135">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-135">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ce3d8-136">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-136">Click Select.</span></span>
7. <span data-ttu-id="ce3d8-137">Klõpsake suvandit Manusta.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-137">Click Attach.</span></span>
    * <span data-ttu-id="ce3d8-138">Looge paranduse kohta märkus.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-138">Create a note about the correction.</span></span> <span data-ttu-id="ce3d8-139">Selles näites on tegevuseks hankijaga ühenduse võtmine, et arutleda mittevastavuse juhtumit.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-139">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
8. <span data-ttu-id="ce3d8-140">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-140">Click New.</span></span>
9. <span data-ttu-id="ce3d8-141">Klõpsake suvandit Märkus.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-141">Click Note.</span></span>
    * <span data-ttu-id="ce3d8-142">Pange tähele, et olenevalt aruande seadistusest saab mittevastavuse haldusega seotud aruannetele printida erinevat tüüpi dokumente.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-142">Note that, depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
10. <span data-ttu-id="ce3d8-143">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-143">In the Description field, type a value.</span></span>
11. <span data-ttu-id="ce3d8-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-144">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="ce3d8-145">Paranduse haldamine</span><span class="sxs-lookup"><span data-stu-id="ce3d8-145">Maintain a correction</span></span>
1. <span data-ttu-id="ce3d8-146">Klõpsake suvandit Märgi lõpuleviiduks.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-146">Click Mark complete.</span></span>
2. <span data-ttu-id="ce3d8-147">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-147">Click OK.</span></span>
3. <span data-ttu-id="ce3d8-148">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-148">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="ce3d8-149">Mittevastavuse sulgemine</span><span class="sxs-lookup"><span data-stu-id="ce3d8-149">Close a nonconformance</span></span>
1. <span data-ttu-id="ce3d8-150">Klõpsake suvandit Funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-150">Click Functions.</span></span>
2. <span data-ttu-id="ce3d8-151">Klõpsake suvandit Sule mittevastavus.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-151">Click Close non conformance.</span></span>
3. <span data-ttu-id="ce3d8-152">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-152">Click Yes.</span></span>
4. <span data-ttu-id="ce3d8-153">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-153">Close the page.</span></span>
5. <span data-ttu-id="ce3d8-154">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ce3d8-154">Close the page.</span></span>
