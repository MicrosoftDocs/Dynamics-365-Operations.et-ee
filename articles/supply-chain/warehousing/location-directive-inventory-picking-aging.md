---
title: Asukohakorralduse varude komplekteerimise ajaline jaotus
description: Selles teemas selgitatakse, kuidas kasutada komplekteerimise ajal asukohakorralduse strateegiaid esimesena sisse, esimesena välja (FIFO) ja viimasena sisse, esimesena välja (LIFO).
author: mirzaab
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile,WHSWorkTable,WHSWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 937af7e24fc72b5b8bc741857913899a239a64d3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835530"
---
# <a name="location-directive-inventory-picking-aging"></a>Asukohakorralduse varude komplekteerimise ajaline jaotus

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas kasutada komplekteerimise ajal asukohakorralduse strateegiaid esimesena sisse, esimesena välja (FIFO) ja viimasena sisse, esimesena välja (LIFO). Need strateegiad töötavad koos aegumiskuupäevadega, mis salvestati jälgitavate asukohtadena, kui varud esmakordselt lattu sisenesid. Funktsioon *Asukohakorralduse varude komplekteerimise aegumine* kasutab aegumise määramisel asukoha kuupäeva. Funktsioon *Lao asukoha olek* värskendab asukoha kuupäeva identifitseerimisnumbri kuupäeva põhjal.

Saate kasutada FIFO- ja LIFO-strateegiaid, et saata nii partii jälgimisega kui ka partii jälgimiseta kaupu, sisestatud kuupäeva alusel, kui varud sisenesid lattu. See võimalus võib olla eriti kasulik partii jälitamiseta varude puhul, mille aegumiskuupäev pole sortimiseks kasutamiseks saadaval.

Varude esmakordsel vastuvõtmisel või loomisel laos, värskendab süsteem vastavat identifitseerimisnumbrit, et praegust kuupäeva kuvataks aegumiskuupäevana. Seda kuupäeva kasutatavad seejärel asukohakorralduse strateegiad kõige vanemate või uuemate varude tuvastamiseks laos. Kui varud teisaldatakse asukohta, mida ei jälgita identifitseerimisnumbri alusel, värskendatakse asukohta ennast aegumise teabega ja seda teavet kasutavad seejärel strateegiad.

## <a name="turn-on-the-feature"></a>Funktsiooni sisselülitamine

