---
title: Väljastuste sortimine
description: Selles teemas antakse teavet väljamineku sortimise kohta. See funktsioon hõlbustab väikeste konteinerite käsitsemist ja aitab lao töötajatel veokis kaubaaluste mahutavust tõhusamalt planeerida ja korraldada.
author: Mirzaab
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 3c576209a86f776ac424f7fb9f2b606bea774a67
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828390"
---
# <a name="outbound-sorting"></a>Väljastuste sortimine

[!include [banner](../includes/banner.md)]

See funktsioon hõlbustab väikeste konteinerite käsitsemist ja aitab lao töötajatel veokis kaubaaluste mahutavust tõhusamalt planeerida ja korraldada. Kui kasutate väljamineku sortimist, saate sortida pakitud konteinereid õigele kaubaalusele, kui need tulevad pakkimisjaamast. Saate luua ka pakkimise hierarhia.

See funktsioon võimaldab teil luua kaubaaluseid konteineritest, mis on pakitud pakkimise funktsiooni kaudu. Konteinerit ei saadeta lõplikku saadetise asukohta, kuna see on algses pakkimisvoos. Selle asemel saavad töötajad konteineri sulgeda ja teisaldada selle sortimise tüübi asukohta. Seejärel saavad nad sortida konteinereid asukohtadele, millel on oma identifitseerimisnumber (LP). Kui konteinerid on sorditud, saab luua töö, et saata kogu identifitseerimisnumber lõplikku saadetise laadimise või vaheasukohta, mis põhineb asukohakorraldustel või teie enda nõudmistel. Lisaks saab sortimise asukoha sulgemise tegevus teisaldada varud kohe lõplikku saadetise asukohta ja komplekteerida tellimusele.

## <a name="turn-on-the-outbound-sorting-feature"></a>Väljamineku sortimise funktsiooni sisselülitamine

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Seega on funktsioon loetletud järgmisel viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Väljamineku sortimine*

## <a name="setup"></a>Häälestus

Selle stsenaariumi puhul peate kasutama standardseid demoandmeid **USMF** ja ladu *62*. Samuti peate lõpule viima järgmistes alamjaotistes kirjeldatud seadistuse.

### <a name="set-up-a-wave-template"></a>Voomalli seadistamine

See seadistus töötleb automaatselt seda voogu ja loob töö, kui rida väljastatakse lattu.

1. Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.
1. Valige mallide loendist **Ladu 62**.
1. Veenduge, et kiirkaardil **Üldine** oleks suvandi **Töötle voogu lattu vabastamisel** väärtuseks seatud *Jah*.

### <a name="set-up-a-worker"></a>Töötaja seadistamine

Pakkimisjaama loetakse asukohaks. Lao töötajad, kes logivad pakkimisjaamas sisse, näevad ja töötavad ainult selles konkreetses pakkimise asukohas plaanitud saadetiste ja konteineritega. Kasutaja, kes logib sisse rakendusse Microsoft Dynamics 365, tuleb seadistada töötajaks Laohalduses. Kui kasutaja nime ei kuvata töökasutajate loendis, kasutage selle lisamiseks järgmist protseduuri.

> [!NOTE]
> Need etapid eeldavad, et kasutaja on süsteemis juba olemas ja on seostatud töövõtja või töötajaga moodulis **Inimressurssid**.

1. Avage jaotis **Laohaldus \> Seadistus \> Töötaja**.
1. Valige suvand **Uus**.
1. Valige väljal **Töötaja** töötajate loendist sihtkasutaja.
1. Valige käsk **Vali**.
1. Valige toimingupaanil nupp **Salvesta**.
1. Valige kiirkaardil **Kasutajad** suvand **Uus**, et luua mobiilse seadme konto ja seadke sellele järgmised väärtused.

    - **Kasutaja ID:** sisestage kordumatu ID.
    - **Kasutajanimi:** sisestage nimi ID jaoks.
    - **Vaikeladu:** *62*
    - **Menüü nimi:** *Peamine*

1. Valige toimingupaanil nupp **Salvesta**.
1. Kuvatakse dialoogiboks **Parooli määramine**, kus saate luua lihtsa parooli, mida kasutaja saab mobiilirakendusse sisselogimiseks kasutada. Määrake järgmised väärtused.

    - **Parool:** sisestage lihtne parool.
    - **Kinnita parool:** sisestage uuesti sama parool.

1. Valige suvand **Sea parool**.

    Tegevuskeskuse teatis ütleb, et teie loodud kasutaja jaoks on parool määratud.

### <a name="create-a-location-type"></a>Asukoha tüübi loomine

1. Avage jaotis **Laohaldus \> Seadistus \> Ladu \> Asukoha tüübid**.
1. Valige toimingupaanil **Uus**, et luua asukoha tüüp ja määrake sellele järgmised väärtused.

    - **Asukoha tüüp:** *SORTIMINE*
    - **Kirjeldus:** *Sortimine*

1. Valige toimingupaanil nupp **Salvesta**.

### <a name="set-up-warehouse-management-parameters"></a>Laohalduse parameetrite seadistamine

1. Avage **Laohaldus \> Seadistus \> Laohalduse parameetrid**.
1. Määrake vahekaardi **Üldine** kiirkaardi **Asukoha tüübid** välja **Sortimise asukoha tüüp** väärtuseks *SORTIMINE*.
1. Valige toimingupaanil nupp **Salvesta**.

