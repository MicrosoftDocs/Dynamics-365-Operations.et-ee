---
title: Elektrooniline aruandlus. Dokumendihalduse failide kasutamine vormingu väljundites (5. osa – vormingu muutmine ja käivitamine)
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b949c2629df0e9db8c11322c9d0d090b200edc2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681753"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a>Elektrooniline aruandlus. Dokumendihalduse failide kasutamine vormingu väljundites (5. osa – vormingu muutmine ja käivitamine)

[!include [banner](../../includes/banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis. Neid toiminguid saab teha DEMF ettevõttes.

Nende etappide lõpule viimiseks peate esmalt viima lõpule etapid protseduuris „Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (4. osa: vormingu käivitamine)”.

See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a>Muutke vormingut manuste lisamiseks, tekitades binaarvormingus sõnumid
1. Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.
2. Laiendage puul valikut Kliendiarve mudel.
3. Laiendage puul valikut Kliendiarve mudel \ Kliendiarve mudel (kohandatud).
4. Valige puult Kliendiarve mudel \ Kliendiarve mudel (kohandatud) \ Elektroonilise arve näidissõnum.
5. Klõpsake valikut Kujundaja.
    * Arve sõnum lisatakse tekitatavasse väljundisse XML-failina, kasutades kodeeringut UNICODE.  
6. Klõpsake suvandit Lisa juur rippdialoogi avamiseks.
7. Valige puul suvand Common\File.
8. Tippige väljale Nimi valik XML-sõnum.
    * XML-sõnum  
9. Sisestage väljale Kodeerimine suvand UTF-8.
    * UTF-8  
10. Klõpsake nuppu OK.
    * Konfigureerige loodav väljund zip-failina.  
11. Klõpsake suvandit Lisa juur rippdialoogi avamiseks.
12. Tehke puul valik Üldine \ Kaust.
13. Tippige väljale Nimi valik Zip-väljund.
    * Zip-väljund  
14. Klõpsake nuppu OK.
15. Valige puult Zip-väljund.
    * Lisage manused loodavale zip-failile algsete nimede ja laienditega failidena.  
16. Klõpsake valikut Lisa rippdialoogi avamiseks.
17. Valige puul suvand Common\File.
18. Tippige Manustatud fail väljale Nimi.
    * Manustatud fail  
19. Klõpsake nuppu OK.
20. Valige puult Zip-väljund \ Manustatud fail.
21. Klõpsake valikut Lisa rippdialoogi avamiseks.
22. Valige puul väärtus Tekst \ Base64.
23. Klõpsake nuppu OK.

## <a name="map-new-format-elements-to-data-model"></a>Uute vorminguelementide vastendamine andmemudeliga
1. Klõpsake vahekaarti Vastendus.
2. Laiendage puus sõlme „model”.
3. Laiendage puul valikut mudel \ Arve manused.
4. Valige puult Zip-väljund \ Manustatud fail \ Base64.
5. Valige puult mudel \ Arve manused \ Faili sisu.
6. Klõpsake valikut Seo.
7. Valige puult Zip-väljund \ Manustatud fail.
8. Klõpsake valikut Failinime redigeerimine.
9. Laiendage puus sõlme „model”.
10. Laiendage puul valikut mudel \ Arve manused.
11. Valige puult mudel \ Arve manused \ Faili nimi.
12. Klõpsake suvandit Andmeallika lisamine.
13. Klõpsake nuppu Salvesta.
14. Sulgege leht.
15. Valige puult mudel \ Arve manused.
16. Klõpsake valikut Seo.
17. Klõpsake nuppu Salvesta.
18. Sulgege leht.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Käivitage valitud arvele koostatud aruanne
1. Klõpsake nuppu Käivita.
2. Jaotise () kaasamiseks laiendage kirjeid.
3. Klõpsake käsku Filtreeri.
4. Valige töölehe Kliendiarve ja välja Müügitellimus rida.
5. Tippige väljal Kriteerium väljale „Müügitellimus” tellimuse number 000148.
    * 000148  
6. Klõpsake nuppu OK.
7. Klõpsake nuppu OK.
    * Vaadake loodud väljundit. Pange tähele, et lisaks XML-vormingus arve sõnumile on igale manusele loodud üks fail. Manuse failidele lisatakse zip-väljund binaarvormingus.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]