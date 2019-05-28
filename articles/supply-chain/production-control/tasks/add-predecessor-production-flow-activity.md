---
title: Tootmisvoo tegevusele eelkäija lisamine
description: Tootmisvoo versiooni puhul peavad kõik tegevused olema järjestatud.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9acb1c2672af70f535f3dce1c8f5a97e8d479158
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552295"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>Tootmisvoo tegevusele eelkäija lisamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tootmisvoo versiooni puhul peavad kõik tegevused olema järjestatud. Tegevusel võib olla üks või mitu eelkäijat või järeltulijat. 

See protseduur näitab, kuidas seostada eelkäijat tegevusega. 

Selle toimingu tegemiseks vajate tootmisvoogu, mille mustandversioonil on vähemalt kaks tegevust, mille saab ühendada. 

Lisateavet leiate tehnilisest ülevaatest Lean manufacturingi tootmisvood ja tegevused.


## <a name="find-the-production-flow-and-version"></a>Otsige üles tootmisvoog ja versioon
1. Minge jaotisse Tootmise juhtimine > Seadistus > Kulusäästlik tootmisvoog > Tootmisvood.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake suvandit Tegevused.

## <a name="select-an-activity-and-add-a-predecessor"></a>Valige tegevus ja lisage eelkäija
1. Otsige loendist ja valige soovitud kirje.
2. Klõpsake valikut Eelkäija lisamine.
3. Valige või sisestage väärtus väljal Tegevus.
4. Sisestage number väljale Tsükliaja määr.
    * Tegevusseoste kogumi tsükli aja vaikimisi väärtus on 1. See eeldab, et mõlemaid tegevusi käitatakse samas tempos või takti ajas. Kui eelkäija töötab kiiremini (väiksema takti ajaga), peaks suhe olema väiksem kui 1; kui eelkäija töötab aeglasemalt (suurema takti ajaga), on tsükli aja suhe suurem kui 1.  
5. Klõpsake nuppu OK.

