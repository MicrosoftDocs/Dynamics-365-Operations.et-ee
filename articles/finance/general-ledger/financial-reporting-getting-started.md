---
title: Finantsaruandluse ülevaade
description: See teema kirjeldab, kuhu pääseb Microsoft Dynamics juurde finantsaruandluses 365 Finantsid ja kuidas kasutada finantsaruandluse võimalusi.
author: aprilolson
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "10444"
- intro-internal
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fcdb5a934818468e00be960f9afe541966e5eabf
ms.sourcegitcommit: e8a2a1e34fa48a42afac9724828f4ec72b6d7085
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2022
ms.locfileid: "8573646"
---
# <a name="get-started-with-financial-reporting"></a>Finantsaruandlusega alustamine 

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kust pääseda juurde finantsaruandlusele ja kasutada finantsaruandluse võimalusi. See sisaldab ka pakutavate vaike-finantsaruannete kirjeldust.

## <a name="accessing-financial-reporting"></a>Juurdepääs finantsaruandlusele

Menüü **Finantsaruandlus** leiate järgmistest asukohtadest.

- **Pearaamat** &gt; **Päringud ja aruanded**
- **Eelarvestamine** &gt; **Päringud ja aruanded** &gt; **Põhiline eelarvestamine**
- **Eelarvestamine** &gt; **Päringud ja aruanded** &gt; **Eelarve plaanimine**
- **Eelarvestamine** &gt; **Päringud ja aruanded** &gt; **Eelarve juhtimine**
- Konsolideerimised

Finantsaruannete loomiseks ja genereerimiseks juriidilisele isikule tuleb seadistada sellele juriidilisele isikule järgmine teave.

- Rahanduskalender
- Ledger
- Kontoplaan
- Currency
- Sisestage kanne vähemalt ühele kontole
- MainAccount on toodud veerus **Valitud** jaotises **Finantsaruandluse seadistuse** leht (**Pearaamat > Pearaamatu seadistus > Finantsaruandluse seadistus**)

## <a name="granting-security-access-to-financial-reporting"></a>Turvalisuse võimaldamine finantsaruandlusele

Rahalise aruandluse funktsioonid on saadaval kasutajatele, kellele on turberollide kaudu määratud sobivad privileegid ja kohustused. Järgmistes jaotistes on nimetatud need privileegid ja kohustused koos seotud rollidega.

### <a name="duties"></a>Kohustused

| Kohustuse silt                            | Kirjeldus                                                             | AOT nimi                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Finantsaruandluse turbe haldamine | Finantsaruandluse turbe haldamine ja administratiivtoimingute tegemine. | FinancialReportsSecurityMaintain |
| Finantsaruannete haldamine            | Finantsaruannete koostamine ja haldamine.                                  | FinancialReportsMaintain         |
| Finantsaruannete loomine            | Finantsaruannete loomine ja värskendamine.                                 | FinancialReportsGenerate         |
| Finantstulemuste ülevaatamine          | Finantstulemuste ülevaatamine ja analüüsimine.                               | FinancialReportsPerfReview       |

### <a name="privileges"></a>Privileegid

| Privileegi silt                       | Kirjeldus                                                             | AOT nimi                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Finantsaruandluse turbe haldamine | Finantsaruandluse turbe haldamine ja administratiivtoimingute tegemine. | FinancialReportsSecuritySystemMaintain |
| Finantsaruannete haldamine            | Finantsaruannete koostamine ja haldamine.                                  | FinancialReportsMaintainReports  |
| Finantsaruannete loomine            | Finantsaruannete loomine ja värskendamine.                                 | FinancialReportsGenerateReports  |
| Finantsaruannete vaatamine                | Finantsaruannete vaatamine.                                                 | FinancialReportsView             |

### <a name="roles"></a>Rollid

