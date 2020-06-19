---
title: Varude saadavuse topeltkirjutus
description: See teema annab teavet varude saadavuse topeltkirjutamise kontrollimise kohta.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
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
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426978"
---
# <a name="inventory-availability"></a><span data-ttu-id="bf4df-103">Varude saadavus</span><span class="sxs-lookup"><span data-stu-id="bf4df-103">Inventory availability</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="bf4df-104">Varude saadavuse abil saate kontrollida oma varusid enne, kui lisate Dynamics 365 mudelipõhistes rakendustes uue toote vormidele **Päringud**, **Tellimused** või **Arved**.</span><span class="sxs-lookup"><span data-stu-id="bf4df-104">Using inventory availability, you can check your inventory before you add a product into the **Quotes**, **Orders**, or **Invoices** forms in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="bf4df-105">Näiteks on varude kontrollimine ja täitmiskuupäeva kindlaks määramine [potentsiaalne klient-raha](dual-write-prospect-to-cash.md) protsessi raames oluline ülesanne.</span><span class="sxs-lookup"><span data-stu-id="bf4df-105">For example, checking inventory and determining a fulfullment date is a key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span> <span data-ttu-id="bf4df-106">Kui teil puuduvad piisavad varud, siis saate hinnata eeldatava varude vastuvõtu ja väljastamise alusel sissetulekuaega.</span><span class="sxs-lookup"><span data-stu-id="bf4df-106">If you don't have enough inventory, you can estimate a delivery date based on projected inventory receipts and issues.</span></span> <span data-ttu-id="bf4df-107">Samuti saate kontrollida toote saadaval lubamiseks teavet, kus leiate saadaval lubamiseks koguse eelmääratletud ajapiiri raames.</span><span class="sxs-lookup"><span data-stu-id="bf4df-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the pre-defined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="bf4df-108">Vaba kaubavaru</span><span class="sxs-lookup"><span data-stu-id="bf4df-108">On-hand Inventory</span></span> 

<span data-ttu-id="bf4df-109">Rakenduses Dynamics 365 Sales on vormide **Päringud**, **Tellimused** või **Arved** päisesse lisatud uus nupp **Vaba kaubavaru**.</span><span class="sxs-lookup"><span data-stu-id="bf4df-109">In the header of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **On-hand Inventory** is added.</span></span> <span data-ttu-id="bf4df-110">Nupule klõpsates ilmub dialoogiaken ning te saate määratleda ettevõtte ja toote, mille kohta soovite kontrollida vaba kaubavaru.</span><span class="sxs-lookup"><span data-stu-id="bf4df-110">When you click the button, a dialog box appears and you can specify the company and the product for which you want to check the on-hand inventory.</span></span> <span data-ttu-id="bf4df-111">See hangib rakendusest Dynamics 365 Supply Chain Management varude teabe ja kuvab sama teabe, mis sisaldub [Vabas kaubavarus](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="bf4df-111">It returns the inventory information from Dynamics 365 Supply Chain Management, and shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span> <span data-ttu-id="bf4df-112">Teave sisaldab järgmisi koguseid.</span><span class="sxs-lookup"><span data-stu-id="bf4df-112">The information includes these quantities:</span></span>

- <span data-ttu-id="bf4df-113">**Laos olev kogus**</span><span class="sxs-lookup"><span data-stu-id="bf4df-113">**On-hand Quantity**</span></span>
- <span data-ttu-id="bf4df-114">**Reserveeritud laos olev kogus**</span><span class="sxs-lookup"><span data-stu-id="bf4df-114">**Reserved On-hand Quantity**</span></span>
- <span data-ttu-id="bf4df-115">**Saadaolev laos olev kogus**</span><span class="sxs-lookup"><span data-stu-id="bf4df-115">**Available On-hand Quantity**</span></span>
- <span data-ttu-id="bf4df-116">**Tellitud kogus**</span><span class="sxs-lookup"><span data-stu-id="bf4df-116">**Orderd Quantity**</span></span>
- <span data-ttu-id="bf4df-117">**Tellimisel kogus**</span><span class="sxs-lookup"><span data-stu-id="bf4df-117">**On-order Quantity**</span></span>
- <span data-ttu-id="bf4df-118">**Reserveeritud tellitud kogus**</span><span class="sxs-lookup"><span data-stu-id="bf4df-118">**Reserved Ordered Quantity**</span></span>
- <span data-ttu-id="bf4df-119">**Saadaolev kogus kokku**</span><span class="sxs-lookup"><span data-stu-id="bf4df-119">**Total Available Quantity**</span></span>

## <a name="atp-information"></a><span data-ttu-id="bf4df-120">ATP teave</span><span class="sxs-lookup"><span data-stu-id="bf4df-120">ATP information</span></span>

<span data-ttu-id="bf4df-121">Rakenduses Dynamics 365 Sales on vormide **Päringud**, **Tellimused** või **Arved** rea kaupadele lisatud uus nupp **Saadaval lubamiseks teave**.</span><span class="sxs-lookup"><span data-stu-id="bf4df-121">On line items of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **ATP Information** is added.</span></span> <span data-ttu-id="bf4df-122">Nupule klõpsates ilmub dialoogiaken ning te saate määratleda ettevõtte, varude saidi, varude lao ja tellimuse koguse.</span><span class="sxs-lookup"><span data-stu-id="bf4df-122">When you click the button, a dialog box appears and you can specify the company, product, inventory Site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="bf4df-123">See hangib rakendusest Supply Chain Management **saadaval lubamiseks teabe** ja kuvab jaotises [Toote lubamine](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) kirjeldatud sätted.</span><span class="sxs-lookup"><span data-stu-id="bf4df-123">It returns the **ATP Information** from Supply Chain Management and shows the settings descrbed in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span> <span data-ttu-id="bf4df-124">Teabe hulka kuulub **Saadaval lubamiseks kogus**, **Sissetulekukogus**, **Väljastatav kogus** ja **Vaba kogus**.</span><span class="sxs-lookup"><span data-stu-id="bf4df-124">The information includes **ATP quantity**, **Receipt quantity**, **Issue quantity**, and **On-hand quantity**.</span></span>
