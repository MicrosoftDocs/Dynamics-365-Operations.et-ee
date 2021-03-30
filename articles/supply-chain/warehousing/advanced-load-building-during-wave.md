---
title: Täiustatud koormuse koostamine voo ajal
description: Selles teemas antakse teavet täiustatud voo koormuse koostamise kohta, mis määrab voo käivitamise ajal saadetised automaatselt olemasolevatele voogudele. Seeläbi saate luua olulisi koormaid, mis tähistavad veokeid, ilma et peaksite kasutama koorma planeerimise töölauda.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod,WHSWaveTemplateTable,WHSLoadMixGroup,WHSLoadBuildTemplate, WHSWaveTableListPage, TMSLoadBuildTemplateApply, TMSLoadBuildTemplates, TMSLoadBuildTemplateCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 1b75d5cec991b2863e7e0213257ac63d5ab566a6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233195"
---
# <a name="advanced-load-building-during-wave"></a>Täiustatud koormuse koostamine voo ajal

[!include [banner](../includes/banner.md)]

Täiustatud voo koormuse koostamine määrab voo käivitamise ajal saadetised automaatselt olemasolevatele voogudele. Seeläbi saate luua olulisi koormaid, mis tähistavad veokeid, ilma et peaksite kasutama koorma planeerimise töölauda. See võimalus on kasulik ettevõtetele, kes soovivad kasutada koormuste mõistet saadetiste jälgimiseks ja planeerimiseks veoki/haagisega, kuid ei soovi neid koormaid iga päev käsitsi luua.

Voo töötlemise ajal loob süsteem tavaliselt uue koormuse igale saadetisele, millele pole koormust määratud. Kuid kui täiustatud voo koormuse koostamine on sisse lülitatud, määrab süsteem igale määramata saadetise olemasolevale koormusele (kui vastav koormus on olemas) ja uued koormused luuakse ainult juhul, kui need on nõutavad. Täiustatud voo koormuse koostamine loob automaatselt uued koormused teie määratletud kriteeriumide põhjal.

Funktsiooni kasutamiseks peate seadistama süsteemi järgmisel viisil.

- Looge *Voomallid*, mis sisaldavad uut meetodit **buildLoads**. See meetod võimaldab neid malle kasutavatel voogudel koostada täiustatud voo koormuseid.
- Seadistage *Koormuse koostamismallid*, linkides need kindla voomalli ja meetodiga. Koormuse koostamismallid juhivad seda, millisele koormusele (olemasolevale või uuele) loodava voo koormusread lisatakse. Saate saadetisi kombineerida või eraldada, tuginedes kriteeriumidele, nagu koormuse mall, seadmed ja muud koormuse rea väljade väärtused.
- Määratlege *Koormuse segagrupid*, et juhtida milliseid kaupu tuleks kombineerida ühes koormuses, milliseid mitte. Samuti saate määrata, kas piirang peaks andma hoiatuse või tõrke, ja kas koormuse malli mahupiirangut tuleks hinnata.

## <a name="turn-on-advanced-wave-load-building-in-your-system"></a>Täiustatud voo koormuse koostamise sisselülitamine teie süsteemis

Enne täiustatud voo koormuse koostamist, peavad teie süsteemis olema sisse lülitatud kaks funktsiooni. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsioonide olekut ja need vajadusel selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsioone järgneval viisil.

- Voo koormuse koostamise funktsioon.

    - **Moodul:** *laohaldus*
    - **Funktsiooni nimi:** *Voo koormuse koostamise funktsioon*

- Organisatsiooniülene vooetapi kood

    - **Moodul:** *laohaldus*
    - **Funktsiooni nimi:** *Organisatsiooniülene vooetapi kood*

### <a name="make-sample-data-available"></a>Näidisandmete kättesaadavaks tegemine

Selle demo kasutamiseks siin määratud näidiskirjete ja -väärtuste abil peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Enne alustamist peate valima ka juriidilise isiku **USMF**.

Seda demot saate kasutada ka juhistena selle funktsiooni kasutamiseks, kui töötate tootmissüsteemis. Kuid sellisel juhul peate asendama oma väärtused ja teil ei pruugi olla teatud tüüpi nõutavaid kirjeid, mida pakuvad standardsed demoandmed.

### <a name="make-sure-that-the-scenario-setup-includes-enough-available-inventory"></a>Veenduge, et stsenaariumi häälestus sisaldaks piisavalt vabu varusid

