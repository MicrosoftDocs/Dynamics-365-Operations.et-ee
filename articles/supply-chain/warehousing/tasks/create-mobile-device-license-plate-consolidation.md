---
title: Mobiilse seadme menüükäsu loomine registreerimismärgi konsolideerimiseks
description: See protseduur näitab, kuidas luua mobiilse seadme menüükäsku litsentsiplaadi konsolideerimise tööle.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1dfb0bb2db5690a966d70f96a3bba2d60833abd4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830998"
---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="a8b19-103">Mobiilse seadme menüükäsu loomine registreerimismärgi konsolideerimiseks</span><span class="sxs-lookup"><span data-stu-id="a8b19-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a8b19-104">See protseduur näitab, kuidas luua mobiilse seadme menüükäsku litsentsiplaadi konsolideerimise tööle.</span><span class="sxs-lookup"><span data-stu-id="a8b19-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="a8b19-105">See võimaldab laotöötajatel konsolideerida kaupu ühele litsentsiplaadile koos teise sama asukoha litsentsiplaadi kaupadega.</span><span class="sxs-lookup"><span data-stu-id="a8b19-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="a8b19-106">Näiteks võidakse seda kasutada, kui mõlemal töökäsul olid järgnevad ajastamise etapid samad, nii et ühendatud kaupadega tuleb teha töö vaid ühe korra.</span><span class="sxs-lookup"><span data-stu-id="a8b19-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="a8b19-107">Saate seda protseduuri kasutada demoandmete ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="a8b19-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="a8b19-108">Seda ülesannet täidab üldjuhul laohaldur.</span><span class="sxs-lookup"><span data-stu-id="a8b19-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="a8b19-109">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="a8b19-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="a8b19-110">Avage Laohaldus > Seadistus > Mobiilne seade > Mobiilse seadme menüü-üksused.</span><span class="sxs-lookup"><span data-stu-id="a8b19-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="a8b19-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="a8b19-111">Click New.</span></span>
3. <span data-ttu-id="a8b19-112">Sisestage väärtus väljale Menüü-üksuse nimi.</span><span class="sxs-lookup"><span data-stu-id="a8b19-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="a8b19-113">Sisestage väärtus väljale Pealkiri.</span><span class="sxs-lookup"><span data-stu-id="a8b19-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="a8b19-114">Tehke väljal Režiim valik Kaudne.</span><span class="sxs-lookup"><span data-stu-id="a8b19-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="a8b19-115">Tehke väljal Tegevuse kood valik Konsolideeri litsentsiplaadid.</span><span class="sxs-lookup"><span data-stu-id="a8b19-115">In the Activity code field, select 'Consolidate license plates'.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]