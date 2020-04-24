---
title: Plaanitud käivitamine
description: Selles teemas selgitatakse plaanitud käivitamist varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 976155b685498456952f7d715779d20191712103
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215512"
---
# <a name="scheduled-execution"></a><span data-ttu-id="595a1-103">Plaanitud käivitamine</span><span class="sxs-lookup"><span data-stu-id="595a1-103">Scheduled execution</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="595a1-104">Saate plaanitud käivitamise seadistamiseks kasutada töökäsu teenindustasemeid.</span><span class="sxs-lookup"><span data-stu-id="595a1-104">You can use work order service levels to set up scheduled execution.</span></span> <span data-ttu-id="595a1-105">(Töökäsu teenindustasemete kohta lisainfo saamiseks vt [Teenindustase ja kirjeldus](service-level-and-description.md).) Plaanitud käivitamine pakub hooldustöötajate töö planeerimises paindlikkust, sest saate seadistada üksikasjalikumaid või vähemate üksikasjadega nõudeid sellele ajavahemikule, millal töökäsk peaks lõpule viidama.</span><span class="sxs-lookup"><span data-stu-id="595a1-105">(For more information about work order service levels, see [Service level and description](service-level-and-description.md).) Scheduled execution provides flexibility in work planning for maintenance workers, because you can set up more detailed or less detailed requirements for the interval that a work order should be completed during.</span></span> <span data-ttu-id="595a1-106">Näiteks võib hooldustöötaja, kes lõpetab töö tootmishoones oodatus varem liikuda edasi teisele lähedalasuvale tööle, mis on planeeritud selleks nädalaks aga mitte ilmtingimata samaks päevaks.</span><span class="sxs-lookup"><span data-stu-id="595a1-106">For example, a maintenance worker who completes a job faster than expected in a production facility might be able to move on to another nearby job that was planned for the current week but not necessarily for the current day.</span></span> <span data-ttu-id="595a1-107">See lähenemine võimaldab töötajate planeerimise ja töö lõpetamise optimeerimist.</span><span class="sxs-lookup"><span data-stu-id="595a1-107">This approach allows for optimization of worker planning and job completion.</span></span>

<span data-ttu-id="595a1-108">Töökäskudega seotud planeeritud käivitamise seadistamine võib olla üldine või spetsiifiline.</span><span class="sxs-lookup"><span data-stu-id="595a1-108">Scheduled execution setup, which is related to work orders, can be generic or specific.</span></span> <span data-ttu-id="595a1-109">Võite seadistada üldised read, mis ei ole piiratud konkreetsete töökäsu tüüpidega, vara tüüpidega jne.</span><span class="sxs-lookup"><span data-stu-id="595a1-109">You can set up generic lines that aren't limited to specific work order types, asset types, and so on.</span></span> <span data-ttu-id="595a1-110">Alternatiivina võite luua planeeritud käivitamise ridu, mis rakenduvad konkreetsele töökäsu tüübile, vara tüübile, hooldustöö tüübile jne.</span><span class="sxs-lookup"><span data-stu-id="595a1-110">Alternatively, you can create scheduled execution lines that apply to a specific work order type, asset type, maintenance job type, and so on.</span></span>

1. <span data-ttu-id="595a1-111">Valige **Varahaldus** \> **Seadistus** \> **Töökäsud** \> **Planeeritud käivitamine**.</span><span class="sxs-lookup"><span data-stu-id="595a1-111">Select **Asset management** \> **Setup** \> **Work orders** \> **Scheduled execution**.</span></span>
2. <span data-ttu-id="595a1-112">Planeeritud käivitamise rea loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="595a1-112">Select **New** to create a scheduled execution line.</span></span>
3. <span data-ttu-id="595a1-113">Valige vajalikud väärtused väljadele **Töö asukoht**, **Töökäsu tüüp**, **Vara tüüp**, **Tootja**, **Mudel**, **Hooldustöö tüübi kategooria**, **Hooldustöö tüüp**, **Hooldustöö tüübi variant** ja **Vahetus**.</span><span class="sxs-lookup"><span data-stu-id="595a1-113">In the **Functional location**, **Work order type**, **Asset type**, **Manufacturer**, **Model**, **Maintenance job type category**, **Maintenance job type**, **Maintenance job type variant**, and **Trade** fields, select values as you require.</span></span>
4. <span data-ttu-id="595a1-114">Valige töökäsu teenindustase väljal **Teenindustase**.</span><span class="sxs-lookup"><span data-stu-id="595a1-114">In the **Service level** field, select a work order service level.</span></span> <span data-ttu-id="595a1-115">Kui jätate selle välja tühjaks, teete kõige üldisemat tüüpi planeeritud käivitamise rea.</span><span class="sxs-lookup"><span data-stu-id="595a1-115">If you leave this field blank, you make the most generic type of scheduled execution line.</span></span> <span data-ttu-id="595a1-116">Üldise rea näite leiate järgneva joonise esimesest kirjest.</span><span class="sxs-lookup"><span data-stu-id="595a1-116">For an example of a generic line, see the first record in the illustration that follows.</span></span> <span data-ttu-id="595a1-117">See rida lubab planeerida kõik sellised töökäsud, millel ei ole töökäsu teenindustaset, konkreetsele kuupäevale ja kellaajale.</span><span class="sxs-lookup"><span data-stu-id="595a1-117">That line enables all work orders that have no work order service level to be scheduled for a specific date and time.</span></span>
5. <span data-ttu-id="595a1-118">Valige ajavahemik väljal **Planeeritud käivitamine**.</span><span class="sxs-lookup"><span data-stu-id="595a1-118">In the **Scheduled execution** field, select the time interval.</span></span>
6. <span data-ttu-id="595a1-119">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="595a1-119">Select **Save**.</span></span>

![Plaanitud käivitamine](media/20-setup-for-work-orders.png)
