---
title: Ülemineku korrigeerimise töölehe kannete sisestamine jaotisse vara rentimine
description: Selles teemas kirjeldatakse funktsiooni, mis võimaldab teil rendiportfelli üle viia uutele rentimise raamatupidamisstandarditele, raamatupidamisstandardite kodeerimise teemale 842 (ASC 842) ja rahvusvahelise finantsaruandluse standardile 16 (IFRS 16).
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7ed62f52753a6697a7547ada0317041669cf3506
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207201"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a>Ülemineku korrigeerimise töölehe kannete sisestamine jaotisse vara rentimine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse funktsiooni, mis võimaldab teil rendiportfelli üle viia uutele rentimise raamatupidamisstandarditele: raamatupidamise standardite kodeerimise teema 842 (ASC 842), mis on üldtunnustatud raamatupidamispõhimõtete standard USA-s (USA RAAMATUPIDAMISTAVA) ja rahvusvahelise finantsaruandluse Standard 16 (IFRS 16).

Lisateavet selle kohta, kuidas seadistada raamat uuele standardile üleminekuks, leiate teemast [Rendiraamatute seadistamine](set-up-lease-books.md).

Ülemineku korrigeerimise töölehe kirje loomisel luuakse töölehe kirje. See kirje kajastab bilansi mõju sellel kuupäeval rendi uutele standarditele üleviimisele. Vastav vara konto debiteeritakse sellel kuupäeval bilansilise väärtuse summas ja kohustise konto krediteeritakse. Erinevused debiteeritakse või krediteeritakse jaotamata kasumile.

Ülemineku korrigeerimise sisestamiseks uute raamatupidamisstandardite järgi toimige järgmiselt.

1. Valige lehel **Rendi kokkuvõte** rendikirje ja seejärel valige **Raamatud**.
2. Valige raamatust **Maksegraafik**.
3. Valige **Maksegraafiku** dialoogiaknast käsk **Kinnita**. Seejärel sulgege dialoogiboks.
4. Valige **Ülemineku korrigeerimine**.

    > [!NOTE]
    > Ülemineku korrigeerimise saab luua ainult nende rendiraamatute jaoks, mis on määratud raamatule, kus väli **Raamatu üleviimine** on saadaval. Kui väärtus väljal **Rendi algus** on hilisem kui ülemineku kuupäev, uuendata väärtust väljal **Ülemineku korrigeerimine**.

5. Töölehe kirje vaatamiseks valige **Vara rentimise töölehed**.
6. Valige uus tööleht ja seejärel valige käsk **Sisesta**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]