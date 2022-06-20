---
title: Kogumi positsioon on täis
description: See artikkel annab teavet klastri positsiooni täieliku funktsiooni kohta. See funktsioon pakub alternatiivi tööjaotuse reeglite jäigemale jõustamisele kogumi komplekteerimisel, kuna see võimaldab suuremat veavaru konteinerite või koormate mahupiirangutes.
author: Mirzaab
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 4d46933b7c60317234b8e39cd6dfd63d383de860
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857137"
---
# <a name="cluster-position-full"></a>Kogumi positsioon on täis

[!include [banner](../includes/banner.md)]

Funktsioon *Kogumi positsioon on täis* pakub alternatiivi tööjaotuse reeglite jäigemale jõustamisele kogumi komplekteerimisel, kuna see võimaldab suuremat veavaru konteinerite või koormate mahupiirangutes. Tavaliselt ei mahu kõik töökäsu kaubad valitud konteinerisse. Kogumeid komplekteerivatel laotöötajatel on selle stsenaariumi korral vähe võimalusi: nad peavad muutuma konteinerit suuremaks või pidama nõu juhiga, et leida muu lahendus.

See funktsioon pakub võimalust kasutada nuppu **Täielik** ühe kogumi tööüksuse korral. Vanemates versioonides oli see suvand saadaval ainult tavalise tellimuse komplekteerimiseks, mitte kogumi komplekteerimiseks. See funktsioon erineb standardsest nupust **Täielik**, kuna see tühistab ülejäänud töö. See ei viita sellele, et kasutaja lisab samasse kogumisse veel ühe asukoha ning see ei loo automaatselt uut tööd.

## <a name="turn-the-cluster-position-full-feature-on-or-off"></a>Kogumi positsiooni täieliku funktsiooni sisse- või väljalülitamine

