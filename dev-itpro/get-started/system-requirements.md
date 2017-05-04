---
title: "Süsteeminõuded"
description: "Teema esitab süsteeminõuete loendi Microsoft Dynamics 365 for Operationsi praeguse versiooni kohta."
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

Teema esitab süsteeminõuete loendi Microsoft Dynamics 365 for Operationsi praeguse versiooni kohta.

<a name="supported-web-browsers"></a>Toetatud veebibrauserid
----------------------

Microsoft Dynamics 365 for Operationsi veebirakendus võib töötada kõigis järgmistes veebibrauserites, mis töötavad nimetatud operatsioonisüsteemis.

-   Microsoft Edge (viimane avalikult saadaolev versioon) Windows 10-s
-   Internet Explorer 11 operatsioonisüsteemides Windows 10, Windows 8.1 või Windows 7
-   Google Chrome (viimane avalikult saadaolev versioon) operatsioonisüsteemides Windows 10, Windows 8.1, Windows 8, Windows 7 või tahvelarvuti Google Nexus 10
-   Apple Safari (viimane avalikult väljastatud versioon) operatsioonisüsteemides Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) või 10.12 (Sierra) või Apple iPad

Iga veebibrauseri uusima versiooni leidmiseks minge tarkvaratootja veebisaidile. **Märkused.**

-   Tegevuse salvestajas loodud piltide jäädvustamiseks ja nende Microsoft Wordi dokumentidesse lisamiseks peab teil olema installitud Chrome’i laiendus. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   Töövooredaktor käivitatakse ClickOnce’i rakendusena. Ainult Microsoft Edge ja Internet Explorer (Microsoft Windowsi toetatud versioonis) toetavad ClickOnce’i rakendusi. Töövooredaktori ClickOnce rakendus nõuab ühilduvat 64-bitist operatsioonisüsteemi.
-   Finantsaruandluse jaoks mõeldud aruandekujundaja käivitatakse ClickOnce’i rakendusena. See nõuab ühilduvat 64-bitist operatsioonisüsteemi. Kui kasutate Chrome’i, peate aruandekoosturi kliendi allalaadimiseks installima laienduse ClickOnce. Kui kasutate Chrome’i inkognito-režiimis, siis veenduge, et laiendus ClickOnce oleks inkognito-režiimi jaoks samuti aktiveeritud.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Retail Cloud POS-i toetatud veebibrauserid

Dynamics 365 for Operationsi Retail Cloud POS-i saab käitada kõigis järgmistes veebibrauserites, mis töötavad nimetatud operatsioonisüsteemides.

-   Microsoft Edge (viimane avalikult saadaolev versioon) Windows 10-s
-   Internet Explorer 11 operatsioonisüsteemides Windows 10, Windows 8.1 või Windows 7
-   Chrome (kõige värskem saadaolev versioon) operatsioonisüsteemis Windows 10, Windows 8.1 või Windows 7

## <a name="network-requirements"></a>Võrgunõuded
-   Dynamics 365 for Operations on mõeldud võrkudele, mille latentsus on vähem kui 150 millisekundit (ms). See on latentsus brauserikliendist Microsoft Azure’i andmekeskusesse, mis majutab rakendust Dynamics 365 for Operations. Soovitame teilt testida võrgulatentsust veebiaadressil <http://www.azurespeed.com>.
-   Rakenduse Dynamics 365 for Operations ribalaiuse nõuded sõltuvad stsenaariumist. Kõige tüüpilisemad stsenaariumid nõuavad ribalaiust rohkem kui 50 kilobaiti sekundis (KB/s). Stsenaariumide puhul, millel on kõrged kasuliku koormuse nõuded (nt tööruumid või stsenaariumid, mis hõlmavad ulatuslikku kohandamist), on soovitatav kasutada rohkem ribalaiust.

Üldiselt on Dynamics 365 for Operations Interneti jaoks optimeeritud. Pendellevi hulk brauserikliendist Azure’i andmekeskusesse on väga väike ja kogu kasulik koormus on tihendatud. **Hoiatus.** Ärge arvutage ribalaiuse nõudeid kliendi asukohast, korrutades kasutajate arvu minimaalsete ribalaiuse nõuetega. Antud asukoha samaaegset kasutust on väga keeruline arvutada. Ribalaiuse nõuete pärast muret tundvate klientide puhul kasutage rakenduse Dynamics 365 for Operations eelvaateversiooni.

