--- 
title: "Tööaja mallide loomine"
description: "Tööajamallid määratlevad kogu nädala tööaja ja neid kasutatakse ajavahemiku tööaegade loomiseks."
author: sorenva
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: ff1978f127a014e75619a4bbbb9b6ff3a3ad7c7a
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="create-working-time-templates"></a>Tööaja mallide loomine

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tööajamallid määratlevad kogu nädala tööaja ja neid kasutatakse ajavahemiku tööaegade loomiseks. See protseduur näitab, kuidas tööajamalli määratleda, kasutades tööaja plaanimise atribuute tööajaintervallide kategooriatesse jaotamiseks. Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.

1. Avage Kõik tööruumid > Ressursi elutsükli haldus.
2. Klõpsake valikut Tööajamallid.

## <a name="create-working-time-template"></a>Tööajamalli loomine
1. Klõpsake valikut Uus.
2. Tippige väärtus väljale Tööaeg.
3. Sisestage väärtus väljale Nimi.
4. Laiendage jaotist Esmaspäev.
5. Klõpsake vahekaarti Lisa.
6. Sisestage kellaaeg väljale Alates.
    * Määrake kellaaeg, millal töö hommikul algab.  
7. Sisestage kellaaeg väljale Kuni.
    * Määrake töötajate lõunavaheaja alguskellaaeg.  
8. Klõpsake vahekaarti Lisa.
9. Sisestage kellaaeg väljale Alates.
    * Määrake töö jätkamise kellaaeg pärast lõunat.  
10. Sisestage kellaaeg väljale Kuni.
    * Määrake tööpäeva lõpp.  

## <a name="replicate-working-times-to-all-week-days"></a>Tööaegade kopeerimine kõigile nädalapäevadele
1. Klõpsake valikut Kopeeri päev.
    * Kopeerige tööajamääratlused esmaspäevalt teisipäevale.  
2. Klõpsake nuppu OK.
3. Klõpsake valikut Kopeeri päev.
    * Kopeerige tööajamääratlused esmaspäevalt kolmapäevale.  
4. Tehke valik väljal Kuni nädalapäevani.
5. Klõpsake nuppu OK.
6. Klõpsake valikut Kopeeri päev.
    * Kopeerige tööajamääratlused esmaspäevalt neljapäevale.  
7. Tehke valik väljal Kuni nädalapäevani.
8. Klõpsake nuppu OK.
9. Klõpsake valikut Kopeeri päev.
    * Kopeerige tööajamääratlused esmaspäevalt reedele.  
10. Tehke valik väljal Kuni nädalapäevani.
11. Klõpsake nuppu OK.

## <a name="define-time-slots-for-special-operations"></a>Eritoimingute ajavahemike määratlemine
1. Laiendage jaotist Reede.
2. Otsige loendist ja valige soovitud kirje.
3. Valige või sisestage väärtus väljal Atribuut.
4. Otsige loendist ja valige soovitud kirje.
5. Valige või sisestage väärtus väljal Atribuut.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Puhkepäevade märkimine komplekteerimiseks suletuks
1. Laiendage jaotist Laupäev.
2. Valige Jah väljal Komplekteerimiseks suletud.
3. Laiendage jaotist Pühapäev.
4. Valige Jah väljal Komplekteerimiseks suletud.


