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
ms.openlocfilehash: 8758b74f9ce7c8687b7c2925ccd04cd512602db0
ms.sourcegitcommit: 8246ba3872a1f3eaa18c8bb1ba86d3c2142a6e10
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/31/2021
ms.locfileid: "7465169"
---
# <a name="create-a-closed-ended-question"></a>Suletud küsimuse loomine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Kinnised küsimused võimaldavad teil pakkuda valikuid, mille hulgast vastaja saab valida. Esmalt peate looma vastusegrupi vastustega, seejärel looma seda vastustegruppi kasutava küsimuse. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="create-an-answer-group"></a>Vastustegrupi loomine
1. Avage **Küsimustik** > **Kujundus** > **Vastustegrupid**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Vastustegrupp**.
4. Sisestage väärtus väljale **Kirjeldus**.
    * Kasutage funktsiooni Juhuslikult vastuste juhuslikult eri järjestuses paigutamiseks iga kord, kui vastusegruppi küsimuse puhul kasutatakse.  
5. Klõpsake suvandit **Vastus**.
6. Klõpsake valikut **Uus**.
    * Seerianumber juhib vastuste kuvamise järjestust, v.a juhul, kui vastustegrupi puhul on valitud Juhuslikult.  
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
3. Kasutage seotud küsimuste koos grupeerimiseks välja Tüüp.
    * Saate kinniste küsimuste puhul kasutada sisendi tüüpe Märkeruut, Alternatiivne nupp või Liitboks.  
4. Valige suvand väljalt **Sisendi tüüp**.
5. Sisestage või valige väärtus väljal **Vastustegrupp**.
6. **Sisestage väärtus väljale Tekst.**



[!INCLUDE[footer-include](../includes/footer-banner.md)]
