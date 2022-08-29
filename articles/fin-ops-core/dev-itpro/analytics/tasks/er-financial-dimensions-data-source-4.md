---
title: Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (4. osa – aruande käivitamine)
description: See artikkel kirjeldab, kuidas konfigureerida elektroonilise aruandluse (ER) mudelit, et kasutada finantsdimensioone ER-aruannete andmeallikana. (4. osa)
author: kfend
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERSolutionTable, SysQueryForm
ms.openlocfilehash: d0fca8b1a6139b71782af05531d9494c968ef9f5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290750"
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
