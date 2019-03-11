---
title: Laovarude sätted
description: Koondplaneerimine kasutab laovarude sätteid, et arvutada kaubavajadusi.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50f47394a4d4e95b4e158ea42a630d9e6e91f05b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "322555"
---
# <a name="coverage-settings"></a>Laovarude sätted

[!include [banner](../includes/banner.md)]

Koondplaneerimine kasutab laovarude sätteid, et arvutada kaubavajadusi. 

saate määratleda laovarude sätteid mitmel viisil:

-   Määrake laovarude grupi laovarude sätted. Saate luua laovarude grupi, mis sisaldab kõigi laovarude grupiga lingitud toodete sätteid. Klõpsake laovarude grupi loomiseks valikuid **Koondplaneerimine &gt; Seadistus &gt; Laovarud &gt; Laovarude grupid**. Saate linkida tootega laovarude grupi. Kui link on tegevuskoha-, lao- või tootedimensiooni kohane, kasutage lehel **Kauba laovarud** välja **Laovarude grupp**. Kui link on üldine olenemata tootedimensioonidest kasutage lehe **Toote üksikasjad** kiirkaardi **Plaan** lehte **Laovarude grupp**. Kui te ei lingi laovarude gruppi tootega, kasutab koondplaneerimine suvandit **Üldine laovarude grupp**, mis on määratud lehel **Koondplaneerimise parameetrid** vaikesättena.

-   Määrake toote laovarude sätted. Saate luua laovarude sätted kindlale tootele. Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**. Valige toode ja klõpsake **toimingupaanil** vahekaardi **Plaan** jaotises **Laovarude grupp** valikut **Kauba laovarud**, et avada leht **Kauba laovarud**. Kui toode on laovarude grupiga juba lingitud, saate laovarude grupi sätted tühistada, kasutades välja **Tühista**. Laovarude sätted lehel**Kauba laovarud** alistavad lehel **Laovarude grupp** olevad sätted.

<!-- -->

-   Määrake toote laovarude sätted viisardi abil. Viisard on etapiviisiline juhend, mis aitab teil häälestada esmaseid kauba laovarude parameetreid. Klõpsake lehel **Kauba laovarud** suvandit **Viisard**, et avada leht **Kauba laovarude viisard**.

<!-- -->

- Määrake dimensioonigrupi kaubavarude sätted. Klõpsake valikuid **Tooteteabe haldus &gt; Üldine &gt; Väljastatud tooted**. Klõpsake lehe **Väljastatud toote üksikasjad** vahekaardil **Üldine** grupis **Administreerimine** linki **Laoala dimensioonigrupp**. Valige lehel **Laoala dimensioonigrupp** väli **Laovarude planeerimine dimensiooni järgi**, et luua laovarude sätted laoala dimensioonigrupi dimensiooni jaoks. Kõigi tootedimensioonide, nagu konfiguratsioon, värv, suurus, stiil, puhul peab olema väli **Laovarude planeerimine dimensiooni järgi** valitud.



<a name="additional-resources"></a>Lisaressursid
--------

[Koondplaanid](master-plans.md)



