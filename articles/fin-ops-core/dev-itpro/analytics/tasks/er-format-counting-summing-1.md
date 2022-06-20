---
title: Elektrooniline aruandlus. Vormingu konfigureerimine loendamiseks ja liitmiseks (1. osa – vormingu loomine)
description: See artikkel kirjeldab, kuidas konfigureerida elektroonilise aruandluse vormingut nii, et loendamine ja summeerimine põhineb juba loodud tekstiväljundi andmetel. (1. osa)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85a25715018f30d2fd8f1405d50cee0b420c0d34
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902621"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a>Elektrooniline aruandlus. Vormingu konfigureerimine loendamiseks ja liitmiseks (1. osa – vormingu loomine)

[!include [banner](../../includes/banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal. Neid toiminguid saab teha igas ettevõttes.

Etappide lõpuleviimiseks, peate esmalt läbima teemas „Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine” kirjeldatudetapid.

See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Juurdepääsu saamine Microsofti pakutavale konfiguratsioonide loendile
1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
    * Veenduge, et „Litware, Inc.“ pakkuja on saadaval ja märgitud aktiivseks.  
2. Valige ettevõte „Litware, Inc.” pakkuja.
3. Klõpsake valikut Hoidlad.
    * Kui on juba olemas hoidla tüübiga Operatsiooniressursid, siis jätke praeguse alamtoimingu ülejäänud etapid vahele.  
4. Klõpsake valikut Lisa rippdialoogi avamiseks.
5. Sisestage väljale Konfiguratsiooni hoidla tüüp tekst Operatsiooniressursid.
6. Klõpsake käsku Loo hoidla.
7. Klõpsake nuppu OK.

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a>Microsofti pakutavate intrastati konfiguratsioonide saamine
1. Klõpsake valikut Ava.
2. Valige puult Intrastati mudel \ Intrastat (DE).
3. Klõpsake Import.
    * Klõpsake valikut Impordi valitud konfiguratsiooni versioonile 1.1.  
4. Klõpsake nuppu Jah.
5. Sulgege leht.
6. Sulgege leht.
7. Klõpsake valikut Aruandluse konfiguratsioonid.
8. Laiendage puul valikut Intrastati mudel.
9. Valige puult Intrastati mudel \ Intrastat (DE).



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]