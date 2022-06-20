---
title: Mis on uut või muutunud Dynamics 365 Human Resources 19. novembris 2021
description: See artikkel kirjeldab funktsioone, mis on kas uued või muutunud autonoomses Microsoftis Dynamics 365 Human Resources 19. novembriks 2021.
author: marcelbf
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d3e08432a4ce4d73cd67ad839191abe9f6e691a6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886069"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-november-19-2021"></a>Mis on uut või muutunud Dynamics 365 Human Resources 19. novembris 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab funktsioone, mis on Microsoftis uued, muutunud või tulevad varsti Dynamics 365 Human Resources.

Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende oodatavate üldiste kättesaadavuse kuupäevade kohta vt [Dynamics 365 Human Resources 2021. väljalaske voost 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See vabastamine sisaldab järgmisi veaparandusi. Muudatused rakenduvad versioonile number 8.1.4591.

### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime seda artiklit värskendada, et kaasata vigaparandused, mis muutsid selle pärast selle artikli algset avaldamist koostesse.

| Väljaande number | Probleem | Kirjeldus |
|---|---|---|
| 626178 | Navigeerimine puudub juhataja iseteeninduse töötaja paanidelt **.** | See probleem on nüüd lahendatud. Navigeerimine on saadaval, et vaadata aruande üksikasju juhataja **iseteeninduses**. |
| 632573 | Kursuse salvestamisel ilmnes kinnitamistõrge **.** | See probleem on nüüd lahendatud. Kui loote kursuse, mille minimaalne **osalejate** arv on suurem kui 0, **lubati** siiski salvestada ka siis, kui maksimaalne osalejate arv on 0. |
| 615955 | Tõrge "Välja **eesmärk** peab olema täidetud" uue värbamistaotluse asukoha loomisel. | Uue värbamistaotluse asukoha aadressi loomisel kuvatakse tõrge: väli Eesmärk peab olema täidetud. Leheküljel pole **väli** Eesmärk saadaval. |
| 620797 | Tühi **sugu välja** tõrge on eksitavad | Kui isiklikule kontaktile ei sisestata sugu, kuvatakse aruandes tekst sisestamiseks "Klõpsa või puudu siin" – see on eksitava, kuna väljale ei saa midagi sisestada. |
| 620800 | Soodustuste väljavõtte link on peidetud. | Soodustusaruanne pole töötaja iseteeninduses **vaikimisi kuvatav**.  Link lisati jaotises Lingid töötaja iseteeninduse **paremale** **poolele**. |
| 629778 | Jõudluse probleem CDS-integratsiooniga. | Autoriseerimisega seotud taotlus põhjustas jõudluse probleemi. |

## <a name="in-preview"></a>Eelvaates

Järgmised uued funktsioonid on eelversioonis. Lisateavet funktsioonide sisse- või väljalülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
|---|---|---|
| Soodustuse halduse tööruum | [Soodustuste halduse tööruum (eelversioon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Soodustuse halduse tööruum](hr-benefits-management-workspace.md) |


## <a name="coming-soon"></a>Peagi tulekul
Plaanitud funktsioonide ja nende [plaanitud väljalasete täieliku loendi leiate Dynamics 365 ja tööstus pilvedest: 2021. väljalaske voost 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
