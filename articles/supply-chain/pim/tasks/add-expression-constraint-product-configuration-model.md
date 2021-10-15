---
title: Avaldise piirangu lisamine toote konfiguratsioonimudelile
description: See protseduur näitab, kuidas saate lisada toote konfiguratsioonimudelile uue piiranguavaldise.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 77e8b991a2615a8f5d238acc4655f231edb6ca98
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569645"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Avaldise piirangu lisamine toote konfiguratsioonimudelile

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas saate lisada toote konfiguratsioonimudelile uue piiranguavaldise. See näitab, kuidas saate lasta lisada kõlarile nurgakaitsme, kui kasutaja on valinud metallist esivõre. See protseduur kasutab komponenti Tipptasemel kõlar demoettevõttes USMF.

## <a name="create-an-expression-constraint"></a>Avaldise piirangu loomine

1. Avage **Tooteteabe haldus \> Tooted \> Tootekonfiguratsiooni mudelid**.
3. Otsige loendist ja valige soovitud kirje.
    * Selles näites kasutatakse tipptasemel kõlari mudelit.  
4. Valige loendis link valitud reas.
5. Laiendage jaotist **Piirangud**.
6. Valige **Lisa**.
7. Valige **Loo**.
8. Sisestage väärtus väljale **Nimi**.

## <a name="enter-expression"></a>Sisesta avaldis

1. Valige **Redigeeri avaldis**.
    * Kui avate selles etapis ülesande salvestises kasutajaliidese, saate kasutada piiranguavaldise koostamiseks IntelliSense’i ja sümbolite loendit.  
2. Sisestage väljale **ConstraintBody** tekst Implies[FrontGrill=="Metal", CornerProtection].
    * See avaldise loogika väidab: kui esivõre on metallist, tuleb valida nurkade kaitse suvand.  
3. Valige **Kinnita**.
    * Kontrollimisfunktsioon vaatab piiranguavaldise läbi ja kontrollib süntaksivigu.  
4. Valige suvand **Sule**.
5. Valige nupp **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]