| Privileegi silt                       | Kohustus                                  | Rollid                                                                           |
|---------------------------------------|---------------------------------------|---------------------------------------------------------------------------------|
| Finantsaruandluse turbe haldamine | Finantsaruandluse turbe haldamine | Turbeadministraator                                                          |
| Finantsaruannete haldamine            | Finantsaruannete haldamine            | Pearaamatupidaja, Raamatupidaja, Finantskontroller, Eelarvehaldur |
| Finantsaruannete loomine            | Finantsaruannete loomine            | Juhataja, Finantsjuht, Raamatupidaja                                                            |
| Finantsaruannete vaatamine                | Finantstulemuste ülevaatamine          | Ühtegi pole määratud                                                                   |

Pärast kasutaja lisamist või rolli muutmist peaks kasutaja mõne minuti jooksul finantsaruandlusele juurde pääsema. 

> [!NOTE]
> Süsteemiadministraatori roll lisatakse finantsaruandluses kõigile rollidele.

## <a name="report-deletions-and-expirations"></a>Aruande kustutamised ja aegumised

Aruande loonud kasutajad saavad oma aruandeid kustutada. Kohustusega **Finantsaruandluse turbe haldamine** kasutajad saavad kustutada teiste aruandeid. 

Väljalaskes 10.0.8 lisati aegumiskuupäevad. Uus nõutav funktsioon lubatakse funktsioonihalduse tööruumi lehel **Kõik**. Funktsioon **Finantsaruannete säilitamise poliitikad** sisaldab järgmisi muudatusi.
* Uued loodud aruanded märgitakse automaatselt, et neil on loomise ajast 90 päeva pärast aegumiskuupäev.
* Kõikidele aruannetele, mis olid olemas enne funktsiooni installimist, antakse 90-päevane aegumisperiood. Kuupäev võidakse lühikest aega kuvada tühjana, kuni finantsaruandluse teenus töötab, luuakse aruanne ja teenus värskendab olemasolevaid tühjade aegumiskuupäevadega aruandeid. 
* **Finantsaruandluse turbe haldamise** kohustusega kasutajatel on juurdepääs sellele funktsioonile. Kõik kohustusega **Finantsaruannete haldamine** kasutad, kellele on antud privileeg **Finantsaruannete aegumise haldamine**, omavad võimalust aegumiskuupäeva muuta. Praegu on saadaval kaks säilitamise võimalust. 

    * Aegumine 90 päeva möödudes.
    * Võimalus seada aruanne mitte kunagi aeguma.

Kui on valitud aegumine, näiteks 90 päeva, siis rakendatakse seda tänasest alates 90 päeva pärast. See toimib teistmoodi, kui aruande loomisel määratud algsest loomiskuupäevast arvestatud 90 päeva. 

Hilisemas funktsioonis kaalutakse täiendavaid võimalusi. Aegumine 90 päeva möödudes on vaikesäte ja sobivate lubadega kasutajad saavad seda **Finantsaruannete** loendi lehel muuta.

## <a name="default-reports"></a>Vaikearuanded

Finantsaruandlus pakub 22 vaike-finantsaruannet. Iga aruanne kasutab põhikonto vaikekategooriaid. Saate kasutada neid aruandeid olemasoleval kujul või finantsaruandluse vajaduste lähtepunktina. Lisaks tavalistele finantsaruannetele nagu kasumiaruanne ja bilanss sisaldavad need vaikearuanded aruandeid, millel on näidatud erinevat tüüpi finantsaruanded, mida saate koostada. 

<!--Each report in the following table links to an Office Mix presentation about the report.-->

