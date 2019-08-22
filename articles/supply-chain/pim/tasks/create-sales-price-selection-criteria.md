---
title: Müügihinna valikukriteeriumide loomine
description: See protseduur näitab, kuidas luua atribuudipõhistele hinnamudelitele müügihinna valikukriteeriumi.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72940f719baca5e8042c2f2caa8abbacb7d8264e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844485"
---
# <a name="create-sales-price-selection-criteria"></a>Müügihinna valikukriteeriumide loomine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas luua atribuudipõhistele hinnamudelitele müügihinna valikukriteeriumi. See protseduur nõuab, et saadaval oleks vähemalt üks müügihinna mudel. Selles näites kasutatakse hinnamudelina demoettevõtte USMF müügihinnamudelit Kõlarilahendus. Tavaliselt kasutab seda protseduuri tootejuht.


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Lisage olemasolevale müügihinna mudelile uus kriteerium
1. Klõpsake valikut Tootevariandi mudeli määratlus.
2. Klõpsake valikut Toote konfiguratsioonimudelid.
3. Valige loendist tootemudeli Kõlarilahendus rida, kuid ärge klõpsake mudeli nime linki.
4. Klõpsake tegumiribal valikut Mudel.
5. Klõpsake valikut Hinnamudeli kriteeriumid.
6. Klõpsake valikut Uus.
7. Tippige väljale Nimi tekst Kliendigrupp 10.
    * Hinnamudeli kriteeriumi nime abil saab tuvastada aluseks olevad valikukriteeriumid.  
8. Valige või sisestage väärtus väljal Hinnamudel.
9. Tehke väljal Tellimuse tüüp valik Müügitellimus.
    * Tellimuse tüüp määrab andmebaasiväljad, mis on valikupäringu puhul saadaval.  
10. Sisestage kuupäev väljale Kehtiv alates.
11. Sisestage kuupäev väljale Loe aegunuks kuupäeval.
12. Klõpsake nuppu Salvesta.

## <a name="create-the-query-for-the-selection-criteria"></a>Valikukriteeriumile päringu loomine
1. Klõpsake nuppu Redigeeri.
2. Valige Kliendid väljalt Tabel. 
3. Valige Kliendigrupp väljalt Väli.
    * Selles näites kasutame valikukriteeriumide puhul konkreetset kliendigruppi.  
4. Valige Kliendigrupp 10 väljalt Kriteerium. 
5. Klõpsake nuppu OK.