Kui töötate demoandmetega **USMF**, peate esmalt veenduma, et teie süsteem oleks seadistatud nii, et igas vastavas asukohas oleks saadaval piisavalt varusid. Selle demo puhul on eelduseks, et laos *62* oleks saadaval järgmised varud.

- **Kaup A0001:** 10 tk
- **Kaup A0002:** 10 tk
- **Kaup M9200:** 10 ea

Kaup **M9200** tuleb lisada lattu. Viige lõpule järgmiste alamjaotiste protseduurid kauba varudesse lisamiseks.

#### <a name="create-a-new-license-plate-id"></a>Uue identifitseerimisnumbri ID loomine

1. Avage jaotis **Laohaldus** \> **Seadistus** \> **Ladu** \> **Identifitseerimisnumbrid**.
1. Valige toimingupaanil nupp **Uus**.
1. Uue rea väljale **Identifitseerimisnumber** sisestage *LP6203*.
1. Valige käsk **Salvesta**.

#### <a name="create-a-standard-cost-for-item-m9200-in-site-6"></a>Standardomahinna loomine kaubale M9200 saidil 6

1. Avage **Tooteteabe haldus** \> **Tooted** \> **Väljastatud tooted**.
1. Otsige **M9200**.
1. Valige kaubarida ja seejärel valige toimingupaani vahekaardi **Kulude haldamine** grupis **Seadistamine** suvand **Kauba hind**.
1. Valige lehe **Kauba hind** vahekaardil **Ootel olevad hinnad**.
1. Valige toimingupaanil nupp **Uus**.
1. Määrake uuel real järgmised väärtused.

    - **Kuluarvutuse tüüp:** *Plaanitud kulu*
    - **Hinna tüüp:** *Kulu*
    - **Versioon:** *10*
    - **Tegevuskoht:** *6*
    - **Hind:** *1,60*

1. Valige toimingupaanil nupp **Salvesta**.
1. Valige toimingupaanil **Aktiveeri ootel olevad hinnad**.
1. Valige vahekaart **Aktiivsed hinnad**, et kontrollida, kas uus omahind on lisatud saidile *6*.

#### <a name="create-inventory-in-warehouse-62"></a>Varude loomine laos 62

1. Avage jaotis **Varude haldus** \> **Töölehe sisestused** \> **Kaubad** \> **Varude korrigeerimine**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage dialoogiboksi **Varude töölehe loomine** kiirkaardi **Ülevaade** väljale **Ladu** väärtus *62*. Võtke vastu vaikeväärtus kõigil teistel väljadel.
1. Valige dialoogiboksi sulgemiseks suvand **OK**.
1. Avatakse leht **Varude korrigeerimine**. Valige uue rea lisamiseks kiirkaardil **Töölehe read** suvand **Uus**.
1. Määrake uuel real järgmised väärtused. Võtke vastu vaikeväärtus kõigil teistel väljadel.

    - **Kauba kood:** *M9200*
    - **Asukoht:** *bulk-003*
    - **Kogus:** muutke väärtuseks *10*.

1. Valige toimingupaanil nupp **Salvesta**.
1. Tõrgete kontrollimiseks valige toimingupaanil **Kinnitamine**.
1. Kontrolli alustamiseks valige dialoogiboksis **Töölehe kontrollimine** suvand **OK**. Teile kuvatakse teade, kui kontroll on lõpule viidud.
1. Varude korrigeerimise kinnitamiseks valige toimingupaanil **Sisesta**.
1. Sisestamise alustamiseks valige dialoogiboksis **Töölehe sisestamine** suvand **OK**. Teile kuvatakse teade, kui sisestamine on lõpule viidud.

## <a name="set-up-advanced-wave-load-building"></a>Täiustatud koormuse koostamise seadistamine

### <a name="regenerate-wave-process-methods"></a>Voo protsessi meetodite uuesti loomine

Peate tõenäoliselt oma voo protsessi meetodid uuesti looma, et muuta koormuse koostamise meetod (**buildLoads**) kättesaadavaks.

1. Avage **Laohaldus** \> **Seadistus** \> **Vood** \> **Voo protsessi meetodid**.
2. Kinnitage, et loendis oleksid **buildLoads**. Kui seda pole, valige selle lisamiseks toimingupaanil **Meetodite uuesti loomine**.

### <a name="set-up-wave-templates"></a>Voomallide seadistamine

Täiustatud voo koormuse koostamise kasutamiseks peate kaasama meetodi **buildLoads** igas asjakohases [voomallis](tasks/configure-wave-processing.md).

