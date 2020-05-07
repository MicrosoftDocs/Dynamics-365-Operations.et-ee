---
title: Finantsaruandluse ülevaade
description: Selles teemas kirjeldatakse, kus pääseda juurde rakenduse Microsoft Dynamics 365 Finance finantsaruandlusele ja kasutada finantsaruandluse võimalusi. See sisaldab pakutavate vaike-finantsaruannete kirjeldust.
author: aprilolson
manager: AnnBe
ms.date: 04/14/2020
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
ms.openlocfilehash: 6cd77e22f9c6f90f6aa9934d70a121008e1274dd
ms.sourcegitcommit: 5419f2b8f51cd5de55be66d1389b5b9d7771fd52
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/15/2020
ms.locfileid: "3262645"
---
# <a name="financial-reporting-overview"></a>Finantsaruandluse ülevaade

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kus pääseda juurde finantsaruandlusele ja kasutada finantsaruandluse võimalusi. See sisaldab ka pakutavate vaike-finantsaruannete kirjeldust.

<a name="accessing-financial-reporting"></a>Juurdepääs finantsaruandlusele
-----------------------------

Menüü **Finantsaruandlus** leiate järgmistest kohtadest.

-   **Pearaamat** &gt; **Päringud ja aruanded**
-   **Eelarvestamine** &gt; **Päringud ja aruanded** &gt; **Põhiline eelarvestamine**
-   **Eelarvestamine** &gt; **Päringud ja aruanded** &gt; **Eelarve plaanimine**
-   **Eelarvestamine** &gt; **Päringud ja aruanded** &gt; **Eelarve juhtimine**
-   Konsolideerimised

Finantsaruannete loomiseks ja genereerimiseks juriidilisele isikule tuleb seadistada sellele juriidilisele isikule järgmine teave.

-   Rahanduskalender
-   Pearaamat
-   Kontoplaan
-   Valuuta

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

Pärast kasutaja lisamist või rolli muutmist peaks kasutaja mõne minuti jooksul finantsaruandlusele juurde pääsema. **Märkus:** süsteemiadministraatori roll lisatakse finantsaruandluses kõigile rollidele.

## <a name="report-deletions-and-expirations"></a>Aruande kustutamised ja aegumised
Aruande loonud kasutajad saavad oma aruandeid kustutada. Kohustusega **Finantsaruandluse turbe haldamine** kasutajad saavad kustutada teiste aruandeid. 

Versioonis 10.0.8 lisati aegumiskuupäevad. Uus nõutav funktsioon lubatakse funktsioonihalduse tööruumis lehel **Kõik**. Funktsioon **Finantsaruannete säilitamise poliitikad** sisaldab järgmisi muudatusi.
* Uued loodud aruanded märgitakse automaatselt, et neil on loomise ajast 90 päeva pärast aegumiskuupäev
* Kõikidele aruannetele, mis olid olemas enne funktsiooni installimist, antakse 90-päevane aegumisperiood. Kuupäev võidakse lühikest aega kuvada tühjana, kuni finantsaruandluse teenus töötab, luuakse aruanne ja teenus värskendab olemasolevaid tühjade aegumiskuupäevadega aruandeid. 
* **Finantsaruandluse turbe haldamise** kohustusega kasutajatel on juurdepääs sellele funktsioonile. Kõik kohustusega **Finantsaruannete haldamine** kasutad, kellele on antud privileeg **Finantsaruannete aegumise haldamine**, omavad võimalust aegumiskuupäeva muuta. Praegu on saadaval kaks säilitamise võimalust. 
  * Aegumine 90 päeva möödudes.
  * Võimalus seada aruanne mitte kunagi aeguma.
  
Hilisemas funktsioonis kaalutakse täiendavaid võimalusi. Aegumine 90 päeva möödudes on vaikesäte ja sobivate lubadega kasutajad saavad seda **Finantsaruannete** loendi lehel muuta.    
  
