--- 
title: Varude loendamine laos
description: "Selle protseduuriga selgitatakse lao inventuuritöölehe loomise ja sisestamise protsessi lao asukohas oleva konkreetse toote inventuuriks."
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fa72cb0d651f5e60797fa41f6e2b2cf1891730b5
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="count-inventory-in-a-warehouse"></a>Varude loendamine laos

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


