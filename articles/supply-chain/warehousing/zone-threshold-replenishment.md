---
title: Tsooniläve täiendamine
description: Tsoonipõhine täiendamine kasutab minimaalse/maksimaakse (min/max) täiendamise strateegiat, kuid see hindab üksikute asukohtade asemel ainult terveid laotsoone. Tänu sellele saavad laohaldurid kiiremini teada, kui komplekteerimistsoonis on vaja täiendavat varu.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 44e7dfdbc980c5df6b9426515365611bc0de45c2
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335941"
---
# <a name="zone-threshold-replenishment"></a>Tsooniläve täiendamine

[!include [banner](../includes/banner.md)]

Tsoonipõhine täiendamine kasutab minimaalse/maksimaakse (min/max) [täiendamise](replenishment.md) strateegiat, kuid see hindab üksikute asukohtade asemel ainult terveid laotsoone. Tänu sellele saavad laohaldurid kiiremini teada, kui komplekteerimistsoonis on vaja täiendavat varu.

Selle funktsiooni seadistus sarnaneb asukohapõhise täiendamise seadistusele. Kuid min/max täiendamise malli seadistamise ajal saate ka määrata, kas läve tuleks hinnata asukoha või tsooni põhjal. Kui seadistate tsoonidel põhineva hindamise, peate tsooni valiku päringule lisama kindlad tsoonid.

Sarnaselt asukohapõhisele min/max täiendamisele, põhineb tsoonipõhine min/max täiendamine minimaalse varu läve häälestusel, mis käivitab valitud kaupade täiendamise töö loomise. See täiendamise töö suurendab varusid selle tsooni jaoks määratud maksimaalse läveni.

> [!NOTE]
> Praeguses väljalaskes ei toetata tootevariantide tsooni täiendamise protsesse.


Erinevalt asukohapõhisest min/max täiendamisest, ei nõua tsoonipõhine min/max täiendamine fikseeritud asukohti selle hindamiseks, kas asukohad peaksid ladustama kindlat kaupa. Tänu sellele võimaldab tsoonipõhine täiendamine kasutada min/max täiendamist ka siis, kui teil pole laos iga kauba või kaubavariandi jaoks fikseeritud asukohti. Kui tsoonis langeb kogus määratud lävest allapoole, luuakse täiendamise töö. Asukohakorraldused määravad, millisesse kindlasse asukohta varud tuleks panna.

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a>Funktsiooni Tsooniläve täiendamine sisselülitamine

Enne kui saate kasutada tsooni *läve täiendamise funktsiooni*, peab see olema teie süsteemi jaoks sisse lülitatud. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Tsooniläve täiendamine*

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a>Tsoonipõhise täiendamise häälestus

Tsoonipõhise täiendamise seadistamiseks peate konfigureerima süsteemi mitu osa. See jaotis tutvustab erinevaid sätteid ja pakub demo andmeväärtusi, mida saate sisestada, kui soovite stsenaariumi selle artikli lõpus läbi töötada.

### <a name="set-up-directive-codes"></a>Korralduskoodide häälestus

[Korralduskoodid](control-warehouse-location-directives.md) võimaldavad teil täpsemalt määratleda asukohamalli, mida kasutatakse töömallis. Iga koodiga luuakse ühine väärtus, millele saate viidata iga mallitüübi konfigureerimisel.

#### <a name="view-and-edit-directive-codes"></a>Korralduskoodide kuvamine ja redigeerimine

Oma korralduskoodide kuvamiseks või redigeerimiseks avage jaotis **Laohaldus \> Häälestus \> Korralduskoodid**.

#### <a name="prepare-demo-data-directive-codes"></a>Demoandmete korralduskoodide ettevalmistamine

Selles näites kirjeldatakse, kuidas valmistada ette korralduskoodi. Kui plaanite stsenaariumit selle artikli lõpus läbi töötada, kasutage demoandmete väärtusi, mis siin antakse. Muul juhul saate kasutada oma väärtusi.

