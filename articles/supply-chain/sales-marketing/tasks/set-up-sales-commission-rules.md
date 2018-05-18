--- 
title: "Müügi komisjonitasu reeglite seadistamine"
description: "See protseduur selgitab, kuidas seadistada ja lubada müügi komisjonitasu arvutamist ning jälgimist."
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8e7d2198b4976a6f60f05690d7b6f11f3da55e28
ms.openlocfilehash: 3d5c38b1f07803242350fe016b45c45d49c0b59b
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---
# <a name="set-up-sales-commission-rules"></a>Müügi komisjonitasu reeglite seadistamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur selgitab, kuidas seadistada ja lubada müügi komisjonitasu arvutamist ning jälgimist. Samuti selgitab see, kuidas luua nii kliendi kui ka kauba komisjonigruppe ning linkida valitud klient ja toode vastavate gruppidega. Seejärel kasutatakse neid gruppe komisjonitasu arvutamise seadistuses kliendi, kauba ja müügiesindajate kombinatsiooni loomiseks, mis tuleb vastendada müügitellimusega, et anda müügiisikutele õigus komisjonitasu saamiseks. Kliendi ja kauba komisjonitasu gruppide loomine on valikuline, kuna komisjonitasu saab arvutada ka üksiku kliendi ja/või kauba kohta. Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega.


## <a name="set-up-commission-groups-and-commission-rates"></a>Komisjonitasu gruppide ja komisjonitasu määrade seadistamine
1. Tehke valik Müük ja turundus > Komisjonitasud > Komisjonitasu kliendigrupid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Grupp.
4. Sisestage väärtus väljale Nimi.
5. Klõpsake nuppu Salvesta.
6. Sulgege leht.
7. Tehke valik Müük ja turundus > Komisjonitasud > Kaubagrupid.
8. Klõpsake valikut Uus.
9. Sisestage väärtus väljale Grupp.
10. Sisestage väärtus väljale Nimi.
11. Sulgege leht.
12. Tehke valik Müük ja turundus > Komisjonitasud > Müügigrupid.
    * Komisjonitasu müügigrupp määrab töötajad müügiesindaja rollis, kellel on õigus saada komisjonitasu, kui asjakohase müügigrupiga seostatud klient ostab teatud kaupu.  
    * Demoettevõtte USMF andmetes on müügigrupp nimega USA müügiesindajad.  
13. Klõpsake toimingupaanil valikut Üldine.
14. Klõpsake valikut Müügiesindaja.
    * Müügiaruande lehel kuvatakse ettevõtte müügiinimesed, kes on seotud kindla komisjonitasu grupiga. Saate määrata mitu müügiesindajat samasse gruppi ja määratleda nende osa lõppkomisjonitasust protsentuaalselt. Komisjonitasu kogumäär kõigi töötajate peale kokku ei tohi olla üle 100.  
15. Märkige loendis valitud rida.
16. Klõpsake nuppu Redigeeri.
17. Määrake komisjonitasu osaks 50.
18. Klõpsake valikut Uus.
19. Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.
20. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks saate filtreerida välja Nime väärtuse Susan Burk järgi.
21. Klõpsake Vali.
22. Määrake komisjonitasu osaks 50.
23. Klõpsake nuppu Salvesta.
24. Tehke valik Müük ja turundus > Komisjonitasud > Komisjonitasu arvutamine.
    * Komisjonitasu arvutamise lehel saate määratleda komisjonitasu määra, mille töötaja saab müügikande eest, kui see sisaldab kliendi ja toote eelmääratud kombinatsiooni. Komisjonitasu määra seadistamise osana peate määrama komisjonitasu arvutamise aluse ja selle, kas see peaks sisaldama või välistama allahindlusi. Saate sisestada ka kehtivusperioodi, mille vältel on komisjonitasu määr aktiivne.  
25. Klõpsake valikut Uus.
26. Valige väljalt Kaubakood suvand Grupp.
27. Klõpsake väljal Kauba seos otsingu avamiseks ripploendi nuppu.
28. Leidke ja valige loendist varem loodud grupp.
29. Klõpsake loendis valitud real olevat linki.
30. Valige väljal Kliendikood suvand Grupp.
31. Klõpsake väljal Kliendi seos otsingu avamiseks ripploendi nuppu.
32. Valige loendist varem seadistatud grupp.
33. Väljal Müügiesindaja seos klõpsake otsingu avamiseks ripploendi nuppu.
34. Otsige loendist ja valige soovitud kirje.
    * Saate säilitada suvandi Enne rea allahindlust.  
    * Saate säilitada komisjonitasu väärtuse arvutamise alusena suvandi Tulu.    
35. Sisestage arv väljale Komisjonitasu protsent.
36. Klõpsake nuppu Salvesta.

## <a name="setting-up-commission-posting"></a>Komisjonitasu sisestamise seadistamine
1. Tehke valik Müük ja turundus > Komisjonitasud > Komisjonitasu sisestamine.
    * Komisjonitasud on töötajatele väljamakstavad ja seetõtu tuleb need seadistada, et tagada õige finantssisestus asjakohastele pearaamatu kontodele. Seda tehakse komisjonitasu sisestamise lehel. Vaadake praeguse ettevõtte jaoks saadaolev seadistus üle. Tavaliselt sisestatakse komisjonitasu summad spetsiaalsele kulukontole ja need on spetsiaalse ostureskontro vastaskontod. Kui teil pole komisjonitasu sisestamisreeglid seadistatud, ei saa süsteem õigustatud komisjonitasudega müügitellimuse arveldust lõpule viia.  
2. Sulgege leht.

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a>Kliendile ja tootele komisjonitasu grupi määramine
1. Tehke valik Müük ja turundus > Kliendid > Kõik kliendid.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
4. Klõpsake nuppu Redigeeri.
5. Laiendage jaotist Müügitellimuse vaikeandmed.
6. Klõpsake väljal Komisjonitasu grupp otsingu avamiseks ripploendi nuppu.
7. Valige loendist varem loodud grupp.
8. Klõpsake väljal Müügigrupp otsingu avamiseks ripploendi nuppu.
9. Otsige loendist ja valige soovitud kirje.
10. Klõpsake nuppu Salvesta.
11. Avage Tooteteabe haldus > Tooted > Väljastatud tooted.
12. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks saate filtreerida välja Kaubakood väärtuse T0020 järgi.
13. Klõpsake loendis valitud real olevat linki.
14. Klõpsake nuppu Redigeeri.
15. Laiendage jaotist Müük.
16. Klõpsake väljal Komisjonitasu grupp otsingu avamiseks ripploendi nuppu.
17. Valige loendist varem loodud komisjonitasu grupp.


