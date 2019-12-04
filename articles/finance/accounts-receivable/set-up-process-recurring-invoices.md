---
title: Korduvate arvete seadistamine ja töötlemine
description: Selles artiklis selgitatakse, kuidas seadistada ja töödelda korduvaid arveid. Saate kasutada korduvaid arveid, kui peate klientidega tuleb arveldada regulaarselt sama summa.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b443630d1612b5095fefa74b5ed6d057be534b7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188943"
---
# <a name="set-up-and-process-recurring-invoices"></a><span data-ttu-id="870a8-104">Korduvate arvete seadistamine ja töötlemine</span><span class="sxs-lookup"><span data-stu-id="870a8-104">Set up and process recurring invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="870a8-105">Selles artiklis selgitatakse, kuidas seadistada ja töödelda korduvaid arveid.</span><span class="sxs-lookup"><span data-stu-id="870a8-105">This article explains how to set up and process recurring invoices.</span></span> <span data-ttu-id="870a8-106">Saate kasutada korduvaid arveid, kui peate klientidega tuleb arveldada regulaarselt sama summa.</span><span class="sxs-lookup"><span data-stu-id="870a8-106">You can use recurring invoices if you must invoice customers for the same amount on a regular basis.</span></span>

<a name="create-a-recurring-free-text-invoice-template"></a><span data-ttu-id="870a8-107">Korduva vabas vormis arve malli loomine</span><span class="sxs-lookup"><span data-stu-id="870a8-107">Create a recurring free text invoice template</span></span>
---------------------------------------------

<span data-ttu-id="870a8-108">Klientidele regulaarselt samade teenuste eest arve esitamiseks tuleb määratleda vabas vormis arve mall, mida saab arvete koostamisel uuesti kasutada.</span><span class="sxs-lookup"><span data-stu-id="870a8-108">To invoice customers for the same services on a regular basis, you must define a free text invoice template that can be reused to create the invoices.</span></span> <span data-ttu-id="870a8-109">See mall sisaldab järgmist teavet:</span><span class="sxs-lookup"><span data-stu-id="870a8-109">This template contains the following information:</span></span>

-   <span data-ttu-id="870a8-110">Päise teave, nt maksugrupid, maksetingimused ja makseviis</span><span class="sxs-lookup"><span data-stu-id="870a8-110">Header information, such as tax groups, terms of payment, and the method of payment</span></span>
-   <span data-ttu-id="870a8-111">Rea teave nagu teenuse kirjeldus, tulukontod, ühiku hind ja arve summa</span><span class="sxs-lookup"><span data-stu-id="870a8-111">Line information, such as the service description, revenue accounts, unit price, and invoice amount</span></span>
-   <span data-ttu-id="870a8-112">Saatmise ja käsitsemise tasud</span><span class="sxs-lookup"><span data-stu-id="870a8-112">Charges for shipping or handling</span></span>
-   <span data-ttu-id="870a8-113">Arvestuse jaotused koos finantsdimensiooni teabega (nt kulukeskused ja äriüksused)</span><span class="sxs-lookup"><span data-stu-id="870a8-113">Accounting distributions together with financial dimension information, such as cost centers and business units</span></span>

<span data-ttu-id="870a8-114">Tegelikult koostate terve arve ja salvestate selle mallina.</span><span class="sxs-lookup"><span data-stu-id="870a8-114">In effect, you're creating an entire invoice and saving it as a template.</span></span> <span data-ttu-id="870a8-115">Saate seadistada malle lehel **Korduvad arved**.</span><span class="sxs-lookup"><span data-stu-id="870a8-115">You can set up the templates using the **Recurring invoices** page.</span></span>

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a><span data-ttu-id="870a8-116">Korduva vabas vormis arve malli määramine kliendile ja kordumise üksikasjade sisestamine</span><span class="sxs-lookup"><span data-stu-id="870a8-116">Assign a free text invoice template to a customer and enter recurrence details</span></span>
<span data-ttu-id="870a8-117">Pärast malli loomist peate määrama malli klientidele, kellega soovite arveldada.</span><span class="sxs-lookup"><span data-stu-id="870a8-117">After the template is created, you must assign the template to the customers that you want to invoice.</span></span> <span data-ttu-id="870a8-118">Lisaks peate määrama, millal ja kui sageli arvet kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="870a8-118">Additionally, you must specify when and how often the invoice will be used.</span></span> <span data-ttu-id="870a8-119">Malle saab määrata vahekaardil **Arve** lehel **Kliendid**.</span><span class="sxs-lookup"><span data-stu-id="870a8-119">You can assign the templates on the **Invoice** tab of the **Customers** page.</span></span> <span data-ttu-id="870a8-120">Lisage mall loendisse ja muutke järgmisi andmeid.</span><span class="sxs-lookup"><span data-stu-id="870a8-120">Add the template to the list, and update the following information:</span></span>

