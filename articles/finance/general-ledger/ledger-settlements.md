---
title: Pearaamatu tasakaalustused
description: See artikkel selgitab, kuidas kasutada pearaamatu tasakaalustuste lehte pearaamatukannete tasakaalustamiseks ja tasakaalustuste tühistamiseks.
author: kweekley
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 6357629f83873437eb62a4839fafd8efd98fffc1
ms.sourcegitcommit: 9041fa6e00ecbdf1a1880659d9bdfff4d888f20e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/22/2022
ms.locfileid: "9800627"
---
# <a name="ledger-settlements"></a>Pearaamatu tasakaalustused

[!include [banner](../includes/banner.md)]

Pearaamatu tasakaalustamine on deebet- ja kreeditkannete vastavusseviimise protsess pearaamatus. Deebet- ja kreeditsummade tasakaalustust kasutatakse pearaamatukonto saldo vastavusseviimiseks üksikasjalike kannetega, mis selle saldo moodustab.

Tasakaalustatud kandeid saab päringutest ja aruannetest välja jätta. Sel viisil on lihtsam analüüsida avatud pearaamatukandeid, mis on pearaamatukonto saldo.

> [!IMPORTANT] 
> Ostureskontro (AP) ja müügireskontro (AR) moodulites on ka arvete ja maksete tasakaalustused. Kui tasakaalustus leiab aset AR-i ja AP alammoodulites, siis vastavaid pearaamatukirjeid automaatselt ei tasakaalustata.

## <a name="ledger-settlement-features"></a>Pearaamatu tasakaalustamise funktsioonid
Finantside Microsoft Dynamics versioonis 10.0.21 **·**  **eemaldati pearaamatu parameetrite lehelt suvand Luba laiendatud pearaamatu tasakaalustamine.**  Laiendatud pearaamatu tasakaalustus on nüüd alati lubatud.
Finantsversioonis 10.0.25 **tutvustati pearaamatu tasakaalustuse ja aasta lõpu sulgemise** funktsiooni vahelist arusaama. See funktsioon muudab põhifunktsioone nii pearaamatu tasakaalustamises kui ka pearaamatu aasta lõpu sulgemises. Enne selle funktsiooni lubamist funktsioonihalduse **tööruumis** vaadake pearaamatu [tasakaalustuse ja aasta lõpu sulgemise vahelist teadmist](awareness-between-ledger-settlement-year-end-close.md).

## <a name="set-up-ledger-settlement"></a>Seadista pearaamatu tasakaalustamine
Peate valima põhikontod, mille jaoks soovite pearaamatu tasakaalustamist teha. Nende põhikontode valimiseks on kaks viisi.

1. Minge pearaamatu **pearaamatu seadistuse** > **pearaamatu** > **parameetritele**.
2.  **Valige vahekaardil Pearaamatu tasakaalustused** kontoplaanid, millelt soovite põhikontosid valida.
3. Valige põhikontod, mille puhul soovite pearaamatu tasakaalustamist teha. Kuna kontoplaanid on globaalsed, on kõigil valitud kontoplaanidele määratud ettevõtetel pearaamatu tasakaalustamiseks valitud samad põhikontod.

  - või -

1. Minge pearaamatu perioodiliste **toimingute** > **pearaamatu** > **tasakaalustustele**.
2. Saate valida **pearaamatu tasakaalustuskontod**.
3. Valige dialoogiboksis kontoplaanid ja põhikontod, mille puhul soovite pearaamatu tasakaalustamist teha. See dialoogiboks on otsetee. Kõik siia lisatav põhikontod kajastuvad ka pearaamatu **parameetrite** lehel.

Samade põhiprotseduuride abil saate igal ajal põhikontod pearaamatu tasakaalustuselt eemaldada. Põhikonto eemaldamine ei mõjuta eelmisi pearaamatu tasakaalustusi. Põhikontot ja kandeid ei kuvata enam pearaamatu tasakaalustamise **lehel**.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Kannete tasakaalustamine
Pearaamatu kannete tasakaalustamiseks toimige järgmiselt.

1. Minge pearaamatu perioodiliste **toimingute** > **pearaamatu** > **tasakaalustustele**.
2. Seadke filtrid lehe ülaosas.

    - Kuupäevavahemiku valimine. Teise võimalusena valige kuupäevavahemiku kood, et kuupäevavahemik automaatselt täita. Me ei soovita teil teha pearaamatu tasakaalustusi kannetele, mis ristvad rahandusaastaid.
    - Muutke sisestuskihti vastavalt vajadusele. Te ei saa tasakaalustada kandeid, mis on erinevates sisestamiskihtides.
    - Põhikonto ja dimensioonide eraldi näitamiseks valige finantsdimensioonide kogum.

