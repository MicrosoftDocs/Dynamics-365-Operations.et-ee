---
title: "Andmete versioonitäiendus liivakastikeskkonnas"
description: "Selles teemas selgitatakse, kuidas teha andmete liivakastikeskkonnas versioonitäiendust AX 2012-st Dynamics 365 for Finance and Operationsiks."
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
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
ms.openlocfilehash: 7140bf740f37a5eb970a5103750a7095d12a33cc
ms.contentlocale: et-ee
ms.lasthandoff: 06/15/2017

---

# <a name="data-upgrade-in-a-sandbox-environment"></a>Andmete versioonitäiendus liivakastikeskkonnas

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

Selle ülesande väljund on täiendatud andmebaas, mida saab kasutada liivakastikeskkonnas. Liivakastikeskkond on keskkond, kus ärikasutajad ja funktsionaalse töörühma liikmed saavad rakenduse funktsioone kontrollida. See funktsioon sisaldab kohandusi ja Microsoft Dynamics AX 2012-st üle toodud andmeid.

Soovitame tungivalt käivitada andmete versioonitäienduse protsessi arenduskeskkonnas, enne kui käivitate selle jagatud liivakastikeskkonnas, kuna see lähenemine aitab vähendada üldist aega, mida on edukaks andmete versioonitäienduseks vaja. Lisateavet leiate jaotisest [Andmete versioonitäiendus arenduskeskkonnas](prepare-data-upgrade.md).

## <a name="overview-of-the-sandbox-data-upgrade-process"></a>Liivakastikeskkonnas andmete versioonitäienduse protsessi ülevaade

Enne andmete versioonitäienduse alustamist liivakastikeskkonnas olete juba täiendanud andmed arenduskeskkonnas, nagu on selgitatud jaotises [Andmete versioonitäiendus arenduskeskkonnas](prepare-data-upgrade.md). Need kaks protsessi on väga sarnased. Peamine erinevus seisneb selles, et liivakastikeskkond kasutab Microsoft Azure SQL-i andmebaasi, samas kui arenduskeskkond kasutab Microsoft SQL Serverit. See tehniline erinevus andmebaasikihis nõuab, et muudaksite liivakastikeskkonnas veidi andmete versioonitäienduse protseduuri, kuna varukoopiat AX 2012 andmebaasist ei saa lihtsalt SQL-i andmebaasi taastada.

![Liivakastiandmete versioonitäienduse protsess](./media/data-upgrade-sandbox.png)

Siin on versioonitäienduse protsessi kõrgetasemelised etapid.

1. Tehke AX 2012 andmebaasist koopia. Soovitame tungivalt koopiat kasutada, kuna eksporditavast koopiast tuleb mõned objektid kustutada.
2. Eksportige kopeeritud andmebaas Bacpaci faili, kasutades tasuta SQL Serveri tööriista nimega SQLPackage.exe. See tööriist annab erilist tüüpi andmebaasi varukoopia, mille saab SQL-i andmebaasi importida.
3. Laadige Bacpaci fail Azure’i mällu üles.
4. Laadige Bacpaci fail liivakastikeskkonnas rakendusobjekti serveri (AOS) seadmesse alla ja seejärel importige see, kasutades faili SQLPackage.exe. Seejärel tuleb käivitada imporditud andmebaasi suhtes skript SQL-i andmebaasi kasutajate lähtestamiseks.
5. Käivitage pakett MajorVersionDataUpgrade.zip andmete versioonitäienduse käivitamiseks imporditud andmebaasi suhtes.

## <a name="create-a-copy-of-the-ax-2012-database"></a>Tehke AX 2012 andmebaasist koopia

Täiendatavast AX 2012 andmebaasist tuleb teha koopia, kuna peate andmebaasist mõned objektid kustutama. Nende objektide hulka kuuluvad kõik Microsoft Windowsi autentimise kasutajad. Need muudatused teevad muudetud andmebaasi AX 2012 puhul kasutamatuks. Selle toimingu käigus teete andmebaasist koopia ja kustutate need objektid.

Selle toimingu peab tegema andmebaasi administraator (DBA) või isik, kellel on sarnased teadmised ja kogemused.

Andmebaasist koopia tegemiseks tehke algsest andmebaasist varukoopia ja taastage see uue nimega. Veenduge, et mõlema andmebaasi jaoks oleks piisavalt vaba ruumi. Saate luua koopia teises serveris. SQL Serveri eksemplari versioon, mis andmebaasi käitab, pole oluline.

Siin on näide koodist, mis loob andmebaasi koopia. Peate seda näidet muutma nii, et see kajastaks teie konkreetse andmebaasi nimesid.

    BACKUP DATABASE [AxDB] TO  DISK = N'D:\Backups\axdb_copyForUpgrade.bak' WITH NOFORMAT, NOINIT,  
    NAME = N'AxDB_copyForUpgrade-Full Database Backup', SKIP, NOREWIND, NOUNLOAD, COMPRESSION,  STATS = 10
    GO

    RESTORE DATABASE [AxDB_copyForUpgrade] FROM  DISK = N'D:\Backups\axdb_copyForUpgrade.bak'   WITH  FILE = 1,  
    MOVE N'AXDBBuild_Data' TO N'F:\MSSQL_DATA\AxDB_copyForUpgrade.mdf',  
    MOVE N'AXDBBuild_Log' TO N'G:\MSSQL_LOGS\AxDB_CopyForUpgrade.ldf',  
    NOUNLOAD,  STATS = 5

Kui koopia on loodud, käivitage selle suhtes skript Transact-SQL (T-SQL).
TEGEVUSED 

### <a name="export-the-copied-database-to-a-bacpac-file"></a>Eksportige kopeeritud andmebaas Bacpaci faili

