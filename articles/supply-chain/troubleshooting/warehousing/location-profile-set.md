---
title: Asukohaprofiil keelab negatiivsed varud, kuid negatiivne käsivarude loend on lubatud
description: Asukohaprofiili valik Luba negatiivne varu väärtuseks on seatud Ei, kuid süsteem lubab siiski negatiivset käsivarude loendit.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026437"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a><span data-ttu-id="0d33f-103">Asukohaprofiil keelab negatiivsed varud, kuid negatiivne käsivarude loend on lubatud</span><span class="sxs-lookup"><span data-stu-id="0d33f-103">Location profile disallows negative inventory, but negative on-hand inventory is permitted</span></span>

<span data-ttu-id="0d33f-104">KB number: 4613622</span><span class="sxs-lookup"><span data-stu-id="0d33f-104">KB number: 4613622</span></span>

## <a name="symptoms"></a><span data-ttu-id="0d33f-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="0d33f-105">Symptoms</span></span>

<span data-ttu-id="0d33f-106">Asukohaprofiili valik **Luba negatiivne varu** väärtuseks on seatud *Ei*, kuid süsteem lubab siiski negatiivset käsivarude loendit.</span><span class="sxs-lookup"><span data-stu-id="0d33f-106">The **Allow negative inventory** option for the location profile is set to *No*, but the system still allows negative on-hand inventory.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="0d33f-107">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="0d33f-107">Example scenario</span></span>

<span data-ttu-id="0d33f-108">Valitsuse reguleeritud kannete puhul peab süsteem saama kirjendada negatiivseid varusid kahjumite reserveerimiseks.</span><span class="sxs-lookup"><span data-stu-id="0d33f-108">For government-regulated transactions, the system must be able to record negative inventory to book losses.</span></span> <span data-ttu-id="0d33f-109">Soovite, et kaubal oleks võimalik näidata negatiivset laovaru, kuid ainult määratud asukohtades, nagu näiteks saadetav.</span><span class="sxs-lookup"><span data-stu-id="0d33f-109">You want an item to be able to show negative inventory, but only in designated locations, such as tanks.</span></span> <span data-ttu-id="0d33f-110">Kui aga kauba mudeligrupp lubab negatiivset laovaru, siis leiate, et pole oluline, kas asukoht on seatud lubama negatiivset laovaru.</span><span class="sxs-lookup"><span data-stu-id="0d33f-110">However, if the item model group allows negative inventory, you find that it doesn't matter whether the location is set to allow negative inventory.</span></span> <span data-ttu-id="0d33f-111">Kui kaup on seadistatud nii, et negatiivne laovaru ei ole lubatud, pole oluline, kuidas asukoha profiil seadistatakse.</span><span class="sxs-lookup"><span data-stu-id="0d33f-111">If the item is set up so that negative inventory isn't allowed, it doesn't matter how the location profile is set up.</span></span>

## <a name="resolution"></a><span data-ttu-id="0d33f-112">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="0d33f-112">Resolution</span></span>

<span data-ttu-id="0d33f-113">Säte **Luba negatiivne laovaru** asukohaprofiilist kehtib ainult laoprotsessidele, nt komplekteerimisele.</span><span class="sxs-lookup"><span data-stu-id="0d33f-113">The **Allow negative inventory** setting from the location profile applies only to warehouse processes, such as picking.</span></span> <span data-ttu-id="0d33f-114">Kauba mudeligrupid, mis on seadistatud lubama negatiivset laovaru, mõjutavad kõiki laohalduse ja laohalduse mooduli protsesse ning asukohaprofiil ei alista seadistust.</span><span class="sxs-lookup"><span data-stu-id="0d33f-114">However, item model groups that are set to allow negative inventory affect all processes from the Inventory management and Warehouse management modules, and the location profile won't override the setting.</span></span>

<span data-ttu-id="0d33f-115">Saate kontrollida, kas laol on lubatud negatiivseid varusid kanda.</span><span class="sxs-lookup"><span data-stu-id="0d33f-115">You can control whether a warehouse is allowed to carry negative inventory.</span></span> <span data-ttu-id="0d33f-116">Seadistage kaubamudeligrupid keelama negatiivset füüsilist laovaru ning seadistama negatiivse laovaru lubamiseks ainult vastava lao.</span><span class="sxs-lookup"><span data-stu-id="0d33f-116">Set your item model groups to disallow negative physical inventory, and set only the relevant warehouse to allow negative inventory.</span></span>
