---
title: Teekonna oleku seadistamine
description: Selles teemas kirjeldatakse, kuidas kehtestada olekuväärtusi, mida kasutajad saavad teekondadele määrata.
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: b7180cc9ab2d13f2260635d717adb7aab2177ab9
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500882"
---
# <a name="voyage-status-setup"></a><span data-ttu-id="c3cb7-103">Teekonna oleku seadistamine</span><span class="sxs-lookup"><span data-stu-id="c3cb7-103">Voyage status setup</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="c3cb7-104">Lehel **Teekonna olek** saate koostada komplekti olekuväärtustest, mida kasutajad saavad teekondadele määrata.</span><span class="sxs-lookup"><span data-stu-id="c3cb7-104">On the **Voyage statuses** page, you establish the set of status values that users can assign to voyages.</span></span> <span data-ttu-id="c3cb7-105">Kasutajad saavad määrata teekonna olekuväärtusi teekonna kõigile tasemetele: teekond, saatmiskonteiner, foolio, ostutellimus ja kaup (osturead ja üleviimistellimuse read).</span><span class="sxs-lookup"><span data-stu-id="c3cb7-105">Users can assign voyage status values to all levels of a voyage: voyage, shipping container, folio, purchase order, and item (purchase lines and transfer order lines).</span></span> <span data-ttu-id="c3cb7-106">Neid kasutatakse kahel otstarbel.</span><span class="sxs-lookup"><span data-stu-id="c3cb7-106">They are used for two purposes:</span></span>

- <span data-ttu-id="c3cb7-107">Saate teavitada kasutajat teekonna, saatmiskonteineri, foolio, ostutellimuse või kauba olekust (osturead ja üleviimistellimuse read).</span><span class="sxs-lookup"><span data-stu-id="c3cb7-107">Inform the user about the status of the voyage, shipping container, folio, purchase order, or item (purchase lines and transfer order lines).</span></span>
- <span data-ttu-id="c3cb7-108">Saate piirata kuluala kasutamist, tõkestades muutmise või kustutamise.</span><span class="sxs-lookup"><span data-stu-id="c3cb7-108">Limit the use of the cost area by preventing modification or deletion.</span></span>

<span data-ttu-id="c3cb7-109">Teekonna olekute seadistamiseks avage **Väljalaadimiskulu \> Seadistamine \> Teekonna olekud**.</span><span class="sxs-lookup"><span data-stu-id="c3cb7-109">To set up your voyage statuses, go to **Landed cost \> Setup \> Voyage statuses**.</span></span> <span data-ttu-id="c3cb7-110">Seal saate toimingupaani nuppude abil olekuid lisada, eemaldada ja redigeerida.</span><span class="sxs-lookup"><span data-stu-id="c3cb7-110">There, you can add, remove, and edit statuses by using the buttons on the Action Pane.</span></span>

<span data-ttu-id="c3cb7-111">Igal kulualal on oma teekonnaolekute komplekt ja hierarhia.</span><span class="sxs-lookup"><span data-stu-id="c3cb7-111">Each cost area has its own set and hierarchy of voyage statuses.</span></span> <span data-ttu-id="c3cb7-112">Seetõttu tuleb lehel **Teekonna olekud** väljal **Kuluala** esmalt valida kuluala, mida soovite vaadata või mille jaoks teekonnaolekuid luua.</span><span class="sxs-lookup"><span data-stu-id="c3cb7-112">Therefore, on the **Voyage statuses** page, in the **Cost area** field, you must first select the cost area that you want to view or create voyage statuses for.</span></span> <span data-ttu-id="c3cb7-113">Seejärel määrake iga teekonna oleku jaoks vastavalt vajadusele väljad, mida kirjeldatakse järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="c3cb7-113">Then, for each voyage status, set the fields that are described in the following table, as required.</span></span> <span data-ttu-id="c3cb7-114">Arvestage, et teekonna olekut võivad automaatselt muuta ka süsteemisündmused, nt jälgimise juhtimiskeskuse abil kehtestatud reeglid.</span><span class="sxs-lookup"><span data-stu-id="c3cb7-114">Note that the status of a voyage can also be automatically changed by system events, such as rules that have been established by using the tracking control center.</span></span>

