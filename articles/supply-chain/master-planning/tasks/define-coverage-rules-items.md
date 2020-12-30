---
title: Kaubakatte reeglite määratlemine
description: Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.
author: ShylaThompson
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11d92185bdbcf7aa1a668b6d2aa311805e42293c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426275"
---
# <a name="define-coverage-rules-for-items"></a>Kaubakatte reeglite määratlemine

[!include [banner](../../includes/banner.md)]

Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. See protseduur näitab, kuidas luua laovarude reegleid ja tühistada kindla kaupa laovarude sätteid. Samuti näitab see, kuidas määrata varude vaikesätteid.


## <a name="create-a-coverage-group"></a>Laovarude grupi loomine
1. Avage **Navigeerimispaan > Moodulid > Koondplaneerimine > Häälestus > Laovarude grupid**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Laovarude grupp**.
4. Sisestage väärtus väljale **Nimi**.
5. Sisestage väärtus väljale **Kalender**. Valige kalender, mida kasutatakse koondplaneerimises gruppi kuuluvate kaupade täiendamissoovituste loomisel.  
6. Valige suvand väljal **Laovarude kood**. Valige nõue selle protseduuri jaoks.  
7. Sisestage väärtus „90” **väljale Laovarude ajapiir (päevades)**. Sellesse gruppi kuuluvate kaupade jaoks loob koondplaneerimine täiendamise soovitused kuni 90 päeva ette.  
8. Sisestage väärtus „1” väljale **Negatiivsed päevad**.
9. Sisestage väärtus „1” väljale **Positiivsed päevad**.
10. Laiendage või ahendage jaotist **Muu**.
11. Sisestage jaotises **Ohutuspiirid päevades** väljale **Vajaduse kuupäeva sissetuleku ohutusvaru** sisestage 1. Näiteks kui sissetuleku ohutusvaru on seatud 1 päevale ja ostutellimuse rida on planeeritud sissetulekuks 15. mail, siis arvutatakse planeerimisel korrigeeritud sissetulekukuupäevaks 16. mai.  
12. Sisestage väärtus „1” väljale **Vajaduse kuupäevast maha arvatud väljamineku ohutusvaru**. Näiteks kui ohutusvaru on seatud 1 päevale ja müügitellimuse rida on planeeritud tarnimiseks 15. mail, siis arvutatakse koondplaneerimisel korrigeeritud tarnekuupäevaks 14. mai.  
13. Sisestage väärtus „1” väljale **Kauba täitmisajale lisatud lisatellimuse ohutusvaru**.
14. Klõpsake valikut **Salvesta**.

## <a name="create-a-new-product"></a>Uue toote loomine
1. Avage **Navigeerimispaan > Moodulid > Tooteteabe haldus > Tooted > Väljastatud tooted**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Toote number**.
4. Sisestage väärtus väljale **Toote nimi**.
5. Klõpsake väljal **Kauba mudeligrupp** otsingu avamiseks ripploendi nuppu.
6. Otsige loendist ja valige soovitud kirje.
7. Klõpsake loendis valitud real olevat linki.
8. Klõpsake väljal **Kaubagrupp** otsingu avamiseks ripploendi nuppu.
9. Otsige loendist ja valige soovitud kirje.
10. Klõpsake loendis valitud real olevat linki.
11. Klõpsake väljal **Laoala dimensiooni grupp** otsingu avamiseks ripploendi nuppu.
12. Otsige loendist ja valige soovitud kirje.
13. Klõpsake loendis valitud real olevat linki.
14. Klõpsake väljal **Jälgimisdimensiooni grupp** otsingu avamiseks ripploendi nuppu.
15. Otsige loendist ja valige soovitud kirje.
16. Klõpsake loendis valitud real olevat linki.
17. Klõpsake valikut **OK**.

## <a name="setup-default-order-settings"></a>Vaike-tellimissätete seadistamine
1. Klõpsake **Toimingupaanil** valikut **Plaan**.
2. Suvandil **Tellimuse sätted** klõpsake **Tellimuse vaikesätted**.
3. Sisestage **Ostutellimuste** loomisel vaikekohana kasutatav koht väljal **Ostukoht**.
4. Sisestage väljale **Varude tegevuskoht** kaupa hoidmise asukoht.
5. Laiendage või ahendage jaotist **Laoseis**.
6. Sisestage väljale **Mitu** väärtus „10“.
7. Tippige väljale **min. tellimuse kogus** väärtus 10.
8. Tippige väljale **maks. tellimuse kogus** väärtus 100.
9. Tippige väljale **standard tellimuse kogus** väärtus 10.
10. Sisestage number väljale **Ostu täitmisaeg**.
11. Valige või puhastage märkeruut **Tööpäevad**.
12. Klõpsake valikut **Salvesta**.
13. Väljal **Vaiketellimuse tüüp** valige „Ostutellimus“.
14. Klõpsake valikut **Salvesta**.
15. Sulgege leht. Sulgege leht Tellimuse vaikesätted.  

## <a name="add-an-item-to-a-coverage-group"></a>Kauba lisamine laovarude gruppi
1. Laiendage või ahendage jaotist **Plaan**.
2. Klõpsake väljal **Laovarude grupp** otsingu avamiseks ripploendi nuppu.
3. Leidke loendist loodud **laovarude grupp**.
4. Klõpsake loendis valitud real olevat linki.

## <a name="create-item-coverage-rules"></a>Kauba laovarude reeglite loomine
1. Klõpsake **Toimingupaanil** valikut **Plaan**.
2. Jaotises **Laovarud** klõpsake valikut **Kauba laovaru**.
3. Klõpsake valikut **Uus**.
4. Klõpsake vahekaarti **Üldine**.
5. Märkige ruut suvandi **Tühista laovarude rühma** sätted päises.
6. Sisestage väärtus „60” väljale **Laovarude ajapiir (päevades)**. Kuigi kaubad laovarude grupis Vajadus on plaanitud 90 päeva ette, plaanitakse see kaup 60 päeva ette.  
7. Sisestage väärtus „2” väljale **Negatiivsed päevad**.
8. Sisestage väärtus „2” väljale **Positiivsed päevad**.
9. Klõpsake vahekaarti **Täitmisaeg**.
10. Märkige ruut suvandi **Ost** päises.
11. Sisestage väljale **Ostu aeg** väärtus „5“.
12. Klõpsake valikut **Salvesta**.

