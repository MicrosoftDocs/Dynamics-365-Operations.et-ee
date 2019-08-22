---
title: Koondplaneerimise käitamise jälgimine
description: Tootmise plaanija soovib näha, kui koondplaneerimise käitamine on pooleli.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b923b215528ecceaed9b5057ddb736ec959f1d65
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845109"
---
# <a name="monitor-a-master-planning-run"></a>Koondplaneerimise käitamise jälgimine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tootmise plaanija soovib näha, kui koondplaneerimise käitamine on pooleli. Kasutage protseduuri lõpuleviimiseks demoandmete ettevõtet USMF.


## <a name="run-master-planning"></a>Koondplaneerimise käivitamine
1. Klõpsake valikul Koondplaneerimine.
    * Leiate selle vaikimisi armatuurlaualt.  
2. Valige või sisestage väärtus väljal Plaan.
    * Näide: StaticPlan  
3. Klõpsake nuppu Käivita.
4. Tehke väljal Töötlemisaja jälgimine valik Jah.
    * Kui väli on juba valitud, jätke see etapp vahele.  
5. Sisestage number väljale Lõimede arv.
6. Jaotise kaasamiseks laiendage kirjeid.
7. Klõpsake käsku Filtreeri.
8. Märkige loendis valitud rida.
    * Märkige rida, kus väli = kauba kood.  
9. Sisestage või valige väärtus väljal Kriteeriumid.
    * Näide: T0001.  
10. Klõpsake nuppu OK.
11. Klõpsake nuppu OK.

## <a name="monitor-the-master-planning-run"></a>Koondplaneerimise käitamise jälgimine
1. Klõpsake nuppu Ajalugu.
2. Klõpsake suvandit Päringud.
3. Klõpsake suvandit Protsessiülesande kestus.
4. Otsige loendist ja valige soovitud kirje.
    * Iga kauba puhul saate ülevaate, kui kaua võttis aega iga planeerimise etapi lõpule viimine.  

