---
title: Asukoha tootedimensioonide segamine
description: Selles teemas antakse teavet asukohatoote dimensiooni segamise kohta. See asukohaprofiili funktsioon aitab parandada asukohahaldust, kui kasutatakse tootevariante või tooteid, millel on dimensioonid, näiteks moetööstuses. See võimaldab teil otsustada, kas kindlas asukohaprofiilis saab kombineerida konfiguratsioone, värve, laade ja suurusi või kas ühte asukohta saab lisada vaid ühe neist dimensioonidest või nende kombinatsiooni.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: b0309c7a7240d7cac9e5b5724a028f2dc70199e4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217025"
---
# <a name="location-product-dimension-mixing"></a>Asukoha tootedimensioonide segamine

[!include [banner](../includes/banner.md)]

Asukohatoote dimensioonide segamine on asukohaprofiili funktsioon, mis aitab parandada asukohahaldust, kui kasutatakse tootevariante või tooteid, millel on dimensioonid, näiteks moetööstuses. See võimaldab teil otsustada, kas kindlas asukohaprofiilis saab kombineerida konfiguratsioone, värve, laade ja suurusi või kas ühte asukohta saab lisada vaid ühe neist dimensioonidest või nende kombinatsiooni.

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a>Asukohatoote dimensiooni segamise funktsiooni sisselülitamine

Enne asukohatoote dimensiooni segamise funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Seega on funktsioon loetletud järgmisel viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Asukohatoote dimensiooni segamine*

## <a name="setup"></a>Häälestus

Igal asukohal laos on vaja sellega seotud asukohaprofiili, mis kirjeldab asukoha atribuute. Seega kõik sama asukohaprofiili kasutavad asukohad saavad lubada tootedimensiooni segamist pärast selle seadistamist.

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a>Asukohaprofiilide konfigureerimine tootedimensiooni segamise lubamiseks

1. Minge asukohta **Laohaldus \> Seadistus \> Ladu \> Asukohaprofiilid**.
1. Valige asukohaprofiilide loendist suvand **HULGI**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Määrake kiirkaardi **Üldine** suvandi **Luba asukohatoote dimensioonipõhine segamine** väärtuseks *Jah*.

    > [!NOTE]
    > Saate määrata selle suvandi väärtuseks *Jah* ainult juhul, kui suvandi **Luba segakaubad** väärtuseks on seatud *Ei*.

1. Määrake kiirkaardi **Lubatud tootedimensioonide segamine** suvandi **Suurus** väärtuseks *Jah*. Selles teemas kirjeldatud stsenaariumis on segamine võimalik ainult nende toodete puhul, millel dimensioon **Suurus** on erinev. Kuid muud suvandid on samuti saadaval.
1. Valige käsk **Salvesta**.

### <a name="create-a-new-product-master-and-product-variants"></a>Uue tooteetaloni ja tootevariandi loomine

1. Avage **Tooteteabe haldus \> Tooted \> Tooteetalonid**.
1. Tooteetaloni loomiseks valige toimingupaanilt suvand **Uus**.
1. Dialoogiboksis **Uus toode** määrake järgmised väärtused.

    - **Toote tüüp:** *Kaup*
    - **Toote alamtüüp:** *Tooteetalon*
    - **Toote number:** *B0001*
    - **Product nimi:** *B0001 Suurus*
    - **Tootedimensioonigrupp:** *Suurus*
    - **Konfiguratsiooni tehnoloogia:** *Eelmääratletud variant*

1. Valige nupp **OK**.
1. Määrake lehe **Toote üksikasjad** kiirkaardil **Üldine** järgmised väärtused.

    - **Loo variandid automaatselt:** *Jah*
    - **Suuruse grupp:** *CASUALDHIR*

1. Eelmääratletud variantide vaatamiseks valige toimingupaanil **Tootevariandid**.

    Kuvatakse leht **Tootevariandid**, mis sisaldab suuruse grupi konfiguratsiooni variantide loendit.

### <a name="release-products-to-the-usmf-company"></a>Toodete väljastamine ettevõtetele USMF

1. Valige toimingupaanil suvand **Toodete väljastamine**.
1. Kinnitage lehel **Toodete valimine väljastamiseks**, et tootenumber *B0001* oleks loendis ja seejärel valige **Edasi**.
1. Valige **Edasi**, et kinnitada väljastatavad tootevariandid.
1. Valige lehel **Ettevõttete valimine, kuhu väljastada** suvand *USMF* ja klõpsake valiku kinnitamiseks **Edasi**.
1. Valige lehel **Valiku kinnitamine** väljastamise lõpule viimiseks **Valmis**.

    Kuvatakse teade „Toiming lõpule viidud”.

### <a name="update-a-released-product-in-the-usmf-company"></a>Väljastatud toote värskendamine ettevõttes USMF

