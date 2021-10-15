---
title: Müügihinna valikukriteeriumide loomine
description: See protseduur näitab, kuidas luua atribuudipõhistele hinnamudelitele müügihinna valikukriteeriumi.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed7083f289948033782f74dd9ed1b3c2d2a73aea
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568443"
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