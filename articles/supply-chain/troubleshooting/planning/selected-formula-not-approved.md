---
title: Valitud valeminumber pole partiitellimuse jaoks kinnitatud
description: Kui proovite plaanitud tellimust kinnitada, kuvatakse tõrketeade, mis ütleb, et valitud valeminumber pole partiitellimuse jaoks kinnitatud.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294052"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a><span data-ttu-id="6ff69-103">Valitud valeminumber pole partiitellimuse jaoks kinnitatud</span><span class="sxs-lookup"><span data-stu-id="6ff69-103">Selected formula number isn't approved for a batch order</span></span>

<span data-ttu-id="6ff69-104">Tõrkekood: PRO2614</span><span class="sxs-lookup"><span data-stu-id="6ff69-104">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="6ff69-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="6ff69-105">Symptoms</span></span>

<span data-ttu-id="6ff69-106">Kui proovite plaanitud tellimust kindlustada, kuvatakse järgmine tõrketeade:</span><span class="sxs-lookup"><span data-stu-id="6ff69-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="6ff69-107">Valitud valeminumber ei ole partiitellimuse puhul kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="6ff69-107">The selected formula number is not approved for a batch order.</span></span>

## <a name="cause"></a><span data-ttu-id="6ff69-108">Põhjus</span><span class="sxs-lookup"><span data-stu-id="6ff69-108">Cause</span></span>

<span data-ttu-id="6ff69-109">Süsteem kinnitab kinnitamistoimingu veendumaks, et aktiivse kauba jaoks on saadaval kinnitatud valem.</span><span class="sxs-lookup"><span data-stu-id="6ff69-109">The system validates the firming operation to make sure that an approved formula is available for the active item.</span></span> <span data-ttu-id="6ff69-110">Tõenäoliselt peate valemi kinnitama.</span><span class="sxs-lookup"><span data-stu-id="6ff69-110">You must probably approve the formula.</span></span>

## <a name="resolution"></a><span data-ttu-id="6ff69-111">Lahendus</span><span class="sxs-lookup"><span data-stu-id="6ff69-111">Resolution</span></span>

<span data-ttu-id="6ff69-112">Valemi kinnitamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="6ff69-112">To approve a formula, follow these steps.</span></span>

1. <span data-ttu-id="6ff69-113">Avage **Tooteteabe haldus \> Kooslused ja valemid \> Valemid**.</span><span class="sxs-lookup"><span data-stu-id="6ff69-113">Go to **Product information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="6ff69-114">Valige asjaomane valem.</span><span class="sxs-lookup"><span data-stu-id="6ff69-114">Select the relevant formula.</span></span>
1. <span data-ttu-id="6ff69-115">Valige tegumiriba vahekaardi **Valem** grupis **Halda** suvand **Kinnita valem**.</span><span class="sxs-lookup"><span data-stu-id="6ff69-115">On the Action Pane, on the **Formula** tab, in the **Maintain** group, select **Approve formula**.</span></span>
1. <span data-ttu-id="6ff69-116">Valige dialoogiboksis **Koosluse või valemi kinnitamine** kinnitaja ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ff69-116">In the **Approve BOM or formula** dialog box, select an approver, and then select **OK**.</span></span>
