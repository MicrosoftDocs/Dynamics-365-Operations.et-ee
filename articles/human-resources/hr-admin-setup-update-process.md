---
title: Värskendamisprotsess
description: Microsoft Dynamics 365 Human Resources on tõeline tarkvara teenusena (Saas), mis pakub pidevaid, puutumatuid teenuse uuendusi rakenduse ja platvormi muudatustele.
author: twheeloc
ms.date: 12/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 197b3c5717494ab3c80a57cda337a9021293bf73
ms.sourcegitcommit: 68efa7b89273d04484566cbe14d3533a8fd4ee53
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/02/2022
ms.locfileid: "9819292"
---
# <a name="update-process"></a>Värskendamisprotsess

_**Rakendub:**  inimressursid autonoomsel infrastruktuuril_ 

> [!NOTE]
> Alates 2022. juulist ei saa uusi inimressursid keskkondi eraldi inimressursside infrastruktuuris Microsoft Dynamics ette luua ja uusi elutsükli teenuste (LCS) projekte ei saa selles luua. Kliendid saavad inimressursside keskkondi kasutusele võtta finantside ja toimingute infrastruktuuris. Lisateavet vt inimressursside ettevalmistamisest [finantside ja toimingute infrastruktuuris](hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Finantside ja toimingute rakenduse infrastruktuuri värskendus- ja kiirparandusprotsess erineb inimressursside autonoomsest uuendamise ja kiirparanduse protsessist. Lisateavet värskendusprotsessi kohta vt teemast Finantside [ja toimingute viimasele värskendusele teisaldamise protsess](../fin-ops-core/dev-itpro/migration-upgrade/upgrade-latest-update.md). Lisateavet kiirparanduste kohta vt värskenduste allalaadimine [elutsükli teenustest (LCS).](/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs.md) 

Microsoft Dynamics 365 Human Resources on tõeline tarkvara teenusena (Saas), mis pakub pidevaid, puutumatuid teenuse uuendusi. Need värskendused sisaldavad nii rakenduse kui ka platvormi muudatusi, mis pakuvad sageli teenuse kriitilist täiustust, sh regulatiivsed uuendused.

## <a name="update-policy"></a>Värskenduspoliitika

Värskendusi antakse välja regulaarselt kõikides keskkondades. Rakenduse Human Resources tugi põhineb [Microsofti elutsükli poliitikal](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), kust leiate terviklikud ja ennustatavad juhised toe saadavuse kohta.

## <a name="release-cadence"></a>Väljaandmise sagedus 

Rakenduse Human Resources värskendusi rakendatakse kõigile keskkondadele automaatselt. Human Resources pakub kahte tüüpi väljaandeid.

- **Teenuse värskendused**: teenuse uuendused sisaldavad kehtivaid platvormivärskendusi, kui need vabastatakse. Lisaks eranditel põhinevatele uuendustele toimuvad regulaarsed teenusevärskendused, mis järgnevad Dynamics 365 finantsplatvormi värskenduste üldisele saadavusele (GA). Lisateavet platvormi väljalasete kohta vt platvormi [uuendustest "Mis on uut või muutunud"](../fin-ops-core/dev-itpro/get-started/whats-new-home-page.md). Värskendustel on etapiviisiline globaalne ümberpööramine üle piirkondade. Lisateavet uuenduste kohta vt teemast [Mis on uut või muutunud Dynamics 365 Human Resources](hr-admin-whats-new.md).

- **Lahenduse Dataverse värskendused**: need värskendused toimuvad vastavalt vajadusele ligikaudu iga kuue nädala järel. Need hõlmavad uusi üksusi ja muudatusi olemasolevatele üksustele rakenduses Dataverse. Need uuendused vabastatakse poole nädala uuendustega samasse piirkonda ja neil võtab aega umbes kuus nädalat kõikide andmekeskuste kaudu kopeerimiseks. Lahenduse värskendused võivad, kuid ei pruugi olla vastavuses kahenädalaste teenuse uuendustega.

> [!NOTE]
> Kui need on väljastatud, on lahenduse värskendused saadaval kõigis andmekeskustes. Kui te ei soovi, et värskendused edastatakse automaatselt, saate neid värskendusi iga andmekeskuse igas keskkonnas käsitsi rakendada.

Vajadusel pakub Inimressursid järgmist tüüpi parandusi.

- **Redaktsioon (kiirparandus)**: veaparandused, mis võivad ilmneda kas koos kahenädalase teenuseuuenduse väljalaskega või eraldi

- **Erakorraline parandus**: ennetavad ja uuesti aktiivsed kiirparandused, mis on olemuselt eraldiseisvad, võivad sisaldada ainult konfiguratsiooni või koodi muudatusi, et lahendada avaldatud saidi probleeme, ja need võivad ilmneda kahenädalasest teenuseuuenduse väljaandest eraldi

Väljaanded vaadatakse üle, testitakse ja kontrollitakse sisemises keskkonnas. Pärast järkude kinnitamist edastatakse need tootmisse.

## <a name="communications"></a>Suhtlus

Saate teada, mis on rakenduses Human Resources töös ja mida oleme väljastanud, järgmistes asukohtades:

- [Dynamics 365 Human Resourcesi teejuht](https://dynamics.microsoft.com/roadmap/human-resources/)

- [Dynamics 365 väljalaskeplaanid](/dynamics365/release-plans/)

- [Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources?](hr-admin-whats-new.md)

- [Teenuse Lifecycle Services (LCS) teema otsing](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (ainult platvormiga seotud vigade jaoks)

- [Rakenduse Human Resources blogi](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [Rakenduse Human Resources Yammeri kogukond](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>Liivakastikeskkonna eelvaatefunktsioonid

Enne nende tootmiskeskkonnas lubamist saate eelvaatefunktsioonid liivakastikeskkonnas kinnitada. Lisateavet funktsioonide lubamise kohta vt [Funktsioonihalduse ülevaade](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Kõik uued funktsioonid jäävad vähemalt 30 päevaks eelvaatesse ja tavaliselt 30–60 päevaks. Peamised funktsioonid on tavaliselt saadaval eelvaate perioodile järgneva iga aasta oktoobris ja aprillis. Kohe kui näete tööruumis **Funktsioonihaldus** uusi võimalusi, saate need sisse lülitada. Mõned funktsioonid võivad olla vaikimisi sisse lülitatud.

Mõnikord on lahutamatu funktsioon vaikimisi sisse lülitatud ja seda ei saa välja lülitada (nt tööruum Funktsioonihaldus).

Kui funktsioon on üldsusele saadaval, võib selle tootmiskeskkonnas sisse või välja lülitada. Tööruum **Funktsioonihaldus** näitab, millal muutub eelvaate funktsioon kohustuslikuks. See kuupäev on tavaliselt 1. oktoobril või 1. aprillil, et ühitada poolaasta väljalaskeplaanidega. Kohustuslikke funktsioone välja lülitada ei saa. Kuni see muutub kohustuslikuks, saate funktsiooni kõikides keskkondades sisse ja välja lülitada.

Soovitame tungivalt vaadata funktsioone liivakasti- või prooviversiooni keskkonnas eelvaates. Kõige parem on luua liivakastikeskkonda koopia oma praegusest keskkonnast või andmebaasist, et saaksite oma andmetega uusi funktsioone täielikult kogeda.

Lisateavet liivakastikeskkonna ettevalmistamise kohta vt [Rakenduse Human Resources projekti ettevalmistamine](hr-admin-setup-provision.md). Proovikeskkonna eemaldamiseks vt [Eksemplari eemaldamine](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>Vigadest teatamine

Eelvaatefunktsioonide testimisel või uute võimaluste proovimisel võite leida üksuseid, mis ei tööta ootuspäraselt. Andke kõikidest vigadest [Microsoft Dynamics 365 toe](https://dynamics.microsoft.com/support/) kaudu teada.

## <a name="see-also"></a>Vt ka

[Dynamics 365 ja Power Platformi väljalaskeplaanid](/dynamics365/release-plans)</br>
[Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources?](hr-admin-whats-new.md)</br>
[Tarkvara elutsükli poliitika](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
