---
title: Kohapealsete keskkondade seadistamine ja juurutamine
description: Teema sisaldab teavet kohapealse keskkonna plaanimise, seadistamise ja juurutamise kohta.
author: kfend
manager: AnnBe
ms.date: 06/14/2017
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
ms.author: sarvanisathish
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: d100f6dbcbdf8f4c12ab04670fb598a88d48d84b
ms.openlocfilehash: 7caf033ab2de5afd6a2d88fa2d41631df4542cbe
ms.contentlocale: et-ee
ms.lasthandoff: 08/10/2017

---

# <a name="set-up-and-deploy-on-premises-environments"></a>Kohapealsete keskkondade seadistamine ja juurutamine

Dokumendis kirjeldatakse, kuidas oma juurutamist plaanida, infrastruktuuri seadistada ja juurutada rakendust Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (kohapealne).

## <a name="finance-and-operations-components"></a>Rakenduse Finance and Operations komponendid

Rakendus Finance and Operations koosneb kolmest põhikomponendist.

- Rakendusobjekti server (AOS)
- Äriteave (BI)
- Finantsaruandlus/halduse aruandja

Need komponendid sõltuvad järgmisest süsteemitarkvarast.

- Microsoft Windows Server 2016
- Microsoft SQL Serveri 2016 SP1, millel on järgmised funktsioonid.

    - Täisteksti indeksi otsing on lubatud.
    - SQL Serveri aruandlusteenused (SSRS).
    - SQL Serveri integreerimisteenused (SSIS).
    
     > [!NOTE]
     > Rakendus ei tööta, kui täistekstiotsing pole lubatud.

