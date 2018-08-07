---
title: Tootedimensioonid
description: "On olemas neli tootedimensiooni: värv, konfiguratsioon, suurus ja stiil. Tootedimensioonid saab ühendada dimensioonigruppidesse ja dimensioonigrupid saab määrata tooteetalonidele. Tootevariantide määratlemise määravad tootedimensioonide kombinatsioonid."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 9cb4bded4b8d841c6d164e6b8ded2cb3fb4d0978
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---

# <a name="product-dimensions"></a>Tootedimensioonid

[!include [banner](../includes/banner.md)]

[!include [Retail name](../includes/retail-name.md)]

On olemas neli tootedimensiooni: värv, konfiguratsioon, suurus ja stiil. Tootedimensioonid saab ühendada dimensioonigruppidesse ja dimensioonigrupid saab määrata tooteetalonidele. Tootevariantide määratlemise määravad tootedimensioonide kombinatsioonid.

Tootedimensioonid on tootevarianti identifitseerivad omadused. Tootevariantide määratlemiseks saate kasutada tootedimensioonide kombinatsioone. Tootevariandi loomiseks peate määratlema tooteetaloni jaoks vähemalt ühe tootedimensiooni.
Tootevariandid
----------------

Tootevariante nimetatakse ka kaupadeks. Kaup on materiaalne toode, mis ei ole sama, mis teenus. Samuti on võimalik määratleda tooteetalon, mille tüüp on Teenus. Kasutades tüüpi Teenus, saate määrata teenuseid sisaldavad tootevariandid. Näiteks saate määrata tooteetaloni nõustamistööle ja tootevariandid tööle, mida teevad vanem- ja nooremnõustajad.

## <a name="product-dimensions"></a>Tootedimensioonid
Saadaval on järgmised tootedimensioonid: konfiguratsioon, värv, suurus ja stiil. Tootevariandi saab luua tootedimensiooni väärtuste alusel.

Tootedimensioonide väärtused, nagu suurus, värv ja stiil, saab luua lehtedel **Suurus**, **Värv** ja **Stiil**, millele pääseb järgmistest asukohtadest: **Tooteteabe haldus** &gt; **Seadistus** &gt; **Dimensiooni- ja variandigrupid** &gt; **Suurused/Värvid/Stiilid**. Tootedimensiooni väärtused konfiguratsioonidimensiooni puhul luuakse tavaliselt kas tootekonfiguraatoris või dimensioonipõhises konfiguraatoris. Tootedimensioone saab luua ja hallata ka lehel **Tootedimensioonid**, millele pääseb juurde järgmistest asukohtadest.
-   Klõpsake suvandeid **Tooteteabe haldus** &gt; **Tooted** &gt; **Tooteetalonid**. Klõpsake **toimingupaanil** valikut **Tootedimensioonid**.
-   Klõpsake suvandeid **Tooteteabe haldus** &gt; **Tooted** &gt; **Kõik tooted ja tooteetalonid**. Valige tooteetalon. Klõpsake **toimingupaanil** valikut **Tootedimensioonid**.
-   Klõpsake valikuid **Tooteteabe haldus** &gt; **Väljastatud tooted**. Valige tooteetalon. Klõpsake **toimingupaanil** suvandit **Toode**. Klõpsake grupis **Tooteetalon** suvandit **Tootedimensioonid**.

Kaubale loodavate variantide arv on piiratud võimalike tootedimensiooni kombinatsioonide arvuga.

| **Näpunäide**                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Toote kasutamisel näiteks tellimusereal valige tootedimensioonid selleks, et määrata tootevariant, millega soovite töötada. |

## <a name="example"></a>Näide
Ettevõte müüb teksasid. Kaup „teksad” kasutab dimensioone Värv ja Suurus. Teksasid müüakse kolmes eri värvis ja kuues eri suuruses. Värvid: sinine, must, pruun, suurused: XS, S, M, L, XL, XXL. Kõik suurused ei ole kõigis kolmes värvis saadaval. Kui kõik kombinatsioonid oleksid olemas, oleks teksasid 18 tüüpi. Selles näites on toodetud ainult järgmised üheksa tootevariandi kombinatsiooni.

| Värv | Suurus |
|-------|------|
| Sinine  | XS   |
| Sinine  | L    |
| Sinine  | E    |
| Must | E    |
| Must | L    |
| Must | XL   |
| Pruun | L    |
| Pruun | XL   |
| Pruun | XXL  |






