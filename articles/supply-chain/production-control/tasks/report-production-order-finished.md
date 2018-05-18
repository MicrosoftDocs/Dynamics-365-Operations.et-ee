---
title: "Tootmistellimuse lõpuleviimisest teatamine"
description: "See protseduur näitab, kuidas tootmistellimust lõpetatuks kinnitada."
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
ms.openlocfilehash: e6f5e7316f89ba7c2b7091eb9df02aa07ea44dbd
ms.contentlocale: et-ee
ms.lasthandoff: 02/06/2018

---
# <a name="report-a-production-order-as-finished"></a>Tootmistellimuse lõpuleviimisest teatamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas tootmistellimust lõpetatuks kinnitada. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. See on kuues protseduur seitsmest, mis selgitab tootmistellimuse elutsüklit.


## <a name="report-a-production-order-as-finished"></a>Tootmistellimuse lõpuleviimisest teatamine
1. Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.
    * Valige tootmistellimus, mille olek on Alustatud.  
2. Klõpsake toimingupaanil valikut Tootmistellimus.
3. Klõpsake valikut Kinnita lõpetamine.
    * Sellel lehel saate kinnitada valmis toote koguse, mille lõpetamine kinnitatakse.  
4. Klõpsake vahekaarti Üldine.
5. Määrake valiku Õige kogus väärtuseks 18.
6. Määrake valiku Veakogus väärtuseks 2.
7. Tehke väljal Vea põhjus valik Materjal.
8. Märkige või tühjendage ruut Lõpeta töö.
9. Valige või tühjendage märkeruut Aktsepteeri viga.
10. Klõpsake nuppu OK.

## <a name="verify-the-report-as-finished-journal"></a>Kinnitage tööleht Kinnita lõpetamine
1. Klõpsake toimingupaanil valikut Kuva.
2. Klõpsake valikut Lõpetatuna kinnitatud.
3. Märkige loendis valitud rida.
4. Klõpsake loendis valitud real olevat linki.
    * Tööleht Kinnita lõpetamine on sisestatud. Kui soovite töölehte korrigeerida, saate koostada käsitsi uue töölehe, millel saab muudatusi teha.  

