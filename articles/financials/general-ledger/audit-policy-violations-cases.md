---
title: Auditipoliitika rikkumised ja juhtumid
description: Artiklis selgitatakse, kuidas auditi poliitikareeglite rikkumistest auditijuhtumeid luuakse. See sisaldab ka teavet erinevate viiside kohta, kuidas auditireeglite kasutavad dokumendi valimise kuupäevavahemikku.
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3ed72f829ca4060fe0a4c03b6d4a47a98cdebd6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568820"
---
# <a name="audit-policy-violations-and-cases"></a>Auditipoliitika rikkumised ja juhtumid

[!include [banner](../includes/banner.md)]

Artiklis selgitatakse, kuidas auditi poliitikareeglite rikkumistest auditijuhtumeid luuakse. See sisaldab ka teavet erinevate viiside kohta, kuidas auditireeglite kasutavad dokumendi valimise kuupäevavahemikku.

<a name="how-audit-cases-are-generated"></a>Auditijuhtumite loomine
-----------------------------

Auditipoliitikaid kasutatakse kuluaruannete, ostutellimuste ja hankija arvete tuvastamiseks, mis ei ole kooskõlas ärireeglitega, mille määratlete ja konfigureerite auditipoliitika reeglitena. 

Auditipoliitikaid käitatakse pakktöötlusrežiimis. Auditipoliitika käitamisel käivitatakse samal ajal kõik sellesse poliitikasse kuuluvad poliitikareeglid.

Iga poliitika reegel hindab dokumentide kogumit. Poliitika reegel valib dokumendid, mis on dokumendi valiku kuupäevavahemikus ja mis ühtivad määratud kriteeriumidega. Näiteks võib üks poliitika reegel valida kuluaruanded, milles on menüüd, mis ületavad 50,00. Teine poliitika reegel võib valida hankija arved, mis tuleb tasuda kindlale hankijale. Iga kogumis valitud dokumendi puhul luuakse rikkumine. See rikkumine on kirje selle kohta, et konkreetne dokument, nt arve 12345, ei ole poliitika reegliga kooskõlas. 

Mitme auditi rikkumise kirjed on grupeeritud kokku ja seostatakse auditijuhtumitega. Vaikimisi grupeeritakse iga auditipoliitika juhtumid auditipoliitika reegli järgi. Soovi korral saate valida muud grupeerimiskriteeriumid, kasutades lehte **Juhtumite grupeerimise kriteeriumid**. Näiteks saate grupeerida kulupäiseid projekti ID ja hankija arveid hankija konto järgi. Sel juhul grupeeritakse kõik sama projekti ID-ga kulu päise rikkumised samasse juhtumisse ja samasse juhtumisse grupeeritakse ka kõik sama hankija kontoga hankija arved. 

> [!NOTE]
> Auditipoliitika reeglite puhul, mis põhinevad päringu tüübil **Duplikaat**, ei grupeerita rikkumisi poliitika reegli või kriteeriumide järgi, mis on määratud lehel **Juhtumite grupeerimise kriteeriumid**. Selle asemel grupeeritakse need auditipoliitika reeglisse integreeritud kriteeriumide alusel. Näiteks kui poliitika reegel hindab kuluaruandeid sama summa, kaupmehe ID ja kuupäeva dubleeritud kulude puhul, on kõik kulud, millel on neil väljadel samad väärtused, üks juhtum. Kõik kulud, millel on erinevad väärtused, on eraldi juhtum.

Pärast auditi juhtumite loomist käsitsetakse neid juhtumihalduse tüüpiliste protsesside abil.

## <a name="document-selection-date-ranges"></a>Dokumendi valiku kuupäevavahemikud
Auditi poliitika käitamisel valib iga poliitika reegel määratud tüüpi dokumendid, millel on dokumendi valiku kuupäevavahemiku kuupäev. Dokumendivaliku kuupäevavahemik määratletakse lehel **Lisavalikud**. Mitme dokumendiga on seostatud rohkem kui üks kuupäev. Auditipoliitika reegli kasutatav kuupäeva väli on määratletud lehel **Poliitika reegli tüüp**.

Järgmiselt on toodud muud moodused, mil auditi poliitika dokumendi valiku kuupäevavahemikku kasutab.

-   Poliitika kasutab iga poliitika reegli versiooni, mis kehtib dokumendi valiku kuupäevavahemiku viimasel päeval. Saate vaadata iga poliitika reegli kehtivuse kuupäevi loendilehel **Auditipoliitikad**.
-   Poliitika kasutab organisatsiooni sõlmi, mis on seostatud poliitikaga dokumendi valiku kuupäevavahemiku viimasel päeval. Loendilehel **Auditipoliitikad** kuvatakse ainult organisatsiooni sõlmed, mis on praegu poliitikaga seostatud.
-   Poliitika reeglite puhul, mis põhinevad päringu tüübil **loendiotsing**, hindab poliitika dokumente jälgitavate üksuste osas, mis jõustuvad dokumendi valiku kuupäevavahemiku viimasel päeval.


Lisateavet vt teemast [Auditipoliitika reeglid](audit-policy-rules.md)



