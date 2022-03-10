---
title: Kontostruktuuride loomine
description: See ülesandejuhend kirjeldab konto struktuuri loomise etappe.
author: aprilolson
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9ba43e243df4ba4b7c0eb6188629686206ff09b
ms.sourcegitcommit: 03f53980a4bc67b73ac2be76a3b3e7331d0db705
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/18/2021
ms.locfileid: "7394535"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
