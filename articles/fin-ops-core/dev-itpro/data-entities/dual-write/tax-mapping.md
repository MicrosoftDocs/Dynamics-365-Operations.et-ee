---
title: Integreeritud maks
description: See artikkel kirjeldab maksuandmete integreerimist finantside ja toimingute ning toimingute vahel Dataverse.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8864a9567d57739aa72fa1859f5cfce6df33e8f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864539"
---
# <a name="integrated-tax"></a>Integreeritud maks

[!include [banner](../../includes/banner.md)]



Maksu seadistusandmed määravad nii kaudsete maksude (KM, GST, käibemaks) kui ka kinnipeetava maksu seadistuse. Need kirjeldavad maksu arvutamise reeglit, maksumäära, maksuarvestust, tasakaalustust ja muid mõisteid.

## <a name="templates"></a>Mallid

Maksuandmed sisaldavad tabeli kaartide kogumit, mis töötavad andmete suhtluse ajal koos, nagu on näha järgmises tabelis.

| Finance and Operationsi rakendused | Klientide kaasamise rakendused | Kirjeldus |
|-----------------------------|-----------------------------------|-------------|
[Kauba käibemaksugrupp](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Käibemaksuhaldurid](mapping-reference.md#193) | msdyn_taxauthorities | |
[Käibemaksuvabastuse koodi olemi CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[Käibemaksugrupid](mapping-reference.md#195) | msdyn_taxgroups | |
[Käibemaksu pearaamatu sisestusgrupid V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Kinnipeetava maksu koodid](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Kinnipeetava maksugrupid](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
