---
title: Vooetapi koodid
description: See artikkel annab ülevaate laine etapikoodidest ja nende kasutamisel.
author: Mirzaab
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveStepCode, WHSReplenishmentTemplates, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4d25f1211db949b38232f945f69f197d5eda9a11
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900473"
---
# <a name="wave-step-codes"></a>Vooetapi koodid

[!include [banner](../includes/banner.md)]

Vooetapi koodid on koodid, mida kasutajad saavad seadistada ja kasutada vastavale mallile konkreetsete juhtumite linkimiseks. Mallid sisaldavad malle täiendamiseks, konteineritesse panemiseks, siltide printimiseks, koormuste loomiseks ja sortimiseks.

Kui voo etapi koode ei kasutata, peavad kasutajad sisestama vaba teksti, et viidata kindlale mallile laine meetodi eksemplarist. Vabal tekstil on kalduvus vigadeks, kuna kasutajad peavad veenduma, et vooetapi tekst, mida nad lisavad konkreetse vooetapi meetodi jaoks voo malli puhul, vastab täpselt sihtmalli tekstile.

Konkreetse vooetapi tüübi vooetapi koodid seadistatakse eraldi lehel. Voomalli iga vooetabi meetodi eksemplari korral, mis vajab vooetapi koodi, tuleb vooetapi kood valida ripploendist. Ripploendi valik asendab vaba tekstisisestuse ja aitab vähendada inimlike vigade riski ja mõju. Seadistuse koode kasutatakse vooetapi meetodi sidumiseks voomallis meetodi sihtmalliga.

> [!NOTE]
> Vooetapi koodide funktsiooni kasutamine on valikuline. See on organisatsiooniüleselt kõigi juriidiliste isikute jaoks lubatud.

## <a name="setup-demo"></a>Häälestuse demo 

Selle demo jaoks peavad olema installitud demo andmed ja peate kasutama testandmete ettevõtet **USMF**.

### <a name="enable-wave-step-codes"></a>Luba vooetapi koodid

Järgige neid samme, et lülitada sisse voo etapi koodide funktsioon.

1. Avage suvand **Funktsioonihaldus**.
2. Valige, et lubada funktsioon nimega **Organisatsiooniülene vooetapi kood**.

Kõik olemasolevad vooetappide vabad tekstid kõikide juriidiliste isikute puhul värskendatakse uuele struktuurile. Pärast seda, kui see värskendus on kõikide juriidiliste isikute jaoks lõpetatud, on see funktsioon lubatud. Kui funktsiooni ei saa ühe või mitme juriidilise isiku puhul lubada, siis pole funktsioon üheski juriidilises isikus lubatud.

Lubamise ajal teostatakse andmete uuendamise ajal kinnitamised. Kui uuendamine ebaõnnestub, kuvatakse tõrketeade. Värskendamine võib nurjuda järgmiste konfliktide tõttu.

- Olemas on topelt vooetapi vabad tekstid.
- Olemas on kohandused.
- Vooetapi vaba tekst, mis on seotud vooetapi meetodi eksemplariga ei vasta oodatud mallitüübile.

Pärast võimalike kinnitamise ajal tuvastatud konfliktide lahendamist saate proovida funktsiooni uuesti lubada.

Kui funktsioon on lubatud, siis muutub leht **Voo etapikoodid** (**Laohaldus \> Seadistus \> Vood \> Voo etapikoodid**) kättesaadavaks. Sellel lehel loetletakse voo etapikoodid, mida värskendati siis, kui organisatsiooniülene voo etapikoodide funktsioon lubati.

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

Sooritate need sammud iga juriidilise isiku puhul.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]