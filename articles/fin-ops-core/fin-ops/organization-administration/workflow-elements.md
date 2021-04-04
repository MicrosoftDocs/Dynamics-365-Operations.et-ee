---
title: Töövoo elemendid
description: Selles teemas kirjeldatakse mitmesuguseid elemente, millest töövoog koosneb.
author: ChrisGarty
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc8606dbf475c7429d9ded1063e94646c6084ef0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559354"
---
# <a name="workflow-elements"></a><span data-ttu-id="73cab-103">Töövoo elemendid</span><span class="sxs-lookup"><span data-stu-id="73cab-103">Workflow elements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73cab-104">Selles teemas kirjeldatakse mitmesuguseid elemente, millest töövoog koosneb.</span><span class="sxs-lookup"><span data-stu-id="73cab-104">This topic describes the various elements that make up a workflow.</span></span>

<span data-ttu-id="73cab-105">Töövoog koosneb elementidest.</span><span class="sxs-lookup"><span data-stu-id="73cab-105">A workflow consists of elements.</span></span> <span data-ttu-id="73cab-106">Järgmised jaotised kirjeldavad iga elemenditüüpi.</span><span class="sxs-lookup"><span data-stu-id="73cab-106">The sections that follow describe each type of element.</span></span>

## <a name="tasks"></a><span data-ttu-id="73cab-107">Ülesanded</span><span class="sxs-lookup"><span data-stu-id="73cab-107">Tasks</span></span>

<span data-ttu-id="73cab-108">*Ülesanne* on tööühik, mille peab tegema.</span><span class="sxs-lookup"><span data-stu-id="73cab-108">A *task* is a unit of work that must be performed.</span></span> <span data-ttu-id="73cab-109">Töövoogu saab lisada kaht tüüpi ülesandeid: käsitsi ja automatiseeritud.</span><span class="sxs-lookup"><span data-stu-id="73cab-109">Two types of tasks can be added to a workflow: manual tasks and automated tasks.</span></span>

### <a name="manual-task"></a><span data-ttu-id="73cab-110">Käsitsi tehtav ülesanne</span><span class="sxs-lookup"><span data-stu-id="73cab-110">Manual task</span></span>

<span data-ttu-id="73cab-111">*Käsitsi ülesanne* on tööühik, mille peab tegema kasutaja.</span><span class="sxs-lookup"><span data-stu-id="73cab-111">A *manual task* is a unit of work that must be performed by a user.</span></span> <span data-ttu-id="73cab-112">Näiteks võivad kuluaruande töövool olla käsitsi ülesanded, mis nõuavad määratud kasutajatelt järgmiste tegevuste lõpuleviimist.</span><span class="sxs-lookup"><span data-stu-id="73cab-112">For example, an expense report workflow can have manual tasks that require the assigned users to complete the following actions:</span></span>

- <span data-ttu-id="73cab-113">Koos kuluaruandega esitatud kviitungite läbivaatus.</span><span class="sxs-lookup"><span data-stu-id="73cab-113">Review the receipts that are submitted together with an expense report.</span></span>
- <span data-ttu-id="73cab-114">Töötaja ülemuse kutsumine.</span><span class="sxs-lookup"><span data-stu-id="73cab-114">Call an employee's manager.</span></span>

### <a name="automated-task"></a><span data-ttu-id="73cab-115">Automatiseeritud ülesanne</span><span class="sxs-lookup"><span data-stu-id="73cab-115">Automated task</span></span>

<span data-ttu-id="73cab-116">*Automatiseeritud ülesanne* on tööühik, mille peab tegema süsteem.</span><span class="sxs-lookup"><span data-stu-id="73cab-116">An *automated task* is a unit of work that must be performed by the system.</span></span> <span data-ttu-id="73cab-117">Inimeste tehtavad toimingud pole vajalikud.</span><span class="sxs-lookup"><span data-stu-id="73cab-117">No human interaction is required.</span></span> <span data-ttu-id="73cab-118">Näiteks võivad müügitellimuse töövool olla automatiseeritud ülesanded, mis nõuavad süsteemilt järgmiste tegevuste lõpuleviimist.</span><span class="sxs-lookup"><span data-stu-id="73cab-118">For example, a sales order workflow can have automated tasks that require the system to complete the following actions:</span></span>

