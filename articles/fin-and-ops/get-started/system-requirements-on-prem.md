---
title: "Asutusesiseste juurutuste süsteeminõuded"
description: "Selles teemas esitatakse süsteeminõuete loend rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition kohapealsete juurutuste jaoks."
author: kfend
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 5230911e1febc66b294f1331846373a472789adf
ms.openlocfilehash: 721c5851cd399398a8dcec5ae110b97a4f17ae0a
ms.contentlocale: et-ee
ms.lasthandoff: 08/04/2017

---

# <a name="system-requirements-for-on-premises-deployments"></a>Asutusesiseste juurutuste süsteeminõuded

[!include[banner](../includes/banner.md)]

Selles teemas esitatakse süsteeminõuete loend rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition kohapealsete juurutuste jaoks. Enne rakenduse Finance and Operations installimist kontrollige vajaduse korral, kas süsteem, millega töötate, vastab minimaalsetele võrgu-, riistvara- või tarkvaranõuetele või ületab neid.

## <a name="network-requirements"></a>Võrgunõuded
Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (kohapealne) töötab võrkudes, mis kasutavad Internet Protocoli versiooni 4 (IPv4) või Internet Protocoli versiooni 6 (IPv6). Võtke süsteemi kavandamisel arvesse võrgukeskkonda ja kasutage järgmisi juhtnööre.

### <a name="network-response-time"></a>Võrgu reageerimisaeg
Järgmises tabelis on toodud minimaalsed võrgunõuded ühenduse loomiseks veebibrauseri ja rakendusobjekti serveri (AOS) vahel ning AOS-i ja andmebaasi vahel kohapealses süsteemis.

| Väärtus     | Veebibrauserist AOS-i                      | AOS-ist andmebaasi |
|-----------|-----------------------------------------|------------------------------------------------------------------------------------------|
| Ribalaius | 50 kilobaiti sekundis (KB/s) kasutaja kohta | 100 megabaiti sekundis (MB/s) |
| Latentsus   | Kuni 250-300 millisekundit (ms)     | Alla 1 ms (ainult kohtvõrk [LAN]). AOS ja andmebaas peavad olema samas asukohas. |

- Finance and Operations (kohapealne) on mõeldud võrkudele, mille latentsus on kuni 250–300 millisekundit (ms). See on latentsus brauserikliendist andmekeskusse, mis majutab rakendust Finance and Operations.
- Rakenduse Finance and Operations (kohapealne) ribalaiuse nõuded olenevad stsenaariumist. Tavaline stsenaarium nõuab brauseri ja rakenduse Finance and Operations serveri vahel suuremat ribalaiust kui 50 kilobaiti sekundis (KB/s). Stsenaariumide puhul, millel on kõrged kasuliku koormuse nõuded (nt tööruumid või stsenaariumid, mis hõlmavad ulatuslikku kohandamist), on soovitatav kasutada rohkem ribalaiust. Konkreetne ribalaius sõltub kasutusest.

Juurutusi, milles AOS ja Microsoft SQL Serveri andmebaas asuvad erinevates andmekeskustes, ei toetata. AOS ja SQL Serveri andmebaas peavad olema samas asukohas. 

Üldiselt on Finance and Operations optimeeritud vähendama brauseri ja serveri pendellevi. Pendellevi hulk brauserikliendist andmekeskusse on kas null või üks iga kasutaja interaktsiooni kohta ning kasulik koormus on tihendatud.

> [!WARNING]
> Ärge arvutage ribalaiuse nõudeid kliendi asukohast, korrutades kasutajate arvu minimaalsete ribalaiuse nõuetega. Antud asukoha samaaegset kasutust on väga keeruline arvutada. Soovitame rakendada rakenduse Finance and Operations mittetootmiskeskkonnas reaalset simulatsiooni, kasutades teie konkreetse valdkonna parimat jõudlusmõõdikut. 

### <a name="lan-environments"></a>LAN-keskkonnad
Kohtvõrgu (LAN) keskkondades ei ole rakendusega Finance and Operations ühenduse loomiseks Microsofti kaugtöölaud Microsoft Windows Serveris vajalik. Siiski võib kaugtöölaud olla nõutav serverijuurutusi moodustavate VM-ide hooldustöödeks.

### <a name="wan-environments"></a>WAN-keskkonnad
Laivõrgu (WAN) keskkondades ei ole rakendusega Finance and Operations ühenduse loomiseks kaugtöölaud Windows Serveris vajalik.

### <a name="internet-connectivity-requirements"></a>Interneti-ühenduvuse nõuded
Finance and Operations (kohapealne) ei nõua Interneti-ühenduvust lõppkasutajate tööjaamadest. Mõni funktsioon ei pruugi siiski ilma Interneti-ühenduvuseta saadaval olla.

