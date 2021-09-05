---
title: Voosildi printimine
description: Selles teemas kirjeldatakse voo sildi printimist ja selgitatakse, kuidas seda seadistada.
author: perlynne
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 6b75dcb7d56648f3be291cb1c09ec57a53477ec0
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344170"
---
# <a name="wave-label-printing"></a>Voosildi printimine

[!include [banner](../includes/banner.md)]

Voo siltide printimine pakub alternatiivset lähenemist siltide printimisele, lisatud on uus vooetapi meetod, mis võimaldab teil luua ja printida silte otse voomallist voo käivitamise ajal. Seetõttu on sildid saadaval juba enne, kui töötajad käitavad töökäsu mobiilses seadmes. Töötajad saavad manustada nõutavad sildid komplekteerimise ajal, mitte pärast seda.

Voo siltide printimine kasutab sildipaigutuste loomiseks Zebra programmeerimiskeelt (ZPL). Sildipaigutus jagatakse kolme ossa (päis, keha ja jalus), et lubada korduva ülesehitusega silte. Voo siltide mallid ütlevad süsteemile, millist sildipaigutust kasutada. Kasutajad saavad määrata, millist printerit kasutatakse. Nad võivad printida silte vastavalt vajadusele ka üheaegselt mitmelt printerilt. Lehel **Voo sildi ajalugu** kuvatakse kirjet kõigist selle seadistuse abil loodud siltidest.

Saate printida ja silte tööpäiste alusel eksemplarhaaval rühmitada, saate printida piirjoonesilte tööpäise kohta, samuti saate printida konteineri sisu silte, juhtumi silte ja muid sarnaseid silte.

> [!NOTE]
> See funktsioon ei asenda olemasolevat sildi printimise funktsiooni, mis põhineb dokumendi marsruudi valikul.

Voo sildi printimine pakub järgmisi täiustusi.

- Saate printida silte vastavalt ühel tööreal olevale pakkide arvule, kasutamata konteinerisse määramist. („Pakk” on ühik, mis on määratud ühiku seeriagrupi ridadele.)
- Saate printida mitu erinevat siltide järjestust (nt pakkide, kastide ja kaubaaluste sildid).
- Saate kaasata siltide loetelu (nt 1/124, 2/124... 124/124) ja määratleda loetelu vahemiku (nt töörida, koormuse rida või saadetis).
- Saate luua ja printida veokirja ID siltidele enne veokirja loomist.
- Saate luua iga paki jaoks kordumatu konteineri seeriaviisilise lähetamise koodi (SSCC) ja lisada selle igale sildile.
- Saate luua GS1-ga ühilduva numbriseeriad veokirja ID ja SSCC jaoks.
- Saate printida silte uuesti nii mobiilsest seadmest kui ka rikkast kliendist.
- Saate tühistada silte (nt kiire komplekteerimise stsenaariumides) ja printida need uuesti.
- Voo siltide ajaloo puhastamine.
- Dokumendi marsruudi valiku paigutuste täiustuste hulka kuuluvad dokumendi marsruudi valiku paigutused ja voo sildi paigutused. (Lisateavet vt [Identifitseerimisnumbrite dokumendi marsruudi valiku paigutus](../warehousing/document-routing-layout-for-license-plates.md).)

Need täiustused lihtsustavad pakkide sildistamist enne kaubaalusele paigutamist. Need on eriti kasulikud ettevõtetele, kes saadavad suurtele jaemüüjatele, mis kinnitavad tellimuse sissetulekuid automaatselt, skannides igat pakki eraldi.

> [!NOTE]
> Saate rakendada selles teemas kirjeldatud konfiguratsiooni stsenaariume eraldi või koos, sõltuvalt teie ärivajadustest. Saate kujundada mitu voo sildi malli, mis töötavad järjekorras (kujutatud stsenaariumis 3). Saate näiteks kasutada stsenaariumi 1 pakkide siltide printimiseks ja stsenaarium 2 kaubaaluste siltide printimiseks (kui kaubaalused on laos erineva suuruse ja kooslusega).

## <a name="turn-on-the-wave-label-printing-feature"></a>Voo sildi printimise funktsiooni sisselülitamine

Enne funktsiooni *Voo sildi printimine* kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Seega on funktsioon loetletud järgmisel viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Voo sildi printimine*

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a>1. stsenaarium: voo sildi printimine, kus luuakse üks voo silt

Selles stsenaariumis näidatakse, kuidas ettevõte saab printida saadetiste silte suurte jaemüüjate jaoks, mis kinnitavad automaatselt tellimuse sissetulekuid, skannides iga pakki eraldi.

Selles stsenaariumis näidatakse täielikku voogu.

### <a name="make-demo-data-available"></a>Demoandmete kättesaadavaks tegemine

Selle stsenaariumiga töötamiseks peavad teil olema installitud demoandmed ja peate valima juriidilise isiku **USMF**.

### <a name="make-sure-that-the-wave-label-method-is-available"></a>Veenduge, et voo sildi meetod oleks saadaval

Peate tõenäoliselt voo protsessi meetodid uuesti looma, et muuta voo siltide printimise meetod kättesaadavaks.

1. Avage jaotis **Laohaldus \> Seadistus \> Vood \> Voo protsessi meetodid**.
1. Kinnitage, et loendis oleks **waveLabelPrinting**. Kui seda pole, valige selle lisamiseks toimingupaanil **Meetodite uuesti loomine**.

### <a name="configure-a-wave-template"></a>Voomalli konfigureerimine

Voomallid võimaldavad teil linkida kindlaid voo meetodite eksemplare vastava voo sildi malliga.

1. Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.
1. Valige voomall, nt **62 Saadetise vaikemall**.
1. Teisaldage kiirkaardil **Meetodid** meetod **Voo sildi printimine** veergu **Valitud meetodid**.
1. Valige veerus **Valitud meetodid** meetod **Voo sildi printimine** ja määrake selle välja **Vooetapi kood** väärtuseks *PrintLabel*. Lisateavet vooetapi koodide kohta leiate teemast [Vooetapi koodid](wave-step-codes.md).

### <a name="create-a-wave-label-layout"></a>Voo sildi paigutuse loomine

