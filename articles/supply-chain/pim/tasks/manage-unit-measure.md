--- 
title: "Mõõtühiku haldamine"
description: "See protseduur näitab, kuidas määratleda mõõtühikut, pakkuda üksuse ja selle kirjelduse ümberarvestusi ja määratleda seotud üksuste teisendusreegleid."
author: sorenva
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: de5baa1e5c30ee998d113f7366c445a65723dfdc
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="manage-unit-of-measure"></a>Mõõtühiku haldamine

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas määratleda mõõtühikut, pakkuda üksuse ja selle kirjelduse ümberarvestusi ja määratleda seotud üksuste teisendusreegleid. Saate selle protseduuriga tutvuda demoandmeid või omaenda andmeid kasutades.

1. Avage Väljastatud toote haldus.
2. Klõpsake suvandit Ühikud.

## <a name="create-a-unit-of-measure"></a>Mõõtühiku loomine
1. Klõpsake valikut Uus.
2. Sisestage väärtus väljale Ühik.
    * Sisestage mõõtühikule viitamisel kasutatav ID või sümbol.  
3. Sisestage väljale Kirjeldus soovitud väärtus.
    * Sisestage mõõtühikule süsteemikeeles kirjeldav nimi.  
4. Valige suvand väljalt Ühiku klass.
    * Ühiku klass määratleb, millisesse loogilisse grupeerimisse, nagu ala, mass või kogus, mõõtühik kuulub.  
5. Sisestage number väljale Kümnendarvuline täpsus.
    * Määrake komakohtade arv, milleni teisendatud mõõtühik tuleb ümardada, kui arvutamine on mõõtühiku puhul lõpule viidud.  
6. Klõpsake nuppu Salvesta.

## <a name="define-unit-translations"></a>Ühiku teisenduste määratlemine
1. Klõpsake suvandit Ühiku tekstid.
2. Klõpsake valikut Uus.
    * Kasutage ühiku teksti mõõtühikut esindava ID või sümboli ümberarvestuse loomiseks kliendi- või hankijapõhises keeles välisdokumentidel kasutamiseks.  
3. Sisestage väärtus väljale Keel või valige see.
4. Sisestage väärtus väljale Tekst.
5. Klõpsake nuppu Salvesta.
6. Sulgege leht.
7. Klõpsake suvandit Ümberarvestatud ühiku kirjeldused.
8. Klõpsake valikut Uus.
    * Määratlege mõõtühiku keelepõhised kirjeldused.  
9. Sisestage väärtus väljale Keel või valige see.
10. Sisestage väljale Kirjeldus soovitud väärtus.
11. Klõpsake nuppu Salvesta.
12. Sulgege leht.

## <a name="define-unit-conversion-rules"></a>Ühiku teisendamise reeglite määratlemine
1. Klõpsake suvandit Ühiku teisendused.
    * Määratlege reeglid mõõtühiku teisendamiseks muudesse mõõtühikutesse ja neist valitud ühiku klassis.  
2. Rippdialoogi avamiseks klõpsake valikut Uus.
3. Sisestage number väljale Tegur.
    * Sihtühiku ja lähteühiku vaheline teisendustegur. Näiteks teisendustegur sentimeetrilt meetrile on 100, sest ühes meetris on 100 sentimeetrit.  
4. Sisestage väärtus väljale Sihtühik või valige see.
5. Valige suvand väljalt Ümardamine.
    * Määratlege, kuidas teisendatud väärtust ümardada.  
6. Klõpsake nuppu OK.
7. Sulgege leht.

