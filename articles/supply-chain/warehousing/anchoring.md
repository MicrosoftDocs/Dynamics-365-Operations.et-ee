---
title: Ankurdamine
description: See teema kirjeldab ankurdamise lubamist ja kasutamist.
author: GalynaFedorova
ms.date: 07/29/2021
ms.topic: article
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-29
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a17574cccbdf6f26f0453bda67eabaa16d559cd3
ms.sourcegitcommit: 99bde425ade701ef244c6bca6d411aef94a59b3c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/20/2021
ms.locfileid: "7505562"
---
# <a name="anchoring"></a>Ankurdamine

[!include [banner](../includes/banner.md)]

See teema annab üksikasju ankurdamise protsessi kohta. See kirjeldab nõutavat konfiguratsiooni ja loogikat, mis käivitatakse, kui laotöötaja muudab kas ajastamiskohta või laadimise asukohta.

Ankurdamisfunktsioon võimaldab alistada ajastus- või laadimisasukoha. Kõik avatud asetamised suunatakse siis uude teie määratud ajastus- või laadimisasukohta.

See funktsioon aitab töötajatel kaupade lähetamisel tõhusam olla. Järgmisena on toodud mõned näited.

- Töötaja, kes peab esitama esimese tellimuse esemed esimese peatuse asukohta, ei saa seda toimingut lõpule viia, kuna eelmine koormus pole asukohta kustutanud. Selle asemel et oodata, kuni vaheasukoha esimene dokk vabaneb, on töötajal võimalik kasutada teise doki vaheasukohta. Seega tühistab töötaja soovitatud vaheasukoha. Töötellimuse ülejäänud kaupade paigutusasukoht värskendatakse teise doki vaheasukohale.
- Töötaja, kes peab sama tarne puhul teostama mitu valikut, võib olla kindel, et kõik üksused on ühte kohta monteeritud. Seetõttu on vaja vähem aega kaupade laadimiseks veoautole.

Konfigureerige ankurdamine mobiilse seadme menüü-üksuste jaoks **Ankur** suvandi abil. Kui määrate selle suvandi väärtuseks *Jah*, saate välja **Ankurdada** abil määrata, kas soovite ankurdada saadetise või koormuse järgi. Kui seate välja **Ankurdada** alusel väärtuseks *Saadetis*, muudetakse järgnevad avatud asetamised selle saadetise uude asukohta. Kui seate välja väärtuseks *Koormus*, muudetakse järgnevad avatud asetamised selle koormuse uude asukohta.

> [!IMPORTANT]
> Järgmiste avatud panemiste asukohta muudetakse ainult töö ridadel, mis luuakse sama töömalli realt. See tähendab, et süsteem ankurdab samalt töömalli realt pärinevad panemisread.

Selles teemas antakse stsenaarium, mis näitab, kuidas ankurdamine toimib. Selle stsenaariumi käigus loote müügitellimuste komplekti ja väljastate need komplektid lattu. Seejärel alistate soovitatud ajastusasukoha ja kontrollite, et kogu allesjäänud mahajääv töö suunatakse uude asukohta.

## <a name="scenario-prerequisite-make-demo-data-available"></a>Stsenaariumi eeltingimus: demoandmete kättesaadavaks tegemine

Selle teema stsenaarium viitab väärtustele ja kirjetele, mis kuuluvad Microsoft Dynamics 365 Supply Chain Managementile esitatud standardsete demoandmete hulka. Kui soovite kasutada siin esitatud väärtusi harjutuste tegemise ajal, veenduge, et töötate keskkonnas, kuhu on demoandmed installitud ja määrake enne alustamist juriidiliseks isikuks *USMF*.

## <a name="scenario-setup"></a>Stsenaariumi häälestus

Enne näitestsenaariumi läbimist peate vastava mobiilseadme menüüelemendi jaoks ankurdamise lubama.

### <a name="set-up-a-mobile-device-menu-item-to-enable-anchoring"></a>Mobiilse seadme menüükäsu seadistamine ankurdamise lubamiseks

