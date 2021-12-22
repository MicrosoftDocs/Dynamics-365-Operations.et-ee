---
title: Mis on uut või muutunud Dynamics 365 Human Resources 19. novembris 2021
description: Selles teemas kirjeldatakse funktsioone, mis on microsoftis uued või muutunud Dynamics 365 Human Resources 19. novembriks 2021.
author: marcelbf
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3a86c1c24fbc758f4e3d0fd8b052e02078bee41e
ms.sourcegitcommit: 88f8a0369ce66b82314db9639491b695e18a7e5c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902968"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-november-19-2021"></a>Mis on uut või muutunud Dynamics 365 Human Resources 19. novembris 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse rakenduse Microsoft Dynamics 365 Human Resources uusi, muutunud või peatselt tulevaid funktsioone.

Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende oodatavate üldiste kättesaadavuse kuupäevade kohta vt [Dynamics 365 Human Resources 2021. väljalaske voost 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See vabastamine sisaldab järgmisi veaparandusi. Muudatused rakenduvad versioonile number 8.1.4591.

### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime värskendada seda teemat, et lisada sellesse versioonijärku pärast selle teema esialgset avaldamist tehtud veaparandusi.

| Väljaande number | Probleem | Kirjeldus |
|---|---|---|
| 626178 | Navigeerimine puudub juhataja iseteeninduse töötaja **paanidelt.** | See probleem on nüüd lahendatud. Navigeerimine on saadaval, et vaadata aruande üksikasju juhataja **iseteeninduses**. |
| 632573 | Kursuse salvestamisel ilmnes **kinnitamistõrge.** | See probleem on nüüd lahendatud. Kui loote kursuse, mille minimaalne osalejate arv on suurem kui 0, lubati siiski salvestada ka siis, kui maksimaalne osalejate arv **on** **0**. |
| 615955 | Tõrge **"Välja** eesmärk peab olema täidetud" uue värbamistaotluse asukoha loomisel. | Uue värbamistaotluse asukoha aadressi loomisel kuvatakse tõrge: väli Eesmärk peab olema täidetud. Leheküljel **pole** väli Eesmärk saadaval. |
| 620797 | Tühi **sugu välja tõrge on** eksitavad | Kui isiklikule kontaktile ei sisestata sugu, kuvatakse aruandes tekst sisestamiseks "Klõpsa või puudu siin" – see on eksitava, kuna väljale ei saa midagi sisestada. |
| 620800 | Soodustuste väljavõtte link on peidetud. | Soodustusaruanne pole töötaja **iseteeninduses vaikimisi** kuvatav.  Link lisati jaotises Lingid töötaja **iseteeninduse** paremale **poolele**. |
| 629778 | Jõudluse probleem CDS-integratsiooniga. | Autoriseerimisega seotud taotlus põhjustas jõudluse probleemi. |

## <a name="in-preview"></a>Eelvaates

Järgmised uued funktsioonid on eelversioonis. Lisateavet funktsioonide sisse- või väljalülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
|---|---|---|
| Soodustuse halduse tööruum | [Soodustuste halduse tööruum (eelversioon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Soodustuse halduse tööruum](hr-benefits-management-workspace.md) |


## <a name="coming-soon"></a>Peagi tulekul
Plaanitud funktsioonide ja nende plaanitud väljalasete täieliku loendi leiate Dynamics 365 ja tööstus [pilvedest: 2021 väljalaske voost](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) 2.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
