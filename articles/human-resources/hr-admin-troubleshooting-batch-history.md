---
title: Jõudluse optimeerimine automaatsete puhastamisülesannetega
description: See teema selgitab, kuidas parandada rakenduse Microsoft Dynamics 365 Human Resources jõudlust, puhastades pakett-töö ajaloo.
author: twheeloc
ms.date: 08/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 12876cf4cbbac893bcbb0178280245d5637bdf73
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413483"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Jõudluse optimeerimine automaatsete puhastamisülesannetega

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Väljastamine**

Microsoft Dynamics 365 Human Resources võib kogeda jõudluse probleeme, kui pakett-töö ajalugu kasvab liiga suureks.

**Põhjus**

Sageli käivitatavad pakett-tööd võivad põhjustada pakett-töö ajaloo jätkusuutmatut kasvu. See võib põhjustada jõudluse probleeme. 

**Eraldusvõime**

Planeerige automaatne ülesanne oma pakett-töö ajaloo puhastamiseks. Soovitame ülesande seadistada iganädalaseks käivitamiseks, kuid sõltuvalt keskkonnast võib osutuda vajalikuks puhastamist sagedamini või harvemini käitada. Järgmine protseduur sisaldab meie soovitatud sätteid, kuid te saate neid vastavalt vajadusele muuta.

1. Valige rakenduses Human Resources suvand **Süsteemihaldus**.

2. Sisestage väljale **Otsing** käsk **Pakett-töö ajaloo puhastamine**.

   ![Otsige pakett-töö ajaloo puhastamist.](media/talent-batch-history-cleanup-search-bar.png)

3. Sisestage jaotisse **Ajaloo limiit (päeva)** väärtus **30**.

   ![Määrake ajaloo limiidiks 30.](media/talent-batch-history-cleanup-history-limit.png)

4. Valige suvand **Käivita taustal** ja seejärel valige **Kordumine**.

   ![Kordumise seadistamine.](media/talent-batch-history-cleanup-recurrence.png)

5. Valikus **Määratle kordumine** seadistage **Alguskuupäev** ja **Algusaeg** töövälisele ajale või nädalavahetusele ning seejärel valige **LÕPP-KUUPÄEV PUUDUB**. 

   ![Määratlege korduse alguskuupäev ja -kellaaeg.](media/talent-batch-history-cleanup-define-recurrence.png)

6. Jaotises **KORDUMISMUSTER** valige **Päevad** ja määrake **KORDA MÄÄRATUD INTERVALLI JÄREL** kuni **7**.

   ![Määrake puhastamisele iganädalane kordus.](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. Valige nupp **OK**.

8. Muutke vajadusel mistahes teisi parameetreid jaotises **Käivita taustal** ja seejärel valige **OK**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