| Vaikearuanne                                                                                         | Kirjeldus                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 12 kuu jooksev ühe veeruga kasumiaruanne – vaikimisi | Vaadake organisatsiooni tulusust viimase 12 kuu jooksul ühes veerus.                                                                                                                                                                                                                                      |
| 12 kuu trendi kasumiaruanne – vaikimisi                 | Vaadake organisatsiooni tulusust iga viimase 12 kuu kohta. Need 12 kuud võivad hõlmata rohkem kui ühte rahandusaastat.                                                                                                                                                                                             |
| Tegelik võrreldes eelarvega – vaikimisi                                | Vaadake kõigi algse eelarve kontode üksikasjalikku saldoteavet ja võrrelge parandatud eelarvet tegelike hälbega summadega.                                                                                                                                                                          |
| Auditi üksikasjad – vaikimisi                                  | Saate vaadata kõigi kontode üksikasjalikku saldoteavet. Selles aruandes kuvatakse deebet- ja kreeditsaldod aruandlusvaluutas ja kohalikus valuutas koos täiendava kandeteabega, nt kasutaja ID, andmeid viimati muutnud kasutaja, viimase muutmise kuupäev ja töölehe ID. |
| Saldoloend – vaikimisi                                   | Saate vaadata kõigi kontode üksikasjalikku saldoteavet. Selles aruandes kuvatakse avamis- ja sulgemissaldod ning deebet- ja kreeditsaldod praeguse perioodi ja möödunud aasta kohta koos täiendavat kandeteabega (nt kanne).                                                                    |
| Bilanss – vaikimisi                                   | Saate vaadata organisatsiooni aasta rahalist seisu.                                                                                                                                                                                                                                                             |
| Kõrvuti konsolideeritud bilanss ja kasumiaruanne – vaikimisi | Saate vaadata kõrvuti organisatsiooni aasta finantsseisundit ja tulusust.                                                                                                                                                                                                                              |
| Rahavoog – vaikimisi                                       | Saate ülevaate organisatsiooni sissetulevast ja väljuvast sularahast.                                                                                                                                                                                                                                   |
| Üksikasjalik JE ja TB ülevaade – vaikimisi                      | Saate kuvada kõigi kontode algsaldo ja tegevuse teabe.                                                                                                                                                                                                                                                      |
| [Üksikasjalik proovibilanss – vaikimisi](trial-balance-financial-reports.md)| Saate vaadata kõigi deebet- ja kreeditsaldodega kontode saldoteavet ja nende saldode netoväärtust koos kande kuupäeva, kande ja töölehe kirjeldusega.                                                                                                                                  |
| Kulude kolme aasta kvartalitrend – vaikimisi             | Saate ülevaate viimase 12 kvartali kuludest kolme viimase aasta jooksul.                                                                                                                                                                                                                                   |
| Finantspealdised: JE ja TB ülevaade – vaikimisi            | Saate vaadata ülevaadet saldodest ja tegevustest vara, kohustuse, omakapitali, tulu, kulu, kasumi või kahjumi finantspealdiste kohta.                                                                                                                                                                           |
| [Kasumiaruanne – vaikimisi](income-statement-financial-report.md)| Saate vaadata organisatsiooni tulusust praeguse perioodi ja aasta puhul kuni praeguse kuupäevani.                                                                                                                                                                                                                                   |
| Pearaamatukannete loend – vaikimisi                        | Saate vaadata kõigi kontode üksikasjalikku saldoteavet. Selles aruandes kuvatakse deebet- ja kreeditsaldod koos täiendava kandeteabega, nt kandekuupäev, töölehe number, kanne, sisestustüüp ja jälgimisnumber.                                                                            |
| Suhtarvud – vaikimisi                                          | Saate vaadata organisatsiooni maksejõulisust, tulusust ja efektiivsuse suhtarve aasta kohta.                                                                                                                                                                                                                           |
| Jooksva 12 kuu kulud – vaikimisi                       | Saate ülevaate kuludest viimase 12 kuu kohta. Need 12 kuud võivad hõlmata rohkem kui ühte rahandusaastat.                                                                                                                                                                                                       |
| Jooksva kvartali kasumiaruanne – vaikimisi               | Vaadake organisatsiooni tulusust kvartalis eelmise aasta kohta ja aasta kohta tänase kuupäevani.                                                                                                                                                                                                                   |
| Kõrvuti bilanss – vaikimisi                      | Saate vaadata organisatsiooni aasta rahalist seisu. Selles aruandes kuvatakse varad ja kohustused ning omakapital kõrvuti.                                                                                                                                                                                |
| [Proovibilansi kokkuvõte – vaikimisi](trial-balance-financial-reports.md)| Saate vaadata bilansi teavet kõigi avamis- ja sulgemissaldode ning deebet- ja kreeditsaldodega kontode puhul koos nende netoerinevusega.                                                                                                                                                                  |
| [Proovibilansi kokkuvõte aasta-aastalt – vaikimisi](trial-balance-financial-reports.md)| Saate vaadata bilansi teavet kõigi avamis- ja sulgemissaldode ning deebet- ja kreeditsaldodega kontode puhul koos nende netoerinevusega praeguse aasta ja möödunud aasta kohta.                                                                                                                           |
| Nädala müük ja allahindlused – vaikimisi                     | Saate ülevaate kuu iga nädala müügist ja allahindlustest. See aruanne sisaldab kokku nelja nädalat.                                                                                                                                                                                                              |
| Saadaolevad eelarvefondid – vaikesäte                         | Saate vaadata üksikasjalikku võrdlust muudetud eelarve, tegelike kulude, eelarvereservide ja eelarvefondide vahel kõigi kontode kohta                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Finantsaruannete avamine

