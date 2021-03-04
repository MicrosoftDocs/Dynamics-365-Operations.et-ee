---
title: Finantsaruandluse ülevaade
description: Selles teemas kirjeldatakse, kus pääseda juurde rakenduse Microsoft Dynamics 365 Finance finantsaruandlusele ja kasutada finantsaruandluse võimalusi.
author: aprilolson
manager: AnnBe
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88436b4a5d6be4172e15fa4a9dadc34696417fb9
ms.sourcegitcommit: eec96c64f44d1b4877d49ee15665a774019d42d7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672440"
---
# <a name="get-started-with-financial-reporting"></a>Rakenduse Financial Reporting kasutamise alustamine 

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kus pääseda juurde finantsaruandlusele ja kasutada finantsaruandluse võimalusi. See sisaldab ka pakutavate vaike-finantsaruannete kirjeldust.

<a name="accessing-financial-reporting"></a>Juurdepääs finantsaruandlusele
-----------------------------

Menüü **Finantsaruandlus** leiate järgmistest asukohtadest.

-   **Pearaamat** &gt; **Päringud ja aruanded**
-   **Eelarvestamine** &gt; **Päringud ja aruanded** &gt; **Põhiline eelarvestamine**
-   **Eelarvestamine** &gt; **Päringud ja aruanded** &gt; **Eelarve plaanimine**
-   **Eelarvestamine** &gt; **Päringud ja aruanded** &gt; **Eelarve juhtimine**
-   Konsolideerimised

Finantsaruannete loomiseks ja genereerimiseks juriidilisele isikule tuleb seadistada sellele juriidilisele isikule järgmine teave.

-   Rahanduskalender
-   Ledger
-   Kontoplaan
-   Currency

## <a name="granting-security-access-to-financial-reporting"></a>Rakendusele Financial Reporting turbejuurdepääsu võimaldamine
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
Finantsaruannete loendist saate luua uue aruande või muuta olemasolevat aruannet. Kui teil on olemas vastavad load, saate koostada uue finantsaruande, valides toimingupaanil suvandi **Uus**. Aruande koostamise programm laaditakse teie seadmesse. Kui aruandekoostur on käivitunud, saate koostada uue aruande. Pärast uue aruande salvestamist kuvatakse see finantsaruannete loendis. Loendis kuvatakse ainult need aruanded, mis on loodud ettevõttele, mida Dynamics 365 Finance'is kasutate. 

## <a name="reporting-tree-definitions"></a>Aruandluspuu definitsioonid 
Üks finantsaruannete koostamiseks kasutatavaid komponente on aruandluspuu definitsioon. Aruandluspuu definitsioon aitab määratleda teie organisatsiooni struktuuri ja hierarhia. See on dimensioonidevaheline hierarhiastruktuur, mis põhineb finantsandmete dimensiooniseostel. See annab teavet aruandlusüksuse tasandil ja kõigi puu üksuste koondtasandil.

Oma organisatsiooni andmete eri viisil kuvamiseks saate luua piiramatu arvu aruandluspuid. Iga aruandluspuu võib sisaldada osakondade ja kokkuvõtvate üksuste mis tahes kombinatsiooni, kuid aruande definitsioon saab korraga ühenduse luua ainult ühe aruandepuuga. 


## <a name="troubleshooting-issues-opening-report-designer"></a>Aruande kujundaja avamise probleemide tõrkeotsing
Mõned tavalisemad juhud, mis võivad põhjustada probleeme aruande kujundaja avamisel. Need probleemid ja nende lahendamise etapid on järgmised.

1. probleem: aruande kujundaja ei käivitu, kui valite suvandi **Uus** või **Redigeeri**.