3. Valige **Kuva kanded**, et kuvada kõik kanded, mis vastavad seatud filtritele ja eelmises jaotises kontoplaani loomisel määratud kontode loendile.

    - Filtrite või dimensioonikogumite muutmisel peate uuesti valima **Kuva kanded**.
    - Kannete filtreerimiseks üksiku põhikonto järgi kasutage filtrit väljal **Pearaamatukonto** . Me ei soovita teil teha pearaamatu tasakaalustusi erinevatele põhikontodele sisestatud kannetele.

4. Valige tasakaalustuse read. Lehekülje ülaosas oleva **valitud summa** välja väärtus suureneb või väheneb, et kajastada valitud ridade kogusummat.
5. Kui olete kannete valimise lõpetanud, valige suvand **Märgi valituna**. Iga valitud kande puhul kuvatakse märge veerus **Märgitud**. Lisaks suureneb või väheneb **märgitud summa** välja väärtus ruudustiku kohal, et kajastada märgitud ridade kogusummat.
6. Kui väärtus väljal Märgitud summa **on**  **0** (null), valige suvand Tasakaalusta **märgitud kanded.** Märgistatud kannete olek uuendatakse olekule **Tasakaalustatud**.

    > [!IMPORTANT]
    > Kõik kanded, mille märkisite aktiivse juriidilise isiku tasakaalustamiseks, tasakaalustatakse, isegi kui neid ei kuvata praegu pearaamatu tasakaalustuse lehel, sest rakendasite filtri.

## <a name="make-transactions-easier-to-find"></a>Muudke kannete leidmine lihtsamaks
Pearaamatu **tasakaalustuste** leht sisaldab võimalusi, mis lihtsustavad tasakaalustuse jaoks vajaminev kannete vaatamist.

- Kasutage märgitud **filtrit**, et filtreerida kandeid selle **põhjal**, kas nende jaoks on märgitud ruut märgitud.
- Olekufiltri **abil** saate filtreerida kandeid nende oleku alusel.
- Valige **kogusumma järgi sortimine** summade järgi absoluutväärtuse järgi. Sel viisil saate grupeerida deebeteid ja kreediteid, mis on ühesuguse summaga.

## <a name="reverse-a-settlement"></a>Tasakaalustuse tühistamine
Saate tühistada ekslikult tehtud tasakaalustuse.

1. Järgige jaotises Kannete tasakaalustamine samme 1 kuni [3](#settle-transactions) , et näidata kandeid, mille suhtes olete huvitatud.
2. Valige **Oleku** filtris valik **Tasakaalustatud**.
3. Valige read, mida tagasipööramiseks valida.
4. Valige Märgitud **kannete tagasipööramine**. Kõigi sama tasakaalustuse ID-ga kannete olek uuendatakse olekuks **Tasakaalusta pole.**

    > [!IMPORTANT]
    > Kõik sama tasakaalustuse ID-ga kanded tühistatakse, isegi kui neid pole märgitud. Näiteks märgitakse ja tasakaalustati neli rida. Kõigil neljal real on sama tasakaalustuse ID. Kui märgite neljast reast ühe ja valite siis **märgitud kannete ümberpööramise**, tühistatakse kõik neli rida.

## <a name="unmark-for-selected-users"></a>Tühista märkimine valitud kasutajate jaoks
Valige **eemaldage märge valitud kasutajatelt,** et eemaldada märge pearaamatu tasakaalustatud kannetelt kõigi juriidiliste isikute puhul kasutaja ID järgi. Näiteks võimaldab see pearaamatupidajal eemaldada puhkusel enne tasakaalustuse lõpetamist puhkusel oleva või organisatsioonist lahkunud kasutaja kannete märke. Toiming lubab teisel kasutajal märkida need kanded tasakaalustamiseks.


## <a name="unmark-all-transactions"></a>Kõikide kannete märgistuse eemaldamine
Kõigi **kannete märke eemaldamine,** et eemaldada kõikide pearaamatu tasakaalustatud kannete märge kõigi kasutajate ja juriidiliste isikute puhul. See toiming on saadaval administraatori rollile.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
