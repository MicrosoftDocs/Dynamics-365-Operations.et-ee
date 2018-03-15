---
title: Tootmistellimuse alustamine
description: "See protseduur selgitab, kuidas alustada tootmistellimust tööde juhtimisel."
author: johanhoffmann
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
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: 3b5657e5eb2719702eae3a3c5178b3a04f7545e3
ms.contentlocale: et-ee
ms.lasthandoff: 02/06/2018

---
# <a name="start-a-production-order"></a>Tootmistellimuse alustamine

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur selgitab, kuidas alustada tootmistellimust tööde juhtimisel. Selles protsessis edastatakse aja- ja materjalitarbimine. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. See on viies protseduur seitsmest, mis selgitab tootmistellimuse elutsüklit.


## <a name="start-a-production-order"></a>Tootmistellimuse alustamine
1. Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.
    * Valige tootmistellimus, mille olek on Väljastatud.  
2. Klõpsake toimingupaanil valikut Tootmistellimus.
3. Klõpsake nuppu Käivita.
    * Sellel lehel saate kinnitada tootmistellimuse alguse.  
4. Klõpsake vahekaarti Üldine.
5. Sisestage väljale Alates oper. Nr number '10'.
6. Valige väljal Automaatne protsessi tarbimine suvand Alati.
7. Märkige ruut Sisesta protsessikaart kohe.
8. Valige väljal Automaatne koosluse tarbimine suvand Alati.
9. Märkige ruut Sisesta komplekteerimisleht kohe.
10. Märkige ruut Prindi komplekteerimisleht.
11. Klõpsake nuppu OK.
    * See on trükitud komplekteerimisleht, millel on toodud tootmistellimuse jaoks kasutatud materjalid.  
12. Sulgege leht.

## <a name="validate-the-picking-list"></a>Komplekteerimislehe kinnitamine
1. Klõpsake toimingupaanil valikut Kuva.
2. Klõpsake suvandit Komplekteerimisleht.
3. Otsige loendist ja valige soovitud kirje.
4. Klõpsake loendis valitud real olevat linki.
5. Klõpsake nuppu Redigeeri.
6. Sisestage number väljale Tarbimine.
7. Klõpsake valikut Sisesta.
8. Klõpsake nuppu OK.
    * Komplekteerimislehe töölehele sisestatakse tootmistellimuse tarbitud materjalid. Enne töölehe sisestamist saate teha korrigeerimisi, kui eeldatav kogus erineb tegelikust tarbitud kogusest.  
9. Klõpsake vahekaarti GridPanel.
10. Sulgege leht.

## <a name="verify-the-route-card-journal"></a>Protsessikaardi töölehe kontrollimine
1. Klõpsake toimingupaanil valikut Kuva.
2. Klõpsake suvandit Protsessikaart.
3. Otsige loendist ja valige soovitud kirje.
4. Klõpsake loendis valitud real olevat linki.
5. Klõpsake nuppu Redigeeri.
6. Sisestage number väljale Tunnid.
7. Klõpsake valikut Sisesta.
8. Klõpsake nuppu OK.
    * Protsessikaardi töölehele kantakse üksikutele toimingutele kulunud aeg. Saate esitada ka õige ja veakoguse.  

