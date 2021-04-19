---
title: Kinkekaardi moodul
description: See teema hõlmab kinkekaardi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.openlocfilehash: a4e4e06ab7032d68fcd36a8e80bc714ebaaac821
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797667"
---
# <a name="gift-card-module"></a>Kinkekaardi moodul

[!include [banner](includes/banner.md)]

See teema hõlmab kinkekaardi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

Kinkekaardid on levinud makseviis e-Commerce’i tehingute korral ja kinkekaardi moodulit saab kasutada kassa moodulites kinkekaartide vastuvõtmiseks. Kinkekaardi moodul toetab Dynamics 365, SVS-i ja Givexi kinkekaarte. SVS-i ja Givexi kinkekaarte lunastatakse Adyen maksepakkuja kaudu. Lisatebe saamiseks väliste kinkekaartide (nt SVS ja Givex) toe kohta vt [Väliste kinkekaartide tugi](./dev-itpro/gift-card.md).

> [!NOTE]
> SVS-i ja Givexi kinkekaartide lunastamise tugi maksmisvoo ajal on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.11. 

Saadaval on kaks kinkekaardi moodulit.

- **Kinkekaart** – seda moodulit saab kasutada lehel Kassa, et lunastada kinkekaart maksevahendina. 
- **Kinkekaardi saldo vaatamine** – seda moodulit saab kasutada mis tahes leheküljel, et kuvada kinkekaardi saldot. See moodul on saadaval Commerce’i väljaandes 10.0.14 ja uuemas.

> [!NOTE]
> Kinkekaardi saldo kontroll-mooduli tugi on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.14.

Järgmisel pildil on näide kinkekaardi moodulist maksmise lehel.

![Kinkekaardi mooduli näide](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>Mooduli atribuudid

- **Kuva lisaväljad** – see atribuut määratleb, millised kinkekaardi väljad tuleks kuvada peale kinkekaardi numbri, mida kuvatakse vaikimisi alati. Näiteks osad kinkekaardid toetavad isikliku ID-numbri (PIN-koodi) kuvamist ja osad toetavad PIN-koodi ja aegumiskuupäeva kuvamist. Selle atripuudi väärtuseks võib määrata ka „Puudub”, mis tähendab, et kuvatakse ainult kinkekaardi number ilma täiendavate väljadeta.

Toetatud väärtused.
-   PIN
-   Aegumiskuupäev
-   PIN-kood ja aegumiskuupäev 
-   None

## <a name="site-settings-for-gift-card-modules"></a>Kinkekaardi moodulite saidisätted

Commerce'i saidiehitaja jaotises **Saidi sätted \> Laiendused** on kinkekaardi mooduli säte nimega **Toetatud kinkekaardi tüüp**. See säte toetab kolme väärtust.
- **Dynamics 365 kinkekaart** – selle sätte rakendamisel lubab kinkekaardi moodul ainult Dynamics 365 kinkekaartide lunastamist. See säte on toetatud ainult e-kaubanduse saidi sisselogitud kasutajate puhul.
- **SVS-i ja Givexi kinkekaardid** – selle sätte rakendamisel lubab kinkekaardi moodul ainult Givexi ja SVS-i kinkekaartide lunastamist. See säte on toetatud e-kaubanduse saidi sisselogitud ja anonüümsete kasutajate puhul.
- **Dynamics 365, SVS-i ja Givexi kinkekaardid** – selle sätte rakendamisel lubab kinkekaardi moodul Dynamics 365, Givexi ja SVS-i kinkekaartide lunastamist. See säte on toetatud ainult e-kaubanduse saidi sisselogitud kasutajate puhul.

> [!IMPORTANT]
> Need sätted on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.11 ning on vajalikud ainult juhul, kui vajate tuge SVS-i või Givexi kinkekaartide jaoks. Kui värskendate rakenduse Dynamics 365 Commerce varasemast versioonist, peate faili appsettings.json käsitsi värskendama. Faili appsettings.json värskendamise juhised leiate teemast [SDK ja mooduliteegi värskendused](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file). 

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