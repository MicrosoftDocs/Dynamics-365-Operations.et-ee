---
title: Kvaliteedikontroll
description: Sellest teemast leiate teavet kvaliteedikontrolli funktsiooni kohta. See funktsioon võimaldab laotöötajatel teha kiireid, pistelisi kontrolle kaupade vastuvõtmisel saabumisalale.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate,WHSWorkClass,WHSWorkTemplateTable.WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 44a4694281f3dd53581c9d8245a0105b37b2b155
ms.sourcegitcommit: 7dc2ff9461c310324937bea2fc160ff056fefd8a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686353"
---
# <a name="quality-check"></a>Kvaliteedikontroll

[!include [banner](../includes/banner.md)]

Funktsioon *Kvaliteedikontroll*võimaldab laotöötajatel teha kiireid, pistelisi kontrolle kaupade vastuvõtmisel saabumisalale. Need pistelised kontrollid on kasulikud, kui töötajad kontrollivad kauba pakendit või muid kergesti äratuntavaid kaupade osi. Funktsioon juhendab töötajaid kiirelt vaatama, kas midagi on ilmselgelt vigane või kahjustatud, enne kui nad ladustavad laokaubad ladustamise asukohta.

See funktsioon on standardse kvaliteedikontrolli alternatiiv. See pakub rohkem paindlikkust ja kiiremat töötlemist.

Selle funktsiooni kasutamisel toimub saabumis- ja kvaliteedikontroll järgmiselt.

1. Kui saadetis saabub, registreerib laotöötaja saabumise. Asukoha registreerimiseks skannib töötaja ka litsentsiplaadi.
1. Töötaja teeb kiire kvaliteedikontrolli ja salvestab selle litsentsiplaadi tulemuse (läbitud või nurjus).
1. Aset leiab üks järgmistest toimingutest.

    - Kui kvaliteedikontroll on läbitud, võetakse litsentsiplaat vastu ja suunatakse vastuvõtvasse asukohta, nagu tavaliselt.
    - Kui kvaliteedikontroll ebaõnnestus, lükatakse litsentsiplaat tagasi ja selle olemasolev ladustamistöö suunatakse ümber edasiseks kontrollimiseks alternatiivsesse asukohta. Luuakse uus kvaliteettellimus. Nurjunud kvaliteedikontrolli põhjal loodud kvaliteettellimuse vaatamiseks avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Kvaliteettellimused**.

Seda protsessi saab häälestada ka nii, et kõik skannitud litsentsiplaadid suunatakse kohe kvaliteedikontrolli asukohta.

## <a name="turn-on-the-quality-check-feature"></a>Kvaliteedikontrolli funktsiooni sisselülitamine

Enne funktsiooni *Kvaliteedikontroll* kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Kvaliteedikontroll*

## <a name="set-up-the-feature-for-the-example-scenario"></a>Funktsiooni häälestamine näidisstsenaariumi jaoks

Sellest jaotisest leiate juhised ja näite funktsiooni *Kvaliteedikontroll* häälestamise ning näidisandmete ettevalmistamise kohta teemas hiljem esitatud näidisstsenaariumi jaoks.

### <a name="make-sample-data-available"></a>Näidisandmete kättesaadavaks tegemine