1. Valige juriidiline isik **USMF** demoandmetega töötamiseks.
1. Avage jaotis **Laohaldus \> Seadistus \> Korralduskoodid**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.
1. Määrake uuel real järgmised väärtused.

    - **Korralduskood:** _Tsooni täiend_
    - **Korralduse kirjeldus:** _Tsooni täiendamine_

1. Uue koodi salvestamiseks valige **Salvesta**.

### <a name="set-up-replenishment-templates"></a>Täiendamismallide häälestamine

[Min/max täiendamismallid](tasks/set-up-min-max-replenishment-process.md) on põhimehhanism komplekteerimiskohtades optimaalsete tasemete säilitamiseks. Nendes mallides peate seadistama reeglid, mida kasutatakse laovarude täiendamiseks. Täiendamise hulka, mille jaoks saab malle kasutada, kuulub ka tsoonipõhine täiendamine.

#### <a name="view-and-edit-replenishment-templates"></a>Täiendamismallide kuvamine ja redigeerimine

Täiendamismall on reeglistik, mis määrab asikoha täiendamise aja ja viisi. Saate valida malli täiendamise tegemise aja ja viisi juhtimiseks. Täiendamismallide kuvamiseks ja redigeerimiseks avage jaotis **Laohaldus \> Seadistus \> Täiendamine \> Täiendamismallid**.

#### <a name="prepare-a-demo-data-replenishment-template"></a>Demoandmete täiendamismalli ettevalmistamine

Selles näites kirjeldatakse, kuidas valmistada ette täiendamismalli. Kui plaanite stsenaariumit selle artikli lõpus läbi töötada, kasutage demoandmete väärtusi, mis siin antakse. Muul juhul saate kasutada oma väärtusi.

1. Valige juriidiline isik **USMF** demoandmetega töötamiseks.
1. Avage jaotis **Laohaldus \> Seadistus \> Täiendamine \> Täiendamismallid**.
1. Lehe redigeerimisrežiimi panemiseks valige **Redigeeri**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida **Ülevaade**.
1. Määrake uuel real järgmised väärtused. Võtke vastu vaikeväärtused kõigil teistel väljadel.

    - **Täiendamismall:** _Tsooni min/max täiend_
    - **Kirjeldus:** _Tsooni min/max täiendamine_
    - **Täiendamise tüüp:** _Minimaalne või maksimaalne_

1. Valige käsk **Salvesta**.
1. Kui uus rida on valitud ruudustikus **Ülevaade**, valige ruudustiku **Täiendamismalli üksikasjad** kohalt suvand **Uus**, et lisada rida, mis on seostatud teie äsja loodud täiendamismalliga *Tsooni min/max. täiend*.
1. Määrake uuel real järgmised väärtused.

    - **Järjekorranumber:** sisestage _1_.
    - **Kirjeldus:** Sisestage _Komplekteerimistsooni täiendamine_.
    - **Täiendamise ühik:** valige _ea_.
    - **Taotluse tüüp:** jätke see väli tühjaks.
    - **Korralduse kood:** see väli seob täiendamismalli asukohakorraldusega. Valige eelnevalt loodud demoandmete korralduskood (_Tsooni täiend_).
    - **Töömall:** jätke see väli tühjaks.
    - **Minimaalne kogus:** see väli määrab koguse, mille puhul täiendamine käivitatakse. Sisestage _50_.
    - **Maksimaalne kogus:** see väli määrab kauba maksimaalse koguse, mis võib tsoonis olla. Loodud varude täiendamistöö suurendab varud sellele kogusele. Sisestage _150_.
    - **Ühik:** see väli määrab minimaalse ja maksimaalse väärtuse ühiku. Valige _ea_.
    - **Nõudluse juurdekasv:** valige _Ümardamine üles_.
    - **Tühjade fikseeritud asukohtade täiendamine:** valige see märkeruut.
    - **Ainult fikseeritud asukohtade täiendamine:** tühjendage see märkeruut.
    - **Toote päringu režiim:** valige _Toote päring_.
    - **Täiendamise läve ulatus:** see väli määratleb, kas mall peaks hindama tsooni või kindla asukoha alusel. Valige _Tsoon_.
    - **Ladu:** valige _61_.

