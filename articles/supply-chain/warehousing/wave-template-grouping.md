---
title: Voomalli rühmitamine
description: Voomalli rühmitamine võimaldab süsteemil kasutada voomalli seadistusi, et määrata teie määratletud kriteeriumide põhjal, kuidas see peaks tükeldama väljastatud ridu ja määrama neid uutele või olemasolevatele voogudele. Sellest funktsioonist võib olla kasu ladudes, kus voogusid luuakse kindlate kriteeriumide põhjal, kuid kus juhid eelistavad käsitsi loomise asemel luua voogusid automaatselt.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: b265c0d5cb43e151386fe90e3a3dea414ec0aca6
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579900"
---
# <a name="wave-template-grouping"></a>Voomalli rühmitamine

[!include [banner](../includes/banner.md)]

Voomalli rühmitamine võimaldab süsteemil kasutada [voomalli seadistusi](tasks/configure-wave-processing.md), et määrata teie määratletud kriteeriumide põhjal, kuidas see peaks tükeldama väljastatud ridu ja määrama neid uutele või olemasolevatele voogudele. Sellest funktsioonist võib olla kasu ladudes, kus voogusid luuakse kindlate kriteeriumide põhjal, kuid kus juhid eelistavad käsitsi loomise asemel luua voogusid automaatselt. See võimaldab süsteemil lisada iga äsja väljastatud saadetise esimesele leitavale voole, millel on samad rühmitamise välja väärtused. Kui vastet ei leita, loob süsteem uue saadetise jaoks uue voo.

> [!IMPORTANT]
> Voomalli rühmitamine pole toetatud töötüüpide *töömaterjalide komplekteerimine* või *kanbani komplekteerimine* jaoks. See on seetõttu, et voo rühmitamine põhineb saadetistel ja need töötüübid ei kasuta saadetisi.

## <a name="turn-on-the-wave-template-grouping-feature"></a>Voomalli rühmitamise funktsiooni sisselülitamine

Enne funktsiooni *Voomalli rühmitamine* kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Voomalli rühmitamine*

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a>Voomalli määramine voomalli rühmitamise kasutamiseks

Voomalli rühmitamise kättesaadavaks tegemiseks järgige neid etappe oma [voomalli](tasks/configure-wave-processing.md) seadistamiseks.

1. Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.
1. Valige vasakus paanis seadistatav voomall. Kui valmistute seda stsenaariumit demoandmete abil läbi töötama selles teemas hiljem, valige mall **62 saadetise vaikemall**.
1. Lehe redigeerimisrežiimi panemiseks valige **Redigeeri**.
1. Määrake kiirkaardil **Üldine** järgmised väärtused.

    - **Automatiseeri voo loomine:** *Jah*
    - **Määra avatud voogudele:** *Jah*
    - **Töötle voogu lattu vabastamisel:** *Ei*

1. Valige toimingupaanil suvand **Redigeeri päringut**, et avada dialoogiboks.
1. Vaadake üle päringu dialoogiboksi vahekaardil **Sortimine** sortimise kriteeriumid ja veenduge, et oleks olemas reegel, mis sisaldab välja, mida soovite kasutada oma voogude rühmitamiseks.

    Kui valmistute seda stsenaariumit demoandmete abil läbi töötama, lisage rida, millel on järgmised väärtused.

    - **Tabel:** *Saadetised*
    - **Tuletatud tabel:** *Saadetised*
    - **Väli:** *Vedaja teenus*

        > [!NOTE]
        > Kui valite selle väärtuse, võidakse kuvada järgmine teade: „Väli Vedaja teenus pole indeksi väli. Kas soovite lisada sellele sortimise?” Sortimise lisamiseks valige **Jah**.

    - **Otsingusuund:** *Kasvav*

