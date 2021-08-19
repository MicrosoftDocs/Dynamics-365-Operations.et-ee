---
title: Konteineri pakkimise strateegiad
description: Selles teemas kirjeldatakse konteinerite pakkimise strateegiate vahelisi erinevusi ja tuuakse näiteid.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 4158fa93d9e424e796c038d0c907ea155868440bfcb79666c3e13fa997d4834b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774725"
---
# <a name="container-packing-strategies"></a>Konteineri pakkimise strateegiad

*Konteineri pakkimisstrateegia* on strateegia, mida saate kasutada kauba konteinerite eraldamise määratlemiseks. See teema selgitab erinevusi strateegiate *Pakenda kõikidesse avatud konteineritesse* ja *Pakenda ainult praegusesse konteinerisse*.

- **Pakenda kõikidesse avatud konteineritesse** – süsteem peab kontrollima kõiki avatud konteinereid, mis on konteinerite tsükli jooksul juba loodud, veendumaks, et kaup mahub ühte neist. Pakkimise ajal kontrollib süsteem iga kaupa, kas see mahub mõnda varem loodud konteinerisse. Kui kaup ei mahu olemasolevasse konteinerisse, loob süsteem uue konteineri ja jätkab tööd seni, kuni see on kogu tellimuse pakkimise lõpetanud.

    Näiteks *n* tellitud üksust vajavad konteinerite loomist. Juhtumi puhul kontrollib süsteem iga kord kauba, mis ei mahu olemasolevasse konteinerisse, töötlemisel kokku (\[(*n* – 1) × (*n* + 1)\] ÷ 2) kontrolli, et hinnata, kas kaup mahub olemasolevatesse konteineritesse.

- **Pakenda ainult praegusesse konteinerisse** – süsteem peab kontrollima ainult viimati loodud konteinerit, et veenduda, et üksus sellesse mahuks. Pakkimise ajal kontrollib süsteem iga kaupa, kas see mahub viimati loodud konteinerisse. Kui kaup ei mahu konteinerisse, loob süsteem uue konteineri ja jätkab tööd seni, kuni see on kogu tellimuse pakkimise lõpetanud.

    Näiteks *n* tellitud üksust vajavad konteinerite loomist. Juhtumi puhul teeb süsteem kokku (*n* – 1) kontrolli, et hinnata, kas kaup mahub konteineritesse.

## <a name="example-of-the-flow-for-container-packing-strategies"></a>Konteinerite pakkimise strateegiate voo näide

Saate konteineri jaoks seadistada järgmised üksused.

| Kaup | Füüsilised dimensioonid (laius × sügavus × kõrgus) | Kaal |
|---|---|---|
| HDMI kaabel 6' | 1 × 1 × 1 | 1 |
| HDMI kaabel 12' | 2 × 1 × 1 | 1 |
| HDMI kaabel 18' | 3 × 1 × 1 | 2 |

Seadistate ka järgmise pakendi jaoks kasutatava kasti.

| Konteiner | Füüsilised dimensioonid (pikkus × laius × kõrgus) | Kaal | Maht |
|---|---|---|---|
| Keskmine kast | 6 × 3 × 2 | 10 | 100 |

Lõpuks seadistate tellimuse, mis sisaldab järgmisi tooteid ja koguseid.

| Müügitellimuse rida | Kogus |
|---|---|
| HDMI kaabel 12' | 9 |
| HDMI kaabel 18' | 8 |
| HDMI kaabel 6' | 13 |

Järgmine tabel võtab kokku, kuidas konteinerite loomine toimib, kui kasutate strateegiat *Pakenda kõikidesse avatud konteineritesse* ja kui kasutate strateegiat *Pakenda ainult praegusesse konteinerisse*.

