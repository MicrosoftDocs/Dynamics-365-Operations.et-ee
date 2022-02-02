---
title: Seadista ja töötle sildmakseid
description: See teema kirjeldab, kuidas seadistada ja töödelda kliendi sildmakseid. Sildmakse on makse, mis sisestatakse pearaamatusse kahe sammuga.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode, VendPaymMode, LedgerJournalTable, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e1418e573f34fadcf0bebc7232d847ee7e9768b
ms.sourcegitcommit: 5bfd6511d710deb539b4030eb0e9c48d25513595
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/19/2022
ms.locfileid: "8014094"
---
# <a name="set-up-and-process-bridged-payments"></a>Seadista ja töötle sildmakseid

[!include [banner](../includes/banner.md)]

Sildmakse on makse, mis sisestatakse pearaamatusse kahe sammuga. Tavaliselt kasutatakse seda lähenemist, kui makseviisiks on seatud Pank ja te peate sisestama kanded pangakontole ainult siis, kui kanne on pangast **tühjendanud**. Te saate seda siiski kasutada ka pearaamatukonto puhul. Sel juhul teisaldab süsteem summa ühest põhikontost teise põhikontole, kui kasutatakse tkontole sisestamisel.

Te saate luua sildmakseid kas Ostureskontrost või Müügireskontrost. Ehkki see teema kirjeldab, kuidas konfigureerida müügireskontro jaoks ajatagastamist, on ostureskontro kannete sammud sarnased.

## <a name="set-up-bridging-posting"></a>Saate häälestada lisatöötlemise sisestamist.

Selleks, et kasutada ajatagastusmeetodit, peate seadistama ühe või mitu maksemeetodit nii, et nad kasutaks **bridging**-sisestusmeetodit. Seejärel peate valimadging account.

1. Avage **müügireskontro &gt; makse &gt; seadistuse makseviisid**.
2. Valige olemasolev makseviis, mille jaoks lubada ajutiselt sisestamist. Teise võimalusena looge uus makseviis.
3. Märkige ruut **Riskini** sisestamine.
4. Väljal **Bridging account** valige põhikonto, mille maksed tuleb sisestada enne, kui need pangakontole tühjendatakse.
5. Sulgege leht.

## <a name="process-and-transfer-bridging-posting"></a>Protsessi ja üleviimise üleminekukontole sisestamine

Etapitööle sisestamise loomiseks ja töötlemiseks järgige neid samme.

1. Avage **Müügireskontro &gt; Maksed &gt; Kliendi makse tööleht**.
2. Valige **Uus**, et luua uus tööleht.
3. Valige **nimi** väljal Nimi.
4. Lisage ridu kliendi maksetöölehele ja valige makseviis, mis on konfigureeritud vaheldamiseks sisestamiseks.
5. Sisestab töölehe. Kanded sisestatakse põhikontole, mille valisite eelmise protseduuri väljal **Bridging** account.

Kui kanded on panga tühjendanud ja soovite makse üle kanda üleminekukontolt makseviisi jaoks määratud maksekontole, järgige neid samme.

1. Avage **Pearaamat &gt; Töölehekirjed &gt; Päevaraamatud**.
2. Valige **Uus**, et luua uus tööleht.
3. Valige **nimi** väljal Nimi.
4. Valige **read töölehe üksikasjade** avamiseks.
5. Valige **&gt; funktsioonid. Valige** sildkanded.
6. Märkige kõik tühjendatud maksed ja seejärel valige **Aktsepteeri**.
7. Sisestab töölehe.
