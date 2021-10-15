---
title: Tootmistellimuse lõpuleviimisest teatamine
description: See protseduur näitab, kuidas tootmistellimust lõpetatuks kinnitada.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd, ProdSetupReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa27691942b27886e85c52b7b3a736a62db7b7bd
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580596"
---
# <a name="report-a-production-order-as-finished"></a>Tootmistellimuse lõpuleviimisest teatamine

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]