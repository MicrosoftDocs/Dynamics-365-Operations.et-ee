---
title: Finantsaruandlus
description: "Selles teemas kirjeldatakse kui juurdepääs Microsoft Dynamics 365 operatsioonide finantsaruandlus ja finants aruandluse võimaluste kasutamine. See sisaldab vaikimisi finantsaruanded, mida pakutakse."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d13747f17b5f382b3a530b1f166681eeec0b9d73
ms.lasthandoff: 03/31/2017


---

# <a name="financial-reporting"></a>Finantsaruandlus

Selles teemas kirjeldatakse kui juurdepääs Microsoft Dynamics 365 operatsioonide finantsaruandlus ja finants aruandluse võimaluste kasutamine. See sisaldab vaikimisi finantsaruanded, mida pakutakse.

<a name="accessing-financial-reporting"></a>Juurdepääs finantsaruandlusele
-----------------------------

Leiad selle **finantsaruandluse** menüü järgnevalt asetab Dynamics 365 toimingute puhul:

-   **Pearaamatu**&gt;**päringute ja aruannete**
-   **Eelarve koostamine**&gt;**Inquires ja aruanded**&gt;**põhilised eelarvestamine**
-   **Eelarve koostamine**&gt;**päringute ja aruannete**&gt;**eelarve planeerimine**
-   **Eelarve koostamine**&gt;**päringute ja aruannete**&gt;**eelarve kontroll**
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
| Finantsaruandluse turbe haldamine | Finantsaruandluse turbe haldamine ja administratiivtoimingute tegemine. | FinancialReportsSecurityMaintain |
| Finantsaruannete haldamine            | Finantsaruannete koostamine ja haldamine.                                  | FinancialReportsMaintainReports  |
| Finantsaruannete loomine            | Finantsaruannete loomine ja värskendamine.                                 | FinancialReportsGenerateReports  |
| Finantsaruannete vaatamine                | Finantsaruannete vaatamine.                                                 | FinancialReportsView             |

### <a name="roles"></a>Rollid

| Privileegi silt                       | Kohustus                                  | Rollid                                                                           |
|---------------------------------------|---------------------------------------|---------------------------------------------------------------------------------|
| Finantsaruandluse turbe haldamine | Finantsaruandluse turbe haldamine | Turbeadministraator                                                          |
| Finantsaruannete haldamine            | Finantsaruannete haldamine            | Pearaamatupidaja, raamatupidamise juhendaja, finantskontrolörile, eelarve juht |
| Finantsaruannete loomine            | Finantsaruannete loomine            | Tegevjuht, Finantsjuht, raamatupidaja                                                            |
| Finantsaruannete vaatamine                | Finantstulemuste ülevaatamine          | Ühtegi pole määratud                                                                   |

Pärast kasutaja lisamist või rolli muutmist peaks kasutaja mõne minuti jooksul finantsaruandlusele juurde pääsema. **Märkus:** rolli sysadmin lisatakse kõik rollid finantsaruannete.

## <a name="default-reports"></a>Vaikearuanded
Finantsaruandlus pakub 22 vaike-finantsaruannet. Iga aruande kasutab põhikonto Vaikekategooriate Dynamics 365 toiminguteks. Saate kasutada neid aruandeid olemasoleval kujul või finantsaruandluse vajaduste lähtepunktina. Lisaks tavalistele finantsaruannetele nagu kasumiaruanne ja bilanss sisaldavad need vaikearuanded aruandeid, millel on näidatud erinevat tüüpi finantsaruanded, mida saate koostada. Iga aruande tabel järgnevatelt Office Mixi esitluse kohta aruande.

