---
title: Kinkekaardi moodul
description: See artikkel katab kinkekaardi moodulid ja kirjeldab, kuidas lisada neid saidi lehtedele moodulis Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cc3d51b9891469b8bb0fa38ae2bcd0b27eee56f9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869486"
---
# <a name="gift-card-module"></a>Kinkekaardi moodul

[!include [banner](includes/banner.md)]

See artikkel katab kinkekaardi moodulid ja kirjeldab, kuidas lisada neid saidi lehtedele moodulis Microsoft Dynamics 365 Commerce.

Kinkekaardid on levinud makseviis e-Commerce’i tehingute korral ja kinkekaardi moodulit saab kasutada kassa moodulites kinkekaartide vastuvõtmiseks. Kinkekaardi moodul toetab Dynamics 365, SVS-i ja Givexi kinkekaarte. SVS-i ja Givexi kinkekaarte lunastatakse Adyen maksepakkuja kaudu. Lisatebe saamiseks väliste kinkekaartide (nt SVS ja Givex) toe kohta vt [Väliste kinkekaartide tugi](./dev-itpro/gift-card.md).

> [!NOTE]
> SVS-i ja Givexi kinkekaartide lunastamise tugi maksmisvoo ajal on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.11. 

Saadaval on kaks kinkekaardi moodulit.

- **Kinkekaart** – seda moodulit saab kasutada kassalehel, et lunastada kinkekaart maksevahendina. 
- **Kinkekaardi saldo vaatamine** – seda moodulit saab kasutada mis tahes leheküljel, et kuvada kinkekaardi saldot. See moodul on saadaval Commerce’i väljaandes 10.0.14 ja uuemas.

> [!NOTE]
> Kinkekaardi saldo kontroll-mooduli tugi on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.14.

Järgmisel pildil on näide kinkekaardi moodulist maksmise lehel.

