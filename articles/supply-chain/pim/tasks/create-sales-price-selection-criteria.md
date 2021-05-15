---
title: Müügihinna valikukriteeriumide loomine
description: See protseduur näitab, kuidas luua atribuudipõhistele hinnamudelitele müügihinna valikukriteeriumi.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69d22c3321beaa2667ee20bff00acd746714b993
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920527"
---
# <a name="create-sales-price-selection-criteria"></a>Müügihinna valikukriteeriumide loomine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas luua atribuudipõhistele hinnamudelitele müügihinna valikukriteeriumi. See protseduur nõuab, et saadaval oleks vähemalt üks müügihinna mudel. Selles näites kasutatakse hinnamudelina demoettevõtte USMF müügihinnamudelit Kõlarilahendus. Tavaliselt kasutab seda protseduuri tootejuht.

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Lisage olemasolevale müügihinna mudelile uus kriteerium

1. Avage **Tooteteabe haldus \> Tooted \> Tootekonfiguratsiooni mudelid**.
1. Valige loendist tootemudeli Kõlarilahenduse rida, kuid ärge klõpsake valimiseks mudeli nime linki.
1. Valige toiminguplaanil **Mudel**.
1. Valige suvand **Hinnamudeli kriteeriumid**.
1. Valige suvand **Uus**.
1. Tippige väljale **Nimi** tekst „Kliendigrupp 10”.
    * Hinnamudeli kriteeriumi nime abil saab tuvastada aluseks olevad valikukriteeriumid.  
1. Valige või sisestage väljal **Hinnamudel** väärtus.
1. Valige väljal **Tellimuse tüüp** suvand *Müügitellimus*.
    * Tellimuse tüüp määrab andmebaasiväljad, mis on valikupäringu puhul saadaval.  
1. Sisestage kuupäev väljale **Kehtiv alates**.
1. Sisestage kuupäev väljale **Loe aegunuks**.
1. Valige käsk **Salvesta**.

## <a name="create-the-query-for-the-selection-criteria"></a>Valikukriteeriumile päringu loomine

1. Valige suvand **Redigeeri**.
2. Valige väljal **Tabel** suvand *Kliendid*.
3. Valige väljal **Väli** suvand *Kliendigrupp*.
    * Selles näites kasutame valikukriteeriumide puhul konkreetset kliendigruppi.  
4. Valige väljal **Kriteeriumid** *Kliendigrupp 10*.
5. Valige nupp **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]