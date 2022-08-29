---
title: Ettevõttesisesed varad teenindamiseks
description: See artikkel kirjeldab, kuidas saate kasutada Microsoft Dynamics 365 Field Service nii kliendi varade kui ka majavarade teenuseks.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: b3e741c85fcad2abc18879280ef7332ae091c984
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289246"
---
# <a name="in-house-assets-for-servicing"></a>Ettevõttesisesed varad teenindamiseks

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Field Service on loodud kliendivarade teenindamiseks. Dynamics 365 Supply Chain Managementi varahaldus on loodud ettevõttesiseste varade haldamiseks. Nende kahe rakenduse integreerimine võimaldab teil kasutada Field Service'it nii klientide kui ka ettevõttesiseste varade teenindamiseks. Samuti saate varasid liigitada töö asukoha ja hierarhia järgi ning jälgida teenindust üksikasjalikul tasemel.

Lisateavet vaadake teemast [Dynamics 365 Field Service'i ja Supply Chain Managementi integreerimine](/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Mallid

Ettevõttesisesed varad sisaldavad põhiliste tabelikaartide kogumit, mis töötavad andmete suhtluse ajal koos, nagu on näha järgmises tabelis.

| Finance and Operations rakendused | Klientide kaasamise rakendused | Kirjeldus |
|-----------------------------|-----------------------------------|-------------|
[Varahalduse vara töötsükli mudelid](mapping-reference.md#119) | msdyn_assetlifecyclemodels | |
[Varahalduse vara töötsükli olekud](mapping-reference.md#120) | msdyn_assetlifecyclestates | |
[Varahalduse varade tüübid](mapping-reference.md#124) | msdyn_customerassetcategories | |
[Varahalduse varad](mapping-reference.md#125) | msdyn_customerassets | |
[Varahalduse töö asukoha töötsükli mudelid](mapping-reference.md#134) | msdyn_functionallocationlifecyclemodels | |
[Varahalduse töö asukoha töötsükli olekud](mapping-reference.md#135) | msdyn_functionallocationlifecyclestates | |
[Varahalduse töö asukohtade tüübid](mapping-reference.md#137) | msdyn_functionallocationtypes | |
[Varahalduse töö asukohad](mapping-reference.md#136) | msdyn_functionallocations | |
[Varahalduse tootjad](mapping-reference.md#153) | msdyn_manufacturers | |
[Varahalduse mudelid](mapping-reference.md#154) | msdyn_models | |
[Varahalduse garantii](mapping-reference.md#209) | msdyn_warranties | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
