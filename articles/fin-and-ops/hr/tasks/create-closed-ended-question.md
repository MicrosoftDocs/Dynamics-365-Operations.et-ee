--- 
title: "Suletud küsimuse loomine"
description: "Kinnised küsimused võimaldavad teil pakkuda valikuid, mille hulgast vastaja saab valida."
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 71b2a2da0b705b84f79adcff25672855e7b5253f
ms.contentlocale: et-ee
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-closed-ended-question"></a>Suletud küsimuse loomine

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kinnised küsimused võimaldavad teil pakkuda valikuid, mille hulgast vastaja saab valida. Esmalt peate looma vastusegrupi vastustega, seejärel looma seda vastustegruppi kasutava küsimuse. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="create-an-answer-group"></a>Vastustegrupi loomine
1. Avage Küsimustik > Kujundus > Vastustegrupid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Vastustegrupp.
4. Sisestage väljale Kirjeldus soovitud väärtus.
    * Kasutage funktsiooni Juhuslikult vastuste juhuslikult eri järjestuses paigutamiseks iga kord, kui vastusegruppi küsimuse puhul kasutatakse.  
5. Klõpsake suvandit Vastus.
6. Klõpsake valikut Uus.
    * Seerianumber juhib vastuste kuvamise järjestust, v.a juhul, kui vastustegrupi puhul on valitud Juhuslikult.  
    * Vastuste eest saab anda punkte küsimustiku punktiarvestuses kasutamiseks.  
7. Sisestage number väljale Punktid.
    * Õige vastuse saab märkida, näitamaks, et valitud vastus on õige. Seda saab kasutada küsimustiku punktiarvestuseks.  
8. Sisestage väärtus väljale Vastus.
    * Jätkake vastusegrupi vastuse valikuvõimaluste loomist.  
9. Klõpsake valikut Uus.
10. Sisestage number väljale Punktid.
11. Sisestage väärtus väljale Vastus.
12. Klõpsake Uus.
13. Sisestage number väljale Punktid.
14. Sisestage väärtus väljale Vastus.
15. Klõpsake Uus.
16. Sisestage number väljale Punktid.
17. Sisestage väärtus väljale Vastus.
18. Klõpsake Uus.
19. Sisestage number väljale Punktid.
20. Sisestage väärtus väljale Vastus.
21. Sulgege leht.
22. Sulgege leht.

## <a name="create-the-question"></a>Küsimuse loomine
1. Avage Küsimustik > Kujundus > Küsimused.
2. Klõpsake valikut Uus.
3. Kasutage seotud küsimuste koos grupeerimiseks välja Tüüp.
    * Saate kinniste küsimuste puhul kasutada sisendi tüüpe Märkeruut, Alternatiivne nupp või Liitboks.  
4. Valige suvand väljalt Sisendi tüüp.
5. Sisestage või valige väärtus väljal Vastustegrupp.
6. Sisestage väärtus väljale Tekst.