Selle [näidisstsenaariumi](#example-scenario) kasutamiseks siin määratud näidiskirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Enne alustamist peate valima ka juriidilise isiku **USMF**.

### <a name="quality-check-template"></a><a name="quality-template"></a>Kvaliteedikontrolli mall

Kvaliteedikontrolli mall määratleb reeglid, mille alusel saab vastuvõtmise ajal teha kiireid, pistelisi kontrolle.

1. Avage **Laohaldus \> Häälestamine \> Töö \> Kvaliteedikontrolli mall**.
1. Malli lisamiseks tabelisse klõpsake valikut **Uus**.
1. Uue malli määratlemiseks määrake järgmised väärtused.

    - **Kvaliteedikontrolli malli nimi:** *Laadimissilla kontroll*

        Sisestage nimi, mis tuvastab sellele mallile rakendatud poliitikad.

    - **Vastuvõtupoliitika:** *Küsi kasutajalt*

        Määrake, kas kasutajatelt peaks töö töötlemise ajal küsima varude vastuvõtmist või tagasilükkamist või kas kvaliteet tuleks automaatselt tagasi lükata. Saadaolevad valikud on *Lükka automaatselt tagasi*ja *Küsi kasutajalt*.

    - **Kvaliteeditöötluse poliitika:** *Loo kvaliteettellimus*

        Valige poliitika, mida tuleks kasutada varude kvaliteedi tagasilükkamise korral. Valikud on järgmised:

        - *Loo ainult töö* – varude liikumise lihtsustamiseks looge vaid töö.
        - *Loo kvaliteettellimus* – kvaliteedikatsete lihtsustamiseks saate luua kvaliteettellimuse.

    - **Katsegrupp:** *Raamistus*

        Määrake katsegrupp, mida tuleks loodud kvaliteettellimuses kasutada. Katsegrupid häälestatakse mooduli **Laohaldus**.

        Jätke katsegrupi jaoks suvand **Purustav katse** väljalülitatuks. See suvand määratleb, kas näidis tuleks katsegrupi katse osana hävitada. Purustava katse kasutamisel genereerib süsteem varude kande, kui kauba jaoks luuakse kvaliteettellimus. Uus laokanne prognoosib varude vähendamist testikoguse puhul. Varude vähendamine toimub, kui kvaliteettellimus viiakse lõpule kinnitamisetapi kaudu. Varude ülekanne tuvastatakse kvaliteettellimusena.

### <a name="work-class--quality-check"></a><a name="work-class"></a>Tööklass – kvaliteedikontroll

Tööklassidega suunatakse ja/või piiratakse töötellimuse ridade tüüpi, mida laotöötajad saavad mobiilses seadmes töödelda.

1. Minge jaotisse **Laohaldus \> Seadistus \> Töö \> Töö klassid**.
1. Valige tööklassi loomiseks **Uus**.
1. Määrake päises järgmised väärtused.

    - **Tööklassi ID:** *QC-kontroll*

        Sisestage tööklassi tuvastav nimi.

    - **Kirjeldus:** *QC-kontroll*

        Sisestage lühikirjeldus, mis näitab, milleks tööklassi kasutatakse.

    - **Töökäsu tüüp:** *Kvaliteet kvaliteedikontrollis*

        Valige tööklassi loodud töökäsu tüüp. Kui häälestate kvaliteedikontrolli töö, valige alati *Kvaliteet kvaliteedikontrollis*.

1. Jätke kiirkaardil **Ladustamise sobivad asukohatüübid** väli **Asukohatüüp** tühjaks.

    Kui valite asukohatüübi, piiritlete asukohad, kuhu kaupu saab ladustada pärast komplekteerimist. Seda välja kasutatakse, kui asukohakorraldus püüab asukohta lahendada või kui laotöötaja määrab mobiilse seadme menüü-üksuse jaoks asukoha käsitsi.

Lisateabe saamiseks tööklasside ja nende loomise kohta vt [Tööklassi loomine](tasks/create-work-class.md).

### <a name="work-template"></a>Töömall

Töömallid võimaldavad teil määratleda tööüksuse toimingud, mida tuleb laos teha. Tavaliselt koosnevad lao tööüksuse toimingud paarist tegevusest: laotöötaja komplekteerib ühes kohas vaba kaubavaru ja viib komplekteeritud kaubavarud teise kohta. Kvaliteedikontrolli töömall määratleb tööüksuse toimingud kvaliteedikontrolliks.

#### <a name="purchase-orders"></a>Ostutellimused

1. Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.
1. Seadke päises väli **Töökäsu tüüp** väärtusele *Ostutellimus*.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Valige töömall, mis peaks sisaldama kvaliteedikontrolli etappi. Valige jaotise **Ülevaade** väljal **Töömall** suvand *51 Ostutellimuse vastuvõtmine*.
1. Märkate, et jaotise **Töömalli üksikasjad** tabelis on kaks olemasolevat rida: üks tegevusele *Komplekteerimine* ja teine tegevusele *Ladustamine*.
1. Tehke jaotises **Töömalli üksikasjad** valik **Uus**, et lisada tabelisse kvaliteedikontrolli rida. Pange tähele, et uue rea välja **Reanumber** väärtuseks on määratud *3*.
1. Määrake uuel real järgmised väärtused. Võtke vastu ülejäänud väljade vaikeväärtused.

    - **Töö tüüp:** *Kvaliteedikontroll*
    - **Tööklassi ID:** *Ost*
    - **Kvaliteedikontrolli malli nimi:** *Laadimissilla kontroll*

        Valige tööklassi kordumatu kood. Selle väärtuse abil saate konfigureerida mobiilse seadme menüüelemente ja töö tüüpe, mida need menüüelemendid saavad töödelda.

1. Oma senise töö salvestamiseks valige tegevuspaanil **Salvesta**.

    Kuvatakse teade, mis ütleb: "Ei sobi – kvaliteedi kontroll peab toimuma kohe pärast komplekteerimist." Seetõttu peate muutma just lisatud rea **Reanumber** väärtust.

1. Uue rea **Reanumbri** väärtuse muutmiseks toimige järgmiselt.

    1. Valige jaotises **Töömalli üksikasjad** rida, milles välja **Töö tüüp** väärtuseks on määratud *Kvaliteedikontroll*.
    2. Valige nupud **Teisalda üles** või **Teisalda alla**, et viia rida *Kvaliteedikontroll* kohta, kus see asub pärast rida *Komplekteerimine*.

1. Valige toimingupaanil nupp **Salvesta**.

#### <a name="quality-in-quality-check"></a>Kvaliteet kvaliteedikontrollis

Järgmisena looge kvaliteedikontrolli jaoks töömall.

1. Muutke lehe **Töömallid** päises välja **Töökäsu tüüp** väärtuseks *Kvaliteet kvaliteedikontrollis*.
1. Valige tegevuspaanil suvand **Uus**, et lisada rida jaotise **Ülevaade** tabelisse.
1. Määrake uuel real järgmised väärtused.

    - **Töömall:** *51 Kvaliteedikontroll*

        Sisestage mallile nimi.

    - **Töömalli kirjeldus:** *51 Kvaliteedikontroll*

1. Valige tegevuspaanil **Salvesta**, et muuta jaotis **Töömalli üksikasjad** kättesaadavaks.
1. Kui jaotises **Ülevaade** on uus mall endiselt valitud, tehke jaotises **Töömalli üksikasjad** valik **Uus** ja lisage rida seal olevasse tabelisse.
1. Määrake uuel real järgmised väärtused.

    - **Töö tüüp:** *Komplekteerimine*
    - **Tööklassi ID:** *QC-kontroll*

        Valige varem kvaliteedikontrolli jaoks loodud [tööklassi](#work-class) nimi.

1. Muu rea tabelisse lisamiseks tehke jaotises **Töömalli üksikasjad** uuesti valik **Uus**.
1. Määrake uuel real järgmised väärtused.

    - **Töö tüüp:** *Ladustamine*
    - **Tööklassi ID:** *QC-kontroll*

        Valige varem kvaliteedikontrolli jaoks loodud [tööklassi](#work-class) nimi.

1. Valige toimingupaanil nupp **Salvesta**.

Töömallide kohta lisateabe saamiseks vt [Laotöö juhtimine töömallide ja asukohakorraldustega](control-warehouse-location-directives.md)

### <a name="location-directive--quality-failures"></a>Asukohakorraldus – kvaliteedivead

Asukoha korraldused on reeglid, mis aitavad tuvastada komplekteerimise ja mahapanemise asukohti varude liigutamisel. Näiteks määratleb asukohakorraldus müügitellimuse kandes koha, kus kaubad komplekteeritakse ja kuhu komplekteeritud kaubad maha pannakse. Peate konfigureerima asukohakorralduse reegli, et määratleda, kuidas nurjunud kvaliteedikontrolli käsitletakse.

1. Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.
1. Seda tüüpi asukohakorraldustega töötamiseks määrake vasakpoolsel paanil välja **Töökäsu tüüp** väärtuseks *Ostutellimused*.
1. Kvaliteedikontrollide asukohakorralduse loomiseks valige tegevuspaanil **Uus**.
1. Määrake päises järgmised väärtused.

    - **Järjekorranumber:** nõustuge vaikeväärtusega.
    - **Nimi:** *51 Kvaliteedikontrolli*

1. Määrake kiirkaardil **Asukohakorraldused** järgmised väärtused. Võtke vastu ülejäänud väljade vaikeväärtused.

    - **Töö tüüp:** *Ladustamine*
    - **Tegevuskoht:** *5*
    - **Ladu:** *51*

1. Korralduse salvestamiseks tegevuspaanil valige **Salvesta** ja muutke kiirkaart **Read** kättesaadavaks.
1. Valige kiirkaardil **Read** suvand **Uus**, et lisada rida ruudustikku.
1. Määrake uuel real järgmised väärtused. Võtke vastu ülejäänud väljade vaikeväärtused.

    - **Alates kogusest:** *1*
    - **Koguseni:** *1000000*

1. Uue rea salvestamiseks ja kiirkaardi **Asukohakorralduse tegevused** kättesaadavaks muutmiseks valige tegevuspaanil **Salvesta**.
1. Kui kiirkaardil **Read** on uus rida endiselt valitud, tehke kiirkaardil **Asukohakorralduse toimingud** valik **Uus** rea sinna lisamiseks tabelis, et saaksite rea jaoks tegevuse häälestada.
1. Uues reas määrake välja **Nimi** väärtuseks *Kvaliteet*. Võtke vastu ülejäänud väljade vaikeväärtused.
1. Valige tegevuspaanil **Salvesta**, et muuta kiirkaardi **Asukohakorralduse tegevused** nupp **Redigeeri päringut** kättesaadavaks.
1. Kui teie lisatud rida on kiirkaardil **Asukohakorralduse tegevused** endiselt valitud, valige käsk **Redigeeri päringut**, et avada dialoogiboks, kus saate redigeerida tegevuse päringut.
1. Vahekaardil **Vahemik** valige käsk **Lisa**, et lisada uus rida päringusse.
1. Määrake uuel real järgmised väärtused.

    - **Tabel:** *Asukohad*
    - **Tuletatud tabel:** *Asukohad*
    - **Väli:** *Asukoht*
    - **Kriteeriumid:** *QMS*

    *QMS*-i asukoht on kvaliteedi laoasukoht.

1. Valige dialoogiboksi sulgemiseks suvand **OK**.
1. Nüüd peate lao *51* jaoks muutma ostutellimuse asukohakorralduste järjestust. Salvestage uus asukohakorraldus *51 kvaliteedikontrolli*, värskendage lehte ja valige loendist asukohakorraldus. Seejärel kasutage lao *51* asukohakorralduse järgmisesse järjestusse panemiseks tegevuspaanil nuppe **Nihuta üles** ja **Nihuta alla**. (Enne kui valite **Nihuta üles** või **Nihuta alla**, peate loendis valima asukohakorralduse.)

    1. 51 Kvaliteedikontrolli
    2. 51 otse-PO
    3. 51 QMS

### <a name="mobile-device-menu-items"></a>Mobiilse seadme menüü-üksused

Konfigureerige menüü-üksus, et mobiilsetes seadmetes olek võimalik kasutada funktsiooni **Kvaliteedikontroll**.

#### <a name="purchase-putaway"></a>Ostu ladustamine

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.
1. Valige loendist menüü-üksus **Ostu ladustamine**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Rea tabelisse lisamiseks valige jaotisest **Tööklassid** suvand **Uus**.
1. Määrake uuel real järgmised väärtused.

    - **Tööklassi ID:** *QC-kontroll*

        Sisestage varem kvaliteedikontrolli jaoks loodud [tööklassi](#work-class) nimi.

    - **Töökäsu tüüp:** *Kvaliteet kvaliteedikontrollis*

1. Valige toimingupaanil nupp **Salvesta**.

#### <a name="purchase-order-line-receiving"></a>Vastuvõttev ostutellimuse rida

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.
1. Valige toimingupaanil nupp **Uus**.
1. Määrake päises järgmised väärtused.

    - **Menüü-üksuse nimi:** *Vastuvõttev ostutellimuse rida*
    - **Pealkiri:** *Vastuvõttev ostutellimuse rida*
    - **Režiim:** *töö*
    - **Kasuta olemasolevat tööd:** *Ei*

1. Määrake kiirkaardil **Üldine** järgmised väärtused. Võtke vastu ülejäänud väljade vaikeväärtused.

    - **Töö loomise protsess:** *Vastuvõttev ostutellimuse rida ja ladustamine*
    - **Loo litsentsiplaat:** *jah*
    - **Töömall:** *51 Ostutellimuse vastuvõtmine*

1. Valige toimingupaanil nupp **Salvesta**.

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Menüü-üksuse lisamine mobiilse seadme menüüsse

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü**.
1. Valige vasakul paanil menüü **Sissetulev**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Valige veerus **Saadaolevad menüüd ja menüü-üksused** uus menüü-üksus **Vastuvõttev ostutellimuse rida**.
1. Valige paremnoole nupp, et teisaldada **Vastuvõttev ostutellimuse rida** veergu **Menüü struktuur**.
1. Tehke veerus **Menüü struktuur** valik **Vastuvõttev ostutellimuse rida** ja seejärel valige menüü-üksuse soovitud kohta viimiseks mobiilse seadme menüüs üles- või allanoolenupp.
1. Valige toimingupaanil nupp **Salvesta**.

## <a name="example-scenario"></a><a name="example-scenario"></a>Näidisstsenaarium

Pärast seda, kui olete teinud kõik eelnevalt kirjeldatud näidisandmed kättesaadavaks ja need häälestanud, saate töötada selle stsenaariumi abil, et proovida funktsiooni *Kvaliteedikontroll*. Selles stsenaariumis kuvatavad väärtused eeldavad, et töötate standardsete demo andmetega, et valisite juriidilise isiku **USMF** ja olete ette valmistanud näidiskirjed, mida on selles teemas varem kirjeldatud. See stsenaarium toimib ka näitena selle kohta, kuidas seda funktsiooni saab tootmises kasutada.

### <a name="create-a-purchase-order"></a>Ostutellimuse loomine

1. Avage **Hanked \> Ostutellimused \> Kõik ostutellimused**.
1. Valige toimingupaanil nupp **Uus**.
1. Dialoogiboksis **Ostutellimuse loomine** määrake järgmised väärtused.

    - **Hankija konto:** *104*
    - **Ladu:** *51*

1. Dialoogiboksi sulgemiseks ja uue müügitellimuse loomiseks valige **OK**.
1. Kiirkaardil **Müügitellimuse read** sisaldab tabel uut, tühja rida. Määrake sellel real järgmised väärtused.

    - **Kauba kood:** *M9203*
    - **Kogus:** *3*
    - **Ühik:** *PL*

1. Valige toimingupaanil nupp **Salvesta**.

### <a name="process-quality-check-receiving"></a>Kvaliteedikontrolli vastuvõtmise töötlemine

Pärast ostutellimuse loomist saab selle vastu võtta, kasutades menüü-üksust **Vastuvõttev ostutellimuse rida** ja funktsiooni *Kvaliteedikontrolli* funktsionaalsust.

#### <a name="receive-pallet-1"></a>Kaubaaluse 1 vastuvõtmine

1. Logige laorakendusse sisse lao *51* kasutajana. (Sisestage *51* kasutaja ID-na ja *1* paroolina.)
1. Avage **Sissetulev \> Vastuvõttev ostutellimuse rida**.
1. Sisestage väljale **PONUM** ostutellimuse number.
1. Kinnitage ostutellimuse number.
1. Sisestage sissetuleva ostutellimuse rea number väljale **LINENUM**. Kuna tellimusel on selles stsenaariumis ainult üks rida, sisestate väljale **LINENUM** iga vastuvõtmisetapi jaoks *1*.
1. Kinnitage reanumber.
1. Sisestage vastuvõetav kogus väljale **Kogus**. Kuna selle stsenaariumi ostutellimuses on kolm kaubaalust (*PL*) ja vastuvõtu etappe on kolm, sisestate iga vastuvõtuetapi jaoks väljale **Kogus** numbri *1*.
1. Kinnitage kogus.

    Kuvataval lehel **Kvaliteedikontroll** pole sisestusvälju. Sellel on allosas ainult kinnituse (märge) nupp ja ülaosas menüünupp (**≡**). (Menüünupule on mõnikord viidatud ka kui hamburgerile või hamburgerinupule). Kvaliteedikontrolli protsessi kiirendamiseks, kui kaubaalus läbib kvaliteedikontrolli, kinnitab kasutaja vaid lehe **Kvaliteedikontroll**.

    ![Kvaliteedikontrolli leht](media/quality-check.png "Kvaliteedikontrolli leht")

1. Kaubaaluse 1 kvaliteedikontrolli läbimiseks valige kinnitusnupp realt 1.

    Kuvataval lehel **Ostutellimused: ladustamine** kuvatakse ladustamistöö üksikasjad.

    - **LOC:** Süsteemi määratud asukoht

        See asukoht on ostutellimuse jaoks määratud ladustamise asukoht.

    - **LP:** Süsteemi genereeritud loodud identifitseerimisnumbri ID
    - **Kaup:** *M9203*
    - **Kogus:** *1 PL: igat toodet 100*

    Kuvatakse ka kauba kirjeldus.

1. Kinnitage ladustamistöö.

    Vastuvõtva ostutellimuse rea lehele **Ülesanne** saate teate "Töö on lõpule viidud". Väli **LINENUM** on saadaval, et saaksite hakata vastu võtma järgmist kaubaalust.

#### <a name="receive-pallet-2"></a>Kaubaaluse 2 vastuvõtmine

Selles stsenaariumis lükatakse kaubaalus 2 tagasi.

1. Sisestage väljale **LINENUM** arv *1* ja kinnitage reanumber.
1. Väli **Kogus** on nüüd saadaval. Sisestage *1*ja kinnitage kogus.

    Kuvatakse leht **Kvaliteedikontroll**. Selle vastuvõtu puhul on kaubaaluse kvaliteet tagasi lükatud ja pannakse kvaliteediasukohta *QMS*.

1. Valige lehe ülaosas nupp Menüü (**≡**) ja seejärel valige menüüs **Lükka tagasi**.
1. Sisestage kuvatavale lehele **Ülesanne** suvand **QMS** asukohana *Ladusta*, et saate kaubaalus täiendavasse kontrolli.

    Kuvataval lehel **Kvaliteet kvaliteedikontrollis: ladustamine** kuvatakse ladustamistöö üksikasjad.

    - **LOC:** *QMS*

        See asukoht on tagasilükatud ostutellimuse vastuvõetava kauba kvaliteedi tagasilükkamise jaoks määratud ladustamise asukoht.

    - **LP:** Süsteemi genereeritud loodud identifitseerimisnumbri ID
    - **Kaup:** *M9203*
    - **Kogus:** *1 PL: igat toodet 100*

    Kuvatakse ka kauba kirjeldus.

1. Kinnitage ladustamistöö.

    Vastuvõtva ostutellimuse rea lehele **Ülesanne** saate teate "Töö on lõpule viidud". Väli **LINENUM** on saadaval, et saaksite hakata vastu võtma järgmist kaubaalust.

Olete nüüd kvaliteedikontrolli lõpule viinud ja loonud tagasilükatud kaubaaluse jaoks kvaliteettellimuse. Loodud tellimuse vaatamiseks avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Kvaliteettellimused**.

Nüüd saab töödelda kvaliteettellimust. See teema ei hõlma kvaliteedi testimist.

Lisateavet kvaliteedijuhtimise kohta vt [Kvaliteedijuhtimise ülevaade](../inventory/enable-quality-management.md)

#### <a name="receive-pallet-3"></a>Kaubaaluse 3 vastuvõtmine

Selle stsenaariumi võetakse kaubaalus 3 vastu.

1. Sisestage väljale **LINENUM** arv *1* ja kinnitage reanumber.
1. Väli **Kogus** on nüüd saadaval. Sisestage *1*ja kinnitage kogus.

    Kuvatakse leht **Kvaliteedikontroll**. Selle kviitungi puhul on kaubaaluse kvaliteet vastu võetud ja see pannakse ladustamise hulgiasukohta.

1. Kvaliteedikontrolli läbimiseks valige kinnitusnupp.

    Kuvataval lehel **Ostutellimused: ladustamine** kuvatakse ladustamistöö üksikasjad.

    - **LOC:** Süsteemi määratud asukoht

        See asukoht on ostutellimuse jaoks määratud ladustamise asukoht.

    - **LP:** Süsteemi genereeritud loodud identifitseerimisnumbri ID
    - **Kaup:** *M9203*
    - **Kogus:** *1 PL: igat toodet 100*

    Kuvatakse ka kauba kirjeldus.

1. Kinnitage ladustamistöö.

    Vastuvõtva ostutellimuse rea lehele **Ülesanne** saate teate "Töö on lõpule viidud". Väli **LINENUM** on saadaval, et saaksite hakata vastu võtma järgmist kaubaalust.

1. Valige lehe ülaosas nupp Menüü (**≡**) ja seejärel tehke menüüsse naasmiseks valik **Tühista**.

Nüüd saate mobiilirakenduse sulgeda.
