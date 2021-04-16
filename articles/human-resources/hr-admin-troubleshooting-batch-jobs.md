---
title: Jõudluse optimeerimine pakett-tööde ajastamisel töövälisele ajale
description: Selles teemas selgitatakse, kuidas lahendada Microsoft Dynamics 365 Human Resourcesi jõudluse probleeme, ajastades pakett-tööd töövälisele ajale.
author: andreabichsel
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 92dd281ed718be5c7ebd843d015c108ee121f30a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794921"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>Jõudluse optimeerimine pakett-tööde ajastamisel töövälisele ajale

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a>Väljastus

Microsoft Dynamics 365 Human Resourcesis võib esineda jõudluse probleeme, kui pikaajalisi pakett-töid käitatakse tavapärasel tööajal.

## <a name="resolution"></a>Eraldusvõime

Ajastage järgmised pakett-tööd töövälisele ajale. Samuti soovitame vaadata üle regulaarselt töötavate pakett-tööde sageduse. Võimalusel vähendage pakett-töö sagedust. Paljudel juhtudel piisab vaikimisi sagedusest.

Järgmised pakett-tööd peaksid töötama öösiti või töövälisel ajal. Kontrollige kindlasti nende korduvate pakett-tööde ajavööndit. Osad pakett-tööd võivad kasutada Lääneranniku aega (PST).

| Pakett-töö | Vaikesagedus |
| --- | --- |
| Pakett-töö ajaloo puhastamine | 1 kord kuus |
| Ekspordi ajastamise puhastamine | 1 kord päevas |
| Common Data Service’i integreerimise vastamata päringu sünkroonimine | 1 kord päevas |
| Andmebaasi tihendamise süsteemi töö, mida tuleb käitada regulaarselt töövälisel ajal | 1 kord päevas |
| Andmebaasi indeksi uuesti loomise süsteemi töö, mida tuleb käitada regulaarselt töövälisel ajal | 1 kord päevas |

1. Valige rakenduses Human Resources suvand **Süsteemihaldus**.

2. Otsige ribal **Otsing** ühte ülaltoodud pakett-töödest.

3. Valige suvand **Käivita taustal** ja seejärel valige **Kordumine**.

   ![Seadistage kordumine](media/talent-batch-history-cleanup-recurrence.png)

4. Valikus **Määratle kordumine** seadistage **Alguskuupäev** ja **Algusaeg** töövälisele ajale või nädalavahetusele. Valige **Lõppkuupäev puudub**. 

   ![Määratlege korduse alguskuupäev ja -kellaaeg](media/talent-batch-history-cleanup-define-recurrence.png)

5. Valige nupp **OK**.

6. Muutke vajadusel mistahes teisi parameetreid jaotises **Käivita taustal** ja seejärel valige **OK**.

## <a name="additional-resources"></a>Lisaressursid

[Jõudluse optimeerimine automaatsete puhastamisülesannetega](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]