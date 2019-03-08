---
title: Klienditeatiste edastamine meili teel
description: Selles teemas selgitatakse, kuidas seadistada reegleid, mis saadavad eelmääratletud sündmuste toimumisel meiliteatisi.
author: tjvass
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 314f04eec04a75aed058c9c38066738e8758f653
ms.sourcegitcommit: 440ebe14ad26574ba227d23ee8370f6b6110645b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2019
ms.locfileid: "373759"
---
# <a name="client-alert-notifications-by-email"></a>Klienditeatiste edastamine meili teel

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Rakenduses Microsoft Dynamics 365 for Finance and Operations saate määratleda kohandatud teatiste reeglid, mis jälgivad andmete filtreeritud vaateid ja saadavad eelmääratletud sündmuste toimumisel meiliteatise. Meiliteatiste saatmise suvand on saadaval kõigi toetatud teatisetüüpide puhul ja selle saab sisse lülitada ka olemasolevate teatisereeglite puhul.

Saate sisseehitatud juhtelementide abil luua teatisereeglid, mis jälgivad süsteemi pakett-tööde filtreeritud vaateid. Jälgides välja **Olek** väärtust, saate konfigureerida ka teatisereeglid, mis saadavad meili pakett-töö nurjumise korral. Pärast nende teatisereeglite loomist ei pea te äriandmete muudatuste leidmiseks enam aruandeid kontrollima. Selle asemel saate lasta Finance and Operationsi arukal muudatuste tuvastamise teenusel lasta neid enda eest jälgida.

Klienditeatised sõltuvad meili alamsüsteemist, mis on esitatud Microsoft Office’iga integratsiooni kaudu. Soovitame kasutada Simple Mail Transfer Protocoli (SMTP) pakkujat, et meiliedastus ei toetuks ainult kohalikule meilikliendile.

Teatiste saatmiseks meili teel peavad kliendid konfigureerima integreeritud meiliteenused. Meiliteatised saadetakse adressaatidele teatiseomanike nimel.

Lisateavet rakenduses Finance and Operations meili konfigureerimise kohta vt teemast [Meili konfigureerimine ja saatmine](../organization-administration/configure-email.md).

Järgmisel pildil on näidatud dialoogiboks **Teatisereegli loomine**, milles on nüüd ka valik **Saada meil**.

[![Dialoogiboks Teatisereegli loomine, kus suvandi Saada meil sätteks on valitud Jah](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> Kui suvandi **Saada meil** sätteks on valitud **Jah**, jätkub teatiste edastamine tegevuskeskusest.

## <a name="alert-notification-email-templates"></a>Teatiste meilimallid

Teenus saadab meiliteatised eelmääratletud meilimalle kasutades, mis edastavad teatise põhiandmed. Need andmed sisaldavad otselinki lehele, kus teatisereegel määratleti.

Järgmisel pildil on näidatud teatiste struktuur, kui need on meili teel vastu võetud.

[![Mallipõhised teatised kirje loomise, välja muutmise ja malli kustutamise kohta](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)
