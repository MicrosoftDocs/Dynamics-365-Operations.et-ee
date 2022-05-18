---
title: Mis on Dynamics 365 Human Resourcesis uut või mida on muudetud (20. september 2021)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 20. septembri 2021 uusi või muutunud funktsioone.
author: marcelbf
ms.date: 09/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a3fd8705c7735cb3c0945f71651fafa767a7addf
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691578"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-20-2021"></a>Mis on Dynamics 365 Human Resourcesis uut või mida on muudetud (20. september 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse rakenduse Microsoft Dynamics 365 Human Resources uusi, muutunud või peatselt tulevaid funktsioone.

Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2021. aasta 2. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.4464.

### <a name="new-features"></a>Uued funktsioonid

Selle väljalaskega tulevad üldiselt kättesaadavaks järgmised funktsioonid.

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
|---|---|---|
| Lihtsustatud palgaintegratsiooni (palgaarvestuse integratsiooni API-d) lubamine | [Lihtsustatud integreerimise lubamine palgaarvestuse pakkujatega](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Palgaarvestuse integratsiooni API](hr-admin-integration-payroll-api-introduction.md) |
| Lubage töötajate märkimine kui valmis maksmiseks | [Lubage töötajate märkimine kui valmis maksmiseks](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Maksmiseks valmis](/dynamics365/human-resources/hr-compensation-payroll) |

### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime värskendada seda teemat, et lisada sellesse versioonijärku pärast selle teema esialgset avaldamist tehtud veaparandusi.

| Väljaande number | Probleem | Kirjeldus |
|---|---|---|
| 619774 | Aadressi kirjelduse redigeerimine ei sünkrooni reaalajas Dataversei. | Töötaja aadressi kirjelduse redigeerimisel ei sünkroonita uuendatud kirjeldust reaalajas Dataversei. Uuenduste saatmiseks värskendati **Logistika asukoha** tabelis kordustellimust. |
| 614603| Tõrge lehel **Töötaja**, kui **Töötaja personalitoimingute** parameeter pole valitud. | Uue töötaja palkamisel või **Töötaja** lehel navigeerides kuvatakse järgmine tõrge: "Välja **Personali toimingu tüüp** peab olema täidetud", isegi kui **Personali toimingud** on välja lülitatud. |
| 615367 | **Kinnitatud vaba aeg** väljal kuvatakse hoiatus ja kuvatakse valesti. | Kui puhkuse ühikuks on määratud **Päevad**, enne kui lubate funktsiooni **Konfigureeri puhkuseühikud puhkuse tüübi kohta**, kuvab vahekaart **Kinnitatud vaba aeg** välja valed hoiatused ja valed veerud. |


## <a name="in-preview"></a>Eelvaates

Järgmised uued funktsioonid on eelversioonis. Lisateavet funktsioonide sisse- või väljalülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
|---|---|---|
| Soodustuse halduse tööruum | [Soodustuste halduse tööruum (eelversioon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Soodustuse halduse tööruum](hr-benefits-management-workspace.md) |
| Kohandatud väljad jaotises Sobilikkus |[Kohandatud väljade tugi kõlblikkuse töötlemises](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Kohandatud väljade kasutamine kõlblikkuse töötlemises](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |
| Eeliste avaldus |[Soodustuste väljavõte](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) | [Eeliste avaldus](hr-benefits-statement.md) |

### <a name="benefits-statement-known-issues"></a>Soodustuste väljavõtte teadaolevad probleemid

| Probleem | Kirjeldus |
|---|---|
| **Aruandeparameetrite** leht **Töötaja iseteeninduses** soodustuste väljavõtete jaoks on vale. | Kui navigeerite **Soodustuste väljavõtetele** **Töötaja iseteeninduses**, kuvatakse **Aruande parameetrid** lehel **Kaasatavad kirjed** ja **Jookse taustal** Kiirklahvid .  Need tuleb eemaldada. |
| **Aruande parameetrite** lehel kuvatakse soodustuste väljavõtete suletud ja tulevased perioodid. | **Soodustuste väljavõtete** aruande sihtlehele liikudes saab kasutaja valida suletud või tulevase kuupäevaga soodustusplaanide perioode, mille tulemuseks on tühi lehekülg. Loendis peaks kuvama ainult praeguse soodustuse plaani perioodi. |
|Viga aruannete saatmisel GER aruande sihtkoha abil. | Soodustuste avalduse saab seadistada kasutama e-posti parameetreid **GER aruande sihtpunktide** lehel. Kui olete seadistuse ja aruande printimise lõpule viinud, saab kasutaja vormingu tõrketeate ja soodustuste aruannet ei saadeta.|


## <a name="coming-soon"></a>Peagi tulekul

Plaanitud funktsioonide täieliku loendi ja nende kavandatud väljaannete kohta leiate teavet teemast [Dynamics 365 Human Resourcesi 2021. aasta 2. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funktsioon | Details |
|---|---|
| Platvormi värskendus 10.0.21 (45) | Platvormi värskendus 10.0.21 välja laskmine on kavandatud algama teenuseväljalaskega 4. oktoobril 2021. Lisateavet vt Platvormi värskendustest [versioonile 10.0.21 Finance and Operations rakendustest (oktoober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
|Jõudluse töölehe laiendatud aruannete vaade | See funktsioon lubatakse vaikimisi järgmises väljapööramises. |


## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 väljalaskevoo 2 ülevaade](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
