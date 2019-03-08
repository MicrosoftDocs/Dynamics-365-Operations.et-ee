---
title: Kulude töövoogude häälestamine
description: Saate seadistada töövooprotsessi, mida kasutatakse reisi- ja kuludokumentide kinnitamiseks.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8294aaa344e3cb6b79fa4f33f368258ca19c8205
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "355721"
---
# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="ecde2-103">Kulude töövoogude häälestamine</span><span class="sxs-lookup"><span data-stu-id="ecde2-103">Set up workflows for expense</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ecde2-104"> Saate seadistada töövooprotsessi, mida kasutatakse reisi- ja kuludokumentide kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="ecde2-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="ecde2-105">Dokumendid, millele saab määratleda töövoogusid, on kuluaruanded, reisiplaanid ja avansimaksete taotlused.</span><span class="sxs-lookup"><span data-stu-id="ecde2-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="ecde2-106">Töövoog esindab äriprotsessi.</span><span class="sxs-lookup"><span data-stu-id="ecde2-106">A workflow represents a business process.</span></span> <span data-ttu-id="ecde2-107">Töövoog määrab, kuidas dokument voogab läbi süsteemi, näidates, kes peab seda töötlema ja kinnitama.</span><span class="sxs-lookup"><span data-stu-id="ecde2-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="ecde2-108">Töövoo süsteemi kasutamine teie organisatsioonis on mitmeti kasulik.</span><span class="sxs-lookup"><span data-stu-id="ecde2-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="ecde2-109">**Järjepidevad protsessid** — töövoo süsteem lubab teil määratleda kinnitusprotsessi kindlatele dokumentidele nagu näiteks ostutaotlused ja kuluaruanded.</span><span class="sxs-lookup"><span data-stu-id="ecde2-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="ecde2-110">Töövoo süsteemi abil tagate, et dokumente töödeldakse ja kinnitatakse järjekindlal ja tõhusal viisil.</span><span class="sxs-lookup"><span data-stu-id="ecde2-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="ecde2-111">Protsessi nähtavus — töövoo süsteem lubab teil jälgida kindla töövoo eksemplari olekut ja ajalugu.</span><span class="sxs-lookup"><span data-stu-id="ecde2-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="ecde2-112">See aitab teil määratleda, kas töövoos tuleks muudatusi tõhususe parandamiseks.</span><span class="sxs-lookup"><span data-stu-id="ecde2-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="ecde2-113">Koondatud tööde loend — kasutajad saavad vaadata koondatud tööde loendit, et näha neile määratud töövoo ülesandeid ja kinnitusi.</span><span class="sxs-lookup"><span data-stu-id="ecde2-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="ecde2-114">**Loodavate töövoogude tüübid**</span><span class="sxs-lookup"><span data-stu-id="ecde2-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="ecde2-115">Järgmises tabelis on esitatud töövoo tüübid, mida saate luua jaotises **Kulu**.</span><span class="sxs-lookup"><span data-stu-id="ecde2-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="ecde2-116"><strong>Tüüp</strong></span><span class="sxs-lookup"><span data-stu-id="ecde2-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="ecde2-117"><strong>Kasutage seda tüüpi järgmiseks</strong></span><span class="sxs-lookup"><span data-stu-id="ecde2-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="ecde2-118"><strong>Kuluaruanne</strong></span><span class="sxs-lookup"><span data-stu-id="ecde2-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="ecde2-119">Kuluaruannetele kinnitamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="ecde2-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="ecde2-120"><strong>Kuluaruande automaatne sisestamine</strong></span><span class="sxs-lookup"><span data-stu-id="ecde2-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="ecde2-121">Kuluaruannetele automaatse sisestamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="ecde2-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="ecde2-122"><strong>Kulurea kaup</strong></span><span class="sxs-lookup"><span data-stu-id="ecde2-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="ecde2-123">Kuluaruannete reaüksustele kinnitamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="ecde2-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="ecde2-124"><strong>Kulurea kauba automaatne sisestamine</strong></span><span class="sxs-lookup"><span data-stu-id="ecde2-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="ecde2-125">Kuluaruannete reaüksustele automaatse sisestamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="ecde2-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="ecde2-126"><strong>Reisitellimus</strong></span><span class="sxs-lookup"><span data-stu-id="ecde2-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="ecde2-127">Reisiplaanidele kinnitamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="ecde2-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="ecde2-128"><strong>Avansimakse taotlus</strong></span><span class="sxs-lookup"><span data-stu-id="ecde2-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="ecde2-129">Sularaha ettemakse taotluste kinnitustöövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="ecde2-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="ecde2-130"><strong>Käibemaksu korvamine</strong></span><span class="sxs-lookup"><span data-stu-id="ecde2-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="ecde2-131">Käibemaksu (KM) korvamise kinnitustöövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="ecde2-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

