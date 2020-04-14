---
title: Mõõtühiku haldamine
description: See protseduur näitab, kuidas määratleda mõõtühikut, pakkuda üksuse ja selle kirjelduse ümberarvestusi ja määratleda seotud üksuste teisendusreegleid.
author: sorenva
manager: AnnBe
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f26b55f6e79200ac273fbb642c49998d8cd7e388
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147614"
---
# <a name="manage-unit-of-measure"></a>Mõõtühiku haldamine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas määratleda mõõtühikut, pakkuda üksuse ja selle kirjelduse ümberarvestusi ja määratleda seotud üksuste teisendusreegleid. Saate selle protseduuriga tutvuda demoandmeid või omaenda andmeid kasutades.

1. Avage **Navigeerimispaan > Moodulid > Tooteteabe haldus > Tooted > Väljastatud tooted**.
2. Klõpsake suvandit **Ühikud**.

## <a name="create-a-unit-of-measure"></a>Mõõtühiku loomine
1. Klõpsake valikut **Uus**.
2. Sisestage väärtus väljale **Ühik**. Sisestage mõõtühikule viitamisel kasutatav ID või sümbol.  
3. Sisestage väärtus väljale **Kirjeldus**. Sisestage mõõtühikule süsteemikeeles kirjeldav nimi.  
4. Valige suvand väljalt **Ühiku klass**. Ühiku klass määratleb, millisesse loogilisse grupeerimisse, nagu ala, mass või kogus, mõõtühik kuulub.  
5. Sisestage number väljale **Kümnendarvuline täpsus**. Määrake komakohtade arv, milleni teisendatud mõõtühik tuleb ümardada, kui arvutamine on mõõtühiku puhul lõpule viidud.  
6. Klõpsake valikut **Salvesta**.

## <a name="define-unit-translations"></a>Ühiku teisenduste määratlemine
1. **Toimingupaanil** klõpsake **Üksuse tekstid**.
2. Klõpsake valikut **Uus**. Kasutage ühiku teksti mõõtühikut esindava ID või sümboli ümberarvestuse loomiseks kliendi- või hankijapõhises keeles välisdokumentidel kasutamiseks.  
3. Sisestage väärtus väljale **Keel** või valige see.
4. **Sisestage väärtus väljale Tekst.**
5. Klõpsake valikut **Salvesta**.
6. Sulgege leht.
7. Klõpsake **tegevuspaanil** **Tõlgitud üksuste kirjeldused**.
8. Klõpsake valikut **Uus**. Määratlege mõõtühiku keelepõhised kirjeldused.  
9. Sisestage väärtus väljale **Keel** või valige see.
10. Sisestage väärtus väljale **Kirjeldus**.
11. Klõpsake valikut **Salvesta**.
12. Sulgege leht.

## <a name="define-unit-conversion-rules"></a>Ühiku teisendamise reeglite määratlemine
1. Klõpsake **tegevuspaanil** **üksuse ühikute teisendamine**. Määratlege reeglid mõõtühiku teisendamiseks muudesse mõõtühikutesse ja neist valitud ühiku klassis.  
2. Rippdialoogi avamiseks klõpsake valikut **Uus**.
3. Sisestage number väljale **Tegur**. Sihtühiku ja lähteühiku vaheline teisendustegur. Näiteks teisendustegur sentimeetrilt meetrile on 100, sest ühes meetris on 100 sentimeetrit.  
4. Sisestage või valige väärtus väljale **Kuni ühikuni**.
5. Valige suvand väljal **Ümardamine**. Määratlege, kuidas teisendatud väärtust ümardada.  
6. Klõpsake valikut **OK**.
7. Sulgege leht.

