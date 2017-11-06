---
title: "Kulutöövoog"
description: "Selles teemas selgitatakse, kuidas saab kasutada rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, töövoosüsteemi kuluaruannete ülevaatamisprotsessi seadistamiseks kuluhalduses."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2c2e01d4da04cd24c2df1690e6e354e1c03cb50d
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="expense-workflow"></a>Kulutöövoog

[!include[banner](../includes/banner.md)]

Saate kasutada rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, töövoosüsteemi kuluaruannete ülevaatamisprotsessi seadistamiseks kuluhalduses. Saate seadistada töövoo, mis kasutab järgmisi kriteeriume määramiseks, kes kuluaruandeid kinnitab.

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