Kui valite menüü **Finantsaruandlus**, kuvatakse ettevõtte vaike-finantsaruannete loend. Seejärel saate aruande avada või seda muuta. Mõne vaikearuande avamiseks valige aruande nimi. Aruande esmakordsel avamisel koostatakse see automaatselt eelmise kuu kohta. Näiteks kui avate aruande esmakordselt augustis 2019, koostatakse aruanne 31. juuli 2019 kohta. Pärast aruande avamist saab seda uurida, minnes süvitsi konkreetsetes andmehulkades ja muutes aruande valikuid.

## <a name="creating-and-modifying-financial-reports"></a>Finantsaruannete koostamine ja muutmine

Finantsaruannete loendist saate luua uue aruande või muuta olemasolevat aruannet. Kui teil on olemas vastavad load, saate koostada uue finantsaruande, valides toimingupaanil suvandi **Uus**. Aruande koostamise programm laaditakse teie seadmesse. Kui aruandekoostur on käivitunud, saate koostada uue aruande. Pärast uue aruande salvestamist kuvatakse see finantsaruannete loendis. Loendis kuvatakse ainult aruanded, mis loodi ettevõttele, mida te Dynamics 365 Finances kasutate. 

## <a name="reporting-tree-definitions"></a>Aruandluspuu definitsioonid

Üks finantsaruannete koostamiseks kasutatavaid komponente on aruandluspuu definitsioon. Aruandluspuu definitsioon aitab määratleda teie organisatsiooni struktuuri ja hierarhia. See on dimensioonidevaheline hierarhiastruktuur, mis põhineb finantsandmete dimensiooniseostel. See annab teavet aruandlusüksuse tasandil ja kõigi puu üksuste koondtasandil.

Oma organisatsiooni andmete eri viisil kuvamiseks saate luua piiramatu arvu aruandluspuid. Iga aruandluspuu võib sisaldada osakondade ja kokkuvõtvate üksuste mis tahes kombinatsiooni, kuid aruande definitsioon saab korraga ühenduse luua ainult ühe aruandepuuga. 

## <a name="update-the-financial-reporting-version-through-slipstreaming"></a>Finantsaruandluse versiooni värskendamine sissevoolu kaudu

