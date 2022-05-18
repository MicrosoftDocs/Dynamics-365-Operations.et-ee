---
title: Suletud küsimuse loomine
description: Kinnised küsimused võimaldavad teil pakkuda valikuid, mille hulgast vastaja saab valida.
author: twheeloc
ms.date: 08/26/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 18b755675b97e608afccea2e48ea3cfca74c984f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686159"
---
# <a name="create-a-closed-ended-question"></a>Suletud küsimuse loomine


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Kinnised küsimused võimaldavad teil pakkuda valikuid, mille hulgast vastaja saab valida. Esmalt peate looma vastusegrupi vastustega, seejärel looma seda vastustegruppi kasutava küsimuse. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="create-an-answer-group"></a>Vastustegrupi loomine
1. Avage **Küsimustik** > **Kujundus** > **Vastustegrupid**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Vastustegrupp**.
4. Sisestage väärtus väljale **Kirjeldus**.
    * Vastuste juhuslikuks **paigutamiseks** kasutage funktsiooni Randomize iga kord, kui vastusegruppi küsimuse jaoks kasutatakse.  
5. Klõpsake suvandit **Vastus**.
6. Klõpsake valikut **Uus**.
    * Järjekorranumber reguleerib vastuste kuvamise järjestust, v.a **juhul, kui** vastusegrupi jaoks on valitud **Juhuslik**.  
    * Vastuste eest saab anda punkte küsimustiku punktiarvestuses kasutamiseks.  
7. Sisestage number väljale **Punktid**.
    * Õige vastuse saab märkida, näitamaks, et valitud vastus on õige. Seda saab kasutada küsimustiku punktiarvestuseks.  
8. Sisestage väärtus väljale **Vastus**.
    * Jätkake vastusegrupi vastuse valikuvõimaluste loomist.  
9. Klõpsake valikut **Uus**.
10. Sisestage number väljale **Punktid**.
11. Sisestage väärtus väljale **Vastus**.
12. Klõpsake valikut **Uus**.
13. Sisestage number väljale **Punktid**.
14. Sisestage väärtus väljale **Vastus**.
15. Klõpsake valikut **Uus**.
16. Sisestage number väljale **Punktid**.
17. Sisestage väärtus väljale **Vastus**.
18. Klõpsake valikut **Uus**.
19. Sisestage number väljale **Punktid**.
20. Sisestage väärtus väljale **Vastus**.
21. Sulgege leht.
22. Sulgege leht.

## <a name="create-the-question"></a>Küsimuse loomine
1. Avage **Küsimustik** > **Kujundus** > **Küsimused**.
2. Klõpsake valikut **Uus**.
3. Välja Tüüp **abil** grupeerige seotud küsimused koos.
    * Suletud küsimuste puhul saate kasutada **sisenditüüpe** **Märkeruut**, **Alternatiivne nupp** või Liitboks.  
4. Valige suvand väljalt **Sisendi tüüp**.
5. Sisestage või valige väärtus väljal **Vastustegrupp**.
6. **Sisestage väärtus väljale Tekst.**



[!INCLUDE[footer-include](../includes/footer-banner.md)]