### <a name="set-up-a-location-profile"></a>Asukohaprofiili seadistamine

1. Minge asukohta **Laohaldus \> Seadistus \> Ladu \> Asukohaprofiilid**.
1. Valige toimingupaanil nupp **Uus**.
1. Määrake päises järgmised väärtused.

    - **Asukohaprofiili ID:** *Sortimine*
    - **Nimi:** *Sortimine*

1. Määrake kiirkaardil **Üldine** järgmised väärtused.

    - **Asukoha vorming:** *ASRB* (riiulirida-sektsioon-riiul-asukoht)
    - **Asukoha tüüp:** *SORTIMINE*
    - **Kasuta identifitseerimisnumbri jälgimist:** *Jah*
    - **Luba segakaubad:** *Jah* (kui määrate selle suvandi väärtuseks *Jah*, määratakse suvandi **Luba segatud varude partiid** väärtuseks *Jah* ja seda ei saa eraldi muuta.)

1. Valige käsk **Salvesta**.

### <a name="set-up-a-location"></a>Asukoha seadistamine

1. Avage **Laohaldus \> Seadistus \> Ladu \> Asukohad**.
1. Tühjendage päises märkeruut **Loo kontrollnumbrid asukoha jaoks**.
1. Valige toimingupaanil **Uus**, et luua asukoht ja määrake sellele järgmised väärtused.

    - **Ladu:** *62*
    - **Asukoht:** *SORT*
    - **Asukohaprofiili ID:** *SORTIMINE*

1. Valige käsk **Salvesta**.

### <a name="set-up-an-outbound-sorting-template"></a>Väljamineku sortimismalli seadistamine

Väljamineku sortimismall määratleb, kas töö luuakse sortimise asukohast ja kas sortimine toimub käsitsi või automaatselt.

Selle stsenaariumi korral loote väljamineku sortimismalli, et koostada kaubaaluseid pärast pakkimisjaama.

1. Avage jaotis **Laohaldus \> Seadistus \> Pakkimine \> Väljamineku sortimismallid**.
1. Valige toimingupaanil nupp **Uus**.
1. Määrake uue malli päises järgmised väärtused.

    - **Väljamineku sortimismalli ID:** *AutoWork*
    - **Kirjeldus:** *Automaatne töö loomine*
    - **Väljamineku sortimismalli tüüp:** *Konteiner*
    - **Ladu:** *62*
    - **Asukoht:** *SORT*

1. Määrake kiirkaardil **Üldine** järgmised väärtused.

    - **Sortimise kontrollimine:** *Asukoha skannimine*
    - **Loo töö asukoha sulgemisel:** *Jah*

        Kui selle suvandi väärtuseks on seatud *Jah*, kui asukoht on suletud, luuakse töö varude lõppsihtkohta teisaldamiseks. Kui väärtuseks on seatud *Ei*, komplekteeritakse varud asukoha sulgemisel kohe tellimusele.

    - **Asukoha määramine:** *Automaatne*

        Kui välja väärtuseks on seatud *Käsitsi*, peab kasutaja alati näitama, millisesse asukohta varud sortida tuleb. Kui selleks on seatud *Automaatne*, juhib süsteem varud võimaluse korral automaatselt asukohta, võttes aluseks sortimismalli jaotamised.

1. Valige **Salvesta**, et muuta nupp **Redigeeri päringut** toimingupaanil kättesaadavaks.
1. Valige toimingupaanil **Päringu redigeerimine**.
1. Lisage päringuredaktoris vahekaardile **Sortimine** rida, millel on järgmised väärtused.

    - **Tabel:** *Saadetised*
    - **Tuletatud tabel:** *Saadetised*
    - **Väli:** *Vedaja teenus*

        Kui valite selle väärtuse, võidakse kuvada järgmine teade: „Väli Vedaja teenus pole indeksi väli. Kas soovite lisada sellele sortimise?” Valige **Jah**.

    - **Otsingusuund:** *Kasvav*

1. Valige nupp **OK**.
1. Teile võidakse kuvada järgmine teade: „Grupeerimine lähtestatakse, kas soovite jätkata?” Valige **Jah**.

    Toimingupaani nupp **Väljamineku sortimismalli piirid** muutub kättesaadavaks.

1. Valige toimingupaanil **Väljamineku sortimismalli piirid**.
1. Määrake dialoogiboksis **Väljamineku sortimise kriteeriumid** järgmised väärtused.

    - **Viitetabeli nimi:** *Saadetised*
    - **Viitevälja nimi:** *Vedaja teenus*
    - **Grupeeri välja alusel:** märkige see ruut, et grupeerida saadetised vedaja teenuse alusel.

1. Valige **OK**, et salvestada oma sätted ja sulgeda dialoogiboks.

### <a name="set-up-container-packing-policies"></a>Konteineri pakkimise poliitikate seadistamine

1. Avage jaotis **Laohaldus \> Seadistus \> Konteinerid \> Konteineri pakkimise poliitikad**.
1. Valige toimingupaanil nupp **Uus**.
1. Määrake uue poliitika päises järgmised väärtused.

    - **Konteineri pakkimise poliitika:** *Sortimine*
    - **Kirjeldus:** *Sortimine*

