---
title: Värskendamisprotsess
description: Microsoft Dynamics 365 Human Resources on tõeline tarkvara teenusena (Saas), mis pakub pidevaid, puutumatuid teenuse uuendusi rakenduse ja platvormi muudatustele.
author: andreabichsel
manager: tfehr
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bb5f7dc17c8f4f3a54bd285cb55088f2176db4a
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112199"
---
# <a name="update-process"></a>Värskendamisprotsess

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Human Resources on tõeline tarkvara teenusena (Saas), mis pakub pidevaid, puutumatuid teenuse uuendusi. Need värskendused sisaldavad nii rakenduse kui ka platvormi muudatusi, mis pakuvad sageli teenuse kriitilist täiustust, sh regulatiivsed uuendused.

## <a name="update-policy"></a>Värskenduspoliitika

Värskendusi antakse välja regulaarselt kõikides keskkondades. Rakenduse Human Resources tugi põhineb [Microsofti elutsükli poliitikal](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), kust leiate terviklikud ja ennustatavad juhised toe saadavuse kohta.

## <a name="release-cadence"></a>Väljaandmise sagedus 

Rakenduse Human Resources värskendusi rakendatakse kõigile keskkondadele automaatselt. Human Resources pakub kahte tüüpi väljaandeid.

- **Teenusevärskendused**: iga kahe nädala tagant toimuvad uuendused, mis sisaldavad veaparandusi ja uusi funktsioone. Teenusevärskendused sisaldavad ka kehtivaid platvormi värskendusi, kui need väljastatakse. Et saada aimu, millal platvormi värskendusi väljastatakse, vt [tabelit 3: Platvormi väljaanded](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases). Kahenädalasi värskendusi levitatakse globaalselt kõigis piirkondades etapiliselt. Lisateavet kahenädalaste uuenduste kohta vt teemat [Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources](hr-admin-whats-new.md).

    Kõik toetatud andmekeskused uuendatakse iga kahe nädala tagant, kui pole teisiti märgitud. USA, Austraalia, Euroopa, Suurbritannia, Aasia ja Kanada piirkonnad sisalduvad kahenädalastes uuendustes. 

- **Lahenduse Dataverse värskendused**: need värskendused toimuvad vastavalt vajadusele ligikaudu iga kuue nädala järel. Need hõlmavad uusi üksusi ja muudatusi olemasolevatele üksustele rakenduses Dataverse. Need uuendused vabastatakse samadele piirkondadele kui kahenädalased uuendused ja neil kulub umbes kuus nädalat, et edastada läbi kõikide andmekeskuste. Lahenduse värskendused võivad, kuid ei pruugi olla vastavuses kahenädalaste teenuse uuendustega.

> [!NOTE]
> Kui need on väljastatud, on lahenduse värskendused saadaval kõigis andmekeskustes. Kui te ei soovi, et värskendused edastatakse automaatselt, saate neid värskendusi iga andmekeskuse igas keskkonnas käsitsi rakendada.

Vajadusel pakub rakendus Human Resources ka järgmist tüüpi parandusi.

- **Redaktsioon (kiirparandus)**: veaparandused, mis võivad ilmneda kas koos kahenädalase teenuseuuenduse väljalaskega või eraldi

- **Erakorraline parandus**: ennetavad ja uuesti aktiivsed kiirparandused, mis on olemuselt eraldiseisvad, võivad sisaldada ainult konfiguratsiooni või koodi muudatusi, et lahendada avaldatud saidi probleeme, ja need võivad ilmneda kahenädalasest teenuseuuenduse väljaandest eraldi

Väljaanded vaadatakse üle, testitakse ja kontrollitakse sisemises keskkonnas. Pärast järkude kinnitamist edastatakse need tootmisse.

## <a name="release-cadence-exceptions-in-2020"></a>Erandid väljaandmise sageduses 2020. aastal

Puhkuse arvestamiseks on 2020. aasta novembri ja detsembri väljastusgraafik järgmine.

- Novembri väljastus: 2. november – 13. november
- Detsembri väljastus: 30. november – 11. detsember
 
Kahenädalane väljaandmise sagedus jätkub tavapäraselt 11. jaanuaril 2021.

## <a name="communications"></a>Suhtlus

Saate teada, mis on rakenduses Human Resources töös ja mida oleme väljastanud, järgmistes asukohtades:

- [Dynamics 365 Human Resourcesi teejuht](https://dynamics.microsoft.com/roadmap/human-resources/)

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

[Dynamics 365 ja Power Platformi väljalaskeplaanid](https://docs.microsoft.com/dynamics365/release-plans)</br>
[Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources?](hr-admin-whats-new.md)</br>
[Tarkvara elutsükli poliitika](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)



[!INCLUDE[footer-include](../includes/footer-banner.md)]