---
title: "Laovarude sätted"
description: "Koondplaneerimine kasutab laovarude sätteid, et arvutada kaubavajadusi."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 591b1cd739bb3be61299f33f180ca7c264d21a35
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="coverage-settings"></a>Laovarude sätted

[!INCLUDE [banner](../includes/banner.md)]

Koondplaneerimine kasutab laovarude sätteid, et arvutada kaubavajadusi. 

saate määratleda laovarude sätteid mitmel viisil:

-   Määrake laovarude grupi laovarude sätted. Saate luua laovarude grupi, mis sisaldab kõigi laovarude grupiga lingitud toodete sätteid. Klõpsake laovarude grupi loomiseks valikuid **Koondplaneerimine &gt; Seadistus &gt; Laovarud &gt; Laovarude grupid**. Saate linkida tootega laovarude grupi. Kui link on tegevuskoha-, lao- või tootedimensiooni kohane, kasutage lehel **Kauba laovarud** välja **Laovarude grupp**. Kui link on üldine olenemata tootedimensioonidest kasutage lehe **Toote üksikasjad** kiirkaardi **Plaan** lehte **Laovarude grupp**. Kui te ei lingi laovarude gruppi tootega, kasutab koondplaneerimine suvandit **Üldine laovarude grupp**, mis on määratud lehel **Koondplaneerimise parameetrid** vaikesättena.

-   Määrake toote laovarude sätted. Saate luua laovarude sätted kindlale tootele. Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**. Valige toode ja klõpsake **toimingupaanil** vahekaardi **Plaan** jaotises **Laovarude grupp** valikut **Kauba laovarud**, et avada leht **Kauba laovarud**. Kui toode on laovarude grupiga juba lingitud, saate laovarude grupi sätted tühistada, kasutades välja **Tühista**. Laovarude sätted lehel**Kauba laovarud** alistavad lehel **Laovarude grupp** olevad sätted.

<!-- -->

-   Määrake toote laovarude sätted viisardi abil. Viisard on etapiviisiline juhend, mis aitab teil häälestada esmaseid kauba laovarude parameetreid. Klõpsake lehel **Kauba laovarud** suvandit **Viisard**, et avada leht **Kauba laovarude viisard**.

<!-- -->

- Määrake dimensioonigrupi kaubavarude sätted. Klõpsake valikuid <strong>Tooteteabe haldus &gt; Üldine &gt; Väljastatud tooted</strong>. Klõpsake lehe <strong>Väljastatud toote üksikasjad</strong> vahekaardi **Üldine** grupis <strong>Haldus</strong> linki <strong>Laoala dimensioonigrupp</strong>. Valige lehel <strong>Laoala dimensioonigrupp</strong> väli <strong>Laovarude planeerimine dimensiooni järgi</strong>, et luua laovarude sätted laoala dimensioonigrupi dimensiooni jaoks. Kõigi tootedimensioonide, nagu konfiguratsioon, värv, suurus, stiil, puhul peab olema väli <strong>Laovarude planeerimine dimensiooni järgi</strong> valitud.



<a name="see-also"></a>Vt ka
--------

[Koondplaanid](master-plans.md)




