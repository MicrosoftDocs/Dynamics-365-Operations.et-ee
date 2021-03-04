---
title: Pearaamatu tasakaalustused
description: Selles teemas kirjeldatakse, kuidas kasutada pearaamatu tasakaalustuste lehte pearaamatukannete tasakaalustamiseks ja taskaalustuste tühistamiseks.
author: mikefalkner
manager: aolson
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: d41a69bed3d1340736cc7df35aa3ded032d4d79d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442278"
---
# <a name="ledger-settlements"></a>Pearaamatu tasakaalustused

[!include [banner](../includes/banner.md)]

Pearaamatu tasakaalustustega saate sobitada deebet- ja krediitkandeid pearaamatus ning märkida need tasakaalustatuks. Sel viisil saate veenduda, et seotud kanded on tühjendatud. Saate ka tühistada ekslikult tehtud tasakaalustusi.

## <a name="enable-advanced-ledger-settlements"></a>Luba laiendatud pearaamatu tasakaalustamised

Laiendatud pearaamatu tasakaalustuste leht pakub lisavõimalusi kannete filtreerimiseks ja valimiseks. Laiendatud pearaamatu tasakaalustuste lehe lubamiseks toimige järgmiselt.

1. Valige **Pearaamat** \> **Pearaamatu seadistamine** \> **Pearaamatu parameetrid**. 
2. Laiendatud pearaamatu tasakaalustamise funktsiooni sisselülitamiseks määrake **Pearaamatu tasakaalustuste** vahekaardil **Laiendatud pearaamatu tasakaalustamised** suvandiks **Jah**. Laiendatud **Pearaamatu tasakaalustuste** lehte kasutatakse, kui valite **Pearaamatu tasakaalustused** suvandis **Perioodilisi toiminguid**. 
3. Peate iga kontoplaani jaoks sisestama pearaamatu tasakaalustamiseks kasutatavate kontode loendi. Seda loendit kasutatakse kannete loendi filtreerimiseks, mis kuvatakse **Pearaamatu tasakaalustuste** leheküljel. Valige **Kontoplaani** loendis kontoplaan ja seejärel valige uute kontode loendisse lisamiseks **Uus**.

## <a name="settle-transactions-by-using-the-advanced-ledger-settlements-page"></a>Tasakaalustage kanded laiendatud pearaamatu tasakaalustuste lehega

Pearaamatu kannete tasakaalustamiseks toimige järgmiselt.

1. Valige **Pearaamat** \> **Perioodilised ülesanded** \> **Pearaamatu tasakaalustused**.
2. Seadke filtrid lehe ülaosas.

    - Valige kuupäevavahemik või **Kuupäevaintervalli kood** automaatseks kuupäevavahemiku täitmiseks.
    - Muutke vajadusel sisestamiskihti.
    - Pearaamatukonto ja dimensiooni eraldi kuvamiseks valige määratud finantsdimensioon.

3. Valige **Kuva kanded**, et kuvada kõik kanded, mis vastavad seatud filtritele ja eelmises jaotises kontoplaani loomisel määratud kontode loendile. Filtrite või dimensioonikogumite muutmisel peate uuesti valima **Kuva kanded**.
4. Valige üks või mitu rida, mida soovite tasakaalustada. Välja **Valitud summa** väärtus lehe ülaosas suureneb või kahaneb vastavalt valitud ridade kogusummale.
5. Pärast kannete valimise lõpetamist valige **Märgi valituks**. Iga valitud kande eest ilmub **Märgistatud** veergu linnuke. Lisaks, välja **Märgistatud summa** väärtus ruudustiku kohal suureneb või kahaneb vastavalt märgistatud ridade kogusummale.
6. Kui **Märgistatud summa** väärtus on **0** (null), valige **Märgistatud kannete tasakaalustamine**. Märgistatud kannete olek uuendatakse olekule **Tasakaalustatud**.

## <a name="make-transactions-easier-to-find"></a>Muudke kannete leidmine lihtsamaks

**Pearaamatu tasakaalustuste** leht sisaldab funktsioone, mis hõlbustavad tasakaalustamist vajavate kannete nägemist.

- Nupp **Tühista valik** tühjendab **Märgistatud** välja kõigist valitud ridadest.
- **Märgistatud** filtri abil saate filtreerida kandeid vastavalt sellele, kas nende **Märgistatud** väli on valitud või tühjendatud.
- **Oleku** filtri abil saate filtreerida kandeid vastavalt sellele, kas nende olek on **Tasakaalustatud** või **Tasakaalustamata**.
- Nupp **Summa järgi sorteerimine** võimaldab sorteerida summasid absoluutväärtuse järgi, nii et saate grupeerida deebetid ja kreeditid, millel on sama summa.

## <a name="reverse-a-settlement"></a>Tasakaalustuse tühistamine

Saate tühistada ekslikult tehtud tasakaalustuse.

1. Otsitavate kannete kuvamiseks järgige jaotise "Kannete tasakaalustamine, kasutades laiendatud pearaamatu tasakaalustamise lehte" samme 1–3.
2. Valige **Oleku** filtris valik **Tasakaalustatud**.
3. Valige üks või mitu rida, mille tasakaalustamist soovite tühistada. Välja **Valitud summa** väärtus lehe ülaosas suureneb või kahaneb vastavalt valitud ridade kogusummale.
4. Pärast kannete valimise lõpetamist valige **Märgi valituks**. Iga valitud kande eest ilmub **Märgistatud** veergu linnuke. Lisaks, välja **Märgistatud summa** väärtus lehe ülaosas suureneb või kahaneb vastavalt märgistatud ridade kogusummale.
5. Kui **Märgistatud summa** väärtus on **0** (null), valige **Märgistatud kannete tasakaalustamise tühistamine**. Märgistatud kannete olek uuendatakse olekule **Tasakaalustamata**.

## <a name="update-the-list-of-accounts-that-are-included-in-the-list-of-transactions"></a>Värskendage kannete loendisse kaasatud kontode loendit

Valige **Pearaamatu tasakaalustuskonto**, et avada dialoogiboks, kui saate redigeerida kannete loendisse kaasatud kontosid. Valige loendisse uue konto lisamiseks **Uus**. Seda loendit kasutatakse kannete loendi filtreerimiseks, mis kuvatakse **Pearaamatu tasakaalustuste** leheküljel.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]