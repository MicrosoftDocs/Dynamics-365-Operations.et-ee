---
title: Kuluaruanded ja mitu kinnitajat
description: See teema sisaldab teavet kuluaruannete kohta, mille peab kinnitama rohkem kui üks isik.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d83a473e2e894856c12b36b4d005c6cb06b765a
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/30/2019
ms.locfileid: "1795120"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="d1f02-103">Kuluaruanded ja mitu kinnitajat</span><span class="sxs-lookup"><span data-stu-id="d1f02-103">Expense reports and multiple approvers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1f02-104">Olenevalt teie organisatsiooni kulude kinnitamise poliitikast võib olla vajalik, et töövõtja esitatud kuluaruande peab kinnitama rohkem kui üks isik.</span><span class="sxs-lookup"><span data-stu-id="d1f02-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="d1f02-105">Kuluaruande kinnitamise töövooprotsessi seadistamisel saate lisada töövoo elemente, mis sisaldavad ülesandeid või etappe kuluaruande ühe või mitme kinnitaja jaoks.</span><span class="sxs-lookup"><span data-stu-id="d1f02-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="d1f02-106">Näiteks võite nõuda, et kõik kuluaruanded peab esmalt kinnitama kuluaruande esitanud töövõtja haldur ja seejärel ostureskontro koordinaator.</span><span class="sxs-lookup"><span data-stu-id="d1f02-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="d1f02-107">Kui otsustate nõuda, et vaja on mitut kuluaruande kinnitajat, saate lisada töövoo elemente ühel järgmistest viisidest.</span><span class="sxs-lookup"><span data-stu-id="d1f02-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="d1f02-108">Lisage üks kinnitamise element, millel on üks etapp.</span><span class="sxs-lookup"><span data-stu-id="d1f02-108">Add one approval element that has one step.</span></span> <span data-ttu-id="d1f02-109">Näiteks võib see etapp nõuda, et kuluaruanne määratakse kasutajagrupile ja selle peavad kinnitama 50% kasutajagrupi liikmetest.</span><span class="sxs-lookup"><span data-stu-id="d1f02-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="d1f02-110">Lisage üks kinnitamise element, millel on mitu etappi.</span><span class="sxs-lookup"><span data-stu-id="d1f02-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="d1f02-111">Kinnitamise element võib sisaldada näiteks järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="d1f02-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="d1f02-112">Kuluaruande kinnitab kuluaruande esitanud töövõtja haldur.</span><span class="sxs-lookup"><span data-stu-id="d1f02-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="d1f02-113">Ostureskontro ametnik kinnitab kviitungid ja kuluaruande üksused.</span><span class="sxs-lookup"><span data-stu-id="d1f02-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="d1f02-114">Eelarve omanik kinnitab kuluaruande.</span><span class="sxs-lookup"><span data-stu-id="d1f02-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="d1f02-115">Lisage mitu kinnitamise elementi, millest igaühel on üks etapp.</span><span class="sxs-lookup"><span data-stu-id="d1f02-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="d1f02-116">Näiteks võite lisada eraldi kinnitamise elemendi iga järgmise etapi jaoks.</span><span class="sxs-lookup"><span data-stu-id="d1f02-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="d1f02-117">Töövõtja haldur kinnitab kuluaruande.</span><span class="sxs-lookup"><span data-stu-id="d1f02-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="d1f02-118">Eelarve omanik kinnitab kuluaruande.</span><span class="sxs-lookup"><span data-stu-id="d1f02-118">The budget owner approves the expense report.</span></span>
