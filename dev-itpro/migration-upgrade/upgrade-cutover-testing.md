---
title: "Versioonitäienduse ülemineku testimine"
description: "Selles teemas selgitatakse, kuidas testida ülesandeid, mis toimuvad pärast AX 2012 väljalülitamist, kuid enne Dynamics 365 for Finance and Operations, Enterprise editioni sisselülitamist."
author: tariqbell
manager: AnnBe
ms.date: 05/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations, UnifiedOperations, Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 711ad5cc3aafacf209704349effb4e08019205ac
ms.contentlocale: et-ee
ms.lasthandoff: 06/15/2017

---

# <a name="upgrade-cutover-testing"></a>Versioonitäienduse ülemineku testimine

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

*Üleminek* on mõiste, mida kasutame uue süsteemi töölepaneku lõpliku protsessi kohta. See üleminekuprotsess koosneb toimingutest, mis tehakse pärast Microsoft Dynamics AX 2012 väljalülitamist, kuid enne Microsoft Dynamics 365 for Finance and Operations, Enterprise editioni sisselülitamist. Versioonitäienduse ülemineku testimise eesmärk on harjutada üleminekuprotsessi, et tagada sujuv kogemus kõigile, kes tegeliku üleminekuga seotud on.

Ülemineku käigus on kaks peamist töövoogu.

- **Tehniline töövoog** – see töövoog sisaldab andmete versioonitäienduse käivitamisprotsessi. Teie ettevõte rakendab lubatud seisuaja hulgale piirmäära. Selle seisuaja jooksul ei ole AX 2012 ega Finance and Operations saadaval. Sellel töövool võib olla vaja ettevõtte seisuaja piiride järgimiseks andmete versioonitäienduse protseduuri häälestada.
- **Funktsionaalne töövoog** – see töövoog sisaldab konfigureerimistoiminguid, mis tehakse pärast andmete versioonitäienduse lõpuleviimist. Kõik need toimingud tuleb dokumenteerida ja kvantifitseerida ning tuleb määrata ressurss, kuna nii funktsionaalne kui ka tehniline töövoog peavad mahtuma ettevõtte seisuaja piiridesse.

Järgmisel illustratsioonil on näidatud üldine protsess ülemineku käikulaskmiseks, nagu see tootmiskeskkonnas toimub.

![Üleminekuprotsess](./media/cutover_1.png)

Üleminekuprotsess erineb põhilisest andmete versioonitäiendusest liivakastikeskkonnas järgmiste omaduste poolest.

- AX 2012 andmebaasi ei kopeerida, vaid üksnes varundatakse ja siis muudetakse algset andmebaasi. See lähenemine on kiirem ja varundamine võimaldab tagasivõtmist, kui tagasivõtmine on vajalik.
- Kuna Finance and Operationsi tootmiskeskkonnal on piiratud juurdepääs, siis teeb varem rakendusobjekti serveri (AOS) liivakastieksemplariga tehtud tegevused nüüd Microsoft DSE töörühm. Need andmed hõlmavad Bacpaci faili allalaadimist ja importimist ning paketi MajorversionDataUpgrade.zip käitamist.
- Lisasime järgmised ülesanded.

    - Tehke suitsukatse.
    - Tehke rakenduse seadistustoimingud. See etapp võib olla suur, olenevalt funktsioonist, mida kasutatakse. Selle etapi käigus konfigureerib funktsioonitöörühm uue rakenduse funktsiooni, et see oleks täiendatud süsteemis kasutamiseks valmis.
    - Lubage kasutajad uuesti sisse. Teavitage oma kasutajabaasi, et versioonitäiendus on tehtud ja nad võivad süsteemi jälle kasutada.

## <a name="technical-workstream"></a>Tehniline töövoog

Tehniline töövoog hõlmab mitmesuguseid tehnilise töörühma liikmeid: andmebaasiadministraator (DBA), AX 2012 süsteemiadministraator, serveriadministraatorid ja arendajad, kes on kursis rakendustega AX 2012 ning Finance and Operations. Selles teemas selgitatakse, millised ülesanded milliseid rolle hõlmavad.

Üleminekukatsete ajal keskendub tehniline töörühm andmete versioonitäienduse protsessi jõudluse ja töökindluse kontrollimisele, veendumaks, et see järgib ettevõtte seisuaja piire. Selle protsessiga on seotud paljud riist- ja tarkvaraelemendid. Mõned neist elementidest on asutusesisesed, samas kui teised on Microsofti pilves. Lisaks on hõlmatud paljud kohandatud rakenduse koodi ja standardkoodi elemendid. Selle testimise tulemus peaks olema usaldusväärne üleminekuprotsess teie keskkonnas.

### <a name="turn-off-the-ax-2012-aos-instances"></a>AX 2012 AOS-i eksemplaride väljalülitamine