Kui valitud on aegumine (nt 90 päeva), annab see 90 päeva alates tänasest, mis on erinev käitumine kui 90 päeva alates algsest loomise kuupäevast, mis on määratud aruande koostamise ajal. 

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
| Üksikasjalik proovibilanss – vaikimisi                         | Saate vaadata kõigi deebet- ja kreeditsaldodega kontode saldoteavet ja nende saldode netoväärtust koos kande kuupäeva, kande ja töölehe kirjeldusega.                                                                                                                                  |
| Kulude kolme aasta kvartalitrend – vaikimisi             | Saate ülevaate viimase 12 kvartali kuludest kolme viimase aasta jooksul.                                                                                                                                                                                                                                   |
| Finantspealdised: JE ja TB ülevaade – vaikimisi            | Saate vaadata ülevaadet saldodest ja tegevustest vara, kohustuse, omakapitali, tulu, kulu, kasumi või kahjumi finantspealdiste kohta.                                                                                                                                                                           |
| Kasumiaruanne – vaikimisi                                | Saate vaadata organisatsiooni tulusust praeguse perioodi ja aasta puhul kuni praeguse kuupäevani.                                                                                                                                                                                                                                   |
| Pearaamatukannete loend – vaikimisi                        | Saate vaadata kõigi kontode üksikasjalikku saldoteavet. Selles aruandes kuvatakse deebet- ja kreeditsaldod koos täiendava kandeteabega, nt kandekuupäev, töölehe number, kanne, sisestustüüp ja jälgimisnumber.                                                                            |
| Suhtarvud – vaikimisi                                          | Saate vaadata organisatsiooni maksejõulisust, tulusust ja efektiivsuse suhtarve aasta kohta.                                                                                                                                                                                                                           |
| Jooksva 12 kuu kulud – vaikimisi                       | Saate ülevaate kuludest viimase 12 kuu kohta. Need 12 kuud võivad hõlmata rohkem kui ühte rahandusaastat.                                                                                                                                                                                                       |
| Jooksva kvartali kasumiaruanne – vaikimisi               | Vaadake organisatsiooni tulusust kvartalis eelmise aasta kohta ja aasta kohta tänase kuupäevani.                                                                                                                                                                                                                   |
| Kõrvuti bilanss – vaikimisi                      | Saate vaadata organisatsiooni aasta rahalist seisu. Selles aruandes kuvatakse varad ja kohustused ning omakapital kõrvuti.                                                                                                                                                                                |
| Proovibilansi kokkuvõte – vaikimisi                          | Saate vaadata bilansi teavet kõigi avamis- ja sulgemissaldode ning deebet- ja kreeditsaldodega kontode puhul koos nende netoerinevusega.                                                                                                                                                                  |
| Proovibilansi kokkuvõte aasta-aastalt – vaikimisi           | Saate vaadata bilansi teavet kõigi avamis- ja sulgemissaldode ning deebet- ja kreeditsaldodega kontode puhul koos nende netoerinevusega praeguse aasta ja möödunud aasta kohta.                                                                                                                           |
| Nädala müük ja allahindlused – vaikimisi                     | Saate ülevaate kuu iga nädala müügist ja allahindlustest. See aruanne sisaldab kokku nelja nädalat.                                                                                                                                                                                                              |
| Saadaolevad eelarvefondid – vaikesäte                         | Saate vaadata üksikasjalikku võrdlust muudetud eelarve, tegelike kulude, eelarvereservide ja eelarvefondide vahel kõigi kontode kohta                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Finantsaruannete avamine
Kui klõpsate menüüd **Finantsaruandlus**, kuvatakse ettevõtte vaike-finantsaruannete loend. Seejärel saate aruande avada või seda muuta. Mõne vaikearuande avamiseks valige aruande nimi. Aruande esmakordsel avamisel koostatakse see automaatselt eelmise kuu kohta. Näiteks kui avate aruande esmakordselt augustis 2016, koostatakse aruanne 31. juuli 2016 kohta. Pärast aruande avamist saab seda uurida, minnes süvitsi konkreetsetes andmehulkades ja muutes aruande valikuid.

## <a name="creating-and-modifying-financial-reports"></a>Finantsaruannete koostamine ja muutmine
Finantsaruannete loendist saate luua uue aruande või muuta olemasolevat aruannet. Kui teil on olemas vastavad load, saate koostada uue finantsaruande, klõpsates tegumiribal nuppu **Uus**. Aruande koostamise programm laaditakse teie seadmesse. Kui aruandekoostur on käivitunud, saate koostada uue aruande. Pärast uue aruande salvestamist kuvatakse see finantsaruannete loendis. Loendis kuvatakse ainult need aruanded, mis on loodud ettevõttele, mida Rahanduses kasutate. 

> [!NOTE] 
> Arvutisse, kuhu aruandekoosturi alla laadite, peab olema installitud Microsoft .NET Frameworki versioon 4.6.2. Selle Microsoft .NET Frameworki versiooni saab laadida alla ja installida [Microsofti allalaadimiskeskusest](https://www.microsoft.com/download/details.aspx?id=53345). Kui kasutate Chrome’i, peate aruandekoosturi kliendi allalaadimiseks installima laienduse ClickOnce. Kui töötate inkognito-režiimis, siis veenduge, et laiendus ClickOnce oleks inkognito-režiimi jaoks aktiveeritud. Finantsaruannete loendis kuvatavat aruannet saab ka muuta. Kui on valitud aruande nime ümber olev ala, klõpsake tegumiribal nuppu **Redigeeri**. Käivitub aruande koostamise programm.

## <a name="additional-resources"></a>Lisaressursid
- [Finantsaruannete vaatamine](view-financial-reports.md)



