---
title: Integreeritu kohad ja laod
description: Siin peatükis kirjeldatakse koha ja lao andmete integratsiooni rakenduse Finance and Operations ja teenuse Dataverse vahel.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: b93e5f15e281c20f8688d496fc78f8b46b8aa996
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560357"
---
# <a name="integrated-sites-and-warehouses"></a>Integreeritud kohad ja laod

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Siin peatükis kirjeldatakse koha ja lao andmete integratsiooni rakenduse Finance and Operations ja teenuse Dataverse vahel. Tegevuskohad ja laod on rakenduses Supply Chain Management levinud kontseptsioonid. Neid kasutatakse ettevõtte tarneahela modelleerimiseks.

## <a name="templates"></a>Mallid

Dataverse’iga integreerimisega on need kontseptsioonid ja kogu asjakohane teave saadaval Dataverse’is järgmises tabelis olevate kohtade ning ladude andmetabelite kaudu.

Finance and Operations rakendused | Muud Dynamics 365 rakendused | Kirjeldus
--------------------------|---------------------------|---
Saidid | msdyn_operationalsites | 
Laod | msdyn_warehouses | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]