---
title: Asukohaprofiili loomine
description: Selles teemas tutvustatakse, kuidas luua asukohaprofiil rakenduses Dynamics 365 Supply Chain Management.
author: ShylaThompson
manager: tfehr
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bd5924447c0af21b5b26a2dc9098cf245b7ee12
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977259"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="b9de8-103">Asukohaprofiili loomine</span><span class="sxs-lookup"><span data-stu-id="b9de8-103">Create a location profile</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b9de8-104">Selles teemas tutvustatakse, kuidas luua asukohaprofiil rakenduses Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b9de8-104">This topic explains how to create a location profile in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="b9de8-105">Igal asukohal laos on vaja sellega seotud asukohaprofiili, mis kirjeldab asukoha atribuute, näiteks seda, kas asukoht lubab segakaupu.</span><span class="sxs-lookup"><span data-stu-id="b9de8-105">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="b9de8-106">Selles protseduuris loome profiili asukohale, mis ei nõua litsentsiplaadi kontrollimist.</span><span class="sxs-lookup"><span data-stu-id="b9de8-106">In this procedure we'll create a profile for a location that doesn't require license plate control.</span></span> <span data-ttu-id="b9de8-107">Lubame segakaubad, varude segaoleku ja tsüklilise inventuuri.</span><span class="sxs-lookup"><span data-stu-id="b9de8-107">We'll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="b9de8-108">Saate seda protseduuri kasutada demoandmete ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="b9de8-108">You can use this procedure in the USMF demo data company.</span></span>


1. <span data-ttu-id="b9de8-109">Navigeerimispaanil avage **Moodulid > Laohaldus > Seadistus > Ladu > Asukohaprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="b9de8-109">In the navigation pane, go to **Modules > Warehouse management > Setup > Warehouse > Location profiles**.</span></span>
2. <span data-ttu-id="b9de8-110">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b9de8-110">Select **New**.</span></span>
3. <span data-ttu-id="b9de8-111">Väljale **Asukohaprofiili ID** sisestage väärtus.</span><span class="sxs-lookup"><span data-stu-id="b9de8-111">In the **Location profile ID** field, type a value.</span></span>
4. <span data-ttu-id="b9de8-112">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="b9de8-112">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="b9de8-113">Väljale **Asukoha vorming** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="b9de8-113">In the **Location format** field, enter or select a value.</span></span>
6. <span data-ttu-id="b9de8-114">Väljale **Asukohatüüp** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="b9de8-114">In the **Location type** field, enter or select a value.</span></span>
7. <span data-ttu-id="b9de8-115">Väljale **Laadimissildade halduse profiili ID** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="b9de8-115">In the **Dock management profile ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="b9de8-116">Valige väärtus **Jah** väljal **Luba segakaubad**.</span><span class="sxs-lookup"><span data-stu-id="b9de8-116">Select **Yes** in the **Allow mixed items** field.</span></span>
9. <span data-ttu-id="b9de8-117">Valige väärtus **Jah** väljal **Luba lao segaolekud**.</span><span class="sxs-lookup"><span data-stu-id="b9de8-117">Select **Yes** in the **Allow mixed inventory statuses** field.</span></span>
10. <span data-ttu-id="b9de8-118">Valige väärtus **Jah** väljal **Luba tsükliline inventuur**.</span><span class="sxs-lookup"><span data-stu-id="b9de8-118">Select **Yes** in the **Allow cycle counting** field.</span></span>
11. <span data-ttu-id="b9de8-119">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b9de8-119">Select **Save**.</span></span>

