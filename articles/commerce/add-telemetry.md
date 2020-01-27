---
title: Telemeetria toetamiseks saidile skriptikoodi lisamine
description: Selles teemas kirjeldatakse saidi lehtedele kliendipoolse skriptikoodi lisamist, et toetada kliendipoolset telemeetriat.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 79d0e11946f3c6f4704d3a726d33de0378eb53bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914535"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Telemeetria toetamiseks saidile skriptikoodi lisamine

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse saidi lehtedele kliendipoolse skriptikoodi lisamist, et toetada kliendipoolset telemeetriat.

## <a name="overview"></a>Ülevaade

Veebianalüüs on oluline tööriist, kui soovite mõista, kuidas kliendid teie saidiga suhtlevad, ja teha otsuseid, mis aitavad maksimaalse teisenduse kogemust optimeerida. Saadaval on palju veebianalüüsi pakette, et aidata teid nende eesmärkide saavutamisel, nagu Google Analytics, Clicky, Moz Analytics ja KISSMetrics. Enamik veebianalüüsi pakette nõuavad, et lisaksite oma saidi kõikidele lehtedele HTML-i elemendile **\<head\>** kliendipoolse skriptikoodi.

> [!NOTE]
> Selle teema juhised rakenduvad ka teistele kohandatud kliendipoolsetele funktsioonidele, mida Microsoft Dynamics 365 Commerce ei paku.

## <a name="create-a-reusable-fragment-for-your-script-code"></a>Skriptikoodi jaoks taaskasutatava fragmendi loomine

Pärast seda, kui loote oma skriptikoodi jaoks fragmenti, saate seda oma saidil kõikidel lehtedel uuesti kasutada.

1. Avage **Fragmendid \> Uus lehe fragment**.
2. Valige suvand **Väline skript**, sisestage fragmendi nimi ja valige seejärel **OK**.
3. Valige fragmendi hierarhias äsja loodud fragmenti jaoks **skripti sisestaja** mooduli alam.
4. Lisage parempoolsel atribuudipaanil oma kliendipoolne skript ja määrake vastavalt vajadusele teised konfiguratsiooni suvandid.

## <a name="add-the-fragment-to-templates"></a>Mallile fragmendi lisamine

1. Avage **Mallid** ja avage lehtede mall, millele soovite oma skriptikoodi lisada.
2. Laiendage vasakpoolsel paanil malli hierarhiat, et kuvada pesa **HTML-i pea**.
3. Valige pesa **HTML-i päis** jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa fragment**.
4. Valige fragment, mille lõite oma skriptikoodi jaoks.
5. Salvestage mall ja registreerige see.

> [!NOTE]
> Pärast lõpetamist peate fragmendi ja põhimalli avaldama. 

## <a name="additional-resources"></a>Lisaressursid

[Logo lisamine](add-logo.md)

[Saidi kujunduse valimine](select-site-theme.md)

[CSS-i alistusfailidega töötamine](css-override-files.md)

[Leheikooni lisamine](add-favicon.md)

[Tervitussõnumi lisamine](add-welcome-message.md)

[Autoriõiguste teatise lisamine](add-copyright-notice.md)

[Saidile keelte lisamine](add-languages-to-site.md)

