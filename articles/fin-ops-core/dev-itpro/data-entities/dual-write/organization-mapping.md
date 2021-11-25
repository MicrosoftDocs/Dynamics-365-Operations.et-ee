---
title: Organisatsiooni hierarhia teenuses Dataverse
description: Siin peatükis kirjeldatakse organisatsiooni andmete integratsiooni Finance and Operations i rakenduste ja teenuse Dataverse vahel.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: c7ef3a11817d60343503c80d89493262711524b1
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782304"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organisatsiooni hierarhia teenuses Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Kuna Dynamics 365 Finance on finantssüsteem, on *organisatsioon* keskne mõiste ja süsteemi seadistus algab organisatsiooni hierarhia konfiguratsioonist. Ettevõtte rahandusasju saab seejärel jälgida organisatsiooni tasemel ja mis tahes tasemel organisatsiooni hierarhias.

Kuigi teenuses Dataverse ei ole organisatsiooni hierarhia mõistet, on sellel mõned lahtised kontseptsioonid, nagu müügi kogutulu. Dataverse’i integratsiooni osana lisatakse organisatsiooni hierarhia andmestruktuur teenusele Dataverse.

## <a name="data-flow"></a>Andmevoog

Ettevõtte ökosüsteemil, mis koosneb Finance and Operations i rakendustest ja Dataverse’ist, on jätkuvalt organisatsiooni hierarhia. See organisatsiooni hierarhia on loodud Finance and Operations i rakendustes, kuid see on informatiivsel ja laiendatavuse eesmärgil esitatud Dataverse’is. Järgmine illustratsioon näitab organisatsiooni hierarhia teavet, mis on avatud Dataverse’i ühesuunalise andmevoona Finance and Operations i rakendustest teenusesse Dataverse.

![Ülesehituse pilt.](media/dual-write-data-flow.png)

Organisatsiooni hierarhia tabeli kaardid on saadaval andmete ühesuunalisel sünkroonimiselt Finance and Operations i rakendustest teenusesse Dataverse.

## <a name="templates"></a>Mallid

Toote teave sisaldab kogu teavet, mis on seotud tootega ja selle määratlusega, nagu tootedimensioonid või jälgimis- ja laoala dimensioonid. Nagu järgmine tabel näitab, luuakse tabeli kaartide kogum, et sünkroonida tooteid ja seotud teavet.

Finance and Operations rakendused | Klientide kaasamise rakendused     | Kirjeldus
-----------------------|--------------------------------|---
[Juriidilised isikud](mapping-reference.md#102) | cdm_companies | Tagab juriidilise isiku (ettevõtte) teabe kahesuunalise sünkroonimise.
[Juriidilised isikud](mapping-reference.md#142) | msdyn_internalorganizations |
[Tootmisüksus](mapping-reference.md#143) | msdyn_internalorganizations |
[Organisatsioonihierarhia – avaldatud](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | See mall tagab avaldatud organisatsiooni hierarhia tabeli ühesuunalise sünkroonimise.
[Organisatsiooni hierarhia eesmärgid](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | See mall tagab organisatsiooni hierarhia eesmärgi tabeli ühesuunalise sünkroonimise.
[Organisatsiooni hierarhia tüüp](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | See mall tagab organisatsiooni hierarhia tüübi tabeli ühesuunalise sünkroonimise.

## <a name="internal-organization"></a>Sisemine korraldus

Sisemine organisatsiooniteave Dataverse’is pärineb kahest tabelist: **Tootmisüksus** ja **Juriidilised isikud**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