Sildi paigutus juhib, milline teave sildil prinditakse ja kuidas see on paigutatakse. Siin saate sisestada ZPL-koodi, mis saadetakse printerisse.

1. Avage jaotis **Laohaldus \> Seadistus \> Dokumendi marsruudi valik \> Voo sildi paigutused**.
1. Looge järgmiste sätetega kirje.

    - **Sildi paigutuse ID:** *Pakk*
    - **Kirjeldus:** *Pakk (SSCC)*

1. Valige toimingupaanil nupp **Salvesta**.
1. Valige toimingupaanil **Voo sildi rea sätted**.

    Kuvatakse leht **Voo sildi rea sätted**. Siin saate konfigureerida sildi dünaamilise osa.

1. Lisage järgmiste sätetega rida.

    - **Rea ID:** *WaveLabel*
    - **Rea tabeli nimi:** *WHSWaveLabel*
    - **Rea algpaigutus:** *0*

        See väli määratleb vertikaalse paigutuse, kus sildil algab rida.

    - **Rea kõrgus:** *0*

        See väli määratleb iga rea kõrguse (punktides) vastavalt ZPL-standardile. Rea kõrgus on horisontaalsete siltide puhul positiivne ja vertikaalsete siltide puhul negatiivne. Kuna selles näites on ainult üks rida, saate väärtuseks seada *0* (null).

    - **Ridu lehel:** *1*

        See väli määratleb ridade arvu, mida saab igale sildile printida.

        > [!NOTE]
        > See seadistus prindib eraldi ZPL-sildi igale kirjele voo siltide tabelis.

1. Sulgege leht.
1. Valige Toimingupaanil nupp **Päringu redigeerimine**.
1. Lisage päringuredaktori dialoogiboksis vahekaardile **Vahemik** rida, millel on järgmised sätted.

    - **Tabel:** *Tööread*
    - **Tuletatud tabel:** *Tööread*
    - **Väli:** *Töö tüüp*
    - **Kriteeriumid:** *Komplekteerimine*

    See päring tagab, et sildile prinditakse ainult komplekteerimise tüübiga tööread, mitte sisestamise tüübiga tööread.

1. Kui soovite printida veokirja ID-d, valige vahekaardil **Liitmised** tabel **Tööread** ja liitke sellega tabel **Saadetised**.
1. Sulgege päringuredaktori dialoogiboks.
1. Kiirkaardil **Printeri teksti paigutuse** on kolm jaotist, kuhu saate kirjutada printeri koodi: **Päise jaotis**, **Keha jaotis** ja **Jaluse jaotis**. Sisestage jaotise **Päise jaotis** väljale **Sildi päis** nõutava päise kood. Näiteks kui kasutate Zebra printereid, saate kasutada järgmist koodi.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. Sisestage jaotise **Keha jaotis** väljale **Sildi keha** nõutava keha ZPL-kood. Siin on näide.

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. Sisestage jaotise **Keha jaotis** väljale **Sildi jalus** nõutava jaluse ZPL-kood. Siin on näide.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > See häälestus prindib igast sildist ühe eksemplari. Kui vajate rohkem eksemplare (nt ühte eksemplari kaubaaluse kummalegi poolele), määrake jaluse jaotise **\^PQn** väärtuseks **n** nõutav eksemplaride arv. Näiteks igast sildist nelja eksemplari printimiseks määrake **\^PQ4**.

Teie silt on nüüd kasutamiseks valmis.

### <a name="create-a-wave-label-type"></a>Voo sildi tüübi loomine

Voo sildi tüüpe kasutatakse voo sildi mallide linkimiseks ühiku seeriagrupi ridade ühikule.

1. Avage jaotis **Laohaldus \> Seadistus \> Dokumendi marsruudi valik \> Voo sildi tüübid**.
1. Lisage järgmiste sätetega voo sildi tüüp.

    - **Sildi tüüp:** *Pakk*
    - **Kirjeldus:** *Pakk*

### <a name="set-up-unit-sequence-groups"></a>Üksuse seeriagruppide häälestamine

Järgmisena seadistage voo sildi tüübile ühiku seeriagrupp.

1. Avage jaotis **Laohaldus \> Seadistus \> Ladu \> Ühiku seeriagrupid**.
1. Valige grupp **Ea Kast PL**.
1. Määrake rea **Kast** välja **Voo taseme tüüp** väärtuseks *Pakk*.

### <a name="create-a-wave-label-template"></a>Voo sildi malli loomine

Järgmisena looge voo sildi tüübile voo sildi mall.

1. Avage jaotis **Laohaldus \> Seadistus \> Dokumendi marsruudi valik \> Voo sildi mallid**.
1. Lisage voo taseme mall ja seadke päises järgmised väärtused.

    - **Voo malli nimi:** *Paki sildid*
    - **Kirjeldus:** *Paki sildid*
    - **Vooetapi kood:** *PrintLabel*
    - **Ladu:** *62*

1. Määrake kiirkaardi **Üldine** välja **Voo sildi tüüp** väärtuseks *Pakk*.
1. Lisage kiirkaardil **Voo sildi malli üksikasjad** uus rida, millel on järgmised sätted.

    - **Sildi paigutuse ID:** *Pakk*
    - **Printeri nimi:** valige sobiv ZPL-printer.
    - **Käivita päring:** *Jah* (see säte on valikuline, kuid see on optimaalse jõudluse tagamiseks soovitatav.)

1. Valige toimingupaanil nupp **Salvesta**.
1. Valikuline: kui seadistate kliendipõhist sildi kujundust, tuleb teil luua päring kliendi konto leidmiseks. Valige kiirkaardil **Voo sildi malli üksikasjad** suvand **Päringu redigeerimine**. Seejärel lisage päringuredaktori dialoogiboksis vahekaardile **Vahemik** rida, millel on järgmised sätted.

    - **Tabel:** *Saadetised*
    - **Tuletatud tabel:** *Saadetised*
    - **Väli:** *Kontonumber*
    - **Kriteeriumid:** sisestage vastava kliendi kontonumber.

    Kui olete lõpetanud, valige päringuredaktori dialoogiboksi sulgemiseks **OK**.