1. Määrake kiirkaardil **Ülevaade** järgmised väärtused.

    - **Ladu:** *62*
    - **Sortimise vaikeasukoht:** *SORTIMINE*
    - **Massiühik:** *kg*
    - **Konteineri sulgemise poliitika:** *Automaatne väljastamine*
    - **Konteineri väljastamise poliitika:** *Konteineri määramine väljamineku sortimise asukohale*

1. Valige käsk **Salvesta**.

### <a name="set-up-packing-profiles"></a>Pakkimisprofiilide seadistamine

Looge uus pakkimisprofiil, mida kasutatakse koos sortimise funktsiooniga.

1. Avage jaotis **Laohaldus \> Seadistus \> Pakkimine \> Pakkimisprofiilid**.
1. Valige toimingupaanil **Uus**, et luua rida ja määrake sellele järgmised väärtused.

    - **Pakkimisprofiili ID:** *Sortimine*
    - **Kirjeldus:** *Sortimine*
    - **Konteineri pakkimise poliitika:** *Sortimine*
    - **Konteineri ID-režiim:** *Automaatne*
    - **Konteineri tüüp:** *Box-Large*
    - **Konteineri automaatne loomine konteineri sulgemisel:** tühjendatud (= *Ei*)

1. Valige käsk **Salvesta**.

### <a name="set-up-work-classes"></a>Töö klasside seadistamine

Seadistage töö klass, mida kasutatakse koos sortimisega.

1. Minge jaotisse **Laohaldus \> Seadistus \> Töö \> Töö klassid**.
1. Valige toimingupaanil **Uus**, et luua sortimiseks töö klass ja määrake sellele järgmised väärtused.

    - **Töö klassi ID:** *Sortimine*
    - **Kirjeldus:** *Sortimine*
    - **Töötellimuse tüüp:** *Sorditud varude komplekteerimine*

1. Valige käsk **Salvesta**.

### <a name="set-up-mobile-device-menu-items"></a>Mobiilse seadme menüü-üksuste seadistamine

#### <a name="set-up-a-new-pallet-menu-item"></a>Uue kaubaaluse menüü-üksuse seadistamine

Looge mobiilse seadme menüü-üksus kaubaaluste loomiseks sortimise ajal.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.
1. Valige toimingupaanil nupp **Uus**.
1. Määrake päises järgmised väärtused.

    - **Menüü-üksuse nimi:** *Kaubaaluse loomine*
    - **Pealkiri:** *Kaubaaluse loomine*
    - **Režiim:** *Kaudne*
    - **Kasuta olemasolevat tööd:** *Ei*

1. Määrake kiirkaardil **Üldine** järgmised väärtused.

    - **Tegevuse kood:** *Väljamineku sortimine*

        Kui selle välja väärtuseks on seatud *Väljamineku sortimine*, kuvatakse väli **Väljamineku sortimismalli ID**.

    - **Protsessijuhendi kasutamine:** *Jah*

        Kui välja **Tegevuse kood** on seatud *Väljamineku sortimine*, seatakse selle suvandi väärtuseks automaatselt *Jah*.

    - **Väljamineku sortimismalli ID:** *AutoWork*

1. Valige käsk **Salvesta**.

#### <a name="set-up-a-new-loading-menu-item"></a>Uue laadimise menüü-üksuse seadistamine

Järgmisena looge menüü-üksus, mis võimaldab kasutajatel teisaldada sorditud laokaupu saadetise asukohta.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.
1. Valige toimingupaanil nupp **Uus**.
1. Määrake päises järgmised väärtused.

    - **Menüü-üksuse nimi:** *Laadimine sortimisest*
    - **Pealkiri:** *Laadimine sortimisest*
    - **Režiim:** *töö*
    - **Kasuta olemasolevat tööd:** *Jah*

1. Määrake kiirkaardi **Üldine** väljal **Suunaja** väärtuseks *Kasutaja suunatud*.
1. Valige kiirkaardil **Tööklassid** suvand **Uus** ja seejärel seadke järgmised väärtused.

    - **Töö klassi ID:** *SORTIMINE*
    - **Töötellimuse tüüp:** *Sorditud varude komplekteerimine*

1. Valige käsk **Salvesta**.

### <a name="set-up-the-mobile-device-menu"></a>Mobiilse seadme menüü seadistamine

Nüüd peate lisama uued menüü-üksused mobiilse seadme menüüsse.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü**.
1. Valige menüü **Väljaminev**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Otsige üles ja valige veerus **Saadaolevad menüüd ja menüü-üksused** suvand **Kaubaaluse loomine**.
1. Valige paremnoole nupp, et teisaldada **Kaubaaluse loomine** veergu **Menüü struktuur**.
1. Kasutage üles- ja allanoole nuppe, et lisada menüü-üksus **Kaubaaluse loomine** mobiilse seadme menüüs soovitud asukohta.
1. Valige käsk **Salvesta**.
1. Korrake seda protseduuri, et lisada menüü-üksus **Laadimine sortimisest** menüüsse **Väljaminev**.

### <a name="set-up-location-directives"></a>Asukohakorralduste häälestamine

*Asukohakorraldused* on reeglid, mis aitavad tuvastada komplekteerimise ja ladustamise asukohti varude liigutamisel. Nüüd tuleb luua reegel sortimise töö haldamiseks.

#### <a name="set-up-a-single-sku-directive"></a>Üksiku SKU-korralduse seadistamine

1. Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.
1. Muutke vasakpoolsel paanil välja **Töökäsu tüüp** väärtuseks *Sorditud varude komplekteerimine*.
1. Valige toimingupaanil nupp **Uus**.
1. Määrake päises järgmised väärtused.

    - **Järjestus:** *1*
    - **Nimi:** *Baydoor*

1. Määrake kiirkaardil **Asukohakorraldused** järgmised väärtused.

    - **Töö tüüp:** *Ladustamine*
    - **Tegevuskoht:** *6*
    - **Ladu:** *62*
    - **Mitu SKU-d:** *Ei*

1. Valige **Salvesta**, et muuta tööriistariba kiirkaardil **Read** kättesaadavaks.
1. Valige kiirkaardil **Read** suvand **Uus** ja seejärel seadke uuel real järgmised väärtused. Võtke vastu kõigi teiste väljade vaikeväärtused.

    - **Järjestus:** *1*
    - **Alates:** *0*
    - **Kuni:** *1 000 000*

1. Valige **Salvesta**, et muuta tööriistariba kiirkaardil **Asukohakorralduse toimingud** kättesaadavaks.
1. Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus** ja seejärel seadke uuel real järgmised väärtused. Võtke vastu kõigi teiste väljade vaikeväärtused.

    - **Järjestus:** *1*
    - **Nimi:** *Baydoor*

1. Valige käsk **Salvesta**.
1. Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Päringu redigeerimine**.
1. Otsige päringuredaktori vahekaardil **Vahemik** üles rida, kus välja **Väli** väärtuseks on seatud *Asukoht*. Määrake selle rea välja **Kriteeriumid** väärtuseks *Baydoor*.
1. Oma sätete salvestamiseks ja päringuredaktori sulgemiseks valige **OK**.

#### <a name="set-up-a-multiple-sku-directive"></a>Mitme SKU-korralduse seadistamine

1. Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.
1. Muutke vasakpoolsel paanil välja **Töökäsu tüüp** väärtuseks *Sorditud varude komplekteerimine*.
1. Valige toimingupaanil nupp **Uus**.
1. Määrake päises järgmised väärtused.

    - **Järjestus:** *2*
    - **Nimi:** *Mitmik-Baydoor*

1. Määrake kiirkaardil **Asukohakorraldused** järgmised väärtused.

    - **Töö tüüp:** *Ladustamine*
    - **Tegevuskoht:** *6*
    - **Ladu:** *62*
    - **Mitu SKU-d:** *Jah*

1. Valige **Salvesta**, et muuta tööriistariba kiirkaardil **Read** kättesaadavaks.
1. Valige kiirkaardil **Read** suvand **Uus** ja seejärel seadke uuel real järgmised väärtused. Võtke vastu kõigi teiste väljade vaikeväärtused.

    - **Järjestus:** *1*
    - **Alates:** *0*
    - **Kuni:** *1 000 000*

1. Valige **Salvesta**, et muuta tööriistariba kiirkaardil **Asukohakorralduse toimingud** kättesaadavaks.
1. Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus** ja seejärel seadke uuel real järgmised väärtused. Võtke vastu kõigi teiste väljade vaikeväärtused.

    - **Järjestus:** *1*
    - **Nimi:** *Mitmik-Baydoor*

1. Valige käsk **Salvesta**.
1. Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Päringu redigeerimine**.
1. Otsige päringuredaktori vahekaardil **Vahemik** üles rida, kus välja **Väli** väärtuseks on seatud *Asukoht*. Määrake selle rea välja **Kriteeriumid** väärtuseks *Baydoor*.
1. Oma sätete salvestamiseks ja päringuredaktori sulgemiseks valige **OK**.

### <a name="set-up-work-templates"></a>Töömallide häälestamine

1. Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.
1. Muutke välja **Töökäsu tüüp** väärtuseks *Sorditud varude komplekteerimine*.
1. Töömalli loomiseks valige toimingupaanilt suvand **Uus**.
1. Vahekaardil **Ülevaade** määrake järgmised väärtused.

    - **Järjestus:** *1*
    - **Töömall:** *Sortimine*
    - **Töömalli kirjeldus:** *Sortimine*

1. Valige **Salvesta**, et muuta kiirkaart **Töömalli üksikasjad** kättesaadavaks.
1. Valige kiirkaardil **Töömalli üksikasjad** suvand **Jah**, et lisada rida ja seejärel seadke sellele järgmised väärtused.

    - **Töö tüüp:** *Komplekteerimine*
    - **Töö klassi ID:** *SORTIMINE*

1. Valige uuesti **Uus**, et lisada teine rida ja seejärel seadke sellele järgmised väärtused.

    - **Töö tüüp:** *Ladustamine*
    - **Töö klassi ID:** *SORTIMINE*

1. Valige käsk **Salvesta**.

## <a name="scenario"></a>Stsenaarium

See stsenaarium simuleerib olukorda, kus pakitud konteinerid tuleks pärast pakkimisjaama sorteerida automaatselt erinevatesse asukohtadesse (kaubaalustele), sõltuvalt saadetise vedaja teenusest. Kui kõik koormuse kõik kaubad on pakitud ja sorditud aadressi järgi, teisaldatakse kaubaalused laadimisukse juurde.

