---
title: Organisatsiooni hierarhia teenusesCommon Data Service
description: Selles teemas kirjeldatakse organisatsiooniliste andmete integreerimist Finance and Operationsi ja teenuse Common Data Service vahel.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca2ac0f9dbb8544b12f23a271423a43b0e601272
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789178"
---
## <a name="organization-hierarchy-in-common-data-service"></a>Organisatsiooni hierarhia teenusesCommon Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Kuna Microsoft Dynamics 365 for Finance and Operations on finantssüsteem, on *organisatsioon* keskne mõiste ja süsteemi seadistus algab organisatsiooni hierarhia konfiguratsioonist. Ettevõtte rahandusasju ja operatsioone saab seejärel jälgida organisatsiooni tasemel ja mis tahes tasemel organisatsiooni hierarhias.

Kuigi teenuses Common Data Service ei ole organisatsiooni hierarhia mõistet, on sellel mõned lahtised kontseptsioonid, nagu müügi kogutulu. Common Data Service’i integratsiooni osana lisatakse organisatsiooni hierarhia andmestruktuur teenusele Common Data Service.

## <a name="data-flow"></a>Andmevoog

Ettevõtte ökosüsteemil, mis koosneb Finance and Operationsist ja Common Data Service’ist, on jätkuvalt organisatsiooni hierarhia. See organisatsiooni hierarhia on loodud Finance and Operationsis, kuid see on informatiivsel ja laiendatavuse eesmärgil esitatud Common Data Service’is. Järgmine illustratsioon näitab organisatsiooni hierarhia teavet, mis on avatud Common Data Service’i ühesuunaline andmevoona Finance and Operationsist teenusesse Common Data Service.

![Ülesehituse tõmmis](media/dual-write-data-flow.png)

## <a name="templates"></a>Mallid

Organisatsiooni hierarhia olemi kaardid on saadaval andmete ühesuunalisel sünkroonimiselt Finance and Operationsist teenusesse Common Data Service.

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a>Organisatsiooni hierarhia eesmärkide haldamine

See mall pakub organisatsiooni hierarhia eesmärgi olemi ühesuunalise sünkroonimist Finance and Operationsilt rakendusse Dynamics 365 Customer Engagement.

<!-- ![architecture image](media/dual-write-purpose.png) -->

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
Hierarhia tüüp | \> | msdyn\_hierarchypurposetypename
Hierarhia tüüp | \> | msdyn\_hierarchytype.msdyn\_name
Hierarhia eesmärk | \>\> | msdyn\_hierarchypurpose
Muudetamatu | \>\> | msdyn\_immutable
Sea vaikeväärtused | \>\> | msdyn\_setasdefault

## <a name="internal-organization-hierarchy-type"></a>Organisatsiooni hierarhia tüüp

See mall pakub organisatsiooni hierarhia tüübi olemi ühesuunaline sünkroonimine Finance and Operations kliendi kaasamine.

<!-- ![architecture image](media/dual-write-type.png) -->

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
NIMI | \> | msdyn\_nimi

## <a name="internal-organization-hierarchy"></a>Organisatsiooni hierarhia

See mall pakub organisatsiooni hierarhia eesmärgi olemi ühesuunaline sünkroonimine Finance and Operations kliendi kaasamine.

<!-- ![architecture image](media/dual-write-organization.png) -->

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
Kehtib | \> | msdyn\_validto
Kehtivuse algus | \> | msdyn\_validfrom
Hierarhia tüüp | \> | msdyn\_hierarchytypename
Peaorganisatsiooni partii number | \> | msdyn\_parentpartyid
Alamorganisatsiooni partii number | \> | msdyn\_childpartyid
Hierarhia tüüp | \> | msdyn\_hierarchytypeid.msdyn\_name
Alamorganisatsiooni partii number | \> | msdyn\_childid.msdyn\_partynumber
Peaorganisatsiooni partii number | \> | msdyn\_parentid.msdyn\_partynumber

## <a name="internal-organization"></a>Sisemine korraldus

Sisemine organisatsiooniteave Common Data Service’is pärineb kahest Finance and Operationsi üksusest: **tootmisüksus** ja **juriidilised isikud**.

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a>Tootmisüksus

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
keel | \> | msdyn\_languageid
Nime pseudonüüm | \> | msdyn\_namealias
NIMI | \> | msdyn\_nimi
Osapoole number | \> | msdyn\_partynumber
Tootmisüksuse tüüp | \>\> | msdyn\_tüüp

### <a name="legal-entity"></a>Juriidiline isik

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
Nime pseudonüüm | \> | msdyn\_namealias
keel | \> | msdyn\_languageid
NIMI | \> | msdyn\_nimi
Osapoole number | \> | msdyn\_partynumber
Pole | \>\> | msdyn\_tüüp
Juriidilise isiku ID | \> | msdyn\_companycode

## <a name="company"></a>Ettevõte

Pakub juriidilise isiku (ettevõtte) teabe kahesuunalist sünkroonimist Finance and Operationsi ja Customer Engagementi vahel.

<!-- ![architecture image](media/dual-write-company.png) -->

Lähteväli | Kaardi tüüp | Sihtväli
---|---|---
NIMI | = | cdm\_name
Juriidilise isiku ID | = | CDM\_companycode