- SQL Serveri haldusstuudio
- Eraldiseisev Microsoft Azure Service Fabric
- Windows PowerShell 5.0 või uuem versioon
- Active Directory Federation Services (AD FS) serveris Windows Server 2016

  Domeenikontroller peab olema Windows Server 2012 R2 või uuem ja domeeni funktsionaalsustase peab olema 2012 R2 või suurem

  Lisateabe saamiseks domeeni funktsionaalsustasemete kohta vt: 
  - [Mis on Active Directory funktsionaalsustasemed?](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
  - [Active Directory domeeniteenuste funktsionaalsustasemete mõistmine](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)


## <a name="lifecycle-services"></a>Elutsükli teenused

Rakenduse Finance and Operations bitid on jaotatud läbi teenuse Microsoft Dynamics Lifecycle Services (LCS). Enne juurutamist peate [Enterprise’i lepingute](https://www.microsoft.com/en-us/Licensing/licensing-programs/enterprise.aspx) kanali kaudu ostma litsentsivõtmed ja seadistama LCS-is kohapealse projekti. Juurutusi saab käivitada ainult LCS-i kaudu. Lisateavet kohapealsete projektide seadistamise kohta LCS-is leiate jaotisest [Kohapealse projekti loomine teenuses Lifecycle Services](../lifecycle-services/lbd-create-lcs-on-prem-project.md).

## <a name="authentication"></a>Autentimine

Kohapealne rakendus töötab AD FS-ga. LCS-iga suhtlemiseks peate konfigureerima ka teenuse Azure Active Directory (Azure AD).

## <a name="standalone-service-fabric"></a>Eraldiseisev Service Fabric

Rakendus Finance and Operations kasutab eraldiseisvat teenust Service Fabric. Lisateavet vt [teenuse Service Fabric dokumentatsioonist](/azure/service-fabric/).

## <a name="infrastructure"></a>Taristu

Rakendus Finance and Operations on mõeldud töötama ülimalt koondunud arhitektuuris. Riistvara konfiguratsioon hõlmab järgmisi komponente.

- Teenuse Service Fabric eraldiseisev kogum, mis põhineb Windows Server 2016 virtuaalsetel masinatel (VM-d)
- SQL Server (toetatud on nii klasterdatud SQL kui ka Always-On)
- AD FS autentimiseks
- Serveri teateploki (SMB) versiooni 3 failiketas talletamiseks
- Valikuline: Microsoft Office Server 2017

Lisateabe saamiseks vt [Süsteeminõuded](../get-started/system-requirements.md) ja suuruse juhised.

### <a name="hardware-layout"></a>Riistvara paigutus

Plaanige oma infrastruktuur ja teenuse Service Fabric kogum vastavalt jaotises [Riistvara suuruse muutmine kohapealsetes keskkondades](../get-started/hardware-sizing-on-premises-environments.md) toodud soovitatud suurustele. Lisateavet teenuse Service Fabric kogumi plaanimise kohta vaadake jaotisest [Teenuse Service Fabric eraldiseisva kogumi juurutamise plaanimine ja ettevalmistamine](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

Järgmises tabelis on toodud riistvarapaigutuse näide. See näide on kogu teemas kasutusel seadistuse illustreerimiseks.

> [!NOTE]
> Teenuse Service Fabric kogumi esmasel sõlmel peab olema vähemalt kolm sõlme. Selles näites on esmase sõlme tüübiks määratud **OrchestratorType**.

| Masina eesmärk                                 | Masina nimi    | IP-aadress    |
|-------------------------------------------------|-----------------|---------------|
| Domeenikontroller                               | DAX7SQLAODC1    | 10.179.108.2  |
| AD FS                                           | DAX7SQLAOADFS1  | 10.179.108.3  |
| Failiserver                                     | DAX7SQLAOFILE1  | 10.179.108.4  |
| SQL-i kogum Always-On                           | DAX7SQLAOSQLA01 | 10.179.108.5  |
|                                                 | DAX7SQLAOSQLA02 | 10.179.108.6  |
|                                                 | DAX7SQLAOSQLA   | 10.179.108.9  |
| Klient                                          | SQLAOCLIENT1    | 10.179.108.11 |
| Teenuse Service Fabric kogum/AOS 1                    | SQLAOSF1AOS1    | 10.179.108.12 |
| Teenuse Service Fabric kogum/AOS 2                    | SQLAOSF1AOS2    | 10.179.108.13 |
| Teenuse Service Fabric kogum/AOS 3                    | SQLAOSF1AOS3    | 10.179.108.14 |
| Teenuse Service Fabric kogum/Orchestrator 1           | SQLAOSF1ORCH1   | 10.179.108.15 |
| Teenuse Service Fabric kogum/Orchestrator 2           | SQLAOSF1ORCH2   | 10.179.108.16 |
| Teenuse Service Fabric kogum/Orchestrator 3           | SQLAOSF1ORCH3   | 10.179.108.17 |
| Teenuse Service Fabric kogum/Halduse aruandja sõlm | SQLAOSMR1       | 10.179.108.18 |
| Teenuse Service Fabric kogum/SSRS-i sõlm                | SQLAOSFBIN1     | 10.179.108.10 |

## <a name="setup"></a>Häälestus

### <a name="prerequisites"></a>Eeltingimused

Enne seadistuse alustamist peavad olema täidetud järgmised eeltingimused. Nende eeltingimuste seadistamine on selle dokumendi ulatusest väljas.

- Active Directory domeeniteenused (AD DS) on teie võrgus installitud ja konfigureeritud.
- AD FS on juurutatud.
- SQL Server, SSRS ja Management Studio on installitud.

### <a name="overview"></a>Ülevaade

Rakenduse Finance and Operations taristu seadistamiseks tuleb lõpule viia järgmised sammud.

1. Domeeninime ja DNS-i tsoonide plaanimine
2. Sertide plaanimine ja omandamine
3. Kasutajate ja teenusekontode plaanimine
4. DNS-i tsoonide loomine ja A-kirjete lisamine
5. VM-de ühendamine domeeniga
6. VM-dele eeltingimuseks oleva tarkvara lisamine
7. Häälestusskriptide LCS-st allalaadimine
8. Konfiguratsiooni kirjeldamine
9. Sertide installimine
10. Teenuse Service Fabric eraldiseisva kogumi seadistamine
11. Rentniku jaoks LCS-i ühenduvuse konfigureerimine
12. Failisalvestusruumi seadistamine
13. SQL Serveri seadistamine
14. Andmebaaside konfigureerimine
15. Identimisteabe krüptimine
16. Seadista SSRS
17. AD FS-i konfigureerimine

### <a name="plan-your-domain-name-and-dns-zones"></a>Domeeninime ja DNS-i tsoonide plaanimine

Soovitame AOS-i tootmisinstalli jaoks kasutada avalikult registreeritud domeeninime. Sel viisil on võimalik sellele väljaspoolt võrku juurde pääseda, kui see peaks vajalik olema.

Näide. Kui teie ettevõtte domeen on contoso.com, võib teie rakenduse Finance and Operations (kohapealne) tsooniks olla d365ffo.onprem.contoso.com ja domeeninimed võivad olla järgmised:

- ax.d365ffo.onprem.contoso.com AOS-i seadmete jaoks;
- sf.d365ffo.onprem.contoso.com teenuse Service Fabric kogumi jaoks.

### <a name="plan-and-acquire-your-certificates"></a>Sertide plaanimine ja omandamine

Teenuse Service Fabric kogumi ja kõigi juurutatud rakenduste kaitsmiseks on nõutavad Secure Sockets Layeri (SSL) serdid. Tootmise ja liivakasti töökoormuste jaoks soovitame hankida serdid, mis pärinevad sertifitseerimisasutuselt (CA) nagu [DigiCert](https://www.digicert.com/ssl-certificate/), [Comodo](https://ssl.comodo.com/), [Symantec](https://www.websecurity.symantec.com/ssl-certificate), [GoDaddy](https://www.godaddy.com/web-security/ssl-certificate), või [GlobalSign](https://www.globalsign.com/en/ssl/). Kui teie domeen on seadistatud [Active Directory serditeenustega](https://technet.microsoft.com/en-us/library/cc772393(v=ws.10).aspx) (AD CS) saate serdid luua kasutades teenust AD CS. Iga sert peab sisaldama privaatvõtit, mis loodi võtmevahetuse jaoks ja see peab olema eksporditav isikuandmete vahetuse (.pfx) faili.

Enda allkirjastatud serte saab kasutada ainult testimise eesmärgil. Mugavuse mõttes sisaldavad häälestusskriptid skripte, mis loovad ja ekspordivad enda allkirjastatud serte. Nagu mainitud, tohib neid serte kasutada ainult testimise eesmärgil.

| Eesmärk                                      | Selgitus | Lisanõuded |
|----------------------------------------------|-------------|-------------------------|
| SQL Serveri SSL-sert                   | Seda serti kasutatakse andmete krüptimiseks, mida edastatakse SQL Serveri eksemplari ja klientrakenduse vahelise võrgu kaudu. | <p>Serdi domeeninimi peab vastama SQL Serveri eksemplari või kuulaja täielikule domeeninimele (FQDN).</p><p>Näide. Kui SQL-i kuulaja on majutatud seadmes DAX7SQLAOSQLA, on serdi DNS-nimi DAX7SQLAOSQLA.onprem.contoso.com.</p> |
| Teenuse Service Fabric serveri sert            | Serti kasutatakse teenuse Service Fabric sõlmedevahelise sõlmelt-sõlmele suhtluse kaitsmisele kaasa aitamiseks. Samuti kasutatakse seda serti selle serveri serdina, mis esitatakse kogumiga ühenduse loonud kliendile. | <p>Serdi domeeninimi peab vastama DNS-i tsoonile, milles AOS-i ja teenust Service Fabric majutatakse.</p><p>Serdi domeeninimi võib näiteks olla \*.onprem.contoso.com or \*.contoso.com.</p><p>Metamärgi serdi kasutamisel rakendub metamärk ainult ühele tasemele. Kui tasemeid on rohkem, tuleb serdile rakendada alamdomeen ja teema alternatiivne nimi (SAN), eelmise näite korral nt \*.contoso.com.</p> |
| Teenuse Service Fabric kliendisert            | Serti kasutavad kliendid teenuse Service Fabric kogumi kuvamiseks ja haldamiseks. | |
| Šifreerimise sert                     | Serti kasutatakse tundliku teabe, nt SQL Serveri parooli ja kasutajakonto paroolide krüptimiseks. | <p>Serdi võtme kasutamine peab sisaldama andmete šifreerimist (10) ega tohi sisaldada serveri või kliendi autentimist.</p><p>Lisateavet vt jaotisest [Saladuste haldamine teenuse Service Fabric rakendustes](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-application-secret-management).</p> |
| AOS-i SSL-sert                          | <p>Serti kasutatakse selle serveri serdina, mis esitatakse kliendile AOS-i veebisaidi jaoks. Samuti kasutatakse seda Windows Communication Foundationi (WCF)/Simple Object Access Protocoli (SOAP) sertide lubamiseks.</p><p>Teenuse Service Fabric serveri serti saab siin kasutada, kui tegemist on metamärgi serdiga.</p> | <p>Serdi domeeninimi peab vastama DNS-i tsoonile, milles AOS-i ja teenust Service Fabric majutatakse.</p><p>Serdi domeeninimi võib näiteks olla \*.d365ffo.onprem.contoso.com, \*.onprem.contoso.com või \*.contoso.com.</p><p>Metamärgi serdi kasutamisel rakendub metamärk ainult ühele tasemele. Kui tasemeid on rohkem, tuleb serdile rakendada alamdomeen ja SAN, eelmise näite korral nt \*.contoso.com.</p> |
| Seansi autentimissert           | Seda serti kasutab AOS kasutaja seansiteabe turbe suurendamiseks. | Samuti on see **failiketta** sert, mida kasutatakse LCS-st tehtava juurutuse ajal. |
| Andmete krüptimise ja andmete allkirjastamise sert | AOS kasutab neid serte tundliku teabe krüptimiseks. | |
| Finantsaruandluse kliendisert       | Serti kasutatakse finantsaruandluse teenuste ja AOS-i vahelise suhtluse turbe suurendamiseks. | |
| Aruandlussert                        | Serti kasutatakse SSRS-i ja AOS-i vahelise suhtluse turbe suurendamiseks. | |
| Kohapealse kohaliku agendi sert           | <p>Serti kasutatakse kohapeal majutatava kohaliku agendi ja LCS-i vahelise suhtluse turbe suurendamiseks.</p><p>Sert võimaldab kohalikul agendil tegutseda teie Azure AD rentniku nimel ja suhelda LCS-ga, et juhtida ja hallata juurutusi.</p> | |

### <a name="plan-your-users-and-service-accounts"></a>Kasutajate ja teenusekontode plaanimine

Rakenduse Finance and Operations (kohapealne) töötamiseks peate looma mitu kasutaja- või teenusekontot. Peate looma kombinatsiooni grupi hallatavatest teenusekontodest (gMSAs), domeeni- ja SQL-i kontodest. Järgnevas tabelis on ära toodud kasutajakontod, nende eesmärk ja selles teemas kasutatavad näidisnimed.

| Kasutajakonto                                            | Tüüp           | Eesmärk | Kasutajanimi |
|---------------------------------------------------------|----------------|---------|-----------|
| Finantsaruandluse rakenduse teenusekonto         | gMSA           |         | Contoso\\svc-FRAS$ |
| Finantsaruandluse protsessi teenusekonto             | gMSA           |         | Contoso\\svc-FRPS$ |
| Finantsaruandluse ühe klõpsuga kujundaja teenusekonto | gMSA           |         | Contoso\\svc-FRCO$ |
| AOS-i teenusekonto                                     | gMSA           | See kasutaja tuleb luua tulevasteks kontrollimisteks. Tulevastes väljalasetes plaanime lubada AOS-i ja gMSA vahelise koostöö. Kui loote selle kasutaja seadistamise ajal, aitate tagada, et üleminek gMSA-le toimub sujuvalt. | Contoso\\svc-AXSF$ |
| AOS-i teenusekonto                                     | Domeenikonto | AOS kasutab seda kasutajat GA väljalaskes. | Contoso\\AXServiceUser |
| AOS SQL DB administraatorkasutaja                                   | SQL-i kasutaja       | Rakendus Finance and Operations kasutab seda kasutajat SQL\*-ga autentimiseks. Tulevastes väljalasetes asendatakse ka see kasutaja gMSA kasutajaga. | AXDBAdmin |
| Kohaliku juurutusagendi teenusekonto                  | gMSA           | Seda kontot kasutab kohalik agent juurutamise juhtimiseks erinevatel sõlmedel. | Contoso\\Svc-LocalAgent$ |

\* SQL-i kasutajanimi ja SQL-i autentimise parool on kaitstud, sest nad on krüptitud ja talletatud failikettale.

### <a name="create-dns-zones-and-add-a-records"></a>DNS-i tsoonide loomine ja A-kirjete lisamine

DNS on integreeritud AD DS-ga ja see võimaldab teil võrgus ressursse korraldada, hallata ja leida. Saate AOS-i hostinimele ja teenuse Service Fabric kogumile luua DNS-i otsingutsoonide edastamise ja A-kirjed. Selles näidisseadistuses on DNS-tsooni nimi d365ffo.onprem.contoso.com ja A-kirjed/hostinimed on järgmised:

- **ax**.d365ffo.onprem.contoso.com AOS-i seadmete jaoks;
- **sf**.d365ffo.onprem.contoso.com teenuse Service Fabric kogumi jaoks.

#### <a name="add-a-dns-zone"></a>DNS-tsooni lisamine

DNS-tsooni lisamiseks kasutage järgmist protseduuri.

1. Logige domeenikontrolleri arvutisse sisse, klõpsake nuppu **Alusta** ja käivitage DNS-i haldur tippides **dnsmgmt.msc**.
2. Paremklõpsake domeenikontrolleri nime ja klõpsake seejärel valikuid **Uus tsoon** \> **Järgmine**.
3. Tehke valik **Primaartsoon**.
4. Jätke märkeruut **Salvesta tsoon Active Directorys (saadaval ainult juhul, kui DNS-server on kirjutatav domeenikontroller)** märgituks ja klõpsake seejärel nuppu **Järgmine**.
5. Tehke valik **Kõigile DNS-serveritele, mis töötavad domeenikontrolleritel selles domeenis: Contoso.com** ja seejärel klõpsake nuppu **Järgmine**.
6. Tehke valik **Edasta otsingutsoon** ja klõpsake seejärel nuppu **Järgmine**.
7. Sisestage oma seadistuse tsooninimi ja seejärel klõpsake nuppu **Järgmine**. Sisestage näiteks **d365ffo.onprem.contoso.com**.
8. Tehke valik **Ära luba dünaamilisi värskendusi** ja klõpsake seejärel nuppu **Järgmine**.

#### <a name="set-up-an-a-record-for-aos"></a>AOS-ile A-kirje seadistamine

Looge uues DNS-tsoonis üks A-kirje nimega **ax.d365ffo.onprem.contoso.com** **iga** teenuse Service Fabric kogumi sõlme kohta, mille tüübiks on **AOSNodeType**. Ärge looge A-kirjeid teiste sõlmetüüpide jaoks.

1. Paremklõpsake uut tsooni ja klõpsake siis valikut **Uus host**.
2. Sisestage teenuse Service Fabric sõlme nimi ja IP-aadress (nt 10.179.108.12) ja klõpsake seejärel valikut **Lisa host**.

#### <a name="set-up-an-a-record-for-the-orchestrator"></a>A-kirje seadistamine korraldajale

Looge uues DNS-tsoonis üks A-kirje nimega **sf.d365ffo.onprem.contoso.com** **iga** teenuse Service Fabric kogumi sõlme kohta, mille tüübiks on **OrchestratorType**. Ärge looge A-kirjeid teiste sõlmetüüpide jaoks.

1. Paremklõpsake uut tsooni ja klõpsake siis valikut **Uus host**.
2. Sisestage teenuse Service Fabric sõlme nimi ja IP-aadress (nt 10.179.108.15) ja klõpsake seejärel valikut **Lisa host**.

#### <a name="join-vms-to-the-domain"></a>VM-de ühendamine domeeniga

Saate ühendada iga VM domeeniga, kui viite lõpule jaotises [Kuidas ühendada Windows Server 2016 Active Directory domeeniga](http://www.tomsitpro.com/articles/join-windows-server-2016-to-ad-domain,2-1063.html) toodud etapid. Teise võimalusena võite kasutada Windows PowerShelli skripti.

```
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
Restart-Computer
```
Kui VM-d on domeeniga ühendatud, lisage AOS-i teenusekontod (Contoso\svc-AXSF$ , Contoso\svc-AXSF$ ) kohalikku administraatorite gruppi. Lisateabe saamiseks vt artiklit [Liikme lisamine kohalikku gruppi](https://technet.microsoft.com/en-us/library/cc772524(v=ws.11).aspx).

#### <a name="disable-user-access-control"></a>Kasutaja juurdepääsu juhtelemendi keelamine 

Selleks, et keelata kasutaja juurdepääsu juhtelement **iga** teenuse Service Fabric sõlme jaoks, käivitage järgmine skript.
```
$RegPath = "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System"
New-ItemProperty -Path $RegPath -Name "EnableLUA" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "ConsentPromptBehaviorAdmin" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "EnableUIADesktopToggle" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "LocalAccountTokenFilterPolicy" -Value 1 -PropertyType "DWORD" -Force
```
> [!IMPORTANT]
> Pärast skripti edukat lõpule viimist peate sõlme taaskäivitama.

#### <a name="add-prerequisite-software-to-vms"></a>VM-dele eeltingimuseks oleva tarkvara lisamine

Järgmine tabel loetleb eeltingimuseks oleva tarkvara, mis tuleb iga sõlmetüübi seadmetele rakendada.

> [!NOTE]
> Pärast komponentide installimist peate oma arvuti taaskäivitama.

| Sõlme tüüp | Komponent | Käsk |
|-----------|-----------|---------|
| AOS       | SNAC – ODBC-draiver | Vt jaotist [Microsoft ODBC-draiver 13.1 SQL Serveri jaoks – Windows + Linux](https://www.microsoft.com/en-us/download/details.aspx?id=53339). |
| AOS       | Microsoft .NET Frameworki versioon 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| AOS       | Microsoft .NET Frameworki versioon 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| AOS       | Interneti teabeteenuste haldamine (IIS) | `Add-WindowsFeature WAS, WAS-Process-Model, WAS-NET-Environment, WAS-Config-APIs`<br>`# Windows Process Activation Service`<br>`Add-WindowsFeature Web-Server, Web-WebServer, Web-Security, Web-Filtering, Web-App-Dev, Web-Net-Ext, Web-Mgmt-Tools, Web-Mgmt-Console` |
| AOS       | Microsoft SQL Server Management Studio 2016 | |
| AOS       | Microsoft Visual C++ edasilevitatavad paketid Microsoft Visual Studio 2013 jaoks | Vt jaotist [Microsoft Visual C++ edasilevitatavad paketid Visual Studio 2013 jaoks](https://support.microsoft.com/en-us/help/3179560). |
| AOS       | Microsoft Accessi andmebaasimootor 2010, edasilevitatav | Vt jaotist [Microsoft Accessi andmebaasimootor 2010, edasilevitatav](https://www.microsoft.com/en-us/download/details.aspx?id=13255) |
| BI        | .NET Frameworki versioon 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| BI        | .NET Frameworki versioon 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| BI        | Microsoft SQL Server 2016 SP1 | |
| BI        | Management Studio 2016 | |
| BI        | SQL Serveri aruandlusteenused 2016 režiimis **Omarežiim** | |
| MR        | .NET Frameworki versioon 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| MR        | .NET Frameworki versioon 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| MR        | Visual C++ edasilevitatavad paketid Visual Studio 2013 jaoks | Vt jaotist [Microsoft Visual C++ edasilevitatavad paketid Visual Studio 2013 jaoks](https://support.microsoft.com/en-us/help/3179560). |

#### <a name="download-setup-scripts-from-lcs"></a>Häälestusskriptide LCS-st allalaadimine

Oleme seadistuse täiustamiseks esitanud mitu skripti. Häälestusskriptide LCS-ist allalaadimiseks järgige neid etappe.

1. Logige LCS-i sisse (<https://lcs.dynamics.com/v2>).
2. Klõpsake armatuurlaual paani **Ühiste vahendite teek**.
3. Klõpsake vahekaarti **Mudel**.
4. Valige ruudustikus rida **Dynamics 365 for Operations – kohapealse juurutamise skriptid**.
5. Klõpsake valikut **Versioonid** ja laadige alla skriptide uusim versioon.

### <a name="describe-your-configuration"></a>Kirjeldage oma konfiguratsiooni

See jaotis annab teavet skriptide kohta, mis tuleb käivitada. Skripte tutvustatakse käivitamise järjekorras. Skriptide käivitamiseks täitke mallifail asukohas $(downloadPath)\\ConfigTemplate.xml. Fail ConfigTemplate.xml kirjeldab teenuse Service Fabric kogumeid, serte, mida nende konfigureerimiseks kasutatakse ja kontosid, millele peab olema antud asjakohaste sertide juurdepääs. Esitatud näites on täidetud selles teemas kirjeldatud näidistaristu väärtused. Mallifaili kasutatakse järgmises osas.

#### <a name="create-the-domain-account-for-a-service-user"></a>Domeenikonto loomine teenuse kasutajale

Domeeni kasutajakonto loomiseks käivitage järgmine käsk: contoso\\AXServiceUser.

```
New-ADUser -Name 'AXServiceUser' `
    -AccountPassword (Read-Host -Prompt 'Specify User Password' -AsSecureString) `
    -PasswordNeverExpires $true -ChangePasswordAtLogon $false `
    -Enabled $true -UserPrincipalName 'AXServiceUser@contoso.com'
```

#### <a name="create-gmsas"></a>gMSA-de loomine

1. Määrake kausta teeks **$(DownloadPath)** ja käivitage järgmine Windows PowerShelli käsk.

    > [!NOTE]
    > See skript ei loo kasutajaid. Skript prindib käsud, mis tuleb domeenikontrolleri arvutis käsitsi käivitada.

    ```
    # Generate gMSA account creation script (shows in console):
    .\Get-NewGMSAInDomainScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

2. Kopeerige käsu väljund Windows PowerShelli aknasse. Veenduge, et reapiirid oleks eemaldatud ja käivitage read Active Directory domeenikontrolleri arvutis, kasutades selleks suuremaid õigusi (tehke paremklõps ja klõpsake käsku **Käivita administraatorina**).
3. Kinnitamaks, et kontode loomine õnnestus, käivitage Active Directory domeenikontrolleri arvutis järgmine skript. Käivitage skript kindlasti pärast seda, kui olete asendanud mustri, mis vastab teenusekontode nimetamisreeglile.

    ```
    #Use this command to validate the gMSA accounts are added to AD.
    #Ensure to replace the Filter parameter with the pattern used to create your accounts.
    Get-ADServiceAccount -Filter { samAccountName -like "svc-*" }
    ```

4. Käivitage klientarvutis skript Export-AddGMSAsONVMScript.ps1. See skript loob skripte, mida käitatakse igas teenuse Service Fabric VM-is ja lisab need kausta, mis vastab igale VM-i nimele.

    ```
    # Exports a script for installing gMSA on VM nodes into a directory VMs\<VMName>, again feed from XML
    .\Export-AddGMSAsOnVMScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

#### <a name="stop-iis"></a>IIS-i peatamine

Teenuse Service Fabric iga VM-ga ühenduse loomiseks kasutage Remote Desktop Protocoli (RDP) ja viige lõpuni jaotises [Veebiserveri (IIS 7) käivitamine või peatamine](https://technet.microsoft.com/en-us/library/cc732317(v=ws.10).aspx) toodud käsitsi tehtavad etapid. Teise võimalusena kasutage järgmist Windows PowerShelli skripti, et teenuse Service Fabric iga VM-iga ühendust luua (kasutades selleks RDP-d).

```
$ServiceName = "WAS"
$wasService = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($wasService)
{
    $wasService.DependentServices | Stop-Service -Force -ErrorAction Continue
    $wasService | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}

$ServiceName = 'W3SVC'
$w3svc = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($w3svc)
{
    $w3svc.DependentServices | Stop-Service -Force -ErrorAction Continue
    $w3svc | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}
```
_IIS-i funktsioon peab olema installitud, kuid keelatud, kuna tootes on IIS dll-idega mõned sõltuvused._

### <a name="install-certificates"></a>Sertide installimine

1. Kui hankisite selles teemas eespool loetletud serdid kehtivalt CA-lt, sisestage failis ConfigTemplate.xml olevate sertide .pfx failinimi ja sõrmejälg. Määrake atribuut **generateSelfSignedCert** väärtusele **Väär** ja atribuut **eksporditav** väärtusele **Väär**. Kopeerige .pfx-failid kausta $(DownloadPath)\\InfrastructureScripts\\Certs.
2. Kui kasutate enda allkirjastatud serte (ainult testimise eesmärgil), käivitage järgmine skript. Enda allkirjastatud sertide loomiseks peab failis ConfigTemplate.xml atribuut **generateSelfSignedCert** olema määratud väärtusele **Tõene** ja atribuut **eksporditav** väärtusele **Tõene**. Skript värskendab XML-i sertide sõrmejäljega.

    ```
    # Create self-signed certs (optionally, use -Display if you only want to see commands):
    # Note: this script is completely driven off ConfigTemplate.xml
    .\New-SelfSignedCertificates.ps1 -InputXml .\ConfigTemplate.xml
    ```

3. Eksportige uued serdid privaatvõtmega (.pfx-fail). Ekspordikäskude loomiseks ja käitamiseks Windows PowerShellis kasutage järgmist skripti. .pfx-failid asetatakse kausta Serdid.

    ```
    # Exports Pfx files into a directory VMs\<VMName>, all the certs will reside in a folder named Certs\
    # Feeds from XML, if certs don't have passwords then you are prompted to enter one
    .\Export-PfxFiles.ps1 -InputXml .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Serdid peavad olema installitud ja peavad olema serdis:\\CurrentUser\\My. Samuti peavad serdid olema eksporditavad.

    Kui kasutate enda allkirjastatud serte, jätkake järgmise osaga. Te ei pea seda protseduuri lõpule viima.

4. Pärast seda, kui olete .pfx-failid eksportinud või kopeerinud kausta $(DownloadPath)\\InfrastructureScripts\\Certs, käivitage järgmised käsud, et luua skriptid, mis asetatakse VM-dele vastavatesse kaustadesse.

    ```
    # Exports script for adding ACLs to certs into a directory VMs\<VMName>
    .\Export-CertificateAclsForVMs.ps1 -InputXml .\ConfigTemplate.xml
    
    # Exports Import-PfxFiles.ps1 script for importing PFXs on VM nodes into a directory VMS\<VMname>:
    .\Export-ImportPfxFilesScript.ps1 -InputXml .\ConfigTemplate.xml
    
    .\Export-UnblockStrongNameScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

5. Kopeerige igas kaustas olevad skriptid kausta nimele vastavatesse VM-desse.
6. Käitage igal VM-l järgmised skriptid kuvamise järjekorras.

    ```
    #Run this script only if it exists
    .\Add-GMSAOnVM.ps1
    
    .\Import-PfxFiles.ps1
    
    .\Set-CertificateAcls.ps1
    
    #Run this script only if it exists
    .\Unblock-StrongName.ps1
    ```

### <a name="set-up-a-standalone-service-fabric-cluster"></a>Teenuse Service Fabric eraldiseisva kogumi seadistamine

1. Käivitage faili ClusterConfig.json loomiseks järgmine käsk.

    ```
    .\New-SFClusterConfig.ps1 -InputXml .\ConfigTemplate.xml
    ```

    Lisateavet vt jaotistest [Etapp 1B: mitme arvuti ülese kogumi loomine](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster), [Eraldiseisva kogumi kaitsmine Windowsis X.509-sertide abil](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-windows-cluster-x509-security) ja [Windows Serveris töötava eraldiseisva kogumi loomine](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster).

2. Laadige [teenuse Service Fabric eraldiseisev installipakett](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#download-the-service-fabric-standalone-package) alla ühte oma teenuse Service Fabric sõlmedest. Pärast ZIP-faili allalaadimist tühistage selle blokeering, tehes ZIP-failil paremklõpsu ja klõpsates seejärel valikut **Atribuudid**. Valige dialoogiboksis alt paremalt märkeruut **Tühista blokeerimine**.
3. Kopeerige ZIP-fail ühte teenuse Service Fabric kogumi sõlmedest ja pakkige see lahti.
4. Kõigis sõlmedes sissetuleva tulemüüri reegli loomiseks portidel 443 ja 445 käivitage järgmised käsud.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "SFInbound443445" -LocalPort 135, 137, 138, 139, 445, 443 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "SFInbound443445"
    ```

5. Ainult SSRS-i sõlmes sissetuleva tulemüüri reegli loomiseks pordil 80 käivitage järgmised käsud.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "Reporting80" -LocalPort 80 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "Reporting80"
    ```

6. Kopeerige oma fail ClusterConfig.json oma eraldiseisva teenuse Service Fabric lahtipakitud installimiskohta.
7. Navigeerige suuremate õiguste abil Windows PowerShellis lahtipakitud installimiskohta ja käivitage atribuudi ClusterConfig testimiseks järgmine käsk.

    ```
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

8. Kui testimine õnnestub, kasutage kogumi juurutamiseks järgmist käsku.

    ```
    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

9. Pärast kogumi loomist avage installimise kinnitamiseks teenuse Service Fabric vaatur mis tahes klientarvutis:

    1. Installige teenuse Service Fabric kliendisert asukohta CurrentUser\\My, kui see ei ole veel installitud.
    2. Avage **IE sätted** \> **Ühilduvusrežiim** ja tühjendage märkeruut **Kuva sisevõrgu saidid ühilduvusrežiimis**.
    3. Minge saidile `https://sf.d365ffo.onprem.contoso.com:19080`, kus sf.d365ffo.onprem.contoso.com on tsoonis määratud teenuse Service Fabric kogumi hostinimi. Kui DNS-i nimelahendus ei ole konfigureeritud, kasutage arvuti IP-aadressi.
    4. Valige kliendisert. Kuvatakse leht **teenuse Service Fabric vaatur**.

### <a name="configure-lcs-connectivity-for-the-tenant"></a>Rentniku jaoks LCS-i ühenduvuse konfigureerimine

Rakenduse Finance and Operations juurutamist ja hooldust juhitakse LCS-i kaudu, kohapealse kohaliku agendi abil. Ühenduvuse loomiseks LCS-st rakenduse Finance and Operations rentnikusse peate konfigureerima serdi, mis lubab kohalikul agendil tegutseda teie Azure AD rentniku nimel (nt Contoso.Onmicrosoft.com).

Kasutage CA-st hangitud kohapealse agendi serti või skriptide abil loodud enda allkirjastatud serti.

LCS-i autoriseerimiseks saavad serte lisada ainult kasutajakontod, millel on üldadministraatori kausta roll. Vaikimisi saab kausta üldadministraatoriks isik, kes teenuse Microsoft Office 365 teie organisatsiooni jaoks registreerib.

> [!NOTE]
> Serdi peate rentniku kohta konfigureerima täpselt ühe korra. Kõik kohapealsed keskkonnad tohivad LCS-iga ühenduse loomiseks kasutada sama serti.

1. Laadige alla ja installige klientarvutisse Azure PowerShelli uusim versioon. Lisateabe saamiseks vt jaotist [Azure PowerShelli installimine ja konfigureerimine](https://docs.microsoft.com/en-us/powershell/azure/install-azurerm-ps?view=azurermps-4.1.0&viewFallbackFrom=azurermps-4.0.0).
2. Kinnitamaks, et teil on üldadministraatori kausta roll, logige sisse [kliendi Azure’i portaali](https://portal.azure.com).
3. Käitage järgmine skript asukohast $(DownloadPath)\\InfrastructureScripts.

   ```
   .\AddCertToServicePrincipal.ps1 -CertificateThumbprint <OnPremLocalAgent Certificate Thumbprint>
   ```

### <a name="set-up-file-storage"></a>Failisalvestusruumi seadistamine

Peate seadistama kaks väga hästi kättesaadavat SMB 3.0 failiketast. Lisateavet SMB 3.0 lubamise kohta vt jaotisest[SMB turbetäiustused](https://technet.microsoft.com/en-us/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1).
Turvaline dialekti läbirääkimine ei saa tuvastada ega takistada versiooni taandamist versioonidelt SMB 2.0 või 3.0 versioonile SMB 1.0. Seetõttu ja ka SMB-krüptimise täielike võimaluste parimaks ärakasutamiseks soovitame tungivalt SMB 1.0 server keelata

> [!NOTE]
> Teie keskkonnas olevate passiivsete andmete turvalisuse tagamiseks peab igas arvutis olema lubatud BitLockeri draivikrüptimine. Lisateavet BitLockeri lubamise kohta leiate jaotisest [BitLocker: kuidas juurutada versioonis Windows Server 2012 ja uuemas](https://docs.microsoft.com/en-us/windows/device-security/bitlocker/bitlocker-how-to-deploy-on-windows-server).

- Failiketas, mis talletab AOS-i üleslaaditud kasutajadokumente (nt \\\\DAX7SQLAOFILE1\\aos-storage).
- Failiketas, mis talletab juurutuse juhtimiseks uusimaid järgu- ja konfiguratsioonifaile (nt \\\\DAX7SQLAOFILE1\\agent))

    > [!NOTE]
    > Hoidke failiketta tee võimalikult lühikesena, et vältida tee maksimaalse pikkuse ületamist failide puhul, mis kettale asetatakse.

1. Käivitage failiketta arvutis järgmine käsk.

    ```
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```
#### <a name="set-up-the-dax7sqlaofile1aos-storage-file-share"></a>Seadistage failiketas \\\\DAX7SQLAOFILE1\\aos-storage

2. Tehke serverihalduris valikud **Faili- ja salvestusruumiteenused** \> **Kettad**.
3. Uue ketta loomiseks nimega **aos-storage** klõpsake valikuid **Ülesanded** \> **Uus ketas** .
4. Andke igale teenuse Service Fabric kogumi arvutile atribuudi **Muuda** õigused, välja arvatud arvutile **OrchestratorNodeType**.
5. Andke õigused **Muuda** kasutaja AOS-i domeenikasutajale (contoso\\AXServiceUser) ja gMSA kasutajale (contoso\\svc-AXSF).

#### <a name="set-up-the-dax7sqlaofile1agent-file-share"></a>Seadistage failiketas \\\\DAX7SQLAOFILE1\\agent

6. Minge uuesti serverihaldurisse, tehke valikud **Faili- ja salvestusruumiteenused** \> **Kettad**.
7. Uue ketta loomiseks nimega **agent** klõpsake valikuid **Ülesanded** \> **Uus ketas** .
8. Andke gMSA kasutajale kohaliku juurutusagendi (contoso\\svc-LocalAgent$) jaoks õigused **Täielikud õigused**.

### <a name="set-up-sql-server"></a>SQL Serveri seadistamine

1. Installige suure kättesaadavusega SQL Server 2016 SP1, kas SQL-i kogumitena, mis hõlmavad talletusala võrku (SAN) või Always-On konfiguratsioonina.  Veenduge, et **andmebaasimootor, aruandlusteenused, täistekstiotsing** ja **haldustööriistad** on juba installitud.
> [!NOTE]
> Veenduge, et SQL Always On on seadistatud vastavalt jaotisele [Algandmete sünkroonimislehe valimine (Always On saadavusrühma viisardid)](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards) ja järgige jaotist [Teiseste andmebaaside käsitsi ettevalmistamine](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs)
2. Käivitage SQL-i teenus domeenikasutajana.
3. Rakenduse Finance and Operations konfigureerimiseks hankige CA-st SSL-sert. Testimise eesmärkidel võite luua ja kasutada enda allkirjastatud serte.

**Enda allkirjastatud sert klasterdatud SQL-i eksemplari jaoks**
   ```
   New-SelfSignedCertificate -CertStoreLocation "cert:\CurrentUser\My" -DnsName "DAX7SQLAOSQLA.contososqlao.com" -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider" -Subject "DAX7SQLAOSQLA.contososqlao.com"
   ```
**Enda allkirjastatud sert Always-On SQL-i eksemplari jaoks**
```
#https://www.derekseaman.com/2014/11/sql-2014-alwayson-ag-pt-13-ssl.html

# Create certificate for each SQL Node (i.e. 2 nodes = 2 certificates)
# Run script on each node
$computerName = $env:COMPUTERNAME.ToLower() 
$domain = $env:USERDNSDOMAIN.ToLower()
$listenerName = 'dax7sqlaosqla' 
$cert = New-SelfSignedCertificate -Subject "$computerName.$domain" -DnsName "$listenerName.$domain", $listenerName, $computerName -Provider 'Microsoft Enhanced RSA and AES Cryptographic Provider'

```
4. SSL-i konfigureerimiseks SQL Serveris viige serdi abil lõpule jaotises [Kuidas lubada SSL-i krüptimine SQL Serveri eksemplari jaoks Microsofti halduskonsooli abil](https://support.microsoft.com/en-us/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console) toodud etapid.
5. Järgige neid etappe iga kogumi sõlme puhul. Veenduge, et teeksite muudatused mitteaktiivses sõlmes ja lülitaksite sellele pärast muudatuste tegemist ümber.

    1. Importige sert asukohta LocalMachine\\My.
    2. Andke serdi õigused teenusekontole, mida kasutatakse SQL-i teenuse käitamiseks. Paremklõpsake Microsofti halduskonsoolis (MMC) serti (certlm.msc) ja klõpsake seejärel valikuid **Ülesanded** \> **Halda privaatvõtmeid**.
    3. Lisage serdi sõrmejälg asukohta HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib\\Certificate.
    4. Määrake Microsoft SQL Serveri konfiguratsioonihalduris atribuut **ForceEncryption** väärtusele **Jah**.

6. Eksportige serdi avalik võti (fail .cer) ja installige see iga teenuse Service Fabric sõlme usaldusväärsesse juurde.

### <a name="configure-the-orchestratordata-database"></a>Andmebaasi OrchestratorData konfigureerimine

1.  Looge tühi andmebaas nimega **OrchestratorData**. Seda andmebaasi kasutab kohapealne kohalik agent juurutuste juhtimiseks.
2.  Andke andmebaasis kohalikule agendile gMSA (svc-LocalAgent$) **db\_owner** õigused:

    1. Laiendage puus serveri nime, laiendage valikuid **Turve** \> **Sisselogimised**, seejärel paremklõpsake ja klõpsake valikut **Uus sisselogimine**.

        ![Uus sisselogimiskäsk](./media/OPSetup_01_NewLogin.png)


    2. Otsige üles teenusekonto **svc-LocalAgent$**. Klõpsake valikut **Asukohad** ja valige **Terve kataloog**, seejärel klõpsake valikut **Objekti tüübid** ja tehke valik **Teenusekonto**.

        ![Valige kasutaja, teenusekonto või grupi dialoogiboks](./media/OPSetup_02_SelectUserServiceAccountOrGroupDialogBox.png)

    3. Määrake atribuut **Assign ServerRole** väärtusele **Avalik**.
    4. Määrake andmebaasile OrchestratorData andmebaasi rolliõigus **db\_owner**.

### <a name="configure-the-finance-and-operations-database"></a>Rakenduse Finance and Operations andmebaasi konfigureerimine

1. Logige LCS-i sisse (<https://lcs.dynamics.com/v2>).
2. Klõpsake armatuurlaual paani **Ühiste vahendite teek**.
3. Klõpsake vahekaarti **Mudel** 
4. Klõpsake ZIP-faili allalaadimiseks ruudustikus rida **kohapealne Dynamics 365 for Operations, Enterprise edition – demoandmed**.
5. ZIP-fail sisaldab tühje ja demoandmete .bak faile. Valige oma vajadustele vastav .bak fail. Näiteks kui vajate demoandmeid, taastage fail AxBootstrapDB_Demodata.bak. 
6. Taastage andmebaas AxBootstrapDB_DemoData.bak.
7. Nimetage ümber andmebaas **AXDBRAIN**.
8. Käivitage taastatud andmebaasis järgmised päringud.

    ```
    ALTER DATABASE AXDBRAIN
    SET READ_COMMITTED_SNAPSHOT ON
    GO
    
    ALTER DATABASE AXDBRAIN
    SET ALLOW_SNAPSHOT_ISOLATION ON
    GO
    ```

4. Värskendage andmebaasi faile:

    1. Tehke andmebaasil paremklõps ja klõpsake siis valikut **Atribuudid**.
    2. Andmebaasi failiatribuutide muutmiseks klõpsake valikut **Failid**.
    3. Sisestage väljal **Algne maht (MB)** väärtus, mis on suurem kui 5120.

        ![Andmebaasi atribuutide dialoogiboks](./media/OPSetup_03_DatabasePropertiesDialogBox.png)

    4. Määrake atribuudi **AXDBBuild\_Data** puhul väli **Autogrowth/Maximize** väärtusele **200** megabaiti (MB).
    5. Määrake atribuudi **AXDBBuild\_Log** puhul väli **Autogrowth/Maximize** väärtusele **500** MB.

        ![Dialoogiboksi Autogrowth muutmine](./media/OPSetup_04_ChangeAutogrowthDialogBox.png)

5. Looge uus kasutaja, kellel on SQL-i autentimine lubatud (axdbadmin).
6. Kasutage kasutajate ja andmebaasirollide vastendamiseks järgmises tabelis olevat teavet.

    | Kasutaja             | Tüüp    | Andmebaasi roll |
    |------------------|---------|---------------|
    | svc-AXSF$        | gMSA    | db\_owner     |
    | svc-LocalAgent$  | gMSA    | db\_owner     |
    | svc-FRPS$        | gMSA    | db\_owner     |
    | svc-FRAS$        | gMSA    | db\_owner     |
    | axdbadmin        | SqlUser | db\_owner     |

7. Andke üksuse svc-AXSF$ kasutajale ja üksuse axdbadmin SQL-i kasutajale andmebaasis tempdb järgmiste rollide juurdepääs:

    - db\_datareader
    - db\_datawriter
    - db\_ddladmin

8. Käivitage haldusstuudios järgmised Transact SQL (T-SQL) käsud:

    ```
    GRANT VIEW SERVER STATE TO axdbadmin
    GRANT VIEW SERVER STATE TO [contososqlao\svc-AXSF$]
    ```
9. Käivitage järgmine käsk:
```
.\Reset-DatabaseUsers.ps1 -DatabaseServer ‘<FQDN of the SQL server>’ -DatabaseName '<AX database name>'
```

### <a name="configure-the-financial-reporting-database"></a>Finantsaruandluse andmebaasi konfigureerimine

1.  Looge tühi andmebaas nimega **FinancialReporting**.
2.  Kasutage kasutajate ja andmebaasirollide vastendamiseks järgmises tabelis olevat teavet.

    | Kasutaja             | Tüüp | Andmebaasi roll |
    |------------------|------|---------------|
    | svc-LocalAgent$  | gMSA | db\_owner     |
    | svc-FRPS$        | gMSA | db\_owner     |
    | svc-FRAS$        | gMSA | db\_owner     |

### <a name="encrypt-credentials"></a>Identimisteabe krüptimine

1. Installige mis tahes klientarvutis šifreerimise sert serdi talletuskohta LocalMachine\\My.
2. Andke praegusele kasutajale serdi privaatvõtme lugemisõigus.
3. Looge siin näidatud viisil fail Credentials.json.

    ```
    {
        "AosPrincipal": {
            "AccountPassword": "<encryptedDomainUserPassword>"
        },
        "AosSqlAuth": {
            "SqlUser": "<encryptedSqlUser>",
            "SqlPwd": "<encryptedSqlPassword>"
        }
    }
    ```

    - **AccountPassword** on AOS-i domeenikasutaja krüptitud domeenikasutaja parool (contoso\\axserviceuser).
    - **SqlUser** on krüptitud SQL-i kasutaja (axdbadmin), kellel on juurdepääs rakenduse Finance and Operations andmebaasile (AXDBRAIN) ja **SqlPassword** on krüptitud SQL-i parool.

4. Kopeerige .json fail SMB failikettale, \\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json.
5. Värskendage faili Credentials.json krüptitud väärtustega.

    ```
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | clip
    ```

    1. Asendage failis Credentials.json üksus **\<encryptedDomainUserPassword\>** krüptitud domeeniparooliga.
    2. Asendage üksus **\<encryptedSqlUser\>** krüptitud rakenduse Finance and Operations SQL-i kasutajaga.
    3. Asendage üksus **\<encryptedSqlPassword\>** rakenduse Finance and Operations SQL-i parooliga.
    
### <a name="set-up-ssrs"></a>Seadista SSRS

1.  Enne alustamist veenduge, et teema alguses loetletud eeltingimused oleks installitud.
2.  Järgige jaotises [SQL Serveri aruandlusteenuste konfigureerimine kohapealseks juurutamiseks](../analytics/configure-ssrs-on-premises.md) toodud etappe.

### <a name="configure-ad-fs"></a>AD FS konfigureerimine

Enne, kui saate selle protseduuri lõpule viia, peab AD FS olema juurutatud Windows Server 2016-sse. Lisateavet AD FS juurutamise kohta leiate jaotisest [Windows Server 2016 juurutusjuhend ja 2012 R2 AD FS juurutusjuhend](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide).

Rakenduse Finance and Operations puhul on lisaks kasutusvalmis AD FS-i vaikekonfiguratsioonile vajalik ka täiendav konfiguratsioon. Järgmiste etappide puhul tuleb Windows PowerShelli käitada arvutis, kuhu on installitud AD FS-i rolliteenus. Kasutajakontol peab AD FS-i haldamiseks olema piisavalt õigusi. Näiteks peab kasutajal olema domeeniadministraatori konto.

1. Konfigureerige AD FS-i identifikaator nii, et see vastaks AD FS-i loa väljaandjale.

    ```
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. Peate Windowsi integreeritud autentimise (WIA) sisevõrgu autentimisühenduste jaoks keelama, v.a juhul, kui olete konfigureerinud AD FS-i segakeskkondade jaoks. Lisateavet selle kohta, kuidas konfigureerida WIA-t nii, et seda saab kasutada AD FS-iga, leiate jaotisest [Brauserite konfigureerimine Windowsi integreeritud autentimise (WIA) kasutamiseks koos AD FS-ga](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia).

   ```
   Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
   ```

3. Sisselogimiseks peab kasutaja meiliaadress olema aktsepteeritav autentimissisend.

   ```
   Add-Type -AssemblyName System.Net
   $fdqn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
   $domainName = $fdqn.Substring($fdqn.IndexOf('.')+1)
   Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
   ```

Selleks, et AD FS usaldaks rakendust Finance and Operations autentimise vahetuse jaoks, tuleb AD FS-is AD FS-i rakendusegrupi all registreerida mitmed rakendusekirjed. Seadistusprotsessi kiirendamiseks ja tõrgete vähendamiseks võite registreerumisel kasutada järgmist skripti. Kopeerige skript Publish-ADFSApplicationGroup.ps1 ja kaust D365FO-OP arvutisse, millesse on installitud AD FS-i rolliteenus. Seejärel käivitage skript kasutajakontoga, nt administraatori kontoga, millel on AD FS-i haldamiseks piisavalt õigusi. Skripti kasutamise kohta lisateabe saamiseks vaadake skriptis loetletud dokumentatsiooni. Märkige üles väljundis määratud kliendi ID-d, kuna seda teavet küsitakse LCS-i hilisemas etapis.

```
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'ax.d365ffo.onprem.contoso.com'
```

AD FS-i halduskonsool peab sarnanema järgmisele illustratsioonile. Serverihalduri avamiseks klõpsake valikuid **Tööriistad** \> **AD FS-i haldus** ja seejärel klõpsake puuvaate vasakus alaosas valikut **Rakendusgrupid**. Üksikasjade vaatamiseks topeltklõpsake rakendusgruppi.

![Rakendusgrupi atribuudid](./media/OPSetup_05_ApplicatioGroupProperties.png)

Lõpetuseks tehke õigsuse kontrollimine, veendudes, et pääsete teenuse Service Fabric sõlme tüübis **AOSNodeType** juurde AD FS-i OpenID konfiguratsiooni URL-ile, avades selleks veebibrauseris saidi `https://<adfs-dns-name>/adfs/.well-known/openid-configuration`. Kui saate teate, et sait pole turvaline, pole te oma AD FS-i SSL-i serti usaldusväärsete juursertimiskeskuste salve lisanud. Seda etappi on kirjeldatud AD FS-i juurutusjuhendis. Kui URL-ile juurdepääsemine õnnestub, tagastatakse JavaScripti objektiesituse (JSON) fail, mis sisaldab teie AD FS-i konfiguratsiooni ja näete, et teie AD FS-i URL on usaldusväärne.

Sellega on taristu seadistamine lõpule viidud. Järgmised lõigud kirjeldavad, kuidas navigeerida [LCS-i](https://lcs.dynamics.com), et seadistada konnektor ja juurutada rakenduse Dynamics 365 for Finance and Operations keskkond.

## <a name="configure-connector-and-install-on-premises-local-agent"></a>Konnektori konfigureerimine ja kohapealse kohaliku agendi installimine

1. Logige [LCS-i](https://lcs.dynamics.com/) sisse ja avage kohapealne juurutusprojekt.
2. Klõpsake hamburgeri menüüs valikut **Projekti sätted**.

    ![Projekti sätete käsk](./media/OPSetup_06_ProjectSettings.png)

3. Klõpsake valikut **Kohapealsed konnektorid**.
4. Klõpsake uue konnektori loomiseks nuppu **Lisa**.
5. Laadige vahekaardil **Hosti taristu häälestamine** alla agendi installer.

    ![Laadige vahekaardil Hosti taristu häälestamine alla agendi installeri nupp](./media/OPSetup_07_DownloadAgentInstaller.png)

6. Kontrollige, et ZIP-fail on blokeerimata. Paremklõpsake faili, klõpsake valikut **Atribuudid** ja valige seejärel **Tühista blokeerimine**.
7. Pakkige agendi installer lahti ühes teenuse Service fabric sõlmedest, mille tüübiks on **OrchestratorType**.
8. Sisestage vahekaardil **Agendi konfigureerimine** konfiguratsioonisätted.
9. Salvestage konfiguratsioon ja klõpsake seejärel konfiguratsioonifaili localagent-config.json allalaadimiseks valikut **Konfiguratsioonide allalaadimine**.

    ![Konfiguratsioonide allalaadimisnupp vahekaardil Agendi konfigureerimine](./media/OPSetup_08_DownloadConfigurations.png)

10. Kopeerige fail localagent-config.json arvutisse, kus asub agendi installeri pakett.
11. Käivitage käsuviibaaknas järgmine käsk, navigeerides selleks kausta, mis sisaldab agendi installerit.

    ```
    LocalAgentCLI.exe Install <path to config.json>
    ```

    > [!NOTE]
    > Kasutajal, kes käsu käivitab, peavad andmebaasis OrchestratorData olema õigused **db\_owner**.
    
12. Kui kohalik agent on edukalt installitud, navigeerige tagasi oma LCS-i kohapealse konnektori juurde.
13. Klõpsake vahekaardil **Seadistuse kinnitamine** nuppu **Sõnumiagent**. See testib kohaliku agendi ja LCS-i ühenduvust. Ühenduse edukal loomisel näeb leht välja samasugune nagu alltoodud graafik.

     ![Agendi kinnitamine](./media/ValidateAgent.PNG)

## <a name="deploy-your-dynamics-365-for-finance-and-operations-on-premises-environment"></a>Teie rakenduse Dynamics 365 for Finance and Operations (kohapealne) keskkonna juurutamine

1. Navigeerige LCS-is oma kohapealse projekti juurde, tehke valikud **Keskkond**, **Liivakast** ja klõpsake valikut **Konfigureeri**
2. Valige oma **keskkonna topoloogia** ja läbige juurutamise käivitamiseks viisard.
3. Kohalik agent avab juurutustaotluse, alustab juurutamist ja annab LCS-ile valmis saades tagasisidet.

