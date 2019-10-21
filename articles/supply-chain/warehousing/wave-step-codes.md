---
title: Vooetapi koodid
description: See teema annab ülevaate vooetapi koodidest ja nende kasutamisest.
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992353"
---
# <a name="wave-step-codes"></a>Vooetapi koodid

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a>Vooetapi koodid

Vooetapi koodid on koodid, mida kasutajad saavad seadistada ja kasutada vastavale mallile konkreetsete juhtumite linkimiseks. Mallid sisaldavad malle täiendamiseks, konteineritesse panemiseks, siltide printimiseks, koormuste loomiseks ja sortimiseks.

Kui voo etapi koode ei kasutata, peavad kasutajad sisestama vaba teksti, et viidata kindlale mallile laine meetodi eksemplarist. Vabal tekstil on kalduvus vigadeks, kuna kasutajad peavad veenduma, et voo-etapi tekst, mida nad lisavad konkreetse vooetapi meetodi jaoks voo malli puhul, vastab täpselt sihtmalli tekstile.

Konkreetse vooetapi tüübi vooetapi koodid seadistatakse eraldi lehel. Voomalli iga vooetabi meetodi eksemplari korral, mis vajab vooetapi koodi, tuleb vooetapi kood valida ripploendist. Ripploendi valik asendab vaba tekstisisestuse ja aitab vähendada inimlike vigade riski ja mõju. Seadistuse koode kasutatakse vooetapi meetodi sidumiseks voomallis meetodi sihtmalliga.

> [!NOTE]
> Vooetabi koodide funktsiooni kasutamine on valikuline ja kasutamine käib iga juriidilise isiku kohta eraldi. Seetõttu, kui konkreetne juriidiline isik kasutab funktsiooni, uuendatakse kõik selle juriidilise isiku olemasolevad voo etapikoodid uude struktuuri.

## <a name="setup-demo"></a>Häälestuse demo 

Selle demo jaoks peavad olema installitud demo andmed ja peate kasutama testandmete ettevõtet **USMF**.

### <a name="enable-wave-step-codes"></a>Luba vooetapi koodid

Järgige neid samme, et lülitada sisse voo etapi koodide funktsioon.

1. Avage **Laohaldus \> Seadistus \> Laohalduse parameetrid**.
2. Määrake vahekaardil **Üldine** kiirkaardil **Vootöötlus** suvand **Luba voo etapikoodid** olekusse **Jah**.

Kõik olemasolevad vooetappide vabad tekstid värskendatakse uuele struktuurile. Pärast seda, kui see värskendus on juriidilise isiku jaoks lõppenud, ei ole suvand **Luba voo etapikoodid** lehel **Laohalduse parameetrid** enam saadaval.

Kinnitused tehakse värskendamise ajal ja kui värskendus nurjub, kuvatakse tõrketeade. Värskendamine võib nurjuda järgmiste konfliktide tõttu.

- Olemas on topelt vooetapi vabad tekstid.
- Olemas on kohandused.
- Vooetapi vaba tekst, mis on seotud vooetapi meetodi eksemplariga ei vasta oodatud mallitüübile.

Pärast võimalike valideerimise ajal tuvastatud konfliktide lahendamist saate värskendusprotsessi uuesti käivitada.

Kui värskendus on edukas, siis on saadaval leht **Voo etapikoodid** (**Laohaldus \> Seadistus \> Vood \> Voo etapikoodid**). Sellel lehel loetletakse voo etapikoodid, mida värskendati siis, kui voo etapikoodide funktsioon sisse lülitati.

### <a name="create-new-wave-step-codes"></a>Uute voo etapikoodid loomine

Saate kasutada lehte **Voo etapikoodid** voo etapikoodide loomiseks ja kustutamiseks.

Iga uus voo etapikood ja sellega seotud ID peab olema kordumatud kõigi voo etapitüüpide puhul ja need peavad olema määratletud konkreetse voo etapitüübi jaoks.

### <a name="apply-wave-step-codes"></a>Voo etapikoodide rakendamine

Kui olete määranud sobivad voo etapikoodid, saab neid rakendada vooprotsessi meetoditele.

Voo etapikoodide rakendamiseks avage sobiv sihtmall. Siin on sihtmallid, millele ona voo etapikoodid määratud osutama.

- **Täiendamise mallid:** Laohaldus \> Seadistus \> Täiendamine \> Täiendamise mallid
- **Koorma loomise mallid:** Laohaldus \> Seadistus \> Koorem \> Koorma loomise mallid
- **Mallide sorteerimine:** Laohaldus \> Seadistus \> Pakkimine \> Väljaminevad sortimise mallid
- **Konteineritesse panemise mallid:** Laohaldus \> Seadistus \> Konteinerid \> Konteinerite loomise mallid
- **Siltide printimise mallid:** Laohaldus \> Seadistus \> Dokumendi marsruutimine \> Voo sildi mallid

Selle loendi malle rakendatakse, kui need on viidatud voo protsessi meetodist, mis on valitud voo mallis. Kui voo etapikood voo malli voo protsessi meetodis vastb ühe mallitüübi voo etapikoodile, siis mall rakendatakse.

### <a name="sample-scenario"></a>Näidisstsenaarium

Järgmine protseduur aitab tagada, et loodud täiendamise mall rakendub voo mallile.

1. Avage **Laohaldus \> Seadistus \> Vood \> Voo etapikoodid**, ja looge voo etapikood tüübile **Täiendamine**.
2. Avage **Laohaldus \> Seadistus \> Täiendamine \> Täiendamise mallid** ja looge täiendamise mall.
3. Täiendamise mallis valige see voo etapikood, mille lõite tüübile **Täiendamine**.
4. Avage **Laohaldus \> Seadistus \> Vood \> Voo mallid** ja valige see voo mall, mida soovite kasutada.
5. Valige mallis kiirkaardil **Meetodid** meetod **Täiendamine**.
6. Valige väljal **Voo etapikood** see voo etapikood, mille valisite täiendamise mallis.
