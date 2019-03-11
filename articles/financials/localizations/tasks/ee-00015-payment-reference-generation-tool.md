---
title: EE-00015 Makseviite loomise tööriist
description: See protseduur juhatab teid läbi makseviidete koostamise protseduuri.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccount, LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Estonia
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 52940dedc05765d376ecc9e2eb52fa9d9c83e4fa
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "370584"
---
# <a name="ee-00015-payment-reference-generation-tool"></a>EE-00015 Makseviite loomise tööriist

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

