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
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3b90bb2a4981f32feb10ee1192e9c4d2e604e7a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071714"
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
    * **Kasutage funktsiooni Randomize** vastuste juhuslikuks paigutamiseks erinevasse järjestusse iga kord, kui vastuserühma küsimuse jaoks kasutatakse.  
5. Klõpsake suvandit **Vastus**.
6. Klõpsake valikut **Uus**.
    * Järjekorranumber juhib vastuste kuvamise järjekorda, välja arvatud juhul, kui **rühma Vastus jaoks** on valitud **randomiseerimine**.  
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
3. **Välja Tüüp** abil saate rühmitada seotud küsimusi koos.
    * Suletud küsimuste puhul saate kasutada **märkeruudu**, **alternatiivinuppu** või **liitbotüüpe**.  
4. Valige suvand väljalt **Sisendi tüüp**.
5. Sisestage või valige väärtus väljal **Vastustegrupp**.
6. **Sisestage väärtus väljale Tekst.**



[!INCLUDE[footer-include](../includes/footer-banner.md)]
