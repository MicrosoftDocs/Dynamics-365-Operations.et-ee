---
title: Commerce'i pitseeritud iseteeninduskomponentide hulgijuurutus
description: See artikkel selgitab, kuidas kasutada iseteeninduse komponendi installijatele raamistikku installimis- ja teenuse juurutamiseks.
author: jashanno
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2021-04-30
ms.openlocfilehash: 66a711aff90221e594f4b2a0df3735eac93d0c9b
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/31/2022
ms.locfileid: "9387015"
---
# <a name="mass-deployment-of-sealed-commerce-self-service-components"></a>Commerce'i pitseeritud iseteeninduskomponentide hulgijuurutus

[!include [banner](../includes/banner.md)]

See artikkel kehtib pitseeritud raamistiku kohta, komponendi installijatele, mis vabastatakse igal kuul, alustades väljalaskega 10.0.18 Microsoft Dynamics ja mis tehakse kättesaadavaks elutsükli teenuste (LCS) ühises varateegis. Pange tähele, et nende uute installijate esimesed mitu väljalaset on määratud kui **(eelvaade)**. Selle määramise ainus eesmärk on eristada uusi installereid, kui Microsoft määrab, kas nende kasutamiseks on lisa funktsiooninõudeid. See ei tähenda, et installijad ei sobi tootmiseks. Tuginedes nende uute installerite väljalasele, plaanib Microsoft amortiseerida vanad (pärand) installijad 2023. aasta oktoober jooksul või selle ümber. 

See artikkel selgitab, kuidas kasutada uusi installijad vaikse installi ja värskenduste hooldamine käsurea argumentide kaudu. Need argumendid lasevad teil teha mitmeti juurutamist mitmel viisil.

> [!NOTE]
> Uued iseteeninduskeskuses pitseeritud installerid ei ole peakontoris saadaval ja neid saab alla laadida ainult LCS-i kaudu.

## <a name="delimiters-for-mass-deployment"></a>Hulgijuurutuse eraldajad

Järgmine tabel näitab eraldajaid, mida saab käsurea käivitamises kasutada.


