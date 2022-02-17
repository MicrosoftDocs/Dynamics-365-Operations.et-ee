---
title: Organisatsiooni hierarhia teenusesDataverse
description: Selles teemas kirjeldatakse organisatsiooniliste andmete integreerimist Finance and Operationsi rakenduste ja teenuse Dataverse vahel.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: afc1b5996667835c460f467526493380aa2d6403
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062082"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organisatsiooni hierarhia teenusesDataverse

[!include [banner](../../includes/banner.md)]



Kuna Dynamics 365 Finance on finantssüsteem, on *organisatsioon* keskne mõiste ja süsteemi seadistus algab organisatsiooni hierarhia konfiguratsioonist. Ettevõtte rahandusasju saab seejärel jälgida organisatsiooni tasemel ja mis tahes tasemel organisatsiooni hierarhias.

Kuigi teenuses Dataverse ei ole organisatsiooni hierarhia mõistet, on sellel mõned lahtised kontseptsioonid, nagu müügi kogutulu. Dataverse’i integratsiooni osana lisatakse organisatsiooni hierarhia andmestruktuur teenusele Dataverse.

## <a name="data-flow"></a>Andmevoog

Ettevõtte ökosüsteemil, mis koosneb Finance and Operationsi rakendustest ja Dataverse’ist, on jätkuvalt organisatsiooni hierarhia. See organisatsiooni hierarhia on loodud Finance and Operationsi rakendustes, kuid see on informatiivsel ja laiendatavuse eesmärgil esitatud Dataverse’is. Järgmine illustratsioon näitab organisatsiooni hierarhia teavet, mis on avatud Dataverse’i ühesuunaline andmevoona Finance and Operationsi rakendustest teenusesse Dataverse.

![Ülesehituse pilt.](media/dual-write-data-flow.png)

Organisatsioonihierarhia tabelikaardid on saadaval andmete ühesuunalise sünkroonimise jaoks rakendustest Finance and Operations Dataverse.

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