- <span data-ttu-id="73cab-119">Krediidikontrolli teostamine.</span><span class="sxs-lookup"><span data-stu-id="73cab-119">Perform a credit check.</span></span>
- <span data-ttu-id="73cab-120">Kliendi jaoks kliendikirje loomine, kui seda veel pole.</span><span class="sxs-lookup"><span data-stu-id="73cab-120">Create a customer record for the customer, if a record doesn't already exist.</span></span>

## <a name="approval-processes"></a><span data-ttu-id="73cab-121">Kinnitusprotsessid</span><span class="sxs-lookup"><span data-stu-id="73cab-121">Approval processes</span></span>

<span data-ttu-id="73cab-122">*Kinnitusprotsess* on eraldi etappidest koosnev protsess.</span><span class="sxs-lookup"><span data-stu-id="73cab-122">An *approval process* is a process that consists of separate steps.</span></span> <span data-ttu-id="73cab-123">Kasutaja saab igas kinnitusetapis teostada järgmisi toiminguid.</span><span class="sxs-lookup"><span data-stu-id="73cab-123">At each approval step, the user can perform the following actions:</span></span>

- <span data-ttu-id="73cab-124">Kinnitage dokument.</span><span class="sxs-lookup"><span data-stu-id="73cab-124">Approve the document.</span></span>
- <span data-ttu-id="73cab-125">Lükake dokument tagasi.</span><span class="sxs-lookup"><span data-stu-id="73cab-125">Reject the document.</span></span>
- <span data-ttu-id="73cab-126">Taotlege dokumendi muutmist.</span><span class="sxs-lookup"><span data-stu-id="73cab-126">Request a change to the document.</span></span>
- <span data-ttu-id="73cab-127">Määrake dokument teisele kasutajale kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="73cab-127">Assign the document to another user for approval.</span></span>

## <a name="line-item-workflow-elements"></a><span data-ttu-id="73cab-128">Rea kauba töövoo elemendid</span><span class="sxs-lookup"><span data-stu-id="73cab-128">Line-item workflow elements</span></span>

<span data-ttu-id="73cab-129">Töövoo saab luua kas dokumentide või dokumendi reakaupade töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="73cab-129">A workflow can be created to process either documents or the line items on a document.</span></span> <span data-ttu-id="73cab-130">Näiteks olete loonud kinnitustöövoo ajatabelite jaoks.</span><span class="sxs-lookup"><span data-stu-id="73cab-130">For example, you've created an approval workflow for timesheets.</span></span> <span data-ttu-id="73cab-131">(Viitame sellele töövoole kui *dokumenditöövoole*.) Saate sellele dokumendi töövoo elemendile lisada *rea kauba töövoo*.</span><span class="sxs-lookup"><span data-stu-id="73cab-131">(We will refer to this workflow as the *document workflow*.) You can add a *line-item workflow* element to that document workflow.</span></span> <span data-ttu-id="73cab-132">Rea kauba elemendi käitamisel esitatakse dokumendi iga reakaup töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="73cab-132">When the line-item element is run, each line item on the document is submitted for processing.</span></span> <span data-ttu-id="73cab-133">Võite lasta kõiki rea kaupu töödelda sama rea kauba töövooga või lasta iga reakaupa töödelda eraldi rea kauba töövooga.</span><span class="sxs-lookup"><span data-stu-id="73cab-133">You might want all the line items to be processed by the same line-item workflow, or you might want each line item to be processed by a different line-item workflow.</span></span> <span data-ttu-id="73cab-134">Oletagem, et töötaja on esitanud ajatabeli, mis sarnaneb järgmisel joonisel toodule.</span><span class="sxs-lookup"><span data-stu-id="73cab-134">Imagine that an employee has submitted a timesheet that resembles the following figure.</span></span>

![Töövoog rea kaupadega](./media/workflow_lineitemworkflow.gif)

<span data-ttu-id="73cab-136">Selles stsenaariumis võib olla vaja luua järgmised reaüksuse töövood.</span><span class="sxs-lookup"><span data-stu-id="73cab-136">In this scenario, you might want to create the following line-item workflows:</span></span>

