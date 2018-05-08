---
title: "Dimensioonipõhine tootekonfiguratsioon"
description: "Dimensioonipõhine toote konfigureerimine tähistab lihtsat lahendust mitme tootevariandi loomiseks ühest tooteetalonist ja selle kooslusest."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 297e60e63b88b610d0886ad16667c4f99cc74ccb
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---

# <a name="dimension-based-product-configuration"></a>Dimensioonipõhine tootekonfiguratsioon

[!include [banner](../includes/banner.md)]

Dimensioonipõhine toote konfigureerimine tähistab lihtsat lahendust mitme tootevariandi loomiseks ühest tooteetalonist ja selle kooslusest.

Dimensioonipõhine tootekonfiguratsioon on üks kolmest integreeritud tootekonfiguratsiooni tehnoloogiatest. Kaks ülejäänud tehnoloogiat on eelmääratletud variandid ja piirangupõhine konfiguratsioon. Kõik kolm tehnoloogiat kasutavad lähtepunktina tooteetaloni ja võimaldavad kasutajal luua ühele tooteetalonile palju tootevariante.

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
Dimensioonipõhise toote tootemudeli koostamise loomulik protsess algab vastavate konfiguratsioonigruppide määratlemisest. On oluline tagada, et kõik tooted, mida koosluses kasutatakse, on väljastatud ettevõttele, millele tootemudel on koostatud. Kui need koosteüksused on paigas, saab kasutaja luua koosluse ja määrata konfiguratsioonigrupid kõigile vastavatele koosluse ridadele. Kui kooslus on valmis, saab määratleda konfigureerimisprotsessi konfiguratsioonigruppide õigesse järjekorda paigutamiseks. [![Dimensioonipõhine toote modelleerimisprotsess](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Kui on olemas teatud erinevatest konfiguratsioonigruppidest pärinevaid tooteid, mida tuleb või mida ei tohi koos kasutada, saate koostada konfigureerimisreeglid, mis need tooteseosed jõustavad. Kui kooslus on seotud koosluse versiooni kaudu dimensioonipõhise tooteetaloniga ja mõlemad on kinnitatud ning aktiveeritud, saate luua tootekonfiguratsioone ja sisestada igale konfiguratsioonile nime. Konfiguratsioonid saab määratleda enne ühegi kande loomist või seda saab teha siis, kui ilmneb vajadus teatud konfiguratsiooni järele.

### <a name="suggested-use"></a>Soovituslik kasutamine

Dimensioonipõhist konfiguratsioonitehnoloogiat saab kõige paremini kasutada piiratud varieeritavusega toodete puhul ja standardsete tootedimensioonide suurus, värv, stiil ja konfiguratsioon ei sobi konkreetse tootevarianti tuvastamiseks. Näiteks võib olla jalgratas raami kõrguse, ratta suuruse, pidurite tüüpide ja erinevate käikudega.

### <a name="next-step"></a>Järgmine samm 

Järgmised kaheksa tegevuse juhist on loetletud nende tegemise järjekorras. 

1.  [Dimensioonipõhise tooteetaloni loomine (tegevuse juhis)](tasks/create-dimension-based-product-master.md)
2.  [Dimensioonipõhise tooteetaloni vabastamine (tegevuse juhis)](tasks/release-dimension-based-product-master.md)
3.  [Vabastatud tooteetaloni täielik põhiseadistus (tegevuse juhis)](tasks/complete-basic-setup-released-product-master.md)
4.  [Konfiguratsioonigruppide määratlemine (tegevuse juhis)](tasks/define-configuration-groups.md)
5.  [Dimensioonipõhise tooteetaloni jaoks koosluse loomine (tegevuse juhis)](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [Konfigureerimisprotsesside määratlemine (tegevuse juhis)](tasks/define-configuration-route.md)
7.  [Konfigureerimisreeglite loomine (tegevuse juhis)](tasks/create-configuration-rules.md)
8.  [Dimensioonipõhiste konfiguratsioonide loomine (tegevuse juhis)](tasks/create-dimension-based-configurations.md)


