---
title: Kontostruktuuride loomine
description: See ülesandejuhend kirjeldab konto struktuuri loomise etappe.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a8df7d7d9c4555bf46ac1cc3f71695837b1369b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968575"
---
# <a name="create-account-structures"></a>Kontostruktuuride loomine

[!include [banner](../../includes/banner.md)]

See ülesandejuhend kirjeldab konto struktuuri loomise etappe. Etapid kasutavad demoandmete ettevõtet USMF.

1. Avage **Navigeerimispaan > Moodulid > Pearaamat > Kontoplaan > Struktuurid > Konfigureeri konto struktuure**.
2. Rippdialoogi avamiseks klõpsake paanil **Toimingupaan** nuppu **Uus**.
3. Väljale **Konto struktuur** sisestage nimi, mis kirjeldab konto struktuuri eesmärki.
4. Väljale **Kirjeldus** sisestage kirjeldus, mis täpsustab konto struktuuri eesmärki.
5. Klõpsake käsku **Loo**.
6. Suvandis **Segmendid ja lubatud väärtused** klõpsake käsku **Lisa segment**.
7. Dimensioonide loendist valige dimensioon, mille soovite lisada konto struktuuri.
8. Loendi lõpus klõpsake käsku **Lisa segment**.
9. Korrake etappe 6 ja 9 vastavalt vajadusele.
10. Jaotises **Lubatud väärtuse üksikasjad** valige segment, et redigeerida lubatud väärtusi.
    Näiteks klõpsake välja **Põhikonto**.  
11. Väljal **Tehtemärk** valige suvand, näiteks "on vahemikus ja hõlmab".
12. Sisestage väärtus väljale **Väärtus**. Näiteks 600 000.  
13. Sisestage väärtus väljale **Kuni**. Näiteks 699 999.  
14. Jaotises **Lubatud väärtuse üksikasjad** klõpsake käsku **Rakenda**.
15. Korrake etappe 10 ja 15 vastavalt vajadusele.  
16. Jaotises **Lubatud väärtuse üksikasjad** klõpsake käsku **Lisa uus kriteerium**.
17. Väljal Tehtemärk valige suvand, näiteks "on vahemikus ja hõlmab".
18. Sisestage väärtus väljale **Väärtus**. Näiteks 033.  
19. Sisestage väärtus väljale **Kuni**. Näiteks 034.  
20. Klõpsake käsku **Rakenda**.
21. Valige ruudustikus segment, mille lubatud väärtusi soovite muuta. Näiteks Kulukeskus.  
22. Sisestage väärtus väljale **Kulukeskus**. Näiteks 007 … 021.  
23. Suvandis **Segmendid ja lubatud väärtused** klõpsake käsku **Lisa**.
24. Sisestage väärtus väljale **Põhikonto**. Näiteks 600 000 … 699 999  
25. Valige ruudustikus segment, mille lubatud väärtusi soovite muuta. Näiteks Osakond.  
26. Sisestage väärtus väljale Osakond. Näiteks 032.  
27. Sisestage väärtus väljale Kulukeskus. Näiteks 086.  
28. Paanil **Toimingupaan** klõpsake käsku **Kontrolli**.
29. Paanil **Toimingupaan** klõpsake käsku **Aktiveeri**.
30. Klõpsake käsku **Aktiveeri**.

