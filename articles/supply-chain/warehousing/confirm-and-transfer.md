---
title: Kinnitamine ja üleviimine
description: Selles teemas selgitatakse, kuidas kasutada funktsiooni Kinnitamine ja üleviimine, mis võimaldab kasutajatel koormusi laost välja saata enne, kui nad viivad lõpule kogu nende koormustega seotud töö.
author: mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTemplate,WHSWorkTemplateTable,WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 70ebe47997f3b5945a433150ae66de6eb41ff12acf4f4f3c8268351116bdd313
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767947"
---
# <a name="confirm-and-transfer"></a>Kinnitamine ja üleviimine

[!include [banner](../includes/banner.md)]

Funktsioon *Kinnitamine ja üleviimine* võimaldab kasutajatel koormusi laost välja saata enne, kui nad viivad lõpule kogu nende koormustega seotud töö. Kui võetakse vastu saadetis, mis sisaldab täielikult komplekteerimata koormaridu, küsitakse kinnitavalt kasutajalt kas tükeldada järelejäänud kogused uude koormusesse või tühistada tühistada kogused.

Süsteemid, mis on seadistatud lubama koormuse tükeldamise stsenaariumide toetamist, kus plaanitud ja osaliselt koormatud koormuseid tuleb kohandada uute või muutuvate asjaolude tõttu.

Klient sisaldab loogikat, mis võimaldab osaliselt koormatud koormuseid sulgeda ja kinnitada saadetuna. Kõik järelejäänud saadetised ja koormuse read (kaasa arvatud täielikud või osalised reakogused) viiakse seejärel üle uuele loodud koormusele ja saadetisele, kui see on nõutav ja seadistus lubab seda. Uued saadetised ja koormused luuakse automaatselt saadetise ja koormuse loomise esialgsete kriteeriumide põhjal ja nende põhiatribuudid jäävad muutumatuks. Samuti on olemas võimalus tühistada järelejäänud kogused automaatselt, kui töökäsku pole veel loodud ja kasutaja peab seda tühistamist vajalikuks.

See funktsioon toetab stsenaariume, kus täiskoormus ei mahu ühele veokile või kus osa koormusest peaks laost lahkuma enne, kui ülejäänud koorem on saatmiseks valmis. Nende stsenaariumide puhul saab järelejäänud tooteid üle kanda uude koormusesse ja seega uuele veokile. Kuna seda funktsiooni saab kasutada koormustega, mis on muidu mõeldud täieliku koormuse saatmiseks, annab see lisapaindlikkust, et veoettevõtjad saaksid lahendada mittestandardseid või ettenägematuid stsenaariume.

Koormuse tükeldamisel teostab funktsioon *Kinnitamine ja üleviimine* järgmised toimingud.

- Uued koormused ja saadetised luuakse vastavalt vajadusele. Igal koormuse või saadetise atribuudid on esialgse koormuse või saadetisega enamjaolt samad. Erandiks on koormuse olek, mis arvutatakse ümber töö oleku alusel.
- Kasutajat teavitatakse, et on loodud uus koormus. Kasutajat teavitatakse ka uue koormuse ID-ist.
- Tükeldatud koormusread, tööpäised ja tööread uuendatakse uue koormuse ja saadetise teabega.
- Kui kogu saadetis tükeldatakse, säilitatakse saadetis ja uuendatakse ainult koormuse viiteid. Kui saadetist tuleb tükeldada, luuakse uus saadetis.

Kui järelejäänud kogused tühistatakse, eemaldatakse koormusest kõik koormusrea kogused, mida pole komplekteeritud ja millega pole seostatud tühistamata tööd. Kui töö on käimas, saab kasutaja tükeldada ainult koormust. Järelejäänud koguseid ei saa tühistada.

Saate tükeldada ainult järgmistele kriteeriumidele vastavaid koormuseid.

- Ühel või mitmel koormusreal on komplekteeritud koguseid.
- Koormuse olek on vähem kui koormatud.
- Koormusrea andmeid pole. (Need andmed luuakse identifitseerimisnumbri konsolideerimise abil vaheasukohas ja funktsioon *Kinnitamine ja üleviimine* ei toeta identifitseerimisnumbri konsolideerimist.)
- Komplekteerimisasukohas ei ole praegu komplekteerimise ootel varusid. (Funktsioon *Kinnitamine ja üleviimine* ei toeta varusid, mis on komplekteeritud pakkimisjaama, kuid pole veel pakitud.)