Selle funktsiooni kättesaadavaks muutmiseks lülitage [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sisse järgmised funktsioonid vastavas järjekorras.

1. Laoasukoha olek
1. Asukohakorralduse varude komplekteerimise ajaline jaotus

## <a name="feature-requirements"></a>Funktsioonide nõuded

Selle funktsiooni kasutamiseks peate määrama suvandi **Luba asukoha olek** väärtuseks *Jah* iga [asukohaprofiili](tasks/create-location-profile.md) jaoks, mida kasutatakse varude ladustamiseks. Selle asukohaprofiili suvandi seadistamiseks avage jaotis **Laohaldus \> Häälestus \> Ladu \> Asukohaprofiilid** ja valige asukohaprofiil. Leiate selle suvandi kiirkaardil **Üldine**.

## <a name="feature-scenarios"></a>Funktsiooni stsenaariumid

Selles jaotises esitatakse näiteid FIFO- ja LIFO-strateegiate seadistamise ja kasutamise kohta.

> [!TIP]
> Selles jaotises esitatakse kaks stsenaariumi, üks FIFO ja teine LIFO kohta. Esitatud protseduurid eeldavad, et teete mõlemad stsenaariumid selles järjekorras. Soovitame teil teha mõlemad stsenaariumid, et saaksite aru nende kahe strateegia vahelistest erinevustest.

### <a name="make-sample-data-available"></a>Näidisandmete kättesaadavaks tegemine

Nende stsenaariumide kasutamiseks siin määratud näidiskirjete ja -väärtuste abil peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Enne alustamist peate valima ka juriidilise isiku **USMF**.

Neid stsenaariume saate kasutada ka juhistena funktsiooni kasutamiseks tootmissüsteemis. Sel juhul tuleb teil siiski sisestada oma väärtused iga siin kirjeldatud sätte jaoks.

### <a name="set-up-the-scenarios"></a><a name="demo-set-up"></a>Stsenaariumide seadistamine

Need demoandmed nõuavad varude kohandamist nende stsenaariumide toetamiseks. Järgige neid etappe varude andmete loomiseks, mis on vajalikud FIFO- ja LIFO-stsenaariumidega töötamiseks.

1. Logige sisse süsteemi, kuhu demoandmed on installitud ja valige juriidiline isik **USMF**.
1. Minge asukohta **Laohaldus \> Seadistus \> Ladu \> Asukohaprofiilid**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Valige asukohaprofiilide loendist suvand **KORRUS-05**.
1. Määrake kiirkaardil **Üldine** suvandi **Luba asukoha olek** väärtuseks *Jah*.
1. Valige käsk **Salvesta**.
1. Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.
1. Valige asukohakorralduste loendis **63 tellimuse konteinerisse määramine**.
1. Lehe redigeerimisrežiimi panemiseks valige **Redigeeri**.
1. Otsige kiirkaardil **Asukohakorralduse tegevused** üles rida, kus välja **Seerianumber** väärtuseks on seatud *1* ja järgige ühte järgmistest etappidest.

    - Kui seadistate FIFO-stsenaariumit, muutke välja **Strateegia** väärtuseks *Asukoha kehtivusaja FIFO*.
    - Kui seadistate LIFO-stsenaariumit, muutke välja **Strateegia** väärtuseks *Asukoha kehtivusaja LIFO*.

1. Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Päringu redigeerimine**.
1. Valige päringu dialoogiboksis vahekaardil **Vahemik** suvand **Lisa**, et lisada rida ja määrake siis järgmised väärtused.

    - **Tabel:** *Asukohad*
    - **Tuletatud tabel:** *Asukohad*
    - **Väli:** *Tsooni ID*
    - **Kriteerium:** *Korrus*

1. Valige **OK**, et rakendada oma sätted ja sulgeda päringu dialoogiboks.
1. Oma asukohakorralduse muudatuste salvestamiseks valige **Salvesta**.
1. Järgige mobiilsel seadmel või rakenduses *Dynamics 365 for Finance and Operations – ladustamine* neid etappe olemasolevate varude eemaldamiseks lao asukohast, et toetada stsenaariume.

    1. Logige lattu *63* sisse vastava kasutaja ID ja parooli abil.
    1. Valige peamenüüs suvand **Kvaliteet**.
    1. Valige menüüs **Kvaliteedihaldus** suvand **Praak**.
    1. Valige lehel **Praak** väli **LOC/LP** ja sisestage *63\_1*.
    1. Valige **Sisesta** või **OK**.
    1. Kinnitage **Praagi** üksikasjad suvandi **Väljastuse korrigeerimine** jaoks, valides **Sisesta** või **OK**.

    Kui identifitseerimisnumbri varude olek on väljastuse korrigeerimine, kuvatakse teade „Töö lõpule viidud”.

    Need etapid jätavad varud kahte asukohta demoandmetes. Igal asukohal on erinev aegumiskuupäev. Asukoha *FL-001* aegumiskuupäev on 15. aprill 2017 ja asukoha *FL-002* aegumiskuupäev on 29. jaanuar 2017. Mõlemad asukohad sisaldavad kaupa *A0001*.

    Nende andmete kuvamiseks avage jaotis **Laohaldus \> Päringud ja aruanded \> Vaba kaubavaru loend** ning seejärel filtreerige ladu *63* ja kaupa *A0001*. Ridadel, kus välja **Asukoht** väärtuseks on seatud *FL-001* või *FL-002*, valige rida, mille väärtus **Füüsilised varud** on positiivne ja seejärel valige toimingupaanil **Kanded**. Väljal **Füüsiline kuupäev** kuvatakse kuupäev, mis vastab ühele eelnevalt mainitud aegumiskuupäevale.

### <a name="scenario-1-set-up-and-use-fifo-location-aging"></a><a name="fifo-demo"></a>1. stsenaarium: FIFO asukoha aegumise seadistamine ja kasutamine

FIFO-strateegia leiab üles asukoha, mis sisaldab vanimat aegumiskuupäeva ja planeerib komplekteerimise sellele aegumiskuupäevale.

1. Kui te pole seda veel teinud, [valmistage ette näidisandmed](#demo-set-up), mis on nõutavad selle stsenaariumi jaoks.
1. Avage jaotis **Müük ja turundus \> Müügitellimus \> Kõik müügitellimused**.
1. Valige suvand **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - Määrake kiirkaardi **Klient** välja **Kliendi konto** väärtuseks *US-001*.
    - Määrake kiirkaardi **Üldine** välja **Ladu** väärtuseks *63*.

1. Valige müügitellimuse loomiseks ja dialoogiboksi sulgemiseks **OK**.
1. Avatakse uus müügitellimus. See sisaldab uut tühja rida kiirkaardi **Müügitellimuse read** ruudustikus. Määrake selle tellimusrea jaoks välja **Kaubakood** väärtuseks *A0001*, välja **Kogus** väärtuseks *1*.
1. Valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.
1. Valige lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida valitud laos varudest selle kauba tellitud kogus.
1. Sulgege leht **Reserveerimine**.
1. Valige toimingupaani lehe **Müügitellimus** vahekaardi **Ladu** grupist **Tegevused** suvand **Vabasta lattu**. Teile kuvatakse teated. Süsteem loob saadetise, lisab selle uuele koormusele ja loob vajaliku töö.
1. Valige kiirkaardi **Müügitellimuse read** menüüst **Ladu** suvand **Töö üksikasjad**, et avada selle müügitellimuse jaoks loodud töö. Pange tähele, et real, kus suvandi **Töö tüüp** väärtus on *Komplekteerimine*, kuvatakse suvandi **Asukoht** väärtuseks *FL-002*. See asukoht sisaldab identifitseerimisnumbrit, millel on vanim aegumiskuupäev (FIFO).
1. Valige **Ladu \> Saadetise üksikasjad**.
1. Märkige kiirkaardilt **Üldine** üles voo ID, et saaksite seda kasutada 2. stsenaariumis.

### <a name="scenario-2-set-up-and-use-lifo-location-aging"></a>2. stsenaarium: LIFO asukoha aegumise seadistamine ja kasutamine

LIFO-strateegia leiab üles asukoha, mis sisaldab uusimat aegumiskuupäeva ja planeerib komplekteerimise sellele aegumiskuupäevale. 2. stsenaariumis saate redigeerida 1. stsenaariumi (FIFO) seadistust ja kasutada selle stsenaariumi käigus loodud müügitellimust ja voogu uuesti.

1. Enne selle stsenaariumi käivitamist seadistage ja viige lõpule täielik FIFO-stsenaarium, nagu kirjeldati [eelmises jaotises](#fifo-demo). Selles stsenaariumis saate kasutada selle stsenaariumi jaoks loodud voogu ja suuremat osa seadistusest uuesti.
1. Redigeerige asukohakorraldust **63 tellimuse konteinerisse määramine**, et see kasutaks strateegiat *Asukoha aegumise LIFO*, mida kirjeldati protseduuri [Stsenaariumide seadistamine](#demo-set-up) esimeses osas.

    Järgmisena saate muuta 1. stsenaariumis müügitellimuse jaoks loodud voogu, et see kasutaks strateegiat *Asukoha aegumise LIFO*.

1. Avage **Laohaldus \> Väljaminevad vood \> Saadetise vood \> Kõik vood**.
1. Valige ja avage voog, mis sisaldab FIFO-stsenaariumi jaoks loodud tellimust.
1. Valige toimingupaani vahekaardil **Töö** suvand **Tühista**, et tühistada FIFO-stsenaariumi jaoks loodud töö.
1. Tehke tegumiriba vahekaardil **Voog** grupis **Voog** valik **Töötlus**.
1. Kui töötlemine on lõpule viidud, valige toimingupaani vahekaardi **Voog** grupis **Seotud teave** suvand **Töö**, et avada selle voo jaoks loodud töö.
1. Lehe **Töö** vahekaardil **Ülevaade** peaks olema kaks rida. Otsige üles rida, kus välja **Töö olek** väärtuseks on seatud *Avatud*.
1. Pange tähele, et real, kus suvandi **Töö tüüp** väärtus on *Komplekteerimine*, kuvatakse suvandi **Asukoht** väärtuseks *FL-001*. See asukoht sisaldab identifitseerimisnumbrit, millel on uusim aegumiskuupäev (LIFO).

Nendes stesaariumides näidati teile, kuidas asukoha aegumise strateegia suunab töö lao asukohta, millel on kas vanimad või uusimad varud, sõltuvalt valitud strateegiast.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]