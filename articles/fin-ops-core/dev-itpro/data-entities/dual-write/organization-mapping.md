---
title: Organisatsiooni hierarhia teenusesDataverse
description: Siin peatükis kirjeldatakse organisatsiooni andmete integratsiooni Finance and Operationsi rakenduste ja teenuse Dataverse vahel.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: e2b652f11db62eb58ffc2ec2fc4322149e7d45d1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680068"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organisatsiooni hierarhia teenusesDataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Kuna Dynamics 365 Finance on finantssüsteem, on *organisatsioon* keskne mõiste ja süsteemi seadistus algab organisatsiooni hierarhia konfiguratsioonist. Ettevõtte rahandusasju saab seejärel jälgida organisatsiooni tasemel ja mis tahes tasemel organisatsiooni hierarhias.

Kuigi teenuses Dataverse ei ole organisatsiooni hierarhia mõistet, on sellel mõned lahtised kontseptsioonid, nagu müügi kogutulu. Dataverse’i integratsiooni osana lisatakse organisatsiooni hierarhia andmestruktuur teenusele Dataverse.

## <a name="data-flow"></a>Andmevoog

Ettevõtte ökosüsteemil, mis koosneb Finance and Operationsi rakendustest ja Dataverse’ist, on jätkuvalt organisatsiooni hierarhia. See organisatsiooni hierarhia on loodud Finance and Operationsi rakendustes, kuid see on informatiivsel ja laiendatavuse eesmärgil esitatud Dataverse’is. Järgmine illustratsioon näitab organisatsiooni hierarhia teavet, mis on avatud Dataverse’i ühesuunalise andmevoona Finance and Operationsi rakendustest teenusesse Dataverse.

![Ülesehituse tõmmis](media/dual-write-data-flow.png)

Organisatsiooni hierarhia tabeli kaardid on saadaval andmete ühesuunalisel sünkroonimiselt Finance and Operationsi rakendustest teenusesse Dataverse.

## <a name="templates"></a>Mallid

Toote teave sisaldab kogu teavet, mis on seotud tootega ja selle määratlusega, nagu tootedimensioonid või jälgimis- ja laoala dimensioonid. Nagu järgmine tabel näitab, luuakse tabeli kaartide kogum, et sünkroonida tooteid ja seotud teavet.

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

Sisemine organisatsiooniteave Dataverse’is pärineb kahest tabelist: **tootmisüksus** ja **juriidilised isikud**.

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