1. Oma muudatuste salvestamiseks ja päringu dialoogiboksi sulgemiseks valige **OK**.
1. Valige toimingupaanil **Voomalli rühmitamine**.
1. Vastavalt vajadusele, valige lehel **Voomalli rühmitamine** märkeruut **Grupeerimisalus** iga rea puhul, mida soovite kasutada tellimuseridade voogudeks rühmitamiseks. Kui valmistute seda stsenaariumit demoandmete abil läbi töötama, märkige ruut **Grupeerimisalus** rea *Vedaja teenus* jaoks.
1. Valige käsk **Salvesta**.
1. Sulgege leht **Voomalli rühmitamine**.
1. Oma malli salvestamiseks valige **Salvesta**.

## <a name="scenario"></a>Stsenaarium

Selles jaotises antakse skript, mille läbi töötamisel saate teada, mida see funktsioon teeb ja kuidas sellega töötada.

### <a name="make-sample-data-available"></a>Näidisandmete kättesaadavaks tegemine

Selle stsenaariumi kasutamiseks siin määratud näidiskirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Enne alustamist peate valima ka juriidilise isiku **USMF**.

Seda stsenaariumi saate kasutada ka juhistena funktsiooni kasutamiseks, kui töötate tootmissüsteemis. Kuid sellisel juhul peate asendama oma väärtused ja teil ei pruugi olla teatud tüüpi nõutavaid kirjeid, mida pakuvad standardsed demoandmed.

### <a name="scenario-wave-template-grouping"></a>Stsenaarium: Voomalli rühmitamine

Selles stsenaariumis kirjeldatakse, kuidas kasutada voomalli rühmitamist mitme voo automaatseks loomiseks voomallis määratletud rühmitamiskriteeriumi põhjal. Selles stsenaariumis seadistatakse voomall süsteemis, et luua üks voog vedaja teenuse kohta.

