---
title: Rahvusvahelise pangakonto numbri (IBAN) konto valideerimise haldamine
description: Selles teemas selgitatakse, kuidas hallata rahvusvahelise pangakonto numbri (IBAN) konto valideerimist.
author: twheeloc
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 89d6c38088e43f0f24fa41accecaa262a64006cf
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462760"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a>Rahvusvahelise pangakonto numbri (IBAN) konto valideerimise haldamine

[!include [banner](../includes/banner.md)]

Rahvusvahelise pangakonto numbri (IBAN) valideerimine suurendab valideerimise hulka, mis tehakse IBAN-i lisamisel pangakontole.

Teave IBAN-i struktuuri kohta on Talletatud Microsoftis Dynamics 365 Finance ja see laaditakse automaatselt, kui kasutate esimest korda IBAN-i pangakontol. See sisaldab IBAN-i pikkust, pangakonto numbri ja protsessinumbri alguspositsioone ning pangakonto numbri ja protsessinumbri pikkuseid.

## <a name="set-up-iban-structures"></a>IBAN-i struktuuride seadistamine

1. Minge jaotisse **Sularaha- ja pangahaldus \> Seadistus \> IBAN-i struktuurid**.
2. Pange tähele, et iga riigi või piirkonna IBAN-i struktuurid on automaatselt seadistatud.
3. Kui teatud **riigi** või regiooni struktuuri on vaja uuendada, valige nupp Redigeeri.
4. Struktuuri definitsioonid on osa igast uuest väljaandest. Pärast iga uuendust uusimate definitsioonide laadimiseks võite kasutada menüüd **Lähtesta struktuurid**.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>IBAN-i struktuuri valideerimine pangakontol

1. Minge jaotisse **Sularaha- ja pangahaldus \> Pangakontod \> Pangakontod**.
2. Looge pangakonto.
3. Sisestage IBAN kiirkaardile **Lisateave**.

    Kui IBAN-i pikkus ei kattu iga riigi või regiooni jaoks määratletud pikkusega, kuvatakse hoiatusteade. Te ei saa jätkata, kui IBAN-i pikkus ei ühti IBAN-i struktuuris määratletud pikkusega.

    Valideerimine kontrollib ka seda, kas pangakonto number ühtib IBAN-i osaga, mis kujutab pangakonto numbrit. Kui pangakonto number ei ühti, kuvatakse hoiatusteade. See teade on ainult hoiatus. Saate jätkata, isegi kui pangakonto number ei ühti.

    Valideerimine kontrollib ka seda, kas protsessikood ühtib IBAN-i osaga, mis kujutab panga protsessikoodi. Protsessikood sisaldab panga numbrit ja sageli ka täiendavat panga filiaali. Kui panga protsessikood ei ühti, kuvatakse hoiatusteade. See teade on ainult hoiatus. Saate jätkata, isegi kui panga protsessikood ei ühti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
