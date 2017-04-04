---
title: Auditipoliitika rikkumised ja juhtumid
description: "Artiklis selgitatakse, kuidas auditi poliitikareeglite rikkumistest auditijuhtumeid luuakse. See sisaldab ka teavet erinevate viiside kohta, kuidas auditireeglite kasutavad dokumendi valimise kuupäevavahemikku."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: ecd32549b6067ed4c1211996e846e210f77f5013
ms.openlocfilehash: 77f72c9414f1fad720055e58e3f704b9c713072f
ms.lasthandoff: 03/31/2017


---

# <a name="audit-policy-violations-and-cases"></a>Auditipoliitika rikkumised ja juhtumid

Artiklis selgitatakse, kuidas auditi poliitikareeglite rikkumistest auditijuhtumeid luuakse. See sisaldab ka teavet erinevate viiside kohta, kuidas auditireeglite kasutavad dokumendi valimise kuupäevavahemikku.

<a name="how-audit-cases-are-generated"></a>Auditijuhtumite loomine
-----------------------------

Auditipoliitikaid kasutatakse kuluaruannete, ostutellimuste ja hankija arvete tuvastamiseks, mis ei ole kooskõlas ärireeglitega, mille määratlete ja konfigureerite auditipoliitika reeglitena. 

Auditipoliitikaid käitatakse pakktöötlusrežiimis. Auditipoliitika käitamisel käivitatakse samal ajal kõik sellesse poliitikasse kuuluvad poliitikareeglid.

Iga poliitika reegel hindab dokumentide kogumit. Poliitika reegel valib dokumendid, mis on dokumendi valiku kuupäevavahemikus ja mis ühtivad määratud kriteeriumidega. Näiteks võib üks poliitika reegel valida kuluaruanded, milles on menüüd, mis ületavad 50,00. Teine poliitika reegel võib valida hankija arved, mis tuleb tasuda kindlale hankijale. Iga kogumis valitud dokumendi puhul luuakse rikkumine. See rikkumine on kirje selle kohta, et konkreetne dokument, nt arve 12345, ei ole poliitika reegliga kooskõlas. 

Mitme auditi rikkumise kirjed on grupeeritud kokku ja seostatakse auditijuhtumitega. Vaikimisi grupeeritakse iga auditipoliitika juhtumid auditipoliitika reegli järgi. Soovi korral saate valida muud grupeerimiskriteeriumid, kasutades lehte **Juhtumite grupeerimise kriteeriumid**. Näiteks saate rühmitada kulu päised projekti ID ja hankija arve makselehed kontode kaupa. Sel juhul jaotatakse kõik kulud päise rikkumisi, mis on sama projekti ID samas asjas ja kõik sama hankija hankija arved on paigutatud samas asjas. 

> [!NOTE]
> Auditi poliitika eeskirjad, mis põhinevad on **dubleerida** Päringutüüp, rikkumised ei ole grupeeritud juhendi või kriteeriume, mis on ära toodud selle **juhtum grupeerimiskriteeriumid** lehel. Selle asemel grupeeritakse need auditipoliitika reeglisse integreeritud kriteeriumide alusel. Näiteks kui poliitika reegel hindab kuluaruandeid sama summa, kaupmehe ID ja kuupäeva dubleeritud kulude puhul, on kõik kulud, millel on neil väljadel samad väärtused, üks juhtum. Kõik kulud, millel on erinevad väärtused, on eraldi juhtum.

Pärast auditi juhtumite loomist käsitsetakse neid juhtumihalduse tüüpiliste protsesside abil.

## <a name="document-selection-date-ranges"></a>Dokumendi valiku kuupäevavahemikud
Auditi poliitika käitamisel valib iga poliitika reegel määratud tüüpi dokumendid, millel on dokumendi valiku kuupäevavahemiku kuupäev. Dokumendivaliku kuupäevavahemik määratletakse lehel **Lisavalikud**. Mitme dokumendiga on seostatud rohkem kui üks kuupäev. Auditipoliitika reegli kasutatav kuupäeva väli on määratletud lehel **Poliitika reegli tüüp**.

Järgmiselt on toodud muud moodused, mil auditi poliitika dokumendi valiku kuupäevavahemikku kasutab.

-   Poliitika kasutab iga poliitika reegli versiooni, mis kehtib dokumendi valiku kuupäevavahemiku viimasel päeval. Saate vaadata iga poliitika reegli kehtivuse kuupäevi loendilehel **Auditipoliitikad**.
-   Poliitika kasutab organisatsiooni sõlmi, mis on seostatud poliitikaga dokumendi valiku kuupäevavahemiku viimasel päeval. Loendilehel **Auditipoliitikad** kuvatakse ainult organisatsiooni sõlmed, mis on praegu poliitikaga seostatud.
-   Poliitika reeglite puhul, mis põhinevad päringu tüübil **loendiotsing**, hindab poliitika dokumente jälgitavate üksuste osas, mis jõustuvad dokumendi valiku kuupäevavahemiku viimasel päeval.


Lisateabe saamiseks vaadake [auditi üldeeskirjad](audit-policy-rules.md)