Eksportige kopeeritud andmebaas Bacpaci faili, kasutades tööriista SQLPackage.exe. Selle sammu peaks tegema DBA või töörühma liige, kellel on samaväärsed teadmised.

Väga tähtis on installida enne selle toimingu alustamist SQL Server Management Studio. Kuigi SQLPackage on olemas Management Studio eelmistes versioonides, ei toimi see õigesti, kui te pole esmalt uusimat versiooni installinud.

See etapp on oluline, kuna eksportimine tuleb seisuajal enne kasutuselevõtmist uuesti teha. Siin on mõned nõuanded.

- Bacpaci protsess kasutab väga intensiivselt I/O-d ja protsessorit. Seetõttu käivitage eksport võimsal seadmel.
- SQLPackage tuleb käivitada kohalikult andmebaasi majutavas seadmes. Ärge käivitage SQLPackage’it kohalikul sülearvutl, mis on andmebaasiseadmega ühendatud, kuna see protsess kasutab ka intensiivselt võrku.

Järgmiseks avage administraatorina **käsuviiba** aken ja käivitage järgmised käsud.

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:export /ssn:localhost /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=1200 /p:VerifyFullTextDocumentTypesSupported=false

Siin on parameetrite selgitus.

- **ssn** (lähteserveri nimi) – SQL Serveri nimi, millest eksportida. Meie protsessi puhul tuleb selleks parameetriks määrata alati **localhost**.
- **sdn** (lähteandmebaasi nimi) – eksporditava andmebaasi nimi.
- **tf** (sihtfail) – selle faili tee ja nimi, millesse eksportida. Kaust peab juba olemas olema, kuid faili loob protsess.
- **/p:CommandTimeout** – päringupõhine aegumisväärtus. See parameeter võimaldab eksportida aegumiseta suuremaid tabeleid.

### <a name="upload-the-bacpac-file-to-azure-storage"></a>Laadige Bacpaci fail Azure’i mällu üles

Laadige Bacpaci fail Azure’i mällu üles. Vt dokumendi UsingStorageExplorer.docx osa TEGEVUSED

### <a name="import-the-bacpac-file-into-sql-database"></a>Importige Bacpaci fail SQL-i andmebaasi

Selles etapis imporditakse eksporditud Bacpaci fail SQL-i andmebaasi eksemplari, mida teie liivakastikeskkond kasutab. Peate esmalt installima oma liivakasti AOS-i seadmesse Management Studio uusima versiooni. Seejärel tuleb fail importida, kasutades tööriista SQLPackage.exe.

Need ülesanded täidetakse otse AOS-i seadmel teie liivakastikeskkonnas, kuna on olemas tulemüüri reeglid, mis piiravad juurdepääsu SQL-i andmebaasieksemplarile. Kuid AOS-i seadme abil saate juurdepääsu.

Ekspordietapi puhul peab teil olema enne importimise alustamist uusim Management Studio versioon. See etapp ei toimi, kui teil on vanem versioon.

Jõudluse huvides soovitame panna Bacpaci faili AOS-i seadmel D-kettale. Azure’ virtuaalsete seadmete (VM-ide) D-ketas on füüsiline ketas, mille jõudlus on teiste ketaste omast tavaliselt parem.

Avage administraatorina **käsuviiba** aken ja käivitage järgmised käsud.

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:<azure sql database server name>.database.windows.net /tu:sqladmin /tp:<password from LCS> /tdn:<New database name> /p:CommandTimeout=1200 /p:DatabaseEdition=Premium /p:DatabaseServiceObjective=P1

Siin on parameetrite selgitus.

- **tsn** (sihtserveri nimi) – SQL Azure’i serveri nimi, kuhu importida. Leiate nime LCS-ist. Pange selle lõppu **.database.windows.net**.
- **tdn** (sihtandmebaasi nimi) – andmebaasi nimi, kuhu importida. Andmebaas peab juba olemas olema. Impordiprotsess loob selle.
- **sf** (lähtefail) – selle faili tee ja nimi, millest importida.
- **tp** (sihtparool) – SQL-i sihtandmebaasi eksemplari SQL-i parool.
- **tu** (sihtkasutaja) – SQL-i sihtandmebaasi eksemplari SQL-i kasutajanimi. Soovitame kasutada nime **sqladmin**. Selle kasutaja parooli saate tuua oma LCS-i projektist.
- **/p:CommandTimeout** – päringupõhine aegumisväärtus. See parameeter võimaldab eksportida aegumiseta suuremaid tabeleid.
- **/p:DatabaseServiceObjective** – loodava andmebaasi teenusejärgu tase. Olemasoleva andmebaasi väärtust saate vaadata Management Studio abil. Tehke andmebaasil paremklõps ja valige siis **Atribuudid**.

Pärast käskude käitamist saate järgmise hoiatuse. Võite seda julgesti eirata.

![Liivakasti tõrge](./media/sandbox-2.png)
 
### <a name="run-the-majorversiondataupgradezip-package"></a>Käivitage pakett MajorVersionDataUpgrade.zip

Käivitage andmete versioonitäienduse juurutatav pakett, nagu on kirjeldatud jaotises [Andmete versioonitäiendus arendus-, demo- või liivakastikeskkonnas](upgrade-data-to-latest-update.md).

### <a name="upgrade-a-copy-of-the-database-in-a-development-environment"></a>Andmebaasieksemplari versioonitäiendus arenduskeskkonnas

Sama andmebaasi versiooni tasub täiendada arenduskeskkonnas. Kui teil on olemas andmebaasieksemplar arenduskeskkondade jaoks, on palju lihtsam uurida täiendatud versiooniga liivakastikeskkonnas avastatud vigu.

