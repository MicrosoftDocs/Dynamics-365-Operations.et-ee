---
title: Korduvate arvete seadistamine ja töötlemine
description: Selles artiklis selgitatakse, kuidas seadistada ja töödelda korduvaid arveid. Saate kasutada korduvaid arveid, kui peate klientidega tuleb arveldada regulaarselt sama summa.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: kfend
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce734567f0c5bf02e30c36484449c3869b82dc84
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724751"
---
# <a name="set-up-and-process-recurring-invoices"></a>Korduvate arvete seadistamine ja töötlemine

[!include [banner](../includes/banner.md)]

Selles artiklis selgitatakse, kuidas seadistada ja töödelda korduvaid arveid. Saate kasutada korduvaid arveid, kui peate klientidega tuleb arveldada regulaarselt sama summa.

## <a name="create-a-recurring-free-text-invoice-template"></a>Korduva vabas vormis arve malli loomine

Klientidele regulaarselt samade teenuste eest arve esitamiseks tuleb määratleda vabas vormis arve mall, mida saab arvete koostamisel uuesti kasutada. See mall sisaldab järgmist teavet:

-   Päise teave, nt maksugrupid, maksetingimused ja makseviis
-   Rea teave nagu teenuse kirjeldus, tulukontod, ühiku hind ja arve summa
-   Saatmise ja käsitsemise tasud
-   Arvestuse jaotused koos finantsdimensiooni teabega (nt kulukeskused ja äriüksused)

Tegelikult koostate terve arve ja salvestate selle mallina. Saate seadistada malle lehel **Korduvad arved**.

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a>Korduva vabas vormis arve malli määramine kliendile ja kordumise üksikasjade sisestamine
Pärast malli loomist peate määrama malli klientidele, kellega soovite arveldada. Lisaks peate määrama, millal ja kui sageli arvet kasutatakse. Malle saab määrata vahekaardil **Arve** lehel **Kliendid**. Lisage mall loendisse ja muutke järgmisi andmeid.

-   Alguskuupäev ja soovi korral korduva arvelduse lõppkuupäev
-   Korduva arvelduse sagedus (nt iga päev või kord kuus)
-   Maksimaalne arvete summa (kui see on vajalik)

Kliendil võib olla mitu malli, millel on erinevad sagedused.

## <a name="generate-the-recurring-invoices"></a>Korduvate arvete loomine
Lehel **Korduvad arved** on ülesanne, mis töötleb korduvate arvete malle. Saate määrata arve kuupäeva ja malli, millest arveid luua. Luuakse arved ja neile määratakse üks kordumise ID-kood iga töödeldava arvegrupi kohta.

## <a name="post-recurring-free-text-invoices"></a>Vabas vormis korduvate arvete sisestamine

Pärast korduvate arvete loomist kuvatakse lehel **Korduvad arved** ülesande sisestamisel arve kordumise ID-koodid. Linki klõpsates saate vaadata kõigi arvete kordumise ID-d. Arvete kordumise ID ülevaatamisel saate eraldi arveid kustutada. Kliendi kordumise sätted lähtestatakse selle malli puhul, et seda saaks hiljem uuesti luua. Kordumise ID-koodile saab sisestada ühe arve, mitu arvet või kõik arved. Kui töövood on lubatud, peate klõpsama enne arvete sisestamist nuppu **Edasta**.

## <a name="print-recurring-free-text-invoices"></a>Vabas vormis korduvate arvete printimine

Kui korduvad arved on sisestatud, saate printida arved vabas vormis arvete loendilehelt. Printida saab valitud arved või valida printimiseks arvete vahemiku.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