Järgige neid samme mobiilse seadme menüü-üksuse ankurdamise lubamiseks.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüükäsud**.
1. Valige loendipaanil kirje nimega *Müügikorje*. Kui see nimi pole olemasolevatel kirjetel, looge see. Kinnitage või määrake kirjele järgmised väärtused:

    - **Menüükäsu nimi:** *müügi komplekteerimine*
    - **Pealkiri:** *Müügi komplekteerimine*
    - **Režiim:** *töö*
    - **Kasuta olemasolevat tööd:** *Jah*
    - **Lavastaja:** *Kasutaja suunal*
    - **Ankurdamine:** *jah*

        Selle sättega saab süsteem müügi komplekteerimise ajal ankurdada mitu töötellimuse rida.

    - **Ankurdada:** *Koorem*

        See säte põhjustab süsteemi ankurdamise koorma järgi.

    - **Sihtlitsentsiplaadi alistamine:** *jah*
    - **Numbrimärgi alistamine panemise ajal:** *jah*
    - **Hoia töö kasutaja poolt lukustatuna:** *jah*
    - **Luba ülekorje:** *jah*

### <a name="set-up-a-work-template-to-enable-staging"></a>Töömalli loomine etappide konfigureerimise lubamiseks

Järgige neid samme, et konfigureerida töömall, et etappide etappide konfigureerimine oleks võimalik. See konfiguratsioon toetab stsenaariumi, kus töötaja paigutab kaubad tellimuse jaoks paigutamisasukohta.

1. Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.
1. Valige väljal **Töökäsu tüüp** suvand *Müügitellimused*.
1. Valige ruudustikus töömall **61 SO Etapp**.
1. Jaotises **Töömalli üksikasjad** veenduge, et järgmised read on olemas ja konfigureeritud nii, nagu siin näidatud:

    - Rida 1:

        - **Töö tüüp:** *Komplekteerimine*
        - **Kohustuslik:** valitud (= *Jah*)
        - **Töö klassi ID:** *SO-komplekteerimine*

    - Rida 2:

        - **Töö tüüp:** *Ladustamine*
        - **Kohustuslik:** valitud (= *Jah*)
        - **Direktiivi kood:** *Etapp*
        - **Töö klassi ID:** *SO-komplekteerimine*

    - Rida 3:

        - **Töö tüüp:** *Komplekteerimine*
        - **Kohustuslik:** valitud (= *Jah*)
        - **Peata töö:** *Jah*
        - **Töö klassi ID:** *SO-koorem*

    - Rida 4:

        - **Töö tüüp:** *Ladustamine*
        - **Kohustuslik:** valitud (= *Jah*)
        - **Direktiivi kood:** *Ruumid*
        - **Töö klassi ID:** *SO-koorem*

1. Valige toimingupaanil suvand **Redigeeri päringut**, et avada päringuredaktor.
1. Veenduge vahekaardil **Vahemik**, et järgmine rida oleks olemas:

    - **Tabel:** *Ajutised töökanded*
    - **Tuletatud tabel:** *Ajutised töökanded*
    - **Väli:** *Ladu*
    - **Kriteeriumid:** *61*

1. Veenduge vahekaardil **Sorteerimine**, et järgmine rida oleks olemas:

    - **Tabel:** *Ajutised töökanded*
    - **Tuletatud tabel:** *Ajutised töökanded*
    - **Väli:** *Saadetise ID*
    - **Otsingusuund:** *Kasvav*

1. Oma sätete kinnitamiseks ja päringuredaktori sulgemiseks valige **OK**. Aktsepteerige muudatused, kui teilt küsitakse.
1. Valige toimingupaanilt suvand **Tööpäise piirid**.
1. Real, kus välja **Välja nimi** väärtuseks on seatud *Saadetise ID*, tehke kindlaks, et märkeruut **Grupeeri selle välja alusel** on valitud.

### <a name="set-up-license-plates-locations-and-inventory"></a>Litsentsiplaatide, asukohtade ja varude häälestamine