Selles artiklis kirjeldatud funktsioonide kasutamiseks peab klastri positsiooni *täielik* funktsioon olema teie süsteemi jaoks sisse lülitatud. Tarneahela halduse 10.0.25 puhul on see funktsioon kohustuslik ja seda ei saa välja lülitada. Kui käitate versiooni, mis on *vanem* kui 10.0.25, saavad administraatorid selle funktsiooni sisse või välja lülitada, otsides kogumi positsiooni täisfunktsiooni Funktsioonihalduse [tööruumis](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="setup"></a>Seadistus

Selles jaotises on toodud juhised ja näide selle kohta, kuidas seadistada ja kasutada funktsiooni *Kogumi positsioon on täis*.

### <a name="make-sample-data-available"></a>Näidisandmete kättesaadavaks tegemine

Selle [näidisstsenaariumi](#example-scenario) kasutamiseks siin määratud näidiskirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Enne alustamist peate valima ka juriidilise isiku **USMF**.

Seda näidisstsenaariumi saate kasutada ka juhistena funktsiooni kasutamiseks, kui töötate tootmissüsteemis. Sel juhul tuleb teil siiski sisestada oma väärtused siin kirjeldatud sätete jaoks.

### <a name="cluster-profiles"></a>Kogumiprofiilid

Peate määrama, kas kogumi ID luuakse automaatselt, kui mitut positsioone kasutatakse, kui kogumid on tükeldatud ning kuidas komplekteerimistööd järjestatakse ja kontrollitakse.

1. Avage **Laohaldus \> Seadistamine \> Mobiilne seade \> Kogumiprofiilid**.
1. Valige loendipaanil kirje **Loo kogum**.
1. Määrake kiirkaardil **Üldine** järgmised väärtused.

    - **Loo kogumi ID:** *jah*
    - **Aktiveeri ametikohad:** *jah*
    - **Ametikohtade arv:** *2*
    - **Ametikoha nimi:** *numbriline*
    - **Tükelda kogum asukohas:** *pane*
    - **Sortimise kontrollimistüüp:** *asukoha skannimine*

1. Kiirkaardil **Kogumi sortimine**. Ruudustik peaks olema tühi (st see ei tohi sisaldada ridu).

### <a name="work-templates"></a>Töömallid

Peate määrama, kuidas luuakse komplekteerimistöö kogumi komplekteerimiseks.

1. Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.
1. Seadke lehe ülaosas välja **Töökäsu tüüp** väärtuseks *Müügitellimused*.
1. Veenduge, et järgnevad demoandmete töömallid on loetletud. Kui need pole saadaval, ei saa te stsenaariumi lõpule viia.

    - 61 SO etapp
    - 61 SO kogumi komplekteerimine

### <a name="location-directives"></a>Asukohakorraldus

Peate määrama, millisest asukohast kaubad komplekteeritakse ja kuhu need pannakse.

1. Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.
1. Seadke loendi päises välja **Töökäsu tüüp** väärtuseks *Müügitellimus*.
1. Veenduge, et järgnevad demoandmete müügitellimusekorraldused on loetletud. Kui need pole saadaval, ei saa te stsenaariumi lõpule viia.

    - 61 kogumi komplekteerimine
    - 61 SO-komplekteerimise tellimus

### <a name="mobile-device-menu-items"></a>Mobiilse seadme menüü-üksused

Peate konfigureerima mobiilse seadme menüü-üksuse kasutama olemasolevat tööd, mida juhitakse kogumi komplekteerimisega. Kogumi komplekteerimiseks tuleb sisse lülitada mobiilse seadme menüü-üksuses parameeter **Luba töö tükeldamine** ja lisada tööklass *SO-komplekteerimine*.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.
1. Valige loendipaanil kirje **Kogumi komplekteerimise loomine**.
1. Valige tegevuse paanil nupp **Redigeeri**.
1. Määrake kiirkaardil **Üldine** järgmised väärtused.

    - **Juhataja:** *Kogumi komplekteerimine*
    - **Loo litsentsiplaat:** *jah*
    - **Luba töö tükeldamine:** *jah*
    - **Kogumi profiili ID:** *Loo kogum*

    Võtke vastu vaikeväärtused kõigil teistel väljadel.

1. Lisage kiirkaardil **Tööklassid** kaks järgmist rida vastavalt vajadusele.

    - Rida 1 (tavaliselt olemas demoandmetes):

        - **Tööklassi ID:** *müük* 
        - **Töökäsu tüüp:** *müügitellimused*

    - Rida 2 (ei pruugi olla demoandmetes olemas):

        - **Töö klassi ID:** *SO-komplekteerimine*
        - **Töökäsu tüüp:** *müügitellimused*

1. Avage tegevuse paanil **Töö kinnituse häälestus**.
1. Valige suvand **Redigeeri**.
1. Sisestage ruudustiku reale järgmised väärtused.
    - **Töö tüüp** - *Komplekteerimine*
    - **Toote kinnitus** - *Valige märkeruut*

1. Valige tegevuse paanil **Salvesta** ja sulgege lehekülg.

## <a name="create-picking-work"></a>Komplekteerimistöö loomine

Enne kui saate alustada kogumi komplekteerimist, peate looma mõne väljamineva töö. Varasemalt loodud kogumiprofiil määrab kaks kogumi positsiooni. Seetõttu tuleb müügitellimuse komplekteerimiseks luua vähemalt kaks töö ID-d. Selle stsenaariumi korral tehakse kandeid laos *61* ning kasutatakse kaupu *L0101* ja *T0100*. Demoandmetel peaks olema piisavalt nende kaupade vaba kaubavaru. Veenduge, et teil on kannete lõpetamiseks piisavalt varusid.

### <a name="create-sales-order-1"></a>Müügitellimuse 1 loomine

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Müügitellimuse 1 loomiseks valige **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - **Kliendi konto:** *US-010*
    - **Ladu:** *61*

1. Valige nupp **OK**.
1. Avatakse uus müügitellimus. Lisage kiirkaardil **Müügitellimuse read** järgmiste sätetega rida.

    - **Kauba kood:** *T0100*
    - **Kogus:** *5*

1. Määrake kiirkaardi **Rea üksikasjad** vahekaardi **Tarne** välja **Kinnitatud tarnekuupäev** väärtuseks tänane kuupäev.
1. Lisage kiirkaardil **Müügitellimuse read** järgmiste sätetega teine rida.

    - **Kauba kood:** *L0101*
    - **Kogus:** *20*

1. Määrake kiirkaardi **Rea üksikasjad** vahekaardi **Tarne** välja **Kinnitatud tarnekuupäev** väärtuseks tänane kuupäev.
1. Iga äsja lisatud rea korral järgige varude reserveerimiseks järgmisi etappe.

    1. Valige reserveeritav rida.
    2. Tehke kiirkaardil **Müügitellimuse read** valik **Varud \> Reserveerimine**.
    3. Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida varud.
    4. Sulgege leht **Reserveerimine**.

1. Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.

    Kui väljalase on lõpule viidud, saate teabesõnumeid, mis näitavad loodud voo ja koormuse ID-sid.

### <a name="create-sales-order-2"></a>Müügitellimuse 2 loomine

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Müügitellimuse 2 loomiseks valige **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - **Kliendi konto:** *US-011*
    - **Ladu:** *61*

1. Valige nupp **OK**.
1. Avatakse uus müügitellimus. Lisage kiirkaardil **Müügitellimuse read** järgmiste sätetega rida.

    - **Kauba kood:** *L0101*
    - **Kogus:** *20*

1. Määrake kiirkaardi **Rea üksikasjad** vahekaardi **Tarne** välja **Kinnitatud tarnekuupäev** väärtuseks tänane kuupäev.
1. Lisage kiirkaardil **Müügitellimuse read** järgmiste sätetega teine rida.

    - **Kauba kood:** *T0100*
    - **Kogus:** *2*

1. Määrake kiirkaardi **Rea üksikasjad** vahekaardi **Tarne** välja **Kinnitatud tarnekuupäev** väärtuseks tänane kuupäev.
1. Iga äsja lisatud rea korral järgige varude reserveerimiseks järgmisi etappe.

    1. Valige reserveeritav rida.
    2. Tehke kiirkaardil **Müügitellimuse read** valik **Varud \> Reserveerimine**.
    3. Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida varud.
    4. Sulgege leht **Reserveerimine**.

1. Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.

    Kui väljalase on lõpule viidud, saate teabesõnumeid, mis näitavad loodud voo ja koormuse ID-sid.

### <a name="get-work-ids-and-license-plate-numbers"></a>Töö ID-de ja identifitseerimisnumbrite hankimine

Loodud peaks olema kaks töö ID-d, millest igaühel on kaks komplekteerimise rida. Järgige neid samme, et leida töö ID-d ja litsentsiplaat määranguid.

1. Avage jaotis **Laohaldus \> Töö \> Töö üksikasjad**.
1. Otsige ruudustikust **Ülevaade** veergu **Tellimuse number** kahe äsja loodud müügitellimuse kohta. Märkige iga müügitellimuse kohta vastav töö ID.
1. Valige rida iga müügitellimuse jaoks, et kuvada seotud teave ruudustikus **Read**. Märkige asukoht, kust iga kaup komplekteeritakse.
1. Avage **Laohaldus \> Päringud ja aruanded \> Vabade kaubavarude loend**.
1. Valige toimingupaanil **Dimensioonid**, et avada dialoogiboks **Dimensiooni kuvamine**.
1. Veenduge, et ruudud **Litsentsiplaat**, **Ladu** ja **Kaubakood** on märgitud ja seejärel valige **OK**.
1. Määrake paanil **Filter** järgmised filtrid.

    - **Kaubakood** – **üks (mitmest)** – *L0101* ja *T100*
    - **Ladu** – **algab väärtusega** – *61*

1. Märkige üles kuvatavad **litsentsiplaadi** väärtused.

## <a name="example-scenario"></a><a name="example-scenario"></a>Näidisstsenaarium

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a>Mobiilse seadme voo käivitamine – toote töö kinnituse häälestus

1. Logige mobiilirakendusse Warehouse Management sisse lao *61* kasutajana.
1. Valige **Väljaminev \> Kogumi komplekteerimise loomine**.

    Kuvatakse leht **ÜLESANNE: töö määramine kogumile**.

1. Sisestage müügitellimuse 1 töö ID, et määrata see kogumi positsioonile 1.
1. Valige **OK** (märke sümbol).
1. Sisestage müügitellimuse 2 töö ID, et määrata see kogumi positsioonile 2.
1. Valige **OK** (märke sümbol).

    Kuvatakse leht **ÜLESANNE: kogumi komplekteerimise loomine: komplekteerimine** ja *Kaup L0101 2 PL*.

Kuna kogumi profiil seab positsioonide arvuks 2, suunab süsteem teid automaatselt esimesele konsolideerivale komplekteerimisele: kauba *L0101* kaks kaubaalust (PL).

Järgmistel etappidel saate toimingu kohta lisateabe (nt komplekteerimiskoha) vaatamiseks igal ajal valida vahekaardi **Üksikasjad**.

1. Määrake välja **KAUP** väärtuseks *L0101*. See kinnitab selle menüü-üksuse jaoks vajaliku kaubakoodi (konfigureerisite selle varem menüü-üksuse loomisel, tehes lehel **Mobiilse seadme menüükäsk** valiku **Töö kinnituse häälestus**).
1. Sisestage identifitseerimisnumber, mis on seotud asukohas oleva komplekteeritava kaubaga. Peate valima kaks kaubaalust.
1. Määrake välja **LP** väärtuseks *LP\_PICK\_01*.
1. Valige **OK** (märke sümbol).

    Kuvatakse leht **ÜLESANNE: sortimine: kogumi komplekteerimise loomine**. Siin sordite kaks komplekteeritud kaubaalust komplekteerimise positsioonile. See positsioon võib olla koorem või konteiner, mida kasutatakse komplekteeritud varude eraldamiseks müügitellimuse järgi.

1. Vaadake üksikasju, mis kuvatakse kauba (*L0101*) ja koguse (*20* ea) kohta, mis sorditakse positsioonile 1 (müügitellimuse 1 korral).
1. Seadke välja **POSITSIOONI NIMI** väärtuseks *1*.
1. Valige **OK** (märke sümbol).
1. Vaadake üksikasju, mis kuvatakse kauba (*L0101*) ja koguse (*20* ea) kohta, mis sorditakse positsioonile 2 (müügitellimuse 2 korral).
1. Seadke välja **POSITSIOONI NIMI** väärtuseks *2*.
1. Valige **OK** (märke sümbol).

    Kuvatakse leht **ÜLESANNE: kogumi komplekteerimise loomine: komplekteerimine** ja *Kaup T0100 7 ea*.

Selle stsenaariumi korral ei saa positsioon 1 aktsepteerida kaupade täielikku kogust, mis tuleb komplekteerida müügitellimuse 1 täitmiseks. Positsioon peab olema märgitud täielikuna. Selle stsenaariumi korral peate viima lõpule teise kauba osalise komplekteerimise. Teine kaup komplekteeritakse osaliselt positsiooni 1 jaoks ja luuakse tellimuse täitmiseks uus töö, mille korral komplekteeritakse järelejäänud kogus.

1. Valige nupp Menüü (nimetatakse mõnikord hamburgeriks või hamburgeri nupuks) ja seejärel valige **Kogumi positsioon on täis**.
1. Määrake positsioon, mis on täis, ja valige *1*.
1. Valige **OK** (märke sümbol).
1. Sisestage komplekteeritav kogus, mida saab endiselt komplekteerida positsioonile 1. Süsteem saab määrata, millise kaubakoodi järgi komplekteeritakse.
1. Sisestage *2*.
1. Valige **OK** (märke sümbol).
1. Ülejäänud kauba positsioonile 2 komplekteerimise lõpuleviimiseks kinnitage kaubakood.
1. Määrake välja **KAUP** väärtuseks *T0100*.
1. Valige **OK** (märke sümbol).
1. Sisestage litsentsiplaat, millelt kaup komplekteeritakse, seades välja **LP** väärtuseks *LPREPL04*.
1. Valige **OK** (märke sümbol).
1. Vaadake üksikasju, mis kuvatakse kauba (*T0100*) ja koguse (*2* ea) kohta, mis sorditakse positsioonile 2 (müügitellimuse 2 korral).
1. Seadke välja **POSITSIOONI NIMI** väärtuseks *2*.
1. Valige **OK** (märke sümbol).
1. Vaadake üksikasju, mis kuvatakse kauba (*T0100*) ja koguse (*2* ea) kohta, mis sorditakse positsioonile 1 (müügitellimuse 1 korral).
1. Seadke välja **POSITSIOONI NIMI** väärtuseks *1*.
1. Valige **OK** (märke sümbol).

    Kuvatakse leht **ÜLESANNE: kogumi komplekteerimise loomine: komplekteerimine**.

Selle stsenaariumi korral on kogumi komplekteerimine lõpule viidud ja kasutaja on suunanud komplekteeritud esemed positsioonist 1 ja 2 vaheasukohta *STAGE01*.

1. Vaadake üle lehel olev teave. See näitab, et lõplik kogus *44* pannakse vaheasukohta.
1. Valige **OK** (märke sümbol).

    Teile kuvatakse teade „Kogum on lõpule viidud”.

Ülejäänud koguse komplekteerimiseks saate nüüd kasutada menüükäsku **Müügi komplekteerimine**. Seejärel saate kasutada menüükäsku **Müügi laadimine**, et teisaldada kaubad vaheasukohast kuni laadimisdokki.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]