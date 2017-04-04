---
title: "Korduvate arvete seadistamine ja töötlemine"
description: "Selles artiklis selgitatakse, kuidas seadistada ja töödelda korduvaid arveid. Saate kasutada korduvaid arveid, kui peate klientidega tuleb arveldada regulaarselt sama summa."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2f14e9227ef56f428d18999aa7b52254580cdfa4
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-and-process-recurring-invoices"></a>Korduvate arvete seadistamine ja töötlemine

Selles artiklis selgitatakse, kuidas seadistada ja töödelda korduvaid arveid. Saate kasutada korduvaid arveid, kui peate klientidega tuleb arveldada regulaarselt sama summa.

<a name="create-a-recurring-free-text-invoice-template"></a>Korduva vabas vormis arve malli loomine
---------------------------------------------

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
Lehel **Korduvad arved **on ülesanne, mis töötleb korduvate arvete malle. Saate määrata arve kuupäeva ja malli, millest arveid luua. Luuakse arved ja neile määratakse üks kordumise ID-kood iga töödeldava arvegrupi kohta.
Vabas vormis korduvate arvete sisestamine
---------------------------------

Pärast korduvate arvete loomist kuvatakse lehel **Korduvad arved **ülesande sisestamisel arve kordumise ID-koodid. Linki klõpsates saate vaadata kõigi arvete kordumise ID-d. Arvete kordumise ID ülevaatamisel saate eraldi arveid kustutada. Kliendi kordumise sätted lähtestatakse selle malli puhul, et seda saaks hiljem uuesti luua. Kordumise ID-koodile saab sisestada ühe arve, mitu arvet või kõik arved. Kui töövood on lubatud, peate klõpsama enne arvete sisestamist nuppu **Edasta**.
Vabas vormis korduvate arvete printimine
----------------------------------

Kui korduvad arved on sisestatud, saate printida arved vabas vormis arvete loendilehelt. Printida saab valitud arved või valida printimiseks arvete vahemiku.


