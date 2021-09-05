---
title: Varude nähtavuse lisandmooduli ülevaade
description: See teema selgitab mis Varude nähtavus on ja kirjeldab selle funktsioone.
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: defbcdc7ada4471345f8c728522e15f16a8bec8f
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344284"
---
# <a name="inventory-visibility-add-in-overview"></a>Varude nähtavuse lisandmooduli ülevaade

[!include [banner](../includes/banner.md)]

Varude nähtavuse lisandmoodul (mida nimetatakse ka *Varude nähtavuseks*) on sõltumatu ja väga muutuv mikroteenus, mis võimaldab reaalajas vaba kaubavaru jälgimist. Seega annab see varudest globaalse ülevaate.

Välised süsteemid pääsevad teenusesse läbi RESTful API-de. Sel viisil saavad nad teha päringuid antud dimensioonikomplektide vaba kaubavaru kohta või teha laoseisus muudatusi erinevates kohandatud andmeallikates.

Microsoft Dataverse'ile loodud mikroteenusena pakub Varude nähtavus laiendatavust. Saate rakenduste loomiseks kasutada Power Appsi. Saate rakendada ka Power BI-d, et pakkuda teie ärivajadustele vastavat kohandatud funktsionaalsust.

Varude nähtavuse saate integreerida mitme kolmanda osapoole süsteemiga, seadistades standardiseeritud varude dimensioonide konfiguratsiooni valikud ja seadistades kandetüübid. Varude nähtavus toetab ka kohandatud laiendatavust konfigureeritavate arvutatud koguste kaudu.

## <a name="supported-features"></a>Toetatud funktsioonid

### <a name="inventory-visibility-integration-with-dynamics-365-supply-chain-management"></a>Inventory Visibility integratsioon rakendusega Dynamics 365 Supply Chain Management

Integreeritud lahendus tõmbab varude andmeid rakendusest Dynamics 365 Supply Chain Management ja jälgib pidevalt varude muutusi. Lisateavet vt teemast [Varude nähtavuse seadistamine](inventory-visibility-setup.md).

### <a name="get-a-global-view-of-inventory"></a>Varude globaalse ülevaate saamine

Integreeritud lahendus võimaldab teil määratleda oma andmeallikad ja tsentraliseerida varude andmed. Lisateavet vt teemast [Varude nähtavuse konfigureerimine](inventory-visibility-configuration.md).

Varude vaatamisele on kaks lähenemist.

- Päringu esitamine suure jõudlusega API kaudu. See API võib tagastada peaaegu reaalajas laoandmed otse vahemällu talletatud eksemplarist. Lepinguid ja näidiseid leiate varude jaotisest [Varude nähtavuse avalikud APId](inventory-visibility-api.md).
- Vaba kaubavaru loendi vaatamine. See loend sünkroonitakse perioodiliselt vahemällu talletatud eksemplarist ja see on nähtav Dataverse'is. Lisateavet vt teemast [Varude nähtavuse rakendus](inventory-visibility-power-platform.md).

### <a name="soft-reservations"></a>Esialgsed reserveeringud

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Esialgne reserveerimine kehtib juhul, kui ettevõte peab reserveerima konkreetse koguse tooteid, et toetada näiteks müügitellimuse täitmist, mis väldib ülemüümist. Kui müügitellimus luuakse ja kinnitatakse rakenduses Supply Chain Management või muudes tellimuste halduse süsteemides, saadetakse Varude nähtavusse taotlus koguse reserveerimiseks. Varude nähtavus võimaldab teil reserveerida tooted, millel on dimensiooni üksikasjad ja konkreetsed kandetüübid. (Lisateavet vt teemast [Varude nähtavuse rakendus](inventory-visibility-power-platform.md).) Pärast koguse edukat reserveerimist tagastatakse reserveerimise ID. Selle reserveeringu ID abil saate linkida tagasi originaaltellimusele rakenduses Supply Chain Management või muudele tellimuste halduse süsteemidele.

Funktsionaalsus on loodud nii, et Varude nähtavuse reserveering ei muuda kogust. Selle asemel reserveeritud kogus ainult märgistatakse. (Seetõttu nimetatakse seda *esialgseks reserveerimiseks*.) Esialgse reserveeringu kogust saab tasakaalustada, kui rakenduses Supply Chain Management või kolmanda osapoole süsteemis tooteid tarbitakse, kutsudes API uuesti koguse lahutamiseks ja Varade nähtavuses koguse värskendamiseks. Lisateavet vt teemast [Varude nähtavuse reserveeringud](inventory-visibility-reservations.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
