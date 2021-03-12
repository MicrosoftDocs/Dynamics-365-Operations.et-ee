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
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d8d28b9670d8752c1039684551d56b1779a10b20
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001595"
---
# <a name="production-output-location"></a><span data-ttu-id="170bb-103">Tootmise väljundasukoht</span><span class="sxs-lookup"><span data-stu-id="170bb-103">Production output location</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="170bb-104">Selles teemas kirjeldatakse hierarhiat, mida kasutatakse tootmise väljundasukoha tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="170bb-104">This topic describes the hierarchy that is used to identify the production output location.</span></span>

<span data-ttu-id="170bb-105">Tootmise väljundasukoht on asukoht, kus lõpetatud kaupu pärast tootmist kõigepealt hoitakse.</span><span class="sxs-lookup"><span data-stu-id="170bb-105">The production output location is the location where a finished good is first stored after it's produced.</span></span> <span data-ttu-id="170bb-106">Tavaliselt on see asukoht lõpetatud kaupu tootva tootmisprotsessi lähedal.</span><span class="sxs-lookup"><span data-stu-id="170bb-106">Usually, this location is close to the production process that produces the finished good.</span></span> <span data-ttu-id="170bb-107">Tootmise väljundasukohta kasutatakse materjali vahehoidlana, enne kui see viiakse saatmisalale, laoasukohta, tootmise sisendasukohta allavoolu tootmisprotsessi puhul jne.</span><span class="sxs-lookup"><span data-stu-id="170bb-107">The production output location is used as intermediate storage for the material before it's moved on to the shipment area, a storage location, a production input location for a downstream production process, and so on.</span></span> 

<span data-ttu-id="170bb-108">Tootmise vauikeasukoht määratakse siis, kui lõpetatud kaubad raporteeritakse tootmistellimusel või partiitellimusel.</span><span class="sxs-lookup"><span data-stu-id="170bb-108">A default production output location is set when finished goods are reported on a production order or batch order.</span></span> <span data-ttu-id="170bb-109">Selle väljundasukoha tuvastamiseks kasutatakse järgmist hierarhiat.</span><span class="sxs-lookup"><span data-stu-id="170bb-109">The following hierarchy is used to identify this output location:</span></span>

1. <span data-ttu-id="170bb-110">Tootmistellimuse või partiitellimuse päises määratletud väljundasukoha kasutamine.</span><span class="sxs-lookup"><span data-stu-id="170bb-110">Use the output location that is defined on the production order or batch order header.</span></span>
2. <span data-ttu-id="170bb-111">Kui asukohta siit ei leita, kasutatakse väljundasukohta, mis on määratletud tootmisprotsessis määratletud viimase toimingu kasutatud ressursis.</span><span class="sxs-lookup"><span data-stu-id="170bb-111">If no location is found there, use the output location that is defined on the resource that is used by the last operation that is defined in the production route.</span></span>
3. <span data-ttu-id="170bb-112">Kui asukohta siit ei leita, kasutatakse väljundasukohta, mis on määratletud tootmisprotsessis määratletud viimase toimingu ressursi kasutatud ressursigrupis.</span><span class="sxs-lookup"><span data-stu-id="170bb-112">If no location is found there, use the output location that is defined on the resource group that is used by the resource for the last operation that is defined in the production route.</span></span>
4. <span data-ttu-id="170bb-113">Kui asukohta siit ei leita, kasutatakse väljundasukohta, mis on määratletud tootmistellimuse jaoks määratud laos.</span><span class="sxs-lookup"><span data-stu-id="170bb-113">If no location is found there, use the output location that is defined on the warehouse that is defined for the production order.</span></span>

<span data-ttu-id="170bb-114">Tootmise vaike-väljundasukoht määratakse ainult toodetele, mis on seadistatud täpsemate laoprotsesside kasutamisega.</span><span class="sxs-lookup"><span data-stu-id="170bb-114">A default production output location is set only for products that are set up by using advanced warehouse processes.</span></span> <span data-ttu-id="170bb-115">Kui seda tüüpi kaup raporteeritakse lõpetatuks, luuakse laotöö tüübiga **Lõpetatud toodete kõrvalepanek** või **Kaastoote ja kõrvalsaaduse kõrvalepanek**.</span><span class="sxs-lookup"><span data-stu-id="170bb-115">When this type of item is reported as finished, warehouse work of the **Finished goods put away** or **Co-product and by-product put away** type is created.</span></span> <span data-ttu-id="170bb-116">Seda tüüpi töö kasutab tootmise väljundasukohta komplekteerimisasukohana.</span><span class="sxs-lookup"><span data-stu-id="170bb-116">This type of work uses the production output location as the pick location.</span></span> <span data-ttu-id="170bb-117">Kõrvalepaneku asukoht määratakse asukohakorraldustega.</span><span class="sxs-lookup"><span data-stu-id="170bb-117">The put-away location is determined by the location directives.</span></span>
