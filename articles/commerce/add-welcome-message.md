---
title: Tervitussõnumi lisamine
description: See teema kirjeldab, kuidas lisada oma Microsoft Dynamics 365 Commerce veebisaidile tervitussõnumi.
author: psimolin
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e61f43eca7d1343d020e1c01b5b1140f07b63c6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797379"
---
# <a name="add-a-welcome-message"></a>Tervitussõnumi lisamine

[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas lisada oma Microsoft Dynamics 365 Commerce veebisaidile tervitussõnumi.

E-kaubanduse veebisaidi tervitussõnum võib teavitada külastajaid käimasolevatest allahindlustest, saidi uuendustest või hooajaliste kollektsioonide saadavusest. Tervitussõnum määratakse teatisemooduli abil.

Teatisemoodul tuleks lisada päise fragmendi pessa **Tõrke-/teabeteated**. Teatisemoodul võimaldab teil määrata kuvatava teksti, teksti värvi ja joonduse. Samuti võimaldab see määrata, kas saidi külastajad võivad sõnumi lõpetada.

Kui jagatud päise fragmenti on lisatud tervitussõnum, kuvatakse see igal lehel, mis kasutab malli, kus seda jagatud päise fragmenti kasutatakse.

Oma saidile tervitussõnumi lisamiseks toimige järgmiselt.

1. Liikuge kaubanduse saidiehitajas oma saidile.
1. Valige suvand **Fragmendid**.
1. Valige päise fragment, millele sõnum lisada.
1. Laiendage liigendpuus suvandit **Tõrke-/teabeteated**.
1. Valige teatise moodul ja valige seejärel **OK**. Kui teatise moodulit pole veel olemas, valige esiteks kolmikpunkti nupp (**...**) suvandi **Tõrke-/teabeteated** kõrval ja seejärel valige käsk **Lisa moodul**.
1. Valige parempoolsel atribuudipaanil vahekaardil **Andmed** suvand **Lisa andmeallikas** ja valige seejärel suvand **Sisu**.
1. Sisestage väljale **Sisendtekst** tervitussõnumi tekst.
1. Valige **Salvesta**, valige päise fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**. 

Iga valitud päise fragmenti kasutava saidi lehe ülaosas ilmub nüüd tervitussõnum.

## <a name="additional-resources"></a>Lisaressursid

[Logo lisamine](add-logo.md)

[Saidi kujunduse valimine](select-site-theme.md)

[CSS-i alistusfailidega töötamine](css-override-files.md)

[Leheikooni lisamine](add-favicon.md)

[Autoriõiguste teatise lisamine](add-copyright-notice.md)

[Saidile keelte lisamine](add-languages-to-site.md)

[Telemeetria toetamiseks saidile skriptikoodi lisamine](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
