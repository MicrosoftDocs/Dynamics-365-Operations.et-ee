---
title: Müügi komisjonitasu reeglite seadistamine
description: See protseduur selgitab, kuidas seadistada ja lubada müügi komisjonitasu arvutamist ning jälgimist.
author: omulvad
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionCustomerGroup, CommissionItemGroup, CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, CommissionCalc, InventPosting, CustTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d575e609ac5289f9acb219322c9df93972e5dfc
ms.sourcegitcommit: 25fe679b73663fda6b5b3c32646026d0993a9f00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/12/2019
ms.locfileid: "1995209"
---
# <a name="set-up-sales-commission-rules"></a>Müügi komisjonitasu reeglite seadistamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur selgitab, kuidas seadistada ja lubada müügi komisjonitasu arvutamist ning jälgimist. Samuti selgitab see, kuidas luua nii kliendi kui ka kauba komisjonigruppe ning linkida valitud klient ja toode vastavate gruppidega. Seejärel kasutatakse neid gruppe komisjonitasu arvutamise seadistuses kliendi, kauba ja müügiesindajate kombinatsiooni loomiseks, mis tuleb vastendada müügitellimusega, et anda müügiisikutele õigus komisjonitasu saamiseks. Kliendi ja kauba komisjonitasu gruppide loomine on valikuline, kuna komisjonitasu saab arvutada ka üksiku kliendi ja/või kauba kohta. Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega.


## <a name="set-up-commission-groups-and-commission-rates"></a>Komisjonitasu gruppide ja komisjonitasu määrade seadistamine
1. Avage **Navigeerimispaan > Moodulid > Müük ja turundus > Komisjonitasud > Komisjonitasu kliendigrupid**.
2. Valige suvand **Uus**.
3. Sisestage väärtus väljale **Grupp**.
4. Sisestage väärtus väljale **Nimi**.
5. Valige käsk **Salvesta**.
6. Sulgege leht.
7. Avage **Navigeerimispaan > Moodulid > Müük ja turundus > Komisjonitasud > Kaubagrupid**.
8. Valige suvand **Uus**.
9. Sisestage väärtus väljale **Grupp**.
10. Sisestage väärtus väljale **Nimi**.
11. Valige käsk **Salvesta**.
12. Sulgege leht.
13. Avage **Müük ja turundus > Komisjonitasud > Müügigrupid**.
    - Komisjonitasu müügigrupp määrab töötajad müügiesindaja rollis, kellel on õigus saada komisjonitasu, kui asjakohase müügigrupiga seostatud klient ostab teatud kaupu.  
    - Demoettevõtte USMF andmetes on müügigrupp nimega USA müügiesindajad.  
14. Valige **Toimingupaanil** suvand **Üldine**.
15. Klõpsake suvandit **Müügiesindaja**. Müügiaruande lehel kuvatakse ettevõtte müügiinimesed, kes on seotud kindla komisjonitasu grupiga. Saate määrata mitu müügiesindajat samasse gruppi ja määratleda nende osa lõppkomisjonitasust protsentuaalselt. Komisjonitasu kogumäär kõigi töötajate peale kokku ei tohi olla üle 100. 
16. Märkige loendis valitud rida.
17. Valige suvand **Redigeeri**.
18. Määrake **Komisjonitasu osa** väärtusele „50“.
19. Klõpsake valikut **Uus**.
20. Klõpsake väljal **Nimi** otsingu avamiseks ripploendi nuppu.
21. Kirjete leidmiseks kasutage valikut **Kiirfilter**. Näiteks saate filtreerida välja Nime väärtuse Susan Burk järgi.
22. Klõpsake **Vali**.
23. Määrake **Komisjonitasu osa** väärtusele „50“.
24. Klõpsake valikut **Salvesta**.
25. Avage **Müük ja turundus > Komisjonitasud > Komisjonitasu arvutamine**. Lehel **Komisjonitasu arvutamine** saate määratleda komisjonitasu määra, mille töötaja saab müügikande eest, kui see sisaldab kliendi ja toote eelmääratud kombinatsiooni. Komisjonitasu määra seadistamise osana peate määrama komisjonitasu arvutamise aluse ja selle, kas see peaks sisaldama või välistama allahindlusi. Saate sisestada ka kehtivusperioodi, mille vältel on komisjonitasu määr aktiivne.  
26. Klõpsake valikut **Uus**.
27. Valige väljal **Kaubakood** „Rühm“.
28. Klõpsake väljal **Kauba seos** otsingu avamiseks ripploendi nuppu.
29. Leidke ja valige loendist varem loodud grupp.
30. Valige väljal **Kliendikood** suvand „Grupp“.
31. Klõpsake väljal **Kliendi seos** otsingu avamiseks ripploendi nuppu.
32. Valige loendist varem seadistatud grupp.
33. Väljal **Müügiesindaja seos** klõpsake otsingu avamiseks ripploendi nuppu.
34. Otsige loendist ja valige soovitud kirje.
    - Saate säilitada suvandi Enne rea allahindlust.  
    - Saate säilitada komisjonitasu väärtuse arvutamise alusena suvandi Tulu.    
35. Sisestage arv väljale Komisjonitasu protsent.
36. Klõpsake valikut **Salvesta**.

## <a name="setting-up-commission-posting"></a>Komisjonitasu sisestamise seadistamine
1. Avage **Navigeerimispaan > Moodulid > Müük ja turundus > Komisjonitasud > Komisjonitasu sisestamine**. Komisjonitasud on töötajatele väljamakstavad ja seetõtu tuleb need seadistada, et tagada õige finantssisestus asjakohastele **Pearaamatu** kontodele. Seda tehakse lehel **Komisjonitasu sisestamine**. Vaadake praeguse ettevõtte jaoks saadaolev seadistus üle. Tavaliselt sisestatakse komisjonitasu summad spetsiaalsele kulukontole ja need on spetsiaalse ostureskontro vastaskontod. Kui teil pole komisjonitasu sisestamisreeglid seadistatud, ei saa süsteem õigustatud komisjonitasudega müügitellimuse arveldust lõpule viia.  
2. Sulgege leht.

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a>Kliendile ja tootele komisjonitasu grupi määramine
1. Avage **Navigeerimispaan > Moodulid > Müük ja turundus > Kliendid > Kõik kliendid**.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
4. Klõpsake valikut **Redigeeri**.
5. Laiendage jaotist **Müügitellimuse vaikeandmed**.
6. Klõpsake väljal **Komisjonitasu grupp** otsingu avamiseks ripploendi nuppu.
7. Valige loendist varem loodud grupp.
8. Väljal **Müügigrupp**, klõpsake otsingu avamiseks ripploendi nuppu.
9. Otsige loendist ja valige soovitud kirje.
10. Klõpsake valikut **Salvesta**.
11. Avage **Navigeerimispaan > Moodulid > Tooteteabe haldus > Tooted > Väljastatud tooted**.
12. Kirjete leidmiseks kasutage valikut **Filter**. Näiteks saate filtreerida välja Kaubakood väärtuse T0020 järgi.
13. Klõpsake loendis valitud real olevat linki.
14. Klõpsake valikut **Redigeeri**.
15. Laiendage jaotist **Müük**.
16. Klõpsake väljal **Komisjonitasu grupp** otsingu avamiseks ripploendi nuppu.
17. Valige loendist varem loodud komisjonitasu grupp.
18. Valige käsk **Salvesta**.

