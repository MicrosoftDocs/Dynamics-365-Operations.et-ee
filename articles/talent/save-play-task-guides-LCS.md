---
title: Tegevuse juhiste salvestamine LCS-i ja nende taasesitamine
description: "Selles teemas selgitatakse, kuidas salvestada tegevuste juhiseid Microsoft Dynamicsi teenusesse Lifecycle Services (LCS) ja neid seejärel taasesitada."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 40b4c3154a04a557b8a670e1f1ae3722c71122fe
ms.contentlocale: et-ee
ms.lasthandoff: 12/04/2018

---

# <a name="save-task-guides-to-lcs-and-replay-them"></a>Tegevuse juhiste salvestamine LCS-i ja nende taasesitamine

[!include [banner](includes/banner.md)]

**Keskkonna üksikasjad** 

Microsoft Dynamics 365 for Talent, mis juurutati Microsoft Dynamicsi teenuse Lifecycle Services (LCS) kaudu

**Probleem**

Klient soovib salvestada uusi tegevuse salvestisi enda LCS-i projekti ja seejärel salvestatud tegevuse juhiseid taasesitada.

**Eraldusvõime**

Tegevuse salvestise salvestamiseks LCS-i tehke järgmist.

1. Logige LCS-i sisse ja valige projekt.
2. Valige paan **Äriprotsesside modelleerija**.
3. Vaadake lehte jaotises Värskendatud BPM-kogemus.
4. Valige teek ja valige seejärel **Kopeeri**.
5. Sisestage äriprotsesside modelleerija (BPM) mudeli jaoks nimi.
6. Logige LCS-ist sisse Talenti.
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