| Pakitakse kõigisse avatud konteineritesse | Pakenda praegusesse konteinerisse |
|---|---|
| <p>HDMI kaabel 12':</p><ol><li>Uue konteineri tüübi loomine, CONT0001.</li><li>Asetage 9 ea konteinerisse CONT0001.</li></ol> | <p>HDMI kaabel 12':</p><ol><li>Uue konteineri tüübi loomine, CONT0001.</li><li>Asetage 9 ea konteinerisse CONT0001.</li></ol> |
| <p>HDMI kaabel 18':</p><ol><li>Kontrollige, kas kaup võiks mahtuda konteinerisse CONT0001.</li><li>Uue konteineri tüübi loomine, CONT0002.</li><li>Asetage 5 ea konteinerisse CONT0002.</li><li>Uue konteineri tüübi loomine, CONT0003.</li><li>Asetage 3 ea konteinerisse CONT0003.</li></ol> | <p>HDMI kaabel 18':</p><ol><li>Kontrollige, kas kaup võiks mahtuda konteinerisse CONT0001.</li><li>Uue konteineri tüübi loomine, CONT0002.</li><li>Asetage 5 ea konteinerisse CONT0002.</li><li>Uue konteineri tüübi loomine, CONT0003.</li><li>Asetage 3 ea konteinerisse CONT0003.</li></ol> |
| <p>HDMI kaabel 6':</p><ol><li>Kontrollige, kas kaup võiks mahtuda konteinerisse CONT0001.</li><li>Asetage 1 ea konteinerisse CONT0001.</li><li>Kontrollige, kas kaup võiks mahtuda konteinerisse CONT0002.</li><li>Kontrollige, kas kaup võiks mahtuda konteinerisse CONT0003.</li><li>Asetage 4 ea konteinerisse CONT0003.</li><li>Uue konteineri tüübi loomine, CONT0004.</li><li>Asetage 8 ea konteinerisse CONT0004.</li></ol> | <p>HDMI kaabel 6':</p><ol><li>Kontrollige, kas kaup võiks mahtuda konteinerisse CONT0003.</li><li>Asetage 4 ea konteinerisse CONT0003.</li><li>Uue konteineri tüübi loomine, CONT0004.</li><li>Asetage 9 ea konteinerisse CONT0004.</li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a>Näidisstsenaarium - ühe tellimuse pakendamine ühte konteinerisse

Selles jaotises on toodud stsenaarium, kus süsteem on seadistatud konsolideerima mitut tellimust ühte saadetisse. Seega tehakse konteinerite kogum müügitellimusest, et tagada, et iga tellimus, mis sisaldab mitut toodet, pakitakse eraldi konteinerisse.

See funktsioon võimaldab teil käsitleda stsenaariume, kus peate igasse konteinerisse pakkima ainult ühe müügitellimuse, nii et jaotuskeskus saab jaekaupluste vahel ristlaadida täiskonteinereid. Lisaks jaemüügi stsenaariumidele (kaupluste tellimus ja saatmine jaotuskeskusesse ristlaadimiseks) kasutatakse seda tehnikat tavaliselt ka kulusäästlikes tarneahelates (müügitellimus ajamahuka tootmisrea kohta).

See stsenaarium näitab, kuidas saate vähendada konteinerite arvu, mida hinnatakse pakkimisel kasutates konteinerite loomisel strateegiat *Pakenda ainult praegusesse konteinerisse*.

### <a name="prerequisites"></a>Eeltingimused

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a>Lülitage süsteemis sisse funktsioon Konsolideeri saadetised

See stsenaarium kasutab funktsiooni *Konsolideeri saadetised*. Kui see funktsioon ei ole juba teie süsteemis saadaval, peate selle [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) abil sisse lülitama.

#### <a name="make-demo-data-available"></a>Demoandmete kättesaadavaks tegemine

See stsenaarium viitab väärtustele ja kirjetele, mis kuuluvad Microsoft Dynamics 365 Supply Chain Managementile esitatud standardsete demoandmete hulka. Kui soovite kasutada siin esitatud väärtusi harjutuste tegemise ajal, veenduge, et töötate keskkonnas, kuhu on demoandmed installitud ja määrake enne alustamist juriidiliseks isikuks **USMF**.

### <a name="inspect-or-create-container-types"></a>Konteineritüüpide kontrollimine või loomine

Oma konteineritüüpide kontrollimiseks või uute konteineritüüpide loomiseks (kui need on nõutud) järgige järgmisi samme.

1. Avage **Laohaldus** \> **Seadistus** \> **Konteinerid** \> **Konteinerite tüübid**.
1. Kontrollige, et kõik järgnevad konteineritüübid on demoandmetes saadaval. Redigeerige või looge konteineritüüpe vastavalt vajadusele.

    - Konteineri tüüp 1:

        - **Konteineri tüübi kood:** *Box-Large*
        - **Kirjeldus:** *suur kast*
        - **Maksimaalne netokaal:** *100*
        - **Maht:** *400*
        - **Pikkus:** *4*
        - **Laius:** *10*
        - **Kõrgus:** *10*

    - Konteineri tüüp 2:

        - **Konteineri tüübi kood:** *Box-Medium*
        - **Kirjeldus:** *keskmine kast*
        - **Maksimaalne netokaal:** *50*
        - **Maht:** *200*
        - **Pikkus:** *2*
        - **Laius:** *10*
        - **Kõrgus:** *10*

    - Konteineri tüüp 3:

        - **Konteineri tüübi kood:** *Box-Small*
        - **Kirjeldus:** *väike kast*
        - **Maksimaalne netokaal:** *20*
        - **Maht:** *100*
        - **Pikkus:** *1*
        - **Laius:** *10*
        - **Kõrgus:** *10*