## <a name="net-framework-requirements"></a>.NET Frameworki nõuded
Dynamics 365 for Operations nõuab .NET Frameworki versiooni 4.6.2 kõikide ühe korra klõpsatavate rakenduste puhul (nt dokumendi marsruudivaliku agent). Installimisjuhiste puhul vaadake teemat [.NET Frameworki installimine](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Toetatud Microsoft Office’i rakendused
-   Microsoft Exceli ja Wordi lisandmooduli käivitamiseks peab teil olema installitud Windowsile või Macile mõeldud Microsoft Office 2016. Versiooninõuete kohta lisateabe saamiseks vaadake teemat [Office’i integratsiooni tõrkeotsing](/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Funktsiooniga Ekspordi Excelisse või Ekspordi Wordi loodud dokumentide vaatamiseks peab teil olema installitud Microsoft Office 2007 või uuem versioon.

## <a name="retail-modern-pos-requirements"></a>Retail Modern POS-i nõuded
### <a name="supported-operating-systems"></a>Toetatud operatsioonisüsteemid

-   Retail Modern POS on 32-bitine rakendus, kuid see võib töötada nii x86- kui ka x64-põhistes arhitektuurides.
-   Retail Modern POS on toetatud ainult operatsioonisüsteemi Windows 10 Pro, Enterprise ja Enterprise Long Term Servicing Branch (LTSB) versioonides.

### <a name="minimum-system-requirements"></a>Minimaalsed süsteeminõuded

-   Minimaalne toetatud eraldusvõime on 1280 × 1024.
-   Retail Modern POS-i käitav arvuti peab vastama nendele nõuetele.
    -   Sellel peab olema minimaalselt kahetuumaline protsessor, mis töötab vähem kui 2 gigahertsiga (GHz).
    -   Sellel peab olema minimaalselt 3 gigabaiti (GB) RAM-i.
    -   Sellel peab olema Interneti-juurdepääs.

## <a name="retail-hardware-station-requirements"></a>Jaemüügi riistvarajaama nõuded
### <a name="supported-operating-systems"></a>Toetatud operatsioonisüsteemid

-   Jaemüügi riistvarajaam on 32-bitine rakendus, kuid see võib töötada nii x86- kui ka 64-põhistes arhitektuurides.
-   Jaemüügi riistvarajaama toetatakse järgmistes operatsioonisüsteemides:
    -   Windows 7 Professionali, Enterprise’i ja Ultimate’i versioonides **Märkus.** Operatsioonisüsteemi Windows 7 toetatakse ainult siis, kui Internet Explorer 11 on süsteemi käsitsi installitud.
    -   Windows 8.1 Update 1 Professionali, Enterprise’i ja manustatud versioonid
    -   Windows 10 Pro, Enterprise’i ja Enterprise LTSB versioonid

### <a name="minimum-system-requirements"></a>Minimaalsed süsteeminõuded

Arvuti peab vastama kõigile järgmiste üksuste installimist ja kasutamist puudutavatele süsteeminõuetele.

-   Interneti teabeteenuste haldamine (IIS)
-   Muu osapoole riistvara

## <a name="retail-store-scale-unit-requirements"></a>Jaekaupluse skaala üksuse nõuded
### <a name="supported-operating-systems"></a>Toetatud operatsioonisüsteemid

-   Jaekaupluse skaala üksus on 32-bitine rakendus, kuid see võib töötada nii x86- kui ka 64-põhistes arhitektuurides.
-   Jaekaupluse skaala üksust toetatakse järgmistes operatsioonisüsteemides:
    -   Windows 7 Professionali, Enterprise’i ja Ultimate’i versioonides
    -   Windows 8.1 Update 1 Professionali, Enterprise’i ja manustatud versioonid
    -   Windows 10 Pro, Enterprise’i ja Enterprise LTSB versioonid

### <a name="minimum-system-requirements"></a>Minimaalsed süsteeminõuded

-   4 GB RAM-i
-   1,6 GHz CPU tippkiirus tuuma kohta (kaks tuuma minimaalselt.)
-   Vähemalt 10 GB vaba ruumi (kanali andmebaas võib nõuda suurel hulgal ruumi)

### <a name="recommended-system-requirements"></a>Soovitatavad süsteeminõuded

-   6 GB RAM-i
-   2,4 GHz i7 (või ekvivalent) CPU tippkiirus tuuma kohta (neli tuuma on soovitatavad).
-   Vähemalt 10 GB vaba ruumi (kanali andmebaas võib nõuda suurel hulgal ruumi)

## <a name="requirements-for-development-on-local-vms"></a>Arenduse nõuded kohalikes VM-ides
Kohalikes virtuaalmasinates (VM-id) arenduse nõuete kohta lisateabe saamiseks vaadake teemat [Asutusesiseselt töötav virtuaalmasin](/dynamics365/operations/dev-itpro/dev-tools/access-instances#vm-that-is-running-in-premises).

<a name="see-also"></a>Vt ka
--------

[Rakenduse Dynamics 365 for Operations hindamiskoopia hankimine](/dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)


