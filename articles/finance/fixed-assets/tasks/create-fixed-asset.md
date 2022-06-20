---
title: Uue põhivara loomine
description: See artikkel selgitab, kuidas luua põhivara loendilehelt uus põhivara kirje.
author: moaamer
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 00c72081d20015737aa027cee9474a54e498cef4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868485"
---
# <a name="create-a-fixed-asset"></a>Uue põhivara loomine

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas luua põhivara loendilehelt **uus põhivara** kirje.

Süsteem määrab vara numbri põhivara grupile määratud numbriseeria põhjal. Kui kasutate põhivara malli varade importimiseks Microsoft Exceli lisandmooduli kaudu või kui kasutate mõnda muud imporditööd, loob süsteem automaatselt põhivara kirjed ja suurendab vara numbrit.

Vara kirje käsitsi loomiseks toimige järgmiselt.

1. Avage **Navigeerimispaan \> Moodulid \> Põhivarad \> Põhivarad \> Põhivarad**.
2. Valige **Toimingupaanil** suvand **Uus**.
3. Väljale **Põhivara grupp** sisestage või valige väärtus. Väli **Arv** on vaikimisi, kui olete lubanud valikud **Nummerda põhivarade funktsioonid automaatselt**, **Põhivarade parameetrid** ja **Põhivara grupp**. Kui te seda teinud pole, sisestage põhivara tuvastamiseks kordumatu number.
4. Sisestage väärtus väljale **Nimi**. Sisestage lisateave, mida teie ettevõte selle vara puhul vajab.
5. Valige **Toimingupaanil** suvand **Raamatud**.
6. Väljale **Soetamiskuupäev** sisestage kuupäev.
7. Väljale **Soetusmaksumus** sisestage arv.

    - Sisestage lisateave, mida teie ettevõte selle raamatu puhul vajab.
    - Sisestage täiendav teave, mida teie ettevõte ülejäänud raamatute jaoks vajab.

8. Sulgege leht.

Põhivarasid saate importida ka Exceli lisandmooduli abil või käivitades imporditöö tööruumis **Andmehaldus**. Enne impordi käivitamist sisestage malli nõutavate väljade väärtused.

Kui te ei määratlenud põhivara numbrit Exceli lisandmooduli mallis või tööruumis Andmehaldus, loob süsteem iga imporditud vara jaoks põhivara numbri ja suurendab automaatselt iga üksuse numbriseeriat. Kuid kui impordite varad ja määratlete varade numbrid mallis, **ei** suurenda süsteem numbriseeriat automaatselt. Sellisel juhul peab administraator numbriseeriat käsitsi uuendama. Kui määratlete põhivara numbri Exceli lisandmooduli mallis, kasutab süsteem määratletud põhivara numbrit ja suurendab numbriseeriat.

> [!NOTE]                                                                                                         
> Pärast kulumi sisestamist väljad **Teenusesse saadetud** ja **Amortiseerimise algus** lukustatakse lehel **Raamat**. Samuti ei uuendata kumbagi välja andmeüksusest.

> [!WARNING]
> Põhivara kirjet ei kustutata, kui kanded sisestati seotud raamatusse või kui vastloodud põhivara sisestatakse töölehe reale, kuid ei sisestata. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
