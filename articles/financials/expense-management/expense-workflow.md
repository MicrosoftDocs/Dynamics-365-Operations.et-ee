---
title: "Kulutöövoog"
description: "Selles teemas selgitatakse, kuidas saab kasutada rakenduse Microsoft Dynamics 365 for Finance and Operations töövoosüsteemi kuluaruannete ülevaatamisprotsessi seadistamiseks kuluhalduses."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 6ee607f723659a5b6ecd655ba4fdfca35a4c582d
ms.contentlocale: et-ee
ms.lasthandoff: 03/26/2018

---

# <a name="expense-workflow"></a><span data-ttu-id="9979c-103">Kulutöövoog</span><span class="sxs-lookup"><span data-stu-id="9979c-103">Expense workflow</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9979c-104">Saate kasutada rakenduse Microsoft Dynamics 365 for Finance and Operations töövoosüsteemi kuluaruannete ülevaatamisprotsessi seadistamiseks kuluhalduses.</span><span class="sxs-lookup"><span data-stu-id="9979c-104">You can use the workflow system in Microsoft Dynamics 365 for Finance and Operations, to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="9979c-105">Saate seadistada töövoo, mis kasutab järgmisi kriteeriume määramiseks, kes kuluaruandeid kinnitab.</span><span class="sxs-lookup"><span data-stu-id="9979c-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="9979c-106">Töötaja aruandlushierarhia ja eelmääratud kinnituslimiidid</span><span class="sxs-lookup"><span data-stu-id="9979c-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="9979c-107">Mitmetasandiline kinnitamine, mis toetab vahepealseid kinnitajaid ja lõplikku kinnitajat</span><span class="sxs-lookup"><span data-stu-id="9979c-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="9979c-108">Finantsdimensioonid ja vastutus projekti eest</span><span class="sxs-lookup"><span data-stu-id="9979c-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="9979c-109">Määramine konkreetsetele kasutajatele või kasutajagruppidele</span><span class="sxs-lookup"><span data-stu-id="9979c-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="9979c-110">Töövoo kinnitusi saab luua kuluaruannetele, reisiplaanidele, avansimaksetele ja käibemaksu (KM) korvamisele.</span><span class="sxs-lookup"><span data-stu-id="9979c-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="9979c-111">**Näide**</span><span class="sxs-lookup"><span data-stu-id="9979c-111">**Example**</span></span>

<span data-ttu-id="9979c-112">Järgmine protsess on kuluaruande kuluhalduse töövoo näide.</span><span class="sxs-lookup"><span data-stu-id="9979c-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="9979c-113">Töötaja koostab ja salvestab kuluaruande.</span><span class="sxs-lookup"><span data-stu-id="9979c-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="9979c-114">Töötaja esitab kuluaruande kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="9979c-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="9979c-115">Kinnitaja tuvastatakse töövoo seadistamise ajal määratud reeglite põhjal.</span><span class="sxs-lookup"><span data-stu-id="9979c-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="9979c-116">Kinnitaja saab teate, et kuluaruanne on kinnitamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="9979c-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="9979c-117">Kinnitaja vaatab kuluaruande üle ja veendub, et järgmised tingimused on täidetud.</span><span class="sxs-lookup"><span data-stu-id="9979c-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="9979c-118">Kulud ei riku ühtegi kulupoliitikat.</span><span class="sxs-lookup"><span data-stu-id="9979c-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="9979c-119">Kui kulu rikub mõnda poliitikat, siis kontrollib kinnitaja, et kuluaruanne sisaldaks sobivat ärilist põhjendust.</span><span class="sxs-lookup"><span data-stu-id="9979c-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="9979c-120">Elektroonilised kviitungid on kuluaruandega seotud.</span><span class="sxs-lookup"><span data-stu-id="9979c-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="9979c-121">Kinnitaja kinnitab kuluaruande.</span><span class="sxs-lookup"><span data-stu-id="9979c-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="9979c-122">Kuluaruanne määratakse sisestamiseks ostureskontro koordinaatorile.</span><span class="sxs-lookup"><span data-stu-id="9979c-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="9979c-123">Tehakse üks järgmistest toimingutest, olenevalt sellest, kas automaatne sisestamine on konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="9979c-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="9979c-124">Kui automaatne sisestamine on konfigureeritud, töödeldakse kuluaruannet maksmiseks ja kuluaruande olekut muudetakse.</span><span class="sxs-lookup"><span data-stu-id="9979c-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="9979c-125">Kui automaatne sisestamine ei ole konfigureeritud, kontrollib ostureskontro koordinaator, et kõik originaalkviitungid oleksid esitatud ja et kviitungid oleksid kooskõlas kuluaruandel olevate kuludega.</span><span class="sxs-lookup"><span data-stu-id="9979c-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="9979c-126">Kontrollida tuleb ka kõigi kuluaruandele sisestatud maksukoodide õigsust.</span><span class="sxs-lookup"><span data-stu-id="9979c-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="9979c-127">Kui need nõuded on kontrollitud, siis kuluaruanne sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="9979c-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="9979c-128">Pärast kuluaruande sisestamist autoriseeritakse kuluaruande makse ja kulud hüvitatakse töötajale.</span><span class="sxs-lookup"><span data-stu-id="9979c-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>

