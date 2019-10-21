---
title: Rakenduse Finance and Operations eemaldatud või aegunud funktsioonid.
description: See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada.
author: sericks007
manager: AnnBe
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70bb8404c5b0e2422948d0b89311c384e3686710
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181078"
---
# <a name="removed-or-deprecated-features-for-finance-and-operations"></a>Rakenduse Finance and Operations eemaldatud või aegunud funktsioonid.

[!include [banner](../includes/banner.md)]

See teema kirjeldab funktsioone, mis on rakendusest Finance and Operations eemaldatud või aegunud.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

See loend peaks aitama teil neid eemaldusi ja aegumisi oma plaanides arvesse võtta. 

> [!NOTE]
> Alates rakenduse Finance and Operations 2017. aasta juulikuu väljaandest platvormivärskendusega 8 on iga eemaldatud või aegunud funktsiooni puhul märgitud juurutuste tüüp. Kõik selles teemas mainitud varasemad versioonid toetasid ainult pilvejuurutusi.

> Üksikasjalikku teavet rakenduse Finance and Operations objektide kohta leiate teemast [Tehnilise teabe aruanded](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Saate võrrelda nende aruannete eri versioone, et õppida objektide kohta, mida on igas rakenduse Finance and Operations versioonis muudetud või eemaldatud.


## <a name="finance-and-operations-1006-with-platform-update-30"></a>Rakenduse Finance and Operations 10.0.6 platvormivärskendus 30

> [!IMPORTANT]
> Dynamics 365 for Finance and Operations 10.0.6 platvormivärskendusega 30 on saadaval suunatud kasutajatele eelväljaande osana. Sisu ja funktsioonid võivad muutuda. Lisateavet eelväljaannete kohta vt teemast [Teenusevärskenduste kättesaadavus](../../fin-and-ops/get-started/public-preview-releases.md).

### <a name="formdatetimecontrolsetutcstring"></a>FormDateTimeControl.setUtcString()

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Me kõrvaldame **setUtcString ()** meetodi, sest parem asenduse meetod on saadaval. |
| **Asendatud teise funktsiooniga?**   | Jah |
| **Mõjutatud tootealad**         | Platvorm |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud: 1. oktoobrist 2020, me ei plaani enam toetada **setUtcString ()** meetodit. Arendajad peaksid kasutama hoopis **setUtcDateTime ()** meetodit. |

### <a name="blacklist-report-it--feature-reference-it-00001"></a>Musta nimekirja aruanne (IT) – funktsiooni viide IT-00001

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Juriidiliselt pole vajalik. |
| **Asendatud teise funktsiooniga?**   | Ei |
| **Mõjutatud tootealad**         | Itaalia tõlge |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud: 1. oktoobrist 2020 me ei plaani enam toetada **musta nimekirja aruannet (IT) – funktsiooni viide IT-00001.** |

### <a name="domestic-tax-report--feature-reference-it-00003"></a>Siseriiklik maksuaruanne – funktsiooni viide IT-00003

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Juriidiliselt pole vajalik. |
| **Asendatud teise funktsiooniga?**   | Ei |
| **Mõjutatud tootealad**         | Itaalia tõlge |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud: 1. oktoobrist 2020 me ei plaani enam toetada **siseriiklikku maksuaruannet (IT) – funktsiooni viide IT-00003.** |


## <a name="finance-and-operations-1005-with-platform-update-29"></a>Rakenduse Finance and Operations 10.0.5 platvormivärskendus 29

### <a name="us-payroll-tax-updates"></a>USA palgaarvestuse maksu uuendused

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Me kõrvaldame kasutuselt USA palgaarvestuse funktsiooni maksu uuendused selle vähese kasutuse ja täiustatud funktsionaalsuse tõttu, mida pakutakse nüüd strateegiliste integratsioonide kaudu.  |
| **Asendatud teise funktsiooniga?**   | Jah |
| **Mõjutatud tootealad**         | Palk |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud: 1. oktoobril 2021. aastal plaanime enam USA palgaarvestuse klientidele maksu uuendusi mitte pakkuda. Funktsionaalsus jääb tootesse, kuid täiendused ei hoia enam funktsioone ajakohasena ja toote defekte hinnatakse iga juhtumi puhul eraldi. Lisateabe saamiseks vaadake teemat [USA palgaarvestuse maksu uuenduste kasutuselt kõrvaldamine lisana rakenduses Microsoft Dynamics 365 for Finance and Operations](https://aka.ms/financepayrollfaq). |


### <a name="data-management-staging-clean-up"></a>Andmehalduse koondamise puhastamine
|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Ei vasta põhinõuetele, mis on vajalikud perioodilise puhastamise plaanimiseks. |
| **Asendatud teise funktsiooniga?**   | Jah, töö ajaloo puhastuse funktsioon lisatakse terviklikult. |
| **Mõjutatud tootealad**         | Andmehaldus |
| **Juurutamissuvand**              | Kõik  |
| **Olek**                         | Aegunud: funktsiooni eemaldamise sihtperiood on aprill 2020. |

## <a name="finance-and-operations-1004-with-platform-update-28"></a>Rakenduse Finance and Operations 10.0.4 platvormivärskendus 28

### <a name="france-fec-accounting-data-export-in-xml"></a>Prantsusmaa: FEC raamatupidamisandmete eksport XML-vormingus

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | TXT-vorminguga asendatud **Prantsuse FEC auditifail** on saadaval suvanditega **Pearaamat** \> **Perioodilised ülesanded** \> **Andmete eksportimine**.
| **Asendatud teise funktsiooniga?**   | Jah |
| **Mõjutatud tootealad**         | Pearaamat |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud. Funktsiooni eemaldamise sihtperiood on 2020. aasta juuli. |


### <a name="legacy-navigation-bar"></a>Pärandnavigeerimisriba

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Päise joondus teiste Dynamicsi ja Office’i toodetega. Lisateavet vt teemast [Uuendatud navigeerimisriba, mis joondub Office’i päisega](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-finance-operations/updatednavbar).
| **Asendatud teise funktsiooniga?**   | Alates platvormivärskendusest 24 on kasutusele võetud otsingufunktsiooniga ümber kujundatud navigeerimisriba. |
| **Mõjutatud tootealad**         | Veebiklient |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud. Alates 2020. aasta aprillist pole pärandnavigeerimisriba enam saadaval. Selle ajani saavad kliendid ennistada pärandnavigeerimisriba lehe **Kliendi jõudlussuvandid** kaudu. |


## <a name="finance-and-operations-1002-with-platform-update-26"></a>Rakenduse Finance and Operations 10.0.2 platvormivärskendus 26


### <a name="legacy-default-action-behavior"></a>Vaiketegevuse pärandkäitumine

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Vaiketegevuste pärandkäitumine ruudustikes annab tulemuseks ootamatu veeru, millel on vaiketegevuse link ruudustiku veergude järel, mis on isikupärastamise kaudu ümber järjestatud. Selle probleemi parandab uus vaikimisi kleepetegevuse funktsioon. Lisateabe saamiseks vt teemat [Vaikimisi kleepetegevused ruudustikes](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/sticky-default-action). |
| **Asendatud teise funktsiooniga?**   | Alates platvormivärskendusest 21 on kasutusele võetud vaikimisi kleepetegevuste funktsioon. Saate selle funktsiooni lubada lehel **Kliendi jõudlussuvandid**. |
| **Mõjutatud tootealad**         | Ruudustikud veebikliendis |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud: alates aprillist 2020 on vaikimisi kleepetegevused vaikekäitumine ilma pärandkäitumisele ennistamise mehhanismita. |

### <a name="legacy-is-one-of-filtering-experience"></a>Pärandfiltreerimisvõimalus „üks (mitmest)“

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Filtreerimisvõimalus „üks (mitmest)” kujundati platvormivärskendusega 22 ümber plaaniga jätta see lõpuks ainsaks „üks (mitmest)” filtreerimisvõimalusest. |
| **Asendatud teise funktsiooniga?**   | Alates platvormivärskendusest 22 muutus filtreerimisvõimalus „üks (mitmest)” saadavaks lehel **Kliendi jõudlussuvandid**. Lisateabe saamiseks vt teemast [Filtreerimisvõimalust „üks (mitmest)” on optimeeritud](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering). |
| **Mõjutatud tootealad**         | Veebiklient |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud: alates aprillist 2020 on parandatud filtreerimisvõimalus „üks (mitmest)” vaikekäitumine ilma pärandkäitumisele ennistamise mehhanismita. |

### <a name="parameter-to-enable-sales-orders-with-multiple-project-contract-funding-sources"></a>Parameeter müügitellimuste lubamiseks mitme projektilepingu rahastamisallikaga
Projektipõhiste müügitellimuste loomise toe, kui projektilepingul on mitu rahastamisallikat, lubatakse suvandi **Projektihalduse parameetrid** sättega **Luba müügitellimused mitme rahastamisallikaga projekti puhul**. Vaikimisi ei ole see parameeter lubatud. 

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Pärast parameetri eemaldamist on see funktsioon alati lubatud. |
| **Asendatud teise funktsiooniga?**   | Nr Mitme rahastamisallikaga projektipõhiste müügitellimuste toetamise funktsioon on alati lubatud.   |
| **Mõjutatud tootealad**         |Parameeter **Luba müügitellimused mitme rahastamisallikaga projektide puhul**. Parameetri eemaldamisel muudetakse järgmisi meetodeid: meetod **ctrlSalesOrderTable** klassis **ProjStatusType**, meetod **valideeri** välja **ProjId** puhul ja meetod **käita** vormil **SalescreateOrder**. Parameetri eemaldamisel muutuvad aegunuks järgmised meetodid: meetod **IsSalesOrderAllowedForMultipleFundingSources** tabelifailis **ProjTable**, meetod **IsAllowSalesOrdersForMultipleFundingSourcesParamEnabled** tabelifailis **ProjTable**, andmeväli **AllowSalesOrdersForMultipleFundingSources** vormil **ProjParameters** ja failides **ProjParameterEntity**, privaatmeetod **IsAssociatedToMultipleFundingSourcesContract** tabelifailis **ProjTable**. |
| **Juurutamissuvand**              | Kõik  |
| **Olek**                         | Aegumine on plaanitud 2020. aprilli väljalaskevoogu. |

### <a name="legacy-workflow-reports-for-tracking-and-instance-status"></a>Pärand-töövooaruanded jälgimise ja eksemplari oleku kohta

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Pärand-töövooaruanded jälgimise ja eksemplari oleku kohta kõrvaldatakse kasutuselt, kuna navigeerimisest neile enam ei viidata. Aruannete nimed on WorkflowWorkflowInstanceByStatusReport ja WorkflowWorkflowTrackingReport. |
| **Asendatud teise funktsiooniga?**   | Nende asemel saab kasutada töövoo ajaloo vormi. |
| **Mõjutatud tootealad**         | Veebiklient |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud: funktsiooni eemaldamise sihtperiood on aprill 2020. |

## <a name="finance-and-operations-1001-with-platform-update-25"></a>Rakenduse Finance and Operations 10.0.1 platvormivärskendus 25

### <a name="deprecated-apis-and-potential-breaking-changes"></a>Aegunud API-d ja võimalikud murrangulised muudatused


#### <a name="deriving-from-internal-classes-is-deprecated"></a>Siseklassidest tuletamine on aegunud

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Enne platvormivärskendust 25 oli võimalik luua klass või tabel, mis on tuletatud teises paketis/moodulis määratletud siseklassist/-tabelist. See ei ole ohutu programmeerimistava. Alates platvormivärskendusest 25 kuvab kompilaator hoiatuse. |
| **Asendatud teise funktsiooniga?**   | Kompilaatori hoiatus asendatakse platvormivärskenduses 26 tõrkega. See muudatus on käitamise ajal tagasiühilduv, mis tähendab seda, et platvormivärskenduse 25 või uuema saab juurutada ükskõik millises liivakasti- või tootmiskeskkonnas ilma kohandatud koodi muutmata. See muudatus mõjutab ainult arendus- ja kompileerimisaega.|
| **Mõjutatud tootealad**         | Visual Studio arendustööriistad |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud: hoiatus muutub platvormivärskenduses 26 kompileerimistõrkeks. |

#### <a name="overriding-internal-methods-is-deprecated"></a>Sisemeetodite alistamine on aegunud

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Enne platvormivärskendust 25 oli võimalik alistada teises paketis/moodulis määratletud tuletatud klassi sisemeetod. See ei ole ohutu programmeerimistava. Alates platvormivärskendusest 25 kuvab kompilaator hoiatuse. |
| **Asendatud teise funktsiooniga?**   | See hoiatus asendatakse platvormivärskenduses 26 kompileerimistõrkega. See muudatus on käitamise ajal tagasiühilduv, mis tähendab seda, et platvormivärskenduse 25 või uuema saab juurutada ükskõik millises liivakasti- või tootmiskeskkonnas ilma kohandatud koodi muutmata. See muudatus mõjutab ainult arendus- ja kompileerimisaega. |
| **Mõjutatud tootealad**         | Visual Studio arendustööriistad |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud: hoiatus muutub platvormivärskenduses 26 kompileerimistõrkeks. |

## <a name="finance-and-operations-1000-with-platform-update-24"></a>Rakenduse Finance and Operations 10.0.0 platvormivärskendus 24

### <a name="renaming-released-products"></a>Väljastatud toodete ümbernimetamine 
|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Kui kasutate funktsiooni **Nimeta esmane võti ümber**, et muuta väljastatud toote ItemId värskendatakse ainult võõrvõtme viited. Mis tahes muud väljastatud toote viited, näiteks tootmistellimustest, säilitavad vana ItemId. Tulemuseks võivad olla ebaühtlased andmed, mis lõpuks blokeerivad äriprotsessid. |
| **Asendatud teise funktsiooniga?**   | Nr |
| **Mõjutatud tootealad**         | Tooteteabe haldus |
| **Juurutamissuvand**              | Kõik  |
| **Olek**                         | Eemaldatud Finance and Operationsi versioonist 10.0.0 platvormi värskendusega 24. Erandjuhtudel, näiteks väljastatud toote esmase võtme varasema ümbernimetamise taastamine, on Microsoftilt võimalik taotleda väljastatud toodete esmase võtme ümbernimetamise piirangu ajutist eemaldamist. |


## <a name="finance-and-operations-813-with-platform-update-23"></a>Rakenduse Finance and Operations 8.1.3 platvormivärskendus 23

### <a name="sql-server-reporting-services-reportviewer-control"></a>Teenuse SQL Server Reporting Services juhtelement ReportViewer
Kliendid saavad platvormi Finance and Operations rakenduste loodud dokumentide allalaadimiseks kasutada teenuse SQL Server Reporting Services (SSRS) manustatud juhtelemendi ReportViewer tegevust **Ekspordi**. See HTML-il põhinev aruande kuvamine võimaldab kasutajatel näha dokumendi lehekülgjaotuseta eelvaadet.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | HTML-il põhineva eelvaate lehekülgjaotuseta vormi tõttu **ei** ole platvormiga Finance and Operations lõplikult loodavad füüsilised dokumendid täpselt samasugused. Kasutades äridokumentide standardvorminguna PDF-i, saavad kasutajad rakenduse aruannete loomisel kasutada ära parandatud jõudlusega tänapäevaseid kuvamisvõimalusi. |
| **Asendatud teise funktsiooniga?**   | Lähitulevikus saab PDF-dokumentidest platvormi Finance and Operations renderdatud aruannete vaikevorming.   |
| **Mõjutatud tootealad**         | See muudatus **ei** mõjuta selliseid kliendistsenaariume, mille korral aruandeid levitatakse elektrooniliselt või saadetakse otse printeritesse.    |
| **Juurutamissuvand**              | Kõik  |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata. Rakenduse aruannete automaatse eelvaatamise funktsioon manustatud PDF-vaaturiga on kavandatud 2019. aasta mai platvormivärskendusse. |

### <a name="client-kpi-controls"></a>Kliendi KPI-juhtelemendid
Arendaja saab manustatud juhtimismõõdikuid (KPI-d) Visual Studio kaudu modelleerida ja lõppkasutaja neid veelgi kohandada.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | KPI-de määramiseks kasutatavad kliendi algsed juhtelemendid püüdsid vähe kliente ja vajasid jälgitavate mõõdikute lisamiseks arendajat. |
| **Asendatud teise funktsiooniga?**   | Teenusel PowerBI.com on olemas tipptasemel tööriistad välistest allikatest pärinevatel andmetel põhinevate KPI-de määramiseks ja haldamiseks.  Tulevases väljaandes plaanime anda teile võimaluse manustada teenuse PowerBI.com majutatud lahendusi rakenduste tööruumides.   |
| **Mõjutatud tootealad**         | See värskendus takistab arendajatel Visual Studio kujundajas uute KPI-juhtelementide loomise.    |
| **Juurutamissuvand**              | Kõik  |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata. |

### <a name="deprecated-apis-and-future-breaking-changes"></a>Aegunud API-d ja tulevased murrangulised muudatused

#### <a name="field-groups-containing-invalid-field-references"></a>Sobimatuid väljaviiteid sisaldavad väljagrupid

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Tabeli metaandmete definitsioonidel korral on võimalik, et väljagrupid sisaldavad sobimatuid väljaviiteid. See probleem on praegu liigitatud *kompilaatori hoiatuseks*, mitte *tõrkeks*, mis tähendab, et juurutatava paketi loomist ja juurutamist saab jätkata ilma probleemi kõrvaldamata. Juurutamise korral võib see põhjustada käitusaja tõrkeid finantsaruandluses ja SQL Serveri aruandlusteenustes (SSRS). Probleemi kõrvaldamiseks:<br><br>1. Eemaldage sobimatu väljaviide tabeli väljagrupi definitsioonist.<br><br>2. Kompileerige uuesti.<br><br>3. Veenduge, et kõikide hoiatuste või tõrgetega oleks tegeletud. |
| **Asendatud teise funktsiooniga?**   | See hoiatus asendatakse tulevikus kompileerimistõrkega.  |
| **Mõjutatud tootealad**         | Visual Studio arendustööriistad. |
| **Juurutamissuvand**              | Kõik. |
| **Olek**                         | Aegunud: hoiatus muutub tulevikus kompileerimisaegseks tõrkeks. Oleme sihiks võtnud 30. platvormivärskenduse. |

#### <a name="complete-list"></a>Täielik loend
Aegunuks kuulutatud API-de täieliku loendi nägemiseks vt teemat [Meetodite ja metaandmete elementide aegunuks kuulutamine](deprecation-deletion-apis.md).

## <a name="finance-and-operations-81-with-platform-update-20"></a>Finance and Operations 8.1 platvormivärskendusega 20

### <a name="batch-transfer-rules-for-subledger-journal-account-entries"></a>Partii ülekannete reeglid alammooduli töölehe konto kirje puhul
Pearaamatu parameetrites muutub sünkroonne ülekanderežiim aegunuks.  Režiim asendatakse ainult asünkroonse ja planeeritud partiiga, mis on juba ülekandmissuvandina olemas. Lisateabe saamiseks vt ajaveebipostitust [Pearaamatu parameetrid – partii ülekandereeglid](https://community.dynamics.com/365/financeandoperations/b/financials/archive/2019/03/15/general-ledger-parameters-batch-transfer-rules).

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Eemaldame sünkroonse suvandi jõudlusmõju tõttu süsteemile. |
| **Asendatud teise funktsiooniga?**   | Asünkroonne ja planeeritud partii on suvandid, mida saab sünkroonse režiimi asemel kasutada.   |
| **Mõjutatud tootealad**         | Pearaamat, ostureskontro, müügireskontro, hange, kulu    |
| **Juurutamissuvand**              | Kõik  |
| **Olek**                         | Aegunud: funktsiooni eemaldamise sihtperiood on versioon 10.0.|

### <a name="electronic-reporting-for-russia"></a>Elektrooniline aruandlus Venemaa puhul
Funktsioon deklaratsioonide TXT- ja XML-failivormingute konfigureerimiseks. 

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Asendatud elektroonilise aruandlusega. |
| **Asendatud teise funktsiooniga?**   | Jah. |
| **Mõjutatud tootealad**         | Pearaamat |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Eemaldatud alates rakenduse Finance and Operations 8.1 platvormivärskendusest 20. |

### <a name="financial-reports-generator-for-russia"></a>Finantsaruannete generaator Venemaa jaoks
Tööriist andmete kogumise seadistamiseks raamatupidamise ja maksuaruannete jaoks ning andmete eksportimiseks XLS- ja DOC-aruandemallidesse. Funktsionaalsed osad: andmete eksportimine XLS- ja DOC-aruandemallidesse, päringud, fikseeritud rekvisiidid on eemaldatud. 

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Eemaldatud osad on asendatud elektroonilise aruandlusega. |
| **Asendatud teise funktsiooniga?**   | Jah. GL-i kontode või maksuregistritega andmekogumisreeglite seadistamiseks tuleb kasutada finantsaruannete seadistuse kasutajaliidest. Andmete eksportimine erinevatesse failitüüpidesse, fikseeritud rekvisiidid ja päringulaadsete andmete kogumisreeglid tuleb konfigureerida elektroonilises aruandluses. |
| **Mõjutatud tootealad**         | Pearaamat. |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Eemaldatud alates rakenduse Finance and Operations 8.1 platvormivärskendusest 20. |

### <a name="integration-with-external-providers-for-sending-electronic-reporting-through-communication-channels-for-russia"></a>Integratsioon väliste pakkujatega elektroonilise aruandluse saatmiseks kommunikatsioonikanalite kaudu Venemaa puhul
Funktsioon loodud deklaratsioonide elektrooniliste failide saatmiseks kausta edasisaatmiseks elektroonilise aruandluse ametlikele pakkujatele ning oleku tagasi importimiseks.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Asendatud elektrooniliste teadete konfigureerimise funktsiooniga. |
| **Asendatud teise funktsiooniga?**   | Jah.  |
| **Mõjutatud tootealad**         | Pearaamat, maks |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Eemaldatud alates rakenduse Finance and Operations 8.1 platvormivärskendusest 20. |


### <a name="profit-tax-register-wizard"></a>Kasumimaksu registreerimise viisard
Funktsioon uute kasumimaksuregistrite jaoks mallide loomiseks. See funktsioon loob X++ objektid uute registrite jaoks, mis luuakse seejärel mallidena, millele on lisatud vastav arvutusloogika.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Funktsioon ei ühildu rakenduse Finance and Operations laiendatavuse mudeliga. |
| **Asendatud teise funktsiooniga?**   | Ei |
| **Mõjutatud tootealad**         | Maks |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Eemaldatud alates rakenduse Finance and Operations 8.1 platvormivärskendusest 20. |


## <a name="finance-and-operations-80-with-platform-update-15"></a>Finance and Operations 8.0 platvormivärskendusega 15
Selles versioonis pole ühtki funktsiooni eemaldatud ega ükski pole aegunud. Platvormivärskendus 15 on kumulatiivne ja sisaldab uusi või muudetud funktsioone platvormivärskendusest 13, platvormivärskendusest 14 ja platvormivärskendusest 15.

## <a name="finance-and-operations-enterprise-edition-73-with-platform-update-12"></a>Eemaldatud alates rakenduse Finance and Operations väljaandest Enterprise edition 7.3 platvormivärskendusega 12.

### <a name="personalized-product-recommendations"></a>Isikupärastatud tootesoovitused 
Alates 15. veebruarist 2018 ei ole jaemüüjatel enam võimalik kassaseadmes isikupärastatud tootesoovitusi kuvada. Lisateavet vt teemast [Isikupärastatud tootesoovitused](../../retail/personalized-product-recommendations.md).  

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Eemaldame tootesoovitusteenuse praeguse versiooni kuniks me seda funktsiooni parema algoritmi ja uuemate jaemüügile suunatud võimalustega täiustame.  |
| **Asendatud teise funktsiooniga?**   | Nr Siiski plaanime selle funktsiooni pärast 2018. aasta kevadet uue soovitusteenuse võimendamiseks taastada.   |
| **Mõjutatud tootealad**         | Isikupärastatud tootesoovitused kassas.                                                    |
| **Juurutamissuvand**              | Kõik                                                                                      |
| **Olek**                         |Eemaldatud alates 15. veebruarist 2018. See mõjutab kliente, kes kasutavad Dynamics 365 for Operations 1611 või uuemat versiooni.  |

### <a name="extension-of-the-list-of-electronic-reporting-er-functions"></a>Elektroonilise aruandluse (ER) funktsioonide loendi pikendus
Võimalust võtta kasutusele ER avaldisekoosturis kasutatavaid funktsioone (lisateavet vt teemast [Elektroonilise aruandluse funktsioonide loendi pikendus](../../dev-itpro/analytics/general-electronic-reporting-formulas-list-extension.md)) enam ei toetata. ER-i API-de muudatuste tõttu muutuvad kutsutava API sisseehitatud funktsioonid ER-i avaldisekoosturist sisemiseks ja neid ei saa enam laiendada.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Koodi sulgemise algatus  |
| **Asendatud teise funktsiooniga?**   | Puudub. Kui mõni uus sisseehitatud funktsioon on vajalik, tuleb uus laiendustaotlus esitada ER-i raamistiku meeskonnale.<br><br>Seni kui nõutud funktsioon on ER-i meeskonnas arendusel, saab nõutud loogika ajutiselt programmeerida kohandatud rakendusklassi meetodina. Seda meetodit saab kasutada ER-i avaldises sellele kohandatud rakendusklassile viitava **rakenduse/klassi** tüübi lisatud ER-i andmeallika atribuudina.  |
| **Mõjutatud tootealad**         | Elektroonilise aruandluse raamistik                                                      |
| **Juurutamissuvand**              | Kõik                                                                                      |
| **Olek**                         | Eemaldatud alates rakenduse Finance and Operations väljaandest Enterprise edition 7.3.    |

### <a name="inventory-by-item-group-and-inventory-by-inventory-dimension-aging-reports"></a>Varud kaubagrupi järgi ja varud varudedimensiooni ajalise jaotuse aruannete järgi

Neid kaht aruannet rakenduses Finance and Operations enam ei toetata. Selle asemel saab kasutajakogemuse parandamiseks kasutada aruannet **Varude ajaline jaotus**.

|   |  |
|--------------|-----------------------|
| **Kasutuselt eemaldamise põhjus**       | Topeltfunktsioon  |
| **Asendatud teise funktsiooniga?** | Jah. Need kaks aruannet on asendatud aruandega **Varude ajaline jaotus**.     |
| **Mõjutatud tootealad**       | Varude haldus, kuluhaldus        |
| **Juurutamissuvand**        | Kõik|
| **Olek**                       | Aegunud: nende kahe aruande menüü-üksused on versioonis 7.3 eemaldatud. Aruannete kood jääb siiski tootesse. Plaan on kood tulevases väljaandes eemaldada. |

### <a name="power-bi-content-packs-available-on-appsource"></a>Power BI sisupaketid on saadaval AppSource’is
Sisupaketid **Kuluhaldus**, **Finantstulemused** ja **Jaemüügikanali jõudlus**, mis on saadaval saidil [Microsoft AppSource](https://appsource.microsoft.com), on Microsoft Power BI tootevärskenduste tagajärjel aegunud. Nende sisupakettide juurutamiseks saidile PowerBI.com kasutatavad süsteemiadministreerimise v vormid on rakenduses Finance and Operations samuti aegunud.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Tootevärskendused rakenduses Microsoft Power BI. |
| **Asendatud teise funktsiooniga?**   | Sisupaketid **Kuluhaldus**, **Finantstulemused** ja **Jaemüügikanali jõudlus**, mis on saadaval saidil [AppSource](https://appsource.microsoft.com), on asendatud analüütiliste rakendustega, mis võimaldavad lahenduse integratsioone andmebaasi tasemel. Lisateavet analüütiliste rakenduste kohta vt teemast [Manustatud Power BI tööruumides](../../dev-itpro/analytics/embed-power-bi-workspaces.md).    |
| **Mõjutatud tootealad**         | Kuluhaldus, Finance ja Retail                                                                                               |
| **Juurutamissuvand**              | Ainult pilveteenus (integratsiooni PowerBI.com’iga ei toetata asutusesisestes juurutustes)                                                                                                            |
| **Olek**                         | Aegunud: funktsiooni eemaldamise sihtperiood on 2018. aasta 2. kvartal.    |

### <a name="standard-ui-in-data-management-workspace"></a>Standardne kasutajaliides andmehalduse tööruumis

Standardne kasutajaliides andmehalduses on pärandkasutajaliides, mis kuvatakse kasutajatele vaikimisi, kui nad külastavad andmehalduse tööruumi.

|   |  |
|------------------|-------------------------|
| **Aegumise/eemaldamise põhjus** | Investeerime uues kasutajaliideses uue kasutajakogemuse pakkumisele.             |
| **Asendatud teise funktsiooniga?**   | Vana kasutajaliidese asendab uus kasutajaliides nimega *Täiustatud vaated*.            |
| **Mõjutatud tootealad**         | Andmehalduse tööruum                                                     |
| **Juurutamissuvand**              | Kõik                                                                           |
| **Olek**                         | Aegunud: funktsiooni eemaldamise sihtperiood on 2018. aasta 2. kvartal. |

### <a name="excise-sales-tax-service-tax-for-india"></a>Aktsiis, käibemaks, teenindusmaks Indias

Need maksud on juba subsummeeritud India GST-sse.

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Aegumise või eemaldamise põhjus**       | Need maksud on juba subsummeeritud India GST-sse.                          |
| **Asendatud teise funktsiooniga?**            | India GST                                                              |
| **Mõjutatud tootealad**                  | Maks                                                                     |
| **Juurutamissuvand**                       | Kõik moodulid                                                   |
| **Olek**                                  | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata. |    

### <a name="file-validation-utility-fvu-for-india"></a>Faili kinnitamise utiliit (FVU) India jaoks

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Aegumise või eemaldamise põhjus**       | Kliendid ei kasuta                                                  |
| **Asendatud teise funktsiooniga?**            | Ei                                                                      |
| **Mõjutatud tootealad**                  | India kinnipeetav maks                                                  |
| **Juurutamissuvand**                       | Kõik moodulid                                                                    |
| **Olek**                                  | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.   |        

### <a name="tdstcs-certificate-for-india"></a>India TDS-i/TCS-i sert

Kasutajad saavad selle alla laadida valitsuse portaalist.

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Aegumise või eemaldamise põhjus**       | Kliendid ei kasuta                                                  |
| **Asendatud teise funktsiooniga?**            | Ei                                                                      |
| **Mõjutatud tootealad**                  | India kinnipeetav maks                                                  |
| **Juurutamissuvand**                       | Kõik moodulid                                                                   |
| **Olek**                                  | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.     |    

### <a name="exportimport-exim-incentive-scheme-for-india"></a>Ekspordi/impordi (EXIM) soodustuste süsteem India jaoks


|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Aegumise või eemaldamise põhjus**       | Kliendid ei kasuta                                                  |
| **Asendatud teise funktsiooniga?**            | Ei                                                                      |
| **Mõjutatud tootealad**                  | Import ja eksport                                                       |
| **Juurutamissuvand**                       | Kõik moodulid                                                                    |
| **Olek**                                  | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.  |    


## <a name="dynamics-365-for-retail-72"></a>Dynamics 365 for Retail 7.2

### <a name="personalized-product-recommendations"></a>Isikupärastatud tootesoovitused 
Alates 15. veebruarist 2018 ei ole jaemüüjatel enam võimalik kassaseadmes isikupärastatud tootesoovitusi kuvada. Lisateavet vt teemast [Isikupärastatud tootesoovitused](../../retail/personalized-product-recommendations.md).  

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Eemaldame tootesoovitusteenuse praeguse versiooni kuniks me seda funktsiooni parema algoritmi ja uuemate jaemüügile suunatud võimalustega täiustame.  |
| **Asendatud teise funktsiooniga?**   | Nr Siiski plaanime selle funktsiooni pärast 2018. aasta kevadet uue soovitusteenuse võimendamiseks taastada.   |
| **Mõjutatud tootealad**         | Isikupärastatud tootesoovitused kassas.                                                    |
| **Juurutamissuvand**              | Kõik                                                                                      |
| **Olek**                         |Eemaldatud alates 15. veebruarist 2018. See mõjutab kliente, kes kasutavad Dynamics 365 for Retail 7.2 või uuemat. |


## <a name="finance-and-operations-enterprise-edition-july-2017-with-platform-update-8"></a>Finance and Operations, Enterprise edition juuli 2017 platvormivärskendus 8

### <a name="currency-conversion-for-accounting-and-reporting-currencies"></a>Valuutateisendus arvestus- ja aruandlusvaluutade jaoks

Valuutateisenduse funktsioon arvestus- ja aruandlusvaluutade jaoks võeti kasutusele koos euro kasutuselevõtuga.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Piiratud kasutus ja juriidilise isiku Koopia funktsiooni lisamine asendamise jaoks.      |
| **Asendatud teise funktsiooniga?**   | Ei, aga funktsioonid juriidilise isiku Koopia ja Konfiguratsioonid lisati, et lihtsustada üleminekut ettevõttele, mille tuumnõudmised on muutuvad. |
| **Mõjutatud tootealad**         | Finantshaldus     |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.   |


### <a name="warehouse-mobile-devices-portal"></a>Lao mobiilsete seadmete portaal

Lao mobiilsete seadmete portaal (WMDP) oli eraldiseisev komponent, mis oli mõeldud ise toimivaks asutusesiseseks juurutamiseks. Seda komponenti rakenduses Finance and Operations enam ei toetata. WMDP funktsiooni on asendanud kasutajakogemust parandav omarakendus.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Topeltfunktsioon.       |
| **Asendatud teise funktsiooniga?**   | Jah. See funktsioon on asendatud Finance and Operationsi ladustamise mooduliga. Lisateavet seadistuse ja eeltingimuste kohta vt teemast [Rakenduse Microsoft Dynamics 365 for Finance and Operations mooduli Ladustamine installimine ja konfigureerimine](../../supply-chain/warehousing/install-configure-warehousing-app.md). |
| **Mõjutatud tootealad**         | Laohaldus, transpordihaldus     |
| **Juurutamissuvand**              | Lao mobiilsete seadmete portaal (WMDP) oli eraldiseisev komponent, mis oli mõeldud ise toimivaks asutusesiseseks juurutamiseks.               |
| **Olek**                         | Aegunud: funktsiooni eemaldamise sihtperiood on 2019. aasta 4. kvartal.   |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>Täpsema panga vastavusseviimise vastavusreegel käsitsi sobitamiseks

Vastavusreeglit kasutati pangadokumendi valimiseks ja märkimiseks, kui dokumente vastavusseviimise töölehel käsitsi sobitati.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Piiratud kasutus.                                                                         |
| **Asendatud teise funktsiooniga?**   | Nr Dokumentide leidmiseks, et neid vastavusse viia, tuleks kasutada veeru filtreerimise võimalusi. |
| **Mõjutatud tootealad**         | Sularaha- ja pangahaldus                                                               |
| **Juurutamissuvand**              | Kõik                                                                                    |
| **Olek**                         | Eemaldatud alates juulist 2017.                                                               |

## <a name="dynamics-365-for-operations-1611-with-platform-update-3"></a>Dynamics 365 for Operations 1611 platvormivärskendusega 3

### <a name="aeb-payment-formats-for-spain"></a>AEB maksevormingud Hispaania puhul

Kliendimaksete ja tarnijamaksete puhul kasutati rahaülekandefailide saatmiseks panka Consejo Superior Bancario maksevorminguid. Nende vormingute sisu määras Asociación Española de Banca. See hõlmab järgmist: Cuaderno 19 32 58 34.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Maksevorminguid enam ei kasutata.                                  |
| **Asendatud teise funktsiooniga?**   | Jah, ISO20022 kreeditiülekanne ja otsedeebeti maksevormingud Hispaania puhul |
| **Mõjutatud tootealad**         | Müügireskontro, ostureskontro                                    |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.           |

### <a name="bank-payments-transfer-for-lithuania"></a>Pangamaksete ülekanne Leedu puhul

Pangamakse ülekanded loodi ja prinditi, kasutades Leedu makseülekande (LT) ekspordivormingut. Leedu turg alustas LITAS-i (ühtlustatud elektroonilise pangandussüsteem) kasutamist 2005. aastal.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Maksevorminguid enam ei kasutata.                        |
| **Asendatud teise funktsiooniga?**   | Yes, ISO20022 kreeditiülekande maksevorming Leedu puhul     |
| **Mõjutatud tootealad**         | Ostureskontro                                               |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata. |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>BBS Direkte Remitteringi maksevormingud Norra puhul

BBS Direkte Remitteringi maksevormingud hõlmavad kliendimakse kogumise eksporti (otsene deebet) ja tagastusteate importi.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Maksevorminguid enam ei kasutata.  |
| **Asendatud teise funktsiooniga?**   | AvtaleGiro Norra kliendimakse vormingut saab kasutada otsedeebeti teadete loomiseks. Tagastusteate importi juurutatakse tulevastes väljalasetes. |
| **Mõjutatud tootealad**         | Müügireskontro, ostureskontro   |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.                                                                                                 |

### <a name="chart-of-accounts-tool-for-spain"></a>Kontoplaani tööriist Hispaania puhul

Seda tööriista kasutatakse siis, kui kontoplaan nõuab Hispaanias suuremaid muudatusi. Kasutajad saavad importida uue kontoplaani Microsoft Excelis või tekstivormingus ja saavad ka importida finantsaruandeid.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Piiratud kasutus                                                  |
| **Asendatud teise funktsiooniga?**   | Ei                                                             |
| **Mõjutatud tootealad**         | Pearaamat                                                 |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata. |

### <a name="dom80-payment-format-for-belgium"></a>Dom80 maksevorming Belgia puhul

Belgia pärandi maksevorming makse kogumiseks (otsedeebet).

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Maksevormingut enam ei kasutata.                          |
| **Asendatud teise funktsiooniga?**   | Jah, ISO 20022 otsedeebeti maksevorming Belgia puhul         |
| **Mõjutatud tootealad**         | Müügireskontro                                            |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata. |

### <a name="dtaezag-payment-formats-for-switzerland"></a>DTA/EZAG maksevormingud Šveitsi puhul

DTA-/EZAG-vormingud integreeritakse ESR-i süsteemi, kuna need saavad olla viitenumbril. Kuna viitenumber ei ole kohustuslik, saab neid vorminguid kasutada mis tahes hankija maksete töötlemiseks. Neid vorminguid kasutavad ettevõtted, millel on pangakonto asukohas, mis ei ole „finantsijärgne”.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Maksevorminguid enam ei kasutata.                        |
| **Asendatud teise funktsiooniga?**   | Yes, ISO20022 kreeditiülekande maksevorming Šveitsi puhul   |
| **Mõjutatud tootealad**         | Ostureskontro                                               |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata. |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>EDIFACT-DIRDEB-i maksevorming Austria puhul

EDIFACT-DIRDEB-i maksevorming makse kogumiseks (otsedeebet).

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Maksevormingut enam ei kasutata.                          |
| **Asendatud teise funktsiooniga?**   | Jah, ISO 20022 otsedeebeti maksevorming Austria puhul         |
| **Mõjutatud tootealad**         | Müügireskontro                                            |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata. |

### <a name="edivat-for-belgium"></a>EDIVAT Belgia puhul

EDIVAT on aegunud Belgia standard elektrooniliseks deklareerimiseks turvalise meili teel. Dynamics AX 2012 säilitab kirjutuskaitstud lahenduse, et lubada juurdepääsu ajaloolistele andmetele.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Funktsionaalsust enam ei kasutata.                           |
| **Asendatud teise funktsiooniga?**   | Ei                                                             |
| **Mõjutatud tootealad**         | Pearaamat                                                 |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata. |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>eGiro EDIFACT CREMUL makse impordivorming Norra puhul

eGiro põhineb rahvusvahelisel UN EDIFACT CREMUL-i (Multiple Credit Advice Message) standardil, mida kasutatakse kliendimaksete automaatseks sisestamiseks. Rakenduses Dynamics AX juurutatakse eGiro kliendimakse impordivorminguna.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Maksevormingut enam ei kasutata.                                                     |
| **Asendatud teise funktsiooniga?**   | Nr Vorming asendatakse tulevastes väljalasetes ISO 20022 väljavõtte impordivormingutega. |
| **Mõjutatud tootealad**         | Müügireskontro                                                                       |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.                            |

### <a name="external-inventory-for-poland"></a>Väliskaubavaru Poola puhul

Tõend kaupade hankijalt võtmise kohta ilma ostuta müügi puhul. Välislaos käsitletavaid kaupu, mis ei mõjuta standardseid varusid, saab müüa ja seejärel osta automaatselt. See protsess loob reaalsed varude teisaldamised.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Asendatud teise funktsiooniga                                    |
| **Asendatud teise funktsiooniga?**   | Jah, sissetuleva veose põhufunktsioon                |
| **Mõjutatud tootealad**         | Ostureskontro, laohaldus                         |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata. |

### <a name="financial-reports-generator-for-eastern-europe"></a>Finantsaruannete generaator Ida-Euroopa puhul

Tööriista kasutatakse andmete kogumise seadistamiseks raamatupidamise ja maksuaruannete jaoks ja andmete XLS- ja DOC-aruande mallidesse eksportimiseks.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Piiratud kasutus                                                                            |
| **Asendatud teise funktsiooniga?**   | Nr Tööriist asendatakse tulevastes väljalasetes elektroonilise aruandluse konfiguratsioonidega. |
| **Mõjutatud tootealad**         | Pearaamat                                                                           |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Kliendimakse kannete import Soome puhul

Saate valida Soome maksete puhul impordivormingu, et importida kliendimakse kanded panga esitatud välisfailist.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Maksevormingut enam ei kasutata.                                                     |
| **Asendatud teise funktsiooniga?**   | Nr Vorming asendatakse tulevastes väljalasetes ISO 20022 väljavõtte impordivormingutega. |
| **Mõjutatud tootealad**         | Müügireskontro                                                                       |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.                            |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Maksekannete importimine pearaamatu töölehele Soome puhul

Vormingut, mis on spetsiifiline Soomele, kasutatakse raamatupidamiskannete pearaamatusse importimiseks.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Maksevormingut enam ei kasutata.                                                     |
| **Asendatud teise funktsiooniga?**   | Nr Vorming asendatakse tulevastes väljalasetes ISO 20022 väljavõtte impordivormingutega. |
| **Mõjutatud tootealad**         | Müügireskontro                                                                       |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.                            |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Integratsioon Isabeliga, sünkroniseeritud (CIS) Belgia jaoks

Isabel on e-panganduse raamistik Euroopas ja de facto standard Belgias.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Integratsioon Isabeli kliendiga on katkestatud.   |
| **Asendatud teise funktsiooniga?**   | Nr Maksevormingu, mida enam ei kasutata, asendatakse Belgia ISO20022 kreeditiülekande maksevorminguga. |
| **Mõjutatud tootealad**         | Ostureskontro     |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.    |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>Modifikatsioonid kontoplaanis ja raamatupidamisreeglites Hispaania puhul

Seda funktsiooni kasutatakse Hispaani kontoplaanides ja raamatupidamisreeglites muudatuste tegemiseks. See vastendab kontod, et aidata teisendada vanu kontoplaane uuteks kontoplaanideks, ja võrdleb eelnevat finantsaastat uue finantsaastaga, isegi kui need sisestati erinevatele kontonumbritele.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Piiratud kasutus                                                  |
| **Asendatud teise funktsiooniga?**   | Ei                                                             |
| **Mõjutatud tootealad**         | Pearaamat                                                 |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata. |

### <a name="pagamento-fornittori-vendor-payment-format"></a>Pagamento Fornittori hankijamakse vorming

Itaalia pärandi maksevorming kreeditülekannetele.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Maksevormingut enam ei kasutata.                          |
| **Asendatud teise funktsiooniga?**   | Jah, ISO20022 kreeditiülekande maksevorming Itaalia puhul         |
| **Mõjutatud tootealad**         | Ostureskontro                                               |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata. |

### <a name="payment-export-formats-for-estonia"></a>Makse ekspordivorming Eesti puhul

Telehansa ja Teleservice'i vorminguid kasutatakse pangamakse ekspordi jaoks.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Maksevorminguid enam ei kasutata.                        |
| **Asendatud teise funktsiooniga?**   | Jah, ISO20022 kreeditiülekande maksevorming Eesti puhul       |
| **Mõjutatud tootealad**         | Ostureskontro                                               |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata. |

### <a name="payment-file-archive-for-norway"></a>Maksefaili arhiiv Norra puhul

Maksefailide loomisel arhiivib failiarhiiv automaatselt kõik loodavad failid, isegi varasemalt kirjutatud või loetud failid.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Asendatud teise funktsiooniga                                        |
| **Asendatud teise funktsiooniga?**   | Jah, elektroonilise aruandluse arhiivitud tööd                            |
| **Mõjutatud tootealad**         | Ostureskontro, müügireskontro, organisatsioonihaldus |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.     |

### <a name="payment-import-formats-for-estonia"></a>Makse impordivorming Eesti puhul

Telehansa ja TeleTeenuse vorminguid kasutatakse pangamakse ekspordi jaoks.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Maksevorminguid enam ei kasutata.                                                    |
| **Asendatud teise funktsiooniga?**   | Nr Vormingud asendatakse tulevastes väljalasetes ISO 20022 väljavõtte impordivormingutega. |
| **Mõjutatud tootealad**         | Müügireskontro                                                                        |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.                             |

### <a name="payroll-information-in-human-resources"></a>Palgateave inimressursside moodulis

Inimressursside palgateave

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | See funktsioon on asendatud tuumlehtedega Palk ja Inimressurssid.  |
| **Asendatud teise funktsiooniga?**   | **Soodustused**, **Tulud** ja muud seotud lehed, mis olid varem moodulis USA palk olemas, on nüüd ümber konfigureeritud ja kuuluvad inimressursside tuumkonfiguratsiooni, et aidata toetada välist palga töötlemist. Sellele funktsioonile pääseb juurde konfiguratsioonivõtmega **Inimressursid 1** \> **Palk**. |
| **Mõjutatud tootealad**         | Inimressursid, Palk   |
| **Olek**                         | Eemaldatud alates rakenduse Dynamics 365 for Operations versioonist 1611.    |

### <a name="performance-management-goal-workflow"></a>Jõudlushalduse eesmärgi töövoog

Jõudlushaldus hõlmab eesmärgihaldust ja integreerimist jõudluse ülevaadetega.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Jõudlushaldus kujundati ümber ja eesmärgi lehtede arvu vähendati, et protsessi lihtsustada.                 |
| **Asendatud teise funktsiooniga?**   | Nr Eesmärgid on nähtavad juhtidele juhi iseteeninduse portaali kaudu ja neid saab muuta ja vaadata vastav juht. |
| **Mõjutatud tootealad**         | Inimkapitali juhtimine       |
| **Olek**                         | Eemaldatud alates rakenduse Dynamics 365 for Operations versioonist 1611.    |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>Postgiroti ja Postgirot Utlandi maksevormingud Rootsi puhul

Postgiroti ja Postgirot Utlandi maksevormingud Rootsi puhul.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Maksevorminguid enam ei kasutata.                        |
| **Asendatud teise funktsiooniga?**   | Jah, ISO20022 kreeditiülekande maksevorming Rootsi puhul        |
| **Mõjutatud tootealad**         | Ostureskontro                                               |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata. |

### <a name="radio-frequency-identifier"></a>Raadiosageduse identifikaator

Raadioidentimine (RFID) on andmete kogumise tehnoloogia, mis kasutab identimisteabe talletamiseks elektroonilisi silte ja selle teabe hankimiseks otsenähtavuse olemasolu mitte eeldavat lugemisseadet.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Vähene kasutamine klientide seas ja piiratud funktsioonide kogum.   |
| **Asendatud teise funktsiooniga?**   | Ei                                              |
| **Mõjutatud tootealad**         | Varud                            |
| **Olek**                         | Eemaldatud alates rakenduse Dynamics 365 for Operations versioonist 1611. |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Aruanne riigi arvete nummerdamise kohta Läti puhul

Läti seadusandlus annab teatud reeglid müügiarvete nummerdamise kohta. Funktsioon võimaldab müügiarvetele kasutaja või kasutajagrupi põhjal spetsiifilised numbrid määrata. Seejärel saate luua aruande või XML-faili. Samuti saate printida aruande kasutatavate arvenumbrite kohta.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Riiklike arvete nummerdamist ei pea enam säilitama. Aruanne kasutatud arvenumbrite kohta ei ole enam vajalik. |
| **Asendatud teise funktsiooniga?**   | Ei       |
| **Mõjutatud tootealad**         | Müügireskontro    |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.  |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Ettevõtte juhi ja pearaamatupidaja nimede seadistamine Leedu puhul

Ettevõtte juhi ja pearaamatupidaja nimed saab määrata ettevõtte teabes ja kasutada erinevates kohaliku aruande väljaprintides.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Asendatud teise funktsiooniga                                     |
| **Asendatud teise funktsiooniga?**   | Jah, ametnike seadistamist saab kasutada samal otstarbel.   |
| **Mõjutatud tootealad**         | Ostureskontro, Müügireskontro, Sularaha- ja pangahaldus |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.  |

### <a name="shipping-carrier-interface"></a>Kättetoimetaja liides

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Topeltfunktsioon   |
| **Asendatud teise funktsiooniga?**   | Osaliselt asendatud transpordihaldusega |
| **Mõjutatud tootealad**         | Müük ja turundus, varude haldus  |
| **Olek**                         | Eemaldatud alates rakenduse Dynamics 365 for Operations versioonist 1611.  |

### <a name="telepay-payment-formats-for-norway"></a>Telepay maksevormingud Norra puhul

TelePay maksevormingud hõlmavad hankijamakse eksporti (kreeditiülekanne) ja kliendimakse kogumist (otsedeebet).

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Maksevorminguid enam ei kasutata.                                                        |
| **Asendatud teise funktsiooniga?**   | Jah, ISO20022 kreeditiülekande maksevorming ja AvtaleGiro kliendimakse vorming Norra puhul |
| **Mõjutatud tootealad**         | Müügireskontro, ostureskontro                                                          |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.                                 |

### <a name="vendor-payment-export-formats-for-finland"></a>Hankijamakse ekspordivormingud Soome puhul

Soome puhul on maksete eksportimiseks saadaval kaks vormingut. LM02 (FI) kasutatakse riigisisesteks makseteks ja LUM2 (FI) kasutatakse välismakseteks.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Maksevorminguid enam ei kasutata.                        |
| **Asendatud teise funktsiooniga?**   | Jah, ISO20022 kreeditiülekande maksevorming Soome puhul       |
| **Mõjutatud tootealad**         | Ostureskontro                                               |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata. |

### <a name="warehouse-management-ii"></a>Laohaldus II

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Laohalduse II lahendus (WMS II), mis oli saadaval moodulis **Varude haldus**, dubleerib funktsiooni, mis on olemas Dynamics AX 2012 R3-ga välja antud moodulis **Laohaldus**.                                                                         |
| **Asendatud teise funktsiooniga?**   | Moodul **Laohaldus**, mis on välja antud rakendustes AX 2012 R3, Dynamics AX 2012 R3 CU8 ja Dynamics AX 2012 R3 CU9 asendab mooduli Laohaldus II funktsioonid. Uuel moodulil on täiustatumad funktsioonid ja paindlikum laohalduse protsess kui moodulil Laohaldus II. |
| **Mõjutatud tootealad**         | Varude haldus, Müük ja turundus, Hanked   |
| **Olek**                         | Eemaldatud alates rakenduse Dynamics 365 for Operations versioonist 1611.    |

### <a name="worker-reminders-in-human-resources"></a>Töötajate meeldetuletused inimressursside moodulis

Inimressursside palgateave

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Vähene kasutus                                                           |
| **Asendatud teise funktsiooniga?**   | Ei                                                                  |
| **Mõjutatud tootealad**         | Inimressursid                                                     |
| **Olek**                         | Eemaldatud alates rakenduse Dynamics 365 for Operations versioonist 1611 |

### <a name="workflow-for-creating-goals"></a>Töövoog eesmärkide loomiseks

Töövoog töötaja eesmärkide loomise haldamiseks on üks mitmest töövoost, mis on saadaval, et aidata koordineerida jõudlushalduse protsessi.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Jõudlushaldus on rakenduses Finance and Operations täielikult ümber kujundatud.     |
| **Asendatud teise funktsiooniga?**   | Ümberkujundatud jõudlushalduse funktsioon annab rohkem kontrolli eesmärkide sisu, progressi jälgimiseks kasutatavate mõõtmiste ja lisadokumentide manustamise üle. Eesmärke saab salvestada mallidena ja seejärel taaskasutada. See funktsioon saab aidata teil kiiremini oma töötajate jaoks täiendavaid eesmärke seadistada. |
| **Mõjutatud tootealad**         | Inimkapitali juhtimine                 |
| **Olek**                         | Eemaldatud alates rakenduse Dynamics 365 for Operations versioonist 1611. |

## <a name="dynamics-ax-70"></a>Dynamics AX 7.0 


### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Võimalus hankijaarve muudatusi tühistada

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Toimivuse täiustamine        |
| **Asendatud teise funktsiooniga?**   | Ei                             |
| **Mõjutatud tootealad**         | Ostureskontro               |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0. |

### <a name="aif-axd-and-axbc-integrations"></a>AIF, AxD ja AxBC integratsioonid

Rakenduste integreerimise raamistikus (AIF) saab vahetada andmeid välissüsteemidega äriloogika kaudu, mis on näidatud teenustena. Dynamics AX sisaldab teenuseid, mis põhinevad dokumentidel ja .NET Business Connectoril (AxBC). Dokument luuakse XML-i abil. XML sisaldab päiseteavet, mis lisatakse *sõnumi* loomiseks, mille saab Dynamics AX-i või sealt välja saata. Dokumentide näites on müügitellimused ja ostutellimused. Kuid peaaegu igasugune üksus (nt klient) võib olla kajastatud dokumendiga. Dokumentidel põhinevad teenused kasutavad klasse **Axd \<Dokument\>**.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | AIF-i ja AxDs-i arhitektuuri ei saanud pilveteenusesse skaleerida. Hulgiimpordiga oli seotud jõudlusprobleeme.                                        |
| **Asendatud teise funktsiooniga?**   | See funktsioon on asendatud andmete importimise/eksportimise raamistikuga, mis toetab korduvat hulgiimportimist/eksportimist. AxBC puhul soovitame kasutada tegelikke tabeleid. |
| **Mõjutatud tootealad**         | AxDs, AxBCs ja AIF   |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.   |

### <a name="billing-code-rate-scripts"></a>Arvelduskoodi kursiskriptid

Arveldusskripte kasutati arvekoodide jaoks arvelduskursside arvutamiseks. Need skriptid on vajalikud kohandatud arenduseks programmeerimiskeeles C Sharp või Visual Basic. Dynamics AX-i praeguses veebis **arvelduskoodi kursiskripte** ei toetata.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Kohandatud C Sharpi või Visual Basicu kohandatud skriptide tuge rakendusse Dynamics AX 7.0 ei lisatud. |
| **Asendatud teise funktsiooniga?**   | Ei                                                                                      |
| **Mõjutatud tootealad**         | Avalik sektor, müügireskontrod                                    |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.                                                          |

### <a name="boms-without-bom-versions"></a>Kooslused ilma koosluse versioonideta

Kui konfiguratsioonivõti **Koosluse versioonid** keelati, peideti koosluse versioonid kõigil vormidel ja süsteem sundis väljastatud toodete ja koosluste vahele 1:1 seose. Praeguses Dynamics AX-i versioonis ei saa konfiguratsioonivõtit **Koosluse versioonid** keelata.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Konfiguratsioonivõtme kasutamist koosluse versioonide juhtimiseks ei saa pilvekeskkonnas skaleerida. |
| **Asendatud teise funktsiooniga?**   | Ei                                                                                      |
| **Mõjutatud tootealad**         | Tooteteabe haldus, Laohaldus                                    |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.                                                          |

### <a name="brazilian-bordero"></a>Brasiilia Bordero

Spetsiifiline maksemeetod Braziilia ettevõtetele

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Tugi Brasiilia Bordero maksemeetodile on katkestatud Brasiilia lokalisatsioonist |
| **Asendatud teise funktsiooniga?**   | Ei   |
| **Mõjutatud tootealad**         | Ostureskontro   |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata. |

### <a name="brazilian-sintegra-statement"></a>Brasiilia Sintegra avaldus

Föderaalmaksu avaldus ICMS maksule

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | See avaldus ei ole enam kohaldatav mõnedes Brasiilia osariikides. |
| **Asendatud teise funktsiooniga?**   | Nr Kasutajad saavad kasutada üldist elektroonilist aruandlustööriista, et konfigureerida avaldust vastavalt konkreetsele olukorrale. |
| **Mõjutatud tootealad**         | Finantsraamatud    |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.   |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>Brasiilia SCAN-i ettenägematute kulude režiim NF-e puhul

(SCAN) ettenägematute kulude keskkonda kasutatakse Nota Fiscal eletrônica (NF-e) oleku loomiseks, eksportimiseks ja importimiseks, kui Secretaria da Fazenda (SEFAZ) keskkond ei ole saadaval.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | See ettenägematute kulude meetod ei ole enam kohaldatav kõikides Brasiilia osariikides |
| **Asendatud teise funktsiooniga?**   | Ei                                                                          |
| **Mõjutatud tootealad**         | Müügireskontro                                                         |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.              |

### <a name="business-analyzer"></a>Majandusanalüüs

See mobiilirakendus võimaldab kasutajatel ettevõtte võtmemõõdikuid üle vaadata.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | See funktsioon on asendatud teise funktsiooniga.   |
| **Asendatud teise funktsiooniga?**   | Microsoft Power BI sisupakett Finantsnäitajate jälgimine sisaldab rahalisi võtmemõõdikuid, mis olid varem saadaval Business Analyzeris. |
| **Mõjutatud tootealad**         | Pearaamat      |
| **Olek**                         | Aegunud: Business Analyzeri kasutamine on aegunud.    |

### <a name="business-statistics"></a>Äristatistika

Äristatistika päringute seadistamine, mis aitavad analüüsida organisatsiooni jõudlust

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Vananenud lähenemine äriteabele, vähene kasutamine ja piiratud funktsioonide kogum |
| **Asendatud teise funktsiooniga?**   | Uued äriteabe lahendused praegusele Dynamics AX-i versioonile                                      |
| **Mõjutatud tootealad**         | Hanked, Ostureskontro, Müük ja turundus, Müügireskontro         |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.                                                               |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Dokumendi kuupäeva muutmise funktsioon arve kinnitamise töölehel

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Vähene kasutus                                                               |
| **Asendatud teise funktsiooniga?**   | Jah. Sisestatud hankija kande dokumendi kuupäeva saab muuta. |
| **Mõjutatud tootealad**         | Ostureskontro                                                        |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.                                          |

### <a name="clieop03-payment-format-for-the-netherlands"></a>Hollandi maksevorming ClieOp03

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | See vorming ei kehti enam Hollandis, kuna see on asendatud SEPA funktsiooniga. |
| **Asendatud teise funktsiooniga?**   | SEPA maksete eksport  |
| **Mõjutatud tootealad**         | Kõik moodulid     |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.   |

### <a name="compliance-center"></a>Vastavuskeskus

Vastavuskeskus oli ettevõtteportaali sait dokumentide nõuete haldamiseks Sarbanes-Oxley seadusega seotud vastavusalgatuste puhul.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Kliendid ei kasuta. Microsoft SharePoint sisaldab sama võimalust, mis oli saadaval vastavuskeskuses. |
| **Asendatud teise funktsiooniga?**   | Ei   |
| **Mõjutatud tootealad**         | Vastavuse ja sisekontrollid  |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.    |

### <a name="connector-for-microsoft-dynamics"></a>Microsoft Dynamicsi konnektor

Seda tööriista kasutati võtmeandmete integreerimiseks Microsoft Dynamics CRM-ist Dynamics ERP rakendustesse.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | See funktsioon on asendatud teise funktsiooniga. |
| **Asendatud teise funktsiooniga?**   | Common data service                                      |
| **Mõjutatud tootealad**         | Dynamics -i konnektor                         |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.                           |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Konteineriüksus ja mitmedimensiooniline laoseis

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Topeltfunktsioon |
| **Asendatud teise funktsiooniga?**   | Jah. Alates versioonist AX 2012 on see funktsioon asendatud konsolideeritud partii tellimuste funktsioonikogumiga. See funktsioon sisaldab konsolideeritud laoseisu vaadet. |
| **Mõjutatud tootealad**         | Tooteteabe haldus, Tootmise juhtimine, Varude haldus, Müük ja turundus  |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0. |

### <a name="cue-group-metadata"></a>Vihjegrupi metaandmed

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Vihjegruppe kasutati kiirinfo alal ühe või mitme vihje kuvamiseks. Selle kasutamine oli piiratud ja oli ka jõudlusprobleeme, kuna kirje muutmine põhivormil põhjustas vihjegrupis ühe päringu vihje kohta. |
| **Asendatud teise funktsiooniga?**   | Ei      |
| **Mõjutatud tootealad**         | Kõik moodulid    |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.  |

### <a name="cue-metadata"></a>Vihje metaandmed

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Vihje metaandmed olid piiratud arvu või summa teabega.    |
| **Asendatud teise funktsiooniga?**   | Modelleerimisel paindlikkuse lisamiseks võeti kasutusele paani metaandmed. Näiteks saate modelleerida praegusi arve, navigeerimist ja tulemuslikkuse võtmenäitajaid (KPI-sid). Arvu paani metaandmed on vihje metaandmete otsene asendus. |
| **Mõjutatud tootealad**         | Kõik moodulid           |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0      |

### <a name="danish-check-format"></a>Taani tšekivorming

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Taani tšekikavandi vormingu tugi on lõpetatud ja aruanne on DK lokaliseerimisest eemaldatud. |
| **Asendatud teise funktsiooniga?**   | Ei    |
| **Mõjutatud tootealad**         | Kõik moodulid    |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.  |

### <a name="data-partitions"></a>Andmesektsioonid

Andmesektsioonid tagavad andmete loogilise eraldamise Dynamicsi AX andmebaasis.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Dynamics AX 2012 R2-s võeti andmete eraldamise võimaldamiseks kasutusele andmesektsioonid. Tavastsenaariumi puhul on ettevõttel tütarettevõtted ja ühe tütarettevõtte andmed ei tohiks olla teisele tütarettevõttele näha, kuigi mõlemaid tütarettevõtteid haldab sama IT-osakond. Kuid uute sektsioonide loomiseks ja nende täitmiseks andmetega ning sektsiooni andmete varundamiseks oli vaja kogu programmis lisaskripte ja halduse üldkulusid. Pilves, kus meil on juurdepääs platvormi teenusena (PaaS) andmebaasiteenustele (Microsoft Azure SQL-i andmebaas) on palju tõhusam kasutada andmebaasi eralduskonteinerina, kui teha eraldamine programmis. Olenemata sellest, kas andmete eraldamine on vajalik tütarettevõtetele, mitmele rentnikule või lihtsalt skaalale, usume, et neid stsenaariume saab käsitleda paremini rakenduse Finance and Operations mitme eksemplari kaudu. |
| **Asendatud teise funktsiooniga?**   | Andmesektsioone kasutavad kliendid peavad kasutama rakenduse Finance and Operations mitut eksemplari, kui andmebaasi taseme eraldamine on kriitiline probleem.    |
| **Mõjutatud tootealad**         | Kõik moodulid  |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.  |


### <a name="database-and-file-share-storage-for-attachments"></a>Andmebaas ja ühine failiketas manuste jaoks

Dynamics AX 2012 lubas manuste talletamist andmebaasis ja failiketastel. Kumbagi neist valikutest enam ei toetata.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Ühist failiketast enam ei toetata, kuna pilve majutatud keskkonnad ei saa kohalike failiketastega suhelda. Andmebaasi talletamine on Azure’i bloobimälu kasuks taunitud. Azure’i bloobimälu on andmebaasis talletamisega samaväärne, kuna dokumentidele pääseb juurde ainult rakenduse Finance and Operations kliendivormide kaudu. See pakub lisaeelist talletusruumi pakkumisel, mis ei mõjuta negatiivselt andmebaasi jõudlust. Bloobimälu on dokumendihalduse vaiketalletusmehhanism ja toimib viivitamatult. |
| **Asendatud teise funktsiooniga?**   | Andmebaasi talletamine on Azure’i bloobimälu kasuks taunitud.   |
| **Mõjutatud tootealad**         | Kõik moodulid  |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.   |

### <a name="delimitation"></a>Eraldamine

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Funktsiooni ei leidnud kasutamist. |
| **Asendatud teise funktsiooniga?**   | Ei                                     |
| **Mõjutatud tootealad**         | Tööajaarvestus                    |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.         |

### <a name="desktop-client"></a>Töölauaklient

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Dynamics AX-i kliendikogemus on ümber kujundatud, et parandada kasutatavust mitme platvormi ja seadme lõikes.                      |
| **Asendatud teise funktsiooniga?**   | Uus veebiklient põhineb töölauavormi metaandmetel ja programmeerimismudelil, mida on muudetud rikkaliku veebiplatvormi pakkumiseks. |
| **Mõjutatud tootealad**         | Kõik moodulid  |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.   |

### <a name="direct-database-connection"></a>Andmebaasi otseühendus

Dynamics AX 2012 R3-s sai Retail Modern POS luua kanali andmebaasiga otse ühenduse samamoodi nagu ettevõtte kassaga. See täiendas Retail Modern POS-i standardset sidepidamisviisi jaemüügiserveri kaudu.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Andmebaasi otseühenduvus nõudis madalamaid turbeprotokolle ja seda kasutati peamiselt kõrgeima jõudluse saavutamiseks. Finance and Operationsi jõudlus- ja turbetäiustuste tõttu põhjustab see funktsioon nüüd rohkem probleeme kui lahendab. |
| **Asendatud teise funktsiooniga?**   | Nr Nüüd toetatakse ainult standardset jaemüügiserveri sidet.  |
| **Mõjutatud tootealad**         | Kanali andmebaas / Retail Modern POS   |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.  |

### <a name="dutch-swift-mt940"></a>Hollandi SWIFT MT940

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Lokaliseeritud funktsiooni asemel kasutatakse nüüd üldist funktsiooni.                    |
| **Asendatud teise funktsiooniga?**   | Jah, see funktsioon on asendatud pangakonto täpsema vastavusseviimise funktsiooniga. |
| **Mõjutatud tootealad**         | Kõik moodulid                                                                              |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.                           |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (Saksamaal XBRL)

See funktsioon andis keele eXtensible Business Reporting Language (XBRL) väljundi, mis on mõeldud spetsiaalselt Saksamaa rakenduse eBilanz taksonoomia jaoks.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Kliendid ei kasuta  |
| **Asendatud teise funktsiooniga?**   | Seda funktsiooni pole asendatud teise funktsiooniga, kuid Saksamaa turul on saadaval mitu spetsiaalset XBRL-i paketti, mis pakuvad rikkalikult XBRL-i funktsioone. |
| **Mõjutatud tootealad**         | Management Reporter      |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.  |

### <a name="enterprise-portal-client"></a>Ettevõtteportaali klient

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Pakutakse ühe kliendi platvormi.  |
| **Asendatud teise funktsiooniga?**   | Uus veebiklient põhineb töölauavormi metaandmetel ja programmeerimismudelil, mida on muudetud rikkaliku veebiplatvormi pakkumiseks. |
| **Mõjutatud tootealad**         | Kõik moodulid  |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.   |

### <a name="environmental-sustainability"></a>Keskkonna jätkusuutlikkus

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Vähene kasutamine klientide seas ja piiratud funktsioonide kogum  |
| **Asendatud teise funktsiooniga?**   | Ei              |
| **Mõjutatud tootealad**         | Vastavus ja sisekontroll, Ostureskontro  |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0. |

### <a name="form-activex-and-managed-host-controls"></a>Vormi ActiveX ja Hallatud host juhtelemendid

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | ActiveX-i ja hallatud hosti juhtelemendid põhinevad kasutuselt eemaldatud töölauakliendil. |
| **Asendatud teise funktsiooniga?**   | Laiendatav juhtimisraamistik toetab uusi HTML-il, CSS-il ja JavaScriptil põhinevaid juhtelemente ning on Microsoft Visual Studio tööriistakeskkonnas esmaklassiline juhtelement. |
| **Mõjutatud tootealad**         | Kõik moodulid     |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.       |

### <a name="generate-prenotes-by-using-a-batch"></a>Eelpäringute loomine partii abil

Eelpäringu loomine pole partii abil võimalik, kuid kasutaja saab seda siiski teha.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Saadud eelpäringu faili säilitamiseks ja kuvamiseks partii abil loomisel pole ühtegi vormi. |
| **Asendatud teise funktsiooniga?**   | Eelpäringuid saab siiski koostada ja kasutaja saab määrata faili salvestamise kohta.   |
| **Mõjutatud tootealad**         | Ostureskontro, Müügireskontro, Sularaha- ja pangahaldus  |
| **Olek**                         | Eemaldatud alates rakenduse AX versioonist 7.0.    |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Saksa DTAUS-makse eksportimine ja konto väljavõtte importimine (kogusummad ja kanded)

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | See vorming ei kehti enam Saksamaal, kuna see on asendatud ühtse euromaksete piirkonna (SEPA) funktsiooniga.                    |
| **Asendatud teise funktsiooniga?**   | Jah, selle funktsiooni on asendanud SEPA maksete eksportimine ja täiustatud panga vastavusseviimise funktsioon kontoväljavõtete importimiseks. |
| **Mõjutatud tootealad**         | Kõik moodulid  |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata. |

### <a name="german-dtazv-payment-format"></a>Saksamaa DTAZV maksevorming

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | See vorming ei kehti enam Saksamaal, kuna see on asendatud SEPA funktsiooniga. |
| **Asendatud teise funktsiooniga?**   | SEPA maksete eksport    |
| **Mõjutatud tootealad**         | Kõik moodulid   |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.    |

### <a name="german-mt940-import"></a>Saksa MT940 importimine

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Lokaliseeritud funktsiooni asemel kasutatakse nüüd üldist funktsiooni.                    |
| **Asendatud teise funktsiooniga?**   | Jah, see funktsioon on asendatud pangakonto täpsema vastavusseviimise funktsiooniga. |
| **Mõjutatud tootealad**         | Kõik moodulid                                                                              |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.                           |

### <a name="german-xml-eu-sales-list"></a>Saksamaa XML EL-i käibearuanne

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Saksa EL-i müügiloendi aruandluses XML-vormingut enam ei toetata. Saksa maksuametile EL-i müügiloendi aruande edastamiseks saab kasutada ainult ELMA5 tekstifaili vormingut. |
| **Asendatud teise funktsiooniga?**   | Ei         |
| **Mõjutatud tootealad**         | Maks        |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.   |

### <a name="gl-ssrs-reports"></a>GL SSRS-i aruanded

Järgmisi menüüelemente sisaldavad aruanded on eemaldatud. **Proovibilansi kokkuvõte**, **Üksikasjalik proovibilanss**, **Kontoplaan**, **Auditijälg**, **Saldod** ja **Saldoloend**.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Microsoft SQL Serveri teenuste Reporting Services (SSRS) finantsaruanded on asendatud Management Reporteri võimaluste ja vaikearuannetega. |
| **Asendatud teise funktsiooniga?**   | Management Reporter (selles Dynamics AX-i versioonis nimega **Finantsaruandlus**)    |
| **Mõjutatud tootealad**         | Pearaamat   |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.   |

### <a name="infopart-and-formpart-metadata"></a>Parameetrite InfoPart ja FormPart metaandmed

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Parameetrite InfoPart ja FormPart metaandmed lubasid kahe kliendi kiirinfo loomise. |
| **Asendatud teise funktsiooniga?**   | Parameetri InfoPart metaandmed, mis oli lihtsustatud vormidefinitsioon, on versioonitäienduse tööriistadega vormiks teisendatud. Parameetri FormPart metaandmed, mis viitasid vormile, on asendatud otsesema viitega, mis on loodud versioonitäienduse tööriistadega. |
| **Mõjutatud tootealad**         | Kõik moodulid    |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.        |

### <a name="main-account-list-page"></a>Põhikonto loendileht

Juriidilise isiku kontode loend ja seotud saldoteave

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Saldoteave on saadaval loendilehel **Proovibilanss** kontode ja dimensioonide kaupa.  |
| **Asendatud teise funktsiooniga?**   | Leht **Põhikontod** sisaldab sama kontoloendit, mis loendileht **Põhikonto**. Ruudustikuvaade lehel **Põhikontod** näitab ka veelgi väiksemat ruudustikulaadset vaadet. |
| **Mõjutatud tootealad**         | Pearaamat      |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.    |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Malaisia ja Singapuri panga rahavooaruanne

See funktsioon võimaldab kasutajal printida rahavoo aruande, mis näitab valitud pangakontode sularaha sissetuleku ja väljamineku kandeid ja üksikasju konkreetse kuupäevavahemiku jooksul.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Sama teavet saab pangakande päringu kaudu. |
| **Asendatud teise funktsiooniga?**   | Pangakande päring                                            |
| **Mõjutatud tootealad**         | Sularaha- ja pangahaldus                                                |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata.          |

### <a name="mexican-cfd-electronic-invoice"></a>Mehhiko CFD elektrooniline arve

See funktsioon lubas Mehhiko elektrooniliste arvete loomise, kasutades meetodit Comprobante Fiscal Digital (CFD), kus ettevõte allkirjastab arve, küsides valitsuselt vajalikku kinnitust. See funktsioon pakub ka igakuist aruannet, mis sisaldab kõiki perioodi jooksul väljastatud elektroonilisi arveid.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Seda meetodit ei rakendata enam. Maksuasutused eemaldasid kasutuselt elektrooniliste arvete koostamise meetodiga CFD ja asendasid selle meetodiga Comprobante Fiscal Digital a través de Internet (CFDI), kus allkirjastamine on delegeeritud muust osapoolest teenusepakkujale (PAC). Igakuine aruanne on eemaldatud ja päringu valik võimaldab kasutajatel varasemate kannete kohta päringuid esitada. |
| **Asendatud teise funktsiooniga?**   | Ei    |
| **Mõjutatud tootealad**         | Konto võlgnevused, Projekt   |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata. |

### <a name="mexico-realized-and-unrealized-vat"></a>Mehhiko realiseeritud ja realiseerimata käibemaks

Dynamics AX 2012 haldas realiseerimata käibemaksu (KM), kasutades Mehhiko kohaseid realiseerimata maksu funktsioone.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Topeltfunktsioon  |
| **Asendatud teise funktsiooniga?**   | Jah, see funktsioon on asendatud standardse tingimusliku käibemaksu tuumfunktsiooniga. |
| **Mõjutatud tootealad**         | Maks   |
| **Olek**                         | Aegunud: selle funktsiooni eemaldamiskuupäev on määramata. |

### <a name="microsoft-outlook-integration"></a>Microsoft Outlook integratsioon


|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | See funktsioon on asendatud Microsoft Exchange Serveri integratsiooniga. |
| **Asendatud teise funktsiooniga?**   | Jah                                                                            |
| **Mõjutatud tootealad**         | Müük ja turundus                                                            |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.                                                 |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Varude ja laohalduse töölehtede privaatne blokeerimine

Varude ja laohalduse töölehed ei toeta enam võimalust märkida tööleht valitud kasutaja puhul privaatseks. Töölehtede privaatsena blokeerimise protsessi toetatakse ainult kasutajagruppide puhul ja redigeerimise ajal.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Funktsiooni ei leidnud kasutamist. |
| **Asendatud teise funktsiooniga?**   | Ei                                     |
| **Mõjutatud tootealad**         | Varud                   |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.         |

### <a name="product-builder"></a>Tootekonstruktor

Tootekonstruktorit kasutati müügitellimuse, ostutellimuse, tootmistellimuse, müügipakkumise, projektipakkumise või kaubavajaduse üksuste dünaamiliseks konfigureerimiseks. Modelleerimise muutujatega tootemudeli põhjal sai kasutaja valida väärtusi kliendi nõudmiste täitmiseks ja kordumatu tootevariandi saamiseks, millel oli kooslus ja protsess.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Tootekonstruktor avaldas X++ koodi lõppkasutajatele ja Dynamics AX-i praeguses versioonis seda ei toetata. See on eemaldatud kattuvate suurte koodibaaside haldamisel dubleerimise vältimiseks.  |
| **Asendatud teise funktsiooniga?**   | Jah. Rakenduses Dynamics AX 2012, kus tootekonstruktori tulevaste versioonide aegumine oli juba välja kuulutatud, võeti kasutusele piirangupõhine konfiguratsioon. Konfiguratsiooni lubamiseks valitakse tooteetalonides piirangupõhise konfiguratsiooni tehnoloogia. Lisateabe saamiseks vt teemat [Toote konfiguratsioonimudeli koostamine](../../supply-chain/pim/build-product-configuration-model.md). |
| **Mõjutatud tootealad**         | Tooteteabe haldus, Müük ja turundus  |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.      |

### <a name="production-floor-app"></a>Tootmisosakonna rakendus
See rakendus on mõeldud tahvelarvutitele, milles töötab Windows 8.1 RT ja Windows 8.1 Pro.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Tänu üleminekule veebipõhisele kliendile saab Dynamics AX 7.0 omakliendi kaudu pakkuda sarnast funktsionaalsust. Töökaardi vahend annab tootmisosakonna kasutajaliidese, mis on optimeeritud puute ja tahvelarvuti vormitegurite jaoks. |
| **Asendatud teise funktsiooniga?**   | Jah. Töökaardi vahend, mis on Dynamics AX 7.0 omaosa.                                                                           |
| **Mõjutatud tootealad**         | Tootmise juhtimine                                                |
| **Olek**                         | Aegunud: selle funktsiooni jaoks pole veel määratud Microsoft Store’ist eemaldamise kuupäeva.                                                |


### <a name="rename-product-dimension"></a>Nimetage tootedimensioon ümber.

Selle funktsiooni abil saate määrata ühe toote standarddimensiooni (suuruse, värvi või stiili) nimeks teie ärivajadustele paremini vastava nime. Ümbernimetamine hõlmas kõiki silte, millel tootedimensiooni nime kasutati.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Dynamics AX-i praegune versioon ei toeta käitusajal siltide muutmist. |
| **Asendatud teise funktsiooniga?**   | Ei                                                                            |
| **Mõjutatud tootealad**         | Tooteteabe haldus                                                |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.                                                |

### <a name="retail-server-connectivity-using-http"></a>Jaemüügiserveri ühenduvus HTTP abil

Dynamics AX 2012 R3-s toimis jaemüügiserveri funktsioon HTTP-sidet (mitteturvalist) kasutades. See täiendas standardset sidet HTTP-si kaudu.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Uute turbenõuete tõttu toetatakse nüüd ainult turvalist sidet, kasutades TLS 1.2 (või uuemat, kui on saadaval). Iseteeninduslik installiprogramm konfigureerib arvuti selle side jaoks automaatselt. |
| **Asendatud teise funktsiooniga?**   | Nr Nüüd toetatakse ainult standardset HTTP-sidet. |
| **Mõjutatud tootealad**         | Jaemüügiserver  |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0. |

### <a name="role-center-pages"></a>Rollikeskuse leheküljed

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Rollikeskuse lehed loodi ettevõtteportaali aegunud platvormile, mis on Dynamics AX-i praeguses versioonis asendatud uue veebikliendi platvormiga. |
| **Asendatud teise funktsiooniga?**   | Uus tööruumi vormi struktuur pakub kasutajatele protsessikeskset kujundust, mis annab sageli kasutatavatele toimingutele hõlpsa juurdepääsu.                       |
| **Mõjutatud tootealad**         | Kõik moodulid    |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0   |

### <a name="sales-tax-jurisdictions"></a>Käibemaksu jurisdiktsioonid

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Vähene kasutamine klientide seas ja piiratud funktsioonide kogum |
| **Asendatud teise funktsiooniga?**   | Ei                                           |
| **Mõjutatud tootealad**         | USA käibemaks                                 |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.               |

### <a name="sites-services"></a>Sites Services

Sites Services võimaldab luua veebisaite, mis laiendavad äriprotsessid Internetti ilma IT-toeta.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Dynamics AX-i kasutataval Microsoft Azure’i taristul on uusi funktsioone, mida saab selle asemel kasutada (näiteks Azure’i saidid). |
| **Asendatud teise funktsiooniga?**   | Ei   |
| **Mõjutatud tootealad**         | Tööruumid Inimressursside värbamine, Juhtumihaldus, Pakkumiskutsed, Hankija registreerimine, Koostöö müügivõimaluste ja kampaaniate jaoks  |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.    |

### <a name="ssas-demand-forecasting-strategy"></a>SSAS-i nõudluse prognoosi strateegia

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Uues pilvarhitektuuris ei toetata selle funktsiooni kujundust. |
| **Asendatud teise funktsiooniga?**   | Teenuse Azure Machine Learning nõudluse prognoosi strateegia                           |
| **Mõjutatud tootealad**         | Koondplaneerimine                                                              |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.                                               |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Hankija arve kaust ilma sisestamise üksikasjadeta

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Vähene kasutus. See funktsioon on asendatud arve töölehega, millel on töövoo funktsioon. |
| **Asendatud teise funktsiooniga?**   | Arve töölehe töövoo võimalused.     |
| **Mõjutatud tootealad**         | Ostureskontro |
| **Olek**                         | Eemaldatud alates rakendusest Dynamics AX 7.0.    |


### <a name="virtual-company-accounts"></a>Virtuaalsed ettevõtted

Virtuaalettevõtete funktsiooni ei toetata enam Dynamics AX-is. Virtuaalettevõtete funktsioon võimaldab kasutajatel seadistada ettevõtete kogumis jagatavaid tabeleid. Funktsiooni kirjelduse leiate siit: [Ettevõtete ja virtuaalettevõtete kontod](https://msdn.microsoft.com/library/aa834382(v=ax.10).aspx). See funktsioon rühmitab tabelid kogumitesse, mis on määratud virtuaalsetele ettevõtetele, mis on olemasolevate „tõeliste” ettevõtete grupid. Päringud koostatakse nii, et kõik virtuaalse ettevõtte ettevõtted pääsevad seotud tabelikogumites olevate tabelite andmetele juurde.

|   |  | 
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | - Enne andmete salvestamist tabelitesse tuleb seadistada virtuaalsed ettevõtted. Virtuaalsete ettevõtete paigutamine olemasolevasse süsteemi on väga raske.<br><br>- Kuna Dynamics AX-i praeguses versioonis on nii palju andmeid normaliseeritud, on väga raske teada, mida tabelikogumitesse lisada. Näiteks on raske teada, milliseid tabeleid jagada. Kõik tabelid, millele virtuaalses ettevõttes olevad tabelid viitavad, tuleb samuti lisada. Tabeli normaliseerimise tõttu peavad isegi mitmesse tabelisse jaotatud lihtsad koondandmed olema virtuaalse ettevõtte osa. Mis tahes siin tehtud viga põhjustab funktsionaalseid probleeme.<br><br>- Kui tabel on virtuaalettevõtte osa, kaotab see andmete päritolu andmed ja salvestatakse ainult virtuaalne ettevõte.   |
| **Asendatud teise funktsiooniga?** | Selleks, et teha tabelid kättesaadavaks kõigi ettevõtete juurest, võib kasutada üldtabeleid. Praegu asendusi ei ole. |   
| **Mõjutatud tootealad**       | Kõik moodulid |   
| **Olek**                       | Eemaldatud alates rakendusest Dynamics AX 7.0.   |   

### <a name="windows-8-tablet-app"></a>Windows 8 tahvelarvuti rakendus

Windows 8 tahvelarvuti rakendus pakkus kulude sisestamise ja kinnitamise funktsioone.

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Finance and Operations ühildub tahvelarvutitega. Tahvelarvuti rakendust pole enam vaja.    |
| **Asendatud teise funktsiooniga?**   | Nr          |
| **Mõjutatud tootealad**         | Kulude haldus   |
| **Olek**                         | Eemaldatud: see funktsioon on saadaval ainult rakendusele Dynamics AX 2012 R3. |

### <a name="workplanner"></a>Tööplaanija

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Vähene kasutus |
| **Asendatud teise funktsiooniga?**   | Ei, kuid leht **Reeglite suhe**, mis avaneb lehelt **Reegligrupid**, toetab sama äristsenaariumi kui mittesoovitatav leht **Tööplaanija**. |
| **Mõjutatud tootealad**         | Tööajaarvestus     |
| **Olek**                         | Koodi ei eemaldatud Vormi JmgWorkPlanner siiski ei migreeritud.    |

### <a name="x-financial-statements"></a>X++ finantsaruanded

|                                                 |                                                                                                          |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <strong>Aegumise/eemaldamise põhjus</strong> |                         See funktsioon on asendatud teise funktsiooniga.                         |
|  <strong>Asendatud teise funktsiooniga?</strong>  | Management Reporter (selles Dynamics AX-i versioonis nimega <strong>Finantsaruandlus</strong>) |
|     <strong>Mõjutatud tootealad</strong>     |                                              Pearaamat                                              |
|             <strong>Olek</strong>             |                                      Eemaldatud alates rakendusest Dynamics AX 2012                                      |