- <span data-ttu-id="73cab-137">**Rea kauba töövoog 1** – seda töövoogu kasutatakse rea kaupade töötlemiseks, kui projekti ID on 1111.</span><span class="sxs-lookup"><span data-stu-id="73cab-137">**Line-item workflow 1** – This workflow is used to process line items where the project ID is 1111.</span></span>
- <span data-ttu-id="73cab-138">**Rea kauba töövoog 2** – seda töövoogu kasutatakse rea kaupade töötlemiseks, kui projekti ID on 2222.</span><span class="sxs-lookup"><span data-stu-id="73cab-138">**Line-item workflow 2** – This workflow is used to process line items where the project ID is 2222.</span></span>
- <span data-ttu-id="73cab-139">**Rea kauba töövoog 3** – seda töövoogu kasutatakse rea kaupade töötlemiseks, kui projekti ID on 3333.</span><span class="sxs-lookup"><span data-stu-id="73cab-139">**Line-item workflow 3** – This workflow is used to process line items where the project ID is 3333.</span></span>

## <a name="flow-control-elements"></a><span data-ttu-id="73cab-140">Voo juhtelemendid</span><span class="sxs-lookup"><span data-stu-id="73cab-140">Flow-control elements</span></span>

<span data-ttu-id="73cab-141">Järgmised elemendid võimaldavad teil kujundada töövood, mis on alternatiivsed harud või samal ajal töötavad harud.</span><span class="sxs-lookup"><span data-stu-id="73cab-141">The following elements let you design workflows that have alternate branches or branches that run at the same time.</span></span>

### <a name="manual-decision"></a><span data-ttu-id="73cab-142">Käsitsi otsus</span><span class="sxs-lookup"><span data-stu-id="73cab-142">Manual decision</span></span>

<span data-ttu-id="73cab-143">*Käsitsi otsus* on punkt, milles töövoog jaguneb kaheks haruks.</span><span class="sxs-lookup"><span data-stu-id="73cab-143">A *manual decision* is a point where a workflow divides into two branches.</span></span> <span data-ttu-id="73cab-144">Kasutaja peab tegema otsuse, mis määrab, millist haru kasutatakse esitatud dokumendi töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="73cab-144">A user must make a decision, and this decision determines which branch is used to process the document that was submitted.</span></span>

### <a name="conditional-decision"></a><span data-ttu-id="73cab-145">Tingimuslik otsus</span><span class="sxs-lookup"><span data-stu-id="73cab-145">Conditional decision</span></span>

<span data-ttu-id="73cab-146">*Tingimuslik otsus* on samuti punkt, milles töövoog jaguneb kaheks haruks.</span><span class="sxs-lookup"><span data-stu-id="73cab-146">A *conditional decision* is also a point where a workflow divides into two branches.</span></span> <span data-ttu-id="73cab-147">Siiski otsustab süsteem, millist haru kasutatakse esitatud dokumendi töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="73cab-147">However, the system decides which branch is used to process the document that was submitted.</span></span> <span data-ttu-id="73cab-148">Selle otsuse tegemiseks hindab süsteem dokumenti, et teha kindlaks, kas see vastab määratud tingimustele.</span><span class="sxs-lookup"><span data-stu-id="73cab-148">To make this decision, the system evaluates the document to determine whether it meets specified conditions.</span></span>

### <a name="parallel-activity"></a><span data-ttu-id="73cab-149">Paralleeltegevus</span><span class="sxs-lookup"><span data-stu-id="73cab-149">Parallel activity</span></span>

<span data-ttu-id="73cab-150">*Paralleeltegevus* on töövoo element, mis sisaldab kaht või enamat töövoo haru, mis töötavad samal ajal.</span><span class="sxs-lookup"><span data-stu-id="73cab-150">A *parallel activity* is a workflow element that includes two or more workflow branches that run at the same time.</span></span>

### <a name="subworkflow"></a><span data-ttu-id="73cab-151">Alamtöövoog</span><span class="sxs-lookup"><span data-stu-id="73cab-151">Subworkflow</span></span>

<span data-ttu-id="73cab-152">*Alamtöövoog* on teise töövoo kontekstis käitatav töövoog.</span><span class="sxs-lookup"><span data-stu-id="73cab-152">A *subworkflow* is a workflow that runs in the context of another workflow.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]