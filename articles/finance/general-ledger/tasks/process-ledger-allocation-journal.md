---
title: Pearaamatu eraldamistöölehe töötlemine
description: See artikkel selgitab, kuidas rakenduses Dynamics 365 Finance eraldustaotlust töödelda.
author: aprilolson
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b86f8f5d090d624e812d9e7e6c0bc0212e5e9716
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902425"
---
# <a name="process-ledger-allocation-journal"></a>Pearaamatu eraldamistöölehe töötlemine

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas eraldustaotlust töödelda. Kasutage lehte Eraldamistaotluse töötlemine selleks, et luua eraldamistööleht, mille saab üle vaadata ja kinnitada enne pearaamatusse sisestamist või sisestada otse pearaamatusse. Eraldamistöölehe saate luua alles siis, kui on olemas vähemalt üks aktiivne töölehe eraldamisreegel. See ülesanne kasutab demoettevõtte USMF andmeid.

1. Navigeerimispaanil minge pearaamatusse ja **> eraldamised > protsessi eraldamistaotlus**.
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
