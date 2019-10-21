---
title: Käibemaksukoodide seadistamine
description: Selles teemas selgitatakse, kuidas seadistada käibemaksukoode rakenduses Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45a4a7a20b20961d707e43b35d61c10a08c74943
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185976"
---
# <a name="set-up-sales-tax-codes"></a>Käibemaksukoodide seadistamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles teemas selgitatakse, kuidas seadistada käibemaksukoode. Käibemaksukoodid luuakse iga kaudse maksu või kohustuse puhul, mida juriidiline isik on kohustatud arvutama, koguma ja käibemaksuhalduritele maksma.

See ülesanne kasutab demoettevõtte USMF andmeid.

1. Avage **Navigeerimispaan > Maks > Kaudsed maksud > Käibemaks > Käibemaksukoodid**.
2. Valige suvand **Uus**.
3. Sisestage väärtus väljale **Käibemaksukood**.
4. Sisestage väärtus väljale **Nimi**.
5. Valige ripploendit avades **Makseperiood**, et määrata, millisele maksumetile ja milliste intervallidega tuleb selle käibemaksu aruanded esitada ja maksud ära maksta.
6. Valige **Pearaamatusse kandmise grupp**, et määrata põhikontod käibemaksu pearaamatusse kandmiseks.
7. Laiendage kiirkaarti **Arvutused**. See sisaldab mitmeid välju, mis juhivad seda, kuidas käibemaksu summasid arvutatakse. Täitke need väljad vastavalt vajadusele.  
8. Valige liidese ülaosas **Toimingupaanil** valik **Käibemaksukood**.
9. Valige **Väärtused**.
10. Sisestage väärtus sellele käibemaksukoodile veerus **väärtus**.
    - Kui päritolu välja kiirkaardil **Arvutused** on valitud summa üksuse kohta, korrutatakse väärtust kande kogusega, et arvutada käibemaksu summa.  Kui maksukood pole ühikupõhine maks, on väärtus protsent, mis rakendatakse selle maksukoodi päritolule käibemaksu summa arvutamiseks.     
11. Valige käsk **Salvesta**.
12. Sulgege leht.
13. Valige käsk **Salvesta**.

