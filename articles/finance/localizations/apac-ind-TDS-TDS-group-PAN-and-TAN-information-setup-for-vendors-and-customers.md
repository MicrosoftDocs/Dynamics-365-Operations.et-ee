---
title: TDS-i grupi, PAN-i ja TAN-i teabe häälestus hankijatele ja klientidele
description: See teema kirjeldab, kuidas seadistada teavet maksu kohta allika (TDS) grupis, püsikonto numbri (PAN) ja maksukonto numbri (TAN) kohta hankijatele ja klientidele.
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
ms.openlocfilehash: fd33b1775afefed798f1e9bb7601f4112222c430
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023179"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a><span data-ttu-id="ec5a6-103">TDS-i grupi, PAN-i ja TAN-i teabe häälestus hankijatele ja klientidele</span><span class="sxs-lookup"><span data-stu-id="ec5a6-103">TDS group, PAN, and TAN information setup for vendors and customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec5a6-104">See teema kirjeldab, kuidas seadistada teavet maksu kohta allika (TDS) grupis, püsikonto numbri (PAN) ja maksukonto numbri (TAN) kohta hankijatele ja klientidele.</span><span class="sxs-lookup"><span data-stu-id="ec5a6-104">This topic explains how to set up information about the Tax Deducted at Source (TDS) group, permanent account number (PAN), and tax account number (TAN) for vendors and customers.</span></span>

