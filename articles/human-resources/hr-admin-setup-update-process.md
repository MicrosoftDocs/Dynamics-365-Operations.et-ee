---
title: Värskendamisprotsess
description: Microsoft Dynamics 365 Human Resources on tõeline tarkvara teenusena (Saas), mis pakub pidevaid, puutumatuid teenuse uuendusi rakenduse ja platvormi muudatustele.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 267682f4497bacf70f93840a948d0e525dfa4aa1
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092197"
---
# <a name="update-process"></a>Värskendamisprotsess

Microsoft Dynamics 365 Human Resources on tõeline tarkvara teenusena (Saas), mis pakub pidevaid, puutumatuid teenuse uuendusi. Need värskendused sisaldavad nii rakenduse kui ka platvormi muudatusi, mis pakuvad sageli teenuse kriitilist täiustust, sh regulatiivsed uuendused.

## <a name="update-policy"></a>Värskenduspoliitika

Värskendusi antakse välja regulaarselt kõikides keskkondades. Rakenduse Human Resources tugi põhineb [Microsofti elutsükli poliitikal](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), kust leiate terviklikud ja ennustatavad juhised toe saadavuse kohta.

## <a name="release-cadence"></a>Väljaandmise sagedus

Rakenduse Human Resources värskendusi rakendatakse kõigile keskkondadele automaatselt. Human Resources pakub kahte tüüpi väljaandeid.

- **Teenusevärskendused**: iganädalased uuendused, mis sisaldavad veaparandusi ja uusi funktsioone. Teenusevärskendused sisaldavad ka kehtivaid platvormi värskendusi, kui need väljastatakse. Et saada aimu, millal platvormi värskendusi väljastatakse, vt [tabelit 3: Platvormi väljaanded](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases). Iganädalased uuendused antakse tavaliselt välja kolmapäeviti. Lisateavet iganädalaste uuenduste kohta vt teemat [Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new).

    Kõik toetatud andmekeskused uuendatakse iga nädal, kui pole teisiti märgitud. Iganädalased uuendused algavad tavaliselt kolmapäeval ja lõppevad pühapäevaks. USA, Austraalia, Euroopa, Suurbritannia, Aasia ja Kanada piirkonnad sisalduvad iganädalastes uuendustes. 

- **Lahenduse Common Data Service värskendused**: need värskendused toimuvad vastavalt vajadusele ligikaudu iga kuue nädala järel. Need hõlmavad uusi üksusi ja muudatusi olemasolevatele üksustele rakenduses Common Data Service. Need uuendused vabastatakse samadele piirkondadele kui iganädalased uuendused ja neil kulub umbes kuus nädalat, et edastada läbi kõikide andmekeskuste. Lahenduse värskendused võivad, kuid ei pruugi olla vastavuses iganädalaste teenuse uuendustega.

Järgmises tabelis on toodud näidisgraafik.

| Nädal | Värskenduse tüüp |
| --- | --- |
| 1 | Teenusevärskendus (kõik piirkonnad) |
| 2 | Teenusevärskendus (kõik piirkonnad) + lahenduse värskendus (1. nädala piirkonnad) |
| 3 | Teenusevärskendus (kõik piirkonnad) + lahenduse värskendus (2. nädala piirkonnad) |
| 4 | Teenusevärskendus (kõik piirkonnad) + lahenduse värskendus (3. nädala piirkonnad) |
| 5 | Teenusevärskendus (kõik piirkonnad) + lahenduse värskendus (4. nädala piirkonnad) |
| 6 | Teenusevärskendus (kõik piirkonnad) + lahenduse värskendus (5. nädala piirkonnad) |
| 7 | Teenusevärskendus (kõik piirkonnad) + lahenduse värskendus (6. nädala piirkonnad) |
| 8 | Teenusevärskendus (kõik piirkonnad) |

> [!NOTE]
> Kui need on väljastatud, on lahenduse värskendused saadaval kõigis andmekeskustes. Kui te ei soovi, et värskendused edastatakse automaatselt, saate neid värskendusi iga andmekeskuse igas keskkonnas käsitsi rakendada.

Vajadusel pakub rakendus Human Resources ka järgmist tüüpi parandusi.

