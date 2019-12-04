---
title: Optimeeri jõudlus automaatse puhastamise ülesannetega
description: See teema selgitab, kuidas lahendada Microsofti Dynamics 365 Talent jõudluse probleeme, puhastades pakett-töö ajaloo.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a053c9094151f4e12e4aadc533dd272258779540
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832578"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Optimeeri jõudlus automaatse puhastamise ülesannetega

[!include [banner](includes/banner.md)]

**Väljastamine**

Microsoft Dynamics 365 Talent võib kogeda jõudluse probleeme, kui pakett-töö ajalugu kasvab liiga suureks.

**Põhjus**

Sageli käivitatavad pakett-tööd võivad põhjustada pakett-töö ajaloo jätkusuutmatut kasvu. See võib põhjustada jõudluse probleeme. 

**Eraldusvõime**

Planeerige automaatne ülesanne oma pakett-töö ajaloo puhastamiseks. Soovitame ülesande seadistada iganädalaseks käivitamiseks, kuid sõltuvalt keskkonnast võib osutuda vajalikuks puhastamist sagedamini või harvemini käitada. Järgmine protseduur sisaldab meie soovitatud sätteid, kuid te saate neid vastavalt vajadusele muuta.

1. Valige Talentis **Süsteemihaldus**.

2. Sisestage väljale **Otsing** käsk **Pakett-töö ajaloo puhastamine**.

   ![Otsige pakett-töö ajaloo puhastamist](media/talent-batch-history-cleanup-search-bar.png)

3. Sisestage jaotisse **Ajaloo limiit (päeva)** väärtus **30**.

   ![Määrake ajaloo limiidiks 30](media/talent-batch-history-cleanup-history-limit.png)

4. Valige suvand **Käivita taustal** ja seejärel valige **Kordumine**.

   ![Seadistage kordumine](media/talent-batch-history-cleanup-recurrence.png)

5. Valikus **Määratle kordumine** seadistage **Alguskuupäev** ja **Algusaeg** töövälisele ajale või nädalavahetusele ning seejärel valige **LÕPP-KUUPÄEV PUUDUB**. 

   ![Määratlege korduse alguskuupäev ja -kellaaeg](media/talent-batch-history-cleanup-define-recurrence.png)

6. Jaotises **KORDUMISMUSTER** valige **Päevad** ja määrake **KORDA MÄÄRATUD INTERVALLI JÄREL** kuni **7**.

   ![Määrake puhastamisele iganädalane kordus](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. Valige nupp **OK**.

8. Muutke vajadusel mistahes teisi parameetreid jaotises **Käivita taustal** ja seejärel valige **OK**.