1. Valige ruudustiku **Täiendamismalli üksikasjad** kohalt **Toodete valimine**.
1. Valige dialoogiboksi **Toote päring** vahekaardil **Vahemik** suvand **Lisa**, et lisada rida ruudustikule.
1. Määrake uuel real järgmised väärtused.

    - **Tabel:** _Kaubad_
    - **Tuletatud tabel:** _Kaubad_
    - **Väli:** _Kaubakood_
    - **Kriteeriumid:** _A0001_

1. Oma päringu salvestamiseks ja dialoogiboksi sulgemiseks valige **OK**.
1. Valige ruudustiku **Täiendamismalli üksikasjad** kohalt **Täiendatavate tsoonide valimine**.
1. Valige dialoogiboksi **Tsooni päring** vahekaart **Vahemik**, et lisada rida ruudustikule.
1. Määrake uuel real järgmised väärtused.

    - **Tabel:** _Lao tsoon_
    - **Tuletatud tabel:** _Lao tsoon_
    - **Väli:** _Tsooni ID_
    - **Kriteerium:** _FLOOR_

1. Oma päringu salvestamiseks ja dialoogiboksi sulgemiseks valige **OK**.

### <a name="set-up-location-directives"></a>Asukohakorralduste häälestamine

Erinevalt asukohapõhisest min/maks. täiendamisest, nõuab tsoonipõhine min/max täiendamine, et seadistaksite nii komplekteerimise asukoha korralduse kui ka ladustamise korralduse, kuna süsteem hindab komplekteerimise asukoha asemel kogu tsooni väljamineva töö jaoks.

#### <a name="view-and-edit-location-directives"></a>Asukohakorralduste kuvamine ja redigeerimine

Oma asukohakorralduste kuvamiseks või redigeerimiseks avage jaotis **Laohaldus \> Häälestus \> Asukohakorraldus**.

Vaadake järgmises jaotises olevaid näiteid, kuidas kasutada sätteid nõutava komplekteerimise asukohadirektiivi ja komplekteerimise asukohadirektiivi loomiseks.

#### <a name="prepare-demo-data-location-directives"></a>Demoandmete asukohakorralduste ettevalmistamine

Demoandmete ettevalmistamiseks nii, et seda saaks kasutada selle artikli lõpus stsenaariumis, peate looma kaks asukohadirektiivi: üks noppimiseks ja teine panemiseks.

##### <a name="create-a-replenishment-pick-directive"></a>Täiendamise komplekteerimise korralduse loomine

1. Valige juriidiline isik **USMF** demoandmetega töötamiseks.
1. Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.
1. Määrake vasakpoolse paani välja **Töökäsu tüüp** suvandiks _Täiendamine_.
1. Uue korralduse loomiseks valige toimingupaanilt suvand **Uus**.
1. Määrake järgmised väärtused.

    - **Järjekorranumber:** nõustuge vaikeväärtusega.
    - **Nimi:** sisestage _Tsooni komplekteerimine_.
    - **Töö tüüp:** Valige _Komplekteerimine_.
    - **Tegevuskoht:** valige _6_.
    - **Ladu:** valige _61_.
    - **Korralduse kood:** jätke see väli tühjaks.
    - **Mitmik-SKU:** määrake selle suvandi väärtuseks _Ei_.