### <a name="inspect-or-create-container-groups"></a>Konteinerigruppide kontrollimine või loomine

Oma konteinerigruppide kontrollimiseks või uute konteinerigruppide loomiseks (kui need on nõutud) järgige järgmisi samme.

1. Avage **Laohaldus** \> **Seadistus** \> **Konteinerid** \> **Konteinerigrupid**.
1. Kontrollige, et kõik järgnevad konteinerigrupid on demoandmetes saadaval. Kui see pole saadaval, valige loomiseks **Uus**.

    - **Konteinerigrupi ID:** *Boxes*
    - **Kirjeldus:** *karbi suurused*

1. Konteinerigrupi **Kastid** kiirkaardil *Üksikasjad* veenduge, et järgmised read on olemas. Kui ei, valige lisamiseks suvand **Uus**.

    - Rida 1:

        - **Järjekorranumber:** *1*
        - **Konteineri tüüp:** *Box-Large*
        - **Konteineri kasutamise protsent:** *100*

    - Rida 2:

        - **Järjekorranumber:** *2*
        - **Konteineri tüüp:** *Box-Medium*
        - **Konteineri kasutamise protsent:** *100*

    - Rida 3:

        - **Järjekorranumber:** *3*
        - **Konteineri tüüp:** *Box-Small*
        - **Konteineri kasutamise protsent:** *100*

### <a name="create-a-new-container-build-template"></a>Looge uus konteineri koostemall

Uue konteineri koostemalli loomiseks tehke järgmist.

1. Avage **Laohaldus** \> **Seadistus** \> **Konteinerid** \> **Konteineri koostemall**.
1. Valige **Uus**, et luua konteineri koostemall, kus on järgmised sätted:

    - **Järjekorranumber:** *1*
    - **Konteineri malli ID:** *Box*
    - **Konteinerigrupi ID:** *Boxes*
    - **Aluspäringu tüübid:** *müügi eraldusrida*
    - **Vooetapi kood:** *234*
    - **Tükeldatud valiku lubamine:** *jah*
    - **Konteineri pakkimisstrateegia:** *pakenda ainult praegusesse konteinerisse*
    - **Pakendamine direktiivi ühikute kaupa:** *ei*

1. Kuigi uue malli rida on endiselt valitud, valige tegevuspaanil **Muuda päringut**.
1. Kuvatakse standardne päringu redaktori dialoogiaken. Järgmiste sätetega rea ​​lisamiseks valige vahekaardil **Sortimine** suvand **Lisa**.

    - **Tabel:** *Ajutised töökanded*
    - **Tuletatud tabel:** *Ajutised töökanded*
    - **Väli:** *Tellimuse number*
    - **Otsingusuund:** *Kasvav*

    > [!IMPORTANT]
    > Kõigi teiste avatud konteinerite rattasõidu vältimiseks ja protsessi kiirendamiseks, kontrollides korraga ühte konteinerit, kasutage lisaks tellimisnumbri järgi sorteerimisele ka strateegiat *Pakenda ainult praegusesse konteinerisse*. See kombinatsioon töötab töömallis nagu tööpaus.

1. Päringuredaktori dialoogiboksi sulgemiseks valige **OK**.
1. Kuigi uue malli rida on endiselt valitud, valige tegevuspaanil **Konteinerite segamise piirangud**.

    Nüüd lisate piirangu, mis asetab kaubad ühest tellimusest ühte konteinerisse. Mis tahes muu tellimuse kaubad pannakse eraldi konteinerisse.

1. Valige **Uus**, et luua segamsie piirangud, kus on järgmised sätted:

    - **Tabel:** *Müügitellimused*
    - **Valige väli:** *SalesId* (väli kuvatakse ruudustikus *müügitellimusena*.)

1. Piirangu lisamiseks valige **OK**.
1. Sulgege leht.

### <a name="set-up-a-wave-template-for-containerization"></a>Voomalli häälestamine konteinerite koostamise jaoks

