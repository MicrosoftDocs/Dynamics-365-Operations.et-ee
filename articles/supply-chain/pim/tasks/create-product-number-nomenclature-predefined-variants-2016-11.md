---
title: Tootenumbri nomenklatuuri loomine eelmääratletud tootevariantide jaoks
description: Selles teemas selgitatakse, kuidas seadistada tootenumbri nomenklatuuri eelmääratletud tootevariantide jaoks ja kuidas määrata see sobivale tootedimensiooni grupile.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a15d1f4ecbf85e22bfadc1dd680d24bc56d807f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007537"
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

