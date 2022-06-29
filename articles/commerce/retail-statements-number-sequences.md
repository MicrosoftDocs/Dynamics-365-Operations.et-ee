---
title: Jaemüügi väljavõtete numbriseeriate häälestamine
description: See artikkel kirjeldab, kuidas konfigureerida numbriseeriaid, mis on vajalikud jaemüügi väljavõtete jaoks moodulis Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: 917d7b7a905a822ca3b1e074055fe0cd4af5555b
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027182"
---
# <a name="set-up-number-sequences-for-retail-statements"></a>Jaemüügi väljavõtete numbriseeriate häälestamine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas konfigureerida numbriseeriaid, mis on vajalikud jaemüügi väljavõtete jaoks moodulis Microsoft Dynamics 365 Commerce.

Jaemüügi väljavõtete tüüpe kasutatakse kahes tüübis Dynamics 365 Commerce: 

- **Kande väljavõtted** on mõeldud loomiseks ja sisestamiseks sagedusega. Neid kasutatakse kaupluse kõikide mitterahaliste kannete peakontorisse sisestamiseks Dynamics 365 Commerce. 
- **Finantsaruanded** on mõeldud loomiseks ja sisestamiseks üks kord tööpäeva kohta. Need hõlmavad ainult suletud vahetusi jaekauplustest, mis on p-töö kaudu Commerce Headquartersi üles laaditud.

## <a name="configure-a-number-sequence-for-statement-posting"></a>Väljavõtte sisestamise numbriseeria konfigureerimine

Kui olete kaupluse häälestamise commerce headquartersis lõpule viinud, peate konfigureerima kordumatu numbriseeria, mida väljavõtte loomise protsessi käigus väljavõtete jaoks kasutada.

Rakenduse Commerce Headquarters väljavõtte sisestamise numbriseeria konfigureerimiseks järgige neid samme.

1. Avage **Organisatsiooni haldus \> Numbriseeriad \> Numbriseeriad**.
1. Valige **uus \> numbriseeria** uue kirje loomiseks.
1. Sisestage **numbriseeria** kood väljale **Identimise kiirkaart** väljal Numbriseeria kood.
1. **Sisestage nimi väljale** Numbriseeria nimi.
1. Valige ulatuse **parameetrite** kiirkaardi väljal **Ulatus** suvand **Tootmisüksus**.
1. **Väljal Tootmisüksus** valige kauplus, mille jaoks numbriseeriat kasutatakse.
1. Määratlege **segmendid** Kiirkaardil Segmendid.
1. Seadke viidete **kiirkaardil** välja **Ala väärtuseks** **Kaupluse.**
1. Seadke viiteväljaks **Väljavõtte** **number ja** seejärel valige **OK**.

    ![ID, ulatuse parameetrid, segmendid ja viidete kiirkaardid numbriseeriate lehel.](media/retail-statements-num-seq-setup-01.png)

1. Värskendage **jaotise** **Numbri** eraldamine kiirkaardil Väikseimad ja Suurimad väljad nii, **·** **·** **·** **et need ühtiksid kiirkaardil Segmentide määratletud tähe- ja numbrisegmendi** pikkusega.
1. **Jõudlus kiirkaardil** soovitame seada **suvandi Eelasukoht väärtuseks** **Jah** **ja numbrikoguse** välja väärtuseks **25**.

    ![Üldine ja jõudluse kiirkaardid numbriseeriate lehel](media/retail-statements-num-seq-setup-02.png)

1. Muudatuste salvestamiseks ja lehe sulgemiseks **valige** tegevuspaanil käsk Salvesta.
