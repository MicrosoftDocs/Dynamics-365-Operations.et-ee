---
title: "Põhivaragruppide asendusväärtuste ja kindlustusväärtuste ümberarvutus"
description: "See artikkel selgitab põhivara asendusväärtuste ja kindlustusväärtuste värskendamist."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3261
ms.assetid: b8876f83-8772-4f2a-b277-12724e2a0c44
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 5ddaaaf166224a74999f3ab0cfa325f7e2e07221
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="recalculate-replacement-costs-and-insured-values-for-fixed-asset-groups"></a>Põhivaragruppide asendusväärtuste ja kindlustusväärtuste ümberarvutus

[!include[banner](../includes/banner.md)]


See artikkel selgitab põhivara asendusväärtuste ja kindlustusväärtuste värskendamist.

Võite saada perioodilisi teateid, et kindlate põhivarade vahetamise või kindlustamise kulu on muutunud. Näiteks võib teie haldur teid teavitada, et viimase aasta inflatsioon oli 3 protsenti, ning seetõttu peate kõigi põhivarade asenduskulusid 3 protsenti tõstma. 

Kuigi saate üksikute põhivarade asenduskulusid ja kindlustusväärtust redigeerida vormil Põhivarad, võite kasutada vormi Värskenda asendusväärtused ja kindlustusväärtused, et värskendada neid väärtusi korraga kogu varade grupile. Selles teemas kirjeldatakse põhivaragruppide või gruppidesse kuuluvate kindlate varade värskendamist.

## <a name="how-values-are-updated"></a> Kuidas väärtusi värskendatakse?
Põhivaragruppide asenduskulude ja kindlustusväärtuse ümberarvutamiseks peate esmalt täpsustama protsenti, mille võrra olemasolevaid asenduskulusid ja kindlustusväärtusi muudetakse, ja seejärel sooritama väärtuste ümberarvutamiseks perioodilise uuenduse. Selleks täpsustage vormil Põhivaragrupid protsente väljadel Asendusväärtuse tegur ja Kindlustusväärtuse tegur. Kuigi täpsustate neid väärtusi põhivaragrupi jaoks, saate vormil Värskenda asendusväärtused ja kindlustusväärtused valida ümberarvutamiseks ainult kindlate gruppi kuuluvate põhivarade asenduskulud ja kindlustusväärtused. 

Kui kasutate varade asenduskulude ja kindlustusväärtuse ümberarvutamiseks vormi Värskenda asendusväärtused ja kindlustusväärtused, kasutatakse järgmisi valemeid.

-   \[(Varade grupi asenduskulu faktor / 100) + 1\] \* varade olemasolev asenduskulu
-   \[(Varade grupi kindlustusväärtuse faktor / 100) + 1\] \* varade olemasolev kindlustusväärtus

> [!NOTE] 
> Kui kasutate vormi Värskenda asendusväärtused ja kindlustusväärtused, värskendatakse nii valitud varade asenduskulu kui ka kindlustusväärtust, te ei saa värskendada üksnes üht väärtust. Ühe väärtuse samaks jätmiseks ja teise värskendamiseks sisestage vormil Põhivaragrupid teguriks 0 (null). Kui tegur on null või tühi, jäetakse arvutus uuendamises vahele. Põhivarade raamatupidamislikku väärtust ja raamatupidamislikku jääkväärtust perioodiline värskendus ei mõjuta. 

## <a name="how-to-use-a-date-to-select-which-items-to-update"></a> Kuidas kasutada kuupäeva värskendatavate kaupade valimisel?
Vaikimisi uuendatakse värskendusprotsessi käigus valitud varasid, mida ei ole antud päeval värskendatud, aga mis võivad olla värskendatud eelmistel päevadel. Näiteks &lt; jooksev kuupäev tähendab „enne tänast”. Saate muuta vormi Värskenda asendusväärtused ja kindlustusväärtused kuupäeva, klõpsates nuppu Vali. Täpsustatud kuupäevakriteeriumit võrreldakse vara viimase perioodilise värskenduse kuupäevaga (väli Viimane perioodiline väärtuse/kulu uuendus vormil Põhivarad). Välja Viimane perioodiline väärtuse/kulu uuendus värskendatakse automaatselt praeguse kuupäevaga iga kord, kui värskendate edukalt põhivara asendus‑ või kindlustusväärtust. 

