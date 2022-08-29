---
title: Integreeritud maks
description: See artikkel kirjeldab maksuandmete integreerimist finantside ja toimingute ning Dataverse.
author: josaw
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8f148b710e2294edf1e402b9b8b22cb24e60a1f2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288790"
---
# <a name="integrated-tax"></a>Integreeritud maks

[!include [banner](../../includes/banner.md)]



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

