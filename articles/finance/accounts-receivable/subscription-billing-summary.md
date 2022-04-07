---
title: Kordustellimuse arvelduse ülevaade
description: See teema kirjeldab kordustellimuse arveldust Microsoftis Dynamics 365 Finance.
author: JodiChristiansen
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-02-09
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 2796e25ec783941de381fb5ae96145eeba870bde
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462465"
---
# <a name="subscription-billing-overview"></a>Kordustellimuse arvelduse ülevaade

[!include [banner](../includes/banner.md)]

Kordustellimuse arveldamine võimaldab organisatsioonidel hallata kordustellimuste tuluvõimalusi ja korduvat arveldust arveldusgraafikute kaudu. Komplekshinna ja arveldusmudelid ning tulu eraldamine on hõlpsasti hallatavad ning neid arveldatakse ja tuvastatakse rea tasemel. Mitme elemendiga tulu eraldamine võimaldab tulu jaotamist vastama rahvusvahelistele raamatupidamisstandarditele (rahvusvaheline finantsaruandluse standard 15 IFRS 15\[\]) ja usa aktsepteeritud raamatupidamistavade (US GAAP) standarditele (raamatupidamisstandardite kodeerimise teema 606 \[ASC 606\]).

Lahendusel on kolm moodulit, mida saab eraldi kasutada. Teise võimalusena saab koos kasutada kõiki kolme moodulit.

- **Korduv lepingu arveldamine** – see moodul võimaldab korduvat arveldust ja hinnahaldust, et kontrollida hinnakujunduse ja arvelduse parameetreid, lepingu uuendamist ja konsolideeritud arveldamist.
- **Tulu ja kulu viitvõlad – see moodul eemaldab käsitsi protsessid ja sõltuvuse välissüsteemidest, haldades tulu ja lubades** reaalajas vihje igakuise korduva tulu kohta.
- **Mitme elemendiga tulu eraldamine** – see moodul aitab tulu vastavusele, käsitledes hinnakujundust ja tulu eraldamist mitme kauba vahel.

Kordustellimuse arveldamine on funktsioonihalduse **kaudu lubatud**. Kuid seda ei saa tulu tuvastamise funktsiooniga **kasutada**. Seepärast peate selle funktsiooni keelama enne kordustellimuse arveldamise lubamist.

1. Funktsioonihalduse **tööruumi** vahekaardil Kõik sisestage **filtrisse** **tulutuvastus** ja seejärel valige filtrina funktsiooni nimi.
2. Valige tulu **tuvastamise funktsioon** ja seejärel keela **.**
3. Funktsiooni **nime filtris** sisestage **kordustellimuse arveldamine** ja seejärel valige mooduli filter.
4. Valige kordustellimuse **arveldusfunktsioon** ja seejärel **luba**.
5. Valige eelmisest loendist üks kolmest moodulist ja seejärel valige **Luba**. Korrake seda sammu iga teise mooduli puhul.

    > [!IMPORTANT]
    > Kordustellimuse **arveldusfunktsioon** peab olema lubatud enne, kui saate lubada mis tahes kolmest moodulist.
