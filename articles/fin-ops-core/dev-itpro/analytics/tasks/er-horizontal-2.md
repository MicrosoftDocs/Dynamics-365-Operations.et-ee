---
title: Elektrooniline aruandlus. Horisontaalselt laiendatavate vahemike kasutamine veergude dünaamiliseks lisamiseks Exceli aruannetes (2. osa – vormingu käivitamine)
description: Selles teemas kirjeldatakse, kuidas konfigureerida elektroonilise aruandluse (ER) vorming looma aruandeid OPENXML töölehtede (Excel) failidena. (2. osa)
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c13179f424d570b23615fe81ca5ddfb7afed582d
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093472"
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

