---
title: Täpsemate reeglistruktuuride loomine ja määramine
description: See artikkel selgitab, kuidas konto struktuuri täpsemat reeglistruktuuri luua ja määrata.
author: aprilolson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72688642936f9428c96aebb34bf9f240dd48b46b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896315"
---
# <a name="create-and-assign-advanced-rule-structures"></a>Täpsemate reeglistruktuuride loomine ja määramine

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas konto struktuuri täpsemat reeglistruktuuri luua ja määrata. Juhendis kasutatakse demoettevõtte USMF andmeid.

## <a name="create-an-advanced-rule-structure"></a>Täpsema reegli struktuuri loomine
1. Avage **Navigeerimispaan > Pearaamat > Kontoplaan > Struktuurid > Täpsema reegli struktuurid**.
2. Rippdialoogi avamiseks valige **Uus**.
3. Sisestage väljale **Täpsema reegli struktuur** reegli struktuuri kirjeldav nimi.
4. Valige nupp **OK**.
5. Valige nupp **Lisa segment**.
6. Valige segmentide loendist finantsdimensioon. Näiteks **Pood**.  
7. Valige nupp **Lisa segment**.
8. Valige **Aktiveeri**.

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a>Täpsema reegli rakendamine konto struktuurile.
1. Avage **Navigeerimispaan > Moodulid > Pearaamat > Kontoplaan > Struktuurid >Konfigureeri konto struktuurid**.
2. Leidke ja valige loendist konto struktuur, millele soovite täpsema reegli rakendada.
3. Valige suvand **Redigeeri**. Võite klõpsata ka suvandit **Täpsemad reeglid**, seejärel palutakse teil panna konto struktuur **mustandrežiimi**.  
4. Valige **Täpsemad reeglid**.
5. Rippdialoogi avamiseks valige **Uus**.
6. Sisestage väärtus väljale **Täpsem reegel**.
7. Sisestage väärtus väljale **Nimi**.
8. Valige **Loo**.
9. Valige **Lisa uus kriteerium**.
10. Väljal **Kus** valige põhikonto või finantsdimensioon.
11. Valige suvand väljal **Operaator**, näiteks **vahemikus** ja **hõlmab**.
12. Sisestage väärtus väljale **Väärtus**.
13. Sisestage väärtus väljale **Kuni**.
14. Klõpsake valikut **Lisa** rippdialoogi avamiseks.
15. Leidke loendis täpsema reegli struktuur, mida soovite kasutada, kui teie sisestatud kriteeriumid on täidetud.
16. Valige **Lisa**.
17. Sulgege leht.
18. Valige **Aktiveeri**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
