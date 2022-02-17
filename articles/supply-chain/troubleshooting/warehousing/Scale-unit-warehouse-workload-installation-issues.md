---
title: Töötlemisprobleemid ilmnevad pärast skaalaüksuse lao töökoormuse installimist
description: Selles teemas kirjeldatakse probleeme, mis võivad ilmneda varsti pärast skaalaüksuse lao töökoormuse installimist, ja antakse nõu nende parandamiseks.
author: perlynne
ms.date: 1/13/2022
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningWorkbench, WHSOutboundLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-01-13
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: f589ffed61b695f471989ab1dd693f30cd5d5262
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071771"
---
# <a name="processing-issues-occur-after-a-scale-unit-warehouse-workload-is-installed"></a>Töötlemisprobleemid ilmnevad pärast skaalaüksuse lao töökoormuse installimist

Selles teemas kirjeldatakse probleeme, mis võivad ilmneda varsti pärast skaalaüksuse lao töökoormuse installimist, ja antakse nõu nende parandamiseks.

## <a name="issue-1-error-after-a-load-is-released-from-a-load-planning-workbench"></a>1. probleem: viga pärast koormuse vabastamist koormuse planeerimise tööpingist

### <a name="symptoms-of-issue-1"></a>Probleemi sümptomid 1

Kui vabastate koormuse **lehelt Koormuse planeerimise töölaud** või **Väljaminev koormuse plaanimise töölaud**, kuvatakse tõrketeade, millel on järgmine vorm.

> Koorma %1 sisestamisel ilmnes erand, koormat ei saanud vabastada.
> 
> UPDATE WHSSHIPMENTTABLE KOMPLEKT...
> 
> Kirjet ei saa redigeerida lähetustes (WHSShipmentTable). Saadetise ID: ...

Siin on tegelik näide, mis sisaldab näidisandmeid:

> Koormuse USMF-000033 postitamisel jäi erand vahele, koormust ei saanud vabastada.
Seanss 5133 (Administraator)
>
> UPDATE WHSSHIPMENTTABLE SET ORDERNUM=?,RECVERSION=?,MODIFIEDDATETIME=?,MODIFIEDBY=? KUS ((RECID=?) JA (RECVERSION=?))  
> [Microsoft] [ODBC Driver 17 FOR SQL Server] [SQL Server] Skaalaüksus @@ proovis uuendada skaalaühiku @A kuuluvaid kirjeid.  
> Object Server Azure:
>
> Kirjet ei saa redigeerida lähetustes (WHSShipmentTable). Saadetise ID: USMF-000031, USMF-000033. SQL-andmebaas väljastas vea.

### <a name="cause-of-issue-1"></a>Probleemi põhjus 1

See probleem võib ilmneda, kui skaala ühiku lao töökoormuse installimisel on olemas järgmine tingimuste kombinatsioon.

- Süsteem sisaldab avaldamata koormust, kus mitu rida on seotud erinevate tellimustega ja mõned koormusread pole saadetisega seotud.
- Süsteem on seadistatud kasutama saadetiste konsolideerimist.

Hajutatud hübriidtiroloogia juurutamisel märgitakse iga koormuse ja saadetise kirje kindla skaalaüksuse või jaoturi omandiks. Kui vabastate koormuse **lehelt Koormuse planeerimise töölaud**, muudab süsteem määratud omandiõigust. Kuid varem loetletud tingimuste tõttu ei pruugi süsteem andmete omandiõigust lahendada. Seetõttu ei vabasta see koormust lattu.

### <a name="resolution-of-issue-1"></a>1. küsimuse lahendamine

Enne lattu vabastamist jagage koormus kaheks väiksemaks koormaks.

## <a name="issue-2-error-while-a-wave-is-processed-on-a-scale-unit"></a>2. probleem: viga laine töötlemisel skaalaühikus

### <a name="symptoms-of-issue-2"></a>Probleemi sümptomid 2

Kui töötlete lainet skaalaühikus, kuvatakse tõrketeade, millel on järgmine vorm.

> Resid = %1, koormuse ID= %2 koormusrida ei saa muuta, kuna see kuulub endiselt ettevõtte jaoturile. Veenduge, et vastav väljaminev koormus on vabastatud skaalaühikule ja seeläbi loodud laotellimuse ridadele.

Siin on tegelik näide, mis sisaldab näidisandmeid:

> Infolog töö jaoks Käivita laine USMF-000000012 (9223377668365210)  
> Ülesande infolog Käivita laine USMF-000000012 (9223377668370462)  
> Resid = 68719478242, koormuse ID= USMF-000034 ei saa muuta koormusrida, kuna see kuulub endiselt ettevõtte jaoturile. Veenduge, et vastav väljaminev koormus on vabastatud skaalaühikule ja seeläbi loodud laotellimuse ridadele.

### <a name="cause-of-issue-2"></a>Probleemi põhjus 2

Hajutatud hübriid-topoloogia juurutamisel määratakse koormuse ja saadetise andmete omamine kindlale skaalaüksusele või jaoturile. Lehvitamise töötlemise osana eeldatakse, et andmete omamine määratakse skaalaüksusele.

Kui installite skaalaüksuse lao töökoormuse, kui avatud saadetis on seotud koormuse ja lainega, ei saa süsteem andmeomandit kontrollida. Seetõttu ebaõnnestub laine töötlemine skaalaüksusel.

### <a name="resolution-of-issue-2"></a>2. küsimuse lahendamine

Vabastage koormus jaoturist lattu.

## <a name="troubleshoot-issues-by-viewing-a-records-ownership-and-destination"></a>Probleemide tõrkeotsing kirje omandiõiguse ja sihtkoha vaatamisel

Hajutatud hübriid-topoloogia juurutamisel märgitakse mitut tüüpi kirjed kindla skaalaüksuse või jaoturi omandiks. Pärast hajutatud hübriidtiroloogiale üleminekut ja/või uue skaalaüksuse lao töökoormuse seadistamist määrab süsteem omandiõiguse igale asjakohasele kirjele. See protsess võib mõnikord põhjustada vigu või ootamatuid tulemusi. Seetõttu aitab teave kirje omandiõiguse ja ülekande sihtkoha kohta tõrkeotsingut probleemide korral, mis ilmnevad pärast seda tüüpi muudatuste tegemist.

Kirje omandiõiguse ja üleviimise sihtkoha vaatamiseks tehke järgmist.

1. Avage vastav kirje.
1. Valige toimingupaani menüü Suvandid **jaotises Kirjeteave** suvand **Kuva kõik väljad**.**·**
1. Kuvataval lehel kuvatakse kõigi valitud kirje jaoks saadaolevate väljade väärtused. Vaadake üle järgmised väljad.

    - **SYSSCALEUNITID** – see väli näitab kirje praegust omanikku.
    - **SYSTARGETSCALEUNITID** – sellel väljal kuvatakse jaoturi või skaalaüksuse skaalaühiku ID, millele kirje üle kantakse, kui praegune omanik on sellega töötamise lõpetanud. Selle välja väärtust kasutavad seda tüüpi protsessi haldavad pakett-tööd. Kuigi see väli pole otseselt omandiõigusega seotud, võib kirje ülekandmisel omandiõigus muutuda. Mõnel juhul on see väli tühi.
