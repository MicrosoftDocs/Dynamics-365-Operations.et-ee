---
title: Exceli töövihiku loomine jaemüügikannete redigeerimiseks
description: Selles teemas kirjeldatakse, kuidas luua Exceli töövihikut, et saaksite Microsoft Dynamics 365 Commerce'is jaemüügikandeid redigeerida.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3a4bc0a91ee2215dcde2f18575d58ab1ef2f5581
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207939"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="5c9f8-103">Exceli töövihiku loomine jaemüügikannete redigeerimiseks</span><span class="sxs-lookup"><span data-stu-id="5c9f8-103">Create an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c9f8-104">Selles teemas kirjeldatakse, kuidas luua Exceli töövihikut, et saaksite Microsoft Dynamics 365 Commerce'is jaemüügikandeid redigeerida.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-104">This topic describes how to create an Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5c9f8-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="5c9f8-105">Overview</span></span>

<span data-ttu-id="5c9f8-106">Saadaval on eelmääratletud Exceli mall, mida kliendid saavad avada süsteemi eri osadest ning kasutada jaemüügikannete redigeerimiseks ja auditeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-106">There is a predefined Excel template that customers can access from different parts of the system and use to edit and audit retail transactions.</span></span> <span data-ttu-id="5c9f8-107">Kuid kliendid saavad selleks otstarbeks luua ka kohandatud Exceli töövihiku.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-107">However, customers can also create a custom Excel workbook for this purpose.</span></span>

## <a name="create-and-configure-an-excel-workbook"></a><span data-ttu-id="5c9f8-108">Exceli töövihiku loomine ja konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="5c9f8-108">Create and configure an Excel workbook</span></span>

<span data-ttu-id="5c9f8-109">Jaemüügikannete redigeerimiseks Exceli töövihiku loomiseks ja konfigureerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-109">To create and configure an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="5c9f8-110">Avage Excel ja looge tühi töövihik.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-110">Open Excel, and create a blank workbook.</span></span>
1. <span data-ttu-id="5c9f8-111">Valige vahekaardil **Lisamine** suvand **Minu lisandmoodulid**.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-111">On the **Insert** tab, select **My add-ins**.</span></span>
1. <span data-ttu-id="5c9f8-112">Valige parempoolsel paanil link **Lisa serveriteave**.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-112">In the right pane, select the **Add server information** link.</span></span>
1. <span data-ttu-id="5c9f8-113">Sisestage serveri URL ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-113">Enter the server URL, and then select **OK**.</span></span>
1. <span data-ttu-id="5c9f8-114">Kui kuvatakse tõrketeade „Ühtegi apleti registreeringut ei leitud“, toimige probleemi lahendamiseks järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-114">If you receive a "No applet registrations found" error message, follow these steps to resolve the issue:</span></span>

    1. <span data-ttu-id="5c9f8-115">Avage Commerce'is **Süsteemihaldus \> Seadistus \> Office'i rakenduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-115">In Commerce, go to **System administration \> Setup \> Office app parameters**.</span></span>
    1. <span data-ttu-id="5c9f8-116">Valige kiirkaardil **Rakenduse parameetrid** suvand **Lähtesta rakenduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-116">On the **App parameters** FastTab, select **Initialize app parameters**.</span></span>
    1. <span data-ttu-id="5c9f8-117">Valige kinnituse teateaknas **OK**.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-117">In the confirmation message box, select **OK**.</span></span>
    1. <span data-ttu-id="5c9f8-118">Valige kiirkaardil **Registreeritud apletid** suvand **Lähtesta apleti registreering**.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-118">On the **Registered applets** FastTab, select **Initialize applet registration**.</span></span>
    1. <span data-ttu-id="5c9f8-119">Korrake vajadusel kolme eelmist sammu.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-119">Repeat the previous three steps as required.</span></span>

