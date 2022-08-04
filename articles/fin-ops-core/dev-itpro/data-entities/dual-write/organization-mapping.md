---
title: Organisatsiooni hierarhia teenusesDataverse
description: See artikkel kirjeldab organisatsiooniandmete integreerimist finantside ja toimingute rakenduste ning rakenduste vahel Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 2f900637855bee3e21916652a373c683e6bf1392
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112014"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organisatsiooni hierarhia teenusesDataverse

[!include [banner](../../includes/banner.md)]



Kuna Dynamics 365 Finance on finantssüsteem, *on* organisatsioon põhimõiste ning süsteemi seadistus algab organisatsiooni hierarhia konfigureerimisega. Ettevõtte rahandusasju saab seejärel jälgida organisatsiooni tasemel ja mis tahes tasemel organisatsiooni hierarhias.

Kuigi teenuses Dataverse ei ole organisatsiooni hierarhia mõistet, on sellel mõned lahtised kontseptsioonid, nagu müügi kogutulu. Dataverse’i integratsiooni osana lisatakse organisatsiooni hierarhia andmestruktuur teenusele Dataverse.

## <a name="data-flow"></a>Andmevoog

Ettevõtte tegevus, mis koosneb finantside ja toimingute rakendustest Dataverse ning omab jätkuvalt organisatsiooni hierarhiat. See organisatsiooni hierarhia on loodud finantside ja toimingute rakenduste põhjal, Dataverse kuid seda kasutatakse teabe ja laiendatavuse eesmärgil. Järgmine näide näitab organisatsiooni hierarhia teavet, mida kuvatakse Dataverse ühepoolese andmevoona finantside ja toimingute rakendustest rakendusse Dataverse.

![Ülesehituse pilt.](media/dual-write-data-flow.png)

Organisatsiooni hierarhia tabeli vastekaardid on saadaval ühepoolne andmete sünkroonimiseks finantside ja toimingute rakendustest rakendusse Dataverse.

## <a name="templates"></a>Mallid

Organisatsiooni on grupp inimesi, kes töötavad koos äriprotsessi või eesmärgi saavutamiseks. Organisatsiooni hierarhia kajastab teie ettevõttesse kuuluvate organisatsioonide vahelisi seoseid. Saate määratleda järgmist tüüpi siseorganisatsioonid: juriidilised isikud, tootmisüksused ja töörühmad. Nagu järgmine tabel näitab, luuakse tabelikaartide kogum, et sünkroonida juriidilisi isikuid, tootmisüksusi ja seotud organisatsioonimishierarhia teavet.

Finance and Operations rakendused | Klientide kaasamise rakendused     | Kirjeldus
-----------------------|--------------------------------|---
[Juriidilised isikud](mapping-reference.md#102) | cdm_companies | 
[Juriidilised isikud](mapping-reference.md#142) | msdyn_internalorganizations |
[Tootmisüksus](mapping-reference.md#143) | msdyn_internalorganizations |
[Organisatsioonihierarhia – avaldatud](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | See mall tagab avaldatud organisatsiooni hierarhia tabeli ühesuunalise sünkroonimise.
[Organisatsiooni hierarhia eesmärgid](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | See mall tagab organisatsiooni hierarhia eesmärgi tabeli ühesuunalise sünkroonimise.
[Organisatsiooni hierarhia tüüp](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | See mall tagab organisatsiooni hierarhia tüübi tabeli ühesuunalise sünkroonimise.

## <a name="internal-organization"></a>Sisemine korraldus

Sisemine organisatsiooniteave Dataverse’is pärineb kahest tabelist: **Tootmisüksus** ja **Juriidilised isikud**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

