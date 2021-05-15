---
title: Dynamics 365 Commerce’i hinnakujunduse mootori kasutamine koos rakendusega Dynamics 365 Sales
description: Selles teemas kirjeldatakse, kuidas kasutada Microsoft Dynamics 365 Commerce hinnakujunduse mootorit rakenduses Dynamics 365 Sales müügipakkumiste loomiseks.
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: fa93b1262049d80148ff23b3d7223ec0f6c2fe68
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941162"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a><span data-ttu-id="d8df1-103">Dynamics 365 Commerce’i hinnakujunduse mootori kasutamine koos rakendusega Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="d8df1-103">Use the Dynamics 365 Commerce pricing engine with Dynamics 365 Sales</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d8df1-104">Selles teemas kirjeldatakse, kuidas kasutada Microsoft Dynamics 365 Commerce hinnakujunduse mootorit rakenduses Dynamics 365 Sales müügipakkumiste loomiseks.</span><span class="sxs-lookup"><span data-stu-id="d8df1-104">This topic describes how to use the Microsoft Dynamics 365 Commerce pricing engine to create sales quotations in Dynamics 365 Sales.</span></span>

<span data-ttu-id="d8df1-105">Dynamics 365 Commerce’i hinnakujunduse mootor toetab enamikke ettevõtja ja tarbija vahelisi (B2C) hinnakujunduse stsenaariume, nagu kaupluse tasemel hinnakujundus, alluvusepõhine ja püsikliendipõhine hinnakujundus, sobitamise allahindlused, koguse allahindlused ja läveallahindlused.</span><span class="sxs-lookup"><span data-stu-id="d8df1-105">The Dynamics 365 Commerce pricing engine supports most business-to-consumer (B2C) pricing scenarios, such as store-level pricing, affiliation-based and loyalty-based pricing, mix-and-match discounts, quantity discounts, and threshold discounts.</span></span> <span data-ttu-id="d8df1-106">Hinnakujunduse mootor kasutab keerukaid reegleid antud pakkumisele või tellimusele parima hinna määramiseks.</span><span class="sxs-lookup"><span data-stu-id="d8df1-106">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span>

<span data-ttu-id="d8df1-107">Kui kasutate [topeltkirjutamist](./dual-write-overview.md), on teil oma hinnakujunduse vajaduste jaoks kolm võimalust.</span><span class="sxs-lookup"><span data-stu-id="d8df1-107">When you use [dual-write](./dual-write-overview.md), you have three options for your pricing needs.</span></span> <span data-ttu-id="d8df1-108">Saate kasutada staatilist hinnakujundust, mis pärineb rakenduse Dynamics 365 Sales hindade loendist, rakenduse Dynamics 365 Supply Chain Management hinnakujunduse mootorist või rakenduse Dynamics 365 Commerce hinnakujunduse mootorist.</span><span class="sxs-lookup"><span data-stu-id="d8df1-108">You can use the static pricing that comes from the price list in Dynamics 365 Sales, the pricing engine in Dynamics 365 Supply Chain Management, or the pricing engine in Dynamics 365 Commerce.</span></span> <span data-ttu-id="d8df1-109">Nende valikute hulgas sobib Commerce’i hinnakujunduse mootor kõige paremini B2C stsenaariumiga.</span><span class="sxs-lookup"><span data-stu-id="d8df1-109">Among these options, the Commerce pricing engine is best suited to B2C scenarios.</span></span>

## <a name="use-the-commerce-pricing-engine-in-sales"></a><span data-ttu-id="d8df1-110">Salesis Commerce’i hinnakujunduse mootori kasutamine</span><span class="sxs-lookup"><span data-stu-id="d8df1-110">Use the Commerce pricing engine in Sales</span></span>

> [!NOTE]
> <span data-ttu-id="d8df1-111">Praegu saab Commerce’i hinnakujunduse mootorit kasutada ainult Salesis pakkumise loomisel.</span><span class="sxs-lookup"><span data-stu-id="d8df1-111">Currently, the Commerce pricing engine can be used only for quotation creation in the Sales.</span></span> <span data-ttu-id="d8df1-112">Müügitellimuse integratsioon Commerce’i hinnakujunduse mootoriga pole veel saadaval.</span><span class="sxs-lookup"><span data-stu-id="d8df1-112">Sales order integration with the Commerce pricing engine isn't yet available.</span></span>

<span data-ttu-id="d8df1-113">Kui kasutajad teevad Salesis müügipakkumisega algust, kopeerib topeltkirjutamise raamistik hinnapakkumise üksikasjad Commerce’i.</span><span class="sxs-lookup"><span data-stu-id="d8df1-113">When users initiate a quotation in Sales, the dual-write framework copies the quotation details to Commerce.</span></span> <span data-ttu-id="d8df1-114">Mis tahes olemasoleva pakkumise ridade muudatused või mis tahes uuena lisatud pakkumise read kopeeritakse Salesist Commerce’i.</span><span class="sxs-lookup"><span data-stu-id="d8df1-114">Any changes to existing quotation lines or any newly added quotation lines in Sales are copied to Commerce.</span></span> <span data-ttu-id="d8df1-115">Kui kasutajad soovivad kasutada hinnapakkumise hinna määramiseks Commerce’i hinnakujunduse mootorit, saavad nad pakkumise hindade värskendamiseks valida suvandi **Hinnapakkumine**, mis põhinev Commerce’i hinnakujunduse mootoril.</span><span class="sxs-lookup"><span data-stu-id="d8df1-115">When users want to use the Commerce pricing engine to price the quotation, they can select **Price quote** to update the prices of the quotation, based on the Commerce pricing engine.</span></span> <span data-ttu-id="d8df1-116">Hinnad uuendatakse seejärel automaatselt nii Salesis kui ka Commerce’is.</span><span class="sxs-lookup"><span data-stu-id="d8df1-116">Prices are then automatically updated in both Sales and Commerce.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d8df1-117">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="d8df1-117">Prerequisites</span></span>

- <span data-ttu-id="d8df1-118">Enne kui saate kasutada Salesis Commerce’i hinnakujunduse mootorit, peate järgima samme teemas [Potentsiaalne kliendist rahaks kaksikkirjutamises](./dual-write-prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="d8df1-118">Before you can use the Commerce pricing engine in Sales, you must follow the steps in [Prospect-to-cash in dual-write](./dual-write-prospect-to-cash.md).</span></span>
- <span data-ttu-id="d8df1-119">Peate käsitsi sisestamiseks hindamise kaubandusleppe välja lülitama, järgides järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="d8df1-119">You must turn off trade agreement evaluation for manual entry by following these steps:</span></span>

    1. <span data-ttu-id="d8df1-120">Avage Commerce’i keskkonnas jaotis **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="d8df1-120">In your Commerce environment, go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    1. <span data-ttu-id="d8df1-121">Tühjendage vahekaardil **Hinnad** kiirkaardil **Kaubanduskokkuleppe hindamine** märkeruut **Käsitsi sisestamine**.</span><span class="sxs-lookup"><span data-stu-id="d8df1-121">On the **Prices** tab, on the **Trade agreement evaluation** FastTab, clear the **Manual entry** check box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d8df1-122">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="d8df1-122">Additional resources</span></span>

[<span data-ttu-id="d8df1-123">Potentsiaalne klient-raha ja kaksikkirjutamine</span><span class="sxs-lookup"><span data-stu-id="d8df1-123">Prospect-to-cash in dual-write</span></span>](./dual-write-prospect-to-cash.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]