- **Redaktsioon (kiirparandus)**: veaparandused, mis võivad ilmneda kas koos iganädalase teenuseuuenduse väljalaskega või eraldi

- **Erakorraline parandus**: ennetavad ja uuesti aktiivsed kiirparandused, mis on olemuselt eraldiseisvad, võivad sisaldada ainult konfiguratsiooni või koodi muudatusi, et lahendada avaldatud saidi probleeme, ja need võivad ilmneda iganädalasest teenuseuuenduse väljaandest eraldi

Väljaanded vaadatakse üle, testitakse ja kontrollitakse sisemises keskkonnas. Pärast järkude kinnitamist edastatakse need tootmisse.

## <a name="exceptions-in-2019"></a>Erandid 2019. a

Järgmised kuupäevad on tavalise väljastusgraafiku erandid.

| Kuupäev | Kirjeldus |
| --- | --- |
| 25. novembri nädal | Uuendusi pole |
| 16. detsembri nädal | Ainult väikesed värskendused |
| 23. detsembri nädal | Uuendusi pole |
| 30. detsembri nädal | Uuendusi pole |

## <a name="communications"></a>Suhtlus

Saate teada, mis on rakenduses Human Resources töös ja mida oleme väljastanud, järgmistes asukohtades:

- [Dynamics 365 Human Resourcesi teejuht](https://dynamics.microsoft.com/roadmap/talent/)

- [Dynamics 365 väljalaskeplaanid](https://docs.microsoft.com/dynamics365/release-plans/)

- [Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources?](hr-admin-whats-new.md)

- [Teenuse Lifecycle Services (LCS) teema otsing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (ainult platvormiga seotud vigade jaoks)

- [Rakenduse Human Resources blogi](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [Rakenduse Human Resources Yammeri kogukond](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>Liivakastikeskkonna eelvaatefunktsioonid

Enne nende tootmiskeskkonnas lubamist saate eelvaatefunktsioonid liivakastikeskkonnas kinnitada. Lisateavet funktsioonide lubamise kohta vt [Funktsioonihalduse ülevaade](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Kõik uued funktsioonid jäävad vähemalt 30 päevaks eelvaatesse ja tavaliselt 30–60 päevaks. Peamised funktsioonid on tavaliselt saadaval eelvaate perioodile järgneva iga aasta oktoobris ja aprillis. Kohe kui näete tööruumis Funktsioonihaldus uusi võimalusi, saate need sisse lülitada. Mõned funktsioonid võivad olla vaikimisi sisse lülitatud.

Mõnikord on lahutamatu funktsioon vaikimisi sisse lülitatud ja seda ei saa välja lülitada (nt tööruum Funktsioonihaldus).

Kui funktsioon on üldsusele saadaval, võib selle tootmiskeskkonnas sisse või välja lülitada. Tööruum Funktsioonihaldus näitab, millal muutub eelvaate funktsioon kohustuslikuks. See kuupäev on tavaliselt 1. oktoobril või 1. aprillil, et ühitada poolaasta väljalaskeplaanidega. Kohustuslikke funktsioone välja lülitada ei saa. Kuni see muutub kohustuslikuks, saate funktsiooni kõikides keskkondades sisse ja välja lülitada.

Soovitame tungivalt vaadata funktsioone liivakasti- või prooviversiooni keskkonnas eelvaates. Kõige parem on luua liivakastikeskkonda koopia oma praegusest keskkonnast või andmebaasist, et saaksite oma andmetega uusi funktsioone täielikult kogeda.

Lisateavet liivakastikeskkonna ettevalmistamise kohta vt [Rakenduse Human Resources projekti ettevalmistamine](hr-admin-setup-provision.md). Proovikeskkonna eemaldamiseks vt [Eksemplari eemaldamine](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>Vigadest teatamine

Eelvaatefunktsioonide testimisel või uute võimaluste proovimisel võite leida üksuseid, mis ei tööta ootuspäraselt. Andke kõikidest vigadest [Microsoft Dynamics 365 toe](https://dynamics.microsoft.com/support/) kaudu teada.

## <a name="see-also"></a>Vt ka

- [Dynamics 365 ja Power Platformi väljalaskeplaanid](https://docs.microsoft.com/dynamics365/release-plans)
- [Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources?](hr-admin-whats-new.md)
- [Tarkvara elutsükli poliitika](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

