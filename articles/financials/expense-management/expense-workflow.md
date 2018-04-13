---
title: "Kulutöövoog"
description: "Selles teemas selgitatakse, kuidas saab kasutada rakenduse Microsoft Dynamics 365 for Finance and Operations töövoosüsteemi kuluaruannete ülevaatamisprotsessi seadistamiseks kuluhalduses."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 6ee607f723659a5b6ecd655ba4fdfca35a4c582d
ms.contentlocale: et-ee
ms.lasthandoff: 03/26/2018

---

# <a name="expense-workflow"></a>Kulutöövoog

[!INCLUDE [banner](../includes/banner.md)]

Saate kasutada rakenduse Microsoft Dynamics 365 for Finance and Operations töövoosüsteemi kuluaruannete ülevaatamisprotsessi seadistamiseks kuluhalduses. Saate seadistada töövoo, mis kasutab järgmisi kriteeriume määramiseks, kes kuluaruandeid kinnitab.

- Töötaja aruandlushierarhia ja eelmääratud kinnituslimiidid
- Mitmetasandiline kinnitamine, mis toetab vahepealseid kinnitajaid ja lõplikku kinnitajat
- Finantsdimensioonid ja vastutus projekti eest
- Määramine konkreetsetele kasutajatele või kasutajagruppidele

Töövoo kinnitusi saab luua kuluaruannetele, reisiplaanidele, avansimaksetele ja käibemaksu (KM) korvamisele.

**Näide**

Järgmine protsess on kuluaruande kuluhalduse töövoo näide.

1. Töötaja koostab ja salvestab kuluaruande.
2. Töötaja esitab kuluaruande kinnitamiseks. Kinnitaja tuvastatakse töövoo seadistamise ajal määratud reeglite põhjal.
3. Kinnitaja saab teate, et kuluaruanne on kinnitamiseks valmis. Kinnitaja vaatab kuluaruande üle ja veendub, et järgmised tingimused on täidetud.

    - Kulud ei riku ühtegi kulupoliitikat. Kui kulu rikub mõnda poliitikat, siis kontrollib kinnitaja, et kuluaruanne sisaldaks sobivat ärilist põhjendust.
    - Elektroonilised kviitungid on kuluaruandega seotud.

4. Kinnitaja kinnitab kuluaruande.
5. Kuluaruanne määratakse sisestamiseks ostureskontro koordinaatorile.
6. Tehakse üks järgmistest toimingutest, olenevalt sellest, kas automaatne sisestamine on konfigureeritud.

    - Kui automaatne sisestamine on konfigureeritud, töödeldakse kuluaruannet maksmiseks ja kuluaruande olekut muudetakse.
    - Kui automaatne sisestamine ei ole konfigureeritud, kontrollib ostureskontro koordinaator, et kõik originaalkviitungid oleksid esitatud ja et kviitungid oleksid kooskõlas kuluaruandel olevate kuludega. Kontrollida tuleb ka kõigi kuluaruandele sisestatud maksukoodide õigsust.

Kui need nõuded on kontrollitud, siis kuluaruanne sisestatakse.

Pärast kuluaruande sisestamist autoriseeritakse kuluaruande makse ja kulud hüvitatakse töötajale.

