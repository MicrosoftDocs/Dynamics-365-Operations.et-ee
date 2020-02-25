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
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 0d32a5f7859f0200da823a73d94b9a6b2a9c8e7d
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019736"
---
# <a name="integrated-tax"></a>Integreeritud maks

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Maksu seadistusandmed määravad nii kaudsete maksude (KM, GST, käibemaks) kui ka kinnipeetava maksu seadistuse. Need kirjeldavad maksu arvutamise reeglit, maksumäära, maksuarvestust, tasakaalustust ja muid mõisteid.

## <a name="templates"></a>Mallid

Maksuandmed sisaldavad olemikaartide kogumit, mis töötavad andmete suhtluse ajal koos, nagu on näha järgmises tabelis.

Finance and Operations   | Muud Dynamics 365 rakendused
-------------------------|---------------------------------
Maksukoodid                  | msdyn\_taxcodes.md
Maksugrupid               | msdyn\_taxgroups.md
Maksu kaubagrupid          | msdyn\_taxitemgroups.md
Maksuvabastused           | msdyn\_taxexemptcodes.md
Maksuhaldurid          | msdyn\_taxauthorities.md
Kinnipeetava maksu koodid      | msdyn\_withholdingtaxcodes.md
Kinnipeetava maksugrupid   | msdyn\_withholdingtaxgroups.md
Maksu pearaamatukonto grupp | msdyn\_taxpostinggroups  

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

