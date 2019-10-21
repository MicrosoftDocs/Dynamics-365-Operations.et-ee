---
title: Rahvusvahelise pangakonto numbri (IBAN) konto valideerimise haldamine
description: Selles teemas selgitatakse, kuidas hallata rahvusvahelise pangakonto numbri (IBAN) konto valideerimist.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: a4f9bc2a22aabc7b83eb15665f37849d505e1b6b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177376"
---
# <a name="manage-international-bank-account-number-iban-validation"></a>Rahvusvahelise pangakonto numbri (IBAN) valideerimise haldamine

[!include [banner](../includes/banner.md)]

Rahvusvahelise pangakonto numbri (IBAN) valideerimine suurendab valideerimise hulka, mis tehakse IBAN-i lisamisel pangakontole.

Teavet IBAN-i struktuuri kohta talletatakse rakenduses Microsoft Dynamics 365 Finance. See teave laaditakse automaatselt, kui kasutate pangakontodel esmakordselt IBAN-i. See sisaldab IBAN-i pikkust, pangakonto numbri ja protsessinumbri alguspositsioone ning pangakonto numbri ja protsessinumbri pikkuseid.

## <a name="set-up-iban-structures"></a>IBAN-i struktuuride seadistamine

1. Minge jaotisse **Sularaha- ja pangahaldus \> Seadistus \> IBAN-i struktuurid**.
2. Pange tähele, et iga riigi või piirkonna IBAN-i struktuurid on automaatselt seadistatud.
3. Kui tahate struktuure konkreetse riigi või piirkonna jaoks kohandada, saate neid redigeerida.
4. Struktuuri definitsioonid on osa igast uuest väljaandest. Pärast iga uuendust uusimate definitsioonide laadimiseks võite kasutada menüüd **Lähtesta struktuurid**.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>IBAN-i struktuuri valideerimine pangakontol

1. Minge jaotisse **Sularaha- ja pangahaldus \> Pangakontod \> Pangakontod**.
2. Looge pangakonto.
3. Sisestage IBAN kiirkaardile **Lisateave**.

    Kui IBAN-i pikkus ei kattu iga riigi või regiooni jaoks määratletud pikkusega, kuvatakse hoiatusteade. Te ei saa jätkata, kui IBAN-i pikkus ei ühti IBAN-i struktuuris määratletud pikkusega.

    Valideerimine kontrollib ka seda, kas pangakonto number ühtib IBAN-i osaga, mis kujutab pangakonto numbrit. Kui pangakonto number ei ühti, kuvatakse hoiatusteade. See teade on ainult hoiatus. Saate jätkata, isegi kui pangakonto number ei ühti.

    Valideerimine kontrollib ka seda, kas protsessikood ühtib IBAN-i osaga, mis kujutab panga protsessikoodi. Protsessikood sisaldab panga numbrit ja sageli ka täiendavat panga filiaali. Kui panga protsessikood ei ühti, kuvatakse hoiatusteade. See teade on ainult hoiatus. Saate jätkata, isegi kui panga protsessikood ei ühti.