> [!NOTE]
> See funktsioon erineb transpordi koormuse funktsioonist, mida tuleks kasutada ladudes, mis ei saa kunagi planeerida ja luua koormusi enne komplekteerimist, vaid koormab saadaoleva transpordiala pärast komplekteerimise lõpuleviimist.
>
> Kasutage funktsiooni *Kinnitamine ja üleviimine* olukordades, kus koormuseid planeeritakse ja luuakse tavaliselt ette ja, kuid kus võib vahel ilmneda erandeid, mille puhul koormus ei mahu saadaolevasse transpordivahendisse (nt veokisse).

## <a name="turn-on-confirm-and-transfer"></a>Kinnitamise ja üleviimise sisselülitamine

Enne funktsiooni *Kinnitamine ja üleviimine* kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Kinnitamine ja üleviimine*

## <a name="set-up-confirm-and-transfer"></a>Kinnitamise ja üleviimise häälestamine

Funktsiooni *Kinnitamine ja üleviimine* kasutamiseks, peate selle sisse lülitama igas asjakohases koormusmallis. Lisaks võite funktsiooni toetamiseks valmistada ette töömallid vastavalt vajadusele. Kui soovite töötada läbi hiljem selles teemas käsitletava näidisstsenaariumi, seadistage oma süsteem selles jaotises kirjeldatud viisil. (See stsenaarium põhineb demoandmetel **USMF**.)

### <a name="prepare-your-load-templates"></a>Koormusmallide ettevalmistamine

1. Avage jaotis **Laohaldus \> Seadistus \> Koormus \> Koormusmallid**.
1. Lehe redigeerimisrežiimi panemiseks valige toimingupaanil **Redigeeri**.
1. Märkige ruut **Luba koormuse tükeldamine saatmise kinnitamisel** igas olemasolevas mallis, millele soovite funktsiooni sisse lülitada. Võite ka valida suvandi **Uus**, et luua uus mall ja konfigureerida seda vastavalt vajadusele. Iga selle malli abil loodav koormus pärib selle funktsiooni. (Kui töötate demoandmetega **USMF**, lülitage see funktsioon sisse koormusmalli **20 konteiner** jaoks.)

### <a name="prepare-your-work-templates"></a>Töömallide ettevalmistamine

See seadistus pole nõutav kõigis olukordades. Siin kuvatud näide tagab, et tööd saab tükeldada saadetisega, et toetada selles teemas hiljem kirjeldatud stsenaariumi. Selle tulemuse saavutamiseks on ka muid võimalusi.

1. Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.
1. Valige lehe ülemises osas olevas ruudustikus olemasolev töömall, kuhu soovite seadistada funktsiooni *Kinnitamine ja üleviimine*. (Kui töötate demoandmetega **USMF**, valige töömall **51 Ettevalmistamiseks komplekteerimine**.) Teise võimalusena saate luua uue töömalli.
1. Valige toimingupaanil suvand **Redigeeri päringut**, et avada dialoogiboks **Müük**.
1. Valige dialoogiboksis **Müük** vahekaardil **Sortimine** suvand **Lisa**, et lisada rida ruudustikule.
1. Määrake uuel real järgmised väärtused.

    - **Tabel:** *Ajutised töökanded*
    - **Tuletatud tabel:** *Ajutised töökanded*
    - **Väli:** *Saadetise ID*
    - **Otsingusuund:** *Kasvav*

1. Valige **OK**, et salvestada oma sätted ja sulgeda dialoogiboks **Müük**.
1. Kui kuvatakse teade, mis ütleb, et grupeerimine lähtestatakse, valige jätkamiseks **Jah**.
1. Valige lehe **Töömallid** ülaosas olevast ruudustikust äsja redigeeritud mall ja seejärel valige toimingupaanil **Tööpäise piir**.
1. Lehe redigeerimisrežiimi panemiseks valige toimingupaanil **Redigeeri**.
1. Määrake ruudustikus järgmised väärtused.

    - **Tabeli nimi:** *Ajutised töökanded*
    - **Välja nimi:** *Saadetise ID*
    - **Grupeeri selle välja alusel:** märkige see ruut.

1. Valige toimingupaanil nupp **Salvesta**.
1. Sulgege leht.

## <a name="scenario"></a>Stsenaarium

Selles stsenaariumis kuvatakse näide, kus komplekteerimisprotsess ei ole veel lõpule viidud, kuid senimaani komplekteeritud kaubad tuleb ikkagi laadida veokile ja saata. Seega kasutaja saab tükeldada komplekteerimata koormusread uude koormusesse. Seejärel värskendatakse kõik andmeseosed automaatselt.

