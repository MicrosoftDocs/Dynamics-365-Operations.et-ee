---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (22. juuni 2021)
description: See artikkel kirjeldab funktsioone, mis on Dynamics 365 Human Resources microsoftis uued või muutunud 22. juunil 2021.
author: marcelbf
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61c457abf87ce2da554ddb1472512416159c4dca
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068420"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-22-2021"></a>Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (22. juuni 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab funktsioone, mis on uued, muutunud või tulevad varsti Dynamics 365 Human Resources.

Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2021. aasta 1. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.4258.

### <a name="new-features"></a>Uued funktsioonid

Selle väljalaskega tulevad üldiselt kättesaadavaks järgmised funktsioonid.

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Tööhõivefunktsioonita töötajatest teavitamine – kui täpsem juurdepääs on sisse lülitatud ja funktsioonihalduses on funktsioon **Kuva kõik töötajad ilma tööhõiveta** keelatud, kuvatakse töötajatel ilma töösuheteta vorm. Kasutaja omakorda lülitab sisse funktsiooni **Kuva kõik tööhõiveta töötajad**. | Pole kohaldatav| [Töösuhteta töötajad](/dynamics365/human-resources/hr-personnel-workers-without-employment)|
| Kohandatud väljade toe jaoks kvalifitseerumise reeglid soodustuste halduses | [Kohandatud välja tugi kõlblikkuse töötlemiseks](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Sobivuse reeglite konfigureerimine](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| Puhkuse tekkepõhise kande auditeerimine | Pole kohaldatav | [Puhkuse tekkepõhise kande auditeerimine](hr-leave-and-absence-accrue.md)|
| Puhkuse ja puudumise töövoo kogemuse täiustused | [Puhkuse ja puudumise töövoo kogemuse täiustused](https://go.microsoft.com/fwlink/?linkid=2147528) | [Taotle vaba aega](hr-employee-self-service-request-time-off.md)|

### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime seda artiklit värskendada, et kaasata vigaparandused, mis muutsid selle järku pärast selle artikli algset avaldamist.

| Väljaande number | Probleem |  Kirjeldus |
| --- | --- | --- |
| 583052 | Tagasisidet saav kasutaja saab saadud tagasisidet redigeerida | Kui töötaja, kes saab jõudluse töölehelt tagasisidet, valib **Lisa väline link**, muutub vorm redigeeritavaks, lubades töötajal muuta saadud jõudluse tagasisidet. |
| 522281 | Compensation Management tasustruktuuri paanide töötajate arvu valimine annab tulemuseks valed tulemused| Tasuplaanidesse süvitsimineku puhul tasu tööruumist kuvatakse õige arv töötajaid. |
| 580683 | Töötaja ja juhi rollidele määratud kasutajad ei saa lisada märkusi ega värskendada jõudluse töölehte | Töötaja ja juhi rollidele määratud kasutajad ei saa lisada märkusi ega värskendada jõudluse töölehte. Kasutaja saab tõrketeate" "Jõudluse töölehe kandes (HcmPerfJournal) ei saa kirjet luua. Turbepoliitika luba keelati." |
| 583077 | Töötaja sünnikuupäev puhkusel ja puudumiste ettevõtte kalendris näitab valet kuupäeva | Kasutajad saavad vaadata puhkuste ja puudumiste ettevõttekalendri töötajate õiget sünnikuupäeva. |
| 586996 | Kui juurdepääs on piiratud ühe ettevõttega, siis ettevõtteülese puhkuse funktsiooni puhul on saldod tühjad | Kui ettevõtteülene puhkusevaade on lubatud, saavad kasutajad töötaja tulevaste puhkuste saldosid õigesti vaadata. |
| 581014 | Ettevõtetevahelise puhkuse ja puudumise vaate lubamine toob tulevaste saldode vaatamisel kaasa vea | Tõrked on fikseeritud, kui kasutajad vaatasid ettevõtteülese puhkuse kuvaga tulevasi puhkusesaldosid. |
| 509404 | Osakonna töötajate arvu analüüsis ei arvestata töötajate liikumist osakondade vahel. | kui töötaja siirdab need ühest osakonnast teise, ei kajasta osakonna töötajate arvu andmed vana osakonda, kust töötaja praegusel aastal aegunud ametikoha üksikasjade puhul vahetatakse. |
| 584851 | Soodustuskrediidi katsereegel "Pole" ei paku krediiti |Paindkrediidi katsereegli "Pole" tulemusena saavad töötajad soodustusperioodi eest nullkrediiti, sõltumata nende palkamise ajast. See on fikseeritud nii, et töötaja peaks saama täielikud paindkrediidid, kui nad on palgatud enne hüvitisperioodi algust, ja mitte juhul, kui nad palkatakse pärast perioodi algust. |
| 584897 | Kohustuse "Välise põhifunktsiooni kasutamine" dubleerimisel ilmnes tõrge | Kui üritati dubleerida kohustust "Kasuta välist põhifunktsiooni", sai kasutaja tõrke: "Ei leidnud objekti identifikaatoriga UserDefinedAppHostDialogView." |
| 575692 | Ootel töötajate puhul pole lisanduv puhkus ja puudumine saadaval | Kui **Sujuvam töötajakirje** on lubatud, saab tulevaste palkade puhul käivitada puhkuse ja puudumise viitvõlga. |
| 580110 | Ettevõtte lisamine palgaarvestuse integratsiooni lähtestab integratsiooni kasutama kõiki üksusi, isegi kui suvand on seatud projekti värskendamata | Kui klient on eemaldanud üksused või muutnud andmeprojekti palgaarvestuse integreerimiseks ja selle valik on seadistatud tõkestama projekti automaatset värskendamist, ignoreerib uue ettevõtte lisamine integratsiooni sätet ja värskendab projekti.  |
| 584518 |Soodustuste töötlemise jõudluse probleemi registreerimine | See viga lahendas pärandi soodustuste registreerimise protsessis jõudluse probleemid. |

## <a name="in-preview"></a>Eelvaates

Järgmised uued funktsioonid on eelversioonis. Lisateavet funktsioonide sisse- või väljalülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Soodustuse halduse tööruum | [Soodustuste halduse tööruum (eelversioon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Soodustuse halduse tööruum](hr-benefits-management-workspace.md) |
| Lihtsustatud palgaintegratsiooni (palgaarvestuse integratsiooni API-d) lubamine | [Lihtsustatud integreerimise lubamine palgaarvestuse pakkujatega](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Palgaarvestuse integratsiooni API](hr-admin-integration-payroll-api-introduction.md)|


## <a name="coming-soon"></a>Peagi tulekul

| Funktsioon | Details |
| --- | --- |
| Platvormi värskendus 10.0.19 (43) | Platvormi värskendus 10.0.19 peaks tuleb välja teenuseväljalaske raames 28. juuni 2021. Lisateavet vt platvormi värskendustest [versioonile 10.0.19 finantside ja toimingute rakendustest (juuni 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19). |
|  Teenuse aastate kuvamise lüliti | See funktsioon võimaldab kasutada erinevaid kuupäevi, et arvutada teenuseaastaid, mis on kuvatud **Sujuvama töötajakirje** vormis ja **Inimesed** vormis.  See on saadaval Human Resources parameetrites. |
|  Luba puudumiste halduril puhkusi hallata | [Luba puudumiste halduril puhkusi hallata](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |
|  Kindlate puhkusetüüpide manused | See funktsioon võimaldab administraatoritel lubada manuste lisamist konkreetsete puhkusetüüpidega puhkusetaotluste esitamisel. |
|  Puhkuseühikute konfigureerimine puhkusetüübi järgi | See funktsioon võimaldab administraatoritel konfigureerida iga puhkuse tüübi puhkuseühikuid (tunde või päevi).  |
| Lubage töötajate märkimine kui valmis maksmiseks | [Lubage töötajate märkimine kui valmis maksmiseks](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) |

Plaanitud funktsioonide täieliku loendi ja nende kavandatud väljaannete kohta leiate teavet teemast [Dynamics 365 Human Resourcesi 2021. aasta 1. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 väljalaskevoo 1 ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

