---
title: Müügihinna valikukriteeriumide loomine
description: See protseduur näitab, kuidas luua atribuudipõhistele hinnamudelitele müügihinna valikukriteeriumi.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 84cef2cbf6f9783f0629fe068a4779a99dca9711
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258586"
---
# <a name="create-sales-price-selection-criteria"></a>Müügihinna valikukriteeriumide loomine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas luua atribuudipõhistele hinnamudelitele müügihinna valikukriteeriumi. See protseduur nõuab, et saadaval oleks vähemalt üks müügihinna mudel. Selles näites kasutatakse hinnamudelina demoettevõtte USMF müügihinnamudelit Kõlarilahendus. Tavaliselt kasutab seda protseduuri tootejuht.


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Lisage olemasolevale müügihinna mudelile uus kriteerium
1. Klõpsake valikut Tootevariandi mudeli määratlus.
2. Klõpsake valikut Toote konfiguratsioonimudelid.
3. Valige loendist tootemudeli Kõlarilahendus rida, kuid ärge klõpsake mudeli nime linki.
4. Klõpsake tegumiribal valikut Mudel.
5. Klõpsake valikut Hinnamudeli kriteeriumid.
6. Klõpsake Uus.
7. Tippige väljale Nimi tekst „Kliendigrupp 10”.
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]