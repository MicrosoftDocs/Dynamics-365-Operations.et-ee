---
title: "Koosluse versiooni määramine"
description: "Nõudluse koostamise ajal, kui kaubal on vaiketellimuse tüüp Tootmine, leiab plaanimismootor laoalal põhineva kehtiva koosluse versiooni."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, InventItemOrderSetup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 134b9f7fd46b5326eb6f1f4fec4ed2bda8a8576a
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="determine-the-bom-version"></a>Koosluse versiooni määramine

[!include[banner](../includes/banner.md)]


Nõudluse koostamise ajal, kui kaubal on vaiketellimuse tüüp Tootmine, leiab plaanimismootor laoalal põhineva kehtiva koosluse versiooni. 

Laoala dimensioon on alati teada ja nimetatud nõudluskandes. Kasutatava koosluse versiooni määramiseks kasutatakse järgmist protsessi.

-   Kui nõudelaoalal on kauba jaoks määratud koosluse versioon, kasutatakse seda laoalapõhist kooslust.
-   Kui nõudelaoalal pole kauba jaoks määratud koosluse versiooni, kasutatakse üldkooslust. Üldkooslus ei nimeta laoala ja see kehtib mitme laoala korral. Kui üldkooslus on olemas, siis kasutatakse seda.
-   Kui ei ole ühtegi kasutuselolevat koosluse versiooni, lõpeb siinkohal nõudluse kooslusearvutus.

Kehtiv koosluse versioon, laoalapõhine või üldine, peab vastama nõutavatele kuupäeva ja koguse kriteeriumidele.






