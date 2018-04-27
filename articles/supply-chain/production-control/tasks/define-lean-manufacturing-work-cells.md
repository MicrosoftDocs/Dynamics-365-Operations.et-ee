--- 
title: "Töörakkude määratlemine: lean manufacturing"
description: "Töörakk on konkreetne ressursigruppide vorm, mida saab lean manufacturingi protsessi tegevustes kasutada."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f060f084baab055a51e390f488ca2553bd997b92
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---
# <a name="define-lean-manufacturing-work-cells"></a>Töörakkude määratlemine: lean manufacturing

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Töörakk on konkreetne ressursigruppide vorm, mida saab lean manufacturingi protsessi tegevustes kasutada. Töörakkudel on sisestus- ja väljastuskohad ning võimsuse määratlus, mis põhineb tootmisvoo mudelil. Lisateavet lean manufacturingi töörakkude ja läbilaskvuse arvutuste kohta leiate lean manufacturingi tehnilistest ülevaadetest. Selle protseduuri loomiseks kasutati demoettevõtte USMF andmeid


## <a name="create-a-work-cell"></a>Looge töörakk. 
1. Avage Organisatsiooni haldus > Ressursid > Ressursigrupid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Ressursigrupp.
    * Tööraku ID on tavaliselt süsteemikood ja see peab juriidilise isiku puhul kordumatu olema.  
4. Sisestage väljale Kirjeldus soovitud väärtus.
    * Kirjeldus sisaldab tööraku nime või tiitlit.  
5. Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.
    * Töörakk asub ühes konkreetses asukohas. Nii sisestus- kui ka väljastusladu ja asukoht peavad olema selles kohas.  
6. Klõpsake loendis valitud real olevat linki.
7. Klõpsake väljal Tootmisüksus otsingu avamiseks ripploendi nuppu.
8. Klõpsake loendis valitud real olevat linki.
    * Valige tootmisüksus, mille juurde see töörakk kuulub.  
9. Märkige ruut Töörakk.
    * Ressursigrupi kasutamiseks säästliku töörakuna tuleb märkida ruut Töörakk.  Pange tähele, et seda atribuuti ei saa muuta pärast ressursigrupi loomist.  
10. Klõpsake väljal Sisestusladu otsingu avamiseks ripploendi nuppu.
11. Klõpsake loendis valitud real olevat linki.
    * Raamatupidamise ja materjali juhtimise jaoks paigutatakse tööde juhtimise moodulisse koondatud kaup tavaliselt konkreetsesse virtuaalsesse lattu. Kuid kui soovite asukohti täiendada, kasutades laotööd, peavad need kuuluma vastuvõtva toorainelao juurde.  
12. Klõpsake väljal Sisestuskoht otsingu avamiseks ripploendi nuppu.
13. Klõpsake loendis valitud real olevat linki.
    * Pange tähele, et protsessitegevuse puhul saab sisestuskoha üldise või konkreetse toote või tootevariandiga üle kirjutada, määratledes komplekteerimistegevused, mis viivad protsessitegevuseni. Tööraku sisestuskohad ei tohi olla litsentsiplaadiga juhitavad.  
14. Klõpsake väljal Väljastusladu otsingu avamiseks ripploendi nuppu.
15. Otsige loendist ja valige soovitud kirje.
    * Mitme tegevusega tootmisvoogude või tootmisliinide puhul on see sageli järgmise tööraku sisestusladu või müügi- või transiitladu, kuhu toode tavaliselt pärast tootmisprotsessi viiakse. Pidage meeles, et lean manufacturingi protsesside mudeli koostamisel on transport tavaliselt raiskamine, nagu ka transpordiaruandlus.  
16. Klõpsake loendis valitud real olevat linki.
17. Klõpsake väljal Väljastuskoht otsingu avamiseks ripploendi nuppu.
    * Mitme protsessitegevusega tootmisvoo puhul on see sageli järgmise tööraku sisestuskoht.  
18. Otsige loendist ja valige soovitud kirje.
19. Klõpsake loendis valitud real olevat linki.
20. Laiendage või ahendage jaotist Toiming.
    * Säästlike kanban-tööde kuluarvestuse ja töötlemise võimaldamiseks tuleb esitada käitusaja kategooria.  