1. Avage jaotis **Laohaldus** \> **Seadistus** \> **Vood** \> **Voomallid**.
1. Voomalli valimine.

    Kui töötate demoandmetega **USMF**, valige mall **62 saadetise vaikemall**.

1. Lehe redigeerimisrežiimi panemiseks valige toimingupaanil **Redigeeri**.
1. Valige kiirkaardi **Meetodid** ruudustikus **Ülejäänud meetodid** meetod **buildLoads**.
1. Valige meetodi **buildLoads** ruudustikku **Valitud meetodid** teisaldamiseks paremnoole nupp.
1. Väärtuse **Vooetapi kood** määramiseks meetodile **buildLoads**, peate esmalt looma koodi voo lehel **Vooetapi koodid**. Saate kasutada mis tahes soovitud väärtust, kuid veenduge, et märgiksite selle üles, kuna seda on hiljem vaja. Koodi **WSC2112** loomiseks toimige järgmiselt.

    1. Klõpsake meetodi **buildLoads** rea väljal **Vooetapi kood** allanoolt ja seejärel valige **Kuva üksikasjad**.
    1. Valige toimingupaani lehel **Vooetapi koodid** suvand **Uus**.
    1. Sisestage väljale **Vooetapi kood** väärtus *WSC2112*.
    1. Sisestage väljale **Vooetapi kirjeldus** väärtus *WSC2112*.
    1. Valige väljal **Vooetapi tüüp** suvand *Koormuse loomine*.

1. Valige **Salvesta** ja sulgege leht.
1. Valige meetodi **buildLoads** rea väljal **Vooetapi kood** äsja loodud kood (**WSC2112**).
1. Valige toimingupaanil nupp **Salvesta**.

> [!NOTE]
> Vooetapi koodid on koodid, mida kasutajad saavad seadistada ja kasutada vastavale mallidele konkreetsete juhtumite linkimiseks. Mallid sisaldavad malle täiendamiseks, konteineritesse panemiseks, siltide printimiseks, koormuste loomiseks ja sortimiseks.
>
> Kui voo etapi koode ei kasutata, peavad kasutajad sisestama vaba teksti, et viidata kindlale mallile laine meetodi eksemplarist. Vabal tekstil on kalduvus tõrgeteks, kuna kasutajad peavad veenduma, et vooetapi tekst, mida nad lisavad konkreetse vooetapi meetodi jaoks voo malli puhul, vastab täpselt sihtmalli tekstile.
>
> Konkreetse vooetapi tüübi vooetapi koodid seadistatakse eraldi lehel. Voomalli iga vooetapi meetodi eksemplari korral, mis vajab vooetapi koodi, tuleb vooetapi kood valida ripploendist. Ripploendi valik asendab vaba tekstisisestuse ja aitab vähendada inimlike vigade riski ja mõju. Seadistuse koode kasutatakse vooetapi meetodi sidumiseks voomallis meetodi sihtmalliga.

### <a name="set-up-load-mix-groups"></a>Voo segagruppide häälestus

Koormuse segagrupid kehtestavad reeglid kaubatüüpidele, mida saab ühte koormusesse kombineerida. Saate seadistada nii palju voo segagruppe kui vaja. Kuid täiustatud voo koormuse koostamise kasutamiseks peate määrama vähemalt ühe. Koormuse segagrupi loomiseks tehke järgmist.

1. Avage jaotis **Laohaldus** \> **Seadistus** \> **Koormus** \> **Koormuse segagrupid**.
1. Koormuse grupi loomiseks valige toimingupaanilt suvand **Uus**.
1. Sisestage väljale **Koormuse segagrupi ID** uue grupi nimi.

    Kui töötate demoandmetega **USMF**, seadke järgmised väärtused.

    - **Koormuse segagrupi ID:** *TV*
    - **Kirjeldus:** *TV*

1. Valige toimingupaanil **Salvesta**, et muuta kiirkaart **Koormuse segagrupi kriteeriumid** kättesaadavaks.
1. Ruudustikku uue rea lisamiseks valige kiirkaardil **Koormuse segagrupi kriteeriumid** suvand **Uus**.
1. Määrake uues reas igale väljale soovitud väärtused. Need väärtused määravad kaubagrupid, mida arvestatakse koormuse segamiseks.

    Kui töötate demoandmetega **USMF**, valige väljal **Kaubagrupp** suvand *TV ja video*.

