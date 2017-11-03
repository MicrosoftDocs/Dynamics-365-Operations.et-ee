---
title: Finantsaruandlus
description: "Selles teemas kirjeldatakse, kus pääseda juurde rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition finantsaruandlusele ja kuidas finantsaruandluse võimalusi kasutada. See sisaldab pakutavate vaike-finantsaruannete kirjeldust."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ed207bdc04041ec2f21cb1038451fc75b8d061a1
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="financial-reporting"></a>Finantsaruandlus

[!include[banner](../includes/banner.md)]


Selles teemas kirjeldatakse, kus pääseda juurde rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition finantsaruandlusele ja kuidas finantsaruandluse võimalusi kasutada. See sisaldab pakutavate vaike-finantsaruannete kirjeldust.

<a name="accessing-financial-reporting"></a>Juurdepääs finantsaruandlusele
-----------------------------

Menüü **Finantsaruandlus** leiate rakenduses Finance and Operations järgmistest kohtadest.

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
| Finantsaruandluse turbe haldamine | Finantsaruandluse turbe haldamine ja administratiivtoimingute tegemine. | FinancialReportsSecurityMaintain |
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

## <a name="default-reports"></a>Vaikearuanded
Finantsaruandlus pakub 22 vaike-finantsaruannet. Iga aruanne kasutab rakenduses Finance and Operations põhikonto vaikekategooriaid. Saate kasutada neid aruandeid olemasoleval kujul või finantsaruandluse vajaduste lähtepunktina. Lisaks tavalistele finantsaruannetele nagu kasumiaruanne ja bilanss sisaldavad need vaikearuanded aruandeid, millel on näidatud erinevat tüüpi finantsaruanded, mida saate koostada. Iga aruanne järgmises tabelis on lingitud Office Mixi esitlusega aruande kohta.