1. <span data-ttu-id="ec5a6-105">Minge **Ostureskontro \> Hankijatele \> Kõik hankijad** või **Müügireskontro \> kliendid \> Kõik kliendid**.</span><span class="sxs-lookup"><span data-stu-id="ec5a6-105">Go to **Accounts payable \> Vendors \> All vendors** or **Accounts receivable \> Customers \> All customers**.</span></span>

    <span data-ttu-id="ec5a6-106">[![Kõigi hankijate leht](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span><span class="sxs-lookup"><span data-stu-id="ec5a6-106">[![All vendors page](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span></span>

2. <span data-ttu-id="ec5a6-107">Tegevuspaanil valige **Uus** TDS-ile kinnipeetava maksu grupi loomiseks ja sisestage nõutavad üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="ec5a6-107">On the Action Pane, select **New** to create a vendor or customer, and enter the required details.</span></span> <span data-ttu-id="ec5a6-108">Teise võimalusena valige olemasolev hankija või klient.</span><span class="sxs-lookup"><span data-stu-id="ec5a6-108">Alternatively, select an existing vendor or customer.</span></span>
3. <span data-ttu-id="ec5a6-109">Määrake suvandi **Arve ja tarne** kiirkaardil **Kinnipeetava maksu** jaotises **Kinnipeetava maksu arvutamine** väärtuseks **Jah** et arvutada hankijale või kliendile kinnipeetav maks, TDS või mks, mis on kogutud allikasse (TCS).</span><span class="sxs-lookup"><span data-stu-id="ec5a6-109">On the **Invoice and delivery** FastTab, in the **Withholding tax** section, set the **Calculate withholding tax** option to **Yes** to calculate withholding tax, TDS, or Tax Collected at Source (TCS) for the vendor or customer.</span></span>
4. <span data-ttu-id="ec5a6-110">Ostuarve TDS arvutatakse hankijale või kliendile määratud TDS-i vaikegrupi alusel.</span><span class="sxs-lookup"><span data-stu-id="ec5a6-110">TDS for a purchase invoice is calculated based on the default TDS group that is defined for the vendor or customer.</span></span> <span data-ttu-id="ec5a6-111">Valige TDS grupp väljal **TDS grupp**.</span><span class="sxs-lookup"><span data-stu-id="ec5a6-111">In the **TDS group** field, select the default TDS group.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ec5a6-112">Kui valite TDS grupi **TDS-i grupp** väljal, muutuvad **Kinnipeetava maksu grupp** ja **TCS-grupp** kättesaamatuks.</span><span class="sxs-lookup"><span data-stu-id="ec5a6-112">When you select a TDS group in the **TDS group** field, the **Withholding tax group** and **TCS group** fields become unavailable.</span></span>

5. <span data-ttu-id="ec5a6-113">Valige **Maksuteabe** kiirkaardi **PAN-teabe** jaotises **Olek** hankija või kliendi püsikonto jaoks olek püsiv:</span><span class="sxs-lookup"><span data-stu-id="ec5a6-113">On the **Tax information** FastTab, in the **PAN information** section, in the **Status** field, select the status of the permanent account number for the vendor or customer:</span></span>

    - <span data-ttu-id="ec5a6-114">**Pole saadaval** – hankijal või kliendil ei ole PAN-i.</span><span class="sxs-lookup"><span data-stu-id="ec5a6-114">**Not available** – The vendor or customer doesn't have a PAN.</span></span>
    - <span data-ttu-id="ec5a6-115">**Saadud** – hankijal või kliendil on PAN.</span><span class="sxs-lookup"><span data-stu-id="ec5a6-115">**Received** – The vendor or customer has a PAN.</span></span>
    - <span data-ttu-id="ec5a6-116">**Rakendatud** – hankija või klient on taotlenud PAN-i.</span><span class="sxs-lookup"><span data-stu-id="ec5a6-116">**Applied** – The vendor or customer has applied for a PAN.</span></span>
    - <span data-ttu-id="ec5a6-117">**Kehtetu** – hankijal või kliendil on PAN, kuid see ei kehti.</span><span class="sxs-lookup"><span data-stu-id="ec5a6-117">**Invalid** – The vendor or customer has a PAN, but it isn't valid.</span></span>

6. <span data-ttu-id="ec5a6-118">Kui valisite **Saadud** **Olek** väljal et näidata hankijale või kliendile PAN-i omamist, sisestage PAN **Numbri** väljale.</span><span class="sxs-lookup"><span data-stu-id="ec5a6-118">If you selected **Received** in the **Status** field to indicate that the vendor or customer has a PAN, enter the PAN in the **Number** field.</span></span> <span data-ttu-id="ec5a6-119">PAN peab koosnema viiest tähestikumärgist, seejärel neljast numbrimärgist ja seejärel ühest tähestikumärgist.</span><span class="sxs-lookup"><span data-stu-id="ec5a6-119">The PAN must consist of five alphabetic characters, then four numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="ec5a6-120">Siin on näide: : **ABCDE1260A**.</span><span class="sxs-lookup"><span data-stu-id="ec5a6-120">Here is an example: **ABCDE1260A**.</span></span>
7. <span data-ttu-id="ec5a6-121">Kui valisite **Saadud** **Olek** väljal et näidata hankijale või kliendile PAN-i omamist, sisestage viitenumber **Viitenumbri** väljale.</span><span class="sxs-lookup"><span data-stu-id="ec5a6-121">If you selected **Applied** in the **Status** field to indicate that the vendor or customer has applied for PAN, enter the reference number in the **Reference number** field.</span></span>
8. <span data-ttu-id="ec5a6-122">Vaadake hankija või kliendi hinnalepete kategooria olemust Kinnipeetava maksu väljal, mis on **Hinna hindamise** väljagrupis:</span><span class="sxs-lookup"><span data-stu-id="ec5a6-122">In the **Nature of assessee** field, select the nature of assessee category that the vendor or customer belongs to:</span></span>

    - <span data-ttu-id="ec5a6-123">Ettevõte</span><span class="sxs-lookup"><span data-stu-id="ec5a6-123">Company</span></span>
    - <span data-ttu-id="ec5a6-124">HUF</span><span class="sxs-lookup"><span data-stu-id="ec5a6-124">HUF</span></span>
    - <span data-ttu-id="ec5a6-125">Kinnita</span><span class="sxs-lookup"><span data-stu-id="ec5a6-125">Firm</span></span>
    - <span data-ttu-id="ec5a6-126">Üksikisik</span><span class="sxs-lookup"><span data-stu-id="ec5a6-126">Individual</span></span>
    - <span data-ttu-id="ec5a6-127">AOP</span><span class="sxs-lookup"><span data-stu-id="ec5a6-127">AOP</span></span>
    - <span data-ttu-id="ec5a6-128">BOI</span><span class="sxs-lookup"><span data-stu-id="ec5a6-128">BOI</span></span>
    - <span data-ttu-id="ec5a6-129">Kohalik omavalitsus</span><span class="sxs-lookup"><span data-stu-id="ec5a6-129">Local authority</span></span>
    - <span data-ttu-id="ec5a6-130">Muud</span><span class="sxs-lookup"><span data-stu-id="ec5a6-130">Others</span></span>

    <span data-ttu-id="ec5a6-131">[![Maksuteabe kiirkaart](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span><span class="sxs-lookup"><span data-stu-id="ec5a6-131">[![Tax information FastTab](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span></span>

9. <span data-ttu-id="ec5a6-132">Seejärel, tegevuspaani **Hankija** vahekaardil, grupis **Kvaliteedijuhtimine**, valige **Registreerumine IDs**, et avada leht **Hallata aadresse**.</span><span class="sxs-lookup"><span data-stu-id="ec5a6-132">On the Action Pane, on the **Vendor** tab, in the **Registration** group, select **Registration IDs** to open the **Manage addresses** page.</span></span>
10. <span data-ttu-id="ec5a6-133">**Aadresside haldamise** lehel **Maksuteabe** kiirkaardil valige **Lisa** või **Redigeeri** et avada **Maksuteabe haldamine** leht, kus saate maksu registreerimiskirjet hallata.</span><span class="sxs-lookup"><span data-stu-id="ec5a6-133">On the **Manage addresses** page, on the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>
11. <span data-ttu-id="ec5a6-134">**Maksuteabe haldamine** lehel **Kinnipeetava maksu** kiirkaardil **Maksukonto number (TAN)** väljal, sisestage TAN.</span><span class="sxs-lookup"><span data-stu-id="ec5a6-134">On the **Manage tax information** page, on the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the TAN.</span></span> <span data-ttu-id="ec5a6-135">TAN peab koosnema viiest tähestikumärgist, seejärel neljast numbrimärgist ja seejärel ühest tähestikumärgist.</span><span class="sxs-lookup"><span data-stu-id="ec5a6-135">The TAN must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="ec5a6-136">Siin on näide: **AFGH54821T**.</span><span class="sxs-lookup"><span data-stu-id="ec5a6-136">Here is an example: **AFGH54821T**.</span></span>
12. <span data-ttu-id="ec5a6-137">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ec5a6-137">Close the page.</span></span>