-   <span data-ttu-id="870a8-121">Alguskuupäev ja soovi korral korduva arvelduse lõppkuupäev</span><span class="sxs-lookup"><span data-stu-id="870a8-121">The start date and, optionally, the end date for the recurring billing</span></span>
-   <span data-ttu-id="870a8-122">Korduva arvelduse sagedus (nt iga päev või kord kuus)</span><span class="sxs-lookup"><span data-stu-id="870a8-122">The frequency of the recurring billing (for example, every day or once a month)</span></span>
-   <span data-ttu-id="870a8-123">Maksimaalne arvete summa (kui see on vajalik)</span><span class="sxs-lookup"><span data-stu-id="870a8-123">The maximum billing amount (if this information is required)</span></span>

<span data-ttu-id="870a8-124">Kliendil võib olla mitu malli, millel on erinevad sagedused.</span><span class="sxs-lookup"><span data-stu-id="870a8-124">A customer can have multiple templates that have different frequencies.</span></span>

## <a name="generate-the-recurring-invoices"></a><span data-ttu-id="870a8-125">Korduvate arvete loomine</span><span class="sxs-lookup"><span data-stu-id="870a8-125">Generate the recurring invoices</span></span>
<span data-ttu-id="870a8-126">Lehel **Korduvad arved**on ülesanne, mis töötleb korduvate arvete malle.</span><span class="sxs-lookup"><span data-stu-id="870a8-126">On the **Recurring invoices** page, there is a task that processes recurring invoice templates.</span></span> <span data-ttu-id="870a8-127">Saate määrata arve kuupäeva ja malli, millest arveid luua.</span><span class="sxs-lookup"><span data-stu-id="870a8-127">You specify the invoice date and the template to generate the invoices from.</span></span> <span data-ttu-id="870a8-128">Luuakse arved ja neile määratakse üks kordumise ID-kood iga töödeldava arvegrupi kohta.</span><span class="sxs-lookup"><span data-stu-id="870a8-128">Invoices will be generated and assigned a single recurrence ID number for each group of invoices that is processed.</span></span>

<a name="post-recurring-free-text-invoices"></a><span data-ttu-id="870a8-129">Vabas vormis korduvate arvete sisestamine</span><span class="sxs-lookup"><span data-stu-id="870a8-129">Post recurring free text invoices</span></span>
---------------------------------

<span data-ttu-id="870a8-130">Pärast korduvate arvete loomist kuvatakse lehel **Korduvad arved**ülesande sisestamisel arve kordumise ID-koodid.</span><span class="sxs-lookup"><span data-stu-id="870a8-130">After recurring invoices are generated, the invoice recurrence IDs appear in a posting task on the **Recurring invoices** page.</span></span> <span data-ttu-id="870a8-131">Linki klõpsates saate vaadata kõigi arvete kordumise ID-d.</span><span class="sxs-lookup"><span data-stu-id="870a8-131">You can view all of the invoices for a recurrence ID by clicking the link.</span></span> <span data-ttu-id="870a8-132">Arvete kordumise ID ülevaatamisel saate eraldi arveid kustutada.</span><span class="sxs-lookup"><span data-stu-id="870a8-132">During your review of the invoices for the recurrence ID, you can delete individual invoices.</span></span> <span data-ttu-id="870a8-133">Kliendi kordumise sätted lähtestatakse selle malli puhul, et seda saaks hiljem uuesti luua.</span><span class="sxs-lookup"><span data-stu-id="870a8-133">The customer's recurrence settings will be reset for that template, so that it can be regenerated later.</span></span> <span data-ttu-id="870a8-134">Kordumise ID-koodile saab sisestada ühe arve, mitu arvet või kõik arved.</span><span class="sxs-lookup"><span data-stu-id="870a8-134">You can post one, many, or all of the invoices for a recurrence ID.</span></span> <span data-ttu-id="870a8-135">Kui töövood on lubatud, peate klõpsama enne arvete sisestamist nuppu **Edasta**.</span><span class="sxs-lookup"><span data-stu-id="870a8-135">If workflows are enabled, you must click **Submit** before you can post the invoices.</span></span>

<a name="print-recurring-free-text-invoices"></a><span data-ttu-id="870a8-136">Vabas vormis korduvate arvete printimine</span><span class="sxs-lookup"><span data-stu-id="870a8-136">Print recurring free text invoices</span></span>
----------------------------------

<span data-ttu-id="870a8-137">Kui korduvad arved on sisestatud, saate printida arved vabas vormis arvete loendilehelt.</span><span class="sxs-lookup"><span data-stu-id="870a8-137">After recurring invoices are posted, you can print the invoices from the free text invoice list page.</span></span> <span data-ttu-id="870a8-138">Printida saab valitud arved või valida printimiseks arvete vahemiku.</span><span class="sxs-lookup"><span data-stu-id="870a8-138">You can print the invoices that are selected, or you can select a range of invoices to print.</span></span>


