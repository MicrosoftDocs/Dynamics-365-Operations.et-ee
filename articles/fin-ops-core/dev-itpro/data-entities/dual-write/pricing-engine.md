---
title: Nõudmisel sünkroonimine Supply Chain Managementi hinnakujunduse mootoriga
description: Selles teemas kirjeldatakse, kuidas kasutada Dynamics 365 Salesi Microsoft Dynamics 365 Supply Chain Managementi hinnakujunduse mootorit.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: e2067e83d3f0c98e986873b8eaf1b817de912c0f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570136"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a><span data-ttu-id="5e78a-103">Nõudmisel sünkroonimine Supply Chain Managementi hinnakujunduse mootoriga</span><span class="sxs-lookup"><span data-stu-id="5e78a-103">Sync on-demand with the Supply Chain Management pricing engine</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="5e78a-104">Microsoft Dynamics 365 Supply Chain Management sisaldab hinnakujunduse mootorit, mis tegeleb kaubanduslepete, hinnakirjade, püsikliendi rogrammide, kampaaniate ja allahindlustega.</span><span class="sxs-lookup"><span data-stu-id="5e78a-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="5e78a-105">Hinnakujunduse mootor kasutab keerukaid reegleid antud pakkumisele või tellimusele parima hinna määramiseks.</span><span class="sxs-lookup"><span data-stu-id="5e78a-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="5e78a-106">Kui kasutate topeltkirjutust, kasutate Dynamics 365 Supply Chain Managementi staatilist hinnakujundust või hinnakujunduse mootorit Dynamics 365 Salesi hinnapakkumise ja tellimuse lehtedel.</span><span class="sxs-lookup"><span data-stu-id="5e78a-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="5e78a-107">Supply Chain Managementi hinnakujunduse mootori kasutamine Salesis</span><span class="sxs-lookup"><span data-stu-id="5e78a-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="5e78a-108">Avage Salesis **Müük \> Tellimused**.</span><span class="sxs-lookup"><span data-stu-id="5e78a-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="5e78a-109">Uue tellimuse loomiseks või olemasolema valimiseks tehke loendis **Minu tellimused** valik **Uus**.</span><span class="sxs-lookup"><span data-stu-id="5e78a-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="5e78a-110">Uue tellimusrea lisamine.</span><span class="sxs-lookup"><span data-stu-id="5e78a-110">Add a new order line.</span></span>
4. <span data-ttu-id="5e78a-111">Kui loote uut tellimust, valige tegevuse paanil suvand **Hinnajärjestus**.</span><span class="sxs-lookup"><span data-stu-id="5e78a-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="5e78a-112">Kui värskendate olemasolevat tellimust, valige tegevuse paanil suvand **Uuestiarvutamine**.</span><span class="sxs-lookup"><span data-stu-id="5e78a-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="5e78a-113">Järgmised veerud täidetakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="5e78a-113">The following columns are automatically filled in:</span></span>

    + <span data-ttu-id="5e78a-114">Üksikasjalik summa</span><span class="sxs-lookup"><span data-stu-id="5e78a-114">Detail Amount</span></span>
    + <span data-ttu-id="5e78a-115">Allahindlus %</span><span class="sxs-lookup"><span data-stu-id="5e78a-115">Discount %</span></span>
    + <span data-ttu-id="5e78a-116">Allahindlus</span><span class="sxs-lookup"><span data-stu-id="5e78a-116">Discount</span></span>
    + <span data-ttu-id="5e78a-117">Transpordieelne summa</span><span class="sxs-lookup"><span data-stu-id="5e78a-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="5e78a-118">Transpord summa</span><span class="sxs-lookup"><span data-stu-id="5e78a-118">Freight Amount</span></span>
    + <span data-ttu-id="5e78a-119">Kogumaks</span><span class="sxs-lookup"><span data-stu-id="5e78a-119">Total Tax</span></span>
    + <span data-ttu-id="5e78a-120">Kogusumma</span><span class="sxs-lookup"><span data-stu-id="5e78a-120">Total Amount</span></span>
    