1. Veenduge, et olete sisse logitud ettevõttesse **USMF**.
1. Väljastatud toote loomise lõpetamiseks minge jaotisse **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Otsige ja valige kaubakood *B0001*, et avada leht **Väljastatud toote üksikasjad**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Veenduge, et kiirkaardi **Üldine** välja **Kauba mudeligrupp** väärtuseks on seatud *FIFO*.
1. Tehke toimingupaani vahekaardil **Toode** grupis **Häälesta** valik **Dimensioonigrupid**.
1. Määrake järgmised väärtused.

    - **Laoala dimensiooni grupp:** *Ladu*
    - **Jälgimisdimensioonigrupp:** *Puudub*

1. Valige nupp **OK**.
1. Tehke toimingupaani vahekaardil **Toode** grupis **Häälesta** valik **Reserveerimishierarhia**.
1. Määrake välja **Reserveerimishierarhia** väärtuseks *Vaikimisi* ja seejärel valige **OK**.
1. Kiirkaardi **Üldine** jaotises **Haldus** näete, et teie valikud on värskendatud.
1. Sisestage kiirkaardi **Ost** väljale **Hind** väärtus *10*.
1. Sisestage kiirkaardi **Kulude haldamine** väljale **Kaubagrupp** väärtus *Heli*.
1. Sisestage kiirkaardi **Ost** väljale **Hind** väärtus *10*.
1. Sisestage kiirkaardi **Ladu** väljale **Ühiku seeriagrupi ID** väärtus *ea*.
1. Valige käsk **Salvesta**.

### <a name="create-a-location-directive"></a>Asukohakorralduse loomine

1. Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.
1. Valige vasakpoolse paani väljal **Töökäsu tüüp** suvand *Ostutellimused*.
1. Valige loendis asukohakorraldus, mille nimi on *24 otse-PO*.
1. Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus**, et lisada rida ruudustikku.
1. Määrake uuel real järgmised väärtused.

    - **Järjekorranumber:** *1*

        Uus rida peaks olema eelnevalt olemasoleva rea ees. Muudatuse tegemiseks kasutage tööriistariba nuppe **Nihuta üles** ja **Nihuta alla** või muutke olemasoleva rea suvandi **Järjekorranumber** väärtuseks *2*.

    - **Nimi:** *Pane asukohaprofiili HULGI*
    - **Fikseeritud asukoha kasutus:** *Fikseeritud ja mittefikseeritud asukohad*
    - **Luba negatiivne laovaru:** *Tühjenda see märkeruut (=Ei)*
    - **Partii lubatud:** *Tühjenda see märkeruut (=Ei)*
    - **Strateegia:** *Puudub*

1. Kui uus rida on valitud, valige ruudustiku kohal **Päringu redigeerimine**.
1. Valige päringu dialoogiboksis vahekaardil **Vahemik** suvand **Lisa**, et lisada rida ruudustikule.
1. Määrake uuel real järgmised väärtused.

    - **Tabel:** *Asukohad*
    - **Tuletatud tabel:** *Asukohad*
    - **Väli:** *Asukohaprofiili ID*
    - **Kriteeriumid:** *BULK*

1. Valige nupp **OK**.
1. Valige toimingupaani lehel **Asukohakorraldused** suvand **Salvesta**.

> [!NOTE]
> Kui kasutate kiirkaardi **Asukohakorralduse tegevused** väljal **Strateegia** asukohastrateegiat *Konsolideerimine* alistatakse kiirkaardi **Lubatud tootedimensioonide segamine** häälestus **Asukohaprofiilides** ja kaubad pannakse samasse asukohta isegi juhul, kui häälestus ei luba seda käitumist.

### <a name="create-a-mobile-device-menu-item"></a>Mobiilse seadme menüü-üksuse loomine

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.
1. Valige toimingupaanil **Uus**, et luua menüü-üksus sortimise jaoks.
1. Määrake päises järgmised väärtused.

    - **Menüü-üksuse nimi:** *Vastuvõttev ostutellimuse rida*
    - **Pealkiri:** *Vastuvõttev ostutellimuse rida*
    - **Režiim:** *töö*
    - **Kasuta olemasolevat tööd:** *Ei*

1. Määrake kiirkaardil **Üldine** järgmised väärtused.

    - **Töö loomise protsess:** *Vastuvõttev ostutellimuse rida ja ladustamine*
    - **Loo litsentsiplaat:** *jah*

1. Valige käsk **Salvesta**.

### <a name="configure-the-mobile-device-menu"></a>Mobiilseadme menüü konfigureerimine

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü**.
1. Valige menüüde loendist suvand **Sissetulev**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Otsige üles ja valige loendist **Saadaolevad menüüd ja menüü-üksused** suvand **Vastuvõttev ostutellimuse rida**.
1. Valige parempoolne noolenupp, et nihutada menüü-üksus **Vastuvõttev ostutellimuse rida** loendisse **Menüüstruktuur**. Sedasi saate lisada uue menüü-üksuse valitud menüüsse.
1. Valige käsk **Salvesta**.

## <a name="scenario"></a>Stsenaarium

See demostsenaarium näitab, kuidas kahte erinevat tootevarianti saab lisada samasse asukohta, kui asukohaprofiil ei luba segakaupu, kuid funktsioon *Asukohatoote dimensiooni segamine* on lubatud. Sellisel juhul saate kasutada varianti **Suurus** kriteeriumina.