1. Valige **Salvesta**, et luua korraldus, millel on teie siiani konfigureeritud sätted.
1. Valige kiirkaardil **Read** suvand **Uus**, et lisada rida ruudustikku.
1. Määrake uuel real järgmised väärtused.

    - **Järjekorranumber:** sisestage _1_.
    - **Alates kogusest:** sisestage _0_.
    - **Kuni koguseni:** sisestage _10000000_.
    - **Ühik:** jätke väli tühjaks.
    - **Koguse asukoha leidmine:** valige _Puudub_.
    - **Piira ühiku alusel:** tühjendage see märkeruut.
    - **Ümardage ühikuni:** tühjendage see märkeruut.
    - **Pakendi koguse asukoha leidmine:** tühjendage see märkeruut.
    - **Luba tükeldamine:** märkige see ruut.

1. Uue rea salvestamiseks valige **Salvesta**.
1. Kui teie uus rida on valitud ruudustikul **Read**, valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus**, et lisada rida ruudustikku.
1. Määrake uuel real järgmised väärtused.

    - **Järjekorranumber:** sisestage _1_.
    - **Nimi:** sisestage _Hulgikomplekteerimine_.
    - **Fikseeritud asukoha kasutus:** valige _Fikseeritud ja mittefikseeritud asukohad_.
    - **Luba negatiivne laovaru:** tühjendage see märkeruut.
    - **Partii lubatud:** tühjendage see märkeruut.
    - **Strateegia:** valige _Puudub_.

1. Uue tegevuse salvestamiseks valige **Salvesta**.
1. Kui uus tegevus on valitud, valige ruudustiku **Asukohakorralduse tegevused** kohalt suvand **Päringu redigeerimine**.
1. Kuvatakse päringu dialoogiboks, kust saate valida asukohad, millest täiendada. Vahekaardil **Vahemik** valige käsk **Lisa**, et lisada uus rida ruudustikule.
1. Määrake uuel real järgmised väärtused.

    - **Tabel:** _Asukohad_
    - **Tuletatud tabel:** _Asukohad_
    - **Väli:** _Tsooni ID_
    - **Kriteeriumid:** _BULK_

1. Oma päringu salvestamiseks ja dialoogiboksi sulgemiseks valige **OK**.
1. Oma asukohakorralduse salvestamiseks valige **Salvesta**.

##### <a name="create-a-replenishment-put-directive"></a>Täiendamise ladustamise korralduse loomine

1. Veenduge, et vasakpoolse paani lehel **Asukohakorraldused** oleks välja **Töökäsu tüüp** väärtuseks _Täiendamine_.
1. Muu korralduse loomiseks valige toimingupaanilt suvand **Uus**.
1. Määrake järgmised väärtused.

    - **Järjekorranumber:** nõustuge vaikeväärtusega.
    - **Nimi:** sisestage _Tsooni ladustamine_.
    - **Töötellimuse tüüp:** valige _Ladustamine_.
    - **Tegevuskoht:** valige _6_.
    - **Ladu:** valige _61_.
    - **Korralduskood:** valige _Tsooni täiend_, et linkida see asukohakorraldus eelnevalt loodud täiendamismalliga, kasutades eelnevalt loodud koodi.
    - **Mitmik-SKU:** määrake selle suvandi väärtuseks _Ei_.

1. Valige **Salvesta**, et luua korraldus, millel on teie siiani konfigureeritud sätted.
1. Valige kiirkaardil **Read** suvand **Uus**, et lisada rida ruudustikku.
1. Määrake uuel real järgmised väärtused.

    - **Järjekorranumber:** sisestage _1_.
    - **Alates kogusest:** sisestage _0_.
    - **Kuni koguseni:** sisestage _10000000_.
    - **Ühik:** jätke väli tühjaks.
    - **Koguse asukoha leidmine:** valige _Puudub_.
    - **Piira ühiku alusel:** tühjendage see märkeruut.
    - **Ümardage ühikuni:** tühjendage see märkeruut.
    - **Pakendi koguse asukoha leidmine:** tühjendage see märkeruut.
    - **Luba tükeldamine:** märkige see ruut.