Finantside ja toimingute rakendusi uuendatakse igal kuul. Finantsaruandlust ei uuendata siiski tingimata selle sagedusega. Lisaks on klientidel rohkem suvandeid finantside ja toimingute rakenduste värskenduste rakendamise kohta. Finantsaruandluse uuendused installitakse automaatselt. Finantsaruandluses on määratud versioon, mida tarbitakse kliendi keskkonnas siis, kui teenuse värskendust rakendatakse, kui käivitatakse ületunnitöö või kui kliendi keskkond on hooldusrežiimis. Seda protsessi nimetatakse *sissevooluks* või *tõeseks*, kuna kõigile kliendi rakendustele on määratud finantsaruandluse sama versioon.

Kõikides versioonides väljastatud muudatused leiate dynamics [365 Financei uutest või muutunud muudatustest](../../finance/get-started/whats-new-home-page.md). Platvormi värskendused ja vigade parandused leiate lehekülje allservas olevast jaotisest "Lisaressursid" iga väljaande kohta.

Valitud sissepööratud versioon on tootmiseks valmis finantsaruandluse üle vaadatud ja kinnitatud versioon. See ühildub mis tahes Dynamics 365 Finance'i varasema või tulevase versiooniga. Näiteks võib finantsaruandlus olla 10.0.19 värskeim järgus, kui klient on veel rakenduse versioonis 10.0.16.

> [!NOTE]
> Ainus valik, kus kliendid saavad eelmisele versioonile liikuda (alandatud stsenaarium), toimub siis, kui Microsoft peatab probleemi tõttu tegeliku ümberpööramise. Kui parandus on saadaval, rakendatakse see automaatselt.

Sissevoolu protsess on täielikult automatiseeritud ja ei nõua kliendi tegevust. Kolm topologi tarbivad sissevoolu, igaüks veidi erineval viisil:

- **Ettevõttesisene** - ettevõttesisene juurutamine ei toeta sisse- ja tõest ülesvoolu.
- **Infrastruktuur teenusena (IaaS)** – Sissevoolu loogikat rakendatakse mis tahes toimingu ajal, mis proovib värskendada finantsaruandlust. See sisaldab binaarseid värskendusi või binaarseid värskendusi sisaldavaid levitamisvorme.
- **Iseteenindus** - iga toiming, mis nõuab finantsaruandluse downtime'i, rakendab sissevoolu loogikat:

    - Binaarvärskendused või ülekanded, mis sisaldavad binaarvärskendusi
    - S lappimine või muu infrastruktuuri seisak
    - AOT paketi juurutused

## <a name="troubleshooting-issues-opening-report-designer"></a>Aruande kujundaja avamise probleemide tõrkeotsing

Mõned tavalisemad juhud, mis võivad põhjustada probleeme aruande kujundaja avamisel. Need probleemid ja nende lahendamise etapid on järgmised.

1. probleem: aruande kujundaja ei käivitu, kui valite suvandi **Uus** või **Redigeeri**.

