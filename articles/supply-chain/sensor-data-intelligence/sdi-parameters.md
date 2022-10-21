---
title: Sensor Data Intelligence’i parameetrid
description: See artikkel annab teavet konfiguratsioonisätete kohta, mis on saadaval Lehele Koosteandmete teabe parameetrid.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreServiceParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 5240537e3a6526ceb35253b9e68f46b1753c6a37
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689369"
---
# <a name="sensor-data-intelligence-parameters"></a>Sensor Data Intelligence’i parameetrid

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Anduriandmete **teabe parameetrite** leht annab mõned sätted, mida saate funktsiooni konfigureerimiseks kasutada. Need sätted hõlmavad Azure’i ühenduse parameetreid ja parameetrit teatiste elueale, mis saadetakse kasutajatele vastavalt alarmi mõõtmetele.

## <a name="read-and-change-connection-details-for-your-azure-iot-solution"></a>Lugege ja muutke ühenduse üksikasju oma Azure’i IoT-lahenduse jaoks.

Tavaliselt seadistate te oma Azure’i IoT lahenduse ja ühendate selle Microsoftiga Dynamics 365 Supply Chain Management **leheküljel Deploy ja Azure’i ressursside ühenduse** kaudu, mis juhib teid läbi mõlema protseduuri. (Lisateavet vt teemast [Juurutage IoT-lahendus Azure’is](sdi-deploy-iot-solution-on-azure.md).) Saate igal tarneahela halduses igal ajal ühenduse üksikasju vaadata ja redigeerida, järgides neid samme.

1. Minge süsteemihalduse **häälestuse \> andteabe \> andeinfo andmeteabe \> parameetritesse**.
1. Sisestage **vahekaardil Ajaseeria** **väljale Taasmõõdulise kaupluse ühenduse stringi** väärtus Esmane ühendusstring (StackExchange.Redis) **Azure’i IoT lahendusele,** mida soovite ühendada. Lisateavet selle väärtuse otsimise kohta vt Azure’i [IoT-lahenduse juurutamine](sdi-deploy-iot-solution-on-azure.md).
1. Vahekaardil Integratsioonid **rakenduse** kliendi **Azure AD ID väljal sisestage kliendi ID** **väärtus Azure’i IoT lahendusele,** millega soovite ühendust luua. Lisateavet selle väärtuse otsimise kohta vt Azure’i [IoT-lahenduse juurutamine](sdi-deploy-iot-solution-on-azure.md).

## <a name="set-the-lifetime-of-alert-messages"></a>Teatisesõnumite eluea saatmine

Iga kord, kui Anduri andmeteave avastab olukorra, mis nõuab kasutaja tähelepanu, saadab see teatise vastavale kasutajale. Et vältida nende teatiste kuhjamist süsteemis, peaksite need seadistama aeguma mõne päeva pärast.

1. Minge süsteemihalduse **häälestuse \> andteabe \> andeinfo andmeteabe \> parameetritesse**.
1. **Teatise salvestatud** päevade arvu saate **sisestada** vahekaardi Teatised väljale Teatise päevad. Pärast määratud aja läbimist kustutatakse teatis.