|                    |   |
|--------------------|---|
| **Brauseriklient** | Sisevõrgustsenaarium ilma Interneti-ühenduvuseta on kohapealse juurutuse valiku kujunduspõhimõte. Mõni pilveteenuseid nõudev funktsioon, näiteks spikri- ja tegevuste juhiste teegid teenuses Microsoft Dynamics Lifecycle Services (LCS) ei ole saadaval. |
| **Server**         | AOS-i või Microsoft Azure Service Fabric järgud peavad olema võimelised LCS-iga suhtlema. Asutusesisene brauseriklient ei nõua Internetile juurdepääsu. |
| **Telemeetria**      | Telemeetria andmed võivad kaotsi minna, kui ühenduses on pikki katkestusi. Ühenduvuse katkemine LCS-iga ei mõjuta kohapealse rakenduse funktsionaalsust. |
| **LCS**            | Ühenduvus LCS-iga on nõutav juurutamiseks, koodi juurutamiseks ja hooldustöödeks. |

## <a name="telemetry-data-transfer-to-the-cloud"></a>Telemeetria andmete ülekandmine pilve
Enamik telemeetriat salvestatakse kohalikult ja sellele pääseb juurde Microsoft Windowsi sündmustevaaturiga. Väike hulk telemeetriasündmusi edastatakse diagnostikaks pilves olevale Microsofti telemeetriakonveierile. Kliendi andmed ja lõppkasutaja identifitseeritavad andmed ei kuulu Microsoftile saadetava telemeetria alla. VM-ide nimed saadetakse Microsoftile, et abistada keskkondade haldamisel ja diagnostikal LCS-i portaalist.

## <a name="domain-requirements"></a>Domeeninõuded
Võtke rakenduse Finance and Operations (kohapealne) installimisel arvesse järgmisi domeeninõudeid.

- Virtuaalarvutid, mis majutavad rakenduse Finance and Operations (kohapealne) komponente, peavad kuuluma Active Directory domeeni. Active Directory domeeniteenused (AD DS) peavad olema konfigureeritud omarežiimis.
- Virtuaalarvutid, mis käitavad rakenduse Finance and Operations (kohapealne) komponente, peavad üksteisele juurde pääsema. Juurdepääs konfigureeritakse AD DS-is. 
- Domeenikontroller peab olema Microsoft Windows Server 2012 R2 või uuem ja domeeni funktsionaalsustase peab olema 2012 R2 või suurem

## <a name="hardware-requirements"></a>Riistvaranõuded
Selles jaotises kirjeldatakse rakenduse Finance and Operations (kohapealne) käitamiseks vajalikku riistvara.

Riistvaranõuded erinevad olenevalt süsteemi konfiguratsioonist, andmete koosseisust ning rakendustest ja funktsioonidest, mida otsustate kasutada. Järgnevalt mõni tegur, mis võib mõjutada rakenduse Finance and Operations (kohapealne) jaoks sobiva riistvara valimist.

- Kannete arv tunnis
- Samaaegsete kasutajate arv

## <a name="minimum-infrastructure-requirements"></a>Minimaalsed taristunõuded
Finance and Operations (kohapealne) kasutab AOS-i, partii, andmehalduse, halduse aruandja ja keskkonna korraldusteenuste majutamiseks Service Fabricit. Microsoft SQL Serveri aruandlusteenuseid (SSRS) ei majutata Service Fabrici kogumis.

SQL Server peab olema seadistatud suure kättesaadavuse HADRON-i seadistuses, millel on tootmises kasutamiseks vähemalt kaks režiimi.

Järgmisel joonisel on toodud sõlmede soovituslik miinimumarv teie Service Fabrici kogumis.

