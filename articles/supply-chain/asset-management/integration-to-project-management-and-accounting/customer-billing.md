---
title: Kliendile kuuluvate varade hooldamise arve
description: Selles teemas selgitatakse, kuidas luua, töödelda ja esitada arve hooldustöö eest, mis tehakse varadele, mis kuuluvad teie klientidele.
author: johanhoffmann
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 643e59f082949ed51ab61d79648a98b83a7f0b03
ms.sourcegitcommit: 1e615288db245f83c5d5e0cd45315400f8946beb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/08/2021
ms.locfileid: "5131837"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a>Kliendile kuuluvate varade hooldamise arve

[!include [banner](../../includes/banner.md)]

Funktsioon *Töökäsu arveldamine* võimaldab teil luua, töödelda ja esitada arve hooldustöö eest, mis tehakse teie klientidele kuuluvatele varadele. See funktsioon võimaldab teil teha järgmisi toiminguid.

- Sidus kliendid neile kuuluvate varadega.
- Töökäsku luues valida kliendi ja vaadata varasid, mida klient omab.
- Häälestada iga kliendi jaoks ülemprojekt.
- Registreerida töökäsu tunde, üksusi, kulusid ja tasusid ning luua seejärel hiljem kliendile arvesoovitus.

Lisaks omab see funktsioon järgmisi funktsioone.

- Kliendi ülemprojekti projektileping kopeeritakse automaatselt asjaomasesse töökäsu projekti.
- Varahaldus saab nüüd kasutada *tasuta* projekti kandetüüpi nii töökäsu prognooside kui ka töökäsu töölehtede jaoks.

## <a name="turn-on-the-customer-billing-feature"></a>Kliendi arveldusfunktsiooni sisselülitamine

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *Projektihaldus ja raamatupidamine*
- **Funktsiooni nimi:** *Töökäsu arveldamine*

## <a name="example-scenario"></a>Näidisstsenaarium

Et teada saada, kuidas see funktsioon töötab, töötage läbi järgmise näite stsenaarium.

Selle stsenaariumi kasutamiseks siin määratud näidiskirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Enne alustamist peate valima **USMF-i** juriidilise isiku.

Seda stsenaariumi saate kasutada ka juhistena funktsiooni kasutamiseks, kui töötate tootmissüsteemis. Kuid sellisel juhul peate asendama oma väärtused ja teil ei pruugi olla teatud tüüpi nõutavaid kirjeid, mida pakuvad standardsed demoandmed.

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a>1. etapp: kliendi jaoks uue projektilepingu loomine

1. Avage **Projektihaldus ja raamatupidamine \> Projektid \> Projektilepingud**.
1. Valige toimingupaanil nupp **Uus**.
1. Dialoogiboksis **Uus projektileping** määrake järgmised väärtused.

    - **Nimi:** *Pelican Wholesales*
    - **Rahastamise tüüp:** *klient*
    - **Rahastamisallikas:** *US-013* (*Pelican Wholesales*)

1. Valige nupp **OK**.

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a>2. etapp: kliendi jaoks uue ülemprojekti loomine

Siin loodud ülemprojekti kasutatakse kliendi töökäskude loomisel.

1. Avage **Projektihaldus ja raamatupidamine \> Projektid \> Kõik projektid**.
1. Valige toimingupaanil nupp **Uus**.
1. Dialoogiboksis **Uus projekt** määrake järgmised väärtused.

    - **Projekti tüüp:** *aeg ja materjal*
    - **Projekti nimi:** *Pelican Wholesalesi töökäsud*
    - **Projekti rühm:** *TM*
    - **Projektilepingu ID:** *Pelican Wholesales* (varem loodud leping)
    - **Alguskuupäev:** valige tänane kuupäev.

1. Valige **Loo projekt**.
1. Uus projekt avatakse. Märkige üles suvandi **Projekti ID** väärtus. Peate selle hiljem sisestama.

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a>3. etapp: varahalduses uue töökäsu tüübi loomine

1. Avage **Varahaldus \> Seadistus \> Töökäsk \> Töökäsu tüübid**.
1. Valige toimingupaanil nupp **Uus**.
1. Uus kirje lisatakse loendisse. Seadke selle jaoks järgmised väärtused.

    - **Töökäsu tüüp:** *teenus*
    - **Nimi:** *Teenuse töökäsud*
    - **Töökäsu töötsükli olek:** *standardne*

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a>4. etapp: kliendikonto sidumine üleprojektiga

Peate nüüd varahalduses projekti seadistamises siduma kliendikonto ülemprojektiga.