Enne müügitellimuste ja saadetiste loomist peate tagama, et nõutavad asukohad, litsentsiplaadid ja varud on olemas.

1. Minge **Laohaldus \> Häälestus \> Ladu \> Litsentsiplaadid** ja looge kaks litsentsiplaati:

    - MyLP1
    - MyLP2

1. Minge **Laohaldus \> Seadistus \> Ladu \> Asukohad** ja looge järgmised asukohad, kui neid juba ei ole.

    | Ladu | Koht   | Asukoha profiili ID | Tsooni ID   |
    |-----------|------------|---------------------|-----------|
    | 61        | 06A01R2S1B | PICK-06             | PÕRAND     |
    | 61        | 06A01R3S1B | PICK-06             | PÕRAND     |
    | 61        | STAGE01    | STAGE               | *(tühi)* |
    | 61        | STAGE02    | STAGE               | *(tühi)* |
    | 61        | STAGE03    | STAGE               | *(tühi)* |
    | 61        | STAGE04    | STAGE               | *(tühi)* |

1. Veenduge, et järgnev inventuur oleks saadaval. Kui peate korrigeerima varusid, saate luua käsitsi liikumisi, kasutada täiendamist või kasutada mis tahes muud voogu.

    | Kaubakood | Kogus | Ladu | Koht   | Litsentsiplaat |
    |-------------|----------|-----------|------------|---------------|
    | A0001       | 100      | 61        | 06A01R2S1B | MyLP1         |
    | A0002       | 100      | 61        | 06A01R3S1B | MyLP2         |

### <a name="create-demand"></a>Nõudluse loomine

Enne ankurdamisfunktsiooni proovimist peate looma teatud nõudluse. Selle stsenaariumi puhul loote samale kliendile kolm müügitellimust.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Esimese müügitellimuse loomiseks valige **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - **Kliendi konto:** *US-001*
    - **Ladu:** *61*

1. Valige nupp **OK**.
1. Avatakse uus müügitellimus. See lisab tühja rea **Müügitellimuse read** kiirkaardil. Seadke selle rea jaoks järgmised väärtused.

    - **Kauba kood:** *A0001*
    - **Kogus:** *1*

1. Valige tööriistaribal **Lisa rida**, et lisada teine müügitellimuse rida, ja määrake sellele järgmised väärtused:

    - **Kauba kood:** *A0002*
    - **Kogus:** *1*

1. Järgige neid etappe iga müügirea puhul, et reserveerida selle jaoks varud:

    1. Valige kiirkaardil **Müügitellimuse read** müükide tellimuse rida.
    1. Valige tööriistaribal **Varude \> Reserveerimine**.
    1. Valige lehel **Reserveerimine** suvand **Reserveeri saatepartii** ja seejärel sulgege leht.
    1. Valige toimingupaanil nupp **Salvesta**.

1. Teise müükide tellimuse loomiseks korrake samme 2–6. Seadke selle jaoks järgmised väärtused.

    - Dialoogiboksis **Müügitellimuse loomine**:

        - **Kliendi konto:** *US-001*
        - **Ladu:** *61*

    - Müügitellimuse real 1:

        - **Kauba kood:** *A0001*
        - **Kogus:** *2*

    - Müügitellimuse real 2:

        - **Kauba kood:** *A0002*
        - **Kogus:** *2*

1. Müügitellimuse 2 iga rea reserveerimiseks korrake 7. sammu.
1. Kolmanda müükide tellimuse loomiseks korrake samme 2–6. Seadke selle jaoks järgmised väärtused.

    - Dialoogiboksis **Müügitellimuse loomine**:

        - **Kliendi konto:** *US-001*
        - **Ladu:** *61*

    - Müügitellimuse real 1:

        - **Kauba kood:** *A0001*
        - **Kogus:** *3*

    - Müügitellimuse real 2:

        - **Kauba kood:** *A0002*
        - **Kogus:** *3*

1. Müügitellimuse 3 iga rea reserveerimiseks korrake 7. sammu.

