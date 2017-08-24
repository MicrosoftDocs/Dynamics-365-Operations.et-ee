--- 
title: "Elektroonilise aruandluse (ER) andmemudeli ettevalmistamine dokumendihalduse failide kasutamiseks vormingu väljundites"
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: cc0909f99be9aad1b6bec22d4ed10381e0484a41
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="prepare-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a>Elektroonilise aruandluse (ER) andmemudeli ettevalmistamine dokumendihalduse failide kasutamiseks vormingu väljundites

[!include[task guide banner](../../includes/task-guide-banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis. Neid toiminguid saab teha igas ettevõttes.

Etappide lõpuleviimiseks, peate esmalt läbima protseduuri Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine etapid.

See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Juurdepääsu saamine Microsofti pakutavale konfiguratsioonide loendile
1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
    * Veenduge, et „Litware, Inc.“ pakkuja on saadaval ja märgitud aktiivseks.  
2. Valige ettevõtte Litware, Inc. pakkuja.
3. Klõpsake valikut Hoidlad.
    * Kui on juba olemas hoidla tüübiga Operatsiooniressursid, siis jätke praeguse alamtoimingu ülejäänud etapid vahele.  
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
    * Valige selle importimiseks mudeli konfiguratsioon Kliendiarve mudel.  
6. Klõpsake Import.
    * Klõpsake valikut Impordi valitud konfiguratsiooni versioonile 1.  
7. Klõpsake nuppu Jah.
8. Sulgege leht.
9. Sulgege leht.
10. Klõpsake valikut Aruandluse konfiguratsioonid.
11. Valige puult Kliendiarve mudel.

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a>Looge tuletatud mudel, et toetada juurdepääsu dokumendihalduse failidele.
    * Loote oma konfiguratsiooni kliendiarve mudelist, tuletades selle Microsofti antud konfiguratsioonist. Kasutate seda konfiguratsiooni juurdepääsu juurutamiseks dokumendihalduse failidele ja nende kättesaadavaks tegemiseks elektroonilistele dokumentidele, mille selle mudeli põhjal loote.  
1. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
2. Sisestage väljale Uus tekst Tuleta väärtusest Nimi: kliendiarve mudel, Microsoft.
3. Tippige väljale Nimi tekst Kliendiarve mudel (kohandatud).
    * Kliendiarve mudel (kohandatud)  
4. Klõpsake Loo konfiguratsioon.