> [!NOTE]
> Selles stsenaariumis kirjeldatud kindlad väärtused põhinevad demoandmetel **USMF**. Soovitame kasutada neid demoandmeid, kui õpetate või õpite seda funktsiooni kasutama. Kui te ei kasuta demoandmeid **USMF**, asendage oma väärtused vastavalt vajadusele.

### <a name="step-1-create-a-load-that-has-multiple-load-lines"></a>1. etapp: looge koormus, millel on mitu koormusrida

Enne selle funktsiooni kasutamist peab teil olema koormus, mis sisaldab mitut koormrida. Samuti peate veenduma, et komplekteerimise asukohtadel on kõikide loodavate tellimuste kõigi üksuste jaoks piisavalt varusid. Vaadake üle asukohakorralduse seadistus (**Laohaldus \> Häälestus \> Asukohakorraldused**) ja märkige üles müügitellimuste komplekteerimiseks kasutatavad komplekteerimise asukohad. Kui peate korrigeerima varusid, looge käsitsi liikumisi, kasutada täiendamist või kasutage mis tahes muud voogu vastavalt vajadusele.

Sobiva koormuse loomiseks looge esmalt kolm müügitellimust, järgides neid etappe.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Valige toimingupaanil **Uus**, et avada dialoogiboks **Müügitellimuse loomine**.
1. Määrake dialoogiboksis **Müügitellimuse loomine** (vähemalt) järgmised väärtused.

    - Määrake kiirkaardi **Klient** välja **Kliendi konto** väärtuseks *US-004* (*Cave Wholesales*).
    - Määrake kiirkaardi **Üldine** välja **Ladu** väärtuseks *51*.

1. Valige müügitellimuse loomiseks **OK** ja sulgege dialoogiboks **Müügitellimuse loomine**.
1. Teie uus müügitellimus on avatud. Lisage ruudustikku **Müügitellimuse read** järgmiste väärtustega rida.

    - **Kauba kood:** *M9200*
    - **Kogus:** *40*
    - **Ühik:** *ea*

1. Valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.
1. Valige toimingupaanl **Reserveerimine** lehe **Reserveerimine** avamiseks.
1. Reserveerige varude müügirida ja seejärel sulgege leht **Reserveerimine**.
1. Korrake etappe 1–4 samale kliendile ja laole teise müügitellimuse lisamiseks.
1. Lisage kaks müügirida, millel on järgmised väärtused. Pärast iga rea lisamist reserveerige selle jaoks varud etappides 6–8 kirjeldatud juhiste järgi.

    - **Rida 1:** määrake välja **Kaubakood** väärtuseks *M9200*, välja **Kogus** väärtuseks *30* ja välja **Ühik** väärtuseks *ea*.
    - **Rida 2:** määrake välja **Kaubakood** väärtuseks *M9201*, välja **Kogus** väärtuseks *20* ja välja **Ühik** väärtuseks *ea*.

1. Korrake etappe 1–4 samale kliendile ja laole kolmanda müügitellimuse lisamiseks.
1. Lisage kaks müügirida, millel on järgmised väärtused. Pärast iga rea lisamist reserveerige selle jaoks varud etappides 6–8 kirjeldatud juhiste järgi.

    - **Rida 1:** määrake välja **Kaubakood** väärtuseks *M9201*, välja **Kogus** väärtuseks *20* ja välja **Ühik** väärtuseks *ea*.
    - **Rida 2:** määrake välja **Kaubakood** väärtuseks *M9202*, välja **Kogus** väärtuseks *60* ja välja **Ühik** väärtuseks *ea*.

#### <a name="load-planning-workbench"></a>Koorma planeerimise töölaud

Koormuse planeerimise töölaud kasutab saadetiste loomiseks koormusmalli ID-d ja vabastab müügitellimuse read lattu.

1. Avage **Laohaldus \> Koormused \> Koormuse plaanimise töölaud**.
1. Valige väljal **Ladu** väärtus *51*.

    Nüüd saate luua äsja loodud müügitellimustele koormuse.

