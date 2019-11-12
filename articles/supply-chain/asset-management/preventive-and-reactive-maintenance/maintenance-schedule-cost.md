---
title: Hooldusgraafiku kulu
description: Selles teemas selgitatakse hooldusgraafiku kulu varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b30fa3c142057b43202a8f5a323c0b425865e971
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571319"
---
# <a name="maintenance-schedule-cost"></a>Hooldusgraafiku kulu

[!include [banner](../../includes/banner.md)]

 

Varahalduses saate arvutada hooldusgraafiku ridade eelarve kulusid. See on kasulik, kui soovite saada ülevaadet oodatavatest kuludest, näiteks kulud seoses planeeritavate järgmise aasta ennetavate hooldustöödega. Arvutused põhinevad olemasolevatel hooldusgraafiku ridadel, mille tüüp on "Hoolduskavad" ja "Hoolduskorrad" ja "Hooldusnõuded".

1. Klõpsake **Varahaldus** > **Päringud** > **Varad** > **Hooldusgraafiku kulu**.

2. Dialoogis **Hooldusgraafiku kulu** saate valida valiku **Finantsdimensioonikogum**, kui soovite näha kulusid finantsdimensioonidesse grupeerituna.

>[!NOTE]
>Finantsdimensioonikogumid seadistatakse jaotises **Pearaamat** > **Kontoplaan** > **Dimensioonid** > **Dinantsdimensioonikogumid**.

3. Saate kasutada välja **Tase**, et näidata kui üksikasjalikke töö asukohaga seotud hooldusgraafiku ridu soovite. Kui sisestate väljale näiteks arvu "1" ja teil on mitmetasandiline töö asukoha struktuur, kuvatakse ülemisel tasemel kõik töö asukoha hooldusgraafiku read ning seetõttu võivad rea tunnid olla alumisel tasemel asuvate töö asukohtade summad. Kui sisestate väljale **Tase** arvu "0", näete üksikasjalikku tulemust, mis näitab kõiki hooldusgraafiku ridu kõigi töö asukoha tasemete kohta, millega nad on seotud.

4. Kui soovite teha arvutusi konkreetsele varale, klõpsake kiirkaardil **Kaasatavad kirjed** nuppu **Filtreeri** ja valige asjakohased varad. Vajadusel saate määrata kuluarvutusele ka **Oodatava alguse** kuupäeva või valida kulu arvutusele erineva **Oleku**

5. Kulu arvutuse alustamiseks klõpsake **OK**.

6. Klõpsake vahekaardi **Hooldusgraafiku kulu** > toimingupaani rühmas **Rühmitusalus...** asjakohastele nuppudele, et kuvada kuluarvutuse soovitud üksikasjade taset. Valitud toimingupaani grupi nupud on esile tõstetud. Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.

7. Klõpsake nuppu **Arvuta kulu**, kui soovite teha uue kuluarvutuse.

Alltoodud illustratsioonil kuvatakse näidet hooldusgraafiku kulu arvutuse tulemustest.

![Joonis 1](media/17-preventive-maintenance.png)

