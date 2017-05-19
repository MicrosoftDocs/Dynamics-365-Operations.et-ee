---
title: Tootmistellimuste loomine
description: "Kui tootmistellimus on loodud, siis käivitatakse taotlus kauba tootmise alustamiseks. Tootmistellimus sisaldab teavet selle kohta, mida toodetakse, tootmise koguse kohta ja kavandatavat valmimiskuupäeva. See sisaldab ka teavet tarbitavate materjalide ja selle kohta, millise protsessi abil kaupa toota."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: b55c4c729350fbe8311953cc21f85bb4122f39f8
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="create-production-orders"></a>Tootmistellimuste loomine

[!include[banner](../includes/banner.md)]


Kui tootmistellimus on loodud, siis käivitatakse taotlus kauba tootmise alustamiseks. Tootmistellimus sisaldab teavet selle kohta, mida toodetakse, tootmise koguse kohta ja kavandatavat valmimiskuupäeva. See sisaldab ka teavet tarbitavate materjalide ja selle kohta, millise protsessi abil kaupa toota.

Tootmistellimus läbib tootmise töötsükli etapid. Kui tellimus luuakse, antakse sellele olek **Loodud**. Kui tellimus lõpetatakse, antakse sellele olek **Lõpetatud**. Parameetri säte võimaldab kasutajal igas staadiumis iga etappi konfigureerida. Sätte saab seadistada üksikkasutajale või kõigi kasutajate jaoks.

Tootmistellimuse põhiüksused on tootmise kooslus ja tootmisprotsess. Need kopeeritakse tootmistellimusele valitud kauba ja toodetava koguse põhjal. Enne tootmistellimuse alustamist saab tootmise kooslust ja protsessi redigeerida.

Tootmistellimust saab luua järgmiste stsenaariumide korral.

-   Materjalinõudlusel põhineva koondplaanimise läbiviimise põhjal.
-   Otse müügitellimuse realt või kõrgema taseme tootmistellimuse loomisel ja hindamisel (seotud tarne).
-   Käsitsi loodud.





