---
title: Tarneaadressi moodul
description: See teema hõlmab tarneaadressi moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce konfigureerida.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6a5eb69c7746be419779b1a844ee35ec375a324c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985632"
---
# <a name="shipping-address-module"></a>Tarneaadressi moodul

[!include [banner](includes/banner.md)]

See teema käsitleb tarneaadressi moodulit ja seletab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce konfigureerida.

## <a name="overview"></a>Ülevaade

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

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a>Maksmise lehele tarneaadressi mooduli lisamine ja vajalike atribuutide seadistamine

Tarneaadressi moodulit saab lisada ainult maksmise moodulisse. Lisateavet selle kohta, kuidas konfigureerida tarneaadressi moodulit ja lisada seda maksmise lehele, leiate teemast [Maksmise moodul](add-checkout-module.md).

## <a name="additional-resources"></a>Lisaressursid

[Ostukorvimoodul](add-cart-module.md)

[Ostukorvi ikooni moodul](cart-icon-module.md)

[Maksmismoodul](add-checkout-module.md)

[Makse moodul](payment-module.md)

[Tarnesuvandite moodul](delivery-options-module.md)

[Järgi tulemise teabe moodul](pickup-info-module.md)

[Tellimuse üksikasjade moodul](order-confirmation-module.md)

[Kinkekaardi moodul](add-giftcard.md)
