---
title: Vabas vormis arve parandamine
description: Selles artiklis selgitatakse, kuidas parandada sisestatud vabas vormis arvet ja väljastada see uuesti parandatud arvena.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76cf1f24a31f246a41601908ebba308551925d90
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177401"
---
# <a name="correct-a-free-text-invoice"></a><span data-ttu-id="6021d-103">Vabas vormis arve parandamine</span><span class="sxs-lookup"><span data-stu-id="6021d-103">Correct a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6021d-104">Selles artiklis selgitatakse, kuidas parandada sisestatud vabas vormis arvet ja väljastada see uuesti parandatud arvena.</span><span class="sxs-lookup"><span data-stu-id="6021d-104">This article explains how to correct a free text invoice that has been posted and reissue it as a corrected invoice.</span></span>

<span data-ttu-id="6021d-105">Juba sisestatud vabas vormis arve parandamiseks avage sisestatud vabas vormis arve.</span><span class="sxs-lookup"><span data-stu-id="6021d-105">To correct a free text invoice that has already been posted, open the posted free text invoice.</span></span> <span data-ttu-id="6021d-106">Valige lehel **Arve** suvand **Tühista** ja seejärel **Arve parandamine**.</span><span class="sxs-lookup"><span data-stu-id="6021d-106">On the **Invoice** page, select **Cancel**, and then select **Correct invoice**.</span></span> <span data-ttu-id="6021d-107">Valige põhjuse kood, lisage kommentaarid ja valige uue parandatud arve kuupäev.</span><span class="sxs-lookup"><span data-stu-id="6021d-107">Select a reason code, add comments, and select the date for new corrected invoice.</span></span> <span data-ttu-id="6021d-108">Saate parandatud arvet muuta ja selle sisestada.</span><span class="sxs-lookup"><span data-stu-id="6021d-108">You can modify the corrected invoice, and post it.</span></span> 

<span data-ttu-id="6021d-109">Parandatud arve sisestamisel koostatakse tühistamisarve krediidisummale, mis võrdub algse arve summaga.</span><span class="sxs-lookup"><span data-stu-id="6021d-109">When you post the corrected invoice, a canceling invoice is created for a credit amount that equals the original invoice amount.</span></span> <span data-ttu-id="6021d-110">Seetõttu on algse arve ja arve tühistamise kombineeritud saldo 0 (null).</span><span class="sxs-lookup"><span data-stu-id="6021d-110">Therefore, the combined balance of the original invoice and the canceling invoice is 0 (zero).</span></span> <span data-ttu-id="6021d-111">Tühistamisarve tasakaalustatakse algse arve suhtes.</span><span class="sxs-lookup"><span data-stu-id="6021d-111">The canceling invoice is settled against the original invoice.</span></span> 

<span data-ttu-id="6021d-112">Pärast parandatud arve sisestamist, on teil kolm arvet.</span><span class="sxs-lookup"><span data-stu-id="6021d-112">After you post the corrected invoice, you will have three invoices:</span></span>

-   <span data-ttu-id="6021d-113">**Algne arve** – arve, mis sisaldab parandatavat teavet.</span><span class="sxs-lookup"><span data-stu-id="6021d-113">**Original invoice** – The invoice that includes the information that you're correcting.</span></span>
-   <span data-ttu-id="6021d-114">**Tühistamisarve** – süsteemi loodud kreeditarve, mis loodi viimati parandatud arve tühistamiseks.</span><span class="sxs-lookup"><span data-stu-id="6021d-114">**Canceling invoice** – The system-generated credit invoice that was created to cancel the invoice that was most recently corrected.</span></span>
-   <span data-ttu-id="6021d-115">**Parandatud arve** – arve, mis sisaldab parandatud arve teavet.</span><span class="sxs-lookup"><span data-stu-id="6021d-115">**Corrected invoice** – The invoice that contains the corrected invoice information.</span></span>

<span data-ttu-id="6021d-116">Tühistamis- ja parandamisarveid saab tuvastada kahel moel.</span><span class="sxs-lookup"><span data-stu-id="6021d-116">You can identify canceling and correcting invoices in two ways:</span></span>

-   <span data-ttu-id="6021d-117">Lehel **Kõik vabas vormis arved** on veerg **Parandus**, kus näete, millised arved on tühistamis- ja parandusarved.</span><span class="sxs-lookup"><span data-stu-id="6021d-117">The **All free text invoices** page includes a **Correction** column, where you can see which invoices are canceling invoices and corrected invoices.</span></span>
-   <span data-ttu-id="6021d-118">Vabas vormis arve päises on näha olek **Tühistusarve \[arve number\]** või **Parandusarve \[arve number\]**.</span><span class="sxs-lookup"><span data-stu-id="6021d-118">The header of the free text invoice shows a status of **Cancelling invoice '\[invoice number\]'** or **Corrected invoice '\[invoice number\]'**.</span></span>

> [!NOTE]
> <span data-ttu-id="6021d-119">See funktsioon on saadaval ainult juhul, kui on valitud konfiguratsioonivõti **Vabas vormis arve parandamine**.</span><span class="sxs-lookup"><span data-stu-id="6021d-119">This feature is available only if the **Free text invoice correction** configuration key is selected.</span></span> <span data-ttu-id="6021d-120">Konfiguratsioonivõtmete lubamise kohta lisateabe saamiseks vaadake jaotist Luba (või keela) konfiguratsioonivõtmed teemas [Hooldusrežiim](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/maintenance-mode)</span><span class="sxs-lookup"><span data-stu-id="6021d-120">For more information on how to enable Configuration keys refer to the Enable (or disable) configuration keys section in the [Maintenance mode](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/maintenance-mode) topic.</span></span> 