5. <span data-ttu-id="5e78a-121">Et tagada, et süsteem võtab hinna arvutamisel arvesse kaubandusleppeid ja müügilepinguid, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="5e78a-121">To ensure that the system considers trade and sales agreements to calculate the price:</span></span>
    1. <span data-ttu-id="5e78a-122">Liikuge teenuses Supply Chain Management oma keskkonna juurde.</span><span class="sxs-lookup"><span data-stu-id="5e78a-122">Navigate to your Supply Chain Management environment.</span></span>
    2. <span data-ttu-id="5e78a-123">Navigeerige jaotisse **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="5e78a-123">Navigate to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    3. <span data-ttu-id="5e78a-124">Valige külgmisel navigeerimisribal vahekaart **Hinnad**.</span><span class="sxs-lookup"><span data-stu-id="5e78a-124">Select the **Prices** tab in the side navigation bar.</span></span>
    4. <span data-ttu-id="5e78a-125">Tühjendage kiirkaardil **Kaubandusleppe hindamine** ruut **Käsitsi sisestamine**.</span><span class="sxs-lookup"><span data-stu-id="5e78a-125">Under the **Trade agreement evaluation** fastab, uncheck the **Manual entry** option.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="5e78a-126">Toimimisviis</span><span class="sxs-lookup"><span data-stu-id="5e78a-126">How it works</span></span>

<span data-ttu-id="5e78a-127">Kui teete Salesis valiku **Hinnajärjestus**, kutsutakse seostatud müügitellimuse jaoks Supply Chain Managementi vahekaardil **Müügitellimus \> Kuva** funktsioon **Kogusummad**.</span><span class="sxs-lookup"><span data-stu-id="5e78a-127">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="5e78a-128">Tellimuse kogusumma väärtusi kasutatakse Salesis vastavate Supply Chain Managementi veergude täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="5e78a-128">The values in the order total in Sales are used to fill in the corresponding columns in Supply Chain Management.</span></span>

<span data-ttu-id="5e78a-129">Kui Supply Chain Managementis avutatakse müügitellimuse kogusumma, hindab arvutus kliendi ja müügitellimuse jaoks loetletud toodete kehtivaid kaubandusleppeid ja müügilepinguid.</span><span class="sxs-lookup"><span data-stu-id="5e78a-129">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="5e78a-130">Seda teavet kasutatakse kogusummade arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="5e78a-130">This information is used to calculate the totals.</span></span> <span data-ttu-id="5e78a-131">Kui valitud on **Hinnajärjestus**, kajastab Sales automaatselt kõiki Supply Chain Managementis tehtud seadistusi.</span><span class="sxs-lookup"><span data-stu-id="5e78a-131">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="5e78a-132">Kitsendused</span><span class="sxs-lookup"><span data-stu-id="5e78a-132">Limitations</span></span>

<span data-ttu-id="5e78a-133">Kui Salesi veerud on täidetud, kehtivad järgmised piirangud.</span><span class="sxs-lookup"><span data-stu-id="5e78a-133">When the columns in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="5e78a-134">Supply Chain Managementi tasude ja tasu eraldamise seadistusi ei kopeerita Salesi.</span><span class="sxs-lookup"><span data-stu-id="5e78a-134">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="5e78a-135">Hinnakujundus ei arvesta Supply Chain Managementi müügitellimuse rea lehe veerus **Jaemüügi kanal** määratletud jaemüügi erihinnakujundust.</span><span class="sxs-lookup"><span data-stu-id="5e78a-135">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** column on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="5e78a-136">Supply Chain Managementi jaotises **Kaubandushüvitise haldus** määratletud allahindlusi ei arvestata.</span><span class="sxs-lookup"><span data-stu-id="5e78a-136">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]