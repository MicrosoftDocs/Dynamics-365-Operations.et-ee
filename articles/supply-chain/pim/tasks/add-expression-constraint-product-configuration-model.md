--- 
title: Avaldise piirangu lisamine toote konfiguratsioonimudelile
description: "See protseduur näitab, kuidas saate lisada toote konfiguratsioonimudelile uue piiranguavaldise."
author: YuyuScheller
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
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8db46c5b8361c96745b440c0d0684e18c06a6c6f
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Avaldise piirangu lisamine toote konfiguratsioonimudelile

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas saate lisada toote konfiguratsioonimudelile uue piiranguavaldise. See näitab, kuidas saate lasta lisada kõlarile nurgakaitsme, kui kasutaja on valinud metallist esivõre. See protseduur kasutab komponenti Tipptasemel kõlar demoettevõttes USMF.


## <a name="create-an-expression-constraint"></a>Avaldise piirangu loomine
1. Klõpsake valikut Tootevariandi mudeli määratlus.
2. Klõpsake valikut Toote konfiguratsioonimudelid.
3. Otsige loendist ja valige soovitud kirje.
    * Selles näites kasutatakse tipptasemel kõlari mudelit.  
4. Klõpsake loendis valitud real olevat linki.
5. Laiendage jaotist Piirangud.
6. Klõpsake vahekaarti Lisa.
7. Klõpsake käsku Loo.
8. Sisestage väärtus väljale Nimi.

## <a name="enter-expression"></a>Sisesta avaldis
1. Klõpsake käsku Muuda avaldist.
    * Kui avate selles etapis ülesande salvestises kasutajaliidese, saate kasutada piiranguavaldise koostamiseks IntelliSense’i ja sümbolite loendit.  
2. Sisestage väljale ConstraintBody tekst Implies[FrontGrill=="Metal", CornerProtection].
    * See avaldise loogika väidab: kui esivõre on metallist, tuleb valida nurkade kaitse suvand.  
3. Klõpsake suvandit Kinnita.
    * Kontrollimisfunktsioon vaatab piiranguavaldise läbi ja kontrollib süntaksivigu.  
4. Klõpsake valikut Sule.
5. Klõpsake nuppu OK.


