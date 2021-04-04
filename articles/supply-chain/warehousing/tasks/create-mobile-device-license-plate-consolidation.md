---
title: Mobiilse seadme menüükäsu loomine registreerimismärgi konsolideerimiseks
description: See protseduur näitab, kuidas luua mobiilse seadme menüükäsku litsentsiplaadi konsolideerimise tööle.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54457261d4f80648050845f309bcbbcc16caa629
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239010"
---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="c1f26-103">Mobiilse seadme menüükäsu loomine registreerimismärgi konsolideerimiseks</span><span class="sxs-lookup"><span data-stu-id="c1f26-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c1f26-104">See protseduur näitab, kuidas luua mobiilse seadme menüükäsku litsentsiplaadi konsolideerimise tööle.</span><span class="sxs-lookup"><span data-stu-id="c1f26-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="c1f26-105">See võimaldab laotöötajatel konsolideerida kaupu ühele litsentsiplaadile koos teise sama asukoha litsentsiplaadi kaupadega.</span><span class="sxs-lookup"><span data-stu-id="c1f26-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="c1f26-106">Näiteks võidakse seda kasutada, kui mõlemal töökäsul olid järgnevad ajastamise etapid samad, nii et ühendatud kaupadega tuleb teha töö vaid ühe korra.</span><span class="sxs-lookup"><span data-stu-id="c1f26-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="c1f26-107">Saate seda protseduuri kasutada demoandmete ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="c1f26-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="c1f26-108">Seda ülesannet täidab üldjuhul laohaldur.</span><span class="sxs-lookup"><span data-stu-id="c1f26-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="c1f26-109">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="c1f26-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="c1f26-110">Avage Laohaldus > Seadistus > Mobiilne seade > Mobiilse seadme menüü-üksused.</span><span class="sxs-lookup"><span data-stu-id="c1f26-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="c1f26-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="c1f26-111">Click New.</span></span>
3. <span data-ttu-id="c1f26-112">Sisestage väärtus väljale Menüü-üksuse nimi.</span><span class="sxs-lookup"><span data-stu-id="c1f26-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="c1f26-113">Sisestage väärtus väljale Pealkiri.</span><span class="sxs-lookup"><span data-stu-id="c1f26-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="c1f26-114">Tehke väljal Režiim valik Kaudne.</span><span class="sxs-lookup"><span data-stu-id="c1f26-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="c1f26-115">Tehke väljal Tegevuse kood valik Konsolideeri litsentsiplaadid.</span><span class="sxs-lookup"><span data-stu-id="c1f26-115">In the Activity code field, select 'Consolidate license plates'.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]