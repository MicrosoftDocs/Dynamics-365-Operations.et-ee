---
title: Pearaamatu eraldamistöölehe töötlemine
description: Selles teemas selgitatakse eraldamise taotluse töötlemist rakenduses Dynamics 365 Finance.
author: aprilolson
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e89aa21f988d50bc1a922e053be0ff2dcd196268
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834408"
---
# <a name="process-ledger-allocation-journal"></a>Pearaamatu eraldamistöölehe töötlemine

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse eraldamise taotluse töötlemist. Kasutage lehte Eraldamistaotluse töötlemine selleks, et luua eraldamistööleht, mille saab üle vaadata ja kinnitada enne pearaamatusse sisestamist või sisestada otse pearaamatusse. Eraldamistöölehe saate luua alles siis, kui on olemas vähemalt üks aktiivne töölehe eraldamisreegel. See ülesanne kasutab demoettevõtte USMF andmeid.

1. Navigeerimispaanil avage **Moodulid > Pearaamat > Eraldamised > Protsessi eraldamise taotlus**.
2. Valige väljal **Reegel** ripploendist soovitud kirje.
3. Sisestage väljale **Kuupäevaga** kuupäev.

    - **Kuupäevaga** on väga tähtis, kui reegli andmeallikas on pearaamat. See kuupäev määrab, millised pearaamatusaldod eraldamisse kaasatakse.  
    - Valige väljal **Nullväärtus** suvand **Peata**. See peatab eraldamisprotsessi ja kuvab teate, et valitud on nullkogus.  

4. Valige väljal **Soovituse valikud** suvand **Ainult soovitus**. Valige suvand **Ainult soovitus** eraldamistöölehel oleva tulemuse ülevaatamiseks ja soovi korral kinnitamiseks enne eraldamise sisestamist pearaamatusse.  
5. Sisestage kuupäev väljale Pearaamatu sisestamisekuupäev.
6. Valige nupp **OK**.
7. Navigeerimispaanil avage **Moodulid > Pearaamat > Eraldamised > Eraldamise päevikud**.
8. Valige **Read**.
9. Valige **Sisesta**.
10. Valige **Sisesta**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]