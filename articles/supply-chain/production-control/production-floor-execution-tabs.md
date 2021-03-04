---
title: Tootmisosakonna käivitusliidese kujundamine
description: See teema kirjeldab, kuidas kujundada kasutajaliidese sisu iga konfiguratsiooni jaoks.
author: johanhoffmann
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 81c5c83128bb81523dee6ede549eece7b0d80e30
ms.sourcegitcommit: d9d1ddce6a334ade8b32b5ea3ac4c1e1a8f72715
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664268"
---
# <a name="design-the-production-floor-execution-interface"></a>Tootmisosakonna käivitusliidese kujundamine

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Saate kujundada kasutajaliidese sisu iga konfiguratsiooni jaoks, mida kasutab tootmisosaoknna käivitusliides. Näiteks võib ühe tööraku töötajal olla vaja avada tööjuhiseid mis on vajalikud, samas kui teises töörakus ei ole juhised vajalikud. Sel juhul tuleb luua kaks konfiguratsiooni, üks nupuga, et avada dokumendi manused, ja üks ilma selle nuputa.

## <a name="design-a-tab"></a>Vahekaardi kujundamine

Lehel **Tootmisosakonna käivituse konfigureerimine** saate luua ja konfigureerida vahekaarte, tehes toimingupaanil valiku **Vahekaartide kujundamine**.

Iga vahekaart on jagatud neljaks osaks, nagu on näha järgmisel joonisel.

![Vahekaardi paigutus](media/pfe-tab-layout.png "Vahekaardi paigutus")

Joonisel kuvatakse järgmised elemendid.

1. Põhitööriistariba
1. Lisatööriistariba
1. Põhivaade
1. Üksikasjalik vaade

Uue vahekaardi loomiseks ja konfigureerimiseks toimige järgmiselt.

1. Avage **Tootmise juhtimine &gt; Häälestus &gt; Tootmise käivitamine**.

1. Lehe **Vahekaartide kujundamine** avamiseks valige toimingupaanil **Vahekaartide kujundamine**.

    ![Vahekaartide kujundamise leht](media/pfe-design-tabs.png "Vahekaartide kujundamise leht")

1. Valige Toimingupaanil suvand **Uus**.

1. Määrake lehe päises järgmised sätted.

    - **Vahekaardi nimi** – määrake vahekaardi nimi.
    - **Põhivaade** – valige üks kahest eelnevalt määratletud tööloendist (*Aktiivsed tööd* või *Kõik tööd*).
    - **Üksikasjalik vaade** – valige tühi väärtus või **töö üksikasjad**. Kui valite tühja väärtuse, ei ole vahekaardil ühtegi üksikasjalikku vaadet. Kui valite **töö üksikasjad**, sisaldab üksikasjalik vaade põhivaates tööde loendis valitud töö üksikasjalikku kirjeldust.

1. Valige jaotises **Põhitööriistariba** nupud, mis peaksid põhitööriistaribal olema. Veerus **Saadaolevad toimingud** kuvatakse loend kõigist nuppudest, mida saab lisada. Veerg **Valitud tegevused** näitab kõigi praegusse konfiguratsiooni kaasatud nuppude loendit. Kasutage nuppe veergude vahel, et teisaldada valitud üksused veergude vahel vastavalt vajadusele. Kasutage veeru **Valitud toimingud** kõrval üles- ja allanuppe, et kontrollida, millises järjekorras on nupud kasutajaliideses esitatud.

1. Valige jaotises **Lisa** **tööriistariba** nupud, mis peaksid lisatööriistaribal olema. Veerus **Saadaolevad toimingud** kuvatakse loend kõigist nuppudest, mida saab lisada. Veerg **Valitud tegevused** näitab kõigi praegusse konfiguratsiooni kaasatud nuppude loendit. Kasutage nuppe veergude vahel, et teisaldada valitud üksused veergude vahel vastavalt vajadusele. Kasutage veeru **Valitud toimingud** kõrval üles- ja allanuppe, et kontrollida, millises järjekorras on nupud kasutajaliideses esitatud.

## <a name="associate-a-tab-with-a-configuration"></a>Vahekaardi seostamine konfiguratsiooniga

Kui olete kõik vajalikud vahekaardid loonud, saate need konfiguratsiooniga seostada.

1. Avage **Tootmise juhtimine &gt; Häälestus &gt; Tootmisosakonna käivituse konfigureerimine**.

    ![Tootmisosakonna käitus](media/pfe-config-prod-floor-execution.png "Tootmisosakonna käitus")

1. Valige kiirkaardil **Vahekaartide valimine** käsk **Lisa**.

1. Ruudustikku lisatakse uus rida. Selle uue rea jaoks valige vahekaardi nimi, mida soovite konfiguratsiooni lisada.

1. Jätkake täiendavate vahekaartide lisamist vastavalt vajadusele.

1. Vahekaartide korraldamiseks vastavalt vajadusele kasutage nuppe **Nihuta üles** ja **Nihuta alla**. Vahekaardid kuvatakse ülaltoodud kuvatõmmisel kuvatud järjekorras vasakult paremale (ülemine vahekaart kuvatakse vasakul).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]