### <a name="create-sales-orders-and-picking-work"></a>Müügitellimuste ja komplekteerimistöö loomine

#### <a name="create-sales-order-1"></a>Müügitellimuse 1 loomine

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Valige toimingupaanil nupp **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - **Kliendi konto:** *US-005*
    - **Ladu:** *62*

1. Valige dialoogiboksi sulgemiseks suvand **OK**.

    Avatakse uus müügitellimus.

1. Lülituge vaatele **Päis**.
1. Määrake kiirkaardi **Tarne** jaotises **Transport** järgmised väärtused.

    - **Vedaja:** *Kaubalennuk*
    - **Vedaja teenus:** *Õhk*

1. Minge vaatesse **Read**.
1. Kui uut rida ei lisata ruudustikku automaatselt, siis valige kiirkaardil **Müügitellimuse read** suvand **Lisa rida** selle lisamiseks.
1. Määrake uuel tellimuse real järgmised väärtused.

    - **Kauba kood:** *A0001*
    - **Kogus:** *2*

1. Kui uus tellimuse rida on veel valitud, valige kiirkaardi **Müügitellimuse read** ruudustiku kohal olevas menüüs **Varud** suvand **Reserveerimine**.
1. Valige lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida laos kogu valitud rea kogus.
1. Müügitellimuse juurde naasmiseks sulgege leht **Reserveerimine**.
1. Tehke tegevuspaani vahekaardil **Ladu** grupis **Tegevused** valik **Vabasta lattu**.
1. Saate teate, mis näitab saadetist ja voogu selle tellimuse jaoks. Märkige üles voo ID-kood ja saadetise ID-kood.

#### <a name="sales-order-2"></a>Müügitellimus 2

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Valige toimingupaanil nupp **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - **Kliendi konto:** *US-006*
    - **Ladu:** *62*

1. Valige dialoogiboksi sulgemiseks suvand **OK**.
1. Avatakse uus müügitellimus. See peaks sisaldama uut tühja rida kiirkaardi **Müügitellimuse read** ruudustikus. Määrake sellel tellimuse real järgmised väärtused.

    - **Kaup:** *A0001*
    - **Kogus:** *1*

1. Määrake kiirkaardi **Rea üksikasjad** vahekaardil **Tarne** välja **Tarneviis** väärtuseks *Flowe-STD*.
1. Valige kiirkaardil **Müügitellimuse read** suvand **Lisa rida** ja seejärel seadke teisel tellimuse real järgmised väärtused.

    - **Kaup:** *A0002*
    - **Kogus:** *1*

1. Muutke kiirkaardi **Rea üksikasjad** vahekaardil **Tarne** välja **Tarneviis** väärtuseks *Air C-Air*.
1. Valige kiirkaardil **Müügitellimuse read** esimene tellimuse rida. Seejärel valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.
1. Valige lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida laos kogu valitud rea kogus.
1. Müügitellimuse juurde naasmiseks sulgege leht **Reserveerimine**.
1. Valige kiirkaardil **Müügitellimuse read** teine tellimuse rida. Seejärel valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.
1. Valige lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida laos kogu valitud rea kogus.
1. Müügitellimuse juurde naasmiseks sulgege leht **Reserveerimine**.
1. Tehke tegevuspaani vahekaardil **Ladu** grupis **Tegevused** valik **Vabasta lattu**.
1. Saate teate, mis näitab saadetist ja voogu selle tellimuse jaoks. Pange tähele, et loodi kaks voo ID-numbrit ja kaks saadetise ID-numbrit, üks iga tarneviisi tarneviisi jaoks müügitellimuse ridadel.

#### <a name="get-the-work-ids-from-the-work-details"></a>Töö ID-de hankimine töö üksikasjadest

1. Avage jaotis **Laohaldus \> Töö \> Töö üksikasjad**.
1. Lehel kuvatakse müügitellimustest loodud töö ID-d. Kasutage enda loodud müügitellimuste voo ID-sid ja saadetise ID-sid, et leida iga voo ja saadetise töö ID. Märkige need töö ID-d üles, sest vajate neid järgmistes etappides. Pange tähele, et teise müügitellimuse jaoks loodi kaks töö ID-d. Kui erinevatest asukohtadest komplekteeritakse erinevaid kaupasid, luuakse eraldi töö ID-d.

### <a name="pick-items-for-the-sales-orders"></a>Kaupade komplekteerimine müügitellimustesse

Viige loodud töö lõpule, kasutades mobiilset seadet kaupade teisaldamiseks pakkimisjaama.

1. Logige mobiilses seadmes sisse lattu *62*, kasutades selleks stsenaariumi jaoks loodud kasutaja ID-d (või olemasoleva demoandmete kasutaja ID-d).
1. Valige peamenüüs suvand **Väljaminev**.
1. Valige menüüs **Väljaminev** suvand **Müügi komplekteerimine**.
1. Sisestage väljale **ID** müügitellimuse 1 jaoks loodud töö ID.
1. Valige nupp **OK**.
1. Sisestage lehel **Müügitellimused – komplekteerimine** siht-LP, mis loodi müügitellimuse 1 jaoks. Pange tähele, et kuvatakse komplekteerimise asukoht (*hulgi-001*), kaup (*A0001*) ja kogus (*2 tk*).
1. Valige nupp **OK**.
1. Vaadake üle teave lehel **Ostutellimused – sisestatud**. Väli **Loc** peaks näitama, et komplekteeritud kaubad lähevad asukohta *Pakkimine*.
1. Valige nupp **OK**.

    Lehel **Skanni töö ID / identifitseerimisnumbri ID** teade „Töö lõpule viidud”, mis näitab, et töö ID müügitellimusest 1 on lõpule viidud.

    Nüüd saate komplekteerida müügitellimuse 2.