### <a name="use-the-load-planning-workbench-to-create-a-load-and-release-it-to-the-warehouse"></a>Koorma planeerimise töölaua kasutamine koorma loomiseks ja lattu vabastamiseks

Järgige neid samme selle stsenaariumi jaoks loodud tellimuste jaoks koormuse loomiseks ja seejärel laos vabastamiseks.

1. Avage **Laohaldus \> Koormused \> Koormuse plaanimise töölaud**.
1. Vahekaardil **Müügiread** leidke ja valige kõik müügitellimuse 1 ja müügitellimuse 2 read.
1. Valige toimingupaani vahekaardi **Pakkumine ja nõudlus** grupis **Lisa** suvand **Uuele koormusele**.
1. Valige dialoogiboksi **Koormuse malli määramine** väljal **Koormuse malli ID** koormuse mall, näiteks *Stnd koormuse mall*.
1. Valige dialoogiboksi sulgemiseks suvand **OK**.
1. Otsige üles ja valige enda loodud koormus jaotises **Koormused**.
1. Valige tööriistaribal **Väljastamine \> Lattu väljastamine**.
1. Dialoogiaknas **Koormuse lattu väljastamine** valige valitud koormuse lattu väljastamiseks **OK**.
1. Avage **Laohaldus \> Töö \> Kõik töö**, et vaadata loodud tööd. Peaksite leidma kaks uut töö ID-d, üks iga saadetise kohta. Igal töö ID-l on komplekteerimise ja asetamise read, mis toovad varud komplekteerimiskohtadest ajastamisasukohta ja ajastamisasukohast ruumini. Märkige üles **Töö ID** väärtus esimesele saadetisele, kuna vajate seda järgmises protseduuris.

### <a name="sales-order-picking-to-the-staging-location-for-the-first-shipment"></a>Müügitellimuse komplekteerimine esimese saadetise paigutamisasukohta

1. Logige mobiilirakendusse Warehouse Management sisse lao *61* töötajana. (Standardsete demoandmete korral saate logida sisse, kasutades _61_ kasutaja ID-na ja paroolina _1_.)
1. Valige peamenüüs suvand **Väljaminev**.
1. Valige menüüs **Väljaminev** suvand **Müügi komplekteerimine**.
1. Valige väli **ID** ja seejärel sisestage esimese saadetise töö ID.
1. Kinnitage kirje.
1. **LP** väljale sisestage esimese kauba (*MinuLP1*) litsentsiplaadi number.
1. Kinnitage kirje.
1. **Siht-LP** väljale sisestage mis tahes number (hilinemise litsentsiplaati ei pea juba olemas olema).

    Peate komplekteerima kõik read, mis loodi töödeldud voost samale sihtidentifitseerimisnumbrile.

1. Kinnitage kirje.
1. **LP** väljale sisestage teise kauba (*MyLP2*) litsentsiplaadi number.
1. Kinnitage kirje.

    Oletage, et töötaja on nüüd tellimuse üles korjanud, aga kui nad saabuvad vaheasukohta, mis töös määratud, leiab ta, et ruum on juba hõivatud. Töötaja näeb siiski, et saadaval on mõni muu lähedal olev asukoht *(STAGE03)*. Seetõttu taotlevad nad muuta vahetamisasukohta. Kuna ankurdamisfunktsioon on lubatud, värskendab süsteem automaatselt selle ja kogu seotud töö ajastusasukohta.

1. Valige **alistamisasukoht**, et pakutavat vaheasukohta alistada.
1. Väljal **Töö erandid** määrake *Vaherada vahetatud*.
1. Sisestage väljale **Asukoht** uus etapiviisiline asukoht (*STAGE03*).
1. Kinnitage kirje. Teile kuvatakse teade „Töö lõpule viidud”.
1. Avage jaotis **Laohaldus \> Töö \> Kõik tööd**.
1. Avage esimese saadetise töö ID. Kontrollige, et vaheasukoht uuendati uude asukohta (*STAGE03*), mis määratleti mobiilse seadmega.
1. Avage teise saadetise töö ID. Kontrollige, et ajastamine oleks ankurdusseadistuse tõttu uuendatud uude ajastamisasukohta (*STAGE03*).