See ülesanne hõlmab AX 2012 süsteemiadministraatoreid ja serveriadministraatoreid.

Kontrollida tuleks järgmisi parameetreid.

- **Ülemineku ajal töötavad pakett-tööd** – pikalt kestev pakett-töö, mis juba käib, takistab süsteemi seiskumist. Plaanige ette, et saaksite oma AOS-i eksemplarid soovitud hetkel seisata. Paketid võib olla vaja plaanida nii, et need oleksid lõpetatud veidi enne, kui AX 2012 sisse lülitate.
- **Integreeritud süsteemid** – teil võib olla teisi AX 2012 keskkonnaga integreeritud süsteeme. Peate neid süsteeme AX 2012 väljalülitamise plaanis arvestama. Näiteks võib olla vaja lülitada integreeritud süsteemid välja mõni aeg enne AX 2012 enese väljalülitamist, et kõik järelejäänud pooleliolevad kanded saaksid lõpetatud. Integreeritud süsteemide nõuded erinevad suuresti ettevõtete lõikes. Seetõttu peab teie asjatundjate töörühm plaanima selle stsenaariumi iseseisvalt.

### <a name="create-a-backup-of-the-ax-2012-database"></a>Looge AX 2012 andmebaasist varukoopia

See ülesanne hõlmab DBA-d. Kui on vajalik tagasivõtmine, kasutatakse varukoopiat. Seda kasutatakse ka viitepunktina, mida hoitakse teatud perioodi jooksul alles ja mis näitab süsteemi olekut ülemineku hetkel.

Kontrollida tuleks järgmisi parameetreid.

- Hankige varundamisprotsessile konkreetne ajastus.
- Kohandage kasutatavaid varuvõimalusi (nt tihendamine vs mittetihendamine), et oleks tagatud kiireim võimalik varundamine.

### <a name="export-the-database-to-bacpac"></a>Eksportige andmebaas Bacpaci

See ülesanne hõlmab DBA-d. Selle ülesande väljund on ekspordifail, mis laaditakse uue süsteemi jaoks Microsoft Azure’i üles.

Kontrollida tuleks järgmisi parameetreid.

- Hankige varundamisprotsessile konkreetne ajastus.
- Optimeerige ekspordiprotsessi, et tagada võimalikult kiire kogemus. Optimeerimine võib nõuda järgmisi toiminguid.

    - Mõõtke ekspordi ajal süsteemi ressursse (nt protsessor, ketta I/O ja mälu).
    - Ressursi kitsaskohtade leidmisel koostage plaan nende leevendamiseks. Tavaliselt leevendatakse neid kitsaskohti, määrates rohkem vajalikku ressurssi.

### <a name="upload-the-bacpac-file-to-azure-storage"></a>Laadige Bacpaci fail Azure’i mällu üles

See ülesanne hõlmab DBA-d või serveri administraatoreid. Selle ülesande käigus teisaldatakse Bacpaci fail Azure’i.

Kontrollida tuleks järgmisi parameetreid.

- Valige seade, mida üleslaadimiseks kasutatakse, ja veenduge, et Azure’i mälu uurimistööriist oleks konfigureeritud ja kasutusvalmis.
- Hankige konkreetsed üleslaadimisprotsessi ajastused, mõõtes seda mitu korda. Üleslaadimise aeg on erinev, olenevalt Interneti-ühenduse kiirusest ja Azure’i andmekeskuse geograafilisest asukohast teie asukoha suhtes.

### <a name="download-and-import-the-bacpac-file-to-the-azure-sql-database"></a>Laadige alla ja importige Bacpaci fail Azure SQL-i andmebaasi

Kui see ülesanne toimub kasutuselevõtmise ajal, teeb selle Microsoft DSE töörühm. Kuid ülemineku testimise käigus on sellega seotud teie andmebaasi administraator. Selle ülesande tulemus on ekspordifail, mis laaditakse uue süsteemi jaoks Azure’i üles.

Kontrollida tuleks järgmisi parameetreid.

- Hankige impordiprotsessile konkreetne ajastus.
- Optimeerige ekspordiprotsessi, et tagada võimalikult kiire kogemus. Optimeerimine võib nõuda järgmisi toiminguid.

    - Mõõtke eksportimise ajal süsteemi ressursse. Järgmisena on toodud mõned näited.

        - **AOS-i seadmel:** protsessor, ketta I/O ja mälu
        - **Azure SQL-i andmebaasi eksemplar:** SQL-i andmebaasi läbilaskevõime (DTU). Azure’i SQL-i DTU-d saab jälgida AOS-i seadmel Microsoft SQL Server Management Studios, vaadates süsteemi vaadet sys.dm_resource_stats system.

    - Ressursi kitsaskohtade leidmisel koostage plaan nende leevendamiseks. Tavaliselt leevendatakse neid kitsaskohti, määrates rohkem vajalikku ressurssi. Kuna seda masinat hostib Microsoft, peate esitama Microsoftile taotluse ressursside suurendamiseks, kui tuvastate, et tegemist on kitsaskohaga.