1. Sisestage väljale **ID** töö ID, mis loodi müügitellimuse 2 jaoks, kus real 1 on kaup *A0001*.
1. Valige nupp **OK**.
1. Sisestage lehele **Müügitellimused – komplekteerimine** siht-LP. Pange tähele, et kuvatakse komplekteerimise asukoht (*hulgi-001*), kaup (*A0001*) ja kogus (*1 tk*).
1. Valige nupp **OK**.
1. Vaadake üle teave lehel **Ostutellimused – sisestatud**. Väli **Loc** peaks näitama, et komplekteeritud kaubad lähevad asukohta *Pakkimine*.
1. Valige nupp **OK**.

    Lehel **Skanni töö ID / identifitseerimisnumbri ID** teade „Töö lõpule viidud”. See teade näitab, et müügitellimuse 2 rea 1 töö ID on lõpule viidud.

1. Sisestage väljale **ID** töö ID, mis loodi müügitellimuse 2 jaoks, kus real 2 on kaup *A0002*.
1. Valige nupp **OK**.
1. Sisestage lehele **Müügitellimused – komplekteerimine** siht-LP. Pange tähele, et kuvatakse komplekteerimise asukoht (*hulgi-002*), kaup (*A0001*) ja kogus (*1 tk*).
1. Valige nupp **OK**.
1. Vaadake üle teave lehel **Ostutellimused – sisestatud**. Väli **Loc** peaks näitama, et komplekteeritud kaubad lähevad asukohta *Pakkimine*.
1. Valige nupp **OK**.

    Lehel **Skanni töö ID / identifitseerimisnumbri ID** teade „Töö lõpule viidud”. See teade näitab, et müügitellimuse 2 rea 2 töö ID on lõpule viidud.

### <a name="pack-sales-orders-into-containers"></a>Müügitellimuste pakkimine konteineritesse

#### <a name="pack-sales-order-1-into-containers"></a>Müügitellimuse 1 pakkimine konteineritesse

1. Avage jaotis **Laohaldus \> Pakkimine ja konteinerisse paigutamine \> Pakkimine**.

    Kuvatavas dialoogiboks **Pakkimisjaama valimine**. Vaikimisi peaks olema väljal **Töötaja** töötaja nimi, mille seadistasite eelnevalt.

1. Määrake järgmised väärtused kindlas pakkimisasukohas plaanitud saadetiste ja konteinerite kuvamiseks ja nendega töötamiseks.

    - **Tegevuskoht:** *6*
    - **Ladu:** *62*
    - **Asukoht:** *Pakkimine*
    - **Pakkimisprofiili ID:** *Sortimine*

1. Valige dialoogiboksi sulgemiseks suvand **OK**.
1. Sisestage lehe **Pakkimine** väljale **Identifitseerimisnumber** müügitellimuse 1 siht-LP. Seejärel valige **Vahekaart** või vajutage klaviatuuril **Sisestusklahvi (Enter)** väljalt väljumiseks.
1. Valige toimingupaanil nupp **Uus konteiner**.
1. Nõustuge kõigi vaikesätetega ja valige **OK**. Märkige üles konteineri ID.
1. Määrake kiirkaardil **Kauba pakkimine** järgmised väärtused.

    - **Kogus:** *1*
    - **Identifikaator:** kaup *A0001*

1. Valige toimingupaanil nupp **Sule konteiner**.
1. Valige dialoogiboksis **Sule konteiner** suvand **Süsteemi kaalu toomine**, et süsteem värskendaks välja **Brutokaal**.
1. Valige nupp **OK**. Konteiner teisaldatakse asukohta *SORTIMINE* ja on sortimiseks valmis.
1. Looge teine konteiner, et lisada teine kaup müügitellimuse 1 LP-st uude konteinerisse.
1. Valige toimingupaanil nupp **Uus konteiner**.
1. Nõustuge kõigi vaikesätetega ja valige **OK**. Märkige üles konteineri ID.
1. Määrake kiirkaardil **Kauba pakkimine** järgmised väärtused.

    - **Kogus:** *1*
    - **Identifikaator:** kaup *A0001*

1. Valige toimingupaanil nupp **Sule konteiner**.
1. Valige dialoogiboksis **Sule konteiner** suvand **Süsteemi kaalu toomine**, et süsteem värskendaks välja **Brutokaal**.
1. Valige nupp **OK**. Konteiner teisaldatakse asukohta *SORTIMINE* ja on sortimiseks valmis.

#### <a name="pack-sales-order-2-into-containers"></a>Müügitellimuse 2 pakkimine konteineritesse

1. Sisestage lehe **Pakkimine** väljale **Identifitseerimisnumber** siht-LP müügitellimuse 2 rea 1 jaoks. Seejärel valige **Vahekaart** või vajutage klaviatuuril **Sisestusklahvi (Enter)** väljalt väljumiseks.
1. Valige toimingupaanil nupp **Uus konteiner**.
1. Nõustuge kõigi vaikesätetega ja valige **OK**. Märkige üles konteineri ID.
1. Määrake kiirkaardil **Kauba pakkimine** järgmised väärtused.

    - **Kogus:** *1*
    - **Identifikaator:** kaup *A0001*

