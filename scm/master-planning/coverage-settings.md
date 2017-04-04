---
title: "Laovarude sätted"
description: "Koondplaneerimine kasutab laovarude sätteid, et arvutada kaubavajadusi."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c1c5654afa6b592e178af052e3e4a7e246a94c9f
ms.lasthandoff: 03/31/2017


---

# <a name="coverage-settings"></a>Laovarude sätted

Koondplaneerimine kasutab laovarude sätteid, et arvutada kaubavajadusi. 

saate määratleda laovarude sätteid mitmel viisil:

-   Määrake laovarude grupi laovarude sätted. Saate luua laovarude grupi, mis sisaldab kõigi laovarude grupiga lingitud toodete sätteid. Klõpsake **kapten planeerimine &gt;Setup &gt;kate &gt;laovarude gruppide** laovarude grupi loomiseks. Saate linkida tootega laovarude grupi. Kui link on tegevuskoha-, lao- või tootedimensiooni kohane, kasutage lehel **Kauba laovarud** välja **Laovarude grupp**. Kui link on üldine olenemata tootedimensioonidest kasutage lehe **Toote üksikasjad** kiirkaardi **Plaan** lehte **Laovarude grupp**. Kui te ei lingi laovarude gruppi tootega, kasutab koondplaneerimine suvandit **Üldine laovarude grupp**, mis on määratud lehel **Koondplaneerimise parameetrid** vaikesättena.

-   Määrake toote laovarude sätted. Saate luua laovarude sätted kindlale tootele. Klõpsake **toote teabekorraldus &gt;toodete &gt;vabastatud toodete**. Valige toote kohta ning **Updatehagi paani**, on **planeerida** vahekaardil, on **laovarude grupi**, klõpsake **kauba laovarud** avamiseks ning **kauba laovarud** lehekülg. Kui toode on laovarude grupiga juba lingitud, saate laovarude grupi sätted tühistada, kasutades välja **Tühista**. Laovarude sätted lehel** Kauba laovarud** alistavad lehel **Laovarude grupp** olevad sätted.

<!-- -->

-   Määrake toote laovarude sätted viisardi abil. Viisard on etapiviisiline juhend, mis aitab teil häälestada esmaseid kauba laovarude parameetreid. Klõpsake lehel **Kauba laovarud** suvandit **Viisard**, et avada leht **Kauba laovarude viisard**.

<!-- -->

-   Määrake dimensioonigrupi kaubavarude sätted. Klõpsake **toote teabekorraldus &gt;ühise &gt;vabastatud toodete**. Kohta on ** välja üksikasju toodete ** lehekülg edasi on **üldise** vahekaardil, on **halduse** nuppu ning **ladustamise dimensioonigrupp** link. Valige lehel **Laoala dimensioonigrupp** väli **Laovarude planeerimine dimensiooni järgi**, et luua laovarude sätted laoala dimensioonigrupi dimensiooni jaoks. Kõik toote mõõtmed, näiteks konfiguratsioon, värv, suurus, stiil, peab olema ka **laovarude planeerimine dimensioonide kaupa** välja valitud.



<a name="see-also"></a>Vt ka
--------

[Master plans](master-plans.md)