> [!NOTE]
> Kõigi ülejäänud avatud panemistöö ridade asukoht, kus on sama vaheasukoht ja mis loodi sama töömalli realt, uuendatakse uude asukohta.

### <a name="use-the-load-planning-workbench-to-add-the-new-sales-order-to-the-existing-load"></a>Koorma planeerimise töölaua kasutamine uue müügitellimuse lisamiseks olemasolevasse koormusse

Järgige neid samme tellimuse lisamiseks koormale ja seejärel vabastage see lattu.

1. Avage **Laohaldus \> Koormused \> Koormuse plaanimise töölaud**.
1. Vahekaardil **Müügiread** leidke ja valige kõik müügitellimuse 3 read.
1. Valige tegevusepaani vahekaardil **Pakkumine ja nõudlus** rühmas **Lisa** **Olemasolevale koormusele**, et lisada valitud tellimuse read olemasolevale koormusele.
1. Valige dialoogiboksi sulgemiseks suvand **OK**.
1. Otsige üles ja valige eelmistest sammudest koormus jaotises **Koormused**.
1. Valige **Väljastamine \> Lattu väljastamine**.
1. Dialoogiaknas **Koormuse lattu väljastamine** valige valitud koormuse lattu väljastamiseks **OK**.
1. Avage **Laohaldus \> Töö \> Kõik töö**, et vaadata loodud tööd. Märkige üles **Töö ID** väärtus, kuna vajate seda järgmises protseduuris.

### <a name="sales-order-picking-to-the-staging-location-for-the-third-shipment"></a>Müügitellimuse komplekteerimine kolmanda saadetise paigutamisasukohta

1. Logige mobiilirakendusse lao *61* töötajana sisse.
1. Valige peamenüüs suvand **Väljaminev**.
1. Valige menüüs **Väljaminev** suvand **Müügi komplekteerimine**.
1. Valige väli **ID** ja seejärel sisestage kolmanda saadetise töö ID.
1. Kinnitage kirje.
1. **LP** väljale sisestage esimese kauba (*MinuLP1*) litsentsiplaadi number.
1. Kinnitage kirje.
1. **Siht-LP** väljale sisestage mis tahes number (hilinemise litsentsiplaati ei pea juba olemas olema).
1. Kinnitage kirje.
1. **LP** väljale sisestage teise kauba (*MyLP2*) litsentsiplaadi number.
1. Kinnitage kirje.

    Nagu esimese koorma puhul, oletame, et töötaja leiab, et määratud ajakoha asukoht ei ole saadaval. Seetõttu soovivad nad kasutada erinevat etapiviisilist asukoha (*STAGE04*).

1. Valige **alistamisasukoht**, et pakutavat vaheasukohta alistada.
1. Väljal **Töö erandid** määrake *Vaherada vahetatud*.
1. Sisestage väljale **Asukoht** uus etapiviisiline asukoht (*STAGE04*).
1. Kinnitage kirje. Teile kuvatakse teade „Töö lõpule viidud”.
1. Avage jaotis **Laohaldus \> Töö \> Kõik tööd**.
1. Avage esimese saadetise töö ID. Kontrollige, et ajastamiskohta ei uuendatud uude ajastamisasukohta (*STAGE04*), sest järelejääv avatud panemisrida ei vasta lõpuleviidud panemisrea töömalli reale.
1. Avage teise saadetise töö ID. Kontrollige, et vaheasukohta ei uuendatud uude vaheasukohta (*STAGE04*), sest järelejääv vaheasukoht ei vasta lõpuleviidud panemisrea vaheasukoha reale. Teisisõnu on lõpuleviidud panemistöö real ja ülejäänud avatud tööreal erinevad vaheasukohad ja sel juhul uuendatakse ainult ridu, mille vaheasukohad on samad.
1. Avage kolmanda saadetise töö ID. Kontrollige, et ajastamine oleks ankurdusseadistuse tõttu uuendatud uude vaheasukohta (*STAGE04*).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
