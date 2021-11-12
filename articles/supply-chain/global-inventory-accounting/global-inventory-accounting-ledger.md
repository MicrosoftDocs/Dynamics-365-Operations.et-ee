---
title: Global Inventory Accounting pearaamat
description: Selles teemas kirjeldatakse Global Inventory Accounting pearaamatuid, mis on määratletud valuuta, kalendri, reegli ja juriidilise isikuga seose kombinatsiooniga.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b29bb1aea9e96b5ef39303025cb286f0d1fde12c
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678879"
---
# <a name="global-inventory-accounting-ledger"></a>Global Inventory Accounting pearaamat

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)] <!--KFM: Until 4/30/2022 -->

Global Inventory Accounting laoarvestusel on oma pearaamatute kogum. Iga kord, kui asjaomase juriidilise isiku jaoks töödeldakse varudega seotud kannet, saab süsteem seda kannet vastavalt vajadusele arvestada mis tahes arvuga Global Inventory Accounting pearaamatutes.

Pearaamat on deebet- ja kreeditmõõdikute register. Need meetmed liigitatakse kuluelementide ja alampearaamatu kontode abil. Global Inventory Accounting pearaamat määratletakse valuuta, kalendri, reegli ja juriidilise isikuga seose kombinatsiooniga.

Global Inventory Accounting pearaamatute seadistamiseks minge **Globaalse laoarvestus \>Seadistustamine \>Globaalse laoarvestuse pearaamat**. Määrake igale pearaamatule järgmised väljad.

- **Nimi** – sisestage pearaamatu nimi.
- **Kirjeldus** – sisestage pearaamatu kirjeldus.
- **Rahanduskalender** – määrake pearaamatu rahanduskalender.
- **Valuuta ja vahetuskursi liik** – kasutage selle kiirkaardi välju, et valida pearaamatu kasutatav arvestusvaluuta ja vahetuskursi liik. Valitud valuuta võib erineda valuutast, mida juriidiline isik kasutab. Global Inventory Accounting laoarvestuses saavad kasutajad määratleda suvalise arvu kuluarvestusandmikke. Global Inventory Accounting laoarvestus toetab laoarvestust mitmes valuutas ja mitmes hindamises. Seadistage järgmised väljad.

    - **Valuuta** – valige kuluarvestuse valuuta, milles varudega seotud väärtusi hoitakse. Need väärtused hõlmavad laoväärtust, müüdud kaupade maksumust, transiitvarusid ja igat liiki hälbeid.
    - **Vahetuskursi tüüp** – valige vahetuskurss, mida süsteem peaks kasutama kandesumma ja kaupade standardkulu teisendamiseks kuluarvestuse valuutasse.

- **Reegli nimi** – määrake reegel. Reegel on poliitikate kogum, mis määrab, kuidas kulusid selles pearaamatus arvestatakse.
- **Juriidiline isik** – pearaamat kajastab valitud juriidilisele isikule sisestatud dokumente.
- **Ettevalmistamine** – saate valida, kas enne pearaamatu loomist loodud laokandeid tuleks töödelda vastavalt pearaamatu valuutale ja konventsioonile. Valige üks järgmistest väärtustest.

    - **Aktiveeritud** – pearaamat peaks töötlema kandeid, mis loodi enne pearaamatu loomist.
    - **Deaktiveeritud** – pearaamat peaks töötlema ainult kandeid, mis loodi pärast pearaamatu loomist.

    > [!IMPORTANT]
    > Pärast uute dokumentide sisestamist **ei** saa te tagasi tulla ega seda välja seada.

- **Olek** – süsteem seab vastloodud pearaamatute olekuks automaatselt *Ettevalmistamine*.
