---
title: Uue laopaigutuse loomine
description: See artikkel kirjeldab, kuidas seadistada teavet asukohtade kohta laos.
author: yufeihuang
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 143648e5317e6dce1b1a76a96d6069abe5d0e351
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859310"
---
# <a name="create-a-new-warehouse-layout"></a>Uue laopaigutuse loomine

[!include [banner](../../includes/banner.md)]

See artikkel kirjeldab, kuidas seadistada teavet asukohtade kohta laos. See rakendub ainult ladudele, mis on loodud, kasutades üldist ladustamist moodulis Varude haldus, mitte nendele ladudele, mis on loodud moodulis Laohaldus. Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.


## <a name="set-the-default-location-capacity"></a>Määrake asukoha vaikemahutavus
1. Navigeerimispaanil avage **Moodulid > Varude haldus > Seadistus > Ladu > Varude ja laohalduse parameetrid**.
2. Valige vahekaart **Asukoht**.
3. Väljale **Standardlaius** sisestage arv.
4. Väljale **Standardmaht** sisestage arv.
5. Väljale **Standardkõrgus** sisestage arv.
6. Valige käsk **Salvesta**.
7. Sulgege leht.

## <a name="define-the-location-name-format"></a>Asukoha nime vormingu määratlemine
1. Navigeerimispaanil avage **Moodulid > Varude haldus > Seadistus > Laovarude jaotamine > Laod**.
2. Valige suvand **Uus**.
3. Sisestage väärtus väljale **Ladu**.
4. Sisestage väärtus väljale **Nimi**.
5. Väljal **Sait** valige otsingust soovitud kirje.
6. Lülituge ümber jaotise **Asukohanimed** laiendusele. Selle jaotise suvandites saate määratleda asukohanimede vaikevormingu. Selles näites on kasutatud riiulirea, sektsiooni ja riiuli numbrit.  
7. Määrake suvandi **Kaasa riiulirida** väärtuseks **Jah**.
8. Määrake suvandi **Kaasa sektsioon** väärtuseks **Jah**. 
9. Sisestage sektsioonile väärtus väljal **Vorming**.
10. Määrake suvandi **Kaasa riiul** väärtuseks **Jah**.
11. Sisestage riiulile väärtus väljal **Vorming**.

## <a name="define-warehouse-locations"></a>Lao asukohtade määratlemine
1. Toimingupaanil valige **Ladu**.
2. Valige **Asukohaviisard**.
3. Valige **Edasi**.
4. Tühistage suvandi **Lähetusalad** valik.
5. Tühistage suvandi **Partii asukohad** valik.
6. Valige **Järgmine** kuni jõuate suvandini **Lõpeta**.
7. Sulgege leht.
8. Värskendage lehte.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]