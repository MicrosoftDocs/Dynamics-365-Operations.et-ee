---
title: Integreeritud maks
description: Selles teemas kirjeldatakse maksuandmete integreerimist rakenduse Finance and Operations ja teenuse Dataverse vahel.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: rhaertle
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: c7e76294944196670ed4b02ebf785c1bed7b5106f73d4b66a15a19c9a4235cbf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738548"
---
# <a name="integrated-tax"></a>Integreeritud maks

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Maksu seadistusandmed määravad nii kaudsete maksude (KM, GST, käibemaks) kui ka kinnipeetava maksu seadistuse. Need kirjeldavad maksu arvutamise reeglit, maksumäära, maksuarvestust, tasakaalustust ja muid mõisteid.

## <a name="templates"></a>Mallid

Maksuandmed sisaldavad tabeli kaartide kogumit, mis töötavad andmete suhtluse ajal koos, nagu on näha järgmises tabelis.

| Finance and Operations rakendused | Klientide kaasamise rakendused | Kirjeldus |
|-----------------------------|-----------------------------------|-------------|
[Kauba käibemaksugrupp](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Käibemaksuhaldurid](mapping-reference.md#193) | msdyn_taxauthorities | |
[Käibemaksuvabastuse koodi olemi CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[Käibemaksugrupid](mapping-reference.md#195) | msdyn_taxgroups | |
[Käibemaksu pearaamatu sisestusgrupid V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Kinnipeetava maksu koodid](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Kinnipeetava maksugrupid](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
