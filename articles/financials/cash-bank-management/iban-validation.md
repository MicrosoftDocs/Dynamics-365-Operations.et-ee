---
title: Rahvusvahelise pangakonto numbri (IBAN) konto valideerimise haldamine
description: Selles teemas selgitatakse, kuidas hallata rahvusvahelise pangakonto numbri (IBAN) konto valideerimist.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: et-ee
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a>Rahvusvahelise pangakonto numbri (IBAN) konto valideerimise haldamine

[!include [banner](../includes/banner.md)]

Rahvusvahelise pangakonto numbri (IBAN) konto valideerimine suurendab valideerimise hulka, mis tehakse IBAN-i lisamisel pangakontole.

IBAN-i struktuur salvestatakse rakendusse Microsoft Dynamics 365 for Finance and Operation ja see laaditakse automaatselt, kui IBAN-it esimest korda pangakontodel kasutate. Pangakonto number on osa IBAN-i numbri jaoks määratud struktuurist. Selle struktuuri põhjal saate hoiatusteateid, kui kontonumbri asukoht ja pikkus IBAN-is ei ühti struktuuris iga riigi või piirkonna jaoks määratud asukohaga.

## <a name="set-up-iban-structures"></a>IBAN-i struktuuride seadistamine

1. Minge jaotisse **Sularaha- ja pangahaldus \> Seadistus \> IBAN-i struktuurid**.
2. Pange tähele, et iga riigi või piirkonna IBAN-i struktuurid on automaatselt seadistatud.
3. Kui teil on vaja struktuure konkreetse riigi või piirkonna jaoks kohandada, saate neid redigeerida.
4. Struktuuri definitsioonid on osa igast uuest väljaandest. Pärast iga uuendust uusimate definitsioonide laadimiseks võite kasutada menüüd **Lähtesta struktuurid**.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>IBAN-i struktuuri valideerimine pangakontol

1. Minge jaotisse **Sularaha- ja pangahaldus \> Pangakontod \> Pangakontod**.
2. Looge pangakonto.
3. Sisestage IBAN kiirkaardile **Lisateave**.

    Teile kuvatakse teade, kui kontonumbri asukoht ja pikkus IBAN-is ei ühti struktuuris iga riigi või piirkonna jaoks määratud asukohaga. Te ei saa jätkata, kui IBAN-i pikkus ei ühti pikkusega IBAN-i struktuuris.

    Valideerimine kontrollib ka seda, kas pangakonto number ühtib IBAN-i osaga, mis kujutab pangakonto numbrit. Kui pangakonto number ei ühti, kuvatakse hoiatusteade. See teade on ainult hoiatus. Saate jätkata, isegi kui pangakonto number ei ühti.

