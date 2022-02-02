---
title: Varude nähtavuse lisandmooduli ülevaade
description: See teema selgitab mis Varude nähtavus on ja kirjeldab selle funktsioone.
author: yufeihuang
ms.date: 10/26/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8871d10dac9103f17780989bc547b6c20ba79b76
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985541"
---
# <a name="inventory-visibility-add-in-overview"></a>Varude nähtavuse lisandmooduli ülevaade

[!include [banner](../includes/banner.md)]

Varude nähtavuse lisandmoodul (mida nimetatakse ka *Varude nähtavuseks*) on sõltumatu ja väga muutuv mikroteenus, mis võimaldab reaalajas vaba kaubavaru jälgimist. Seega annab see varudest globaalse ülevaate.

Välised süsteemid pääsevad teenusesse läbi RESTful API-de. Sel viisil saavad nad teha päringuid antud dimensioonikomplektide vaba kaubavaru kohta või teha laoseisus muudatusi erinevates kohandatud andmeallikates.

Microsoft Dataverse'ile loodud mikroteenusena pakub Varude nähtavus laiendatavust. Saate rakenduste loomiseks kasutada Power Appsi. Saate rakendada ka Power BI-d, et pakkuda teie ärivajadustele vastavat kohandatud funktsionaalsust.

Varude nähtavuse saate integreerida mitme kolmanda osapoole süsteemiga, seadistades standardiseeritud varude dimensioonide konfiguratsiooni valikud ja seadistades kandetüübid. Varude nähtavus toetab ka kohandatud laiendatavust konfigureeritavate arvutatud koguste kaudu.

## <a name="inventory-visibility-integration-with-dynamics-365-supply-chain-management"></a>Inventory Visibility integratsioon rakendusega Dynamics 365 Supply Chain Management

Integreeritud lahendus tõmbab varude andmeid rakendusest Dynamics 365 Supply Chain Management ja jälgib pidevalt varude muutusi. Lisateabe saamiseks vt [Inventory Visibility installimine ja seadistamine](inventory-visibility-setup.md) ning [Inventory Visibility konfigureerimine](inventory-visibility-configuration.md).

## <a name="get-a-global-view-of-inventory"></a>Varude globaalse ülevaate saamine

Integreeritud lahendus võimaldab teil määratleda oma andmeallikad ja tsentraliseerida varude andmed. Lisateavet vt teemast [Inventory Visibility konfigureerimine](inventory-visibility-configuration.md).

Varude vaatamisele on kaks lähenemist.

- Päringu esitamine suure jõudlusega API kaudu. See API võib tagastada peaaegu reaalajas laoandmed otse vahemällu talletatud eksemplarist. Lepinguid ja näidiseid leiate varude jaotisest [Varude nähtavuse avalikud APId](inventory-visibility-api.md).
- Vaba kaubavaru loendi vaatamine. See loend sünkroonitakse perioodiliselt vahemällu talletatud eksemplarist ja see on nähtav Dataverse'is. Lisateavet vt teemast [Varude nähtavuse rakendus](inventory-visibility-power-platform.md).

## <a name="soft-reservations"></a>Esialgsed reserveeringud

Esialgne reserveerimine kehtib juhul, kui ettevõte peab reserveerima konkreetse koguse tooteid, et toetada näiteks müügitellimuse täitmist, mis väldib ülemüümist. Kui müügitellimus luuakse ja kinnitatakse rakenduses Supply Chain Management või muudes tellimuste halduse süsteemides, saadetakse Varude nähtavusse taotlus koguse reserveerimiseks. Varude nähtavus võimaldab teil reserveerida tooted, millel on dimensiooni üksikasjad ja konkreetsed kandetüübid. (Lisateavet vt teemast [Varude nähtavuse rakendus](inventory-visibility-power-platform.md).) Pärast koguse edukat reserveerimist tagastatakse reserveerimise ID. Selle reserveeringu ID abil saate linkida tagasi originaaltellimusele rakenduses Supply Chain Management või muudele tellimuste halduse süsteemidele.

Funktsionaalsus on loodud nii, et Varude nähtavuse reserveering ei muuda kogust. Selle asemel reserveeritud kogus ainult märgistatakse. (Seetõttu nimetatakse seda *esialgseks reserveerimiseks*.) Esialgse reserveeringu kogust saab tasakaalustada, kui rakenduses Supply Chain Management või kolmanda osapoole süsteemis tooteid tarbitakse, kutsudes API uuesti koguse lahutamiseks ja Varade nähtavuses koguse värskendamiseks. Lisateavet vt teemast [Varude nähtavuse reserveeringud](inventory-visibility-reservations.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