1. Valige toimingupaanil **Salvesta**, et muuta kiirkaart **Koormuse segagrupi piirangud** kättesaadavaks.
1. Ruudustikku uue rea lisamiseks valige kiirkaardil **Koormuse segagrupi piirangud** suvand **Uus**.
1. Määrake uues reas igale väljale soovitud väärtused.

    Kui töötate demoandmetega **USMF**, seadke järgmised väärtused.

    - **Kaubagrupp:** *CarAudio*
    - **Koormuse koostamise toiming:** *Piiramine* (see väärtus takistab kaubagruppi **CarAudio** kuuluvate kaupade lisamist samasse koormusesse kaubagruppi **TV ja video** kuuluvate kaupadega.)

1. Jätkake reeglitega töötamist senikaua, kuni olete lisanud kõik koormuse segagrupi jaoks vajalikud kriteeriumid ja piirangud.

Kui töötate demoandmetega **USMF**, olete nüüd selle häälestuse lõpetanud.

### <a name="set-up-load-build-templates"></a>Koormuse koostamismallide häälestamine

Saate seadistada nii palju koormuse koostamismalle kui vaja. Kuid täiustatud voo koormuse koostamise kasutamiseks peate määrama vähemalt ühe. Koosmuse koostamismalli loomiseks tehke järgmist.

1. avage jaotis **Laohaldus** \> **Seadistus** \> **Koormus** \> **Voo koormuse koostamise mallid**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.
1. Määrake uuel real järgmised väärtused.

    | Väli | Kirjeldus | Demoandmete USMF väärtus |
    |---|---|---|
    | Järjekorranumber | Malli hindamise järjekord. | *1* |
    | Koorma koostamise malli nimi | Sisestage koormuse koostamismalli kordumatu identifikaator. Peaksite sisestama selle malli nime, mille lõite või uuendasite eelnevalt selles häälestuses. | *62 saadetise vaikemall* |
    | Vooetapi kood | Sisestage vooetapi kood, mda kasutada malli linkimiseks voomeetodiga. Peaksite sisestama meetodi **buildLoads** jaoks valitus koodi, kui seadistasite voomalli eelnevalt selles häälestuses. | *WSC2112* |
    | Koormuse malli ID | Valige koormuse mall, mida kasutada uute koormuste loomisel ja millega vastendada olemasolevatele koormustele määramisel. Koormuse mall määratleb maksimaalse kaalu ja mahu, mis on lubatud kogu koormuse puhul. | *Stand koormuse mall* |
    | Seadmed | Varustus, millega vastendada olemasolevatele koormatele määramisel ja mida sisestada uute loodavate koormate puhul. | Jätke see väli tühjaks. |
    | Koorma segamisgrupi ID | Valige koormuse segagrupp, mida kasutada, kui kaup koormuses lubatakse. Segagrupid kehtestavad reeglid kaubatüüpidele, mida saab ühte koormusesse kombineerida. Peaksite valima ühe segagrupi, mille eelnevalt lõite selles häälestuses. | *TV* |
    | Kasuta avatud koormaid | Valige, kas olemasolevatele avatud koormustele tuleks juurde lisada. Valikud on järgmised:<ul><li>**Puudub** – ärge lisage avatud koormusi ühelegi olemasolevale koormusele.</li><li>**Mis tahes** – lisage avatud koormuseid kõigile olemasolevatele koormustele, mis rea puhul kehtivad.</li><li>**Määratud** – lisage voole määratud koormusele avatud koormuseid.</li></ul> | *Mõni* |
    | Loo koormad | Määrake, kas tuleks luua uusi koormuseid, kui ükski olemasolev koormus ei vasta kriteeriumidele. | Valitud (= *Jah*) |
    | Saadetise rea tükeldamise lubamine | Määrake, kas ühte koormuse rida saab tükeldada mitme koormuse üleselt, kui täielik rida ületab koormuse malli maksimaalset võimsust. | Tühjendatud (= *Ei*) |
    | Valideeri maht | Määrake, kas koormuse koostamine peaks kontrollima igal koormuse rea lisamisel kaalu ja mahtu, tagamaks, et koormuse malli mahupiiranguid järgitakse. | Tühjendatud (= *Ei*) |

1. Valige toimingupaanil **Salvesta**, et muuta suvand **Redigeeri päringut** kättesaadavaks.
1. Valige toiminguribal suvand **Redigeeri päringut**, et avada dialoogiboks päringu redigeerimiseks.
1. Valige päringu dialoogiboksis vahekaardil **Sortimine** suvand **Lisa**, et lisada rida ruudustikule.
1. Määratlege uues reas sortimise reeglid, mida soovite kasutada. Määrake näiteks järgmised väärtused, et sortida otsingutulemusi kasvavas järjestuses tellimuse numbri järgi.

    - **Tabel:** *Koormuse üksikasjad*
    - **Tuletatud tabel:** *Koormuse üksikasjad*
    - **Väli:** *Tellimuse number*
    - **Otsingusuund:** *Kasvav*