1. Valige ruudustiku vahekaardil **Müügiread** müügiread uute müügitellimuste jaoks.
1. Valige toimingupaani vahekaardi **Pakkumine ja nõudlus** grupis **Lisa** suvand **Uuele koormusele**.
1. Valige dialoogiboksi **Koorma malli määramine** väljal **Koorma malli ID** suvand *20' konteiner*.
1. Valige nupp **OK**.
1. Otsige lehe **Koorma planeerimise töölaud** jaotise **Koormused** ruudustikust üles lao *51* jaoks äsja loodud koormuse ID. Kerige paremale, kuni kuvatakse veerg **Luba koormuse tükeldamine saadetise kinnitamisel**. Teie koormuse jaoks tuleb valida see märkeruut.
1. Valige koormus.
1. Töö loomiseks valige ruudustiku kohal menüüs **Vabastamine** suvand **Lattu vabastamine**.
1. Kinnitage, et dialoogiboksis **Koormuse vaastamine lattu** kuvatakse kiirkaardil **Kaasatavad kirjed** teie koormuse ID-d.
1. Valige nupp **OK**.

    Teile võidakse kuvada teade „Töötlemise toiming”, kui süsteem loob saadetised ja töö.

1. Lehe **Koorma planeerimise töölaud** jaotises **Koormused** peaks nüüd olema kuvatud koormuse olek *Voog moodustatud*. Valige koormus ja seejärel valige ruudustiku kohal olevas menüüs **Seotud teave** suvand **Voo üksikasjad**, et vaadata loodud saadetise ID-sid. Kui olete lõpetanud, sulgege leht **Vood**.
1. Valige lehe **Koorma planeerimise töölaud** jaotisest **Koormused** koormus ja seejärel valige ruudustiku kohal olevast menüüst **Seotud teave** suvand **Töö üksikasjad**, et vaadata müügitellimuste jaoks loodud tööd.
1. Märkige üles loodud töö ID-d. Peate tõenäoliselt kerima paremale, et näha müügitellimuse numbrit ja saadetise ID-d, mis on seostatud töö ID-ga.

### <a name="step-2-set-up-the-execution-flow-for-mobile-devices"></a>2. etapp: seadistage mobiilsete seadmete käivitamise voog

Mobiilse seadme ülesanded nõuavad kasutaja andmete sisestamist, nt töö ID või identifitseerimisnumbri ID. Tavaliselt edastatakse nende väljade teave lao kasutajatele vöötkoodide vormis, mille võib leida dokumentidest, pakenditelt või riiulitest. Stsenaariumide jaoks mobiilse seadme etappide lõpuleviimiseks veenduge, et olete tuvastanud kannete töö ID-d ja kandes oleva kauba ja asukoha idnentifitseerimisnumbri ID-d.

