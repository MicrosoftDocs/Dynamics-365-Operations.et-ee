---
title: Kliendi teatiste teatamine meili teel
description: See artikkel annab teavet selle kohta, kuidas seadistada reegleid, mis saadavad eelmääratletud sündmuste asetleidvad meiliteatiste.
author: RichdiMSFT
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 469c7fdda40780d6e559819103d73d7a4e7132a1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878274"
---
# <a name="client-alert-notifications-by-email"></a>Kliendi teatiste teatamine meili teel

[!include [banner](../includes/banner.md)]

Saate määratleda kohandatud teatiste reeglid, mis jälgivad andmete filtreeritud vaateid ja saadavad eelmääratletud sündmuste toimumisel meiliteatise. Meiliteatiste saatmise suvand on saadaval kõigi toetatud teatisetüüpide puhul ja saate need sisse lülitada ka olemasolevate teatisereeglite puhul.

Saate sisseehitatud juhtelementide abil luua teatisereeglid, mis jälgivad süsteemi pakett-tööde filtreeritud vaateid. Jälgides välja **Olek** väärtust, saate konfigureerida ka teatisereeglid, mis saadavad meili pakett-töö nurjumise korral. Pärast nende teatisereeglite loomist ei pea te äriandmete muudatuste leidmiseks enam aruandeid kontrollima. Selle asemel saate lasta arukal muudatuste tuvastamise teenusel lasta neid enda eest jälgida.

Klienditeatised sõltuvad meili alamsüsteemist, mis on esitatud Microsoft Office’iga integratsiooni kaudu. Soovitame kasutada Simple Mail Transfer Protocoli (SMTP) pakkujat, et meiliedastus ei toetuks ainult kohalikule meilikliendile.

Teatiste saatmiseks meili teel peavad kliendid konfigureerima integreeritud meiliteenused. Meiliteatised saadetakse adressaatidele teatiseomanike nimel.

Lisateavet meili konfigureerimise kohta vt teemast [Meili konfigureerimine ja saatmine](../organization-administration/configure-email.md).

Järgmisel pildil on näidatud dialoogiboks **Teatisereegli loomine**, milles on nüüd ka valik **Saada meil**.

[![Dialoogiboks Teatisereegli loomine, kus suvandi Saada meil sätteks on valitud Jah.](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> Kui suvandi **Saada meil** sätteks on valitud **Jah**, jätkub teatiste edastamine tegevuskeskusest.

## <a name="alert-notification-email-templates"></a>Teatiste meilimallid

Teenus saadab meiliteatised eelmääratletud meilimalle kasutades, mis edastavad teatise põhiandmed.

Järgmisel pildil on näidatud teatiste struktuur, kui need on meili teel vastu võetud.

[![Mallipõhised teatised kirje loomise, välja muutmise ja malli kustutamise kohta.](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]