![Kinkekaardi mooduli näide.](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>Mooduli atribuudid

- **Kuva lisavälju** – see atribuut määratleb, millised kinkekaardi väljad tuleks kuvada peale kinkekaardi numbri, mida kuvatakse vaikimisi alati. Näiteks osad kinkekaardid toetavad isikliku ID-numbri (PIN-koodi) kuvamist ja osad toetavad PIN-koodi ja aegumiskuupäeva kuvamist. Selle atripuudi väärtuseks võib määrata ka „Puudub”, mis tähendab, et kuvatakse ainult kinkekaardi number ilma täiendavate väljadeta.

    Toetatud on järgmised väärtused:

    - PIN
    - Aegumiskuupäev
    - PIN-kood ja aegumiskuupäev 
    - None

- **Luba külaliskasutajatele** – kui see atribuut on lubatud, saavad külaliskasutajad kinkekaarte lunastada või saldosid kontrollida. See atribuut nõuab, et Commerce'i peakorteris lubataks kinkekaartidele anonüümne (külalis)juurdepääs. Lisateavet leiate teemast [Kinkekaardimaksete lubamine külaliste väljaregistreerimiseks](#enable-gift-card-payments-for-guest-checkout).

> [!IMPORTANT]
> Atribuut **Luba külaliskasutajatele** on saadaval alates Commerce'i versiooni 10.0.21 väljalaskest. See nõuab Commerce mooduli teegi paketi versiooni 9.31 installimist.

## <a name="site-settings-for-gift-card-modules"></a>Kinkekaardi moodulite saidisätted

Commerce'i saidiehitaja jaotises **Saidi sätted \> Laiendused** on kinkekaardi mooduli säte nimega **Toetatud kinkekaardi tüüp**. See säte toetab kolme väärtust.
- **Dynamics 365 kinkekaart** – selle sätte rakendamisel lubab kinkekaardi moodul ainult Dynamics 365 kinkekaartide lunastamist. See säte on toetatud ainult e-kaubanduse saidi sisselogitud kasutajate puhul.
- **SVS-i ja Givexi kinkekaardid** – selle sätte rakendamisel lubab kinkekaardi moodul ainult Givexi ja SVS-i kinkekaartide lunastamist. See säte on toetatud e-kaubanduse saidi sisselogitud ja anonüümsete kasutajate puhul.
- **Dynamics 365, SVS-i ja Givexi kinkekaardid** – selle sätte rakendamisel lubab kinkekaardi moodul Dynamics 365, Givexi ja SVS-i kinkekaartide lunastamist. See säte on toetatud ainult e-kaubanduse saidi sisselogitud kasutajate puhul.

> [!IMPORTANT]
> Need sätted on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.11 ning on vajalikud ainult juhul, kui vajate tuge SVS-i või Givexi kinkekaartide jaoks. Kui värskendate rakenduse Dynamics 365 Commerce varasemast versioonist, peate faili appsettings.json käsitsi värskendama. Faili appsettings.json värskendamise juhised leiate teemast [SDK ja mooduliteegi värskendused](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file). 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a>Sisemiste kinkekaartide laiendamine e-kaubanduses kasutamiseks

Vaikimisi ei ole sisemised kinkekaardid e-kaubanduses kasutamiseks optimeeritud. Seetõttu peate enne sisemiste kinkekaartide maksmiseks kasutamiseks lubamist konfigureerima need laienditega, mis aitavad neid turvalisemaks muuta. Siin on kinkekaardi alad, mida peate laiendama enne, kui lubate sisemiste kinkekaartide kasutamist tootmises.

- **Kinkekaardi number** – numbriseeriaid kasutatakse sisemiste kinkekaartide jaoks kinkekaardi numbrite loomiseks. Kuna numbriseeriaid on lihtne prognoosida, peaksite laiendama kinkekaardi numbrite genereerimist nii, et väljastatud kinkekaardi numbrite jaoks kasutatakse juhuslikke krüptograafiliselt turvalisi stringe.
- **GetBalance** – **GetBalance** API-d kasutatakse kinkekaardi saldode otsimiseks. Vaikimisi on see API avalik. Kui PIN-ilt ei nõuta kinkekaardi saldode otsimist, võib brute force-ründed kasutada **GetBalance** API-d saldodega kinkekaardi numbrite otsimiseks. Rakendades nii sisemiste kinkekaartide kui API drosselimise PIN-i nõudeid, saate riski leevendada.
- **PIN** – vaikimisi ei toeta sisemised kinkekaardid PIN-e. Ettevõttesiseseid kinkekaarte tuleb laiendada nii, et saldode otsimiseks on vajalik PIN. Seda funktsiooni saab kasutada ka kinkekaartide lukustamiseks pärast järjestikuste PIN-koodi vale sisestamise katseid.

## <a name="enable-gift-card-payments-for-guest-checkout"></a>Lubage kinkekaardi maksed külalise väljaregistreerimiseks

Vaikimisi ei ole kinkekaardimaksed lubatud külalise (anonüümse) väljaregistreerimise jaoks. Nende lubamiseks toimige järgmiselt.

1. Commerce'i Headquartersis minge asukohta **Jaemüük ja kaubandus \> Kanali seadistamine \> POSi seadistamine \> POS \> POSi operatsioonid**.
1. Valige ja hoidke all (või paremklõpsake) ruudustiku päist ning valige käsk **Lisa veerud**.
1. Dialoogiaknas **Veergude lisamine** valige märkeruut **AllowAnonymousAccess**.
1. Tehke valik **Värskenda**.
1. Toimingute **520** (kinkekaardi saldo) ja **214** puhul seadke välja **AllowAnonymousAccess** väärtuseks **1**.
1. Valige käsk **Salvesta**.
1. Käivitage jaotusgraafik **1090** muudatuste sünkroonimiseks kanali andmebaasiga. 

## <a name="add-a-gift-card-module-to-a-page"></a>Lehele kinkekaardi mooduli lisamine

Juhiste saamiseks kinkekaardi mooduli lisamiseks kassa lehele ja nõutavate atribuutide määramiseks, vt [Kassa moodul](add-checkout-module.md).

## <a name="additional-resources"></a>Lisaressursid

[Ostukorvimoodul](add-cart-module.md)

[Ostukorvi ikooni moodul](cart-icon-module.md)

[Maksmismoodul](add-checkout-module.md)

[Makse moodul](payment-module.md)

[Tarneaadressi moodul](ship-address-module.md)

[Tarnesuvandite moodul](delivery-options-module.md)

[Järeletulemisteabe moodul](pickup-info-module.md)

[Tellimuse üksikasjade moodul](order-confirmation-module.md)

[Väliste kinkekaartide tugi](./dev-itpro/gift-card.md)

[SDK ja mooduliteegi värskendused](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
