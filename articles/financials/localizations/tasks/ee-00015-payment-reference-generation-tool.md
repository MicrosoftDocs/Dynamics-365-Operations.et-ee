--- 
title: "Makseviite genereerimise tööriist (Ida-Euroopa)"
description: "See protseduur juhatab teid läbi makseviidete koostamise protseduuri."
author: v-oloski
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Estonia
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 187f11c79d8e1b25fa1f93178fcfb41569d47026
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="payment-reference-generation-tool-eastern-europe"></a>Makseviite genereerimise tööriist (Ida-Euroopa)

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur juhatab teid läbi makseviidete koostamise protseduuri. Ülesande loomisel kasutati demoettevõtte DEMF, mille juriidilise isiku esmase aadressi riigiks/regiooniks on määratud Eesti, andmeid. See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.


## <a name="specify-a-number-sequence-for-payment-references"></a>Määratlege viitenumbrite jaoks numbriseeria vorming.
1. Minge jaotisse Müügireskontro > Seadistus > Müügireskontro parameetrid.
2. Klõpsake vahekaarti Numbriseeriad.
3. Viiteveerus. Leidke ja valige kirje "Makseviide".
4. Sisestage või valige väärtus väljal Numbriseeria kood.
    * Võite valida eraldi, vastloodud numbrilise ja pideva numbriseeria. Demo eesmärgil kasutage "Acco_18".  
5. Klõpsake nuppu Salvesta.

## <a name="create-payment-reference-numbers"></a>Loo makse viitenumbrid
1. Avage Müügireskonto > Perioodilised ülesanded > Viitenumbrite loomine.
2. Väljal Viitenumbrite loomine valige Jah.
    * Juba klientidele määratud viitenumbrite kustutamiseks valige käsk "Kustuta maksete viitenumbrid". Võite piirata klientide hulka, kellelt soovite eemaldada või kellele lisada viitenumbri. Selleks kasutage jaotist "Kirjenda kaasamiseks" ja määrake klientidele või kliendirühmadele kriteeriumid.  
3. Klõpsake nuppu OK.


