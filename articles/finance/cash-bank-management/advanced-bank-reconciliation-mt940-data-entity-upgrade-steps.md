---
title: Täpsem panga vastavusseviimise MT940 import – liitandmeüksuse täiendamise etapid
description: Järjekorranumber tuleb lisada pangaväljavõtte impordiüksusele, et toetada MT940 vormingut.
author: panolte
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d6534cc0835eabe91ab485e1d71412885d12123f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827430"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>Täpsem panga vastavusseviimise MT940 import – liitandmeüksuse täiendamise etapid

[!include [banner](../includes/banner.md)]

Järjekorranumber tuleb lisada pangaväljavõtte impordiüksusele, et toetada MT940 vormingut. 

Kasutage järgmiseid etappe, et lisada pangaväljavõtte impordiüksus MT940 vormingu toetamiseks.

1.  Kompileerige ja sünkroonige järgmine:
    -   Liitüksus\\BankStatementImportEntity
    -   Üksus\\BankStatementBalanceEntity
    -   Üksus\\BankStatementDocumentEntity
    -   Üksus\\BankStatementEntity
    -   Üksus\\BankStatementLineEntity
    -   Tabelid\\BankStatementStaging

2.  Andmehaldus\\andmeprojektid.
    1.  MT940 importimisprojekti(de) laadimine
        1.  Muutke XSLT-d.
            -   Klõpsake suvandit **Kuva kaart**.
            -   Klõpsake pangaväljavõtte dokumendi valikut **Kuva kaart**.
            -   Klõpsake valikut **Teisendused**
            -   Kustutage fail BankReconiliation-to-Composite.xslt.
            -   Lisage faili BankReconiliation-to-Composite.xsl uus versioon.

        2.  Avage valik **Seerianumber** paigutuses **Lähteandmed**.
            1.  Lähteandmete vorming = XML-Element.
            2.  Üksuse nimetus = Pangaväljavõtted.
            3.  Andmefaili üleslaadimise = uus faili SampleBankCompositeEntity.xml versioon.
            4.  Klõpsake valikut **Jah**, et olemasolev fail üle kirjutada.
            5.  Klõpsake valikut **Jah**, et luua uus vastendus.
            6.  Kontrollige, kas **Seerianumber** on vastendatud.
                -   Klõpsake väljavõtte üksust **Kuva kaart**.
                -   Kontrollige, kas **SequenceNumber** on vastendatud valikult Allikas valikule Ajastamine.

3.  Importige uus väljavõte.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]