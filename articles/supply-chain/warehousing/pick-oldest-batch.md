---
title: Vanima partii komplekteerimine mobiilsel seadmel
description: Selles teemas kirjeldatakse, kuidas seadistada ja rakendada mobiilselt seadmelt vanima partii komplekteerimise valikuid.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 205317cccbde220d9198246f47076fc186286969
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="pick-oldest-batch-on-a-mobile-device"></a><span data-ttu-id="fd6f9-103">Vanima partii komplekteerimine mobiilsel seadmel</span><span class="sxs-lookup"><span data-stu-id="fd6f9-103">Pick oldest batch on a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd6f9-104">Konfiguratsioonile **Komplekteeri vanim partii** pääseb juurde mobiilse seadme menüü kaudu ja see võimaldab sundida laotöötajaid või hoiatada neid, et nad komplekteeriksid oma praeguses asukohas vanima partii.</span><span class="sxs-lookup"><span data-stu-id="fd6f9-104">You can access the configuration **Pick oldest batch** via a mobile device menu and it allows you to force or warn warehouse workers to pick the oldest batch in their current location.</span></span>  

## <a name="where-it-applies"></a><span data-ttu-id="fd6f9-105">Kus see kehtib</span><span class="sxs-lookup"><span data-stu-id="fd6f9-105">Where it applies</span></span>
<span data-ttu-id="fd6f9-106">Vanima partii komplekteerimine on konfigureeritud mobiilse seadme menüüelementides ja see käivitab allpool nimetatud kaupade partii komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="fd6f9-106">Pick oldest batch is configured on mobile device menu items and effects the pick for batch below items.</span></span>

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a><span data-ttu-id="fd6f9-107">Vanima partii komplekteerimise konfiguratsiooni seadistamine</span><span class="sxs-lookup"><span data-stu-id="fd6f9-107">How to set up the configuration for Pick oldest batch</span></span> 
<span data-ttu-id="fd6f9-108">Kaupade puhul, mis on seadistatud kasutama olemasolevat tööd, saab valiku **Komplekteeri vanim partii** olekuks määrata mobiilse seadme menüüst **Pole**, **Hoiata** või **Sunni**.</span><span class="sxs-lookup"><span data-stu-id="fd6f9-108">For items that are set to use existing work, **Pick oldest batch** can be set to **None**, **Warn**, or **Force** from a mobile device menu.</span></span>

<span data-ttu-id="fd6f9-109">**Pole**: töötajad ei saa ühtegi teadet ja neil lubatakse komplekteerida nende asukohas ükskõik millist partiid.</span><span class="sxs-lookup"><span data-stu-id="fd6f9-109">**None**: Workers will not receive any messages and they will be allowed to pick any batch in their location.</span></span>

<span data-ttu-id="fd6f9-110">**Hoiata** ja **Sunni**: kui töötaja valib partii, kuvatakse partii juhtelemendi kohal vanima aegumiskuupäevaga partii(de) loend.</span><span class="sxs-lookup"><span data-stu-id="fd6f9-110">**Warn** and **Force**:  A list of the batch(es) with the oldest expiration date will be displayed above the batch control when the worker selects a batch.</span></span> <span data-ttu-id="fd6f9-111">Kui asukohta juhitakse litsentsiplaadiga, siis kuvatakse litsentsiplaadi juhtelemendi kohal vanima partiiga litsentsiplaatide loend.</span><span class="sxs-lookup"><span data-stu-id="fd6f9-111">If the location is license plate controlled, a list of license plates that have the oldest batch will be displayed above the license plate control.</span></span> 
-   <span data-ttu-id="fd6f9-112">**Hoiata**: kui töötaja valib litsentsiplaadi või partii, mida kuvatavas loendis pole, siis muutub juhtelement tühjaks ja kuvatakse hoiatus, et on olemas vanem partii, mida valida.</span><span class="sxs-lookup"><span data-stu-id="fd6f9-112">**Warn**: If a worker chooses a license plate or batch that is not on the shown list, the control will be blanked and a warning will be shown that there is an older batch to select.</span></span> <span data-ttu-id="fd6f9-113">Et saada luba töö jätkamiseks võib töötaja valida uuesti sama litsentsiplaadi või partii.</span><span class="sxs-lookup"><span data-stu-id="fd6f9-113">To be allowed to continue the work, the worker can select the same license plate or batch again.</span></span>  
-   <span data-ttu-id="fd6f9-114">**Sunni**: töötajad saavad jätkuvalt teate, et komplekteerimiseks on olemas vanem partii.</span><span class="sxs-lookup"><span data-stu-id="fd6f9-114">**Force**: Workers will continue to receive the message that there is an older batch to pick.</span></span>

