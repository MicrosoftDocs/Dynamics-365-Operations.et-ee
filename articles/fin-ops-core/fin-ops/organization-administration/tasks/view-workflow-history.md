---
title: Töövooajaloo kuvamine
description: Selles teemas kirjeldatakse, kuidas vaadata töövoo süsteemi töötlemiseks ja kinnitamiseks edastatud dokumendi olekut.
author: jasongre
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 325478ed89b9c650899001dd08d1c98550fce520
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798976"
---
# <a name="view-workflow-history"></a><span data-ttu-id="9421e-103">Töövooajaloo kuvamine</span><span class="sxs-lookup"><span data-stu-id="9421e-103">View workflow history</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9421e-104">Selles teemas kirjeldatakse, kuidas vaadata töövoo süsteemi töötlemiseks ja kinnitamiseks edastatud dokumendi olekut.</span><span class="sxs-lookup"><span data-stu-id="9421e-104">This topic describes the steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="9421e-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="9421e-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="9421e-106">Avage **Navigeerimispaan > Moodulid > Üldine > Päringud > Töövoog > Töövoo ajalugu**.</span><span class="sxs-lookup"><span data-stu-id="9421e-106">Go to **Navigation pane > Modules > Common > Inquiries > Workflow > Workflow history**.</span></span>
    - <span data-ttu-id="9421e-107">Kasutage seda vormi, et kuvada töövoosüsteemile töötlemiseks ja kinnitamiseks edastatud dokumendi olek.</span><span class="sxs-lookup"><span data-stu-id="9421e-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    - <span data-ttu-id="9421e-108">**Eksemplari ID** on dokumenti töötleva või töötlemise lõpetanud töövoo eksemplari identifitseerimiskood.</span><span class="sxs-lookup"><span data-stu-id="9421e-108">The **Instance ID** is the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="9421e-109">**Olek** on dokumendi töövoo olek.</span><span class="sxs-lookup"><span data-stu-id="9421e-109">The **Status** is the workflow status of the document.</span></span>  
    - <span data-ttu-id="9421e-110">**Töövoo ID** on dokumenti töötleva või töötlemise lõpetanud töövoo identifitseerimiskood.</span><span class="sxs-lookup"><span data-stu-id="9421e-110">The **Workflow ID** is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="9421e-111">**Dokument** on dokumendi identifitseerimiskood.</span><span class="sxs-lookup"><span data-stu-id="9421e-111">The **Document** is the identification code of the document.</span></span>  
    - <span data-ttu-id="9421e-112">**Dokumendi tüüp** on töötlemisele esitatud dokumendi tüüp.</span><span class="sxs-lookup"><span data-stu-id="9421e-112">The **Document type** is the type of document that was submitted for processing.</span></span>  
    - <span data-ttu-id="9421e-113">**Töövoog** on dokumenti töötleva või töötlemise lõpetanud töövoo nimi.</span><span class="sxs-lookup"><span data-stu-id="9421e-113">The **Workflow** is the name of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="9421e-114">**Versioon** on dokumenti töötleva või töötlemise lõpetanud töövoo versiooninumber.</span><span class="sxs-lookup"><span data-stu-id="9421e-114">The **Version** is the version number of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="9421e-115">**Loomise kuupäev ja kellaaeg** on dokumendi esitamise kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="9421e-115">The **Created date and time** is the date and time that the document was submitted.</span></span>  
    - <span data-ttu-id="9421e-116">**Kulunud aeg** on dokumendi esitamisest kulunud aeg.</span><span class="sxs-lookup"><span data-stu-id="9421e-116">The **Elapsed time** is the time that has passed since the document was submitted.</span></span>  
    - <span data-ttu-id="9421e-117">Nupp **Jätka** võimaldab teil jätkata valitud dokumendi töövooprotsessi.</span><span class="sxs-lookup"><span data-stu-id="9421e-117">The **Resume** button allows you to resume the workflow process for the selected document.</span></span>  
    - <span data-ttu-id="9421e-118">Nupp **Tagasikutsumine** võimaldab teil kutsuda tagasi valitud dokumendi, nii et see ei oleks töödeldud.</span><span class="sxs-lookup"><span data-stu-id="9421e-118">The **Recall** button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="9421e-119">Valige loendis link soovitud reas.</span><span class="sxs-lookup"><span data-stu-id="9421e-119">In the list, select the link in the desired row.</span></span>
    - <span data-ttu-id="9421e-120">Veenduge, et jaotis **Tööüksused** oleks laiendatud.</span><span class="sxs-lookup"><span data-stu-id="9421e-120">Make sure the **Work items** section is expanded.</span></span> <span data-ttu-id="9421e-121">Selles jaotises saate vaadata valitud dokumendiga seotud üksuseid.</span><span class="sxs-lookup"><span data-stu-id="9421e-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="9421e-122">Näiteks ülesanne tuleb vajaduse korral lõpule viia või dokument kinnitada.</span><span class="sxs-lookup"><span data-stu-id="9421e-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    - <span data-ttu-id="9421e-123">Nupp **Määra uuesti** avab dialoogiboksi, kus saate tööüksuse määrata ümber teisele kasutajale.</span><span class="sxs-lookup"><span data-stu-id="9421e-123">The **Reassign** button will open a dialog box where you can reassign a work item to another user.</span></span>  
    - <span data-ttu-id="9421e-124">Veenduge, et jaotis **Jälgimise üksikasjad** oleks laiendatud.</span><span class="sxs-lookup"><span data-stu-id="9421e-124">Make sure the **Tracking details** section is expanded.</span></span> <span data-ttu-id="9421e-125">Selles jaotises saate vaadata valitud dokumendi töövoo ajalugu.</span><span class="sxs-lookup"><span data-stu-id="9421e-125">In this section you can view the workflow history of the selected document.</span></span>  