1. Valige toimingupaanil suvand **Päringu redigeerimine**, et avada terve sildi malli päringuredaktori dialoogiboks.
1. Lisage päringuredaktori dialoogiboksis vahekaardile **Sortimine** rida, millel on järgmised sätted.

    - **Tabel:** *Tööread*
    - **Tuletatud tabel:** *Tööread*
    - **Väli:** *Koormuse viiterea ID (kirje-ID)*
    - **Otsingusuund:** *Kasvav*

1. Päringuredaktori dialoogiboksi sulgemiseks valige **OK**.
1. Teateaken palub teil rühmitamise lähtestamise toimingu kinnitada. Jätkamiseks valige **Jah**.
1. Valige toimingupaanil **Voo sildi malligrupp**.
1. Valige dialoogiboksis **Voo sildi malligrupp** rida, kus välja **Viitevälja nimi** väärtuseks on seatud *Viite koormuse rea ID* ja seejärel märkige sellel real ruut **Sildi kooste ID**.

    > [!NOTE]
    > See häälestus loob ühe sildi järjestuse („Pakk 1/X”) koormuse rea kohta kogu voos, sõltumata töö rühmitamise seadistusest. Seda sildi järjestust saab printida sildi paigutusele.

### <a name="configure-number-sequence-extensions"></a>Numbriseeria laienduste konfigureerimine

