---
title: Pangatöölehe liitüksuse värskendamine
description: Järgmised etapid on vajalikud, et lisada täiendav väli BankTransactionType liitüksusele BankJournalEntity.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7e265915cf3f53a8243788b50a9374d521efbbae
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819598"
---
# <a name="update-the-bank-journal-composite-entity"></a>Pangatöölehe liitüksuse värskendamine

[!include [banner](../includes/banner.md)]

Järgmised etapid on vajalikud, et lisada täiendav väli BankTransactionType liitüksusele BankJournalEntity.

Kasutage järgmisi etappe, et lisada täiendav väli BankTransactionType liitüksusele BankJournalEntity.

1.  Kompileerige ja sünkroonige järgmised panga töölehe liitüksused, üksused ja vahetabelid.
    -   Liitüksus\\BankJournalEntity
    -   Üksus\\BankJournalHeaderEntity
    -   Üksus\\BankJournalLineEntity
    -   Tabel\\BankJournalHeaderStaging
    -   Tabel\\BankJournalLineStaging

2.  Andmehaldus\\andmeprojektid
    -   Avage tüüp **Pangakanne** paigutuses **Lähteandmed**.
        -   Lähteandmete vorming = XML-element
        -   Üksuse nimi = Panga tööleht
        -   Andmefaili üleslaadimise = uus faili SampleBankJournalCompositeEntity.xml versioon.
        -   Klõpsake valikut **Jah**, et olemasolev fail üle kirjutada.
        -   Klõpsake valikut **Jah**, et luua vastendus nullist.
        -   Kontrollige, kas pangakande tüüp on vastendatud.
            -   Klõpsake rea üksust **Kuva kaart**.
            -   Kontrollige, kas pangekande tüüp on vastendatud valikult Allikas valikule Ajastamine.

3.  Importige uus väljavõte.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]