---
title: Krediidi ja võlanõuete ülevaade
description: Selles teemas antakse ülevaade krediidi ja võlanõuete funktsionaalsusest.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a822e5f5a6cb71a0234b1776211788578470b0bb
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124296"
---
# <a name="credit-and-collections-overview"></a><span data-ttu-id="a1890-103">Krediidi ja võlanõuete ülevaade</span><span class="sxs-lookup"><span data-stu-id="a1890-103">Credit and collections overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1890-104">Saate hallata oma klientide krediidilimiite ja vajadusel teostada võlanõudmise tegevusi.</span><span class="sxs-lookup"><span data-stu-id="a1890-104">You can manage credit limits for your customers and perform collection activities when they become necessary.</span></span>

## <a name="credit-management"></a><span data-ttu-id="a1890-105">Krediidihaldus</span><span class="sxs-lookup"><span data-stu-id="a1890-105">Credit management</span></span>

<span data-ttu-id="a1890-106">Kliendi krediidihaldus võimaldab teil hallata krediidilimiite ja kontrollida müügitellimuste voogu läbi sisestamisprotsessi teie loodud krediidireeglite alusel.</span><span class="sxs-lookup"><span data-stu-id="a1890-106">Customer credit management lets you manage credit limits and control the flow of sales orders through the posting process, based on credit rules that you create.</span></span>

<span data-ttu-id="a1890-107">Krediidihalduse protsess võib sisaldada järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="a1890-107">The credit management process can include any of the following steps:</span></span>

- <span data-ttu-id="a1890-108">Klientide krediidiatribuutide värskendamine, mis annab nende krediidivõime kohta täiendavat teavet.</span><span class="sxs-lookup"><span data-stu-id="a1890-108">Update credit attributes for customers to provide additional information about their credit worthiness.</span></span>
- <span data-ttu-id="a1890-109">Krediidilimiitide loomine klientidele krediidilimiidi korrigeerimise abil.</span><span class="sxs-lookup"><span data-stu-id="a1890-109">Create credit limits for customers by using credit limit adjustments.</span></span>
- <span data-ttu-id="a1890-110">Ajutiste krediidilimiitide loomine klientidele krediidilimiidi korrigeerimise abil.</span><span class="sxs-lookup"><span data-stu-id="a1890-110">Create temporary credit limits for customers by using credit limit adjustments.</span></span> <span data-ttu-id="a1890-111">Sel viisil saate ärilistel vajadustel kliendi krediidilimiite ajutiselt suurendada või vähendada.</span><span class="sxs-lookup"><span data-stu-id="a1890-111">In this way, you can temporarily increase or decrease customer credit limits, based on business requirements.</span></span>
- <span data-ttu-id="a1890-112">Täiendavate andmete lisamine, mis võib mõjutada krediidilimiiti, nt kindlustuse ja garantiide info.</span><span class="sxs-lookup"><span data-stu-id="a1890-112">Add information that can affect the credit limit, such as information about insurance and guarantees.</span></span>
- <span data-ttu-id="a1890-113">Looge kliente kokku ühendavaid kliendi krediidigruppe, et nad saaksid jagada ühte krediidilimiiti.</span><span class="sxs-lookup"><span data-stu-id="a1890-113">Create customer credit groups that link customers together so that they share a single credit limit.</span></span>
- <span data-ttu-id="a1890-114">Määrake klientidele riskiskoorid ja seejärel kasutage neid skoore krediidilimiidi korrigeerimise abil nende klientide krediidilimiitide automaatseks loomiseks.</span><span class="sxs-lookup"><span data-stu-id="a1890-114">Assign risk scores to customers, and then use the scores to automatically generate credit limits for those customers through credit limit adjustments.</span></span>
- <span data-ttu-id="a1890-115">Looge blokeerimise reeglid, mis panevad ühe või mitme sisestamise protsessi ajal tellimuse ootele, põhinedes sellistel faktoritel nagu risk, maksetingimused, kreediti limiidid, tähtaja ületanud summad ja kasutatud krediidilimiit.</span><span class="sxs-lookup"><span data-stu-id="a1890-115">Create blocking rules that put an order on hold during one or more posting processes, based on factors such as risk, payment terms, credit limits, overdue amounts, and the percentage of the credit limit that has been used.</span></span>
- <span data-ttu-id="a1890-116">Hallake ootel olevate müügitellimuste loendit, vaadake üle ootelepaneku põhjused ja kõrvaldage probleeme.</span><span class="sxs-lookup"><span data-stu-id="a1890-116">Manage a list of sales orders that are on hold, review the reasons for the hold, and mitigate issues.</span></span>
- <span data-ttu-id="a1890-117">Vabastage müügitellimused, et need läheksid edasi sisestamise protsessi kaudu.</span><span class="sxs-lookup"><span data-stu-id="a1890-117">Release sales orders so that they continue through the posting process.</span></span>
- <span data-ttu-id="a1890-118">Seadistage töövoog krediidilimiidi muudatuste ja müügitellimuse vabastamiste kinnitamise haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="a1890-118">Set up a workflow to manage the approval of credit limit changes and sales order releases.</span></span>