### <a name="run-the-majorversiondataupgradezip-package"></a>Käivitage pakett MajorVersiondataUpgrade.zip

Kui see ülesanne toimub kasutuselevõtmise ajal, teeb selle Microsoft DSE töörühm. Kuid ülemineku testimise ajal on sellega seotud arendajad. Selle ülesande käigus teisendatakse vana andmebaasi struktuur uue süsteemi struktuuriks.

Andmebaasi sünkroonimisprotsess töötab selle ülesande osana. Andmebaasi sünkroonimine võib mõnes olukorras märkimisväärselt aega võtta, nt kui tabelil on kobarindeks muutunud, kuna see toiming on SQL-is kulukas.

Soovitame tungivalt teha analüüsimis- ja silumisprotsessi kõigepealt arenduskeskkonnas. Liivakastikeskkonnas on silumise ja analüüsi valikud rohkem piiratud. Eesmärk on väike arv (või üldse mitte) probleeme, mis tuleb üleminekutestide käigus lahendada.

Kontrollida tuleks järgmisi parameetreid.

- Hankige impordiprotsessile konkreetne ajastus.
- Optimeerige protsessi, et tagada kiireim kogemus. Optimeerimine võib nõuda järgmisi toiminguid.

    - Jälgige eraldi versioonitäienduse skriptide toimimist tabeli ReleaseUpdateScriptsExecution kaudu.
    - Kohandage skripte toimivuse optimeerimiseks. See toiming võib nõuda skripti X++ koodi kohandamiseks selle optimeerimiseks andmekogumi jaoks.
    - Jälgige Azure SQL-i DTU-d, kasutades teenuse Microsoft Dynamics Lifecycle Services (LCS) jälgimist või süsteemivaadet sys.dm_resources_stats in Management Studios. Kui ressursid on maksimaalselt kasutatud, võib olla vaja küsida Microsoft DSE töörühmalt kõrgemat andmebaasi taset.

### <a name="roll-back-to-ax-2012"></a>Võtke tagasi AX 2012

Selle ülesande eesmärk on taastada andmebaas, kasutades varukoopiat, mis tehti AX 2012 väljalülitamisel, ja lülitage AX 2012 siis uuesti sisse. Integreeritud süsteemide olekut võib olla samuti vaja taastada. Kuid kuna integreeritud süsteemid on ettevõtete lõikes erinevad, tuleb see stsenaarium eraldi plaanida, lähtudes teie konkreetsetest tingimustest. Kuigi eelmise versiooni tagasivõtmise vajadus on ebatõenäoline, on väga oluline, et teil oleks äraproovitud protsess juhuks, kui seda peaks olema vaja teha.

## <a name="functional-workstream"></a>Funktsionaalne töövoog

Pärast andmete versioonitäiendust on uues keskkonnas vaja teha mitu konfiguratsioonitoimingut. Selle töövoo eesmärk on dokumenteerida ja kvantifitseerida kõik konfigureerimistoimingud ja määrata igale toimingule ressurss, et tagada võimalus teha neid toiminguid koos tehnilise töövooga seisuaja jooksul.

Tavaliselt hõlmavad funktsionaalsed toimingud konkreetsete süsteemi parameetrite väärtuste või muude konfigureerimisandmete muutmist. Need toimingud selgitatakse välja täieliku funktsionaalse testi läbiviimisel, mis on üleminekutestist eraldi tegevus. Seda tüüpi ülesande tuvastamisel tuleks see vaadata üle koos funktsionaalse ressursi ja teie arendajaga.

Suuremad muudatused võivad nõuda uue kohandatud andmete versioonitäienduse skripti kirjutamist andmete uuendamiseks andmetäienduse protsessi käigus. Kuid funktsionaalne ressurss saab teha uue süsteemi kaudu pärast andmete versioonitäiendust käsitsi väiksemaid muudatusi.

Suuremaid muudatusi, millel on uued andmete versioonitäienduse skriptid, tuleb testida. Seetõttu tuleb käivitada vähemalt üks paketi täiendav MajorVersionDataUpgrade.zip kordus. On oluline, et kaaluksite paketi teistkordse käitamise kulu võrreldes andmete käsitsi sisestamise kuluga.

Iga käsitsi tehtava muudatuse puhul tuleb üleminekuplaani dokumenti lisada ülesanne. Selles ülesandes peavad olema näidatud järgmised andmed.

-   Mis on ülesanne ja mida on vaja teha?
-   Kes seda tegema peab?
-   Kui kaua see aega võtab?

