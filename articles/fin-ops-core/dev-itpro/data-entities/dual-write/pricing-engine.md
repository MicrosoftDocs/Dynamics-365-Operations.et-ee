---
title: Nõudmisel sünkroonimine Dynamics 365 Supply Chain Managementi hinnakujunduse mootoriga
description: Selles teemas kirjeldatakse, kuidas kasutada Dynamics 365 Salesi Microsoft Dynamics 365 Supply Chain Managementi hinnakujunduse mootorit.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: ef4465144155130087b078f9f96911df38b62c41
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173173"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a><span data-ttu-id="51e17-103">Nõudmisel sünkroonimine Dynamics 365 Supply Chain Managementi hinnakujunduse mootoriga</span><span class="sxs-lookup"><span data-stu-id="51e17-103">Sync with the Dynamics 365 Supply Chain Management pricing engine on demand</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="51e17-104">Microsoft Dynamics 365 Supply Chain Management sisaldab hinnakujunduse mootorit, mis tegeleb kaubanduslepete, hinnakirjade, püsikliendi rogrammide, kampaaniate ja allahindlustega.</span><span class="sxs-lookup"><span data-stu-id="51e17-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="51e17-105">Hinnakujunduse mootor kasutab keerukaid reegleid antud pakkumisele või tellimusele parima hinna määramiseks.</span><span class="sxs-lookup"><span data-stu-id="51e17-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="51e17-106">Kui kasutate topeltkirjutust, kasutate Dynamics 365 Supply Chain Managementi staatilist hinnakujundust või hinnakujunduse mootorit Dynamics 365 Salesi hinnapakkumise ja tellimuse lehtedel.</span><span class="sxs-lookup"><span data-stu-id="51e17-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="51e17-107">Supply Chain Managementi hinnakujunduse mootori kasutamine Salesis</span><span class="sxs-lookup"><span data-stu-id="51e17-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="51e17-108">Avage Salesis **Müük \> Tellimused**.</span><span class="sxs-lookup"><span data-stu-id="51e17-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="51e17-109">Uue tellimuse loomiseks või olemasolema valimiseks tehke loendis **Minu tellimused** valik **Uus**.</span><span class="sxs-lookup"><span data-stu-id="51e17-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="51e17-110">Uue tellimusrea lisamine.</span><span class="sxs-lookup"><span data-stu-id="51e17-110">Add a new order line.</span></span>
4. <span data-ttu-id="51e17-111">Kui loote uut tellimust, valige tegevuse paanil suvand **Hinnajärjestus**.</span><span class="sxs-lookup"><span data-stu-id="51e17-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="51e17-112">Kui värskendate olemasolevat tellimust, valige tegevuse paanil suvand **Uuestiarvutamine**.</span><span class="sxs-lookup"><span data-stu-id="51e17-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="51e17-113">Järgmised väljad täidetakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="51e17-113">The following fields are automatically filled in:</span></span>

    + <span data-ttu-id="51e17-114">Üksikasjalik summa</span><span class="sxs-lookup"><span data-stu-id="51e17-114">Detail Amount</span></span>
    + <span data-ttu-id="51e17-115">Allahindlus %</span><span class="sxs-lookup"><span data-stu-id="51e17-115">Discount %</span></span>
    + <span data-ttu-id="51e17-116">Allahindlus</span><span class="sxs-lookup"><span data-stu-id="51e17-116">Discount</span></span>
    + <span data-ttu-id="51e17-117">Transpordieelne summa</span><span class="sxs-lookup"><span data-stu-id="51e17-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="51e17-118">Transpord summa</span><span class="sxs-lookup"><span data-stu-id="51e17-118">Freight Amount</span></span>
    + <span data-ttu-id="51e17-119">Kogumaks</span><span class="sxs-lookup"><span data-stu-id="51e17-119">Total Tax</span></span>
    + <span data-ttu-id="51e17-120">Kogusumma</span><span class="sxs-lookup"><span data-stu-id="51e17-120">Total Amount</span></span>

## <a name="how-it-works"></a><span data-ttu-id="51e17-121">Toimimisviis</span><span class="sxs-lookup"><span data-stu-id="51e17-121">How it works</span></span>

<span data-ttu-id="51e17-122">Kui teete Salesis valiku **Hinnajärjestus**, kutsutakse seostatud müügitellimuse jaoks Supply Chain Managementi vahekaardil **Müügitellimus \> Kuva** funktsioon **Kogusummad**.</span><span class="sxs-lookup"><span data-stu-id="51e17-122">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="51e17-123">Tellimuse kogusumma väärtusi kasutatakse Salesis vastavate Supply Chain Managementi väljade täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="51e17-123">The values in the order total in Sales are used to fill in the corresponding fields in Supply Chain Management.</span></span>

<span data-ttu-id="51e17-124">Kui Supply Chain Managementis avutatakse müügitellimuse kogusumma, hindab arvutus kliendi ja müügitellimuse jaoks loetletud toodete kehtivaid kaubandusleppeid ja müügilepinguid.</span><span class="sxs-lookup"><span data-stu-id="51e17-124">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="51e17-125">Seda teavet kasutatakse kogusummade arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="51e17-125">This information is used to calculate the totals.</span></span> <span data-ttu-id="51e17-126">Kui valitud on **Hinnajärjestus**, kajastab Sales automaatselt kõiki Supply Chain Managementis tehtud seadistusi.</span><span class="sxs-lookup"><span data-stu-id="51e17-126">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="51e17-127">Kitsendused</span><span class="sxs-lookup"><span data-stu-id="51e17-127">Limitations</span></span>

<span data-ttu-id="51e17-128">Kui Salesi väljad on täidetud, kehtivad järgmised piirangud.</span><span class="sxs-lookup"><span data-stu-id="51e17-128">When the fields in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="51e17-129">Supply Chain Managementi tasude ja tasu eraldamise seadistusi ei kopeerita Salesi.</span><span class="sxs-lookup"><span data-stu-id="51e17-129">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="51e17-130">Hinnakujundus ei arvesta Supply Chain Managementi müügitellimuse rea lehe väljal **Jaemüügi kanal** määratletud jaemüügi erihinnakujundust.</span><span class="sxs-lookup"><span data-stu-id="51e17-130">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** field on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="51e17-131">Supply Chain Managementi jaotises **Kaubandushüvitise haldus** määratletud allahindlusi ei arvestata.</span><span class="sxs-lookup"><span data-stu-id="51e17-131">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>
