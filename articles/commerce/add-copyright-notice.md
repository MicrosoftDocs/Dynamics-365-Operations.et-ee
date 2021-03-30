---
title: Autoriõiguste teatise lisamine
description: Selles teemas kirjeldatakse kuidas oma e-kaubanduse veebisaidile autoriõiguse teatist lisada.
author: psimolin
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2ea04854636fdd0c2b3223bb19d5f06a19836151
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206363"
---
# <a name="add-a-copyright-notice"></a>Autoriõiguste teatise lisamine

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse kuidas oma e-kaubanduse veebisaidile autoriõiguse teatist lisada.

## <a name="prerequisites"></a>Eeltingimused

Enne saidile autoriõiguse teatise lisamist peavad teil olema järgmised üksused.

- Jagatud jaluse fragmenti sisaldav mall.
- Seda malli kasutav leht.

## <a name="add-a-copyright-notice"></a>Autoriõiguste teatise lisamine

Iga konkreetset malli kasutava lehe allossa autoriõiguse teatise lisamiseks toimige järgmiselt.

1. Avage **Fragmendid** ja valige seejärel **Uus**.
1. Valige dialoogiboksis **Uus fragment** moodul **Jalus** ja pange fragmendile nimi. Sisestage näiteks **Jalus-autoriõigus**.
1. Valige nupp **OK**.
1. Navigeerimispaanil valige kolmikpunkti nupp (**...**) suvandi **Jalus** kõrval ja valige seejärel **Lisa moodul**.
1. Dialoogiaknas valige suvand **Jaluse kategooria** ja seejärel valige nupp **OK**.
1. Navigeerimispaanil valige kolmikpunkti nupp suvandi **Jaluse kategooria** kõrval ja valige seejärel **Lisa moodul**.
1. Dialoogiaknas valige suvand **Tekstiplokk** ja seejärel valige nupp **OK**.
1. Valige navigeerimispaanil **Tekstiplokk**.
1. Lisage paremal atribuutide paanil väljale **Lõik** oma autoriõiguse sõnum. Sisestage näiteks **(C) Fabrikam 2019**.
1. Valige **Salvesta**, valige **Lõpeta redigeerimine** ja valige seejärel **Avalda**.
1. Valige suvand **Mallid**, valige mall ja seejärel käsk **Redigeeri**.
1. Jaotises **Lehe liigendus** laiendage suvandit **Kehatekst** ja laiendage seejärel suvandit **Vaikeleht**.
1. Valige suvandi **Jaluse pesa** kõrval kolmikpunkti nupp ja seejärel valige käsk **Lisa fragment**.
1. Valige varem loodud fragment ja seejärel valige käsk **Vali**.
1. Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

Autoriõiguse teatist sisaldav jalus kuvatakse automaatselt kõigi valitud malli kasutavate lehtede allosas.

## <a name="additional-resources"></a>Lisaressursid

[Logo lisamine](add-logo.md)

[Saidi kujunduse valimine](select-site-theme.md)

[CSS-i alistusfailidega töötamine](css-override-files.md)

[Leheikooni lisamine](add-favicon.md)

[Tervitussõnumi lisamine](add-welcome-message.md)

[Saidile keelte lisamine](add-languages-to-site.md)

[Telemeetria toetamiseks saidile skriptikoodi lisamine](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]