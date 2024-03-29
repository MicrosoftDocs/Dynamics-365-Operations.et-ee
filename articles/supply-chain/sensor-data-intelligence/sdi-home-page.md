---
title: Sensor Data Intelligence’i avaleht
description: See artikkel annab ülevaate Anduri andmeteabest. Organisatsioonid saavad seda funktsiooni Dynamics 365 Supply Chain Management kasutada Microsofti äriprotsesside juhtida vastavalt tootmisplaani masinate ja seadmete reaktsiooni internetile (IoT).
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: ba030364056db8b0524de22aacbc6528ef77813b
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689853"
---
# <a name="sensor-data-intelligence-home-page"></a>Sensor Data Intelligence’i avaleht

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Microsofti anduri Dynamics 365 Supply Chain Management andmeteave võimaldab organisatsioonidel juhtida hankeahela halduses äriprotsesse, mis põhinevad tootmispinna masinate ja seadmete infol (IoT) põhinevates seadmetes. See on IoT *intelligence’i funktsiooni* uuendatud, ümbernimetatud versioon, mis oli eelnevalt saadaval tarneahela haldamise jaoks.

Anduri andmeteave võimaldab teil teostada järgmisi ülesandeid:

- Koguge masinate ja seadmete üksikasju, et värskendada hooldusvara loenduriväärtusi tarneahela halduses ja juhtida ennustushooldust.
- Seadistage lahendus, kasutades lihtsat põhilist Microsoft Dynamics viisardit komponentide käsitsi installimise ja konfigureerimise asemel elutsükli teenustes (LCS).
- Juurutage komponendid oma kordustellimusel, nii et teil on paindlikum Azure’i komponentide haldamine.
- Konfigureerige, kaaluge ja laiendage lahendust Kui Äriloogikat, mis töötab Azure’i komponentidel. Neid komponente hallatakse nüüd teie enda kordustellimusel. Seetõttu saate neid vastavalt oma kordumatutele ärivajadustele kohandada.

## <a name="business-scenarios"></a>Äristsenaariumid

Anduri andmeteave võimaldab mitut tüüpi funktsioone, millest igaüks on esindatud konkreetse *stsenaariumiga* süsteemis. Iga stsenaarium annab süsteemis täpsema konfiguratsioonivalikute komplekti, nagu kirjeldatud järgmises tabelis.

| Stsenaarium | Kirjeldus |
|---|---|
| [Vara seisakuaeg](sdi-scenario-asset-downtime.md) | Jälgida masina varade efektiivsust, kasutades anduriandmeid masina tööea jälgimiseks. |
| [Varahaldus](sdi-scenario-asset-maintenance.md) | Minimeerige hoolduskulusid ja pikendage vara eluiga, parandades hooldusplaane, mis põhinevad masina varade kriitiliste kontrollpunktide lugemistel. |
| [Arvuti olek](sdi-scenario-equipment-downtime.md) | Tagage operatsiooni efektiivsus, kasutades andurnäiduid planeerijate teavitamiseks masinakatkestustest ja pakub võimalusi võimalike viivituste maandamiseks. |
| [Toote kvaliteet](sdi-scenario-product-quality.md) | Tagage tootepartiide kvaliteet, võrreldes iga tootepartii tegelike atribuutide (nt temperatuurid, temperatuur või kohandatud määratletud kvaliteedimõõdulised) andurinäidud. Süsteem teavitab kasutajaid hälvete ilmnemisel. |
| [Tootmise viivitused](sdi-scenario-production-delays.md) | Kasutage andurinäiduid, et võrrelda tegelikku tsükli aega plaanitud tsükli ajaga ja teavitada ülevaatajad, kui tootmist ei ole graafikus. Seejärel saavad ülevaatajad vastavalt vajadusele tagada maksimaalse operatsiooni tõhusus. |

## <a name="architecture"></a>Arhitektuur

Järgmine aarhitektuurdiagramm annab ülevaate lahendusest ja selle komponentidest.

![Anduri andmeteabe aarhitektuurdiagramm.](media/sdi-architecture.png "Koosteandmete teabe aarhitektuurdiagramm")