1. Oma muudatuste salvestamiseks ja dialoogiboksi sulgemiseks valige **OK**.
1. Määrake kiirkaardil **Piir** reeglid, et juhtida, kuidas teie koormuseid tükeldatakse. Üldjuhul võite piiriks seada kohandatud väljad, mis on laiendatud koormuse reale, nt **Marsruut**, **Ülevaade** või **Käitamine**. Näiteks ühe koormuse loomiseks tellimuse numbri kohta, märkige ruut **Piir** järgmiste väärtustega rea puhul.

    - **Viitetabeli nimi:** *Koormuse üksikasjad*
    - **Viitevälja nimi:** *Tellimuse number*

## <a name="scenario"></a>Stsenaarium

Selles stsenaariumis näidatakse, kuidas selles teemas eelnevalt kirjeldatud sätted mõjutavad laotoiminguid müügitellimuse töötlemise ajal. See stsenaarium kasutab demoandmeid **USMF** koos teiste demoväärtustega, mis on esitatud nendes seadistuse juhistes.

### <a name="create-sales-orders"></a>Müügitellimuste loomine

1. Avage **Müük ja turundus** \> **Müügitellimused** \> **Kõik müügitellimused**.
1. Valige toimingupaanil **Uus**, et avada dialoogiboks **Müügitellimuse loomine**.
1. Määrake dialoogiboksis järgmised väärtused.

    - Määrake kiirkaardi **Klient** välja **Kliendi konto** väärtuseks *US-007*.
    - Määrake kiirkaardi **Üldine** välja **Ladu** väärtuseks *62*.

1. Valige müügitellimuse loomiseks ja dialoogiboksi sulgemiseks **OK**.
1. Teie uus müügitellimus on avatud. See peaks sisaldama uut tühja rida kiirkaardi **Müügitellimuse read** ruudustikus. Määrake selle uue rea välja **Kaubakood** väärtuseks *A0001*, välja **Kogus** väärtuseks *1*.
1. Valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.
1. Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**.
1. Müügitellimusse naasmiseks valige lehe paremas ülanurgas nupp **Sule** (**X**).
1. Tehke tegevuspaani vahekaardil **Ladu** grupis **Tegevused** valik **Vabasta lattu**. Süsteem loob saadetise ja lisab selle uuele koormusele, kuna olemasolev koormus ei sisalda selle tellimuse numbriga koormuse ridu.

    Saate teabesõnumeid, mis näitavad selle tellimuse jaoks loodud tööd, voogu ja saadetist.

1. Müügireal koormuse, saadetise ja töö üksikasjade kinnitamiseks valige rida ja seejärel valige ruudustiku kohal olevas menüüs **Ladu** suvand **Koormuse üksikasjad**, **Saadetise üksikasjad** või **Töö üksikasjad**.
1. Valige äsja loodud müügitellimuses kiirkaardil **Müügitellimuse read** suvand **Lisa rida**, et lisada teine rida.
1. Määrake uue rea välja **Kaubakood** väärtuseks *A0002*, välja **Kogus** väärtuseks *1*.
1. Korrake ridu 6–9 rea reserveerimiseks ja lattu vabastamiseks. Süsteem loob teie lisatud reale **uue** saadetise. Kuid kuna kasutate täiustatud voo koormuse koostamist, lisab süsteem selle saadetise ja koormuse rea olemasolevale voole. Kui te ei kasutaks täiustatud voo koormuse koostamist, looks süsteem saadetise jaoks uue koormuse.
1. Valige äsja loodud müügitellimuses kiirkaardil **Müügitellimuse read** suvand **Lisa rida**, et lisada teine rida.
1. Määrake uue rea välja **Kaubakood** väärtuseks *M9200*, välja **Kogus** väärtuseks *1*.
1. Korrake ridu 6–9 rea reserveerimiseks ja lattu vabastamiseks. Nagu eelnevalt, loob süsteem teie lisatud reale **uue** saadetise. Kuid kuna kaup pärineb kaubagrupist **CarAudio**, ei **läbi see koormuse segagrupile määratud piiranguid**. Seetõttu **lisatakse see uuele koormusele**. Kui te pole koormuse loomise mallis määranud koormuse segagruppi, oleks see saadetis lisatud esimesele koormusele.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]