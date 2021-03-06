---
title: Uue laopaigutuse loomine
description: Selles teemas kirjeldatakse, kuidas seadistada lao asukohtade teavet.
author: perlynne
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a329df85c339c90e4bdc620c8a63837ebc19a7c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833973"
---
# <a name="create-a-new-warehouse-layout"></a>Uue laopaigutuse loomine

[!include [banner](../../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas seadistada lao asukohtade teavet. See rakendub ainult ladudele, mis on loodud, kasutades üldist ladustamist moodulis Varude haldus, mitte nendele ladudele, mis on loodud moodulis Laohaldus. Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.


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