1. Valige toimingupaanil nupp **Sule konteiner**.
1. Valige dialoogiboksis **Sule konteiner** suvand **Süsteemi kaalu toomine**, et süsteem värskendaks välja **Brutokaal**.
1. Valige nupp **OK**. Konteiner teisaldatakse asukohta *SORTIMINE* ja on sortimiseks valmis.
1. Sisestage väljale **Identifitseerimisnumber või saadetis** siht-LP müügitellimuse 2 rea 2 jaoks. Seejärel valige **Vahekaart** või vajutage klaviatuuril **Sisestusklahvi (Enter)** väljalt väljumiseks.
1. Valige toimingupaanil nupp **Uus konteiner**.
1. Nõustuge kõigi vaikesätetega ja valige **OK**. Märkige üles konteineri ID.
1. Määrake kiirkaardil **Kauba pakkimine** järgmised väärtused.

    - **Kogus:** *1*
    - **Identifikaatori väli:** kaup *A0002*

1. Valige toimingupaanil nupp **Sule konteiner**.
1. Valige dialoogiboksis **Sule konteiner** suvand **Süsteemi kaalu toomine**, et süsteem värskendaks välja **Brutokaal**.
1. Valige nupp **OK**. Konteiner teisaldatakse asukohta *SORTIMINE* ja on sortimiseks valmis.

Konteineri üksikasjade kuvamiseks avage jaotis **Laohaldus \> Pakkimine ja konteinerisse määramine \> Konteinerid** ja otsige pakkimise ajal loodud konteineri ID-sid.

### <a name="sort-the-containers"></a>Konteinerite sortimine

> [!IMPORTANT]
> Kui avate mobiilirakenduses menüü-üksuse **Kaubaaluse loomine**, et teha väljamineku sortimist, kuvatakse nupp, mille märgistus on **Täielik**. *Ärge kasutage nuppu **Täielik** asukoha sortimiseks või sulgemiseks.*
>
> Nupp **Täielik** on vaikimisi saadaval ja seda ei saa lehelt keelata ega eemaldada. Seda ei kasutata funktsiooni *Väljamineku sortimine*.

#### <a name="sort-the-first-container"></a>Esimese konteineri sortimine

1. Logige mobiilses seadmes sisse lattu *62*, kasutades selleks stsenaariumi jaoks loodud kasutaja ID-d (või olemasoleva demoandmete kasutaja ID-d).
1. Valige peamenüüs suvand **Väljaminev**.
1. Valige menüüs **Väljaminev** suvand **Kaubaaluse loomine**.
1. Sisestage väljale **LP/Con** esimese konteineri ID, mis on seostatud müügitellimusega 1.
1. Valige nupp **OK**.
1. Kuna ühtegi sortimise asukohta pole praegu olemas, peate selle määrama. Sisestage väljale **Sortimise asukoha ID** väärtus *SP01*.
1. Kuna ükski LP pole praegu seotud asukohaga *SP01*, peate selle määrama. Sisestage väljale **LP** väärtus *PLP01*.
1. Valige nupp **OK**.
1. Kuna sortimise asukoha kinnitamine on sisse lülitatud, peate sisestama sortimise asukoha ID uuesti. Sisestage väljale **Sortimise asukoha ID** väärtus *SP01*.
1. Valige nupp **OK**.

    Teile kuvatakse teade „Töö lõpule viidud”.

> [!TIP]
> Sortimise asukoha ja selles oleva LP kuvamiseks avage jaotis **Laohaldus \> Pakkimine ja konteinerisse määramine \> Väljamineku sortimise asukoha määramised**.
>
> Lehel **Väljamineku sortimise asukoha määramised** kuvatakse kõik praegu aktiivsed sortimise asukohad. Väljal **Sortimise asukoha kanded** kuvatakse LP, mis on seostatud iga sortimise asukohaga ja selles asukohas olevad konteinerid. Pange tähele, et üks sortimise asukoht on praegu olemas ja kiirkaardil **Sortimise asukoha kriteeriumid** kuvatakse kriteerium **Saadetis – vedaja teenus – õhk**.

#### <a name="sort-the-remaining-containers"></a>Järelejäänud konteinerite sortimine

1. Logige mobiilses seadmes sisse lattu *62*, kasutades selleks stsenaariumi jaoks loodud kasutaja ID-d (või olemasoleva demoandmete kasutaja ID-d).
1. Valige peamenüüs suvand **Väljaminev**.
1. Valige menüüs **Väljaminev** suvand **Kaubaaluse loomine**.
1. Sisestage väljale **LP/Con** teise konteineri ID, mis on seostatud müügitellimusega 1.
1. Valige nupp **OK**. Kuna sortimismall on seadistatud automaatselt sortima ja vastavate kriteeriumidega sortimise asukoht on juba olemas, suunatakse teid automaatselt õigesse sortimise asukohta.
1. Valige nupp **OK**.
1. Kinnitage sortimise asukoha ID, et näidata, et varud on õiges kohas. Sisestage väljale **Sortimise asukoha ID** väärtus *SP01*.
1. Valige nupp **OK**.

    Töö müügitellimuse 1 teise konteineriga on lõpule viidud. Nüüd saate sortida müügitellimuse 2 ülejäänud konteinerid.

