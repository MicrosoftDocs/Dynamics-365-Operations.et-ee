---
title: Eemaldatud või aegunud platvormi funktsioonid
description: See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Finance and Operationsi rakenduste platvormi uuendustest.
author: sericks007
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 0065f5c101237de49ae362ecd3378ec5046dbf4b
ms.sourcegitcommit: c4500b626667185643b3a2e7fc3a004d42198d07
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/29/2021
ms.locfileid: "7725045"
---
# <a name="removed-or-deprecated-platform-features"></a>Eemaldatud või aegunud platvormi funktsioonid

[!include [banner](../includes/banner.md)]

See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Finance and Operationsi rakenduste platvormi uuendustest.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

See loend peaks aitama teil neid eemaldusi ja aegumisi oma plaanides arvesse võtta. 

Üksikasjalikku teavet rakenduse Finance and Operationsi rakenduste objektide kohta leiate teemast [Tehnilise teabe aruanded](/dynamics/s-e/global/axtechrefrep_61). Saate võrrelda nende aruannete eri versioone, et õppida objektide kohta, mida on igas Finance and Operationsi rakenduste versioonis muudetud või eemaldatud.

## <a name="feature-removal-effective-october-2021"></a>Funktsiooni eemaldamine jõustub 2021. aasta oktoobris

### <a name="microsoft-azure-sql-reports-in-lifecycle-services-lcs"></a>Microsoft Azure Lifecycle Services’i (LCS) SQL aruanded

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Kõik tegevused ja seire viiakse läbi sisemiselt, platvormi kaudu, automatiseerimise abil. See ei nõua käsitsi sekkumist.|
| **Asendatud teise funktsiooniga?**   | Jah, nüüd on olemas automatiseeritud süsteem, mis renderdab need võimalused aegunuks. |
| **Mõjutatud tootealad**         | SQL-i aruanded: praegune DTU, praeguse DTU üksikasjad, lukustamise üksikasjad, praeguse plaani juhendi loend, päringu ID-de loendi toomine, SQL-i päringuplaani toomine antud plaani ID jaoks, päringuplaanide ja käivitamise oleku toomine, konfiguratsiooni saamine, oota statistikat, kõige kallimate päringute loend |
| **Juurutamissuvand**              | Pilve juurutamine: Mõjutab Microsoft`i hallatud tootmiskeskkondi ja liivakastikeskkondi kihist 2 kuni kihini 5. |
| **Olek**                         | Eemaldatud |

### <a name="azure-sql-actions-in-lcs"></a>Azure SQL-i tegevused LCS-is

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Mõned SQL-aruanded LCS-s aeguvad. Kõik tegevused ja seire viiakse läbi sisemiselt, platvormi kaudu, automatiseerimise abil. See ei nõua käsitsi sekkumist. |
| **Asendatud teise funktsiooniga?**   | Jah, nüüd on olemas automatiseeritud süsteem, mis renderdab need võimalused aegunuks. |
| **Mõjutatud tootealad**         | SQL-i tegevused: plaanijuhendi loomine, et sundida plaani ID-d, luua plaanijuhend tabeli vihjete lisamiseks, plaani juhendi eemaldamine, lehelukkude keelamine/lukustamine ja lukustamise eskalatsioon, tabeli statistika värskendamine, indeksi uuesti loomine, indeksi loomine |
| **Juurutamissuvand**              | Pilve juurutamine: Mõjutab Microsoft`i hallatud tootmiskeskkondi ja liivakastikeskkondi kihist 2 kuni kihini 5. |
| **Olek**                         | Eemaldatud |


## <a name="feature-deprecation-effective-october-2021"></a>Funktsiooni tugi lõpetatakse 2021. aasta oktoobris

### <a name="show-related-document-attachments-feature"></a>Funktsioon "Kuva seotud dokumendimanused".

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Funktsioon andis ootamatuid tulemusi. |
| **Asendatud teise funktsiooniga?**   | Ei. Kõik selle funktsiooniga seotud edasised plaanid edastatakse meie standardse väljalaskelaine avalikustamisprotsessi kaudu. |
| **Mõjutatud tootealad**         | Veebiklient – ​​dokumentide manustamise kogemus |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud  |

