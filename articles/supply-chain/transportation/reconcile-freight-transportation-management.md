---
title: Veose vastavusseviimine transpordihalduses
description: Selles artiklis selgitatakse veose vastavusseviimise protsessi.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f92808f904ba93513e20b74bd2b597712cb93d4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "344773"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="aed40-103">Veose vastavusseviimine transpordihalduses</span><span class="sxs-lookup"><span data-stu-id="aed40-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aed40-104">Selles artiklis selgitatakse veose vastavusseviimise protsessi.</span><span class="sxs-lookup"><span data-stu-id="aed40-104">This article describes the freight reconciliation process.</span></span>

<span data-ttu-id="aed40-105">Veose vastavusseviimine võib toimuda käsitsi või olla seadistatud toimuma automaatselt.</span><span class="sxs-lookup"><span data-stu-id="aed40-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="aed40-106">Veose automaatse vastavusseviimise kasutamiseks tuleb seadistada auditi koondandmed, milles saate määratleda kriteeriumid, mis määravad, millised veoarved automaatselt vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="aed40-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="aed40-107">Veose vastavusseviimise protsess</span><span class="sxs-lookup"><span data-stu-id="aed40-107">The freight reconciliation process</span></span>
<span data-ttu-id="aed40-108">Veohinnad arvutab hinnamootor, mis on seotud vastava vedajaga.</span><span class="sxs-lookup"><span data-stu-id="aed40-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="aed40-109">Koorma kinnitamisel koostatakse veoarve ja veohinnad kantakse sellele üle.</span><span class="sxs-lookup"><span data-stu-id="aed40-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="aed40-110">Veohinnad jaotatakse vastavale lähtedokumendile (ostutellimus, müügitellimus ja/või üleviimistellimus) muude kuludena, olenevalt tavapärase arveldusprotsessi puhul kasutatavast seadistusest.</span><span class="sxs-lookup"><span data-stu-id="aed40-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="aed40-111">Kauba vastavusseviimise protsess (mida nimetatakse ka vastendusprotsessiks) alustatakse kohe, kui veoarve vedajalt saabub.</span><span class="sxs-lookup"><span data-stu-id="aed40-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="aed40-112">Arve võib võtta vastu elektrooniliselt või paberkandjal.</span><span class="sxs-lookup"><span data-stu-id="aed40-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="aed40-113">Kui arve saadakse paberkandjal, võite koostada elektroonilise arve, kasutades mallina veoarvet.</span><span class="sxs-lookup"><span data-stu-id="aed40-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span> 

<span data-ttu-id="aed40-114">[![Veose vastavusseviimise protsess](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="aed40-114">[![Freight reconcilation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="aed40-115">Käsitsi vastavusseviimine</span><span class="sxs-lookup"><span data-stu-id="aed40-115">Manual reconciliation</span></span>
<span data-ttu-id="aed40-116">Kui viite veose vastavusse käsitsi, tuleb vastendada iga arve rida veoarve reaga või arveldatava koorma ridadega.</span><span class="sxs-lookup"><span data-stu-id="aed40-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="aed40-117">Selline vastendamine toimub lehel **Veoarve ja arvete võrdlemine**.</span><span class="sxs-lookup"><span data-stu-id="aed40-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="aed40-118">Kui arve real olev summa ei vasta veoarve summale, tuleb valida vahe jaoks vastavusseviimise põhjus.</span><span class="sxs-lookup"><span data-stu-id="aed40-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="aed40-119">Kui vastavusseviimisel on mitu põhjust, võite vastendamata summa nende vahel ära jagada.</span><span class="sxs-lookup"><span data-stu-id="aed40-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="aed40-120">Vastavusseviimise põhjus määrab, kuidas vahesummad pearaamatusse sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="aed40-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="aed40-121">Kui arvestatakse kogu arve summat, esitatakse see kinnitamiseks ja seejärel tööleht sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="aed40-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="aed40-122">Järgmine illustratsioon näitab, kuidas koostada rakenduses Microsoft Dynamics 365 for Finance and Operations veose arvet ja veost vastavusse viia.</span><span class="sxs-lookup"><span data-stu-id="aed40-122">The following illustration shows how to generate a freight invoice and do freight reconciliation in Microsoft Dynamics 365 for Finance and Operations.</span></span> 
<span data-ttu-id="aed40-123">[![Veose vastavusseviimise ülesanded Dynamics AX-is](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="aed40-123">[![Freight reconcilation tasks in Dynamics AX](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>
## <a name="automatic-reconciliation"></a><span data-ttu-id="aed40-124">Automaatne vastavusseviimine</span><span class="sxs-lookup"><span data-stu-id="aed40-124">Automatic reconciliation</span></span>
<span data-ttu-id="aed40-125">Automaatse vastavusseviimise kasutamiseks tuleb määrata vastavusseviimise graafik ning kasutatavad arved ja vedajad.</span><span class="sxs-lookup"><span data-stu-id="aed40-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="aed40-126">Vastendamine arve ridadel ja veoarvetel toimub auditi koondandmete ja veose arve tüübi seadistusele.</span><span class="sxs-lookup"><span data-stu-id="aed40-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="aed40-127">Pärast automaatse vastavusseviimise käitamist tuleb tegeleda arvetega, millele süsteem vastet ei leia.</span><span class="sxs-lookup"><span data-stu-id="aed40-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="aed40-128">Neid arveid peab siis käsitsi töötlema, enne kui saate kõik arved maksmiseks sisestada.</span><span class="sxs-lookup"><span data-stu-id="aed40-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>



