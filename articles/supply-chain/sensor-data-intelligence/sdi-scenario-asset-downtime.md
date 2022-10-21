---
title: Vara seisakuaja stsenaarium
description: See artikkel kirjeldab vara ületunnitöö stsenaariumi, mis võimaldab teil kasutada koosteandmeid põhivarade kättesaadavuse jälgimiseks.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetObjectProductionStop
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: b82d757d1e69203012949bc397220fa42ada4ac2
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689425"
---
# <a name="the-asset-downtime-scenario"></a>Vara seisakuaja stsenaarium

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Vara ületunnitöö stsenaarium loob hoolduse downtime’i kirje, kui arvutilt ei saadi kindlaksmääratud ajapiiri jooksul pärast viimast signaali. Stsenaarium nõuab, et te sobite masinaga seadmega, mis edastab aeg-ajalt signaali Azure IoT keskusele, kui masin töötab, kuid ei saada signaali, kui masin ei tööta.

## <a name="set-up-the-asset-downtime-scenario"></a>Vara ületunnitöö stsenaariumi häälestamine

Järgige neid samme vara ettemaksmisstsenaariumi *häälestamiseks* tarneahela halduses.

1. Stsenaariumite **lehe \> avamiseks \> minge varahalduse \> seadistuse anduri** andmeteabe **stsenaariumite** lehele.
2. Vara ettemaks **stsenaariumi kastis** valige konfigureerimisviisard **selle** stsenaariumi jaoks häälestusviisardi avamiseks.
3. **Lehel Andurid** valige anduri **lisamiseks** ruudustikule uus. Seejärel määrake selle jaoks järgmised väljad:

    - **Anduri ID – sisestage selle anduri ID**, mida kasutate. (Kui kasutatePakkumiste PI Azure IoT Online Simulaator ja olete seadistanud selle vastavalt kirjeldusele [Simuleeritud andur testimiseks seadistage, sisestage](sdi-set-up-simulated-sensor.md)*AssetDownTime*.)
    - **Anduri** kirjeldus – sisestage anduri kirjeldus.

4. Korrake eelmist sammu iga lisaanduri korral, mida soovite nüüd lisada. Saate igal ajal tagasi tulla ja lisada rohkem anduriid.
5. Valige **Edasi**.
6. **Jaotises Andurid** ärikirjete **vastendamise lehel** valige kirje ühe äsja lisatud andurite jaoks.
7. Jaotises Ärikirjete **vastendamine** valige **suvand** Uus, et lisada rida ruudustikku.
8. Seadke uuel real välja **Ärikirje väärtuseks** ressurss, mida kasutate seireks valitud andurit. (Kui kasutate demoandmeid, valige *AK-101, Air Liin 1* puhul)
9. Valige **Edasi**.
10. Vara ületunnitöö **läve** lehel määrake, kui kaua pärast viimast signaali peab süsteem ootama, enne kui saadab vara ettemakstud aja. Läve määratlemiseks on kaks võimalust:

    - **Vaikelävi (minutites)** – seadistage see väli vaikeläve määratlemiseks. See väärtus rakendub kõigile ressurssidele, kus välja **Teatise lävi (minutites)** väärtuseks on seatud kaks minutit või vähem. Minimaalne väärtus on *2* (minutites).
    - **Lävi, mis määrab, et masin ei vasta (minutites)** – iga ruudustikus ressursi puhul, kus ei soovi vaikeläve kasutada, sisestage sellele väljale alistamisväärtus. Ressursid, mis on määratud kasutama lävi 2 või vähem minutit, kasutavad selle **asemel vaikeläve (minutites)** sätet.
11. Valige **Edasi**.
12. Andurite **aktiveerimise lehe** ruudustikus valige seadistatav andur ja seejärel valige **aktiveeritav**. Iga aktiveeritud anduri puhul ruudustikus kuvatakse märge veerus **Aktiivne**.
13. Valige **Lõpeta**.

## <a name="work-with-the-asset-downtime-scenario"></a>Tööta vara ettemakstud stsenaariumiga

Kui süsteem ei saa varalt signaali stsenaariumi konfiguratsioonis määratletud läve piires, loob süsteem sellele varale hoolduse ületunnitöö kirje. Juhatajad peaksid perioodiliselt üle vaatama downtime kirjed (nt üks kord iga töövahetuse jooksul) ja rakendama sobivad põhjuse koodid ja lõppajad iga downtime-registreerimise jaoks. Järgige neid samme vara hoolduse downtime-kirjete vaatamiseks:

1. Avage varahaldus **ja > > Kõik varad**.
2. Otsige ja valige vara, mida soovite üle vaadata. (Kui kasutate demoandmeid, valige *AK-101*.)
3. Tegevuspaanil **avage** **vahekaart** Vara ja valige jaotisest Töötellimused suvand Hoolduse downtime **(i),** et avada leht valitud vara hoolduse tööea kirjete jaoks.
