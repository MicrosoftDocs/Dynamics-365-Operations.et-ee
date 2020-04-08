---
title: Elektrooniline aruandlus. Horisontaalselt laiendatavate vahemike kasutamine veergude dünaamiliseks lisamiseks Exceli aruannetes (2. osa – vormingu käivitamine)
description: Järgmistes etappides selgitatakse, kuidas kasutaja, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll, saab konfigureerida elektroonilise aruandluse vormingut, et luua aruandeid OPENXML-i töölehtede (Exceli) failidena, milles saab luua dünaamiliselt vajalikke veerge horisontaalselt laiendatavate vahemikena.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 66c2a97a068ed83f93699f14e827bdc2fb580d93
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141829"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a>Elektrooniline aruandlus. Horisontaalselt laiendatavate vahemike kasutamine veergude dünaamiliseks lisamiseks Exceli aruannetes (2. osa – vormingu käivitamine)

[!include [banner](../../includes/banner.md)]

Järgmistes etappides selgitatakse, kuidas kasutaja, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll, saab konfigureerida elektroonilise aruandluse vormingut, et luua aruandeid OPENXML-i töölehtede (Exceli) failidena, milles saab luua dünaamiliselt vajalikke veerge horisontaalselt laiendatavate vahemikena. Neid toiminguid saab teha DEMF ettevõttes.

Nende etappide lõpule viimiseks peate esmalt viima lõpule etapid protseduuris „Elektrooniline aruandlus Horisontaalselt laiendatavate vahemike kasutamine veergude dünaamiliseks lisamiseks Exceli aruannetes (1. osa: vormingu koostamine)”.

See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.


## <a name="find-created-format"></a>Loodud vormingu otsimine
1. Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.
2. Laiendage puul jaotist Finantsdimensioonide näidismudel.
3. Valige puult Finantsdimensioonide näidismudel \ Näidisaruanne horisontaalselt laiendatavate vahemikega.

## <a name="execute-format-to-create-excel-output"></a>Käivitage vorming Exceli väljundi loomiseks.
1. Klõpsake nuppu Käivita.
2. Tippige väljale Dimensiooni nimi väärtus BusinessUnit;CostCenter;Department.
    * Valige või sisestage väärtus väljal Dimensiooni nimi.  Kõigi praeguse ettevõtte dimensioonide valimiseks sisestage järgmine: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
3. Jaotise kaasamiseks laiendage kirjeid.
4. Klõpsake käsku Filtreeri.
5. Valige tabeli Pearaamatu tööleht rida ja väli Töölehe partiinumber.
6. Tippige väljale Kriteeriumid väärtus 00057..00058.
    * 00057..00058  
7. Klõpsake nuppu OK.
8. Klõpsake nuppu OK.
    * Vaadake loodud väljundit. Pange tähele, et äsja loodud Exceli fail sisaldab sama veergude arvu, mis finantsdimensioonide jaoks valiti. Aruande päis nendes veergudes tähistab finantsdimensioonide nimesid. Kannete read nendes veergudes tähistavad finantsdimensioone. Käivitage see aruanne ja valige teistsugused dimensioonid nägemiseks, et aruanne ei sõltu valitud dimensioonide arvust ega selle eksemplari jaoks konfigureeritud dimensioonide arvust.  

