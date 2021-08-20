---
title: Lao ruumi leidmine
description: Selles teemas antakse teavet lao ruumi leidmise kohta. Lao ruumi leidmise abil saate konsolideerida nõudlust kauba ja mõõtühiku järgi tellimustest, mille olek on tellitud, reserveeritud või väljastatud. See aitab laohalduritel nutikalt planeerida komplekteerimise asukohti enne tellimuse lattu väljatamist ja komplekteerimistöö loomist.
author: mirzaab
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 92e0d2ef468a47579d21428009f1fd2dfcb8b0c19874d1a8d44e638f9f0a7c89
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738121"
---
# <a name="warehouse-slotting"></a>Lao ruumi leidmine

[!include [banner](../includes/banner.md)]

Mitmed saadavalolevad laoruumi paigutamise funktsioonid aitavad laohalduritel nutikalt planeerida komplekteerimise asukohti enne tellimuse lattu väljastamist ja komplekteerimistöö loomist.

*Lao paigutamise funktsiooni* abil saate konsolideerida nõudlust kauba ja mõõtühiku järgi tellimustest, mille olek on *Tellitud*, *Reserveeritud* või *Väljastatud*. Loodud nõudlust saab seejärel rakendada asukohtadele, mida kasutatakse koguse, ühiku, füüsiliste dimensioonide, fikseeritud asukohtade ja muu alusel komplekteerimiseks. Pärast seda, kui ruumi leidmise plaan on loodud, saab luua täiendamise töö, et tuua igasse asukohta sobiv kogus varusid.

*Üleviimistellimustele laoruumi leidmise* funktsioon võimaldab laohaldajatel täiendada komplekteerimise asukohti, mis põhinevad nõudel, mis ei ole veel lattu väljastatud. See tagab, et kõik komplekteerimise asukohad kaasavad kõik kaubad, mis on vajalikud üleviimistellimuste jaoks pärast nende lattu väljastamist. Selle funktsiooni kasutamiseks tuleb teil sisse lülitada ka *Laoruumi leidmise funktsioon*.

*Laoruumi eraldamise täiustuste* funktsioon lisab valiku malli ridadele, mida kasutatakse *Laoruumi eraldamise funktsioonis*. Suvand võimaldab süsteemil kaaluda olemasolevat vaba kaubavaru sihtkoha asukohas. Seetõttu võidakse ruumi loomiseks luua vähem täiendusi. *Laoruumi paigutamise täiustamise* funktsioon nõuab, et kasutataks ka *Laoruumi eraldamise funktsiooni*. Seda saab soovi korral kasutada koos *Lao ümberpaigutamisega üleviimistellimuste* funktsiooni jaoks.

## <a name="turn-on-the-warehouse-slotting-features"></a>Laoruumi leidmise funktsioonide sisselülitamine

Enne nende funktsioonide kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsioonide olekut ja need vajadusel sisse lülitada. Järgmiste funktsioonide sisselülitamine vastavalt vajadusele:

- Laopesade planeerimise funktsioon
- Laoruumi leidmine üleviimistellimuste jaoks

    > [!IMPORTANT]
    > *Laoruumi leidmise funktsioon* peab enne seda funktsiooni olema sisse lülitatud.

- Laoruumi leidmise eraldamise täiustused

    > [!IMPORTANT]
    > *Laoruumi leidmise funktsioon* peab enne seda funktsiooni olema sisse lülitatud.

## <a name="set-up-warehouse-slotting"></a>Lao ruumi leidmise seadistamine

Lao ruumi leidmise kasutamiseks peate seadistama järgmised elemendid oma süsteemis:

- Ruumi leidmise mõõtühiku järgud
- Korralduse koodid
- Ruumi leidmise mallid
- Asukohakorraldus

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a>Mõõtühikute järkude loomine ruumi leidmise jaoks

Mõõtühikute järgud võimaldavad mitme mõõtühiku grupeerimist ruumi leidmise eesmärgil. Näiteks kui erineva suurusega kaste komplekteeritakse samalt kastide komplekteerimise alalt, saab iga suuruse jaoks luua ühe järgu. **Iga mõõtühiku jaoksa tuleb luua rida, mis on selle järgu osa.**