## <a name="collections-management"></a><span data-ttu-id="a1890-119">Sissenõuete haldus</span><span class="sxs-lookup"><span data-stu-id="a1890-119">Collections management</span></span>

<span data-ttu-id="a1890-120">Leht **Sissenõuded** annab keskse vaate, kus hallatakse müügireskontro nõudeid.</span><span class="sxs-lookup"><span data-stu-id="a1890-120">The **Collections** page provides a centralized view where accounts receivable collections information is managed.</span></span> <span data-ttu-id="a1890-121">Sissenõuete haldurid saavad kasutada seda keskset vaadet sissenõuete haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="a1890-121">Collections managers can use this centralized view to manage collections.</span></span> <span data-ttu-id="a1890-122">Inkassaatorid saavad alustada sissenõudmise protsessi kas klientide loendist, mis luuakse eelmääratud sissenõude kriteeriumite alusel, või lehelt **Kliendid**.</span><span class="sxs-lookup"><span data-stu-id="a1890-122">Collections agents can begin the collections process either from customer lists that are generated by using predefined collection criteria or from the **Customers** page.</span></span>

<span data-ttu-id="a1890-123">Enne sissenõuete seadistamise alustamist või nendega töötamist peaksite teadma järgmisi põhimõtteid.</span><span class="sxs-lookup"><span data-stu-id="a1890-123">Before you start to set up or work with collections, you should understand the following concepts:</span></span>

- <span data-ttu-id="a1890-124">Kliendi aegumise hetktõmmised sisaldavad aegunud saldoteavet teatud ajahetkel.</span><span class="sxs-lookup"><span data-stu-id="a1890-124">Customer aging snapshots contain aged balance information at a specific point in time.</span></span>
- <span data-ttu-id="a1890-125">Sissenõuete kliendikaustad aitavad teil oma tööd korraldada.</span><span class="sxs-lookup"><span data-stu-id="a1890-125">Collections customer pools help you organize your work.</span></span>
- <span data-ttu-id="a1890-126">Inkassaatoritel võivad olla oma kliendikaustad.</span><span class="sxs-lookup"><span data-stu-id="a1890-126">Collections agents can have their own customer pools.</span></span>
- <span data-ttu-id="a1890-127">Loendilehtedel korraldatakse sissenõuete kliendid, tegevused ja juhtumid.</span><span class="sxs-lookup"><span data-stu-id="a1890-127">List pages organize collections customers, activities, and cases.</span></span>
- <span data-ttu-id="a1890-128">Kogu kliendi sissenõuete teave on ühel lehel ja saate tegevusi sellelt lehelt teha.</span><span class="sxs-lookup"><span data-stu-id="a1890-128">All collections information for a customer is on one page, and you can take action from that page.</span></span>
- <span data-ttu-id="a1890-129">Intresside ja tasude puhul saab loobumise, ennistamise või tühistamise teha ühe etapina.</span><span class="sxs-lookup"><span data-stu-id="a1890-129">Interest and fees can be waived, reinstated, or reversed in one step.</span></span>
- <span data-ttu-id="a1890-130">Mahakandmiskanded saab luua ühe etapina.</span><span class="sxs-lookup"><span data-stu-id="a1890-130">Write-off transactions can be created in one step.</span></span>
- <span data-ttu-id="a1890-131">Ebapiisavate vahendite (NSF) maksed saab töödelda ühe etapina.</span><span class="sxs-lookup"><span data-stu-id="a1890-131">Not sufficient funds (NSF) payments can be processed in one step.</span></span>

<span data-ttu-id="a1890-132">Nende kontseptsioonide kirjeldused leiate jaotisest [Võlanõuete halduse võtmekontseptsioonid](./cm-collections-concepts.md).</span><span class="sxs-lookup"><span data-stu-id="a1890-132">For descriptions of these concepts, see [Collections management key concepts](./cm-collections-concepts.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a1890-133">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a1890-133">Additional resources</span></span>

[<span data-ttu-id="a1890-134">Kliendi krediidihalduse parameetrite seadistus</span><span class="sxs-lookup"><span data-stu-id="a1890-134">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="a1890-135">Kliendi krediidihalduse andmete seadistus</span><span class="sxs-lookup"><span data-stu-id="a1890-135">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="a1890-136">Kliendile krediidihalduse andmete lisamine</span><span class="sxs-lookup"><span data-stu-id="a1890-136">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="a1890-137">Kliendi krediidigrupid</span><span class="sxs-lookup"><span data-stu-id="a1890-137">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="a1890-138">Kliendi kreeditilimiidi korrigeerimised</span><span class="sxs-lookup"><span data-stu-id="a1890-138">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="a1890-139">Müügitellimuste krediidi ootelolekud</span><span class="sxs-lookup"><span data-stu-id="a1890-139">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="a1890-140">Perioodilised kliendi krediidihalduse ülesanded</span><span class="sxs-lookup"><span data-stu-id="a1890-140">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)
