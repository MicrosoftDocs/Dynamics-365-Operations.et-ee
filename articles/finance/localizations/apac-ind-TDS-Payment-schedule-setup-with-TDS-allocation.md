---
title: TDS-i eraldamisega maksegraafikute häälestamine
description: See teema kirjeldab, kuidas seadistada maksegraafikuid allika (TDS) eraldamisel mahaarvatud maksuga.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023186"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a><span data-ttu-id="80841-103">TDS-i eraldamisega maksegraafikute häälestamine</span><span class="sxs-lookup"><span data-stu-id="80841-103">Set up payment schedules with TDS allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80841-104">See teema kirjeldab, kuidas seadistada maksegraafikuid allika (TDS) eraldamisel mahaarvatud maksuga.</span><span class="sxs-lookup"><span data-stu-id="80841-104">This topic explains how to set up payment schedules with Tax Deducted at Source (TDS) allocation.</span></span>

1. <span data-ttu-id="80841-105">Avage **Ostureskontro \> Makse seadistus \> Maksegraafikud**.</span><span class="sxs-lookup"><span data-stu-id="80841-105">Go to **Accounts payable \> Payment setup \> Payment schedules**.</span></span>

    <span data-ttu-id="80841-106">[![Maksegraafikute leht](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span><span class="sxs-lookup"><span data-stu-id="80841-106">[![Payment schedules page](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span></span>

2. <span data-ttu-id="80841-107">Tegevuspaanil valige **Uus** TDS-ile kinnipeetava maksu grupi loomiseks ja sisestage nõutavad üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="80841-107">On the Action Pane, select **New** to create a payment schedule, and enter the required details.</span></span>
3. <span data-ttu-id="80841-108">Valige **Eraldamine** väljal meetod, mida kasutada makse eraldamiseks maksegraafiku jaoks:</span><span class="sxs-lookup"><span data-stu-id="80841-108">In the **Allocation** field, select the method to use to allocate the payment for the payment schedule:</span></span>

    - <span data-ttu-id="80841-109">Kokku</span><span class="sxs-lookup"><span data-stu-id="80841-109">Total</span></span>
    - <span data-ttu-id="80841-110">Fikseeritud summa</span><span class="sxs-lookup"><span data-stu-id="80841-110">Fixed amount</span></span>
    - <span data-ttu-id="80841-111">Fikseeritud kogus</span><span class="sxs-lookup"><span data-stu-id="80841-111">Fixed quantity</span></span>
    - <span data-ttu-id="80841-112">Määratud</span><span class="sxs-lookup"><span data-stu-id="80841-112">Specified</span></span>

    <span data-ttu-id="80841-113">**Kinnipeetava maksu eraldamise** väljal kuvatakse maksegraafiku TDS-i eraldamismeetod.</span><span class="sxs-lookup"><span data-stu-id="80841-113">The **Withholding tax allocation** field shows the TDS allocation method for the payment schedule.</span></span> <span data-ttu-id="80841-114">Kui valite **Kokku** väljal **Eraldamine**, seatakse **Kinnipeetava maksu eraldamise** väljal automaatselt **Kokku**.</span><span class="sxs-lookup"><span data-stu-id="80841-114">If you select **Total** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Total**.</span></span> <span data-ttu-id="80841-115">Kui valite väljal **Fikseeritud summa**, **Fikseeritud kogus**, või **i Määratud** **Eraldamise** väljal, seatakse **Eraldamise** väärtuseks automaatselt **Proportsionaalne**.</span><span class="sxs-lookup"><span data-stu-id="80841-115">If you select **Fixed amount**, **Fixed quantity**, or **Specified** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Proportionally**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="80841-116">Kui **Kinnipeetava maksu eraldamise** väli on seatud **Kokku**, siis arvutatakse makse osamaksed brutosumma alusel, mis sisaldabTDS-summat.</span><span class="sxs-lookup"><span data-stu-id="80841-116">If the **Withholding tax allocation** field is set to **Total**, the payment installments are calculated based on the gross amount, which includes the TDS amount.</span></span> <span data-ttu-id="80841-117">Kui **Kinnipeetava maksu eraldamise** väli on seatud **Proportsionaalne**, siis arvutatakse makse osamaksed brutosumma alusel, mis sisaldabTDS-summat.</span><span class="sxs-lookup"><span data-stu-id="80841-117">If the **Withholding tax allocation** field is set to **Proportionally**, the payment installments are calculated based on the net invoice amount after the TDS amount is deducted.</span></span>

4. <span data-ttu-id="80841-118">Sisestage vormile nõutavad üksikasjad ja siis sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="80841-118">Enter the other required details, and then close the page.</span></span>
