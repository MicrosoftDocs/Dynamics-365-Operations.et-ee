---
title: Kaubakatte reeglite määratlemine
description: Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 02aa3b2b7924cdf6317225bfce23f182aa390b8c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "320623"
---
# <a name="define-coverage-rules-for-items"></a>Kaubakatte reeglite määratlemine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. See protseduur näitab, kuidas luua laovarude reegleid ja tühistada kindla kaupa laovarude sätteid. Samuti näitab see, kuidas määrata varude vaikesätteid.


## <a name="create-a-coverage-group"></a>Laovarude grupi loomine
1. Avage Laovarude grupid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Laovarude grupp.
4. Sisestage väärtus väljale Nimi.
5. Sisestage väärtus väljale Kalender.
    * Valige kalender, mida kasutatakse koondplaneerimises gruppi kuuluvate kaupade täiendamissoovituste loomisel.  
6. Valige suvand väljal Laovarude kood.
    * Valige nõue selle protseduuri jaoks.  
7. Sisestage väärtus „90” väljale Laovarude ajapiir (päevades).
    * Sellesse gruppi kuuluvate kaupade jaoks loob koondplaneerimine täiendamise soovitused kuni 90 päeva ette.  
8. Sisestage väärtus „1” väljale Negatiivsed päevad.
9. Sisestage väärtus „1” väljale Positiivsed päevad.
10. Laiendage või ahendage jaotist Muu.
11. Sisestage väärtus „1” väljale Vajaduse kuupäevale lisatud sissetuleku ohutusvaru.
    * Näiteks kui sissetuleku ohutusvaru on seatud 1 päevale ja ostutellimuse rida on planeeritud sissetulekuks 15. mail, siis arvutatakse planeerimisel korrigeeritud sissetulekukuupäevaks 16. mai.  
12. Sisestage väärtus „1” väljale Vajaduse kuupäevast maha arvatud väljamineku ohutusvaru.
    * Näiteks kui ohutusvaru on seatud 1 päevale ja müügitellimuse rida on planeeritud tarnimiseks 15. mail, siis arvutatakse koondplaneerimisel korrigeeritud tarnekuupäevaks 14. mai.  
13. Sisestage väärtus „1” väljale Kauba täitmisajale lisatud lisatellimuse ohutusvaru.
14. Klõpsake nuppu Salvesta.

## <a name="create-a-new-product"></a>Uue toote loomine
1. Avage Väljastatud tooted.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Toote number.
4. Sisestage väärtus väljale Toote nimi.
5. Klõpsake väljal Kauba mudeligrupp otsingu avamiseks ripploendi nuppu.
6. Otsige loendist ja valige soovitud kirje.
7. Klõpsake loendis valitud real olevat linki.
8. Klõpsake väljal Kaubagrupp otsingu avamiseks ripploendi nuppu.
9. Otsige loendist ja valige soovitud kirje.
10. Klõpsake loendis valitud real olevat linki.
11. Klõpsake väljal Laoala dimensiooni grupp otsingu avamiseks ripploendi nuppu.
12. Otsige loendist ja valige soovitud kirje.
13. Klõpsake loendis valitud real olevat linki.
14. Klõpsake väljal Jälgimisdimensiooni grupp otsingu avamiseks ripploendi nuppu.
15. Otsige loendist ja valige soovitud kirje.
16. Klõpsake loendis valitud real olevat linki.
17. Klõpsake nuppu OK.

## <a name="setup-default-order-settings"></a>Vaike-tellimissätete seadistamine
1. Klõpsake toimingupaanil valikut Plaan.
2. Klõpsake valikut Tellimuse vaikesätted.
3. Sisestage ostutellimuste loomisel vaikekohana kasutatav koht väljal Ostukoht.
4. Sisestage väljale Varude tegevuskoht kaupa hoidmise asukoht.
5. Laiendage või ahendage jaotist Varud.
6. Määrake valiku Mitu väärtuseks „10”.
7. Määrake Min tellimuse koguseks 10.
8. Määra maksimaalseks tellimuse koguseks 100.
9. Määrake välja Vaikekogus väärtuseks „10”.
10. Sisestage arv väljale Ostu täitmisaeg.
11. Valige või tühjendage märkeruut Tööpäevad.
12. Klõpsake nuppu Salvesta.
13. Valige Ostutellimus väljal Vaikimisi tellimusetüüp.
14. Klõpsake nuppu Salvesta.
15. Sulgege leht.
    * Sulgege leht Tellimuse vaikesätted.  

## <a name="add-an-item-to-a-coverage-group"></a>Kauba lisamine laovarude gruppi
1. Laiendage või ahendage jaotist Plaan.
2. Klõpsake väljal Laovarude grupp otsingu avamiseks ripploendi nuppu.
3. Leidke loendist loodud laovarude grupp.
4. Klõpsake loendis valitud real olevat linki.

## <a name="create-item-coverage-rules"></a>Kauba laovarude reeglite loomine
1. Klõpsake toimingupaanil valikut Plaan.
2. Klõpsake valikut Kauba laovarud.
3. Klõpsake valikut Uus.
4. Klõpsake vahekaarti Üldine.
5. Märkige ruut suvandi Tühista laovarude grupi sätted päises.
6. Sisestage väärtus „60” väljale Laovarude ajapiir (päevades).
    * Kuigi kaubad laovarude grupis Vajadus on plaanitud 90 päeva ette, plaanitakse see kaup 60 päeva ette.  
7. Sisestage väärtus „2” väljale Negatiivsed päevad.
8. Sisestage väärtus „2” väljale Positiivsed päevad.
9. Klõpsake vahekaarti Täitmisaeg.
10. Märkige ruut suvandi Ost päises.
11. Sisestage väärtus „5” väljale Ostuaeg.
12. Klõpsake nuppu Salvesta.

