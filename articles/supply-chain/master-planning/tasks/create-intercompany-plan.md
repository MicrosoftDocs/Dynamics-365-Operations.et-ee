---
title: Kontsernisisese plaani loomine
description: See protseduur näitab, kuidas luua kontsernisisest plaani.
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ae3d8a7c437ffd41a4864bd8548aa84c8ab8f32
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978269"
---
# <a name="create-an-intercompany-plan"></a>Kontsernisisese plaani loomine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas luua kontsernisisest plaani. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="set-up-an-intercompany-planning-group"></a>Kontsernisisese plaanimisgrupi seadistamine 
1. Paanil **Navigeerimispaan** avage **Moodulid > Koondplaneerimine > Kontsernisisesed plaanimisgrupid**. 
2. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks saate filtrida välja Nimi väärtuse 10 järgi.
3. Märkige loendis valitud rida.
4. Klõpsake  **Kustuta**. See etapp on vajalik kontsernisisese plaanimistsükli lühendamiseks.   Kontsernisisene plaanimine käivitab kõigis ettevõtetes koondplaneerimise plaanimisgrupis, alustades madalaimast plaanimisjärjestusest.  
5. Klõpsake nuppu **Jah**.
6. Sulgege leht.

## <a name="create-an-intercompany-plan"></a>Kontsernisisese plaani loomine
1. Paanil **Navigeerimispaan** avage **Moodulid > Koondplaneerimine > Tööruumid > Koondplaneerimine**.
2. Klõpsake **Kontsernisisene koondplaneerimine**.  
3. Väljal **Kontsernisisene plaanimisgrupp** klõpsake rippmenüü nuppu, et avada otsing.
4. Klõpsake loendis valitud real olevat linki. Valige kontsernisisene plaanimisgrupp 10.  
5. Väljale **Kontsernisisese plaanimise iteratsioonide arv** sisestage "2". Kontsernisisesel plaanimisgrupil 10 on kaks liiget. Selleks, et lisada lähteettevõtte (USMF) viivitused klientettevõtte (DEMF) ees, on vaja käivitada kontsernisisene plaanimine mõlemal ettevõttel kaks korda. Esimene iteratsioon lisab nõudluse ja tuvastab viivitused lähteettevõttes (USMF). Teine iteratsioon lisab viivitused USMF-ilt DEMF-ile.  
6. Väljal **Esimene iteratsioon** valige "Taasloomine".
7. Väljal **Järgnevad iteratsioonid** valige "Taasloomine".
8. Väljale **Lõimede arv** sisestage arv. See tähistab planeerimises kasutatavate paralleelsete lõimede arvu.  
9. Klõpsake valikut **OK**.

## <a name="view-the-result-of-the-plan"></a>Plaani tulemuse vaatamine
1. Väljal **Plaan** klõpsake ripploendi nuppu, et avada otsing.
2. Klõpsake loendis valitud real olevat linki. Klõpsake valiku StaticPlan linki. Peate olema ettevõttes USMF.  
3. Klõpsake **Plaanitud tellimused**.