1. <span data-ttu-id="5c9f8-120">Valige **Kujundus** ja seejärel **Lisa tabel**.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-120">Select **Design**, and then select **Add table**.</span></span>
1. <span data-ttu-id="5c9f8-121">Valige muudetavate andmete alusel üksused, mis tuleb redigeerimiseks Exceli töövihikusse lisada.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-121">Based on the data that has to be modified, select the entities that must be added to the Excel workbook for editing.</span></span> <span data-ttu-id="5c9f8-122">Kasutage viitena järgmist tabelit.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-122">Use the following table as a reference.</span></span>

    | <span data-ttu-id="5c9f8-123">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="5c9f8-123">Transaction type</span></span> | <span data-ttu-id="5c9f8-124">Kasutatavad andmeüksused</span><span class="sxs-lookup"><span data-stu-id="5c9f8-124">Data entities to use</span></span> |
    |------------------|----------------------|
    | <span data-ttu-id="5c9f8-125">Selvehulgimüügikanded, veebitellimused, asünkroonsed klienditellimused, asünkroonsed kliendihinnapakkumised</span><span class="sxs-lookup"><span data-stu-id="5c9f8-125">Cash and carry transactions, Online orders, Async customer orders, Async customer quotes</span></span> | <span data-ttu-id="5c9f8-126">Kanne (auditeeritav), müügikanne (auditeeritav), maksekanded (auditeeritav), maksukanded (auditeeritav), allahindluse kanded (auditeeritav), tasukanded (auditeeritav)</span><span class="sxs-lookup"><span data-stu-id="5c9f8-126">Transaction (auditable), Sales transaction (auditable), Payment transactions (auditable), Tax transactions (auditable), Discount transactions (auditable), Charge transactions (auditable)</span></span> |
    | <span data-ttu-id="5c9f8-127">Raha hoiustamine panka</span><span class="sxs-lookup"><span data-stu-id="5c9f8-127">Bank drop</span></span> | <span data-ttu-id="5c9f8-128">Kanne (auditeeritav), panka hoiustatud maksevahendi kanded (auditeeritav)</span><span class="sxs-lookup"><span data-stu-id="5c9f8-128">Transaction (auditable), Banked tender transactions (auditable)</span></span> |
    | <span data-ttu-id="5c9f8-129">Seifi viidav raha</span><span class="sxs-lookup"><span data-stu-id="5c9f8-129">Safe drop</span></span> | <span data-ttu-id="5c9f8-130">Kanne (auditeeritav), seifi hoiustatud maksevahendi kanded (auditeeritav)</span><span class="sxs-lookup"><span data-stu-id="5c9f8-130">Transaction (auditable), Safe tender transactions (auditable)</span></span> |
    | <span data-ttu-id="5c9f8-131">Päevakassa</span><span class="sxs-lookup"><span data-stu-id="5c9f8-131">Tender declaration</span></span> | <span data-ttu-id="5c9f8-132">Kanne (auditeeritav), päevakassakanded (auditeeritav)</span><span class="sxs-lookup"><span data-stu-id="5c9f8-132">Transaction (auditable), Tender declaration transactions (auditable)</span></span> |
    | <span data-ttu-id="5c9f8-133">Tulu, kulu</span><span class="sxs-lookup"><span data-stu-id="5c9f8-133">Income, Expense</span></span> | <span data-ttu-id="5c9f8-134">Kanne (auditeeritav), tulu-/kulukanded (auditeeritav), maksetehingud (auditeeritav)</span><span class="sxs-lookup"><span data-stu-id="5c9f8-134">Transaction (auditable), Income/Expense transactions (auditable), Payment transactions (auditable)</span></span> |
    | <span data-ttu-id="5c9f8-135">Algsumma deklareerimine, maksevahendi eemaldamine, sularaha sissemakse, maksevahendi muutmine, arve maksmine, kliendi deposiit</span><span class="sxs-lookup"><span data-stu-id="5c9f8-135">Declare starting amount, Tender removal, Float entry, Change tender, Invoice payment, Customer deposit</span></span> | <span data-ttu-id="5c9f8-136">Kanne (auditeeritav), maksekanded (auditeeritav)</span><span class="sxs-lookup"><span data-stu-id="5c9f8-136">Transaction (auditable), Payment transactions (auditable)</span></span> |

    > [!NOTE]
    > <span data-ttu-id="5c9f8-137">Oluline on lisada igasse Exceli töövihikusse ainult üks andmeüksus.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-137">It's important that you add only one data entity to each Excel workbook.</span></span> <span data-ttu-id="5c9f8-138">Lisaks tuleb asjaomasesse töövihikusse lisada kõik võtmesümboliga tähistatud väljad.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-138">Additionally, all fields that are marked by a key symbol must be added to the relevant workbook.</span></span>

1. <span data-ttu-id="5c9f8-139">Pärast töövihiku konfigureerimist rakendage nõutavad filtrid.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-139">After the workbook is configured, apply the required filters.</span></span> <span data-ttu-id="5c9f8-140">Veenduge, et rakendaksite samu filtreid kõigi faili töölehtede korral.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-140">Be sure to apply the same filters to all the worksheets in the file.</span></span> <span data-ttu-id="5c9f8-141">Ärge laadige Exceli faili väga suuri andmehulkasid.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-141">Avoid loading very large amounts of data into the Excel file.</span></span> <span data-ttu-id="5c9f8-142">Muidu võib see jõudlust mõjutada ning Excel ja teie süsteem võivad aeglasemaks muutuda.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-142">Otherwise, performance might be affected, and Excel and your system might slow down.</span></span> <span data-ttu-id="5c9f8-143">Soovitame kasutada failis alati filtrit „Ettevõte“ ning kas filtrit „Väljavõtte number“ või filtrit „Kande number“.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-143">We recommend that you always use "Company" and either "Statement Number" or "Transaction Number" as filters for your file.</span></span>
1. <span data-ttu-id="5c9f8-144">Kui filtrid on konfigureeritud, valige andmete laadimiseks **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-144">After the filters are configured, select **Refresh** to load the data.</span></span>
1. <span data-ttu-id="5c9f8-145">Redigeerige vajalikke andmeid ja seejärel avaldage need.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-145">Edit the required data, and then publish it.</span></span> <span data-ttu-id="5c9f8-146">Kui nupp **Avalda** pole saadaval, ei lisatud Exceli töövihikusse tõenäoliselt olulisi välju.</span><span class="sxs-lookup"><span data-stu-id="5c9f8-146">If the **Publish** button is unavailable, some key fields probably weren't added to the Excel workbook.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5c9f8-147">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="5c9f8-147">Additional resources</span></span>

[<span data-ttu-id="5c9f8-148">Selvehulgimüügi- ja kassahalduskannete redigeerimine ning auditeerimine</span><span class="sxs-lookup"><span data-stu-id="5c9f8-148">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="5c9f8-149">Veebitellimuse ja asünkroonse klienditellimuse kannete redigeerimine ning auditeerimine</span><span class="sxs-lookup"><span data-stu-id="5c9f8-149">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="5c9f8-150">Jaemüügikannete finantsdimensioonide redigeerimine</span><span class="sxs-lookup"><span data-stu-id="5c9f8-150">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="5c9f8-151">Väljade lisamine Exceli töövihikusse jaemüügikannete redigeerimiseks</span><span class="sxs-lookup"><span data-stu-id="5c9f8-151">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]