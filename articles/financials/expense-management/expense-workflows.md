---
title: "Kulude töövoogude häälestamine"
description: "Saate seadistada töövooprotsessi, mida kasutatakse reisi- ja kuludokumentide kinnitamiseks."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: eb8ff11a03ba18b78595cd04f63b2456aec53bf2
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="32255-103">Kulude töövoogude häälestamine</span><span class="sxs-lookup"><span data-stu-id="32255-103">Set up workflows for expense</span></span>

[!include[banner](../includes/banner.md)]<span data-ttu-id="32255-104"> Saate seadistada töövooprotsessi, mida kasutatakse reisi- ja kuludokumentide kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="32255-104"> You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="32255-105">Dokumendid, millele saab määratleda töövoogusid, on kuluaruanded, reisiplaanid ja avansimaksete taotlused.</span><span class="sxs-lookup"><span data-stu-id="32255-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="32255-106">Töövoog esindab äriprotsessi.</span><span class="sxs-lookup"><span data-stu-id="32255-106">A workflow represents a business process.</span></span> <span data-ttu-id="32255-107">Töövoog määrab, kuidas dokument voogab läbi süsteemi, näidates, kes peab seda töötlema ja kinnitama.</span><span class="sxs-lookup"><span data-stu-id="32255-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="32255-108">Töövoo süsteemi kasutamine teie organisatsioonis on mitmeti kasulik.</span><span class="sxs-lookup"><span data-stu-id="32255-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="32255-109">**Järjepidevad protsessid** — töövoo süsteem lubab teil määratleda kinnitusprotsessi kindlatele dokumentidele nagu näiteks ostutaotlused ja kuluaruanded.</span><span class="sxs-lookup"><span data-stu-id="32255-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="32255-110">Töövoo süsteemi abil tagate, et dokumente töödeldakse ja kinnitatakse järjekindlal ja tõhusal viisil.</span><span class="sxs-lookup"><span data-stu-id="32255-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="32255-111">Protsessi nähtavus — töövoo süsteem lubab teil jälgida kindla töövoo eksemplari olekut ja ajalugu.</span><span class="sxs-lookup"><span data-stu-id="32255-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="32255-112">See aitab teil määratleda, kas töövoos tuleks muudatusi tõhususe parandamiseks.</span><span class="sxs-lookup"><span data-stu-id="32255-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="32255-113">Koondatud tööde loend — kasutajad saavad vaadata koondatud tööde loendit, et näha neile määratud töövoo ülesandeid ja kinnitusi.</span><span class="sxs-lookup"><span data-stu-id="32255-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="32255-114">**Loodavate töövoogude tüübid**</span><span class="sxs-lookup"><span data-stu-id="32255-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="32255-115">Järgmises tabelis on esitatud töövoo tüübid, mida saate luua jaotises **Kulu**.</span><span class="sxs-lookup"><span data-stu-id="32255-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>

| <span data-ttu-id="32255-116">**Tüüp**</span><span class="sxs-lookup"><span data-stu-id="32255-116">**Type**</span></span>                           | <span data-ttu-id="32255-117">**Kasutage seda tüüpi järgmiseks**</span><span class="sxs-lookup"><span data-stu-id="32255-117">**Use this type to**</span></span>                                                 |     
|------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="32255-118">**Kuluaruanne**</span><span class="sxs-lookup"><span data-stu-id="32255-118">**Expense report**</span></span>                 | <span data-ttu-id="32255-119">Kuluaruannetele kinnitamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="32255-119">Create approval workflows for expense reports.</span></span>                       |      
| <span data-ttu-id="32255-120">**Kuluaruande automaatne sisestamine**</span><span class="sxs-lookup"><span data-stu-id="32255-120">**Expense report auto posting**</span></span>    | <span data-ttu-id="32255-121">Kuluaruannetele automaatse sisestamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="32255-121">Create automatic posting workflows for expense reports.</span></span>              |     
| <span data-ttu-id="32255-122">**Kulurea kaup**</span><span class="sxs-lookup"><span data-stu-id="32255-122">**Expense line item**</span></span>              | <span data-ttu-id="32255-123">Kuluaruannete reaüksustele kinnitamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="32255-123">Create approval workflows for line items on expense reports.</span></span>         |     
| <span data-ttu-id="32255-124">**Kulurea kauba automaatne sisestamine**</span><span class="sxs-lookup"><span data-stu-id="32255-124">**Expense line item auto posting**</span></span> | <span data-ttu-id="32255-125">Kuluaruannete reaüksustele automaatse sisestamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="32255-125">Create automatic posting workflows for line items on expense reports.</span></span>|
| <span data-ttu-id="32255-126">**Reisitellimus**</span><span class="sxs-lookup"><span data-stu-id="32255-126">**Travel requisition**</span></span>             | <span data-ttu-id="32255-127">Reisiplaanidele kinnitamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="32255-127">Create approval workflows for travel requisitions.</span></span>                   |    
| <span data-ttu-id="32255-128">**Avansimakse taotlus**</span><span class="sxs-lookup"><span data-stu-id="32255-128">**Cash advance request**</span></span>           | <span data-ttu-id="32255-129">Sularaha ettemakse taotluste kinnitustöövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="32255-129">Create approval workflows for cash advance requests.</span></span>                 |     
| <span data-ttu-id="32255-130">**Käibemaksu korvamine**</span><span class="sxs-lookup"><span data-stu-id="32255-130">**VAT tax recovery**</span></span>               | <span data-ttu-id="32255-131">Käibemaksu (KM) korvamise kinnitustöövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="32255-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span> |       

