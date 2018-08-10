--- 
title: Tootmisvoo versioonile olemasoleva tegevuse lisamine
description: "Tootmisvoogude uute versioonide loomisel võite otsustada lisada vanematele versioonidele loodud tegevused uude versiooni."
author: cvocph
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a74fb34db71ba4b539c1b6ede361329aaeb94920
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a>Tootmisvoo versioonile olemasoleva tegevuse lisamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