Enne alustamist valmistage voomall ette selles teemas eelnevalt kirjeldatud jaotises [Voomalli määramine voomalli rühmitamise kasutamiseks](#set-up-template) olevate juhiste põhjal. Kui te töötate demoandmetega selles stsenaariumis, kasutage kindlasti demoandmete väärtusi, mida selles protseduuris soovitatakse. See seadistus rühmitab teie vood vastavalt vedaja teenusele, mis määratakse iga müügitellimuse jaoks.

#### <a name="create-sales-order-1"></a>Müügitellimuse 1 loomine

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Müügitellimuse loomiseks valige **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - Määrake kiirkaardi **Klient** välja **Kliendi konto** väärtuseks *US-004*.
    - Määrake kiirkaardi **Üldine** välja **Ladu** väärtuseks *62*.

1. Valige müügitellimuse loomiseks **OK** ja sulgege dialoogiboks **Müügitellimuse loomine**.
1. Uus müügitellimus avatakse vaates **Read**. Märkige üles müügitellimuse number.
1. Lülituge vaatele **Päis**.
1. Määrake kiirkaardi **Tarne** jaotises **Transport** järgmised väärtused.

    - **Vedaja:** *Kaubalennuk*
    - **Vedaja teenus:** *Õhk*

1. Minge tagasi vaatesse **Read**.
1. Valige jaotises **Müügitellimuse read** suvand **Lisa rida**, et lisada rida ruudustikule.
1. Määrake uuel real järgmised väärtused.

    - **Kauba kood:** *A0002*
    - **Kogus:** *2*

1. Valige uus tellimuserida ja seejärel valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.
1. Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida laos kogu valitud rea kogus.
1. Müügitellimuse juurde naasmiseks sulgege leht **Reserveerimine**.
1. Tehke tegevuspaani vahekaardil **Ladu** grupis **Tegevused** valik **Vabasta lattu**.
1. Saate teate, mis näitab saadetist ja voogu selle tellimuse jaoks. Märkige üles voo ID-kood ja saadetise ID-koodid.

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a>Müügitellimuse 1 jaoks loodud voo kuvamine

1. Avage **Laohaldus \> Väljaminevad vood \> Saadetise vood \> Kõik vood**.
1. Valige voo ID, mis loodi müügitellimusest.
1. Valige voo ID link, et avada voo üksikasjade leht.
1. Pange tähele, et saadetis on lisatud kiirkaardile **Voo read**.

#### <a name="create-sales-order-2"></a>Müügitellimuse 2 loomine

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Müügitellimuse loomiseks valige **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - Määrake kiirkaardi **Klient** välja **Kliendi konto** väärtuseks *US-005*.
    - Määrake kiirkaardi **Üldine** välja **Ladu** väärtuseks *62*.

1. Valige müügitellimuse loomiseks **OK** ja sulgege dialoogiboks **Müügitellimuse loomine**.
1. Uus müügitellimus avatakse vaates **Read**. Märkige üles müügitellimuse number.
1. Lülituge vaatele **Päis**.
1. Määrake kiirkaardi **Tarne** jaotises **Transport** järgmised väärtused.

    - **Vedaja:** *Voogude liigutamine*
    - **Vedaja teenus:** *Std*

1. Minge tagasi vaatesse **Read**.
1. Valige jaotises **Müügitellimuse read** suvand **Lisa rida**, et lisada rida ruudustikule.
1. Määrake uuel real järgmised väärtused.

    - **Kauba kood:** *A0001*
    - **Kogus:** *1*

1. Valige uus tellimuserida ja seejärel valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.
1. Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida laos kogu valitud rea kogus.
1. Müügitellimuse juurde naasmiseks sulgege leht **Reserveerimine**.
1. Tehke tegevuspaani vahekaardil **Ladu** grupis **Tegevused** valik **Vabasta lattu**.
1. Saate teate, mis näitab saadetist ja voogu selle tellimuse jaoks. Märkige üles voo ID-kood ja saadetise ID-koodid. Pange tähele, et voo ID erineb esimese müügitellimuse voo ID-st.

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a>Müügitellimuse 2 jaoks loodud voo kuvamine

1. Avage **Laohaldus \> Väljaminevad vood \> Saadetise vood \> Kõik vood**.
1. Valige voo ID, mis loodi teisest müügitellimusest.
1. Valige voo ID link, et avada voo üksikasjade leht.
1. Pange tähele, et saadetis on lisatud kiirkaardile **Voo read**.

Selle saadetise jaoks loodi uus voog, kuna see kasutab esimesest müügitellimusest erinevat vedaja teenust.

#### <a name="create-sales-order-3"></a>Müügitellimuse 3 loomine

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Müügitellimuse loomiseks valige **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - Määrake kiirkaardi **Klient** välja **Kliendi konto** väärtuseks *US-006*.
    - Määrake kiirkaardi **Üldine** välja **Ladu** väärtuseks *62*.

1. Valige müügitellimuse loomiseks **OK** ja sulgege dialoogiboks **Müügitellimuse loomine**.
1. Uus müügitellimus avatakse vaates **Read**. Märkige üles müügitellimuse number.
1. Lülituge vaatele **Päis**.
1. Määrake kiirkaardi **Tarne** jaotises **Transport** järgmised väärtused.

    - **Vedaja:** *Kaubalennuk*
    - **Vedaja teenus:** *Õhk*

1. Minge tagasi vaatesse **Read**.
1. Valige jaotises **Müügitellimuse read** suvand **Lisa rida**, et lisada rida ruudustikule.
1. Määrake uuel real järgmised väärtused.

    - **Kauba kood:** *A0001*
    - **Kogus:** *1*

1. Valige uus tellimuserida ja seejärel valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.
1. Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida laos kogu valitud rea kogus.
1. Müügitellimuse juurde naasmiseks sulgege leht **Reserveerimine**.
1. Tehke tegevuspaani vahekaardil **Ladu** grupis **Tegevused** valik **Vabasta lattu**.
1. Saate teate, mis näitab saadetist ja voogu selle tellimuse jaoks. Märkige üles voo ID-kood ja saadetise ID-koodid. Saadetis määrati olemasolevale voole esimesest müügitellimusest.

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a>Müügitellimuste 1 ja 3 voo kuvamine

1. Avage **Laohaldus \> Väljaminevad vood \> Saadetise vood \> Kõik vood**.
1. Valige voo ID, mis loodi kolmandast müügitellimusest.
1. Valige voo ID link, et avada voo üksikasjade leht.
1. Pange tähele, et saadetis lisati kiirkaardile **Voo read** koos esimese müügitellimuse saadetisega.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]