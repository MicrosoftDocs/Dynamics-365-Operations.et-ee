---
title: Asukoha litsentsiplaadi paigutus
description: Identifitseerimisnumbri asukoha positsioneerimine võimaldab teil näha, kus identifitseerimisnumber asub mitme kaubaalusega asukohas, nt asukoht, mis kasutab kahekordsete kaubaalustega riiuleid.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: e52b313e0a00c04edf9003aa6292146936f837d4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889424"
---
# <a name="location-license-plate-positioning"></a>Asukoha litsentsiplaadi paigutus

[!include [banner](../includes/banner.md)]

Identifitseerimisnumbri asukoha positsioneerimine võimaldab teil näha, kus identifitseerimisnumber asub mitme kaubaalusega asukohas, nt asukoht, mis kasutab kahekordsete kaubaalustega riiuleid.

Funktsioon lisab igale lattu paigutatavale identifitseerimisnumbrile järjekorranumbri. Seda järjekorranumbrit kasutatakse identifitseerimisnumbrite järjestamiseks laos. Seetõttu toetab funktsioon nutikalt selliseid stsenaariume, kus kliendid kasutavad gravitatsioonipõhist ladustamissüsteemi ja peavad komplekteerimise eesmärgil teadma, milline on identifitseerimisnumbri esikülg.

See artikkel sisaldab stsenaariumi, mis näitab, kuidas funktsiooni seadistada ja kasutada.

## <a name="turn-the-location-license-plate-positioning-feature-on-or-off"></a>Asukoha litsentsiplaadi paigutamise funktsiooni sisse- või väljalülitamine