[![Sõlmede soovituslik miinimumarv teie Service Fabrici kogumis](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>Protsessori ja RAM-i nõuded
Järgmistes tabelites on toodud protsessorite arv ja muutmälu (RAM) maht, mis on vajalik igale selle juurutusvaliku käitamiseks nõutavale rollile. Lisateabe saamiseks vaadake Service Fabricu eraldiseisva kogumi jaoks soovitatud miinimumnõudeid [Service Fabricu kogumi kavandamine ja ettevalmistamine](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

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

**Minimaalsed suuruseprognoosid tootmis- ja liivakastikeskkonna juurutuste puhul\***

| Topoloogia                                        | Roll                          | Eksemplaride arv |
|-------------------------------------------------|-------------------------------|---------------------|
| Tootmine                                      | AOS (andmehaldur, partii)  | 3                   |
|                                                 | Halduse aruandja           | 2                   |
|                                                 | SQL Serveri aruandlusteenused | 1                   |
|                                                 | Korraldaja\*\*              | 3                   |
| Liivakast                                         | AOS, andmehaldur, partii   | 2                   |
|                                                 | Halduse aruandja           | 1                   |
|                                                 | SQL Serveri aruandlusteenused | 1                   |
|                                                 | Korraldaja                  | 3                   |
| *Tootmis- ja liivakastitopoloogiate kokkuvõte* |                               | *16*                |

\* Selles tabelis esitatud numbreid kontrollivad meie eelvaatekliendid ja numbrites võib toimuda muudatusi klientide tagasiside põhjal.

\*\* Korraldaja on määratud primaarseks sõlmetüübiks ja seda kasutatakse ka Service Fabricu teenuste käitamiseks.

**SQL-tagaserveri ja AD DS-i algsed prognoosid**

<table>
<thead>
<tr>
<th></th>
<th>Roll</th>
<th>Virtuaalarvutid/Eksemplarid</th>
<th>Tuumad</th>
<th>Tuumade koguarv</th>
<th>Mälu eksemplari kohta (GB)</th>
<th>Kogu mälu (GB)</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="3"><strong>Ühistaristu</strong></td>
<td>SQL-i server*</td>
<td>2</td>
<td>8</td>
<td>16</td>
<td>32</td>
<td>64</td>
</tr>
<tr>
<td>Failiserver/Salvestusruumi võrk/Saadaolev salvestusruum</td>
<td colspan="5"><p>Tagasalvestusruum peab põhinema välkdraivil (SSD) käitusaja salvestusruumi võrgus (SAN).</p>
<p>Suuruse ja sisendi/väljundi operatsioonide arv sekundis (IOPS) põhineb töökoormusel.</p></td>
</tr>
<tr>
<td>Active Directory</td>
<td>3</td>
<td>4</td>
<td>12</td>
<td>16</td>
<td>48</td>
</tr>
<tr>
<td><em>Ühistaristu kokkuvõte</em></td>
<td></td>
<td><em>5</em></td>
<td></td>
<td><em>28</em></td>
<td></td>
<td><em>112</em></td>
</tr>
</tbody>
</table>

\*SQL Serveri suurused sõltuvad oluliselt töökoormusest. Lisateavet vaadake teemast [Riistavara suuruse muutmine kohapealsete keskkondade puhul](hardware-sizing-on-premises-environments.md).

## <a name="storage"></a>Ladustamine

- **AOS** – Finance and Operations (kohapealne) kasutab struktuurimata andmete talletamiseks serveri teateploki (SMB) 3.0 ühiskasutust. Lisateavet vaadake jaotisest [Storage Spaces Direct Windows Server 2016-s](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL** – võimalikud on järgmised valikud.

    - Väga saadaval SSD seadistamine
    - Veebikannete töötlemise (OLTP) läbilaskeks optimeeritud SAN
    - Kõrge jõudlusega otse ühendatud talletusruum (DAS) 

- **SQL Serveri ja andmehalduse IOPS** – talletusruum nii andmehalduse kui ka SQL Serveri jaoks peab võimaldama vähemalt 2000 sisend-/väljundtoimingut sekundis (IOPS). Tootmise IOPS sõltub paljudest teguritest. Lisateavet vaadake teemast [Riistavara suuruse muutmine kohapealsete keskkondade puhul](hardware-sizing-on-premises-environments.md).
- **VM IOPS** – igal virtuaalarvutil peaks olema vähemals 100 kirjutamise IOPS-i.

## <a name="virtual-host-requirements"></a>Virtuaalhosti nõuded
Virtuaalhostide seadistamisel rakenduse Finance and Operations (kohapealne) keskkonna jaoks vaadake järgmisi juhtnööre: [Service Fabricu kogumi kavandamine ja ettevalmistamine](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) ning [Service Fabricu kogumi kirjeldamine](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). Igal virtuaalhostil peab olema piisav arv tuumi selle taristu jaoks, mille suurust muudetakse. Võimalikud on mitu täpsemat konfiguratsiooni, kus SQL Server asub füüsilisel riistvaral, kuid kõik muu on virtualiseeritud. Kui SQL Server on virtualiseeritud, peab ketta alamsüsteem olema kiire SAN või sellega samaväärne. Kõigil juhtudel veenduge, et virtuaalhosti põhiseadistus oleks hästi kättesaadav ja liiane. Ühelgi juhul ei tohiks virtualiseerimise kasutamisel teha ühtki VM-i hetkvõtet.

## <a name="software-requirements-for-all-server-computers"></a>Kõigi serveriarvutite tarkvaranõuded
Enne kui arvutisse saab installida rakenduse Finance and Operations (kohapealne) mis tahes komponendi, peab selles olema järgmine tarkvara.

- Microsoft .NET Frameworki versioon 4.5.1 või uuem
- Service Fabric

Lisateabe saamiseks vaadake teemat [Service Fabricu kogumi kavandamine ja ettevalmistamine](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>Toetatud serveri operatsioonisüsteemid
Järgmises tabelis on toodud serveri operatsioonisüsteemid, mida rakenduse Finance and Operations komponendid toetavad.

| Operatsioonisüsteem                                     | Märkmed |
|------------------------------------------------------|-------|
| Microsoft Windows Server 2016 Datacenter või Standard | Need nõuded kehtivad andmebaasi ja Service Fabricu kogumi jaoks, mis majutab AOS-i. |

## <a name="software-requirements-for-database-servers"></a>Andmebaasiserverite tarkvaranõuded

- Toetatakse ainult SQL Server 2016 64-bitist versiooni.
- Tootmiskeskkonnas soovitame installida kasutatava SQL Serveri versiooni uusima koondvärskenduse (CU).
- Finance and Operations (kohapealne) toetab Unicode’i sortimisreegleid, mis on tõstutundetud, rõhumärgitundlikd, kana-tundlikud ja laiusetundetud. Sortimisreeglid peavad vastama AOS-i eksemplare käitavate arvutite Windowsi lokaadile. Uue installi seadistamisel soovitame valida SQL Serveri sortimisreeglite asemel Windowsi sortimisreeglid. Lisateavet SQL Serveri andmebaasi jaoks sortimisreeglite valimise kohta vaadake jaotisest [SQL Serveri dokumentatsioon](/sql/sql-server/sql-server-technical-documentation).

Järgmises tabelis on toodud SQL Serveri versioonid, mida rakenduse Finance and Operations andmebaasid toetavad. Lisateabe saamiseks vaadake [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016)i minimaalseid riistvaranõudeid.

| Vajadus                                                      | Märkmed |
|------------------------------------------------------------------|-------|
| Microsoft SQL Server 2016 Standard Edition või Enterprise Edition | SQL Server 2016 riistvaranõudeid vaadake jaotisest [Riist- ja tarkvaranõuded SQL Server 2016 installimiseks](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-client-computers"></a>Klientarvutite tarkvaranõuded
Veebirakendust Finance and Operations saab käitada igas seadmes, milles on HTML 5.0-ga ühilduv veebibrauser. Kindlad Microsofti kinnitatud seadme/brauseri kombinatsioonid on järgmised.

- Microsoft Edge (viimane avalikult saadaolev versioon) Windows 10-s
- Internet Explorer 11 operatsioonisüsteemides Windows 10, Windows 8.1 või Windows 7
- Google Chrome (viimane avalikult saadaolev versioon) operatsioonisüsteemides Windows 10, Windows 8.1, Windows 8, Windows 7 või tahvelarvuti Google Nexus 10
- Apple Safari (viimane avalikult väljastatud versioon) operatsioonisüsteemides Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) või 10.12 (Sierra) või Apple iPad

## <a name="software-requirements-for-active-directory-federation-services"></a>Teenuste Active Directory Federation Services tarkvaranõuded 
Active Directory Federation Services (AD FS) on nõutud serveris Windows Server 2016.

Domeenikontroller peab olema Microsoft Windows Server 2012 R2 või uuem ja domeeni funktsionaalsustase peab olema 2012 R2 või suurem Lisateabe saamiseks domeeni funktsionaalsustasemete kohta vt järgmisi lehti.

- [Mis on Active Directory funktsionaalsustasemed?](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Active Directory domeeniteenuste funktsionaalsustasemete mõistmine](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)

## <a name="supported-microsoft-office-applications"></a>Toetatud Microsoft Office’i rakendused
Rakenduse Finance and Operations pilve- ja kohapealsetes juurutustes toetatakse järgmisi Microsoft Office’i rakendusi.

-   Microsoft Exceli ja Microsoft Wordi lisandmooduli käivitamiseks peab teil olema installitud Windowsile või Macile mõeldud Microsoft Office 2016. Versiooninõuete kohta lisateabe saamiseks vaadake teemat [Office’i integratsiooni tõrkeotsing](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Funktsiooniga Ekspordi Excelisse või Ekspordi Wordi loodud dokumentide vaatamiseks peab teil olema installitud Microsoft Office 2007 või uuem versioon.
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>Jaemüügikomponentide riist- ja tarkvaranõuded
Finance and Operations (kohapealne) ei sisalda praegu jaemüügikomponente.

