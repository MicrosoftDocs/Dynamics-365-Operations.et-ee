---
title: Arve tükeldamise funktsioon
description: Selles teemas kirjeldatakse arvete tarneaadressi ja maksukonto numbri (TAN) tükeldamise seadistust ja funktsioone.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: f9bb4db14cbb7c9abb33ccee532ed73b378317bb
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/12/2022
ms.locfileid: "8408351"
---
# <a name="split-invoice-functionality"></a>Arve tükeldamise funktsioon

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse arvete tarneaadressi ja maksukonto numbri (TAN) tükeldamise seadistust ja funktsioone.

Märkige **Ostureskontro parameetrite** lehel **Üldine** vahekaardil **Toote sissetulek** või **Arve** et sisestada ja tükeldada toote sissetulek või arve, mille tarneaadressid TAN-is on erinevad kui **Ostutellimuse** lehel. Seejärel tükeldatakse sisestatud arve tarneaadressi ja teenuseaadressi järgi.

Kinnituse, komplekteerimislehe, saatelehe või arve sisestamiseks ja tükeldamiseks seadke **Koondvärskendus** vahekaardil **Tarneteave suvandi** kiirkaardil **Tarneteabe** suvandi **Kinnitus**, **Komplekteerimisleht**, **Saateleht** või **Arve** valik **Jah** kui müügitellimuse lehel on erinevate arveridade jaoks määratud erinevad **tarneaadressid** ja TAN-id. Seejärel tükeldatakse sisestatud arve tarneaadressi ja teenuseaadressi järgi.

> [!IMPORTANT]
> - Kui **tarneteabe** valikud ei ole seatud valikule **Jah** sisestatakse arve üksiku arvena. Arve tükeldamist ei toimu.
> - Saatelehe tükeldamiseks ja sisestamiseks, kus arve ridadel on erinevad tarneaadressid ja TAN-id, tuleb tarneteabe jaoks **Tarneteabe** **Saatelehe suvandi** väärtuseks seada **Jah**.
> - Saatelehe tükeldamiseks ja sisestamiseks, kus arve ridadel on erinevad tarneaadressid ja TAN-id, tuleb **Arve** suvand **Saatelehe teave** väärtuseks seada **Jah**.
> - Saatelehe sisestamiseks, kus arve ridadel on erinevad tarneaadressid, aga sama TAN, tuleb **Arve** valik **Tarne teave** suvand seada **Ei**. Seejärel tükeldatakse sisestatud arve tarneaadressi järgi.

## <a name="example"></a>Näide

Selles näites on **Arve** valik **Tarne teave** seadistatud **Jah** **Koonduuendamise** vahekaardil **Ostureskontro parameetrite** lehel. Sisestatakse ostuarve, kus tarneaadresside ja TN-ide ridade seadistus on järgmine:

- **Kauba rida 1:** Tarneaadress 1, ABCD-ABCD12345A
- **Kauba rida 2:** Tarneaadress 1, ABCD-ABCD12345A
- **Kauba rida 3:** Tarneaadress 2, ABCD-ABCD12345B
- **Kauba rida 4:** Tarneaadress 3, TAN-ABCD12345A

Sel juhul tükeldatakse esialgne arve kaheks arveks ja sisestatakse järgmisel viisil:

- Arve 1 sisestatakse kaubareale 1 ja kaubareale 2, kuna mõlemal real on sama tarneaadress ja tagasiarveldmiskuupäev.
- Arve 2 sisestatakse kaubareale 3.
- Arve 3 sisestatakse kaubareale 4.