Numbriseeria laiendused juhivad konkreetsete numbriseeriate GS1 vastavust. See konfiguratsioon on praeguse stsenaariumi puhul valikuline. Lisateavet ja konfigureerimise juhiseid leiate teemast [Numbriseeria laienduste konfigureerimine](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Müügitellimuse loomine ja selle väljastamine lattu

1. Avage jaotis **Müük ja turundus \> Müügitellimus \> Kõik müügitellimused**.
1. Looge järgmiste sätetega müügitellimuse rida.

    - **Kliendi konto:** *US-001*
    - **Ladu:** *62*

1. Lisage kaks müügitellimuse rida, millel on järgmised sätted.

    - Müügitellimuse rida 1:

        - **Kauba kood:** *A0001*
        - **Kogus:** *9024*
        - **Ühik:** *ea* (9024 ea = 376 kasti = 47 PL)

    - Müügitellimuse rida 2:

        - **Kauba kood:** *A0002*
        - **Kogus:** *9016*
        - **Ühik:** *ea* (9016 ea = 322 kasti = 46 PL)

    > [!NOTE]
    > Siin esitatud kaubad ja kogused on ainult näited. Need peavad kasutama ühiku seeriagruppi, mille eelnevalt määratlesite, neile tuleb määratleda vastav ühiku teisendamine ühikult *ea* ühikule *Kast* ühikule *PL* ja neil peab olema kaubavarusid laos *62*. Lisateavet leiate teemast [Mõõtühik ja varude poliitika](unit-measure-stocking-policies.md).

1. Valige müügitellimuse rida 1. Seejärel valige menüü **Varud** jaotisest **Müügitellimuse rida** suvand **Reserveerimised**.
1. Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii** ja seejärel sulgege leht.
1. Korrake etappe 4 ja 5 müügitellimuse rea 2 puhul.
1. Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.

    Toimub järgmine:

    - Süsteem töötleb loodud saadetist, kasutades malli, mis sisaldab sildi printimise etappi. Sildi paigutust kasutatakse sildi vormingu määratlemiseks ja tulemuseks on silt, mis prinditakse sildi mallis valitud printeriga.
    - Voo sildid luuakse ja prinditakse. Siltide arv on võrdne pakkide arvuga (selles näites on 376 kasti silti rea 1 ja 322 kasti silti rea 2 jaoks).
    - Saadetistele luuakse uus veokirja ID. Kui konfigureerisite numbriseeria laiendused, järgib voo sildi ID numbrivormingut **SSCC-18**. 

Saate kuvada ja uuesti printida järgmiste lehtede voo silte. Valige iga lehe toimingupaani vahekaardil **Saadetised** grupis **Seotud teave** suvand **Voo sildid**.

- Kõik saadetised \> Saadetise üksikasjad
- Kõik koormused \> Koormuse üksikasjad
- Kõik vood
- Voo sildid
- Voosildi ajalugu

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a>2. stsenaarium: voo siltide printimine konteinerisse määramiseks (voo sildi kirjeteta)

See stsenaarium võimaldab teil printida voo silte, kui kasutate konteineritesse määramist, et jaotada kaubad automaatselt kastidesse ja seetõttu ei vaja voo sildi kirjet. Sel juhul toimib konteineri ID SSCC-kohatäitena.

Selle ja 1. stsenaariumi peamised erinevused on järgmised.

- **Voo sildi mallid:** te ei vali voo sildi tüüpi voo sildi mallis ja te ei vaja sildi kooste rühmitamist. Vastasel juhul konfigureerite voo sildi malli ja lingite voo malliga samamoodi, nagu on kirjeldatud stsenaariumis 1. Peate jätma voo sildi tüübi tühjaks, et voo silte ei loodaks.
- **Voo siltide paigutused:** konfigureerite voo sildi paigutuse rea sätted tööridade jaoks, mitte voo sildi kirjed. Peate konfigureerima rea sätte sildi paigutuse jaoks, kasutades tabelit **WHSWorkLine** tabeli **WHSWaveLabel** asemel. Säte **Ridade arv lehekülje kohta** reguleerib ridade arvu, mis on keha jaotises. 

See konfiguratsioon sobib ka äristsenaariumide jaoks, kus mitu erinevat kaupa pakitakse ühte sildistatud kasti või kaubaalusele ja seda pakkimise protsessi saab määratleda töö loomisel (näiteks töö, mis on grupeeritud saadetisega).

Selles stsenaariumis näidatakse täielikku voogu.

### <a name="make-demo-data-available"></a>Demoandmete kättesaadavaks tegemine

Selle stsenaariumiga töötamiseks peavad teil olema installitud demoandmed ja peate valima juriidilise isiku **USMF**.

### <a name="make-sure-that-the-wave-label-method-is-available"></a>Veenduge, et voo sildi meetod oleks saadaval

Peate tõenäoliselt voo protsessi meetodid uuesti looma, et muuta voo siltide printimise meetod kättesaadavaks.

1. Avage jaotis **Laohaldus \> Seadistus \> Vood \> Voo protsessi meetodid**.
1. Kinnitage, et loendis oleks **waveLabelPrinting**. Kui seda pole, valige selle lisamiseks toimingupaanil **Meetodite uuesti loomine**.

### <a name="set-up-a-wave-template"></a>Voomalli seadistamine

Voomallid võimaldavad teil linkida kindlaid voo meetodite eksemplare vastava voo sildi malliga.

1. Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.
1. Valige voomall, nt **63 konteinerisse määramine**.
1. Teisaldage kiirkaardil **Meetodid** meetod **Voo sildi printimine** veergu **Valitud meetodid**.
1. Valige veerus **Valitud meetodid** meetod **Voo sildi printimine** ja määrake selle välja **Vooetapi kood** väärtuseks *PrintLabel*. Lisateavet vooetapi koodide kohta leiate teemast [Vooetapi koodid](wave-step-codes.md).

### <a name="create-a-wave-label-layout"></a>Voo sildi paigutuse loomine

1. Avage jaotis **Laohaldus \> Seadistus \> Dokumendi marsruudi valik \> Voo sildi paigutused**.
1. Looge järgmiste sätetega kirje.

    - **Sildi paigutuse ID:** *Pakk*
    - **Kirjeldus:** *Pakk (SSCC)*

1. Valige toimingupaanil nupp **Salvesta**.
1. Valige toimingupaanil **Voo sildi rea sätted**.

    Kuvatakse leht **Voo sildi rea sätted**. Siin saate konfigureerida sildi dünaamilise osa.

1. Lisage järgmiste sätetega rida.

    - **Rea ID:** *WorkLine*
    - **Rea tabeli nimi:** *WHSWorkLine*
    - **Rea algpaigutus:** *500*

        See väli määratleb vertikaalse paigutuse, kus sildil algab rida.

    - **Rea kõrgus:** *–50*

        See väli määratleb iga rea kõrguse. Rea kõrgus on horisontaalsete siltide puhul positiivne ja vertikaalsete siltide puhul negatiivne.

    - **Ridu lehel:** *5*

        See väli määratleb ridade arvu, mida saab igale sildile printida.

        > [!NOTE]
        > See seadistus prindib mitu ZPL-silti töö kohta, kus igal lehel võib olla kuni viis töörida. Näiteks kui silt prinditakse konteinerile, millel on 12 rida, prinditakse kolm silti. Kui soovite printida iga komplekteerimise rea kohta eraldi sildi, seadke väärtuseks *1*.

1. Sulgege leht.
1. Valige Toimingupaanil nupp **Päringu redigeerimine**.
1. Lisage päringuredaktori dialoogiboksis vahekaardile **Vahemik** rida, millel on järgmised sätted.

    - **Tabel:** *Tööread*
    - **Tuletatud tabel:** *Tööread*
    - **Väli:** *Töö tüüp*
    - **Kriteeriumid:** *Komplekteerimine*

1. Kui soovite printida veokirja ID-d, valige vahekaardil **Liitmised** tabel **Tööread** ja liitke sellega tabel **Saadetised**.
1. Sulgege päringuredaktori dialoogiboks.
1. Kiirkaardil **Printeri teksti paigutuse** on kolm jaotist, kuhu saate kirjutada printeri koodi: **Päise jaotis**, **Keha jaotis** ja **Jaluse jaotis**. Sisestage jaotise **Päise jaotis** väljale **Sildi päis** nõutava päise kood. Näiteks kui kasutate Zebra printereid, saate kasutada järgmist koodi.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. Sisestage jaotise **Keha jaotis** väljale **Sildi keha** nõutava keha ZPL-kood. Siin on näide.

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. Sisestage jaotise **Keha jaotis** väljale **Sildi jalus** nõutava jaluse ZPL-kood. Siin on näide.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > See häälestus prindib igast sildist ühe eksemplari. Kui vajate rohkem eksemplare (nt ühte eksemplari kaubaaluse kummalegi poolele), määrake jaluse jaotise **\^PQn** väärtuseks **n** nõutav eksemplaride arv. Näiteks igast sildist nelja eksemplari printimiseks määrake **\^PQ4**.

Teie silt on nüüd kasutamiseks valmis.

### <a name="create-a-wave-label-template"></a>Voo sildi malli loomine

1. Avage jaotis **Laohaldus \> Seadistus \> Dokumendi marsruudi valik \> Voo sildi mallid**.
1. Lisage voo taseme mall ja seadke päises järgmised väärtused.

    - **Voo malli nimi:** *Konteineri sildid*
    - **Kirjeldus:** *Konteineri sildid*
    - **Vooetapi kood:** *PrintLabel*
    - **Ladu:** *63*

1. Lisage kiirkaardil **Voo sildi malli üksikasjad** rida, millel on järgmised sätted.

    - **Sildi paigutuse ID:** *Konteiner*
    - **Printeri nimi:** valige sobiv ZPL-printer.
    - **Käivita päring:** *Jah* (see säte on valikuline, kuid see on optimaalse jõudluse tagamiseks soovitatav.)

1. Valige toimingupaanil nupp **Salvesta**.
1. Valikuline: kui seadistate kliendipõhist sildi kujundust, tuleb teil luua päring kliendi konto leidmiseks. Valige kiirkaardil **Voo sildi malli üksikasjad** suvand **Päringu redigeerimine**. Seejärel lisage päringuredaktori dialoogiboksis vahekaardile **Vahemik** rida, millel on järgmised sätted.

    - **Tabel:** *Saadetised*
    - **Tuletatud tabel:** *Saadetised*
    - **Väli:** *Kontonumber*
    - **Kriteeriumid:** sisestage vastava kliendi kontonumber.

    Kui olete lõpetanud, valige päringuredaktori dialoogiboksi sulgemiseks **OK**.

### <a name="configure-number-sequence-extensions"></a>Numbriseeria laienduste konfigureerimine

Numbriseeria laiendused juhivad konkreetsete numbriseeriate GS1 vastavust. See konfiguratsioon on praeguse stsenaariumi puhul valikuline. Lisateavet ja konfigureerimise juhiseid leiate teemast [Numbriseeria laienduste konfigureerimine](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Müügitellimuse loomine ja selle väljastamine lattu

1. Avage jaotis **Müük ja turundus \> Müügitellimus \> Kõik müügitellimused**.
1. Looge järgmiste sätetega müügitellimuse rida.

    - **Kliendi konto:** *US-001*
    - **Ladu:** *63*

1. Lisage viis müügitellimuse rida.

    - Müügitellimuse rida 1:

        - **Kauba kood:** *A0001*
        - **Kogus:** *10*

    - Müügitellimuse rida 2:

        - **Kauba kood:** *A0002*
        - **Kogus:** *20*

    - Müügitellimuse rida 3:

        - **Kauba kood:** *L0006*
        - **Kogus:** *20*

    - Müügitellimuse rida 4:

        - **Kauba kood:** *L0100*
        - **Kogus:** *40*

    - Müügitellimuse rida 5:

        - **Kauba kood:** *L0101*
        - **Kogus:** *50*

    > [!NOTE]
    > Siin esitatud kaubad ja kogused on ainult näited. Neil peab olema laovaru määratud laos.

1. Valige müügitellimuse rida 1. Seejärel valige menüü **Varud** jaotisest **Müügitellimuse rida** suvand **Reserveerimised**.
1. Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii** ja seejärel sulgege leht.
1. Korrake etappe 4 ja 5 iga täiendava müügitellimuse rea.
1. Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.

    Toimub järgmine:

    - Süsteem töötleb loodud saadetist, kasutades malli, mis sisaldab sildi printimise etappi. Sildi paigutust kasutatakse sildi vormingu määratlemiseks ja lõpptulemuseks on silt, millel on viis rida ja mis prinditakse sildi mallis valitud printeriga.
    - Saadetistele luuakse uus veokirja ID. Kui konfigureerisite numbriseeria laiendused, järgib voo sildi ID numbrivormingut **SSCC-18**. 

Saate need voo sildid uuesti printida, avades jaotise **Laohaldus \> Päringud ja aruanded \> Laine sildi ajalugu**.

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a>3. stsenaarium: voo sildi printimine mitmeastmeliste siltide puhul

Selles stsenaariumis näidatakse, kuidas kasutada voo siltide printimise funktsiooni, kui ladustamisprotsessid nõuavad mitmeastmelisi saadetise silte. Näiteks võib olla vaja printida eraldi sildid pakkide ja kaubaaluste jaoks ning piirjoonesilt terve saadetise jaoks. Piirjoonesildid on siltide eritüüp, mida saab kasutada rullide ja konteinerite eraldajana, nt sildid saadetise ID ja vöötkoodi jaoks, et silte saaks pärast printimist hõlpsasti sortida.

Peamine erinevus selle stsenaariumi konfiguratsiooni ja 1. stsenaariumi konfiguratsiooni vahel on see, et lisaks piirjoonesiltide lubamisele tuleb mitu voo sildi tüüpi seostada voo sildi mallide ja ühiku seeriagrupi ridadega. Selle konfiguratsiooni saavutamiseks peate seadistama selle stsenaariumi jaoks järgmised elemendid.

- **Voo töötlemise meetodid:** peate märkima voo sildi meetodiks korratav, lisama selle mallile kaks (või enam) korda ja seadma erinevad vooetapi koodid.
- **Voo siltide mallid:** peate konfigureerima voo sildi mallid ja linkima need voo malliga. Igal voo sildi mallil on oma voo sildi tüüp.
- **Voo sildi paigutused:** peate looma mitu voo sildi paigutust. Iga sildi astme kohta tuleb eraldi sildi paigutus ja piirjoonesildile oma paigutus.

Selles stsenaariumis näidatakse täielikku voogu.

### <a name="make-demo-data-available"></a>Demoandmete kättesaadavaks tegemine

Selle stsenaariumiga töötamiseks peavad teil olema installitud demoandmed ja peate valima juriidilise isiku **USMF**.

### <a name="set-up-a-wave-process-method"></a>Voo protsessi meetodi seadistamine

1. Avage jaotis **Laohaldus \> Seadistus \> Vood \> Voo protsessi meetodid**.
1. Kinnitage, et loendis oleks **waveLabelPrinting**. Kui seda pole, valige selle lisamiseks toimingupaanil **Meetodite uuesti loomine**.
1. Märkige meetodi **waveLabelPrinting** puhul ruut **Muuda meetod korduvaks**.

### <a name="set-up-a-wave-template"></a>Voomalli seadistamine

1. Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.
2. Valige voomall, nt **62 Saadetise vaikemall**.
3. Teisaldage kiirkaardil **Meetodid** meetod **Voo sildi printimine** veergu **Valitud meetodid**.
4. Määrake veerus **Valitud meetodid** väärtus **Vooetapi kood**, nt *Pakk* meetodi **Voo sildi printimine** jaoks. Lisateavet vooetapi koodide kohta leiate teemast [Vooetapi koodid](wave-step-codes.md).
5. Teisaldage meetod **Voo sildi printimine** teist korda veergu **Valitud meetodid**.
6. Määrake veerus **Valitud meetodid** erinev väärtus **Vooetapi kood**, nt *Kaubaalus* teise meetodi **Voo sildi printimine** jaoks. Lisateavet vooetapi koodide kohta leiate teemast [Vooetapi koodid](wave-step-codes.md).

### <a name="create-three-wave-label-layouts"></a>Voo sildi kolme paigutuse loomine

1. Avage jaotis **Laohaldus \> Seadistus \> Dokumendi marsruudi valik \> Voo sildi paigutused**.
1. Looge järgmiste sätetega kirje.

    - **Sildi paigutuse ID:** *Pakk*
    - **Kirjeldus:** *Pakk (SSCC)*

1. Valige toimingupaanil nupp **Salvesta**.
1. Valige toimingupaanil **Voo sildi rea sätted**.

    Kuvatakse leht **Voo sildi rea sätted**. Siin saate konfigureerida sildi dünaamilise osa.

1. Lisage järgmiste sätetega rida.

    - **Rea ID:** *WaveLabel*
    - **Rea tabeli nimi:** *WHSWaveLabel*
    - **Rea algpaigutus:** *0*

        See väli määratleb vertikaalse paigutuse, kus sildil algab rida.

    - **Rea kõrgus:** *0*

        See väli määratleb iga rea kõrguse (punktides) vastavalt ZPL-standardile. Rea kõrgus on horisontaalsete siltide puhul positiivne ja vertikaalsete siltide puhul negatiivne. Kuna selles näites on ainult üks rida, saate väärtuseks seada *0* (null).

    - **Ridu lehel:** *1*

        See väli määratleb ridade arvu, mida saab igale sildile printida.

        > [!NOTE]
        > See seadistus prindib eraldi ZPL-sildi igale kirjele voo siltide tabelis.

1. Sulgege leht.
1. Valige Toimingupaanil nupp **Päringu redigeerimine**.
1. Lisage päringuredaktori dialoogiboksis vahekaardile **Vahemik** rida, millel on järgmised sätted.

    - **Tabel:** *Tööread*
    - **Tuletatud tabel:** *Tööread*
    - **Väli:** *Töö tüüp*
    - **Kriteeriumid:** *Komplekteerimine*

    See päring tagab, et sildile prinditakse ainult komplekteerimise tüübiga tööread, mitte sisestamise tüübiga tööread.

1. Kui soovite printida veokirja ID-d, valige vahekaardil **Liitmised** tabel **Tööread** ja liitke sellega tabel **Saadetised**. 
1. Sulgege päringuredaktori dialoogiboks.
1. Kiirkaardil **Printeri teksti paigutuse** on kolm jaotist, kuhu saate kirjutada printeri koodi: **Päise jaotis**, **Keha jaotis** ja **Jaluse jaotis**. Sisestage jaotise **Päise jaotis** väljale **Sildi päis** nõutava päise kood. Näiteks kui kasutate Zebra printereid, saate kasutada järgmist koodi.


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. Sisestage jaotise **Keha jaotis** väljale **Sildi keha** nõutava keha ZPL-kood. Siin on näide.

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. Sisestage jaotise **Keha jaotis** väljale **Sildi jalus** nõutava jaluse ZPL-kood. Siin on näide.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > See häälestus prindib igast sildist ühe eksemplari. Kui vajate rohkem eksemplare (nt ühte eksemplari kaubaaluse kummalegi poolele), määrake jaluse jaotise **\^PQn** väärtuseks **n** nõutav eksemplaride arv. Näiteks igast sildist nelja eksemplari printimiseks määrake **\^PQ4**.

1. Esimene silt on nüüd kasutamiseks valmis.
1. Looge järgmiste sätetega teine paigutuse kirje.

    - **Sildi paigutuse ID:** *Kaubaalus*
    - **Kirjeldus:** *Kaubaalus*

1. Valige toimingupaanil nupp **Salvesta**.
1. Valige toimingupaanil **Voo sildi rea sätted**.

    Kuvatakse leht **Voo sildi rea sätted**. Siin saate konfigureerida sildi dünaamilise osa.

1. Lisage järgmiste sätetega rida.

    - **Rea ID:** *WaveLabel*
    - **Rea tabeli nimi:** *WHSWaveLabel*
    - **Rea algpaigutus:** *0*

        See väli määratleb vertikaalse paigutuse, kus sildil algab rida.

    - **Rea kõrgus:** *0*

        See väli määratleb iga rea kõrguse (punktides) vastavalt ZPL-standardile. Rea kõrgus on horisontaalsete siltide puhul positiivne ja vertikaalsete siltide puhul negatiivne. Kuna selles näites on ainult üks rida, saate väärtuseks seada *0* (null).

    - **Ridu lehel:** *1*

        See väli määratleb ridade arvu, mida saab igale sildile printida.

        > [!NOTE]
        > See seadistus prindib eraldi ZPL-sildi igale kirjele voo siltide tabelis.

1. Sulgege leht.
1. Valige Toimingupaanil nupp **Päringu redigeerimine**.
1. Lisage päringuredaktori dialoogiboksis vahekaardile **Vahemik** rida, millel on järgmised sätted.

    - **Tabel:** *Tööread*
    - **Tuletatud tabel:** *Tööread*
    - **Väli:** *Töö tüüp*
    - **Kriteeriumid:** *Komplekteerimine*

    See päring tagab, et sildile prinditakse ainult komplekteerimise tüübiga tööread, mitte sisestamise tüübiga tööread.

1. Kui soovite printida veokirja ID-d, valige vahekaardil **Liitmised** tabel **Tööread** ja liitke sellega tabel **Saadetised**.
1. Sulgege päringuredaktori dialoogiboks.
1. Kiirkaardil **Printeri teksti paigutuse** on kolm jaotist, kuhu saate kirjutada printeri koodi: **Päise jaotis**, **Keha jaotis** ja **Jaluse jaotis**. Sisestage jaotise **Päise jaotis** väljale **Sildi päis** nõutava päise kood. Näiteks kui kasutate Zebra printereid, saate kasutada järgmist koodi.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. Sisestage jaotise **Keha jaotis** väljale **Sildi keha** nõutava keha ZPL-kood. Siin on näide.

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. Sisestage jaotise **Keha jaotis** väljale **Sildi jalus** nõutava jaluse ZPL-kood. Siin on näide.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > See häälestus prindib igast sildist ühe eksemplari. Kui vajate rohkem eksemplare (nt ühte eksemplari kaubaaluse kummalegi poolele), määrake jaluse jaotise **\^PQn** väärtuseks **n** nõutav eksemplaride arv. Näiteks igast sildist nelja eksemplari printimiseks määrake **\^PQ4**.

1. Teine silt on nüüd kasutamiseks valmis.
1. Looge järgmiste sätetega kolmas paigutuse kirje.

    - **Sildi paigutuse ID:** *Piirjoon*
    - **Kirjeldus:** *Piirjoonesilt*

1. Valige toimingupaanil nupp **Salvesta**.
1. Kiirkaardil **Printeri teksti paigutuse** on kolm jaotist, kuhu saate kirjutada printeri koodi: **Päise jaotis**, **Keha jaotis** ja **Jaluse jaotis**. Sisestage jaotise **Päise jaotis** väljale **Sildi päis** nõutava päise ZPL-kood. Siin on näide.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. Seekord pole keha nõutav. Seega, sisestage ainult nõutav tekst jaotises **Jaluse jaotis**. Siin on näide.

    ```plaintext
    ^XZ
    ```

    Kolmas silt on nüüd kasutamiseks valmis.

    > [!NOTE]
    > See kolmas silt on piirjoonesilt, mida kasutatakse sildi rullide vahelise eraldajana.

### <a name="create-two-wave-label-types"></a>Voo sildi kahe tüübi loomine

1. Avage jaotis **Laohaldus \> Seadistus \> Dokumendi marsruudi valik \> Voo sildi tüübid**.
1. Looge järgmiste sätetega kirje.

    - **Sildi tüüp:** *Pakk*
    - **Kirjeldus:** *Pakk*

1. Looge järgmiste sätetega teine kirje.

    - **Sildi tüüp:** *Kaubaalus*
    - **Kirjeldus:** *Kaubaalus*

### <a name="set-up-unit-sequence-groups"></a>Üksuse seeriagruppide häälestamine

1. Avage jaotis **Laohaldus \> Seadistus \> Ladu \> Ühiku seeriagrupid**.
1. Valige või looge grupp **Ea Kast PL**.
1. Määrake rea **Kast** välja **Voo taseme tüüp** väärtuseks *Pakk*.
1. Määrake rea **PL** välja **Voo taseme tüüp** väärtuseks *Kaubaalus*.

### <a name="create-wave-label-templates"></a>Voo sildi mallide loomine

1. Avage jaotis **Laohaldus \> Seadistus \> Dokumendi marsruudi valik \> Voo sildi mallid**.
1. Looge järgmiste sätetega sildi mall.

    - **Voo malli nimi:** *Paki sildid*
    - **Kirjeldus:** *Paki sildid*
    - **Vooetapi kood:** *Pakk*
    - **Ladu:** *62*

1. Valige kiirkaardil **Üldine** väljal **Voo sildi tüüp** suvand, nt *Pakk*.
1. Lisage kiirkaardil **Voo sildi malli üksikasjad** rida, millel on järgmised sätted.

    - **Sildi paigutuse ID:** *Pakk*
    - **Printeri nimi:** valige sobiv ZPL-printer.
    - **Käivita päring:** *Jah* (see säte on valikuline, kuid see on optimaalse jõudluse tagamiseks soovitatav.)

1. Valige toimingupaanil nupp **Salvesta**.
1. Valikuline: kui seadistate kliendipõhist sildi kujundust, tuleb teil luua päring kliendi konto leidmiseks. Valige kiirkaardil **Voo sildi malli üksikasjad** suvand **Päringu redigeerimine**. Seejärel lisage päringuredaktori dialoogiboksis vahekaardile **Vahemik** rida, millel on järgmised sätted.

    - **Tabel:** *Saadetised*
    - **Tuletatud tabel:** *Saadetised*
    - **Väli:** *Kontonumber*
    - **Kriteeriumid:** sisestage vastava kliendi kontonumber.

    Kui olete lõpetanud, valige päringuredaktori dialoogiboksi sulgemiseks **OK**.

1. Valige toimingupaanil suvand **Päringu redigeerimine**, et avada terve sildi malli päringuredaktori dialoogiboks.
1. Lisage päringuredaktori dialoogiboksis vahekaardile **Sortimine** rida, millel on järgmised sätted.

    - **Tabel:** *Tööread*
    - **Tuletatud tabel:** *Tööread*
    - **Väli:** *Koormuse viiterea ID (kirje-ID)*
    - **Otsingusuund:** *Kasvav*

1. Lisage järgmiste sätetega teine rida.

    - **Tabel:** *Tööread*
    - **Tuletatud tabel:** *Tööread*
    - **Väli:** *Saadetise ID*
    - **Otsingusuund:** *Kasvav*

1. Päringuredaktori dialoogiboksi sulgemiseks valige **OK**.
1. Teateaken palub teil rühmitamise lähtestamise toimingu kinnitada. Jätkamiseks valige **Jah**.
1. Valige toimingupaanil **Voo sildi malligrupp**.
1. Määrake dialoogiboksi **Voo sildi malli grupp** reale, kus välja **Viitevälja nimi** väärtuseks on seatud *Saadetise ID*, järgmised väärtused.

    - **Prindi piirjoonesilt:** märkige see ruut.
    - **Sildi paigutuse ID:** valige piirjoonesilt. (Valige näiteks sildi paigutus *Piirjoon*, mille eelnevalt selles stsenaariumis lõite.)
    - **Printeri nimi:** valige piirjoonesildile printer. (Tavaliselt tuleb sildi rullide tükeldamise eesmärgil valida sama printer, mis on valitud kiirkaardil **Voo sildi malli üksikasjad**. Kuid ka muud stsenaariumid on võimalikud.)

1. Märkige real, kus välja **Viitevälja nimi** väärtuseks on seatud *Koormuse viiterea ID*, ruut **Sildi kooste ID**.

    > [!NOTE]
    > See häälestus loob ühe sildi järjestuse („Pakk 1/X”) koormuse rea kohta kogu voos, sõltumata töö rühmitamise seadistusest. Seda sildi järjestust saab printida sildi paigutusele. Lisaks eraldatakse erinevate saadetiste sildid valitud piirjoonesildiga.

1. Valige **OK** dialoogiboksi **Voo sildi malli grupp** sulgemiseks.
1. Looge järgmiste sätetega teine sildi mall.

    - **Voo malli nimi:** *Kaubaaluse sildid*
    - **Kirjeldus:** *Kaubaaluse sildid*
    - **Vooetapi kood:** *Kaubaalus*
    - **Ladu:** *62*

1. Valige kiirkaardil **Üldine** väljal **Voo sildi tüüp** suvand, nt *Kaubaalus*.
1. Lisage kiirkaardil **Voo sildi malli üksikasjad** rida, millel on järgmised sätted.

    - **Sildi paigutuse ID:** *Kaubaalus*
    - **Printeri nimi:** valige sobiv ZPL-printer.
    - **Käivita päring:** *Jah* (see säte on valikuline, kuid see on optimaalse jõudluse tagamiseks soovitatav.)

1. Valige toimingupaanil nupp **Salvesta**.
1. Valikuline: kui seadistate kliendipõhist sildi kujundust, tuleb teil luua päring kliendi konto leidmiseks. Valige kiirkaardil **Voo sildi malli üksikasjad** suvand **Päringu redigeerimine**. Seejärel lisage päringuredaktori dialoogiboksis vahekaardile **Vahemik** rida, millel on järgmised sätted.

    - **Tabel:** *Saadetised*
    - **Tuletatud tabel:** *Saadetised*
    - **Väli:** *Kontonumber*
    - **Kriteeriumid:** sisestage vastava kliendi kontonumber.

    Kui olete lõpetanud, valige päringuredaktori dialoogiboksi sulgemiseks **OK**. 

1. Valige toimingupaanil suvand **Päringu redigeerimine**, et avada terve sildi malli päringuredaktori dialoogiboks.
1. Lisage päringuredaktori dialoogiboksis vahekaardile **Sortimine** rida, millel on järgmised sätted.

    - **Tabel:** *Tööread*
    - **Tuletatud tabel:** *Tööread*
    - **Väli:** *Koormuse viiterea ID (kirje-ID)*
    - **Otsingusuund:** *Kasvav*

1. Lisage järgmiste sätetega teine rida.

    - **Tabel:** *Tööread*
    - **Tuletatud tabel:** *Tööread*
    - **Väli:** *Saadetise ID*
    - **Otsingusuund:** *Kasvav*

1. Päringuredaktori dialoogiboksi sulgemiseks valige **OK**.
1. Teateaken palub teil rühmitamise lähtestamise toimingu kinnitada. Jätkamiseks valige **Jah**.
1. Valige toimingupaanil **Voo sildi malligrupp**.
1. Määrake dialoogiboksi **Voo sildi malli grupp** reale, kus välja **Viitevälja nimi** väärtuseks on seatud *Saadetise ID*, järgmised väärtused.

    - **Prindi piirjoonesilt:** märkige see ruut.
    - **Sildi paigutuse ID:** valige piirjoonesilt. (Valige näiteks sildi paigutus *Piirjoon*, mille eelnevalt selles stsenaariumis lõite.)
    - **Printeri nimi:** valige piirjoonesildile printer. (Tavaliselt tuleb sildi rullide tükeldamise eesmärgil valida sama printer, mis on valitud kiirkaardil **Voo sildi malli üksikasjad**. Kuid ka muud stsenaariumid on võimalikud.)

1. Märkige real, kus välja **Viitevälja nimi** väärtuseks on seatud *Koormuse viiterea ID*, ruut **Sildi kooste ID**.

    > [!NOTE]
    > See häälestus loob ühe sildi järjestuse („Pakk 1/X”) koormuse rea kohta kogu voos, sõltumata töö rühmitamise seadistusest. Seda sildi järjestust saab printida sildi paigutusele. Lisaks eraldatakse erinevate saadetiste sildid valitud piirjoonesildiga.

### <a name="configure-number-sequence-extensions"></a>Numbriseeria laienduste konfigureerimine

Numbriseeria laiendused juhivad konkreetsete numbriseeriate GS1 vastavust. See konfiguratsioon on praeguse stsenaariumi puhul valikuline. Lisateavet ja konfigureerimise juhiseid leiate teemast [Numbriseeria laienduste konfigureerimine](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Müügitellimuse loomine ja selle väljastamine lattu

1. Avage jaotis **Müük ja turundus \> Müügitellimus \> Kõik müügitellimused**.
1. Looge järgmiste sätetega müügitellimuse rida.

    - **Kliendi konto:** *US-001*
    - **Ladu:** *62*

1. Lisage kaks müügitellimuse rida.

    - Müügitellimuse rida 1:

        - **Kauba kood:** *A0001*
        - **Kogus:** *9024*
        - **Ühik:** *ea* (9024 ea = 376 kasti = 47 PL)

    - Müügitellimuse rida 2:

        - **Kauba kood:** *A0002*
        - **Kogus:** *9016*
        - **Ühik:** *ea* (9016 ea = 322 kasti = 46 PL)

    > [!NOTE]
    > Siin esitatud kaubad ja kogused on ainult näited. Need peavad kasutama ühiku seeriagruppi, mille eelnevalt määratlesite, neile tuleb määratleda vastav ühiku teisendamine ühikult *ea* ühikule *Kast* ühikule *PL* ja neil peab olema kaubavarusid laos *62*. Lisateavet leiate teemast [Mõõtühik ja varude poliitika](unit-measure-stocking-policies.md).

1. Valige müügitellimuse rida 1. Seejärel valige menüü **Varud** jaotisest **Müügitellimuse rida** suvand **Reserveerimised**.
1. Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii** ja seejärel sulgege leht.
1. Korrake etappe 4 ja 5 müügitellimuse rea 2 puhul.
1. Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.

    Toimub järgmine: 

    - Süsteem töötleb loodud saadetist, kasutades malli, mis sisaldab sildi printimise etappi. Sildi paigutust kasutatakse sildi vormingu määratlemiseks ja tulemuseks on silt, mis prinditakse sildi mallis valitud printeriga.
    - Voo sildid luuakse ja prinditakse. Siltide arv on võrdne pakkide arvuga (selles näites on 376 kasti silti 1. rea kohta, 322 kasti silti 2. rea kohta, 47 PL silti 1. rea kohta, 47 PL silti 2. rea kohta ja kaks piirjoonesilti, millel on saadetise ID).
    - Saadetistele luuakse uus veokirja ID. Kui konfigureerisite numbriseeria laiendused, järgib voo sildi ID numbrivormingut **SSCC-18**. 

Saate kuvada ja uuesti printida järgmiste lehtede voo silte.

- Kõik saadetised \> Saadetise üksikasjad
- Kõik koormused \> Koormuse üksikasjad
- Kõik vood
- Voo sildid
- Voosildi ajalugu

Enamiku nende lehtede puhul leiate vastava funktsiooni, valides toimingupaani vahekaardi **Saadetised** grupis **Seotud teave** suvandi **Voo sildid**.

## <a name="additional-resources"></a>Lisaressursid

- [Voosiltide uuesti printimine ja tühistamine](reprint-and-void-wave-labels.md)
- [Voo sildi printimise plaanimine voo ajal](configure-task-based-wave-label-printing.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
