--- 
title: Puhvervaru abil minimaalse laovaru uuendamine
description: "See protseduur näitab, kuidas arvutada varasemate kannete põhjal minimaalse laovaru soovitusi ja uuendada siis soovituste abil kauba laovaru."
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 72b873faaee7bc86bd98f90ca2fb12a216d2f06b
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# Puhvervaru abil minimaalse laovaru uuendamine

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas arvutada varasemate kannete põhjal minimaalse laovaru soovitusi ja uuendada siis soovituste abil kauba laovaru. Seda tehakse puhvervaru töölehe abil. Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid. See ülesanne on mõeldud tootmise plaanijale minimaalsete laovarude säilitamiseks.


## Uue puhvervaru töölehe nime loomine
1. Avage Puhvervaru töölehe nimed.
2. Klõpsake valikut Uus.
3. Tippige väljale Nimi väärtus Materjal.
4. Tippige väljale Kirjeldus väärtus Materjal.
5. Sulgege leht.

## Puhvervaru töölehe loomine
1. Avage Puhvervaru arvutamine.
2. Klõpsake valikut Uus.
3. Sisestage või valige väärtus väljal Nimi.
    * Valige puhvervaru töölehe nimi, mille lõite, nt Materjal.  
4. Klõpsake suvandit Loo read.
5. Sisestage kuupäev väljale Alguskuupäev.
    * Määrake kuupäevaks 2015-01-02.  
6. Sisestage kuupäev väljale Lõpukuupäev.
    * Määrake kuupäevaks 2015-12-30.  
7. Klõpsake nuppu OK.
    * See loob read dimensioonidele, millel on laokanded.  

## Arvuta soovitus
1. Klõpsake valikut Arvuta soovitus.
2. Tehke valik Kasuta täitmisaja jooksul keskmist väljaminekut.
3. Määrake valiku Korrutustegur väärtuseks 10.
    * Tegurit Korruta kasutatakse soovituse korrigeerimiseks. Kuna demoandmetel on vaid mõned kanded, tuleb realistliku soovituse saamiseks tegur määrata.  
4. Klõpsake nuppu OK.
    * Kerige alla M0002 ja M0003 leidmiseks. Vaadake veergu Arvutatud miinimumkogus.   

## Miinimumkoguse uuendamine
1. Sisestage number väljale Uus miinimumkogus.
    * Uuendage väärtust Uus miinimumkogus nii, et see vastaks väärtusele jaotises Arvutatud miinimumkogus. Kui Arvutatud miinimum on null, võite sisestada soovitud tulevase väärtuse. Näiteks võite sisestada sellele väljale väärtuse Arvutatud miinimumkogus M0002 kohta, millel on ladu 12.  
2. Otsige loendist ja valige soovitud kirje.
    * Näiteks võite valida M0002, millel on ladu 12.  
3. Sisestage number väljale Uus miinimumkogus.
    * Uuendage väärtust Uus miinimumkogus nii, et see vastaks väärtusele jaotises Arvutatud miinimumkogus. Kui Arvutatud miinimum on null, võite sisestada soovitud tulevase väärtuse.  

## Uue miinimumkoguse sisestamine ja tulemuse kinnitamine
1. Klõpsake valikut Sisesta.
2. Klõpsake nuppu OK.
3. Klõpsake, et järgida linki väljal Kaubakood.
4. Klõpsake, et järgida linki väljal Kaubakood.
5. Klõpsake toimingupaanil valikut Plaan.
6. Klõpsake valikut Kauba laovarud.
    * Pange tähele, et miinimumkoguseks on määratud uus miinimumkogus puhvervaru töölehelt.  