Selles artiklis kirjeldatud funktsioonide kasutamiseks peab asukoha *litsentsiplaadi paigutamise* funktsioon olema teie süsteemi jaoks sisse lülitatud. Tarneahela halduse 10.0.25 puhul on see funktsioon kohustuslik ja seda ei saa välja lülitada. Kui käitate versiooni, mis on *vanem kui 10.0.25, saavad administraatorid selle funktsiooni sisse või välja lülitada, otsides asukoha litsentsiplaadi*[paigutamise funktsiooni Funktsioonihalduse tööruumis](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="example-scenario"></a>Näidisstsenaarium

### <a name="make-sample-data-available"></a>Näidisandmete kättesaadavaks tegemine

Selle stsenaariumi kasutamiseks siin soovitatud väärtuste abil, peate kasutama süsteemi, kuhu on installitud näidisandmed. Enne alustamist peate valima ka juriidilise isiku **USMF**.

### <a name="set-up-the-feature-for-this-scenario"></a>Funktsiooni seadistamine selle stsenaariumi jaoks

Viige lõpule järgmised protseduurid, et seadistada *selles* artiklis esitatud stsenaariumi jaoks asukoha litsentsiplaadi paigutamise funktsioon.

#### <a name="location-profiles"></a>Asukoha profiilid

Funktsioon peab olema asukohaprofiilis sisse lülitatud iga asukoha jaoks, kus seda kasutatakse.

1. Minge asukohta **Laohaldus \> Seadistus \> Ladu \> Asukohaprofiilid**.
1. Valige vasakpoolsel paanil asukohaprofiilide loendist **BULK-06**.
1. Funktsioon on lisanud kaks uut suvandit kiirkaardile **Üldine**. Määrake järgmised väärtused.

    - **Luba identifitseerimisnumbri positsioon:** *Jah*

        Kui selle suvandi väärtuseks on seatud *Jah*, säilitatakse identifitseerimisnumbri positsioon selle asukoha identifitseerimisnubrite puhul.

    - **Kuva mobiilse seadme LP-positsioon:** *Jah*

        Kui selle suvandi väärtuseks on seatud *Jah*, kuvatakse identifitseerimisnumbri positsioon mobiilse seadme kasutajatele korrigeerimise ja inventuuri ajal. Selle suvandi sätet saate muuta ainult juhul, kui funktsioon on sisse lülitatud.

1. Valige käsk **Salvesta**.

#### <a name="location-directives"></a>Asukohakorraldus

1. Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.
1. Veenduge, et vasakpoolsel paanil on välja **Töötellimuse tüüp** väärtuseks seatud *Müügitellimused*.
1. Valige asukohakorralduste loendis **61 SO tellimuse komplekteerimine**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Valige kiirkaardil **Read** rida, mille suvandi **Järjekorranumber** väärtus on *2*.
1. Valige kiirkaardil **Asukohakorralduse tegevused** rida, mille suvandi **Nimi** väärtus on *Komplekteeri kaubaalusest väiksem kogus* (see peaks olema ainus rida) ja muutke selle suvandi **Järjekorranumber** väärtuseks *2*.
1. Valige ruudustiku kohal suvand **Uus**, et lisada rida uue asukohakorralduse tegevuse jaoks.
1. Määrake uuel real järgmised väärtused.

    - **Järjekorranumber:** *1*
    - **Nimi:** *Komplekteerimise positsioon 1*

1. Kui uus rida on valitud, valige ruudustiku kohal **Päringu redigeerimine**.
1. Valige päringuredaktoris vahekaart **Liitmised**.
1. Laiendage tabeli liitmist **Asukohad**, et kuvada liitmist tabelis **Varude dimensioonid**.
1. Laiendage tabeli liitmist **Varude dimensioonid**, et kuvada liitmist tabelis **Vaba kaubavaru**.
1. Valige **Varude dimensioonid** ja seejärel valige **Lisa tabeli liitmine**.
1. Valige kuvatava tabelite loendi veerust **Seos** suvand **Identifitseerimisnumber (Identifitseerimisnumber)**. Seejärel valige **Vali**, et lisada **Identifitseerimisnumber** tabeli liitmisse **Varude dimensioonid**.
1. Kui **Identifitseerimisnumber** on valitud, valige **Lisa tabeli liitmine**.
1. Valige kuvatava tabelite loendi veerust **Seos** suvand **Asukoha identifitseerimisnumbri positsioneerimine (Identifitseerimisnumber)**. Seejärel valige **Vali**, et lisada **Asukoha identifitseerimisnumbri positsioneerimine** tabeli liitmisse **Varude dimensioonid**.

    ![Tabeli liitmised.](media/LpTableJoin.png "Tabeli liitmised")

1. Värskendatud liidetud tabelite kinnitamiseks ja päringuredaktori sulgemiseks valige **OK**.
1. Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Redigeeri päringut** uuesti, et avada päringuredaktor uuesti.
1. Vahekaardil **Vahemik** valige käsk **Lisa**, et lisada uus rida ruudustikule.
1. Määrake uuel real järgmised väärtused.

    - **Tabel:** *Asukoha identifitseerimisnumbri positsioneerimine*
    - **Tuletatud tabel:** *Asukoha identifitseerimisnumbri positsioneerimine*
    - **Väli:** *LP positsioon*
    - **Kriteeriumid:** *1*

    ![Uus vahemik.](media/LpPositionCriteria.png "Uus vahemik")

1. Oma muudatuste kinnitamiseks ja päringu redaktori sulgemiseks valige **OK**.

### <a name="set-up-sample-data-for-this-scenario"></a>Näidisandmete seadistamine selle stsenaariumi jaoks

Selle stsenaariumi puhul peab kasutaja logima sisse ladustamise mobiilirakendusse, kasutades töötajat, kes on seadistatud laos *61* töötamiseks. Kasutaja peab ka kanded lõpule viima.

Kuna funktsioon *Asukoha identifitseerimisnumbri positsioneerimine* lisab asukohas identifitseerimisnumbri positsioonidele uue identifikaatori, peate stsenaariumi toetamiseks looma esmalt mõned andmed.

#### <a name="spot-count-the-first-location"></a>Esimese asukoha punktinventuur

1. Avage ladustamise mobiilirakendus ja logige sisse lattu *61*.
1. Avage jaotis **Varud \> Punktinventuur**.
1. Määrake lehel **Punktinventuur** välja **Asukoht** väärtuseks *01A01R1S1B*.
1. Valige nupp **OK**.

    Sellel lehel kuvatakse teie sisestatud asukoht. Samuti kuvatakse järgmine teade: „Asukoht lõpule viidud, kas soovite lisada uue LP või kauba?”

1. Asukohas inventuuri lisamiseks valige **Värskenda**.
1. Valige leht **Tsükliline inventuur: lisage uus LP või kaup**, väli **Kaup** ja sisestage seejärel väärtus *A0001*.
1. Valige nupp **OK**.
1. Valige leht **Tsükliline inventuur: lisage uus LP või kaup**, väli **LP** ja sisestage seejärel väärtus *LP1001* (või mis tahes muu teie valitud identifitseerimisnumbri number).

    Lehel **Tsükliline inventuur: lisage uus LP või kaup** kuvatakse **Identifitseerimisnumbri positsioon 1**.

1. Valige nupp **OK**.

    Nüüd peate määrama kauba koguse, mida identifitseerimisnumbris loendatakse.

1. Määrake välja **Kogus** väärtuseks *10*.
1. Valige nupp **OK**.

    Sellel lehel kuvatakse teie sisestatud asukoht. Samuti kuvatakse järgmine teade: „Asukoht lõpule viidud, kas soovite lisada uue LP või kauba?”

1. Asukohas teise inventuuri lisamiseks valige **Värskenda**.
1. Valige leht **Tsükliline inventuur: lisage uus LP või kaup**, väli **Kaup** ja sisestage seejärel väärtus *A0002*.
1. Valige nupp **OK**.
1. Valige leht **Tsükliline inventuur: lisage uus LP või kaup**, väli **LP** ja sisestage seejärel väärtus *LP1002* (või mis tahes muu teie valitud identifitseerimisnumbri number, eeldusel, et see erineb teie eelnevalt määratud identifitseerimisnumbri numbrist).
1. Muutke identifitseerimisnumbri positsiooni, määrates välja **LP-positsioon** väärtuseks *2*.
1. Valige nupp **OK**.
1. Määrake kauba kogus, mida loendatakse identifitseerimisnumbris, seadistades välja **Kogus** väärtuseks *10*.
1. Valige nupp **OK**.

    Sellel lehel kuvatakse teie sisestatud asukoht. Samuti kuvatakse järgmine teade: „Asukoht lõpule viidud, kas soovite lisada uue LP või kauba?”

1. Valige nupp **OK**.

Töö on nüüd lõpule viidud.

#### <a name="spot-count-the-second-location"></a>Teise asukoha punktinventuur

1. Määrake lehel **Punktinventuur** välja **Asukoht** väärtuseks *01A01R1S2B*.
1. Valige nupp **OK**.

    Sellel lehel kuvatakse teie sisestatud asukoht. Samuti kuvatakse järgmine teade: „Asukoht lõpule viidud, kas soovite lisada uue LP või kauba?”

1. Asukohas inventuuri lisamiseks valige **Värskenda**.
1. Valige leht **Tsükliline inventuur: lisage uus LP või kaup**, väli **Kaup** ja sisestage seejärel väärtus *A0002*.
1. Valige nupp **OK**.
1. Valige leht **Tsükliline inventuur: lisage uus LP või kaup**, väli **LP** ja sisestage seejärel väärtus *LP1003* (või mis tahes muu teie valitud identifitseerimisnumbri number, eeldusel, et see erineb mõlemast teie eelnevalt määratud identifitseerimisnumbri numbrist).

    Lehel **Tsükliline inventuur: lisage uus LP või kaup** kuvatakse **Identifitseerimisnumbri positsioon 1**.

1. Valige nupp **OK**.
1. Määrake kauba kogus, mida loendatakse identifitseerimisnumbris, seadistades välja **Kogus** väärtuseks *10*.
1. Valige nupp **OK**.

    Sellel lehel kuvatakse teie sisestatud asukoht. Samuti kuvatakse järgmine teade: „Asukoht lõpule viidud, kas soovite lisada uue LP või kauba?”

1. Valige nupp **OK**.

Töö on nüüd lõpule viidud.

#### <a name="work-details"></a>Töö üksikasjad

> [!NOTE]
> Mobiilirakenduse punktinventuurid loovad tsüklilise inventuuri töö Microsoft Dynamics 365-s. See töö eeldab, et loendused aktsepteeritakse enne nende sisestamist varudesse.

1. Logige sisse rakendusse Dynamics 365 Supply Chain Management.
1. Avage jaotis **Laohaldus \> Töö \> Töö üksikasjad**.
1. Otsige vahekaardilt **Ülevaade** üles järgmiste väärtustega read.

    - **Töötellimuse tüüp:** *Tsükliline inventuur*
    - **Ladu:** *61*
    - **Töö olek:** *Läbivaatuse ootel*

    Nende ridade jaoks peaks olema loodud kaks töö ID-d. Mõlema töö ID loendused tuleb vastu võtta.

1. Valige ruudustikus esimese töö ID töökäsu tüübi *Tsükliline inventuur* jaoks.
1. Valige toimingupaani vahekaardil **Töö** grupis **Töö** üksus **Tsükliline inventuur**.

    Kuvatakse kaks rida, kummagi identifitseerimisnumbri kohta üks. Väljade **Loendatud kogus**, **Asukoht**, **Identifitseerimisnumber** ja **Kaup** väärtused peaksid vastama mobiilses seadmes loodud inventuuri kirjetele. Kui mõni nendest väljadest pole nähtav, valige toimingupaanil **Kuva dimensioonid** nende ruudustikku lisamiseks.

1. Valige mõlemad read.
1. Valige toimingupaanil **Kinnita inventuur**.
1. Kuvatakse teade „Sisestamine – tööleht”. Valige **Teate üksikasjad** sisestatud töölehe numbri vaatamiseks.
1. Sulgege teate üksikasjad.
1. Värskendage lehte **Töö**.

    Esimese töö ID on suletud ja seda enam ei kuvata.

    > [!TIP]
    > Suletud töö kuvamiseks märkige ruudustiku kohal märkeruut **Kuva suletud**.

    Nüüd saate kinnitada asukohas *01A01R1S2B* oleva identifitseerimisnumbri töö.

1. Valige vahekaardil **Ülevaade** teise töö ID töökäsu tüübi *Tsükliline inventuur* jaoks.
1. Valige toimingupaani vahekaardil **Töö** grupis **Töö** üksus **Tsükliline inventuur**.

    Kuvatakse üks rida kauba ja identifitseerimisnumbri jaoks. Väljade **Loendatud kogus**, **Asukoht**, **Identifitseerimisnumber** ja **Kaup** väärtused peaksid vastama mobiilses seadmes loodud inventuuri kirjetele.

1. Valige rida.
1. Valige toimingupaanil **Kinnita inventuur**.
1. Kuvatakse teade „Sisestamine – tööleht”. Valige **Teate üksikasjad** sisestatud töölehe numbri vaatamiseks.
1. Sulgege teate üksikasjad.
1. Värskendage lehte **Töö**.

    Teise töö ID on suletud ja seda enam ei kuvata.

    > [!TIP]
    > Suletud töö kuvamiseks märkige ruudustiku kohal märkeruut **Kuva suletud**.

#### <a name="on-hand-by-location"></a>Laoseis asukoha järgi

1. Avage jaotis **Laohaldus \> Päringud ja aruanded \> Vaba varu asukoha järgi**.
1. Määrake järgmised väärtused.

    - **Tegevuskoht:** *6*
    - **Ladu:** *61*
    - **Värskenda kõigis asukohtades:** *Jah*

1. Pange tähele, et asukohas *01A01R1S1B* on kaks identifitseerimisnumbrit.

    - **A0001**, kus välja **LP-positsioon** väärtuseks on seatud *1*
    - **A0002**, kus välja **LP-positsioon** väärtuseks on seatud *2*

1. Pange tähele, et asukohas *01A01R1S2B* on üks identifitseerimisnumber.

    - **A0002**, kus välja **LP-positsioon** väärtuseks on seatud *1*

### <a name="sales-order-scenario"></a>Müügitellimuse stsenaarium

Nüüd, kui funktsioon *Asukoha identifitseerimisnumbri positsioneerimine* on seadistatud ja varud on etapiviisilised, peate looma müügitellimuse komplekteerimistöö loomiseks, mis suunab lao töötaja komplekteerima kaupa *A0002* varude asukohast, kus kaubaaluse ID on positsioonil *1*.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Valige toimingupaanil nupp **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - **Kliendi konto:** *US-004*
    - **Ladu:** *61*

1. Valige nupp **OK**.
1. Kiirkaardi **Müügitellimuse read** ruudustikku on lisatud uus rida. Määrake sellel uuel real järgmised väärtused.

    - **Kauba kood:** *A0002*
    - **Kogus:** *1*

1. Valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.
1. Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida varud tellimuserea jaoks.
1. Sulgege leht **Reserveerimine**.
1. Tehke tegevuspaani vahekaardil **Ladu** grupis **Tegevused** valik **Vabasta lattu**.

    Saate teabesõnumi, mis näitab selle tellimuse jaoks loodud voo ID-d ja saadetise ID-d.

1. Valige ruudustiku kohal oleva menüü **Ladu** kiirkaardilt **Müügitellimuse read** suvand **Töö üksikasjad**.
1. Kuvatakse leht **Töö**, mis kuvab müügirea jaoks loodud töö. Märkige üles kuvatav töö ID.

### <a name="sales-picking-scenario"></a>Müügi komplekteerimise stsenaarium

1. Avage mobiilirakendus ja logige sisse lattu *61*.
1. Avage jaotis **Väljaminev \> Müügi komplekteerimine**.
1. Valige leht **Töö ID / identifitseerimisnumbri ID skannimine**, valige väli **ID** ja sisestage seejärel müügirea välja töö ID.
1. Pange tähele, et komplekteerimistöö suunab teid komplekteerima kauba *A0002* asukohast *01A01R1S2B*. Saate selle juhise seetõttu, et kaup *A0002* on identifitseerimisnumbri all, mis on selles asukohas positsioonis *1*.

    ![Positsiooni 1 asukoht.](media/LocationLicensePlatePositioning.png "Positsiooni 1 asukoht")

1. Sisestage selle asukoha jaoks loodud identifitseerimisnumbri ID ja seejärel järgige viipasid müügitellimuse komplekteerimiseks.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]