| <span data-ttu-id="c3cb7-115">Field</span><span class="sxs-lookup"><span data-stu-id="c3cb7-115">Field</span></span> | <span data-ttu-id="c3cb7-116">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c3cb7-116">Description</span></span> |
|---|---|
| <span data-ttu-id="c3cb7-117">Reisi olek</span><span class="sxs-lookup"><span data-stu-id="c3cb7-117">Voyage status</span></span> | <span data-ttu-id="c3cb7-118">Sisestage teekonna oleku nimi.</span><span class="sxs-lookup"><span data-stu-id="c3cb7-118">Enter the name of the voyage status.</span></span> |
| <span data-ttu-id="c3cb7-119">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c3cb7-119">Description</span></span> | <span data-ttu-id="c3cb7-120">Sisestage teekonna oleku kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="c3cb7-120">Enter a description of the voyage status.</span></span> |
| <span data-ttu-id="c3cb7-121">Muuda</span><span class="sxs-lookup"><span data-stu-id="c3cb7-121">Modify</span></span> | <span data-ttu-id="c3cb7-122">Valige see märkeruut, kui kasutajatel on lubatud selle olekuga teekondi muuta.</span><span class="sxs-lookup"><span data-stu-id="c3cb7-122">Select this check box if users are allowed to modify voyages that have this status.</span></span> |
| <span data-ttu-id="c3cb7-123">Kustutamine</span><span class="sxs-lookup"><span data-stu-id="c3cb7-123">Delete</span></span> | <span data-ttu-id="c3cb7-124">Valige see märkeruut, kui kasutajatel on lubatud selle olekuga teekondi kustutada.</span><span class="sxs-lookup"><span data-stu-id="c3cb7-124">Select this check box if users are allowed to delete voyages that have this status.</span></span> |
| <span data-ttu-id="c3cb7-125">Kohustuslik</span><span class="sxs-lookup"><span data-stu-id="c3cb7-125">Mandatory</span></span> | <span data-ttu-id="c3cb7-126">Valige see märkeruut, et muuta teekonna olek kohustuslikuks, et seda ei saaks vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="c3cb7-126">Select this check box to make the voyage status mandatory, so that it can't be skipped.</span></span> |
| <span data-ttu-id="c3cb7-127">Ema</span><span class="sxs-lookup"><span data-stu-id="c3cb7-127">Parent</span></span> | <span data-ttu-id="c3cb7-128">Selle välja abil saate kehtestada olekuväärtuste hierarhia.</span><span class="sxs-lookup"><span data-stu-id="c3cb7-128">Use this field to establish a hierarchy among the status values.</span></span> <span data-ttu-id="c3cb7-129">Teekonna olekuid saab muuta (kas käsitsi või automaatselt) ainult hierarhias allapoole, emaolekust ühte selle tütarolekusse.</span><span class="sxs-lookup"><span data-stu-id="c3cb7-129">Voyage statuses can be changed (either manually or automatically) only downward in the hierarchy, from a parent status to one of its child statuses.</span></span>

> [!NOTE]
> <span data-ttu-id="c3cb7-130">Seadistada tuleb ainult need konkreetsed teekonna olekud, mida teie organisatsioon kasutab.</span><span class="sxs-lookup"><span data-stu-id="c3cb7-130">You have to set up only the specific voyage statuses that your organization uses.</span></span> <span data-ttu-id="c3cb7-131">Tüüpilisteks teekonna olekuteks on *Kinnitatud*, *Transiidis olevad kaubad*, *Vastuvõetud*, *Kuluarvestuseks valmis* ja *Arvestatud kulu*.</span><span class="sxs-lookup"><span data-stu-id="c3cb7-131">Typical voyage statuses include *Confirmed*, *Goods in transit*, *Received*, *Ready for costing*, and *Costed*.</span></span> <span data-ttu-id="c3cb7-132">Kuid võib olla ka teisi olekuid.</span><span class="sxs-lookup"><span data-stu-id="c3cb7-132">However, other statuses might be present.</span></span>
