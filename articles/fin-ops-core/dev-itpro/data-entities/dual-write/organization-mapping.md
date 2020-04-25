---
title: Organisatsiooni hierarhia teenusesCommon Data Service
description: Siin peatükis kirjeldatakse organisatsiooni andmete integratsiooni Finance and Operationsi rakenduste ja teenuse Common Data Service vahel.
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
ms.openlocfilehash: fc5db8d04a2860df0c917816e2910c6fbda941ff
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173150"
---
# <a name="organization-hierarchy-in-common-data-service"></a>Organisatsiooni hierarhia teenusesCommon Data Service

[!include [banner](../../includes/banner.md)]



Kuna Dynamics 365 Finance on finantssüsteem, on *organisatsioon* keskne mõiste ja süsteemi seadistus algab organisatsiooni hierarhia konfiguratsioonist. Ettevõtte rahandusasju saab seejärel jälgida organisatsiooni tasemel ja mis tahes tasemel organisatsiooni hierarhias.

Kuigi teenuses Common Data Service ei ole organisatsiooni hierarhia mõistet, on sellel mõned lahtised kontseptsioonid, nagu müügi kogutulu. Common Data Service’i integratsiooni osana lisatakse organisatsiooni hierarhia andmestruktuur teenusele Common Data Service.

## <a name="data-flow"></a>Andmevoog

Ettevõtte ökosüsteemil, mis koosneb Finance and Operationsi rakendustest ja Common Data Service’ist, on jätkuvalt organisatsiooni hierarhia. See organisatsiooni hierarhia on loodud Finance and Operationsi rakendustes, kuid see on informatiivsel ja laiendatavuse eesmärgil esitatud Common Data Service’is. Järgmine illustratsioon näitab organisatsiooni hierarhia teavet, mis on avatud Common Data Service’i ühesuunalise andmevoona Finance and Operationsi rakendustest teenusesse Common Data Service.

![Ülesehituse tõmmis](media/dual-write-data-flow.png)

## <a name="templates"></a>Mallid

Organisatsiooni hierarhia olemi kaardid on saadaval andmete ühesuunalisel sünkroonimiselt Finance and Operationsi rakendustest teenusesse Common Data Service.

## <a name="templates"></a>Mallid

Toote teave sisaldab kogu teavet, mis on seotud tootega ja selle määratlusega, nagu tootedimensioonid või jälgimis- ja laoala dimensioonid. Nagu järgmine tabel näitab, luuakse olemikaartide kogum, et sünkroonida tooteid ja seotud teavet.

Finance and Operations rakendused | Muud Dynamics 365 rakendused | Kirjeldus
-----------------------|--------------------------------|---
Organisatsiooni hierarhia eesmärgid | msdyn_internalorganizationhierarchypurposes | See mall tagab organisatsiooni hierarhia eesmärgi üksuse ühesuunalise sünkroonimise.
Organisatsiooni hierarhia tüüp | msdyn_internalorganizationhierarchytypes | See mall tagab organisatsiooni hierarhia tüübi üksuse ühesuunalise sünkroonimise.
Organisatsiooni hierarhia – avaldatud | msdyn_internalorganizationhierarchies | See mall tagab avaldatud organisatsiooni hierarhia üksuse ühesuunalise sünkroonimise.
Tootmisüksus | msdyn_internalorganizations | 
Juriidilised isikud | msdyn_internalorganizations | 
Juriidilised isikud | cdm_companies | Tagab juriidilise isiku (ettevõtte) teabe kahesuunalise sünkroonimise.


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a>Sisemine korraldus

Sisemine organisatsiooniteave Common Data Service’is pärineb kahest üksusest: **tootmisüksus** ja **juriidilised isikud**.

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]

