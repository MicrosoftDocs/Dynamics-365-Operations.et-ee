---
title: "Reakauba töövoo konfigureerimine"
description: "Selles teemas selgitatakse, kuidas konfigureerida reakaupa töövoo elementi."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 2781a0344f1de5caf0031d7c3d5b88678be153a4
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="configure-a-line-item-workflow"></a>Reakauba töövoo konfigureerimine

[!include[banner](../includes/banner.md)]


Selles teemas selgitatakse, kuidas konfigureerida reakaupa töövoo elementi.

Töövooredaktoris reakauba töövoo elemendi konfigureerimiseks paremklõpsake elementi ja seejärel klõpsake valikut **Atribuudid**, et avada leht **Atribuudid**. Seejärel kasutage reakauba töövoo elemendi atribuutide konfigureerimiseks järgmisi protseduure.

## <a name="name-the-lineitem-workflow-element"></a>Reakauba töövoo elemendile nime andmine
Tehke reakauba töövoo elemendile nime sisestamiseks järgmist.

1.  Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2.  Sisestage väljale **Nimi** reakauba töövoo elemendi jaoks kordumatu nimi.

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a>Määrake, kas sama töövoogu kasutatakse kõigi reakaupade töötlemiseks.
Järgige neid etappe, et määrata, kas sama töövoogu kasutatakse dokumendi kõigi reakaupade töötlemiseks.

1.  Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2.  Kui sama töövoog peab töötlema dokumendi kõiki reakaupu, klõpsake valikut **Kutsu üksik töövoog kõigile reakaupadele**. Seejärel valige töövoog, millega reakaupu töödelda.
3.  Kui teatud töövoog peaks töötlema reakaupu, mis vastavad määratud tingimustele, klõpsake valikut **Kutsu töövoog igale reakaubale**. Järgige neid etappe tingimustekogumi määratlemiseks.
    1.  Klõpsake vahekaarti **Lisa**.
    2.  Valige tabelist tingimus.
    3.  Sisestage vahekaardil **Tingimuse nimi** määratletava tingimustekogumi nimi.
    4.  Tingimuse sisestamiseks klõpsake valikut **Lisa tingimus**.
    5.  Sisestage täiendavad vajalikud tingimused.
    6.  Kontrollimaks, kas sisestatud tingimustekogum on õigesti konfigureeritud, klõpsake käsku **Katseta**. Lehel **Töövoo tingimuse katsetamine** alas **Kontrolli tingimust** valige kirje ja seejärel klõpsake käsku **Katseta**. Süsteem hindab kirjet otsustamaks, kas see vastab teie määratud tingimustele. Klõpsake **OK** või valikut **Tühista**, et naasta lehele **Atribuudid**.

    Vahekaardil **Töövoog** valige töövoog, mida kasutada teie määratletud tingimustekogumile vastavate reakaupade töötlemiseks.