## <a name="platform-updates-for-version-10023-of-finance-and-operations-apps"></a>Rakenduste Finance and Operations Platformi versiooni 10.0.23 värskendused

### <a name="ondbsynchronize-event"></a>OnDBSynchronize üritus

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Selle sündmuse läbiviimiseks puudub kontroll. |
| **Asendatud teise funktsiooniga?**   | Jah, teisaldage sündmusega **OnDBSynchronzie** tellitud olemasolevad meetodid SysSetupi laiendatud klassi. |
| **Mõjutatud tootealad**         | Andmebaasi sünkroonimine |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud. Planeeritud kolimiskuupäev on oktoober 2022. |


### <a name="systemnotificationsmanageraddnotification-api"></a>SystemNotificationsManager.AddNotification API

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Microsoft nõuab teatiste lisamisel täiendavaid parameetreid. |
| **Asendatud teise funktsiooniga?**   | Jah, API **SystemNotificationsManager.AddSystemNotification()**. See API nõuab loodud teatiste jaoks ExpirationDateTime ja RuleID selgesõnalist määramist. |
| **Mõjutatud tootealad**         | Veebiklient |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud. Planeeritud kolimiskuupäev on aprill 2023. |

## <a name="platform-updates-for-version-10021-of-finance-and-operations-apps"></a>Rakenduste Finance and Operations Platformi versiooni 10.0.21 värskendused