| Vaikearuanne                                                                                         | Kirjeldus                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [12 kuu jooksev ühe veeruga kasumiaruanne – vaikimisi](https://mix.office.com/watch/76kc7bm3wnt1) | Vaadake organisatsiooni tulusust viimase 12 kuu jooksul ühes veerus.                                                                                                                                                                                                                                      |
| [12 kuu trendi kasumiaruanne – vaikimisi](https://mix.office.com/watch/12brmfge5p8r)                 | Vaadake organisatsiooni tulusust iga viimase 12 kuu kohta. Need 12 kuud võivad hõlmata rohkem kui ühte rahandusaastat.                                                                                                                                                                                             |
| [Tegelik võrreldes eelarvega – vaikimisi](https://mix.office.com/watch/fi439lkwr0no)                                | Vaadake kõigi algse eelarve kontode üksikasjalikku saldoteavet ja võrrelge parandatud eelarvet tegelike hälbega summadega.                                                                                                                                                                          |
| [Auditi üksikasjad – vaikimisi](https://mix.office.com/watch/1i15nzd3nwkyh)                                  | Saate vaadata kõigi kontode üksikasjalikku saldoteavet. Selles aruandes kuvatakse deebet- ja kreeditsaldod aruandlusvaluutas ja kohalikus valuutas koos täiendava kandeteabega, nt kasutaja ID, andmeid viimati muutnud kasutaja, viimase muutmise kuupäev ja töölehe ID. |
| [Saldoloend – vaikimisi](https://mix.office.com/watch/1kezwu2a10fq4)                                   | Saate vaadata kõigi kontode üksikasjalikku saldoteavet. Selles aruandes kuvatakse avamis- ja sulgemissaldod ning deebet- ja kreeditsaldod praeguse perioodi ja möödunud aasta kohta koos täiendavat kandeteabega (nt kanne).                                                                    |
| [Bilanss – vaikimisi](https://mix.office.com/watch/zkgq0u7visw9)                                   | Saate vaadata organisatsiooni aasta rahalist seisu.                                                                                                                                                                                                                                                             |
| [Kõrvuti konsolideeritud bilanss ja kasumiaruanne – vaikimisi](https://mix.office.com/watch/zkgq0u7visw9) | Saate vaadata kõrvuti organisatsiooni aasta finantsseisundit ja tulusust.                                                                                                                                                                                                                              |
| [Rahavoog – vaikimisi](https://mix.office.com/watch/jd3go9pz6390)                                       | Saate ülevaate organisatsiooni sissetulevast ja väljuvast sularahast.                                                                                                                                                                                                                                   |
| [Üksikasjalik JE ja TB ülevaade – vaikimisi](https://mix.office.com/watch/1sw9fmtwgjb1f)                      | Saate kuvada kõigi kontode algsaldo ja tegevuse teabe.                                                                                                                                                                                                                                                      |
| [Üksikasjalik proovibilanss – vaikimisi](https://mix.office.com/watch/1ewwgbpv0iwrl)                         | Saate vaadata kõigi deebet- ja kreeditsaldodega kontode saldoteavet ja nende saldode netoväärtust koos kande kuupäeva, kande ja töölehe kirjeldusega.                                                                                                                                  |
| [Kulude kolme aasta kvartalitrend – vaikimisi](https://mix.office.com/watch/gwm4zu7tmtj8)             | Saate ülevaate viimase 12 kvartali kuludest kolme viimase aasta jooksul.                                                                                                                                                                                                                                   |
| [Finantspealdised: JE ja TB ülevaade – vaikimisi](https://mix.office.com/watch/1sw9fmtwgjb1f)            | Saate vaadata ülevaadet saldodest ja tegevustest vara, kohustuse, omakapitali, tulu, kulu, kasumi või kahjumi finantspealdiste kohta.                                                                                                                                                                           |
| [Kasumiaruanne – vaikimisi](https://mix.office.com/watch/sbuhgl5hzuhi)                                | Saate vaadata organisatsiooni tulusust praeguse perioodi ja aasta puhul kuni praeguse kuupäevani.                                                                                                                                                                                                                                   |
| [Pearaamatukannete loend – vaikimisi](https://mix.office.com/watch/19h9v2rmh48vy)                        | Saate vaadata kõigi kontode üksikasjalikku saldoteavet. Selles aruandes kuvatakse deebet- ja kreeditsaldod koos täiendava kandeteabega, nt kandekuupäev, töölehe number, kanne, sisestustüüp ja jälgimisnumber.                                                                            |
| [Suhtarvud – vaikimisi](https://mix.office.com/watch/b08hfc5h92me)                                          | Saate vaadata organisatsiooni maksejõulisust, tulusust ja efektiivsuse suhtarve aasta kohta.                                                                                                                                                                                                                           |
| [Jooksva 12 kuu kulud – vaikimisi](https://mix.office.com/watch/iywod5qmqhz7)                       | Saate ülevaate kuludest viimase 12 kuu kohta. Need 12 kuud võivad hõlmata rohkem kui ühte rahandusaastat.                                                                                                                                                                                                       |
| [Jooksva kvartali kasumiaruanne – vaikimisi](https://mix.office.com/watch/1k4yl6a6oyxqc)               | Vaadake organisatsiooni tulusust kvartalis eelmise aasta kohta ja aasta kohta tänase kuupäevani.                                                                                                                                                                                                                   |
| [Kõrvuti bilanss – vaikimisi](https://mix.office.com/watch/zkgq0u7visw9)                      | Saate vaadata organisatsiooni aasta rahalist seisu. Selles aruandes kuvatakse varad ja kohustused ning omakapital kõrvuti.                                                                                                                                                                                |
| [Proovibilansi kokkuvõte – vaikimisi](https://mix.office.com/watch/1ewwgbpv0iwrl)                          | Saate vaadata bilansi teavet kõigi avamis- ja sulgemissaldode ning deebet- ja kreeditsaldodega kontode puhul koos nende netoerinevusega.                                                                                                                                                                  |
| [Proovibilansi kokkuvõte aasta-aastalt – vaikimisi](https://mix.office.com/watch/1ewwgbpv0iwrl)           | Saate vaadata bilansi teavet kõigi avamis- ja sulgemissaldode ning deebet- ja kreeditsaldodega kontode puhul koos nende netoerinevusega praeguse aasta ja möödunud aasta kohta.                                                                                                                           |
| [Nädala müük ja allahindlused – vaikimisi](https://mix.office.com/watch/112ng0hy5de0j)                     | Saate ülevaate kuu iga nädala müügist ja allahindlustest. See aruanne sisaldab kokku nelja nädalat.                                                                                                                                                                                                              |
| [Saadaolevad eelarvefondid – vaikesäte](https://mix.office.com/watch/15hcpezcbx7tv)                         | Saate vaadata üksikasjalikku võrdlust muudetud eelarve, tegelike kulude, eelarvereservide ja eelarvefondide vahel kõigi kontode kohta                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Finantsaruannete avamine
Kui klõpsate menüüd **Finantsaruandlus**, kuvatakse ettevõtte vaike-finantsaruannete loend. Seejärel saate aruande avada või seda muuta. Mõne vaikearuande avamiseks valige aruande nimi. Aruande esmakordsel avamisel koostatakse see automaatselt eelmise kuu kohta. Näiteks kui avate aruande esmakordselt augustis 2016, koostatakse aruanne 31. juuli 2016 kohta. Pärast aruande avamist saab seda uurida, minnes süvitsi konkreetsetes andmehulkades ja muutes aruande valikuid.

## <a name="creating-and-modifying-financial-reports"></a>Finantsaruannete koostamine ja muutmine
Finantsaruannete loendist saate luua uue aruande või muuta olemasolevat aruannet. Kui teil on olemas vastavad load, saate koostada uue finantsaruande, klõpsates tegumiribal nuppu **Uus**. Aruande koostamise programm laaditakse teie seadmesse. Kui aruandekoostur on käivitunud, saate koostada uue aruande. Pärast uue aruande salvestamist kuvatakse see finantsaruannete loendis. Loendis kuvatakse ainult need aruanded, mis on loodud ettevõttele, mida Finance and Operationsis kasutate. Lisateavet finantsaruannete koostamise ja muutmise kohta rakenduses Finance and Operationsleiate neist [ajaveebipostitustest](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/tag/learning/) Dynamicsi finantsaruandluse ajaveebis. **Märkus:** arvutisse, kuhu aruandekoosturi alla laadite, peab olema installitud Microsoft .NET Frameworki versioon 4.6.2. Selle Microsoft .NET Frameworki versiooni saab laadida alla ja installida [siit](https://www.microsoft.com/en-us/download/details.aspx?id=53345). Kui kasutate Chrome’i, peate aruandekoosturi kliendi allalaadimiseks installima laienduse ClickOnce. Kui töötate inkognito-režiimis, siis veenduge, et laiendus ClickOnce oleks inkognito-režiimi jaoks aktiveeritud. Finantsaruannete loendis kuvatavat aruannet saab ka muuta. Kui on valitud aruande nime ümber olev ala, klõpsake tegumiribal nuppu **Redigeeri**. Käivitub aruande koostamise programm.

<a name="see-also"></a>Vt ka
--------

[Finantsaruannete vaatamine](view-financial-reports.md)

[Dynamicsi finantsaruandluse ajaveeb](http://blogs.msdn.com/b/dynamics_financial_reporting/)