1. Sisestage väljale **LP/Con** müügitellimuse 2 konteineri ID, milles on kaup *A0001*. Kuna vedaja teenus on erinev, palutakse teil sisestada uus sortimise asukoht ja määrata sellele asukohale LP. Kasutage sortimise asukohta *SP02* ja LP-d *PLP02*.
1. Valige nupp **OK**.
1. Kinnitage sortimise asukoht, sisestades väljale **Sortimise asukoha ID** väärtuse *SP02*.
1. Valige nupp **OK**.

    Töö konteineriga on lõpule viidud.

1. Sisestage väljale **LP/Con** müügitellimuse 2 järelejäänud konteineri ID, milles on kaup *A0002*. Kuna vedaja teenus ühtib müügitellimuse 1 vedaja teenusega, kuvab süsteem olemasoleva sortimise asukoha, millel on vastavad kriteeriumid.
1. Valige nupp **OK**.
1. Kinnitage sortimise asukoht, sisestades väljale **Sortimise asukoha ID** väärtuse *SP01*.
1. Valige nupp **OK**.

    Töö konteineriga on lõpule viidud.

### <a name="close-the-outbound-sorting-positions"></a>Väljamineku sortimise asukohtade sulgemine

Kui kõik varud on sorditud, tuleb asukoht enne töö loomist sulgeda. Luuakse sorditud varude komplekteerimistöö, et teisaldada varud laadimisukse juurde.

#### <a name="close-a-position-from-the-mobile-device"></a>Asukoha sulgemine mobiilsest seadmest

1. Logige mobiilses seadmes sisse lattu *62*, kasutades selleks stsenaariumi jaoks loodud kasutaja ID-d (või olemasoleva demoandmete kasutaja ID-d).
1. Valige peamenüüs suvand **Väljaminev**.
1. Valige menüüs **Väljaminev** suvand **Kaubaaluse loomine**.
1. Sisestage väljale **LP/Con** konteineri ID, mis sorditi sortimise asukohta *SP01*.
1. Valige nupp **OK**.
1. Teile kuvatakse järgmine teade: „Konteiner on juba sorditud asukohta SP01. Kas soovite selle asukoha sulgeda?” Valige suvand **Sule**.

    Töö on lõpule viidud.

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a>Asukoha sulgemine väljamineku sortimise asukoha määramistest

1. Avage jaotis **Laohaldus \> Pakkimine ja konteinerisse määramine \> Väljamineku sortimise asukoha määramised**.
1. Valige vasakust veerust **SP02**. See väljamineku sortimise asukoha rida on see, mille sulgete.
1. Valige toimingupaanil nupp **Sule asukoht**. Sortimise asukoha kirje on suletud ja seda enam ei kuvata.

    > [!TIP]
    > Kõigi suletud asukoha kirjete kuvamiseks märkige ruut **Kuva suletud**.

### <a name="sorted-inventory-picking"></a>Sorditud varude komplekteerimine

Peate viima lõpule sorditud varude komplekteerimistöö. Kui see on lõpule viidud, komplekteeritakse varud müügitellimusele. Seejärel kehtivad kõik muud laoprotsessid.

1. Logige mobiilses seadmes sisse lattu *62*, kasutades selleks stsenaariumi jaoks loodud kasutaja ID-d (või olemasoleva demoandmete kasutaja ID-d).
1. Valige peamenüüs suvand **Väljaminev**.
1. Valige menüüs **Väljaminek** suvand **Laadi sortimisest**.
1. Sisestage esimese sortimise asukoha siht-LP ID *SP01*. Määrake välja **ID** väärtuseks *PLP01*.
1. Valige nupp **OK**.
1. Lehel **Sorditud varude komplekteerimine: komplekteerimine** kuvatakse komplekteerimistöö, mida tuleb teha. Komplekteerige askohast *SORTIMINE* ja siht-LP-st *PLP01*, millel on mitu kaupa ja kogus *3*.
1. Valige nupp **OK**.
1. Lehel **Sorditud varude komplekteerimine: sisestatud** kuvatakse sisestamistöö, mida tuleb teha. Sisestage askohta *Baydoor* ja siht-LP *PLP01*, millel on mitu kaupa ja kogus *3*.
1. Valige nupp **OK**.

    Töö on lõpule viidud.

1. Sisestage teise sortimise asukoha identifitseerimisnumbri ID *SP02*. Määrake välja **ID** väärtuseks *PLP02*.
1. Valige nupp **OK**.
1. Lehel **Sorditud varude komplekteerimine: komplekteerimine** kuvatakse komplekteerimistöö, mida tuleb teha. Komplekteerige askohast *SORTIMINE* ja siht-LP-st *PLP02*, millel on mitu kaupa ja kogus *1*.
1. Valige nupp **OK**.
1. Lehel **Sorditud varude komplekteerimine: sisestatud** kuvatakse sisestamistöö, mida tuleb teha. Sisestage askohta *Baydoor* ja siht-LP *PLP02*, millel on mitu kaupa ja kogus *1*.
1. Valige nupp **OK**.

    Töö on lõpule viidud.

Sellest alates kehtivad kõik muud laoprotsessid.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]