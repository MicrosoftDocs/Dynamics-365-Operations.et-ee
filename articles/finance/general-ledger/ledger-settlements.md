---
title: Pearaamatu tasakaalustused
description: Selles teemas kirjeldatakse, kuidas kasutada pearaamatu tasakaalustuste lehte pearaamatukannete tasakaalustamiseks ja taskaalustuste tühistamiseks.
author: kweekley
ms.date: 01/31/2022
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
ms.openlocfilehash: e98b012210338e7f18cb874eefbc8a023aa4428b
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075320"
---
# <a name="ledger-settlements"></a>Pearaamatu tasakaalustused

[!include [banner](../includes/banner.md)]

Pearaamatu tasakaalustus on pearaamatu deebet- ja kreeditkannete sobitamise protsess. Deebet- ja kreeditsummade arveldamist kasutatakse pearaamatukonto saldo vastavusse ühildamiseks selle saldo moodustavate üksikasjalike kannetega.

Tasakaalustatud kanded saab päringutest ja aruannetest välja jätta. Sel viisil on lihtsam analüüsida avatud pearaamatukandeid, mis moodustavad pearaamatukonto saldo.

> [!IMPORTANT] 
> Ostureskontro (AP) ja müügireskontro moodulid (AR) arveldavad ka arveid ja makseid. Kui tasakaalustamine toimub liit- ja AP-alammoodulites, ei tasakaalustata vastavaid andmikukandeid automaatselt.

## <a name="ledger-settlement-features"></a>Pearaamatu tasakaalustuse funktsioonid
Microsofti Dynamics 365 Finance versioonis 10.0.21 **eemaldati** lehelt Pearaamatu parameetrite suvand Luba täpsem pearaamatu **tasakaalustus**. Täpsem pearaamatu tasakaalustus on nüüd alati lubatud.
Finance'i versioonis 10.0.25 **võeti kasutusele teadlikkus pearaamatu tasakaalustamise ja aastalõpu sulgemisfunktsiooni** vahel. See funktsioon muudab põhifunktsioone nii pearaamatu tasakaalustuses kui ka pearaamatu aastalõpu sulgemises. Enne selle funktsiooni lubamist **funktsioonihalduse** tööruumis lugege lisateavet teemast [Teadlikkus pearaamatu tasakaalustuse ja aastalõpu sulgemise](awareness-between-ledger-settlement-year-end-close.md) vahel.

## <a name="set-up-ledger-settlement"></a>Pearaamatu tasakaalustuse häälestamine
Peate valima põhikontod, mille jaoks soovite pearaamatu tasakaalustuse teha. Nende põhikontode valimiseks on kaks võimalust.

1. **Avage pearaamatu** > **ledger setupGeneral** > **ledger parameters**.
2. Valige vahekaardil **Pearaamatu tasakaalustused** nende kontode diagrammid, mille hulgast soovite põhikontod valida.
3. Valige põhikontod, mille pearaamatu tasakaalustamiseks. Kuna kontoplaanid on globaalsed, on kõigil ettevõtetel, kellele valitud kontoplaanid on määratud, pearaamatu tasakaalustamiseks valitud samad põhikontod.

  - või -

1. **Avage pearaamatPeriodsed** > **ülesandedLedgeri** > **tasakaalustused**.
2. Valige **Pearaamatu tasakaalustuskontod**.
3. Valige dialoogiboksis konto- ja põhikontode diagrammid, mille jaoks pearaamatu tasakaalustada. See dialoogiboks on otsetee. Kõik siia lisatud põhikontod kajastuvad **ka pearaamatu parameetrite** lehel.

Põhikontode pearaamatu tasakaalustuselt eemaldamiseks saate igal ajal kasutada samu põhiprotseduure. Põhikonto eemaldamine ei mõjuta varasemaid pearaamatu tasakaalustusi. Põhikontot ja kandeid ei kuvata **siiski enam lehel Pearaamatu tasakaalustus**.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Kannete tasakaalustamine
Pearaamatu kannete tasakaalustamiseks toimige järgmiselt.

