---
title: Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (4. osa – aruande käivitamine)
description: See artikkel kirjeldab, kuidas konfigureerida elektroonilise aruandluse (ER) mudelit, et kasutada finantsdimensioone ER-aruannete andmeallikana. (4. osa)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ef1944655893f191502b4d1e8e1372f6d2e755f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881126"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a>Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (4. osa – aruande käivitamine)

[!include [banner](../../includes/banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana. Neid toiminguid saab teha DEMF ettevõttes.

Nende etappide lõpule viimiseks peate esmalt viima lõpule etapid protseduuris „Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (3. osa: aruande koostamine)”. Peate konfigureerima ka dokumentide vaiketüübid lehel Elektroonilise aruande parameetrid. Dokumentide vaiketüübid määratakse ka siis, kui mõne elektroonilise aruandluse konfiguratsiooni alla laadite ja impordite. 


## <a name="run-report"></a>Aruande käitamine
1. Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.
2. Laiendage puul jaotist Finantsdimensioonide näidismudel.
3. Valige puult Finantsdimensioonide näidismudel \ Pearaamatu töölehe aruanne.
4. Klõpsake käsku Käita.
![ER-i konfiguratsiooni leht.](../media/er-financial-dimensions-guides-run1.png)
5. Valige või sisestage väärtus väljal Dimensiooni nimi.
    * Kõigi praeguse ettevõtte dimensioonide valimiseks sisestage järgmine teave: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
![Elektroonilise aruande parameetrite välja liikumine, dimensiooni nime rippmenüü.](../media/er-financial-dimensions-guides-run2.png)
6. Jaotise kaasamiseks laiendage kirjeid.
7. Klõpsake käsku Filtreeri.
8. Valige tabeli Pearaamatu tööleht rida ja väli Töölehe partiinumber.
9. Tippige väärtus 00057 väljale Kriteeriumid.
10. Klõpsake nuppu OK.
11. Klõpsake nuppu OK.
![Elektroonilise aruande parameetrite liikumine välja, jaotis Aruanded kaasamiseks.](../media/er-financial-dimensions-guides-run3.png)
    * Vaadake loodud väljundit. Iga valitud partii kande puhul esitatakse asjakohase finantsdimensioonikogumi finantsdimensioonid. Käivitage see aruanne ja valige teistsugused dimensioonid nägemiseks, et aruanne ei sõltu valitud dimensioonide arvust ega selle eksemplari jaoks konfigureeritud dimensioonide arvust.  
![ER-i konfiguratsioonide loodud väljund.](../media/er-financial-dimensions-guides-run4.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
