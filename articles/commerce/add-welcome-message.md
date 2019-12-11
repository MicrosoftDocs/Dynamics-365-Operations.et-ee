---
title: Tervitussõnumi lisamine
description: See teema kirjeldab, kuidas lisada oma Microsoft Dynamics 365 Commerce veebisaidile tervitussõnum.
author: psimolin
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 25a4e91646916b03c8a138fc713577f429ab633c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697378"
---
# <a name="add-a-welcome-message"></a>Tervitussõnumi lisamine

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas lisada oma Microsoft Dynamics 365 Commerce veebisaidile tervitussõnum.

## <a name="overview"></a>Ülevaade

E-kaubanduse veebisaidi tervitussõnum võib teavitada külastajaid käimasolevatest allahindlustest, saidi uuendustest või hooajaliste kollektsioonide saadavusest. Tervitussõnum määratakse teatisemooduli abil.

Teatisemoodul tuleks lisada päise fragmendi pessa **Tõrke-/teabeteated**. Teatisemoodul võimaldab teil määrata kuvatava teksti, teksti värvi ja joonduse. Samuti võimaldab see määrata, kas saidi külastajad võivad sõnumi lõpetada.

Kui jagatud päise fragmenti on lisatud tervitussõnum, kuvatakse see igal lehel, mis kasutab malli, kus seda jagatud päise fragmenti kasutatakse.

Oma saidile tervitussõnumi lisamiseks toimige järgmiselt.

1. Avage rakenduses Dynamics 365 Commerce oma sait.
1. Valige suvand **Fragmendid**.
1. Valige päise fragment, millele sõnum lisada.
1. Laiendage liigendpuus suvandit **Tõrke-/teabeteated**.
1. Valige teatise moodul.

    Kui teatise moodulit pole veel olemas, valige kolmikpunkti nupp (**...**) suvandi **Tõrke-/teabeteated** kõrval ja seejärel valige käsk **Lisa moodul**. Valige teatise moodul ja valige seejärel **OK**.

1. Valige parempoolsel atribuudipaanil vahekaardil **Andmed** suvand **Lisa andmeallikas**ja valige seejärel suvand **Sisu**.
1. Sisestage väljale **Sisendtekst** tervitussõnumi tekst.
1. Salvestage pease fragment, kontrollige seda ja avaldage see.

Iga valitud päise fragmenti kasutava saidi lehe ülaosas ilmub nüüd tervitussõnum.

## <a name="additional-resources"></a>Lisaressursid

[Logo lisamine](add-logo.md)

[Saidi kujunduse valimine](select-site-theme.md)

[Leheikooni lisamine](add-favicon.md)

[Autoriõiguste teatise lisamine](add-copyright-notice.md)

[Saidile keelte lisamine](add-languages-to-site.md)

[Telemeetria toetamiseks saidile skriptikoodi lisamine](add-telemetry.md)