1. **Avage pearaamatPeriodsed** > **ülesandedLedgeri** > **tasakaalustused**.
2. Seadke filtrid lehe ülaosas.

    - Kuupäevavahemiku valimine. Teise võimalusena valige kuupäevavahemiku automaatseks täitmiseks kuupäevavahemiku kood. Me ei soovita teil teha pearaamatu tasakaalustust finantsaastaid läbivate kannete puhul.
    - Muutke sisestuskihti vastavalt vajadusele. Te ei saa arveldada tehinguid, mis on erinevates postitamiskihtides.
    - Põhikonto ja dimensioonide eraldi kuvamiseks valige finantsdimensioonikomplekt.

3. Valige **Kuva kanded**, et kuvada kõik kanded, mis vastavad seatud filtritele ja eelmises jaotises kontoplaani loomisel määratud kontode loendile.

    - Filtrite või dimensioonikogumite muutmisel peate uuesti valima **Kuva kanded**.
    - Kannete filtreerimiseks üksikule põhikontole kasutage välja Pearaamatukonto **filtrit**. Me ei soovita teil teha pearaamatu tasakaalustust kannete jaoks, mis on konteeritud erinevatele põhikontodele.

4. Valige arveldamiseks read. Väärtus **Valitud summa** lehe ülaosas olev väli suureneb või väheneb, et kajastada valitud ridade kogusummat.
5. Kui olete tehingute valimise lõpetanud, valige **Märgi valituks**. Iga valitud tehingu kohta kuvatakse linnuke **Märgitud** veerg. Lisaks väärtus **Märgitud summa** ruudustiku kohal olev väli suureneb või väheneb, et kajastada märgitud joonte kogusummat.
6. Kui väärtus on **Märgitud summa** väli on **0** (null), valige **Arveldage märgitud tehingud**. Märgistatud kannete olek uuendatakse olekule **Tasakaalustatud**.

    > [!IMPORTANT]
    > Kõik aktiivse juriidilise isiku tasakaalustamiseks märgitud kanded tasakaalustatakse, isegi kui neid pole praegu pearaamatu tasakaalustuse lehel kuvatud, kuna rakendasite filtri.

## <a name="make-transactions-easier-to-find"></a>Muudke kannete leidmine lihtsamaks
The **Pearaamatu arveldused** leht sisaldab võimalusi, mis hõlbustavad arveldamiseks vajalike tehingute vaatamist.

- Kasutage kannete filtreerimiseks filtrit **selle** põhjal, **kas nende jaoks on märgitud ruut Märgitud**.
- **Kasutage olekufiltrit** kannete filtreerimiseks nende oleku alusel.
- Summade sortimiseks absoluutväärtuse järgi valige **Sordi absoluutsumma** järgi. Sel viisil saate rühmitada deebeteid ja krediite, millel on sama summa.

## <a name="reverse-a-settlement"></a>Tasakaalustuse tühistamine
Saate tühistada ekslikult tehtud tasakaalustuse.

1. Järgige samme 1 kuni 3 jaotises [Arvelda tehingud](#settle-transactions) Teid huvitavate tehingute kuvamiseks.
2. Valige **Oleku** filtris valik **Tasakaalustatud**.
3. Valige ümberpööramiseks read.
4. Valige **Pöördmärgistatud tehingud**. Kõigi sama arveldus-ID-ga tehingute olekut värskendatakse **Ei lahendatud**.

    > [!IMPORTANT]
    > Kõik sama arveldus-ID-ga tehingud tühistatakse, isegi kui need pole märgitud. Näiteks märgiti ja arveldati neli rida. Kõigil neljal real on sama asula ID. Kui märgite ühe neist neljast reast ja seejärel valige **Pöördmärgistatud tehingud**, pööratakse kõik neli rida ümber.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
