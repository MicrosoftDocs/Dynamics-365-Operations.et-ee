--- 
title: "ISO20022 kreeditiülekande konfiguratsiooni importimine"
description: "See protseduur näitab, kuidas importida hankija makse elektroonilise aruandluse konfiguratsiooni."
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 71c0175178203006e297466c4a37cd3e6319b6ea
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="import-iso20022-credit-transfer-configuration"></a>ISO20022 kreeditiülekande konfiguratsiooni importimine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas importida hankija makse elektroonilise aruandluse konfiguratsiooni. Näitena on kasutatud Saksamaa ISO 20022 kreeditülekande vormingut. Seda protseduuri saab kasutada teiste saadaolevate elektroonilise aruandluse vormingute puhul. 

See ülesanne loodi, kasutades demoettevõtte DEMF andmeid, kuid võite kasutada selle ülesande täitmiseks mis tahes demoettevõtet.

See on esimene viiest ülesandest, mis illustreerivad koos hankija makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone. See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.

1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
2. Valige saadaolevate konfiguratsiooni pakkujate loendist Microsoft.
3. Klõpsake valikut Määra aktiivseks.
4. Klõpsake valikut Hoidlad.
5. Klõpsake valikut Ava.
6. Klõpsake suvandit Näita filtreid.
7. Rakendage järgmised filtrid: sisestage filtri väärtus „ISO20022 kreeditülekanne (DE)” väljale „Konfiguratsiooni nimi”, kasutades filtri tehtemärki „algab üksusega”
    * Teine võimalus on otsida konfiguratsioon loendist üles, valida see ja teisaldada see siis importimisülesandesse.  
8. Klõpsake Import.
    * Kui nupp Impordi pole saadaval, tähendab see, et see konfiguratsioon on juba imporditud.  
9. Klõpsake nuppu Jah.