21. Klõpsake väljal Käitusaja kategooria otsingu avamiseks ripploendi nuppu.
22. Otsige loendist ja valige soovitud kirje.
    * Käitusaja kulukategooriat kasutatakse standardses kuluarvestuses ja omahinna tagasiarvestuses.  
23. Klõpsake loendis valitud real olevat linki.
24. Laiendage või ahendage jaotist Kalendrid.
25. Klõpsake vahekaarti Lisa.
26. Klõpsake väljal Kalender otsingu avamiseks ripploendi nuppu.
27. Otsige loendist ja valige soovitud kirje.
    * Tavaliselt kasutavad ühe tegevuskoha töörakud ühte tööajakalendrit. Kui töörakkudel saavad olla eraldi tööajad, võib olla vaja koostada töörakule konkreetne tööajakalender. Pange tähele, et kalendrile peab olema määratletud standardne tööaeg, kui seda kasutatakse säästliku tööraku jaoks, kuna võimsuse määratlus on tavaliselt seotud tööpäeva standardse tööajaga.  
28. Klõpsake loendis valitud real olevat linki.
29. Laiendage või ahendage jaotist Tööraku võimsus.
30. Klõpsake vahekaarti Lisa.
31. Klõpsake väljal Tootmisvoo mudel otsingu avamiseks ripploendi nuppu.
32. Otsige loendist ja valige soovitud kirje.
    * See protseduur nõuab tootmisvoo mudeli tüüpi Läbilaskevõime, et näidata läbilaskevõime määratlust.  
33. Klõpsake loendis valitud real olevat linki.
34. Valige suvand väljalt Võimsuse periood.
    * Suvandid on järgmised. Standardne tööpäev – võimsust väljendatakse tööraku tööaja kalendri standardse tööpäeva pikkusega. Iga päeva puhul määratakse tegelik tööaeg kalendri järgi ja kehtiv saadaolev võimsus arvutatakse selle põhjal.   Nädal – võimaldab iganädalast võimsust. Tegeliku tööajaga korrigeerimist ei toimu.   Kuu – lubab igakuist võimsust. Tegeliku võimsusega korrigeerimist ei toimu.   Tavaliselt kasutatakse standardset tööpäeva igapäevaste perioodide ja iganädalast võimsust iganädalaste võimsuseperioodide puhul.  
35. Sisestage number väljale Keskmine läbilaskekogus.
    * Pange tähele, et säästlikku tööd ei seadistata ideaalses keskkonnas kunagi maksimaalse võimsusega. Selle asemel tuleb võimsus määratleda alati tavapärastes oludes toimuvate tegevuste jaoks.  
36. Klõpsake väljal Ühik otsingu avamiseks ripploendi nuppu.
37. Klõpsake loendis valitud real olevat linki.
38. Ühiku toiming ResolveChanges.

## <a name="add-a-financial-dimension"></a>Finantsdimensiooni lisamine
1. Laiendage või ahendage jaotist Finantsdimensioonid.
    * Pange tähele, et tootmisvoole määratletud finantsdimensioonid alistavad antud tööraku finantsdimensiooni.    Valitavad finantsdimensioonid olenevad teie süsteemi finantsdimensioonide konfiguratsioonist. Järgmised sammud vastavad demoettevõtte USMF andmetele. Erinevate andmete kasutamisel ei pruugi need toimingud kehtida.  
2. Klõpsake väljal CostCenter otsingu avamiseks ripploendi nuppu.
3. Otsige loendist ja valige soovitud kirje.
    * Säästlike töörakkude puhul valitavad dimensioonid sõltuvad finantsdimensioonide rakendamisest konkreetse juriidilise isiku arvestusmudelis.  
4. Klõpsake loendis valitud real olevat linki.
5. Klõpsake väljal ItemGroup otsingu avamiseks ripploendi nuppu.
6. Otsige loendist ja valige soovitud kirje.
7. Klõpsake loendis valitud real olevat linki.

## <a name="save"></a>Salvesta
1. Klõpsake nuppu Salvesta.