Näide 

Muutsite sõiduki-, kontorimööbli- ja hoonegruppide asenduskulusid eile 5 protsendi võrra ja nüüd leiate, et need varad on õigesti muudetud. Nende varade tänasesse ülejäänud põhivarade värskendamisse kaasamise vältimiseks sisestage väljale Viimane perioodiline väärtuse/kulu uuendus eilsele eelnev kuupäev (&lt; eilne kuupäev), sest viimane sõiduki, kontorimööbli ja hoonegruppide värskendus sai teoks väljaspool teie sisestatud kuupäevakriteeriumi.

## <a name="cumulative-effect-of-each-update"></a> Iga värskenduse kumulatiivne efekt
Igal värskendusel on kumulatiivne efekt. Seetõttu peaksite värskendusi hoolikalt planeerima. Kui tõstate näiteks kõiki varasid teisipäeval 3% võrra ja siis tõstate kontorimööblit reedel 4%, tõuseb kontorimööbel kokku 7,12 protsenti.

## <a name="scenario"></a>Stsenaarium
Teie haldur teavitab teid põhivarade järgnevaist muutustest:
-   Kõigi põhivarade, v.a arvutite, asenduskulude tõusmine 3,25 protsendi võrra.
-   Kogu kontorimööbli asenduskulude tõus lisaks 1 protsendi võrra.
-   Kõigi arvutite asenduskulude ja kindlustusväärtuse langus 10 protsendi võrra.

Tehke järgmised muudatused.
1.  Sisestage vormil Põhivaragrupid kõigi põhivaragruppide, v.a Kontorimööbli grupp ja Arvutite grupp, väljale Asendusväärtuse tegur väärtus 3,25 ja väljale Kindlustusväärtuse tegur väärtus 0.
2.  Sisestage Kontorimööbli grupi jaoks väljal Asendusväärtuse tegur väärtus 4,25 ja väljal Kindlustusväärtuse tegur väärtus 0.
3.  Sisestage Arvutite grupi jaoks väljal Asendusväärtuse tegur väärtus ‑10 ja väljal Kindlustusväärtuse tegur väärtus ‑10.
4.  Kõigi põhivarade ümberarvutamise sooritamiseks klõpsake vormil Värskenda asendusväärtused ja kindlustusväärtused nuppu OK.

Järgmisel päeval aga teavitab teie juht, et arvutid langesid 10% asemel 8%, seega peate korrigeerima asenduskulusid ja kindlustusväärtust. Vea parandamiseks saate kasutada ühte kahest võimalusest.
-   Redigeerige käsitsi vormil Põhivarad iga Arvutite põhivaragruppi kuuluva põhivara välju Kindlustusväärtus ja Asendusväärtus. Arvutage ja sisestage käsitsi väärtused, nagu oleksite algset summat 8% võrra vähendanud. Selle meetodi puhul ei kasuta te vormi Värskenda asendusväärtused ja kindlustusväärtused.
-   Sisestage vormil Põhivaragrupid Arvutite grupi asenduskulude ja kindlustusväärtuse tegurid väljadele Asendusväärtuse tegur ja Kindlustusväärtuse tegur. See lähtestab varad tagasi algväärtusele (enne 10-protsendilist alanemist) ja rakendab algväärtusele 8-protsendilist alanemist. Seejärel kasutage – olenevalt teguritest, mida peate sisestama, – väärtuste ümberarvutuseks vormi Värskenda asendusväärtused ja kindlustusväärtused.

> [!NOTE]  
> Te ei saa tegurit -10 tagasi võtta positiivse 10 sisestamisega (või teguriga 2, mis on -10 ja -8 vahe), sest summasid ei arvutata nii, nagu soovite. 






