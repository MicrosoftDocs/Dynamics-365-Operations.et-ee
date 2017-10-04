---
title: Varude loendamine laos
description: "Selle protseduuriga selgitatakse lao inventuuritöölehe loomise ja sisestamise protsessi lao asukohas oleva konkreetse toote inventuuriks."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 1d2ecf1cd80e05b59f206fb5f684d6a86fa5733e
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="count-inventory-in-a-warehouse"></a>Varude loendamine laos

[!include[task guide banner](../../includes/task-guide-banner.md)]

Selle protseduuriga selgitatakse lao inventuuritöölehe loomise ja sisestamise protsessi lao asukohas oleva konkreetse toote inventuuriks. Seda protseduuri rakendatakse funktsiooni „üldine ladustamine” puhul laohalduse moodulis, mitte ladustamisfunktsiooni puhul moodulis Laohaldus. Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades. Kui kasutate oma andmeid, siis veenduge, et teil oleksid tooted ja asukohad seadistatud ja et oleksite loonud inventuuritöölehtedele varude töölehe nime. Inventuuri teeb harilikult laotöötaja.


## <a name="create-an-inventory-counting-journal"></a>Lao inventuuritöölehe loomine
1. Avage Laohaldus > Töölehe sisestused > Kauba inventuur > Inventuur.
2. Klõpsake valikut Uus.
3. Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.
4. Klõpsake loendis soovitud lao inventuuritöölehe nime
    * Mõned muud väljad täidetakse teie valitud lao inventuuritöölehe nime seadistuse põhjal.  
5. Klõpsake väljal Töötaja otsingu avamiseks ripploendi nuppu.
6. Valige loendist töötaja, keda soovite kasutada.
7. Klõpsake Vali.
8. Klõpsake nuppu OK.

## <a name="create-journal-lines"></a>Tööleheridade loomine
1. Klõpsake valikut Uus.
2. Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.
3. Otsige loendist ja valige soovitud kirje.
    * Kui kasutate demoettevõtte USMF andmeid, valige A0001.  
4. Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.
5. Otsige loendist ja valige soovitud kirje.
    * Kui kasutate demoettevõtte USMF andmeid, valige tegevuskoht 2.  
6. Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.
7. Otsige loendist ja valige soovitud kirje.
    * Kui kasutate demoettevõtte USMF andmeid, valige ladu 24.  
8. Klõpsake väljal Asukoht otsingu avamiseks ripploendi nuppu.
9. Otsige loendist ja valige soovitud kirje.
    * Kui kasutate demoettevõtte USMF andmeid, valige tegevuskoht BULK-001.  
10. Sisestage number väljale Loendatud.
    * Kui sisestate loendatud arvu, mis erineb väljal Laoseis näidatud arvust, värskendatakse välja Kogus, näidates lahknevust.  
11. Klõpsake nuppu Salvesta.

## <a name="post-the-inventory-counting-journal"></a>Lao inventuuritöölehe sisestamine
1. Klõpsake valikut Sisesta.
    * Kui sisestate lao inventuuritöölehe ja loendatud arv erineb väljal Laoseis olevast kogusest, sisestatakse lao sissetulek või väljaminek, kaubavaru taset ja väärtust muudetakse ja tekitatakse pearaamatukanded.  
2. Klõpsake nuppu OK.

## <a name="view-inventory-transactions"></a>Varude kannete kuvamine
1. Klõpsake Ladu.
2. Klõpsake suvandit Kanded.
    * Siin saate vaadata kõiki seotud kandeid, mis teie laoinventuuri töölehe sisestamisel luuakse.   
