---
title: "Põhivarakannete sisestamine sisestuskihtidele"
description: "See artikkel annab ülevaate sisestamiskihi funktsioonist põhivarakannete puhul."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 2d65dca16cf4ead60c8664066828240c82e58a4f
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="post-fixed-asset-transactions-to-posting-layers"></a>Põhivarakannete sisestamine sisestuskihtidele

[!include[banner](../includes/banner.md)]


See artikkel annab ülevaate sisestamiskihi funktsioonist põhivarakannete puhul.

Põhivara amortiseeritakse sageli mitmel viisil ja eri eesmärkidel. Maksueesmärgil arvutatakse kulum praeguste maksureeglite alusel, et saavutada suurima võimalik maksustuseelne kulum, kuid aruandluseks arvutatakse kulum vastavalt raamatupidamisseadustele ja -standarditele. Eri liiki kulumeid arvutatakse ja kirjendatakse sisestuskihtides ükshaaval.

Iga põhivaraga seotud raamat seadistatakse kindla sisestuskihi jaoks, millel on üldine kulumieesmärk. Sisestuskihte on kümme: praegune, toimingud, maks ja seitse kohandatud kihti. Raamatu puhul saab pearaamatusse sisestamise ka keelata, määrates valiku Sisesta pearaamatusse sätteks Ei. Seejärel seatakse välja Sisestamiskiht väärtuseks automaatselt Puudub. Tavaliselt kasutatakse raamatuid, mis pearaamatusse ei sisesta, maksuaruandluse jaoks. See lähenemine lisab paindlikkust vararegistri varasemate kannete kustutamisel, kuna neid pole pearaamatuga kooskõlastatud.

Põhivara töölehed määratletakse lehel Töölehtede nimed, valides suvandid Pearaamat > Töölehtede seadistus > Töölehtede nimed. Iga tööleht, millele saate kulumeid sisestada, määratletakse töölehe nime alusel ainult ühe sisestuskihi kohta. Töölehe sisestuskihti ei saa muuta. See piirang aitab tagada, et iga sisestuskihi kanded hoitakse eraldi. Iga sisestuskihi kohta peate looma vähemalt ühe töölehe. Kui kasutate raamatuid, mis pearaamatusse ei sisesta, peate looma ka töölehe, milles sisestamiskihi sätteks on määratud Puudub.

Saate määrata põhivarakannete jaoks pearaamatukontosid lehel Põhivara sisestusreeglid. Igale sisestusreeglile tuleb valida vastav kandetüüp ja raamat ning seejärel määrata pearaamatukontod. Saate seadistada sisestusreeglite kirje igale raamatule, mis sisestab pearaamatusse.

> [!NOTE] 
> Tuletatud raamatute kasutamisel saate kandeid sisestada korraga eri sisestuskihtidesse. Looge esmase raamatu kanded töölehel, mille sisestuskiht vastab raamatu sisestuskihile. Sisestamise ajal kantakse tuletatud raamatu kanded vastavatesse sisestuskihtidesse.

Lisateavet vt teemadest [Tuletatud raamatud](derived-books.md) ja [Sisestamine tuletatud raamatute kaudu](post-derived-value-models.md).