| Eraldaja                 | Kirjeldus |
|---------------------------|-------------|
| –AadTokenIssuerPrefix | Microsofti () loa Azure Active Directory väljaandja Azure AD eesliide. |
| –AsyncClientAadClientId | Kliendi Azure AD ID, mida Async Client peaks peakontoriga side ajal kasutama. |
| –AsyncClientAppInssünkroonsInstrumentationKey | Async Clienti AppInsights vahendamise võti. |
| –AsyncClientCertFullPath | Täielikult vormindatud URN-tee, mis kasutab sõrmejälge Async Clienti Azure AD identiteedi serdi asukoha otsingumõõdustikna, mida tuleks kasutada autentimiseks peakontoriga suhtlemisel. Näiteks on `store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` õigesti vormindatud URLN. **\<MyThumbprint\>** Väärtus asendatakse kasutatava serdi sõrmejäljega. Ärge kasutage seda parameetrit koos parameetriga **-AsyncClientCertThumbprint**. |
| –AsyncClientCertThumbprint | Async Clienti identiteedi serdi sõrmejälg, mida tuleks kasutada autentimiseks peakontoriga Azure AD suhtlemisel. Seda sõrmejälge kasutatakse LocalMachine’i **/** minu kaupluse asukoha ja nime otsimiseks õige kasutatava serdi leidmiseks. Ärge kasutage seda parameetrit koos parameetriga **-AsyncClientCertFullPath**. |
| -ClientAppInsarvutidInstrumentationKey | AppInsights Kliendi vahendivahendi võti. |
| -CloudPosAppInsklahvisInstrumentationKey | Pilve kassa AppInsights vahenditeenuse võti |
| -Konfiguratsioon | Installi käigus kasutatav konfiguratsioonifail. Failinime näiteks on **Contoso.CommerceScaleUnit.xml**. |
| –CposAadClientId | Kliendi Azure AD ID, mida Cloud POS peaks seadme aktiveerimisel kasutama. See parameeter ei ole nõutav ettevõttes juurutamiseks. |
| –seade | Seadme ID, nagu näidatud peakontori **seadmete** lehel. |
| -EnvironmentId | Keskkonna ID |
| -HardwareStationAppInskonfiguratsioonisInstrumentationKey | Riistvarajaama vahendi AppInsights võti. |
| Installi | Parameeter, mis määrab, kas installija esitatud komponent tuleb installida. See parameeter on vajalik installi sooritamiseks ning sellel ei ole juhtkriipsu märki. |
| -InstallOffline | Modern POS-i puhul määrab see parameeter, et ka võrguühenduseta andmebaas tuleb installida ja konfigureerida. Kasutage ka **parameetrit -SQLServerName**. Vastasel juhul proovib installiprogramm leida eeltingimustele vastanud vaikeeksemplari. |
| – port | Port, mida jaemüügiserveri virtuaalkaust peab seostama ja kasutab. Kui ühtegi porti pole määratud, kasutatakse vaikeporti 443. |
| -Registreeri | Registri ID, nagu näha peakontori **lehel** Registrid. |
| –RetailServerAadClientId | Kliendi Azure AD ID, mida jaemüügiserver peaks peakontoriga side ajal kasutama. |
| –RetailServerAadResourceId | Jaemüügiserveri rakenduse Azure AD ressursi ID, mida tuleb kasutada seadme aktiveerimisel. See parameeter ei ole nõutav ettevõttes juurutamiseks. |
| –RetailServerCertFullPath | Täielikult vormindatud URLN-tee, mis kasutab sõrmejälge, kui jaemüügiserveri Azure AD identiteedi serdi otsingumõõdustik, mida tuleks kasutada autentimiseks peakontoriga suhtlemisel. Näiteks on õigesti vormindatud URLN, `store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` kus väärtus **\<MyThumbprint\>** asendatakse kasutatava serdi sõrmejäljega. Ärge kasutage seda parameetrit koos parameetriga **-RetailServerCertThumbprint**. |
| –RetailServerCertThumbprint | Jaemüügiserveri identiteedi serdi sõrmejälg, mida tuleks kasutada autentimiseks peakontoriga Azure AD suhtlemisel. Seda sõrmejälge kasutatakse LocalMachine’i **/** minu kaupluse asukoha ja nime otsimiseks õige kasutatava serdi leidmiseks. Ärge kasutage seda parameetrit koos parameetriga **-RetailServerCertFullPath**. |
| –RetailServerURL | Jaemüügiserveri URL, mida installer peaks kasutama. (Seda URL-i nimetatakse ka Commerce Scale Unitiks \[CSU\] URL.) Modern POS-i puhul kasutatakse seda väärtust seadme aktiveerimisel. |
| –SkipAadCredentialsCheck| Lüliti, mis näitab, kas Azure AD mandaadi eeltingimuste kontrollid tuleks vahele jätta. Vaikeväärtus on **väär**. |
| –SkipCertCheck | Lüliti, mis näitab, kas serdi eeltingimuse kontrollid tuleks vahele jätta. Vaikeväärtus on **väär**. |
| -SkipiisCheck | Lüliti, mis näitab, kas teenuse Internet Information Services (IIS) eeltingimuse kontrollid tuleks vahele jätta. Vaikeväärtus on **väär**. |
| -SkipNetFrameworkCheck | Lüliti, mis näitab, kas .NET Frameworki eeltingimuste kontrollid tuleks vahele jätta. Vaikeväärtus on **väär**. |
| –SkipScaleUnitCheck | Lüliti, mis näitab, kas installitud komponentide seisundi kontroll tuleks vahele jätta. Vaikeväärtus on **väär**. |
| –SkipsChannelCheck | Lüliti, mis näitab, kas turvalise kanali eeltingimuse kontrollid tuleks vahele jätta. Vaikeväärtus on **väär**. |
| -SkipSqlFullTextCheck | Lüliti, mis näitab, kas SQL Serveri täisteksti otsingut vajav eeltingimuse kinnitamine tuleks vahele jätta. Vaikeväärtus on **väär**. |
| -SkipSqlServerCheck | Lüliti, mis näitab, kas SQL Serveri eeltingimuste kontrollid tuleks vahele jätta. Vaikeväärtus on **väär**. |
| -SQLServerName | SQL Serveri nimi. Kui nime pole määratud, proovib installer leida vaikeeksemplari. |
| –SslcertFullPath | Täielikult vormindatud URLN-tee, mis kasutab sõrmejälge serdi asukoha otsingumõõdustikuna, mida tuleks kasutada HTTP liikluse krüptimiseks kaaluühikul. Näiteks on õigesti vormindatud URLN, `store:\/\/My\/LocalMachine\?FindByThumbprint\=\<MyThumbprint\>` kus väärtus **\<MyThumbprint\>** asendatakse kasutatava serdi sõrmejäljega. Ärge kasutage seda parameetrit koos parameetriga **-SslCertThumbprint**. |
| –SslCertThumbprint | Serdi sõrmejälg, mida tuleks kasutada HTTP krüptimiseks kaaluühikuga. Seda sõrmejälge kasutatakse LocalMachine’i **/** minu kaupluse asukoha ja nime otsimiseks õige kasutatava serdi leidmiseks. Ärge kasutage seda parameetrit koos parameetriga **-SslCertFullPath**. |
| – StoreSystemAosUrl | Peakontori (AOS) URL. |
| –StoreSystemChannelDatabaseId | Kanali andmebaasi ID (nimi). |
| -RentnikId | Rentniku Azure AD ID. |
| –TransactionServiceAzureAuthority | Amet Transaction Service Azure AD. |
| –TransactionServiceAzureResource | Transaction Service’i Azure AD ressurss |
| –TrustSqlServerCertificate | Lüliti, mis näitab, kas Serveri serti peaks SQL Serveri ühenduse loomise ajal usaldama. Turvariske vältides ei tohi tootmisjuurutused kunagi siia tarnida tõest **väärtust**. Vaikeväärtus on **väär**. |
| –Verbosity | Installi ajal nõutav logimise tase. Tavaliselt ei tohi seda väärtust kasutada. |
| -WindowsPhoneAppInsklahvisInstrumentationKey | Riistvarajaama vahendi AppInsights võti. |

## <a name="general-overview"></a>Üldine ülevaade

Iseteenindusinstallijate uuel raamistikul on erinevad funktsioonid ja täiustused. Uus raamistik loob praegu installijad ainult Modern POS-ile, riistvarajaamale ja CSU-le (ise majutatud). On oluline mõista pitseeritud installeride põhilist käsureakasutust, mis peaks sarnanema järgmise näite omaga. 
 
```Console
<Component Installer Name>.exe install -<Parameter Name> "<Parameter Information>"
```

Installiprogramm nõuab parameetri **installimist** (või **desinstallimist** installi eemaldamiseks) ja selle installi spetsiifilisi parameetreid. **Parameetri nimi** peab sisaldama mis tahes vajalikke parameetreid, nt registrit, CSU URL-i või serditeavet. **Parameetriteave** peaks hõlmama mis tahes lisateavet parameetrite kohta.

Pitseeritud raamistik on loodud selleks, et lubada järgmisi muudatusi:
- **Pitseeritud** – uus installeri raamistik eraldab Microsofti jaotatud põhikomponendi installerid laiendatavusel põhinevatest kohandustest. Seejärel installitakse kohandused, kuid need tühistatakse seejärel uuenduste puhul (nii lubatakse värskendusi ainult Microsofti baaskomponendi, ainult kohanduste või mõlema puhul).
- **GUI-väiksem** – liidest (UI) pole enam. Selle asemel on iga komponendi installeri jaoks täielikult käsureaga juhitav täitmisfail. See muudatus on üks mitmest võtmemuudatuses või -funktsioonist, mida kasutatakse uue installeri raamistiku fookuses hulgijuurutusega kasutamiseks.
- **Sündmuste logimine** – täiustatud installilogid võimaldavad installi lõpuleviimise või nurjumise paremat kinnitamist, läbi viidud etappe ja loodud hoiatusi või tõrkeid.
- **Puhastamine** : uues raamistikus teevad komponendi installerid tööd installikaustade täieliku terviklikkuse säilitamiseks, puhastades enne uute komponentide installimist komponendi kausta täieliku sisu. See puhastus tagab, et puuduvad üle jäänud failid, mis võivad põhjustada probleeme ja ennetada edukat installimist.

Uude raamistikku ei ole ülekantud kolme komponenti: virtuaalne välis simulaator, Async Server Connectori teenus (kasutatakse Dynamics AX 2012 R3 toe puhul) ja Reaalajas teenuse asendus (kasutatakse Dynamics AX 2012 R3 toe puhul).

> [!NOTE]
> Installijad talletatakse kohalikult ja kinnipeetud.  Oluline on aja jooksul hallata või kustutada kinnipeetud installijad kettaruumi mitterajamiseks. On soovitatav säilitada põhikomponentide praegune installer ja kõik uusimate versioonide laiendiinstallid erakordstest olukordadest taastamiseks.

## <a name="migration"></a>Migratsiooni

Vanade iseteeninduse raamistiku komponendi installerilt uutele raamistiku komponendiinstallijatele tuleb vanad komponendid desinstallida.

- **Modern POS** – uus installeri raamistik põhjustas rakendusele uue rakenduse allkirja ID saamise. Seetõttu on enne uue Modern POS-i komponendi installimist vaja vanade komponentide täielikku desinstallimist. Täieliku desinstallimise nõude tõttu nõutakse seadme aktiveerimist uuesti. (See seadme taasaktiveerimine on korrane nõue, kuid desinstallimist ei esine uuesti.)
- **Riistvarajaam –** IIS-i veebisaidina nõuab uus installeri raamistik põhikausta struktuuri uuesti tööd. Seetõttu on enne uue raamistiku riistvarajaama komponendi installimist vaja vanade komponentide täielikku desinstallimist.
- **Commerce Scale Unit (CSU, ise hostitud)** – kuna mitmed IIS-i veebisaite, nõuab uus installiraamistiku, et põhikausta struktuur taastöötatakse.  Seetõttu nõutakse vanade komponentide täielikku desinstallimist enne uue raamistiku CSU (ise hostitud) komponendi installimist.

## <a name="modern-pos"></a>Modern POS

### <a name="before-you-begin"></a>Enne alustamist

On kriitiline eemaldada vana iseteeninduse Modern POS-i komponent. Lisateabe saamiseks vt selle artikli varasemaid migreerimistoiminguid.

> [!NOTE]
> Ühes arvutis, nagu arendaja topoloogia või demokeskkond või kui Commerce Scale Unit ja Modern POS on installitud samasse arvutisse, on võimalik, et Store Commerce ei saa seadme aktiveerimist lõpule viia. See probleem ilmneb, kuna Store Commerce ei saa võrgukõnesid samale arvutile teha (st kõned iseendale). Kuigi see ei peaks kunagi olema tootmissätte stsenaarium, saab probleemi leevendada, lubades AppContaaineri silmuse erandi, et side saaks toimuda sama arvutiga. Selle silmuse lubamiseks on avalikult saadaval erinevad avaldused. Lisateavet silmuse kohta vt"Silmuse [lubamine ja võrgu isolatsiooni tõrkeotsing"](/previous-versions/windows/apps/hh780593(v=win.10)). On oluline mõista, et silmus võib olla turvarisk, nii et ilma vajaduseta pole silmuse kasutamine soovitatav.

### <a name="examples-of-silent-deployment"></a>Vaikse juurutamise näited

See jaotis näitab näiteid käskudest, mida kasutatakse Modern POS-i installimiseks.

#### <a name="silently-install-modern-pos"></a>Installige Modern POS vaikses installis

Järgmine käsk installib (või uuendab) Modern POS-i vaikses installis. Sellel on standardne käsustruktuur, mida kasutatakse praegu installitud komponentide vaikseks hooldamiseks. Struktuur kasutab faili **&lt; InstallerName.exe&gt; põhiväärtusi**.

Järgnevad peamised käsud näitavad saadaolevaid valikuid, kui installi taotletakse. On väga soovitatav, et seda käsku kasutatakse installeri esmakordsel testimisel või kasutamisel.

```Console
CommerceModernPOS.exe -help install
```

> [!NOTE]
> Modern POS-i jaoks ei ole konfiguratsioonifail nõutav. Installiprogrammil on nüüd seadme aktiveerimise ajal kasutatavate väärtuste parameetrid (mis on selles artiklis varem kuvatud).

Järgmine käsk määrab kõik parameetrid, mida tuleb kasutada seadme aktiveerimisel pärast Modern POS-i rakenduse installimist. Selles näites kasutatakse **The-3** registrit, mis on demoandmetes tavaliselt Dynamics 365 Commerce kasutatav väärtus.

```Console
CommerceModernPOS.exe install -Register "Houston-3" -Device "Houston-3" -RetailServerURL "https://MyDynamics365CommerceURL.dynamics.com/Commerce"
```

Järgmine käsk määrab parameetrid, mida tuleks kasutada ühenduseta andmebaasi installimiseks ja konfigureerimiseks. SQL Server on määratud koos kasutatava konfiguratsioonifailiga.

```Console
CommerceModernPOS.exe install -InstallOffline -SQLServerName "SQLExpress" -Config "ModernPOS.Houston-3.xml"
```

Nende mõistete segamist ja sobitamist saate kasutada soovitud installitulemuste saavutamiseks.

## <a name="hardware-station"></a>Riistvarajaam

### <a name="before-you-begin"></a>Enne alustamist

On oluline eemaldada vana iseteeninduse riistvarajaama komponent. Lisateabe saamiseks vt selle artikli varasemaid migreerimistoiminguid. Kaupmehe konto teabe tööriist pole enam olemas. Selle asemel installitakse kaupmehe konto teave, kui müügikoha terminal on ühendatud riistvarajaamaga. Selle installeri esmakordsel testimisel on soovitatav käitada järgmist käsku:

```Console
CommerceHardwareStation.exe -help install
```

### <a name="examples-of-silent-deployment"></a>Vaikse juurutamise näited

Selles jaotises kuvatakse riistvarajaama installimiseks kasutatavate käskude näiteid.

#### <a name="silently-install-hardware-station"></a>Installige riistvarajaam vaikses installis

Järgmine käsk installib (või uuendab) riistvarajaama vaikselt. Sellel on standardne käsustruktuur, mida kasutatakse praegu installitud teenusekomponentide jaoks. Struktuur kasutab faili **&lt; InstallerName.exe&gt; põhiväärtusi**.

Järgmine põhikäsk käitab täitmisfaili installeri.

```Console
HardwareStation.exe install -Port 443 -StoreSystemAOSURL "https://MyDynamics365CommerceURL.dynamics.com/" -StoreSystemChannelDatabaseID "Houston" -SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers"
```

> [!NOTE]
> Konfiguratsioonifail ei ole riistvarajaama jaoks nõutav. Installeril on nüüd nõutavate väärtuste parameetrid (mis on selles artiklis varem kuvatud).

Järgmine käsk määrab kõik parameetrid, mis on nõutavad standardse installi eeltingimuste kontrolli vahelejätmiseks. 

> [!NOTE]
> Tšekkide vahelejätmine ei ole soovitatav ilma põhjaliku katsetamiseta enne seda või arendusolukordades.

```Console
HardwareStation.exe install -SkipFirewallUpdate -SkipOPOSCheck -SkipVersionCheck -SkipURLCheck -Config "HardwareStation.Houston.xml"
```

Nagu tava, on soovitud installitulemuste saavutamiseks ühine nende mõistete segamine ja sobitamine.

## <a name="commerce-scale-unit-self-hosted"></a>Commerce Scale Unit (isehostitud)

Selle installeri esmakordsel testimisel on soovitatav käitada järgmist käsku:

```Console
CommerceStoreScaleUnitSetup.exe -help install
```

### <a name="before-you-begin"></a>Enne alustamist

On kriitiline eemaldada vana iseteeninduse CSU (ise hostitud) komponent. Lisateabe saamiseks vt selle artikli varasemaid migreerimistoiminguid.

### <a name="examples-of-silent-deployment"></a>Vaikse juurutamise näited

Selles jaotises kuvatakse näited käskudest, mida kasutatakse CSU installimiseks (ise hostitud).

#### <a name="silently-install-csu-self-hosted"></a>Installige CSU vaikses installis (ise hostitav).

Järgmine käsk installib (või värskendab) CSU -d (ise hostitakse). Sellel on standardne käsustruktuur, mida kasutatakse praegu installitud komponentide vaikseks hooldamiseks. Struktuur kasutab faili **&lt; InstallerName.exe&gt; põhiväärtusi**.

Võrreldes teiste iseteeninduse installijatega on Commerce Scale Unit (CSU) keerukam ja nõuab üsna suurt hulka täiendavat teavet. Järgmine käsk on minimaalne käsk (koos parameetritega), mis on vajalik täitmisfaili installeri käivitamiseks siis, kui konfiguratsioonifaili pole olemas.

```Console
CommerceScaleUnit.exe install -port 446 -SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate -Config "Contoso.StoreSystemSetup.xml"
```

> [!NOTE]
> CsU (ise hostitud) jaoks on konfiguratsioonifail siiski nõutav.

Järgmine käsk on põhjalikum käsk, mis käitab täitmisfaili installerit mõne alternatiivse parameetriga.

```Console
CommerceScaleUnit.exe install -Port 446 -SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate -Verbosity 0 -Config "Contoso.StoreSystemSetup.xml"
```

Järgmine käsk määrab parameetrid, mis on nõutavad eeltingimuste kontrollimise vahelejätmiseks standardse installimise ajal. 

> [!NOTE]
> Tšekkide vahelejätmine ei ole soovitatav ilma põhjaliku katsetamiseta enne seda või arendusolukordades.


```Console
CommerceScaleUnit.exe installer -skipscaleunithealthcheck -skipcertcheck -skipaadcredentialscheck -skipschannelcheck -skipiischeck -skipnetcorebundlecheck -skipsqlservercheck -skipnetframeworkcheck -skipversioncheck -skipurlcheck -Config "Contoso.StoreSystemSetup.xml" -SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate
```

Nende mõistete segamist ja sobitamist saate kasutada soovitud installitulemuste saavutamiseks.

<!--## Mass deployment examples using InTune

This section will be added in a future update.

## Mass deployment examples using System Center Configuration Manager (SCCM)

This section will be added in a future update.-->

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
