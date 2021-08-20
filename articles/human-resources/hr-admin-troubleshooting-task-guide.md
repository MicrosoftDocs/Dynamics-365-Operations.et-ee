---
title: Tegevuse juhiste salvestamine LCS-i ja nende taasesitamine
description: Selles artiklis selgitatakse, kuidas salvestada tegevusjuhiseid teenusesse Microsoft Dynamics Lifecycle Services (LCS) ja neid seejärel taasesitada.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e8cf6338e17c9d4f0f50e5c36291ce4f81800f76951e873f2e0cf435cc3cc97e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713074"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a>Tegevuse juhiste salvestamine LCS-i ja nende taasesitamine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Keskkonna üksikasjad** 

Microsoft Dynamics 365 Human Resources, mis on juurutatud teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu

**Väljasta**

Klient soovib salvestada uusi tegevuse salvestisi oma LCS-i projekti ja seejärel salvestatud tegevuse juhiseid taasesitada.

**Eraldusvõime**

Tegevuse salvestise salvestamiseks LCS-i tehke järgmist.

1. Logige LCS-i sisse ja valige projekt.
2. Valige paan **Äriprotsesside modelleerija**.
3. Vaadake lehte jaotises Värskendatud BPM-kogemus.
4. Valige teek ja valige seejärel **Kopeeri**.
5. Sisestage äriprotsesside modelleerija (BPM) mudeli jaoks nimi.
6. Logige rakendusse Human Resources teenuses LCS sisse.
7. Sisestage väljale **Otsing** suvand **spikker**. Teenuse Lifecycle Services spikker on avatud.
8. Valige teenuse Lifecycle Services spikri konfiguratsiooni jaoks nupp **Värskenda**.

    Ilmuma peaks uus aktiivsena kuvatav BPM-i teek.

9. Sulgege leht.
10. Looge tegevuse salvestis.
11. Kui olete lõpetanud, valige **Salvesta teenusesse Lifecycle Services**.

    ![Salvesta teenusesse Lifecycle Services.](media/task-guides.png)

12. Valige BPM-i teek ja sõlm, kuhu tegevuse salvestis salvestada.

Tegevuse juhise taasesitamiseks LCS-ist tehke järgmist.

1. Käivitage tegevuse salvestaja.
2. Valige **Ava LCS-ist**.
3. Valige salvestatud tegevuse juhist omavad teek ja BPM-i sõlm.
4. Avage tegevuse juhis.


[!INCLUDE[footer-include](../includes/footer-banner.md)]