* Valige Internet Exploreris **Sätted** ja seejärel valige **Interneti suvandid**. Valige vahekaart **Turve**. Valige Usaldusväärsed saidid ja seejärel valige **Saidid**. Sisestage jaotisesse **Lisa see veebisait tsooni** väärtus „\*\.dynamics.com” (jutumärkideta) ja seejärel valige **Lisa**. 
* Valige Internet Exploreris **Sätted** ja seejärel valige **Interneti suvandid**. Valige vahekaart **Turve**. Valige Usaldusväärsed saidid. Muutke alal, mille silt on Selle tsooni turbetase suvandi väärtuseks **Keskmine-madal**.
* Keelake hüpikakende blokeerija oma brauseris.
* Tööjaamad peavad installima Microsoft .NET Frameworki versiooni 4.7.2 või uuema. Selle Microsoft .NET Frameworki versiooni saab laadida alla ja installida [Microsofti allalaadimiskeskusest](https://dotnet.microsoft.com/download/dotnet-framework/net472).
* Kui kasutate Chrome’i brauserit, peate aruande koostaja kliendi allalaadimiseks installima laienduse ClickOnce. Kui töötate Chrome’is inkognito-režiimis, siis veenduge, et laiendus ClickOnce oleks inkognito-režiimi jaoks aktiveeritud. Lisateavet Chrome’i laiendi ClickOkone kohta vt teemast [Pilvjuurutuste süsteeminõuded](../../fin-ops-core/fin-ops/get-started/system-requirements.md).
* Kui kasutate Microsoft Edge’i Chrome’i brauseriga, ei pea te Edge Chromiumi jaoks laiendust ClickOnce installima. Samas aruandekoosturi klientrakenduse allalaadimiseks peate suvandi ClickOnce lubama. Kui töötate inkognito-režiimis, siis veenduge, et laiendus ClickOnce oleks inkognito-režiimi jaoks aktiveeritud.

    1. Avage uus brauser rakenduses Microsoft Edge.
    2. Sisestage **edge://flags** ja valige **Sisesta**.
    3. Otsige üles suvand **ClickOnce'i tugi** või kasutage otselinki **edge://flags/#edge-click-once**.
    4. Seadke rippmenüü suvandi väärtuseks **Lubatud**.
    5. Valige **Taaskäivita brauser**.

2. probleem: kasutajale ei ole määratud vajalikke lubasid rakenduse Financial Reporting kasutamiseks. 

* Et kontrollida, kas kasutajal pole luba, valige suvand **Jah** tõrkes „Rakenduse Financial Reporting serveriga ei saanud ühendada. Valige Jah, kui soovite jätkata ja määrata teise serveri aadressi.” Seejärel valige **Testi ühendust**. Kui teil pole luba, kuvatakse teade, mis ütleb: „Ühenduse loomise katse nurjus. Kasutajal pole serveriga ühenduse loomiseks vajalikke lubasid. Pöörduge süsteemiadministraatori poole.”
* Nõutavad load on loetletud ülalpool [Rakendusele Financial reporting turbejuurdepääsu võimaldamine](#granting-security-access-to-financial-reporting). Rakenduse Financial reporting turve põhineb nendel lubadel. Teil pole juurdepääsu, kui teile pole määratud neid lubasid (või mõnda muud turberolli, mis sisaldab neid lubasid). 
* Integratsiooniülesanne **Ettevõtte kasutajate pakkuja ettevõttele** (mis vastutab ka kasutaja integreerimise eest) käivitub 5-minutilise vahemikuga. Rakenduses Financial Reporting mis tahes õiguste muudatuste jõustumiseks võib kuluda kuni 10 minutit. 

    Kui teine kasutaja saab avada aruande kujundaja, valige **Tööriistad** ja seejärel valige **Integratsiooni olek**. Kinnitage, et integratsiooni vastendamine „Ettevõtte kasutajate pakkuja ettevõttele” on edukalt käivitatud, kuna teile määrati luba rakenduse Financial Reporting kasutamiseks. 

* Võib olla võimalik, et teine tõrge takistas suvandi **Dynamicsi kasutaja integreerimine rakenduse Financial Reporting kasutajaks** lõpetamist. Võib olla ka võimalik, et andmekava lähtestamine on käivitatud ja veel lõpule viimata või ilmnes mõni muu süsteemi tõrge. Proovige protsess hiljem uuesti käivitada. Kui probleem ei lahene, pöörduge oma süsteemiadministraatori poole.

3. probleem: pääsete edasi **ClickOnce'i Report Designer** sisselogimise lehelt, kuid ei saa rakenduses Report Designer sisselogimist lõpule viia. 

* Mandaadi sisestamise ajal peab peie kohalikus arvutis määratud aeg jääma viie minuti vahemikku rakenduse Financial Reporting serveris oleva ajaga. Kui erinevus on üle viie minuti, ei luba süsteem sisse logida. 
* Kui teie arvuti kellaaeg erineb Financial aruandluse serveri ajast, soovitame lubada Windows suvandil seadistada arvuti aeg automaatselt. 

## <a name="troubleshoot-report-designer-issues-with-event-viewer"></a>Report Designer probleemide tõrkeotsing sündmusevaaturiga

Financial aruandluse kasutamisel tekkinud probleemide analüüsimiseks saate kasutada sündmusevaaturit. 

### <a name="what-happens-when-you-have-connections-issues-with-financial-reporting"></a>Mis toimub siis, kui teil on probleemid Financial aruandlusega? 

Siin on mõned sammud, mida saate teha, et muuta oma vestlus Microsoft`i toega tõhusamaks, mis aitab viia teid kiiremini lahenduseni. 
 
Järgmised sammud läbivad sündmusevaaturi teadete sisselutusprotsessi Financial aruandluses. Sündmustevaaturi loodud logid aitavad insenere ühenduse probleemi kiires tuvastamises. Esitage nende logide koopiad koos oma piletiga toe saamiseks.


1. Kopeerib faili RegisterETW.zip kliendi tööjaama (eelistatult töölauale) ja ekstraktib [RegisterETW.zip](https://mbs2.microsoft.com/fileexchange/?fileID=60b1106b-d5f8-4e0f-8041-039102505122).
2. Veenduge, et Windows Event vaatur on suletud.
3. Avage administraatori PowerShell käsuviip ja minge kataloogi, kus asub RegisterETW.ps1.
4. Käivitage järgmine käsk: .\RegisterETW.ps1

    PowerShell`i edukas väljund kontrollitakse teatega, **kompetenteeritud RegisterETW skriptiga**.

    Avage sündmusevaatur uuesti ja näete nüüd neid logisid jaotises **Microsoft > Dynamics**:

    * MR-Klient
    * MR-DVT
    * MR-Integratsioon
    * MR-logija
    * MR-Aruandlus
    * MR_Planeerijaülesanded
    * MR-Sql
    * MR-TraceManager

5. Probleemi taasesitamine rakenduses report designer.
6. Eksportige MR-logija sündmused sündmusevaaturi abil.

## <a name="troubleshoot-issues-connecting-to-financial-reporting"></a>Financial aruandlust ühendavate probleemide tõrkeotsing

Probleem: kuvatakse tõrge "Ei saa ühendust finantsaruandluse serveriga".

* Määrake, kas probleem ilmneb Chrome või Edge interneti-brauserites.
* Kui probleem ilmneb ainult ühes brauseris, võib see olla ClickOnce probleem. 
* Kui saate ühenduse veateate, valige ühenduse testimiseks **Test** katsetus, et näha, milline teade kuvatakse. 
* Probleem võib olla tingitud teisest kasutajast, kellel pole Financial aruandlusele juurdepääsu. Kui kasutajal ei ole juurdepääsu, saab ta teate, et tal pole luba.
* Kui probleem ilmneb mitmes brauseris, veenduge, et tööjaama kella väärtuseks oleks seatud automaatne.
* Töötage kasutajaga, kellel on turvaadministraatori õigused Dynamics 365 Finances ja administraatoriõigused võrgudomeenile, et sisse logida oma tööjaama, et näha, kas nad on ühendatud. Kui nad saavad ühendust, võib probleem olla seotud võrguõigustega.
* Keelake tööjaamas ajutiselt tulemüür. Kui saate siis rakendusega Report Designer ühenduse luua, oli probleem seotud tulemüüriga. Probleemi lahendamiseks tehke koostööd oma organisatsiooni IT-osakonnaga.

## <a name="additional-resources"></a>Lisaressursid

- [Finantsaruannete vaatamine](view-financial-reports.md)
- [Aruandluspuu definitsioonid finantsaruannetes](../../fin-ops-core/dev-itpro/analytics/financial-reporting-tree-definitions.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
