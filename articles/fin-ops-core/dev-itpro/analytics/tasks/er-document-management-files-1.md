---
title: Elektrooniline aruandlus. Dokumendihalduse failide kasutamine vormingu väljundites (1. osa – andmemudeli ettevalmistamine)
description: See artikkel kirjeldab, kuidas konfigureerida elektroonilise aruandluse (ER) vormingut dokumendihalduse failide (manuste) kasutamiseks ER-väljundis. (1. osa)
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form:
- ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
- ERSolutionTable, ERSolutionCreateDropDialog
ms.openlocfilehash: f407555eca4c4bd08d09047e9d8f8512cb99d254
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291020"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a>Elektrooniline aruandlus. Dokumendihalduse failide kasutamine vormingu väljundites (1. osa – andmemudeli ettevalmistamine)

[!include [banner](../../includes/banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis. Neid toiminguid saab teha igas ettevõttes.

Etappide lõpuleviimiseks, peate esmalt läbima teemas „Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine” kirjeldatudetapid.

See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Juurdepääsu saamine Microsofti pakutavale konfiguratsioonide loendile
1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.

    Veenduge, et „Litware, Inc.“ pakkuja on saadaval ja märgitud aktiivseks.  

2. Valige ettevõtte Litware, Inc. pakkuja.
3. Klõpsake valikut Hoidlad.

    Kui on juba olemas hoidla tüübiga Operatsiooniressursid, siis jätke praeguse alamtoimingu ülejäänud etapid vahele.  

4. Klõpsake valikut Lisa rippdialoogi avamiseks.
5. Sisestage väljale Konfiguratsiooni hoidla tüüp tekst Operatsiooniressursid.
6. Klõpsake käsku Loo hoidla.
7. Klõpsake nuppu OK.

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a>Microsofti antud kliendiarve mudeli konfiguratsioonide hankimine
1. Klõpsake suvandit Näita filtreid.
2. Rakendage järgmised filtrid: sisestage väljale Nimi filtriväärtus Operatsiooniressursid, kasutades filtri tehtemärki „algab järgmisega”; sisestage väljale Kirjeldus filtriväärtus "", kasutades filtri tehtemärki „algab järgmisega”
3. Klõpsake suvandit Näita filtreid.
4. Klõpsake valikut Ava.
5. Valige puult Kliendiarve mudel.

    Valige selle importimiseks mudeli konfiguratsioon Kliendiarve mudel.  

6. Klõpsake Import.

    Klõpsake valikut Impordi valitud konfiguratsiooni versioonile 1.  

7. Klõpsake nuppu Jah.
8. Sulgege leht.
9. Sulgege leht.
10. Klõpsake valikut Aruandluse konfiguratsioonid.
11. Valige puult Kliendiarve mudel.

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a>Looge tuletatud mudel, et toetada juurdepääsu dokumendihalduse failidele.
Loote oma konfiguratsiooni kliendiarve mudelist, tuletades selle Microsofti antud konfiguratsioonist. Kasutate seda konfiguratsiooni juurdepääsu juurutamiseks dokumendihalduse failidele ja nende kättesaadavaks tegemiseks elektroonilistele dokumentidele, mille selle mudeli põhjal loote.  
1. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
2. Sisestage väljale Uus tekst Tuleta väärtusest Nimi: kliendiarve mudel, Microsoft.
3. Tippige väljale Nimi tekst Kliendiarve mudel (kohandatud).
4. Klõpsake Loo konfiguratsioon.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