1. Avage jaotis **Laohaldus \> Häälestus \> Täiendamine \> Ruumi leidmise mõõtühikute järgud**.
1. Valige suvand **Uus**.
1. Määrake päises järgmised väärtused.

    - **Mõõtühiku järk:** *EaBoxPl*
    - **Kirjeldus:** *Iga kasti kaubaalus*

1. Valige käsk **Salvesta**.
1. Valige kiirkaardil **Mõõtühikud** suvand **Uus**, et lisada rida ruudustikku.
1. Määrake uuel real järgmised väärtused.

    - **Ühik:** *Kast*
    - **Kirjeldus:** jätke väli tühjaks. See täidetakse muudatuste salvestamisel automaatselt.
    - **Ühiku klass:** *Kogus*

1. Klõpsake valikut **Uus**, et lisada ruudustikku teine rida.
1. Määrake uuel real järgmised väärtused.

    - **Ühik:** *ea*
    - **Kirjeldus:** jätke väli tühjaks. See täidetakse muudatuste salvestamisel automaatselt.
    - **Ühiku klass:** *Kogus*

1. Klõpsake valikut **Uus**, et lisada ruudustikku kolmas rida.
1. Määrake uuel real järgmised väärtused.

    - **Ühik:** *PL*
    - **Kirjeldus:** jätke väli tühjaks. See täidetakse muudatuste salvestamisel automaatselt.
    - **Ühiku klass:** *Kogus*

1. Järgu salvestamiseks valige **Salvesta**.

### <a name="create-a-directive-code-for-slotting"></a>Korralduskoodi loomine ruumi leidmiseks

Peate valima korralduskoodi, mis tuleks malliga seostada.

1. Avage jaotis **Laohaldus \> Seadistus \> Korralduskoodid**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage väljale **Korralduskood** väärtus *Ruumi leidmine*.
1. Sisestage väljale **Korralduse kirjeldus** väärtus *Ruumi leidmine*.

### <a name="set-up-slotting-templates"></a>Ruumi leidmise mallide seadistamine

Iga ruumi leidmise mall juhib seda, kuidas kindla lao asukohtade jaoks määratakse varusid. Iga mall peab sisaldama rida iga ruumi leidmise täpsustuse jaoks. Kasutage selle jaotise protseduure, et häälestada ruumi leidmise malle.

1. Avage jaotis **Laohaldus \> Seadistus \> Täiendamine \> Ruumi leidmise mallid**.
1. Valige malli loomiseks **Uus**.

Järgmisena peate seadistama malli päise, ruumi leidmise kirjelduse ja asukohakorraldused järgmistes alamjaotistes kirjeldatud juhiste järgi. Üleviimistellimuste paigutamine meenutab müügitellimuste paigutamise seadistust, kuid **Nõudluse tüüp** välja väärtuseks seatakse *Üleviimistellimused*, mitte *Müügitellimused*.

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a>Müügitellimuse paigutamiseks kasutatava malli päise seadistamine

1. Määrake malli päises järgmised väärtused.

    - **Ruumi leidmise mall:** _61_
    - **Kirjeldus:** _61_
    - **Nõudluse tüüp:** *Müügitellimus*

        > [!NOTE]
        > Praegu *Müügitellimused* ja *Üleviimistellimused* ainukesed toetatavad nõudluse tüübid. *Üleviimistellimusi* saate valida ainult juhul, kui *Laoruumi leidmine üleviimistellimusele* funktsioon on sisse lülitatud.

    - **Nõudluse strateegia:** _Tellitud_

        Sellel väljal on saadaval järgmised väärtused.

        - **Tellitud** – müügitellimuse täielikku tellitud kogust tuleks arvestada nõudlusena.
        - **Reserveeritud** – ainult reserveeritud müügitellimuse rea (füüsilised ja tellitud) koguseid tuleks arvestada nõudlusena.
        - **Väljastatud** – Väljastatud kogus tuleks lugeda nõudluseks.

    - **Ladu:** _61_
    - **Luba voo nõudmisel kasutada reserveerimata koguseid:** _Jah_

