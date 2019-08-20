---
title: Asukohaprofiili loomine
description: Igal asukohal laos on vaja sellega seotud asukohaprofiili, mis kirjeldab asukoha atribuute, näiteks seda, kas asukoht lubab segakaupu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9e1217a1105e1d53fc937f927e066e392f1ef14
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847323"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="a4e42-103">Asukohaprofiili loomine</span><span class="sxs-lookup"><span data-stu-id="a4e42-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a4e42-104">Igal asukohal laos on vaja sellega seotud asukohaprofiili, mis kirjeldab asukoha atribuute, näiteks seda, kas asukoht lubab segakaupu.</span><span class="sxs-lookup"><span data-stu-id="a4e42-104">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="a4e42-105">Selles protseduuris loome profiili asukohale, mis ei nõua litsentsiplaadi kontrollimist.</span><span class="sxs-lookup"><span data-stu-id="a4e42-105">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="a4e42-106">Lubame segakaubad, varude segaoleku ja tsüklilise inventuuri.</span><span class="sxs-lookup"><span data-stu-id="a4e42-106">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="a4e42-107">Saate seda protseduuri kasutada demoandmete ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="a4e42-107">You can use this procedure in the USMF demo data company.</span></span>

1. <span data-ttu-id="a4e42-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="a4e42-108">Click New.</span></span>
2. <span data-ttu-id="a4e42-109">Sisestage väärtus väljale Asukohaprofiili ID.</span><span class="sxs-lookup"><span data-stu-id="a4e42-109">In the Location profile ID field, type a value.</span></span>
3. <span data-ttu-id="a4e42-110">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="a4e42-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a4e42-111">Sisestage või valige väärtus väljal Asukoha vorming.</span><span class="sxs-lookup"><span data-stu-id="a4e42-111">In the Location format field, enter or select a value.</span></span>
5. <span data-ttu-id="a4e42-112">Sisestage või valige väärtus väljal Asukoha tüüp.</span><span class="sxs-lookup"><span data-stu-id="a4e42-112">In the Location type field, enter or select a value.</span></span>
6. <span data-ttu-id="a4e42-113">Sisestage või valige väärtus väljal Laadimissildade halduse profiili ID.</span><span class="sxs-lookup"><span data-stu-id="a4e42-113">In the Dock management profile ID field, enter or select a value.</span></span>
7. <span data-ttu-id="a4e42-114">Tehke väljal Luba segakaubad valik Jah.</span><span class="sxs-lookup"><span data-stu-id="a4e42-114">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="a4e42-115">Tehke väljal Luba lao segaolekud valik Jah.</span><span class="sxs-lookup"><span data-stu-id="a4e42-115">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="a4e42-116">Valige väljal Luba tsükliline inventuur väärtus Jah.</span><span class="sxs-lookup"><span data-stu-id="a4e42-116">Select Yes in the Allow cycle counting field.</span></span>
10. <span data-ttu-id="a4e42-117">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="a4e42-117">Click Save.</span></span>
11. <span data-ttu-id="a4e42-118">Avage Laohaldus > Seadistus > Ladu > Asukohaprofiilid.</span><span class="sxs-lookup"><span data-stu-id="a4e42-118">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>

