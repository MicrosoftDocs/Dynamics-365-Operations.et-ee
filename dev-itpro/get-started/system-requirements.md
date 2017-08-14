---
title: "Süsteeminõuded"
description: "Teema esitab süsteeminõuete loendi Microsoft Dynamics 365 Finance and Operations, Enterprise editioni pilve- ja kohapealsete juurutuste kohta."
author: sericks007
manager: AnnBe
ms.date: 07/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 871ba89973f6af341c536f67db056bebb54600b3
ms.contentlocale: et-ee
ms.lasthandoff: 07/25/2017

---

# <a name="system-requirements"></a>Süsteeminõuded

[!include[banner](../includes/banner.md)]


Teema esitab süsteeminõuete loendi Microsoft Dynamics 365 Finance and Operations, Enterprise editioni pilve- ja kohapealsete juurutuste kohta. Enne rakenduse Finance and Operations installimist kontrollige vajaduse korral, kas süsteem, millega töötate, vastab minimaalsetele võrgu-, riistvara- või tarkvaranõuetele või ületab neid.


## <a name="supported-microsoft-office-applications"></a>Toetatud Microsoft Office’i rakendused
Rakenduse Finance and Operations pilve- ja kohapealsetes juurutustes toetatakse järgmisi Office’i rakendusi.
-   Microsoft Exceli ja Wordi lisandmooduli käivitamiseks peab teil olema installitud Windowsile või Macile mõeldud Microsoft Office 2016. Versiooninõuete kohta lisateabe saamiseks vaadake teemat [Office’i integratsiooni tõrkeotsing](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Funktsiooniga Ekspordi Excelisse või Ekspordi Wordi loodud dokumentide vaatamiseks peab teil olema installitud Microsoft Office 2007 või uuem versioon.

# <a name="system-requirements-specific-to-cloud-deployments"></a>Pilvejuurutuse kohased süsteeminõuded
## <a name="network-requirements"></a>Võrgunõuded
-   Finance and Operations on mõeldud võrkudele, mille latentsus on kuni 250–300 millisekundit (ms). See on latentsus brauserikliendist Microsoft Azure’i andmekeskusesse, mis majutab rakendust Finance and Operations. Soovitame teilt testida võrgulatentsust veebiaadressil <http://www.azurespeed.com>.
-   Rakenduse Finance and Operations ribalaiuse nõuded sõltuvad stsenaariumist. Kõige tüüpilisemad stsenaariumid nõuavad ribalaiust rohkem kui 50 kilobaiti sekundis (KB/s). Stsenaariumide puhul, millel on kõrged kasuliku koormuse nõuded (nt tööruumid või stsenaariumid, mis hõlmavad ulatuslikku kohandamist), on soovitatav kasutada rohkem ribalaiust.

Üldiselt on Finance and Operations Interneti jaoks optimeeritud. Pendellevi hulk brauserikliendist Azure’i andmekeskusesse on väga väike ja kogu kasulik koormus on tihendatud. 

> [!WARNING]
> Ärge arvutage ribalaiuse nõudeid kliendi asukohast, korrutades kasutajate arvu minimaalsete ribalaiuse nõuetega. Antud asukoha samaaegset kasutust on väga keeruline arvutada. Ribalaiuse nõuete pärast muret tundvate klientide puhul kasutage rakenduse Finance and Operations eelvaateversiooni.

## <a name="net-framework-requirements"></a>.NET Frameworki nõuded
Finance and Operations nõuab .NET Frameworki versiooni 4.6.2 kõikide ühe korra klõpsatavate rakenduste puhul (nt dokumendi marsruudivaliku agent). Installimisjuhiste puhul vaadake teemat [.NET Frameworki installimine](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-web-browsers"></a>Toetatud veebibrauserid
Veebirakenduse võib töötada kõigis järgmistes veebibrauserites, mis töötavad nimetatud operatsioonisüsteemis.


-   Microsoft Edge (viimane avalikult saadaolev versioon) Windows 10-s
-   Internet Explorer 11 operatsioonisüsteemides Windows 10, Windows 8.1 või Windows 7
-   Google Chrome (viimane avalikult saadaolev versioon) operatsioonisüsteemides Windows 10, Windows 8.1, Windows 8, Windows 7 või tahvelarvuti Google Nexus 10
-   Apple Safari (viimane avalikult väljastatud versioon) operatsioonisüsteemides Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) või 10.12 (Sierra) või Apple iPad

Iga veebibrauseri uusima versiooni leidmiseks minge tarkvaratootja veebisaidile. 

> [!NOTE]
> -   Installitud peab olema väljalaske-eelne Chrome’i versioon, et lubada kuvatõmmise piltide salvestamine tegevuse salvestajas ja nende lisamine loodud Microsoft Wordi dokumentidesse. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   Töövooredaktor käivitatakse ClickOnce’i rakendusena. Ainult Microsoft Edge ja Internet Explorer (Microsoft Windowsi toetatud versioonis) toetavad ClickOnce’i rakendusi. Töövooredaktori ClickOnce rakendus nõuab ühilduvat 64-bitist operatsioonisüsteemi.
> -   Finantsaruandluse jaoks mõeldud aruandekujundaja käivitatakse ClickOnce’i rakendusena. See nõuab ühilduvat 64-bitist operatsioonisüsteemi. Kui kasutate Chrome’i, peate aruandekoosturi kliendi allalaadimiseks installima laienduse ClickOnce. Kui kasutate Chrome’i inkognito-režiimis, siis veenduge, et laiendus ClickOnce oleks inkognito-režiimi jaoks samuti aktiveeritud.
> -   PDF-failide eelvaateks soovitame kasutada brausereid, nagu Microsoft Edge (viimane avalikult saadaolev versioon) Windows 10-s või Google Chrome (viimane avalikult saadaolev versioon) Windows 10-s, Windows 8.1-s, Windows 8-s, Windows 7-s või tahvelarvutis Google Nexus 10.


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Retail Cloud POS-i toetatud veebibrauserid

Retail Cloud POS võib töötada kõigis järgmistes veebibrauserites, mis töötavad nimetatud operatsioonisüsteemides.

-   Microsoft Edge (viimane avalikult saadaolev versioon) Windows 10-s
-   Internet Explorer 11 operatsioonisüsteemides Windows 10, Windows 8.1 või Windows 7
-   Chrome (kõige värskem saadaolev versioon) operatsioonisüsteemis Windows 10, Windows 8.1 või Windows 7

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

-   Microsoft Dynamics AX-i konnektoril on kaks eraldi installiprogrammi: **Async Server Connector service** ja **Real-time service for Dynamics AX 2012 R3**.
-   Mõlemad komponendid on 32-bitised rakendused, kuid töötavad nii x86- kui ka x64-põhistes arhitektuurides.
-   Mõlemaid komponente toetatakse järgmistes operatsioonisüsteemides.
    -   Windows 7 Professionali, Enterprise’i ja Ultimate’i versioonides
    -   Windows 8.1 Update 1 Professionali, Enterprise’i ja manustatud versioonid
    -   Windows 10 Pro, Enterprise’i ja Enterprise LTSB versioonid
    -   Windows Server 2012 R2, Windows Server 2016

### <a name="minimum-system-requirements"></a>Minimaalsed süsteeminõuded

-   2 GB RAM, soovituslik 4 GB RAM
-   1,6 GHz CPU tippkiirus tuuma kohta (kaks tuuma minimaalselt.)
-   Vähemalt 10 GB vaba ruumi (kanali andmebaas võib nõuda suurel hulgal ruumi)

## <a name="requirements-for-development-on-local-vms"></a>Arenduse nõuded kohalikes VM-ides
Kohalikes virtuaalmasinates (VM-id) arenduse nõuete kohta lisateabe saamiseks vaadake teemat [Asutusesiseselt töötav virtuaalmasin](../dev-tools/access-instances.md).

# <a name="system-requirements-for-on-premises-deployments"></a>Asutusesiseste juurutuste süsteeminõuded

## <a name="network-requirements"></a>Võrgunõuded
Finance and Operations (kohapealne) saab töötada võrkudes, mis kasutavad Interneti-protokolli versiooni 4 (IPv4) või Interneti-protokolli versiooni 6 (IPv6). Võtke süsteemi kavandamisel arvesse võrgukeskkonda ja kasutage järgmisi juhtnööre.

### <a name="network-response-time"></a>Võrgu reageerimisaeg
Järgmises tabelis on toodud minimaalsed võrgunõuded ühenduse loomiseks veebibrauseri ja rakendusobjekti serveri (AOS) vahel ning AOS-i ja andmebaasi vahel kohapealses süsteemis.

| Väärtus     | Veebibrauserist AOS-i | AOS-ist andmebaasi                                            |
|-----------|--------------------|------------------------------------------------------------|
| Ribalaius | 50 kB/s kasutaja kohta   | 100 MB/s                                                   |
| Latentsus   | < 250–300 ms       | < 1 ms (ainult LAN). AOS ja andmebaas peavad olema samas asukohas. |

- Finance and Operations (kohapealne) on mõeldud võrkudele, mille latentsus on kuni 250–300 millisekundit (ms). See on latentsus brauserikliendist andmekeskusse, mis majutab rakendust Finance and Operations.
- Rakenduse Finance and Operations (kohapealne) ribalaiuse nõuded olenevad stsenaariumist. Tavaline stsenaarium nõuab brauseri ja Finance and Operationsi serveri vahel suuremat ribalaiust kui 50 kilobaiti sekundis (KB/s). Stsenaariumide puhul, millel on kõrged kasuliku koormuse nõuded (nt tööruumid või stsenaariumid, mis hõlmavad ulatuslikku kohandamist), on soovitatav kasutada olenevalt kasutusest suuremat ribalaiust.
Juurutusi, milles AOS ja SQL Serveri andmebaas asuvad erinevates andmekeskustes, ei toetata. AOS ja SQL Serveri andmebaas peavad olema samas asukohas. Üldiselt on Finance and Operations optimeeritud vähendama brauseri ja serveri pendellevi. Pendellevi hulk brauserikliendist andmekeskusse on kas null või üks iga kasutaja interaktsiooni kohta ning kasulik koormus on tihendatud.

> [!WARNING]
> Ärge arvutage ribalaiuse nõudeid kliendi asukohast, korrutades kasutajate arvu minimaalsete ribalaiuse nõuetega. Antud asukoha samaaegset kasutust on väga keeruline arvutada. Soovitame rakendada rakenduse Finance and Operations mittetootmiskeskkonnas reaalset simulatsiooni, kasutades teie konkreetse valdkonna parimat jõudlusmõõdikut. 

### <a name="lan-environments"></a>LAN-keskkonnad
Kohtvõrgu (LAN) keskkondades ei ole rakendusega Finance and Operations ühenduse loomiseks Microsofti kaugtöölaud Microsoft Windows Serveris vajalik. Siiski võib see olla nõutav serverijuurutusi moodustavate VM-ide hooldustöödeks.

### <a name="wan-environments"></a>WAN-keskkonnad
Laivõrgu (WAN) keskkondades ei ole rakendusega Finance and Operations ühenduse loomiseks kaugtöölaud Windows Serveris vajalik.

### <a name="internet-connectivity-requirements"></a>Interneti-ühenduvuse nõuded
Finance and Operations (kohapealne) ei nõua Interneti-ühenduvust lõppkasutajate tööjaamadest. Mõni funktsioon ei pruugi siiski ilma Interneti-ühenduvuseta saadaval olla.

| Brauseriklient | Sisevõrgustsenaarium ilma Interneti-ühenduvuseta on kohapealse juurutuse valiku kujunduspõhimõte. Mõni pilveteenuseid nõudev funktsioon, näiteks spikri- ja tegevuste juhiste teegid LCS-is ei ole saadaval. |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Server         | AOS või Service Fabricu järk peavad olema võimelised LCS-iga suhtlema. Asutusesisene brauseriklient ei nõua Internetile juurdepääsu.                                                                                |
| Telemeetria      | Telemeetria andmed võivad kaotsi minna, kui ühenduses on pikki katkestusi. Ühenduvuse katkemine LCS-iga ei mõjuta kohapealse rakenduse funktsionaalsust.                                                |
| LCS            | Ühenduvus LCS-iga on nõutav juurutamiseks, koodi juurutamiseks ja hooldustöödeks.                                                                                                                                 |
## <a name="telemetry-data-transfer-to-the-cloud"></a>Telemeetria andmete ülekandmine pilve
Enamik telemeetriat salvestatakse kohalikult ja sellele pääseb juurde Microsoft Windowsi sündmustevaaturiga. Väike hulk telemeetriasündmusi edastatakse diagnostikaks pilves olevale Microsofti telemeetriakonveierile. Kliendi andmed ja lõppkasutaja identifitseeritavad andmed ei kuulu Microsoftile saadetava telemeetria alla. VM-ide nimed saadetakse Microsoftile, et abistada keskkondade haldamisel ja diagnostikal LCS-i portaalist.

## <a name="domain-requirements"></a>Domeeninõuded
Võtke rakenduse Finance and Operations (kohapealne) installimisel arvesse järgmisi domeeninõudeid.

- Virtuaalarvutid, mis majutavad rakenduse Finance and Operations (kohapealne) komponente, peavad kuuluma Active Directory domeeni. Active Directory domeeniteenused (AD DS) peavad olema konfigureeritud omarežiimis.
- Virtuaalarvutid, mis käitavad rakenduse Finance and Operations (kohapealne) komponente, peavad juurde pääsema üksteisele, mis on konfigureeritud Active Directory domeeniteenustes. 
- Domeenikontroller peab töötama Microsoft Windows Server 2016-s.

## <a name="hardware-requirements"></a>Riistvaranõuded
Selles jaotises kirjeldatakse rakenduse Finance and Operations (kohapealne) käitamiseks vajalikku riistvara.
Riistvaranõuded erinevad olenevalt süsteemi konfiguratsioonist, andmete koosseisust ning rakendustest ja funktsioonidest, mida otsustate kasutada. Järgnevalt mõni tegur, mis võib mõjutada rakenduse Finance and Operations (kohapealne) jaoks sobiva riistvara valimist.

- Kannete arv tunnis.
- Samaaegsete kasutajate arv.

## <a name="minimum-infrastructure-requirements"></a>Minimaalsed taristunõuded
Finance and Operations (kohapealne) kasutab AOS-i, partii, andmehalduse, halduse aruandja ja keskkonna korraldusteenuste majutamiseks Microsoft Azure Service Fabricut. Microsoft SQL Serveri aruandlusteenuseid (SSRS) ei majutata Service Fabricu kogumis.
SQL Server peab olema seadistatud suure kättesaadavuse HADRON-i seadistuses, millel on tootmises kasutamiseks vähemalt kaks režiimi.
Järgmisel joonisel on toodud sõlmede soovituslik miinimumarv teie Service Fabricu kogumis.

[![sõlmede soovituslik miinimumarv teie service fabricu kogumis](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>Protsessori ja RAM-i nõuded
Järgmises tabelis on toodud protsessorite arv ja muutmälu (RAM) maht, mis on vajalik igale selle juurutusvaliku käitamiseks nõutavale rollile. Lisateabe saamiseks vaadake Service Fabricu eraldiseisva kogumi jaoks soovitatud miinimumnõudeid [Service Fabricu kogumi kavandamine ja ettevalmistamine](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

> [!NOTE]
> Kui samasse arvutisse on installitud mõni muu Microsofti tarkvara, peab süsteem vastama ka selle tarkvara puhul kehtivatele riistvaranõuetele. Soovitame seada samas arvutis, milles käitate AOS-i, teiste serverirakenduste piiranguks 1 gigabait (GB) RAM-i.

**Suuruse muutmine rolli- ja topoloogiatüübi alusel**

| Topoloogia   | Roll (sõlme tüüpi)              | Soovitatav protsessori tuumade arv | Soovitatav mälu (GB) |
|------------|-------------------------------|-----------------------------|-------------------------|
| Tootmine | AOS, andmehaldur, partii   | 8                           | 24                      |
|            | Halduse aruandja           | 4                           | 16                      |
|            | SQL Serveri aruandlusteenused | 4                           | 16                      |
|            | Korraldaja                  | 4                           | 16                      |
| Liivakast    | AOS, andmehaldur, partii   | 4                           | 24                      |
|            | Halduse aruandja           | 4                           | 16                      |
|            | SQL Serveri aruandlusteenused | 4                           | 16                      |
|            | Korraldaja                  | 4                           | 16                      |

**Minimaalsed suuruseprognoosid tootmis- ja liivakastikeskkonna juurutuste puhul**\*

| Topoloogia                                  | Roll                          | Eksemplaride arv |
|-------------------------------------------|-------------------------------|---------------------|
| Tootmine                                | AOS (andmehaldur, partii)  | 3                   |
|                                           | Halduse aruandja           | 2                   |
|                                           | SQL Serveri aruandlusteenused | 1                   |
|                                           | Korraldaja\*\*                | 3                   |
| Liivakast                                   | AOS, andmehaldur, partii   | 2                   |
|                                           | Halduse aruandja           | 1                   |
|                                           | SQL Serveri aruandlusteenused | 1                   |
|                                           | Korraldaja                  | 3                   |
| *Tootmis- ja liivakastitopoloogiate kokkuvõte* |                               | 16                  |

\*Need arvud on heaks kiitnud meie eelvaateversiooni kliendid ja vajaduse korral võib neid selle tagasiside põhjal reguleerida.

\*\*Korraldaja on määratud primaarseks sõlmetüübiks ja seda kasutatakse ka Service Fabricu teenuste käitamiseks.

**SQL-tagaserveri ja AD algsed prognoosid**

[![SQL-tagaserveri ja AD algsed prognoosid](./media/system-reqs-on-premises-02.PNG)](./media/system-reqs-on-premises-02.PNG) 

\*SQL Serveri suurused sõltuvad oluliselt töökoormusest. Lisateavet vaadake jaotisest [Riistavara suuruse muutmine kohapealsete keskkondade puhul](#Hardware-sizing-for-on-premises-environments).

## <a name="storage"></a>Ladustamine

- **AOS** – Finance and Operations (kohapealne) kasutab struktuurimata andmete talletamiseks serveri teateploki (SMB) 3.0 ühiskasutust. Lisateavet vaadake jaotisest [Storage Spaces Direct Windows Server 2016-s](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL** – kasutatavad valikud on järgmised.
    - Suure saadavusega välkdraivi (SSD) seadistus.
    - OLTP-läbilaskele optimeeritud talletusala võrk (SAN).
    - Kõrge jõudlusega otse ühendatud talletusruum (DAS) 
- **SQL-i ja andmehalduse IOPS** – talletusruum nii andmehalduse kui ka SQL Serveri jaoks peab võimaldama vähemalt 2000 sisend-/väljundtoimingut sekundis (IOPS). Tootmise IOPS sõltub paljudest teguritest. Lisateavet vaadake jaotisest Riistavara suuruse muutmine kohapealsete keskkondade puhul. 
- **Virtuaalarvuti IOPS** – iga virtuaalarvuti peab võimaldama vähemalt 100 kirjutamise IOPS-i.

## <a name="virtual-host-requirements"></a>Virtuaalhosti nõuded
Virtuaalhostide seadistamisel rakenduse Finance and Operations (kohapealne) keskkonna jaoks vaadake järgmisi juhtnööre: [Service Fabricu kogumi kavandamine ja ettevalmistamine](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) ning [Service Fabricu kogumi kirjeldamine](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). Igal virtuaalhostil peab olema piisav arv tuumi selle taristu jaoks, mille suurust muudetakse. Võimalikud on mitu täpsemat konfiguratsiooni, kus SQL Server asub füüsilisel riistvaral, kuid kõik muu on virtualiseeritud. Kui SQL Server on virtualiseeritud, peab ketta alamsüsteem olema kiire SAN või sellega samaväärne. Kõigil juhtudel veenduge, et virtuaalhosti põhiseadistus oleks hästi kättesaadav ja liiane. Ühelgi juhul ei tohiks virtualiseerimise kasutamisel teha ühtki VM-i hetkvõtet.

## <a name="software-requirements-for-all-server-computers"></a>Kõigi serveriarvutite tarkvaranõuded
Enne kui arvutisse saab installida rakenduse Finance and Operations (kohapealne) mis tahes komponendi, peab selles olema järgmine tarkvara.

- Microsoft .NET Framework 4.5.1 või kõrgem versioon
- Service Fabric Lisateabe saamiseks vaadake jaotist [Service Fabricu kogumi kavandamine ja ettevalmistamine](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>Toetatud serveri operatsioonisüsteemid
Järgmises tabelis on toodud serveri operatsioonisüsteemid, mida rakenduse Finance and Operations komponendid toetavad.

| Operatsioonisüsteem                                     | Märkmed                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------|
| Microsoft Windows Server 2016 Datacenter või Standard | Need nõuded kehtivad andmebaasi ja Service Fabricu kogumi jaoks, mis majutab AOS-i. |

## <a name="software-requirements-for-database-servers"></a>Andmebaasiserverite tarkvaranõuded

- Toetatakse ainult SQL Server 2016 64-bitist versiooni.
- Tootmiskeskkonnas soovitame installida kasutatava SQL Serveri versiooni uusima koondvärskenduse (CU).
- Finance and Operations (kohapealne) toetab Unicode’i sortimisreegleid, mis on tõstutundetud, rõhumärgitundlikd, kana-tundlikud ja laiusetundetud. Sortimisreeglid peavad vastama AOS-i eksemplare käitavate arvutite Windowsi lokaadile. Uue installi seadistamisel soovitame valida SQL Serveri sortimisreeglite asemel Windowsi sortimisreeglid. Lisateavet SQL Serveri andmebaasi jaoks sortimisreeglite valimise kohta vaadake jaotisest [SQL Serveri dokumentatsioon](/sql/sql-server/sql-server-technical-documentation).
Järgmises tabelis on toodud SQL Serveri versioonid, mida rakenduse Finance and Operations andmebaasid toetavad. Lisateabe saamiseks vaadake [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016)i minimaalseid riistvaranõudeid.

| Vajadus                                                      | Märkmed                                                                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Microsoft SQL Server 2016 Standard Edition või Enterprise Edition | SQL Server 2016 riistvaranõudeid vaadake jaotisest [Riist- ja tarkvaranõuded SQL Server 2016 installimiseks](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-client-computers"></a>Klientarvutite tarkvaranõuded
Veebirakendust Finance and Operations saab käitada igas seadmes, milles on HTML5.0-ga ühilduv veebibrauser. Kindlad Microsofti kinnitatud seadme/brauseri kombinatsioonid on järgmised.

- Microsoft Edge (viimane avalikult saadaolev versioon) Windows 10-s
- Internet Explorer 11 operatsioonisüsteemides Windows 10, Windows 8.1 või Windows 7
- Google Chrome (viimane avalikult saadaolev versioon) operatsioonisüsteemides Windows 10, Windows 8.1, Windows 8, Windows 7 või tahvelarvuti Google Nexus 10
- Apple Safari (viimane avalikult väljastatud versioon) operatsioonisüsteemides Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) või 10.12 (Sierra) või Apple iPad

## <a name="software-requirements-for-active-directory-federation-services"></a>Teenuste Active Directory Federation Services tarkvaranõuded 
Active Directory Federation Services (AD FS) serveris Windows Server 2016

Domeenikontroller peab olema Windows Server 2012 R2 või uuem ja domeeni funktsionaalsustase peab olema 2012 R2 või suurem

Lisateabe saamiseks domeeni funktsionaalsustasemete kohta vt: 
- [Mis on Active Directory funktsionaalsustasemed?](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Active Directory domeeniteenuste funktsionaalsustasemete mõistmine](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>Jaemüügikomponentide riist- ja tarkvaranõuded
Finance and Operations (kohapealne) ei sisalda praegu jaemüügikomponente.

<a name="see-also"></a>Vt ka
--------

[Rakenduse Dynamics 365 for Finance and Operations, Enterprise Editioni hindamiskoopia hankimine](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)

