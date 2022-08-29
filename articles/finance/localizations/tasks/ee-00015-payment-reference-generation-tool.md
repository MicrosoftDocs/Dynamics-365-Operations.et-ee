---
title: EE-00015 Makseviite loomise tööriist
description: See protseduur juhatab teid läbi makseviidete koostamise protseduuri.
author: AdamTrukawka
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Estonia
ms.author: atrukawk
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: MainAccount, LedgerJournalTable, LedgerJournalTransDaily
ms.openlocfilehash: 99382240e631bfa4307ceb6f2de4ca34610f5e8c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282373"
---
# <a name="ee-00015-payment-reference-generation-tool"></a>EE-00015 Makseviite loomise tööriist

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
