---
title: Vastavuse loomine ja töötlemine
description: Selles teemas tutvustatakse, kuidas teha mittevastavuse haldust olemasoleva kvaliteettellimuse põhjal.
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4525e79cb388cc9bbcfe1d038a53cf53916a678c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008063"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="63411-103">Vastavuse loomine ja töötlemine</span><span class="sxs-lookup"><span data-stu-id="63411-103">Create and process a conformance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="63411-104">Selles teemas tutvustatakse, kuidas teha mittevastavuse haldust olemasoleva kvaliteettellimuse põhjal.</span><span class="sxs-lookup"><span data-stu-id="63411-104">This topic explains how to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="63411-105">Saate käivitada selle salvestise demoettevõttes USMF ja kasutada soovitatud väärtusi.</span><span class="sxs-lookup"><span data-stu-id="63411-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="63411-106">Tavaliselt teostab selle protseduuri kvaliteediametnik.</span><span class="sxs-lookup"><span data-stu-id="63411-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="63411-107">Eeltingimusena täitke juhised jaotises [Kontrollige kaupade kvaliteeti](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="63411-107">As a prerequisite, complete the instructions in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span> <span data-ttu-id="63411-108">Mittevastavuse kinnitamise töötlemiseks peab ülesandesalvestist käitavale kasutajale olema lehel Kasutajad määratud väärtus „Nimi”.</span><span class="sxs-lookup"><span data-stu-id="63411-108">To process the approval of a nonconformance, the user who runs the task recording must have a "Name" value assigned on the Users page.</span></span> <span data-ttu-id="63411-109">Dokumendi märkuste kasutamiseks peab kasutajal olema kasutajasuvandites aktiveeritud ka suvand Dokumenditöötlus.</span><span class="sxs-lookup"><span data-stu-id="63411-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="63411-110">Kvaliteettellimuse valimine</span><span class="sxs-lookup"><span data-stu-id="63411-110">Select a quality order</span></span>
1. <span data-ttu-id="63411-111">Navigeerimispaanil avage **Moodulid > Varud > Perioodilised ülesanded > Kvaliteethaldus > Kvaliteettellimus**.</span><span class="sxs-lookup"><span data-stu-id="63411-111">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="63411-112">Valige loendist kvaliteettellimus, mis loodi jaotises [Kontrolli kaupade kvaliteeti](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="63411-112">In the list, select the quality order that was created in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="63411-113">Mittevastavuse loomine</span><span class="sxs-lookup"><span data-stu-id="63411-113">Create a nonconformance</span></span>
1. <span data-ttu-id="63411-114">Toimingupaanil valige **Päringud**.</span><span class="sxs-lookup"><span data-stu-id="63411-114">On the Action Pane, select **Inquiries**.</span></span>
2. <span data-ttu-id="63411-115">Valige **Mittevastavused**.</span><span class="sxs-lookup"><span data-stu-id="63411-115">Select **Non conformances**.</span></span>
3. <span data-ttu-id="63411-116">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="63411-116">Select **New**.</span></span>
4. <span data-ttu-id="63411-117">Rippmenüü väljal **Probleemi tüüp** valige probleem, mis leiti kontrollimise protsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="63411-117">In the drop-down menu of the **Problem type** field, select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="63411-118">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="63411-118">Select **OK**.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="63411-119">Mittevastavuse kinnitamine/tagasilükkamine</span><span class="sxs-lookup"><span data-stu-id="63411-119">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="63411-120">Valige **Funktsioonid**.</span><span class="sxs-lookup"><span data-stu-id="63411-120">Select **Functions**.</span></span>
2. <span data-ttu-id="63411-121">Valige **Kinnita mittevastavus**.</span><span class="sxs-lookup"><span data-stu-id="63411-121">Select **Approve non conformance**.</span></span> <span data-ttu-id="63411-122">Selles näites kinnitage mittevastavus.</span><span class="sxs-lookup"><span data-stu-id="63411-122">For this example, approve the nonconformance.</span></span> <span data-ttu-id="63411-123">Kinnitatud mittevastavusi saab seostada seotud toimingutega, et salvestada töö, mis on tehtud osana mittevastavusi käsitlemisest ja nagu selles teemas, paranduste käsitlemise töötlemisel.</span><span class="sxs-lookup"><span data-stu-id="63411-123">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this topic, the processing of correction handling.</span></span>  
3. <span data-ttu-id="63411-124">Valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="63411-124">Select **Yes**.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="63411-125">Parandustegevuse loomine</span><span class="sxs-lookup"><span data-stu-id="63411-125">Create a correction action</span></span>
1. <span data-ttu-id="63411-126">Valige **Parandused**.</span><span class="sxs-lookup"><span data-stu-id="63411-126">Select **Corrections**.</span></span>
2. <span data-ttu-id="63411-127">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="63411-127">Select **New**.</span></span>
3. <span data-ttu-id="63411-128">Uue rea väljal **Personalinumber** valige rippmenüüst soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="63411-128">In the **Personnel number** field of the new row, select the desired record from the drop down menu.</span></span>
4. <span data-ttu-id="63411-129">Klõpsake **Vali**.</span><span class="sxs-lookup"><span data-stu-id="63411-129">Click **Select**.</span></span>
5. <span data-ttu-id="63411-130">Valige **Manusta**.</span><span class="sxs-lookup"><span data-stu-id="63411-130">Select **Attach**.</span></span> <span data-ttu-id="63411-131">Looge paranduse kohta märkus.</span><span class="sxs-lookup"><span data-stu-id="63411-131">Create a note about the correction.</span></span> <span data-ttu-id="63411-132">Selles näites on tegevuseks hankijaga ühenduse võtmine, et arutleda mittevastavuse juhtumit.</span><span class="sxs-lookup"><span data-stu-id="63411-132">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
6. <span data-ttu-id="63411-133">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="63411-133">Select **New**.</span></span>
7. <span data-ttu-id="63411-134">Valige **Märge**.</span><span class="sxs-lookup"><span data-stu-id="63411-134">Select **Note**.</span></span> <span data-ttu-id="63411-135">Sõltuvalt aruande seadistusest saab eri dokumendi tüüpe printida aruannetele, mis on seotud mittevastavuse haldusega.</span><span class="sxs-lookup"><span data-stu-id="63411-135">Depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
8. <span data-ttu-id="63411-136">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="63411-136">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="63411-137">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="63411-137">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="63411-138">Paranduse haldamine</span><span class="sxs-lookup"><span data-stu-id="63411-138">Maintain a correction</span></span>
1. <span data-ttu-id="63411-139">Valige **Märgi lõpuleviiduks**.</span><span class="sxs-lookup"><span data-stu-id="63411-139">Select **Mark complete**.</span></span>
2. <span data-ttu-id="63411-140">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="63411-140">Select **OK**.</span></span>
3. <span data-ttu-id="63411-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="63411-141">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="63411-142">Mittevastavuse sulgemine</span><span class="sxs-lookup"><span data-stu-id="63411-142">Close a nonconformance</span></span>
1. <span data-ttu-id="63411-143">Valige **Funktsioonid**.</span><span class="sxs-lookup"><span data-stu-id="63411-143">Select **Functions**.</span></span>
2. <span data-ttu-id="63411-144">Valige **Sulge mittevastavus**.</span><span class="sxs-lookup"><span data-stu-id="63411-144">Select **Close non conformance**.</span></span>
3. <span data-ttu-id="63411-145">Valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="63411-145">Select **Yes**.</span></span>
4. <span data-ttu-id="63411-146">Sulgege lehed.</span><span class="sxs-lookup"><span data-stu-id="63411-146">Close the pages.</span></span>
