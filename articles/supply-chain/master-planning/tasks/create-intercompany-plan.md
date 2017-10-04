--- 
title: Kontsernisisese plaani loomine
description: "See protseduur näitab, kuidas luua kontsernisisest plaani."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 7c7f466add55fb9a24c3fb8f1f92df712a8622e3
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="create-an-intercompany-plan"></a>Kontsernisisese plaani loomine

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas luua kontsernisisest plaani. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="set-up-an-intercompany-planning-group"></a>Kontsernisisese plaanimisgrupi seadistamine 
1. Avage jaotis Kontsernisisesed plaanimisgrupid.
    * Koondplaneerimine > Seadistus > Kontsernisisesed plaanimisgrupid  
2. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks saate filtrida välja Nimi väärtuse 10 järgi.
3. Märkige loendis valitud rida.
4. Klõpsake  Kustuta.
    * See etapp on vajalik kontsernisisese plaanimistsükli lühendamiseks.   Kontsernisisene plaanimine käivitab kõigis ettevõtetes koondplaneerimise plaanimisgrupis, alustades madalaimast plaanimisjärjestusest.  
5. Klõpsake nuppu Jah.
6. Sulgege leht.

## <a name="create-an-intercompany-plan"></a>Kontsernisisese plaani loomine
1. Klõpsake valikut Kontsernisisene koondplaneerimine.
    * See on koondplaneerimise tööruumis.  
2. Klõpsake väljal Kontsernisisene plaanimisgrupp otsingu avamiseks ripploendi nuppu.
3. Klõpsake loendis valitud real olevat linki.
    * Valige kontsernisisene plaanimisgrupp 10.  
4. Sisestage väljale Plaanitud kontsernisiseste iteratsioonide arv number 2.
    * Kontsernisisesel plaanimisgrupil 10 on kaks liiget. Selleks, et lisada lähteettevõtte (USMF) viivitused klientettevõtte (DEMF) ees, on vaja käivitada kontsernisisene plaanimine mõlemal ettevõttel kaks korda. Esimene iteratsioon lisab nõudluse ja tuvastab viivitused lähteettevõttes (USMF). Teine iteratsioon lisab viivitused USMF-ilt DEMF-ile.  
5. Tehke valik väljal Esimene iteratsioon.
6. Valige Taasloomine väljalt Esimene iteratsioon.
7. Valige Taasloomine väljalt Järgnevad iteratsioonid.
8. Sisestage number väljale Lõimede arv.
    * See tähistab planeerimises kasutatavate paralleelsete lõimede arvu.  
9. Klõpsake nuppu OK.

## <a name="view-the-result-of-the-plan"></a>Plaani tulemuse vaatamine
1. Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.
2. Klõpsake loendis valitud real olevat linki.
    * Klõpsake valiku StaticPlan linki. Peate olema ettevõttes USMF.  
3. Klõpsake valikut Planeeritud tellimused.

