---
title: "Pilvjuurutuste süsteeminõuded"
description: "Teema esitab süsteeminõuete loendi rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition pilvejuurutuste kohta."
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: 7fe11966b27eb0793a47835e05e465d809bf3407
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="system-requirements-for-cloud-deployments"></a>Pilvjuurutuste süsteeminõuded

[!include[banner](../includes/banner.md)]

Teema esitab süsteeminõuete loendi rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition pilvejuurutuste kohta. Enne rakenduse Finance and Operations installimist kontrollige vajaduse korral, kas süsteem, millega töötate, vastab minimaalsetele võrgu-, riistvara- või tarkvaranõuetele või ületab neid.

## <a name="supported-web-browsers"></a>Toetatud veebibrauserid
Veebirakenduse võib töötada kõigis järgmistes veebibrauserites, mis töötavad nimetatud operatsioonisüsteemis.

-   Microsoft Edge (viimane avalikult saadaolev versioon) Windows 10-s
-   Internet Explorer 11 operatsioonisüsteemides Windows 10, Windows 8.1 või Windows 7
-   Google Chrome (viimane avalikult saadaolev versioon) operatsioonisüsteemides Windows 10, Windows 8.1, Windows 8, Windows 7 või tahvelarvuti Google Nexus 10
-   Apple Safari (viimane avalikult väljastatud versioon) operatsioonisüsteemides Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) või 10.12 (Sierra) või Apple iPad

Iga veebibrauseri uusima versiooni leidmiseks minge tarkvaratootja veebisaidile. 

> [!NOTE]
> -   Peate installima väljalaske-eelse Chrome’i versiooni, et lubada kuvatõmmise piltide salvestamine tegevuse salvestajas ja nende lisamine loodud Microsoft Wordi dokumentidesse. <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> -   Töövooredaktor käivitatakse ClickOnce’i rakendusena. Ainult Microsoft Edge ja Internet Explorer (Microsoft Windowsi toetatud versioonis) toetavad ClickOnce’i rakendusi. Töövooredaktori ClickOnce rakendus nõuab ühilduvat 64-bitist operatsioonisüsteemi.
> -   Finantsaruandluse jaoks mõeldud aruandekujundaja käivitatakse ClickOnce’i rakendusena. See nõuab ühilduvat 64-bitist operatsioonisüsteemi. Kui kasutate Chrome’i, peate aruandekoosturi kliendi allalaadimiseks installima laienduse ClickOnce. Kui kasutate Chrome’i inkognito-režiimis, siis veenduge, et laiendus ClickOnce oleks inkognito-režiimi jaoks samuti aktiveeritud.
> -   PDF-failide eelvaateks soovitame kasutada brausereid, nagu Microsoft Edge (viimane avalikult saadaolev versioon) Windows 10-s või Google Chrome (viimane avalikult saadaolev versioon) Windows 10-s, Windows 8.1-s, Windows 8-s, Windows 7-s või tahvelarvutis Google Nexus 10.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Retail Cloud POS-i toetatud veebibrauserid

Retail Cloud POS võib töötada kõigis järgmistes veebibrauserites, mis töötavad nimetatud operatsioonisüsteemides.

-   Microsoft Edge (viimane avalikult saadaolev versioon) Windows 10-s
-   Internet Explorer 11 operatsioonisüsteemides Windows 10, Windows 8.1 või Windows 7
-   Chrome (kõige värskem saadaolev versioon) operatsioonisüsteemis Windows 10, Windows 8.1 või Windows 7

## <a name="network-requirements"></a>Võrgunõuded
-   Finance and Operations on mõeldud võrkudele, mille latentsus on kuni 250–300 millisekundit (ms). See on latentsus brauserikliendist Microsoft Azure’i andmekeskusesse, mis majutab rakendust Finance and Operations. Soovitame teilt testida võrgulatentsust veebiaadressil <http://www.azurespeed.com>.
-   Rakenduse Finance and Operations ribalaiuse nõuded sõltuvad stsenaariumist. Kõige tüüpilisemad stsenaariumid nõuavad ribalaiust rohkem kui 50 kilobaiti sekundis (KB/s). Stsenaariumide puhul, millel on kõrged kasuliku koormuse nõuded (nt tööruumid või stsenaariumid, mis hõlmavad ulatuslikku kohandamist), on soovitatav kasutada rohkem ribalaiust.