1. Avage **Varahaldus \> Seadistamine \> Töökäsud \> Projekti seadistamine**.
1. Valige vahekaardil **Ülemprojekt** suvand **Lisa**, et lisada rida.
1. Määrake uuel real järgmised väärtused.

    - **Kliendikonto:** *US-013* (*Pelican Wholesales*)
    - **Projekti ID:** sisestage projekti ID, mille olete varem üles märkinud.

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a>5. etapp: projektirühma ja tüübi töökäsu projektiga sidumine

Peate olema endiselt lehel **Projekti seadistamine** (**Varahaldus \> Seadistamine \> Töökäsud \> Projekti häälestamine**).

1. Valige vahekaardil **Projektirühm** suvand **Lisa**, et lisada rida.
1. Määrake uuel real järgmised väärtused.

    - **Töötellimuse tüüp:** *teenus* (varem loodud töökäsu tüüp)
    - **Projekti rühm:** *TM*

> [!NOTE]
> Töökäsu projekti leping päritakse alati ülemprojektilt.

### <a name="step-6-link-an-asset-to-the-customer-id"></a>6. etapp: siduge vara kliendi ID-ga

1. Avage **Varahaldus \> Varad \> Aktiivsed varad**.
1. Väljal **Filter** sisestage väärtus *VE-102* ja valige filtrimisaluseks **Vara**.
1. Valig selle seadistuste avamiseks vara.
1. Määrake kiirkaardi **Klient** välja **Kliendi konto** väärtuseks *US-013* (*Pelican Wholesales*).

    Väli **Nimi** värskendatakse automaatselt väärtusele *Pelican Wholesales*.

### <a name="step-7-create-a-new-work-order-on-the-asset"></a>7. etapp: vara uue töökäsu tüübi loomine

1. Avage **Varahaldus \> Töökäsud \> Aktiivsed töökäsud**.
1. Valige toimingupaanil nupp **Uus**.
1. Dialoogiboksis **Töökäsu loomine** määrake järgmised väärtused.

    - **Töökäsu tüüp:** *teenus*
    - **Kirjeldus:** *auto remontimine*
    - **Kliendikonto:** *US-013* (*Pelican Wholesales*)
    - **Vara:** *VE-102*

        > [!NOTE]
        > Otsing näitab ainult valitud kliendikontoga seotud varasid.

    - **Hooldustöö tüüp:** *remont*
    - **Valdkond:** *mehaanika*
    - **Teenuse tase:** *4*

1. Valige nupp **OK**.

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a>8. etapp: töötellimuse läbivaatamine ja selle kallal töötamine

Selles jaotises töötate eelmises jaotses loodud töökäsu kallal.

1. Järgige järgmisi samme, et veenduda, kas ülemprojekt on *Pelican Wholesalesi töökäsk*.

    1. Valige jaotises **Töökäsu hooldustööd** rida.
    1. Kiirkaardil **Rea üksikasjad** kontrollige väärtust **Projekti ID**. See peaks olema sidekriipsuga number kujul *\<Parent-Project-ID\>-\<Project-ID\>*. See väärtus on link.
    1. Valige projekti ID link, et avada lehekülg, kus saate vaadata ülemprojekti ja projekti nimesid.

1. Tegumiriba vahekaardi **Töökäsk** rühmas **Töötsükli olek** valige **Värskenda töökäsu olekut**.
1. Dialoogiboksis **Töökäsu oleku värskendamine** veerus **Valimine** valige märkeruut rea jaoks, kus väli **Töötsükli olek** on määratud valikule *Pooleli*.
1. Valige nupp **OK**.
1. Dialoogiboksis **Töötsükli olek: pooleli** valige **OK**.

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a>9. etapp: sisestage töökäsule kulunud tunnid ja looge uus arve soovitus

Selles jaotises jätkate töötamist töökäsuga, mille kallal eelmises jaotises töötasite.

1. Toimingupaani vahekaardi **Töökäsk** grupis **Projekt** valige suvand **Töölehed**.

    Kuvatakse leht **Töökäsu töölehed**. Siin saate registreerida töökäsule kulutatud aja.

1. Valige kiirkaardil **Tunnid** suvand **Lisa rida**.
1. Uuel real seadke määrake välja **Tunnid** väärtuseks *4*.
1. Tehke toimingupaanil valik **Sisesta töölehed**.
1. Sulgege leht **Töökäsu töölehed**, et töökäsku naasta.
1. Toimingupaanil vahekaardil **Arveldamine** valige suvand **Uus arve soovitus**.
1. Dialoogiboksis **Arve soovituse loomine** jaotises **Projektitehingud** valige märkeruut **Valimine** iga rea jaoks, mille kohta arve soovite esitada.
1. Dialoogiboksi sulgemiseks ja uue arve soovituse vaatamiseks valige **OK**.
