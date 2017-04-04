---
title: "Dimensioonipõhine tootekonfiguratsioon"
description: "Dimensioonipõhine toote konfigureerimine tähistab lihtsat lahendust mitme tootevariandi loomiseks ühest tooteetalonist ja selle kooslusest."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 7fbf69dc217a2f61ec3aeda952ff221491e9385a
ms.lasthandoff: 03/31/2017


---

# <a name="dimension-based-product-configuration"></a>Dimensioonipõhine tootekonfiguratsioon

Dimensioonipõhine toote konfigureerimine tähistab lihtsat lahendust mitme tootevariandi loomiseks ühest tooteetalonist ja selle kooslusest.

Toode dimensiooni konfiguratsioon on üks kolm sisseehitatud toote konfiguratsiooni tehnoloogiat. Kaks ülejäänud tehnoloogiat on eelmääratletud variandid ja piirangupõhine konfiguratsioon. Kõik kolm tehnoloogiat kasutavad lähtepunktina tooteetaloni ja võimaldavad kasutajal luua ühele tooteetalonile palju tootevariante.

## <a name="key-concepts"></a>Põhimõisted
Dimensioonipõhise tootekonfiguratsiooni aluseks on järgmised põhimõisteid.

-   Tooteetalonid
-   Konfiguratsiooni tootedimensioon
-   Konfiguratsioonigrupid
-   Kooslus
-   Konfigureerimisprotsess
-   Konfiguratsioonireeglid

### <a name="product-masters"></a>Tooteetalonid

Tooteetalon on igasuguse toote konfiguratsiooniprotsessi lähtepunkt. Toote dimensioonipõhise konfiguratsiooni puhul on vaja selle konkreetse konfiguratsioonitehnoloogiaga tooteetaloni ja toote dimensioonigruppi, mis sisaldab konfiguratsiooni tootedimensiooni.

### <a name="configuration-product-dimension"></a>Konfiguratsiooni tootedimensioon

Konfiguratsiooni tootedimensiooni kasutatakse tooteetalonide tootevariantide tuvastamiseks dimensioonipõhise konfiguratsioonitehnoloogiaga. Konfiguratsiooni dimensiooni väärtuse sisestab kasutaja ja see peaks aitama tuvastada üksikuid tootevariante.

### <a name="configuration-groups"></a>Konfiguratsioonigrupid

Konfiguratsioonigrupid määratletakse keskhoidlas ja neid saab kasutada kõigi dimensioonipõhiste toote konfiguratsioonimudelite jaoks. Konfiguratsioonigrupid on seotud üksikute koosluse ridadega ja need hoiavad koos üksteist välistavate ridade gruppi. See tähendab, et ühe tootevariandi puhul saab valida grupist ainult ühe rea.

### <a name="bill-of-materials-bom"></a>Kooslus

Kooslus tähistab dimensioonipõhise tootekonfiguratsiooni koosteüksusi. See peab sisaldama kõik tootevariandis kasutatavaid tooteid. Iga koosluse rida võib viidata konfiguratsioonigrupile. Kui rida ei viita konfiguratsioonigrupile, lisatakse see kõigile tootevariantidele.

### <a name="configuration-route"></a>Konfigureerimisprotsess

Konfiguratsiooniprotsess määrab konfiguratsioonigruppide järjestuse, nagu need kasutajale toote konfiguratsiooniprotsessis kuvatakse.

### <a name="configuration-rules"></a>Konfiguratsioonireeglid

Konfiguratsioonireeglid kajastavad mehhanismi, mis tagab, et ühes koosluse konfiguratsioonigrupis sisalduv toode lisab toote sama koosluse konfiguratsioonigruppi või arvab selle sealt välja.

## <a name="product-modeling-process"></a>Toote modelleerimisprotsess
Dimensioonipõhise toote tootemudeli koostamise loomulik protsess algab vastavate konfiguratsioonigruppide määratlemisest. On oluline tagada, et kõik tooted, mida koosluses kasutatakse, on väljastatud ettevõttele, millele tootemudel on koostatud. Komponentide kohta, kasutaja saab luua Koosluse ning määrata konfiguratsioonigruppide kõik vajalikud Koosluse read. Kui kooslus on valmis, võib määratleda konfiguratsiooniprotsessi tellimise Konfiguratsioonigrupid õiges järjestuses. \[caption id = "manuse\_282671" viia = "alignnone" width = "1187"\][![mõõtme toode protsessi modelleerimine](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) mõõtme toode protsessi modelleerimine\[/caption\] kui erinevate konfiguratsioonigruppide, et kas peab või ei tohi kasutada koos teatud tooteid, saate luua reeglid jõustavad need toote suhted. Kui kooslus on seotud koosluse versiooni kaudu dimensioonipõhise tooteetaloniga ja mõlemad on kinnitatud ning aktiveeritud, saate luua tootekonfiguratsioone ja sisestada igale konfiguratsioonile nime. Konfiguratsioonid saab määratleda enne ühegi kande loomist või seda saab teha siis, kui ilmneb vajadus teatud konfiguratsiooni järele.

### <a name="suggested-use"></a>Soovituslik kasutamine

Dimensioonipõhist konfiguratsioonitehnoloogiat saab kõige paremini kasutada piiratud varieeritavusega toodete puhul ja standardsete tootedimensioonide suurus, värv, stiil ja konfiguratsioon ei sobi konkreetse tootevarianti tuvastamiseks. Näiteks võib olla jalgratas raami kõrguse, ratta suuruse, pidurite tüüpide ja erinevate käikudega.


