---
title: Uue laopaigutuse loomine
description: Selles protseduuris näitlikustatakse, kuidas seadistada lao asukohtade teavet.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26314f9015feded41f105814b85069fff0c62964
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "360528"
---
# <a name="create-a-new-warehouse-layout"></a>Uue laopaigutuse loomine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles protseduuris näitlikustatakse, kuidas seadistada lao asukohtade teavet. See rakendub ainult ladudele, mis on loodud, kasutades üldist ladustamist moodulis Varude haldus, mitte nendele ladudele, mis on loodud moodulis Laohaldus. Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.


## <a name="set-the-default-location-capacity"></a>Määrake asukoha vaikemahutavus
1. Avage Varude haldus > Seadistus > Varude ja lao halduse parameetrid.
2. Klõpsake vahekaarti Asukohad.
3. Sisestage arv väljale Standardlaius.
4. Sisestage arv väljale Standardmaht.
5. Sisestage arv väljale Standardkõrgus.
6. Klõpsake nuppu Salvesta.
7. Sulgege leht.

## <a name="define-the-location-name-format"></a>Asukoha nime vormingu määratlemine
1. Avage Varude haldus > Seadistus > Laovarude jaotamine > Laod.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Ladu.
4. Sisestage väärtus väljale Nimi.
5. Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.
6. Otsige loendist ja valige soovitud kirje.
7. Lülitage ümber jaotis Asukoha nimed.
    * Selle jaotise suvandites saate määratleda asukohanimede vaikevormingu. Selles näites on kasutatud riiulirea, sektsiooni ja riiuli numbrit.  
8. Seadistage suvand Kaasa riiulirida väärtusele Jah.
9. Seadistage suvand Kaasa sektsioon väärtusele Jah. 
10. Sisestage sektsiooni jaoks väärtus väljale Vorming.
    * Näide: ‑##  
11. Seadistage suvand Kaasa riiul väärtusele Jah.
12. Sisestage riiuli jaoks väärtus väljale Vorming.
    * Näide: ‑##  

## <a name="define-warehouse-locations"></a>Lao asukohtade määratlemine
1. Klõpsake toimingupaanil valikut Ladu.
2. Klõpsake Asukohaviisardit.
3. Klõpsake käsku Edasi.
4. Tühistage suvand Lähetusalad
5. Tühistage suvand Hulgiasukohad
6. Klõpsake käsku Edasi.
7. Klõpsake käsku Edasi.
8. Klõpsake käsku Edasi.
9. Klõpsake käsku Edasi.
10. Klõpsake käsku Edasi.
11. Klõpsake käsku Edasi.
12. Klõpsake käsku Edasi.
    * Pange tähele, et sellel lehel kuvatavad füüsilised dimensioonid on need, mille te selle protseduuri alguses seadistasite.  
13. Klõpsake käsku Edasi.
14. Klõpsake Lõpeta.
15. Sulgege leht.
16. Värskendage lehte.

