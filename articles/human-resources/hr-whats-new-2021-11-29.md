---
title: Mis on uut või muudetud Dynamics 365 Human Resources 19. november 2021
description: Selles teemas kirjeldatakse funktsioone, mis on eraldiseisvas Microsoftis uued või muudetud Dynamics 365 Human Resources 19. novembriks 2021.
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
ms.openlocfilehash: 618d90f95637002f444b334e16d3fef466dda65e
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087470"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-november-19-2021"></a>Mis on uut või muudetud Dynamics 365 Human Resources 19. november 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse rakenduse Microsoft Dynamics 365 Human Resources uusi, muutunud või peatselt tulevaid funktsioone.

Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Uute funktsioonide ja nende eeldatavate üldiste saadavuskuupäevade kohta lisateabe saamiseks vt [Dynamics 365 Human Resources 2021. aasta väljalaskelaine 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljalase sisaldab järgmisi veaparandusi. Muudatused rakenduvad versioonile number 8.1.4591.

### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime värskendada seda teemat, et lisada sellesse versioonijärku pärast selle teema esialgset avaldamist tehtud veaparandusi.

| Väljaande number | Probleem | Kirjeldus |
|---|---|---|
| 626178 | Töötaja paanidel puudub navigeerimine **Juhataja iseteenindus** | See probleem on nüüd lahendatud. Navigeerimine on saadaval, et näha aruande üksikasju **Juhataja iseteenindus**. |
| 632573 | A salvestamisel ei esine kinnitusviga **Kursus** | See probleem on nüüd lahendatud. Kursuse loomisel koos **Minimaalne osalejate arv** 0-st suuremaks lubati siiski salvestada isegi siis, kui **Maksimaalne osalejate arv** on 0. |
| 615955 | Viga "Field **Eesmärk** tuleb uue värbamistaotluse asukoha loomisel täita. | Uue värbamistaotluse asukoha aadressi loomisel kuvatakse tõrketeade: "Välja "Eesmärk" tuleb täita." Siiski, **Eesmärk** väli pole lehel saadaval. |
| 620797 | Tühi **Sugu** välja viga on eksitav | Kui isikliku kontakti jaoks sugu ei ole sisestatud, kuvatakse aruandes teksti "teksti sisestamiseks klõpsake või puudutage siin" – see on eksitav, kuna väljale ei saa midagi sisestada. |
| 620800 | Kasuavalduse link on peidetud | Kasu avaldus ei ole vaikimisi kuvatav **Töötaja iseteenindus**.  Paremale küljele lisati link **Töötaja iseteenindus** all **Lingid** osa |
| 629778 | CDS-i integreerimise jõudluse probleem. | Autoriseerimisega seotud taotlus põhjustas jõudlusprobleemi. |

## <a name="in-preview"></a>Eelvaates

Järgmised uued funktsioonid on eelversioonis. Lisateavet funktsioonide sisse- või väljalülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
|---|---|---|
| Soodustuse halduse tööruum | [Soodustuste halduse tööruum (eelversioon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Soodustuse halduse tööruum](hr-benefits-management-workspace.md) |


## <a name="coming-soon"></a>Peagi tulekul
Kavandatavate funktsioonide ja nende kavandatud väljalasete täieliku loendi vaatamiseks vt [Dynamics 365 ja valdkonna pilved: 2021. aasta väljalaskelaine 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
