---
title: "Süsteeminõuded"
description: "Käesolevas peatükis on kirjeldatud praegune versioon Microsoft Dynamics 365 operatsioonide süsteeminõuded."
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 9220c093d3f6d6700127c93651db4083be300311
ms.lasthandoff: 03/31/2017


---

# <a name="system-requirements"></a>Süsteeminõuded

Käesolevas peatükis on kirjeldatud praegune versioon Microsoft Dynamics 365 operatsioonide süsteeminõuded.

<a name="supported-web-browsers"></a>Toetatud veebibrauserid
----------------------

Microsoft Dynamics 365 toimingute veebirakenduse jaoks saab käitada järgmine veebibrausereid, mis töötavad määratud operatsioonisüsteemides:

-   Microsoft Edge (Viimane üldkasutatavate versioon) operatsioonisüsteemis Windows 10
-   Internet Explorer 11 operatsioonisüsteemides Windows 10, Windows 8.1 või Windows 7
-   Google Chrome (Viimane üldkasutatavate versioon) Windows 10, Windows 8.1, Windows 8, Windows 7 või Google Nexus 10 tahvelarvuti
-   Apple Safari (uusim üldkasutatavate versioon) Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) või 10.12 (Sierra) või Apple iPad

Iga veebibrauseri uusima versiooni leidmiseks minge tarkvaratootja veebisaidile. **Märkused.**

-   Pilte, mis genereeritakse tööülesanne Recorder ja lisada neid Microsoft Wordi dokumente, peab teil olema installitud Chrome'i laiendus. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   ClickOnce'i rakendus käivitatakse töövoo redaktor. Ainult Microsoft Edge ja Internet Explorer (kohta Microsoft Windowsi toetatud versiooni) toetada ClickOnce'i rakendusi. Töövoo redaktor ClickOnce'i rakendus nõuab 64-bitine ühilduv operatsioonisüsteem.
-   ClickOnce'i rakendus käivitatakse Aruandekujundaja finantsaruandluseks. Selleks on vaja ühilduvat operatsioonisüsteemi 64-bitine. Chrome kasutamisel installige ClickOnce'i pikendamine et alla aruande disainer klient. Kui kasutate Chrome'i inkognito režiimis, veenduge, et ClickOnce'i laiendamine on lubatud ka inkognito režiimi.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Retail Cloud POS-i toetatud veebibrauserid

Jaemüügi pilve POS Dynamics 365 operatsioonide saab käivitada mis tahes järgmine veebibrausereid, mis töötavad määratud operatsioonisüsteemides:

-   Microsoft Edge (Viimane üldkasutatavate versioon) operatsioonisüsteemis Windows 10
-   Internet Explorer 11 operatsioonisüsteemides Windows 10, Windows 8.1 või Windows 7
-   Chrome (Viimane üldkasutatavate versioon) Windows 10, Windows 8.1 või Windows 7

## <a name="network-requirements"></a>Nõuded võrgule
-   Dynamics 365 toiminguteks on projekteeritud võrkude latentsus vähem kui 150 millisekundit (ms). See on latency brauseri klientrakenduses Microsoft Azure andmete keskus, mis korraldab Dynamics 365 toiminguteks. Soovitame testida võrgu latency kell <http://www.azurespeed.com>.
-   Dynamics 365 operatsioonide ribalaius nõuded sõltuvad oma stsenaarium. Kõige tüüpilisem stsenaariumid nõuavad ribalaius üle 50 kilobaiti sekundis (KBps). Stsenaariume, mis on konstrueerimisel nõudeid, tööruumide või stsenaariume, mis on seotud ulatusliku kohandamine, nagu soovitatakse rohkem ribalaiust.

Üldjuhul Dynamics 365 toiminguteks on optimeeritud Internet. Edasi-tagasi brauseri kliendi Azure'i andmekeskuse arv on väga väike ja kogu kandevõime on tihendatud. **Hoiatus:** ei Arvuta ribalaius nõuetele kliendi asukohast kasutajate arv korrutatakse minimaalse ribalaiuse nõudeid. Samaaegne kasutamine konkreetses asukohas on väga raske arvutada. Klientidele, kes on mures ribalaius nõuetele, kasutada preview versiooni Dynamics 365 toiminguteks.

