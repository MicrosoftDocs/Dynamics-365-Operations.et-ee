---
title: Tootmisvoo versioonile olemasoleva tegevuse lisamine
description: Tootmisvoogude uute versioonide loomisel võite otsustada lisada vanematele versioonidele loodud tegevused uude versiooni.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f73274c6e102df3007793e027587793d87c4f83
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579300"
---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a>Tootmisvoo versioonile olemasoleva tegevuse lisamine

[!include [banner](../../includes/banner.md)]

Tootmisvoogude uute versioonide loomisel võite otsustada lisada vanematele versioonidele loodud tegevused uude versiooni. See protseduur näitab, kuidas olemasolevale tootmisvoole luuakse uus versioon ilma tegevusi kopeerimata. Järgmises etapis lisatakse uuele versioonile olemasolev tegevus. 

See toiming nõuab tootmisvoogu, millele on juba loodud versioon ja tegevused.


## <a name="create-a-new-production-flow-version"></a>Loo uus tootmisvoo versioon
1. Minge jaotisse Tootmise juhtimine > Seadistus > Kulusäästlik tootmisvoog > Tootmisvood.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
4. Klõpsake nuppu Redigeeri.
5. Märkige loendis valitud rida.
6. Sisestage kuupäev ja kellaaeg väljale Aegumiskuupäev.
    * Pange tähele, et enne uue tootmisvoo versiooni loomist tuleb kindlasti kontrollida aktiivse versiooni aegumiskuupäeva ja aega. Uus versioon luuakse kehtiva alguskuupäevaga, mis loob ühenduse valitud versiooni aegumiskuupäevaga.  
7. Klõpsake vahekaarti Lisa.
8. Tehke väljal Kopeeri versioonist valik Ei.
    * Valige Ei, et alustada tühja versiooniga, kui enamik kopeeritud versiooni tegevustest asendatakse uute tegevustega. Lisage muutmata tegevused käsitsi vormile Lisa olemasolev funktsioon tegevusele.  
9. Tehke väljal Kanban-reeglite dubleerimine valik Ei.
    * Kui tegevusi ei kopeerita uude versiooni, pole uue versiooni loomise ajal võimalik kanban-reegleid kopeerida.   Selle asemel kasutatakse hiljem kanban-reegli vormil asendamise kanbani loomise funktsiooni, et asendada vana tootmisvoo versiooni kanban-reeglid kanban-reeglitega, mis kasutavad uue versiooni tegevusi.  
10. Klõpsake nuppu OK.
11. Otsige loendist ja valige soovitud kirje.

## <a name="add-an-existing-activity"></a>Olemasoleva tegevuse lisamine
1. Klõpsake suvandit Tegevused.
2. Klõpsake valikut Lisa olemasolev rippdialoogi avamiseks.
    * Otsige üles ja valige olemasolev tegevus, mis tuleb lisada uuele tootmisvoo versioonile.  Pange tähele, et loendis kuvatakse kõik sellele tootmisvoole kõigi varasemate versioonide jaoks loodud tegevused.  
3. Valige või sisestage väärtus väljal Tegevus.
4. Klõpsake nuppu OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]