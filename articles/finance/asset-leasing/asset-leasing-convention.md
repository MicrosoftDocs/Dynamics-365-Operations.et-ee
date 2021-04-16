---
title: Vara rentimise reeglid
description: Selles teemas kirjeldatakse renditavate varade reegleid.
author: moaamer
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e6450438a6e8c594590df3cc4502895913f50d01
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842390"
---
# <a name="asset-leasing-conventions"></a><span data-ttu-id="ea0c0-103">Vara rentimise reeglid</span><span class="sxs-lookup"><span data-stu-id="ea0c0-103">Asset leasing conventions</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ea0c0-104">Selles teemas kirjeldatakse renditavate varade reegleid.</span><span class="sxs-lookup"><span data-stu-id="ea0c0-104">This topic describes conventions for leased assets.</span></span> <span data-ttu-id="ea0c0-105">Rentimisreegleid kasutatakse rendiraamatu alguskuupäeva määramiseks.</span><span class="sxs-lookup"><span data-stu-id="ea0c0-105">Leasing conventions are used to determine the commencement date of a lease book.</span></span> <span data-ttu-id="ea0c0-106">Kui rentimisreegeli väärtuseks on määratud **Puudub**, on alguskuupäev sama, mis rendi alguskuupäev (st välja **Rendi alguskuupäev** väärtus).</span><span class="sxs-lookup"><span data-stu-id="ea0c0-106">If the leasing convention is set to **None**, the commencement date is the same as the start date for the lease (that is, the value of the **Lease start date** field).</span></span> <span data-ttu-id="ea0c0-107">Kui rentimisreegliks on määratud **Terve kuu**, on alguskuupäev selle kuu esimene päev, millesse langeb rendi alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="ea0c0-107">If the leasing convention is set to **Full month**, the commencement date is the first day of the month that the lease's start date falls in.</span></span>

<span data-ttu-id="ea0c0-108">Alguskuupäev määrab kohustise amortiseerimise ja vara kulumi graafikute perioodi alguskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="ea0c0-108">The commencement date determines the start date of the period for the liability amortization and asset depreciation schedules.</span></span> <span data-ttu-id="ea0c0-109">Intressikulud ja amortisatsioonikulud sisestatakse vastavate graafikute perioodi lõppkuupäeval.</span><span class="sxs-lookup"><span data-stu-id="ea0c0-109">Interest expenses and depreciation expenses are posted on the period end date of the corresponding schedules.</span></span> <span data-ttu-id="ea0c0-110">Esialgne tuvastuse ja korrigeerimise töölehekirje sisestatakse alguskuupäeval.</span><span class="sxs-lookup"><span data-stu-id="ea0c0-110">The initial recognition and adjustment journal entry are posted on the commencement date.</span></span>

> [!NOTE]
> <span data-ttu-id="ea0c0-111">Rentimisreeglite funktsioon peab olema funktsioonihalduse kaudu sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="ea0c0-111">The feature for leasing conventions must be turned on through Feature Management.</span></span> <span data-ttu-id="ea0c0-112">Otsige tööruumis **Funktsioonihaldus** üles funktsioon nimega **Vara rentimise rentimisreegel** ja seejärel tehke valik **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="ea0c0-112">In the **Feature management** workspace, find and select the feature that is named **Leasing convention for asset leasing** feature, and then select **Enable now**.</span></span>

<span data-ttu-id="ea0c0-113">Rentimisreeglid määratakse rendivara raamatu häälestuseks.</span><span class="sxs-lookup"><span data-stu-id="ea0c0-113">Leasing conventions are assigned to the setup for a lease asset book.</span></span>

<span data-ttu-id="ea0c0-114">Rentimisreegli kuvamiseks või määramiseks tehke järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="ea0c0-114">To view or assign the leasing convention, follow these steps.</span></span>

1. <span data-ttu-id="ea0c0-115">Avage **Vara rentimine \> Seadistus \> Rendiraamatud**.</span><span class="sxs-lookup"><span data-stu-id="ea0c0-115">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="ea0c0-116">Valige väljal **Rentimisreegel** üks järgmistest väärtustest.</span><span class="sxs-lookup"><span data-stu-id="ea0c0-116">In the **Leasing convention** field, select one of the following values.</span></span>

    | <span data-ttu-id="ea0c0-117">Rentimise reegel</span><span class="sxs-lookup"><span data-stu-id="ea0c0-117">Leasing convention</span></span> | <span data-ttu-id="ea0c0-118">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ea0c0-118">Description</span></span> |
    |--------------------|-------------|
    | <span data-ttu-id="ea0c0-119">None</span><span class="sxs-lookup"><span data-stu-id="ea0c0-119">None</span></span>               | <span data-ttu-id="ea0c0-120">Kohustise amortiseerimise ja vara kulumi graafikud algavad rendi alguskuupäeval, kuna alguskuupäev on võrdne rendi alguskuupäevaga.</span><span class="sxs-lookup"><span data-stu-id="ea0c0-120">The liability amortization and asset depreciation schedules start on the lease's start date, because the commencement date equals the lease's start date.</span></span> <span data-ttu-id="ea0c0-121">Lõppkuupäev on üks kuu hiljem.</span><span class="sxs-lookup"><span data-stu-id="ea0c0-121">The end date is one month later.</span></span> <span data-ttu-id="ea0c0-122">See rentimisreegel ei taga, et intress sisestatakse iga kuu viimasel päeval.</span><span class="sxs-lookup"><span data-stu-id="ea0c0-122">This leasing convention doesn't guarantee that the interest will be posted on the last day of each month.</span></span> |
    | <span data-ttu-id="ea0c0-123">Terve kuu</span><span class="sxs-lookup"><span data-stu-id="ea0c0-123">Full month</span></span>         | <span data-ttu-id="ea0c0-124">Rentide puhul, mille alguskuupäev langeb kuu mis tahes päevale, hakkavad kohustise amortiseerimise ja vara kulumi graafikud kulusid koondama selle kuu esimesel päeval.</span><span class="sxs-lookup"><span data-stu-id="ea0c0-124">For leases that have a start date that occurs at any time during the month, the liability amortization and asset depreciation schedules start to accrue expenses on the first day of that month.</span></span> <span data-ttu-id="ea0c0-125">See rentimisreegel tagab, et kogu kuu intress kogutakse iga kuu viimasel päeval.</span><span class="sxs-lookup"><span data-stu-id="ea0c0-125">This leasing convention ensures that interest is accrued on the last day of each month for the whole month.</span></span> |

3. <span data-ttu-id="ea0c0-126">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ea0c0-126">Select **Save**.</span></span>

<span data-ttu-id="ea0c0-127">Rendi loomisel sisestatakse iga raamatu alguskuupäev automaatselt, lähtudes sisestatud rendi alguskuupäevast ja raamatu jaoks määratud rentimisreeglist.</span><span class="sxs-lookup"><span data-stu-id="ea0c0-127">When a lease is created, the commencement date of each book is automatically entered based on the start date that is entered for the lease and the leasing convention that is specified for the book.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]