1. Logige mobiilsesse seadmesse sisse, kasutades kasutaja ID-d ja parooli lao *51* jaoks.
1. Valige **Väljaminev**.
1. Valige **Müügi komplekteerimine**.
1. Teil on võimalus sisestada töö ID või identifitseerimisnumbri ID. Sisestage esimese müügitellimuse töö ID ja seejärel valige käsk **Sisesta**.
1. Sisestage väljale **Loc** asukoht, mis kinnitab komplekteerimiskohta. Seejärel valige **Sisesta**.
1. Sisestage väljale **LP** identifitseerimisnumbri ID. Identifitseerimisnumbri ID peab vastama kaubale, laole ja asukohale valitud asukohas komplekteeritud kauba jaoks. Kui olete lõpetanud, valige **Sisesta**.
1. Sisestage väljale **Kaup** komplekteeritava kauba kinnitamiseks kaubakood ja seejärel valige **Sisesta**.
1. Sisestage väljale **Kogus** komplekteeritava kauba kogus ja seejärel valige **Sisesta**.
1. Sisestage väljale **Siht-LP** sihtidentifitseerimisnumbri ID. Sihtidentifitseerimisnumbri määratleb kasutaja. Sisestage kindlasti identifitseerimisnumbri ID, mida te mäletate. Soovitame kasutada praegust kuupäeva koos kahekohalise seeriaga (AAKKPP\#\#) nagu see vorming, nt *19112301*. Kui olete lõpetanud, valige **Sisesta**.
1. Vaadake üle kuvatav teave. See teave on *Komplekteerimise* teave, millest saavad nüüd *Ootele pandud* andmed ootele pandud kande jaoks. Kui olete lõpetanud, valige **Sisesta**.

    - Teile kuvatakse teade **Töö lõpule viidud**.

1. Korrake etappe 4–10 teise müügitellimuse töö ID jaoks.

Järgmine etapp on kahe komplekteeritud identifitseerimisnumbri laadimine veokile.

1. Logige mobiilsesse seadmesse sisse, kasutades kasutaja ID-d ja parooli lao *51* jaoks.
1. Valige **Väljaminev**.
1. Valige **Müügi laadimine**.
1. Sisestage kasutaja määratletud sihtidentifitseerimisnumbri ID, mille lõite eelmises protseduuris esimese töö ID jaoks. Seejärel valige **Sisesta**, et panna sihtkoha identifitseerimisnumber asukohta **ETAPP**.
1. Sisestage sihtidentifitseerimisnumbri ID uuesti ja seejärel valige **Sisesta**, et panna identifitseerimisnumber asukohta **BAYDOOR**.
1. Korrake etappe 4–5 selle sihtidentifitseerimisnumbri ID jaoks, mille lõite teise töö ID jaoks.

Kaks töö ID-d on nüüd suletud (laaditud).

### <a name="step-3-confirm-the-outbound-shipment"></a>3. etapp: kinnitage väljaminev saadetis

Selles etapis kinnitate kaks müügitellimust ja tööd, mis on selle koormuse jaoks lõpetatud, et saata koormuse komplekteeritud kaubad ja luua uus koormus komplekteerimata kaupadele. Väljamineva saadetise kinnitus tuleb teha lehel **Koormuse üksikasjad**.

1. Avage **Laohaldus \> Koormused \> Koormuse plaanimise töölaud**.
1. Valige ruudustiku jaotises **Koormused** enda loodud koormuse ID rida.
1. Valige koormuse ID link, et avada leht **Koormuse üksikasjad**.
1. Kinnituse alustamiseks valige lehe **Koormuse üksikasjad** toimingupaani vahekaardi **Saatmine ja vastuvõtmine** grupis **Kinnitamine** suvand **Väljaminev saadetis**.
1. Valige dialoogiboksi **Saadetise kinnitamine** väljal **Koormuse tükeldamise meetod saadetise kinnitamisel** suvand *Tükelda kogus uude koormusesse*.
1. Valige nupp **OK**.

    Teile võidakse kuvada teade „Töötlemise toiming”.

    Saate teateid, mis näitavad, et koormuse saadetis on kinnitatud ja tükeldatud kogusest on loodud uus koormus.

Uute loodud koormuste kuvamiseks värskendage lehte **Koorma planeerimine**.

Samuti saate kinnitada, et kannete seoseid on uuendatud järgmistel viisidel.

- Järelejäänud (töötlemata) saadetist ja saadetise ridu värskendatakse uue koormuse ID-ga.
- Müügitellimus lingitakse uue koormuse ID-ga.
- Algne koormus ei sisalda järelejäänud koormuseridu.
- Järelejäänud tööd on uuendatud uue koormuse ID-ga.
- Voog jääb samaks.
- Uue koormuse olek on õigesti värskendatud. (Kui töö olek on _Töötlemisel_, peaks ka koormuse olek olema _Töötlemisel_ .)

## <a name="notes-and-tips"></a>Märkmed ja näpunäited

- Saate sisse lülitada ka parameetri **Luba koormuse tükeldamine saadetise kinnitamise ajal** pärast seda, kui parameeter **Koormuse mall** on välja lülitatud, kuid enne laadimise protsessi alustamist. Liikuge soovitud koormuse juurde ja seejärel lülitage parameetersisse päise vaates.
- Suvand **Tükelda kogus uude koormusesse** toimib ka siis, kui osade järelejäänud tööpäiste oleksuks on *Töötlemisel*. Seega saate funktsiooni kasutada ka siis, kui töötajad juba käitavad tellimuste komplekteerimist.
- Kui valite **Tühista täitmata kogus** samal ajal, kui on järelejäänud töid, mille olek on *Avatud* või *Käimas*, kuvatakse järgmine tõrketeade: „Koormuse järelejäänud kogust ei saa tühistada. Koormusel on olemasolev töö.”
- Kui valite **Tühista täitmata kogus**, kui ei ole järelejäänud töid, kuid koormusel on vabastamata koormuseridu, kuvatakse järgmine tõrketeade: „Koormuse saadetist ei saanud kinnitada, kuna kauba kogus ületab tarnimiseks määratletud protsendimäära.” Tõrke vältimiseks saate määrata vabastamata koormuserea **Alatarne** protsendiks 100. Vabastamata ridu ei teisaldata uude koormusesse, kuid praegune koormus kinnitatakse alatarnega. Sel juhul ei saa te algset tellimust uuesti vabastada. Seetõttu tuleb teil seda mõnel muul viisil käsitleda.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]