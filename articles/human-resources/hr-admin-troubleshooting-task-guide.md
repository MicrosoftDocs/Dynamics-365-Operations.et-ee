---
title: Tegevuse juhiste salvestamine LCS-i ja nende taasesitamine
description: Selles artiklis selgitatakse, kuidas salvestada tegevusjuhiseid teenusesse Microsoft Dynamics Lifecycle Services (LCS) ja neid seejärel taasesitada.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7d6102bafc9b55f9eff05bfc4a63c177c6548694
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463258"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a>Tegevuse juhiste salvestamine LCS-i ja nende taasesitamine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Keskkonna üksikasjad** 

Microsoft Dynamics 365 Human Resources, mis on juurutatud teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu

**Väljastamine**

Klient soovib salvestada uusi tegevuse salvestisi enda LCS-i projekti ja seejärel salvestatud tegevuse juhiseid taasesitada.

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

    ![Salvesta teenustesse Lifecycle Services](media/task-guides.png)

12. Valige BPM-i teek ja sõlm, kuhu tegevuse salvestis salvestada.

Tegevuse juhise taasesitamiseks LCS-ist tehke järgmist.

1. Käivitage tegevuse salvestaja.
2. Valige **Ava LCS-ist**.
3. Valige salvestatud tegevuse juhist omavad teek ja BPM-i sõlm.
4. Avage tegevuse juhis.


[!INCLUDE[footer-include](../includes/footer-banner.md)]