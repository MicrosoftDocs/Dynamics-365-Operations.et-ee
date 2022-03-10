---
title: Tootenumbri nomenklatuuri loomine eelmääratletud tootevariantide jaoks
description: Selles teemas selgitatakse, kuidas seadistada tootenumbri nomenklatuuri eelmääratletud tootevariantide jaoks ja kuidas määrata see sobivale tootedimensiooni grupile.
author: t-benebo
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5179dd54f22de11dc4c0f54113376f13b2f59c48
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569573"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Tootenumbri nomenklatuuri loomine eelmääratletud tootevariantide jaoks

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse, kuidas seadistada tootenumbri nomenklatuuri eelmääratletud tootevariantide jaoks ja kuidas määrata see sobivale tootedimensiooni grupile. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. Uus tootenumbri nomenklatuur on määratud tootedimensioonigrupile Värv ja Suurus. Enamasti teeb selle toimingu toote koostaja.


## <a name="create-a-product-number-nomenclature"></a>Tootenumbri nomenklatuuri loomine

1. Avage **Tooteteabe haldus \> Seadistamine \> Tootenomenklatuurid**.
1. Valige suvand **Uus**.
1. Väljale **Nimi** sisestage nomenklatuuri nimi, mis aitab tuvastada sihttoote dimensiooni grupi, näiteks `ColorSize`.
1. Sisestage väärtus väljale **Kirjeldus**.
1. Valige **Lisa**.
1. Valige **Tooteetaloni** number.
1. Valige **Lisa**.
1. Valige **Tekstikonstant**.
1. **Sisestage väärtus väljale Tekst.**
1. Valige **Lisa**.
1. Valige **Värv**.
1. Valige **Lisa**.
1. Valige **Tekstikonstant**.
1. **Sisestage väärtus väljale Tekst.**
1. Valige **Lisa**.
1. Valige **Suurus**.
1. Sulgege leht.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Nomenklatuuri määramine tooteetalonile

1. Valige **Toote dimensiooni grupid**.
2. Valige rühm **SizeCol dimensioon**.
3. Valige suvand **Redigeeri**.
4. Valige väärtus **Jah** väljal **Kasuta nomenklatuuri**.
5. Väljale **Tootevariandi numbri nomenklatuur** sisestage või valige väärtus.
6. Sulgege leht.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]