---
title: Tootenumbri nomenklatuuri loomine eelmääratletud tootevariantide jaoks
description: Selles teemas selgitatakse, kuidas seadistada tootenumbri nomenklatuuri eelmääratletud tootevariantide jaoks ja kuidas määrata see sobivale tootedimensiooni grupile.
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 073b680c48855b2a8902c19cedfbf98cdbfdf17d
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150043"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Tootenumbri nomenklatuuri loomine eelmääratletud tootevariantide jaoks

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse, kuidas seadistada tootenumbri nomenklatuuri eelmääratletud tootevariantide jaoks ja kuidas määrata see sobivale tootedimensiooni grupile. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. Uus tootenumbri nomenklatuur on määratud tootedimensioonigrupile Värv ja Suurus. Enamasti teeb selle toimingu toote koostaja.


## <a name="create-a-product-number-nomenclature"></a>Tootenumbri nomenklatuuri loomine
1. Valige **Tootevariandi mudeli määratlus**.
2. Valige **Toote nomenklatuur**.
3. Valige suvand **Uus**.
4. Väljale **Nimi** sisestage nomenklatuuri nimi, mis aitab tuvastada sihttoote dimensiooni grupi, näiteks `ColorSize`.
5. Sisestage väärtus väljale **Kirjeldus**.
6. Valige **Lisa**.
7. Valige **Tooteetaloni** number.
8. Valige **Lisa**.
9. Valige **Tekstikonstant**.
10. **Sisestage väärtus väljale Tekst.**
11. Valige **Lisa**.
12. Valige **Värv**.
13. Valige **Lisa**.
14. Valige **Tekstikonstant**.
15. **Sisestage väärtus väljale Tekst.**
16. Valige **Lisa**.
17. Valige **Suurus**.
18. Sulgege leht.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Nomenklatuuri määramine tooteetalonile
1. Valige **Toote dimensiooni grupid**.
2. Valige rühm **SizeCol dimensioon**.
3. Valige suvand **Redigeeri**.
4. Valige väärtus **Jah** väljal **Kasuta nomenklatuuri**.
5. Väljale **Tootevariandi numbri nomenklatuur** sisestage või valige väärtus.
6. Sulgege leht.