## <a name="net-framework-requirements"></a>.NET raamistiku nõuetele
Dynamics 365 operatsioonide nõuab .NET Frameworki versiooni 4.6.2 kõik klõpsake-kord rakendusi, nagu dokumendi marsruutimise agent. Paigaldamise juhised leiate [.NET Frameworki installimist](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Toetatud Microsoft Office'i rakendused
-   Käivitage Microsoft Excel ja lisandmoodulid, peab teil olema Microsoft Office 2016 for Windows või Mac installitud. Lisateavet versiooni nõuetele, vt [Office integratsiooni tõrkeotsing](/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Eksport Excelisse või eksport Wordi funktsiooni loodavate dokumentide vaatamiseks peab olema Microsoft Office 2007 või hiljem paigaldatud.

## <a name="retail-modern-pos-requirements"></a>Jaemüügi kaasaegne POS nõuetele
### <a name="supported-operating-systems"></a>Toetatud operatsioonisüsteemid

-   Jaemüügi kaasaegne POS on 32-bitise programmi, kuid see töötab nii x86 kui x64 arhitektuuride.
-   Jaemüügi kaasaegne POS toetatakse ainult Windows 10 Pro, ettevõte, ettevõtte pikk mõiste teeninduse haru (LTSB) versioon.

### <a name="minimum-system-requirements"></a>Minimaalsed süsteeminõuded

-   Minimaalne toetatud resolutsioon on 1280 × 1024.
-   Jaemüügi kaasaegne POS kohta käitavas arvutis peab vastama järgmistele nõuetele:
    -   See peab olema, vähemalt, dual-core protsessor, mis töötab vähemalt 2-gigahertsine (GHz).
    -   See peab olema, vähemalt 3 gigabaiti (GB) muutmälu.
    -   See peab olema internetiühendus.

## <a name="retail-hardware-station-requirements"></a>Jaemüügi riistvara station
### <a name="supported-operating-systems"></a>Toetatud operatsioonisüsteemid

-   Jaemüügi riistvara on 32-bitise programmi, kuid see töötab nii x86 kui x64 arhitektuuride.
-   Jaemüügi riistvara station toetatakse järgmisi süsteeme:
    -   Windows 7 Professional, Enterprise ja Ultimate Editioni **Märkus:** Windows 7 toetab ainult siis, kui Internet Explorer 11 installimist käsitsi süsteemi.
    -   Windows 8.1 Update 1 Professional, Enterprise või Embedded väljaannete
    -   Windows 10 Pro, Enterprise ja Enterprise LTSB väljaanded

### <a name="minimum-system-requirements"></a>Minimaalsed süsteeminõuded

Arvuti peab vastama kõigile süsteeminõuetele installides ja kasutades järgmist:

-   Interneti teabeteenuste haldamine (IIS)
-   Muu riistvara

## <a name="retail-store-scale-unit-requirements"></a>Jaemüügi poe skaala ühik nõuetele
### <a name="supported-operating-systems"></a>Toetatud operatsioonisüsteemid

-   Kauplusesse skaala ühik on 32-bitise programmi, kuid see töötab nii x86 kui x64 arhitektuuride.
-   Kauplusesse skaala ühik toetatakse järgmisi süsteeme:
    -   Windows 7 Professional, Enterprise ja Ultimate Editioni
    -   Windows 8.1 Update 1 Professional, Enterprise või Embedded väljaannete
    -   Windows 10 Pro, Enterprise ja Enterprise LTSB väljaanded

### <a name="minimum-system-requirements"></a>Minimaalsed süsteeminõuded

-   4 GB RAM
-   1.6 GHz peak CPU kiirus tuuma kohta (kaks tuuma on minimaalne).
-   Vähemalt 10 GB vaba ruumi (kanali andmebaasi võib nõuda palju ruumi).

### <a name="recommended-system-requirements"></a>Soovituslik süsteeminõuded

-   6 GB RAM
-   2.4 GHz i7 (või samaväärne) piigi CPU kiirus (soovitatavalt neli protsessorituuma.) tuuma kohta
-   Vähemalt 10 GB vaba ruumi (kanali andmebaasi võib nõuda palju ruumi).

## <a name="requirements-for-development-on-local-vms"></a>Nõuete väljatöötamiseks kohaliku VMs
Teavet nõuete väljatöötamine kohaliku virtuaalarvuti (VM), vt [töötab kohapeal VM](/dynamics365/operations/dev-itpro/dev-tools/access-instances#vm-that-is-running-in-premises).

<a name="see-also"></a>Vt ka
--------

[Saada tutvumiskoopia Dynamics 365 toiminguteks](/dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)


