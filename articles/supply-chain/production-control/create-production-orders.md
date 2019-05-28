---
title: Tootmistellimuste loomine
description: Kui tootmistellimus on loodud, siis käivitatakse taotlus kauba tootmise alustamiseks. Tootmistellimus sisaldab teavet selle kohta, mida toodetakse, tootmise koguse kohta ja kavandatavat valmimiskuupäeva. See sisaldab ka teavet tarbitavate materjalide ja selle kohta, millise protsessi abil kaupa toota.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2957b387aac9e0218f88572fa605cde1a30c52e5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572623"
---
# <a name="create-production-orders"></a>Tootmistellimuste loomine

[!include [banner](../includes/banner.md)]

Kui tootmistellimus on loodud, siis käivitatakse taotlus kauba tootmise alustamiseks. Tootmistellimus sisaldab teavet selle kohta, mida toodetakse, tootmise koguse kohta ja kavandatavat valmimiskuupäeva. See sisaldab ka teavet tarbitavate materjalide ja selle kohta, millise protsessi abil kaupa toota.

Tootmistellimus läbib tootmise töötsükli etapid. Kui tellimus luuakse, antakse sellele olek **Loodud**. Kui tellimus lõpetatakse, antakse sellele olek **Lõpetatud**. Parameetri säte võimaldab kasutajal igas staadiumis iga etappi konfigureerida. Sätte saab seadistada üksikkasutajale või kõigi kasutajate jaoks.

Tootmistellimuse põhiüksused on tootmise kooslus ja tootmisprotsess. Need kopeeritakse tootmistellimusele valitud kauba ja toodetava koguse põhjal. Enne tootmistellimuse alustamist saab tootmise kooslust ja protsessi redigeerida.

Tootmistellimust saab luua järgmiste stsenaariumide korral.

-   Materjalinõudlusel põhineva koondplaanimise läbiviimise põhjal.
-   Otse müügitellimuse realt või kõrgema taseme tootmistellimuse loomisel ja hindamisel (seotud tarne).
-   Käsitsi loodud.