Üldiselt on Finance and Operations Interneti jaoks optimeeritud. Pendellevi hulk brauserikliendist Azure’i andmekeskusesse on väga väike ja kogu kasulik koormus on tihendatud. 

> [!WARNING]
> Ärge arvutage ribalaiuse nõudeid kliendi asukohast, korrutades kasutajate arvu minimaalsete ribalaiuse nõuetega. Antud asukoha samaaegset kasutust on väga keeruline arvutada. Ribalaiuse nõuete pärast muret tundvate klientide puhul kasutage rakenduse Finance and Operations eelvaateversiooni.

## <a name="net-framework-requirements"></a>.NET Frameworki nõuded
Finance and Operations nõuab Microsoft .NET Frameworki versiooni 4.6.2 kõikide ClickOnce-tüüpi rakenduste puhul (nt dokumendi marsruudivaliku agent). Installimisjuhiste puhul vaadake teemat [.NET Frameworki installimine](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Toetatud Microsoft Office’i rakendused
Rakenduse Finance and Operations pilve- ja kohapealsetes juurutustes toetatakse järgmisi Microsoft Office’i rakendusi.

-   Microsoft Exceli ja Wordi lisandmooduli käivitamiseks peab teil olema installitud Windowsile või Macile mõeldud Microsoft Office 2016. Versiooninõuete kohta lisateabe saamiseks vaadake teemat [Office’i integratsiooni tõrkeotsing](../../dev-itpro/office-integration/office-integration-troubleshooting.md).
-   Funktsiooniga Ekspordi Excelisse või Ekspordi Wordi loodud dokumentide vaatamiseks peab teil olema installitud Microsoft Office 2007 või uuem versioon.

## <a name="retail-modern-pos-requirements"></a>Retail Modern POS-i nõuded

> [!NOTE]
> Kui Retail Modern POS kasutab võrguühenduseta andmebaasi, peab arvuti vastama kõikidele Microsoft SQL Serveri nõuetele. Retail Modern POS-i võrguühenduseta andmebaas töötab teenusega Microsoft SQL Server 2012, millel on hoolduspakett Service Pack 3 või uuem, teenusega Microsoft SQL Server 2014, millel on hoolduspakett Service Pack 2 või uuem, ja teenusega teenusega Microsoft SQL Server 2016. Soovitame alati kasutada uusimat saadaolevat väljannet ja installida uusimad hoolduspaketid.

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

    -   Windows 7 Professionali, Enterprise’i ja Ultimate’i versioonides 
    
        > [!NOTE]
        > Windows 7 toetatakse ainult siis, kui Internet Explorer 11 on käsitsi arvutisse installitud.

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

## <a name="connector-requirements"></a>Konnektori nõuded
### <a name="supported-operating-systems"></a>Toetatud operatsioonisüsteemid

-   Microsoft Dynamics AX-i konnektoril on kaks eraldi installiprogrammi: programm Async Server Connector service'i jaoks ja programm Real-time service for Dynamics AX 2012 R3 jaoks.
-   Mõlemad komponendid on 32-bitised rakendused, kuid töötavad nii x86- kui ka x64-põhistes arhitektuurides.
-   Mõlemaid komponente toetatakse järgmistes operatsioonisüsteemides.

    -   Windows 7 Professionali, Enterprise’i ja Ultimate’i versioonides
    -   Windows 8.1 Update 1 Professionali, Enterprise’i ja manustatud versioonid
    -   Windows 10 Pro, Enterprise’i ja Enterprise LTSB versioonid
    -   Microsoft Windows Server 2012 R2 ja Microsoft Windows Server 2016

### <a name="minimum-system-requirements"></a>Minimaalsed süsteeminõuded
-   2 GB RAM, soovituslik 4 GB RAM
-   1,6 GHz CPU tippkiirus tuuma kohta (kaks tuuma minimaalselt.)
-   Vähemalt 10 GB vaba ruumi (kanali andmebaas võib nõuda suurel hulgal ruumi)

## <a name="requirements-for-development-on-local-vms"></a>Arenduse nõuded kohalikes VM-ides
Kohalikes virtuaalmasinates (VM-id) arenduse nõuete kohta lisateabe saamiseks vaadake teemat [Asutusesiseselt töötav virtuaalmasin](../../dev-itpro/dev-tools/access-instances.md).


## <a name="see-also"></a>Vt ka

[Rakenduse Dynamics 365 for Finance and Operations, Enterprise Editioni hindamiskoopia hankimine](../../dev-itpro/dev-tools/get-evaluation-copy.md)

