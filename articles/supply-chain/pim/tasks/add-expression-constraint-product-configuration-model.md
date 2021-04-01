---
title: Avaldise piirangu lisamine toote konfiguratsioonimudelile
description: See protseduur näitab, kuidas saate lisada toote konfiguratsioonimudelile uue piiranguavaldise.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 81026d8622d3f03b3b87747800f4845cda823569
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256155"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Avaldise piirangu lisamine toote konfiguratsioonimudelile

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]