Samuti saate määrata päringu hinnatava nõudluse ulatuse kitsendamiseks.

#### <a name="set-up-slotting-specifications-for-each-template"></a>Ruumi leidmise täpsustuste seadistamine iga malli jaoks

Iga loodava müügitellimuse malli jaoks järgige neid etappe, et lisada rida iga ruumi leidmise täpsustuse jaoks.

1. Valige kiirkaardil **Ruumi leidmise malli üksikasjad** suvand **Uus**, et luua malli rida.
1. Määrake uuel real järgmised väärtused.

    - **Järjestus:** _1_
    - **Kirjeldus:** _Fikseeritud asukoht_
    - **Minimaalne kogus:** _1_

        See väli määratleb rea jaoks nõutava minimaalse koguse.

    - **Maksimaalne kogus:** _1000000_

        See väli määratleb rea jaoks kehtiva maksimaalse koguse.

    - **Ühik:** jätke väli tühjaks.

        See väli määratleb mõõtühiku, millele minimaalne ja maksimaalne kogus viitab.

    - **Mõõtühiku järk:** _EaBoxPl_

        See väli määratleb rea jaoks kehtiva mõõtühiku. (Lisateavet leiate selle teema varasemast jaotisest [Ruumi leidmise mõõtühikute järkude seadistamine](#unit-tiers).)

    - **Määra ruumi kriteeriumid:** _Koguse kaalumine_

        Sellel väljal on saadaval järgmised väärtused.

        - **Tühja eeldamine** – see süsteem peaks eeldama, et kõik komplekteerimisala asukohad on tühjad ja neid ei tohiks kontrollida varudes.
        - **Koguse kaalumine** – see süsteem peaks kontrollima varusid komplekteerimisala asukohtades ja ei tohiks jätta vahele asukohti, mis pole tühjad.
        - **Arvestage laoseisu** – Süsteem peaks kontrollima, kas sihtkohas oleva kauba jaoks on reserveeritud kogused. Kui kogus on piisavalt suur, et rahuldada vähemalt üht nõudluse rea ühikut, vähendatakse loodud paigutamise plaani kirjet saadaoleva summa võrra. Näiteks kui nõudlus on 10 kasti ja üks kast on laos olemas, on leitud nõudlus üheksa kasti. Kui nõudlus on 10 kasti ja üks kast on käepärast, on leitud nõudlus 10 kasti. See väärtus on saadaval ainult siis, kui funktsioon *Lao paigutamise täiustamine* on sisse lülitatud.

    - **Korralduskood:** _Ruumi leidmine_

        See väli määratleb asukohakorralduse, mida kasutatakse täiendamistöö komplekteerimise asukoha leidmiseks.

    - **Ületäitumise asukoht:** jätke see väli tühjaks.

        See väli määratleb asukoha, kuhu varud ladustatakse juhul, kui rea töötlemisel koguse asukohta ei leita.

    - **Luba loobumine:** _Jah_

        Kui selle suvandi väärtuseks on seatud *Jah*, luuakse liikumise töö juhul, kui nõudlusele ei leita ruumi, et võtta varud välja asukohtadest, kus on varusid, kuid leitud ruumi ei kasutatud. Seejärel käivitatakse mall uuesti. Seekord eirab see varusid asukohtades. See funktsioon töötab kõige paremini siis, kui välja **Ruumi kriteeriumide määramine** on seatud _Koguse kaalumine_.

    - **Fikseeritud asukoha kasutus:** _Ainult selle toote fikseeritud asukohad_

        Sellel väljal on saadaval järgmised väärtused.

        - **Fikseeritud ja mittefikseeritud asukohad** – süsteem ei tohiks piirduda ainult fikseeritud asukohtade kasutamisega.
        - **Ainult selle toote fikseeritud asukohad** – süsteem peaks kasutama ainult nende asukohtade ruumi, mis on selle toote jaoks fikseeritud asukohad.
        - **Ainult selle tootevariandi fikseeritud asukohad** – süsteem peaks kasutama ainult nende asukohtade ruumi, mis on selle tootevariandi jaoks fikseeritud asukohad.

> [!NOTE]
> Kui paigutamise mall sisaldab vähemalt ühte rida, kus välja **Määra ruumi kriteerium** väärtuseks on seatud *Arvestage olemasolevat kaubavaru*, ei lubata mitte ühtegi malli rida soiku jääda.

1. Valige käsk **Salvesta**.
1. Teise malli rea loomiseks valige **Uus**.
1. Määrake uuel real järgmised väärtused.

    - **Järjestus:** _2_
    - **Kirjeldus:** _Muu_
    - **Minimaalne kogus:** _1_
    - **Maksimaalne kogus:** _1000000_
    - **Ühik:** jätke väli tühjaks.
    - **Mõõtühiku järk:** _EaBoxPl_
    - **Määra ruumi kriteeriumid:** _Koguse kaalumine_
    - **Korralduskood:** _Ruumi leidmine_
    - **Ületäitumise asukoht:** jätke see väli tühjaks.
    - **Luba loobumine:** _Jah_
    - **Fikseeritud asukohtade kasutamine:** _Fikseeritud ja mittefikseeritud asukohad_

    Teise rea päringus saate nüüd määrata kriteeriumid, mille alusel määratletakse, millistest asukohtadest selle rea nõudlusele saab ruumi leida.

1. Otsige üles rida, kus välja **Järjestus** väärtuseks on seatud *2*.
1. Valige **Päringu redigeerimine**.
1. Vahekaardil **Vahemik** valige käsk **Lisa**, et lisada uus rida ruudustikule.
1. Määrake uuel real järgmised väärtused.

    - **Tabel:** *Asukohad*
    - **Tuletatud tabel:** *Asukohad*
    - **Väli:** *Asukohaprofiili ID*
    - **Kriteeriumid:** *Pick-06* (valige väljal kahekordne plussmärk \[**++**\] loendi laiendamiseks ja seejärel valige *Pick-06* - *Komplekteerimissait 6*.)

1. Valige nupp **OK**.

#### <a name="set-up-location-directives"></a>Asukohakorralduste häälestamine

Vähemalt üks asukohakorraldus peab olema seadistatud, et toetada ruumi leidmise valikuid. Kasutage selles jaotises olevaid protseduure uue *täiendamise asukohakorralduse* seadistamiseks ruumi leidmise valikute tegemiseks.

1. Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.
1. Valige vasakpoolse paani väljal **Töökäsu tüüp** suvand *Täiendamine*.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage uue asukohakorralduse päise väljale **Nimi** väärtus *61 ruumi leidmise komplekteerimine*.
1. **Järjekorranumber** väljal nõustuge vaikeväärtusega.

##### <a name="configure-the-location-directives-fasttab"></a>Asukohakorralduste kiirkaardi konfigureerimine

1. Määrake kiirkaardil **Asukohakorraldused** järgmised väärtused. Võtke vastu vaikeväärtused kõigil teistel väljadel.

    - **Töö tüüp:** _Komplekteerimine_
    - **Tegevuskoht:** _6_
    - **Ladu:** _61_
    - **Korralduskood:** _Ruumi leidmine_

1. Valige **Salvesta**, et muuta kiirkaart **Read** kättesaadavaks.

##### <a name="configure-the-lines-fasttab"></a>Ridade kiirkaardi konfigureerimine

1. Rea loomiseks valige kiirkaardil **Read** suvand **Uus**.
1. Määrake uuel real järgmised väärtused.

    - **Alates kogusest:** _0_
    - **Koguseni:** _1000000_

1. Võtke vastu ülejäänud väljade vaikeväärtused.
1. Valige **Salvesta**, et muuta kiirkaart **Asukohakorralduse toimingud** kättesaadavaks.

##### <a name="configure-the-location-directive-actions-fasttab"></a>Asukohakorralduste tegevuste kiirkaardi konfigureerimine

1. Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus**, et luua rida.
1. Määrake uuel real järgmised väärtused. Võtke vastu vaikeväärtused kõigil teistel väljadel.

    - **Järjekorranumber:** nõustuge vaikeväärtusega.
    - **Nimi:** _Hulgi_
    - **Strateegia:** _Puudub_

1. Võtke vastu ülejäänud väljade vaikeväärtused.
1. Valige **Salvesta**, et muuta nupp **Päringu redigeerimine** kättesaadavaks.

##### <a name="edit-the-query"></a>Redigeeri päringut

1. Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Päringu redigeerimine**.
1. Vahekaardil **Vahemik** valige käsk **Lisa**, et lisada uus rida ruudustikule.
1. Määrake uuel real järgmised väärtused.

    - **Tabel:** *Asukohad*
    - **Tuletatud tabel:** *Asukohad*
    - **Väli:** *Tsooni ID*
    - **Kriteeriumid:** *Hulgi* (valige väljal kahekordne plussmärk \[**++**\] loendi laiendamiseks ja seejärel valige *Hulgi*.)

1. Valige nupp **OK**.

## <a name="scenario"></a>Stsenaarium

### <a name="set-up-the-scenario"></a>Stsenaariumi seadistamine

Selle stsenaariumi puhul saate kasutada sisseehitatud näidisandmeid ja luua selles jaotises kirjeldatud kirjeid.

#### <a name="use-the-usmf-sample-data"></a>USMF-näidisandmete kasutamine

Selle stsenaariumi kasutamiseks siin määratud näidiskirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Enne alustamist peate valima ka juriidilise isiku **USMF**.

#### <a name="create-demand"></a>Nõudluse loomine

Järgige neid etappe nõudluse loomiseks, millele soovite ruumi leidmist rakendada.

1. Avage jaotis **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Müügitellimuse loomiseks valige **Uus**.
1. Valige dialoogiboksi **Müügitellimuse loomine** väljal **Kliendi konto** suvand _US-007_.
1. Valige väljal **Ladu** väärtus _61_.
1. Valige nupp **OK**.
1. Avatakse uus müügitellimus. See lisab uue tühja rea kiirkaardil **Müügitellimuse read**. Määrake sellel real järgmised väärtused.

    - **Kaup:** _L0101_
    - **Kogus:** _20_

1. Valige **Lisa rida**, et lisada uus rida ja seadke järgmised väärtused.

    - **Kaup:** _T0100_
    - **Kogus:** _8_

1. Valige käsk **Salvesta**.
1. Teise müügitellimuse loomiseks valige **Uus**.
1. Valige dialoogiboksi **Müügitellimuse loomine** väljal **Kliendi konto** suvand _US-008_.
1. Valige väljal **Ladu** väärtus _61_.
1. Avatakse uus müügitellimus. See lisab uue tühja rea kiirkaardil **Müügitellimuse read**. Määrake sellel real järgmised väärtused.

    - **Kaup:** _T0100_
    - **Kogus:** _1_

1. Valige käsk **Salvesta**.

### <a name="walk-through-a-typical-slotting-scenario"></a>Tavalise ruumi leidmise stsenaariumi ülevaade

Kui kõik eeltingimuseks olevad elemendid on eelmise jaotise kirjelduste järgi paigas, olete valmis funktsiooni proovima, tehes läbi kõik selles jaotises olevad harjutused.

#### <a name="generate-demand"></a>Loo nõudlus

1. Avage jaotis **Laohaldus \> Seadistus \> Täiendamine \> Ruumi leidmise mallid** ja valige eelnevalt loodud ruumi leidmise mall.
1. Valige toimingupaanil **Loo nõudlus**. See käsk hindab kõiki süsteemis olevaid nõudlusi, mis ühtivad ruumi leidmise malli päringuga. Kõigi tellimuste kõik nõudlused konsolideeritakse seejärel ühele reale koguse/mõõtühiku kohta. Kui protsess on lõpule viidud, kuvatakse teade.

#### <a name="slotting-demand"></a>Ruumi leidmise nõudlus

*Ruumi leidmise nõudlus* kuvab nõudluse loomise tulemused ruumi leidmise malli seadistuse põhjal.

- Valige toimingupaanil **Ruumi leidmise nõudlus**, et kuvada käsu **Loo nõudlus** tulemusi. Ruumi leidmise nõudluse ridu saab redigeerida. Saate kustutada rea, lisada uue rea või redigeerida rea üksikasju.

> [!NOTE]
> Saate redigeerida nõudlust käsitsi või importida selle andmehalduse abil välisest süsteemist. Ruumi leidmise nõudluses olevat kasutatakse järgmises etapis, olenemata selle päritolust.

#### <a name="locate-demand"></a>Nõudluse leidmine

Kui nõudlus on loodud, peate käsu **Otsi nõudlust** abil looma *ruumi leidmise plaani*.

- Valige toimingupaanil **Otsi nõudlust**. Ruumi leidmise protsess töötab. Kui protsess on lõpule viidud, kuvatakse teade.

#### <a name="slotting-plan"></a>Ruumi leidmise plaan

Ruumi leidmise plaan kuvab asukohta, kuhu iga kaup/kogus määrati, kas kasutati ületäitumist, kas loodi loobumistöö ja kasutatud malli rida. *Kõik nõudlused, millele ruumi ei leitud, on punasega esile tõstetud.*

- Valige toimingupaanil **Ruumi leidmise plaan** tulemuste kuvamiseks.

> [!NOTE]
> - **Nõudluse loomise**, **Nõudluse leidmise** ja **Täiendamise** protsesside käivitamine on nüüd käivitatud. (Need protsessid on saadaval tegumiribal **Paigutuse mallid** lehel.)
> - **Nõudluse loomise**, **Nõudluse leidmise** ja **Täiendamise käivitamise** protsessid on lukus tagamaks, et neid ei saa samal ajal käivitada. Muul juhul võidakse kasutatavaid andmeid kustutada.
> - **Nõudluse loomine** ja **Nõudluse leidmise** protsessid näitavad hoiatust, kui käivitamine ei loo kirjeid või kui kirjetel puudub teave.
> - Kui valite **Paigutusplaani**, ei ole tegumiribal nuppe **Uus**, **Redigeeri** või **Kustuta**, sest andmeallikat ei saa redigeerida.
> - Kui valite **Täitmise käivitamise**, kinnitab süsteem valitud teenindusaegade malli ja protsessid.

#### <a name="create-replenishment"></a>Täiendamise loomine

Kui ruumi leidmise plaan on loodud, peate selle plaani põhjal looma *täiendamise töö*.

- Valige tegevuste paanil käsk **Käivita täiendamine**. Kui protsess on lõpule viidud, kuvatakse teade. See teade näitab tööjärgu ID jaoks loodud päiste arvu.

Kasutatavad asukohakorraldused tuvastatakse igale malli reale määratud korralduskoodi alusel.

## <a name="tips"></a>Näpunäited

### <a name="set-up-automatic-slotting"></a>Automaatse ruumi leidmise seadistamine

Kui kõik vajalikud elemendid on paigas, saate häälestada ruumi leidmise automaatse käivitamise nende etappide abil.

1. Avage jaotis **Laohaldus \> Täiendamine \> Käivita ruumi leidmine**.
1. Määrake käivitatavad ruumi leidmise etapid. Valige vähemalt üks järgmistest ruumi leidmise etappidest.

    - Loo nõudlus
    - Nõudluse leidmine
    - Täiendustöö loomine

    > [!NOTE]
    > Ruumi leidmise etapid on progresseeruvad. Kui soovite valida suvandit *Otsi nõudlust*, peate esmalt valima *Loo nõudlus*.

1. Määrake kasutatav ruumi leidmise mall.
1. Soovi korral saate määrata kordumise automaatselt käivituma.

Selle stsenaariumi harjutuste jaoks **ärge** seadistage automaatset ruumi leidmist.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]