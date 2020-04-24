---
title: Tootmise väljundasukoht
description: Selles teemas kirjeldatakse hierarhiat, mida kasutatakse tootmise väljundasukoha tuvastamiseks.
author: johanhoffmann
manager: tfehr
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e4002bf7dddb196edf306268ecc16e1bfa5d6d1e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211303"
---
# <a name="production-output-location"></a><span data-ttu-id="78f94-103">Tootmise väljundasukoht</span><span class="sxs-lookup"><span data-stu-id="78f94-103">Production output location</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78f94-104">Selles teemas kirjeldatakse hierarhiat, mida kasutatakse tootmise väljundasukoha tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="78f94-104">This topic describes the hierarchy that is used to identify the production output location.</span></span>

<span data-ttu-id="78f94-105">Tootmise väljundasukoht on asukoht, kus lõpetatud kaupu pärast tootmist kõigepealt hoitakse.</span><span class="sxs-lookup"><span data-stu-id="78f94-105">The production output location is the location where a finished good is first stored after it's produced.</span></span> <span data-ttu-id="78f94-106">Tavaliselt on see asukoht lõpetatud kaupu tootva tootmisprotsessi lähedal.</span><span class="sxs-lookup"><span data-stu-id="78f94-106">Usually, this location is close to the production process that produces the finished good.</span></span> <span data-ttu-id="78f94-107">Tootmise väljundasukohta kasutatakse materjali vahehoidlana, enne kui see viiakse saatmisalale, laoasukohta, tootmise sisendasukohta allavoolu tootmisprotsessi puhul jne.</span><span class="sxs-lookup"><span data-stu-id="78f94-107">The production output location is used as intermediate storage for the material before it's moved on to the shipment area, a storage location, a production input location for a downstream production process, and so on.</span></span> 

<span data-ttu-id="78f94-108">Tootmise vauikeasukoht määratakse siis, kui lõpetatud kaubad raporteeritakse tootmistellimusel või partiitellimusel.</span><span class="sxs-lookup"><span data-stu-id="78f94-108">A default production output location is set when finished goods are reported on a production order or batch order.</span></span> <span data-ttu-id="78f94-109">Selle väljundasukoha tuvastamiseks kasutatakse järgmist hierarhiat.</span><span class="sxs-lookup"><span data-stu-id="78f94-109">The following hierarchy is used to identify this output location:</span></span>

1. <span data-ttu-id="78f94-110">Tootmistellimuse või partiitellimuse päises määratletud väljundasukoha kasutamine.</span><span class="sxs-lookup"><span data-stu-id="78f94-110">Use the output location that is defined on the production order or batch order header.</span></span>
2. <span data-ttu-id="78f94-111">Kui asukohta siit ei leita, kasutatakse väljundasukohta, mis on määratletud tootmisprotsessis määratletud viimase toimingu kasutatud ressursis.</span><span class="sxs-lookup"><span data-stu-id="78f94-111">If no location is found there, use the output location that is defined on the resource that is used by the last operation that is defined in the production route.</span></span>
3. <span data-ttu-id="78f94-112">Kui asukohta siit ei leita, kasutatakse väljundasukohta, mis on määratletud tootmisprotsessis määratletud viimase toimingu ressursi kasutatud ressursigrupis.</span><span class="sxs-lookup"><span data-stu-id="78f94-112">If no location is found there, use the output location that is defined on the resource group that is used by the resource for the last operation that is defined in the production route.</span></span>
4. <span data-ttu-id="78f94-113">Kui asukohta siit ei leita, kasutatakse väljundasukohta, mis on määratletud tootmistellimuse jaoks määratud laos.</span><span class="sxs-lookup"><span data-stu-id="78f94-113">If no location is found there, use the output location that is defined on the warehouse that is defined for the production order.</span></span>

<span data-ttu-id="78f94-114">Tootmise vaike-väljundasukoht määratakse ainult toodetele, mis on seadistatud täpsemate laoprotsesside kasutamisega.</span><span class="sxs-lookup"><span data-stu-id="78f94-114">A default production output location is set only for products that are set up by using advanced warehouse processes.</span></span> <span data-ttu-id="78f94-115">Kui seda tüüpi kaup raporteeritakse lõpetatuks, luuakse laotöö tüübiga **Lõpetatud toodete kõrvalepanek** või **Kaastoote ja kõrvalsaaduse kõrvalepanek**.</span><span class="sxs-lookup"><span data-stu-id="78f94-115">When this type of item is reported as finished, warehouse work of the **Finished goods put away** or **Co-product and by-product put away** type is created.</span></span> <span data-ttu-id="78f94-116">Seda tüüpi töö kasutab tootmise väljundasukohta komplekteerimisasukohana.</span><span class="sxs-lookup"><span data-stu-id="78f94-116">This type of work uses the production output location as the pick location.</span></span> <span data-ttu-id="78f94-117">Kõrvalepaneku asukoht määratakse asukohakorraldustega.</span><span class="sxs-lookup"><span data-stu-id="78f94-117">The put-away location is determined by the location directives.</span></span>
