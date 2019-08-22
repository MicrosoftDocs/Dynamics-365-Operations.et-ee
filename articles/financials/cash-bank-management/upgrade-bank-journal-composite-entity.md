---
title: Pangatöölehe liitüksuse värskendamine
description: Järgmised etapid on vajalikud, et lisada täiendav väli BankTransactionType liitüksusele BankJournalEntity.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 974d6b3b11df92debdec26860fd9eea00a9f2313
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841773"
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




