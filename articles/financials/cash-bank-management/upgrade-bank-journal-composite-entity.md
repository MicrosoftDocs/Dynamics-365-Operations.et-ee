---
title: "Pangatöölehe liitüksuse värskendamine"
description: "Järgmised etapid on vajalikud, et lisada täiendav väli BankTransactionType liitüksusele BankJournalEntity."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 43413aad9d537e518f7276ccab11ce01d23cf13f
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017

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