Voomalli seadistamiseks tehke järgmist.

1. Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.
1. Määrake loendi paani välja **Voomalli tüüp** suvandiks *Lähetamine*.
1. Valige loendist **63 konteinerite loomise** mall.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Otsige kiirkaardi **Meetodid** veerust **Valitud meetodid**, järgmine rida:

    - **Meetodi nimi:** *konteinerisse määramine*
    - **Nimi:** *konteinerisse määramine*

1. Seadke rea välja **Vooetapi kood** väärtuseks *234*.

### <a name="set-up-a-work-template"></a>Töömalli häälestamine

Töömalli seadistamiseks tehke järgmist.

1. Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.
1. Seadke välja **Töökäsu tüüp** valikuks *Müügitellimused*.
1. Ruudustikus **Ülevaade** leidke ja valige töömall, mida tuleks kasutada üksiktellimuse pakkimiseks ühte konteinerisse. Valige selle stsenaariumi jaoks mall **63 Ettevalmistamiseks konteinerisse**.
1. Valige Toimingupaanil nupp **Päringu redigeerimine**.
1. Kuvatakse standardne päringu redaktori dialoogiaken. Vahekaardil **Sortimine** lisage järgmised read:

    - Rida 1:

        - **Tabel:** *Ajutised töökanded*
        - **Tuletatud tabel:** *Ajutised töökanded*
        - **Väli:** *Saadetise ID*
        - **Otsingusuund:** *Kasvav*

    - Rida 2:

        - **Tabel:** *Ajutised töökanded*
        - **Tuletatud tabel:** *Ajutised töökanded*
        - **Väli:** *Tellimuse number*
        - **Otsingusuund:** *Kasvav*

    - Rida 3:

        - **Tabel:** *Ajutised töökanded*
        - **Tuletatud tabel:** *Ajutised töökanded*
        - **Väli:** *konteineri ID*
        - **Otsingusuund:** *Kasvav*

1. Päringuredaktori dialoogiboksi sulgemiseks valige **OK**.
1. Teile kuvatakse järgmine teade: „Grupeerimine lähtestatakse, kas soovite jätkata?” Jätkamiseks valige **Jah**.
1. Kui **63 Ettevalmistamiseks konteinerisse** on veel valitud, valige tegevuspaanil **Tööpäiste piirid**.

    Nüüd rakendate töö katkestamiseks sätteid, nii et tellimuse iga konteiner on lingitud ühe töötellimusega.

1. Märkige ruut **Rühmita selle välja järgi** iga rea puhul lehel **Tööpäise piirid** (**Saadetise ID**, **Tellimuse number** ja **Konteineri ID**).
1. Sulgege leht.

### <a name="set-up-shipment-consolidation-policies"></a>Seadistage saadetise konsolideerimise põhimõtted

Saadetise konsolideerimise poliitika seadistamiseks toimige järgmiselt.

1. Avage jaotis **Laohaldus \> Seadistus \> Lattu väljastamine \> Saadetise konsoldeerimispoliitika**.
1. Seadke loendi paanil välja **Poliitika tüüp** väärtuseks *Müügitellimus*.
1. Valige loendist **vaike** poliitika.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Valige kiirkaardi **Konsolideerimise väljad** loendist **Valitud väljad** rida, mille välja **Välja nimi** väärtuseks on seatud *Tellimuse number*.
1. Valige nupu **Eemalda** ![vasaknool.](media/backward-button.png) Klõpsake , et teisaldada **Ülejäänud väljad** loendisse .
1. Valige toimingupaanil nupp **Salvesta**.

### <a name="set-up-physical-dimensions-for-the-product"></a>Seadistage toote füüsilised mõõtmed

Selles stsenaariumis kasutatavate toodete füüsiliste mõõtmete häälestamiseks järgige neid samme.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Valige toode, kus **kaubakoodi** väli on seadistatud valikule *A0001*.
1. Valige toimingupaani vahekaardi **Varude haldamine** grupis **Ladu** suvand **Füüsilised dimensioonid**.
1. Lehel **Füüsilised mõõtmed** peaksite ruudustikus nägema järgmist rida:

    - **Ühik:** *tk*
    - **Brutokaal:** *3,00*
    - **Laius:** *2,00*
    - **Sügavus:** *2,00*
    - **Kõrgus:** *4,00*
    - **Maht:** *16,00*

