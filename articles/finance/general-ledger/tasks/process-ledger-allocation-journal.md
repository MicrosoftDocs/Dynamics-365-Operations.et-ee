---
title: Pearaamatu eraldamistöölehe töötlemine
description: See artikkel selgitab, kuidas rakenduses Dynamics 365 Finance eraldustaotlust töödelda.
author: aprilolson
ms.date: 11/15/2022
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
ms.openlocfilehash: 1f22b5042e0e3726afcb1061852fdbd8de770c61
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779388"
---
# <a name="process-ledger-allocation-journal"></a>Pearaamatu eraldamistöölehe töötlemine

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas eraldustaotlust töödelda. Kasutage protsessi **eraldamise taotluse lehte** eraldamise töölehe loomiseks, mida saab enne Pearaamatusse sisestamist üle vaadata ja heaks kiita või otse Pearaamatusse sisestada. Eraldamistöölehe saate luua alles siis, kui on olemas vähemalt üks aktiivne töölehe eraldamisreegel. See ülesanne kasutab demoettevõtte USMF andmeid.

1. Navigeerimispaanil minge pearaamatusse ja **> eraldamised > protsessi eraldamistaotlus**.
2. Valige väljal **Reegel** ripploendist soovitud kirje.
3. Sisestage väljale **Kuupäevaga** kuupäev.

    - **Kuupäevaga** on väga tähtis, kui reegli andmeallikas on pearaamat. See kuupäev määrab, millised pearaamatusaldod eraldamisse kaasatakse.  
    - Valige väljal **Nullväärtus** suvand **Peata**. See peatab eraldamisprotsessi ja kuvab teate, et valitud on nullkogus.  

4. Valige väljal **Soovituse valikud** suvand **Ainult soovitus**. Valige **ainult soovitus** enne eraldamise pearaamatusse sisestamist eraldustöölehtede **tulemuse** ülevaatamiseks ja valikuliseks kinnitamiseks.  
5. **Pearaamatu sisestamiskuupäeva väljale** sisestage kuupäev.
6. Valige nupp **OK**.
7. Navigeerimispaanil avage **Moodulid > Pearaamat > Eraldamised > Eraldamise päevikud**.
8. Valige **Read**.
9. Valige **Sisesta**.
10. Valige **Sisesta**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
