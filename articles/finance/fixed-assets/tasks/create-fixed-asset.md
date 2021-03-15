---
title: Uue põhivara loomine
description: Selles teemas selgitatakse, kuidas luua uut põhivara kirjet loendilehel Põhivara.
author: moaamer
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab330c604b2485687544a7d8b3eef3a652fa2069
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985133"
---
# <a name="create-a-fixed-asset"></a>Uue põhivara loomine

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse, kuidas luua uut põhivara kirjet loendilehel **Põhivara**.

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