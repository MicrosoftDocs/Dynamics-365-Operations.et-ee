---
title: Integreeritud maks
description: Selles teemas kirjeldatakse maksuandmete integreerimist rakenduse Finance and Operations ja teenuse Common Data Service vahel.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
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
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 68461f375c6d5b04f224331dc192c921cf3c4d04
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979325"
---
# <a name="integrated-tax"></a>Integreeritud maks

[!include [banner](../../includes/banner.md)]



Maksu seadistusandmed määravad nii kaudsete maksude (KM, GST, käibemaks) kui ka kinnipeetava maksu seadistuse. Need kirjeldavad maksu arvutamise reeglit, maksumäära, maksuarvestust, tasakaalustust ja muid mõisteid.

## <a name="templates"></a>Mallid

Maksuandmed sisaldavad olemikaartide kogumit, mis töötavad andmete suhtluse ajal koos, nagu on näha järgmises tabelis.

Finance and Operations rakendused | Mudeljuhitud Dynamics 365 rakendused | Kirjeldus |
-------------------------|---------------------------------|----|
Kauba käibemaksugrupp | msdyn_taxitemgroups |
Käibemaksuhaldurid | msdyn_taxauthorities |
Käibemaksuvabastuse koodi olemi CDS | msdyn_taxexemptcodes |
Käibemaksugrupid | msdyn_taxgroups |
Käibemaksu pearaamatu sisestusgrupid V2 | msdyn_taxpostinggroups |
Kinnipeetava maksu koodid | msdyn_withholdingtaxcodes |
Kinnipeetava maksugrupid | msdyn_withholdingtaxgroups | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