* Valige Internet Exploreris **Sätted** ja seejärel valige **Interneti suvandid**. Valige vahekaart **Turve**. Valige Usaldusväärsed saidid ja seejärel valige **Saidid**. Sisestage jaotisesse **Lisa see veebisait tsooni** väärtus „\*\.dynamics.com” (jutumärkideta) ja seejärel valige **Lisa**. 
* Valige Internet Exploreris **Sätted** ja seejärel valige **Interneti suvandid**. Valige vahekaart **Turve**. Valige Usaldusväärsed saidid. Muutke alal, mille silt on Selle tsooni turbetase suvandi väärtuseks **Keskmine-madal**.
* Keelake hüpikakende blokeerija oma brauseris.
* Tööjaamad peavad installima Microsoft .NET Frameworki versiooni 4.6.2 või uuema. Selle Microsoft .NET Frameworki versiooni saab laadida alla ja installida [Microsofti allalaadimiskeskusest](https://www.microsoft.com/download/details.aspx?id=53345).
* Kui kasutate Chrome’i brauserit, peate aruande koostaja kliendi allalaadimiseks installima laienduse ClickOnce. Kui töötate Chrome’is inkognito-režiimis, siis veenduge, et laiendus ClickOnce oleks inkognito-režiimi jaoks aktiveeritud. Lisateavet Chrome’i laiendi ClickOkone kohta vt teemast [Pilvjuurutuste süsteeminõuded](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements).
* Kui kasutate Microsoft Edge’i Chrome’i brauseriga, ei pea te Edge Chromiumi jaoks laiendust ClickOnce installima. Samas aruandekoosturi klientrakenduse allalaadimiseks peate suvandi ClickOnce lubama. Kui töötate inkognito-režiimis, siis veenduge, et laiendus ClickOnce oleks inkognito-režiimi jaoks aktiveeritud.
     1. Avage uus brauser rakenduses Microsoft Edge.
     2. Sisestage **edge://flags** ja valige **Sisesta**.
     3. Otsige üles suvand **ClickOnce'i tugi** või kasutage otselinki **edge://flags/#edge-click-once**.
     4. Seadke rippmenüü suvandi väärtuseks **Lubatud**.
     5. Valige **Taaskäivita brauser**.

2. probleem: kasutajale ei ole määratud vajalikke lubasid rakenduse Financial Reporting kasutamiseks. 

* Et kontrollida, kas kasutajal pole luba, valige suvand **Jah** tõrkes „Rakenduse Financial Reporting serveriga ei saanud ühendada. Valige Jah, kui soovite jätkata ja määrata teise serveri aadressi.” Seejärel valige **Testi ühendust**. Kui teil pole luba, kuvatakse teade, mis ütleb: „Ühenduse loomise katse nurjus. Kasutajal pole serveriga ühenduse loomiseks vajalikke lubasid. Pöörduge süsteemiadministraatori poole.”
* Nõutavad load on loetletud ülalpool teemas [Rakendusele Financial Reporting turbejuurdepääsu võimaldamine](#granting-security-access-to-financial-reporting). Rakenduse Financial Reporting turve põhineb nendel lubadel. Teil pole juurdepääsu, kui teile pole määratud neid lubasid (või mõnda muud turberolli, mis sisaldab neid lubasid). 
* Integratsiooniülesanne **Ettevõtte kasutajate pakkuja ettevõttele** (mis vastutab ka kasutaja integreerimise eest) käivitub 5-minutilise vahemikuga. Rakenduses Financial Reporting mis tahes õiguste muudatuste jõustumiseks võib kuluda kuni 10 minutit. 
  Kui teine kasutaja saab avada aruande kujundaja, valige **Tööriistad** ja seejärel valige **Integratsiooni olek**. Kinnitage, et integratsiooni vastendamine „Ettevõtte kasutajate pakkuja ettevõttele” on edukalt käivitatud, kuna teile määrati luba rakenduse Financial Reporting kasutamiseks. 
* Võib olla võimalik, et teine tõrge takistas suvandi **Dynamicsi kasutaja integreerimine rakenduse Financial Reporting kasutajaks** lõpetamist. Võib olla ka võimalik, et andmekava lähtestamine on käivitatud ja veel lõpule viimata või ilmnes mõni muu süsteemi tõrge. Proovige protsess hiljem uuesti käivitada. Kui probleem ei lahene, pöörduge oma süsteemiadministraatori poole.

3. probleem: pääsete edasi ClickOnce'i aruande kujundaja sisselogimise lehelt, kuid ei saa aruande kujundajas sisselogimist lõpule viia. 

* Mandaadi sisestamise ajal peab peie kohalikus arvutis määratud aeg jääma viie minuti vahemikku rakenduse Financial Reporting serveris oleva ajaga. Kui erinevus on üle viie minuti, ei luba süsteem sisse logida. 
* Sellisel juhul soovitame lubada Windowsi suvandi, mis seadistab arvuti aja automaatselt. 

## <a name="additional-resources"></a>Lisaressursid
- [Finantsaruannete vaatamine](view-financial-reports.md)
- [Aruandluspuu definitsioonid finantsaruannetes](../../fin-ops-core/dev-itpro/analytics/financial-reporting-tree-definitions.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]