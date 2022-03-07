---
title: Tootenumbri nomenklatuuri loomine konfigureeritud tootevariantide jaoks
description: See protseduur näitab, kuidas seadistada konfigureeritud tootevariantidele tootenumbri nomenklatuuri ja kuidas selle saab konfigureeritavale tooteetalonile manustada.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7711d9832288327e700acd47fb30cce0c76e5e9a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568395"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a>Tootenumbri nomenklatuuri loomine konfigureeritud tootevariantide jaoks

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas seadistada konfigureeritud tootevariantidele tootenumbri nomenklatuuri ja kuidas selle saab konfigureeritavale tooteetalonile manustada. See protseduur näitab ka, kuidas toote konfiguratsioonimudeli komponendile konfiguratsiooni nomenklatuuri koostada. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. Uus tootenumbri nomenklatuur määratakse D0004 tooteetalonile. Enamasti teeb selle toimingu toote koostaja.

## <a name="create-a-product-number-nomenclature"></a>Tootenumbri nomenklatuuri loomine

1. Avage **Tooteteabe haldus \> Seadistamine \> Tootenomenklatuurid**.
1. Valige suvand **Uus**.
1. Sisestage väärtus väljale **Nimi**.
1. Sisestage väärtus väljale **Kirjeldus**.
1. Valige **Lisa**.
1. Valige **Tooteetaloni koondnumber**.
1. Valige **Lisa**.
1. Valige **Tekstikonstant**.
1. Märkige loendis valitud rida.
1. **Sisestage väärtus väljale Tekst.**
1. Valige **Lisa**.
1. Valige **Konfiguratsioon**.
1. Sulgege leht.

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a>Tootenumbri nomenklatuuri määramine tooteetalonile

1. Avage **Tooteteabe haldus \> Tooted \> Tooteetalonid**.
1. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks saate filtreerida välja **Tootenumber** väärtuse D järgi.
1. Valige loendis link valitud reas.
1. Valige suvand **Redigeeri**.
1. Valige väärtus *Jah* väljal **Kasuta nomenklatuuri**.
1. Väljale **Tootevariandi numbri nomenklatuur** sisestage või valige väärtus.
1. Sulgege leht.
1. Sulgege leht.

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a>Nomenklatuuri loomine toote konfiguratsioonimudeli komponendile

1. Avage **Tooteteabe haldus \> Tooted \> Tootekonfiguratsiooni mudelid**.
1. Otsige loendist ja valige soovitud kirje.
1. Valige loendis link valitud reas.
1. Valige suvand **Redigeeri**.
1. Tehke väljal *Kasuta konfiguratsiooni nomenklatuur* valik **Jah**.
1. Valige **Lisa**.
1. Valige **Atribuudi väärtus**.
1. Märkige loendis valitud rida.
1. Valige või sisestage väärtus väljal **Atribuut**.
1. Valige **Lisa**.
1. Valige **Tekstikonstant**.
1. Märkige loendis valitud rida.
1. **Sisestage väärtus väljale Tekst.**
1. Valige **Lisa**.
1. Valige **Atribuudi väärtus**.
1. Märkige loendis valitud rida.
1. Valige või sisestage väärtus väljal **Atribuut**.
1. Valige **Lisa**.
1. Valige **Tekstikonstant**.
1. Märkige loendis valitud rida.
1. **Sisestage väärtus väljale Tekst.**
1. Valige **Lisa**.
1. Valige **Atribuudi väärtus**.
1. Märkige loendis valitud rida.
1. Valige või sisestage väärtus väljal **Atribuut**.
1. Valige **Lisa**.
1. Valige **Tekstikonstant**.
1. Märkige loendis valitud rida.
1. **Sisestage väärtus väljale Tekst.**
1. Valige **Lisa**.
1. Valige **Atribuudi väärtus**.
1. Märkige loendis valitud rida.
1. Valige või sisestage väärtus väljal **Atribuut**.
1. Valige **Lisa**.
1. Valige **Tekstikonstant**.
1. Märkige loendis valitud rida.
1. **Sisestage väärtus väljale Tekst.**
1. Valige **Lisa**.
1. Valige **Numbriseeria väärtus**.
1. Märkige loendis valitud rida.
1. Sisestage või valige väärtus väljal **Numbriseeria**.
1. Sulgege leht.
1. Sulgege leht.
1. Sulgege leht.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]