| Vaikearuanne                                                                                         | Kirjeldus                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [12 Month Rolling Single Column Income Statement – Default](https://mix.office.com/watch/76kc7bm3wnt1) | Vaadake organisatsiooni tulusust viimase 12 kuu jooksul ühes veerus.                                                                                                                                                                                                                                      |
| [12 Month Trend Income Statement – Default](https://mix.office.com/watch/12brmfge5p8r)                 | Vaadake organisatsiooni tulusust iga viimase 12 kuu kohta. Need 12 kuud võivad hõlmata rohkem kui ühte rahandusaastat.                                                                                                                                                                                             |
| [Actual vs Budget – Default](https://mix.office.com/watch/fi439lkwr0no)                                | Vaadake kõigi algse eelarve kontode üksikasjalikku saldoteavet ja võrrelge parandatud eelarvet tegelike hälbega summadega.                                                                                                                                                                          |
| [Audit Details – Default](https://mix.office.com/watch/1i15nzd3nwkyh)                                  | Saate vaadata kõigi kontode üksikasjalikku saldoteavet. Selles aruandes kuvatakse deebet- ja kreeditsaldod aruandlusvaluutas ja kohalikus valuutas koos täiendava kandeteabega, nt kasutaja ID, andmeid viimati muutnud kasutaja, viimase muutmise kuupäev ja töölehe ID. |
| [Balance List – Default](https://mix.office.com/watch/1kezwu2a10fq4)                                   | Saate vaadata kõigi kontode üksikasjalikku saldoteavet. Selles aruandes kuvatakse avamis- ja sulgemissaldod ning deebet- ja kreeditsaldod praeguse perioodi ja möödunud aasta kohta koos täiendavat kandeteabega (nt kanne).                                                                    |
| [Balance Sheet – Default](https://mix.office.com/watch/zkgq0u7visw9)                                   | Saate vaadata organisatsiooni aasta rahalist seisu.                                                                                                                                                                                                                                                             |
| [Balance Sheet and Income Statement Side by Side - Default](https://mix.office.com/watch/zkgq0u7visw9) | Saate vaadata kõrvuti organisatsiooni aasta finantsseisundit ja tulusust.                                                                                                                                                                                                                              |
| [Cash Flow – Default](https://mix.office.com/watch/jd3go9pz6390)                                       | Saate ülevaate organisatsiooni sissetulevast ja väljuvast sularahast.                                                                                                                                                                                                                                   |
| [Detailed JE and TB Review – Default](https://mix.office.com/watch/1sw9fmtwgjb1f)                      | Saate kuvada kõigi kontode algsaldo ja tegevuse teabe.                                                                                                                                                                                                                                                      |
| [Detailed Trial Balance - Default](https://mix.office.com/watch/1ewwgbpv0iwrl)                         | Saate vaadata kõigi deebet- ja kreeditsaldodega kontode saldoteavet ja nende saldode netoväärtust koos kande kuupäeva, kande ja töölehe kirjeldusega.                                                                                                                                  |
| [Expenses Three Year Quarterly Trend – Default](https://mix.office.com/watch/gwm4zu7tmtj8)             | Saate ülevaate viimase 12 kvartali kuludest kolme viimase aasta jooksul.                                                                                                                                                                                                                                   |
| [Financial Captions JE and TB Review – Default](https://mix.office.com/watch/1sw9fmtwgjb1f)            | Saate vaadata ülevaadet saldodest ja tegevustest vara, kohustuse, omakapitali, tulu, kulu, kasumi või kahjumi finantspealdiste kohta.                                                                                                                                                                           |
| [Income Statement – Default](https://mix.office.com/watch/sbuhgl5hzuhi)                                | Saate vaadata organisatsiooni tulusust praeguse perioodi ja aasta puhul kuni praeguse kuupäevani.                                                                                                                                                                                                                                   |
| [Ledger Transaction List – Default](https://mix.office.com/watch/19h9v2rmh48vy)                        | Saate vaadata kõigi kontode üksikasjalikku saldoteavet. Selles aruandes kuvatakse deebet- ja kreeditsaldod koos täiendava kandeteabega, nt kandekuupäev, töölehe number, kanne, sisestustüüp ja jälgimisnumber.                                                                            |
| [Ratios – Default](https://mix.office.com/watch/b08hfc5h92me)                                          | Saate vaadata organisatsiooni maksejõulisust, tulusust ja efektiivsuse suhtarve aasta kohta.                                                                                                                                                                                                                           |
| [Rolling 12 Month Expenses – Default](https://mix.office.com/watch/iywod5qmqhz7)                       | Saate ülevaate kuludest viimase 12 kuu kohta. Need 12 kuud võivad hõlmata rohkem kui ühte rahandusaastat.                                                                                                                                                                                                       |
| [Rolling Quarter Income Statement – Default](https://mix.office.com/watch/1k4yl6a6oyxqc)               | Vaata organisatsiooni kasumlikkuse kvartalis möödunud aasta ja aasta tänaseni.                                                                                                                                                                                                                   |
| [Side by Side Balance Sheet – Default](https://mix.office.com/watch/zkgq0u7visw9)                      | Saate vaadata organisatsiooni aasta rahalist seisu. Selles aruandes kuvatakse varad ja kohustused ning omakapital kõrvuti.                                                                                                                                                                                |
| [Summary Trial Balance – Default](https://mix.office.com/watch/1ewwgbpv0iwrl)                          | Saate vaadata bilansi teavet kõigi avamis- ja sulgemissaldode ning deebet- ja kreeditsaldodega kontode puhul koos nende netoerinevusega.                                                                                                                                                                  |
| [Summary Trial Balance Year Over Year – Default](https://mix.office.com/watch/1ewwgbpv0iwrl)           | Saate tasakaalu andmeid kõik kontod, mis on jooksval aastal ja möödunud aasta avamine ja lõppbilanssi ja deebet- ja kreeditsaldode koos nende neto erinevus.                                                                                                                           |
| [Weekly Sales and Discounts - Default](https://mix.office.com/watch/112ng0hy5de0j)                     | Saate ülevaate kuu iga nädala müügist ja allahindlustest. See aruanne sisaldab kokku nelja nädalat.                                                                                                                                                                                                              |
| [Eelarve vahendeid - vaikimisi](https://mix.office.com/watch/15hcpezcbx7tv)                         | Vaata muudetud eelarve, tegelikud kulud, eelarve broneerimine ja eelarve vahendeid kõigi kontode üksikasjalikult võrrelda                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Finantsaruannete avamine
Kui klõpsate menüüd **Finantsaruandlus**, kuvatakse ettevõtte vaike-finantsaruannete loend. Seejärel saate aruande avada või seda muuta. Mõne vaikearuande avamiseks valige aruande nimi. Aruande esmakordsel avamisel koostatakse see automaatselt eelmise kuu kohta. Näiteks kui avate aruande esimest korda augustis 2016, luuakse aruanne 31 juuli 2016. Pärast aruande avamist saab seda uurida, minnes süvitsi konkreetsetes andmehulkades ja muutes aruande valikuid.

## <a name="creating-and-modifying-financial-reports"></a>Finantsaruannete koostamine ja muutmine
Finantsaruannete loendist saate luua uue aruande või muuta olemasolevat aruannet. Kui teil on vastavad õigused, saate luua uue finantsaruande klõpsates **uus** Updatehagi paani. Aruande disainer programm on loendi. Peale Aruandekujundaja hakkab seejärel saate luua uue aruande. Pärast uue aruande salvestamist kuvatakse see finantsaruannete loendis. Loendis kuvatakse ainult aruandeid, mis on loodud ettevõte, mis kasutamisel Dynamics 365 toiminguteks. Lisateavet protsessi ning luua ja muuta finantsaruanded Dynamics 365 operatsioonide viitavad need [blogi postitusi](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/tag/learning/) : dünaamika rahaline aruandlus blogi. **Märkus:** arvuti, allalaaditavate disainer klient peab olema installitud Microsoft .NET Frameworki versiooni 4.6.2 aruande. Microsoft .NET Frameworki versiooni allalaaditavate ja paigaldatud [siin](https://www.microsoft.com/en-us/download/details.aspx?id=53345). Kui kasutate Chrome'i, installige ClickOnce'i laiendamine et alla aruande disainer klient. Kui kasutate inkognito režiimis, veenduge, et ClickOnce'i laiendamine on lubatud inkognito režiimis. Finantsaruannete loendis kuvatavat aruannet saab ka muuta. Kui on valitud aruande nime ümber olev ala, klõpsake tegumiribal nuppu **Redigeeri**. Käivitub aruande koostamise programm.

<a name="see-also"></a>Vt ka
--------

[View financial reports](view-financial-reports.md)

[Dynamicsi finantsaruandluse ajaveeb](http://blogs.msdn.com/b/dynamics_financial_reporting/)


