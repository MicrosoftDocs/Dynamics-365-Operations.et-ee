---
title: "Põhivarakandeid sisestuskihtidele"
description: "See artikkel annab ülevaate sisestamiskihi funktsioonist põhivarakannete puhul."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 4b112eee303604149c7609972a60c2014d4be423
ms.lasthandoff: 03/31/2017


---

# <a name="post-fixed-asset-transactions-to-posting-layers"></a>Põhivarakandeid sisestuskihtidele

See artikkel annab ülevaate sisestamiskihi funktsioonist põhivarakannete puhul.

Põhivara amortiseeritakse sageli mitmel viisil ja eri eesmärkidel. Maksueesmärgil arvutatakse kulum praeguste maksureeglite alusel, et saavutada suurima võimalik maksustuseelne kulum, kuid aruandluseks arvutatakse kulum vastavalt raamatupidamisseadustele ja -standarditele. Eri liiki kulumeid arvutatakse ja kirjendatakse sisestuskihtides ükshaaval.

Iga põhivaraga seotud raamat seadistatakse kindla sisestuskihi jaoks, millel on üldine kulumieesmärk. Sisestuskihte on kümme: praegune, toimingud, maks ja seitse kohandatud kihti. Raamatu puhul saab pearaamatusse sisestamise ka keelata, määrates valiku Sisesta pearaamatusse sätteks Ei. Seejärel seatakse välja Sisestamiskiht väärtuseks automaatselt Puudub. Tavaliselt kasutatakse maksuaruandluseks raamatuid, et ära Postita pearaamatusse. Selline lähenemine kaudu saate täiendavaid kustutada ajalooliste kannete saamiseks, sest nad ei ole pühendunud pearaamatu.

Põhivara töölehed määratletakse lehel Töölehtede nimed, valides suvandid Pearaamat > Töölehtede seadistus > Töölehtede nimed. Iga tööleht, millele saate kulumeid sisestada, määratletakse töölehe nime alusel ainult ühe sisestuskihi kohta. Töölehe sisestamiskihi ei saa muuta. See piirang aitab tagada, et iga sisestuskihi kanded hoitakse eraldi. Iga sisestuskihi kohta peate looma vähemalt ühe töölehe. Kasutamisel raamatuid, et ära Postita pearaamatusse, peate looma ka töölehe, kus sisestamiskihi sätteks pole.

Saate määrata põhivarakannete jaoks pearaamatukontosid lehel Põhivara sisestusreeglid. Igale sisestusreeglile tuleb valida vastav kandetüüp ja raamat ning seejärel määrata pearaamatukontod. Saate seadistada sisestusreeglite kirje igale raamatule, mis sisestab pearaamatusse.

> [!NOTE] 
> Tuletatud raamatute abil saate konteerida korraga eri sisestuskihtidesse tehingute samal ajal. Looge esmase raamatu kanded töölehel, mille sisestuskiht vastab raamatu sisestuskihile. Sisestamise ajal kantakse tuletatud raamatu kanded vastavatesse sisestuskihtidesse.

Lisateabe saamiseks vaadake teemat [saadud raamatud](derived-books.md) ja [sisestamine tuletatud raamatud](post-derived-value-models.md).