1. Uue rea salvestamiseks valige **Salvesta**.
1. Kui teie uus rida on valitud ruudustikul **Read**, valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus**, et lisada rida ruudustikku.
1. Määrake uuel real järgmised väärtused.

    - **Järjekorranumber:** sisestage _1_.
    - **Nimi:** sisestage _Tsooni ladustamine_.
    - **Fikseeritud asukoha kasutus:** valige _Fikseeritud ja mittefikseeritud asukohad_.
    - **Luba negatiivne laovaru:** tühjendage see märkeruut.
    - **Partii lubatud:** tühjendage see märkeruut.
    - **Strateegia:** valige _Konsolideeri_.

1. Uue tegevuse salvestamiseks valige **Salvesta**.
1. Kui uus tegevus on endiselt valitud, valige ruudustiku **Asukohakorralduse tegevused** kohalt suvand **Päringu redigeerimine**.
1. Kuvatakse päringu dialoogiboks, kust saate valida tsooni, kuhu täiendada. See tsoon peaks vastama täiendamismallis määratud tsoonile. Vahekaardil **Vahemik** valige käsk **Lisa**, et lisada uus rida ruudustikule.
1. Määrake uuel real järgmised väärtused.

    - **Tabel:** _Asukohad_
    - **Tuletatud tabel:** _Asukohad_
    - **Väli:** _Tsooni ID_
    - **Kriteerium:** _FLOOR_

1. Oma päringu salvestamiseks ja dialoogiboksi sulgemiseks valige **OK**.
1. Oma asukohakorralduse salvestamiseks valige **Salvesta**.

## <a name="scenario"></a>Stsenaarium

Selles jaotises esitatakse näidisstsenaarium, mis näitab, kuidas selle funktsiooniga töötada.

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a>Valmistage ette näidisstsenaariumi jaoks nõutavad näidisandmed

Enne, kui alustate stsenaariumi läbimist, peate aktiveerima näidisandmed ja seadistama funktsiooni nii, nagu on kirjeldatud selles jaotises ja selle artikli eelmistes jaotistes.

#### <a name="use-the-usmf-legal-entity"></a>Juriidilise isiku USMF kasutamine

Selle stsenaariumi kasutamiseks siin määratud näidiskirjete ja -väärtuste abil peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/fin-ops/get-started/demo-data.md). Enne alustamist peate valima ka juriidilise isiku **USMF**.

#### <a name="prepare-additional-sample-data"></a>Täiendavate näidisandmete ettevalmistamine

