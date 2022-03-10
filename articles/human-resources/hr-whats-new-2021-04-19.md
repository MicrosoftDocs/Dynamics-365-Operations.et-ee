---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (19. aprill, 2021)?
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 19. aprill 2021 uusi või muutunud funktsioone.
author: marcelbf
ms.date: 04/19/2021
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
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fadad34be31f6522654bc3af47a4f71695dcc5fea7f0b3e760ff26d79d88eb4c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722507"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-19-2021"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (19. aprill, 2021)?

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi, muutunud või peatselt tulevaid funktsioone.

Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2021. aasta 1. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.4113.

### <a name="new-features"></a>Uued funktsioonid

Selle väljalaskega tulevad üldiselt kättesaadavaks järgmised funktsioonid.

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Platvormi värskendus 10.0.17 (41) | -- | [Platvormi uuendamine versioonile 10.0.17 Finance and Operations rakenduste puhul (aprill 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md) |
| Kohandatud väljade tugi soodustuste halduse vormidel | [Kohandatud väljade tugi soodustuste halduses](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management)| [Soodustuste halduse ülevaade](hr-benefits-management-overview.md)|

### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime värskendada seda teemat, et lisada sellesse versioonijärku pärast selle teema esialgset avaldamist tehtud veaparandusi.

| Väljaande number | Väljasta |  Kirjeldus |
| --- | --- | --- |
| 552164 | **Töötaja** **iseteeninduse salvestatud vaade > Avatud kursused** ei tööta kursustel, mis sisaldavad päevakorda | Kui avatud kursustel (ESS) kasutatakse salvestatud vaadet ja ühele kursusele on lisatud päevakord, siis ei näita vaade enam selle kursuse kohta mitut rida |
| 560614 | **Soodustused > Elusündmuse valikud** näitavad lahknevusi kohtspikri dokumentatsioonis ja koodi käitumises. | Uuendatud kohtspikkerid **elusündmuse valikutes** korrigeeritud käitumise näitamiseks. |
| 560616 | **Soodustused > Elusündmuste suvandid** on töötaja soodustusplaanis redigeeritavad, kuid muudatusi need ei mõjutata. | Elusündmuse suvandi uuendatud käitumine vahetub olekule "Lubatud" või "Keelatud" sõltuvalt sõltuvate isikute suvanditest; see toimub kohtspikri dokumentatsiooni suhtes. |
| 565054 | Kui laiendatud **juurdepääs** on sees, ei saa vaadata **tööhõiveta** töötajaid. | See lahendab probleemi, kus laiendatud juurdepääs on sisse lülitatud ja ainult süsteemi administraatorid saavad vaadata tööhõiveta **tööhõiveta** **töötajate loendi** sisu. Kuna see parandus on turbemuutus, peate sellega Funktsioonihalduses liituma. Kui funktsioon on sees, näevad vormile juurdepääsu omavad rollid sisu ka siis, kui täpsem juurdepääs on sees. Lisateabe saamiseks vt teemat [Tööhõiveta töötajad](hr-personnel-workers-without-employment.md). |
| 570586 | Taotluse kinnitamisest loobumine nurjub, kui tööleminek lõpeb enne selle töötaja viimast kannet läbi kõikide puhkuseplaanide. | Pärast töösuhte lõppu ei nurju puhkuse taotluse kinnitamine töötaja puhkusekannete tõttu.|
| 570783 | Ettevõtteülese puhkuse lubamine ja keelamine inimressursside jagatud parameetrites muudab seda, mida näevad ühes ettevõttes töötavad isikud puhkusetaotlustes. | Ühes ettevõttes töötavad töötajad ei näe muudatusi aja küsimises, kui parameeter on lubatud või keelatud. |
| 572343 | Nõutud põhjusekoodi ei kuvata, kui ettevõtteülese puhkuse vaate funktsioon on lubatud. | Nõutud põhjusekoodi kuvatakse ootuspäraselt, kui ettevõtteülese puhkuse vaate funktsioon on lubatud. |
| 573676 | Perioodi ei saa **soodustuste haldusse** **> Lingid > Soodustusplaanid** lisada. | Fikseeritud vead, kus **perioodi** ei saanud olemasolevas **soodustusplaani** vormis lisada või värskendada. |

## <a name="in-preview"></a>Eelvaates

Järgmised uued funktsioonid on eelversioonis. Lisateavet funktsioonide sisse- või väljalülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Soodustuse halduse tööruum | [Soodustuste halduse tööruum (eelversioon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Soodustuse halduse tööruum](hr-benefits-management-workspace.md) |
| Puhkuse ja puudumise töövoo kogemuse täiustused | [Puhkuse ja puudumise töövoo kogemuse täiustused](https://go.microsoft.com/fwlink/?linkid=2147528) | [Taotle vaba aega](hr-employee-self-service-request-time-off.md)|
| Lihtsustatud palgaintegratsiooni (palgaarvestuse integratsiooni API-d) lubamine | [Lihtsustatud integreerimise lubamine palgaarvestuse pakkujatega](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Palgaarvestuse integratsiooni API](hr-admin-integration-payroll-api-introduction.md)|

## <a name="coming-soon"></a>Peagi tulekul

| Funktsioon | Details |
| --- | --- |
| Töövoog saab automaatselt heaks kiita juhataja poolt töötajate jaoks sisestatud oskused. | Peagi tulekul. |
| Platvormi värskendus 10.0.18 (42) | Platvormi värskendus 10.0.18 peaks tuleb välja teenuseväljalaske raames 17. mail 2021. Lisateavet leiate teemast [Finance and Operationsi rakenduste versiooni 10.0.18 platvormivärskendused (mai 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18). |
| Kohandatud väljade toe jaoks kvalifitseerumise reeglid soodustuste halduses  | [Kohandatud välja tugi kõlblikkuse töötlemiseks](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

Plaanitud funktsioonide täieliku loendi ja nende kavandatud väljaannete kohta leiate teavet teemast [Dynamics 365 Human Resourcesi 2021. aasta 1. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 väljalaskevoo 1 ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