Enne alustamist veenduge, et laos *24*, mis kasutab asukohaprofiili *HULGI*, poleks tühjasid asukohti.

### <a name="create-a-purchase-order"></a>Ostutellimuse loomine

Loote ostutellimuse, millel on kolm rida: kaks rida sama tootenumbriga, kuid erineva variandiga **Suurus** ja kolmanda rea erinevale tootele, millel pole variante.

1. Avage jaotis **Ostureskontro \> Ostutellimused \> Kõik ostutellimused**.
1. Valige toimingupaanil nupp **Uus**.
1. Dialoogiboksis **Ostutellimuse loomine** määrake järgmised väärtused.

    - **Hankija konto:** *1001*
    - **Ladu:** *24*

1. Valige nupp **OK**.
1. Luuakse ostutellimus ja lisatakse uus rida kiirkaardile **OIstutellimuse read**. Märkige üles ostutellimuse number.
1. Määrake uuel real järgmised väärtused.

    - **Kauba kood:** *B0001*
    - **Suurus** *L*
    - **Kogus:** *2*

1. Valige ruudustiku kohal **Lisa rida**, et lisada teine ostutellimuse rida ja seadke järgmised väärtused.

    - **Kauba kood:** *B0001*
    - **Suurus** *XL*
    - **Kogus:** *2*

1. Valige **Lisa rida**, et lisada kolmas ostutellimuse rida ja seadke järgmised väärtused.

    - **Kauba kood:** *A0001*
    - **Kogus:** *1*

1.Valige **Salvesta**.

### <a name="receive-purchase-order-lines-in-the-warehouse-app"></a>Ostutellimuse ridade vastuvõtmine laorakenduses

1. Logige laorakendusse sisse kasutajana, kes on lubatud lao *24* jaoks.
1. Valige menüü **Sissetulev**.
1. Valige **Vastuvõttev ostutellimuse rida**.
1. Valige väli **PONUM** ja sisestage ostutellimuse number.
1. Kinnitage kirje, valides lehe allosas kinnitamise nupu (✔).
1. Sisestage sissetuleva ostutellimuse rea number. Valige väli **LINENUM** ja seejärel kasutage numbriklahvistikku väärtuse *1* sisestamiseks.
1. Kinnitage kirje.
1. Sisestage sissetulev kogus. Valige plussmärgi nupp (**+**) kaks korda, et suurendada välja **Kogus** väärtuseks *2*.
1. Registreerige oma kirje, valides lehe allosas nupu (✔) ja seejärel kinnitage oma kirje, valides nupu (✔) uuesti.
1. Vaadake teavet lehel **Ostutellimused: sisestatud**. Sellel lehel kuvatakse ladustamiseks loodud töö (Töö 1).

    Kuvatakse asukoht, kuhu vastuvõetud kaup ladustatakse, identifitseerimisnumber, kaup, suurus ja ülesande **Vastuvõttev ostutellimuse rida** kogus, mille äsja lõpule viisite.

1. Kinnitage ladustamise töö.
1. Korrake etappe 4–11 ostutellimuse rea 2 jaoks. Kuid etapis 8 määrake koguseks *1*.

    Luuakse uus ladustamise töö (Töö 2) Tööga 1 samasse asukohta.

1. Korrake etappe 4–11 uuesti ostutellimuse rea 2 jaoks. Etapis 8 määrake järelejäänud koguseks *1*.

    Luuakse uus ladustamise töö (Töö 3) Tööga 1 ja 2 samasse asukohta. Selline käitumine ilmneb juhul, kui kasutatakse asukohakorraldust *Konsolideerimine* ja kiirkaart **Lubatud tootedimensiooni segamine** seadistuses *Hulgi* **Asukohaprofiilid** lubab variandi **Suurus** segamist asukohas.

1. Korrake etappe 4–11 ostutellimuse rea 3 jaoks. Määrake etapis 8 kogus *1* kaubakoodi *A0001* jaoks.

    Luuakse uus ladustamise töö (Töö 4) ostutellimuse ridadel 1 ja 2 kasutatud asukohast erinevas asukohas. Selline käitumine ilmneb seetõttu, et asukohaprofiil ei luba segatooteid, kuid see lubab segadimensioone samal tooteetalonil.

1. Valige lehe ülaosas nupp Menüü (nimetatakse mõnikord hamburgeriks või hamburgeri nupuks) ja seejärel valige **Tühista**, et väljuda suvandist **Vastuvõttev ostutellimuse rida**.

> [!TIP]
> Võite seda stsenaariumi korrata, kuid määrake seekord jaotise *HULGI* **Asukohaprofiilid** kiirkaardil **Luba tootedimensioonide segamine** suvandi väärtuseks **Suurus** - *Ei*, et ühtegi tootedimensiooni ei saaks segada. Sellisel juhul pannakse ostutellimuse vastuvõtmisel iga tootevariant uude asukohta.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]