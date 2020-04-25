---
title: Loo tarbimise aruandeid
description: Selles teemas tutvustatakse, kuidas luua tarbimise aruandeid varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d28acbccc35b3f59f9cca7236dd721a1d9bdead8
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216432"
---
# <a name="create-consumption-reports"></a>Loo tarbimise aruandeid

[!include [banner](../../includes/banner.md)]

 

Kui olete loonud ja sisestanud töökäskude tarbimise registreeringud varahalduses, on tarbimise üksikasjade kuvamiseks saadaval kaks aruannet.


## <a name="asset-consumption-report"></a>Vara tarbimise aruanne

Kui olete sisestanud töökäskude tarbimise, saate vara tarbimise aruande printida. Aruanne kuvab tunde, tunni kulusid, kauba kulusid ja varade kohta sisestatud kulusid.

1. Klõpsake **Varahaldus** > **Aruanded** > **Varad** > **Vara tarbimine**.

2. Dialoogiboksis **Vara tarbimine** valige parameetrid ja üksikasja tase, mida soovite näha, valides **Jah** asjakohastel tumblernuppudel ja sisestades töö asukoha taseme jaotisesse **Kuva**.
    - Saate kasutada välja **Tase**, et näidata kui üksikasjalikke töö asukohtade vara ridu te soovite. 
    
        Kui sisestate väljale näiteks arvu "1" ja teil on mitmetasandiline töö asukoha struktuur, kuvatakse ülemisel tasemel kõik töö asukoha varad ning seetõttu võivad tunnid real olla lisatud ülespoole töö asukohtades, mis asuvad madalamal tasemel. 
        
        Kui sisestate väljale **Tasemed** arvu "0", näete üksikasjalikku tulemust, mis näitab kõiki varasid kõigi töö asukoha tasemete kohta, millega need on seotud. 
        
    - Valige **Jah** tumblernupul **Kõigi alamvarade summa**, et näha iga alamvara summat aruandes.

3. Valige kuupäevaintervall jaotises **Kuupäevad**.

4. Kiirkaardil **Sihtkoht** valige, kas soovite aruande kuvada ekraanil, printida või salvestada faili või meilina.

5. Vajaduse korral saate valida, milliseid konkreetseid varasid aruandes kuvada. Kiirkaardil **Kaasatavad kirjed** klõpsake **Filter** ja lisage varad, mida soovite aruandesse kaasata.

6. Aruande loomiseks klõpsake nuppu **OK**.


## <a name="work-order-consumption-report"></a>Töökäsu tarbimise aruanne

Kui olete sisestanud töökäskude tarbimise, saate töökäsu tarbimise aruande printida. Aruanne kuvab tunde, tunni kulusid, kauba kulusid ja töökäskude kohta sisestatud kulusid.

1. Klõpsake **Varahaldus** > **Aruanded** > **Töökäsud** > **Töökäsu tarbimine**.

2. Dialoogiboksis **Töökäsu tarbimine** valige parameetrid ja üksikasja tase, mida soovite aruandesse kaasata, valides **Jah** asjakohastel tumblernuppudel ja sisestades töö asukoha taseme jaotisesse **Kuva**.

3. Valige kuupäevaintervall jaotises **Kuupäevad**.

4. Kiirkaardil **Sihtkoht** valige, kas soovite aruande kuvada ekraanil, printida või salvestada faili või meilina.

5. Vajaduse korral saate valida, milliseid konkreetseid töökäske aruandes kuvada. Kiirkaardil **Kaasatavad kirjed** klõpsake **Filter** ja lisage töökäsud, mida soovite aruandesse kaasata.

6. Aruande loomiseks klõpsake nuppu **OK**.


>[!NOTE]
>Samuti saate luua [töökäsu aruande](../work-orders/work-order-report.md), mis sisaldab rohkem töökäsu üksikasju.

