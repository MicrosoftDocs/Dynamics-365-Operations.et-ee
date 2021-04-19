---
title: Tarneaadressi moodul
description: See teema hõlmab tarneaadressi moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce konfigureerida.
author: anupamar-ms
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: fd48a04612159cbe29a2cc7cafea1c9c4c8745b4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795425"
---
# <a name="shipping-address-module"></a>Tarneaadressi moodul

[!include [banner](includes/banner.md)]

See teema hõlmab tarneaadressi moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce konfigureerida.

Tarneaadressi moodul võimaldab klientidel maksmise voo ajal lisada või valida tellimuse tarneaadressi. Kui klient on sisse logitud, kuvatakse aadressid, mis selle kliendi jaoks eelmisel korral salvestati, ja klient saab teha nende seast valiku. Klient saab lisada ka uue aadressi. Tarneaadressi moodulit kasutatakse kõigi kaupade puhul, mis nõuavad tarnet.

Tarneaadressi vorminguid saab määratleda Commerce'i peakontoris iga riigi või regiooni jaoks ning tarneaadressi moodul täidab seejärel riigi-/regioonipõhiseid reegleid.

Kui kliendid sisestavad tarneaadressi maksmise voos, on neil võimalus salvestada aadress esmase aadressina. See valik kuvatakse ainult siis, kui klient on sisse logitud.

Kuigi tarneaadressi moodul ei paku aadressi kinnitamist, saab seda funktsiooni rakendada kohandamise kaudu.

Järgmisel pildil on näide uuest tarneaadressi moodulist maksmise lehel.

![Tarneaadressi mooduli näide maksmise lehel](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a>Mooduli atribuudid

| Atribuudi nimi | Väärtused | Kirjeldus |
|---------------|--------|-------------|
| Pealkiri | Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**) | Tarneaadressi mooduli valikuline pealkiri. |
| Kuva aadressi tüüp | **Tõene** või **Väär** | Kui selle valikulise atribuudi väärtuseks on seatud **Tõene**, kuvatakse aadressi tüüp, nt **Kodu** või **Ettevõte**. Kui aadressi tüüpi pole määratud, salvestatakse aadress automaatselt nii, et selle **Tüüp**=**Muu**. |
| Lubage automaatne soovitus| **Tõene** või **Väär** | Kui valikuline atribuut on seatud väärtusele **Tõene**, antakse automaatsed aadressisoovitused. Need soovitused on toetatud Bingi kaartide puhul. Lisateavet selle kohta, kuidas seadistada oma saidi jaoks Bing Mapsi integratsioon, vt [poe valimise moodulit](store-selector.md). See funktsioon on saadaval Commerce'i versiooni 10.0.15 väljalaskes.|
|Automaatsed soovitatud valikud| Number| Kui automaatsed aadressisoovitused on lubatud, saate määrata lisavalikud, näiteks maksimaalse soovituste arvu.|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a>Maksmise lehele tarneaadressi mooduli lisamine ja vajalike atribuutide seadistamine

Tarneaadressi moodulit saab lisada ainult maksmise moodulisse. Lisateavet selle kohta, kuidas konfigureerida tarneaadressi moodulit ja lisada seda maksmise lehele, leiate teemast [Maksmise moodul](add-checkout-module.md).

## <a name="additional-resources"></a>Lisaressursid

[Ostukorvimoodul](add-cart-module.md)

[Ostukorvi ikooni moodul](cart-icon-module.md)

[Maksmismoodul](add-checkout-module.md)

[Makse moodul](payment-module.md)

[Tarnesuvandite moodul](delivery-options-module.md)

[Järeletulemise teabe moodul](pickup-info-module.md)

[Tellimuse üksikasjade moodul](order-confirmation-module.md)

[Kinkekaardi moodul](add-giftcard.md)

[Kaupluse valimise moodul](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]