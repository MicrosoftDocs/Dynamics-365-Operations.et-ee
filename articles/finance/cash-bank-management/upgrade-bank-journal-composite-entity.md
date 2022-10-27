---
title: Pangatöölehe liitüksuse värskendamine
description: Selles artiklis loetletakse sammud, mida on vaja välja BankTransactionType lisamiseks liitväljale BankJournalEntity.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1855f9680ba6bcf8eb46608882a128b4a21f0dac
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715199"
---
# <a name="update-the-bank-journal-composite-entity"></a>Pangatöölehe liitüksuse värskendamine

[!include [banner](../includes/banner.md)]

Selles artiklis loetletakse sammud, mida on vaja välja BankTransactionType lisamiseks liitväljale BankJournalEntity.

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
