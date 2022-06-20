---
title: Mis on Dynamics 365 Human Resourcesis uut või mida on muudetud (5. oktoober 2021)
description: See artikkel kirjeldab funktsioone, mis on uued või microsoftis Dynamics 365 Human Resources muudetud 5. oktoober 2021 jaoks.
author: marcelbf
ms.date: 10/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cc8cd8616f1b82258fccbb2b41d5e72a90aaed63
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845108"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-5-2021"></a>Mis on Dynamics 365 Human Resourcesis uut või mida on muudetud (5. oktoober 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab funktsioone, mis on Microsoftis uued, muutunud või tulevad varsti Dynamics 365 Human Resources.

Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2021. aasta 2. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.4485.

### <a name="new-features"></a>Uued funktsioonid

Selle väljalaskega tulevad üldiselt kättesaadavaks järgmised funktsioonid.

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
|---|---|---|
| Platvormi värskendus 10.0.21 (45) | -- | [Platvormi värskendused versioonile 10.0.21 Finantside ja toimingute rakendustele (oktoober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21) |


### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime seda artiklit värskendada, et kaasata vigaparandused, mis muutsid selle pärast selle artikli algset avaldamist koostesse.

| Väljaande number | Probleem | Kirjeldus |
|---|---|---|
| 598896 | Töötaja summat ei kuvata enne, kui töötaja on registreerimise lõpetanud | Lehel **Töötaja iseteenindus** ei kuvatud töötaja hüvitise summat. Töötaja hüvitise summa kuvatakse nüüd lehel **Hüvitiste iseteenindus**.  |
| 613440 | **Andmehaldusest** ei saa andmeid eksportida | Andmete eksportimisel **Andmehalduse** projekti jaoks nurjub eksport ootamatult. |
| 618327 | **Aruande parameetrite** lehel kuvatakse soodustuste väljavõtete suletud ja tulevased perioodid | Kui navigeerite **Soodustuste väljavõtetele** **Töötaja iseteeninduses**, kuvatakse **Aruande parameetrid** lehel **Kaasatavad kirjed** ja **Jookse taustal** Kiirklahvid . Need jaotised eemaldati.|
| 618326 | Soodustuste väljavõtete puhul kuvatakse vale **Aruandeparameetrite** leht **Töötaja iseteeninduses**| **Soodustuste väljavõtete** aruande sihtlehele liikudes saab kasutaja valida suletud või tulevase kuupäevaga soodustusplaanide perioode, mille tulemuseks on tühi lehekülg. Loendis peaks kuvama ainult praeguse soodustuse plaani perioodi. |

## <a name="in-preview"></a>Eelvaates

Järgmised uued funktsioonid on eelversioonis. Lisateavet funktsioonide sisse- või väljalülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
|---|---|---|
| Soodustuse halduse tööruum | [Soodustuste halduse tööruum (eelversioon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Soodustuse halduse tööruum](hr-benefits-management-workspace.md) |
| Kohandatud väljad jaotises Sobilikkus |[Kohandatud väljade tugi kõlblikkuse töötlemises](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Kohandatud väljade kasutamine kõlblikkuse töötlemises](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |
| Eeliste avaldus |[Soodustuste väljavõte](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) | [Soodustuste avaldus](hr-benefits-statement.md) |

### <a name="benefits-statement-known-issues"></a>Soodustuste väljavõtte teadaolevad probleemid

| Probleem | Kirjeldus |
|---|---|
|Viga aruannete saatmisel **GER aruande sihtkoha** abil | Soodustuste avalduse saab seadistada kasutama e-posti parameetreid **GER aruande sihtpunktide** lehel. Kui olete seadistuse ja aruande printimise lõpule viinud, saab kasutaja vormingu tõrketeate ja soodustuste aruannet ei saadeta.|

## <a name="feature-management-changes"></a>Funktsioonihalduse muutused

| Funktsioon | Kirjeldus |
|---|---|
|Jõudluse töölehe laiendatud aruannete vaade | See funktsioon lubatakse vaikimisi käesolevas väljalaskes. |

## <a name="coming-soon"></a>Peagi tulekul

Plaanitud funktsioonide täieliku loendi ja nende kavandatud väljaannete kohta leiate teavet teemast [Dynamics 365 Human Resourcesi 2021. aasta 2. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funktsioon | Üksikasjad |
|---|---|
| Platvormi värskendus 10.0.22 (46) | Platvormi värskendus 10.0.22 välja laskmine on kavandatud algama teenuseväljalaskega 1. novembril 2021. Lisateavet vt Platvormi värskendustest [versioonile 10.0.22 Finance and Operations rakendustest (november 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22). |



## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 väljalaskevoo 2 ülevaade](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