Kui olete valinud **USMF-i**[juriidilise isiku, lisage nõutavad täiendavad näidisandmed,](#setup) nagu on kirjeldatud selle artikli jaotises Tsoonipõhise täiendamise häälestamine.

#### <a name="check-your-on-hand-inventory"></a>Vaba kaubavaru kontrollimine

Järgige neid etappe, et veenduda, kas teie süsteem sisaldab näidisstsenaariumi toetamiseks piisavalt varusid.

1. Veenduge, et kauba *A0001* jaoks oleks vaba kaubavaru komplekteerimistsooni kahes eri asukohas (*FLOOR*), mis on määratud täiendamismallis. Kuid kogu varu peaks olema väiksem kui nõutav minimaalne kogus (*50*), mis on määratletud täiendamismallis. Sel viisil saate simuleerida, kuidas toimub arvutamine üksiku asukoha asemel terve tsooni jaoks. **Kasutage varude korrigeerimiseks mis tahes laoprotsessi.**
1. Veenduge, et kauba *A0001* jaoks oleks piisavalt varusid hulgiasukohas, mis on määratud tsooni komplekteerimise asukohakorralduses, kus täiendamistöö peaks komplekteerima kaubad tsooni ID-st *BULK*. Kogu varu peaks olema rohkem kui nõutav maksimaalne kogus (*150*), mis on määratletud täiendamismallis.
1. Valikuline, kuid soovitatav: tehke lao korrigeerimise töölehe loomiseks järgmist.

    1. Avage jaotis **Varude haldus \> Töölehe sisestused \> Kaubad \> Varude korrigeerimine**.
    1. Valige suvand **Uus**.
    1. Valige dialoogiboksi **Varude töölehe loomine** väljal **Ladu** väärtus *61*.
    1. Valige nupp **OK**.
    1. Kasutage kiirkaardil **Töölehe read** nuppu **Uus**, et lisada ruudustikku kolm rida ja seadke järgmised väärtused. Pärast kõigi ridade seadistamise lõpule viimist valige **Salvesta**.

        - **Rida 1:**

            - **Kauba kood:** *A0001*
            - **Tegevuskoht:** *6*
            - **Ladu:** *61*
            - **Asukoht:** *02A01R1S1B*
            - **Identifitseerimisnumber:** valige loendist olemasolev identifitseerimisnumber või looge uus.
            - **Kogus:** *1000*

        - **Rida 2:**

            - **Kauba kood:** *A0001*
            - **Tegevuskoht:** *6*
            - **Ladu:** *61*
            - **Asukoht:** *07A01R2S1B*
            - **Identifitseerimisnumber:** valige loendist olemasolev identifitseerimisnumber või looge uus.
            - **Kogus:** *15*

        - **Rida 3:**

            - **Kauba kood:** *A0001*
            - **Tegevuskoht:** *6*
            - **Ladu:** *61*
            - **Asukoht:** *07A01R1S1B*
            - **Identifitseerimisnumber:** valige loendist olemasolev identifitseerimisnumber või looge uus.
            - **Kogus:** *10*

    1. Valige toimingupaanil **Kinnita**. Lahendage kõik leitud tõrked enne järgmisse etappi liikumist.
    1. Varude lattu sisestamiseks valige toimingupaanil **Sisesta**.

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a>Näidisstsenaarium: käivitage tsoonipõhine min/max täiendamine

Kui kõik eeltingimuseks olevad näidisandmed on olemas, saate käivitada täiendamise, järgides neid etappe.

1. Avage jaotis **Laohaldus \> Täiendamine \> Täiendamine**.
1. Valige dialoogiboksi **Täiendamine** kiirkaardil **Kaasatavad kirjed** suvand **Filter**.
1. Redigeerige dialoogiboksi **Päring** vahekaardil **Vahemik** tabeli vaikerida järgmisel viisil.

    - **Tabel:** valige _Täiendamismallid_.
    - **Tuletatud tabel:** valige _Täiendamismallid_.
    - **Väli:** valige _Täiendamismall_.
    - **Kriteeriumid:** valige _Tsoon min/max täiend_. Selle sama täiendamismalli lõite selle stsenaariumi jaoks demoandmete ettevalmistamise ajal.

1. Päringu salvestamiseks sulgemiseks valige **OK** ja minge tagasi dialoogiboksi **Täiendamine**.
1. Täiendamismalli käitamiseks valige **OK**.

Täiendamistöö on nüüd loodud, et komplekteerida varusid tsoonist *BULK* ja täiendada tsooni *FLOOR*.

## <a name="notes-and-tips"></a>Märkmed ja näpunäited

Siin on mõningaid märkuseid ja näpunäited funktsiooniga töötamiseks.

- Täiendamistöö seadistamiseks, mis läheks soovitud tsooni, saate linkida täiendamismalli read ja asukohkorraldused ühel järgmistest viisidest.

    - Redigeerige asukohakorralduse päise päringut ja filtreerige valitud täiendamismalli read.
    - Kasutage korralduskoodi täiendamismalli real ja muutke see ladustamise asukohakorraldusele vastavaks.

- Kui kasutate dünaamilisi asukohti, luuakse täiendamistöö kas esimese saadaoleva asukoha või juba varusid sisaldava asukoha jaoks, kui asukohakorralduse tegevus on seadistatud kasutama strateegiat **Konsolideerimine**.
- Kui kasutate tsoonide asemel fikseeritud asukohti, peaksite kasutama [standardset min/max täiendamist](tasks/set-up-min-max-replenishment-process.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]