1. Sulgege leht.
1. Valige toode, kus **kaubakoodi** väli on seadistatud valikule *A0002*.
1. Valige toimingupaani vahekaardi **Varude haldamine** grupis **Ladu** suvand **Füüsilised dimensioonid**.
1. Lehel **Füüsilised mõõtmed** peaksite ruudustikus nägema järgmist rida:

    - **Ühik:** *tk*
    - **Brutokaal:** *4,00*
    - **Laius:** *3,00*
    - **Sügavus:** *1,00*
    - **Kõrgus:** *3,00*
    - **Maht:** *9,00*

### <a name="create-sales-order-1"></a>Müügitellimuse 1 loomine

Müügitellimuse loomiseks tehke järgmist.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Valige toimingupaanil nupp **Uus**.
1. Kuvatakse dialoogiboks uue müügitellimuse loomiseks. Määrake järgmised väärtused.

    - **Kliendi konto:** *US-001*
    - **Ladu:** *63*

1. Valige müügitellimuse loomiseks ja dialoogiboksi sulgemiseks **OK**.
1. Avatakse uus müügitellimus. Lisage kiirkaardil **Müügitellimuse read** järgmised müügiread:

    - Rida 1:

        - **Kauba kood:** *A0001*
        - **Kogus:** *2*

    - Rida 2:

        - **Kauba kood:** *A0002*
        - **Kogus:** *2*

1. Valige esimene rida ja seejärel valige **Laovarud \> Reserveerimine**.
1. Valige tegevuspaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**. Seejärel sulgege leht.
1. Korrake teise rea kahte eelmist sammu.
1. Sulgege leht.

### <a name="create-sales-order-2"></a>Müügitellimuse 2 loomine

Teise müügitellimuse loomiseks toimige järgmiselt.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Valige toimingupaanil nupp **Uus**.
1. Kuvatakse dialoogiboks uue müügitellimuse loomiseks. Määrake järgmised väärtused.

    - **Kliendi konto:** *US-001*
    - **Ladu:** *63*

1. Valige müügitellimuse loomiseks ja dialoogiboksi sulgemiseks **OK**.
1. Avatakse uus müügitellimus. Lisage kiirkaardil **Müügitellimuse read** järgmised müügiread:

    - Rida 1:

        - **Kauba kood:** *A0001*
        - **Kogus:** *4*

    - Rida 2:

        - **Kauba kood:** *A0002*
        - **Kogus:** *4*

1. Valige esimene rida ja seejärel valige **Laovarud \> Reserveerimine**.
1. Valige tegevuspaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**. Seejärel sulgege leht.
1. Korrake teise rea kahte eelmist sammu.
1. Sulgege leht.

### <a name="create-the-load"></a>Koormuse loomine

Selle stsenaariumi jaoks loodud tellimuste jaoks koormuse loomiseks ja seejärel lattu väljaandmiseks toimige järgmiselt.

1. Avage **Laohaldus \> Koormused \> Koormuse plaanimise töölaud**.
1. Otsige üles ja valige vahekaardil **Müügiread** kõik müügitellimuse read selle stsenaariumi jaoks loodud müügitellimused.
1. Valige toimingupaani vahekaardi **Pakkumine ja nõudlus** grupis **Lisa** suvand **Uuele koormusele**. Valitud tellimuseread lisatakse uude koormusse.
1. Valige dialoogiboksi **Koormuse malli määramine** väljal **Koormuse malli ID** koormuse mall, näiteks *40' koormus*.
1. Valige dialoogiboksi sulgemiseks suvand **OK**.
1. Otsige üles ja valige äsja loodud koormus jaotises **Koormused**.
1. Valige **Väljastamine \> Lattu väljastamine**.
1. Dialoogiaknas **Lattu väljastamine** valige valitud koormuse lattu väljastamiseks **OK**.

### <a name="verify-the-shipments-and-containers"></a>Kontrolli saadetisi ja konteinereid

Järgmine protseduur võimaldab teil kontrollida loodud saadetisi. Selle abil saate selle stsenaariumi jaoks loodud tellimuse üle vaadata ja veenduda, et olete oodatud tulemused saavutanud.

1. Avage **Laohaldus \> Saadetised \> Kõik saadetised**.
1. Otsige ja valige saadetis, mis loodi äsja väljaantud koorma jaoks.
1. Avage toimingupaanilt vahekaart **Transport** ja valige **Kuva konteinerid**.
1. Veenduge, et müügitellimuste kaubad määratakse kahte erinevasse konteinerisse.

## <a name="additional-resources"></a>Lisaressursid

- [Konteinerisse määramine](wave-containerization.md)