### <a name="skype-for-business-online-support"></a>Skype'i ärirakenduse veebiväljaande tugi

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Skype'i ärirakenduse veebiväljaanne on käibelt kõrvaldatud. Lisateabe saamiseks vaadake, [Skype'i ärirakenduse veebiväljaanne on käibelt kõrvaldatud](https://techcommunity.microsoft.com/t5/microsoft-teams-blog/the-skype-for-business-online-service-has-retired/ba-p/2596601). |
| **Asendatud teise funktsiooniga?**   | Praegu mitte, ehkki võime edaspidi kaaluda Teams'i kohaloleku lisamist.|
| **Mõjutatud tootealad**         | Veebiklient |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud. **Skype on lubatud** säte on välja lülitatud alates väljalaskest 10.0.21. Selle sätte eemaldamise eesmärk on 2022. aasta aprilliks. Kuid funktsioon lõpetab töö pärast seda, kui Skype töörühm on teenuse sulgenud. |
 
## <a name="feature-deprecation-effective-august-2021"></a>Funktsioon aegub 2021. aasta augustist

### <a name="microsoft-azure-sql-reports-in-lifecycle-services-lcs"></a>Microsoft Azure Lifecycle Services’i (LCS) SQL aruanded

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Kõik tegevused ja seire viiakse läbi sisemiselt, platvormi kaudu, automatiseerimise abil. See ei nõua käsitsi sekkumist.|
| **Asendatud teise funktsiooniga?**   | Jah, nüüd on olemas automatiseeritud süsteem, mis renderdab need võimalused aegunuks. |
| **Mõjutatud tootealad**         | SQL-i aruanded: praegune DTU, praeguse DTU üksikasjad, lukustamise üksikasjad, praeguse plaani juhendi loend, päringu ID-de loendi toomine, SQL-i päringuplaani toomine antud plaani ID jaoks, päringuplaanide ja käivitamise oleku toomine, konfiguratsiooni saamine, oota statistikat, kõige kallimate päringute loend |
| **Juurutamissuvand**              | Pilve juurutamine: Mõjutab Microsoft`i hallatud tootmiskeskkondi ja liivakastikeskkondi kihist 2 kuni kihini 5. |
| **Olek**                         | Aegunud: Planeeritud eemaldamise kuupäev oktoobris 2021. |

### <a name="azure-sql-actions-in-lcs"></a>Azure SQL-i tegevused LCS-is

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Mõned SQL-aruanded LCS-s aeguvad. Kõik tegevused ja seire viiakse läbi sisemiselt, platvormi kaudu, automatiseerimise abil. See ei nõua käsitsi sekkumist. |
| **Asendatud teise funktsiooniga?**   | Jah, nüüd on olemas automatiseeritud süsteem, mis renderdab need võimalused aegunuks. |
| **Mõjutatud tootealad**         | SQL-i tegevused: plaanijuhendi loomine, et sundida plaani ID-d, luua plaanijuhend tabeli vihjete lisamiseks, plaani juhendi eemaldamine, lehelukkude keelamine/lukustamine ja lukustamise eskalatsioon, tabeli statistika värskendamine, indeksi uuesti loomine, indeksi loomine |
| **Juurutamissuvand**              | Pilve juurutamine: Mõjutab Microsoft`i hallatud tootmiskeskkondi ja liivakastikeskkondi kihist 2 kuni kihini 5. |
| **Olek**                         | Aegunud: Planeeritud eemaldamise kuupäev oktoobris 2021. |

## <a name="feature-deprecation-effective-may-2021"></a>Funktsioon aegus 2021. aasta maist

### <a name="globalization-portal-in-lifecycle-services-lcs"></a>Globalisatsiooni portaal rakenduses Lifecycle Services (LCS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Kaotame LCS Globalization portaali, kuna selle funktsiooni on alistanud teised LCS-põhised teenused. |
| **Asendatud teise funktsiooniga?**   | Jah, see funktsioon asendatakse LCS-i probleemi [otsingu](../lifecycle-services/issue-search-lcs.md) ja [Dynamicsi regulatiivse teatise esitamise teenusega](../lcs-solutions/submit-localization-alerts.md). |
| **Mõjutatud tootealad**         | Globaliseerimise portaali funktsioonid LCS-is|
| **Juurutamissuvand**              | Pilvjuurutus |
| **Olek**                         | Taunitud: planeeritud eemaldamise kuupäev mais 2022. |


## <a name="feature-removed-effective-january-28-2021"></a>Funktsioon eemaldati 28. jaanuaril 2021

### <a name="batch-job-to-handle-sql-index-defragmentation"></a>Pakett-töö SQL-indeksi defragmentimise käsitsemiseks

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Töö, seire ja halduse üldkulude vähendamiseks ja klientide indeksihalduse säilitamiseks on see funktsioon eemaldatud. |
| **Asendatud teise funktsiooniga?**   | Tulevikus teevad indeksihooldust Microsofti teenused. See toimub pidevalt ilma kasutaja töökoormusi mõjutamata. |
| **Mõjutatud tootealad**         | Finance and Operations rakendused|
| **Juurutamissuvand**              | Pilve juurutamine – mõjutab Microsofti hallatud töökeskkondi ja liivakastikeskkondi kihist 2 kuni kihini 5. |
| **Olek**                         | See funktsioon on eemaldatud. |


## <a name="platform-updates-for-version-10017-of-finance-and-operations-apps"></a>Rakenduste Finance and Operations Platformi versiooni 10.0.17 värskendused


### <a name="visual-studio-2015"></a>Visual Studio 2015

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Uusimate Visual Studio versioonide toetamiseks tuleb Visual Studio X++ laiendites teha teatud muudatusi. Need muudatused ei ühildu Visual Studioga 2015. |
| **Asendatud teise funktsiooniga?**   | Visual Studio 2015 asemel saab kasutatavaks ja nõutavaks versiooniks Visual Studio 2017. |
| **Mõjutatud tootealad**         | Visual Studio arendustööriistad |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Värskendamisel eemaldatakse eelmised X++ tööriistad Visual Studio 2015-st ja värskendatud tööriistu ei installita Visual Studio 2015-de. See ei mõjuta majutatud järke. Virtuaalmasinaid koostades tuleb konveieri (koostamisdefinitsioon) käsitsi uuendada, et muuta sõltuvus MSBuild 14.0-st (Visual Studio 2015) variandile MSBuild 15.0 (Visual Studio 2017), nagu kirjeldatud jaotises [Pärandkonveieri värskendamine lahenduses Azure Pipelines](../dev-tools/pipeline-msbuild-update.md). |

### <a name="user-avatar"></a>Kasutaja avatar 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Kasutaja avatar, mis kuvatakse navigeerimisriba paremal küljel, toodi Dynamics 365 päise juhtelemendi API-d kasutades, mis on aegunud. |
| **Asendatud teise funktsiooniga?**   | Selle asemel näevad kasutajad navigeerimisribal ringis oma initsiaale. See on sama visuaal, mida praegu kasutatakse arendusmasinates. |
| **Mõjutatud tootealad**         | Veebiklient |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Eemaldatud alates versioonist 10.0.17 |

### <a name="enterprise-portal-ep-deprecation"></a>Ettevõtteportaali (EP) amortiseerumine  

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Dynamics AX 2012 ettevõtteportaaliga (EP) seostatud metaandmete artefaktid on aegunud, kuna EP-d pole kunagi Finance and Operationsi rakendustes toetatud. |
| **Asendatud teise funktsiooniga?**   | Ei |
| **Mõjutatud tootealad**         | Veebiklient |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Katkestatud: Kogu EP kood plaanitakse eemaldada 2021. aasta oktoobri väljalaskes. |

## <a name="platform-updates-for-version-10015-of-finance-and-operations-apps"></a>Rakenduste Finance and Operations Platformi versiooni 10.0.15 värskendused

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11 Dynamics 365 tugi on iganenud

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Kehtib alates 2020. detsembrist, Microsoft Internet Explorer 11 tugi kõigile Dynamics 365 toodetele on iganenud ja Internet Explorer 11 ei toetata pärast 2021. aasta augustit.<br><br>See mõjutab kliente, kes kasutavad Dynamics 365 tooteid, mis on mõeldud kasutamiseks Internet Explorer 11 liidese kaudu. Pärast 2021. aasta augustit, Internet Explorer 11 ei toetata selliste Dynamics 365 toodete puhul. |
| **Asendatud teise funktsiooniga?**   | Soovitame klientide minna üle Microsoft Edge-le.|
| **Mõjutatud tootealad**         | Kõik Dynamics 365 tooted |
| **Juurutamissuvand**              | Kõik|
| **Olek**                         | Internet Explorer 11 ei toetata pärast 2021. aasta augustit.|


### <a name="visual-studio-add-in-to-apply-metadata-hotfixes"></a>Visual Studio lisandmoodul metaandmete kiirparanduste rakendamiseks

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Metaandmete kiirparandused ei ole enam toetatud pärast [One Versioni](../../fin-ops/get-started/one-version.md) teenusevärskendusi, mis võeti kasutusele juulis 2018 koos versiooniga 8.1. |
| **Asendatud teise funktsiooniga?**   | Üksikud metaandmete kiirparandused ei ole toetatud versioonide jaoks saadaval. Selle asemel rakendatakse kumulatiivseid kvaliteedivärskendusi. |
| **Mõjutatud tootealad**         | Visual Studio lisandmoodulid |
| **Juurutamissuvand**              | Virtuaalsed masinad arendamiseks |
| **Olek**                         | Alates versioonist 10.0.15 ei ole lisandmoodul enam Visual Studio tööriistades. |


## <a name="platform-updates-for-version-10014-of-finance-and-operations-apps"></a>Rakenduste Finance and Operations Platformi versiooni 10.0.14 värskendused

### <a name="online-users-page"></a>Võrgus viibivate kasutajate leht 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | See on pärandleht, mis loodi eelmise kliendi-/serveriarhitektuuri jaoks. Sellel lehel olev teave ei ole alati täpne, mis võib tekitada segadust ja olla eksitav. |
| **Asendatud teise funktsiooniga?**   | Uus leht on saadaval hilisemas värskenduses.|
| **Mõjutatud tootealad**         | Süsteemihaldus |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | See vorm eemaldatakse 2021. a oktoobris.   |


## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>Rakenduste Finance and Operations Platformi versiooni 10.0.13 värskendused


### <a name="custom-code-defined-in-ssrs-report-properties"></a>SSRS-aruande atribuutides määratletud kohandatud kood 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Üldiselt on kohandatud koodi pakutav kasu piiratud, samal ajal kui selle toetamiseks on vaja märkimisväärseid ressursse ja arvutusvõimsust. Kohandatud koodi kasutavad peamiselt aruande loojad, et kutsuda kohandatud koodi moodulist välja avalikke meetodeid. Siiski ei toeta pilvepõhine teenus SSRS-aruannete puhul viiteid kohandatud moodulitele. |
| **Asendatud teise funktsiooniga?**   | Aruande loojad võivad jätkata viitamist avalikele .NET-i API-dele, et teha mistahes tekstiboksi avaldises matemaatika, teisenduse ja vorminguga seotud toiminguid. Lisateavet leiate teemast [Koodi lisamine aruandesse (SSRS)](/sql/reporting-services/report-design/add-code-to-a-report-ssrs).  |
| **Mõjutatud tootealad**         | RDL-is määratletud, kohandatud koodi sisaldavate rakenduse aruande kujunduste alamhulk. |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Versioonis 10.0.13 hakkab kompilaator väljastama hoiatusi selliste eksemplaride korral, mille puhul tuvastati SSRS-aruande definitsioonis kohandatud kood. Probleemi lahendamiseks avage aruande kujunduse definitsioon ja eemaldage kõik kohandatud koodi artefaktid. See hoiatus asendatakse tulevases värskenduses kompilaatori tõrkega.   |

### <a name="upgrade-of-three-jquery-component-libraries"></a>Kolme jQuery komponenditeegi täiendamine 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Kolme jQuery komponenditeeki uuendatakse turvaparandustega ja valuuta haldamiseks.   
| **Asendatud teise funktsiooniga?**   | Mõjutatud on järgmised teegid: jQuery (versioonilt 2.1.4 versioonile 3.5.0), jQuery UI (versioonilt 1.11.4 versioonile 1.12.1), jQuery qTip (versioonilt 2.2.1 versioonile 3.0.3). JQuery on migreerimisjuhised internetis kättesaadavaks teinud.  |
| **Mõjutatud tootealad**         | Laiendatavad juhtelemendid, täpsemalt kohandatud JavaScripti kood, mis kasutab iganenud või eemaldatud API-sid |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Versioonis 10.0.13 / platvormivärskenduses 37 saavad kliendid pärast funktsiooni „Kolme jQuery komponenditeegi täiendamine” lubamist hakata soovi korral kasutama uusimaid teeke. Uued teegid tuleb kasutusele võtta 2021. aprilli väljaandega, et anda aega mõjutatud API-de migreerimiseks.   |

### <a name="existing-grid-controlforcelegacygrid-api"></a>Olemasoleva tabeli juhtelement/forceLegacyGrid() API

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Olemasoleva tabeli juhtelement asendatakse uue ruudustiku juhtelemendiga. |
| **Asendatud teise funktsiooniga?**   | [Uue tabeli juhtelement](../..//fin-ops/get-started/grid-capabilities.md) |
| **Mõjutatud tootealad**         | Veebiklient |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Versioonis 10.0.13 on uus tabeli juhtelement üldiselt saadaval ja kliendid saavad funktsiooni valikuliselt sisse lülitada. Uus võrgukontroll lülitatakse vaikimisi sisse 2021. aasta oktoobri väljaandega ja praegu on plaanitud teha see kohustuslikuks 2022. aasta aprillis. Kui uus tabeli juhtelement muutub kohustuslikuks ei saa **forceLegacyGrid()** API-t enam kasutada. |

### <a name="personalization-without-saved-views"></a>Salvestatud vaadeteta isikupärastamine 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Isikupärastamise alamsüsteem on muudetud salvestatud vaadete funktsiooniga nii, tagamaks parema jõudluse ja pakkumaks täiendavaid võimalusi. |
| **Asendatud teise funktsiooniga?**   | Salvestatud vaated |
| **Mõjutatud tootealad**         | Veebiklient |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Versioonis 10.0.13/Platvormi värskendusega nr 37 on salvestatud vaadete funktsioon üldiselt saadaval ja kliendid saavad selle valikuliselt sisse lülitada. Salvestatud vaadete funktsioon muutub kohustuslikuks 2021. aasta oktoobri väljalaskes. |


## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>Rakenduste Finance and Operations Platformi versiooni 10.0.12 värskendused

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>Kehtetuid väljaviiteid sisaldavad ruudustiku või grupi juhtelemendi vormilaiendused

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Ruudustiku või grupi juhtelementide andmegrupi atribuute kasutatakse väljagrupi kõikide väljade automaatseks kuvamiseks. Laiendusega lisatud ruudustiku või grupi juhtelement võib sisaldada välju, mis ei ole enam väljagrupis määratletud, või väljagrupis määratletud väljad võivad puududa. See võib põhjustada käitusajal vastuolulist käitumist. Rakenduste Finance and Operations Platformi versiooni 10.0.12 värskendused liigitavad nüüd selle probleemi kompilaatori *hoiatusena*. Probleemi lahendamiseks avage vormilaiendus ja salvestage see.
| **Asendatud teise funktsiooniga?**   | See kompilaatori hoiatus asendatakse tulevases värskenduses kompilaatori tõrkega. |
| **Mõjutatud tootealad**         | Visual Studio arendustööriistad |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Kompilaatori hoiatus on kasutusele võetud Finance and Operationsi rakenduste versiooni 10.0.12 platvormivärskendustes. |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Rakenduste Finance and Operations Platformi versiooni 10.0.11 värskendused

### <a name="explicit-safe-lists-for-self-service-environments"></a>Üksikasjalikud turvalised loendid iseteeninduskeskkondade jaoks

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | IP-de lisamine turvalistesse loenditesse on muutunud. Iseteenindus ei toeta enam turvaliste IP-de loendeid. |
| **Asendatud teise funktsiooniga?**   | Lisateavet vt teemast [Azure Active Directory tingimusliku juurdepääsu konfigureerimine](/appcenter/general/configuring-aad-conditional-access).|
| **Mõjutatud tootealad**         | Turve |
| **Juurutamissuvand**              | Pilv |
| **Olek**                         | Aegunud: see funktsioon on iseteeninduse juurutustes täielikult aegunud. |

### <a name="visual-studio-2015"></a>Visual Studio 2015

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Uusimate Visual Studio versioonide toetamiseks tuleb Visual Studio X++ laiendites teha teatud muudatusi. Need muudatused ei ühildu Visual Studioga 2015. |
| **Asendatud teise funktsiooniga?**   | Visual Studio 2015 asemel saab kasutatavaks ja nõutavaks versiooniks Visual Studio 2017. |
| **Mõjutatud tootealad**         | Visual Studio arendustööriistad |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Virtuaalarvutid, mis kasutavad versiooni 10.0.13 (Platform update 37) või hilisemat, sisaldavad programmi Visual Studio 2017. Versioon 10.0.16 (Platform Update 40) on viimane väljalase, mis toetab programmi Visual Studio 2015. Virtuaalarvutid, millel on ainult Visual Studio 2015 ei saa värskendada versioonile 10.0.17 (Platform update 41). |

### <a name="field-groups-containing-invalid-field-references"></a>Sobimatuid väljaviiteid sisaldavad väljagrupid

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Tabeli metaandmete määratluste väljagrupid võivad sisaldada kehtetuid väljaviiteid. Nende väljagruppide juurutamise korral võib see põhjustada käitusaja tõrkeid teenuses Financial Reporting ja Microsoft SQL Serveri aruandlusteenustes (SSRS). Platform update'i 23 lisati kompilaatori *hoiatus*, mis lubas selle metaandmete probleemi lahendamise. Rakenduste Finance and Operations Platformi versiooni 10.0.11 värskendused liigitavad selle probleemi kompilaatori *tõrkena*.<p>Sellep probleemi lahendamiseks tehke järgmist.</p><ol><li>Eemaldage sobimatu väljaviide tabeli väljagrupi definitsioonist.</li><li>Kompileerige uuesti.</li><li>Veenduge, et kõik tõrked oleksid lahendatud.</li></ol> |
| **Asendatud teise funktsiooniga?**   | See kompilaatori tõrge asendab kompilaatori hoiatuse jäädavalt.  |
| **Mõjutatud tootealad**         | Visual Studio arendustööriistad |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud: kompilaatori hoiatus on Finance and Operations rakenduste versiooni 10.0.11 platvormivärskendustes kompilaatori tõrge. |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>ISV-litsentsid, mis on loodud SHA1 räsialgoritmi abil

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Sõltumatu tarkvara hankija (ISV) litsentside loomise protsess on muutunud. Lisateabe saamiseks vt [sõltumatu tarkvara hankija (ISV) litsentsimine](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes). |
| **Asendatud teise funktsiooniga?**   | Jah. Windows PowerShelli kasutamine litsentside loomiseks. |
| **Mõjutatud tootealad**         | Visual Studio arendustööriistad |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud: ISV litsentsid, mis loodi SHA1 räsialgoritmi abil. See algoritm sõltus sertidest, mis loodi utiliidi MakeCert abil ja see utiliit on aegunud.<br><br>Aegunud: SHA1 kasutamine turbe või räsimise eesmärgil. SHA1 ei tööta enam 2021. aasta alguses. Seetõttu ei tohiks seda enam kasutada.<br><br>Eemaldatud: toetus transpordi kihi turvalisusele (tls) 1.0 ja TLS 1.1 sissetulevad või väljaminevad taotlused. |

## <a name="platform-update-32"></a>Platvormivärskendus update 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Töövoo taotluse muutmise dialoogiboks ei sisalda enam kasutaja valiku ripploendit

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | See oli turvalisuse probleem, kuna muudatuse taotluse võis saata soovimatule kasutajale. See oli ka kasutatavuse probleem, sest see sundis kasutajat määratlema, kes oli töövoo algataja, ja valida need käsitsi.  |
| **Asendatud teise funktsiooniga?**   | Ei |
| **Mõjutatud tootealad**         | Töövoog |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Kasutaja valiku ripploend eemaldati taotluse muudatuse dialoogiboksist platvormi värskenduses 32. Taotluse muutmise taotlused saadetakse automaatselt algatajale, nagu see on ette nähtud. Lisateavet selle funktsiooni kohta vt teemast [Tegevused töövoo kinnitusprotsessis](../../fin-ops/organization-administration/workflow-actions.md?toc=%2fdynamics365%2fcommerce%2ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Manustatud süvitsi mindavaid linke ei toetata enam lehekülgjaotusega dokumentides, mida pilve majutatud teenus renderdab 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Teenuse renderdatud dokumentidesse manustatud navigeermise URL-id võivad sisaldada tundlikke äriandmeid. Eemaldame manustatud süvitsi mindavate linkide toe dokumentidest ettevaatusabinõuna, et täiendavalt kaitsta kliendiandmeid. Kasutajad saavad kasu ka parandatud jõudlusest ja selle muudatuse tulemusel saavad toota dokumente interaktiivselt.  |
| **Asendatud teise funktsiooniga?**   | Ei |
| **Mõjutatud tootealad**         | Aruandlus |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Seda funktsiooni eemaldatakse aktiivselt teenusest.<br><br>Kaasaegne klient pakub mitmeid võimalusi vaadete loomiseks, mis sisaldavad automaatselt loodud linke, mis aitavad rakenduses navigeerida. Lehekülgjaotusega dokumente, mida teenuses renderdatakse, soovitatakse kasutada välissuhtluses, nagu adressaatidele meilitud, arhiivitud ja prinditud. Oleme parandanud dokumentide eelvaate kogemust otse brauseris, mis võimaldab otsest juurdepääsu kohalikele printeritele. Lisateabe saamiseks vaadake teemat [PDF-dokumentide eelvaade manustatud vaaturi abil](../analytics/preview-pdf-documents.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Varasemad teatised eemaldatud või aegunud funktsioonidest
Lisateavet funktsioonide kohta, mis on eelnevatest versioonidest eemaldatud või aegunud, vt teemat [Varasematest versioonidest eemaldatud või aegunud funktsioonid](../migration-upgrade/deprecated-features.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
