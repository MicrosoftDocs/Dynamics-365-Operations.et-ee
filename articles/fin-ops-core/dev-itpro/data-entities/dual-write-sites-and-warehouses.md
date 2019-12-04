---
title: Integreeritu kohad ja laod
description: Siin peatükis kirjeldatakse koha ja lao andmete integratsiooni Finance and Operationsi ning Common Data Service’i vahel.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 4cf402e2811aaf92ddfa78eaf6d8887d88d93cbc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770980"
---
# <a name="integrated-sites-and-warehouses"></a>Integreeritu kohad ja laod

[!include [banner](../includes/banner.md)]

Siin peatükis kirjeldatakse koha ja lao andmete integratsiooni Finance and Operationsi ning Common Data Service’i vahel. Tegevuskohad ja laod on rakenduses Supply Chain Management levinud kontseptsioonid. Neid kasutatakse ettevõtte tarneahela modelleerimiseks.

## <a name="templates"></a>Mallid

Common Data Service’iga integreerimisega on need kontseptsioonid ja kogu asjakohane teave saadaval Common Data Service’is järgmises tabelis olevate kohtade ning ladude üksuste kaudu.

Finance and Operationsi rakendused | Muud Dynamics 365 rakendused | Kirjeldus
--------------------------|---------------------------|---
Saidid | msdyn_operationalsites | 
Laod | msdyn_warehouses | 

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [operational sites](dual-write/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](dual-write/InventWarehouseEntity-msdyn-warehouse.md)]

