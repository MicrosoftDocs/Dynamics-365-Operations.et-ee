---
title: Ettevõttesisesed varad teenindamiseks
description: Selles teemas kirjeldatakse, kuidas saate kasutada Microsoft Dynamics 365 Field Service'it nii klientide kui ka ettevõttesiseste varade teenindamiseks.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 1e423199d0639db5e403e280880036b590149095
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172942"
---
# <a name="in-house-assets-for-servicing"></a>Ettevõttesisesed varad teenindamiseks

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Field Service on loodud kliendivarade teenindamiseks. Dynamics 365 Supply Chain Managementi varahaldus on loodud ettevõttesiseste varade haldamiseks. Nende kahe rakenduse integreerimine võimaldab teil kasutada Field Service'it nii klientide kui ka ettevõttesiseste varade teenindamiseks. Samuti saate varasid liigitada töö asukoha ja hierarhia järgi ning jälgida teenindust üksikasjalikul tasemel.

Lisateavet vaadake teemast [Dynamics 365 Field Service'i ja Supply Chain Managementi integreerimine](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Mallid

Ettevõttesisesed varad sisaldavad põhiliste olemikaartide kogumit, mis töötavad andmete suhtluse ajal koos, nagu on näha järgmises tabelis.

| Finance and Operations rakendused | Mudeljuhitud Dynamics 365 rakendused | Kirjeldus |
|-----------------------------|-----------------------------------|-------------|
| Varahalduse vara töötsükli mudelid | msdyn\_assetlifecyclemodels | |
| Varahalduse vara töötsükli olekud | msdyn\_assetlifecyclestates | |
| Varahalduse varad | msdyn\_customerassets | |
| Varahalduse varade tüübid | msdyn\_customerassetcategories | |
| Varahalduse töö asukoha töötsükli mudelid | msdyn\_functionallocationlifecyclemodels | |
| Varahalduse töö asukoha töötsükli olekud | msdyn\_functionallocationlifecyclestates | |
| Varahalduse töö asukohad | msdyn\_functionallocations | |
| Varahalduse töö asukohtade tüübid | msdyn\_functionallocationtypes | |
| Varahalduse tootjad | msdyn\_manufacturers | |
| Varahalduse mudelid | msdyn\_models | |
| Varahalduse garantii | msdyn\_warranties | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]
