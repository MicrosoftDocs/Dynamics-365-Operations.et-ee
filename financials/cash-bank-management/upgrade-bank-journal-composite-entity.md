---
title: "Pangatöölehe liitüksuse värskendamine"
description: "Järgmised etapid on vajalikud, et lisada täiendav väli BankTransactionType liitüksusele BankJournalEntity."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 364bdff8f8d825cc50760631bb533b531f8b2121
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="update-the-bank-journal-composite-entity"></a>Pangatöölehe liitüksuse värskendamine

[!include[banner](../includes/banner.md)]


Järgmised etapid on vajalikud, et lisada täiendav väli BankTransactionType liitüksusele BankJournalEntity.

Kasutage järgmisi etappe, et lisada täiendav väli BankTransactionType liitüksusele BankJournalEntity.

1.  Kompileerige ja sünkroonige järgmised panga töölehe liitüksused, üksused ja vahetabelid.
    -   Liitüksus\\BankJournalEntity
    -   Üksus\\BankJournalHeaderEntity
    -   Üksus\\BankJournalLineEntity
    -   Tabel\\BankJournalHeaderStaging
    -   Tabel\\BankJournalLineStaging

2.  Andmehaldus\\andmeprojektid
    -   Avage tüüp **Pangakanne**paigutuses **Lähteandmed**.
        -   Lähteandmete vorming = XML-element
        -   Üksuse nimi = Panga tööleht
        -   Andmefaili üleslaadimise = uus faili SampleBankJournalCompositeEntity.xml versioon.
        -   Klõpsake valikut **Jah**, et olemasolev fail üle kirjutada.
        -   Klõpsake valikut **Jah**, et luua vastendus nullist.
        -   Kontrollige, kas pangakande tüüp on vastendatud.
            -   Klõpsake rea üksust **Kuva kaart**.
            -   Kontrollige, kas pangekande tüüp on vastendatud valikult Allikas valikule Ajastamine.

3.  Importige uus väljavõte.





