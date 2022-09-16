---
title: Töötaja päise juhtelement
description: See artikkel annab teavet personalistava päise juhtelemendi kohta töötajate iseteeninduskeskuses Inimesed ja Microsofti lehel Töötaja Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2867a952df79161aaee657dbc3df1f3298294dd5
ms.sourcegitcommit: 167f73a834629752c6b79c312d744e52df7f0927
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445987"
---
# <a name="worker-header-control"></a>Töötaja päise juhtelement

Microsoft Dynamics 365 Human Resources pakub personalistavat päise juhtelementi **Töötaja iseteeninduses**, **Inimeste** keskuses ja sujuval töötaja **lehel**. Päis sisaldab põhiteavet töötaja kohta ning ühe klõpsuga tegevusi (nt e-kirjastamine, kutsumine või sõnumside). Päise saab muuta, eemaldades väljad või lisades väljad, k.a kohandatud väljad, et näidata lisateavet. Uue päise juhtelemendi kasutamiseks minge funktsioonihalduse **ja lubage** töötaja **päise juhtelemendi** funktsioon.

## <a name="personalization"></a>Isikupärastamine

Üks töötaja päise juhtelemendi põhieelist on võime isikupärastada päises kuvatavat teavet.

Päise ülemises parempoolses jaotises on grupp kolmel väljal, mis näitavad erinevaid andmeid, sõltuvalt töötaja olekust. Seda väljagruppi nimetatakse päise punktiakna osaks. Saate isikupärastada päise punktiakna osa, eemaldades praegused väljad või lisades välju. Väljad, mida saab lisada Punktilampi osasse **päise** juhtelemendis, erinevad töötajate iseteeninduse, **inimeste** keskuse ja töötaja **lehe** jaoks.

## <a name="employee-self-service"></a>Töövõtja iseteenindus

Töötaja iseteeninduslehe **töötaja päis** sisaldab järgmist teavet:

- Töötaja nimi
- Personalinumber
- Positsiooni tiitel
- Osakonnad
- Töötaja tüüp
- Tööle juriidiline isik
- Töötamise aastad
- Aruanded (juhataja)
- Positsiooni tüüp

Päis sisaldab ka ühe klõpsuga tegevust isiku isikuandmete redigeerimiseks. Isikliku **teabe lehe** avamiseks töötaja iseteeninduses **valige** suvand **Redigeeri isiklikke üksikasju**.

## <a name="people-hub"></a>Inimeste keskus

Töötajate päis inimeste **keskuses** (tööruumi **lehekülg** Inimesed) sisaldab järgmist teavet:

- Töötaja nimi
- Personalinumber
- Positsiooni tiitel
- Osakonnad
- Töötaja tüüp
- Tööle juriidiline isik
- Töötamise aastad
- Aruanded (juhataja)
- Positsiooni tüüp

Päis sisaldab ka ühe klõpsuga tegevusi (nt meilid, kutsumine või sõnumside). Kui kasutaja vaatab oma teavet inimeste tööruumi lehel, **sisaldab** **ühe klõpsuga toiming nuppu Isiklike** andmete redigeerimine. Kasutaja saab selle nupu valida, et avada isikliku **teabe lehekülg** Töötaja **iseteeninduses**.

## <a name="streamlined-worker-page"></a>Sujuvamaks töötajaleht

Sujuval töötaja lehel olevas **töötaja päises** on järgmine teave:

- Töötaja nimi
- Personalinumber
- Positsiooni tiitel
- Osakonnad
- Töötaja tüüp
- Tööle juriidiline isik

Sõltuvalt töötaja olekust võivad päise andmed muutuda. Näiteks kui töötaja on ettevõttest väljunud, **sisaldab päise juhtelement väljutud** pääsmeid, töösuhte lõppkuupäeva ja lõpetamise põhjust.

Allolevas tabelis kuvatakse päises erinevate töötajaolekute kohta kuvatavad andmed.

| Töövõtja olek | Kuvatavad andmed | Märkus |
|-----------------|--------------------|------|
| Ootel | <ul><li>Nimi</li><li>Personalinumber</li><li>Positsiooni tiitel</li><li>Osakond</li><li>Töötaja tüüp</li><li>Juriidiline isik</li><li>Ootel märk</li><li>Alguskuupäev</li><li>Aruannete sihtkoht:</li><li>Positsiooni tüüp</li></ul> | |
| Viimati palgatud | <ul><li>Nimi</li><li>Personalinumber</li><li>Positsiooni tiitel</li><li>Osakond</li><li>Töötaja tüüp</li><li>Juriidiline isik</li><li>Hiljutise palkamise märk</li><li>Töötamise aastad</li><li>Aruannete sihtkoht:</li><li>Positsiooni tüüp</li></ul> | Vaikimisi kuvatakse viimase **7** päeva jooksul palgatud töötajate hiljutine palkamise märk. Selle sätte muutmiseks **sisestage** **·** **ajaraami lehekülje Inimressursside parameetrid vahekaardi Üldine jaotises Hiljutised palkamised.** Näiteks viimase **14** **päeva jooksul palgatud töötajate hiljutise palkamise vaatamiseks seadke välja Periood** **väärtuseks 14** **ja** välja Ühiku väärtuseks **Päevad**. |
| Aktiivne töötaja | <ul><li>Nimi</li><li>Personalinumber</li><li>Positsiooni tiitel</li><li>Osakond</li><li>Töötaja tüüp</li><li>Juriidiline isik</li><li>Alguskuupäev</li><li>Aruannete sihtkoht:</li><li>Positsiooni tüüp</li></ul> | |
| Lahkumine | <ul><li>Nimi</li><li>Personalinumber</li><li>Positsiooni tiitel</li><li>Osakond</li><li>Töötaja tüüp</li><li>Juriidiline isik</li><li>Pääsmest väljumine</li><li>Töötamise aastad</li><li>Aruannete sihtkoht:</li><li>Positsiooni tüüp</li></ul> | Vaikimisi kuvatakse väljumispääs **töötajate** puhul, kes lahkuvad järgmise seitsme päeva jooksul. Selle sätte muutmiseks **sisestage** **·** **inimressursside parameetrite lehele vahekaardil Üldine jaotises Töötaja** kuupäevavahemikust väljumine ajaraam. Näiteks selleks, et **vaadata** väljumispääse järgmise 14 päeva jooksul lahkuva töötaja kohta, **·** **seadke välja Periood väärtuseks 14** **ja ühiku välja väärtuseks** Päevad.**·** |
| Lahkunud | <ul><li>Väljutud pääsmest</li><li>Personalinumber</li><li>Töösuhte lõppkuupäev</li><li>Põhjuse kood</li></ul> | Vaikimisi kuvatakse lahkumispääs **töötajate puhul,** kes on viimase 7 päeva jooksul jäänud. Selle sätte muutmiseks **sisestage** **·** **inimressursside parameetrite lehel vahekaardil Üldine jaotisesSe Väljutud** töötajad ajavahemik ajaraam. Näiteks viimase **14** **·** **päeva jooksul jäänud töötajate välja Väljutud pääsme vaatamiseks seadke välja Periood väärtuseks 14** **ja** välja Ühik väärtuseks **Päevad**. |
